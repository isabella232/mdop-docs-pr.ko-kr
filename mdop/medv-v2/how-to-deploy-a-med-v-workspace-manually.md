---
title: 수동으로 MED-V 작업 영역을 배포하는 방법
description: 수동으로 MED-V 작업 영역을 배포하는 방법
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827278"
---
# 수동으로 MED-V 작업 영역을 배포하는 방법


경우에 따라 회사에서 전자 소프트웨어 배포 시스템을 사용 하 여 응용 프로그램을 배포 하지 않는 경우와 같이 MED-V 작업 영역을 수동으로 배포 하는 것이 좋습니다.

이 섹션에서는 MED-V 작업 영역을 수동으로 배포 하는 방법에 대 한 지침을 제공 합니다.

**수동으로 MED-V 작업 영역을 배포 하려면**

1.  모든 필수 구성 요소 응용 프로그램과 MED-V 작업 영역 패키지 파일을 공유 드라이브나 DVD에 복사 합니다. 다음은 필수 응용 프로그램 및 파일의 목록입니다.

    -   **Windows 가상 PC** 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    -   **Windows 가상 PC 추가 및 업데이트** 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    -   **Med-v 호스트 에이전트 설치 파일** – 호스트 에이전트 (Med-v-v _HostAgent \ _Setup 설치 파일)를 설치 합니다.

        **Warning**  
        MED-V 호스트 에이전트를 설치 하기 전에 Internet Explorer를 닫은 경우 나중에 URL 리디렉션으로 충돌이 발생할 수 있습니다. 배포 중에 컴퓨터 다시 시작을 지정 하 여이 작업을 수행할 수도 있습니다.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. 나열 된 순서 대로 다음을 설치 합니다. 최종 사용자가이 작업을 수동으로 수행할 수도 있고 스크립트를 만들어 다음을 설치할 수도 있습니다.

   -   Windows 가상 PC 및 Windows 가상 PC 추가 및 업데이트 컴퓨터를 다시 시작 해야 합니다.

   -   MED-V 호스트 에이전트

       **참고**  
       실행 중인 경우 MED-V 호스트 에이전트 설치를 완료 하려면 먼저 Internet Explorer를 다시 시작 해야 합니다.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. 처음 설치할 때 완료 합니다.

   MED-V 작업 영역을 설치한 후에는 MED-V를 시작 하는 옵션이 있습니다. 이렇게 하면 MED-V 호스트 에이전트가 시작 됩니다. 해당 시점에 MED-V를 시작 하거나 나중에 MED-V 호스트 에이전트를 시작 하 여 처음 설치를 완료할 수 있습니다.

   MED-V 호스트 에이전트를 시작 하려면 **시작**을 클릭 하 고 **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 호스트 에이전트**를 클릭 합니다.

## 관련 항목


[전자 소프트웨어 배포 시스템을 통해 MED-V 작업 영역을 배포하는 방법](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[MED-V 작업 영역 패키지 배포](deploying-the-med-v-workspace-package.md)









