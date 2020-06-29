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
# <span data-ttu-id="11bf0-103">기록 창</span><span class="sxs-lookup"><span data-stu-id="11bf0-103">History Window</span></span>


<span data-ttu-id="11bf0-104">Gpo를 두 번 클릭 하거나 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **기록**클릭 하 여 Gpo (그룹 정책 개체)의 기록을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="11bf0-105">또한 GPMC ( **그룹 정책 관리 콘솔** )에 각 GPO에 대 한 탭으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="11bf0-106">기록은 선택한 GPO의 수명에서 이벤트 기록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="11bf0-107">**기록** 창에서 gpo 버전 내의 설정에 대 한 보고서를 가져오거나, gpo의 여러 버전을 비교 하거나, 이전 버전의 gpo로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="11bf0-108">기록 창에서 이벤트 필터링</span><span class="sxs-lookup"><span data-stu-id="11bf0-108">Filtering events in the History window</span></span>


<span data-ttu-id="11bf0-109">**기록** 창 내의 탭은 GPO 기록의 상태를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11bf0-110">탭</span><span class="sxs-lookup"><span data-stu-id="11bf0-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="11bf0-111">필터링</span><span class="sxs-lookup"><span data-stu-id="11bf0-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-112">모든 상태</span><span class="sxs-lookup"><span data-stu-id="11bf0-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-113">GPO 기록의 모든 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-114">고유 버전</span><span class="sxs-lookup"><span data-stu-id="11bf0-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-115">아카이브에 체크 된 고유한 GPO 버전만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="11bf0-116">프로덕션 환경에 배포 된 버전, 고유 버전에 대 한 바로 가기 및 정보 상태는이 목록에서 생략 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="11bf0-117">이벤트 정보</span><span class="sxs-lookup"><span data-stu-id="11bf0-117">Event information</span></span>


<span data-ttu-id="11bf0-118">GPO 기록의 각 상태에 대 한 정보가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11bf0-119">GPO 특성</span><span class="sxs-lookup"><span data-stu-id="11bf0-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="11bf0-120">설명</span><span class="sxs-lookup"><span data-stu-id="11bf0-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-121">날짜 변경</span><span class="sxs-lookup"><span data-stu-id="11bf0-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-122">상태 열의 작업을 수행한 시간의 타임 스탬프 <strong> 입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="11bf0-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-123">시</span><span class="sxs-lookup"><span data-stu-id="11bf0-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-124">GPO 기록의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-125">변경한 사람</span><span class="sxs-lookup"><span data-stu-id="11bf0-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-126">GPO를 체크 인 하거나 배포한 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-127">설명</span><span class="sxs-lookup"><span data-stu-id="11bf0-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-128">이 버전이 수정 된 시점에 GPO를 체크 인 하거나 배포 하는 사람이 입력 한 메모입니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="11bf0-129">이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-130">삭제할</span><span class="sxs-lookup"><span data-stu-id="11bf0-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-131">보관 저장소에 보존 된 각 GPO의 고유 버전 수가 제한 되어 있는 경우이 버전의 GPO를 삭제할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="11bf0-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="11bf0-132">참고</span><span class="sxs-lookup"><span data-stu-id="11bf0-132">Note</span></span></strong><br/><p><span data-ttu-id="11bf0-133">GPO를 마우스 오른쪽 단추로 클릭 한 다음 <strong> 삭제 허용 또는 삭제 허용 안 함을 클릭 하 여 해당 버전을 삭제할 수 있습니다 </strong> <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="11bf0-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-134">컴퓨터 버전</span><span class="sxs-lookup"><span data-stu-id="11bf0-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-135">GPO의 컴퓨터 구성 부분에 대 한 버전을 자동으로 생성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-136">사용자 버전</span><span class="sxs-lookup"><span data-stu-id="11bf0-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-137">GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-138">GPO 상태</span><span class="sxs-lookup"><span data-stu-id="11bf0-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-139">컴퓨터 구성과 사용자 구성을 서로 별도로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="11bf0-140">이 상태는 사용할 수 있는 GPO의 일부를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-141">WMI 필터</span><span class="sxs-lookup"><span data-stu-id="11bf0-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-142">이 GPO에 적용 된 WMI 필터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="11bf0-143">WMI 필터는 <strong> </strong> GPMC의 콘솔 트리에서 도메인에 대 한 wmi 필터 폴더에 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="11bf0-144">보고</span><span class="sxs-lookup"><span data-stu-id="11bf0-144">Reports</span></span>


<span data-ttu-id="11bf0-145">**설정** 및 **차이점** 단추에는 선택한 gpo 버전에 대 한 gpo 설정에 대 한 보고서가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="11bf0-146">GPO 버전을 마우스 오른쪽 단추로 클릭 하면 XML 기반 보고서도 표시할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11bf0-147">단추</span><span class="sxs-lookup"><span data-stu-id="11bf0-147">Button</span></span></th>
<th align="left"><span data-ttu-id="11bf0-148">효과</span><span class="sxs-lookup"><span data-stu-id="11bf0-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-149">설정</span><span class="sxs-lookup"><span data-stu-id="11bf0-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-150">선택한 GPO 버전 내의 설정을 표시 하는 HTML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-151">차이점</span><span class="sxs-lookup"><span data-stu-id="11bf0-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-152">선택한 여러 GPO 버전 내의 설정을 비교 하 여 HTML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="11bf0-153">차이점 보고서에 대 한 주요 정보</span><span class="sxs-lookup"><span data-stu-id="11bf0-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11bf0-154">기호</span><span class="sxs-lookup"><span data-stu-id="11bf0-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="11bf0-155">의미</span><span class="sxs-lookup"><span data-stu-id="11bf0-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="11bf0-156">색상</span><span class="sxs-lookup"><span data-stu-id="11bf0-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11bf0-157">없음</span><span class="sxs-lookup"><span data-stu-id="11bf0-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="11bf0-158">두 Gpo에 동일한 설정이 있는 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="11bf0-159">수준에 따라 다름</span><span class="sxs-lookup"><span data-stu-id="11bf0-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-160">[#]</span><span class="sxs-lookup"><span data-stu-id="11bf0-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-161">항목이 두 Gpo에 모두 있지만 변경 된 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="11bf0-162">화면이</span><span class="sxs-lookup"><span data-stu-id="11bf0-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="11bf0-163">[-]</span><span class="sxs-lookup"><span data-stu-id="11bf0-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-164">항목이 첫 번째 GPO에만 있음</span><span class="sxs-lookup"><span data-stu-id="11bf0-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="11bf0-165">빨간색</span><span class="sxs-lookup"><span data-stu-id="11bf0-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="11bf0-166">[+]</span><span class="sxs-lookup"><span data-stu-id="11bf0-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="11bf0-167">두 번째 GPO에만 항목이 있음</span><span class="sxs-lookup"><span data-stu-id="11bf0-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="11bf0-168">녹색</span><span class="sxs-lookup"><span data-stu-id="11bf0-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="11bf0-169">설정이 변경 된 항목의 경우 항목을 확장할 때 변경 된 설정이 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="11bf0-170">각 GPO의 특성 값은 Gpo가 보고서에 표시 되는 순서 대로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="11bf0-171">일부 설정이 변경 되 면 항목이 두 개의 다른 항목 (첫 번째 GPO에만 표시 되며 변경 된 하나의 항목이 아닌 한 항목으로 보고 됨)이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bf0-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="11bf0-172">추가 참조</span><span class="sxs-lookup"><span data-stu-id="11bf0-172">Additional references</span></span>

-   [<span data-ttu-id="11bf0-173">내용 탭</span><span class="sxs-lookup"><span data-stu-id="11bf0-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









