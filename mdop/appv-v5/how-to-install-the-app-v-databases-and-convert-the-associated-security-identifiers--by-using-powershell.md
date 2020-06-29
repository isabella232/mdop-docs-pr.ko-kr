---
title: App-v 데이터베이스를 설치 하 고 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환 하는 방법
description: App-v 데이터베이스를 설치 하 고 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환 하는 방법
author: dansimp
ms.assetid: 9399342b-1ea7-41df-b988-33e302f9debe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb4ff48a532d4c9ec7035421c6e8e7dcd41f5214
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814044"
---
# App-v 데이터베이스를 설치 하 고 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환 하는 방법


SQL 스크립트를 실행할 때 Microsoft SQL Server에서 사용 하는 표준 형식과 16 진수 형식에서 AD DS (Active Directory 도메인 서비스) 사용자 또는 컴퓨터 계정의 수를 모두 형식으로 변환 하려면 다음 PowerShell 프로시저를 사용 합니다.

이 절차를 시도 하기 전에 다음 목록에 표시 된 정보 및 예제를 읽고 이해 해야 합니다.

-   **. 입력** -SID 형식으로 변환 하는 데 사용 되는 계정이 나 계정입니다. 단일 계정 이름 또는 계정 이름 배열이 될 수 있습니다.

-   **. 출력** -표준 및 16 진수 형식의 해당 SID를 사용 하는 계정 이름 목록

-   **예제의** -

    **.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | 서식-목록을**표시 합니다.

    **$accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "DOMAIN \ _user \ _account2")**

    **$AccountsArray .\\ConvertToSID.ps1 | 쓰기-출력 FilePath .\\SIDs.txt 너비 200**

    \#&gt;

**AD DS (Active Directory 도메인 서비스) 사용자 또는 컴퓨터 계정의 수를 형식이 지정 된 Sid (보안 식별자)로 변환 하려면**

1. 다음 스크립트를 텍스트 편집기로 복사 하 고 PowerShell 스크립트 파일 (예: **ConvertToSIDs.ps1**)로 저장 합니다.

2. PowerShell 콘솔을 열려면 **시작** 을 클릭 하 고 **powershell**을 입력 합니다. **Windows PowerShell**을 마우스 오른쪽 단추로 클릭하고 **관리자 권한으로 실행**을 선택합니다.

   ```powershell
   <#
   .SYNOPSIS
   This PowerShell script will take an array of account names and try to convert each of them to the corresponding SID in standard and hexadecimal formats.

   .DESCRIPTION
   This is a PowerShell script that converts any number of Active Directory (AD) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by SQL server when running SQL scripts.

   .INPUTS
   The account(s) to convert to SID format. This can be a single account name or an array of account names. Please see examples below.

   .OUTPUTS
   A list of account names with the corresponding SID in standard and hexadecimal formats

   .EXAMPLE
   .\ConvertToSID.ps1 DOMAIN\user_account1 DOMAIN\machine_account1$ DOMAIN\user_account2 | Format-List

   .EXAMPLE
   $accountsArray = @("DOMAIN\user_account1", "DOMAIN\machine_account1$", "DOMAIN_user_account2")

   .\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\SIDs.txt -Width 200
   #>

   function ConvertSIDToHexFormat
   {
      param([System.Security.Principal.SecurityIdentifier]$sidToConvert)

      $sb = New-Object System.Text.StringBuilder

      [int] $binLength = $sidToConvert.BinaryLength

      [Byte[]] $byteArray = New-Object Byte[] $binLength

      $sidToConvert.GetBinaryForm($byteArray, 0)

      foreach($byte in $byteArray)
      {
          $sb.Append($byte.ToString("X2")) |Out-Null
      }
      return $sb.ToString()
   }

   [string[]]$myArgs = $args



   if(($myArgs.Length -lt 1) -or ($myArgs[0].CompareTo("/?") -eq 0))
   {
       [string]::Format("{0}====== Description ======{0}{0}" +
                  "  Converts any number of user or machine account names to string and hexadecimal SIDs.{0}" +
                  "  Pass the account(s) as space separated command line parameters. (For example 'ConvertToSID.exe DOMAIN\\Account1 DOMAIN\\Account2 ...'){0}" +
                  "  The output is written to the console in the format 'Account name    SID as string   SID as hexadecimal'{0}" +
                  "  And can be written out to a file using standard PowerShell redirection{0}" +
                  "  Please specify user accounts in the format 'DOMAIN\username'{0}" +
                  "  Please specify machine accounts in the format 'DOMAIN\machinename$'{0}" +
                  "  For more help content, please run 'Get-Help ConvertToSID.ps1'{0}" +
                  "{0}====== Arguments ======{0}" +



                  "{0}  /?    Show this help message", [Environment]::NewLine)
   }
   else
   {
       #If an array was passed in, try to split it
       if($myArgs.Length -eq 1)
       {
           $myArgs = $myArgs.Split(' ')
       }

       #Parse the arguments for account names
       foreach($accountName in $myArgs)
       {
           [string[]] $splitString = $accountName.Split('\')  # We're looking for the format "DOMAIN\Account" so anything that does not match, we reject

           if($splitString.Length -ne 2)
           {
               $message = [string]::Format("{0} is not a valid account name. Expected format 'Domain\username' for user accounts or 'DOMAIN\machinename$' for machine accounts.", $accountName)

               Write-Error -Message $message
               continue
           }

           #Convert any account names to SIDs
           try
           {
               [System.Security.Principal.NTAccount] $account = New-Object System.Security.Principal.NTAccount($splitString[0], $splitString[1])

               [System.Security.Principal.SecurityIdentifier] $SID = [System.Security.Principal.SecurityIdentifier]($account.Translate([System.Security.Principal.SecurityIdentifier]))
           }
           catch [System.Security.Principal.IdentityNotMappedException]
           {
               $message = [string]::Format("Failed to translate account object '{0}' to a SID. Please verify that this is a valid user or machine account.", $account.ToString())

               Write-Error -Message $message

               continue
           }

           #Convert regular SID to binary format used by SQL

           $hexSIDString = ConvertSIDToHexFormat $SID

           $SIDs = New-Object PSObject

           $SIDs | Add-Member NoteProperty Account $accountName

           $SIDs | Add-Member NoteProperty SID $SID.ToString()

           $SIDs | Add-Member NoteProperty Hexadecimal $hexSIDString

           Write-Output $SIDs
       }
   }
   ```

3. 인수로 변환할 계정을 전달 하는이 절차의 1 단계에서 저장 한 스크립트를 실행 합니다.

   예를 들면

   **.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-List "또는" $accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "DOMAIN \ _user \ _account2")**

   **$AccountsArray .\\ConvertToSID.ps1 | 쓰기-출력 FilePath .\\SIDs.txt 너비 200 "**

   **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[PowerShell을 사용하여 App-V 관리](administering-app-v-by-using-powershell.md)
