---
title: 도메인 사용자 또는 그룹을 구성하는 방법
description: 도메인 사용자 또는 그룹을 구성하는 방법
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827198"
---
# <span data-ttu-id="680fc-103">도메인 사용자 또는 그룹을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="680fc-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="680fc-104">배포 설정을 사용 하 여 MED-V 작업 영역에 액세스할 수 있는 사용자 또는 그룹을 제어 하 고 MED-V 작업 영역을 사용할 수 있는 시간과 오프 라인으로 사용 가능한 지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="680fc-105">MED-V 작업 영역과 호스트 간의 액세스를 제어 하는 추가 규칙을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="680fc-106">모든 MED-V 작업 영역 권한은 **정책** 모듈의 **배포** 탭에서 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="680fc-107">사용자가 MED-V 작업 영역을 활용할 수 있도록 하려면 먼저 MED-V 작업 영역 권한에 도메인 사용자 또는 그룹을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="680fc-108">그런 다음 각 사용자 또는 그룹에 대 한 사용 권한을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="680fc-109">도메인 사용자 또는 그룹을 추가 하는 방법</span><span class="sxs-lookup"><span data-stu-id="680fc-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="680fc-110">도메인 사용자 또는 그룹을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="680fc-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="680fc-111">**사용자/그룹** 창에서 추가를 클릭 **합니다.**</span><span class="sxs-lookup"><span data-stu-id="680fc-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="680fc-112">**사용자 또는 그룹 이름 입력** 대화 상자에서 다음 중 하나를 수행 하 여 도메인 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="680fc-113">**사용자 또는 그룹 이름 입력** 필드에 도메인에 있는 사용자 또는 그룹 또는 컴퓨터의 로컬 사용자 또는 그룹을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="680fc-114">그런 다음 **이름 확인** 을 클릭 하 여 기존 이름으로 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="680fc-115">**찾기를** 클릭 하 여 표준 **사용자 또는 그룹 선택** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="680fc-116">그런 다음 도메인 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="680fc-117">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-117">Click **OK**.</span></span>

    <span data-ttu-id="680fc-118">도메인 사용자 또는 그룹이 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="680fc-119">참고</span><span class="sxs-lookup"><span data-stu-id="680fc-119">Note</span></span>**  
    <span data-ttu-id="680fc-120">신뢰할 수 있는 도메인의 사용자는 수동으로 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="680fc-121">도메인 사용자 또는 그룹을 제거 하는 방법</span><span class="sxs-lookup"><span data-stu-id="680fc-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="680fc-122">도메인 사용자 또는 그룹을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="680fc-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="680fc-123">**사용자/그룹** 창에서 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="680fc-124">**제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-124">Click **Remove**.</span></span>

    <span data-ttu-id="680fc-125">사용자 또는 그룹이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-125">The user or group is deleted.</span></span>

## <span data-ttu-id="680fc-126">사용자 또는 그룹에 대 한 사용 권한을 설정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="680fc-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="680fc-127">사용자 또는 그룹에 대 한 사용 권한을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="680fc-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="680fc-128">사용 권한을 설정할 사용자 또는 그룹을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="680fc-129">다음 표에 설명 된 대로 MED-V 작업 영역 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="680fc-130">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="680fc-131">작업 영역 배포 속성</span><span class="sxs-lookup"><span data-stu-id="680fc-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="680fc-132">속성 설명 *일반*</span><span class="sxs-lookup"><span data-stu-id="680fc-132">Property Description *General*</span></span>

<span data-ttu-id="680fc-133">사용자 또는 그룹에 대 한 작업 영역 사용 &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="680fc-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="680fc-134">이 사용자 또는 그룹에 대 한 MED-V 작업 영역을 사용 하도록 설정 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="680fc-135">이 날짜에 작업 영역이 만료 됨</span><span class="sxs-lookup"><span data-stu-id="680fc-135">Workspace expires on this date</span></span>

<span data-ttu-id="680fc-136">이 사용자 또는 그룹에 대 한 사용 권한 집합에 대해 만료 날짜를 지정 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="680fc-137">이 확인란을 선택 하면 날짜 상자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="680fc-138">날짜를 설정 하면 사용 권한이 지정 된 날짜의 끝에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="680fc-139">오프 라인 작업 시간 제한</span><span class="sxs-lookup"><span data-stu-id="680fc-139">Offline work is restricted to</span></span>

<span data-ttu-id="680fc-140">이 확인란을 선택 하 여이 사용자 또는 그룹에 대 한 정책을 새로 고쳐야 하는 기간을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="680fc-141">선택 하면 기간 상자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="680fc-142">지정 된 기간이 끝날 때 일 또는 시간을 설정 하면 정책이 새로 고쳐지지 않는 경우 사용자 또는 그룹을 연결할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="680fc-143">작업 영역 삭제 옵션</span><span class="sxs-lookup"><span data-stu-id="680fc-143">Workspace deletion options</span></span>

<span data-ttu-id="680fc-144">MED-V 작업 영역 삭제 옵션을 설정 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="680fc-145">자세한 내용은 [Med-v 작업 영역 삭제 옵션을 설정 하는 방법을](how-to-set-med-v-workspace-deletion-options.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="680fc-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="680fc-146">데이터 전송</span><span class="sxs-lookup"><span data-stu-id="680fc-146">Data Transfer</span></span>*

<span data-ttu-id="680fc-147">호스트와 작업 영역 간 클립보드 지원</span><span class="sxs-lookup"><span data-stu-id="680fc-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="680fc-148">이 확인란을 선택 하면 호스트와 MED-V 작업 영역 간에 복사 하 여 붙여 넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="680fc-149">호스트와 작업 영역 간의 파일 전송 지원</span><span class="sxs-lookup"><span data-stu-id="680fc-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="680fc-150">호스트와 MED-V 작업 영역 간에 파일을 전송할 수 있도록 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="680fc-151">**파일 전송** 상자에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="680fc-152">**Both**-호스트와 med-v 작업 영역 간에 파일을 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="680fc-153">**호스트 대 작업 공간**-호스트에서 med-v 작업 공간으로 파일을 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="680fc-154">**호스트할 작업 영역**— med-v 작업 영역의 파일을 호스트로 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="680fc-155">참고</span><span class="sxs-lookup"><span data-stu-id="680fc-155">Note</span></span>**  
<span data-ttu-id="680fc-156">권한이 없는 사용자가 파일을 전송 하려고 하면 파일 전송을 수행할 수 있는 권한이 있는 사용자의 자격 증명을 입력 하 라는 메시지가 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="680fc-157">중요</span><span class="sxs-lookup"><span data-stu-id="680fc-157">Important</span></span>**  
<span data-ttu-id="680fc-158">Windows XP SP3에서 파일 전송을 지원 하려면 아래와 같이 레지스트리를 편집 하 여 오프 라인 파일 동기화를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="680fc-159">고급</span><span class="sxs-lookup"><span data-stu-id="680fc-159">Advanced</span></span>

<span data-ttu-id="680fc-160">고급 파일 전송 옵션을 설정 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="680fc-161">자세한 내용은 [고급 파일 전송 옵션을 설정 하는 방법을](how-to-set-advanced-file-transfer-options.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="680fc-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="680fc-162">장치 컨트롤</span><span class="sxs-lookup"><span data-stu-id="680fc-162">Device Control</span></span>*

<span data-ttu-id="680fc-163">호스트에 연결 된 프린터로 인쇄할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="680fc-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="680fc-164">이 확인란을 선택 하면 사용자가 호스트 프린터를 사용 하 여 MED-V 작업 영역에서 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="680fc-165">참고</span><span class="sxs-lookup"><span data-stu-id="680fc-165">Note</span></span>**  
<span data-ttu-id="680fc-166">호스트에 정의 된 프린터가 인쇄를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="680fc-167">CD/DVD에 대 한 액세스를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="680fc-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="680fc-168">이 MED-V 작업 영역의 CD 또는 DVD 드라이브에 대 한 액세스를 허용 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="680fc-169">여러 멤버 자격</span><span class="sxs-lookup"><span data-stu-id="680fc-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="680fc-170">사용자가 그룹의 일부이 고 해당 권한이 속한 그룹에만 사용자에 게 적용 되는 경우에는 모든 사용 권한이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="680fc-171">사용자가 서로 다른 두 그룹의 구성원 인 경우 가장 덜 제한적인 권한이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="680fc-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="680fc-172">관련 항목</span><span class="sxs-lookup"><span data-stu-id="680fc-172">Related topics</span></span>


[<span data-ttu-id="680fc-173">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="680fc-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="680fc-174">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="680fc-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="680fc-175">MED-V 작업 영역 삭제 옵션을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="680fc-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="680fc-176">고급 파일 전송 옵션을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="680fc-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









