---
title: DaRT 7.0을 배포하는 방법
description: DaRT 7.0을 배포하는 방법
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813049"
---
# DaRT 7.0을 배포하는 방법


이 항목에서는 환경에 Microsoft 진단 및 복구 도구 집합 (DaRT) 7을 배포 하는 지침을 제공 합니다. 이 항목의 첫 번째 절차에서는 한 관리자 컴퓨터에 모든 기능을 설치 하 고 있다고 가정 합니다. 예를 들어 전자 소프트웨어 배포 시스템을 사용 하 여 여러 컴퓨터에서 DaRT를 배포 하거나 제거 해야 하는 경우 명령줄 설치 옵션을 사용 하는 것이 더 쉬울 수 있습니다. 이러한 옵션은 사용 가능한 명령줄 옵션에 대 한 사용 예를 제공 하는이 항목의 두 번째 절차에 정의 되어 있습니다.

**중요**  DaRT를 설치 하기 전에 컴퓨터가 [DaRT 7.0 지원 구성](dart-70-supported-configurations-dart-7.md)에 나열 된 최소 시스템 요구 사항을 충족 하는지 확인 합니다.

 

**관리자 컴퓨터에 DaRT를 설치 하려면**

1.  소프트웨어 다운로드의 일부로 받은 DaRT 설치 파일을 찾습니다.

2.  시스템 요구 사항에 해당 하는 DaRT 설치 파일을 32 비트 또는 64 비트 중에서 두 번 클릭 합니다. DaRT 설치 파일의 이름은 **MSDaRT70.msi**입니다.

3.  Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.

4.  DaRT를 설치 하기 위한 대상 폴더를 선택 하 고 모든 사용자에 대해 DaRT를 설치 해야 하는지, 현재 사용자만 설치할 것인지를 선택한 후 **다음**을 클릭 합니다.

5.  설치를 **일반**또는 **사용자 지정**또는 **완료**로 선택 하 고 **다음**을 클릭 합니다.

    -   **일반적** 으로 가장 자주 사용 되는 도구를 설치 합니다. 이 방법은 대부분의 사용자에 게 좋습니다.

    -   **사용자 지정** 을 사용 하면 설치 된 도구와 설치 위치를 선택할 수 있습니다. 이는 다른 헬프 데스크 컴퓨터에 서로 다른 DaRT 도구를 설치 하는 경우 고급 사용자에 게 적합 합니다.

    -   **완료** -모든 DaRT 도구를 설치 하 고 가장 많은 디스크 공간을 필요로 합니다.

    설치 방법을 선택한 후 **다음**을 클릭 합니다.

6.  설치를 시작 하려면 **설치**를 클릭 합니다.

7.  설치가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 종료 합니다.

**명령 프롬프트에서 DaRT를 설치 하려면**

1.  다음 예제에서는 모든 DaRT 기능을 설치 하는 방법을 보여 줍니다.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  다음 예제에서는 **DaRT 복구 이미지 마법사**만 설치 하는 방법을 보여 줍니다.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  다음 예제에서는 충돌 분석기와 DaRT 원격 연결 뷰어만 설치 하는 방법을 보여 줍니다.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  다음 예제에서는 Windows Installer에 대 한 설치 로그를 만듭니다. 이는 디버깅 하는 데 유용 합니다.

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

**참고**  DaRT 설치 명령 프롬프트 옵션에/qn 또는/qb를 추가 하 여 자동 설치를 수행할 수 있습니다.

 

## 관련 항목


[관리자 컴퓨터에 DaRT 7.0 배포](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





