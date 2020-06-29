---
title: 프로젝트 템플릿을 만들고 사용하는 방법
description: 프로젝트 템플릿을 만들고 사용하는 방법
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814260"
---
# 프로젝트 템플릿을 만들고 사용하는 방법


앱-V 5.0 프로젝트 템플릿을 사용 하 여 기존 가상 응용 프로그램 패키지와 연결 된 일반적으로 적용 되는 설정을 저장할 수 있습니다. 그런 다음 해당 환경에서 새 가상 응용 프로그램 패키지를 만들 때 이러한 설정을 적용할 수 있습니다. 프로젝트 템플릿을 사용 하 여 가상 응용 프로그램 패키지를 만드는 프로세스를 간소화할 수 있습니다.

**참고**  패키지를 업그레이드 하는 동안 App-v 5.0 프로젝트 템플릿을 적용 하는 경우가 있습니다. 예를 들어 사용자 지정 제외 목록을 사용 하 여 응용 프로그램을 시퀀싱 한 경우에는 연결 된 템플릿을 만들고 저장 하 여 시퀀싱 된 응용 프로그램을 업그레이드 하는 동안 나중에 사용할 수 있도록 하는 것이 좋습니다.

App-v 5.0 Application 가속기는 응용 프로그램에 따라 다르며 앱-v 5.0 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있기 때문에 앱-V 5.0 프로젝트 템플릿은 앱-V 5.0 응용 프로그램 가속기와 다릅니다.

새 서식 파일을 만들고 적용 하려면 다음 절차를 사용 합니다.

**프로젝트 서식 파일을 만들려면**

1.  App-v 5.0 sequencer를 시작 하려면 sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization sequencer**를 클릭 합니다.

**참고**  가상 응용 프로그램 패키지가 현재 App-v 5.0 Sequencer 콘솔에 열려 있는 경우이 절차의 3 단계로 건너뛰십시오.

2. App-v 5.0 프로젝트 템플릿을 사용 하 여 저장 하려는 설정이 포함 된 기존 가상 응용 프로그램 패키지를 열려면 **파일**  /  **열기**를 클릭 한 다음 **패키지 편집**을 클릭 합니다. **패키지 선택** 페이지에서 **찾아보기를** 클릭 하 고 열려고 하는 가상 응용 프로그램 패키지를 찾습니다. **편집**을 클릭합니다.

3. 앱-V 5.0 Sequencer 콘솔에서 서식 파일을 저장 하려면 파일을 서식 파일로 **File**  /  **저장**을 클릭 합니다. 새 서식 파일과 함께 저장 되는 설정을 검토 한 후 **확인**을 클릭 합니다. 새 App-v 5.0 프로젝트 템플릿과 연결 되는 이름을 지정 합니다. 저장을 클릭 합니다.
   새 App-v 5.0 프로젝트 서식 파일은이 절차의 3 단계에서 지정한 디렉터리에 저장 됩니다.

**프로젝트 서식 파일을 적용 하려면**

**중요**  패키지 가속기와 함께 프로젝트 템플릿을 사용 하 여 가상 응용 프로그램 패키지를 만드는 기능은 지원 되지 않습니다.

1.  App-v 5.0 sequencer를 시작 하려면 sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization sequencer**를 클릭 합니다.

2.  App-v 5.0 프로젝트 템플릿을 사용 하 여 새 가상 응용 프로그램 패키지를 만들거나 업그레이드 하려면 서식 **파일**  /  **에서 새로 만들기**를 클릭 합니다.

3.  사용할 프로젝트 서식 파일을 선택 하려면 프로젝트 서식 파일이 저장 된 디렉터리로 이동 하 여 프로젝트 템플릿을 선택한 다음 **열기**를 클릭 합니다.

    새 가상 응용 프로그램 패키지를 만듭니다. 지정 된 서식 파일을 사용 하 여 저장 한 설정이 만들려는 새 가상 응용 프로그램 패키지에 적용 됩니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)









