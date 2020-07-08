---
title: Sequencer Console 정보
description: Sequencer Console 정보
author: dansimp
ms.assetid: 36ecba89-a0f5-4d4d-981c-7f581aa43695
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 21d1c668e9d6cbd51dd852cf40799d5df072bb00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819908"
---
# Sequencer Console 정보


Microsoft App-v (Application Virtualization) sequencer를 사용 하기 전에 App-v 시퀀서 콘솔에 대 한 다음 정보를 숙지 해야 합니다. 다음 섹션에서는 Sequencer 콘솔에서 사용할 수 있는 도구에 대해 설명 합니다.

## Application Virtualization Sequencer 콘솔 메뉴 옵션


App-v Sequencer 콘솔에서 사용할 수 있는 메뉴 항목은 다음과 같습니다.

-   **File** -시퀀싱 된 응용 프로그램을 만들고, 열고, 수정 하 고, 저장 하는 데 도움이 되는 다양 한 명령이 있습니다.

-   **편집** -기존 가상 응용 프로그램을 편집 하기 위한 다양 한 명령이 포함 되어 있습니다.

-   **보기** -가상 응용 프로그램의 속성을 보기 위한 다양 한 명령이 포함 되어 있습니다.

-   **도구** -가상 응용 프로그램을 구성 하기 위한 다양 한 도구와 진단이 포함 되어 있습니다.

## <a href="" id="application-virtualization-sequencer-console-toolbar-options-"></a>Application Virtualization Sequencer 콘솔 도구 모음 옵션


App-v 시퀀서 콘솔에서 사용할 수 있는 도구 모음 단추는 다음과 같습니다.

-   **새 패키지** -를 클릭 하 여 새 시퀀싱 된 응용 프로그램을 만듭니다.

-   **열기** -클릭 하 여 앱-V 시퀀서 콘솔에서 시퀀싱 된 응용 프로그램 패키지를 엽니다.

-   **업그레이드를 위해 열고** , 업데이트를 업그레이드 하거나 적용 하려면 클릭 하 여 시퀀싱 된 응용 프로그램을 엽니다.

-   **저장** -클릭 하 여 시퀀싱 된 가상 응용 프로그램을 저장 합니다.

-   **시퀀싱 마법사** -시퀀싱 마법사를 열려면 클릭 합니다. **도구**옵션 아래의 **일반** 탭에서 변경 작업을 수행 하는 경우 시퀀싱 마법사를 시작 하려면이 단추를 사용 해야 합니다  /  **Options**.

## 가상 응용 프로그램 탭


App-v Sequencer 콘솔에서 가상 응용 프로그램을 볼 때 다음 탭이 표시 됩니다.

-   **속성** -선택한 가상 응용 프로그램에 대 한 정보를 표시 합니다. 가상 응용 프로그램과 연결 된 패키지 이름 및 설명을 업데이트할 수 있습니다.

-   **배포** -대상 컴퓨터에서 가상 응용 프로그램에 액세스 하는 방법에 대 한 정보를 표시 합니다. 가상 응용 프로그램 배달 방법을 구성할 수 있으며 대상 컴퓨터에서 실행 해야 하는 운영 체제를 구성할 수 있습니다. 연결 된 출력 옵션을 구성할 수도 있습니다. 클라이언트가 파일의 가상 응용 프로그램에 액세스 하도록 하려는 경우 경로를 지정할 때 다음과 같은 형식을 사용 합니다. **File://server/share/path/.sft**. 업그레이드 중에 패키지와 연결 된 보안을 유지 하려면 **보안 설명자 적용** 을 선택 하 고, 업그레이드 중에는 해당 권한이 다시 설정 됩니다.

-   **변경 내용** -가상 응용 프로그램에 대 한 업데이트에 대 한 정보를 표시 합니다.

-   **Files** -선택한 가상 응용 프로그램과 연결 된 파일을 표시 합니다. 적절 한 필드를 사용 하 여 관련 파일 속성을 약간만 수정할 수 있습니다.

-   **가상 레지스트리** -선택한 가상 응용 프로그램과 연결 된 가상 레지스트리가 표시 됩니다. 적절 한 항목을 마우스 오른쪽 단추로 클릭 하 여 레지스트리 키를 추가 하거나 삭제할 수 있습니다.

-   **가상 파일 시스템** -선택한 가상 응용 프로그램과 연결 된 가상 파일 시스템을 표시 합니다. 해당 항목을 마우스 오른쪽 단추로 클릭 하 고 옵션을 선택 하 여이 탭에서 파일 시스템 항목을 추가, 삭제 또는 편집할 수 있습니다.

-   **가상 서비스** -선택한 가상 응용 프로그램과 연결 된 서비스를 표시 합니다.

-   **Osd** -가상 응용 프로그램과 연결 된 Osd (개방형 소프트웨어 설명자)에 대 한 정보를 표시 합니다. 해당 항목을 마우스 오른쪽 단추로 클릭 하 고 원하는 작업을 선택 하 여 OSD 파일과 연결 된 파일을 업데이트할 수 있습니다.

## 관련 항목


[Application Virtualization Sequencer 개요](application-virtualization-sequencer-overview.md)

 

 





