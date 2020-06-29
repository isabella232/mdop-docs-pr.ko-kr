---
title: GPO의 현재 버전의 레이블 지정
description: GPO의 현재 버전의 레이블 지정
author: dansimp
ms.assetid: cadc8769-21da-44b0-8122-6cafdb448913
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b15a4d3ee006fb37db4ce7362a2f5c92d7c233e5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820663"
---
# GPO의 현재 버전의 레이블 지정


현재 버전의 GPO (그룹 정책 개체)에 레이블을 지정 하 여 해당 기록에서 쉽게 식별할 수 있습니다. 레이블을 사용 하 여 문제가 발생 하는 경우 롤백할 수 있는 알려진 양호한 버전을 식별할 수 있습니다. 또한 한 번에 동일한 레이블을 사용 하 여 여러 Gpo에 레이블을 지정 하 여 나중에 롤백이 필요한 경우 동일한 지점으로 롤백해야 하는 관련 Gpo를 표시할 수 있습니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**기록에서 현재 버전의 Gpo에 레이블을 지정 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

3.  현재 버전에 레이블을 지정 하려는 GPO를 클릭 합니다. 여러 Gpo를 선택 하려면 SHIFT 키를 누르고 인접 한 Gpo 그룹의 마지막 GPO를 클릭 하거나 CTRL 키를 누른 상태로 개별 Gpo를 클릭 합니다. 선택한 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **레이블을**클릭 합니다.

4.  선택한 각 GPO의 기록에 표시할 레이블과 메모를 입력 한 다음 **확인**을 클릭 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.

### 추가 고려 사항

-   기본적으로이 절차를 수행 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 또는 **gpo 배포** 권한이 있어야 합니다.

### 추가 참조

-   [GPO 편집](editing-a-gpo-agpm40.md)

 

 





