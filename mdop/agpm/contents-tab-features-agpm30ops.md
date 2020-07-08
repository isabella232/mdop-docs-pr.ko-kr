---
title: 내용 탭 기능
description: 내용 탭 기능
author: dansimp
ms.assetid: 725f025a-c30a-4d07-add1-4e0ed9a1a5fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f64aad16a3335d78641812121692f6d5f6436ee1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818908"
---
# 내용 탭 기능


**콘텐츠** 탭의 각 보조 탭에는**그룹 정책 개체** 및 **그룹과 사용자**라는 두 가지 섹션이 있습니다.

## 그룹 정책 개체 섹션


**그룹 정책 개체** 섹션은 Gpo (그룹 정책 개체)의 필터링 된 목록을 표시 하 고 각 gpo에 대해 다음 특성을 식별 합니다.

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
<td align="left"><p><strong>이름</strong></p></td>
<td align="left"><p>GPO의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>시</strong></p></td>
<td align="left"><p>선택한 GPO의 상태</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>변경한 사람</strong></p></td>
<td align="left"><p>체크 인 한 편집기나 선택한 GPO를 배포한 승인자</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>날짜 변경</strong></p></td>
<td align="left"><p>제어 된 GPO의 경우, 수정 또는 체크 아웃 한 후에 가장 최근에 체크 인 한 날짜입니다. 미제어 GPO의 경우 마지막으로 수정한 날짜입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>설명</strong></p></td>
<td align="left"><p>수정한 시간에 GPO를 체크 인 하거나 배포한 사람이 입력 한 메모입니다. 이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</p></td>
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
<td align="left"><p>컴퓨터 구성과 사용자 구성을 개별적으로 관리할 수 있습니다. GPO 상태는 사용할 수 있는 GPO의 일부를 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>WMI 필터</strong></p></td>
<td align="left"><p>이 GPO에 적용 된 WMI 필터를 표시 합니다. WMI 필터는 <strong> </strong> GPMC의 콘솔 트리에서 도메인에 대 한 wmi 필터 폴더에 관리 됩니다.</p></td>
</tr>
</tbody>
</table>

 

## 그룹 및 사용자 섹션


GPO를 선택 하면 **그룹 및 사용자** 섹션에는 해당 gpo에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록이 표시 됩니다. 각 그룹 또는 사용자에 대해 허용 된 사용 권한 및 상속이 표시 됩니다. AGPM 관리자는 표준 AGPM 역할 (편집자, 승인자, 검토자, AGPM 관리자) 또는 사용자 지정 된 사용 권한 조합을 사용 하 여 사용 권한을 구성할 수 있습니다.

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
<td align="left"><p><strong>Add</strong></p></td>
<td align="left"><p>보안 설명자에 새 항목을 추가 합니다. Active Directory의 모든 사용자 또는 그룹을 추가할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>제거</strong></p></td>
<td align="left"><p>선택 된 항목을 액세스 제어 목록에서 제거 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>특성</strong></p></td>
<td align="left"><p>선택한 개체의 속성을 표시 합니다. 속성 페이지는 <strong> Active Directory 사용자 및 컴퓨터의 개체에 대해 표시 되는 것과 동일 합니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>고급</strong></p></td>
<td align="left"><p><strong>액세스 제어 목록 편집기를 엽니다 </strong> .</p></td>
</tr>
</tbody>
</table>

 

### 추가 고려 사항

-   특정 작업과 관련 된 역할 및 권한에 대 한 자세한 내용은 [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks-agpm30ops.md), [편집자 작업](performing-editor-tasks-agpm30ops.md)수행, [승인자 작업 수행](performing-approver-tasks-agpm30ops.md), [검토자 작업 수행](performing-reviewer-tasks-agpm30ops.md)의 작업을 참조 하세요.

### 추가 참조

-   [내용 탭](contents-tab-agpm30ops.md)

 

 





