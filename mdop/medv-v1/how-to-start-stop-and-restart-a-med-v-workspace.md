---
title: MED-V 작업 영역을 시작, 중지 및 다시 시작하는 방법
description: MED-V 작업 영역을 시작, 중지 및 다시 시작하는 방법
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825723"
---
# MED-V 작업 영역을 시작, 중지 및 다시 시작하는 방법


**MED-V 작업 영역을 시작 하려면**

1.  알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.

2.  하위 메뉴에서 **시작 작업 영역**을 클릭 합니다.

    -   컴퓨터에서 실행 중인 MED-V 작업 영역이 여러 개인 경우 **작업 영역 선택** 창이 나타납니다.

        1.  MED-V 작업 영역을 선택 합니다.

        2.  다음에 **묻지 않고 선택한 작업 영역 시작** 확인란을 선택 하 여 다음에 클라이언트가 시작 될 때이 창을 건너뛰고 선택한 med-v 작업 영역을 자동으로 엽니다.

        3.  **확인**을 클릭합니다.

    **작업 영역 인증 시작** 창이 나타납니다.

    -   컴퓨터에 MED-V 작업 영역이 여러 개 있고 지정 된 MED-V 작업 영역을 사용 하기로 결정 한 경우 다음 그림에 표시 된 창이 나타납니다.

        ![](images/medv-logon.gif)

    -   컴퓨터에 MED-V 작업 영역이 하나만 있는 경우 "마지막으로 사용한 작업 영역 시작" 옵션을 사용할 수 없습니다.

3.  도메인 사용자 자격 증명을 입력 합니다.

    **참고**  Med-v 작업 영역이 처음 시작 될 때 사용자 이름은 &lt; 도메인 이름 &gt; \\ &lt; 사용자 이름 형식 이어야 &gt; 합니다.

     

4.  **내 비밀 번호 저장** 을 선택 하 여 세션 간에 비밀 번호를 저장 합니다.

    **참고**  암호 저장 기능을 사용 하도록 설정 하려면 ClientSettings.xml 파일에서 EnableSavePassword 특성을 True로 설정 해야 합니다. 이 파일은 *Servers\\configuration Server\\* 폴더에서 찾을 수 있습니다.

     

5.  다른 MED-V 작업 영역을 선택 하려면 **마지막으로 사용한 작업 영역 시작** 확인란의 선택을 취소 합니다.

6.  **확인**을 클릭합니다.

    MED-V 작업 영역 구성에 따라 몇 가지 상태 화면이 표시 됩니다.

    **작업 영역 시작** 화면이 나타납니다.

**MED-V 작업 영역을 다시 시작 하려면**

1.  클라이언트가 실행 되는 경우 알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.

2.  하위 메뉴에서 **작업 영역 다시 시작**을 클릭 합니다.

    MED-V 작업 영역이 다시 시작 됩니다.

    -   영구 MED-V 작업 영역에서 가상 컴퓨터를 종료 한 다음 다시 시작 합니다.

    -   Revertible MED-V 작업 영역에서 가상 컴퓨터는 실제로 종료 되지 않습니다. 그 대신 원래 상태로 돌아갑니다.

**MED-V 작업 영역을 중지 하려면**

1.  알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.

2.  하위 메뉴에서 **작업 영역 중지**를 클릭 합니다.

    MED-V 작업 영역이 중지 됩니다.

## 관련 항목


[MED-V 클라이언트를 시작 및 종료하는 방법](how-to-start-and-exit-the-med-v-client.md)

 

 





