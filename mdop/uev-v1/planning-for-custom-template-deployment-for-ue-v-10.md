---
title: UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획
description: UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821193"
---
# UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획


Microsoft UE-V (User Experience Virtualization)는 UE-V를 통해 캡처 및 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다. UE-V 생성기를 사용 하 여 사용자가 기본 UE-V 템플릿에 포함 되지 않은 응용 프로그램의 설정을 로밍 하도록 하는 사용자 지정 설정 위치 템플릿을 만들 수 있습니다. 테스트 환경에서 응용 프로그램 설정이 올바르게 로밍 되도록 사용자 지정 템플릿을 테스트 한 후 엔터프라이즈의 컴퓨터에 이러한 설정 위치 템플릿을 배포할 수 있습니다.

사용자 지정 설정 위치 템플릿을 ESD (엔터프라이즈 소프트웨어 배포) 등의 기존 배포 인프라를 사용 하 여 그룹 정책 기본 설정과 함께 배포 하거나 UE-V 설정 템플릿 카탈로그를 구성할 수 있습니다. ESD 또는 그룹 정책을 사용 하 여 배포한 서식 파일은 UE-V WMI 또는 PowerShell로 등록 해야 합니다.

## 설정 서식 파일 카탈로그


사용자 환경 가상화 설정 템플릿 카탈로그는 UE-V 컴퓨터 또는 모든 사용자 지정 설정 위치 템플릿을 저장 하는 SMB (서버 메시지 블록) 네트워크 공유의 폴더 경로입니다. UE-V agent가이 위치에서 새 서식 파일 또는 업데이트 된 템플릿을 검색 합니다. UE-V agent는 매일이 위치를 확인 하 고이 폴더의 템플릿을 기반으로 동기화 동작을 업데이트 합니다. 폴더를 마지막으로 확인 한 후에이 폴더에서 추가 또는 업데이트 된 서식 파일이 UE-V 에이전트에서 등록 되었습니다. 이 폴더에서 제거 되는 UE-V agent deregisters 템플릿입니다. 기본적으로 서식 파일은 매일 오전 3:30에 한 번씩 등록 되 고 등록이 취소 됩니다. 작업 스케줄러의 현지 시간입니다. UE-V 작업에 대 한 자세한 내용은 [Ue-v 예약 작업의 빈도 변경을](changing-the-frequency-of-ue-v-scheduled-tasks.md)참조 하세요.

설치 명령줄 옵션, 그룹 정책, WMI 또는 PowerShell을 사용 하 여 설정 템플릿 카탈로그 경로를 구성할 수 있습니다. 설정 서식 파일 카탈로그 경로에 저장 된 서식 파일은 예약 된 작업에 의해 자동으로 등록 및 등록 취소 됩니다. 필요에 따라이 예약 된 작업을 사용자 지정할 수 있습니다.

## 기본 Microsoft 서식 파일 바꾸기


UE-V agent는 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 기본 설정 위치 템플릿 그룹을 설치 합니다. 엔터프라이즈에 이러한 서식 파일의 사용자 지정 버전이 필요한 경우 설정 서식 파일 카탈로그를 사용 하도록 UE-V 에이전트를 구성할 수 있으며, 그런 다음 기본 Microsoft 템플릿을 바꿔야 합니다.

UE-V agent를 설치 하는 동안 명령줄 매개 변수를 `RegisterMSTemplates` 사용 하 여 기본 Microsoft 템플릿의 등록을 사용 하지 않도록 설정할 수 있습니다. UE-V 매개 변수를 설정 하는 방법에 대 한 자세한 내용은 [Ue-v 구성 방법 계획](planning-for-ue-v-configuration-methods.md)을 참조 하세요.

그룹 정책을 사용 하 여 설정 템플릿 카탈로그 경로를 구성 하는 경우 기본 Microsoft 서식 파일을 바꾸도록 선택할 수 있습니다. 기본 Microsoft 서식 파일을 바꾸도록 정책 설정을 구성한 경우 UE-V agent에 의해 설치 된 모든 기본 Microsoft 서식 파일이 컴퓨터에서 삭제 되 고 설정 서식 파일 카탈로그에 있는 템플릿만 사용 됩니다. `RegisterMSTemplates`기본 Microsoft 서식 파일을 무시 하려면 Ue-v 에이전트 구성 설정을 true로 설정 해야 합니다.

**참고**  사용 하도록 설정 된 후이 정책 설정을 사용 하지 않도록 설정 하면 UE-V agent가 기본 Microsoft 템플릿을 복원 하지 않습니다.

 

기본 Microsoft 서식 파일과 동일한 ID를 사용 하는 사용자 지정 서식 파일 카탈로그에 UE-V agent가 기본 Microsoft 서식 파일을 바꾸도록 구성 되어 있지 않은 경우 카탈로그의 Microsoft 서식 파일은 무시 됩니다.

UE-V PowerShell 기능을 사용 하 여 기본 템플릿을 바꿀 수도 있습니다. 기본 Microsoft 템플릿을 PowerShell로 바꾸려면 기본 Microsoft 서식 파일을 모두 등록 취소 한 다음 사용자 지정 된 서식 파일을 등록 합니다.

**참고**  이전 설정 패키지는 응용 프로그램에 대해 새 설정 템플릿을 배포 하는 경우에도 설정 저장소 위치에 남아 있습니다. 에이전트에서 이러한 패키지를 읽지는 않지만, 자동으로 삭제 되지는 않습니다.

 

## 관련 항목


[UE-V 1.0 계획](planning-for-ue-v-10.md)

[UE-V 1.0과 동기화할 응용 프로그램 계획](planning-which-applications-to-synchronize-with-ue-v-10.md)

[UE-V 구성 방법 계획](planning-for-ue-v-configuration-methods.md)

사용자 지정 서식 파일 배포 계획
 

 





