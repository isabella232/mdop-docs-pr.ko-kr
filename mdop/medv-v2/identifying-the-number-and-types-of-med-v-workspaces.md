---
title: MED-V 작업 영역의 번호 및 유형 식별
description: MED-V 작업 영역의 번호 및 유형 식별
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827263"
---
# <span data-ttu-id="c2080-103">MED-V 작업 영역의 번호 및 유형 식별</span><span class="sxs-lookup"><span data-stu-id="c2080-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="c2080-104">MED-V는 Windows XP가 필요 하거나 호스트 컴퓨터의 버전과 다른 Internet Explorer 버전을 필요로 하는 응용 프로그램을 실행 하기 위한 가상 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="c2080-105">이 가상 환경은 MED-V 작업 영역 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="c2080-106">Windows 7로 마이그레이션할 때 조직이 직면 하는 응용 프로그램 호환성 요구 사항에 따라 특정 사용자 또는 부서에만 MED-V 작업 영역이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="c2080-107">배포를 계획할 때 엔터프라이즈에서 필요한 MED-V 작업 영역의 수를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="c2080-108">또한 각 MED-V 작업 영역의 요구 사항을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="c2080-109">MED-V 작업 영역의 수 및 유형 식별</span><span class="sxs-lookup"><span data-stu-id="c2080-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="c2080-110">엔터프라이즈에서 MED-V 작업 영역을 만들 컴퓨터와 그룹을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="c2080-111">일반적으로 이러한 응용 프로그램에 액세스 해야 하는 사용자는 Windows 7로 마이그레이션할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="c2080-112">마이그레이션할 수 없는 응용 프로그램과이 응용 프로그램을 실행 하는 데 MED-V 작업 영역이 필요한 사용자를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="c2080-113">아직 Windows 7에 최적화 되지 않은 인트라넷 주소도 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="c2080-114">MED-V 작업 영역에서는 최종 사용자가 아직 Windows 7로 마이그레이션할 준비가 되지 않은 해당 웹 주소에 더 잘 액세스할 수 있는 Internet Explorer 브라우저를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="c2080-115">MED-V 배포를 준비 하 고 계획 하는 동안에는 호스트 컴퓨터의 Internet Explorer에서 MED-V 작업 영역의 Internet Explorer로 리디렉션할 URL 주소 목록을 식별 하 고 컴파일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="c2080-116">마지막으로, 디스크 공간 요구 사항을 평가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="c2080-117">대부분의 MED-V 작업 영역은 2gb 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="c2080-118">시스템에서 사용 가능한 디스크 공간은 MED-V의 구성 및 사용자 수에 따라 신속 하 게 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="c2080-119">또한 회사의 기본 배포 방법에 추가 공간이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="c2080-120">일반적으로 MED-V 작업 영역에 대해 최소 10gb의 디스크 공간을 확보 해야 하지만 이미지 크기에 따라 크게 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="c2080-121">MED-V 작업 영역에 대 한 디스크 공간 요구 사항 계산</span><span class="sxs-lookup"><span data-stu-id="c2080-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="c2080-122">MED-V 작업 영역에는 설치 되어 있는 호스트 컴퓨터의 메모리와 디스크 공간이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="c2080-123">최소한 호스트에 2gb의 디스크 공간이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="c2080-124">디스크 공간은 변수 이며 사용자의 MED-V 작업 영역에 있는 응용 프로그램 및 데이터의 수에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="c2080-125">MED-V에 최소 10gb의 디스크 공간을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="c2080-126">이 크기는 기본 Windows XP 작업 영역 및 몇 가지 기본 설치 응용 프로그램 및 웹 리디렉션을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="c2080-127">또한 호스트 스왑 드라이브에 사용 가능한 공간을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="c2080-128">기본 구성에서는 MED-V와 배포 된 단일 MED-V 작업 영역이 6 ~ 8gb 만큼 소모 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="c2080-129">MED-V 작업 영역에 많은 수의 응용 프로그램을 포함 하거나 각 컴퓨터에 둘 이상의 사용자가 있는 경우 다음과 같은 계산을 사용 하 여 MED-V 작업 영역에 필요한 디스크 공간을 보다 정확 하 게 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="c2080-130">기본 VHD + (컴퓨터별 사용자 x (차이점 디스크 + 저장 된 상태))</span><span class="sxs-lookup"><span data-stu-id="c2080-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="c2080-131">필요한 디스크 공간을 계산 하려면 다음을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="c2080-132">**기본 VHD의 크기** -med-v 작업 영역을 만드는 데 사용 된 가상 하드 디스크입니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="c2080-133">**중요**  .. A i a dv 파일을 압축 했으므로 계산에는. a dv 파일 크기를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c2080-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="c2080-134">**컴퓨터당 사용자** – med-v는 컴퓨터의 각 사용자에 대해 med-v 작업 영역을 만듭니다. MED-V 작업 영역은 각 사용자가 로그온 할 때 디스크 공간을 소모 하 고 MED-V 작업 영역이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="c2080-135">기본 VHD와의 차이를 추적 하는 데 사용 되는 **차이점 보관용 디스크의 크기** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="c2080-136">이 크기는 가상 하드 디스크에 응용 프로그램 및 소프트웨어 업데이트를 추가 하는 경우에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="c2080-137">각 MED-V 사용자가 처음으로 MED-V를 시작할 때 차이점 보관용 디스크가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="c2080-138">**저장 된 상태 파일의 크기로,** 가상 컴퓨터에서 상태를 유지 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="c2080-139">일반적으로이는 가상 컴퓨터에 할당 된 RAM 보다 약간 더 큽니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="c2080-140">예를 들어 1 GB의 RAM이 할당 되 면 1081000 KB에 대 한 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="c2080-141">다음 예제에서는 2.6 GB 가상 하드 디스크가 있는 MED-V 작업 영역의 세 가지 사용자를 기준으로 계산을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="c2080-142">2.6 gb + (3 x (1.5 gb + 1gb)) = 10.1 gb</span><span class="sxs-lookup"><span data-stu-id="c2080-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="c2080-143">**참고**  MED-V 모범 사례는 랩 배포를 사용 하 여 요구 사항의 유효성을 검사 하는 데 필요한 공간을 계산 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="c2080-144">파일 크기를 확인 하기 위해 파일 찾기</span><span class="sxs-lookup"><span data-stu-id="c2080-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="c2080-145">다음 위치에는 컴퓨터 및 사용자 설정에 대 한 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2080-146">형식</span><span class="sxs-lookup"><span data-stu-id="c2080-146">Type</span></span></th>
<th align="left"><span data-ttu-id="c2080-147">위치</span><span class="sxs-lookup"><span data-stu-id="c2080-147">Location</span></span></th>
<th align="left"><span data-ttu-id="c2080-148">파일</span><span class="sxs-lookup"><span data-stu-id="c2080-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2080-149">기본 VHD</span><span class="sxs-lookup"><span data-stu-id="c2080-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2080-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="c2080-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="c2080-151">InternalName </em> -여기서 <em> INTERNALNAME </em> 는 Med-v 작업 영역 포장기에서 선택한 가상 하드 디스크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2080-152">차이점 보관용 디스크</span><span class="sxs-lookup"><span data-stu-id="c2080-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2080-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="c2080-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="c2080-154">WorkspaceName </em></span><span class="sxs-lookup"><span data-stu-id="c2080-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2080-155">저장 된 상태 파일</span><span class="sxs-lookup"><span data-stu-id="c2080-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2080-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="c2080-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="c2080-157">WorkspaceName </em> v</span><span class="sxs-lookup"><span data-stu-id="c2080-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2080-158">공유 MED-V 작업 영역의 디스크 공간 요구 사항 계산</span><span class="sxs-lookup"><span data-stu-id="c2080-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="c2080-159">단일 컴퓨터에서 공유 MED-V 작업 영역 배포를 계산 하는 경우 MED-V는 모든 사용자에 대해 하나의 차이점 보관용 디스크만 구성 되므로 계산에서 컴퓨터당 사용자 수는 항상 "1"입니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="c2080-160">%ProgramData%\\Microsoft\\Medv\\AllUsers.의 공유 MED-V 작업 영역에 대 한 차이점 보관용 디스크와 저장 된 상태 파일을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2080-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="c2080-161">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c2080-161">Related topics</span></span>


[<span data-ttu-id="c2080-162">MED-V 배포 정의 및 계획</span><span class="sxs-lookup"><span data-stu-id="c2080-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="c2080-163">MED-V 계획</span><span class="sxs-lookup"><span data-stu-id="c2080-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





