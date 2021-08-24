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
ms.openlocfilehash: 63099d425b51bfde52eac59771007b1c765acf05
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910423"
---
# <a name="deploying-the-mbam-10-server-infrastructure"></a>MBAM 1.0 서버 인프라 배포


1~5대의 서버를 사용하여 다양한 구성에서 Microsoft BitLocker 관리 및 모니터링(MBAM) 서버 기능을 설치할 수 있습니다. 일반적으로는 확장성 요구에 따라 프로덕션 환경에 3~5개의 서버로 구성해야 합니다. MBAM의 성능 확장성 및 권장되는 배포 토폴로지에 대한 자세한 내용은 MBAM 확장성 및 High-Availability [가이드 백서 를 참조하십시오.](https://go.microsoft.com/fwlink/p/?LinkId=258314)

## <a name="deploy-all-mbam-10-on-a-single-server"></a>단일 서버에 모든 MBAM 1.0 배포


이 구성에서는 모든 MBAM 기능이 단일 서버에 설치됩니다. MBAM 서버 인프라용 이 배포 토폴로지에서는 최대 21,000MBAM 클라이언트 컴퓨터를 지원합니다.

**중요**  
이 구성은 지원되지만 테스트에만 권장됩니다.

 

이 섹션의 절차에서는 단일 서버에 MBAM 기능의 전체 설치에 대해 설명합니다.

[단일 서버에서 MBAM을 설치 및 구성하는 방법](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <a name="deploy-mbam-10-on-distributed-servers"></a>분산 서버에 MBAM 1.0 배포


MBAM 기능은 확장성 요구에 따라 서로 다른 구성으로 설치할 수 있습니다. MBAM 서버 기능 배포를 계획하는 방법에 대한 자세한 내용은 [Planning for MBAM 1.0 Server Deployment을 참조하십시오.](planning-for-mbam-10-server-deployment.md)

이 섹션의 절차에서는 분산 서버에 MBAM 기능의 전체 설치에 대해 설명합니다.

### <a name="three-computer-configuration"></a>3대의 컴퓨터 구성

다음 다이어그램에는 MBAM용 3대의 컴퓨터 배포 토폴로지가 표시됩니다. 최대 55,000MBAM 클라이언트를 지원하는 프로덕션 환경에는 이 토폴로지가 권장됩니다.

![mbam 세 개의 컴퓨터 배포 토폴로지입니다.](images/mbam-3-server.jpg)

이 구성에서 MBAM 기능은 다음 구성으로 설치됩니다.

1.  복구 및 하드웨어 데이터베이스, 준수 및 감사 데이터베이스, 준수 및 감사 보고서가 서버에 설치됩니다.

2.  관리 및 모니터링 서버 기능이 서버에 설치됩니다.

3.  MBAM 그룹 정책 템플릿은 GPO(그룹 정책 개체)를 수정할 수 있는 컴퓨터에 설치됩니다.

### <a name="four-computer-configuration"></a>4대의 컴퓨터 구성

다음 다이어그램에는 MBAM용 4대의 컴퓨터 배포 토폴로지가 표시됩니다. 최대 110,000MBAM 클라이언트를 지원하는 프로덕션 환경에는 이 토폴로지가 권장됩니다.

![mbam 4개의 컴퓨터 배포 토폴로지입니다.](images/mbam-4-computer.jpg)

이 구성에서 MBAM 기능은 다음 구성으로 설치됩니다.

1.  복구 및 하드웨어 데이터베이스, 준수 및 감사 데이터베이스, 준수 및 감사 보고서가 서버에 설치됩니다.

2.  관리 및 모니터링 서버 기능은 NLB(네트워크 부하 분산) 서버 클러스터에 구성된 서버에 설치됩니다.

3.  MBAM 그룹 정책 템플릿은 그룹 정책 개체를 수정할 수 있는 컴퓨터에 설치됩니다.

### <a name="five-computer-configuration"></a>5대의 컴퓨터 구성

다음 다이어그램에는 MBAM용 5대의 컴퓨터 배포 토폴로지가 표시됩니다. 최대 135,000MBAM 클라이언트를 지원하는 프로덕션 환경에는 이 토폴로지가 권장됩니다.

![mbam 5 컴퓨터 배포 토폴로지.](images/mbam-5-computer.jpg)

이 구성에서 MBAM 기능은 다음 구성으로 설치됩니다.

1.  복구 및 하드웨어 데이터베이스가 서버에 설치됩니다.

2.  준수 및 감사 데이터베이스 및 준수 및 감사 보고서가 서버에 설치됩니다.

3.  관리 및 모니터링 서버 기능은 NLB(네트워크 부하 분산) 서버 클러스터에 구성된 서버에 설치됩니다.

4.  MBAM 그룹 정책 템플릿은 그룹 정책 개체를 수정할 수 있는 컴퓨터에 설치됩니다.

[분산 서버에서 MBAM을 설치 및 구성하는 방법](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[MBAM에 대한 네트워크 부하 분산을 구성하는 방법](how-to-configure-network-load-balancing-for-mbam.md)

## <a name="other-resources-for-mbam-10-server-features-deployment"></a>MBAM 1.0 서버 기능 배포를 위한 기타 리소스


[MBAM 1.0 배포](deploying-mbam-10.md)

 

 





