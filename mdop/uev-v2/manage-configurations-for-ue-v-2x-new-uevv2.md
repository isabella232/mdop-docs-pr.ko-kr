---
title: UE-V 2.x에 대한 구성 관리
description: UE-V 2.x에 대한 구성 관리
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827383"
---
# UE-V 2.x에 대한 구성 관리


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1 수명 주기를 진행 하는 동안 UE-V Agent의 구성을 관리 하 고 설정 패키지 파일과 같은 리소스에 대 한 저장소 위치도 관리 해야 합니다. 사용자가 UE-V를 사용 하 여 상호 작용 하는 방식을 정의 하도록 회사 설정 센터를 구성 하는 등 다른 작업을 수행 해야 할 수 있습니다. 다음 항목에서는 이러한 UE-V 리소스 관리에 대 한 지침을 제공 합니다.

## 그룹 정책 개체를 사용 하 여 UE-V 2. x 구성


그룹 정책 개체를 사용 하 여 UE-V가 컴퓨터에서 설정을 동기화 하는 방식을 정의 하는 설정을 수정할 수 있습니다.

[그룹 정책 개체를 사용 하 여 UE-V 2. x 구성](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## System Center Configuration Manager 2012에서 UE-V 2. x 구성


SystemCenter2012 ConfigurationManager를 사용 하 여 ue-v 2 구성 팩을 사용 하 여 UE-V 에이전트를 관리할 수 있습니다.

[System Center Configuration Manager 2012에서 UE-V 2. x 구성](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## UE-V를 사용 하 여 PowerShell 및 WMI 관리


UE-V는 관리자가 다양 한 UE-V 작업을 수행 하는 데 도움이 되는 Windows PowerShell cmdlet을 제공 합니다.

[Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## UE-V 2. x에 대 한 회사 설정 센터 구성


UE-V Agent를 사용 하 여 사용자가 UE-V를 사용 하는 방식을 정의 하 여 설치한 회사 설정 센터를 구성할 수 있습니다.

[UE-V 2. x에 대 한 회사 설정 센터 구성](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## UE-V 2. x에 대 한 구성 설정의 예


다음은 UE-V 구성 설정의 몇 가지 예입니다.

-   **설정 저장소 경로:** UE-V 설정을 저장 하는 파일 공유의 위치를 지정 합니다.

-   **설정 서식 파일 카탈로그 경로:** 새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 지정 합니다.

-   **Microsoft 서식 파일 등록:** 설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.

-   **동기화 방법:** UE-V가 동기화 공급자를 사용할지 아니면 "없음"을 사용 하는지를 지정 합니다. "SyncProvider"는 네트워크에 연결 되지 않은 컴퓨터를 지원 합니다. "없음"은 컴퓨터가 항상 네트워크에 연결 되어 있는 경우 적용 됩니다. Sync 메서드에 대 한 자세한 내용은 [ue-v 2. x에 대 한 Sync 메서드](sync-methods-for-ue-v-2x-both-uevv2.md)를 참조 하세요.

-   **동기화 시간 제한:** 설정 저장소 위치에서 사용자 설정을 검색할 때 시간이 초과 되기 전에 컴퓨터가 대기 하는 시간 (밀리초)을 지정 합니다.

-   **동기화 사용:** UE-V 설정 동기화를 사용할 수 있는지 여부를 지정 합니다.

-   **최대 패키지 크기:** UE-V Agent가 경고를 보고 하는 설정 패키지 파일의 임계값 크기 (바이트)를 지정 합니다.

-   **Windows 앱 설정 동기화 안 함:** UE-V가 Windows 앱을 동기화 하지 않도록 지정 합니다.

-   **첫 번째 사용 알림 사용/사용 안 함:** 사용자의 컴퓨터에서 UE-V Agent가 처음 실행 될 때 UE-V가 대화 상자를 표시할지 여부를 지정 합니다.

-   **트레이 아이콘 설정/해제:** UE-V가 알림 영역에 아이콘을 표시할지 여부와 연결 된 알림을 표시할지를 지정 합니다. 아이콘은 회사 설정 센터에 대 한 링크를 제공 합니다.

-   **사용자 지정 연락처 하이퍼링크:** 회사 설정 센터에서 **IT 대화 상대** 하이퍼링크에 대 한 경로, 텍스트 및 설명을 정의 합니다.






## 관련 항목


[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

[UE-V 2.x에 대한 필수 기능 배포](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





