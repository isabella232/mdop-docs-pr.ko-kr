---
title: MED-V 2.0 배포 개요
description: MED-V 2.0 배포 개요
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826108"
---
# MED-V 2.0 배포 개요


이 섹션에서는 MED-V (Enterprise 데스크톱 가상화) 2.0를 설치 하 고 배포 하는 방법에 대 한 일반적인 정보와 지침을 제공 합니다.

## 개요


MED-V 2.0는 응용 프로그램을 배포 하는 데 사용 하는 것과 동일한 메서드를 사용 하 여 MED-V를 배포 하 고 관리 하는 응용 프로그램 모델을 기반으로 하 고 있습니다. 배포 된 MED-V 솔루션에는 MED-V 호스트 에이전트와 게스트 에이전트의 두 가지 구성 요소가 있습니다. MED-V 호스트 에이전트는 Windows 7 데스크톱에 설치 되 고 med-v 게스트 에이전트는 MED-V 작업 영역 내의 Windows XP에 설치 됩니다. MED-V에는 med-v 작업 영역을 만들고 구성 하는 데 필요한 정보와 도구를 제공 하는 MED-V 작업 영역 포장기도 포함 되어 있습니다.

**중요**  
MED-V는 MED-V 작업 영역 포장기, MED-V 호스트 에이전트, 모든 사용자에 대 한 MED-V 작업 영역의 설치만 지원 합니다. **ALLUSERS = ""** 를 선택 해야만 현재 사용자에 대해 med-v를 설치 하면 구성 요소 설치와 med-v 작업 영역의 설정에 오류가 발생 합니다.



### MED-V 설치 파일

MED-V는 MED-V를 실행 하는 데 필요한 다음 설치 파일을 포함 합니다.

**MED-V 호스트 에이전트 설치 파일**

호스트 에이전트 설치 파일의 이름은 MED-V\_HostAgent\_Setup.exe입니다. 이 파일은 전사적 배포의 일부로 각각의 관련 최종 사용자 컴퓨터에 배포 및 설치 됩니다.

**MED-V 작업 영역 포장기 설치 파일**

MED-V 작업 영역 포장기 설치 파일의 이름은 MED-V\_WorkspacePackager\_Setup.exe입니다. 이 파일을 사용 하 여 관리자 권한 및 사용 권한이 있는 컴퓨터에 MED-V 작업 영역 포장기를 설치 합니다. 데스크톱 관리자는 MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역을 만들고 관리 합니다.

**참고**  
MED-V 게스트 에이전트는 처음 설정 하는 동안 자동으로 설치 됩니다.



### MED-V 배포 프로세스

다음은 MED-V 설치 및 배포 프로세스의 상위 수준에 대 한 간략 한 설명입니다.

1.  관리 자격 증명이 있고 MED-V 작업 영역 패키지를 작성 하는 데 사용할 컴퓨터에 MED-V 작업 영역 포장기를 설치 합니다. 자세한 내용은 [Med-v 작업 영역 포장기를 설치 하는 방법을](how-to-install-the-med-v-workspace-packager.md)참조 하세요.

2.  Med-v 이미지를 준비 하 고 MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역 패키지를 만듭니다. 자세한 내용은 [med-v에 대 한 작업](operations-for-med-v.md)을 참조 하세요.

3.  엔터프라이즈 전체에 필요한 MED-V 구성 요소를 배포 합니다. MED-V의 필수 구성 요소는 Windows 가상 PC, MED-V 호스트 에이전트, MED-V 작업 영역입니다.

**중요**  
MED-V 구성 요소를 설치 하려면 관리 자격 증명이 필요 합니다. 최종 사용자가 MED-V를 설치 하는 경우 관리 자격 증명을 입력 하 라는 메시지가 표시 됩니다. 또한, ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 설치 하는 경우에는 관리 자격 증명을 컨텍스트에서 제공할 수 있습니다.



### MED-V 구성 요소

엔터프라이즈 전반에 걸쳐 배포 하는 MED-V 구성 요소는 다음과 같이 구성 됩니다.

**Windows 가상 PC**

MED-V는 호환성 솔루션을 위해 Windows 가상 PC 이미지 내에서 작동 합니다. Windows 가상 PC 및 Windows 7 용 업데이트 (KB977206)가 필요 합니다. 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

**MED-V 호스트 에이전트 설치 파일**

MED-V\_HostAgent\_Setup.exe.

**MED-V 작업 영역 설치 파일**

MED-V 작업 영역 설치 파일은 다음과 같이 구성 된 MED-V 작업 영역 패키지를 빌드할 때 만들어집니다.

MED-V 작업 영역 설치를 실행 하는 setup.exe 실행 프로그램

&lt;Med-v \ _workspace \ _name &gt; .msi 설치 관리자

&lt; &gt; 압축 된 가상 하드 디스크인 VHD \ _filename medv 파일

구성 설정 파일 ( &lt; 작업 영역 \ _name &gt; .reg 및 &lt; workspace \ _name &gt; . ps1)

MED-V를 배포 하려면 필요한 모든 설치 파일을 호스트 컴퓨터 또는 호스트 컴퓨터에서 액세스할 수 있는 공유에 복사 합니다. Windows 가상 PC, MED-V 호스트 에이전트, MED-V 작업 영역에 대 한 구성 요소 설치 파일을 실행 합니다. 그런 다음 MED-V 호스트 에이전트를 시작 하 여 MED-V의 첫 번째 설정을 완료 합니다.

수동으로 설치를 수행할 수 있습니다. 그러나 전자 소프트웨어 배포 방법을 사용 하 여 구성 요소의 배포를 자동화 하는 것이 좋습니다. 자세한 내용은 [전자 소프트웨어 배포 시스템을 통해 Med-v 작업 영역을 배포 하는 방법을](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)참조 하세요.

**참고**  
설치 옵션을 제어 하는 데 사용할 수 있는 명령줄 인수에 대 한 자세한 내용은 [Med-v 설치 파일의 명령줄 옵션](command-line-options-for-med-v-installation-files.md)을 참조 하세요.



## 배포 단계


엔터프라이즈 전체에 MED-V를 배포 하는 경우 설치 및 최초 설정에는 두 가지 주요 고려 사항이 있습니다.

### 설치

1.  **Windows 가상 PC** -설치 하는 동안 med-v는 WINDOWS 가상 Pc와 windows 7 (KB977206)에 대 한 필수 업데이트를 확인 합니다. 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    MED-V를 설치 하기 전에 Windows 7 설치의 일부로 이러한 항목을 설치 하거나 MED-V 배포의 일부로 설치할 수 있습니다. 그러나 MED-V에는 해당 배포에 대 한 메커니즘이 포함 되어 있지 않습니다. ESD (전자 소프트웨어 배포) 시스템을 사용 하거나 Windows 7 이미지의 일부로 배포 해야 합니다.

    **중요**  
    배치 파일을 사용 하 여 MED-V 구성 요소를 설치 하는 경우에는 MED-V 호스트 에이전트 및 MED-V 작업 영역 패키지 파일 뒤에 Windows 가상 PC 및 Windows 가상 PC 핫픽스가 설치 되도록 지정 하는 것이 가장 좋습니다. 즉, Windows Update는 다시 시작을 요구 하 여 설치 프로세스에 간섭이 발생 하지 않습니다.



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. **Med-v 호스트 에이전트** – med-v가 실행 되는 Windows 7 컴퓨터에 Med-v 호스트 에이전트를 설치 합니다. MED-V 작업 영역을 설치 하기 전에이를 설치 하 고 Windows 가상 PC가 설치 되어 있는지 확인 해야 합니다.

3. **Med-v 작업 영역** – Med-v 작업 영역 포장기를 사용 하 여이 설치에 필요한 파일 (setup.exe, medv, .msi 파일)을 만듭니다. MED-V 작업 영역을 설치 하려면 setup.exe를 실행 합니다. 이렇게 하면 다른 파일이 필요에 따라 트리거됩니다. 설치는 Windows가 시작 될 때 항상 MED-V를 실행 하는 MED-V 호스트 에이전트를 시작 하는 로컬 컴퓨터 실행 키 아래에 레지스트리의 항목을 배치 합니다.

   **중요**  
   MED-V 작업 영역의 설치는 최종 사용자가 대화형으로 실행 하거나 전자 소프트웨어 배포 시스템을 통해 자동으로 실행할 수 있습니다. MED-V 작업 영역 설치에는 관리 자격 증명이 필요 하므로 최종 사용자가 MED-V 작업 영역을 설치 하려면 컴퓨터의 관리자 여야 합니다. 또는 전자 소프트웨어 배포 시스템은 일반적으로 시스템 컨텍스트에서 실행 되며 충분 한 사용 권한이 있습니다.



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### 처음 설치 시

MED-V와 필수 구성 요소가 설치 된 후에는 MED-V를 구성 해야 합니다. MED-V 구성을 처음 설정 하는 것으로 알려져 있습니다. **Med-v 작업 영역 포장기**를 사용 하 여 처음으로 자동 또는 대화형으로 실행 되도록 구성할 수 있습니다. MED-V를 처음 설정 하는 경우에는 사용자가 MED-V 작업 영역에 대 한 인증을 위해 사용자의 암호를 입력 해야 하지만, 그렇지 않은 경우에는 거의 보이지 않을 수 있습니다. 알림은 처음 설치를 완료 하 고 응용 프로그램을 사용할 수 있는 경우와 같이 알림 영역에 표시 됩니다. 다음은 MED-V를 처음 설정할 때 발생 하는 작업입니다.

1.  가상 하드 디스크를 구성 해야 합니다. 최소 설정이 실행 되 고 Windows XP 이미지가 확장 됩니다. 일반적으로이는 숨겨진 창에서 발생 하지만 MED-V는이 구성 중에 표시 되도록 구성할 수 있습니다.

2.  최소 설정이 완료 되 면 ESD 소프트웨어나 다른 응용 프로그램 설치, 이미지 구성 등 추가 구성에 필요한 명령을 실행할 수 있습니다. 이는 Sysprep.inf 파일에서 호출할 수 있지만 필요 하지는 않습니다. 자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.

3.  Ftscompletion.exe는 구성의 마지막 단계로 실행 됩니다. 이 프로세스는 MED-V 구성을 완료 하 고, MED-V 작업 영역에 액세스 하 고, 로그를 복사 하 고, med-v 작업 영역이 준비 되었음을 알리는 신호를 허용 하 고, MED-V 작업 영역을 다시 시작 하도록 RDP 그룹에 사용자를 추가 합니다. 이 프로세스는 MED-V 작업 영역을 만들 때이를 구성한 경우 MED-V 작업 영역의 관리자로 사용자를 추가할 수도 있습니다. Ftscompletion.exe는 일반적으로 Sysprep, inf 파일을 통해 호출 되지만, 스크립트와 같은 다른 메서드를 통해 실행할 수도 있습니다. 그러나 Ftscompletion.exe는 워크스테이션이 구성 되었을 때 수행 되는 마지막 동작 이어야 합니다. 자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.

4.  Ftscompletion.exe에 의해 MED-V 작업 영역이 다시 시작 되 면 최종 사용자가 로그온 됩니다. 처음 설정 하는 동안 암호를 저장 하지 않은 경우 다시 메시지가 표시 됩니다. 그런 다음 MED-V 작업 영역이 시작 되 고 사용자 용으로 구성 됩니다. 구성에는 그룹 정책 적용이 포함 됩니다.

    Windows XP에 대 한 응용 프로그램 호환성 환경에 적합 한 정책만 적용 하는 것이 좋습니다. 예를 들어 데스크톱 개인 설정 정책은 일반적으로 적용할 필요가 없으며 사용 하지 않도록 설정 해야 합니다. 로컬 프로필만 허용 하는 방법에 대 한 자세한 내용은 [로밍 사용자 프로필 ()에 대 한 그룹 정책 설정](https://go.microsoft.com/fwlink/?LinkId=205072) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=205072) .

처음 설치를 완료 한 후 최종 사용자에 게는 게시 된 응용 프로그램이 준비 되었다는 알림이 표시 됩니다. 그런 다음 **시작** 메뉴에서 med-v 작업 영역에 설치 된 응용 프로그램에 액세스할 수 있습니다.

## 관련 항목


[MED-V 배포 환경 준비](prepare-the-deployment-environment-for-med-v.md)

[MED-V 배포](deployment-of-med-v.md)









