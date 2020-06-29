---
title: MBAM 1.0 서버 배포 계획
description: MBAM 1.0 서버 배포 계획
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812428"
---
# MBAM 1.0 서버 배포 계획


MBAM (Microsoft BitLocker 관리 및 모니터링) 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 서버 기능 집합에 따라 달라 집니다.

## MBAM 서버 배포 계획


다음 MBAM 기능은 MBAM 서버 배포에 대 한 서버 인프라를 나타냅니다.

-   복구 및 하드웨어 데이터베이스

-   준수 및 감사 데이터베이스

-   규정 준수 및 감사 보고서

-   관리 및 모니터링 서버

MBAM 서버 데이터베이스 및 기능은 사용자의 확장성 요구에 따라 다른 구성으로 설치할 수 있습니다. 모든 MBAM 서버 기능은 단일 서버에 설치 되거나 여러 서버에 걸쳐 배포 될 수 있습니다. 일반적으로 실제 요구 사항에 따라 2 개 또는 4 개 서버의 구성을 사용할 수도 있지만, 프로덕션 환경에는 3 대의 서버 또는 5 서버 구성을 사용 하는 것이 좋습니다.

**참고**  MBAM 및 권장 배포 토폴로지의 성능 확장성에 대 한 자세한 내용은의 MBAM 확장성 및 고가용성 가이드 백서 백서를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=258314> .

 

각 MBAM 기능에는 특정 전제 조건이 있습니다. 전체 서버 기능 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항 목록은 [mbam 1.0 배포 전제 조건](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.

서버 관련 MBAM 기능 외에도 서버 설정 응용 프로그램에는 MBAM 그룹 정책 서식 파일이 포함 되어 있습니다. 이 서식 파일은 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 모든 컴퓨터에 설치할 수 있습니다.

## MBAM 서버 기능 배포 순서


MBAM 서버 기능을 배포 하는 경우 다음 순서로 기능을 설치 합니다.

1.  복구 및 하드웨어 데이터베이스

2.  준수 및 감사 데이터베이스

3.  준수 감사 및 보고서

4.  관리 및 모니터링 서버

5.  정책 서식 파일

**참고**  각 기능을 설치 하는 컴퓨터의 이름을 추적 하세요. 이 정보는 설치 프로세스 전체에서 사용 합니다. 배포 검사 목록을 인쇄 하 고 사용 하 여 설치 과정을 도울 수 있습니다. MBAM 배포 검사 목록에 대 한 자세한 내용은 [mbam 1.0 배포 검사 목록을](mbam-10-deployment-checklist.md)참조 하세요.

 

## 관련 항목


[MBAM 1.0 배포 계획](planning-to-deploy-mbam-10.md)

[MBAM 1.0 서버 인프라 배포](deploying-the-mbam-10-server-infrastructure.md)

 

 





