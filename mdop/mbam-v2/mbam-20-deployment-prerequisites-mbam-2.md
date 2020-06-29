---
title: MBAM 2.0 배포 필수 구성 요소
description: MBAM 2.0 배포 필수 구성 요소
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826013"
---
# MBAM 2.0 배포 필수 구성 요소


Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하기 위한 전제 조건을 충족 하는지 확인 해야 합니다. 이 섹션에서는 Microsoft BitLocker 관리 및 모니터링 서버 기능 및 클라이언트를 배포 하기 전에 컴퓨팅 환경을 성공적으로 계획 하는 데 도움이 되는 정보를 제공 합니다. 구성 관리자를 사용 하 여 MBAM을 설치 하는 경우 추가 필수 구성 요소에 대해 [구성 관리자를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md) 을 참조 하세요.

## MBAM 서버 기능에 대 한 설치 필수 조건


각 MBAM 서버 기능에는 MBAM 기능을 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다. MBAM 설치 프로그램이 설치를 시작 하기 전에 모든 필수 구성 요소를 충족 하는지 확인 합니다.

### 관리 및 모니터링 서버용 필수 조건

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
<td align="left"><p><strong>Windows Server 웹 서버 역할</strong></p></td>
<td align="left"><p>이 역할은 관리 및 모니터링 서버 기능에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>웹 서버 (IIS) 관리 도구</strong></p></td>
<td align="left"><p><strong>IIS 관리 스크립트 및 도구를 선택 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SSL 인증서</strong></p></td>
<td align="left"><p>선택 사항. 클라이언트와 웹 서비스 간의 통신을 보호 하려면 신뢰할 수 있는 보안 기관에서 서명한 인증서를 얻고 설치 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>웹 서버 역할 서비스</strong></p></td>
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
<td align="left"><p><strong>Windows Server 기능</strong></p></td>
<td align="left"><p><strong>.NET Framework 3.5.1 기능:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>WCF 활성화</p>
<ul>
<li><p>HTTP 활성화</p></li>
<li><p>비 HTTP 활성화</p></li>
</ul></li>
</ul>
<p><strong>Windows Process Activation Service:</strong></p>
<ul>
<li><p>프로세스 모델</p></li>
<li><p>.NET 환경</p></li>
<li><p>구성 Api</p></li>
</ul></td>
</tr>
</tbody>
</table>



**참고**  
지원 되는 운영 체제 목록은 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.



### 규정 준수 및 감사 보고서의 필수 조건

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
<td align="left"><p>지원 되는 SQL Server 버전</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</p></td>
<td align="left"><p>다음을 사용 하 여 SQL Server 설치:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS 데이터 정렬</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>SSRS (SQL Server Reporting Services)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SSRS 인스턴스 권한 – 보고서와 다른 별도의 서버에 데이터베이스를 설치 하는 경우에만 보고서를 설치 해야 합니다.</p></td>
<td align="left"><p>필요한 인스턴스 권한:</p>
<ul>
<li><p>폴더 만들기</p></li>
<li><p>보고서 게시</p></li>
</ul>
<p>MBAM 서버 설치 중에 SSRS를 설치 하 고 실행 해야 합니다. "기본" 모드에서 SSRS를 구성 하 고, 설정 되지 않음 또는 "SharePoint" 모드를 설정 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



### 복구 데이터베이스에 대 한 필수 조건

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
<td align="left"><p>지원 되는 SQL Server 버전</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</p></td>
<td align="left"><p>다음을 사용 하 여 SQL Server 설치:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS 데이터 정렬</p></li>
<li><p>SQL Server 관리 도구</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>필요한 SQL Server 권한</p></td>
<td align="left"><p>필요한 권한:</p>
<ul>
<li><p>SQL 인스턴스 로그인 서버 역할:</p>
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
<td align="left"><p>선택 사항-SQL Server에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능 설치</p></td>
<td align="left"><p>TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에서 설정 된 여러 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 하는데, 이것은 사용자가 로그온 한 계정에 SQL Server 테이블에서 복구 키 정보를 보는 동안 데이터베이스에 대 한 사용 권한이 있는 경우 복구 키 정보가 표시 됨을 의미 합니다.</p>
</div>
<div>

</div>
<p>TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> mbam 2.0 보안 고려 사항에 대해 자세히 알아보세요 </a> .</p></td>
</tr>
</tbody>
</table>



### 준수 및 감사 데이터베이스에 대 한 필수 조건

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
<td align="left"><p>지원 되는 SQL Server 버전</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</p></td>
<td align="left"><p>다음을 사용 하 여 SQL Server 설치:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS 데이터 정렬</p></li>
<li><p>SQL Server 관리 도구</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>필요한 SQL Server 권한</p></td>
<td align="left"><p>필요한 권한:</p>
<ul>
<li><p>SQL 인스턴스 로그인 서버 역할:</p>
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
<td align="left"><p>선택 사항-SQL Server의 TDE (투명 데이터 암호화) 기능을 설치 합니다.</p></td>
<td align="left"><p>TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에서 설정 된 여러 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 하는데, 이것은 사용자가 로그온 한 계정에 SQL Server 테이블에서 복구 키 정보를 보는 동안 데이터베이스에 대 한 사용 권한이 있는 경우 복구 키 정보가 표시 됨을 의미 합니다.</p>
</div>
<div>

</div>
<p>TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> mbam 2.0 보안 고려 사항에 대 한 자세한 정보</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server는 MBAM 서버 설치 중에 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SQL Server 에이전트 서비스가 실행 중이 고 선택한 SQL Server 인스턴스에서 자동 시작으로 설정 되어 있어야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### 셀프 서비스 포털의 필수 구성 요소

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
<td align="left"><p>지원 되는 Windows Server 버전</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2.0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">ASP.NET MVC 2 다운로드</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 서비스 IIS 관리 도구</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## MBAM 클라이언트의 필수 구성 요소


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
<td align="left"><p><strong>Windows 7 클라이언트 </strong> - 에는 TPM (신뢰할 수 있는 플랫폼 모듈) 기능이 있어야 합니다.</p></td>
<td align="left"><p>TPM 버전은 1.2 이상 이어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TPM 칩이 BIOS에서 켜져 있고 운영 체제에서 재설정 가능 해야 합니다.</p></td>
<td align="left"><p>자세한 내용은 BIOS 설명서를 참조 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows 8 클라이언트만 </strong> : mbam이 tpm 복구 키를 저장 하 고 관리 하도록 하려면 tpm 자동 프로비저닝이 꺼져 있어야 하 고 mbam을 배포 하기 전에 tpm 소유자로 설정 해야 합니다. TPM 자동 프로비저닝을 끄려면-TpmAutoProvisioning을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> </a> .</p>
<ul>
<li><p>TPM 자동 프로비저닝이 해제 되어 있어야 합니다.</p></li>
<li><p>Mbam을 배포 하기 전에 \ AM을 TPM 소유자로 설정 해야 합니다.</p></li>
</ul></td>
<td align="left"><p>TPM 자동 프로비저닝을 끄려면-TpmAutoProvisioning을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> </a> .</p>
<div class="alert">
<strong>참고</strong><br/><p>키보드, 비디오 또는 마우스가 키보드, 비디오 또는 마우스 (KVM) 스위치를 통해 직접 연결 되어 관리 되지 않는지 확인 합니다. KVM 스위치는 컴퓨터의 실제 현재 상태를 감지 하는 기능을 방해할 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## 관련 항목


[MBAM 2.0 배포 계획](planning-to-deploy-mbam-20-mbam-2.md)

[MBAM 2.0 지원되는 구성](mbam-20-supported-configurations-mbam-2.md)









