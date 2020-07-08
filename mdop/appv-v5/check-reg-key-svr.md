---
title: App-V 5.x Server 를 설치하기 전에 레지스트리 키 확인
description: App-V 5.x Server 를 설치하기 전에 레지스트리 키 확인
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814708"
---
# App-V 5.x Server 를 설치하기 전에 레지스트리 키 확인

App-v 5.0 SP1 핫픽스 패키지 3 이상에서 App-v 서버를 업그레이드 하는 경우이 섹션의 단계를 완료 하 고 앱-V 5. x 서버를 설치 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>이 단계가 필요한 경우</strong></p></td>
<td align="left"><p>.Msp 파일을 사용 하 여 설치한 이후 핫픽스 패키지를 사용 하 여 App-v 5.0 SP1에서 업그레이드 하는 경우</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>이 단계를 수행 해야 하는 구성 요소</strong></p></td>
<td align="left"><p>업그레이드 하는 App-v 서버 구성 요소만</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>이 단계를 수행 해야 하는 경우</strong></p></td>
<td align="left"><p>App-v Server를 App-V 5. x로 업그레이드 하기 전에</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>수행 해야 할 작업</strong></p></td>
<td align="left"><p>다음 표의 정보를 사용 하 여 <code>HKLM\Software\Microsoft\AppV\Server</code> 원래 서버 설치에서 제공한 값으로 각 레지스트리 키 값을 업데이트 합니다. 이 단계를 완료 하면 App-v 5.0 SP1 핫픽스 패키지를 설치할 때 제거 되었을 수 있는 레지스트리 값이 복원 됩니다.</p></td>
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

