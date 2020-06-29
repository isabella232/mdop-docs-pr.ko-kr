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
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827098"
---
# UE-V 1.0의 개략적인 아키텍처


이 항목에서는 Microsoft UE-V (User Experience Virtualization) 설정 로밍 솔루션의 상위 수준 아키텍처 요소에 대해 설명 합니다. 다음 요소는 표준 UE-V 배포의 일부입니다.

![ue-v agent 아키텍처 다이어그램](images/ue-vagentarchitecturaldiagram.gif)

UE-V Agent는 UE-V 설정 위치 템플릿에서 식별 되는 응용 프로그램 및 운영 체제 프로세스를 모니터링 합니다. 응용 프로그램이 나 운영 체제가 시작 되 면 설정 패키지에서 설정을 읽고 컴퓨터에 적용 합니다. 응용 프로그램이 닫히거나 운영 체제가 잠그거나 종료 되 면 설정 저장소 위치의 UE-V settings 패키지에 설정이 저장 됩니다.

## 설정 저장소 위치


설정 저장소 위치는 사용자 환경 가상화 에이전트에서 읽기 및 쓰기 설정에 액세스 하는 파일 공유입니다. 이 위치는 Active Directory home 디렉터리 이거나 UE-V 설치 중에 정의 되어 있습니다. UE-V 에이전트를 설치 하는 동안 위치를 설정 하거나 그룹 정책, WMI 또는 PowerShell을 사용 하 여 나중에 설정할 수 있습니다. 위치는 사용자가 액세스할 수 있는 모든 공용 파일 공유에 있을 수 있습니다. 설치 하는 동안 설정 저장소 위치를 설정할 수 없는 경우에는 UE-V가 Active Directory에서 홈 디렉터리를 사용 합니다. UE-V agent는 위치를 확인 하 고 사용자 설정을 저장 하 고 액세스 하는 사용자에 게 숨겨진 시스템 폴더를 만듭니다. 설정 저장소에 대 한 자세한 내용은 [ue-v 용 환경 준비](preparing-your-environment-for-ue-v.md)를 참조 하세요.

## UE-V 에이전트


UE-V agent가 사용자 환경 가상화에 의해 동기화 되는 설정을 사용 하 여 각 컴퓨터에 설치 됩니다. 에이전트는 등록 된 응용 프로그램 및 운영 체제를 모니터링 하 여 설정에 대 한 변경 내용을 적용 하 고 해당 설정을 컴퓨터 간에 동기화 합니다. 설정은 응용 프로그램이 시작 될 때 설정 저장소 위치에서 응용 프로그램으로 적용 됩니다. 그러면 해당 설정이 응용 프로그램을 닫을 때 설정 저장소 위치로 다시 저장 됩니다. 운영 체제 설정은 사용자가 로그온 하거나, 컴퓨터를 잠금 해제 하거나, 사용자가 RDP (원격 데스크톱 프로토콜)을 사용 하 여 컴퓨터에 원격으로 연결할 때 적용 됩니다. 에이전트는 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있거나 원격 연결이 끊어질 때 설정을 저장 합니다. UE-V 에이전트에 대 한 자세한 내용은 [ue-v 용 환경 준비](preparing-your-environment-for-ue-v.md)를 참조 하세요.

## <a href="" id="bkmk-settingslocationtemplate"></a>설정 위치 템플릿


설정 위치 템플릿은 사용자 환경 가상화를 통해 모니터링할 설정 위치를 정의 하는 XML 파일입니다. 이러한 설정 템플릿에 정의 된 설정 위치만 UE-V Agent를 실행 하는 컴퓨터에서 캡처 또는 적용 됩니다. 설정 위치 템플릿은 값이 컴퓨터에 저장 된 위치만 포함 하 고 설정 값으로 구성 되어 있지 않습니다.

UE-V는 일부 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치를 지정 하는 설정 위치 템플릿의 집합을 포함 합니다. 관리자는 UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.

[UE-V 1.0과 동기화할 응용 프로그램 계획](planning-which-applications-to-synchronize-with-ue-v-10.md)

[UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)

[사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## 설정 패키지


응용 프로그램 설정 및 Windows 설정은 UE-V Agent에서 만든 설정 패키지에 저장 됩니다. 설정 패키지는 설정 위치 템플릿에 표시 되는 설정의 컬렉션입니다. 이러한 설정 패키지는 빌드, 로컬 저장, 설정 저장소 위치에 복사 됩니다. "마지막 쓰기 wins"는 단일 사용자가 두 대 이상의 컴퓨터를 저장소 위치로 동기화 할 때 유지 되는 설정을 결정 합니다. 한 컴퓨터에서 실행 되는 에이전트는 다른 컴퓨터에서 실행 되는 에이전트와 독립적으로 설정 위치를 읽고 씁니다. 다음 에이전트가 설정 저장소 위치에서 읽을 때 가장 최근에 쓰여진 설정 및 값이 적용 됩니다.

![ue-v 생성자 프로세스](images/ue-vgeneratorprocess.gif)

## 설정 서식 파일 카탈로그


설정 템플릿 카탈로그는 UE-V 컴퓨터 또는 모든 사용자 지정 설정 위치 템플릿을 저장 하는 SMB (서버 메시지 블록) 네트워크 공유의 폴더 경로입니다. UE-V agent가이 위치에서 새 서식 파일 또는 업데이트 된 템플릿을 검색 합니다. UE-V agent는 매일이 위치를 확인 하 고이 폴더의 템플릿을 기반으로 동기화 동작을 업데이트 합니다. 마지막 검사 이후이 폴더에서 추가 되거나 업데이트 된 서식 파일이 UE-V agent에 의해 등록 됩니다. UE-V agent가이 폴더에서 제거 된 템플릿을 deregisters. 작업 스케줄러에서 서식 파일을 하루에 한 번씩 등록 하 고 등록 취소 했습니다. UE-V와 함께 제공 되는 기본 설정 위치 템플릿만 사용 하는 경우 설정 템플릿 카탈로그는 필요 하지 않습니다. 설정 배포 카탈로그에 대 한 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획 수립](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.

## 사용자 환경 가상화 생성기


사용자 환경 가상화 생성기를 사용 하 여 엔터프라이즈에 사용 되 고 로밍 설정 솔루션에 포함 하려는 응용 프로그램의 설정 위치를 저장할 사용자 지정 설정 위치 템플릿을 만들 수 있습니다. UE-V 생성기는 레지스트리 값의 위치와 응용 프로그램에 대 한 설정 파일을 검색 한 다음 설정 위치 템플릿 XML 파일에 해당 위치를 기록 합니다. 그런 다음 이러한 설정 위치 템플릿을 사용자 컴퓨터에 배포할 수 있습니다. 또한 UE-V 생성기를 사용 하면 관리자가 기존 서식 파일을 편집 하거나 다른 XML 편집기를 사용 하 여 만든 서식 파일의 유효성을 검사할 수 있습니다.

UE-V 생성기는 응용 프로그램을 모니터링 하 여 설정을 저장 하는 위치를 검색 하 고 기록 합니다. 이렇게 하려면 HKEY \ _CURRENT \ _USER 레지스트리 또는 **사용자** \\ \ [사용자 이름 \ \ \ **AppData**  \\  **로밍 및 사용자** \\ \ \ \ \ **AppData**  \\  **Local**)의 파일 폴더에서 응용 프로그램이 읽거나 쓰는 위치를 모니터링 합니다.

검색 프로세스는 로그인 한 사용자가 값을 쓸 수 없는 레지스트리 키와 파일을 제외 합니다. 이러한 항목이 XML 파일에 포함 되지 않습니다. 또한 검색 프로세스는 Windows 운영 체제의 핵심 기능과 연결 된 레지스트리 키와 파일을 제외 합니다.

UE-V 생성기에 대 한 자세한 내용은 [Ue-v 생성기 설치](installing-the-ue-v-generator.md)를 참조 하세요.

## 관련 항목


[Microsoft User Experience Virtualization(UE-V) 1.0](index.md)

[User Experience Virtualization 1.0 시작](getting-started-with-user-experience-virtualization-10.md)

[User Experience Virtualization 1.0 정보](about-user-experience-virtualization-10.md)

[사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





