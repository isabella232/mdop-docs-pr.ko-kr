---
title: MBAM 2.0 서버 배포 계획
description: MBAM 2.0 서버 배포 계획
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812612"
---
# MBAM 2.0 서버 배포 계획


MBAM (Microsoft BitLocker 관리 및 모니터링) 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 서버 기능 집합에 따라 달라 집니다. Configuration Manager 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 하는 경우 [구성 관리자를 사용 하 여 MBAM 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.

**참고**  Microsoft BitLocker 관리 및 모니터링을 단일 서버에 설치 하는 것은 테스트 환경에만 적합 합니다.

 

## MBAM 서버 배포 계획


MBAM 서버 배포의 인프라에는 다음 기능이 포함 됩니다.

-   복구 데이터베이스

-   준수 및 감사 데이터베이스

-   규정 준수 및 감사 보고서

-   셀프 서비스 포털

-   관리 및 모니터링 서버

-   MBAM 그룹 정책 서식 파일

MBAM 서버 데이터베이스 및 기능은 확장성 요구 사항에 따라 다른 구성으로 설치할 수 있습니다. 모든 MBAM 서버 기능은 단일 서버에 설치 되거나 여러 서버에 걸쳐 배포 될 수 있습니다. 프로덕션 환경에 대 한 두 서버 구성을 사용 하는 것이 좋으며, 컴퓨팅 요구 사항에 따라 두 개에서 4 개 서버의 구성을 사용할 수도 있습니다.

각 MBAM 기능에는 특정 전제 조건이 있습니다. 전체 서버 기능 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항 목록은 [mbam 2.0 배포 전제 조건](mbam-20-deployment-prerequisites-mbam-2.md) 및 [Mbam 2.0 지원 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.

서버 관련 MBAM 기능 외에도 서버 설정 응용 프로그램에는 MBAM 그룹 정책 서식 파일이 포함 되어 있습니다. 이 서식 파일에는 엔터프라이즈에서 BitLocker 드라이브 암호화를 관리 하도록 구성 된 GPO (그룹 정책 개체) 설정이 포함 되어 있습니다. GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 컴퓨터에이 서식 파일을 설치할 수 있습니다.

MBAM 서버 배포를 계획할 때, 모든 복구 키가 만료 되는 경우 MBAM의 BitLocker 복구 키가 단일 용도로만 사용 됨을 고려해 야 합니다. 키를 사용한 후에 만료 되도록 하려면 지원 센터 포털 또는 셀프 서비스 포털을 통해 검색 해야 합니다.

## MBAM 서버 기능 배포 순서


여러 서버에 MBAM 기능을 배포 하려면 다음 순서로 기능을 설치 해야 합니다.

1.  복구 데이터베이스

2.  준수 및 감사 데이터베이스

3.  준수 감사 및 보고서

4.  셀프 서비스 포털

5.  관리 및 모니터링 서버

6.  MBAM 그룹 정책 서식 파일

**참고**  각 기능을 설치 하는 컴퓨터의 이름을 추적 하세요. 이 정보는 설치 프로세스 전체에서 사용 해야 합니다. 이 작업을 위해 배포 검사 목록을 인쇄 하 고 사용할 수 있습니다. MBAM 배포 검사 목록에 대 한 자세한 내용은 [mbam 2.0 배포 검사 목록을](mbam-20-deployment-checklist-mbam-2.md)참조 하세요.

 

## 관련 항목


[MBAM 2.0 배포 계획](planning-to-deploy-mbam-20-mbam-2.md)

[MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





