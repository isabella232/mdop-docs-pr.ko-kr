---
title: UE-V 2.0의 새로운 기능
description: UE-V 2.0의 새로운 기능
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824963"
---
# UE-V 2.0의 새로운 기능


Microsoft UE-V (User Experience Virtualization) 2.0는 UE-V 1.0에 비해 이러한 새로운 기능과 기능을 제공 합니다. [MICROSOFT ue-v (User Experience Virtualization) 2.0 릴리스](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) 정보는 ue-v 2.0 릴리스에 대 한 자세한 정보를 제공 합니다.

## CSC (클라이언트측 캐시)가 더 이상 필요 하지 않습니다.


이 버전의 UE-V를 통해 Windows 오프 라인 파일 기능에 대 한 요구 사항이 대체 되어 클라이언트측 설정 캐시를 지 원하는 **동기화 공급자**가 도입 되었습니다.

UE-V를 사용 하 여 응용 프로그램을 열거나 닫을 때 또는 Windows가 잠그거나 잠금 해제 또는 로그온 또는 로그 오프할 때에만 설정을 동기화 하는 것은 동기화 공급자입니다.

-   "**트리거 이벤트**"를 사용 하 여 로컬 응용 프로그램 및 Windows 설정을 대역외 외부에 동기화 합니다.

-   예약 된 **작업** 을 사용 하 여 엔터프라이즈 요구 사항에 대해 선택한 간격에 따라 설정 저장소 패키지를 동기화 합니다 (기본적으로 30 분 마다).

특정 조건을 충족 하면 동기화가 더 빈번 하 게 제공 됩니다.

-   사용자가 새 회사 설정 센터 응용 프로그램의 **지금 동기화** 단추를 클릭 하면 설정이 동기화 됩니다.

-   동기화 공급자는 예약 된 동기화 작업을 기다리지 않고 단일 응용 프로그램에 대해서도 시작할 수 있습니다. 예를 들어 응용 프로그램을 닫을 때 모든 설정 변경 내용이 로컬 캐시에 기록 되 고, 동기화 공급자 프로세스가 비동기적으로 실행 되어 새 설정 변경 내용을 설정 저장소 위치로 이동 합니다.

## Windows 앱 동기화


Windows 앱 개발자는 동기화 할 설정을 정의할 수 있으며, 이러한 설정을 이제 UE-V를 사용 하 여 캡처 및 동기화 할 수 있습니다.

기본적으로 UE-V는 Windows 8 및 Windows 8.1에 포함 된 많은 Windows 앱의 설정을 동기화 합니다. Windows PowerShell, WMI (Windows Management Instrumentation) 또는 그룹 정책을 사용 하 여 동기화 된 앱 목록을 수정할 수 있습니다.

**참고**  도메인 사용자가 로그인 자격 증명을 Microsoft 계정에 연결 하는 경우 UE-V는 Windows 앱 설정을 동기화 하지 않습니다. 이 링크는 Microsoft OneDrive에 설정을 동기화 하므로 UE-V-V는 데스크톱 응용 프로그램을 동기화 할 수만 있습니다.

 

## Microsoft 계정 연결


OneDrive를 통한 설정 동기화는 Microsoft 계정으로 로그인 하거나 Microsoft 계정을 도메인 계정에 연결 하는 경우 Windows 8에 대 한 새로운 방법입니다. 도메인 사용자가 UE-V를 사용 하 고 있고 Microsoft 계정에 로그인 한 경우 ...

-   UE-V는 데스크톱 응용 프로그램에 대 한 설정만 동기화 합니다.

-   Microsoft 계정에서 Windows 앱 설정 및 Windows 바탕 화면 설정 처리

## 회사 설정 센터


사용자에 게는 UE-V 2에서 회사 설정 센터 라는 응용 프로그램을 통해 동기화 되는 설정에 대 한 몇 가지 제어 기능을 제공할 수 있습니다. 회사 설정 센터는 UE-V Agent와 함께 설치 되며, 사용자는 제어판, **시작** 메뉴, **시작** 화면, ue-v 알림 영역 아이콘에서 액세스할 수 있습니다.

회사 설정 센터에서는 동기화 되는 설정을 표시 하 고 사용자가 UE-V의 동기화 상태를 볼 수 있도록 합니다. 사용자가 허용할 경우 회사 설정 센터를 사용 하 여 동기화 할 설정을 선택할 수 있습니다. **지금 동기화** 단추를 클릭 하 여 모든 설정을 즉시 동기화 할 수도 있습니다.






## 관련 항목


[UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

[UE-V 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





