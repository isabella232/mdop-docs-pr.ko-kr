---
title: GPO 체크 인
description: GPO 체크 인
author: dansimp
ms.assetid: e428cfff-651f-4903-bf01-d742714d2fa9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6adbcfa1c2b0d79389bc16dd1dde5afc0a4ec4a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819148"
---
# GPO 체크 인


일반적으로 편집자는 수정이 완료 되 면 편집한 Gpo (그룹 정책 개체)를 체크 인해야 합니다. 자세한 내용은 [오프 라인으로 GPO 편집](edit-a-gpo-offline.md)을 참조 하세요. 그러나 편집기를 사용할 수 없는 경우에는 승인자가 GPO도 확인할 수 있습니다.

이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**편집기에 의해 체크 아웃 된 GPO를 체크 인하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

    -   편집기에서 변경한 내용을 취소 하려면 해당 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크 아웃 취소**를 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.

    -   편집기에서 변경한 내용을 유지 하려면 해당 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크**인을 클릭 합니다.

3.  GPO의 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.

4.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. **제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.

### 추가 고려 사항

-   기본적으로이 절차를 수행 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 또는 **gpo 배포** 권한이 있어야 합니다. 승인자 또는 AGPM 관리자 (또는 **GPO 배포** 권한이 있는 다른 그룹 정책 관리자)가 아닌 경우 gpo를 체크 아웃 한 편집기 여야 합니다.

### 추가 참조

-   [승인자 작업 수행](performing-approver-tasks.md)

-   [오프라인에서 GPO 편집](edit-a-gpo-offline.md)

 

 





