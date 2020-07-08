---
title: 가상 컴퓨터 구성의 예
description: 가상 컴퓨터 구성의 예
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824588"
---
# 가상 컴퓨터 구성의 예


다음은 일반적인 가상 컴퓨터 구성의 예입니다. 하나는 영구 MED-V 작업 영역에 있고 하나는 revertible MED-V 작업 영역에 있습니다.

**참고**  이러한 예제는 모든 환경에서 사용할 수 있는 것은 아닙니다. 환경에 따라 구성을 조정 합니다.

 

**영구 MED-V 작업 영역에서 일반적인 도메인 설정을 구성 하려면**

1.  기본 이미지에 Sysprep를 구성 하 여 고유한 SID를 만듭니다. 자세한 내용은 [med-v에 대 한 가상 PC 이미지 만들기](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages)를 참조 하세요.

2.  **Vm 설정** 탭에서 **vm 설치 실행** 확인란을 선택 합니다.

3.  **VM 컴퓨터 이름 패턴** 섹션에서 컴퓨터 이미지 이름에 대 한 패턴을 구성 합니다. 자세한 내용은 [VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)참조 하세요.

4.  **스크립트 편집기**를 클릭 하 고 **VM 설정 스크립트 편집기** 대화 상자에서 다음 작업을 구성 합니다.

    1.  **컴퓨터 이름 바꾸기**

    2.  **Windows 다시 시작**

    3.  **연결 확인**

    4.  **도메인 참가**

    5.  **자동 로그온 사용 안 함**

    자세한 내용은 [스크립트 동작을 설정 하는 방법을](how-to-set-up-script-actions.md)참조 하세요.

5.  **정책** 메뉴에서 **커밋을**클릭 합니다.

**Revertible 작업 영역에서 일반적인 설정을 구성 하려면**

1.  **Vm 설정** 탭에서 **컴퓨터 이름 패턴을 기반으로 VM 이름 바꾸기** 확인란을 선택 합니다.

2.  **VM 컴퓨터 이름 패턴** 섹션에서 컴퓨터 이미지 이름에 대 한 패턴을 구성 합니다. 자세한 내용은 [VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)참조 하세요.

3.  **정책** 메뉴에서 **커밋을**클릭 합니다.

## 관련 항목


[MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[VM 컴퓨터 이름 패턴 속성을 구성하는 방법](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[스크립트 동작을 설정하는 방법](how-to-set-up-script-actions.md)

 

 





