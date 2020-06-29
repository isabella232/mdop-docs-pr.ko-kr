---
title: MBAM 1.0 배포 계획
description: MBAM 1.0 배포 계획
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823188"
---
# MBAM 1.0 배포 계획


Microsoft BitLocker 관리 및 모니터링 (MBAM) 1.0 배포 계획을 만들기 전에 여러 가지 배포 구성과 필수 구성 요소를 고려해 야 합니다. 이 섹션에는 비즈니스 요구 사항에 가장 적합 한 배포 계획을 공식화 하는 데 필요한 정보를 수집 하기 위한 정보가 포함 되어 있습니다.

## MBAM 1.0 지원 되는 구성 검토


MBAM 클라이언트 및 서버 기능 설치에 대 한 컴퓨팅 환경을 준비한 후에는 MBAM에 대해 지원 되는 구성 정보를 검토 하 여 MBAM을 설치 하는 컴퓨터가 최소 하드웨어 및 운영 체제 요구 사항을 충족 하는지 확인 해야 합니다. MBAM 배포 필수 구성 요소에 대 한 자세한 내용은 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md)를 참조 하세요.

[MBAM 1.0 지원되는 구성](mbam-10-supported-configurations.md)

## MBAM 1.0 서버 및 클라이언트 배포 계획


MBAM 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 서버 기능 집합에 따라 달라 집니다. 이러한 기능은 단일 서버에 설치 하거나 여러 서버에 걸쳐 배포할 수 있습니다.

관리자는 MBAM 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다. Active Directory 도메인 서비스 등의 도구를 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터를 직접 암호화 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.

MBAM을 사용 하면 최종 사용자가 컴퓨터를 받기 전이나 나중에 그룹 정책을 사용 하는 방법으로 조직의 컴퓨터를 암호화할 수 있습니다. 조직에서 하나 또는 두 가지 방법 모두를 사용할 수 있습니다. 두 방법을 모두 사용 하기로 선택 하는 경우 준수, 보고 및 키 복구 지원을 향상 시킬 수 있습니다.

[MBAM 1.0 서버 배포 계획](planning-for-mbam-10-server-deployment.md)

[MBAM 1.0 클라이언트 배포 계획](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>MBAM 계획에 대 한 기타 리소스


-   [MBAM 1.0 계획](planning-for-mbam-10.md)

 

 





