---
title: MBAM 2.5 배포의 예시된 기능
description: MBAM 2.5 배포의 예시된 기능
author: dansimp
ms.assetid: 7b5eff42-af8c-4bd0-a20a-18cc2e779f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 139980fb6712b40685a41bab45610da670803afa
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910623"
---
# <a name="illustrated-features-of-an-mbam-25-deployment"></a>MBAM 2.5 배포의 예시된 기능


이 항목에서는 다음 토폴로지의 Microsoft BitLocker 관리 및 모니터링(MBAM) 2.5 배포를 구성하는 개별 기능에 대해 설명합니다.

-   MBAM 독립 실행형

-   System Center Configuration Manager 통합

**중요**  
이러한 기능은 MBAM 배포에 권장되는 아키텍처를 나타내지 않습니다. 이 정보는 MBAM 배포를 구성하는 개별 기능을 이해하기 위한 가이드로만 사용할 수 있습니다. MBAM에 대한 권장 아키텍처는 [MBAM 2.5용](high-level-architecture-for-mbam-25.md) 고급 아키텍처를 참조합니다.



이 항목에 언급된 지원되는 소프트웨어 버전 목록은 [MBAM 2.5 지원되는 구성을 참조하세요.](mbam-25-supported-configurations.md)

## <a name="mbam-stand-alone-topology"></a><a href="" id="bkmk-standalone"></a> MBAM 독립 실행형 토폴로지


다음 이미지 및 표에서는 MBAM 독립 실행형 토폴로지의 기능에 대해 설명하고 있습니다.

![mbab2\-5.](images/mbam2-5-standalonecomponents.png)

|기능 유형|설명|데이터베이스|
|-|-|-|
|복구 데이터베이스|이 데이터베이스에는 MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터가 저장됩니다.|이 기능은 Windows 실행 서버 및 지원되는 SQL Server 구성됩니다.|
|준수 및 감사 데이터베이스|이 데이터베이스는 호스트에서 사용되는 보고서에 주로 사용되는 준수 SQL Server Reporting Services 저장합니다.|이 기능은 Windows 실행 서버 및 지원되는 SQL Server 구성됩니다.|
|준수 및 감사 보고서|||
|보고 웹 서비스|이 웹 서비스를 사용하면 관리 및 모니터링 웹 사이트와 보고 데이터가 SQL Server 인스턴스 간에 통신할 수 있습니다.|이 기능은 서버가 실행되는 서버에 Windows 설치됩니다.|
|보고 웹 사이트(관리 및 모니터링 웹 사이트)|관리 및 모니터링 웹 사이트에서 보고서를 볼 수 있습니다. 보고서는 기업의 클라이언트 컴퓨터에 대한 복구 감사 및 규정 준수 상태 데이터를 제공합니다.|이 기능은 서버가 실행되는 서버에서 Windows 구성됩니다.|
|SQL Server Reporting Services(SSRS)|보고서는 SSRS 데이터베이스 인스턴스에서 구성됩니다. 보고서는 SSRS 또는 관리 및 모니터링 웹 사이트에서 직접 볼 수 있습니다.|이 기능은 Windows 서버 및 SSRS를 실행하는 지원되는 SQL Server 인스턴스에서 구성됩니다.|
|Self-Service Server|||
|Self-Service 웹 서비스|이 웹 서비스는 MBAM 클라이언트와 관리 및 모니터링 웹 사이트 및 Self-Service 포털에서 복구 데이터베이스와 통신하는 데 사용됩니다.|이 기능은 서버가 실행되는 컴퓨터에 Windows 설치됩니다.|
|Self-Service 웹 사이트(셀프 서비스 포털)|이 웹 사이트를 사용하면 클라이언트 컴퓨터의 최종 사용자가 BitLocker 암호를 분실하거나 잊어버린 경우 웹 사이트에 독립적으로 로그인하여 복구 키를 받을 수 있습니다.|이 기능은 서버가 실행되는 컴퓨터에서 Windows 구성됩니다.|
|관리 및 모니터링 서버|||
|관리 및 모니터링 웹 서비스|모니터링 웹 서비스는 MBAM 클라이언트 및 웹 사이트에서 데이터베이스와 통신하는 데 사용됩니다.|이 기능은 서버가 실행되는 컴퓨터에 Windows 설치됩니다.|

**중요**  
MBAM 클라이언트, 관리 및 모니터링 웹 사이트 및 Self-Service 포털이 복구 데이터베이스와 직접 통신하는 Microsoft BitLocker 관리 및 모니터링(MBAM) 2.5 SP1에서는 Self-Service 웹 서비스를 더 이상 사용할 수 없습니다.

**중요**  
MBAM 클라이언트 및 웹 사이트가 복구 데이터베이스와 직접 통신하기 때문에 모니터링 웹 서비스는 Microsoft BitLocker Administration and Monitoring(MBAM) 2.5 SP1에서 더 이상 사용할 수 없습니다.


## <a name="system-center-configuration-manager-integration-topology"></a><a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager 통합 토폴로지

다음 이미지 및 표에서는 System Center Configuration Manager 통합 토폴로지의 기능에 대해 설명하고 있습니다.

![mbam2\-5.](images/mbam2-5-cmcomponents.png)

**중요**  
MBAM 클라이언트, 관리 및 모니터링 웹 사이트 및 Self-Service 포털이 복구 데이터베이스와 직접 통신하는 Microsoft BitLocker 관리 및 모니터링(MBAM) 2.5 SP1에서는 Self-Service 웹 서비스를 더 이상 사용할 수 없습니다.

**Warning**  
MBAM 클라이언트 및 웹 사이트가 복구 데이터베이스와 직접 통신하기 때문에 모니터링 웹 서비스는 Microsoft BitLocker Administration and Monitoring(MBAM) 2.5 SP1에서 더 이상 사용할 수 없습니다.


|                        기능 유형                        |                                                                                                    설명                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Self-Service Server                     |                                                                                                                                                                                                                   |
|                  Self-Service 웹 서비스                  |                                                 이 웹 서비스는 MBAM 클라이언트 및 Self-Service 포털에서 복구 데이터베이스와 통신하는 데 사용됩니다.                                                  |
|                    Self-Service 웹 사이트                    |                          이 웹 사이트를 사용하면 클라이언트 컴퓨터의 최종 사용자가 BitLocker 암호를 분실하거나 잊어버린 경우 웹 사이트에 독립적으로 로그인하여 복구 키를 받을 수 있습니다.                          |
| 관리 및 모니터링 서버/복구 감사 보고서 |                                                                                                                                                                                                                   |
|         관리 및 모니터링 웹 서비스          |                               이 웹 서비스를 사용하면 관리 및 모니터링 웹 사이트와 보고 데이터가 SQL Server 데이터베이스 간에 통신할 수 있습니다.                               |
|           관리 및 모니터링 웹 사이트            | 복구 감사 보고서는 관리 및 모니터링 웹 사이트에서 볼 수 있습니다. Configuration Manager 콘솔을 사용하여 다른 모든 보고서를 보거나 보고서에서 직접 SQL Server Reporting Services. |
|                         데이터베이스                          |                                                                                                                                                                                                                   |
|                     복구 데이터베이스                      |                                                                 이 데이터베이스에는 MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터가 저장됩니다.                                                                  |
|                       데이터베이스 감사                       |                                                                   이 데이터베이스에는 복구 시도 및 활동에 대한 감사 정보가 저장됩니다.                                                                    |
|               Configuration Manager 기능               |                                                                                                                                                                                                                   |
|          Configuration Manager 관리 콘솔          |                                                                   이 콘솔은 Configuration Manager에 기본 제공되어 있으며 보고서를 보는 데 사용됩니다.                                                                   |
|               Configuration Manager 보고서                |                                                             보고서에는 기업의 클라이언트 컴퓨터에 대한 준수 및 복구 감사 데이터가 표시 됩니다.                                                              |
|               SQL Server Reporting Services                |                                                SSRS는 MBAM 보고서를 사용 가능하게 합니다. 보고서는 SSRS 또는 Configuration Manager 콘솔에서 직접 볼 수 있습니다.                                                 |

## <a name="related-topics"></a>관련 항목

[MBAM 2.5의 개략적인 아키텍처](high-level-architecture-for-mbam-25.md)

[MBAM 2.5 시작](getting-started-with-mbam-25.md)

## <a name="got-a-suggestion-for-mbam"></a>MBAM에 대한 제안이 있나요?
- 여기에 제안을 추가하거나 [투표합니다.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- MBAM 문제의 경우 [MBAM TechNet 포럼 을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




