---
title: 기록 창
description: 기록 창
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820788"
---
# 기록 창


Gpo를 두 번 클릭 하거나 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **기록**클릭 하 여 Gpo (그룹 정책 개체)의 기록을 표시할 수 있습니다. 또한 GPMC ( **그룹 정책 관리 콘솔** )에 각 GPO에 대 한 탭으로 표시 됩니다.

기록에는 보관에 저장 된 선택한 GPO의 모든 버전이 나열 됩니다. **기록** 창에서 gpo 내의 설정에 대 한 보고서를 가져오거나, gpo의 여러 버전을 비교 하거나, 이전 버전의 gpo로 롤백할 수 있습니다.

## 기록 창에서 이벤트 필터링


**기록** 창 내의 탭에서 표시 되는 이벤트를 필터링 합니다.

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
<td align="left"><p><strong>모두 표시</strong></p></td>
<td align="left"><p>모든 버전의 GPO를 표시 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>체크 인 됨</strong></p></td>
<td align="left"><p>해당 GPO의 체크 인 버전만 표시 합니다. 배포 된 버전은이 목록에서 생략 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>레이블만</strong></p></td>
<td align="left"><p>연결 된 레이블이 있는 Gpo만 표시 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 이벤트 정보


선택한 GPO의 기록에 각 이벤트에 대 한 정보가 제공 됩니다.

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
<td align="left"><p><strong>컴퓨터</strong></p></td>
<td align="left"><p>GPO의 컴퓨터 구성 부분에 대 한 버전을 자동으로 생성 했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>사용자</strong></p></td>
<td align="left"><p>GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>시간</strong></p></td>
<td align="left"><p>상태 필드의 작업을 수행 했을 때의 GPO 버전의 타임 스탬프입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>시</strong></p></td>
<td align="left"><p>선택한 GPO 버전의 상태:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>배포 </strong> 됨:이 버전의 GPO는 현재 프로덕션 환경에 살고 있습니다.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>체크 인 </strong> :이 버전의 GPO를 사용 하 여 승인 된 편집기가 편집을 확인 하거나 그룹 정책 관리자가 배포할 수 있습니다.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>체크 아웃 </strong> :이 버전의 GPO는 현재 편집자에 의해 체크 아웃 되었으므로 다른 편집기에서 사용할 수 없습니다. (체크 아웃 상태는 다음에 <strong> 기록 되지 않습니다. </strong>현재 GPO가 체크 아웃 되었는지 표시 하는 경우를 제외 하 고 기록</p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong>만들어짐 </strong> : GPO를 처음 만들 때의 날짜와 시간을 식별 합니다.</p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong>레이블이 지정 됨 </strong> : 레이블이 지정 된 GPO 버전을 식별 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>GPO 상태</strong></p></td>
<td align="left"><p>컴퓨터 구성과 사용자 구성을 서로 별도로 관리할 수 있습니다. 이 상태는 사용할 수 있는 GPO의 일부를 보여 줍니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>소유자</strong></p></td>
<td align="left"><p>GPO를 체크 인 하거나 배포한 사람입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>설명</strong></p></td>
<td align="left"><p>이 버전이 수정 된 시점에 GPO 소유자가 입력 한 메모입니다. 이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 보고


단일 GPO 버전 또는 여러 GPO 버전이 선택 되었는지 여부에 따라 **설정** 및 **차이점** 단추에 gpo 설정에 대 한 보고서가 표시 됩니다. GPO 버전을 마우스 오른쪽 단추로 클릭 하면 XML 기반 보고서도 표시할 수 있는 옵션이 제공 됩니다.

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

-   [내용 탭](contents-tab.md)

 

 





