---
title: 명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법
description: 명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816918"
---
# 명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법


명령줄을 사용 하 여 가상 응용 프로그램 패키지를 열 수 있습니다. 관리자 권한으로 **cmd** 프롬프트를 실행 해야 합니다.

명령줄을 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 열려면 다음 절차를 사용 합니다.

**명령줄을 사용 하 여 시퀀싱 된 응용 프로그램을 열려면**

1.  명령 프롬프트를 열려면 **시작**을 클릭 하 고 **실행**을 선택 하 고 **Cmd**를 입력 한 다음 **확인**을 클릭 합니다.

2.  명령 프롬프트에서 **cd\\** 를 입력 하 고 Sequencer가 설치 된 디렉터리의 경로를 지정한 다음 enter 키를 누릅니다 **.**

3.  명령 프롬프트에서 다음 명령을 입력 하 고 기울임꼴로 표시 된 텍스트를 값으로 바꿉니다.

    SFTSequencer/OPEN:*"열려고 하는 sprj 파일을 지정 합니다."*

    Enter **키를**누릅니다.

4.  다음 선택적 매개 변수를 지정할 수도 있습니다. 명령 프롬프트에서 다음 명령을 입력 하 고 기울임꼴로 표시 된 텍스트를 값으로 바꿉니다.

    /PACKAGENAME: "*패키지 이름을 지정 합니다."*

    /MSI-연결 된 Microsoft Windows Installer를 생성 하도록 지정 합니다.

    /COMPRESS – 패키지의 압축 여부를 지정 합니다. 기본적으로 패키지는 압축 되지 않습니다.

    Enter **키를**누릅니다.

    **참고**  설치 관리자 또는 Windows Installer 패키지에 그래픽 사용자 인터페이스가 있으면 명령줄 매개 변수를 지정한 후에 표시 됩니다.

     

## 관련 항목


[명령줄을 사용하여 가상 응용 프로그램을 관리하는 방법](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





