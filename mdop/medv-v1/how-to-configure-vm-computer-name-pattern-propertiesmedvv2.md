---
title: VM 컴퓨터 이름 패턴 속성을 구성하는 방법
description: VM 컴퓨터 이름 패턴 속성을 구성하는 방법
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827078"
---
# <span data-ttu-id="cc725-103">VM 컴퓨터 이름 패턴 속성을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cc725-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="cc725-104">가상 컴퓨터 컴퓨터 이름 패턴을 revertible 및 영구 MED-V 작업 영역에 모두 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="cc725-105">Revertible — 관리자는 각 Revertible MED-V 작업 영역 인스턴스에 고유한 이름을 할당 하 여 동일한 MED-V 작업 영역을 사용 하는 여러 컴퓨터를 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="cc725-106">Persistent-영구 MED-V 작업 영역에서 관리자는 설치 스크립트 중에 컴퓨터 이름을 변경 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="cc725-107">Revertible MED-V 작업 영역에 가상 컴퓨터 컴퓨터 이름 패턴을 할당 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cc725-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="cc725-108">Revertible MED-V 작업 영역에 가상 컴퓨터 컴퓨터 이름 패턴을 할당 하려면</span><span class="sxs-lookup"><span data-stu-id="cc725-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="cc725-109">Revertible MED-V 작업 영역을 클릭 하 여 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="cc725-110">**REVERTIBLE Vm 설정** 섹션에서 **컴퓨터 이름 패턴을 기반으로 VM 이름 바꾸기** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="cc725-111">**VM 컴퓨터 이름 패턴** 섹션에 다음 옵션을 사용 하 여 가상 컴퓨터 이미지를 명명 하는 데 사용할 패턴을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="cc725-112">**상수**-med-v 작업 영역을 사용 하는 모든 컴퓨터에서 상수가 되는 자유 텍스트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="cc725-113">**변수 (variable**)-변수 **삽입**을 클릭 하 여 변수를 입력 하 고 다음 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="cc725-114">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-114">User name</span></span>**

        -   **<span data-ttu-id="cc725-115">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-115">Domain name</span></span>**

        -   **<span data-ttu-id="cc725-116">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-116">Host name</span></span>**

        -   **<span data-ttu-id="cc725-117">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-117">Workspace name</span></span>**

        -   **<span data-ttu-id="cc725-118">가상 머신 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-118">Virtual machine name</span></span>**

        <span data-ttu-id="cc725-119">선택한 변수는 MED-V 작업 영역을 사용 하는 컴퓨터에 한정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="cc725-120">예를 들어 **도메인 이름을** 선택 하면 각 컴퓨터의 고유 이름에 컴퓨터의 도메인 이름이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="cc725-121">**임의 문자**-패턴에 포함할 각 문자에 대해 "\ #"을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="cc725-122">MED-V 작업 영역을 사용 하는 각 컴퓨터에는 지정 된 길이의 접미사가 있으며,이는 임의로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="cc725-123">참고</span><span class="sxs-lookup"><span data-stu-id="cc725-123">Note</span></span>**  
    <span data-ttu-id="cc725-124">컴퓨터 이름의 한계는 15 자입니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="cc725-125">패턴이 한도를 초과 하는 경우에는 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="cc725-126">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="cc725-127">참고</span><span class="sxs-lookup"><span data-stu-id="cc725-127">Note</span></span>**  
    <span data-ttu-id="cc725-128">Revertible VM 컴퓨터 이름 패턴은 컴퓨터 이름 패턴 ( **REVERTIBLE Vm 설정** 섹션)을 **기반으로 VM 이름을 바꿀** 때만 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="cc725-129">영구 MED-V 작업 영역에 가상 컴퓨터 컴퓨터 이름 패턴을 할당 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cc725-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="cc725-130">가상 컴퓨터 컴퓨터 이름 패턴을 영구 MED-V 작업 영역에 할당 하려면</span><span class="sxs-lookup"><span data-stu-id="cc725-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="cc725-131">영구적 MED-V 작업 영역을 클릭 하 여 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="cc725-132">**영구 VM 설정** 섹션에서 **스크립트 편집기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="cc725-133">**스크립트 작업** 대화 상자에서 **추가**를 클릭 하 고 하위 메뉴에서 **컴퓨터 이름 바꾸기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="cc725-134">**확인** 을 클릭 하 여 **스크립트 작업** 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="cc725-135">**Vm 설정** 탭의 **Vm 컴퓨터 이름 패턴** 섹션에 다음을 사용 하 여 컴퓨터의 이름을 바꾸는 데 사용할 패턴을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="cc725-136">**상수**-컴퓨터 이름에 포함 될 무료 텍스트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="cc725-137">**변수 (variable**)-변수 **삽입**을 클릭 하 여 변수를 입력 하 고 다음 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="cc725-138">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-138">User name</span></span>**

        -   **<span data-ttu-id="cc725-139">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-139">Domain name</span></span>**

        -   **<span data-ttu-id="cc725-140">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-140">Host name</span></span>**

        -   **<span data-ttu-id="cc725-141">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-141">Workspace name</span></span>**

        -   **<span data-ttu-id="cc725-142">가상 머신 이름</span><span class="sxs-lookup"><span data-stu-id="cc725-142">Virtual machine name</span></span>**

        <span data-ttu-id="cc725-143">선택한 변수는 이름을 바꾸는 컴퓨터에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="cc725-144">예를 들어 **도메인 이름을** 선택 하면 컴퓨터 이름에 컴퓨터의 도메인 이름이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="cc725-145">**임의 문자**-패턴에 포함할 각 문자에 대해 "\ #"을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="cc725-146">컴퓨터에는 지정 된 길이의 접미사가 있으며,이는 임의로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="cc725-147">참고</span><span class="sxs-lookup"><span data-stu-id="cc725-147">Note</span></span>**  
    <span data-ttu-id="cc725-148">컴퓨터 이름의 한계는 15 자입니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="cc725-149">패턴이 한도를 초과 하는 경우에는 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="cc725-150">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="cc725-151">참고</span><span class="sxs-lookup"><span data-stu-id="cc725-151">Note</span></span>**  
    <span data-ttu-id="cc725-152">**스크립트 작업** 대화 상자에서 작업으로 설정 된 경우에만 컴퓨터 이름이 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc725-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="cc725-153">자세한 내용은 [스크립트 동작을 설정 하는 방법을](how-to-set-up-script-actions.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cc725-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="cc725-154">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cc725-154">Related topics</span></span>


[<span data-ttu-id="cc725-155">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="cc725-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="cc725-156">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="cc725-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="cc725-157">스크립트 동작을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="cc725-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="cc725-158">가상 컴퓨터 구성의 예</span><span class="sxs-lookup"><span data-stu-id="cc725-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









