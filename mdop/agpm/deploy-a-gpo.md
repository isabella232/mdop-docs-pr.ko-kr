---
title: GPO 배포
description: GPO 배포
author: dansimp
ms.assetid: a0a3f292-e3ab-46ae-a0fd-d7b2b4ad8883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a98bdd758937d86cf8c30c5abf0b49302d377360
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818698"
---
# GPO 배포


AGPM (고급 그룹 정책 관리)을 사용 하면 승인자가 새 또는 편집한 GPO (그룹 정책 개체)를 프로덕션 환경에 배포할 수 있습니다. 이전 버전의 GPO 다시 배포에 대 한 자세한 내용은 [이전 버전의 gpo로 롤백을](roll-back-to-a-previous-version-of-a-gpo.md)참조 하세요.

이 절차를 완료 하려면 고급 그룹 정책 관리에서 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**프로덕션 환경에 GPO를 배포 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

3.  배포할 GPO를 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 합니다.

4.  GPO에 대 한 링크를 검토 하려면 **고급**을 클릭 합니다. 트리 노드에 마우스 포인터를 잠시 두면 세부 정보를 표시할 수 있습니다.

    -   기본적으로 GPO에 대 한 모든 연결이 복원 됩니다.

    -   링크가 복원 되지 않도록 하려면 해당 링크에 대 한 확인란의 선택을 취소 합니다.

    -   모든 링크가 복원 되는 것을 방지 하려면 **GPO 배포** 대화 상자에서 **링크 복원** 확인란의 선택을 취소 합니다.

5.  **예**를 클릭합니다. **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.

**참고**  최신 버전의 GPO가 배포 되었는지 확인 하려면 **제어** 탭에서 GPO를 두 번 클릭 하 여 **기록을**표시 합니다. GPO의 **기록** 에서 **상태** 열은 gpo가 배포 되었는지 여부를 나타냅니다.

 

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **gpo** 사용 권한이 있어야 합니다.

### 추가 참조

-   [승인자 작업 수행](performing-approver-tasks.md)

 

 





