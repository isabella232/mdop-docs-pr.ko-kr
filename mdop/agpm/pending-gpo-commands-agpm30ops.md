---
title: 보류 중인 GPO 명령
description: 보류 중인 GPO 명령
author: dansimp
ms.assetid: 3868dda0-8a41-4bba-9b0c-9f656f9a3cd5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde41ea33305290174eab6e34c382aec4ce8b18d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822473"
---
# <span data-ttu-id="aeec9-103">보류 중인 GPO 명령</span><span class="sxs-lookup"><span data-stu-id="aeec9-103">Pending GPO Commands</span></span>


<span data-ttu-id="aeec9-104">**보류 중** 탭:</span><span class="sxs-lookup"><span data-stu-id="aeec9-104">The **Pending** tab:</span></span>

-   <span data-ttu-id="aeec9-105">GPO (그룹 정책 개체)에 대 한 요청을 표시 합니다 (예: 만들기, 제어, 배포 또는 삭제).</span><span class="sxs-lookup"><span data-stu-id="aeec9-105">Displays a list of Group Policy Objects (GPOs) with pending requests for GPO management actions (such as creation, control, deployment, or deletion).</span></span>

-   <span data-ttu-id="aeec9-106">보류 중인 요청에 응답 하 고 Gpo의 기록 및 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-106">Provides a shortcut menu with commands for responding to pending requests and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="aeec9-107">선택한 GPO에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="aeec9-108">이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 다음 중 해당 되는 옵션을 비롯 한 바로 가기 메뉴가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="aeec9-109">제어 및 기록</span><span class="sxs-lookup"><span data-stu-id="aeec9-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aeec9-110">명령</span><span class="sxs-lookup"><span data-stu-id="aeec9-110">Command</span></span></th>
<th align="left"><span data-ttu-id="aeec9-111">효과</span><span class="sxs-lookup"><span data-stu-id="aeec9-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aeec9-112">기록</span><span class="sxs-lookup"><span data-stu-id="aeec9-112">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-113">보관 함에 저장 된 선택한 GPO의 모든 버전이 나열 된 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-113">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="aeec9-114">기록에서 GPO 내의 설정에 대 한 보고서를 얻고, 두 버전의 GPO를 비교 하거나, GPO를 서식 파일과 비교 하거나, 이전 버전의 GPO로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-114">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to a previous version of a GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aeec9-115">철회</span><span class="sxs-lookup"><span data-stu-id="aeec9-115">Withdraw</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-116">요청을 승인 하기 전에 보류 중인 요청을 철회 하 여 선택한 GPO를 만들거나 제어 하거나 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-116">Withdraw your pending request to create, control, or delete the selected GPO before the request has been approved.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aeec9-117">승인</span><span class="sxs-lookup"><span data-stu-id="aeec9-117">Approve</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-118">편집기에서 대기 중인 요청을 완료 하 여 선택한 GPO를 만들거나, 제어 하거나, 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-118">Complete a pending request from an Editor to create, control, or delete the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aeec9-119">거절</span><span class="sxs-lookup"><span data-stu-id="aeec9-119">Reject</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-120">편집기에서 대기 중인 요청을 거부 하 여 선택한 GPO를 만들거나, 제어 하거나, 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-120">Deny a pending request from an Editor to create, control, or delete the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="aeec9-121">보고</span><span class="sxs-lookup"><span data-stu-id="aeec9-121">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aeec9-122">명령</span><span class="sxs-lookup"><span data-stu-id="aeec9-122">Command</span></span></th>
<th align="left"><span data-ttu-id="aeec9-123">효과</span><span class="sxs-lookup"><span data-stu-id="aeec9-123">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aeec9-124">설정</span><span class="sxs-lookup"><span data-stu-id="aeec9-124">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-125">선택한 GPO 내의 설정을 표시 하거나 Gpo가 최근에 제어, 가져오기 또는 체크 인 되었을 때의 조직 구성 단위에서 선택한 Gpo에 대 한 링크를 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-125">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPOs from organizational units as of when the GPOs are most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aeec9-126">차이점</span><span class="sxs-lookup"><span data-stu-id="aeec9-126">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-127">선택한 두 Gpo 내의 설정과 선택한 GPO 및 서식 파일을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-127">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="aeec9-128">기타</span><span class="sxs-lookup"><span data-stu-id="aeec9-128">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aeec9-129">명령</span><span class="sxs-lookup"><span data-stu-id="aeec9-129">Command</span></span></th>
<th align="left"><span data-ttu-id="aeec9-130">효과</span><span class="sxs-lookup"><span data-stu-id="aeec9-130">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aeec9-131">새로 고침</span><span class="sxs-lookup"><span data-stu-id="aeec9-131">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-132">변경 내용을 통합 하기 위해 GPMC (그룹 정책 관리) 콘솔의 표시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-132">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="aeec9-133">일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-133">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aeec9-134">Help</span><span class="sxs-lookup"><span data-stu-id="aeec9-134">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aeec9-135">AGPM에 대 한 도움말을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeec9-135">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="aeec9-136">추가 참조</span><span class="sxs-lookup"><span data-stu-id="aeec9-136">Additional references</span></span>

-   [<span data-ttu-id="aeec9-137">내용 탭</span><span class="sxs-lookup"><span data-stu-id="aeec9-137">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="aeec9-138">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="aeec9-138">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="aeec9-139">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="aeec9-139">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





