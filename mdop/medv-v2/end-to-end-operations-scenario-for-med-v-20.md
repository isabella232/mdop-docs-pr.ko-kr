---
title: MED-V 2.0 종단 간 작업 시나리오
description: MED-V 2.0 종단 간 작업 시나리오
author: dansimp
ms.assetid: 1d87f5f3-9fc5-4731-8bd1-c155714f34ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90a7c2135ad27040ed87dac980b67321eb771574
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826168"
---
# MED-V 2.0 종단 간 작업 시나리오


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0의이 샘플 시나리오는 여러 시나리오를 통해 종단간를 배포 하 고 관리 하는 데 도움이 됩니다. 이 샘플 시나리오는 개별 시나리오 및 절차를 컨텍스트에 추가할 수 있도록 하는 사례 연구를 통해 생각 하면 됩니다.

이 섹션에서는 enterprise에서 종단간 솔루션으로 MED-V 작업 영역을 만들고, 배포 하 고, 관리 하는 데 필요한 기본 정보와 지침을 제공 합니다.

## MED-V 작업 단계별 시나리오


MED-V 작업 시나리오에서 수행 하는 단계별 절차에는 다음이 포함 됩니다.

-   [Med-v에 대 한 Windows 가상 Pc 이미지 만들기](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc) med-v에 대 한 WINDOWS 가상 pc 이미지를 만들고 구성 하는 방법을 검토 합니다. 사용자에 게 MED-V 작업 영역을 제공 하려면 먼저 MED-V에 대 한 MED-V 작업 영역 설치 패키지를 빌드하는 데 사용 하는 VHD (가상 하드 디스크)를 준비 해야 합니다.

-   [Med-v에 대 한 Windows 가상 Pc 이미지 만들기](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingwindowsxpontovpc) WINDOWS 가상 pc 이미지에 WINDOWS XP SP3 운영 체제를 설치 하는 방법을 검토 합니다. MED-V를 사용 하려면 MED-V 작업 영역을 빌드하기 전에 windows XP SP3이 Windows 가상 PC 이미지에 설치 되어 있어야 합니다.

-   [Med-v에 대 한 Windows 가상 Pc 이미지 만들기](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingnet) .net FRAMEWORK 3.5 SP1 및 업데이트 KB959209을 med-v와 함께 사용 하기 위해 준비 하는 WINDOWS 가상 PC 이미지에 수동으로 설치 하는 방법을 검토 합니다. MED-V에는 .NET Framework 3.5 SP1이 필요 하며 업데이트 [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) 는 https://go.microsoft.com/fwlink/?LinkId=204950) 알려진 여러 응용 프로그램 호환성 문제를 해결 합니다.

-   [Med-v에 대 한 Windows 가상 PC 이미지 만들기](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-applypatchestovpc) 최신 소프트웨어 업데이트 및 다른 핫픽스를 사용 하 여 med-v를 실행 하는 데 필요 하거나 중요 한 windows XP 이미지를 업데이트 하는 방법을 검토 합니다.

-   [Med-v에 대 한 Windows 가상 PC 이미지 만들기](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installintegration) windows XP 이미지에 통합 구성 요소 패키지를 설치 하는 방법을 검토 합니다. 이러한 기능을 통해 가상 환경과 물리적 컴퓨터 간의 상호 작용을 향상 시킬 수 있습니다.

-   [Windows VIRTUAL PC 이미지에 응용 프로그램을 설치](installing-applications-on-a-windows-virtual-pc-image.md) 하면 전자 소프트웨어 배포 시스템 및 바이러스 백신 소프트웨어와 같이 med-v를 실행 하는 경우 유용한 windows XP 이미지에 특정 종류의 소프트웨어를 설치 하는 방법이 나와 있습니다.

-   [Med-v 용 Windows 가상 PC 이미지 구성](configuring-a-windows-virtual-pc-image-for-med-v.md) Sysprep를 사용 하 여 이미지를 구성 하 여 med-v와 함께 사용할 준비가 되었는지 확인 하는 방법에 대해 설명 합니다. 그런 다음 준비 된 MED-V 이미지를 사용 하 여 MED-V 작업 영역 패키지를 만듭니다.

-   [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md) 엔터프라이즈 전체에 배포 하는 med-v 작업 영역 패키지를 작성 하는 방법을 검토 합니다. MED-V 작업 영역 패키지를 배포 하 여 최종 사용자 컴퓨터에 MED-V 작업 영역을 설치 합니다. MED-V 작업 영역은 MED-V에서 제공 하는 가상 컴퓨터와 최종 사용자가 상호 작용 하는 Windows XP 데스크톱 환경입니다.

-   [Med-v 작업 영역 패키지 테스트](testing-the-med-v-workspace-package.md) 처음 설정 및 응용 프로그램 게시와 같은 med-v 작업 영역 패키지의 기능을 테스트할 수 있는 테스트 환경을 만드는 방법에 대해 설명 합니다. MED-V 작업 영역 패키지 테스트를 완료 하 고 의도 한 대로 작동 하는지 확인 한 후에는 엔터프라이즈 전체에 배포할 수 있습니다.

-   [Med-v 작업 영역 패키지 배포](deploying-the-med-v-workspace-package.md) 전자 소프트웨어 배포 시스템 또는 Windows 7 이미지를 사용 하 여 med-v 작업 영역을 배포 하는 방법에 대해 설명 합니다. 또는이 섹션에서는 MED-V 작업 영역을 수동으로 배포 하는 방법에 대해서도 설명 합니다.

-   [Med-v 작업 영역 모니터링](monitor-med-v-workspaces.md) med-v 작업 영역의 배포를 모니터링 하 여 첫 번째 설정이 성공적으로 완료 되었는지 여부를 확인 하는 방법을 검토 합니다. 첫 설치가 성공적으로 완료 될 때까지 MED-V가 사용할 수 있는 상태가 아니기 때문에 처음 설치의 성공 여부를 모니터링 하는 것이 중요 합니다. 또한이 섹션에서는 MED-V에 영향을 줄 수 있는 네트워크 변경을 감지 하도록 환경을 설정할 수 있습니다.

-   [Med-v 작업 영역 관리 응용 프로그램](manage-med-v-workspace-applications.md) 배포 된 med-v 작업 영역에서 응용 프로그램을 설치 및 제거 하거나 게시 및 게시 취소 하는 방법을 검토 합니다. 이 섹션에서는 MED-V 작업 영역의 소프트웨어를 수동으로 업데이트 하는 방법과 자동 업데이트를 관리 하는 방법에 대해서도 설명 합니다. MED-V 작업 영역은 자동 소프트웨어 업데이트 프로세스가 엔터프라이즈의 실제 컴퓨터와 동일 하 게 관리 되어야 하는 별도의 운영 체제를 포함 하는 가상 컴퓨터입니다.

-   [MED-V URL 리디렉션 관리](manage-med-v-url-redirection.md) 배포 된 med-v 작업 영역에서 웹 주소 리디렉션 설정을 추가 하 고 제거 하는 방법을 검토 합니다. 레지스트리를 통해 또는 MED-V 작업 영역을 다시 작성 하 여 URL 리디렉션 정보를 추가 또는 제거할 수 있습니다. MED-V 작업 영역 포장기의 마법사를 사용 하 여 웹 주소 리디렉션을 관리할 수도 있습니다.

-   [Med-v 작업 영역 설정 관리](manage-med-v-workspace-settings.md) Med-v 작업 영역 포장기를 사용 하 여 med-v 구성 설정을 확인 하 고 편집 하는 방법을 검토 합니다. 이 섹션에는 구성 가능한 모든 MED-V 레지스트리 키가 나열 되며 각각에 대 한 유형, 기본 및 설명이 포함 됩니다. 이 섹션에는 MED-V 작업 영역에서 프린터를 관리 하는 방법에 대 한 정보도 포함 되어 있습니다. MED-V 2.0에서는 프린터 리디렉션을 통해 사용자가 MED-V 가상 컴퓨터와 호스트 컴퓨터 간에 일관 된 인쇄 환경을 제공 합니다.

## 관련 항목


[MED-V 작업](operations-for-med-v.md)

[MED-V 2.0에 대한 종단 간 계획 시나리오](end-to-end-planning-scenario-for-med-v-20.md)

[MED-V 2.0에 대한 종단 간 배포 시나리오](end-to-end-deployment-scenario-for-med-v-20.md)

 

 





