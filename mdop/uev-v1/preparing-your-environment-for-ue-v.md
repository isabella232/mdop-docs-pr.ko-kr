---
title: UE-V용 환경 준비
description: UE-V용 환경 준비
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824648"
---
# UE-V용 환경 준비


Microsoft UE-V (User Experience Virtualization)는 설정 저장소 위치를 사용 하 여 컴퓨터 간에 설정을 로밍 합니다. 설정 저장소 위치는 파일 공유 이므로 UE-V 에이전트 배포 중에 구성 되어야 합니다. 설정 저장소 위치 또는 Active Directory 홈 디렉터리로 정의 되어야 합니다. 또한 관리자는 일관성 있는 동기화를 지원 하도록 시간 서버를 구성 해야 합니다. UE-V를 사용할 수 있도록 환경을 준비 하려면 다음 사항을 고려해 야 합니다.

-   [Ue-v 설정 저장소](#bkmk-uevsettingsstorage):

    -   [설정 저장소 위치 정의](#bkmk-definingsettingsstoragelocation)

    -   [UE-V를 사용 하 여 Active Directory Home 디렉터리 사용](#bkmk-usingactivedirectoryhomedirectory)

-   [UE-V 설정 동기화에 대 한 컴퓨터 시계 동기화](#bkmk-synchronizecomputerclocks)

-   [성능 및 용량 계획](#bkmk-performancecapacityplanning)

운영 체제 및 컴퓨터 요구 사항에 대 한 자세한 내용은 [ue-v 1.0에서 지원 되는 구성을](supported-configurations-for-ue-v-10.md)참조 하세요.

## <a href="" id="bkmk-uevsettingsstorage"></a>UE-V 설정 저장소


설정 저장소 위치 또는 Active Directory 홈 디렉터리인 두 가지 구성 중 하나를 사용 하 여 사용자 환경 가상화 설정 저장소를 정의할 수 있습니다.

### <a href="" id="bkmk-definingsettingsstoragelocation"></a>설정 저장소 위치 정의

UE-V 설정 저장소 위치는 UE-V 사용자가 액세스할 수 있는 표준 네트워크 공유입니다. 설정 저장소 위치를 정의 하기 전에 루트 디렉터리를 만들어야 합니다. 공유에 설정을 저장할 사용자에 게는 저장소 위치에 대 한 읽기/쓰기 권한이 있어야 합니다. UE-V Agent가이 루트 디렉터리 아래에 사용자 관련 폴더를 만듭니다. 설정 저장소 위치는 **Settingsstoragepath** 구성 옵션을 설정 하 여 정의 합니다. 이 옵션은 다음과 같은 방법으로 구성할 수 있습니다.

-   명령줄 매개 변수 또는 일괄 처리 스크립트를 통해 UE-V 에이전트를 설치 하는 동안

-   그룹 정책을 사용 합니다.

-   설치 후 PowerShell 또는 WMI를 사용 합니다.

경로는 서버 및 공유의 UNC (범용 명명 규칙) 경로에 있어야 합니다. 예를 **\\\\server\\settingsshare\\**. 이 구성 옵션은 특정 로밍 시나리오를 사용 하도록 설정 하는 변수 사용을 지원 합니다.

서버의 UNC 경로와 공유 하는 변수를 사용할 수 있습니다 `%username%` . 이렇게 하면 사용자가 로그인 하는 모든 컴퓨터 또는 세션에 동일한 설정 환경이 제공 됩니다. 다음과 같은 시나리오를 위해이 구성을 고려해 야 합니다.

1.  기업의 사용자는 유사 하 게 구성 된 여러 물리적 컴퓨터를 가질 수 있으며 각 사용자의 설정은 모든 컴퓨터에서 동일 해야 합니다.

2.  엔터프라이즈의 사용자는 각 사용자의 VDI 세션에서 설정이 유지 되어야 하는 VDI (가상 데스크톱 인프라) 풀을 사용 합니다.

3.  기업의 사용자는 하나의 물리적 컴퓨터를 보유 하 고 있으며 추가적으로 VDI를 사용 합니다. 각 사용자의 설정 환경은 물리적 컴퓨터 또는 VDI 세션을 사용 하 든 관계 없이 동일 해야 합니다.

4.  여러 엔터프라이즈 컴퓨터는 여러 사용자가 사용 합니다. 각 사용자의 설정 환경은 모든 컴퓨터에서 동일 해야 합니다.

**%Username%\\%computername%** 변수를 서버의 UNC 경로와 공유 하는 데 사용할 수 있습니다. 이렇게 하면 각 컴퓨터에 대 한 설정 환경이 유지 됩니다. 다음과 같은 시나리오를 위해이 구성을 고려해 야 합니다.

1.  기업의 사용자는 여러 개의 물리적 컴퓨터를 보유 하 고 있으며 각 컴퓨터에 대 한 설정 환경을 유지 하려고 합니다.

2.  엔터프라이즈 컴퓨터는 여러 사용자가 사용 합니다. 설정 환경은 사용자가 로그인 하는 각 컴퓨터에 대해 유지 되어야 합니다.

UE-V agent는 UE-V `SettingsStoragePath` 구성 설정 및 정의 된 변수를 기반으로 사용자 관련 설정 저장소 경로를 동적으로 만듭니다.

UE-V agent `SettingsPackages` 가 각 사용자 관련 저장소 위치 내에서 이름이 지정 된 숨겨진 시스템 폴더를 동적으로 만듭니다. UE-V agent는 등록 된 UE-V 설정 위치 템플릿에서 정의한 대로이 위치에 대 한 설정을 읽고 씁니다.

설정 저장소 위치가 사용자의 관리 컴퓨터 집합에 대해 동일 하면 해당 UE-V 설정이 "마지막 쓰기 wins" 규칙에 따라 결정 됩니다. 한 컴퓨터에서 실행 되는 에이전트는 다른 컴퓨터에서 실행 되는 에이전트와 독립적으로 설정 위치를 읽고 씁니다. 마지막으로 작성 된 설정 및 값은 다음 에이전트가 설정 저장소 위치에서 읽을 때 적용 되는 설정입니다. 자세한 내용은 [ue-v 1.0에 대 한 설정 저장소 위치 배포](deploying-the-settings-storage-location-for-ue-v-10.md)를 참조 하세요.

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a>UE-V를 사용 하 여 Active Directory home 디렉터리 사용

에이전트가 배포 될 때 UE-V-V에 대해 구성 된 설정 저장소 위치가 없으면 사용자의 Active Directory (AD) 홈 디렉터리가 설정 위치 패키지를 저장 하는 데 사용 됩니다. UE-V agent가 각 사용자의 AD home 디렉터리 아래에 있는 설정 저장소 폴더를 동적으로 만듭니다. 설정 저장소 위치 (SettingsStoragePath)가 달리 정의 되지 않은 경우 에이전트는 Active Directory 홈 디렉터리만 사용 합니다.

## <a href="" id="bkmk-synchronizecomputerclocks"></a>UE-V 설정 동기화에 대 한 컴퓨터 시계 동기화


UE-V agent를 실행 하 여 설정을 동기화 하는 컴퓨터는 시간 서버를 사용 해야 합니다. 타임 스탬프는 설정 저장소 위치에서 설정을 동기화 해야 하는지 여부를 결정 하는 데 사용 됩니다. 컴퓨터 시계가 정확 하지 않으면 이전 설정이 최신 설정을 덮어쓰거나 새 설정이 설정 저장소 위치에 저장 되지 않을 수 있습니다. 시간 서버를 사용 하면 UE-V가 일관 된 설정 환경을 유지할 수 있습니다.

## <a href="" id="bkmk-performancecapacityplanning"></a>성능 및 용량 계획


UE-V의 용량 요구 사항은 표준 디스크 용량 및 네트워크 상태 모니터링을 사용 하 여 결정할 수 있습니다. UE-V가 설정 패키지 저장소에 대 한 SMB (서버 메시지 블록) 공유를 사용 합니다. 설정 패키지의 크기는 특정 응용 프로그램에 대 한 설정 정보에 따라 달라 집니다. 대부분의 설정 패키지는 작지만 데스크톱 이미지와 같은 잠재적으로 크기가 큰 파일을 동기화 하면 성능이 저하 될 수 있으며, 특히 네트워크 속도가 느릴 때 문제가 발생 합니다. 네트워크 지연 문제를 최소화 하려면 사용자 컴퓨터가 있는 동일한 로컬 네트워크에 설정 저장소 위치를 만들어야 합니다.

기본적으로 UE-V 동기화는 네트워크가 느리거나 설정 패키지가 큰 경우 2 초 후에 시간이 초과 됩니다. 그룹 정책을 사용 하 여 시간 제한을 구성할 수 있습니다. 시간 제한을 설정 하는 방법에 대 한 자세한 내용은 [그룹 정책 개체를 사용 하 여 Ue-v 구성을](configuring-ue-v-with-group-policy-objects.md)참조 하세요.

## 관련 항목


[Microsoft User Experience Virtualization(UE-V) 1.0](index.md)

[UE-V 1.0 계획](planning-for-ue-v-10.md)

[UE-V 1.0에 지원되는 구성](supported-configurations-for-ue-v-10.md)

 

 





