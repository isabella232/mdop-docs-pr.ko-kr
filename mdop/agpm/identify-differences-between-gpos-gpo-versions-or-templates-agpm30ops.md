---
title: GPO, GPO 버전 또는 템플릿 간의 차이점 식별
description: GPO, GPO 버전 또는 템플릿 간의 차이점 식별
author: dansimp
ms.assetid: e391fa91-3956-4150-9d43-900cfc88d543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88c37a3723c31fb110e731084237a8d89350a4ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820773"
---
# <span data-ttu-id="2aff3-103">GPO, GPO 버전 또는 템플릿 간의 차이점 식별</span><span class="sxs-lookup"><span data-stu-id="2aff3-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="2aff3-104">Gpo (그룹 정책 개체), 템플릿 또는 GPO의 다른 버전 간의 차이점을 분석 하는 HTML 기반 차이점 보고서를 생성 하거나 XML 기반 차이를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy Objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="2aff3-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에 대 한 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="2aff3-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="2aff3-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="2aff3-107">Gpo, GPO 버전 또는 템플릿의 차이점 확인</span><span class="sxs-lookup"><span data-stu-id="2aff3-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="2aff3-108">두 개의 Gpo 또는 템플릿 간에</span><span class="sxs-lookup"><span data-stu-id="2aff3-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="2aff3-109">GPO와 서식 파일 간</span><span class="sxs-lookup"><span data-stu-id="2aff3-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="2aff3-110">한 GPO의 두 버전 사이</span><span class="sxs-lookup"><span data-stu-id="2aff3-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="2aff3-111">GPO 버전과 서식 파일 간에</span><span class="sxs-lookup"><span data-stu-id="2aff3-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="2aff3-112">두 Gpo 또는 템플릿 간의 차이점을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="2aff3-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="2aff3-113">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2aff3-114">세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="2aff3-115">두 개의 Gpo 또는 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="2aff3-116">Gpo 또는 서식 파일 중 하나를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo 또는 템플릿의 설정을 요약 한 차이점 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="2aff3-117">GPO와 서식 파일 간의 차이점을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="2aff3-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="2aff3-118">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2aff3-119">세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="2aff3-120">GPO를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **서식 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="2aff3-121">서식 파일과 보고서 유형을 선택한 다음 **확인** 을 클릭 하 여 GPO 및 템플릿의 설정을 요약 하는 차이점 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="2aff3-122">한 GPO의 두 버전 간의 차이점을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="2aff3-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="2aff3-123">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2aff3-124">세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="2aff3-125">GPO를 두 번 클릭 하 여 기록을 표시 한 다음 비교할 버전을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="2aff3-126">버전 중 하나를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo의 설정을 요약 하는 차이점 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="2aff3-127">GPO 버전과 서식 파일 간의 차이점을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="2aff3-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="2aff3-128">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2aff3-129">세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo (또는 두 개의 템플릿을 비교 하는 경우 서식 파일)를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="2aff3-130">해당 GPO를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="2aff3-131">원하는 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 클릭 한 다음 **서식 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="2aff3-132">서식 파일 및 보고서 유형을 선택 하 고 **확인** 을 클릭 하 여 GPO 버전 및 템플릿의 설정을 요약 하는 차이점 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="2aff3-133">차이점 보고서에 대 한 주요 정보</span><span class="sxs-lookup"><span data-stu-id="2aff3-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2aff3-134">기호</span><span class="sxs-lookup"><span data-stu-id="2aff3-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="2aff3-135">의미</span><span class="sxs-lookup"><span data-stu-id="2aff3-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="2aff3-136">색상</span><span class="sxs-lookup"><span data-stu-id="2aff3-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2aff3-137">없음</span><span class="sxs-lookup"><span data-stu-id="2aff3-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="2aff3-138">두 Gpo에 동일한 설정이 있는 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="2aff3-139">수준에 따라 다름</span><span class="sxs-lookup"><span data-stu-id="2aff3-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2aff3-140">[#]</span><span class="sxs-lookup"><span data-stu-id="2aff3-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2aff3-141">항목이 두 Gpo에 모두 있지만 변경 된 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="2aff3-142">화면이</span><span class="sxs-lookup"><span data-stu-id="2aff3-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2aff3-143">[-]</span><span class="sxs-lookup"><span data-stu-id="2aff3-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2aff3-144">항목이 첫 번째 GPO에만 있음</span><span class="sxs-lookup"><span data-stu-id="2aff3-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="2aff3-145">빨간색</span><span class="sxs-lookup"><span data-stu-id="2aff3-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2aff3-146">[+]</span><span class="sxs-lookup"><span data-stu-id="2aff3-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2aff3-147">두 번째 GPO에만 항목이 있음</span><span class="sxs-lookup"><span data-stu-id="2aff3-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="2aff3-148">녹색</span><span class="sxs-lookup"><span data-stu-id="2aff3-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="2aff3-149">설정이 변경 된 항목의 경우 항목을 확장할 때 변경 된 설정이 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="2aff3-150">각 GPO의 특성 값은 Gpo가 보고서에 표시 되는 순서 대로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="2aff3-151">일부 설정이 변경 되 면 항목이 두 개의 다른 항목 (첫 번째 GPO에만 표시 되며 변경 된 항목이 하나가 아닌 두 개에만 표시 됨)으로 보고 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="2aff3-152">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="2aff3-152">Additional considerations</span></span>

-   <span data-ttu-id="2aff3-153">이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2aff3-154">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="2aff3-155">또한 Gpo 목록을 표시 하려면 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aff3-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="2aff3-156">추가 참조</span><span class="sxs-lookup"><span data-stu-id="2aff3-156">Additional references</span></span>

-   [<span data-ttu-id="2aff3-157">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="2aff3-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





