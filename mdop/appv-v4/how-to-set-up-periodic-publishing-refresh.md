---
title: 정기적인 게시 새로 고침을 설정하는 방법
description: 정기적인 게시 새로 고침을 설정하는 방법
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816553"
---
# 정기적인 게시 새로 고침을 설정하는 방법


다음 절차를 사용 하 여 클라이언트에서 App-v 서버의 게시 정보를 정기적으로 새로 고치도록 구성할 수 있습니다. 클라이언트가 구성 되 면 새로 고침 작업이 자동으로 수행 됩니다. 이러한 설정은이 컴퓨터의 모든 사용자가 동일한 설정을 볼 수 있도록 클라이언트에 대 한 기본 설정을 구성 합니다.

**참고**  이 절차를 수행한 후에는 로그인 시 첫 번째 새로 고침 이후 새 설정에 따라 게시 정보가 새로 고쳐집니다. 이 첫 번째 새로 고침이 발생 하면 서버는 구성 방법에 따라 컴퓨터 설정을 다른 설정으로 재정의할 수 있습니다. **속성** 대화 상자에 있는 **새로 고침** 탭에는 로컬로 구성 된 클라이언트 컴퓨터 설정 및 게시 서버에서 사용자에 게 구성 했을 수 있는 설정이 표시 됩니다.

 

**응용 프로그램 가상화 서버의 게시 정보를 정기적으로 새로 고치려면**

1.  **범위** 창에서 **서버 게시** 를 클릭 합니다.

2.  **결과** 창에서 원하는 서버를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.

3.  **속성** 대화 상자의 **새로 고침** 탭에서 **구성 새로 고침 간격** 확인란을 선택 하 고 필드의 빈도를 나타내는 숫자를 입력 합니다. 그런 다음 드롭다운 메뉴에서 **분**, **시간**, **일** 을 선택 합니다.

    **참고**  이 설정을 통해 클라이언트는 구성 된 기간이 경과할 때마다 게시 정보를 새로 고칩니다. 새로 고침을 수행할 때 사용자가 로그인 하지 않으면 사용자가 다음에 로그인 할 때 새로 고침이 수행 됩니다. 그러면 타이머가 다음 기간 동안 다시 시작 됩니다.

     

4.  구성을 변경 하려면 **적용** 을 클릭 합니다.

5.  서버 구성을 마쳤으면 **확인** 을 클릭 하 여 대화 상자를 종료 하 고 응용 프로그램 가상화 클라이언트 관리 콘솔로 돌아갑니다.

## 관련 항목


[Application Virtualization Client Management Console에서 클라이언트를 구성하는 방법](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





