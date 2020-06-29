---
title: VM 컴퓨터 이름 패턴 속성을 구성하는 방법
description: VM 컴퓨터 이름 패턴 속성을 구성하는 방법
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827078"
---
# VM 컴퓨터 이름 패턴 속성을 구성하는 방법


가상 컴퓨터 컴퓨터 이름 패턴을 revertible 및 영구 MED-V 작업 영역에 모두 할당할 수 있습니다.

-   Revertible — 관리자는 각 Revertible MED-V 작업 영역 인스턴스에 고유한 이름을 할당 하 여 동일한 MED-V 작업 영역을 사용 하는 여러 컴퓨터를 구분할 수 있습니다.

-   Persistent-영구 MED-V 작업 영역에서 관리자는 설치 스크립트 중에 컴퓨터 이름을 변경 하도록 설정할 수 있습니다.

## Revertible MED-V 작업 영역에 가상 컴퓨터 컴퓨터 이름 패턴을 할당 하는 방법


**Revertible MED-V 작업 영역에 가상 컴퓨터 컴퓨터 이름 패턴을 할당 하려면**

1.  Revertible MED-V 작업 영역을 클릭 하 여 구성 합니다.

2.  **REVERTIBLE Vm 설정** 섹션에서 **컴퓨터 이름 패턴을 기반으로 VM 이름 바꾸기** 확인란을 선택 합니다.

3.  **VM 컴퓨터 이름 패턴** 섹션에 다음 옵션을 사용 하 여 가상 컴퓨터 이미지를 명명 하는 데 사용할 패턴을 입력 합니다.

    -   **상수**-med-v 작업 영역을 사용 하는 모든 컴퓨터에서 상수가 되는 자유 텍스트를 입력 합니다.

    -   **변수 (variable**)-변수 **삽입**을 클릭 하 여 변수를 입력 하 고 다음 중 하나를 선택 합니다.

        -   **사용자 이름**

        -   **도메인 이름**

        -   **호스트 이름**

        -   **작업 영역 이름**

        -   **가상 머신 이름**

        선택한 변수는 MED-V 작업 영역을 사용 하는 컴퓨터에 한정 됩니다. 예를 들어 **도메인 이름을** 선택 하면 각 컴퓨터의 고유 이름에 컴퓨터의 도메인 이름이 포함 됩니다.

    -   **임의 문자**-패턴에 포함할 각 문자에 대해 "\ #"을 입력 합니다. MED-V 작업 영역을 사용 하는 각 컴퓨터에는 지정 된 길이의 접미사가 있으며,이는 임의로 생성 됩니다.

    **참고**  
    컴퓨터 이름의 한계는 15 자입니다. 패턴이 한도를 초과 하는 경우에는 잘립니다.



4.  **정책** 메뉴에서 **커밋을**선택 합니다.

    **참고**  
    Revertible VM 컴퓨터 이름 패턴은 컴퓨터 이름 패턴 ( **REVERTIBLE Vm 설정** 섹션)을 **기반으로 VM 이름을 바꿀** 때만 할당할 수 있습니다.



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## 영구 MED-V 작업 영역에 가상 컴퓨터 컴퓨터 이름 패턴을 할당 하는 방법


**가상 컴퓨터 컴퓨터 이름 패턴을 영구 MED-V 작업 영역에 할당 하려면**

1.  영구적 MED-V 작업 영역을 클릭 하 여 구성 합니다.

2.  **영구 VM 설정** 섹션에서 **스크립트 편집기**를 클릭 합니다.

3.  **스크립트 작업** 대화 상자에서 **추가**를 클릭 하 고 하위 메뉴에서 **컴퓨터 이름 바꾸기를**클릭 합니다.

4.  **확인** 을 클릭 하 여 **스크립트 작업** 대화 상자를 닫습니다.

5.  **Vm 설정** 탭의 **Vm 컴퓨터 이름 패턴** 섹션에 다음을 사용 하 여 컴퓨터의 이름을 바꾸는 데 사용할 패턴을 입력 합니다.

    -   **상수**-컴퓨터 이름에 포함 될 무료 텍스트를 입력 합니다.

    -   **변수 (variable**)-변수 **삽입**을 클릭 하 여 변수를 입력 하 고 다음 중 하나를 선택 합니다.

        -   **사용자 이름**

        -   **도메인 이름**

        -   **호스트 이름**

        -   **작업 영역 이름**

        -   **가상 머신 이름**

        선택한 변수는 이름을 바꾸는 컴퓨터에만 적용 됩니다. 예를 들어 **도메인 이름을** 선택 하면 컴퓨터 이름에 컴퓨터의 도메인 이름이 포함 됩니다.

    -   **임의 문자**-패턴에 포함할 각 문자에 대해 "\ #"을 입력 합니다. 컴퓨터에는 지정 된 길이의 접미사가 있으며,이는 임의로 생성 됩니다.

    **참고**  
    컴퓨터 이름의 한계는 15 자입니다. 패턴이 한도를 초과 하는 경우에는 잘립니다.



6.  **정책** 메뉴에서 **커밋을**선택 합니다.

    **참고**  
    **스크립트 작업** 대화 상자에서 작업으로 설정 된 경우에만 컴퓨터 이름이 변경 됩니다. 자세한 내용은 [스크립트 동작을 설정 하는 방법을](how-to-set-up-script-actions.md)참조 하세요.



## 관련 항목


[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

[MED-V 작업 영역 만들기](creating-a-med-v-workspacemedv-10-sp1.md)

[스크립트 동작을 설정하는 방법](how-to-set-up-script-actions.md)

[가상 컴퓨터 구성의 예](examples-of-virtual-machine-configurationsv2.md)









