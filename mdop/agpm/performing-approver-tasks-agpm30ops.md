---
title: 승인자 작업 수행
description: 승인자 작업 수행
author: dansimp
ms.assetid: 9f711824-191b-4b4b-a1c6-a3b2116006a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e4a848608a3be1dbb0632f0145b4fc1d1bc631
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820473"
---
# 승인자 작업 수행


승인자는 AGPM 관리자 (모든 권한)가 승인 하는 사람이 며, Gpo (그룹 정책 개체)를 만들고, 배포 하 고, 삭제 하 고, 요청 (일반적으로 편집자의)을 승인 또는 거부 하 여 Gpo를 만들거나 배포 하거나 삭제할 수 있습니다.

**중요**  Gpo의 중앙 보관 파일에 연결 되어 있는지 확인 합니다. 자세한 내용은 [AGPM 서버 연결 구성을](configure-an-agpm-server-connection-reviewer-agpm30ops.md)참조 하세요.

 

-   [보류 중인 작업 승인 또는 거부](approve-or-reject-a-pending-action-agpm30ops.md)

-   [GPO 만들기, 제어 또는 가져오기](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

-   [GPO 체크 인](check-in-a-gpo-agpm30ops.md)

-   [GPO 배포](deploy-a-gpo-agpm30ops.md)

-   [이전 버전의 GPO로 롤백](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)

-   [GPO 삭제, 복원 또는 destroy](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

**참고**  GPO를 승인 하기 전에 승인자는 포함 된 정책 설정을 검토 해야 합니다. 승인자 역할에는 검토자 역할에 대 한 사용 권한이 포함 되므로 승인자는 정책 설정을 검토 하 고 Gpo를 비교할 수 있습니다. 자세한 내용은 [검토자 작업 수행](performing-reviewer-tasks-agpm30ops.md) 을 참조 하세요.

 

### 추가 고려 사항

기본적으로 승인자 역할에는 다음 사용 권한이 제공 됩니다.

-   콘텐츠 나열

-   설정 읽기

-   GPO 만들기

-   GPO 배포

-   GPO 삭제

또한 승인자는 자신이 만들었거나 제어 하는 Gpo에 대해 모든 권한을 갖습니다.

 

 





