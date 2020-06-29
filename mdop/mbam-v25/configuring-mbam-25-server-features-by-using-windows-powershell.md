---
title: Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성
description: Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822838"
---
# Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성


MBAM 2.5 서버 소프트웨어를 설치한 후에는 Windows PowerShell cmdlet 또는 MBAM 서버 구성 마법사를 사용 하 여 MBAM 2.5 서버 기능을 구성할 수 있습니다. 이 항목에서는 Windows PowerShell cmdlet을 사용 하 여 MBAM 2.5를 구성 하는 방법에 대해 설명 합니다. 대신 마법사를 사용 하려면 [MBAM 2.5 서버 기능 구성을](configuring-the-mbam-25-server-features.md)참조 하세요.

## 이 항목의 내용


이 항목에는 Windows PowerShell을 사용 하 여 MBAM 구성에 대 한 다음 정보가 포함 됩니다.

-   [MBAM 2.5에 대 한 Windows PowerShell 도움말을 로드 하는 방법](#bkmk-load-posh-help)

-   [MBAM Windows PowerShell cmdlet에 대 한 도움말을 가져오는 방법](#bkmk-help-specific-cmdlet)

-   [Windows PowerShell을 사용 하는 경우에만 수행할 수 있는 구성 및 MBAM 서버 구성 마법사를 사용 하는 경우](#bkmk-config-only-posh)

-   [Windows PowerShell을 사용 하 여 MBAM 서버 기능을 구성 하기 위한 필수 구성 요소 및 요구 사항](#bkmk-prereqs-posh-mbamsvr)

-   [Windows PowerShell을 사용 하 여 원격 컴퓨터에 MBAM 구성](#bkmk-remote-config)

-   [필수 계정 및 해당 Windows PowerShell cmdlet 매개 변수](#bkmk-reqd-posh-accts)

MBAM을 관리 하는 데 사용 되는 **MbamBitLockerRecoveryKey** 및 **Get-MbamTPMOwnerPassword** windows powershell cmdlet에 대 한 자세한 내용은 [Windows powershell을 사용 하 여 mbam 2.5 관리](using-windows-powershell-to-administer-mbam-25.md)를 참조 하세요.

## <a href="" id="bkmk-load-posh-help"></a>MBAM 2.5에 대 한 Windows PowerShell 도움말을 로드 하는 방법


TechNet의 Windows PowerShell cmdlet 목록은 [Windows powershell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화](https://go.microsoft.com/fwlink/?LinkId=392816)를 참조 하세요.

**MBAM 서버 소프트웨어를 설치한 후 Windows PowerShell cmdlet에 대 한 MBAM 2.5 도움말을 로드 하려면**

1.  Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.

2.  Type **Update-도움말-Microsoft * MBAM**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>MBAM Windows PowerShell cmdlet에 대 한 도움말을 가져오는 방법


MBAM에 대 한 Windows PowerShell 도움말은 다음 형식으로 제공 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows PowerShell 도움말 형식</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows PowerShell 명령 프롬프트에서 <strong> get-help </strong> &lt; <em> cmdlet을 입력 합니다.</em>&gt;</p></td>
<td align="left"><p>최신 Windows PowerShell cmdlet을 업로드 하려면, MBAM에 대 한 Windows PowerShell 도움말을 로드 하는 방법에 대 한 이전 섹션의 지침을 따릅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 페이지로 TechNet에서</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>다운로드 센터에서 Word .docx 파일로</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>.Pdf 파일로 다운로드 센터에서</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Windows PowerShell을 사용 하는 경우에만 수행할 수 있는 구성 및 MBAM 서버 구성 마법사를 사용 하는 경우


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows PowerShell을 사용 하 여 수행할 수 있는 구성</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>웹 응용 프로그램에서 웹 서비스를 별도의 컴퓨터에 설치 합니다.</p></td>
<td align="left"><p>마법사를 사용 하 여 웹 서비스와 웹 응용 프로그램을 같은 컴퓨터에 설치 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>모든 Configuration Manager 개체를 설치 하지 않고 별도의 보고 서비스에 대 한 보고서를 사용 하도록 설정 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager에서 모든 개체를 삭제 합니다.</p></td>
<td align="left"><p>에서 개체를 삭제 하면 구성 관리자에서 모든 준수 데이터가 삭제 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>데이터베이스에 대 한 사용자 지정 연결 문자열을 입력 합니다.</p></td>
<td align="left"><p>예: 미러링 작업을 수행 하도록 웹 응용 프로그램을 구성 하려면 <strong> Enable-MbamWebApplication cmdlet을 사용 하 여 </strong> 연결 문자열에 적절 한 장애 조치 파트너 구문을 지정 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>필수 구성 요소 검사에 실패 한 경우에도 유효성 검사를 건너뛰고 기능을 구성 합니다.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**참고**  Windows PowerShell cmdlet 또는 MBAM 서버 구성 마법사를 사용 하 여 MBAM 데이터베이스를 사용 하지 않도록 설정할 수 없습니다. 준수 및 감사 데이터가 실수로 제거 되는 것을 방지 하기 위해 데이터베이스 관리자는 데이터베이스를 수동으로 제거 해야 합니다.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Windows PowerShell을 사용 하 여 MBAM 서버 기능을 구성 하기 위한 필수 구성 요소 및 요구 사항


구성을 시작 하기 전에 다음 필수 구성 요소를 완료 합니다.

**계정 관련 필수 조건**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보 또는 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>필요한 계정을 만듭니다.</p></td>
<td align="left"><p><strong> </strong> 이 항목의 뒷부분에 나오는 필수 계정 및 해당 Windows PowerShell cmdlet 매개 변수 섹션을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell cmdlet에 매개 변수로 전달 하는 사용자 계정 및 그룹은 도메인에서 유효한 계정 이어야 합니다.</p></td>
<td align="left"><p>로컬 계정은 사용할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>하위 수준 형식으로 계정을 지정 합니다.</p></td>
<td align="left"><p>예제:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**사용 권한 관련 필수 조건**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보 또는 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 기능을 구성 하는 로컬 컴퓨터의 관리자 여야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>관리자 권한 Windows PowerShell 명령 프롬프트를 사용 하 여 모든 Windows PowerShell cmdlet을 실행 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>사용-MbamDatabase cmdlet에 </strong> 만 해당 됩니다.</p>
<p>&quot; &quot; 대상 Microsoft SQL Server 데이터베이스의 인스턴스에 대 한 데이터베이스 사용 권한을 만들어야 합니다.</p>
<p>이 사용자 계정은 로컬 관리자 그룹에 속해 있거나, MBAM 볼륨 섀도 복사본 서비스 (VSS) 기록기를 등록 하는 Backup Operators 그룹의 일부 여야 합니다.</p></td>
<td align="left"><p>기본적으로 데이터베이스 관리자 또는 시스템 관리자는 필요한 &quot; 모든 데이터베이스 권한을 만들어야 합니다 &quot; .</p>
<p></p>
<p>VSS 기록기에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> 볼륨 섀도 복사본 서비스를 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>System Center Configuration Manager 통합 기능에 </strong> 만 해당:</p>
<p>이 기능을 사용 하도록 설정 하는 사용자에 게는 구성 관리자에서 다음 권한이 있어야 합니다.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration Manager의 권한 유형</th>
<th align="left">필요한 권한</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration Manager 사이트 권한:</p></td>
<td align="left"><p>- Read</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 수집 권한:</p></td>
<td align="left"><p>- 만들기-삭제-읽기-변경-배포 구성 항목</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 구성 항목 권한:</p></td>
<td align="left"><p>- 만들기-삭제-읽기</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Windows PowerShell을 사용 하 여 원격 컴퓨터에 MBAM 구성


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>이 접근 권한 값을 사용 하는 경우</strong></p></td>
<td align="left"><p>원격 컴퓨터에서 MBAM 2.5 서버 기능을 구성 하려는 경우 Windows PowerShell cmdlet이 한 컴퓨터에서 실행 되 고 있으며 다른 원격 컴퓨터에서 기능을 구성 하 고 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>수행 해야 할 작업</strong></p></td>
<td align="left"><p>Windows PowerShell을 사용 하 여 원격 컴퓨터에서 MBAM 2.5 서버 기능을 구성 하려면 다음을 수행 해야 합니다.</p>
<ul>
<li><p>MBAM 2.5 서버 소프트웨어가 원격 컴퓨터에 설치 되어 있는지 확인 합니다.</p></li>
<li><p>CredSSP (자격 증명 보안 지원 공급자) 프로토콜을 사용 하 여 Windows PowerShell 세션을 엽니다.</p></li>
<li><p>WinRM (Windows Remote Management)을 사용 하도록 설정 합니다. WinRM을 사용 하도록 설정 하는 데 실패 하 고 올바르게 구성 하는 경우 <strong> </strong> 이 표에 설명 된 새 PSSession cmdlet에 오류가 표시 되 고 문제를 해결 하는 방법에 대 한 설명이 나와 있습니다. WinRM에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> Windows Remote Management 사용을 참조 하세요 </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>수행 해야 하는 이유</strong></p></td>
<td align="left"><p>이 프로토콜은 사용자의 관리 자격 증명을 사용 하 여 Windows PowerShell cmdlet이 Active Directory 도메인 서비스에 연결할 수 있도록 합니다. 이 프로토콜을 사용 하지 않고 Windows PowerShell 세션을 시작 하는 경우 유효성 검사 오류가 나타날 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>CredSSP 프로토콜을 사용 하 여 Windows PowerShell 세션을 시작 하는 방법</strong></p></td>
<td align="left"><p>Windows PowerShell 프롬프트에서 다음 코드를 입력 합니다.</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>다음 코드에서는 예를 보여 줍니다.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>필수 계정 및 해당 Windows PowerShell cmdlet 매개 변수


다음 표에서는 MBAM 2.5 서버 기능을 구성 하는 데 필요한 계정에 대해 설명 합니다. 또한 구성 중에 계정을 지정 해야 하는 해당 Windows PowerShell cmdlet 및 매개 변수도 나열 합니다.

Cmdlet 매개 변수 형식 (사용자 또는 그룹) 설명-MBAMDatabase 사용

AccessAccount

사용자 또는 그룹

이 데이터베이스의 데이터 및 보고서에 대 한 액세스 권한을 웹 응용 프로그램에 제공 하기 위해이 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹을 지정 합니다. 값이 도메인 사용자 인 경우 **Enable-MbamWebApplication** cmdlet을 실행 하는 데 사용 되는 **Webserviceapplicationpoolcredential** 매개 변수는 동일한 사용자 계정을 사용 해야 합니다. 값이 도메인 사용자 그룹인 경우 **Webserviceapplicationpoolcredential** 매개 변수에서 사용 하는 도메인 계정이이 그룹의 구성원 이어야 합니다.

ReportAccount

사용자 또는 그룹

이 데이터베이스에 대 한 읽기 전용 권한이 있는 도메인 사용자 또는 사용자 그룹을 지정 하 여 정책 준수 및 감사 데이터에 대 한 MBAM 보고서 액세스를 제공 합니다. 값이 도메인 사용자 이면 **Enable-MbamReport** Cmdlet의 **ComplianceAndAuditDBCredential** 매개 변수는 동일한 사용자 계정을 사용 해야 합니다. 값이 도메인 사용자 그룹인 경우 **ComplianceAndAuditDBCredential** 매개 변수에 사용 되는 도메인 계정이이 그룹의 구성원 이어야 합니다.

사용-MbamReport

ComplianceAndAuditDBCredential

사용자

로컬 SSRS 인스턴스가 MBAM 준수 및 감사 데이터베이스에 연결 하는 데 사용 하는 관리 자격 증명을 지정 합니다. 관리 자격 증명의 도메인 사용자는 **Enable-MbamDatabase** cmdlet을 실행 하는 동안 사용 되는 **reportaccount** 매개 변수에 사용 되는 사용자 계정과 동일 해야 합니다. Domain Users 그룹을 **Reportaccount** 매개 변수와 함께 사용 하는 경우이 계정은 해당 그룹의 구성원 이어야 합니다.

**중요**  관리 자격 증명에 지정 된 계정에는 보안이 향상 되는 사용자 권한이 제한 되어 있어야 합니다. 또한 계정의 암호가 만료 되지 않도록 설정 되어 있어야 합니다.

 

ReportsReadOnlyAccessGroup

Group

보고서에 대 한 읽기 권한이 있는 도메인 사용자 그룹을 지정 합니다. 지정 된 그룹은 **Enable-MbamWebApplication** Cmdlet의 **ReportsReadOnlyAccessGroup** 매개 변수에 사용 되는 그룹과 동일 해야 합니다.

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Group

보고서 영역을 제외한 관리 및 모니터링 웹 사이트의 모든 영역에 액세스할 수 있는 도메인 사용자 그룹을 지정 합니다.

HelpdeskAccessGroup

Group

관리 및 모니터링 웹 사이트의 **TPM 관리** 및 **드라이브 복구** 영역에 대 한 액세스 권한이 있는 도메인 사용자 그룹을 지정 합니다.

ReportsReadOnlyAccessGroup

Group

관리 및 모니터링 웹 사이트의 **보고서** 영역에 대 한 읽기 권한이 있는 domain Users 그룹을 지정 합니다. 지정 된 그룹은 **Enable-MbamReport** Cmdlet의 **ReportsReadOnlyAccessGroup** 매개 변수에 사용 되는 그룹과 동일 해야 합니다.

WebServiceApplicationPoolCredential

사용자

이 (가) MBAM 웹 응용 프로그램에 사용할 도메인 사용자를 지정 합니다. 이 계정은 **Enable-MbamDatabase** Cmdlet의 **accessaccount** 매개 변수에 지정 된 것과 동일한 도메인 사용자 계정 이어야 합니다. **사용-MbamDatabase** cmdlet을 실행할 때 **accessaccount** 매개 변수에서 도메인 사용자 그룹을 사용 하는 경우 여기에 지정 된 도메인 사용자는 해당 그룹의 구성원 이어야 합니다. 관리 자격 증명을 지정 하지 않으면 이전에 사용 하도록 설정 된 웹 응용 프로그램에서 지정한 관리 자격 증명이 사용 됩니다. 모든 웹 응용 프로그램에서 동일한 응용 프로그램 풀 id를 사용 합니다. 여러 번 지정 된 경우에는 가장 최근에 지정 된 값이 사용 됩니다.

**중요**  보안 향상을 위해 관리 자격 증명에 지정 된 계정을 제한 된 사용자 권한으로 설정 합니다. 또한 계정 암호가 만료 되지 않도록 설정 합니다. 기본 제공 IIS \ _IUSRS 계정 또는 **Webserviceapplicationpoolcredential** 매개 변수에 사용 되는 계정이 인증 로컬 보안 설정 **이후에 클라이언트 가장** 에 추가 되어 있는지 확인 합니다.

로컬 보안 설정을 보려면 **로컬 보안 정책 편집기**를 열고, **로컬 정책** 노드를 확장 하 고, **사용자 권한 할당** 노드를 선택한 다음 **인증 후 클라이언트로 가장** 을 두 번 클릭 하 고 세부 정보 창에서 **일괄 작업으로 로그온** 그룹 정책 설정을 사용 합니다.

 

 




## 관련 항목


[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)

[MBAM 2.5 서버 기능 구성의 유효성 검사](validating-the-mbam-25-server-feature-configuration.md)

[Windows PowerShell을 사용하여 MBAM 2.5 관리](using-windows-powershell-to-administer-mbam-25.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





