---
title: 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
description: 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9ec9b1e4391fde3083564f34b5f89d1c5bd174f7
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910673"
---
# <a name="high-level-architecture-of-mbam-25-with-stand-alone-topology"></a>독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처


이 항목에서는 Configuration Manager 독립 실행형 토폴로지로 Microsoft BitLocker 관리 및 모니터링(MBAM)을 배포하기 위한 권장 아키텍처에 대해 설명합니다. 이 토폴로지에서 MBAM은 독립 실행형 제품으로 배포됩니다. 또는 Configuration Manager와 MBAM을 통합하는 Configuration Manager 통합 토폴로지를 사용하여 MBAM을 배포할 수 있습니다. 자세한 내용은 Configuration Manager 통합 토폴로지가 있는 [MBAM 2.5의 고급 아키텍처를 참조하세요.](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

이 항목에 언급된 지원되는 소프트웨어 버전 목록은 [MBAM 2.5 지원되는 구성을 참조하세요.](mbam-25-supported-configurations.md)

**참고**  
테스트 환경에서만 단일 서버 아키텍처를 사용하는 것이 좋습니다.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>권장되는 서버 수 및 지원되는 클라이언트 수


프로덕션 환경에서 권장되는 서버 수 및 지원되는 클라이언트 수는 다음과 같습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">프로덕션 환경의 권장 아키텍처</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>서버 및 기타 컴퓨터 수</p></td>
<td align="left"><p>서버 2개</p>
<p>하나의 workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원되는 클라이언트 컴퓨터 수</p></td>
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="recommended-mbam-high-level-architecture-with-the-stand-alone-topology"></a>독립 실행형 토폴로지가 있는 권장 MBAM 고급 아키텍처


다음 다이어그램 및 표에서는 독립 실행형 토폴로지가 있는 MBAM에 대해 권장되는 높은 수준의 두 서버 아키텍처에 대해 설명하고 있습니다. MBAM 다중 포리스트 배포에는 단 방법 또는 양측 트러스트가 필요합니다. 단방 트러스트의 경우 서버 도메인이 클라이언트 도메인을 트러스트해야 합니다.

![mbam2.](images/mbam2-5-2servers.png)

이 서버에서 구성할 서버 기능 설명 데이터베이스 서버

준수 및 감사 데이터베이스

이 기능은 Windows 실행 서버에서 구성되고 지원되는 SQL Server 인스턴스입니다.

준수 **및 감사 데이터베이스는** 주로 호스트를 구성하는 보고서에 사용되는 준수 SQL Server Reporting Services 저장합니다.

복구 데이터베이스

이 기능은 Windows 실행 서버에서 구성되고 지원되는 SQL Server 인스턴스입니다.

복구 **데이터베이스에는** MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터가 저장됩니다.

보고

이 기능은 Windows 실행 서버에서 구성되고 지원되는 SQL Server 인스턴스입니다.

**보고서는** 기업의 클라이언트 컴퓨터에 대한 복구 감사 및 규정 준수 상태 데이터를 제공합니다. 관리 및 모니터링 웹 사이트에서 보고서에 액세스하거나 보고서에서 직접 액세스할 SQL Server Reporting Services.

관리 및 모니터링 서버

관리 및 모니터링 웹 사이트

이 기능은 서버가 실행되는 컴퓨터에서 Windows 구성됩니다.

관리 **및 모니터링 웹 사이트는** 다음에 사용됩니다.

-   최종 사용자가 잠겨 있는 경우 해당 컴퓨터에 다시 액세스할 수 있도록 합니다. 웹 사이트의 이 영역을 일반적으로 Help Desk라고 합니다.

-   클라이언트 컴퓨터의 준수 상태 및 복구 활동을 표시하는 보고서를 볼 수 있습니다.

Self-Service 포털

이 기능은 서버가 실행되는 컴퓨터에서 Windows 구성됩니다.

셀프 서비스 **포털은** 클라이언트 컴퓨터의 최종 사용자가 BitLocker 암호를 분실하거나 잊어버린 경우 복구 키를 받을 수 있도록 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그온할 수 있도록 하는 웹 사이트입니다.

이 웹 사이트에 대한 웹 서비스 모니터링

이 기능은 서버가 실행되는 컴퓨터에서 Windows 구성됩니다.

모니터링 **웹 서비스는** MBAM 클라이언트 및 웹 사이트에서 데이터베이스와 통신하는 데 사용됩니다.

**중요**  
MBAM 웹 사이트가 복구 데이터베이스와 직접 통신하기 때문에 모니터링 웹 서비스는 Microsoft BitLocker Administration and Monitoring(MBAM) 2.5 SP1에서 더 이상 사용할 수 없습니다.

 

관리 workstation

MBAM 그룹 정책 템플릿

-   MBAM 그룹 정책 템플릿은 BitLocker 드라이브 암호화를 관리할 수 있도록 MBAM의 구현 설정을 정의하는 그룹 정책 설정입니다.

-   MBAM을 실행하기 전에 MDOP 그룹 [정책(.admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) 템플릿을 다운로드하는 방법에서 그룹 정책 템플릿을 다운로드하여 지원되는 Windows Server 또는 Windows 운영 체제를 실행하는 서버 또는 Windows 합니다.

-   이 Workstation은 전용 컴퓨터가 아니어도 됩니다.

MBAM 클라이언트 및 Configuration Manager 클라이언트 컴퓨터

MBAM 클라이언트 소프트웨어

MBAM 클라이언트:

-   그룹 정책 개체를 사용하여 엔터프라이즈의 클라이언트 컴퓨터에 BitLocker 드라이브 암호화를 적용합니다.

-   운영 체제 드라이브, 고정 데이터 드라이브 및 이동식(USB) 데이터 드라이브의 세 가지 데이터 드라이브 유형에 대한 Bitlocker 복구 키를 수집합니다.

-   클라이언트 컴퓨터에 대한 복구 정보 및 컴퓨터 정보를 수집합니다.



## <a name="related-topics"></a>관련 항목


[MBAM 2.5 시작](getting-started-with-mbam-25.md)

[Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[MBAM 2.5 배포의 예시된 기능](illustrated-features-of-an-mbam-25-deployment.md)

 

## <a name="got-a-suggestion-for-mbam"></a>MBAM에 대한 제안이 있나요?
- 여기에 제안을 추가하거나 [투표합니다.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- MBAM 문제의 경우 [MBAM TechNet 포럼 을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam) 





