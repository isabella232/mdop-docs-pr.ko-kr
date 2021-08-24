---
title: UE-V 1.0의 개략적인 아키텍처
description: UE-V 1.0의 개략적인 아키텍처
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b54a9a207f9b74ad3d028cf4ab1f9842d59b0b3a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910453"
---
# <a name="high-level-architecture-for-ue-v-10"></a>UE-V 1.0의 개략적인 아키텍처


이 항목에서는 Microsoft User Experience Virtualization(UE-V) 로밍 솔루션의 높은 수준의 아키텍처 요소에 대해 설명합니다. 다음 요소는 표준 배포에 UE-V 요소입니다.

![ue-v 에이전트 아키텍처 다이어그램.](images/ue-vagentarchitecturaldiagram.gif)

UE-V 에이전트는 응용 프로그램 및 운영 체제 프로세스가 UE-V 설정 위치 템플릿에서 식별되는 프로세스를 모니터링합니다. 응용 프로그램 또는 운영 체제가 시작되면 설정 패키지에서 설정을 읽고 컴퓨터에 적용됩니다. 응용 프로그램을 닫거나 운영 체제를 잠그거나 종료하면 설정 저장소 위치의 UE-V 설정 패키지에 설정이 저장됩니다.

## <a name="settings-storage-location"></a>설정 저장소 위치


설정 저장소 위치는 User Experience Virtualization 에이전트가 설정을 읽고 쓰기 위해 액세스하는 파일 공유입니다. 이 위치는 Active Directory 홈 디렉터리 또는 설치 중에 UE-V 정의됩니다. UE-V 에이전트를 설치하는 동안 위치를 설정하거나 나중에 그룹 정책, WMI 또는 PowerShell을 사용하여 설정할 수 있습니다. 위치는 사용자가 액세스할 수 있는 모든 일반 파일 공유에 있을 수 있습니다. 설치 중에 설정 저장소 위치를 설정하지 UE-V Active Directory의 홈 디렉터리를 사용하게 됩니다. UE-V 에이전트는 위치를 확인하여 사용자 설정을 저장하고 액세스할 사용자가 숨겨져 있는 시스템 폴더를 만듭니다. 설정 저장소에 대한 자세한 내용은 [Preparing Your Environment for UE-V.](preparing-your-environment-for-ue-v.md)

## <a name="ue-v-agent"></a>UE-V 에이전트


사용자 UE-V 가상화에서 동기화되는 설정을 사용하여 각 컴퓨터에 설치됩니다. 에이전트는 등록된 응용 프로그램 및 운영 체제에서 설정이 변경된 내용을 모니터링하고 컴퓨터 간에 이러한 설정을 동기화합니다. 설정 응용 프로그램이 시작될 때 설정 저장소 위치에서 응용 프로그램으로 적용됩니다. 그러면 응용 프로그램이 닫히면 설정 저장 위치에 설정이 다시 저장됩니다. 운영 체제 설정은 사용자가 로그온할 때, 컴퓨터 잠금이 해제된 경우 또는 사용자가 RDP(원격 데스크톱 프로토콜)를 사용하여 컴퓨터에 원격으로 연결할 때 적용됩니다. 에이전트는 사용자가 로그오프할 때, 컴퓨터가 잠겨 있는 경우 또는 원격 연결이 끊어진 경우 설정을 저장합니다. UE-V 대한 자세한 내용은 [Preparing Your Environment for UE-V.](preparing-your-environment-for-ue-v.md)

## <a name="settings-location-templates"></a><a href="" id="bkmk-settingslocationtemplate"></a>설정 위치 템플릿


설정 위치 템플릿은 User Experience Virtualization에서 모니터링할 설정 위치를 정의하는 XML 파일입니다. 이러한 설정 템플릿에 정의된 설정 위치만 에이전트를 실행하는 컴퓨터에 캡처되거나 UE-V 적용됩니다. 설정 위치 서식 파일에는 설정 값이 포함되지 않습니다. 값이 컴퓨터에 저장되는 위치만 포함되어 있습니다.

UE-V Microsoft 응용 프로그램에 대한 설정 위치를 지정하는 설정 위치 템플릿 집합과 설정 Windows 포함되어 있습니다. 관리자는 UE-V 생성기를 사용하여 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.

[UE-V 1.0과 동기화할 응용 프로그램 계획](planning-which-applications-to-synchronize-with-ue-v-10.md)

[UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)

[사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## <a name="settings-packages"></a>설정 패키지


응용 프로그램 설정 및 Windows 설정은 에이전트 에이전트에서 만든 설정 패키지에 UE-V 저장됩니다. 설정 패키지는 설정 위치 템플릿에 나타내는 설정 컬렉션입니다. 이러한 설정 패키지는 로컬로 만들어지며 설정 저장소 위치에 복사됩니다. "마지막 쓰기가 가장 좋습니다."는 한 사용자가 두 대 이상의 컴퓨터를 저장소 위치에 동기화할 때 보존되는 설정을 확인합니다. 한 컴퓨터에서 실행되는 에이전트는 다른 컴퓨터에서 실행되는 에이전트와는 독립적으로 설정 위치를 읽고 읽습니다. 가장 최근에 작성된 설정 및 값은 다음 에이전트가 설정 저장소 위치에서 읽을 때 적용됩니다.

![ue-v 생성기 프로세스.](images/ue-vgeneratorprocess.gif)

## <a name="settings-template-catalog"></a>설정 템플릿 카탈로그


설정 템플릿 카탈로그는 UE-V 컴퓨터의 폴더 경로 또는 모든 사용자 지정 설정 위치 템플릿을 저장하는 SMB(서버 메시지 블록) 네트워크 공유입니다. 이 UE-V 에이전트는 이 위치에서 새 서식 파일 또는 업데이트된 서식 파일을 검색합니다. 이 UE-V 에이전트는 매일 이 위치를 확인하고 이 폴더의 템플릿에 따라 동기화 동작을 업데이트합니다. 마지막 검사 이후 이 폴더에 추가되거나 업데이트된 서식 파일은 UE-V 등록됩니다. 이 UE-V 에이전트는 이 폴더에서 제거된 템플릿의 이름을 제거합니다. 템플릿은 작업 스케줄러에 의해 매일 한 번 등록 및 등록되지 않습니다. 기본 설정 위치 서식 파일만 사용할 경우 UE-V 템플릿 카탈로그가 필요하지 않습니다. 설정 배포 카탈로그에 대한 자세한 내용은 [Planning for Custom Template Deployment for UE-V 1.0을 참조하십시오.](planning-for-custom-template-deployment-for-ue-v-10.md)

## <a name="user-experience-virtualization-generator"></a>User Experience Virtualization Generator


User Experience Virtualization Generator를 사용하면 엔터프라이즈에서 사용하며 로밍 설정 솔루션에 포함할 응용 프로그램의 설정 위치를 저장할 사용자 지정 설정 위치 템플릿을 만들 수 있습니다. UE-V 생성기는 레지스트리 값의 위치와 응용 프로그램의 설정 파일을 검색한 다음 설정 위치 템플릿 XML 파일에 해당 위치를 기록합니다. 그런 다음 이러한 설정 위치 템플릿을 사용자 컴퓨터에 배포할 수 있습니다. 또한 UE-V 생성기를 사용하면 관리자가 기존 템플릿을 편집하거나 다른 XML 편집기로 만든 서식 파일 유효성을 검사할 수 있습니다.

UE-V 생성기는 응용 프로그램을 모니터링하여 해당 설정이 저장되는 위치를 검색하고 기록합니다. 이를 위해 응용 프로그램이 HKEY\_CURRENT\_USER 레지스트리 또는 **Users** \\ \[User name\] \\ **AppData**  \\  **Roaming** 및 Users \\ \[User name\] \\ **AppData**  \\  **Local의**파일 폴더에서 읽거나 쓰는 위치를 모니터링합니다.

검색 프로세스에서는 로그인한 사용자가 값을 쓸 수 없는 레지스트리 키와 파일이 제외됩니다. 이 중 XML 파일에는 이러한 파일이 포함되지 않습니다. 또한 검색 프로세스에서는 Windows 운영 체제의 핵심 기능과 연결된 레지스트리 키와 파일도 제외됩니다.

UE-V 대한 자세한 내용은 [Installing the UE-V Generator를 참조하십시오.](installing-the-ue-v-generator.md)

## <a name="related-topics"></a>관련 항목


[Microsoft User Experience Virtualization(UE-V) 1.0](index.md)

[User Experience Virtualization 1.0 시작](getting-started-with-user-experience-virtualization-10.md)

[User Experience Virtualization 1.0 정보](about-user-experience-virtualization-10.md)

[사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





