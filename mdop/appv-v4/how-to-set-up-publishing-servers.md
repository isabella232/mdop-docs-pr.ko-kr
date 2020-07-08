---
title: 게시 서버를 설정하는 방법
description: 게시 서버를 설정하는 방법
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816528"
---
# 게시 서버를 설정하는 방법


다음 절차를 사용 하 여 클라이언트 관리 콘솔에서 직접 Application Virtualization Server를 추가 하 고 구성할 수 있습니다.

**응용 프로그램 게시 서버를 추가 하려면**

1.  **결과** 창에서 팝업 메뉴를 마우스 오른쪽 단추로 클릭 하 고 새 **서버** 를 선택 하 여 새 Application Virtualization server 마법사를 시작 하거나, **게시 서버** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **새 서버** 를 선택 합니다.

2.  마법사의 페이지 1에서 **표시 이름** 필드에 서버 이름을 입력 하 고 **유형** 드롭다운 목록에서 서버 유형을 선택 합니다. 서버 유형의 드롭다운 목록에서 **응용 프로그램 가상화 서버**, **향상 된 보안 응용 프로그램 가상화 서버**, **표준 HTTP 서버**또는 **향상 된 보안 HTTP 서버** 를 선택할 수 있습니다.

3.  **다음**을 클릭합니다.

4.  마법사의 2 페이지에서 **호스트 이름** 및 **포트** 필드에 적절 한 정보를 입력 합니다. **Path** 필드는 Application Virtualization 서버에 대해 편집할 수 없습니다. 표준 HTTP 서버 또는 향상 된 보안 HTTP 서버에 대 한 경로를 입력 해야 합니다.

5.  **마침을** 클릭 하 여 서버를 추가 합니다.

**응용 프로그램 게시 서버를 설정 하려면**

1.  **결과** 창에서 원하는 서버를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.

2.  서버 이름을 변경할 수 있는 **일반** 탭을 클릭 하 고 서버 유형의 드롭다운 목록에서 유형을 선택한 다음 호스트 이름 및 포트를 지정 합니다. 서버 종류가 표준 HTTP 서버 또는 향상 된 보안 HTTP 서버인 경우 **경로** 필드도 편집할 수 있습니다.

3.  **새로 고침** 탭을 클릭 하 고 **사용자 로그인 시 게시 새로 고침** 확인란이 기본적으로 선택 되어 있습니다. 새로 고침 빈도를 변경 하려면 **게시 새로 고침 간격** 확인란을 선택 하 고 필드의 빈도를 나타내는 숫자를 입력 합니다. 그런 다음 드롭다운 메뉴에서 **분**, **시간**, **일** 을 선택 합니다. (입력할 수 있는 최소 시간은 30 분입니다.)

4.  구성을 변경 하려면 **적용** 을 클릭 합니다.

5.  게시가 완료 되 면 **확인** 을 클릭 하 여 대화 상자를 종료 하 고 클라이언트 관리 콘솔로 돌아갑니다.

## 관련 항목


[연결이 끊긴 작업 모드 설정을 사용 중지하거나 수정하는 방법](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





