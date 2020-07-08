---
title: MBAM 2.0 지원되는 구성
description: MBAM 2.0 지원되는 구성
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823908"
---
# MBAM 2.0 지원되는 구성


이 항목에서는 독립 실행형 토폴로지를 사용 하 여 사용자 환경에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0을 설치 하 고 실행 하기 위한 요구 사항을 지정 합니다. 이후 릴리스에 적용 되는 지원 되는 구성에 대해서는 해당 릴리스에 대 한 설명서를 참조 하세요.

구성 관리자 토폴로지를 사용 하 여 MBAM 2.0을 설치 하 고 시스템 요구 사항 목록을 검토 하려면 [구성 관리자를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.

프로덕션 환경에서 MBAM을 실행 하는 데 권장 되는 구성은 확장성 요구 사항에 따라 두 개의 서버를 사용 하는 것입니다. 이 구성은 최대 20만 MBAM 클라이언트를 지원 합니다. 독립 실행형 MBAM 서버 인프라에 대 한 이미지 및 설명은 [mbam 2.0의 상위 수준 아키텍처](high-level-architecture-for-mbam-20-mbam-2.md)를 참조 하세요.

**참고**  Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.

 

## <a href="" id="---------mbam-server-system-requirements"></a> MBAM 서버 시스템 요구 사항


### 서버 운영 체제 요구 사항

다음 표에는 Microsoft BitLocker 관리 및 모니터링 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>스탠더드 또는 Datacenter Edition</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>

 

**참고**  도메인 컨트롤러 컴퓨터에는 MBAM 서비스, 보고서 또는 데이터베이스를 설치 하는 기능이 지원 되지 않습니다.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>서버 프로세서, RAM 및 디스크 공간 요구 사항

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">하드웨어 구성 요소</th>
<th align="left">최소 요구 사항</th>
<th align="left">권장 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>처리자</p></td>
<td align="left"><p>2.33 GHz</p></td>
<td align="left"><p>2.33 GHz 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8gb</p></td>
<td align="left"><p>12gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>2GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a>SQLServer 데이터베이스 요구 사항

다음 표에는 복구 데이터베이스, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 포함 된 관리 및 모니터링 서버 기능 설치에 대해 지원 되는 SQLServer 버전이 나와 있습니다. 데이터베이스에는 추가적으로 SQL Server 관리 도구를 설치 해야 합니다.

**참고**  MBAM은 기본적으로 SQL 클러스터링, 미러링 또는 가용성 그룹을 지원 하지 않습니다. 데이터베이스를 설치 하려면 독립 실행형 SQL server에서 MBAM 서버 설치를 실행 해야 합니다.

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server 버전</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">하드웨어 구성 요소</th>
<th align="left">최소 요구 사항</th>
<th align="left">권장 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>처리자</p></td>
<td align="left"><p>2.33 GHz</p></td>
<td align="left"><p>2.33 GHz 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8gb</p></td>
<td align="left"><p>12gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>5GB</p></td>
<td align="left"><p>5gb 이상</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> MBAM 클라이언트 시스템 요구 사항


### 클라이언트 운영 체제 요구 사항

다음 표에는 Microsoft BitLocker 관리 및 모니터링 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise 또는 Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Enterprise 버전</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8 Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>클라이언트 RAM 요구 사항

Microsoft BitLocker 관리 및 모니터링 클라이언트 설치와 관련 된 RAM 요구 사항은 없습니다.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> MBAM 그룹 정책 시스템 요구 사항


다음 표에는 Microsoft BitLocker 관리 및 그룹 정책 템플릿 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise 또는 Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Enterprise 버전</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>스탠더드 또는 Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 2.0 배포 계획](planning-to-deploy-mbam-20-mbam-2.md)

[MBAM 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





