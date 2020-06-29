---
title: 사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업
description: 사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823978"
---
# 사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업


사용자 컴퓨터 간에 응용 프로그램을 로밍 하기 위해 Microsoft UE-V (사용자 환경 가상화)에서 *설정 위치 템플릿을*사용 합니다. 일부 설정 위치 템플릿은 사용자 환경 가상화에 포함 되어 있습니다. UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들거나 편집 하거나 확인할 수도 있습니다.

UE-V 생성기는 응용 프로그램이 해당 설정을 저장 하는 위치를 검색 하 고 캡처하는 응용 프로그램을 모니터링 합니다. 모니터링 되는 응용 프로그램은 일반 응용 프로그램 이어야 합니다. UE-V 생성기는 다음 응용 프로그램 종류에 대 한 설정 위치 템플릿을 만들 수 없습니다.

-   가상화 된 응용 프로그램

-   터미널 서비스를 통해 제공 되는 응용 프로그램

-   Java 응용 프로그램

-   Windows 8 응용 프로그램

## UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 만들기


UE-V 생성기를 사용 하 여 설정 위치 템플릿을 만드는 방법

[UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 만들기](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 편집


UE-V 생성기를 사용 하 여 설정 위치 템플릿을 편집 하는 방법을 설명 합니다.

[UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 편집](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 유효성 검사


Ue-v 생성기 외부에서 수정 된 설정 위치 템플릿의 유효성을 검사 하는 데 사용 하는 방법을 설명 합니다.

[UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 유효성 검사](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a>표준 및 비표준 설정 위치


UE-V 생성기는 응용 프로그램에서 설정 정보를 저장 하는 데 사용 하는 설정 파일 및 레지스트리 설정을 검색 하는 위치를 식별 하는 데 도움이 됩니다. UE-V 생성기를 사용 하 여 검색 프로세스의 일부로 응용 프로그램을 열면 표준 위치에서 설정을 캡처할 수 있습니다. 표준 위치에는 다음이 포함 됩니다.

-   **레지스트리 설정** – **HKEY \ _CURRENT \ _USER** 아래의 레지스트리 위치

-   **응용 프로그램 설정 파일** – \\ **사용자** \\ [사용자 이름 \ \ **AppData**  \\  **로밍** ]에 저장 된 파일

UE-V 생성기는 일반적으로 응용 프로그램 소프트웨어 파일을 저장 하는 위치를 사용자 컴퓨터와 환경 간에 원활 하 게 로밍 하지 않습니다. UE-V 생성기는 이러한 위치를 제외 합니다. 제외 된 위치는 다음과 같습니다.

-   HKEY \ _CURRENT \ _USER 로그온 한 사용자가 값을 쓸 수 없는 레지스트리 키 및 파일

-   HKEY _CURRENT \ _USER Windows 운영 체제의 핵심 기능과 연결 된 레지스트리 키 및 파일

-   HKEY \ _LOCAL \ _MACHINE 하이브에 있는 모든 레지스트리 키 (관리자 권한이 필요 하며, 설정 하려면 UAC 계약이 필요할 수 있음)

-   Program Files 디렉터리에 있는 파일 (관리자 권한이 필요 하 고 설정에 대 한 UAC 동의가 필요할 수 있음)

-   사용자 \\ [사용자 이름 \] \\ AppData에 있는 파일은 다음을 허용 합니다.

-   % Systemroot%에 위치 하는 Windows 운영 체제 파일 (관리자 권한이 필요 하며, 설정 하려면 UAC 동의가 필요할 수 있음)

이러한 위치에 저장 된 레지스트리 키 및 파일이 응용 프로그램 설정을 로밍 하기 위해 필요한 경우에는 템플릿 만들기 프로세스 중에 제외 된 위치를 설정 위치 템플릿에 수동으로 추가할 수 있습니다.

## 이 제품에 대 한 기타 리소스


[UE-V 1.0 작업](operations-for-ue-v-10.md)

[UE-V 1.0 관리](administering-ue-v-10.md)

 

 





