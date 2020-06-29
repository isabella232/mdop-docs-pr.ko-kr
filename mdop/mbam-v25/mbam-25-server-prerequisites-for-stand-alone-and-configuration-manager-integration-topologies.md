---
title: 독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소
description: 독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825998"
---
# 독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소


Microsoft BitLocker 관리 및 모니터링 (MBAM) 설치를 시작 하기 전에이 항목에 나열 된 전제 조건을 완료 해야 합니다. 이러한 전제 조건은 MBAM 독립 실행형 토폴로지와 System Center Configuration Manager 통합 토폴로지에 적용 됩니다.

System Center Configuration Manager를 사용 하 여 MBAM을 배포 하는 경우에는 [구성 관리자 통합 토폴로지에만 적용 되는 mbam 2.5 서버 필수 구성](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)요소에 나열 된 추가 전제 조건을 완료 해야 합니다.

MBAM에 대해 지원 되는 하드웨어 및 운영 체제 목록은 [mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.

**중요**  
MBAM 없이 BitLocker를 사용 하는 경우 드라이브를 해독 한 다음 services.msc를 사용 하 여 TPM을 지워야 합니다. MBAM 클라이언트 PC가 이미 암호화 되어 있고 TPM 소유자 암호가 생성 된 경우 TPM의 소유권을 가질 수 없습니다.



## 필수 MBAM 역할 및 계정


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AD DS (Active Directory 도메인 서비스)에서 만든 그룹</p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">이 그룹 및 계정에 대 한 설명은 MBAM 2.5 그룹 및 계정에 대 한 계획을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



## 복구 데이터베이스에 대 한 필수 조건


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 SQL Server 버전</p></td>
<td align="left"><p>SQL_Latin1_General_CP1_CI_AS 데이터 정렬을 사용 하 여 Microsoft SQL Server를 설치 합니다.</p>
<p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>필요한 SQL Server 권한</p></td>
<td align="left"><p>필요한 권한:</p>
<ul>
<li><p>SQL Server 인스턴스 로그인 서버 역할:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>SQL Server Reporting Services 인스턴스 권한:</p>
<ul>
<li><p>폴더 만들기</p></li>
<li><p>보고서 게시</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>선택 사항-SQL Server에서 사용할 수 있는 TDE (투명 데이터 암호화) 기능을 설치 합니다.</p></td>
<td align="left"><p>TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에 적용 되는 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 합니다. 즉, SQL Server 데이터베이스에서 복구 키 정보를 보고 있고 해당 데이터베이스에 대 한 사용 권한이 있는 계정으로 로그온 한 경우 복구 키 정보가 표시 됩니다. TDE에 대 한 자세한 내용은 <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> mbam 2.5 보안 고려 사항을 참조 </a> 하세요.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 데이터베이스 엔진 서비스</p></td>
<td align="left"><p>MBAM 서버 설치 중에 SQL Server 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>Windows PowerShell을 사용 하 여 원격 컴퓨터에서 데이터베이스를 구성 하는 경우 windows PowerShell을 복구 데이터베이스 서버에 설치할 필요가 없습니다.</p></td>
</tr>
</tbody>
</table>



## 준수 및 감사 데이터베이스에 대 한 필수 조건


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 SQL Server 버전</p></td>
<td align="left"><p>SQL_Latin1_General_CP1_CI_AS 데이터 정렬을 사용 하 여 SQL Server를 설치 합니다.</p>
<p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>필요한 SQL Server 권한</p></td>
<td align="left"><p>필요한 권한:</p>
<ul>
<li><p>SQL Server 인스턴스 로그인 서버 역할:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>SQL Server Reporting Services 인스턴스 권한:</p>
<ul>
<li><p>폴더 만들기</p></li>
<li><p>보고서 게시</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>선택 사항-SQL Server에 TDE (투명 데이터 암호화) 기능 설치</p></td>
<td align="left"><p>TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에 적용 되는 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</p>
<p>TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 합니다. 즉, SQL Server 데이터베이스에서 복구 키 정보를 보고 있고 해당 데이터베이스에 대 한 사용 권한이 있는 계정으로 로그온 한 경우 복구 키 정보가 표시 됩니다. TDE에 대 한 자세한 내용은 <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> mbam 2.5 보안 고려 사항을 참조 </a> 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 데이터베이스 엔진 서비스</p></td>
<td align="left"><p>MBAM 서버 설치 중에 SQL Server 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다. 그러나 SQL Server는 원격으로 실행할 수 있습니다. MBAM 서버 소프트웨어를 설치 하는 것과 동일한 서버에 있을 필요는 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>Windows PowerShell을 사용 하 여 원격 컴퓨터에서 데이터베이스를 구성 하는 경우 windows PowerShell을 준수 및 감사 데이터베이스 서버에 설치 하지 않아도 됩니다.</p></td>
</tr>
</tbody>
</table>



## 보고서에 대 한 필수 조건


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 SQL Server 버전</p></td>
<td align="left"><p>SQL_Latin1_General_CP1_CI_AS 데이터 정렬을 사용 하 여 SQL Server를 설치 합니다.</p>
<p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SSRS (SQL Server Reporting Services)</p></td>
<td align="left"><p>MBAM 서버 설치 중에 SSRS를 설치 하 고 실행 해야 합니다.</p>
<p>구성 &quot; &quot; 되지 않음 또는 SharePoint 모드가 아닌 기본 모드에서 SSRS를 구성할 수 &quot; &quot; 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SSRS 인스턴스 권한 – 보고서를 구성 하는 서버에서 별도의 서버에 데이터베이스를 설치 하는 경우에만 보고서를 구성 해야 합니다.</p></td>
<td align="left"><p>필요한 인스턴스 권한:</p>
<ul>
<li><p>폴더 만들기</p></li>
<li><p>보고서 게시</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>Windows PowerShell을 사용 하 여 원격 컴퓨터에서 데이터베이스를 구성 하는 경우 windows PowerShell을이 데이터베이스 서버에 설치할 필요가 없습니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>관리 및 모니터링 서버용 필수 조건


다음 표에는 MBAM 관리 및 모니터링 서버의 설치 필수 구성 요소가 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 웹 서버 역할</p></td>
<td align="left"><p>이 역할은 관리 및 모니터링 서버 기능에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 서버 (IIS) 관리 도구</p></td>
<td align="left"><p><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SSL 인증서</strong></p></td>
<td align="left"><p>선택 사항. 클라이언트 컴퓨터와 웹 서비스 간의 통신을 보호 하려면 신뢰할 수 있는 보안 기관에서 서명한 인증서를 얻고 설치 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 서버 역할 서비스</p></td>
<td align="left"><p><strong>일반적인 HTTP 기능:</strong></p>
<ul>
<li><p>정적 콘텐츠</p></li>
<li><p>기본 문서</p></li>
</ul>
<p><strong>응용 프로그램 개발:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET 확장성</p></li>
<li><p>ISAPI 확장</p></li>
<li><p>ISAPI 필터</p></li>
</ul>
<p><strong>보안이</strong></p>
<ul>
<li><p>Windows 인증</p></li>
<li><p>요청 필터링</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 기능</p></td>
<td align="left"><p><strong>.NET Framework 4.5 기능:</strong></p>
<ul>
<li><p><strong>.NET Framework 4.5 또는 4.6</strong></p>
<ul>
<li><p><strong></strong> - 이 버전의 windows server에는 windows server 2016 .net Framework 4.6이 이미 설치 되어 있지만, 사용 하도록 설정 해야 합니다.</p></li>  
<li><p><strong>Windows server 2012 또는 Windows Server 2012 R2 </strong> - .net Framework 4.5이 이러한 버전의 windows server에 대해 이미 설치 되어 있지만이를 사용 하도록 설정 해야 합니다.</p></li>
<li><p><strong>Windows Server 2008 R2 </strong> - .net Framework 4.5는 windows Server 2008 r2에 포함 되어 있지 않으므로 <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Microsoft .net framework 4.5을 다운로드 </a> 하 여 별도로 설치 해야 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>MBAM 2.0 또는 MBAM 2.0 SP1에서 업그레이드 하는 경우 .NET Framework 4.5을 설치 해야 하는 경우 <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> </a> 웹 사이트를 작동 하는 데 필요한 추가 단계는 mbam 2.5에 대 한 릴리스 정보를 참조 하세요.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>WCF 활성화</strong></p>
<ul>
<li><p>HTTP 활성화</p></li>
<li><p>비 HTTP 정품 인증 (Windows Server 2008, 2012 및 2012 R2에만 해당)</p>
<p></p></li>
</ul></li>
<li><p><strong>TCP 활성화</strong></p></li>
</ul>
<p><strong>Windows Process Activation Service:</strong></p>
<ul>
<li><p>프로세스 모델</p></li>
<li><p>.NET Framework 환경</p></li>
<li><p>구성 Api</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4.0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">ASP.NET MVC 4 다운로드</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SPN (서비스 사용자 이름)</p></td>
<td align="left"><p>웹 응용 프로그램에는 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 가상 호스트 이름에 대 한 SPN이 필요 합니다.</p>
<p>관리 권한이 Active Directory 도메인 서비스에서 Spn을 만들 수 있도록 허용 하는 경우 MBAM이 사용자를 위한 SPN을 만듭니다. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Spn을 </a> 만드는 데 필요한 권한에 대 한 자세한 내용은 Setspn을 참조 하세요.</p>
<p>Spn을 만들 수 있는 관리자 권한이 없는 경우 다음 명령을 사용 하 여 조직의 Active Directory 관리자에 게 사용자의 SPN을 만들도록 요청 해야 합니다.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>코드 예제에서 가상 호스트 이름은 mbamvirtual.contoso.com 웹 응용 프로그램 풀에 사용 되는 도메인 계정은 contoso\mbamapppooluser.입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>부하 분산을 설정 하는 경우 모든 서버에서 동일한 응용 프로그램 풀 계정을 사용 합니다.</p>
</div>
<div>

</div>
<p>정규화 된 NetBIOS 및 사용자 지정 호스트 이름에 대 한 Spn을 등록 하는 방법에 대 한 자세한 내용은 <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> MBAM 웹 사이트 보안 방법 계획을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



## 셀프 서비스 포털의 필수 구성 요소


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 Windows Server 버전</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4.0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">ASP.NET MVC 4 다운로드</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 서비스 IIS 관리 도구</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SPN (서비스 사용자 이름)</p></td>
<td align="left"><p>웹 응용 프로그램에는 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 가상 호스트 이름에 대 한 SPN이 필요 합니다.</p>
<p>관리 권한이 Active Directory 도메인 서비스에서 Spn을 만들 수 있도록 허용 하는 경우 MBAM이 사용자를 위한 SPN을 만듭니다. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Spn을 </a> 만드는 데 필요한 권한에 대 한 자세한 내용은 Setspn을 참조 하세요.</p>
<p>Spn을 만들 수 있는 관리자 권한이 없는 경우 다음 명령을 사용 하 여 조직의 관리자에 게 사용자를 위한 SPN을 만들어야 하는 Active Directory 관리자에 게 요청 해야 합니다.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>코드 예제에서 가상 호스트 이름은 mbamvirtual.contoso.com 웹 응용 프로그램 풀에 사용 되는 도메인 계정은 contoso\mbamapppooluser.입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>부하 분산을 설정 하는 경우 모든 서버에서 동일한 응용 프로그램 풀 계정을 사용 합니다.</p>
</div>
<div>

</div>
<p>정규화 된 NetBIOS 및 사용자 지정 호스트 이름에 대 한 Spn을 등록 하는 방법에 대 한 자세한 내용은 <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> MBAM 웹 사이트 보안 방법 계획을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



## 관리 워크스테이션의 필수 구성 요소


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 클라이언트를 설치 하기 전에, <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> MDOP 그룹 정책 (admx) 템플릿을 가져오는 방법과 </a> 엔터프라이즈에서 BitLocker 드라이브 암호화에 대해 구현 하려는 설정으로 구성 하는 방법에서 Mbam 그룹 정책 템플릿을 다운로드 하세요.</p></td>
<td align="left"><p>MBAM 클라이언트를 설치 하기 전에 다음을 수행 합니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">수행할 작업</th>
<th align="left">지침을 받을 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 그룹 정책 서식 파일 복사</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">MBAM 2.5 그룹 정책 템플릿 복사</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>그룹 정책 설정 편집</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">MBAM 2.5 그룹 정책 설정 편집</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## 관련 항목


[MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)

[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)

[MBAM 2.5 지원되는 구성](mbam-25-supported-configurations.md)




## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




