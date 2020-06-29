---
title: App-V 5.1 Client 제거 방법
description: App-V 5.1 Client 제거 방법
author: dansimp
ms.assetid: 21f2d946-fc9f-4cd3-899b-ac52b3fbc306
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9338bef6b8a3123f9b8f49036427121987e7aa9f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813657"
---
# App-V 5.1 Client 제거 방법


컴퓨터에서 Microsoft App-v (Application Virtualization) 5.1 클라이언트를 제거 하려면 다음 절차를 사용 합니다. App-v 5.1 클라이언트를 제거 하면 클라이언트를 실행 하는 컴퓨터에 게시 된 모든 패키지도 제거 됩니다. 제거 작업이 완료 되지 않은 경우에는 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 패키지를 다시 게시 해야 합니다.

**중요**  
제거 절차를 수행 하기 전에 App-v 5.1 클라이언트 서비스가 실행 되 고 있는지 확인 해야 합니다.



**App-v 5.1 클라이언트를 제거 하려면**

1.  제어판에서 프로그램 제거 프로그램을 두 **번 클릭 한**  /  **Uninstall a Program**다음 **Microsoft Application Virtualization 클라이언트**를 두 번 클릭 합니다.

2.  표시 되는 대화 상자에서 **예** 를 클릭 하 여 제거 프로세스를 계속 합니다.

    **중요**  
    제거 프로세스는 취소 또는 중단할 수 없습니다.



3.  진행률 표시줄에 남은 시간이 표시 됩니다. 이 단계가 완료 되 면 제거 프로세스를 완료 하기 위해 모든 관련 드라이버를 중지할 수 있도록 컴퓨터를 다시 시작 해야 합니다.

    **참고**  
    명령줄을 사용 하 여 다음 스위치를 사용 하 여 App-v 5.1 클라이언트를 제거할 수도 **있습니다.**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## 관련 항목


[App-V 5.1 배포](deploying-app-v-51.md)









