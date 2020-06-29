---
title: MED-V에 대한 가상 PC 이미지 만들기
description: MED-V에 대한 가상 PC 이미지 만들기
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823663"
---
# <span data-ttu-id="de236-103">MED-V에 대한 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="de236-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="de236-104">MED-V에 대 한 VPC (가상 PC) 이미지를 만들려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="de236-105">[VPC 이미지를 만듭니다](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="de236-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="de236-106">[Med-v 작업 영역 .msi 패키지를 VPC 이미지에 설치](#bkmk-howtoinstallthemedvworkspacemsipackage)합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="de236-107">[VPC 이미지에서 med-v 가상 컴퓨터 필수 구성 요소 도구를 실행](#bkmk-howtorunthevirtualmachineprerequisitestool)합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="de236-108">[VPC 이미지에서 가상 컴퓨터 필수 구성 요소를 수동으로 구성](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites)합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="de236-109">[Med-v 이미지에 대 한 Sysprep을 구성](#bkmk-howtoconfiguresysprepformedvimages) 합니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="de236-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="de236-110">[Microsoft 가상 PC를 끄십시오](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="de236-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="de236-111">Microsoft Virtual PC를 사용 하 여 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="de236-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="de236-112">Microsoft Virtual PC를 사용 하 여 가상 PC 이미지를 만들려면 가상 PC 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="de236-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="de236-113">자세한 내용은 다음을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="de236-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="de236-114">Windows 가상 PC 도움말</span><span class="sxs-lookup"><span data-stu-id="de236-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="de236-115">가상 컴퓨터 만들기 및 게스트 운영 체제 설치</span><span class="sxs-lookup"><span data-stu-id="de236-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="de236-116">MED-V 작업 영역의 msi 패키지를 설치 하는 방법</span><span class="sxs-lookup"><span data-stu-id="de236-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="de236-117">가상 PC 이미지를 만든 후에 MED-V 작업 영역 .msi 패키지를 이미지에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="de236-118">MED-V 작업 영역 이미지를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="de236-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="de236-119">가상 컴퓨터를 시작 하 고, 내부에서 MED-V 작업 영역의 msi 패키지를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="de236-120">MED-V 작업 영역의 .msi 패키지는 *MED-V\_workspace\_x.msi*호출 되며 여기서 *x* 는 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="de236-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="de236-121">예를 들어 *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="de236-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="de236-122">MED-V 작업 영역 .msi 패키지를 두 번 클릭 하 고 설치 마법사 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="de236-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="de236-123">참고</span><span class="sxs-lookup"><span data-stu-id="de236-123">Note</span></span>**  
    <span data-ttu-id="de236-124">새 MED-V 버전이 출시 되 고 기존 가상 PC 이미지가 업데이트 되 면 기존 MED-V 작업 영역 .msi 패키지를 제거 하 고 컴퓨터를 다시 부팅 한 다음 새 MED-V 작업 영역 .msi 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="de236-125">가상 컴퓨터 필수 구성 요소 도구를 실행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="de236-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="de236-126">VM (가상 컴퓨터) 필수 구성 요소 도구는 몇 가지 필수 구성 요소를 자동화 하는 마법사입니다.</span><span class="sxs-lookup"><span data-stu-id="de236-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="de236-127">참고</span><span class="sxs-lookup"><span data-stu-id="de236-127">Note</span></span>**  
<span data-ttu-id="de236-128">마법사에서 많은 매개 변수를 구성할 수 있지만, MED-V의 적절 한 작동에 필요한 속성은 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="de236-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="de236-129">가상 컴퓨터 필수 구성 요소 도구를 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="de236-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="de236-130">MED-V 작업 영역 .msi 패키지가 설치 된 후 Windows **시작** 메뉴에서 **모든 프로그램의 &gt; Med-v &gt; VM 필수 구성 요소 도구**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="de236-131">참고</span><span class="sxs-lookup"><span data-stu-id="de236-131">Note</span></span>**  
    <span data-ttu-id="de236-132">가상 컴퓨터 필수 구성 요소 도구를 실행 하는 사용자는 로컬 관리자 권한이 있어야 하며 사용자만 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="de236-133">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-133">Click **Next**.</span></span>

3. <span data-ttu-id="de236-134">**Windows 설정** 페이지의 다음과 같은 구성 가능한 속성에서 구성할 구성을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="de236-135">사용자의 개인 기록 정보 지우기</span><span class="sxs-lookup"><span data-stu-id="de236-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="de236-136">로컬 프로필 임시 디렉터리 지우기</span><span class="sxs-lookup"><span data-stu-id="de236-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="de236-137">다음 Windows 이벤트에서 소리 사용 안 함: 시작, 로그온, 로그 오프</span><span class="sxs-lookup"><span data-stu-id="de236-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="de236-138">참고</span><span class="sxs-lookup"><span data-stu-id="de236-138">Note</span></span>**  
   <span data-ttu-id="de236-139">그룹 정책에서 Windows 페이지 보호기를 사용 하도록 설정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="de236-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="de236-140">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-140">Click **Next**.</span></span>

5. <span data-ttu-id="de236-141">**Internet Explorer 설정** 페이지의 구성 가능한 다음 속성에서 구성할 구성을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="de236-142">자동 완성 기능을 사용 하지 않음</span><span class="sxs-lookup"><span data-stu-id="de236-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="de236-143">바로 가기를 실행 하는 데 창을 다시 사용할 수 없도록 설정</span><span class="sxs-lookup"><span data-stu-id="de236-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="de236-144">검색 기록 지우기</span><span class="sxs-lookup"><span data-stu-id="de236-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="de236-145">Internet Explorer 7에서 탭 브라우저 사용</span><span class="sxs-lookup"><span data-stu-id="de236-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="de236-146">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-146">Click **Next**.</span></span>

7. <span data-ttu-id="de236-147">**Windows 서비스** 페이지의 다음과 같은 구성 가능한 속성에서 구성할 구성을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="de236-148">보안 센터 서비스</span><span class="sxs-lookup"><span data-stu-id="de236-148">Security center service</span></span>**

   -   **<span data-ttu-id="de236-149">작업 스케줄러 서비스</span><span class="sxs-lookup"><span data-stu-id="de236-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="de236-150">자동 업데이트 서비스</span><span class="sxs-lookup"><span data-stu-id="de236-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="de236-151">시스템 복원 서비스</span><span class="sxs-lookup"><span data-stu-id="de236-151">System restore service</span></span>**

   -   **<span data-ttu-id="de236-152">인덱싱 서비스</span><span class="sxs-lookup"><span data-stu-id="de236-152">Indexing service</span></span>**

   -   **<span data-ttu-id="de236-153">무선 제로 구성</span><span class="sxs-lookup"><span data-stu-id="de236-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="de236-154">빠른 사용자 전환 호환성</span><span class="sxs-lookup"><span data-stu-id="de236-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="de236-155">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-155">Click **Next**.</span></span>

9. <span data-ttu-id="de236-156">**Windows 자동 로그온** 페이지에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="de236-157">**Windows 자동 로그온 사용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="de236-158">**사용자 이름** 및 **암호**를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="de236-159">**적용**을 클릭 하 고 표시 되는 확인 상자에서 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="de236-160">**요약** 페이지에서 **마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="de236-161">참고</span><span class="sxs-lookup"><span data-stu-id="de236-161">Note</span></span>**  
<span data-ttu-id="de236-162">그룹 정책이 필수 구성 요소 도구에 설정 된 필수 설정을 덮어쓰지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="de236-163">MED-V 가상 컴퓨터 수동 설치 선행 조건을 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="de236-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="de236-164">가상 컴퓨터 필수 구성 요소 도구를 통해 몇 가지 구성을 구성할 수 없으며 수동으로 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="de236-165">가상 컴퓨터 설정</span><span class="sxs-lookup"><span data-stu-id="de236-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="de236-166">Microsoft Virtual PC 콘솔에서 다음 가상 컴퓨터 설정을 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="de236-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="de236-167">플로피 디스크 드라이브를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="de236-168">실행 취소-디스크 (**설정 &gt; 실행 취소-디스크**)를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="de236-169">이미지에 가상 CPU가 하나만 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="de236-170">가상 컴퓨터와 사용자가 게시 된 응용 프로그램 (예: 사용자 입력이 필요한 메시지)과 관련이 없는 경우 상호 작용을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="de236-171">이미지 설정</span><span class="sxs-lookup"><span data-stu-id="de236-171">Image Settings</span></span>

    <span data-ttu-id="de236-172">이미지 내에서 다음의 수동 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="de236-173">**전원 옵션 속성** 창에서 최대 절전 모드 및 절전 모드를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="de236-174">최신 Windows 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="de236-175">**Windows 시작 및 복구** 대화 상자의 **시스템 오류** 섹션에서 **자동으로 다시 시작** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="de236-176">이미지가 VLK 라이선스 키를 사용 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="de236-177">VPC 추가 설치</span><span class="sxs-lookup"><span data-stu-id="de236-177">Installing VPC Additions</span></span>

    <span data-ttu-id="de236-178">**작업** 메뉴에서 **가상 컴퓨터 추가 설치 또는 업데이트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="de236-179">인쇄 구성</span><span class="sxs-lookup"><span data-stu-id="de236-179">Configuring Printing</span></span>

    <span data-ttu-id="de236-180">다음 방법 중 하나를 통해 MED-V 작업 영역에서 인쇄를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de236-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="de236-181">가상 컴퓨터에 프린터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="de236-182">호스트 컴퓨터에 구성 된 프린터를 사용 하 여 인쇄를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="de236-183">MED-V 이미지에 대해 Sysprep를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="de236-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="de236-184">MED-V 작업 영역에서 여러 개의 MED-V 작업 영역이 단일 컴퓨터에서 실행 되는 경우에는 Sysprep를 구성 하 여 고유한 SID (보안 식별자)를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de236-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="de236-185">Sysprep를 사용 하 여 도메인에 가입 하지 않는 것이 좋습니다. 대신, [스크립트 동작을 설정 하는 방법](how-to-set-up-script-actions.md)에 설명 된 대로 med-v 조인 도메인 스크립트 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="de236-186">참고</span><span class="sxs-lookup"><span data-stu-id="de236-186">Note</span></span>**  
<span data-ttu-id="de236-187">Sysprep는 Windows 운영 체제에 대 한 Microsoft 시스템 준비 유틸리티입니다.</span><span class="sxs-lookup"><span data-stu-id="de236-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="de236-188">MED-V 작업 영역에서 Sysprep를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="de236-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="de236-189">*Sysprep*이라는 시스템 드라이브의 루트에 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de236-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="de236-190">Windows 설치 CD에서 시스템 드라이브의 루트로 *deploy.cab* 를 추출 하거나 Microsoft 웹 사이트에서 최신 배포 도구 업데이트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="de236-191">Windows 2000의 경우 [windows 2000 용 배포 도구 업데이트](https://go.microsoft.com/fwlink/?LinkId=143001)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="de236-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="de236-192">Windows XP의 경우 [WINDOWS xp 용 배포 도구 업데이트](https://go.microsoft.com/fwlink/?LinkId=143000)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="de236-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="de236-193">**설치 관리자** (setupmgr.exe)를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="de236-194">설치 관리자 마법사를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="de236-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="de236-195">Sysprep을 구성 하 고 MED-V 작업 영역을 만든 후에는 Sysprep을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="de236-196">Sysprep를 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="de236-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="de236-197">시스템 드라이브의 루트에 있는 Sysprep 폴더에서 시스템 준비 도구 (Sysprep.exe)를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="de236-198">경고 메시지 상자가 나타나면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="de236-199">**Sysprep 속성** 대화 상자에서 활성화 및 **최소 설정 사용** **에 대 한 유예 기간 다시 설정** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="de236-200">다시 **봉인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="de236-201">표시 되는 확인 메시지 상자에 나열 된 정보가 마음에 들지 않으면 **취소** 를 클릭 하 고 선택 항목을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="de236-202">**확인** 을 클릭 하 여 시스템 준비 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="de236-203">Microsoft Virtual PC를 끄는 중</span><span class="sxs-lookup"><span data-stu-id="de236-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="de236-204">모든 구성 요소를 설치 하 고 구성한 후에는 Microsoft 가상 PC를 닫고 **끄기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="de236-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="de236-205">관련 항목</span><span class="sxs-lookup"><span data-stu-id="de236-205">Related topics</span></span>


<span data-ttu-id="de236-206">MED-V 이미지 만들기 [스크립트 작업을 설정 하는 방법](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="de236-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>









