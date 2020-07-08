---
title: GPO의 배포 요청
description: GPO의 배포 요청
author: dansimp
ms.assetid: 5783cfd0-bd93-46b4-8fa0-684bd39aa8fc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e9cc0fc12962dbdd7758c429a20fdd7c55b3cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820383"
---
# GPO의 배포 요청


GPO (그룹 정책 개체)를 수정 하 고 체크 인 한 후에는 프로덕션 환경에 적용 되도록 GPO를 배포 합니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 역할이 나 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**도메인의 프로덕션 환경에 GPO 배포를 요청 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

3.  배포할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **배포**를 클릭 합니다.

4.  승인자 또는 AGPM 관리자 이거나 Gpo를 배포 하기 위한 특별 한 권한이 없는 경우 배포 요청을 제출 해야 합니다. 요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다. GPO의 **기록** 에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. GPO가 **보류** 탭의 gpo 목록에 표시 됩니다. 승인자가 요청을 승인 하면 해당 GPO가 **보류 중** 탭에서 **제어** 탭으로 이동 하 고 배포 됩니다.

### 추가 고려 사항

-   기본적으로이 절차를 수행 하려면 편집기 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.

-   승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다. GPO가 **제어** 탭으로 반환 됩니다.

### 추가 참조

-   [편집기 작업 수행](performing-editor-tasks-agpm40.md)

 

 





