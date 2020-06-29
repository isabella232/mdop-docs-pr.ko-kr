---
title: 내용 탭 기능
description: 내용 탭 기능
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818893"
---
# <span data-ttu-id="95db4-103">내용 탭 기능</span><span class="sxs-lookup"><span data-stu-id="95db4-103">Contents Tab Features</span></span>


<span data-ttu-id="95db4-104">**콘텐츠** 탭의 각 보조 탭에는**그룹 정책 개체** 및 **그룹과 사용자**라는 두 가지 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-104">Each secondary tab within the **Contents** tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="95db4-105">그룹 정책 개체 섹션</span><span class="sxs-lookup"><span data-stu-id="95db4-105">Group Policy objects section</span></span>


<span data-ttu-id="95db4-106">**그룹 정책 개체** 섹션은 Gpo (그룹 정책 개체)의 필터링 된 목록을 표시 하 고 각 gpo에 대해 다음 특성을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-106">The **Group Policy objects** section displays a filtered list of Group Policy Objects (GPOs) and identifies the following attributes for each GPO.</span></span> <span data-ttu-id="95db4-107">**검색** 상자를 사용 하 여 특정 특성을 가진 gpo를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-107">You can use the **Search** box to search for GPOs with specific attributes.</span></span> <span data-ttu-id="95db4-108">자세한 내용은 [Gpo 목록 검색 및 필터링](search-and-filter-the-list-of-gpos.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95db4-108">For more information, see [Search and Filter the List of GPOs](search-and-filter-the-list-of-gpos.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95db4-109">GPO 특성</span><span class="sxs-lookup"><span data-stu-id="95db4-109">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="95db4-110">설명</span><span class="sxs-lookup"><span data-stu-id="95db4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-111">이름</span><span class="sxs-lookup"><span data-stu-id="95db4-111">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-112">GPO의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-112">Name of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="95db4-113">시</span><span class="sxs-lookup"><span data-stu-id="95db4-113">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-114">선택한 GPO의 상태</span><span class="sxs-lookup"><span data-stu-id="95db4-114">The state of the selected GPO</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-115">변경한 사람</span><span class="sxs-lookup"><span data-stu-id="95db4-115">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-116">체크 인 한 편집기나 선택한 GPO를 배포한 승인자</span><span class="sxs-lookup"><span data-stu-id="95db4-116">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="95db4-117">날짜 변경</span><span class="sxs-lookup"><span data-stu-id="95db4-117">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-118">제어 된 GPO의 경우, 수정 또는 체크 아웃 한 후에 가장 최근에 체크 인 한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-118">For a controlled GPO, the most recent date it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="95db4-119">미제어 GPO의 경우 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-119">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-120">설명</span><span class="sxs-lookup"><span data-stu-id="95db4-120">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-121">수정한 시간에 GPO를 체크 인 하거나 배포한 사람이 입력 한 메모입니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-121">A comment entered by the person who checked in or deployed a GPO at the time that it was modified.</span></span> <span data-ttu-id="95db4-122">이전 버전으로 롤백할 필요가 있는 경우 버전의 특성을 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-122">Useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="95db4-123">컴퓨터 버전</span><span class="sxs-lookup"><span data-stu-id="95db4-123">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-124">GPO의 컴퓨터 구성 부분을 자동으로 생성 된 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-124">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-125">사용자 버전</span><span class="sxs-lookup"><span data-stu-id="95db4-125">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-126">GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-126">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="95db4-127">GPO 상태</span><span class="sxs-lookup"><span data-stu-id="95db4-127">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-128">컴퓨터 구성과 사용자 구성을 개별적으로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-128">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="95db4-129">GPO 상태는 사용할 수 있는 GPO의 일부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-129">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-130">WMI 필터</span><span class="sxs-lookup"><span data-stu-id="95db4-130">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-131">이 GPO에 적용 된 WMI 필터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-131">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="95db4-132">WMI 필터는 <strong> </strong> GPMC의 콘솔 트리에서 도메인에 대 한 wmi 필터 폴더에 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-132">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="95db4-133">그룹 및 사용자 섹션</span><span class="sxs-lookup"><span data-stu-id="95db4-133">Groups and Users section</span></span>


<span data-ttu-id="95db4-134">GPO를 선택 하면 **그룹 및 사용자** 섹션에는 해당 gpo에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-134">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="95db4-135">각 그룹 또는 사용자에 대해 허용 된 사용 권한 및 상속이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-135">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="95db4-136">AGPM 관리자는 표준 AGPM 역할 (편집자, 승인자, 검토자, AGPM 관리자) 또는 사용자 지정 된 사용 권한 조합을 사용 하 여 사용 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-136">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95db4-137">단추</span><span class="sxs-lookup"><span data-stu-id="95db4-137">Button</span></span></th>
<th align="left"><span data-ttu-id="95db4-138">효과</span><span class="sxs-lookup"><span data-stu-id="95db4-138">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-139">Add</span><span class="sxs-lookup"><span data-stu-id="95db4-139">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-140">보안 설명자에 새 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-140">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="95db4-141">Active Directory의 모든 사용자 또는 그룹을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-141">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="95db4-142">제거</span><span class="sxs-lookup"><span data-stu-id="95db4-142">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-143">선택 된 항목을 액세스 제어 목록에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-143">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95db4-144">특성</span><span class="sxs-lookup"><span data-stu-id="95db4-144">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-145">선택한 개체의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95db4-145">Display the properties for the selected object.</span></span> <span data-ttu-id="95db4-146">속성 페이지는 <strong> Active Directory 사용자 및 컴퓨터의 개체에 대해 표시 되는 것과 동일 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="95db4-146">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="95db4-147">고급</span><span class="sxs-lookup"><span data-stu-id="95db4-147">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="95db4-148"><strong>액세스 제어 목록 편집기를 엽니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="95db4-148">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="95db4-149">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="95db4-149">Additional considerations</span></span>

-   <span data-ttu-id="95db4-150">특정 작업과 관련 된 역할 및 권한에 대 한 자세한 내용은 [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks-agpm40.md), [편집자 작업](performing-editor-tasks-agpm40.md)수행, [승인자 작업 수행](performing-approver-tasks-agpm40.md), [검토자 작업 수행](performing-reviewer-tasks-agpm40.md)의 작업을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95db4-150">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="95db4-151">추가 참조</span><span class="sxs-lookup"><span data-stu-id="95db4-151">Additional references</span></span>

-   [<span data-ttu-id="95db4-152">내용 탭</span><span class="sxs-lookup"><span data-stu-id="95db4-152">Contents Tab</span></span>](contents-tab-agpm40.md)

 

 





