---
title: AGPM 서버 연결 구성
description: AGPM 서버 연결 구성
author: dansimp
ms.assetid: 74e8f348-a8ed-4d69-a8e0-9c974aaeca2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83a2437ee8c2fe562141ff167cb85c6a06b7cefe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818918"
---
# AGPM 서버 연결 구성


올바른 중앙 보관 저장소에 연결 되어 있는지 확인 하려면 AGPM 서버 연결의 구성을 검토 합니다. AGPM 관리자 (모든 권한)가 사용자를 위해 AGPM 서버 연결을 구성 하지 않은 경우 수동으로 구성 해야 합니다.

**AGPM 서버를 선택 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창에서 **AGPM 서버** 탭을 클릭 합니다.

    -   **Agpm 서버** 탭의 옵션을 사용할 수 없는 경우 agpm 관리자가 중앙에서 구성 했습니다.

    -   **Agpm 서버** 탭의 옵션을 사용할 수 있는 경우 agpm 서버의 정규화 된 컴퓨터 이름 (예: server.contoso.com)과 agpm 서비스가 수신 대기 하는 포트 (기본적으로 포트 4600)를 입력 합니다. **적용**을 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.

### 추가 고려 사항

-   선택 된 AGPM 서버는 **콘텐츠** 탭에 표시 되는 Gpo와 **도메인 위임** 탭 설정이 적용 되는 위치를 결정 합니다. 관리 템플릿을 통해 중앙에서 관리 되지 않는 경우 각 그룹 정책 관리자는 해당 도메인의 AGPM 서버를 가리키도록이 설정을 구성 해야 합니다.

### 추가 참조

-   [편집기 작업 수행](performing-editor-tasks.md)

-   [승인자 작업 수행](performing-approver-tasks.md)

-   [검토자 작업 수행](performing-reviewer-tasks.md)

 

 





