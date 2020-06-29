---
title: 저장된 GPO 버전 제한
description: 저장된 GPO 버전 제한
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820623"
---
# 저장된 GPO 버전 제한


기본적으로 제어 되는 모든 GPO (그룹 정책 개체)의 모든 버전이 AGPM 서버의 보관 저장소에 보존 됩니다. 그러나 각 GPO에 대해 보존 되는 버전 수를 제한 하 고 해당 제한이 초과 되는 경우 이전 버전을 삭제할 수 있습니다. GPO 버전이 삭제 되 면 버전 레코드가 GPO의 기록에 남아 있지만 GPO 버전 자체는 보관 저장소에서 삭제 됩니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**저장 된 GPO 버전 수를 제한 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창에서 **AGPM 서버** 탭을 클릭 합니다.

3.  **보관 파일에서 이전 버전의 Gpo 삭제** 확인란을 선택 하 고, 현재 버전을 제외한 각 gpo에 대해 저장할 최대 gpo 버전 수를 입력 합니다. 현재 버전만 보존 하려면 0을 입력 합니다. 최대값은 999 보다 크지 않아야 합니다.

    **중요**  **기록** 창의 **고유 버전** 탭에 표시 되는 GPO 버전만이 제한에 따라 계산 됩니다.

     

4.  **적용** 단추를 클릭 합니다.

### 추가 고려 사항

-   기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다. 특히 도메인에 대 한 **목록 콘텐츠** 및 **옵션 수정** 권한이 있어야 합니다.

-   기록에 삭제 되지 않도록 표시 하 여 GPO 버전이 삭제 되는 것을 방지할 수 있습니다. 이렇게 하려면 GPO 기록의 버전을 마우스 오른쪽 단추로 클릭 하 고 **삭제 안 함**을 클릭 합니다.

### 추가 참조

-   [아카이브 관리](managing-the-archive.md)

 

 





