---
title: DaRT 7.0 배포 계획
description: DaRT 7.0 배포 계획
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821318"
---
# DaRT 7.0 배포 계획


배포 계획을 만들기 전에 고려해 야 하는 여러 가지 배포 구성 및 필수 구성 요소가 있습니다. 이 섹션에는 비즈니스 요구 사항에 가장 적합 한 배포 계획을 공식화 하는 데 필요한 정보를 수집 하기 위한 정보가 포함 되어 있습니다.

Microsoft 진단 및 복구 도구 집합 (DaRT) 7 설치 계획을 수립할 때 다음 사항을 고려 하세요.

-   DaRT를 설치 하는 경우 DaRT 실행과 관련 된 모든 작업을 수행 하는 IT 관리자 컴퓨터에 모든 기능을 설치할 수 있습니다. 또는 IT 관리자 컴퓨터에서 복구 이미지를 만드는 DaRT 기능만 설치할 수 있습니다. 그런 다음 기술 지원팀 에이전트 컴퓨터에서 dart **원격 연결 뷰어** 및 **충돌 분석기**와 같은 dart를 실행 하는 데 사용 되는 기능을 설치 합니다.

-   DaRT를 원격으로 실행할 수 있으려면 헬프데스크 에이전트 컴퓨터와 원격으로 문제를 해결할 수 있는 모든 컴퓨터가 동일한 네트워크에 있는지 확인 합니다.

-   DaRT를 프로덕션으로 배포 하기 전에 먼저 테스트를 위해 랩 환경을 만들 수 있습니다. 테스트 랩에는 IT 관리자/헬프데스크 에이전트 컴퓨터 역할을 하는 최소 두 개의 컴퓨터와 최종 사용자 컴퓨터 역할을 하는 컴퓨터가 포함 되어야 합니다. 또는 IT 관리자 책임을 헬프데스크 에이전트의 책임과 구분 하려는 경우 연구실에서 세 대의 컴퓨터를 사용할 수 있습니다.

## 지원 되는 구성 검토


Microsoft 진단 및 복구 도구 집합 (DaRT) 7 지원 구성 정보를 검토 하 여 클라이언트 또는 기능 설치를 위해 선택한 컴퓨터가 최소 하드웨어 및 운영 체제 요구 사항을 충족 하는지 확인 해야 합니다.

[DaRT 7.0 지원되는 구성](dart-70-supported-configurations-dart-7.md)

## DaRT 복구 이미지 만들기 계획


DaRT 복구 이미지를 만들 때는 이미지에 포함할 도구를 결정 해야 합니다. 이러한 결정을 내릴 때는 최종 사용자가 다양 한 DaRT 도구에 액세스할 수 있다는 점에 유의 해야 합니다. 복구 이미지를 만들 때 추가 드라이버 또는 파일을 포함할지 여부도 지정 합니다. DaRT 복구 이미지에 포함 하려는 추가 드라이버 또는 파일의 위치를 확인 합니다.

DaRT 복구 이미지를 만들기 위한 전제 조건과 기타 추가 계획 권장 사항을 알고 있어야 합니다.

[DaRT 7.0 복구 이미지 만들기 계획](planning-to-create-the-dart-70-recovery-image.md)

## DaRT 복구 이미지 저장 및 배포 계획


여러 메서드를 사용 하 여 DaRT 복구 이미지를 저장 하 고 배포할 수 있습니다. 사용할 방법을 결정할 때는 각각의 장점과 단점을 고려해 야 합니다. 또한 enterprise에서 DaRT를 사용 하는 방법도 고려해 야 합니다.

**참고**  조직에서 두 개 이상의 메서드를 사용 하는 것이 좋습니다. 예를 들어 대부분의 경우 원격 파티션에서 DaRT로 부팅 하 고 최종 사용자 컴퓨터가 네트워크에 연결할 수 없는 경우 USB 플래시 드라이브를 사용할 수 있습니다.

 

[DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## DaRT 배포 계획을 위한 기타 리소스


[DaRT 7.0 계획](planning-for-dart-70-new-ia.md)

 

 





