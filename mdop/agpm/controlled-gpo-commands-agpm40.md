---
title: 제어된 GPO 명령
description: 제어된 GPO 명령
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821118"
---
# <span data-ttu-id="5abe2-103">제어된 GPO 명령</span><span class="sxs-lookup"><span data-stu-id="5abe2-103">Controlled GPO Commands</span></span>


<span data-ttu-id="5abe2-104">**제어** 탭:</span><span class="sxs-lookup"><span data-stu-id="5abe2-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="5abe2-105">AGPM (고급 그룹 정책 관리)에서 관리 하는 Gpo (그룹 정책 개체) 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="5abe2-106">Gpo를 관리 하 고 Gpo에 대 한 기록 및 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="5abe2-107">선택한 GPO에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="5abe2-108">이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 바로 가기 메뉴가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu.</span></span> <span data-ttu-id="5abe2-109">이 메뉴에는 다음 중 해당 되는 옵션이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-109">This menu includes whichever of the following options are applicable.</span></span>

## <span data-ttu-id="5abe2-110">제어 및 기록</span><span class="sxs-lookup"><span data-stu-id="5abe2-110">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5abe2-111">명령</span><span class="sxs-lookup"><span data-stu-id="5abe2-111">Command</span></span></th>
<th align="left"><span data-ttu-id="5abe2-112">효과</span><span class="sxs-lookup"><span data-stu-id="5abe2-112">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-113">새로운 제어 된 GPO</span><span class="sxs-lookup"><span data-stu-id="5abe2-113">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-114">AGPM에서 관리 되는 변경 컨트롤이 있는 새 GPO를 만들고이를 도메인의 프로덕션 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-114">Create a new GPO with change control managed through AGPM and deploy it to the production environment of the domain.</span></span> <span data-ttu-id="5abe2-115">GPO를 만들 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-115">If you do not have permission to create a GPO, you are prompted to submit a request.</span></span> <span data-ttu-id="5abe2-116">(이 옵션은 다음을 마우스 오른쪽 단추로 클릭할 <strong> 때 GPO가 선택 되어 있지 않은 경우 표시 됩니다. 그룹 정책 개체 </strong> 목록.</span><span class="sxs-lookup"><span data-stu-id="5abe2-116">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-117">기록</span><span class="sxs-lookup"><span data-stu-id="5abe2-117">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-118">보관 함에 저장 된 선택한 GPO의 모든 버전이 나열 된 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-118">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="5abe2-119">기록에서 GPO 내의 설정에 대 한 보고서를 얻고, 두 버전의 GPO를 비교 하거나, GPO를 서식 파일과 비교 하거나, 이전 버전의 GPO로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-119">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5abe2-120">보고</span><span class="sxs-lookup"><span data-stu-id="5abe2-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5abe2-121">명령</span><span class="sxs-lookup"><span data-stu-id="5abe2-121">Command</span></span></th>
<th align="left"><span data-ttu-id="5abe2-122">효과</span><span class="sxs-lookup"><span data-stu-id="5abe2-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-123">설정</span><span class="sxs-lookup"><span data-stu-id="5abe2-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-124">선택한 GPO 내의 설정을 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 하거나 GPO (들)가 최근에 제어, 가져오기 또는 체크 인 되었을 때의 조직 구성 단위에서 선택한 GPO에 대 한 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-125">차이점</span><span class="sxs-lookup"><span data-stu-id="5abe2-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-126">선택한 두 Gpo 내의 설정과 선택한 GPO 및 서식 파일을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5abe2-127">편집</span><span class="sxs-lookup"><span data-stu-id="5abe2-127">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5abe2-128">명령</span><span class="sxs-lookup"><span data-stu-id="5abe2-128">Command</span></span></th>
<th align="left"><span data-ttu-id="5abe2-129">효과</span><span class="sxs-lookup"><span data-stu-id="5abe2-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-130">Edit</span><span class="sxs-lookup"><span data-stu-id="5abe2-130">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-131"><strong>그룹 정책 관리 편집기 창을 열어 </strong> 선택한 GPO를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-131">Open the <strong>Group Policy Management Editor</strong> window to change the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-132">체크 아웃</span><span class="sxs-lookup"><span data-stu-id="5abe2-132">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-133">오프 라인으로 편집할 수 있도록 보관 저장소에서 선택한 GPO 복사본을 가져와 보관 저장소에 다시 체크 인 될 때까지 다른 사람이 GPO를 편집 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-133">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing the GPO until it is checked back into the archive.</span></span> <span data-ttu-id="5abe2-134">체크 아웃은 AGPM 관리자 (모든 권한)에 의해 재정의 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-134">Check Out can be overridden by an AGPM Administrator (Full Control).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-135">체크인</span><span class="sxs-lookup"><span data-stu-id="5abe2-135">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-136">다른 승인 된 편집기에서 변경 하거나 승인자가 GPO를 도메인의 프로덕션 환경에 배포할 수 있도록 선택한 GPO의 편집 된 버전을 보관 함에 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-136">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy the GPO to the production environment of the domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-137">체크 아웃 취소</span><span class="sxs-lookup"><span data-stu-id="5abe2-137">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-138">체크 아웃 된 GPO를 변경 하지 않고 보관 함으로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-138">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5abe2-139">버전 관리</span><span class="sxs-lookup"><span data-stu-id="5abe2-139">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5abe2-140">명령</span><span class="sxs-lookup"><span data-stu-id="5abe2-140">Command</span></span></th>
<th align="left"><span data-ttu-id="5abe2-141">효과</span><span class="sxs-lookup"><span data-stu-id="5abe2-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-142">프로덕션에서 가져오기</span><span class="sxs-lookup"><span data-stu-id="5abe2-142">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-143">선택한 GPO에 대해 도메인의 프로덕션 환경에 있는 버전을 보관에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-143">For the selected GPO, copy the version in the production environment of the domain to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-144">파일에서 가져오기</span><span class="sxs-lookup"><span data-stu-id="5abe2-144">Import from File</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-145">선택한 체크 아웃 된 GPO의 정책 설정을 GPO 백업 파일에서 해당 설정으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-145">Replace the policy settings of the selected, checked-out GPO with those from a GPO backup file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-146">삭제</span><span class="sxs-lookup"><span data-stu-id="5abe2-146">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-147">선택한 GPO를 휴지통으로 이동 하 고 배포 된 버전 (있는 경우)을 프로덕션에 남길 것인지 아니면 아카이브의 버전 외에 배포 된 버전을 삭제할지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-147">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete the deployed version in addition to the version in the archive.</span></span> <span data-ttu-id="5abe2-148">GPO를 삭제할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-148">If you do not have permission to delete a GPO, you are prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-149">배포</span><span class="sxs-lookup"><span data-stu-id="5abe2-149">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-150">선택한 GPO를 보관 함으로 체크 인 한 도메인의 프로덕션 환경으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-150">Move the selected GPO that is checked into the archive to the production environment of the domain.</span></span> <span data-ttu-id="5abe2-151">이 작업을 수행 하면 네트워크에서 활성화 되 고 이전에 GPO의 활성 버전 (있는 경우)이 덮어써집니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-151">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="5abe2-152">GPO를 배포할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-152">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-153">다음으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="5abe2-153">Export to</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-154">선택한 GPO를 다른 도메인에 복사할 수 있도록 백업 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-154">Save the selected GPO to a backup file so that you can copy it to another domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-155">Label</span><span class="sxs-lookup"><span data-stu-id="5abe2-155">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-156">선택한 GPO에 설명 레이블 (예: &quot; 알려진 양호한 &quot; 레코드)과 기록 유지에 대 한 설명을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-156">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="5abe2-157">레이블은 <strong> 상태 열에 나타나며 </strong> <strong> 기록 창의 메모 열에 메모를 표시 </strong> <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-157">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window.</span></span> <span data-ttu-id="5abe2-158">또한 문제가 발생 하는 경우 롤백할 수 있도록 이전 버전의 GPO를 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-158">They help you identify earlier versions of a GPO so that you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-159">Rename</span><span class="sxs-lookup"><span data-stu-id="5abe2-159">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-160">선택한 GPO의 이름을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-160">Change the name of the selected GPO.</span></span> <span data-ttu-id="5abe2-161">GPO가 이미 배포 된 경우 GPO를 재배포 하면 도메인의 프로덕션 환경에서 이름이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-161">If the GPO has already been deployed, the name will be updated in the production environment of the domain when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-162">서식 파일로 저장</span><span class="sxs-lookup"><span data-stu-id="5abe2-162">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-163">선택한 GPO의 설정을 기반으로 새 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-163">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5abe2-164">기타</span><span class="sxs-lookup"><span data-stu-id="5abe2-164">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5abe2-165">명령</span><span class="sxs-lookup"><span data-stu-id="5abe2-165">Command</span></span></th>
<th align="left"><span data-ttu-id="5abe2-166">효과</span><span class="sxs-lookup"><span data-stu-id="5abe2-166">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5abe2-167">새로 고침</span><span class="sxs-lookup"><span data-stu-id="5abe2-167">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-168">변경 내용을 통합 하기 위해 GPMC (그룹 정책 관리) 콘솔의 표시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-168">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="5abe2-169">일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-169">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5abe2-170">Help</span><span class="sxs-lookup"><span data-stu-id="5abe2-170">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5abe2-171">AGPM에 대 한 도움말을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5abe2-171">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5abe2-172">추가 참조</span><span class="sxs-lookup"><span data-stu-id="5abe2-172">Additional references</span></span>

-   [<span data-ttu-id="5abe2-173">내용 탭</span><span class="sxs-lookup"><span data-stu-id="5abe2-173">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="5abe2-174">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="5abe2-174">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="5abe2-175">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="5abe2-175">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="5abe2-176">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="5abe2-176">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





