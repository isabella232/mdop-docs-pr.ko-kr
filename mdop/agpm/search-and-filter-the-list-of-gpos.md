---
title: GPO 목록 검색 및 필터링
description: GPO 목록 검색 및 필터링
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820263"
---
# GPO 목록 검색 및 필터링


AGPM (고급 그룹 정책 관리)에서 Gpo (그룹 정책 개체) 및 해당 특성의 목록을 검색 하 여 표시 되는 Gpo 목록을 필터링 할 수 있습니다. 예를 들어 특정 이름, 상태 또는 주석을 사용 하 여 Gpo를 검색할 수 있습니다. 특정 그룹 정책 관리자 또는 특정 날짜에 의해 마지막으로 변경 된 Gpo를 검색할 수도 있습니다.

## 복잡 한 검색 수행


다음과 같이 GPO 속성 1 형식을 사용 하 여 복잡 한 검색을 수행할 수 있습니다 *. 검색 문자열 1 GPO 특성 2: 검색 문자열 2 ... 모든 열 검색 문자열* 검색은 대/소문자를 구분 하지 않습니다.

-   **GPO 특성:** **컴퓨터 버전이** 나 **사용자 버전이**아닌 AGPM의 gpo 목록에 있는 모든 열 머리글 Gpo 특성에는 gpo 이름, 상태, 가장 최근에 GPO를 변경한 사용자, GPO가 가장 최근에 변경 된 날짜 및 시간, 설명, GPO 상태, GPO에 적용 된 WMI 필터 등이 포함 됩니다.

-   **검색 문자열:** 지정 된 열에서 검색할 텍스트입니다. 문자열에 공백이 포함 되어 있으면 문자열을 따옴표로 묶어야 합니다.

-   **모든 열 검색 문자열:** **컴퓨터 버전과** **사용자 버전이**아닌 AGPM의 gpo 목록에 있는 모든 열에서 검색 하는 텍스트입니다. 공백으로 구분 된 여러 문자열을 포함할 수 있습니다. 문자열에 공백이 포함 되어 있으면 문자열을 따옴표로 묶어야 합니다.

각 GPO 특성 및 검색 문자열 쌍과 논리 AND 연산을 사용 하 여 각 열 검색 문자열을 결합 합니다. 결과는 지정 된 각 특성에 지정 된 검색 문자열이 포함 되어 있고 하나 이상의 열에 모든 열 검색 문자열이 표시 되는 모든 Gpo의 목록입니다. 검색은 GPO 이름 또는 사용자 이름의 일부를 입력 하 고 해당 텍스트를 이름에 포함 하는 모든 Gpo 목록을 볼 수 있도록 문자열에 대해 부분적으로 일치 하는 항목을 반환 합니다.

다음은 검색의 예입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">검색 결과 설명</th>
<th align="left">검색 쿼리</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>모든 Gpo (이름에는 문자 <strong> 보안 및 북미)가 포함 </strong> <strong> </strong> 됩니다.</p></td>
<td align="left"><p><strong>이름: </strong><strong> 보안 </strong><strong> 이름: </strong> &quot; <strong> 북미</strong>&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>모든 체크 아웃 된 Gpo</p></td>
<td align="left"><p><strong>상태: </strong> &quot; <strong> 체크 아웃 됨</strong>&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>관리자 라는 사용자가 최근에 변경 <strong> </strong> 하 고 이전 달에 최근에 변경 된 모든 gpo</p></td>
<td align="left"><p><strong>변경한 사람: </strong><strong> 관리자 </strong><strong> 변경 날짜: </strong><strong> 마지막 월</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Word <strong> 방화벽이 </strong> 가장 최근 메모에 포함 되 고 모든 <strong> </strong> 열에 word 보안이 표시 되는 모든 gpo</p></td>
<td align="left"><p><strong>설명: </strong><strong> 방화벽 </strong><strong> 보안</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>모든 설정을 사용할 수 없는 상태인 모든 gpo </strong></p></td>
<td align="left"><p><strong>gpo 상태: </strong><strong> 모두</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>내 Wmi 필터를 </strong> 적용 하 고 <strong> 사용자 구성 설정 상태를 사용할 수 </strong> 없는 Wmi 필터가 있는 모든 gpo</p></td>
<td align="left"><p><strong>wmi 필터: </strong> &quot; <strong> 내 wmi 필터 </strong> &quot; <strong> gpo 상태: </strong><strong> 사용자</strong></p></td>
</tr>
</tbody>
</table>

 

## 날짜 지정


Windows에서 검색 하는 데 사용할 수 있는 것과 동일한 특별 용어를 사용 하 여 특정 날짜 또는 시간에 변경 된 Gpo를 검색할 수 있습니다. 특정 날짜 또는 시간을 입력 하는 경우 **날짜 변경** 열에 사용 되는 형식을 사용 해야 합니다. 다음은 **변경 날짜** 열을 검색 하는 예입니다.

-   **날짜 변경:****10/10/2009**

-   **날짜 변경:****10/10/2009 9:00:00 오전**

-   **날짜 변경:****thisweek**

**날짜 변경** 열을 검색할 때 대/소문자를 구분 하지 않는 다음과 같은 특수 용어를 사용할 수 있습니다.

-   **오늘**

-   **어제**

-   **ThisWeek**

-   **LastWeek**

-   **ThisMonth**

-   **마지막 달**

-   **TwoMonths**

-   **ThreeMonths**

-   **ThisYear**

-   **LastYear**

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다. 특히, 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.

-   GPO 특성에 대 한 자세한 내용은 [콘텐츠 탭 기능](contents-tab-features-agpm40.md)을 참조 하세요.

### 추가 참조

-   [고급 그룹 정책 관리 4.0](advanced-group-policy-management-40.md)

 

 





