---
title: GPO 링크 검토
description: GPO 링크 검토
author: dansimp
ms.assetid: 5ae95afc-2b89-45cf-916c-efe2d43b2211
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6532a669c6841c2342514c0911f74bc0b1fbc86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818358"
---
# GPO 링크 검토


선택한 GPO (그룹 정책 개체) 또는 gpo가 조직 구성 단위에 연결 된 위치를 표시 하는 다이어그램을 표시할 수 있습니다. Gpo 연결 다이어그램은 GPO가 제어, 가져오기 또는 체크 인 될 때마다 업데이트 됩니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에 대 한 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

## GPO 링크 검토


-   [하나 이상의 Gpo](#bkmk-gpos)

-   [하나 이상의 GPO 버전](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**하나 이상의 Gpo에 대 한 GPO 링크를 표시 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 **제어**됨, **보류 중**또는 **휴지통** 탭을 클릭 하 여 gpo를 표시 합니다.

3.  링크를 표시할 하나 이상의 Gpo를 선택 하 고 선택한 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **설정을**클릭 하 고 **gpo 연결** 을 클릭 하 여 선택한 gpo에 대 한 링크가 있는 도메인 및 조직 구성 단위 다이어그램을 표시 합니다.

### <a href="" id="bkmk-gpo-versions"></a>

**하나 이상의 GPO 버전에 대 한 GPO 링크를 표시 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 **제어** 또는 **휴지통** 탭을 클릭 하 여 gpo를 표시 합니다.

3.  해당 GPO를 두 번 클릭 하 여 기록을 표시 합니다.

4.  설정을 검토할 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo 설정에 대 한 요약 정보를 표시 합니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 읽기** 권한이 있어야 합니다. 또한 Gpo 목록을 표시 하려면 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.

### 추가 참조

-   [검토자 작업 수행](performing-reviewer-tasks-agpm30ops.md)

 

 





