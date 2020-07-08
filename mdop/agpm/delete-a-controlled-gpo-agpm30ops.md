---
title: 제어된 GPO 삭제
description: 제어된 GPO 삭제
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818713"
---
# 제어된 GPO 삭제


승인자는 제어 된 GPO (그룹 정책 개체)를 휴지통으로 이동 하 여 삭제할 수 있습니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**제어 된 GPO를 삭제 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

3.  삭제 하려는 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.

    -   Gpo의 배포 버전을 실제 환경에 그대로 유지 하면서 보관 파일에서 GPO를 삭제 하려면 **보관 파일 에서만 Gpo 삭제**를 클릭 합니다.

    -   보관 및 프로덕션 환경에서 모두 GPO를 삭제 하려면 **보관 및 프로덕션에서 Gpo 삭제**를 클릭 합니다.

4.  GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. GPO가 **제어** 탭에서 제거 되 고 **휴지통** 탭에 표시 되며 복원 하거나 삭제할 수 있습니다. 보관 함 에서만 GPO를 삭제 하면 **제어** 되지 않은 탭에도 표시 됩니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠와** **gpo** 사용 권한이 있어야 합니다.

-   관리 되지 않는 GPO를 먼저 제어 하지 않고 프로덕션 환경에서 삭제 하려면 **그룹 정책 관리 콘솔**에서 **포리스트**, **도메인**을 차례로 클릭 하 고 ** &lt; MyDomain &gt; **을 클릭 한 다음 **그룹 정책 개체**를 클릭 합니다. 미제어 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.

### 추가 참조

-   [GPO 삭제, 복원 또는 destroy](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





