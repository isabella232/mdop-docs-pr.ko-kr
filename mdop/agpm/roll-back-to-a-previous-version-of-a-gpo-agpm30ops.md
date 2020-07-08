---
title: 이전 버전의 GPO로 롤백
description: 이전 버전의 GPO로 롤백
author: dansimp
ms.assetid: 2a98ad8f-32cb-41eb-ab99-0318f2a55d81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 715f70ad6e87a0b2fa463426d4f6a8955250e446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820288"
---
# 이전 버전의 GPO로 롤백


승인자는 이전 버전의 GPO를 기록에 다시 배포 하 여 GPO (그룹 정책 개체)에 대 한 변경 내용을 롤백할 수 있습니다. 이전 버전의 GPO를 배포 하면 현재 프로덕션 중인 GPO 버전이 덮어써집니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**이전 버전의 GPO를 프로덕션 환경에 배포 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

3.  배포할 GPO를 두 번 클릭 하 여 **기록을**표시 합니다.

4.  배포할 버전을 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 한 다음 **예**를 클릭 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. **기록** 창에서 **닫기를**클릭 합니다.

**참고**  다시 배포 된 버전이 의도 한 버전과 일치 하는지 확인 하려면 두 버전의 차이점 보고서를 검토 합니다. GPO의 **기록** 창에서 두 버전을 강조 표시 한 다음 마우스 오른쪽 단추를 클릭 하 고 **차이점** 및 **HTML 보고서** 또는 **XML 보고서**중 하나를 선택 합니다.

 

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **gpo** 사용 권한이 있어야 합니다.

### 추가 참조

-   [승인자 작업 수행](performing-approver-tasks-agpm30ops.md)

 

 





