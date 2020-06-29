---
title: GPO, GPO 버전 또는 템플릿 간의 차이점 식별
description: GPO, GPO 버전 또는 템플릿 간의 차이점 식별
author: dansimp
ms.assetid: e391fa91-3956-4150-9d43-900cfc88d543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88c37a3723c31fb110e731084237a8d89350a4ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820773"
---
# GPO, GPO 버전 또는 템플릿 간의 차이점 식별


Gpo (그룹 정책 개체), 템플릿 또는 GPO의 다른 버전 간의 차이점을 분석 하는 HTML 기반 차이점 보고서를 생성 하거나 XML 기반 차이를 생성할 수 있습니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에 대 한 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

## Gpo, GPO 버전 또는 템플릿의 차이점 확인


-   [두 개의 Gpo 또는 템플릿 간에](#bkmk-two-gpos)

-   [GPO와 서식 파일 간](#bkmk-gpo-and-template)

-   [한 GPO의 두 버전 사이](#bkmk-two-versions)

-   [GPO 버전과 서식 파일 간에](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**두 Gpo 또는 템플릿 간의 차이점을 확인 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.

3.  두 개의 Gpo 또는 템플릿을 선택 합니다.

4.  Gpo 또는 서식 파일 중 하나를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo 또는 템플릿의 설정을 요약 한 차이점 보고서를 표시 합니다.

### <a href="" id="bkmk-gpo-and-template"></a>

**GPO와 서식 파일 간의 차이점을 확인 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.

3.  GPO를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **서식 파일**을 클릭 합니다.

4.  서식 파일과 보고서 유형을 선택한 다음 **확인** 을 클릭 하 여 GPO 및 템플릿의 설정을 요약 하는 차이점 보고서를 표시 합니다.

### <a href="" id="bkmk-two-versions"></a>

**한 GPO의 두 버전 간의 차이점을 확인 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.

3.  GPO를 두 번 클릭 하 여 기록을 표시 한 다음 비교할 버전을 강조 표시 합니다.

4.  버전 중 하나를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo의 설정을 요약 하는 차이점 보고서를 표시 합니다.

### <a href="" id="bkmk-gpo-version-and-template"></a>

**GPO 버전과 서식 파일 간의 차이점을 확인 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.

3.  해당 GPO를 두 번 클릭 하 여 기록을 표시 합니다.

4.  원하는 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **서식 파일**을 클릭 합니다.

5.  서식 파일 및 보고서 유형을 선택 하 고 **확인** 을 클릭 하 여 GPO 버전 및 템플릿의 설정을 요약 하는 차이점 보고서를 표시 합니다.

## 차이점 보고서에 대 한 주요 정보


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">기호</th>
<th align="left">의미</th>
<th align="left">색상</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>없음</p></td>
<td align="left"><p>두 Gpo에 동일한 설정이 있는 항목이 있습니다.</p></td>
<td align="left"><p>수준에 따라 다름</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>항목이 두 Gpo에 모두 있지만 변경 된 설정이 있습니다.</p></td>
<td align="left"><p>화면이</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>항목이 첫 번째 GPO에만 있음</p></td>
<td align="left"><p>빨간색</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>두 번째 GPO에만 항목이 있음</p></td>
<td align="left"><p>녹색</p></td>
</tr>
</tbody>
</table>

 

-   설정이 변경 된 항목의 경우 항목을 확장할 때 변경 된 설정이 식별 됩니다. 각 GPO의 특성 값은 Gpo가 보고서에 표시 되는 순서 대로 표시 됩니다.

-   일부 설정이 변경 되 면 항목이 두 개의 다른 항목 (첫 번째 GPO에만 표시 되며 변경 된 항목이 하나가 아닌 두 개에만 표시 됨)으로 보고 될 수 있습니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 읽기** 권한이 있어야 합니다. 또한 Gpo 목록을 표시 하려면 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.

### 추가 참조

-   [검토자 작업 수행](performing-reviewer-tasks-agpm30ops.md)

 

 





