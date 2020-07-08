---
title: UE-V 1.0 배포
description: UE-V 1.0 배포
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827148"
---
# UE-V 1.0 배포


Microsoft UE-V (User Experience Virtualization)에서 지 원하는 다양 한 배포 구성이 있습니다. 이 섹션에는 배포의 여러 단계에서 완료 해야 하는 작업을 성공적으로 수행 하는 데 도움이 되는 일반적인 정보와 단계별 절차가 포함 되어 있습니다.

## UE-V에 대 한 배포 정보


UE-V 배포의 경우 네트워크 공유에 설정 저장소 위치와 설정을 동기화 하는 모든 컴퓨터에 UE-V agent가 설치 되어 있어야 합니다. Ue-v 그룹 정책 템플릿을 사용 하 여 UE-V 설정을 관리할 수 있습니다. 다음 항목에서는 이러한 기능을 배포 하는 방법에 대해 설명 합니다.

[UE-V 1.0에 대한 설정 저장소 위치 배포](deploying-the-settings-storage-location-for-ue-v-10.md)

모든 UE-V 배포에는 동기화 된 설정 값이 포함 된 설정 패키지가 있는 설정 저장소 위치가 필요 합니다.

[UE-V 에이전트 배포](deploying-the-ue-v-agent.md)

UE-V를 사용 하 여 설정을 동기화 하려면 컴퓨터에 UE-V Agent가 설치 되어 실행 중 이어야 합니다.

[UE-V 그룹 정책 ADMX 템플릿 설치](installing-the-ue-v-group-policy-admx-templates.md)

UE-V 에이전트 및 표준 UE-V 구성을 배포 하기 전에 그룹 정책을 사용 하 여 UE-V 설정을 미리 구성할 수 있습니다.

## 사용자 지정 서식 파일 배포 배포 정보


UE-V에 포함 된 Microsoft 응용 프로그램 (예: lob (기간 업무) 응용 프로그램)이 아닌 다른 응용 프로그램에 대 한 사용자 지정 설정 위치 템플릿을 만들려는 경우 설정 서식 파일 카탈로그를 배포 하 고 UE-V 생성기를 설치 하 여 해당 템플릿을 만들어야 합니다. 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.

[UE-V 생성기 설치](installing-the-ue-v-generator.md)

UE-V 생성기를 사용 하 여 기본 응용 프로그램 이외의 응용 프로그램 설정을 동기화 하는 데 도움이 되는 사용자 지정 설정 위치 템플릿을 만들고 편집 하 고 유효성을 검사 합니다.

[UE-V 1.0에 대한 설정 템플릿 카탈로그 배포](deploying-the-settings-template-catalog-for-ue-v-10.md)

UE-V Agent의 기본 응용 프로그램이 아닌 다른 응용 프로그램을 지원 하기 위해 사용자 지정 설정 위치 템플릿을 배포 해야 하는 경우이를 저장할 설정 템플릿 카탈로그를 구성 해야 합니다.

[UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

UE-V 에이전트의 기본 응용 프로그램이 아닌 다른 응용 프로그램을 동기화 해야 하는 경우 UE-V 생성기를 사용 하 여 만든 사용자 지정 설정 위치 템플릿을 UE-V 설정 템플릿 카탈로그에 배포할 수 있습니다.

**참고**  사용자 지정 서식 파일을 배포 하려면 설정 서식 파일 카탈로그가 필요 합니다. 기본 Microsoft 응용 프로그램 템플릿은 UE-V Agent를 사용 하 여 배포 됩니다.

 

## 이 제품에 대 한 항목


[Microsoft User Experience Virtualization(UE-V) 1.0](index.md)

[User Experience Virtualization 1.0 시작](getting-started-with-user-experience-virtualization-10.md)

[UE-V 1.0 계획](planning-for-ue-v-10.md)

[UE-V 1.0 작업](operations-for-ue-v-10.md)

[UE-V 1.0 문제 해결](troubleshooting-ue-v-10.md)

 

 





