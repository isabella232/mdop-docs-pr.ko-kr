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
# <span data-ttu-id="ede42-103">기록 창</span><span class="sxs-lookup"><span data-stu-id="ede42-103">History Window</span></span>


<span data-ttu-id="ede42-104">Gpo를 두 번 클릭 하거나 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **기록**클릭 하 여 Gpo (그룹 정책 개체)의 기록을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-104">The history of a Group Policy object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="ede42-105">또한 GPMC ( **그룹 정책 관리 콘솔** )에 각 GPO에 대 한 탭으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="ede42-106">기록에는 보관에 저장 된 선택한 GPO의 모든 버전이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-106">The history provides a list of all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="ede42-107">**기록** 창에서 gpo 내의 설정에 대 한 보고서를 가져오거나, gpo의 여러 버전을 비교 하거나, 이전 버전의 gpo로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-107">From the **History** window, you can obtain a report of the settings within a GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="ede42-108">기록 창에서 이벤트 필터링</span><span class="sxs-lookup"><span data-stu-id="ede42-108">Filtering events in the History window</span></span>


<span data-ttu-id="ede42-109">**기록** 창 내의 탭에서 표시 되는 이벤트를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-109">The tabs within the **History** window filter the events displayed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ede42-110">탭</span><span class="sxs-lookup"><span data-stu-id="ede42-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="ede42-111">필터링</span><span class="sxs-lookup"><span data-stu-id="ede42-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-112">모두 표시</span><span class="sxs-lookup"><span data-stu-id="ede42-112">Show All</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-113">모든 버전의 GPO를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-113">Display all versions of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-114">체크 인 됨</span><span class="sxs-lookup"><span data-stu-id="ede42-114">Checked In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-115">해당 GPO의 체크 인 버전만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-115">Display only checked-in versions of the GPO.</span></span> <span data-ttu-id="ede42-116">배포 된 버전은이 목록에서 생략 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-116">The deployed version is omitted from this list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-117">레이블만</span><span class="sxs-lookup"><span data-stu-id="ede42-117">Labels Only</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-118">연결 된 레이블이 있는 Gpo만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-118">Display only GPOs that have labels associated with them.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ede42-119">이벤트 정보</span><span class="sxs-lookup"><span data-stu-id="ede42-119">Event information</span></span>


<span data-ttu-id="ede42-120">선택한 GPO의 기록에 각 이벤트에 대 한 정보가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-120">Information is provided for each event in the history of the selected GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ede42-121">GPO 특성</span><span class="sxs-lookup"><span data-stu-id="ede42-121">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="ede42-122">설명</span><span class="sxs-lookup"><span data-stu-id="ede42-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-123">컴퓨터</span><span class="sxs-lookup"><span data-stu-id="ede42-123">Computer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-124">GPO의 컴퓨터 구성 부분에 대 한 버전을 자동으로 생성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-124">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-125">사용자</span><span class="sxs-lookup"><span data-stu-id="ede42-125">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-126">GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-126">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-127">시간</span><span class="sxs-lookup"><span data-stu-id="ede42-127">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-128">상태 필드의 작업을 수행 했을 때의 GPO 버전의 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-128">Timestamp of the version of the GPO when the action in the status field was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-129">시</span><span class="sxs-lookup"><span data-stu-id="ede42-129">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-130">선택한 GPO 버전의 상태:</span><span class="sxs-lookup"><span data-stu-id="ede42-130">The state of the selected version of the GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="ede42-131">배포 </strong> 됨:이 버전의 GPO는 현재 프로덕션 환경에 살고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-131">Deployed</strong>: This version of the GPO is currently live in the production environment.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="ede42-132">체크 인 </strong> :이 버전의 GPO를 사용 하 여 승인 된 편집기가 편집을 확인 하거나 그룹 정책 관리자가 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-132">Checked In</strong>: This version of the GPO is available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="ede42-133">체크 아웃 </strong> :이 버전의 GPO는 현재 편집자에 의해 체크 아웃 되었으므로 다른 편집기에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-133">Checked Out</strong>: This version of the GPO is currently checked out by an Editor and is unavailable for other Editors.</span></span> <span data-ttu-id="ede42-134">(체크 아웃 상태는 다음에 <strong> 기록 되지 않습니다. </strong>현재 GPO가 체크 아웃 되었는지 표시 하는 경우를 제외 하 고 기록</span><span class="sxs-lookup"><span data-stu-id="ede42-134">(The checked out state is not recorded in the <strong>History</strong> except to indicate if a GPO is currently checked out.)</span></span></p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong><span data-ttu-id="ede42-135">만들어짐 </strong> : GPO를 처음 만들 때의 날짜와 시간을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-135">Created</strong>: Identifies the date and time of the initial creation of the GPO.</span></span></p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong><span data-ttu-id="ede42-136">레이블이 지정 됨 </strong> : 레이블이 지정 된 GPO 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-136">Labeled</strong>: Identifies a labeled version of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-137">GPO 상태</span><span class="sxs-lookup"><span data-stu-id="ede42-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-138">컴퓨터 구성과 사용자 구성을 서로 별도로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="ede42-139">이 상태는 사용할 수 있는 GPO의 일부를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-140">소유자</span><span class="sxs-lookup"><span data-stu-id="ede42-140">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-141">GPO를 체크 인 하거나 배포한 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-141">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-142">설명</span><span class="sxs-lookup"><span data-stu-id="ede42-142">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-143">이 버전이 수정 된 시점에 GPO 소유자가 입력 한 메모입니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-143">A comment entered by the owner of a GPO at the time that this version was modified.</span></span> <span data-ttu-id="ede42-144">이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-144">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ede42-145">보고</span><span class="sxs-lookup"><span data-stu-id="ede42-145">Reports</span></span>


<span data-ttu-id="ede42-146">단일 GPO 버전 또는 여러 GPO 버전이 선택 되었는지 여부에 따라 **설정** 및 **차이점** 단추에 gpo 설정에 대 한 보고서가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-146">Depending on whether a single GPO version or multiple GPO versions are selected, the **Settings** and **Differences** buttons display reports on GPO settings.</span></span> <span data-ttu-id="ede42-147">GPO 버전을 마우스 오른쪽 단추로 클릭 하면 XML 기반 보고서도 표시할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-147">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ede42-148">단추</span><span class="sxs-lookup"><span data-stu-id="ede42-148">Button</span></span></th>
<th align="left"><span data-ttu-id="ede42-149">효과</span><span class="sxs-lookup"><span data-stu-id="ede42-149">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-150">설정</span><span class="sxs-lookup"><span data-stu-id="ede42-150">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-151">선택한 GPO 버전 내의 설정을 표시 하는 HTML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-151">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-152">차이점</span><span class="sxs-lookup"><span data-stu-id="ede42-152">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-153">선택한 여러 GPO 버전 내의 설정을 비교 하 여 HTML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-153">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ede42-154">차이점 보고서에 대 한 주요 정보</span><span class="sxs-lookup"><span data-stu-id="ede42-154">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ede42-155">기호</span><span class="sxs-lookup"><span data-stu-id="ede42-155">Symbol</span></span></th>
<th align="left"><span data-ttu-id="ede42-156">의미</span><span class="sxs-lookup"><span data-stu-id="ede42-156">Meaning</span></span></th>
<th align="left"><span data-ttu-id="ede42-157">색상</span><span class="sxs-lookup"><span data-stu-id="ede42-157">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ede42-158">없음</span><span class="sxs-lookup"><span data-stu-id="ede42-158">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ede42-159">두 Gpo에 동일한 설정이 있는 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-159">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="ede42-160">수준에 따라 다름</span><span class="sxs-lookup"><span data-stu-id="ede42-160">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-161">[#]</span><span class="sxs-lookup"><span data-stu-id="ede42-161">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-162">항목이 두 Gpo에 모두 있지만 변경 된 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-162">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="ede42-163">화면이</span><span class="sxs-lookup"><span data-stu-id="ede42-163">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ede42-164">[-]</span><span class="sxs-lookup"><span data-stu-id="ede42-164">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-165">항목이 첫 번째 GPO에만 있음</span><span class="sxs-lookup"><span data-stu-id="ede42-165">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="ede42-166">빨간색</span><span class="sxs-lookup"><span data-stu-id="ede42-166">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ede42-167">[+]</span><span class="sxs-lookup"><span data-stu-id="ede42-167">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ede42-168">두 번째 GPO에만 항목이 있음</span><span class="sxs-lookup"><span data-stu-id="ede42-168">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="ede42-169">녹색</span><span class="sxs-lookup"><span data-stu-id="ede42-169">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="ede42-170">설정이 변경 된 항목의 경우 항목을 확장할 때 변경 된 설정이 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-170">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="ede42-171">각 GPO의 특성 값은 Gpo가 보고서에 표시 되는 순서 대로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-171">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="ede42-172">일부 설정이 변경 되 면 항목이 두 개의 다른 항목 (첫 번째 GPO에만 표시 되며 변경 된 하나의 항목이 아닌 한 항목으로 보고 됨)이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ede42-172">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="ede42-173">추가 참조</span><span class="sxs-lookup"><span data-stu-id="ede42-173">Additional references</span></span>

-   [<span data-ttu-id="ede42-174">내용 탭</span><span class="sxs-lookup"><span data-stu-id="ede42-174">Contents Tab</span></span>](contents-tab.md)

 

 





