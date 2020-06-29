---
title: 제어되지 않은 GPO 명령
description: 제어되지 않은 GPO 명령
author: dansimp
ms.assetid: 05a8050f-adc3-465b-8524-bbe95745165c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8efd1c1d3005fd97b92d392140b92bae6a38681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818243"
---
# <span data-ttu-id="078d9-103">제어되지 않은 GPO 명령</span><span class="sxs-lookup"><span data-stu-id="078d9-103">Uncontrolled GPO Commands</span></span>


<span data-ttu-id="078d9-104">**제어** 되지 않은 탭:</span><span class="sxs-lookup"><span data-stu-id="078d9-104">The **Uncontrolled** tab:</span></span>

-   <span data-ttu-id="078d9-105">AGPM (고급 그룹 정책 관리)에서 관리 되지 않는 Gpo (그룹 정책 개체)의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-105">Displays a list of Group Policy Objects (GPOs) not managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="078d9-106">AGPM 관리에서 제어 되지 않은 Gpo를 가져오고 Gpo에 대 한 기록 및 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-106">Provides a shortcut menu with commands for bringing uncontrolled GPOs under the management of AGPM and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="078d9-107">선택한 GPO에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="078d9-108">이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 다음 중 해당 되는 옵션을 비롯 한 바로 가기 메뉴가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="078d9-109">제어 및 기록</span><span class="sxs-lookup"><span data-stu-id="078d9-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="078d9-110">명령</span><span class="sxs-lookup"><span data-stu-id="078d9-110">Command</span></span></th>
<th align="left"><span data-ttu-id="078d9-111">효과</span><span class="sxs-lookup"><span data-stu-id="078d9-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="078d9-112">기록</span><span class="sxs-lookup"><span data-stu-id="078d9-112">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-113">보관 함에 저장 된 선택한 GPO의 모든 버전이 나열 된 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-113">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="078d9-114">기록에서 GPO 내의 설정에 대 한 보고서를 얻고, 두 버전의 GPO를 비교 하거나, GPO를 서식 파일과 비교 하거나, 이전 버전의 GPO로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-114">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="078d9-115">컨트롤</span><span class="sxs-lookup"><span data-stu-id="078d9-115">Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-116">선택한 제어 되지 않는 GPO를 AGPM의 변경 컨트롤 관리 아래에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-116">Bring the selected uncontrolled GPO under the change control management of AGPM.</span></span> <span data-ttu-id="078d9-117">GPO를 제어할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-117">If you do not have permission to control a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="078d9-118">서식 파일로 저장</span><span class="sxs-lookup"><span data-stu-id="078d9-118">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-119">선택한 GPO의 설정을 기반으로 새 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-119">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="078d9-120">보고</span><span class="sxs-lookup"><span data-stu-id="078d9-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="078d9-121">명령</span><span class="sxs-lookup"><span data-stu-id="078d9-121">Command</span></span></th>
<th align="left"><span data-ttu-id="078d9-122">효과</span><span class="sxs-lookup"><span data-stu-id="078d9-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="078d9-123">설정</span><span class="sxs-lookup"><span data-stu-id="078d9-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-124">선택한 GPO 내의 설정을 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="078d9-125">차이점</span><span class="sxs-lookup"><span data-stu-id="078d9-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-126">선택한 두 Gpo 내의 설정과 선택한 GPO 및 서식 파일을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="078d9-127">기타</span><span class="sxs-lookup"><span data-stu-id="078d9-127">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="078d9-128">명령</span><span class="sxs-lookup"><span data-stu-id="078d9-128">Command</span></span></th>
<th align="left"><span data-ttu-id="078d9-129">효과</span><span class="sxs-lookup"><span data-stu-id="078d9-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="078d9-130">새로 고침</span><span class="sxs-lookup"><span data-stu-id="078d9-130">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-131">변경 내용을 통합 하기 위해 GPMC (그룹 정책 관리) 콘솔의 표시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-131">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="078d9-132">일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-132">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="078d9-133">Help</span><span class="sxs-lookup"><span data-stu-id="078d9-133">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="078d9-134">AGPM에 대 한 도움말을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d9-134">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="078d9-135">추가 참조</span><span class="sxs-lookup"><span data-stu-id="078d9-135">Additional references</span></span>

-   [<span data-ttu-id="078d9-136">내용 탭</span><span class="sxs-lookup"><span data-stu-id="078d9-136">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="078d9-137">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="078d9-137">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="078d9-138">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="078d9-138">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="078d9-139">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="078d9-139">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 




