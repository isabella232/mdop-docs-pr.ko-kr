---
title: UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포
description: UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827123"
---
# UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포


Microsoft UE-V (User Experience Virtualization)는 사용자 환경 가상화에 의해 캡처되고 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다. UE-V는 사용자 지정 설정 위치 템플릿을 만들 수 있는 도구인 UE-V 생성기와 같은 표준 템플릿 집합을 포함 합니다. 설정 위치 템플릿을 만든 후에는 테스트 환경에서 응용 프로그램 설정이 올바르게 로밍 되는지 확인 하도록 테스트 해야 합니다. 그러면 설정 위치 템플릿을 엔터프라이즈의 컴퓨터에 안전 하 게 배포할 수 있습니다.

설정 위치 템플릿은 엔터프라이즈 소프트웨어 배포 (ESD), 그룹 정책 기본 설정 또는 UE-V 설정 템플릿 카탈로그 구성을 사용 하 여 배포할 수 있습니다. ESD 또는 그룹 정책을 사용 하 여 배포 된 서식 파일은 UE-V WMI 또는 PowerShell을 통해 등록 되어야 합니다. 설정 서식 파일 카탈로그 위치에 저장 된 서식 파일은 UE-V agent에서 자동으로 등록 합니다.

## 설정 템플릿 카탈로그 경로를 사용 하 여 설정 위치 템플릿 배포


UE-V 설정 위치 템플릿 카탈로그 경로는 그룹 정책, 에이전트 설치 명령줄 매개 변수, WMI 또는 PowerShell 등의 메서드를 사용 하 여 정의할 수 있습니다. 서식 파일 카탈로그 경로를 정의한 후에는 UE-V agent가이 위치에서 새 서식 파일 또는 업데이트 된 템플릿을 검색 합니다. UE-V agent는 하루에이 위치를 확인 하 고이 폴더에 있는 서식 파일을 기반으로 동기화 동작을 업데이트 합니다. 마지막 검사 이후이 폴더에서 추가 되거나 업데이트 된 서식 파일이 UE-V agent에 의해 등록 됩니다. 또한 UE-V agent는이 폴더에서 제거 된 템플릿의 등록을 취소 합니다. 작업 스케줄러에서 서식 파일을 하루에 한 번씩 등록 하 고 등록 취소 했습니다.

**설정 템플릿 카탈로그 경로를 사용 하 여 UE-V 설정 위치 템플릿을 배포 하려면**

1.  설정 템플릿 카탈로그로 정의 된 네트워크 공유 폴더로 이동 합니다.

2.  UE-V 컴퓨터에 대 한 원하는 UE-V agent 템플릿 구성을 반영 하도록 설정 템플릿 카탈로그에서 설정 위치 템플릿을 추가, 제거 또는 업데이트 합니다.

3.  컴퓨터의 서식 파일은 설정 템플릿 카탈로그에 대 한 변경 내용에 따라 매일 업데이트 됩니다.

4.  관리자 권한 명령 프롬프트를 열고 **% program filesws Microsoft 사용자 환경 가상화 \\ 에이전트 \ \ &lt; x86 또는 x64 &gt; **로 이동한 다음 **ApplySettingsTemplateCatalog.exe** 를 실행 하 여 ue-v Agent를 실행 하는 컴퓨터의 템플릿을 수동으로 업데이트 합니다.

## 관련 항목


[Microsoft User Experience Virtualization(UE-V) 1.0](index.md)

[UE-V 1.0 배포](deploying-ue-v-10.md)

[UE-V 1.0과 동기화할 응용 프로그램 계획](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





