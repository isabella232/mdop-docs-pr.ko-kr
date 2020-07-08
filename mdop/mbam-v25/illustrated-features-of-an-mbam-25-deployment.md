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
ms.openlocfilehash: c3b205d4f0b4b18cf8bdbf51982b5a59e5e1b9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812396"
---
# MBAM 2.5 배포의 예시된 기능


이 항목에서는 다음 토폴로지에 대해 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 배포를 구성 하는 개별 기능에 대해 설명 합니다.

-   MBAM 독립 실행형

-   System Center Configuration Manager 통합

**중요**  
이러한 기능은 MBAM을 배포 하는 데 권장 되는 아키텍처를 나타내지는 않습니다. 이 정보를 가이드로만 사용 하 여 MBAM 배포를 구성 하는 개별 기능을 이해할 수 있습니다. MBAM에 대해 권장 되는 아키텍처는 [mbam 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md) 를 참조 하세요.



이 항목에 설명 된 소프트웨어의 지원 되는 버전 목록은 [Mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.

## <a href="" id="bkmk-standalone"></a> MBAM 독립 실행형 토폴로지


다음 이미지 및 표에서는 MBAM 독립 실행형 토폴로지의 기능에 대해 설명 합니다.

![mbab2\-5](images/mbam2-5-standalonecomponents.png)

|기능 유형|설명|데이터베이스|
|-|-|-|
|복구 데이터베이스|이 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.|이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에서 구성 되었습니다.|
|준수 및 감사 데이터베이스|이 데이터베이스는 SQL Server Reporting Services가 호스트 하는 보고서에 주로 사용 되는 규정 준수 데이터를 저장 합니다.|이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에서 구성 되었습니다.|
|규정 준수 및 감사 보고서|||
|보고 웹 서비스|이 웹 서비스를 사용 하면 관리 데이터를 저장 하는 SQL Server 인스턴스 및 관리 및 모니터링 웹 사이트 간 통신이 가능 합니다.|이 기능은 Windows Server를 실행 하는 서버에 설치 되어 있습니다.|
|보고 웹 사이트 (관리 및 모니터링 웹 사이트)|관리 및 모니터링 웹 사이트에서 보고서를 볼 수 있습니다. 보고서는 엔터프라이즈의 클라이언트 컴퓨터에 대 한 복구 감사 및 준수 상태 데이터를 제공 합니다.|이 기능은 Windows Server를 실행 하는 서버에서 구성 되었습니다.|
|SSRS (SQL Server Reporting Services)|보고서는 SSRS 데이터베이스 인스턴스에서 구성 됩니다. 보고서는 SSRS 또는 관리 및 모니터링 웹 사이트에서 직접 볼 수 있습니다.|이 기능은 Windows Server를 실행 하는 서버와 SSRS를 실행 하는 지원 되는 SQL Server 인스턴스를 구성 합니다.|
|셀프 서비스 서버|||
|셀프 서비스 웹 서비스|이 웹 서비스는 MBAM 클라이언트와 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털이 복구 데이터베이스와 통신 하는 데 사용 됩니다.|이 기능은 Windows Server를 실행 하는 컴퓨터에 설치 되어 있습니다.|
|셀프 서비스 웹 사이트 (셀프 서비스 포털)|이 웹 사이트를 사용 하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그인 하 여 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 얻을 수 있습니다.|이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.|
|관리 및 모니터링 서버|||
|관리 및 모니터링 웹 서비스|모니터링 웹 서비스는 MBAM 클라이언트와 웹 사이트에서 데이터베이스와 통신 하는 데 사용 됩니다.|이 기능은 Windows Server를 실행 하는 컴퓨터에 설치 되어 있습니다.|

**중요**  
이 셀프 서비스 웹 서비스는 MBAM 클라이언트, 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털이 복구 데이터베이스와 직접 통신 하는 MBAM (Microsoft BitLocker 관리 및 모니터링) 2.5 SP1에서 더 이상 사용할 수 없습니다.

**중요**  
MBAM 클라이언트와 웹 사이트가 복구 데이터베이스와 직접 통신 하기 때문에 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1에서는 모니터링 웹 서비스를 더 이상 사용할 수 없습니다.


## <a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager 통합 토폴로지

다음 이미지 및 표에서는 System Center Configuration Manager 통합 토폴로지의 기능에 대해 설명 합니다.

![mbam2\-5](images/mbam2-5-cmcomponents.png)

**중요**  
이 셀프 서비스 웹 서비스는 MBAM 클라이언트, 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털이 복구 데이터베이스와 직접 통신 하는 MBAM (Microsoft BitLocker 관리 및 모니터링) 2.5 SP1에서 더 이상 사용할 수 없습니다.

**Warning**  
MBAM 클라이언트와 웹 사이트가 복구 데이터베이스와 직접 통신 하기 때문에 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1에서는 모니터링 웹 서비스를 더 이상 사용할 수 없습니다.


|                        기능 유형                        |                                                                                                    설명                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    셀프 서비스 서버                     |                                                                                                                                                                                                                   |
|                  셀프 서비스 웹 서비스                  |                                                 이 웹 서비스는 MBAM 클라이언트와 셀프 서비스 포털에서 복구 데이터베이스와 통신 하는 데 사용 됩니다.                                                  |
|                    셀프 서비스 웹사이트                    |                          이 웹 사이트를 사용 하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그인 하 여 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 얻을 수 있습니다.                          |
| 관리 및 모니터링 서버/복구 감사 보고서 |                                                                                                                                                                                                                   |
|         관리 및 모니터링 웹 서비스          |                               이 웹 서비스를 사용 하면 관리 데이터를 저장 하는 SQL Server 데이터베이스와 관리 및 모니터링 웹 사이트 간에 통신할 수 있습니다.                               |
|           관리 및 모니터링 웹 사이트            | 복구 감사 보고서는 관리 및 모니터링 웹 사이트에서 볼 수 있습니다. 다른 모든 보고서를 보거나 SQL Server Reporting Services에서 직접 보고서를 보려면 Configuration Manager 콘솔을 사용 합니다. |
|                         데이터베이스                          |                                                                                                                                                                                                                   |
|                     복구 데이터베이스                      |                                                                 이 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.                                                                  |
|                       데이터베이스 감사                       |                                                                   이 데이터베이스는 복구 시도 및 활동에 대 한 감사 정보를 저장 합니다.                                                                    |
|               Configuration Manager 기능               |                                                                                                                                                                                                                   |
|          Configuration Manager 관리 콘솔          |                                                                   이 콘솔은 구성 관리자에 기본 제공 되며 보고서를 보는 데 사용 됩니다.                                                                   |
|               Configuration Manager 보고서                |                                                             보고서는 엔터프라이즈의 클라이언트 컴퓨터에 대 한 규정 준수 및 복구 감사 데이터를 표시 합니다.                                                              |
|               SQL Server Reporting Services                |                                                SSRS는 MBAM 보고서를 사용 하도록 설정 합니다. SSRS 또는 Configuration Manager 콘솔에서 직접 보고서를 볼 수 있습니다.                                                 |

## 관련 항목

[MBAM 2.5의 개략적인 아키텍처](high-level-architecture-for-mbam-25.md)

[MBAM 2.5 시작](getting-started-with-mbam-25.md)

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




