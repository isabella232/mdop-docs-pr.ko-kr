---
title: MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법
description: MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812444"
---
# MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법


이 항목에서는 구성 관리자와 MBAM을 통합 하는 System Center Configuration Manager 통합 토폴로지를 사용 하도록 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 구성 하는 방법에 대해 설명 합니다.

이 지침에서는 다음을 사용 하 여 Configuration Manager 통합을 구성 하는 방법을 설명 합니다.

-   Windows PowerShell cmdlet

-   MBAM 서버 구성 마법사

이 지침은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에서 권장 되는 아키텍처를 기반으로 합니다.

**구성을 시작 하기 전에 다음을 수행 합니다.**

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
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처</a></p></td>
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
<td align="left"><p>MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 토폴로지의 경우, MBAM 서버 소프트웨어를 설치 하는 컴퓨터에 Configuration Manager 콘솔을 설치 해야 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows powershell 필수 구성 요소 검토 (Windows PowerShell cmdlet을 사용 하 여 MBAM 구성에만 해당 하는 경우에만 적용)</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</a></p></td>
</tr>
</tbody>
</table>



**Windows PowerShell을 사용 하 여 Configuration Manager 통합을 구성 하려면**

1.  구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.

2.  **사용-MbamCMIntegration** Windows PowerShell cmdlet을 사용 하 여 보고서를 구성 합니다. 이 cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamCMIntegration**을 입력 하세요.

**마법사를 사용 하 여 System Center Configuration Manager 통합을 구성 하려면**

1.  System Center Configuration Manager 통합 기능을 구성할 서버에서 MBAM 서버 구성 마법사를 시작 합니다. **시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.

2.  **새 기능 추가**를 클릭 하 고 **System Center Configuration Manager 통합**을 선택한 후 **다음**을 클릭 합니다.

    마법사에서 구성 관리자 통합에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.

3.  필수 구성 요소 확인에 성공 하면 **다음** 을 클릭 하 여 계속 합니다. 그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.

4.  마법사에서 필드 값을 입력 하려면 다음 설명을 사용 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">필드</th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>SQL Server Reporting Services 서버</strong></p></td>
    <td align="left"><p>보고 서비스 지점의 역할을 가진 서버의 FQDN (정규화 된 도메인 이름) MBAM Configuration Manager 보고서가 배포 되는 서버입니다.</p>
    <p>서버를 지정 하지 않으면 구성 관리자 보고서가 로컬 서버에 배포 됩니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>SQL Server Reporting Services 인스턴스</strong></p></td>
    <td align="left"><p>Configuration Manager 보고서가 배포 되는 SSRS (SQL Server Reporting Services) 인스턴스의 이름입니다.</p>
    <p>인스턴스를 지정 하지 않으면 Configuration Manager 보고서가 기본 SSRS 인스턴스 이름에 배포 됩니다. 서버에 System Center 2012 Configuration Manager가 설치 되어 있으면 입력 하는 값이 무시 됩니다.</p></td>
    </tr>
    </tbody>
    </table>



5.  **요약** 페이지에서 추가 되는 기능을 검토 합니다.

    **참고**  
    방금 만든 항목의 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기** 및 스크립트 저장을 클릭 합니다.



6.  **추가** 를 클릭 하 여 서버에 Configuration Manager 통합 기능을 추가한 다음 **닫기를**클릭 합니다.



## 관련 항목


[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)

[MBAM 2.5 서버 기능 구성의 유효성 검사](validating-the-mbam-25-server-feature-configuration.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.






