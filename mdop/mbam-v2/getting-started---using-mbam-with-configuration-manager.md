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
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825168"
---
# 시작 - Configuration Manager를 통해 MBAM 사용


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하는 경우 구성 관리자 2007 또는 SystemCenter2012 ConfigurationManager와 MBAM을 통합 하는 토폴로지를 선택할 수 있습니다. Mbam에서 지원 되는 구성 관리자의 목록은 [구성 관리자로 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요. 통합 토폴로지에서는 하드웨어 준수 및 보고 기능이 MBAM에서 제거 되 고 Configuration Manager에서 액세스 됩니다.

**중요**  Windows To Go는 구성 관리자 2007와 함께 MBAM의 통합 토폴로지를 설치 하는 경우 지원 되지 않습니다.

 

## Configuration Manager와 함께 MBAM 사용


MBAM의 통합은 다음 섹션에서 자세히 설명 하는 구성 관리자 2007 또는 SystemCenter2012 ConfigurationManager에 다음 세 항목을 설치 하는 새 구성 팩을 기반으로 합니다.

구성 항목 및 구성 기준으로 구성 된 구성 데이터

컬렉션

보고

### 구성 데이터

구성 데이터를 통해 "bitlocker 보호" 라고 하는 구성 기준을 설치 하는데, 여기에는 "BitLocker 운영 체제 드라이브 보호" 및 "BitLocker 고정 데이터 드라이브 보호"의 두 가지 구성 항목이 포함 됩니다. 구성 기준은 컬렉션에 배포 되며,이는 MBAM이 설치 되어 있는 경우에도 만들어집니다. 두 개의 구성 항목은 클라이언트 컴퓨터의 준수 상태를 평가 하기 위한 기반을 제공 합니다. 이 정보는 구성 관리자에서 캡처, 저장 및 평가 됩니다. 구성 항목은 os (운영 체제 드라이브) 및 FDDs (탑재형 Data Drives)에 대 한 규정 준수 요구 사항에 기반을 둔 것입니다. 이러한 드라이브 유형에 대 한 준수를 평가할 수 있도록 배포 된 컴퓨터에 대 한 필수 세부 정보가 수집 됩니다. 기본적으로 구성 기준은 12 시간 마다 준수 상태를 평가 하 고 규정 준수 데이터를 구성 관리자에 게 보냅니다.

### 컬렉션

MBAM 지원 컴퓨터 라고 하는 컬렉션을 만듭니다. 구성 기준은이 컬렉션에 있는 클라이언트 컴퓨터를 대상으로 합니다. 기본적으로 12 시간 마다 실행 되며 구성원 자격을 평가 하는 동적 컬렉션입니다. 구성원 자격은 다음 세 가지 조건을 기준으로 합니다.

-   지원 되는 버전의 Windows 운영 체제입니다. 현재 MBAM은 windows 365 enterprise 및 windows 365 to go를 지원 합니다. windows를 Go 할 수 있습니다.

-   물리적 컴퓨터입니다. 가상 머신은 지원 되지 않습니다.

-   TPM (신뢰할 수 있는 플랫폼 모듈)을 사용할 수 있습니다. Windows 7에는 호환 가능한 TPM 1.2 이상 버전이 필요 합니다. Windows 8 및 Windows To Go에는 TPM이 필요 하지 않습니다.

컬렉션은 모든 컴퓨터에 대해 평가 되며 정책 준수 평가와 MBAM 통합에 대 한 보고를 위한 기반을 제공 하는 호환 컴퓨터의 하위 집합을 만듭니다.

### 보고

준수를 보는 데 사용할 수 있는 네 개의 보고서가 있습니다. 채널은 다음과 같습니다.

-   **BitLocker 엔터프라이즈 준수 대시보드** -단일 보고서에 대 한 정보 보기 (준수 상태 배포, 비규격 – 오류 발생), 드라이브 유형별 준수 상태 배포 등의 세 가지 다양 한 보고 정보가 제공 됩니다. 보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.

-   **Bitlocker 엔터프라이즈 준수 세부 정보** – IT 관리자가 엔터프라이즈의 BitLocker 암호화 준수 상태에 대 한 정보를 보고 각 컴퓨터의 준수 상태를 포함할 수 있습니다. 보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.

-   **BitLocker 컴퓨터 준수** – it 관리자가 개별 컴퓨터를 보고 특정 상태의 준수 여부 또는 비규격에 대해 보고 된 이유를 확인할 수 있습니다. 또한이 보고서에는 OSD (운영 체제 드라이브) 및 FDDs (고정식 data drives)의 암호화 상태도 표시 됩니다.

-   **BitLocker Enterprise 준수 요약** -IT 관리자는 mbam 정책을 사용 하 여 엔터프라이즈의 규정 준수 상태를 확인할 수 있습니다. 각 컴퓨터의 상태가 평가 되며,이 보고서에는 정책에 대 한 엔터프라이즈의 모든 컴퓨터 준수에 대 한 요약이 표시 됩니다. 보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.

## 구성 관리자와 함께 MBAM의 상위 수준 아키텍처


다음 이미지는 구성 관리자 토폴로지와 함께 MBAM 아키텍처를 보여 줍니다. 이 구성은 프로덕션 환경에서 최대 20만 MBAM 클라이언트를 지원 합니다.

![구성 관리자를 사용 하 여 mbam 아키텍처](images/mbam2-cmserver.gif)

이 아키텍처의 서버, 데이터베이스 및 기능에 대 한 설명은 다음과 같습니다. 아키텍처 이미지의 서버 기능 및 데이터베이스는 설치 하는 것이 좋습니다. 컴퓨터 또는 서버 아래에 나열 됩니다.

-   **데이터베이스 서버** – **복구 데이터베이스**, **감사 데이터베이스**및 **감사 보고서** 가 Windows Server 및 지원 되는 SQLServer 인스턴스에 설치 됩니다. 복구 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다. 감사 데이터베이스는 복구 데이터에 액세스 한 클라이언트 컴퓨터에서 수집 된 감사 활동 데이터를 저장 합니다. 감사 보고서는 엔터프라이즈에서 클라이언트 컴퓨터의 준수 상태에 대 한 데이터를 제공 합니다.

-   Configuration **Manager 주 사이트 서버** – Configuration manager 서버에 System Center Configuration manager 통합 토폴로지와 함께 mbam 서버 설치가 포함 되어 있으며,이는 configuration manager 기본 사이트 서버에 설치 되어 있어야 합니다. Configuration Manager 서버는 클라이언트 컴퓨터에서 하드웨어 인벤터리 정보를 수집 하 고 클라이언트 컴퓨터의 BitLocker 규격을 보고 하는 데 사용 됩니다. MBAM 설정 서버 설치를 실행 하면 컬렉션 및 구성 데이터가 Configuration Manager 기본 사이트 서버에 설치 됩니다.

-   **관리** 및 모니터링 서버- **관리 및 모니터링 서버** 는 Windows Server에 설치 되며 관리 및 모니터링 웹 사이트와 모니터링 웹 서비스로 구성 됩니다. 관리 및 모니터링 웹 사이트는 활동을 감사 하 고 복구 데이터 (예: BitLocker 복구 키)에 액세스 하는 데 사용 됩니다. **셀프 서비스 포털** 도 관리 및 모니터링 서버에 설치 됩니다. 포털을 사용 하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그인 하 여 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 얻을 수 있습니다. 감사 보고서는 관리 및 모니터링 서버에도 설치 됩니다.

-   **관리 워크스테이션** - **정책 템플릿은** BitLocker 드라이브 암호화에 대 한 mbam 구현 설정을 정의 하는 그룹 정책 개체로 구성 됩니다. 모든 서버 또는 워크스테이션에 정책 템플릿을 설치할 수 있지만, 일반적으로 지원 되는 Windows server 또는 클라이언트 컴퓨터인 관리 워크스테이션에 설치 됩니다. 워크스테이션이 전용 컴퓨터 일 필요는 없습니다.

-   **Mbam 클라이언트** 및 **Configuration Manager 클라이언트** 컴퓨터

    -   **Mbam 클라이언트** 는 다음 작업을 수행 합니다.

        -   그룹 정책 개체를 사용 하 여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 암호화를 적용 합니다.

        -   세 가지 BitLocker 데이터 드라이브 유형 (운영 체제 드라이브, 고정 데이터 드라이브, 이동식 데이터 (USB) 드라이브)에 대 한 복구 키를 수집 합니다.

        -   클라이언트 컴퓨터에 대 한 복구 정보 및 컴퓨터 정보를 수집 합니다.

    -   Configuration manager **클라이언트** – configuration manager 클라이언트를 사용 하 여 클라이언트 컴퓨터에 대 한 하드웨어 호환성 데이터를 수집 하 고 구성 관리자가 준수 정보를 보고할 수 있습니다.

## 관련 항목


[Configuration Manager와 함께 MBAM 사용](using-mbam-with-configuration-manager.md)

 

 





