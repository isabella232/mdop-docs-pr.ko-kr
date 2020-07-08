---
title: App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법
description: App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817648"
---
# App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법


앱-V 프로젝트 템플릿을 사용 하 여 기존 가상 응용 프로그램 패키지와 연결 된 일반적으로 적용 되는 설정을 저장할 수 있습니다. 이러한 설정은 가상 응용 프로그램 패키지를 만드는 프로세스를 간소화 하는 데 도움이 될 수 있는 환경에서 새 가상 응용 프로그램 패키지를 만들 때 적용할 수 있습니다.

**참고**  새 가상 응용 프로그램 패키지를 만들 때만 App-v 프로젝트 템플릿을 적용할 수 있습니다. 기존 가상 응용 프로그램 패키지에 프로젝트 템플릿을 적용 하는 것은 지원 되지 않습니다.

 

App-v 프로젝트 템플릿을 적용 하는 방법에 대 한 자세한 내용은 [App-v 프로젝트 템플릿 적용 방법 (app-v 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)을 참조 하세요.

App-v 응용 프로그램 가속기는 응용 프로그램에 따라 다르며 앱-v 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있으므로 app-v 프로젝트 템플릿은 앱-v 응용 프로그램 가속기와 다릅니다. 또한 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들 때는 프로젝트 템플릿을 사용할 수 없습니다.

다음 일반 설정은 App-v 프로젝트 템플릿과 함께 저장 됩니다.

-   **고급 모니터링 옵션** 모니터링 하는 동안 Microsoft Update를 실행할 수 있도록 설정 하 고 .dll을 다시 기준으로 합니다 **.**

-   **패키지 배포 설정** **프로토콜**, **호스트 이름**, **포트**, **경로**, **운영**체제, **보안 설명자 적용**, **MSI 만들기**, **압축 패키지**를 포함 합니다.

-   **일반 옵션** **Microsoft Windows Installer (MSI)** 패키지를 생성 하 고, **이벤트 가상화 허용**, **서비스 가상화 허용**, **패키지 버전을 파일 이름에 추가**하도록 허용 합니다.

-   **제외 항목** 제외 패턴 목록을 포함 합니다.

**프로젝트 서식 파일을 만들려면**

1.  App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.

2.  가상 응용 프로그램 패키지가 현재 App-v Sequencer에서 열려 있는 경우이 절차의 3 단계로 건너뜁니다. 앱-V 프로젝트 템플릿을 사용 하 여 저장할 설정이 포함 된 기존 가상 응용 프로그램 패키지를 열려면 **파일**  /  **열기** 를 클릭 하 고 **패키지** **편집** 을 클릭 합니다. **패키지 선택** 페이지에서 **찾아보기를** 클릭 하 고 열려고 하는 가상 응용 프로그램 패키지를 찾습니다. **편집**을 클릭합니다.

3.  App-v Sequencer 콘솔에서 **파일**  /  **을 서식 파일로 저장**을 클릭 합니다. 새 서식 파일과 함께 저장 되는 설정을 검토 한 후 **확인**을 클릭 합니다. 새 App-v 프로젝트 템플릿과 연결 되는 이름을 지정 합니다. **Save**을 클릭합니다.

    새 App-v 프로젝트 템플릿은이 절차의 3 단계에서 지정한 디렉터리에 저장 됩니다.

## 관련 항목


[Application Virtualization Sequencer(App-V 4.6 SP1)에 대한 작업](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[App-V 프로젝트 템플릿(App-V 4.6 SP1)을 적용하는 방법](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





