---
title: 시작 - Configuration Manager를 통해 MBAM 사용
description: 시작 - Configuration Manager를 통해 MBAM 사용
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f23a0eba923608fb6e25e44ee2843f3cde4c2dc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910813"
---
# <a name="getting-started---using-mbam-with-configuration-manager"></a>시작 - Configuration Manager를 통해 MBAM 사용


Microsoft BitLocker 관리 및 모니터링(MBAM)을 설치하면 MBAM을 Configuration Manager 2007 또는 2012 Configuration Manager와 통합하는 System Center 수 있습니다. MBAM에서 지원하는 지원되는 Configuration Manager 버전 목록은 Configuration Manager를 통해 MBAM 배포 계획을 [참조하세요.](planning-to-deploy-mbam-with-configuration-manager-2.md) 통합 토폴로지에서 하드웨어 준수 및 보고 기능은 MBAM에서 제거되고 Configuration Manager에서 액세스됩니다.

**중요**  
Windows To Go는 Configuration Manager 2007과 함께 MBAM의 통합 토폴로지 설치 시 지원되지 않습니다.

 

## <a name="using-mbam-with-configuration-manager"></a>Configuration Manager와 함께 MBAM 사용


MBAM의 통합은 Configuration Manager 2007 또는 System Center 2012 Configuration Manager에 다음 세 항목을 설치하는 새로운 구성 팩을 기반으로 합니다. 이 내용은 다음 섹션에서 자세히 설명합니다.

구성 항목 및 구성 기준으로 구성된 구성 데이터

컬렉션

보고

### <a name="configuration-data"></a>구성 데이터

구성 데이터는 "BitLocker Protection"이라는 구성 기준을 설치합니다. 이 기본 설정에는 "BitLocker 운영 체제 드라이브 보호" 및 "BitLocker 고정 데이터 드라이브 보호"의 두 가지 구성 항목이 포함되어 있습니다. 구성 기준은 MBAM을 설치할 때도 만들어지며 컬렉션에 배포됩니다. 두 구성 항목은 클라이언트 컴퓨터의 준수 상태를 평가하기 위한 기반을 제공합니다. 이 정보는 Configuration Manager에서 캡처, 저장 및 평가됩니다. 구성 항목은 OSD(운영 체제 드라이브) 및 FDD(고정 데이터 드라이브)에 대한 규정 준수 요구 사항을 기반으로 합니다. 배포된 컴퓨터에 대한 필수 세부 정보는 해당 드라이브 유형에 대한 준수를 평가할 수 있도록 수집됩니다. 기본적으로 구성 기준은 12시간마다 준수 상태를 평가하고 구성 관리자에게 준수 데이터를 전송합니다.

### <a name="collection"></a>컬렉션

MBAM은 MBAM 지원 컴퓨터라는 컬렉션을 만듭니다. 구성 기준은 이 컬렉션에 있는 클라이언트 컴퓨터를 대상으로 합니다. 이 컬렉션은 기본적으로 12시간마다 실행되어 구성원 자격을 평가하는 동적 컬렉션입니다. 멤버 자격은 세 가지 기준을 기반으로 합니다.

-   이 버전은 지원되는 버전의 Windows 운영 체제입니다. 현재 MBAM은 Windows 7 Enterprise 및 Windows 7 Ultimate, Windows 8 Enterprise 및 Windows To Go만 지원하며 Windows To Go가 실행되는 Windows 8 Enterprise.

-   이 컴퓨터는 실제 컴퓨터입니다. 가상 컴퓨터는 지원되지 않습니다.

-   TPM(신뢰할 수 있는 플랫폼 모듈)을 사용할 수 있습니다. 호환되는 버전의 TPM 1.2 이상이 7을 사용하려면 Windows 필요합니다. Windows 8 Windows To Go에는 TPM이 필요하지 않습니다.

컬렉션은 모든 컴퓨터에 대해 평가하고 MBAM 통합에 대한 준수 평가 및 보고를 위한 기반을 제공하는 호환되는 컴퓨터의 하위 집합을 만듭니다.

### <a name="reports"></a>보고

규정 준수를 보는 데 사용할 수 있는 보고서는 네 가지입니다. 채널은 다음과 같습니다.

-   **BitLocker 엔터프라이즈 준수** 대시보드 – IT 관리자는 단일 보고서에 대한 세 가지 정보 보기, 준수 상태 배포, 비준수 - 오류 배포 및 드라이브 유형별로 규정 준수 상태 배포를 제공합니다. 보고서의 드릴다운 옵션을 사용하면 IT 관리자가 데이터를 클릭하고 선택한 상태와 일치하는 컴퓨터 목록을 볼 수 있습니다.

-   **BitLocker 엔터프라이즈 규정** 준수 세부 정보 – IT 관리자가 엔터프라이즈의 BitLocker 암호화 준수 상태에 대한 정보를 볼 수 있으며 각 컴퓨터의 규정 준수 상태를 포함합니다. 보고서의 드릴다운 옵션을 사용하면 IT 관리자가 데이터를 클릭하고 선택한 상태와 일치하는 컴퓨터 목록을 볼 수 있습니다.

-   **BitLocker 컴퓨터** 준수 – IT 관리자가 개별 컴퓨터를 보고 특정 상태의 규격 또는 규격이 아닌 것으로 보고된 이유를 확인할 수 있습니다. 또한 이 보고서에는 OSD(운영 체제 드라이브) 및 고정 데이터 드라이브(FDD)의 암호화 상태도 표시됩니다.

-   **BitLocker 엔터프라이즈 준수 요약** – IT 관리자가 MBAM 정책을 사용하여 엔터프라이즈의 준수 상태를 볼 수 있습니다. 각 컴퓨터의 상태가 평가되는 보고서에는 정책에 대한 엔터프라이즈의 모든 컴퓨터 준수 요약이 표시 됩니다. 보고서의 드릴다운 옵션을 사용하면 IT 관리자가 데이터를 클릭하고 선택한 상태와 일치하는 컴퓨터 목록을 볼 수 있습니다.

## <a name="high-level-architecture-of-mbam-with-configuration-manager"></a>High-Level MBAM의 아키텍처 및 구성 관리자


다음 이미지는 Configuration Manager 토폴로지가 있는 MBAM 아키텍처를 보여줍니다. 이 구성은 프로덕션 환경에서 최대 200,000MBAM 클라이언트를 지원합니다.

![구성 관리자를 통해 mbam 아키텍처.](images/mbam2-cmserver.gif)

이 아키텍처의 서버, 데이터베이스 및 기능에 대한 설명은 다음과 같습니다. 아키텍처 이미지의 서버 기능 및 데이터베이스는 설치하는 것이 권장되는 컴퓨터 또는 서버 아래에 나열됩니다.

-   **데이터베이스 서버** - **복구** **데이터베이스,** **** 감사 데이터베이스 및 감사 보고서가 Windows 및 지원되는 SQL Server 인스턴스입니다. 복구 데이터베이스에는 MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터가 저장됩니다. 감사 데이터베이스에는 복구 데이터에 액세스한 클라이언트 컴퓨터에서 수집한 감사 활동 데이터가 저장됩니다. 감사 보고서는 기업에서 클라이언트 컴퓨터의 준수 상태에 대한 데이터를 제공합니다.

-   **Configuration Manager 주** 사이트 서버 - Configuration Manager 서버에는 Configuration Manager 기본 사이트 서버에 설치해야 하는 System Center Configuration Manager 통합 토폴로지가 포함된 MBAM 서버 설치가 포함되어 있습니다. Configuration Manager Server는 클라이언트 컴퓨터에서 하드웨어 인벤토리 정보를 수집하고 클라이언트 컴퓨터의 BitLocker 규정 준수를 보고하는 데 사용됩니다. MBAM 설치 서버 설치를 실행하면 Configuration Manager 기본 사이트 서버에 컬렉션 및 구성 데이터가 설치됩니다.

-   **관리 및** 모니터링 서버 **** - 관리 및 모니터링 서버는 Windows 서버에 설치되어 관리 및 모니터링 웹 사이트와 모니터링 웹 서비스로 구성됩니다. 관리 및 모니터링 웹 사이트는 활동을 감사하고 복구 데이터(예: BitLocker 복구 키)에 액세스하는 데 사용됩니다. 셀프 **서비스 포털은** 관리 및 모니터링 서버에도 설치됩니다. 클라이언트 컴퓨터의 최종 사용자가 BitLocker 암호를 분실하거나 잊어버린 경우 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그온하여 복구 키를 받을 수 있습니다. 감사 보고서는 관리 및 모니터링 서버에도 설치됩니다.

-   **관리 Workstation** - **정책** 템플릿은 BitLocker 드라이브 암호화에 대한 MBAM 구현 설정을 정의하는 그룹 정책 개체로 구성됩니다. 정책 템플릿은 모든 서버 또는 workstation에 설치할 수 있지만 일반적으로 서버 또는 클라이언트 컴퓨터에 지원되는 관리 Windows 설치됩니다. 이 Workstation은 전용 컴퓨터가 아니어도 됩니다.

-   **MBAM 클라이언트** 및 **Configuration Manager 클라이언트** 컴퓨터

    -   **MBAM 클라이언트는** 다음 작업을 수행합니다.

        -   그룹 정책 개체를 사용하여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 암호화를 적용합니다.

        -   운영 체제 드라이브, 고정 데이터 드라이브 및 USB(이동식 데이터) 드라이브의 세 가지 BitLocker 데이터 드라이브 유형에 대한 복구 키를 수집합니다.

        -   클라이언트 컴퓨터에 대한 복구 정보 및 컴퓨터 정보를 수집합니다.

    -   **Configuration Manager 클라이언트** - Configuration Manager 클라이언트를 사용하면 Configuration Manager에서 클라이언트 컴퓨터에 대한 하드웨어 호환성 데이터를 수집하고 Configuration Manager에서 준수 정보를 보고할 수 있습니다.

## <a name="related-topics"></a>관련 항목


[Configuration Manager와 함께 MBAM 사용](using-mbam-with-configuration-manager.md)

 

 





