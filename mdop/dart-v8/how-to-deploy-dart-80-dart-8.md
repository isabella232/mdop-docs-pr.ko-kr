---
title: DaRT 8.0을 배포하는 방법
description: DaRT 8.0을 배포하는 방법
author: dansimp
ms.assetid: ab772e7a-c02f-4847-acdf-8bd362769a77
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e7d64297f7687ebc0a23add3aa749ee4719beee4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824298"
---
# DaRT 8.0을 배포하는 방법


다음 지침에서는 사용자 환경에서 Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0을 배포 하는 방법을 설명 합니다. DaRT 소프트웨어를 다운로드 하려면 MDOP를 [얻는 방법을](https://go.microsoft.com/fwlink/?LinkId=322049)참조 하세요. 한 관리자 컴퓨터에 모든 기능을 설치 하는 것으로 간주 됩니다. 예를 들어 전자 소프트웨어 배포 시스템을 사용 하 여 여러 컴퓨터에서 DaRT 8.0을 배포 하거나 제거 해야 하는 경우 명령줄 설치 옵션을 사용 하는 것이 더 쉬울 수 있습니다. 사용 가능한 명령줄 옵션에 대 한 설명과 예제는이 섹션에 나와 있습니다.

**중요**  DaRT를 설치 하기 전에, 모든 필수 소프트웨어를 설치 하 고 컴퓨터가 최소 시스템 요구 사항을 충족 하는지 확인 하기 위해 [dart 8.0에서 지원 되는 구성을](dart-80-supported-configurations-dart-8.md) 참조 하세요. DaRT를 설치 하는 컴퓨터는 Windows 8 또는 Windows Server 2012을 실행 해야 합니다.

 

다음 두 가지 구성 중 하나를 사용 하 여 DaRT를 설치할 수 있습니다.

-   Pc에 DaRT와 모든 DaRT 도구를 설치 합니다.

-   DaRT 복구 이미지를 만드는 데 필요한 도구만 관리자 컴퓨터에 설치한 다음 **원격 연결 뷰어** 를 설치 하 고 필요한 경우에는 헬프 데스크 컴퓨터에 **충돌 분석기** 를 설치 합니다.

DaRT 설치 파일은 32 비트 및 64 비트 버전에서 모두 사용할 수 있습니다. DaRT 복구 이미지 마법사를 실행 하는 컴퓨터의 아키텍처와 일치 하는 버전을 설치 합니다 (만들려는 복구 이미지의 컴퓨터 아키텍처가 아님).

DaRT 설치 파일 버전 중 하나를 사용 하 여 32 비트 또는 64 비트 컴퓨터에 대 한 복구 이미지를 만들 수 있지만, 32 비트 및 64 비트 컴퓨터에 대해 하나의 복구 이미지를 만들 수는 없습니다.

**관리자 컴퓨터에 DaRT 및 모든 DaRT 도구를 설치 하려면**

1.  DaRT 8.0 설치 관리자 파일의 32 비트 또는 64 비트 버전을 다운로드 합니다. DaRT를 설치 하는 컴퓨터와 일치 하는 아키텍처를 선택 하 고 DaRT 복구 이미지 마법사를 실행 합니다.

2.  DaRT 8.0을 다운로드 한 폴더에서 시스템 요구 사항에 해당 하는 **MSDaRT80.msi** 설치 파일을 실행 합니다.

3.  **Microsoft DaRT 8.0 설정 마법사 시작** 페이지에서 **다음**을 클릭 합니다.

4.  Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.

5.  **Microsoft 업데이트** 페이지에서 **업데이트를 확인할 때 microsoft Update 사용**을 선택 하 고 **다음**을 클릭 합니다.

6.  **설치 폴더 선택** 페이지에서 폴더를 선택 하거나 **다음** 을 클릭 하 여 기본 설치 위치에 DaRT를 설치 합니다.

7.  **설치 옵션** 페이지에서 설치 하려는 dart 기능을 선택 하거나 **다음** 을 클릭 하 여 모든 기능과 함께 DaRT를 설치 합니다.

8.  설치를 시작 하려면 **설치**를 클릭 합니다.

9.  설치가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 종료 합니다.

## 명령 프롬프트를 사용 하 여 관리자 컴퓨터에 DaRT 및 모든 DaRT 도구를 설치 하려면


DaRT를 설치 하거나 제거 하는 경우 명령 프롬프트에서 설치 파일을 실행 하는 옵션이 있습니다. 이 섹션에서는 명령 프롬프트에 DaRT를 설치 하거나 제거할 때 지정할 수 있는 다양 한 옵션의 몇 가지 예를 설명 합니다.

다음 예제에서는 모든 DaRT 기능을 설치 하는 방법을 보여 줍니다.

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

다음 예제에서는 DaRT 복구 이미지 마법사만 설치 하는 방법을 보여 줍니다.

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

다음 예제에서는 충돌 분석기와 DaRT 원격 연결 뷰어만 설치 하는 방법을 보여 줍니다.

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

다음 예제에서는 Windows Installer에 대 한 설치 로그를 만듭니다. 이는 디버깅 하는 데 유용 합니다.

``` syntax
msiexec.exe /i MSDaRT80.msi /l*v log.txt 
```

**참고**  /Qn 또는/qb를 추가 하 여 자동 설치를 수행할 수 있습니다.

 

**DaRT 설치의 유효성을 검사 하려면**

1.  **시작**을 클릭 하 고 **진단 및 복구 도구 집합**을 선택 합니다.

    **진단 및 복구 도구 집합** 창이 열립니다.

2.  설치를 위해 선택한 모든 DaRT 도구가 성공적으로 설치 되었는지 확인 합니다.

## 관련 항목


[관리자 컴퓨터에 DaRT 8.0 배포](deploying-dart-80-to-administrator-computers-dart-8.md)

 

 





