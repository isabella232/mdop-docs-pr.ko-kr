---
title: 템플릿 명령
description: 템플릿 명령
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820183"
---
# <span data-ttu-id="cfb3e-103">템플릿 명령</span><span class="sxs-lookup"><span data-stu-id="cfb3e-103">Template Commands</span></span>


<span data-ttu-id="cfb3e-104">**서식 파일** 탭:</span><span class="sxs-lookup"><span data-stu-id="cfb3e-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="cfb3e-105">새 Gpo (그룹 정책 개체)를 만드는 데 사용할 수 있는 사용 가능한 서식 파일 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-105">Displays a list of available templates that you can use to create new Group Policy Objects (GPOs).</span></span>

-   <span data-ttu-id="cfb3e-106">선택한 서식 파일을 기반으로 GPO를 만들고 서식 파일을 관리 하 고 서식 파일에 대 한 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="cfb3e-107">선택한 서식 파일에 액세스할 수 있는 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="cfb3e-108">서식 파일을 변경할 수 없기 때문에 서식 파일에는 기록이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="cfb3e-109">그러나 GPO 버전과 마찬가지로 서식 파일의 설정을 설정 보고서와 함께 표시 하거나 차이점 보고서를 사용 하 여 다른 GPO와 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="cfb3e-110">**참고**  서식 파일은 편집 가능한 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="cfb3e-111">이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 다음 중 해당 되는 옵션을 비롯 한 바로 가기 메뉴가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="cfb3e-112">컨트롤</span><span class="sxs-lookup"><span data-stu-id="cfb3e-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cfb3e-113">명령</span><span class="sxs-lookup"><span data-stu-id="cfb3e-113">Command</span></span></th>
<th align="left"><span data-ttu-id="cfb3e-114">효과</span><span class="sxs-lookup"><span data-stu-id="cfb3e-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cfb3e-115">새로운 제어 된 GPO</span><span class="sxs-lookup"><span data-stu-id="cfb3e-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-116">선택한 서식 파일을 기반으로 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="cfb3e-117">새 GPO를 프로덕션 환경에 배포 하는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-117">The option to deploy the new GPO to the production environment is provided.</span></span> <span data-ttu-id="cfb3e-118">GPO를 만들 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="cfb3e-119">(이 옵션은 다음을 마우스 오른쪽 단추로 클릭할 <strong> 때 GPO가 선택 되어 있지 않은 경우 표시 됩니다. 그룹 정책 개체 </strong> 목록.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="cfb3e-120">보고</span><span class="sxs-lookup"><span data-stu-id="cfb3e-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cfb3e-121">명령</span><span class="sxs-lookup"><span data-stu-id="cfb3e-121">Command</span></span></th>
<th align="left"><span data-ttu-id="cfb3e-122">효과</span><span class="sxs-lookup"><span data-stu-id="cfb3e-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cfb3e-123">설정</span><span class="sxs-lookup"><span data-stu-id="cfb3e-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-124">선택한 GPO 내의 설정을 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cfb3e-125">차이점</span><span class="sxs-lookup"><span data-stu-id="cfb3e-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-126">두 개의 선택한 GPO 템플릿 내의 설정을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="cfb3e-127">서식 파일 관리</span><span class="sxs-lookup"><span data-stu-id="cfb3e-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cfb3e-128">명령</span><span class="sxs-lookup"><span data-stu-id="cfb3e-128">Command</span></span></th>
<th align="left"><span data-ttu-id="cfb3e-129">효과</span><span class="sxs-lookup"><span data-stu-id="cfb3e-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cfb3e-130">기본값으로 설정</span><span class="sxs-lookup"><span data-stu-id="cfb3e-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-131">선택한 서식 파일을 새 GPO를 만들 때 자동으로 사용할 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cfb3e-132">삭제</span><span class="sxs-lookup"><span data-stu-id="cfb3e-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-133">선택한 서식 파일을 휴지통으로 이동 <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="cfb3e-134">GPO를 삭제할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cfb3e-135">Rename</span><span class="sxs-lookup"><span data-stu-id="cfb3e-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-136">선택한 서식 파일의 이름을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="cfb3e-137">기타</span><span class="sxs-lookup"><span data-stu-id="cfb3e-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cfb3e-138">명령</span><span class="sxs-lookup"><span data-stu-id="cfb3e-138">Command</span></span></th>
<th align="left"><span data-ttu-id="cfb3e-139">효과</span><span class="sxs-lookup"><span data-stu-id="cfb3e-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cfb3e-140">새로 고침</span><span class="sxs-lookup"><span data-stu-id="cfb3e-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-141">변경 내용을 통합 하도록 그룹 정책 관리 콘솔의 표시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="cfb3e-142">일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cfb3e-143">Help</span><span class="sxs-lookup"><span data-stu-id="cfb3e-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cfb3e-144">AGPM (고급 그룹 정책 관리)에 대 한 도움말을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb3e-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="cfb3e-145">추가 참조</span><span class="sxs-lookup"><span data-stu-id="cfb3e-145">Additional references</span></span>

-   [<span data-ttu-id="cfb3e-146">내용 탭</span><span class="sxs-lookup"><span data-stu-id="cfb3e-146">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="cfb3e-147">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="cfb3e-147">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="cfb3e-148">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="cfb3e-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





