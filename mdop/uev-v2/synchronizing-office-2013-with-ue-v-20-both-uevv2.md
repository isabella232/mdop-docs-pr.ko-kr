---
title: Office 2013를 UE-V 2.0와 동기화
description: Office 2013를 UE-V 2.0와 동기화
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826888"
---
# Office 2013를 UE-V 2.0와 동기화


Microsoft UE-V (User Experience Virtualization) 2.0는 UE-V 서식 파일 갤러리에서 제공 하는 서식 파일을 사용 하 여 Microsoft Office 2013 응용 프로그램 설정의 동기화를 지원 합니다. UE-V 2 및 App-v 5.0 SP2의 Office 2013 Professional Plus 지원의 조합으로 UE-V를 사용 하는 모든 장치 또는 가상화 된 데스크톱의 가상화 된 Office 2013 인스턴스에서 동일한 환경을 사용할 수 있습니다.

Office 2013의 UE-V 응용 프로그램 설정 지원을 활성화 하려면 [MICROSOFT ue-v (User Experience Virtualization) 2 서식 파일 갤러리](https://go.microsoft.com/fwlink/p/?LinkId=246589)에서 공식 ue-v Office 2013 서식 파일을 다운로드할 수 있습니다. 이 리소스는 Microsoft에서 제작한 UE-V 설정 위치 서식 파일 및 커뮤니티 개발 설정 위치 서식 파일을 제공 합니다.

## UE-V의 Microsoft Office 지원


UE-V 1.0 및 UE-V 2에는 Microsoft Office 2010에 대 한 설정 위치 서식 파일이 포함 되어 있습니다. 이러한 템플릿은 UE-V 에이전트 설치 프로세스의 일부로 배포 및 등록 됩니다. 이러한 서식 파일은 장치 간에 사용자의 Office 환경을 동기화 하는 데 도움이 됩니다. Office 2013의 UE-V 서식 파일은 Office 2010의 서식 파일과 매우 유사한 설정 환경을 제공 합니다. Office 365 환경에서 roamed Microsoft Office 2013 설정은 이러한 설정에 포함 되지 않습니다. Office 365 특정 설정 목록은 [office 2013의 사용자 및 로밍 설정 개요](https://go.microsoft.com/fwlink/p/?LinkId=391220)를 참조 하세요.

## Office 2013 설정 동기화


다음 표에는 UE-V의 Office 2013 지원에 대 한 세부 정보가 포함 되어 있습니다.

### Microsoft Office 용 지원 되는 UE-V 서식 파일

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Office 2013 서식 파일 (ue-v in-V 갤러리에서 사용 가능한 UE-V 2.0):</th>
<th align="left">Office 2010 서식 파일 (UE-V 1.0 &amp; 1.0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### UE-V 템플릿에서 지원 되는 Microsoft Office 응용 프로그램

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Microsoft Office 업로드 관리자</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Office 2013 서식 파일 배포


다음 메서드를 사용 하 여 UE-V 설정 위치 템플릿을 배포할 수 있습니다.

-   **PowerShell을 통해 템플릿을 등록**합니다. Windows PowerShell을 사용 하 여 컴퓨터를 관리 하는 경우 다음 Windows PowerShell 명령을 관리자 권한으로 열기를 실행 하 여이 설정 위치 서식 파일을 등록 합니다.

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    UE-V 및 Windows PowerShell을 사용 하는 방법에 대 한 자세한 내용은 [Windows PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿 관리](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)를 참조 하세요.

-   **서식 파일 카탈로그 경로를 통해 서식 파일을 등록**합니다. 설정 서식 파일 카탈로그 경로를 사용 하 여 사용자 컴퓨터에서 서식 파일을 관리 하는 경우 Office 2013 서식 파일을 UE-V 에이전트에 정의 된 폴더에 복사 합니다. 다음에 템플릿 자동 업데이트 (ApplySettingsCatalog.exe) 예약 된 작업이 실행 될 때 설정 위치 템플릿이 장치에 등록 됩니다. 자세한 내용은 [ue-v 2 용 설정 서식 파일 카탈로그 배포](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)를 참조 하세요.

-   **Configuration Manager를 통해 서식 파일을 등록**합니다. Configuration Manager를 사용 하 여 UE-V 설정 저장소 템플릿을 관리 하는 경우 템플릿 기준선 CAB을 다시 만들고 구성 관리자로 가져온 다음 기준을 클라이언트에 배포 합니다. 자세한 내용은 [Microsoft 사용자 환경 가상화 2의 System Center 2012 구성 팩](https://go.microsoft.com/fwlink/?LinkId=317263)에 대 한 설명서에서 제공 하는 지침을 참조 하세요.






 

 





