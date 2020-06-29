---
title: 새 제어된 GPO 만들기
description: 새 제어된 GPO 만들기
author: dansimp
ms.assetid: 5ce760f6-9f05-42b4-b787-7835ab8e324e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67c6af686b9ba7254cdaf93bd2d294b2d5bbb681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821098"
---
# 새 제어된 GPO 만들기


**변경 제어** 폴더를 통해 만든 새 Gpo (그룹 정책 개체)는 자동으로 제어 되므로 관리할 수 있습니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**AGPM을 통해 변경 제어가 관리 되는 새 GPO를 만들려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **변경 컨트롤**을 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.

3.  **새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.

    1.  새 GPO의 이름을 입력 합니다.

    2.  선택 사항: GPO에 대 한 **기록** 에 표시할 새 gpo에 대 한 설명을 입력 합니다.

    3.  새 GPO를 도메인의 프로덕션 환경에 즉시 배포 하려면 **라이브 만들기**를 클릭 합니다. 새 GPO를 즉시 배포 하지 않고 오프 라인으로 만들려면 **오프 라인으로 만들기**를 클릭 합니다.

    4.  새 GPO의 시작 점으로 사용할 GPO 서식 파일을 선택 하 고 **확인**을 클릭 합니다.

4.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. **제어** 탭의 gpo 목록에 새 GPO가 표시 됩니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히, 도메인에 대 한 **목록 콘텐츠** 및 **GPO 만들기** 권한이 있어야 합니다.

### 추가 참조

-   [GPO 만들기 또는 제어](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





