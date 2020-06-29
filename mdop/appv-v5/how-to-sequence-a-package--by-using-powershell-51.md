---
title: PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법
description: PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법
author: dansimp
ms.assetid: 6134c6be-937d-4609-a516-92d49154b290
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1bc2933fdb64080dab3b514784e7f68b0236df9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813692"
---
# PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법


PowerShell을 사용 하 여 새 App-v 5.1 패키지를 만들려면 다음 절차를 사용 합니다.

**참고**  이 절차를 사용 하기 전에 연결 된 설치 관리자 파일을 sequencer를 실행 하는 컴퓨터에 복사 하 고 [app-v 5.1 시퀀서 및 클라이언트 배포에 대 한 계획](planning-for-the-app-v-51-sequencer-and-client-deployment.md)의 sequencer 섹션을 읽고 이해 해야 합니다.

 

**PowerShell을 사용 하 여 새 가상 응용 프로그램을 만들려면**

1.  App-v 5.1 sequencer를 설치 합니다. Sequencer를 설치 하는 방법에 대 한 자세한 내용은 [sequencer를 설치 하는 방법을](how-to-install-the-sequencer-51beta-gb18030.md)참조 하세요.

2.  PowerShell 콘솔을 열려면 **시작** 을 클릭 하 고 **powershell**을 입력 합니다. **Windows PowerShell**을 마우스 오른쪽 단추로 클릭하고 **관리자 권한으로 실행**을 선택합니다.

3.  PowerShell 콘솔을 사용 하 여 **appvsequencer: import 모듈**을 입력 합니다.

4.  패키지를 만들려면 **New AppvSequencerPackage** cmdlet을 사용 합니다. 패키지를 만들려면 다음 매개 변수가 필요 합니다.

    -   **Name** -패키지의 이름을 지정 합니다.

    -   **Primaryvirtualapplicationdirectory** -응용 프로그램을 설치 하는 데 사용 되는 디렉터리 경로를 지정 합니다. 이 경로는 반드시 존재 해야 합니다.

    -   **설치 관리자** -연결 된 응용 프로그램 설치 관리자의 경로를 지정 합니다.

    -   **Path** -패키지의 출력 디렉터리를 지정 합니다.

    예:

    **AppvSequencerPackage-패키지 &lt; &gt; 루트-설치 관리자 경로에 대 한 package의 virtualapplicationdirectory 경로의 이름입니다. &lt; &gt; &lt; 출력 경로의 설치 관리자 실행 파일 이름 &gt; -OutputPath &lt; 디렉터리&gt;**

    Sequencer가 패키지를 만들 때까지 기다립니다. PowerShell을 사용 하 여 패키지를 만들면 시간이 걸릴 수 있습니다. 패키지가 제대로 만들어지지 않은 경우 오류가 반환 됩니다.

    다음 목록에는 **새 AppvSequencerPackage** cmdlet에 사용할 수 있는 추가 선택적 매개 변수가 표시 됩니다.

    -   AcceleratorFilePath – 패키지를 생성 하는 데 대 한 가속기 .cab 파일 경로를 지정 합니다.

    -   InstalledFilesPath-로컬에 설치 된 응용 프로그램 파일이 저장 되는 경로를 지정 합니다.

    -   InstallMediaPath-설치 미디어가 있는 위치에 대 한 경로를 지정 합니다.

    -   서식 파일 경로 수-시퀀싱 프로세스를 사용자 지정 하려는 경우 서식 파일에 대 한 경로를 지정 합니다.

    -   FullLoad-패키지를 열기 전에 앱-V 5.1를 실행 하는 컴퓨터에 완전히 다운로드 되도록 지정 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[PowerShell을 사용하여 App-V 5.1 관리](administering-app-v-51-by-using-powershell.md)

 

 





