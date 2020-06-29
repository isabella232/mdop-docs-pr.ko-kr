---
title: 응용 프로그램 라이선스 노드
description: 응용 프로그램 라이선스 노드
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819513"
---
# <span data-ttu-id="adcbb-103">응용 프로그램 라이선스 노드</span><span class="sxs-lookup"><span data-stu-id="adcbb-103">Applications Licenses Node</span></span>


<span data-ttu-id="adcbb-104">응용 프로그램 **라이선스** 노드는 응용 프로그램 가상화 서버 관리 콘솔의 **범위** 창에서 응용 프로그램 가상화 시스템 노드 보다 한 수준 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="adcbb-105">이 노드를 선택 하면 **결과** 창에 라이선스 및 라이선스 그룹 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="adcbb-106">다음 라이선스 유형을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-106">The following license types are available:</span></span>

-   <span data-ttu-id="adcbb-107">**무제한 라이선스**– 동시 사용자 수에 대 한 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="adcbb-108">이 라이선스 방법은 엔터프라이즈 차원의 라이선스를 응용 프로그램과 연결 하려는 경우에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="adcbb-109">**동시 라이선스**-응용 프로그램을 사용할 수 있는 최대 동시 사용자 수를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="adcbb-110">**라이선스 명명**— 개별 사용자에 게 라이선스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="adcbb-111">명명 된 라이선스를 사용 하 여 특정 사용자가 항상 응용 프로그램을 실행할 수 있도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="adcbb-112">**참고**  동일한 응용 프로그램에 대해 동시 및 명명 된 라이선스를 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="adcbb-113">**응용 프로그램 라이선스** 노드를 마우스 오른쪽 단추로 클릭 하 여 다음 요소를 포함 하는 팝업 메뉴를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="adcbb-114">새로운 무제한 라이선스</span><span class="sxs-lookup"><span data-stu-id="adcbb-114">New Unlimited License</span></span>**  
<span data-ttu-id="adcbb-115">새로운 무제한 라이선스 마법사를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="adcbb-116">이 마법사는 다음 페이지로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="adcbb-117">**응용 프로그램 라이선스 그룹 이름** 필드에 라이선스 그룹의 이름을 입력 하 고 **라이선스 만료 경고** 필드에 값 (분)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="adcbb-118">(0 ~ 100의 값을 입력할 수 있습니다.) 위쪽 및 아래 화살표 키를 사용 하 여 분 수를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="adcbb-119">**라이선스 설명** 필드에 간단한 설명 텍스트를 입력 하 고 **사용** 확인란을 선택 하 여 라이선스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="adcbb-120">필요에 따라 **만료 날짜** 필드를 사용 하 여 라이선스의 만료 날짜를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="adcbb-121">확인란을 선택 하 여 표시 된 만료 날짜를 사용 하거나 달력 유틸리티를 사용 하 여 원하는 만료 날짜를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="adcbb-122">**마침을** 클릭 하 여 새 라이선스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="adcbb-123">새 동시 라이선스</span><span class="sxs-lookup"><span data-stu-id="adcbb-123">New Concurrent License</span></span>**  
<span data-ttu-id="adcbb-124">새 동시 라이선스 마법사를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="adcbb-125">이 마법사는 다음 세 페이지로 구성 되며 새로운 무제한 라이선스 마법사와 거의 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="adcbb-126">**응용 프로그램 라이선스 그룹 이름** 필드에 라이선스 그룹의 이름을 입력 하 고 **라이선스 만료 경고** 필드에 값 (분)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="adcbb-127">(0 ~ 100의 값을 입력할 수 있습니다.) 위쪽 및 아래 화살표 키를 사용 하 여 분 수를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="adcbb-128">**라이선스 설명** 필드에 간단한 설명 텍스트를 입력 하 고 **동시 라이선스 수량** 필드에 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="adcbb-129">위쪽 및 아래 화살표를 사용 하 여 동시 라이선스 수를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="adcbb-130">**사용** 확인란을 선택 하 여 라이선스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="adcbb-131">필요에 따라 **만료 날짜** 필드를 사용 하 여 라이선스의 만료 날짜를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="adcbb-132">확인란을 선택 하 여 표시 된 만료 날짜를 사용 하거나 달력 유틸리티를 사용 하 여 원하는 만료 날짜를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="adcbb-133">**마침을** 클릭 하 여 새 라이선스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="adcbb-134">명명 된 새 라이선스</span><span class="sxs-lookup"><span data-stu-id="adcbb-134">New Named License</span></span>**  
<span data-ttu-id="adcbb-135">명명 된 새 라이선스 마법사를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="adcbb-136">이 마법사는 다음 네 페이지로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="adcbb-137">**응용 프로그램 라이선스 그룹 이름** 필드에 라이선스 그룹의 이름을 입력 하 고 **라이선스 만료 경고** 필드에 값 (분)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="adcbb-138">(0에서 100 까지의 값을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="adcbb-139">위쪽 및 아래 화살표 키를 사용 하 여 분 수를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="adcbb-140">**라이선스 설명** 필드에 간단한 설명 텍스트를 입력 하 고 **사용** 확인란을 선택 하 여 라이선스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="adcbb-141">필요에 따라 **만료 날짜** 필드를 사용 하 여 라이선스의 만료 날짜를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="adcbb-142">확인란을 선택 하 여 표시 된 만료 날짜를 사용 하거나 달력 유틸리티를 사용 하 여 원하는 만료 날짜를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="adcbb-143">명명 된 사용자 **추가**, **편집**또는 **제거** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="adcbb-144">**마침을** 클릭 하 여 새 라이선스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="adcbb-145">보기</span><span class="sxs-lookup"><span data-stu-id="adcbb-145">View</span></span>**  
<span data-ttu-id="adcbb-146">**결과** 창의 모양 및 콘텐츠를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="adcbb-147">여기에서 새 창</span><span class="sxs-lookup"><span data-stu-id="adcbb-147">New Window from Here</span></span>**  
<span data-ttu-id="adcbb-148">선택한 노드를 루트 노드로 하 여 새 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="adcbb-149">새로 고침</span><span class="sxs-lookup"><span data-stu-id="adcbb-149">Refresh</span></span>**  
<span data-ttu-id="adcbb-150">서버 뷰를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="adcbb-151">목록 내보내기</span><span class="sxs-lookup"><span data-stu-id="adcbb-151">Export List</span></span>**  
<span data-ttu-id="adcbb-152">**결과** 창의 내용이 들어 있는 탭으로 구분 된 텍스트 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="adcbb-153">이 항목에는 만드는 텍스트 파일의 위치를 지정 하는 표준 **파일 저장** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="adcbb-154">Help</span><span class="sxs-lookup"><span data-stu-id="adcbb-154">Help</span></span>**  
<span data-ttu-id="adcbb-155">응용 프로그램 가상화 서버 관리 콘솔에 대 한 도움말 시스템을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="adcbb-156">**범위** 창의 **응용 프로그램 라이선스** 노드 아래에 표시 되는 라이선스 그룹 또는 라이선스를 클릭 하는 경우 다음 요소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="adcbb-157">보기</span><span class="sxs-lookup"><span data-stu-id="adcbb-157">View</span></span>**  
<span data-ttu-id="adcbb-158">**결과** 창의 모양 및 콘텐츠를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="adcbb-159">여기에서 새 창</span><span class="sxs-lookup"><span data-stu-id="adcbb-159">New Window from Here</span></span>**  
<span data-ttu-id="adcbb-160">선택한 노드를 루트 노드로 하 여 새 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="adcbb-161">삭제</span><span class="sxs-lookup"><span data-stu-id="adcbb-161">Delete</span></span>**  
<span data-ttu-id="adcbb-162">**결과** 창에서 패키지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="adcbb-163">Rename</span><span class="sxs-lookup"><span data-stu-id="adcbb-163">Rename</span></span>**  
<span data-ttu-id="adcbb-164">**결과** 창에서 패키지의 이름을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="adcbb-165">목록 내보내기</span><span class="sxs-lookup"><span data-stu-id="adcbb-165">Export List</span></span>**  
<span data-ttu-id="adcbb-166">**결과** 창의 내용이 들어 있는 탭으로 구분 된 텍스트 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="adcbb-167">이 항목에는 만드는 텍스트 파일의 위치를 지정 하는 표준 **파일 저장** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="adcbb-168">특성</span><span class="sxs-lookup"><span data-stu-id="adcbb-168">Properties</span></span>**  
<span data-ttu-id="adcbb-169">선택한 라이선스 그룹에 대 한 **속성** 대화 상자를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="adcbb-170">**속성** 대화 상자의 **일반** 탭에 라이선스 그룹에 대 한 정보가 표시 되 고 **라이선스 만료 경고** 필드의 시간 값을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="adcbb-171">**응용 프로그램** 탭에는 라이선스 그룹과 연결 된 응용 프로그램 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="adcbb-172">Help</span><span class="sxs-lookup"><span data-stu-id="adcbb-172">Help</span></span>**  
<span data-ttu-id="adcbb-173">응용 프로그램 가상화 서버 관리 콘솔에 대 한 도움말 시스템을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbb-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="adcbb-174">관련 항목</span><span class="sxs-lookup"><span data-stu-id="adcbb-174">Related topics</span></span>


[<span data-ttu-id="adcbb-175">응용 프로그램 라이선스 정보</span><span class="sxs-lookup"><span data-stu-id="adcbb-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="adcbb-176">Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="adcbb-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="adcbb-177">Server Management Console: 응용 프로그램 라이선스 노드</span><span class="sxs-lookup"><span data-stu-id="adcbb-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





