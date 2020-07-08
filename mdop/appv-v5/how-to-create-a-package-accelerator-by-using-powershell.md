---
title: PowerShell을 사용하여 패키지 가속기를 만드는 방법
description: PowerShell을 사용하여 패키지 가속기를 만드는 방법
author: dansimp
ms.assetid: 8e527363-d961-4153-826a-446a4ad8d980
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4270db9a5f0603cff1f33e6244a5abb517572d97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814297"
---
# PowerShell을 사용하여 패키지 가속기를 만드는 방법


앱-V 5.0 패키지 가속기는 대규모의 복잡 한 응용 프로그램을 자동으로 시퀀싱 합니다. 또한 App-v 5.0 패키지 가속기를 적용 하는 경우 가상화 된 패키지를 만들기 위해 수동으로 응용 프로그램을 설치 해야 하는 것은 아닙니다.

**패키지 가속기를 만들려면**

1.  App-v 5.0 sequencer를 설치 합니다. Sequencer를 설치 하는 방법에 대 한 자세한 내용은 [sequencer를 설치 하는 방법을](how-to-install-the-sequencer-beta-gb18030.md)참조 하세요.

2.  PowerShell 콘솔을 열려면 **시작** 을 클릭 하 고 **powershell**을 입력 합니다. **Windows PowerShell**을 마우스 오른쪽 단추로 클릭하고 **관리자 권한으로 실행**을 선택합니다. **새로운 AppvPackageAccelerator** cmdlet을 사용 합니다.

3.  패키지 가속기를 만들려면, 설치 미디어 또는 설치 파일에서 바로 연결을 만들 수 있도록 하 고, 액셀러레이터 키를 사용 하는 사용자를 위한 추가 정보 파일을 선택 해야 합니다. 패키지 가속기 cmdlet을 사용 하려면 다음 매개 변수가 필요 합니다.

    -   **InstalledFilesPath** -응용 프로그램 설치 경로를 지정 합니다.

    -   **설치 관리자** – 응용 프로그램 설치 미디어 경로를 지정 합니다.

    -   **InputPackagePath** – appv 패키지의 경로를 지정 합니다.

    -   **Path** – 패키지의 출력 디렉터리를 지정 합니다.

    다음 예에서는 appv 패키지와 설치 미디어를 사용 하 여 패키지 가속기를 만드는 방법을 보여 줍니다.

    **New-AppvPackageAccelerator-InputPackagePath &lt; 경로에 대 한 설치 관리자 &gt; 경로- &lt; &gt; 출력 경로의 설치 관리자 실행 파일의 경로 &lt; 디렉터리&gt;**

    **AppvPackageAccelerator** cmdlet에 사용할 수 있는 추가 선택적 매개 변수는 다음 목록에 표시 됩니다.

    -   **AcceleratorDescriptionFile** -사용자가 만든 패키지 가속기 지침에 대 한 경로를 지정 합니다. 패키지 가속기 지침은 패키지 가속기를 사용 하 여 만든 패키지와 함께 패키지 되는 **.txt** 또는 **.rtf** 설명 파일입니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[PowerShell을 사용하여 App-V 관리](administering-app-v-by-using-powershell.md)

 

 





