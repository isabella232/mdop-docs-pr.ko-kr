---
title: DaRT 8.0 정보
description: DaRT 8.0 정보
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821283"
---
# DaRT 8.0 정보


Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0는 Windows 기반 컴퓨터의 문제를 해결 하 고 복구 하는 데 도움이 됩니다. 여기에는 시작할 수 없는 컴퓨터도 포함 됩니다. DaRT 8.0은 WinRE (Windows 복구 환경)를 확장 하는 강력한 도구 집합입니다. DaRT를 사용 하 여 컴퓨터의 이벤트 로그 또는 시스템 레지스트리를 검사 하는 등의 문제를 분석 하 여 원인을 확인할 수 있습니다. DaRT는 파티션 (예: 주 파티션 및 논리 드라이브)을 포함 하는 기본 하드 디스크의 복구를 지원 하 고 볼륨 복구를 지원 합니다.

**참고**  DaRT는 동적 디스크의 복구를 지원 하지 않습니다.

 

DaRT는 원인을 파악 하는 즉시 문제를 해결 하는 데 도움이 되는 도구를 제공 하기도 합니다. 예를 들어 DaRT의 도구를 사용 하 여 결함이 있는 장치 드라이버를 사용 하지 않도록 설정 하 고, 삭제 된 파일을 복원 하 고, 컴퓨터에 맬웨어를 검색 하 여 설치 된 Windows 운영 체제를 시작할 수 없는 경우에도이 작업을 수행할 수 있습니다.

DaRT는 일반적으로 컴퓨터를 이미지로 복원 하는 것 보다 짧은 시간에 32 비트 또는 64 비트 버전의 Windows 8을 실행 하는 컴퓨터를 빠르게 복구 하는 데 도움이 될 수 있습니다.

DaRT의 기능을 통해 복구 이미지를 만들 수 있습니다. 복구 이미지는 Windows RE (Windows 복구 환경)를 시작 하 여 **진단 및 복구 도구 집합** 창을 시작 하 고 DaRT 도구에 액세스할 수 있습니다.

Dart 복구 **이미지 마법사** 를 사용 하 여 dart 복구 이미지를 만듭니다. 기본적으로 마법사는 ISO (국제 표준화 기구) 이미지 파일과 WIM (Windows Imaging Format) 파일을 만들고, 이미지를 CD, DVD 또는 USB에 구울 수 있도록 합니다. 이미지를 최종 사용자의 컴퓨터에 로컬로 배포 하거나 원격 네트워크 파티션이나 로컬 하드 드라이브의 복구 파티션에서 배포할 수 있습니다.

## <a href="" id="what-s-new-in-dart-8-0"></a>DaRT 8.0의 새로운 기능


DaRT 8.0는 Windows 8의 32 비트 또는 64 비트 버전을 실행 하는 컴퓨터를 빠르게 복구 하는 데 도움이 될 수 있습니다. 일반적으로 컴퓨터를 이미지로 전환 하는 데 걸리는 시간 보다 짧습니다. DaRT 8.0에는 다음과 같은 새로운 기능이 있습니다.

### Windows 8 또는 Windows Server 2012를 사용 하 여 DaRT 이미지 만들기

DaRT 8.0 Windows® 8 또는 Windows Server® 2012을 사용 하 여 DaRT 이미지를 만들 수 있습니다. Windows 8 이전 버전의 windows 또는 Windows Server 2012에서 고객은 이전 버전의 DaRT를 계속 사용 해야 합니다.

### 한 컴퓨터에서 32 및 64 비트 이미지 모두 생성

DaRT 8.0를 사용 하면 컴퓨터와 32 비트 또는 64 비트 컴퓨터 인지 여부에 관계 없이 DaRT를 실행 하는 단일 컴퓨터에서 32 비트 및 64 비트 이미지를 모두 생성할 수 있습니다. DaRT7에서 만든 이미지는 DaRT를 실행 하는 컴퓨터와 같은 비트 단위 여야 합니다.

### BIOS 또는 UEFI 인터페이스 중 하나가 있는 컴퓨터를 지 원하는 이미지 하나를 만듭니다.

통합 된 UEFI (Extensible 펌웨어 인터페이스) 및 BIOS 인터페이스 둘 다에 대 한 DaRT 8.0의 지원으로 두 인터페이스 중 하나를 사용 하는 컴퓨터에서 작동 하는 이미지만 만들 수 있습니다.

### GPT (GUID 파티션 테이블)를 사용 하 여 분할

DaRT 8.0 도구는 이제 이전 MBR (마스터 부트 레코드) 파티션 구성표 보다 디스크를 분할 하는 더욱 유연한 메커니즘을 제공 하는 Windows 8 GPT 디스크를 지원 합니다. DaRT 8.0 도구는 계속 MBR 파티션을 지원 합니다.

### 로컬 하드 디스크에 Windows 8 및 Windows Server 2012 설치

DaRT 8.0 도구는 Windows 8 및 Windows Server 2012이 로컬 하드 디스크에 설치 되어 있는 경우에만 사용할 수 있습니다. 현재 Windows To Go는 지원 되지 않습니다.

### <a href="" id="-------------dart-8-0-release-notes"></a> DaRT 8.0 릴리스 정보

이 문서에 대 한 자세한 내용 및 최신 뉴스에 대 한 자세한 내용은 [DaRT 8.0 릴리스 노트](release-notes-for-dart-80--dart-8.md)를 참조 하세요.

## DaRT 8.0를 얻는 방법


이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .

## 관련 항목


[DaRT 8.0 시작](getting-started-with-dart-80-dart-8.md)

[DaRT 8.0 릴리스 정보](release-notes-for-dart-80--dart-8.md)

 

 





