---
title: UE-V 구성 방법 계획
description: UE-V 구성 방법 계획
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827093"
---
# UE-V 구성 방법 계획


Microsoft UE-V (User Experience Virtualization) 구성은 엔터프라이즈 전체에서 설정을 동기화 하는 방법을 결정 합니다. 이 항목에서는 비즈니스 요구 사항에 가장 적합 한 구성 계획을 공식화 하는 데 도움이 되도록 UE-V 구성을 만드는 방법에 대해 설명 합니다.

## UE-V 용 구성 방법


사용 하는 구성 방법에 따라 에이전트를 설치 하기 전이나 설치한 후에 UE-V를 구성할 수 있습니다.

**그룹 정책:** 기존 그룹 정책 인프라를 사용 하 여 ue-v 에이전트 배포 전 또는 후에 ue-v를 구성할 수 있습니다. UE-V ADMX 서식 파일은 일반적인 UE-V Agent 구성 옵션의 중앙 관리를 가능 하 게 하며 UE-V 동기화를 구성 하는 설정을 포함 합니다. 그룹 정책을 사용 하는 네트워크 환경은 에이전트 배포에 대비 하 여 UE-V를 미리 구성할 수 있습니다.

[그룹 정책 개체를 사용하여 UE-V 구성](configuring-ue-v-with-group-policy-objects.md)

[UE-V 그룹 정책 ADMX 템플릿 설치](installing-the-ue-v-group-policy-admx-templates.md)

**명령줄 또는 배치 스크립트 설치:** ue-v 에이전트 배포와 함께 사용 되는 매개 변수는 여러 ue-v 설정의 구성을 허용 합니다. System Center Configuration Manager와 같은 전자 소프트웨어 배포 시스템에서는 UE-V 에이전트 소프트웨어를 배포 하 고 설치할 때 이러한 매개 변수를 사용 하 여 클라이언트를 구성 합니다. 설치 매개 변수 목록과 샘플 설치 스크립트는 [Ue-v 에이전트 배포](deploying-the-ue-v-agent.md)를 참조 하세요.

**Powershell 및 wmi:** POWERSHELL 또는 wmi를 사용 하는 스크립팅된 명령을 사용 하 여 ue-v agent가 설치 된 후 구성을 수정할 수 있습니다. PowerShell 및 WMI 명령 목록은 [powershell 및 wmi를 사용 하 여 ue-v 1.0 에이전트 및 패키지 관리](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)를 참조 하세요.

**레지스트리 설정 편집:** UE-V 설정은 레지스트리에 저장 되며 RegEdit 등의 레지스트리 설정을 수정할 수 있는 도구를 사용 하 여 수정할 수 있습니다.

**참고**  레지스트리를 수정 하면 데이터가 손실 되거나 컴퓨터가 응답 하지 않을 수 있습니다. 다른 구성 메서드를 사용 하는 것이 좋습니다.

 

### UE-V 구성 설정

다음은 UE-V 구성 설정의 예입니다.

-   **저장소 경로 설정:** ue-v 설정을 저장 하는 파일 공유의 위치를 지정 합니다.

-   **설정 템플릿 카탈로그 경로:** 새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 지정 합니다.

-   **Microsoft 서식 파일 등록:** 설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.

-   **동기화 방법:** Windows 오프 라인 파일 기능을 오프 라인 지원에 사용 하는지 여부를 지정 합니다.

-   **동기화 시간 제한:** 설정 저장소 위치에서 사용자 설정을 검색할 때 시간이 초과 되기 전에 컴퓨터가 대기 하는 시간 (밀리초)을 지정 합니다.

-   **동기화 사용:** ue-v 설정을 동기화 할 수 있는지 여부를 지정 합니다.

-   **최대 패키지 크기:** ue-v agent가 경고를 보고 하는 설정 패키지 파일 임계값 크기 (바이트)를 지정 합니다.

## 관련 항목


[UE-V 1.0 계획](planning-for-ue-v-10.md)

[UE-V 구성 계획](planning-for-ue-v-configuration.md)

 

 





