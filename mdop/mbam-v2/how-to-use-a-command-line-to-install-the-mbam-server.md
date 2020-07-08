---
title: 명령줄을 사용하여 MBAM 서버를 설치하는 방법
description: 명령줄을 사용하여 MBAM 서버를 설치하는 방법
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825643"
---
# 명령줄을 사용하여 MBAM 서버를 설치하는 방법


명령줄을 사용 하 여 독립 실행형 또는 구성 관리자 토폴로지로 MBAM 서버를 설치할 수 있습니다. 다음 명령줄 예제는 테스트 환경 에서만 사용 해야 하는 아키텍처 인 단일 서버에 MBAM을 배포 하는 것입니다. 여러 서버가 있어야 하는 프로덕션 환경에 MBAM을 배포 하는 경우 적절 하 게 명령줄을 변경 해야 합니다.

## 단독 토폴로지를 사용 하 여 MBAM 2.0 서버를 배포 하기 위한 명령줄


다음과 비슷한 명령줄을 사용 하 여 독립 실행형 토폴로지에 MBAM 서버를 설치할 수 있습니다.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

다음 표에서는 독립 실행형 토폴로지와 함께 MBAM 서버를 배포 하기 위한 명령줄 매개 변수에 대해 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">매개 변수 값</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>대규모</p></td>
<td align="left"><p>0</p></td>
<td align="left"><p>0-독립 실행형 토폴로지</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>01</p></td>
<td align="left"><p>0 – 라이선스에 동의 안 함-사용권 계약에 동의 agreement1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>서버에 설치할 기능</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>KeyDatabase</p></td>
<td align="left"><p>복구 데이터베이스</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>준수 및 감사 보고서 데이터베이스</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>보고</p></td>
<td align="left"><p>규정 준수 및 감사 보고서</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>셀프 서비스 포털</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>PolicyTemplate</p></td>
<td align="left"><p>MBAM 그룹 정책 서식 파일</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>준수 및 감사 데이터베이스에 액세스할 수 있는 Reporting Services 서비스 계정의 도메인 및 사용자 계정</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>준수 및 감사 데이터베이스에 액세스 하는 Reporting Services 서비스 계정의 암호입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>이름은</p></td>
<td align="left"><p>준수 및 감사 데이터베이스용 SQL Server 인스턴스 이름 – <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>이름은</p></td>
<td align="left"><p>복구 데이터베이스용 SQL Server 인스턴스 이름 – <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>이름은</p></td>
<td align="left"><p>준수 및 감사 보고서가 설치 되는 SQL Server Reporting Server 인스턴스 – <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 포트입니다. "83"는 예를 보여 줍니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>셀프 서비스 포털 웹 사이트의 포트 "83"는 예를 보여 줍니다.</p></td>
</tr>
</tbody>
</table>

 

## Configuration Manager 토폴로지로 MBAM 2.0 서버를 배포 하기 위한 명령줄


다음과 비슷한 명령줄을 사용 하 여 구성 관리자 토폴로지에 MBAM 서버를 설치할 수 있습니다.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

다음 표에서는 구성 관리자 토폴로지에 MBAM 2.0 서버를 설치 하기 위한 명령줄 매개 변수에 대해 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">매개 변수 값</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>대규모</p></td>
<td align="left"><p>raid-1</p></td>
<td align="left"><p>1-구성 관리자 토폴로지</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>01</p></td>
<td align="left"><p>0 – 라이선스에 동의 안 함-사용권 계약에 동의 agreement1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>이름은</p></td>
<td align="left"><p>감사 데이터베이스용 SQL Server 인스턴스 이름- <strong> % computername%를 </strong> 컴퓨터 이름으로 바꾸기</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>이름은</p></td>
<td align="left"><p>복구 데이터베이스용 SQL Server 인스턴스 이름- <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>이름은</p></td>
<td align="left"><p>감사 보고서가 설치 되는 SQL Server Reporting Server 인스턴스 –% computername%를 컴퓨터 이름으로 바꿉니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>준수 및 감사 데이터베이스에 액세스할 수 있는 Reporting Services 서비스 계정의 도메인 및 사용자 계정</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>준수 및 감사 데이터베이스에 액세스 하는 Reporting Services 서비스 계정의 암호입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 포트입니다. "83"는 예를 보여 줍니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>셀프 서비스 포털 웹 사이트의 포트 "83"는 예를 보여 줍니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





