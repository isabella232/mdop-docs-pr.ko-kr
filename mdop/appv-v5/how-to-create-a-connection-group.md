---
title: 연결 그룹을 만드는 방법
description: 연결 그룹을 만드는 방법
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814340"
---
# 연결 그룹을 만드는 방법


이 단계를 사용 하 여 App-v 관리 콘솔을 사용 하 여 연결 그룹을 만듭니다. PowerShell을 사용 하 여 연결 그룹을 만들려면 [powershell을 사용 하 여 독립 실행형 컴퓨터에서 연결 그룹을 관리 하는 방법을](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md)참조 하세요.

패키지를 연결 그룹에 배치 하면 패키지 루트 경로가 병합 됩니다. 패키지를 제거 하는 경우 나머지 패키지만 병합 된 루트를 유지 관리 합니다.

**연결 그룹을 만들려면**

1.  App-v 5.0 관리 콘솔에서 **패키지**를 선택 합니다.

2.  연결 **그룹** 을 선택 하 여 연결 그룹 라이브러리를 표시 합니다.

3.  **연결 그룹 추가** 를 선택 하 여 새 연결 그룹을 만듭니다.

4.  **새 연결 그룹** 창에서 그룹에 대 한 설명을 입력 합니다.

5.  연결 **된 패키지** 창에서 **편집** 을 클릭 하 여 새 응용 프로그램을 연결 그룹에 추가 합니다.

6.  **패키지 전체 라이브러리** 창에서 추가할 응용 프로그램을 선택 하 고 화살표를 클릭 하 여 응용 프로그램을 추가 합니다.

    응용 프로그램을 제거 하려면 **패키지** 창에서 제거할 응용 프로그램을 선택 하 고 화살표를 클릭 합니다.

    연결 그룹의 응용 프로그램에 대 한 우선 순위를 해당 하려면 **패키지** 창의 화살표를 사용 합니다.

    **중요**  기본적으로 특정 응용 프로그램과 연결 된 Active Directory 도메인 서비스 액세스 구성은 연결 그룹에 추가 되지 않습니다. Active Directory access 구성을 전송 하려면 다음 **의 패키지** 창에 있는 **그룹 액세스에 패키지 액세스 추가**를 선택 합니다.

     

7.  모든 응용 프로그램을 추가 하 고 Active Directory 액세스를 구성한 후 **적용**을 클릭 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)

[연결 그룹 관리](managing-connection-groups.md)

 

 





