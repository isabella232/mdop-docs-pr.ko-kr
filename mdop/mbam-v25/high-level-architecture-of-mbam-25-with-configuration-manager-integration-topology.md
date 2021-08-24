---
title: Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
description: Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: a0f9349391794100a670e382bb18d0713f4b5b60
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910723"
---
# <a name="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology"></a>Configuration Manager 통합 토폴로지가 있는 MBAM 2.5의 개성 높은 아키텍처

이 항목에서는 Configuration Manager 통합 토폴로지와 함께 Microsoft BitLocker 관리 및 모니터링(MBAM)을 배포하기 위한 권장 아키텍처에 대해 설명합니다. 이 토폴로지에서는 MBAM과 MBAM을 System Center Configuration Manager. 독립 실행형 토폴로지로 MBAM을 배포하는 경우 독립 실행형 토폴로지가 [있는 MBAM 2.5의 고급 아키텍처를 참조합니다.](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

이 항목에 언급된 지원되는 소프트웨어 버전 목록은 [MBAM 2.5 지원되는 구성을 참조하세요.](mbam-25-supported-configurations.md)

**중요**  
Windows To Go는 Configuration Manager 2007을 사용하는 경우 Configuration Manager 통합 토폴로지 설치에 지원되지 않습니다.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>권장되는 서버 수 및 지원되는 클라이언트 수


프로덕션 환경에서 권장되는 서버 수 및 지원되는 클라이언트 수는 다음과 같습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">권장 아키텍처</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>서버 및 기타 컴퓨터 수</p></td>
<td align="left"><p>서버 3개</p>
<p>하나의 workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원되는 클라이언트 컴퓨터 수</p></td>
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="differences-between-configuration-manager-integration-and-stand-alone-topologies"></a>Configuration Manager 통합과 독립 실행형 토폴로지의 차이점


토폴로지의 주요 차이점은 다음입니다.

-   규정 준수 및 보고 기능은 MBAM에서 제거되고 Configuration Manager에서 액세스됩니다.

-   MBAM 관리 및 모니터링 웹 사이트에서 계속 보는 복구 감사 보고서를 제외하고는 Configuration Manager 관리 콘솔에서 보고서를 볼 수 있습니다.

## <a name="recommended-mbam-high-level-architecture-with-the-configuration-manager-integration-topology"></a>Configuration Manager 통합 토폴로지로 권장되는 MBAM 고급 아키텍처


다음 다이어그램 및 표에서는 Configuration Manager 통합 토폴로지가 있는 MBAM에 권장되는 고급 아키텍처에 대해 설명하고 있습니다. MBAM 다중 포리스트 배포에는 단 방법 또는 양측 트러스트가 필요합니다. 단방 트러스트의 경우 서버 도메인이 클라이언트 도메인을 트러스트해야 합니다.

![mbam2\-5.](images/mbam2-5-cmserver.png)

### <a name="database-server"></a>데이터베이스 서버

#### <a name="recovery-database"></a>복구 데이터베이스

이 기능은 Windows Server를 실행하는 컴퓨터에서 구성되고 지원되는 SQL Server 인스턴스입니다.

복구 **데이터베이스에는** MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터가 저장됩니다.

#### <a name="audit-database"></a>감사 데이터베이스

이 기능은 Windows Server를 실행하는 컴퓨터에서 구성되고 지원되는 SQL Server 인스턴스입니다.

감사 **데이터베이스에는** 복구 데이터에 액세스한 클라이언트 컴퓨터에서 수집한 감사 활동 데이터가 저장됩니다.

#### <a name="reports"></a>보고

이 기능은 Windows Server를 실행하는 컴퓨터에서 구성되고 지원되는 SQL Server 인스턴스입니다.

**보고서는** 기업의 클라이언트 컴퓨터에 대한 복구 감사 데이터를 제공합니다. Configuration Manager 콘솔에서 보고서를 보거나 보고서에서 직접 볼 SQL Server Reporting Services.

### <a name="configuration-manager-primary-site-server"></a>Configuration Manager 기본 사이트 서버

System Center Configuration Manager 통합 기능

-   이 기능은 Configuration Manager 인프라의 최상위 계층 서버인 Configuration Manager 주 사이트 서버에 구성됩니다.

-   **Configuration Manager Server는** 클라이언트 컴퓨터에서 하드웨어 인벤토리 정보를 수집하고 클라이언트 컴퓨터의 BitLocker 규정 준수를 보고하는 데 사용됩니다.

-   Microsoft BitLocker 관리 및 모니터링 설치 마법사를 실행하여 서버 소프트웨어를 설치하면 MBAM 지원 컴퓨터 컬렉션, 구성 기준 및 보고서가 Configuration Manager 기본 사이트 서버에 구성됩니다.

-   **Configuration Manager 콘솔은** MBAM Server 소프트웨어를 설치하는 컴퓨터와 동일한 컴퓨터에 설치해야 합니다.

### <a name="administration-and-monitoring-server"></a>관리 및 모니터링 서버

#### <a name="administration-and-monitoring-website"></a>관리 및 모니터링 웹 사이트

이 기능은 서버가 실행되는 컴퓨터에서 Windows 구성됩니다.

관리 **및 모니터링 웹 사이트는** 다음에 사용됩니다.

-   최종 사용자가 잠겨 있는 경우 해당 컴퓨터에 다시 액세스할 수 있도록 합니다. 웹 사이트의 이 영역을 일반적으로 Help Desk라고 합니다.

-   클라이언트 컴퓨터의 복구 활동을 보여 주며 복구 감사 보고서를 시청합니다. 다른 보고서는 Configuration Manager 콘솔에서 볼 수 있습니다.

#### <a name="self-service-portal"></a>셀프 서비스 포털

이 기능은 서버가 실행되는 컴퓨터에서 Windows 구성됩니다.

셀프 서비스 **포털은** 클라이언트 컴퓨터의 최종 사용자가 BitLocker 암호를 분실하거나 잊어버린 경우 복구 키를 받을 수 있도록 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그온할 수 있도록 하는 웹 사이트입니다.

#### <a name="monitoring-web-services-for-this-website"></a>이 웹 사이트에 대한 웹 서비스 모니터링

이 기능은 서버가 실행되는 컴퓨터에 Windows 설치됩니다.

모니터링 **웹 서비스는** MBAM 클라이언트 및 웹 사이트에서 데이터베이스와 통신하는 데 사용됩니다.

**중요**<br>MBAM 웹 사이트가 복구 데이터베이스와 직접 통신하기 때문에 모니터링 웹 서비스는 Microsoft BitLocker Administration and Monitoring(MBAM) 2.5 SP1에서 더 이상 사용할 수 없습니다. 

 

### <a name="management-workstation"></a>관리 workstation

#### <a name="mbam-group-policy-templates"></a>MBAM 그룹 정책 템플릿

-   **MBAM 그룹** 정책 템플릿은 BitLocker 드라이브 암호화를 관리할 수 있도록 MBAM의 구현 설정을 정의하는 그룹 정책 설정입니다.

-   MBAM을 실행하기 전에 MDOP 그룹 [정책(.admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) 템플릿을 다운로드하는 방법에서 그룹 정책 템플릿을 다운로드하여 지원되는 Windows Server 또는 Windows 운영 체제를 실행하는 서버 또는 Windows 합니다.

    **참고**<br>이 Workstation은 전용 컴퓨터가 아니어도 됩니다.

     

### <a name="mbam-client-and-configuration-manager-client-computer"></a>MBAM 클라이언트 및 Configuration Manager 클라이언트 컴퓨터

#### <a name="mbam-client-software"></a>MBAM 클라이언트 소프트웨어

**MBAM 클라이언트:**

-   그룹 정책 개체를 사용하여 엔터프라이즈의 클라이언트 컴퓨터에 BitLocker 드라이브 암호화를 적용합니다.

-   운영 체제 드라이브, 고정 데이터 드라이브 및 이동식(USB) 데이터 드라이브의 세 가지 데이터 드라이브 유형에 대한 BitLocker 복구 키를 수집합니다.

-   클라이언트 컴퓨터에 대한 복구 정보 및 컴퓨터 정보를 수집합니다.

#### <a name="configuration-manager-client"></a>구성 관리자 클라이언트

**Configuration Manager 클라이언트를 사용하면** Configuration Manager가 클라이언트 컴퓨터에 대한 하드웨어 호환성 데이터를 수집하고 준수 정보를 보고할 수 있습니다.

 

## <a name="differences-in-mbam-deployment-for-supported-configuration-manager-versions"></a>지원되는 Configuration Manager 버전에 대한 MBAM 배포의 차이점


Configuration Manager 통합 토폴로지와 함께 MBAM을 배포할 때 기본 사이트 서버에 MBAM을 설치할 수 있습니다. 그러나 MBAM 설치는 2012 Configuration Manager System Center Configuration Manager 2007에서 다르게 작동합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration Manager 버전</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p>
<p>System Center 2012 Configuration Manager</p></td>
<td align="left"><p>기본 사이트 서버 또는 중앙 관리 서버에 MBAM을 설치하면 MBAM이 해당 사이트 서버에서 모든 설치 작업을 수행하게 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007 R2</p>
<p>Configuration Manager 2007</p></td>
<td align="left"><p>중앙 사이트 상위 서버가 있는 더 큰 Configuration Manager 계층 구조의 일부인 기본 사이트 서버에 MBAM을 설치하는 경우 MBAM은 중앙 사이트 상위 서버를 식별하고 해당 상위 서버에서 모든 설치 작업을 수행합니다. 설치에는 선행 구성표 확인 및 Configuration Manager 개체 및 보고서 설치가 포함됩니다.</p>
<p>예를 들어 중앙 사이트 상위 서버의 자식인 기본 사이트 서버에 MBAM을 설치하면 MBAM은 상위 서버에 모든 Configuration Manager 개체 및 보고서를 설치합니다. 상위 서버에 MBAM을 설치하면 MBAM은 해당 상위 서버에서 모든 설치 작업을 수행합니다.</p></td>
</tr>
</tbody>
</table>

 

## <a name="how-mbam-works-with-configuration-manager"></a>Configuration Manager에서 MBAM이 작동하는 방식


MBAM과 Configuration Manager의 통합은 다음 표에 설명된 항목을 설치하는 구성 팩을 기반으로 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration Manager에 설치된 항목</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>구성 데이터</p></td>
<td align="left"><p>구성 데이터는 다음 두 가지 구성 항목을 포함하는 "BitLocker Protection"이라는 구성 기준을 설치합니다.</p>
<ul>
<li><p>BitLocker 운영 체제 드라이브 보호</p></li>
<li><p>BitLocker 고정 데이터 드라이브 보호</p></li>
</ul>
<p>구성 기준은 MBAM을 설치할 때도 생성되는 MBAM Supported Computers 컬렉션에 배포됩니다.</p>
<p>두 구성 항목은 클라이언트 컴퓨터의 준수 상태를 평가하기 위한 기반을 제공합니다. 이 정보는 Configuration Manager에서 캡처, 저장 및 평가됩니다.</p>
<p>구성 항목은 운영 체제 드라이브 및 고정 데이터 드라이브에 대한 규정 준수 요구 사항을 기반으로 합니다. 배포된 컴퓨터에 대한 필수 세부 정보는 해당 드라이브 유형에 대한 준수를 평가할 수 있도록 수집됩니다.</p>
<p>기본적으로 구성 기준은 12시간마다 준수 상태를 평가하고 구성 관리자에게 준수 데이터를 전송합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 지원되는 컴퓨터 컬렉션</p></td>
<td align="left"><p>MBAM은 MBAM 지원 컴퓨터라는 컬렉션을 만듭니다. 구성 기준은 이 컬렉션에 있는 클라이언트 컴퓨터를 대상으로 합니다.</p>
<p>이 컬렉션은 동적 컬렉션입니다. 기본적으로 12시간마다 실행되어 다음 세 가지 기준에 따라 멤버십을 평가합니다.</p>
<ul>
<li><p>컴퓨터가 지원되는 버전의 Windows 운영 체제입니다.</p></li>
<li><p>컴퓨터가 실제 컴퓨터입니다. 가상 컴퓨터는 지원되지 않습니다.</p></li>
<li><p>컴퓨터에 사용할 수 있는 TPM(신뢰할 수 있는 플랫폼 모듈)이 있습니다. 호환되는 버전의 TPM 1.2 이상이 7을 사용하려면 Windows 필요합니다. Windows 10, Windows 8.1, Windows 8 및 Windows To Go에는 TPM이 필요하지 않습니다.</p></li>
</ul>
<p>컬렉션은 모든 컴퓨터에 대해 평가하며 호환되는 컴퓨터의 하위 집합이 만들어지며, MBAM 통합에 대한 규정 준수 평가 및 보고를 위한 기반을 제공합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>보고</p></td>
<td align="left"><p>Configuration Manager 통합 토폴로지로 MBAM을 구성하면 복구 감사 보고서를 제외한 Configuration Manager의 모든 보고서가 표시됩니다. 이 보고서는 MBAM 관리 및 모니터링 웹 사이트에서 계속 표시됩니다. Configuration Manager에서 사용할 수 있는 보고서는 다음입니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">보고서</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>BitLocker 엔터프라이즈 준수 대시보드</p></td>
<td align="left"><p>IT 관리자에게 단일 보고서의 세 가지 정보 보기, 즉 규정 준수 상태 배포, 비준수 - 오류 배포 및 드라이브 유형별로 규정 준수 상태 배포를 제공합니다. 보고서의 드릴다운 옵션을 통해 IT 관리자는 데이터를 클릭하고 선택한 상태와 일치하는 컴퓨터 목록을 볼 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker 엔터프라이즈 규정 준수 세부 정보</p></td>
<td align="left"><p>IT 관리자가 엔터프라이즈의 BitLocker 암호화 준수 상태에 대한 정보를 볼 수 있도록 하여 각 컴퓨터의 준수 상태를 포함합니다. 보고서의 드릴다운 옵션을 통해 IT 관리자는 데이터를 클릭하고 선택한 상태와 일치하는 컴퓨터 목록을 볼 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker 컴퓨터 준수</p></td>
<td align="left"><p>IT 관리자가 개별 컴퓨터를 보고 규격 상태 또는 규격이 아닌 상태로 보고된 이유를 확인할 수 있습니다. 또한 이 보고서에는 운영 체제 드라이브 및 고정 데이터 드라이브의 암호화 상태도 표시됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker 엔터프라이즈 준수 요약</p></td>
<td align="left"><p>IT 관리자가 엔터프라이즈에서 MBAM 정책 준수 상태를 볼 수 있도록 합니다. 각 컴퓨터의 상태가 평가되는 보고서에는 정책에 대한 엔터프라이즈의 모든 컴퓨터 준수 요약이 표시 됩니다. 보고서의 드릴다운 옵션을 통해 IT 관리자는 데이터를 클릭하고 선택한 상태와 일치하는 컴퓨터 목록을 볼 수 있습니다.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <a name="related-topics"></a>관련 항목


[MBAM 2.5 시작](getting-started-with-mbam-25.md)

[독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[MBAM 2.5 배포의 예시된 기능](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <a name="got-a-suggestion-for-mbam"></a>MBAM에 대한 제안이 있나요?
- 여기에 제안을 추가하거나 [투표합니다.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- MBAM 문제의 경우 [MBAM TechNet 포럼 을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




