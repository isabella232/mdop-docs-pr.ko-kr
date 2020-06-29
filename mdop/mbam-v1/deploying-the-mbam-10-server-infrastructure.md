---
title: MBAM 1.0 서버 인프라 배포
description: MBAM 1.0 서버 인프라 배포
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825178"
---
# MBAM 1.0 서버 인프라 배포


하나 ~ 다섯 개의 서버를 사용 하 여 다양 한 구성에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 기능을 설치할 수 있습니다. 일반적으로 사용자의 확장성 요구에 따라 프로덕션 환경에 대해 3 ~ 5 대의 서버 구성을 사용 해야 합니다. MBAM 및 권장 배포 토폴로지의 성능 확장성에 대 한 자세한 내용은 [Mbam 확장성 및 고가용성 가이드 백서](https://go.microsoft.com/fwlink/p/?LinkId=258314)를 참조 하세요.

## 모든 MBAM 1.0를 단일 서버에 배포


이 구성에서는 모든 MBAM 기능이 단일 서버에 설치 됩니다. 이 MBAM 서버 인프라에 대 한이 배포 토폴로지에서는 최대 21000 MBAM 클라이언트 컴퓨터를 지원 합니다.

**중요**  이 구성은 지원 되지만 테스트에만 권장 됩니다.

 

이 섹션의 절차는 모든 MBAM 기능을 단일 서버에 설치 하는 방법을 설명 합니다.

[단일 서버에서 MBAM을 설치 및 구성하는 방법](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## 분산 서버에 MBAM 1.0 배포


MBAM 기능은 사용자의 확장성 요구에 따라 다른 구성으로 설치할 수 있습니다. MBAM 서버 기능 배포를 계획 하는 방법에 대 한 자세한 내용은 [mbam 1.0 서버 배포 계획](planning-for-mbam-10-server-deployment.md)을 참조 하세요.

이 섹션의 절차에서는 분산 서버의 MBAM 기능을 모두 설치 하는 방법에 대해 설명 합니다.

### 3-컴퓨터 구성

다음 다이어그램에는 MBAM에 대 한 세 가지 컴퓨터 배포 토폴로지가 표시 되어 있습니다. 최대 55000 MBAM 클라이언트를 지 원하는 프로덕션 환경에이 토폴로지를 권장 합니다.

![mbam 3 대의 컴퓨터 배포 토폴로지](images/mbam-3-server.jpg)

이 구성에서 MBAM 기능은 다음 구성으로 설치 됩니다.

1.  복구 및 하드웨어 데이터베이스, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 서버에 설치 됩니다.

2.  서버에 관리 및 모니터링 서버 기능이 설치 되어 있습니다.

3.  MBAM 그룹 정책 템플릿은 GPO (그룹 정책 개체)를 수정할 수 있는 컴퓨터에 설치 되어 있습니다.

### 4 컴퓨터 구성

다음 다이어그램에는 MBAM에 대 한 4 개의 컴퓨터 배포 토폴로지가 표시 되어 있습니다. 11만 MBAM 클라이언트를 지 원하는 프로덕션 환경에이 토폴로지를 권장 합니다.

![mbam 4 개의 컴퓨터 배포 토폴로지.](images/mbam-4-computer.jpg)

이 구성에서 MBAM 기능은 다음 구성으로 설치 됩니다.

1.  복구 및 하드웨어 데이터베이스, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 서버에 설치 됩니다.

2.  관리 및 모니터링 서버 기능은 NLB (네트워크 부하 분산) 서버 클러스터에 구성 된 서버에 설치 됩니다.

3.  MBAM 그룹 정책 템플릿은 그룹 정책 개체를 수정할 수 있는 컴퓨터에 설치 되어 있습니다.

### 5 대의 컴퓨터 구성

다음 다이어그램에는 MBAM에 대 한 5 컴퓨터 배포 토폴로지가 표시 되어 있습니다. 최대 135000 MBAM 클라이언트를 지 원하는 프로덕션 환경에이 토폴로지를 권장 합니다.

![mbam 컴퓨터 배포 토폴로지](images/mbam-5-computer.jpg)

이 구성에서 MBAM 기능은 다음 구성으로 설치 됩니다.

1.  복구 및 하드웨어 데이터베이스가 서버에 설치 되어 있습니다.

2.  준수 및 감사 데이터베이스와 규정 준수 및 감사 보고서가 서버에 설치 되어 있습니다.

3.  관리 및 모니터링 서버 기능은 NLB (네트워크 부하 분산) 서버 클러스터에 구성 된 서버에 설치 됩니다.

4.  MBAM 그룹 정책 템플릿은 그룹 정책 개체를 수정할 수 있는 컴퓨터에 설치 되어 있습니다.

[분산 서버에서 MBAM을 설치 및 구성하는 방법](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[MBAM에 대한 네트워크 부하 분산을 구성하는 방법](how-to-configure-network-load-balancing-for-mbam.md)

## MBAM 1.0 서버 기능 배포에 대 한 기타 리소스


[MBAM 1.0 배포](deploying-mbam-10.md)

 

 





