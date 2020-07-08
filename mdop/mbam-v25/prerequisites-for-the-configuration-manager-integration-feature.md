---
title: Configuration Manager 통합 기능의 필수 구성 요소
description: Configuration Manager 통합 기능의 필수 구성 요소
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825013"
---
# Configuration Manager 통합 기능의 필수 구성 요소


System Center Configuration Manager 통합 토폴로지에 MBAM을 배포 하는 경우 [구성 관리자 통합 토폴로지와 함께 mbam 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)에서 설명한 대로 3 서버 아키텍처를 사용 하는 것이 좋습니다. 이 아키텍처는 50만 클라이언트 컴퓨터를 지원할 수 있습니다.

**중요**  
Windows To Go는 Configuration Manager 2007를 사용 중인 경우 Configuration Manager 통합 토폴로지 설치에 대해 지원 되지 않습니다.



## Configuration Manager 통합 기능에 대 한 일반적인 전제 조건


구성 관리자를 사용 하 여 MBAM을 설치 하는 경우 독립 실행형 토폴로지의 필수 구성 요소 외에 다음과 같은 추가 필수 구성 요소가 필요 합니다.

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
<td align="left"><p>Configuration manager 서버는 Configuration Manager 시스템의 기본 사이트입니다.</p></td>
<td align="left"><p>해당 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>하드웨어 인벤터리 클라이언트 에이전트는 Configuration Manager 서버에 있습니다.</p></td>
<td align="left"><p>System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> 구성 관리자에서 하드웨어 인벤토리를 구성 하는 방법을 참조 하세요 </a> .</p>
<p>Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> 사이트의 하드웨어 인벤토리를 구성 하는 방법을 참조 </a> 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 중인 Configuration Manager 버전에 따라 다음 중 하나를 사용할 수 있습니다.</p>
<ul>
<li><p>준수 설정-(System Center 2012 구성 관리자)</p></li>
<li><p>DCM (바람직한 구성 관리) 클라이언트 에이전트 – (구성 관리자 2007)</p></li>
</ul></td>
<td align="left"><p>System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> 구성 관리자에서 준수 설정 구성을 참조 하세요 </a> .</p>
<p>구성 관리자 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> 원하는 구성 관리 클라이언트 에이전트 속성을 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>보고 서비스 지점은 구성 관리자에서 정의 됩니다. SQL Server Reporting Services (SSRS)에 필요 합니다.</p></td>
<td align="left"><p>System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> 구성 관리자의 보고서에 대 한 필수 구성 요소를 참조 하세요 </a> .</p>
<p>Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> SQL Reporting services에 대 한 보고 서비스 지점을 만드는 방법을 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 2007에는 Microsoft .NET Framework 2.0이 필요 합니다.</p></td>
<td align="left"><p>Configuration Manager 2007에서 필요한 DCM (구성 관리) 클라이언트 에이전트는 준수를 보고 하기 위해 .NET Framework 2.0를 필요로 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>.NET Framework 3.5을 설치 하면 .NET Framework 2.0가 자동으로 설치 됩니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Configuration Manager에서 MBAM을 설치 하는 데 필요한 권한


구성 관리자를 사용 하 여 MBAM을 설치 하려면 다음 표에 나열 된 최소 권한을 사용 하는 보안 역할을 가진 Configuration Manager에 관리자가 있어야 합니다. 또한이 표에는 기본 컴퓨터 관리자 권한 이상의 사용자에 게는 MBAM 서버를 설치 하는 데 필요한 권한도 나와 있습니다.

**다음 표의 사용 권한은 두 버전의 Configuration Manager에 모두 적용 됩니다.**

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
<td align="left"><p>SQL Server 인스턴스 로그인 서버 역할:-dbcreator-processadmin</p></td>
<td align="left"><p>- 복구 데이터베이스-감사 데이터베이스</p></td>
</tr>
<tr class="even">
<td align="left"><p>SSRS 인스턴스 권한:-폴더 만들기-보고서 게시</p></td>
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



## .Mof 파일에 대 한 필수 변경 사항


클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면 System Center 2012 Configuration Manager 및 Microsoft System Center Configuration Manager 2007에 대 한 구성. mof 파일과 Sms \ _def .mof 파일을 편집 해야 합니다. 지침은 [Configuration Manager 통합 토폴로지에만 적용 되는 Mbam 2.5 서버 필수 구성 요소](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)를 참조 하세요.



## 관련 항목


[독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





