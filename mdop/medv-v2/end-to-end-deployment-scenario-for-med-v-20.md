---
title: MED-V 2.0에 대한 종단 간 배포 시나리오
description: MED-V 2.0에 대한 종단 간 배포 시나리오
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826173"
---
# MED-V 2.0에 대한 종단 간 배포 시나리오


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0의이 샘플 시나리오는 여러 시나리오를 통해 종단간 구성 요소를 배포 하는 데 도움이 됩니다. 이 샘플 시나리오는 개별 시나리오 및 절차를 컨텍스트에 추가할 수 있도록 하는 사례 연구를 통해 생각 하면 됩니다.

이 섹션에서는 엔터프라이즈의 종단간 솔루션으로 MED-V 구성 요소를 배포 하는 데 필요한 기본 정보와 지침을 제공 합니다.

## MED-V 배포 단계별 시나리오


이 단계별 시나리오의 항목에는 다음이 포함 됩니다.

-   [Med-v 2.0 지원 되는 구성](med-v-20-supported-configurations.md) 환경에서 Microsoft 엔터프라이즈 데스크톱 가상화 (med-v) 2.0을 설치 하 고 실행 하는 데 필요한 요구 사항에 대해 설명 합니다. 이 항목에서는 운영 체제 요구 사항, 구성 요구 사항 및 MED-V 작업 영역 요구 사항을 지정 합니다. 이 항목에는 MED-V 2.0에서 지 원하는 언어에 대 한 지역화 정보도 포함 되어 있습니다.

-   [Med-v 2.0 배포 개요](med-v-20-deployment-overview.md) 엔터프라이즈 전체에 med-v를 설치 하 고 배포 하는 데 도움이 되는 일반적인 정보와 지침에 대해 설명 합니다. MED-V 구성 요소는 클라이언트 기반 이며 기존 엔터프라이즈 인프라 및 프로세스를 사용 하 여 전달 하 고 관리 합니다. 이 항목에서는 MED-V 설치 파일 및 배포 하는 MED-V 구성 요소에 대 한 정보를 포함 하는 MED-V 솔루션에 대 한 개요를 제공 합니다. 이 항목에서는 MED-V 설치 및 배포 프로세스에 대 한 개략적인 수준의 개요도 제공 합니다.

-   [Med-v에 대 한 배포 환경 준비](prepare-the-deployment-environment-for-med-v.md) med-v 2.0 배포를 위해 환경을 준비 하는 방법에 대해 설명 합니다. 이 섹션에서는 Microsoft Windows 7 및 그룹 정책을 사용 하 여 운영 체제, 응용 프로그램 및 사용자 설정의 중앙 집중화 된 관리 및 구성을 제공 하는 Active Directory 인프라와 같은 MED-V 환경에 필요한 필수 구성 요소에 대해 설명 합니다. 또한이 섹션에서는 Windows 가상 PC 및 필요한 Windows 가상 PC 업데이트와 같이 엔터프라이즈 전체에 MED-V 2.0를 설치 하 고 배포 하기 위해 가져야 하는 필수 구성 요소에 대해 설명 합니다.

-   [Med-v 구성 요소 배포](deploy-the-med-v-components.md) 엔터프라이즈 전체에 필요한 모든 설치 파일과 med-v 구성 요소를 설치할 수 있는 다양 한 방법을 설명 합니다. MED-V를 설치 및 배포 하려면 일반적으로 다음 단계를 수행 합니다.

    1.  Med-v 작업 영역 패키지를 작성 하는 데 사용 하는 관리자 컴퓨터에 **Med-v 작업 영역 포장기** 를 설치 합니다. 자세한 내용은 [Med-v 작업 영역 포장기를 설치 하는 방법을](how-to-install-the-med-v-workspace-packager.md)참조 하세요.

    2.  MED-V 작업 영역 패키지를 만들고 테스트 합니다. 자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md) 및 [Med-v 작업 영역 패키지 테스트](testing-the-med-v-workspace-package.md)를 참조 하세요.

    3.  회사의 기존 응용 프로그램 배포 방법을 사용 하 여 엔터프라이즈 전체에 MED-V를 배포 합니다. 자세한 내용은 [Med-v 작업 영역 패키지 배포](deploying-the-med-v-workspace-package.md)를 참조 하세요.

## 관련 항목


[MED-V 배포](deployment-of-med-v.md)

[MED-V 2.0에 대한 종단 간 계획 시나리오](end-to-end-planning-scenario-for-med-v-20.md)

[MED-V 2.0 종단 간 작업 시나리오](end-to-end-operations-scenario-for-med-v-20.md)

 

 





