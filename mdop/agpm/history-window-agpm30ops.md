---
title: 기록 창
description: 기록 창
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820798"
---
# 기록 창


Gpo를 두 번 클릭 하거나 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **기록**클릭 하 여 Gpo (그룹 정책 개체)의 기록을 표시할 수 있습니다. 또한 GPMC ( **그룹 정책 관리 콘솔** )에 각 GPO에 대 한 탭으로 표시 됩니다.

기록은 선택한 GPO의 수명에서 이벤트 기록을 제공 합니다. **기록** 창에서 gpo 버전 내의 설정에 대 한 보고서를 가져오거나, gpo의 여러 버전을 비교 하거나, 이전 버전의 gpo로 롤백할 수 있습니다.

## 기록 창에서 이벤트 필터링


**기록** 창 내의 탭은 GPO 기록의 상태를 필터링 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">탭</th>
<th align="left">필터링</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>모든 상태</strong></p></td>
<td align="left"><p>GPO 기록의 모든 상태를 표시 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>고유 버전</strong></p></td>
<td align="left"><p>아카이브에 체크 된 고유한 GPO 버전만 표시 합니다. 프로덕션 환경에 배포 된 버전, 고유 버전에 대 한 바로 가기 및 정보 상태는이 목록에서 생략 됩니다.</p></td>
</tr>
</tbody>
</table>



## 이벤트 정보


GPO 기록의 각 상태에 대 한 정보가 제공 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">GPO 특성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>날짜 변경</strong></p></td>
<td align="left"><p>상태 열의 작업을 수행한 시간의 타임 스탬프 <strong> 입니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>시</strong></p></td>
<td align="left"><p>GPO 기록의 상태입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>변경한 사람</strong></p></td>
<td align="left"><p>GPO를 체크 인 하거나 배포한 사람입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설명</strong></p></td>
<td align="left"><p>이 버전이 수정 된 시점에 GPO를 체크 인 하거나 배포 하는 사람이 입력 한 메모입니다. 이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>삭제할</strong></p></td>
<td align="left"><p>보관 저장소에 보존 된 각 GPO의 고유 버전 수가 제한 되어 있는 경우이 버전의 GPO를 삭제할 수 있는지 여부</p>
<div class="alert">
<strong>참고</strong><br/><p>GPO를 마우스 오른쪽 단추로 클릭 한 다음 <strong> 삭제 허용 또는 삭제 허용 안 함을 클릭 하 여 해당 버전을 삭제할 수 있습니다 </strong> <strong> </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>컴퓨터 버전</strong></p></td>
<td align="left"><p>GPO의 컴퓨터 구성 부분에 대 한 버전을 자동으로 생성 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>사용자 버전</strong></p></td>
<td align="left"><p>GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO 상태</strong></p></td>
<td align="left"><p>컴퓨터 구성과 사용자 구성을 서로 별도로 관리할 수 있습니다. 이 상태는 사용할 수 있는 GPO의 일부를 보여 줍니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>WMI 필터</strong></p></td>
<td align="left"><p>이 GPO에 적용 된 WMI 필터를 표시 합니다. WMI 필터는 <strong> </strong> GPMC의 콘솔 트리에서 도메인에 대 한 wmi 필터 폴더에 관리 됩니다.</p></td>
</tr>
</tbody>
</table>



## 보고


**설정** 및 **차이점** 단추에는 선택한 gpo 버전에 대 한 gpo 설정에 대 한 보고서가 표시 됩니다. GPO 버전을 마우스 오른쪽 단추로 클릭 하면 XML 기반 보고서도 표시할 수 있는 옵션이 제공 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단추</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>설정</strong></p></td>
<td align="left"><p>선택한 GPO 버전 내의 설정을 표시 하는 HTML 기반 보고서를 생성 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>차이점</strong></p></td>
<td align="left"><p>선택한 여러 GPO 버전 내의 설정을 비교 하 여 HTML 기반 보고서를 생성 합니다.</p></td>
</tr>
</tbody>
</table>



### 차이점 보고서에 대 한 주요 정보

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

-   일부 설정이 변경 되 면 항목이 두 개의 다른 항목 (첫 번째 GPO에만 표시 되며 변경 된 하나의 항목이 아닌 한 항목으로 보고 됨)이 발생할 수 있습니다.

### 추가 참조

-   [내용 탭](contents-tab-agpm30ops.md)









