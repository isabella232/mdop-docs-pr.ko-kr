---
title: 기록 창
description: 기록 창
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820793"
---
# <span data-ttu-id="029df-103">기록 창</span><span class="sxs-lookup"><span data-stu-id="029df-103">History Window</span></span>


<span data-ttu-id="029df-104">Gpo를 두 번 클릭 하거나 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **기록**클릭 하 여 Gpo (그룹 정책 개체)의 기록을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="029df-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="029df-105">또한 GPMC (그룹 정책 관리 콘솔)에 각 GPO에 대 한 탭으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="029df-106">기록은 선택한 GPO의 수명에서 이벤트 기록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="029df-107">**기록** 창에서 gpo 버전의 설정에 대 한 보고서를 가져오거나, gpo의 여러 버전을 비교 하거나, 이전 버전의 gpo로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="029df-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="029df-108">기록 창에서 이벤트 필터링</span><span class="sxs-lookup"><span data-stu-id="029df-108">Filtering events in the History window</span></span>


<span data-ttu-id="029df-109">**기록** 창 내의 탭은 GPO 기록의 상태를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="029df-110">탭</span><span class="sxs-lookup"><span data-stu-id="029df-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="029df-111">필터링</span><span class="sxs-lookup"><span data-stu-id="029df-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-112">모든 상태</span><span class="sxs-lookup"><span data-stu-id="029df-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-113">GPO 기록의 모든 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-114">고유 버전</span><span class="sxs-lookup"><span data-stu-id="029df-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-115">아카이브에 체크 된 고유한 GPO 버전만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="029df-116">프로덕션 환경에 배포 된 버전, 고유 버전에 대 한 바로 가기 및 정보 상태는이 목록에서 생략 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="029df-117">이벤트 정보</span><span class="sxs-lookup"><span data-stu-id="029df-117">Event information</span></span>


<span data-ttu-id="029df-118">GPO 기록의 각 상태에 대 한 정보가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="029df-119">GPO 특성</span><span class="sxs-lookup"><span data-stu-id="029df-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="029df-120">설명</span><span class="sxs-lookup"><span data-stu-id="029df-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-121">날짜 변경</span><span class="sxs-lookup"><span data-stu-id="029df-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-122">상태 열의 작업을 수행한 시간의 타임 스탬프 <strong> 입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="029df-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-123">시</span><span class="sxs-lookup"><span data-stu-id="029df-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-124">GPO 기록의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="029df-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-125">변경한 사람</span><span class="sxs-lookup"><span data-stu-id="029df-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-126">GPO를 체크 인 하거나 배포한 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="029df-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-127">설명</span><span class="sxs-lookup"><span data-stu-id="029df-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-128">이 버전이 변경 된 시점에 GPO를 체크 인 하거나 배포한 사람이 입력 한 메모는 이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-129">삭제할</span><span class="sxs-lookup"><span data-stu-id="029df-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-130">보관 저장소에 보존 된 각 GPO의 고유 버전 수가 제한 되어 있는 경우이 버전의 GPO를 삭제할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="029df-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="029df-131">참고</span><span class="sxs-lookup"><span data-stu-id="029df-131">Note</span></span></strong><br/><p><span data-ttu-id="029df-132">GPO를 마우스 오른쪽 단추로 클릭 한 다음 <strong> 삭제 허용 또는 삭제 허용 안 함을 클릭 하 여 gpo의 버전을 삭제할 수 있는지 여부를 변경할 수 있습니다 </strong> <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="029df-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-133">컴퓨터 버전</span><span class="sxs-lookup"><span data-stu-id="029df-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-134">GPO의 컴퓨터 구성 부분을 자동으로 생성 된 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="029df-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-135">사용자 버전</span><span class="sxs-lookup"><span data-stu-id="029df-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-136">GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="029df-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-137">GPO 상태</span><span class="sxs-lookup"><span data-stu-id="029df-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-138">컴퓨터 구성과 사용자 구성을 서로 별도로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="029df-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="029df-139">이 상태는 사용할 수 있는 GPO의 일부를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="029df-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-140">원본 GPO 정보</span><span class="sxs-lookup"><span data-stu-id="029df-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-141">다른 포리스트에서 가져온 GPO의 경우, 원래 GPO 이름, 도메인, 마지막 변경 내용과 연결 된 사용자 및 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="029df-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="029df-142">보고</span><span class="sxs-lookup"><span data-stu-id="029df-142">Reports</span></span>


<span data-ttu-id="029df-143">**설정** 및 **차이점** 단추에는 선택한 gpo 버전에 대 한 gpo 설정에 대 한 보고서가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="029df-144">또한 GPO 버전을 마우스 오른쪽 단추로 클릭 하면 XML 기반 보고서를 표시할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="029df-145">단추</span><span class="sxs-lookup"><span data-stu-id="029df-145">Button</span></span></th>
<th align="left"><span data-ttu-id="029df-146">효과</span><span class="sxs-lookup"><span data-stu-id="029df-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-147">설정</span><span class="sxs-lookup"><span data-stu-id="029df-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-148">선택한 GPO 버전 내의 설정을 표시 하는 HTML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-149">차이점</span><span class="sxs-lookup"><span data-stu-id="029df-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-150">선택한 여러 GPO 버전 내의 설정을 비교 하 여 HTML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="029df-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="029df-151">차이점 보고서에 대 한 주요 정보</span><span class="sxs-lookup"><span data-stu-id="029df-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="029df-152">기호</span><span class="sxs-lookup"><span data-stu-id="029df-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="029df-153">의미</span><span class="sxs-lookup"><span data-stu-id="029df-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="029df-154">색상</span><span class="sxs-lookup"><span data-stu-id="029df-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="029df-155">없음</span><span class="sxs-lookup"><span data-stu-id="029df-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="029df-156">두 Gpo에 동일한 설정이 있는 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="029df-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="029df-157">수준에 따라 다름</span><span class="sxs-lookup"><span data-stu-id="029df-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-158">[#]</span><span class="sxs-lookup"><span data-stu-id="029df-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-159">항목이 두 Gpo에 모두 있지만 변경 된 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="029df-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="029df-160">화면이</span><span class="sxs-lookup"><span data-stu-id="029df-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="029df-161">[-]</span><span class="sxs-lookup"><span data-stu-id="029df-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-162">항목이 첫 번째 GPO에만 있음</span><span class="sxs-lookup"><span data-stu-id="029df-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="029df-163">빨간색</span><span class="sxs-lookup"><span data-stu-id="029df-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="029df-164">[+]</span><span class="sxs-lookup"><span data-stu-id="029df-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="029df-165">두 번째 GPO에만 항목이 있음</span><span class="sxs-lookup"><span data-stu-id="029df-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="029df-166">녹색</span><span class="sxs-lookup"><span data-stu-id="029df-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="029df-167">설정이 변경 된 항목의 경우 항목을 확장할 때 변경 된 설정이 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="029df-168">각 GPO의 특성 값은 Gpo가 보고서에 표시 되는 순서 대로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="029df-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="029df-169">일부 설정이 변경 되 면 항목이 두 개의 항목 (첫 번째 GPO에만 표시 되 고 하나는 변경 된 하나의 항목 대신에 표시 됨)으로 보고 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="029df-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="029df-170">추가 참조</span><span class="sxs-lookup"><span data-stu-id="029df-170">Additional references</span></span>

-   [<span data-ttu-id="029df-171">내용 탭</span><span class="sxs-lookup"><span data-stu-id="029df-171">Contents Tab</span></span>](contents-tab-agpm40.md)









