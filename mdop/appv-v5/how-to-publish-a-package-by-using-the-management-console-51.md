---
title: 관리 콘솔을 사용하여 패키지를 게시하는 방법
description: 관리 콘솔을 사용하여 패키지를 게시하는 방법
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813769"
---
# 관리 콘솔을 사용하여 패키지를 게시하는 방법


App-v 5.1 패키지를 게시 하려면 다음 절차를 사용 합니다. 패키지를 게시 하면 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 해당 패키지의 응용 프로그램에 액세스 하 고 실행할 수 있습니다.

**참고**  앱-V 5.0 SP3에서 시작 하는 경우에는 관리자만 패키지를 게시 하거나 게시 취소할 수 있는 기능이 지원 됩니다.

 

**App-v 5.1 패키지 게시**

1.  앱-V 5.1 관리 콘솔에서 게시할 패키지의 이름을 클릭 하거나 마우스 오른쪽 단추로 클릭 합니다. **게시**를 선택합니다.

2.  **상태** 열을 검토 하 여 패키지가 게시 되었고 현재 사용할 수 있는지 확인 합니다. 패키지를 사용할 수 있는 경우 **게시** 상태가 표시 됩니다.

    패키지가 성공적으로 게시 되지 않으면 **게시** 되지 않은 상태와 함께 패키지를 사용할 수 없는 이유를 설명 하는 오류 텍스트가 표시 됩니다.

**관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면**

1.  다음 그룹 정책 개체 노드로 이동 합니다.

    **컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시**.

2.  **관리자 권한으로 게시** 그룹 정책 설정을 사용 하도록 설정 합니다.

    또는 PowerShell을 사용 하 여이 항목을 설정 하려면 [powershell을 사용 하 여 독립 실행형 컴퓨터에서 실행 되는 app-v 5.1 패키지를 관리 하는 방법을](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)참조 하세요.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

[관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





