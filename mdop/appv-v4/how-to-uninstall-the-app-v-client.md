---
title: App-V Client 제거 방법
description: App-V Client 제거 방법
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816523"
---
# App-V Client 제거 방법


컴퓨터에서 응용 프로그램 가상화 클라이언트를 제거 하려면 다음 절차를 사용 합니다.

**Application Virtualization 데스크톱 클라이언트를 제거 하려면**

1.  제어판에서 **프로그램 추가/제거** (또는 Windows Vista에서 **프로그램 및 기능**)를 두 번 클릭 한 다음 **Microsoft Application Virtualization 데스크톱 클라이언트**를 두 번 클릭 합니다.

2.  표시 되는 대화 상자에서 **예** 를 클릭 하 여 제거 프로세스를 계속 합니다.

    **중요**  제거 프로세스는 취소 또는 중단할 수 없습니다.

     

3.  계속 하기 전에 Microsoft Application Virtualization 클라이언트 트레이 응용 프로그램을 닫아야 한다는 메시지가 나타나면 알림 영역의 App-v 아이콘을 마우스 오른쪽 단추로 클릭 하 고 **끝내기** 를 선택 하 여 응용 프로그램을 닫습니다. 그런 다음 **다시 시도** 를 클릭 하 여 제거 과정을 계속 합니다.

    **중요**  하나 이상의 가상 응용 프로그램을 사용 하 고 있다는 메시지가 표시 될 수 있습니다. 계속 하기 전에 열려 있는 응용 프로그램을 닫고 데이터를 저장 합니다. 그런 다음 **확인** 을 클릭 하 여 제거 과정을 계속 합니다.

     

4.  진행률 표시줄에 남은 시간이 표시 됩니다. 이 단계가 완료 되 면 제거 프로세스를 완료 하기 위해 모든 관련 드라이버를 중지할 수 있도록 컴퓨터를 다시 시작 해야 합니다.

    **참고**  제거 프로세스가 완료 된 후 다음 레지스트리 키가 남아 있습니다.

    -   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid

    -   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5

    -   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "Client" = dword: 00000000

    -   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey

     

## 관련 항목


[명령줄을 사용하여 클라이언트를 설치하는 방법](how-to-install-the-client-by-using-the-command-line-new.md)

[Application Virtualization Client를 수동으로 설치하는 방법](how-to-manually-install-the-application-virtualization-client.md)

[클라이언트에 가상 응용 프로그램을 게시하는 방법](how-to-publish-a-virtual-application-on-the-client.md)

 

 





