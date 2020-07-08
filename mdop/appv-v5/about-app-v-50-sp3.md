---
title: App-V 5.0 SP3 정보
description: App-V 5.0 SP3 정보
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814973"
---
# App-V 5.0 SP3 정보


다음 섹션을 사용 하 여 Microsoft Application Virtualization (App-v) 5.0 SP3에 적용 되는 중요 한 변경 사항에 대 한 정보를 검토 합니다.

-   [앱-V 5.0 SP3 소프트웨어 필수 구성 요소 및 지원 되는 구성](#bkmk-sp3-prereq-configs)

-   [App-V 5.0 SP3으로 마이그레이션](#bkmk-migrate-to-50sp3)

-   [수동으로 만든 연결 그룹 xml 파일에는 스키마 업데이트가 필요 합니다.](#bkmk-update-schema-cg)

-   [연결 그룹 개선](#bkmk-cg-improvements)

-   [관리자가 특정 사용자를 위해 패키지를 게시 하 고 게시 취소할 수 있습니다.](#bkmk-usersid-pub-pkgs-specf-user)

-   [패키지 게시 및 게시 취소를 위해 관리자만 사용 하도록 설정](#bkmk-admins-only-pub-unpub-pkgs)

-   [RunVirtual registry 키는 사용자에 게 게시 되는 패키지를 지원 합니다.](#bkmk-runvirtual-reg-key)

-   [새 PowerShell cmdlet 및 업데이트 가능한 cmdlet 도움말](#bkmk-posh-cmdlets-help)

-   [PVAD (주 가상 응용 프로그램 디렉터리)가 숨겨져 있지만 켤 수 있습니다.](#bkmk-pvad-hidden)

-   [App-v 게시 메타 데이터를 보려면 ClientVersion이 필요 합니다.](#bkmk-pub-metadata-clientversion)

-   [App-v 이벤트 로그가 통합 되었습니다.](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>앱-V 5.0 SP3 소프트웨어 필수 구성 요소 및 지원 되는 구성


App-v 5.0 SP3 소프트웨어 요구 사항 및 지원 되는 구성에 대 한 다음 링크를 참조 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">전제 조건과 지원 되는 구성에 대 한 링크</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">App-V 5.0 SP3 필수 구성 요소</a></p></td>
<td align="left"><p>App-v 5.0 SP3 설치를 시작 하기 전에 설치 해야 하는 필수 소프트웨어</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 지원되는 구성</a></p></td>
<td align="left"><p>App-v Server, Sequencer 및 클라이언트 구성 요소에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>App-V 5.0 SP3으로 마이그레이션


다음 정보를 사용 하 여 이전 버전의 App-v 5.0 SP3으로 업그레이드 합니다.

### 업그레이드를 시작 하기 전에

업그레이드를 시작 하기 전에 다음 정보를 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">업그레이드 하기 전에 검토할 항목</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>업그레이드할 구성 요소</p></td>
<td align="left"><ol>
<li><p>App-v Server</p></li>
<li><p>않았음이</p></li>
<li><p>앱-V 클라이언트 또는 App-v (원격 데스크톱 서비스) 클라이언트</p></li>
<li><p>연결 그룹</p></li>
</ol>
<div class="alert">
<strong>참고</strong><br/><p>App-v 클라이언트 사용자 인터페이스를 사용 하려면 <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> Microsoft Application Virtualization 5.0 클라이언트 UI 응용 프로그램에서 기존 버전을 다운로드 </a> 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 4. x에서 업그레이드</p></td>
<td align="left"><p>먼저 App-v 5.0으로 업그레이드 해야 합니다. 앱-V 4. x에서 App-v 5.0 SP3으로 직접 업그레이드할 수 없습니다.</p>
<p>자세한 내용은 다음을 참조하세요.</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">App-V 5.0 정보</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">App-V의 이전 버전에서 마이그레이션 계획</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱-V 5.0 이상에서 업그레이드</p></td>
<td align="left"><p>다음 버전 중 하나에서 앱-V 5.0 SP3으로 직접 업그레이드할 수 있습니다.</p>
<ul>
<li><p>App-V 5.0</p></li>
<li><p>App-v 5.0 SP1</p></li>
<li><p>App-v 5.0 SP2</p></li>
</ul>
<p>App-v 5.0 SP3으로 업그레이드 하려면이 문서의 나머지 섹션에 나와 있는 단계를 따르세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>업그레이드 후 패키지 및 연결 그룹의 필수 변경 사항</p></td>
<td align="left"><p>없음. 패키지 및 연결 그룹은 현재 처럼 계속 작동 합니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>앱-V 인프라를 업그레이드 하는 단계

앱-V 인프라의 각 구성 요소를 App-v 5.0 SP3으로 업그레이드 하려면 다음 단계를 완료 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">자세한 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1 단계: App-v Server를 업그레이드 합니다.</p>
<p>App-v 서버를 사용 하지 않는 경우에는이 단계를 건너뛰고 다음 단계로 이동 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>App-v 5.0 SP3 클라이언트는 App-v 5.0 SP1 서버와 호환 됩니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>다음 단계를 따르세요.</p>
<ol>
<li><p>App-v <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> </a> Server 설치에 영향을 줄 수 있는 문제에 대 한 앱-v 5.0 SP3 릴리스 정보를 검토 합니다.</p></li>
<li><p>관리 데이터베이스 및/또는 보고 데이터베이스를 업그레이드 하는 데 사용 하는 방법에 따라 다음 중 하나를 수행 합니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">데이터베이스 업그레이드 방법</th>
<th align="left">단계</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>이 단계를 건너뛰고 3 단계 ("App-v Server를 업그레이드 하는 경우 ...")로 이동 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL 스크립트</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>관리 데이터베이스</strong></p></td>
<td align="left"><p>설치 또는 업그레이드 하려면 <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> SQL 스크립트를 설치 또는 업그레이드 (app-v 5.0 SP3 관리 서버 데이터베이스 실패)를 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>보고 데이터베이스</strong></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법의 단계를 따릅니다 </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>App-v 5.0 SP1 핫픽스 패키지 3 이상에서 App-v 서버를 업그레이드 하는 경우 <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> app-v 5.0 SP3 서버 설치 후 레지스트리 키 확인 섹션의 단계를 완료 </a> 하세요.</p></li>
<li><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">App-v 5.0 서버를 배포 하는 방법의 단계를 따릅니다 </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>2 단계: App-v Sequencer를 업그레이드 합니다.</p></td>
<td align="left"><p><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">Sequencer를 설치 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3 단계: App-v 클라이언트 또는 App-v RDS 클라이언트를 업그레이드 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">App-v 클라이언트를 배포 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>App-v 5.0 SP3 서버를 설치 하기 전에 레지스트리 키 확인

앞의 표에 있는 3 단계입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>이 단계가 필요한 경우</strong></p></td>
<td align="left"><p>.Msp 파일을 사용 하 여 설치한 이후 핫픽스 패키지를 사용 하 여 App-v SP1에서 업그레이드 하는 경우</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>이 단계를 수행 해야 하는 구성 요소</strong></p></td>
<td align="left"><p>업그레이드 하는 App-v 서버 구성 요소만</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>이 단계를 수행 해야 하는 경우</strong></p></td>
<td align="left"><p>앱-V 5.0 SP3으로 업그레이드 하기 전에</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>수행 해야 할 작업</strong></p></td>
<td align="left"><p>다음 표의 정보를 사용 하 여 <code>HKLM\Software\Microsoft\AppV\Server</code> 원래 서버 설치에서 제공한 값으로 각 레지스트리 키 값을 업데이트 합니다. 이 단계를 완료 하면 App-v SP1 핫픽스 패키지를 설치할 때 제거 되었을 수 있는 레지스트리 값이 복원 됩니다.</p></td>
</tr>
</tbody>
</table>



**ManagementDatabase 키**

관리 데이터베이스를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">키 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>공용 액세스 계정이 비로컬 관리 데이터베이스에 액세스 하는 데 필요한 지 여부를 설명 합니다. 필요한 경우 값이 "1"로 설정 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>관리 데이터베이스의 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>관리 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정입니다.</p>
<p><code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>관리 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</p>
<p><code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>관리 데이터베이스용 SQL Server 인스턴스입니다.</p>
<p>값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>관리 데이터베이스에 대 한 쓰기 (관리자) 액세스에 사용 되는 계정입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>관리 데이터베이스에 대 한 쓰기 (관리자) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>관리 서버 원격 컴퓨터 계정 (계정).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>관리 서버 (%0)에 대 한 설치 관리자 로그인</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>유효한 값은 다음과 같습니다.</p>
<ul>
<li><p><strong>1 </strong> – 관리 서비스가 로컬 컴퓨터에 있으며,이는 MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT 비어 있습니다.</p></li>
<li><p><strong>0 </strong> - 관리 서비스는 로컬 컴퓨터와 다른 컴퓨터에 있습니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>



**ManagementService 키**

관리 서버를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ManagementService` 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">키 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>AD DS (Active Directory 도메인 서비스) 그룹 또는 App.config (App-v) 관리 권한이 있는 계정입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>관리 데이터베이스를 포함 하는 SQL server 인스턴스입니다.</p>
<p>값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>관리 데이터베이스를 사용 하는 원격 SQL 서버의 이름입니다.</p>
<p>값이 비어 있으면 로컬 컴퓨터를 사용 합니다.</p></td>
</tr>
</tbody>
</table>



**ReportingDatabase 키**

보고 데이터베이스를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">키 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>로컬이 아닌 보고 데이터베이스에 액세스 하는 데 공개 액세스 계정이 필요한 지 여부를 설명 합니다. 필요한 경우 값이 "1"로 설정 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>보고 데이터베이스의 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>보고 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정입니다.</p>
<p><code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>보고 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</p>
<p><code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>보고 데이터베이스용 SQL Server 인스턴스입니다.</p>
<p>값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Reporting server 컴퓨터 계정 (계정)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Reporting server (%0)에 대 한 설치 관리자 로그인</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>유효한 값은 다음과 같습니다.</p>
<ul>
<li><p><strong>1 </strong> – Reporting service가 로컬 컴퓨터에 있으며,이는 REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT 비어 있습니다.</p></li>
<li><p><strong>0 </strong> - Reporting services가 로컬 컴퓨터와 다른 컴퓨터에 있습니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>



**ReportingService 키**

보고 서버를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ReportingService` 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">키 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>보고 데이터베이스용 SQL Server 인스턴스입니다.</p>
<p>값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>보고 데이터베이스를 사용 하는 원격 SQL 서버의 이름입니다.</p>
<p>값이 비어 있으면 로컬 컴퓨터를 사용 합니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a>수동으로 만든 연결 그룹 xml 파일에는 스키마 업데이트가 필요 합니다.


연결 그룹 XML 파일을 수동으로 만들고 [연결 그룹 개선](#bkmk-cg-improvements)에 설명 된 새 "선택적 패키지" 및 "모든 버전 사용" 기능을 사용 하려는 경우 XML 파일에서 다음 스키마를 지정 해야 합니다.

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

예제 및 자세한 내용은 [연결 그룹 파일 정보](about-the-connection-group-file.md)를 참조 하세요.

## <a href="" id="bkmk-cg-improvements"></a>연결 그룹 개선


앱-V 5.0 SP3에 추가 된 선택적 패키지 및 기타 개선 기능을 사용 하 여 연결 그룹을 더욱 쉽게 관리할 수 있습니다. 다음 표에서는 새 연결 그룹 기능을 사용 하 여 수행할 수 있는 작업과 각 작업에 대 한 자세한 정보에 대 한 링크를 요약 하 여 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업/기능</th>
<th align="left">설명</th>
<th align="left">추가 정보 링크</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>연결 그룹이 선택적 패키지를 포함 하도록 설정</p></td>
<td align="left"><p>연결 그룹에 선택적 패키지를 포함 하면 사용자가 제공 하는 응용 프로그램에 따라 연결 그룹의 가상 환경에 포함 될 응용 프로그램을 동적으로 결정할 수 있습니다.</p>
<p>여러 개의 연결 그룹을 관리 하는 것은 동일한 연결 그룹에서 선택적 및 선택 사항이 아닌 패키지를 혼합할 수 있기 때문입니다. 패키지를 혼합 하면 사용자가 공통 된 패키지를 하나만 가질 수 있지만 서로 다른 사용자 그룹이 동일한 연결 그룹을 사용할 수 있습니다.</p>
<p><strong>예 </strong> : 모든 사용자에 대해 Microsoft Office를 사용 하 여 패키지를 사용 하도록 설정할 수 있지만 다양 한 Office 플러그 인을 사용자의 다른 하위 집합에 포함 하는 다양 한 선택적 패키지를 사용 하도록 설정 합니다.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">연결 그룹에서 선택적 패키지를 사용하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>연결 그룹을 변경 하지 않고 선택 패키지 게시 취소 또는 삭제</p></td>
<td align="left"><p>앱-V 클라이언트에서 연결 그룹을 비활성화 하거나 다시 사용 하도록 설정 하지 않고 연결 그룹에 있는 선택적 패키지를 게시 취소 하거나 게시 취소 하 고 게시 합니다.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">연결 그룹에서 선택적 패키지를 사용하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 게시 및 전역 게시 패키지가 포함 된 연결 그룹 게시</p></td>
<td align="left"><p>사용자가 게시 하 고 전역적으로 게시 된 패키지를 포함 하는 사용자 게시 연결 그룹을 만듭니다.</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>연결 그룹에서 패키지 버전을 무시 하도록 만들기</p></td>
<td align="left"><p>연결 그룹을 사용 하지 않도록 설정 하지 않고 패키지를 업그레이드할 수 있도록 모든 버전의 패키지를 받아들이도록 연결을 구성 합니다. 또한 연결 그룹에 잘못 된 버전이 있는 선택적 패키지가 있는 경우 패키지가 무시 되 고 연결 그룹의 가상 환경이 만들어지지 않도록 차단 되지 않습니다.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">연결 그룹에서 패키지 버전을 무시하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>최종 사용자의 게시 기능 제한</p></td>
<td align="left"><p>관리자 (최종 사용자가 아님)만 패키지를 게시 하 고 연결 그룹을 사용 하도록 설정할 수 있습니다.</p></td>
<td align="left"><p>연결 그룹에 대 한 자세한 내용은 <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> 관리자만 연결 그룹을 사용 하도록 허용 하는 방법을 참조 하세요.</a></p>
<p>패키지에 대 한 자세한 내용은 다음 문서를 참조 하세요.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">추가 정보 링크</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>관리 콘솔</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">관리 콘솔을 사용하여 패키지를 게시하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>타사 전자 소프트웨어 전달 시스템</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">ESD를 사용하여 관리자만 패키지를 게시할 수 있도록 하는 방법</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>특정 사용자에 대 한 연결 그룹을 설정 하거나 해제 합니다.</p></td>
<td align="left"><p>관리자는 다음 cmdlet을 사용 하 여 optional <strong> – UserSID 매개 변수를 사용 하 여 특정 사용자에 대 한 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있습니다 </strong> .</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Disable-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>연결 그룹의 하나의 가상 디렉터리에 동일한 패키지 경로 병합</p></td>
<td align="left"><p>연결 그룹에 있는 둘 이상의 패키지에 동일한 디렉터리 경로가 포함 된 경우 경로가 연결 그룹 가상 환경 내의 단일 가상 디렉터리로 병합 됩니다.</p>
<p>이러한 경로 병합을 통해 한 패키지의 응용 프로그램이 다른 패키지의 파일에 액세스할 수 있습니다.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">연결 그룹 가상 환경 정보</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>관리자가 특정 사용자를 위해 패키지를 게시 하 고 게시 취소할 수 있습니다.


관리자는 다음 cmdlet을 사용 하 여 특정 사용자에 대 한 패키지를 게시 하거나 게시할 수 있습니다. Cmdlet을 사용 하려면 **– UserSID** 매개 변수를 입력 하 고 그 뒤에 사용자의 SID (보안 식별자)가와 야 합니다. 자세한 내용은 다음을 참조하세요.

-   [PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">예</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>게시-AppvClientPackage</p></td>
<td align="left"><p>게시-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>게시 취소-AppvClientPackage</p></td>
<td align="left"><p>게시 취소-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>패키지 게시 및 게시 취소를 위해 관리자만 사용 하도록 설정


다음 방법 중 하나를 사용 하 여 패키지를 게시 하거나 게시가 취소 하는 경우에만 관리자 (최종 사용자가 아님)만 사용할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>그룹 정책 설정</p></td>
<td align="left"><p>다음 그룹 정책 개체 노드로 이동 합니다.</p>
<p><strong>컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시 </strong> .</p>
<p><strong>관리자 권한으로 게시 </strong> 그룹 정책 설정을 사용 하도록 설정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>RunVirtual registry 키는 사용자에 게 게시 되는 패키지를 지원 합니다.


App-v 5.0 SP3은 사용자 게시 된 패키지에 있는 가상화 된 응용 프로그램에서 **Runvirtual** 레지스트리 키를 사용 하는 데 대 한 지원을 추가 합니다. **Runvirtual** registry 키를 사용 하 여 가상 환경에서 로컬에 설치 된 응용 프로그램을 실행할 수 있으며, app-v를 통해 가상화 된 응용 프로그램과 함께

이전에는 App-v 패키지의 가상화 된 응용 프로그램을 전역으로 게시 해야 했습니다. 가상 응용 프로그램을 사용 하 여 가상 환경에서 **로컬에 설치** 된 응용 프로그램을 실행 하는 다른 방법에 대 한 자세한 내용은 가상 [응용 프로그램을 사용 하 여 로컬에 설치 된 응용 프로그램 실행](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)을 참조 하세요.

## <a href="" id="bkmk-posh-cmdlets-help"></a>새 PowerShell cmdlet 및 업데이트 가능한 cmdlet 도움말


앱-V 5.0 SP3에는 새 PowerShell cmdlet 및 업데이트 가능한 cmdlet 도움말이 포함 되어 있습니다. Cmdlet 모듈을 다운로드 하려면 [PowerShell cmdlet을 로드 하는 방법과 Cmdlet 도움말](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets)을 참조 하세요.

### 새 앱-V 5.0 SP3 Server PowerShell cmdlet

연결 그룹을 관리 하는 데 도움이 되도록 App-v 서버에 대 한 새 Windows PowerShell cmdlet이 추가 되었습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>추가-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>연결 그룹의 끝에 패키지를 추가 하 여 패키지를 선택 및/또는 연결 그룹 내에 있는 버전이 없는 상태로 구성할 수 있도록 합니다&#39;s 패키지 목록입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>연결 그룹 패키지에 대 한 세부 정보 (예: 선택 사항)를 편집할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>제거-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>연결 그룹에서 패키지를 제거 합니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>PowerShell cmdlet에 대 한 도움말 보기

Cmdlet 도움말은 다음 형식으로 사용할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">형식</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>다운로드 가능한 모듈</p></td>
<td align="left"><p>Cmdlet 모듈을 다운로드 한 후 최신 도움말을 확인 하려면 다음을 수행 하세요.</p>
<ol>
<li><p>Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</p></li>
<li><p>다음 명령 중 하나를 입력 하 여 원하는 모듈에 대 한 cmdlet을 로드 합니다.</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-v 구성 요소</th>
<th align="left">명령을 입력 합니다.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v Server</p></td>
<td align="left"><p>업데이트-도움말-모듈 AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 시퀀서</p></td>
<td align="left"><p>업데이트-도움말-모듈 AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 클라이언트</p></td>
<td align="left"><p>업데이트-도움말-모듈 AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>TechNet에서 웹 페이지로</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Windows PowerShell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화의 앱-V 노드를 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



자세한 내용은 [PowerShell cmdlet을 로드 하는 방법과 Cmdlet 도움말](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md)을 참조 하세요.

## <a href="" id="bkmk-pvad-hidden"></a>PVAD (주 가상 응용 프로그램 디렉터리)가 숨겨져 있지만 켤 수 있습니다.


App-v 5.0 SP3에서 기본 virtual application directory (PVAD)가 숨겨져 있지만, 다시 켜고 다음 방법 중 하나를 사용 하 여 표시 되도록 할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">단계</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>명령줄 매개 변수 사용</p></td>
<td align="left"><p><strong>– EnablePVADControl </strong> 매개 변수를Sequencer.exe에 <strong> 전달 </strong> 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>레지스트리 하위 키 만들기</p></td>
<td align="left"><ol>
<li><p>레지스트리 편집기에서 다음으로 이동 합니다. <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>참고</strong><br/><p><code>Compatibility</code>하위 키가 없으면 만들어야 합니다.</p>
</div>
<div>

</div></li>
<li><p>EnablePVADControl 이라는 DWORD 값을 <strong> 만들고 </strong> 값을 1로 설정 <strong> </strong> 합니다.</p>
<p>값 <strong> </strong> 이 0 이면 PVAD가 숨겨져 있음을 의미 합니다.</p></li>
</ol></td>
</tr>
</tbody>
</table>



**PVAD에 대 한 자세한 정보:** 시퀀서를 사용 하 여 패키지를 만드는 경우 패키지의 설치 경로를 입력할 수 있습니다. 이전 버전의 App-v에서는 응용 프로그램의 PVAD (주 가상 응용 프로그램 디렉터리)를 경로로 지정 해야 했습니다. PVAD는 앱을 사용 하지 않는 경우 일반적으로 로컬 컴퓨터에 응용 프로그램을 설치 하는 디렉터리입니다. 예를 들어 컴퓨터에 Office를 설치 하는 경우 일반적으로 PVAD는 C:\\program files Files\\Microsoft Office\\.입니다.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>App-v 게시 메타 데이터를 보려면 ClientVersion이 필요 합니다.


App-v 5.0 SP3에서는 메타 데이터에 대해 App-v 게시 서버를 쿼리할 때 주소에 다음 값을 제공 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">값</th>
<th align="left">추가적인 세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p><strong>쿼리에서 clientversion 매개 변수를 생략 하면 </strong> 메타 데이터가 새 APP-V 5.0 SP3 기능을 제외 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ClientOS</strong></p></td>
<td align="left"><p>패키지를 시퀀싱 할 때 특정 클라이언트 운영 체제를 선택 하는 경우에만이 값을 제공 해야 합니다. 기본값 (모든 운영 체제)을 선택 하는 경우 쿼리에이 값을 지정 하지 마세요.</p>
<p><strong>쿼리에서 clientos 매개 변수를 생략 하면 </strong> 모든 운영 체제를 지원 하도록 시퀀싱 된 패키지만 메타 데이터에 표시 됩니다.</p></td>
</tr>
</tbody>
</table>



이 쿼리의 구문 및 예제는 [App-v Server 게시 메타 데이터 보기](viewing-app-v-server-publishing-metadata.md)를 참조 하세요.

## <a href="" id="bkmk-event-logs-moved"></a>App-v 이벤트 로그가 통합 되었습니다.


이전에 **응용 프로그램 및 서비스 로그/microsoft/appv/app-v &lt; 구성 요소 &gt; **에 있는 다음 이벤트 로그가 **응용 프로그램 및 서비스 로그/Microsoft/appv/servicelog**로 이동 되었습니다.

로그를 보려면 **View** &gt; 이벤트 뷰어 응용 프로그램에서 **분석 표시 및 디버그 로그** 보기를 선택 합니다.

클라이언트-카탈로그 클라이언트-통합 클라이언트-PackageConfig 클라이언트-스크립팅 클라이언트-서비스 클라이언트-Vemgr 클라이언트-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary 하위 시스템-ActiveX 하위 시스템-AppPath 하위 시스템-Com 하위 시스템-fta

## MDOP 기술을 활용 하는 방법


앱-V는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.






## 관련 항목


[App-V 5.0 SP3 릴리스 정보](release-notes-for-app-v-50-sp3.md)









