---
title: 보고서를 생성하는 방법
description: 보고서를 생성하는 방법
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826993"
---
# <span data-ttu-id="04b2d-103">보고서를 생성하는 방법</span><span class="sxs-lookup"><span data-stu-id="04b2d-103">How to Generate Reports</span></span>


<span data-ttu-id="04b2d-104">MED-V의 관리자는 다음 보고서 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="04b2d-105">[상태 (status](#bkmk-generatingastatusreport))-상태 보고서를 사용 하 여 지정 된 기간을 기준으로 각 사용자의 모든 활성 사용자 및 모든 med-v 작업 영역의 현재 상태를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="04b2d-106">여기에는 현재 서버에 연결 되어 있는 컴퓨터를 보거나, 현재 연결 되어 있지 않은 경우, 서버에 마지막으로 연결 된 날짜와 시간, 각 컴퓨터의 상태, 기타 관련 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="04b2d-107">[활동 로그](#bkmk-generatinganactivitylogreport)-이 보고서를 사용 하 여 정의 된 날짜 범위에서 특정 호스트 또는 사용자가 생성 한 이벤트를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="04b2d-108">[오류 로그](#bkmk-generatinganerrorlogreport)-이 보고서를 사용 하 여 정의 된 날짜 범위에서 특정 호스트 또는 사용자가 생성 한 오류를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="04b2d-109">적절 한 열 이름을 클릭 하 여 열을 기준으로 보고서 결과를 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="04b2d-110">보고서 결과는 열 머리글을 보고서의 맨 위로 끌어 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="04b2d-111">여러 열 머리글을 끌어 한 열 뒤에 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="04b2d-112">상태 보고서를 생성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="04b2d-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="04b2d-113">상태 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="04b2d-113">To generate a status report</span></span>**

1.  <span data-ttu-id="04b2d-114">**보고서** 관리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="04b2d-115">**보고서 모듈의** **보고서 형식** 메뉴에서 **상태**를 선택 하 고 **생성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="04b2d-116">보고서 매개 변수 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="04b2d-117">**보고서 매개 변수** 대화 상자의 **일 수** 필드에 숫자를 입력 하거나 화살표를 사용 하 여 상황 보고서에 포함할 일 수를 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="04b2d-118">상태 보고서가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-118">A status report is generated.</span></span> <span data-ttu-id="04b2d-119">보고서 매개 변수는 다음 표에 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="04b2d-120">클라이언트 MED-V 작업 영역 속성</span><span class="sxs-lookup"><span data-stu-id="04b2d-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04b2d-121">속성</span><span class="sxs-lookup"><span data-stu-id="04b2d-121">Property</span></span></th>
<th align="left"><span data-ttu-id="04b2d-122">설명</span><span class="sxs-lookup"><span data-stu-id="04b2d-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-123">시간</span><span class="sxs-lookup"><span data-stu-id="04b2d-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-124">이벤트가 발생 한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04b2d-125">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-125">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-126">기본적으로 이벤트는 내림차순 날짜 순서로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="04b2d-127">그러나 받은 시간 열을 클릭 하 여 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-128">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-129">이벤트를 시작한 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04b2d-130">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-130">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-131">사용자가 로그온 하기 전에 이벤트가 발생 한 경우 사용자 이름은 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-132">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-133">호스트 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-134">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-135">MED-V 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-136">작업 영역 컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-137">MED-V 작업 영역이 실행 되는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-138">온라인</span><span class="sxs-lookup"><span data-stu-id="04b2d-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-139">클라이언트 컴퓨터의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="04b2d-140">멈추었습니다</span><span class="sxs-lookup"><span data-stu-id="04b2d-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04b2d-141">&lt;작업 영역이 시작 된 날짜 및 시간에 시작 됨&gt;</span><span class="sxs-lookup"><span data-stu-id="04b2d-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-142">클라이언트 버전</span><span class="sxs-lookup"><span data-stu-id="04b2d-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-143">클라이언트의 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-144">정책 버전</span><span class="sxs-lookup"><span data-stu-id="04b2d-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-145">MED-V 작업 영역이 현재 사용 중인 정책 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-146">이미지 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-147">이미지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-148">이미지 버전</span><span class="sxs-lookup"><span data-stu-id="04b2d-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-149">MED-V 작업 영역이 현재 사용 중인 이미지 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04b2d-150">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-150">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-151">컴퓨터에 아직 다운로드 하지 않은 경우 MED-V 작업 영역 버전을 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="04b2d-152">활동 로그 보고서를 생성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="04b2d-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="04b2d-153">활동 로그 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="04b2d-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="04b2d-154">**보고서** 관리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="04b2d-155">보고서 모듈이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="04b2d-156">**보고서 모듈의** **보고서 형식** 메뉴에서 **활동 로그**를 선택 하 고 **생성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="04b2d-157">**보고서 매개 변수** 대화 상자에서 다음 매개 변수 중 하나 이상을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="04b2d-158">**일 수**-보고서에 표시할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="04b2d-159">**사용자 이름 포함**-입력 된 텍스트를 포함 하는 사용자 이름이 보고서에 포함 된 경우 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="04b2d-160">**호스트 이름에**는 호스트 이름에 입력 된 텍스트가 포함 된 모든 이벤트가 보고서에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="04b2d-161">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-161">Click **OK**.</span></span>

    <span data-ttu-id="04b2d-162">이벤트 및 날짜가 선택 된 상태로 보고서가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="04b2d-163">보고서 매개 변수는 다음 표에 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="04b2d-164">활동 로그 보고서 속성</span><span class="sxs-lookup"><span data-stu-id="04b2d-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04b2d-165">속성</span><span class="sxs-lookup"><span data-stu-id="04b2d-165">Property</span></span></th>
<th align="left"><span data-ttu-id="04b2d-166">설명</span><span class="sxs-lookup"><span data-stu-id="04b2d-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-167">이벤트 ID</span><span class="sxs-lookup"><span data-stu-id="04b2d-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-168">이벤트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-169">심각도</span><span class="sxs-lookup"><span data-stu-id="04b2d-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="04b2d-170">정보, 오류, 경고</span><span class="sxs-lookup"><span data-stu-id="04b2d-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-171">범주</span><span class="sxs-lookup"><span data-stu-id="04b2d-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-172">보고서가 참조 하는 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-173">설명</span><span class="sxs-lookup"><span data-stu-id="04b2d-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-174">이벤트에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-175">수신 시간</span><span class="sxs-lookup"><span data-stu-id="04b2d-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-176">서버에서 이벤트를 받은 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04b2d-177">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-177">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-178">클라이언트가 오프 라인으로 작업 하는 경우 서버는 클라이언트가 온라인 상태일 때 보고서를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="04b2d-179">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-179">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-180">기본적으로 이벤트는 내림차순 날짜 순서로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="04b2d-181">그러나 받은 시간 열을 클릭 하 여 변경할 수 있습니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="04b2d-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-182">클라이언트 시간</span><span class="sxs-lookup"><span data-stu-id="04b2d-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-183">클라이언트 시계에 따라 이벤트가 발생 한 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-184">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-185">호스트 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-186">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-187">이벤트를 시작한 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-188">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-189">MED-V 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-190">작업 영역 컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-191">MED-V 작업 영역이 실행 되는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="04b2d-192">오류 로그 보고서를 생성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="04b2d-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="04b2d-193">오류 로그 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="04b2d-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="04b2d-194">**보고서** 관리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="04b2d-195">**보고서 모듈의** **보고서 유형** 메뉴에서 **오류 로그**를 선택 하 고 **생성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="04b2d-196">**보고서 매개 변수** 대화 상자에서 다음 매개 변수 중 하나 이상을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="04b2d-197">**일 수**-보고서에 표시할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="04b2d-198">**사용자 이름 포함**-입력 된 텍스트를 포함 하는 사용자 이름이 보고서에 포함 된 경우 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="04b2d-199">**호스트 이름에**는 호스트 이름에 입력 된 텍스트가 포함 된 모든 이벤트가 보고서에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="04b2d-200">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-200">Click **OK**.</span></span>

    <span data-ttu-id="04b2d-201">이벤트 및 날짜가 선택 된 상태로 보고서가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="04b2d-202">보고서 매개 변수는 다음 표에 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="04b2d-203">오류 로그 보고서 속성</span><span class="sxs-lookup"><span data-stu-id="04b2d-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04b2d-204">속성</span><span class="sxs-lookup"><span data-stu-id="04b2d-204">Property</span></span></th>
<th align="left"><span data-ttu-id="04b2d-205">설명</span><span class="sxs-lookup"><span data-stu-id="04b2d-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-206">이벤트 ID</span><span class="sxs-lookup"><span data-stu-id="04b2d-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-207">이벤트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-208">범주</span><span class="sxs-lookup"><span data-stu-id="04b2d-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-209">보고서가 참조 하는 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-210">설명</span><span class="sxs-lookup"><span data-stu-id="04b2d-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-211">이벤트에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-212">수신 시간</span><span class="sxs-lookup"><span data-stu-id="04b2d-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-213">서버에서 이벤트를 받은 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04b2d-214">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-214">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-215">클라이언트가 오프 라인으로 작업 하는 경우 서버는 클라이언트가 온라인 상태일 때 보고서를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="04b2d-216">참고</span><span class="sxs-lookup"><span data-stu-id="04b2d-216">Note</span></span></strong><br/><p><span data-ttu-id="04b2d-217">기본적으로 이벤트는 내림차순 날짜 순서로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="04b2d-218">그러나 받은 시간 열을 클릭 하 여 변경할 수 있습니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="04b2d-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-219">클라이언트 시간</span><span class="sxs-lookup"><span data-stu-id="04b2d-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-220">클라이언트 시계에 따라 이벤트가 발생 한 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-221">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-222">호스트 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04b2d-223">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-224">이벤트를 시작한 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04b2d-225">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="04b2d-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="04b2d-226">MED-V 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04b2d-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











