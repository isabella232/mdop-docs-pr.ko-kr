---
title: 일반적인 보조 탭 기능
description: 일반적인 보조 탭 기능
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819088"
---
# 일반적인 보조 탭 기능


각 보조 탭에는**그룹 정책 개체** 및 **그룹과 사용자**라는 두 가지 섹션이 있습니다.

## 그룹 정책 개체 섹션


**그룹 정책 개체** 섹션에는 Gpo (그룹 정책 개체)의 필터링 된 목록이 표시 되며 각 gpo에 대 한 다음 특성을 식별 합니다.

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
<td align="left"><p>그룹 정책 개체의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>컴퓨터 (Comp.)</strong></p></td>
<td align="left"><p>GPO의 컴퓨터 구성 부분에 대 한 버전을 자동으로 생성 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>사용자</strong></p></td>
<td align="left"><p>GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>시</strong></p></td>
<td align="left"><p>선택한 GPO의 상태입니다.</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>미제어: </strong> AGPM에서 관리 되지 않습니다.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>체크 인: </strong> 권한이 있는 편집기에서 편집을 확인 하거나 그룹 정책 관리자가 배포할 수 있습니다.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>체크 아웃 됨: </strong> 현재 편집 중입니다. 체크 아웃 하거나 AGPM 관리자가 확인 한 편집기에서 체크 아웃할 때까지 다른 편집기에서이를 사용할 수 없습니다.</p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong>보류 중: </strong> 그룹 정책 관리자가 만들거나, 제어 하거나, 배포 하거나, 삭제 하기 전에 승인을 기다립니다.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>삭제 됨: </strong> 보관에서 삭제 되지만 복원할 수 있습니다.</p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong>서식 파일: </strong> 새 gpo를 만들 때 시작 점으로 사용할 GPO의 정적 버전입니다.</p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong>서식 파일 (기본값): </strong> 이 서식 파일은 기본적으로 새 GPO를 만들 때 사용 되는 시작 위치입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>GPO 상태</strong></p></td>
<td align="left"><p>컴퓨터 구성과 사용자 구성을 개별적으로 관리할 수 있습니다. GPO 상태는 사용할 수 있는 GPO의 일부를 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>WMI 필터</strong></p></td>
<td align="left"><p>이 GPO에 적용 된 WMI 필터를 표시 합니다. WMI 필터는 <strong> </strong> GPMC 콘솔 트리의 도메인에 대 한 wmi 필터 노드에서 관리 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>수정됨</strong></p></td>
<td align="left"><p>제어 된 GPO의 경우, 수정 또는 체크 아웃 한 후에 체크 인 되는 가장 최근 날짜입니다. 미제어 GPO의 경우 마지막으로 수정한 날짜입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>소유자</strong></p></td>
<td align="left"><p>체크 인 한 편집기나 선택한 GPO를 배포한 승인자</p></td>
</tr>
</tbody>
</table>

 

## 그룹 및 사용자 섹션


GPO를 선택 하면 **그룹 및 사용자** 섹션에는 해당 gpo에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록이 표시 됩니다. 각 그룹 또는 사용자에 대해 허용 된 사용 권한 및 상속이 표시 됩니다. AGPM 관리자는 표준 AGPM 역할 (편집기, 승인자 및 검토자) 또는 사용자 지정 된 사용 권한 조합을 사용 하 여 사용 권한을 구성할 수 있습니다.

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

-   특정 작업과 관련 된 역할 및 권한에 대 한 자세한 내용은 [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks.md), [편집자 작업](performing-editor-tasks.md)수행, [승인자 작업 수행](performing-approver-tasks.md), [검토자 작업 수행](performing-reviewer-tasks.md)의 작업을 참조 하세요.

### 추가 참조

-   [내용 탭](contents-tab.md)

 

 





