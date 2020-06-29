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
# <span data-ttu-id="bda42-103">일반적인 보조 탭 기능</span><span class="sxs-lookup"><span data-stu-id="bda42-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="bda42-104">각 보조 탭에는**그룹 정책 개체** 및 **그룹과 사용자**라는 두 가지 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="bda42-105">그룹 정책 개체 섹션</span><span class="sxs-lookup"><span data-stu-id="bda42-105">Group Policy objects section</span></span>


<span data-ttu-id="bda42-106">**그룹 정책 개체** 섹션에는 Gpo (그룹 정책 개체)의 필터링 된 목록이 표시 되며 각 gpo에 대 한 다음 특성을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bda42-107">GPO 특성</span><span class="sxs-lookup"><span data-stu-id="bda42-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="bda42-108">설명</span><span class="sxs-lookup"><span data-stu-id="bda42-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bda42-109">이름</span><span class="sxs-lookup"><span data-stu-id="bda42-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-110">그룹 정책 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bda42-111">컴퓨터 (Comp.)</span><span class="sxs-lookup"><span data-stu-id="bda42-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-112">GPO의 컴퓨터 구성 부분에 대 한 버전을 자동으로 생성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bda42-113">사용자</span><span class="sxs-lookup"><span data-stu-id="bda42-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-114">GPO의 사용자 구성 부분에 대 한 자동 생성 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bda42-115">시</span><span class="sxs-lookup"><span data-stu-id="bda42-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-116">선택한 GPO의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="bda42-117">미제어: </strong> AGPM에서 관리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="bda42-118">체크 인: </strong> 권한이 있는 편집기에서 편집을 확인 하거나 그룹 정책 관리자가 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="bda42-119">체크 아웃 됨: </strong> 현재 편집 중입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="bda42-120">체크 아웃 하거나 AGPM 관리자가 확인 한 편집기에서 체크 아웃할 때까지 다른 편집기에서이를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="bda42-121">보류 중: </strong> 그룹 정책 관리자가 만들거나, 제어 하거나, 배포 하거나, 삭제 하기 전에 승인을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="bda42-122">삭제 됨: </strong> 보관에서 삭제 되지만 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="bda42-123">서식 파일: </strong> 새 gpo를 만들 때 시작 점으로 사용할 GPO의 정적 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="bda42-124">서식 파일 (기본값): </strong> 이 서식 파일은 기본적으로 새 GPO를 만들 때 사용 되는 시작 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bda42-125">GPO 상태</span><span class="sxs-lookup"><span data-stu-id="bda42-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-126">컴퓨터 구성과 사용자 구성을 개별적으로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="bda42-127">GPO 상태는 사용할 수 있는 GPO의 일부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bda42-128">WMI 필터</span><span class="sxs-lookup"><span data-stu-id="bda42-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-129">이 GPO에 적용 된 WMI 필터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="bda42-130">WMI 필터는 <strong> </strong> GPMC 콘솔 트리의 도메인에 대 한 wmi 필터 노드에서 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bda42-131">수정됨</span><span class="sxs-lookup"><span data-stu-id="bda42-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-132">제어 된 GPO의 경우, 수정 또는 체크 아웃 한 후에 체크 인 되는 가장 최근 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="bda42-133">미제어 GPO의 경우 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bda42-134">소유자</span><span class="sxs-lookup"><span data-stu-id="bda42-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-135">체크 인 한 편집기나 선택한 GPO를 배포한 승인자</span><span class="sxs-lookup"><span data-stu-id="bda42-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bda42-136">그룹 및 사용자 섹션</span><span class="sxs-lookup"><span data-stu-id="bda42-136">Groups and Users section</span></span>


<span data-ttu-id="bda42-137">GPO를 선택 하면 **그룹 및 사용자** 섹션에는 해당 gpo에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="bda42-138">각 그룹 또는 사용자에 대해 허용 된 사용 권한 및 상속이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="bda42-139">AGPM 관리자는 표준 AGPM 역할 (편집기, 승인자 및 검토자) 또는 사용자 지정 된 사용 권한 조합을 사용 하 여 사용 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bda42-140">단추</span><span class="sxs-lookup"><span data-stu-id="bda42-140">Button</span></span></th>
<th align="left"><span data-ttu-id="bda42-141">효과</span><span class="sxs-lookup"><span data-stu-id="bda42-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bda42-142">Add</span><span class="sxs-lookup"><span data-stu-id="bda42-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-143">보안 설명자에 새 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="bda42-144">Active Directory의 모든 사용자 또는 그룹을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bda42-145">제거</span><span class="sxs-lookup"><span data-stu-id="bda42-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-146">선택 된 항목을 액세스 제어 목록에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bda42-147">특성</span><span class="sxs-lookup"><span data-stu-id="bda42-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-148">선택한 개체의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bda42-148">Display the properties for the selected object.</span></span> <span data-ttu-id="bda42-149">속성 페이지는 <strong> Active Directory 사용자 및 컴퓨터의 개체에 대해 표시 되는 것과 동일 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="bda42-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bda42-150">고급</span><span class="sxs-lookup"><span data-stu-id="bda42-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bda42-151"><strong>액세스 제어 목록 편집기를 엽니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="bda42-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="bda42-152">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="bda42-152">Additional considerations</span></span>

-   <span data-ttu-id="bda42-153">특정 작업과 관련 된 역할 및 권한에 대 한 자세한 내용은 [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks.md), [편집자 작업](performing-editor-tasks.md)수행, [승인자 작업 수행](performing-approver-tasks.md), [검토자 작업 수행](performing-reviewer-tasks.md)의 작업을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bda42-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="bda42-154">추가 참조</span><span class="sxs-lookup"><span data-stu-id="bda42-154">Additional references</span></span>

-   [<span data-ttu-id="bda42-155">내용 탭</span><span class="sxs-lookup"><span data-stu-id="bda42-155">Contents Tab</span></span>](contents-tab.md)

 

 





