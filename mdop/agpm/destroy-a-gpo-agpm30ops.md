---
title: GPO destroy
description: GPO destroy
author: dansimp
ms.assetid: bfabd71a-47f3-462e-b86f-5f15762b9e28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 842a546c4db9cc6048908521baa05c6cc1a1a8a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818683"
---
# GPO destroy


승인자는 GPO (그룹 정책 개체)를 파기 하 고 휴지통에서 제거 하 고 영구적으로 삭제 하 여 더 이상 복원할 수 없습니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**더 이상 복원할 수 없도록 GPO를 영구적으로 삭제 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.

3.  삭제할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.

4.  **예** 를 클릭 하 여 선택한 GPO 및 보관 저장소의 모든 백업을 영구적으로 삭제할 것인지 확인 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. **휴지통** 탭에서 GPO가 제거 되 고 영구적으로 삭제 됩니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠와** **gpo** 사용 권한이 있어야 합니다.

### 추가 참조

-   [GPO 삭제, 복원 또는 destroy](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





