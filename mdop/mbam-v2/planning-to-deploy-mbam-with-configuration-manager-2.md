---
title: Configuration Manager에서 MBAM을 배포하는 계획
description: Configuration Manager에서 MBAM을 배포하는 계획
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825628"
---
# Configuration Manager에서 MBAM을 배포하는 계획


Configuration Manager 토폴로지로 MBAM을 배포 하려면 20만 클라이언트를 지 원하는 3-서버 아키텍처가 권장 됩니다. 별도의 서버를 사용 하 여 구성 관리자를 실행 하 고 시작 하는 아키텍처 이미지에 표시 된 대로 두 서버에서 기본 관리 및 모니터링 기능을 설치 합니다 ( [구성 관리자와 함께 MBAM 사용)](getting-started---using-mbam-with-configuration-manager.md).

**중요**  
Windows To Go는 구성 관리자 2007와 함께 MBAM의 통합 토폴로지를 설치 하는 경우 지원 되지 않습니다.



## Configuration Manager에서 MBAM을 설치 하기 위한 배포 필수 작업


Configuration Manager를 사용 하 여 MBAM을 설치 하기 전에 다음 전제 조건을 충족 하는지 확인 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration manager 서버가 Configuration Manager 시스템의 기본 사이트 인지 확인 합니다.</p></td>
<td align="left"><p>해당 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 서버에서 하드웨어 인벤터리 클라이언트 에이전트를 사용 하도록 설정 합니다.</p></td>
<td align="left"><p>Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> 사이트의 하드웨어 인벤토리를 구성 하는 방법을 참조 </a> 하세요.</p>
<p>System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> 구성 관리자에서 하드웨어 인벤토리를 구성 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 중인 Configuration Manager 버전에 따라 DCM (구성 관리) 에이전트 또는 준수 설정을 사용 하도록 설정 합니다.</p></td>
<td align="left"><p>Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> 원하는 구성 관리 클라이언트 에이전트 속성 보기를 사용 하도록 설정 </a> 합니다.</p>
<p>System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> 구성 관리자에서 준수 설정 구성을 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager에서 보고 서비스 시점을 정의 합니다. SQL Reporting Services에 필요 합니다.</p></td>
<td align="left"><p>Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> SQL Reporting services에 대 한 보고 서비스 지점을 만드는 방법을 참조 하세요 </a> .</p>
<p>System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> 구성 관리자의 보고서에 대 한 필수 구성 요소를 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Configuration Manager에서 지원 되는 버전


MBAM은 다음 버전의 Configuration Manager를 지원 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">지원 되는 버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 이상</p></td>
<td align="left"><p>64비트</p>
<div class="alert">
<strong>참고</strong><br/><p>Configuration Manager 2007는 32 비트 이지만 64 비트 MBAM 소프트웨어와 일치 하려면 64 비트 운영 체제에 SQL Server를 설치 해야 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center 2012 구성 관리자</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



Configuration Manager 서버에서 지원 되는 구성 목록은 사용 중인 구성 관리자 버전에 해당 하는 웹 페이지를 참조 하세요. MBAM에는 Configuration Manager 서버에 대 한 추가 시스템 요구 사항이 없습니다.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> MBAM 및 SQL Server 시스템 요구 사항


MBAM 서버 및 구성 관리자 토폴로지의 SQL Server에 대해 지원 되는 구성 및 시스템 요구 사항은 독립 실행형 토폴로지의 경우와 동일 합니다. 독립 실행형 시스템 요구 사항에 대해서는 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요. MBAM 서버 및 SQL Server 프로세서, RAM 및 구성 관리자 토폴로지의 디스크 공간 요구 사항에 대 한 자세한 내용은 다음 섹션을 참조 하세요.

## Mbam 서버 프로세서, RAM, 디스크 공간 요구 사항 MBAM


다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 MBAM 서버의 서버 프로세서, RAM, 디스크 공간 요구 사항이 나열 되어 있습니다.

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
<td align="left"><p>4GB</p></td>
<td align="left"><p>8gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>2GB</p></td>
</tr>
</tbody>
</table>



## SQL Server 프로세서, RAM 및 디스크 공간 요구 사항


다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 SQL Server 컴퓨터에 대 한 서버 프로세서, RAM, 디스크 공간 요구 사항이 나와 있습니다.

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
<td align="left"><p>4GB</p></td>
<td align="left"><p>8gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>5GB</p></td>
<td align="left"><p>5gb 이상</p></td>
</tr>
</tbody>
</table>



## MBAM 서버를 설치 하는 데 필요한 권한


구성 관리자를 사용 하 여 MBAM을 설치 하려면 다음 표에 나열 된 최소 권한을 사용 하는 보안 역할을 가진 Configuration Manager에 관리자가 있어야 합니다. 또한이 표에는 기본 컴퓨터 관리자 권한 이상의 사용자에 게는 MBAM 서버를 설치 하는 데 필요한 권한도 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용 권한</th>
<th align="left">MBAM 서버 기능</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL 인스턴스 로그인 서버 역할:-dbcreator-processadmin</p></td>
<td align="left"><p>- 복구 데이터베이스-감사 데이터베이스</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services 인스턴스 권한:-폴더 만들기-보고서 게시</p></td>
<td align="left"><p>- System Center Configuration Manager 통합</p></td>
</tr>
</tbody>
</table>



**System Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용 권한</th>
<th align="left">Configuration Manager 서버 기능</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration Manager 사이트 권한:-읽기</p></td>
<td align="left"><p>System Center Configuration Manager 통합</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 컬렉션 권한:-만들기-삭제-읽기-수정-배포 구성 항목</p></td>
<td align="left"><p>System Center Configuration Manager 통합</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 구성 항목 권한:-만들기-삭제-읽기</p></td>
<td align="left"><p>System Center Configuration Manager 통합</p></td>
</tr>
</tbody>
</table>



**Configuration Manager 2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용 권한</th>
<th align="left">Configuration Manager 서버 기능</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration Manager 사이트 권한:-읽기</p></td>
<td align="left"><p>System Center Configuration Manager 통합</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 컬렉션 권한:-Create-Delete-Read-ReadResource</p></td>
<td align="left"><p>System Center Configuration Manager 통합</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 구성 항목 권한:-만들기-삭제-읽기-배포</p></td>
<td align="left"><p>System Center Configuration Manager 통합</p></td>
</tr>
</tbody>
</table>



## 구성 관리자 토폴로지에 대 한 MBAM 기능 배포 순서


Configuration Manager 서버에 MBAM을 배포 하는 경우 다음 순서에 따라 배포 작업을 완료 해야 합니다.

1.  Configuration Manager 서버에서 구성 .mof 파일을 편집 합니다.

2.  Sms \ _def .mof 파일 구성 관리자 서버를 만들거나 편집 합니다.

3.  Configuration Manager 서버에 MBAM을 설치 합니다.

4.  데이터베이스 서버에 복구 데이터베이스와 감사 데이터베이스를 설치 합니다.

5.  관리 및 모니터링 서버에 MBAM 기능을 설치 합니다.

## Configuration Manager를 사용 하 여 MBAM을 설치 하기 위한 계획 검사 목록


이 검사 목록에서는 Microsoft BitLocker 관리 및 Configuration Manager를 사용 하 여 배포 모니터링을 계획할 때 고려해 야 할 항목의 권장 단계 및 상위 수준 목록을 간략하게 설명 합니다. 이 검사 목록을 스프레드시트 프로그램에 복사 하 여 사용을 위해 사용자 지정 하는 것이 좋습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">작업</th>
<th align="left">참조</th>
<th align="left">참고</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Configuration Manager가 MBAM을 사용 하 여 작동 하는 방법과 권장 되는 상위 수준 아키텍처를 보여 주는 시작 정보를 검토 합니다.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">시작 - Configuration Manager를 통해 MBAM 사용</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>배포 필수 구성 요소, 지원 되는 구성, 필요한 사용 권한, 각 기능에 대 한 배포 순서를 설명 하는 계획 정보를 검토 합니다.</p></td>
<td align="left"><p>Configuration Manager에서 MBAM을 배포하는 계획</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 그룹 정책 요구 사항 계획 및 구성</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">MBAM 2.0 그룹 정책 요구 사항 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>필요한 Active Directory 도메인 서비스 보안 그룹을 계획 하 고 만들고 MBAM 로컬 보안 그룹 구성원 요구 사항에 대 한 계획을 수립 합니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">MBAM 2.0 관리자 역할 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 배포 배포 계획입니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">MBAM 2.0 클라이언트 배포 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## 관련 항목


[Configuration Manager와 함께 MBAM 사용](using-mbam-with-configuration-manager.md)









