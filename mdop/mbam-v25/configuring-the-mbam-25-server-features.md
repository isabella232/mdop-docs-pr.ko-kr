---
title: MBAM 2.5 서버 기능 구성
description: MBAM 2.5 서버 기능 구성
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823058"
---
# MBAM 2.5 서버 기능 구성


이 정보를 사용 하 여 [mbam 2.5 서버 소프트웨어를 설치한](installing-the-mbam-25-server-software.md)후 Microsoft BitLocker 관리 및 모니터링 (mbam) 2.5 서버 기능을 구성할 시작 합니다. MBAM을 구성 하는 데 사용할 수 있는 방법에는 다음 두 가지가 있습니다.

-   MBAM 서버 구성 마법사

-   Windows PowerShell cmdlet

## MBAM 서버 기능 구성을 시작 하기 전에


MBAM 서버 기능 구성을 시작 하기 전에 다음 단계를 검토 하 고 완료 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">지침을 받을 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM에 권장 되는 아키텍처를 검토 합니다.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">MBAM 2.5의 개략적인 아키텍처</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM에 대해 지원 되는 구성을 검토 합니다.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>각 서버에서 필수 구성 요소를 완성 합니다.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>이 메서드를 사용 하 여 MBAM 서버 기능을 구성 하는 경우 Windows PowerShell을 사용 하 여 필수 구성 요소를 검토 하 여 MBAM 서버 기능을 구성할 수 있습니다.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</a></p></td>
</tr>
</tbody>
</table>

 

## MBAM 서버 기능을 구성 하는 단계


다음 표의 각 행은 [MBAM 2.5에 권장 되는 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에 따라 별도의 서버에서 구성할 기능에 대해 설명 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">설치할 기능</th>
<th align="left">지침을 받을 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>데이터베이스를 구성 합니다.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">MBAM 2.5 데이터베이스를 구성하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>보고서를 구성 합니다.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">MBAM 2.5 보고서를 구성하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 응용 프로그램을 구성 합니다.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>System Center Configuration Manager 통합을 구성 합니다 (해당 하는 경우).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</a></p></td>
</tr>
</tbody>
</table>

 

MBAM 서버 기능 구성에 대 한 이벤트 목록은 [서버 이벤트 로그](server-event-logs.md)를 참조 하세요.



## 관련 항목


MBAM 2.5 서버 기능 구성
 

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




