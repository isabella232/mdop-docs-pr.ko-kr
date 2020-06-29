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
# <span data-ttu-id="fdb20-103">GPO 목록 검색 및 필터링</span><span class="sxs-lookup"><span data-stu-id="fdb20-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="fdb20-104">AGPM (고급 그룹 정책 관리)에서 Gpo (그룹 정책 개체) 및 해당 특성의 목록을 검색 하 여 표시 되는 Gpo 목록을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="fdb20-105">예를 들어 특정 이름, 상태 또는 주석을 사용 하 여 Gpo를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="fdb20-106">특정 그룹 정책 관리자 또는 특정 날짜에 의해 마지막으로 변경 된 Gpo를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="fdb20-107">복잡 한 검색 수행</span><span class="sxs-lookup"><span data-stu-id="fdb20-107">Performing a complex search</span></span>


<span data-ttu-id="fdb20-108">다음과 같이 GPO 속성 1 형식을 사용 하 여 복잡 한 검색을 수행할 수 있습니다 *. 검색 문자열 1 GPO 특성 2: 검색 문자열 2 ... 모든 열 검색 문자열*</span><span class="sxs-lookup"><span data-stu-id="fdb20-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="fdb20-109">검색은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="fdb20-110">**GPO 특성:** **컴퓨터 버전이** 나 **사용자 버전이**아닌 AGPM의 gpo 목록에 있는 모든 열 머리글</span><span class="sxs-lookup"><span data-stu-id="fdb20-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="fdb20-111">Gpo 특성에는 gpo 이름, 상태, 가장 최근에 GPO를 변경한 사용자, GPO가 가장 최근에 변경 된 날짜 및 시간, 설명, GPO 상태, GPO에 적용 된 WMI 필터 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="fdb20-112">**검색 문자열:** 지정 된 열에서 검색할 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="fdb20-113">문자열에 공백이 포함 되어 있으면 문자열을 따옴표로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="fdb20-114">**모든 열 검색 문자열:** **컴퓨터 버전과** **사용자 버전이**아닌 AGPM의 gpo 목록에 있는 모든 열에서 검색 하는 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="fdb20-115">공백으로 구분 된 여러 문자열을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="fdb20-116">문자열에 공백이 포함 되어 있으면 문자열을 따옴표로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="fdb20-117">각 GPO 특성 및 검색 문자열 쌍과 논리 AND 연산을 사용 하 여 각 열 검색 문자열을 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="fdb20-118">결과는 지정 된 각 특성에 지정 된 검색 문자열이 포함 되어 있고 하나 이상의 열에 모든 열 검색 문자열이 표시 되는 모든 Gpo의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="fdb20-119">검색은 GPO 이름 또는 사용자 이름의 일부를 입력 하 고 해당 텍스트를 이름에 포함 하는 모든 Gpo 목록을 볼 수 있도록 문자열에 대해 부분적으로 일치 하는 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="fdb20-120">다음은 검색의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdb20-121">검색 결과 설명</span><span class="sxs-lookup"><span data-stu-id="fdb20-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="fdb20-122">검색 쿼리</span><span class="sxs-lookup"><span data-stu-id="fdb20-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdb20-123">모든 Gpo (이름에는 문자 <strong> 보안 및 북미)가 포함 </strong> <strong> </strong> 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fdb20-124">이름: </strong><strong> 보안 </strong><strong> 이름: </strong> &quot; <strong> 북미</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="fdb20-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdb20-125">모든 체크 아웃 된 Gpo</span><span class="sxs-lookup"><span data-stu-id="fdb20-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fdb20-126">상태: </strong> &quot; <strong> 체크 아웃 됨</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="fdb20-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdb20-127">관리자 라는 사용자가 최근에 변경 <strong> </strong> 하 고 이전 달에 최근에 변경 된 모든 gpo</span><span class="sxs-lookup"><span data-stu-id="fdb20-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fdb20-128">변경한 사람: </strong><strong> 관리자 </strong><strong> 변경 날짜: </strong><strong> 마지막 월</span><span class="sxs-lookup"><span data-stu-id="fdb20-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdb20-129">Word <strong> 방화벽이 </strong> 가장 최근 메모에 포함 되 고 모든 <strong> </strong> 열에 word 보안이 표시 되는 모든 gpo</span><span class="sxs-lookup"><span data-stu-id="fdb20-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fdb20-130">설명: </strong><strong> 방화벽 </strong><strong> 보안</span><span class="sxs-lookup"><span data-stu-id="fdb20-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdb20-131"><strong>모든 설정을 사용할 수 없는 상태인 모든 gpo </strong></span><span class="sxs-lookup"><span data-stu-id="fdb20-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fdb20-132">gpo 상태: </strong><strong> 모두</span><span class="sxs-lookup"><span data-stu-id="fdb20-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdb20-133"><strong>내 Wmi 필터를 </strong> 적용 하 고 <strong> 사용자 구성 설정 상태를 사용할 수 </strong> 없는 Wmi 필터가 있는 모든 gpo</span><span class="sxs-lookup"><span data-stu-id="fdb20-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fdb20-134">wmi 필터: </strong> &quot; <strong> 내 wmi 필터 </strong> &quot; <strong> gpo 상태: </strong><strong> 사용자</span><span class="sxs-lookup"><span data-stu-id="fdb20-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fdb20-135">날짜 지정</span><span class="sxs-lookup"><span data-stu-id="fdb20-135">Specifying dates</span></span>


<span data-ttu-id="fdb20-136">Windows에서 검색 하는 데 사용할 수 있는 것과 동일한 특별 용어를 사용 하 여 특정 날짜 또는 시간에 변경 된 Gpo를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="fdb20-137">특정 날짜 또는 시간을 입력 하는 경우 **날짜 변경** 열에 사용 되는 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="fdb20-138">다음은 **변경 날짜** 열을 검색 하는 예입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="fdb20-139">**날짜 변경:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="fdb20-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="fdb20-140">**날짜 변경:\*\*\*\*10/10/2009 9:00:00 오전**</span><span class="sxs-lookup"><span data-stu-id="fdb20-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="fdb20-141">**날짜 변경:\*\*\*\*thisweek**</span><span class="sxs-lookup"><span data-stu-id="fdb20-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="fdb20-142">**날짜 변경** 열을 검색할 때 대/소문자를 구분 하지 않는 다음과 같은 특수 용어를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="fdb20-143">오늘</span><span class="sxs-lookup"><span data-stu-id="fdb20-143">Today</span></span>**

-   **<span data-ttu-id="fdb20-144">어제</span><span class="sxs-lookup"><span data-stu-id="fdb20-144">Yesterday</span></span>**

-   **<span data-ttu-id="fdb20-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="fdb20-145">ThisWeek</span></span>**

-   **<span data-ttu-id="fdb20-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="fdb20-146">LastWeek</span></span>**

-   **<span data-ttu-id="fdb20-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="fdb20-147">ThisMonth</span></span>**

-   **<span data-ttu-id="fdb20-148">마지막 달</span><span class="sxs-lookup"><span data-stu-id="fdb20-148">LastMonth</span></span>**

-   **<span data-ttu-id="fdb20-149">TwoMonths</span><span class="sxs-lookup"><span data-stu-id="fdb20-149">TwoMonths</span></span>**

-   **<span data-ttu-id="fdb20-150">ThreeMonths</span><span class="sxs-lookup"><span data-stu-id="fdb20-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="fdb20-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="fdb20-151">ThisYear</span></span>**

-   **<span data-ttu-id="fdb20-152">LastYear</span><span class="sxs-lookup"><span data-stu-id="fdb20-152">LastYear</span></span>**

### <span data-ttu-id="fdb20-153">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="fdb20-153">Additional considerations</span></span>

-   <span data-ttu-id="fdb20-154">이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="fdb20-155">특히, 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb20-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="fdb20-156">GPO 특성에 대 한 자세한 내용은 [콘텐츠 탭 기능](contents-tab-features-agpm40.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fdb20-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="fdb20-157">추가 참조</span><span class="sxs-lookup"><span data-stu-id="fdb20-157">Additional references</span></span>

-   [<span data-ttu-id="fdb20-158">고급 그룹 정책 관리 4.0</span><span class="sxs-lookup"><span data-stu-id="fdb20-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





