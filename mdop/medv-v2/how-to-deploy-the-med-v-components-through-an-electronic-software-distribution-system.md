---
title: 전자 소프트웨어 배포 시스템을 통해 MED-V 구성 요소를 배포하는 방법
description: 전자 소프트웨어 배포 시스템을 통해 MED-V 구성 요소를 배포하는 방법
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824853"
---
# <span data-ttu-id="a812d-103">전자 소프트웨어 배포 시스템을 통해 MED-V 구성 요소를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="a812d-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="a812d-104">전자 소프트웨어 배포 시스템을 사용 하면 느리거나 빠른 네트워크 연결을 통해 여러 컴퓨터로 소프트웨어를 효율적으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="a812d-105">다음 섹션에서는 소프트웨어 배포 시스템을 사용 하 여 엔터프라이즈 전체의 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 구성 요소를 배포 하는 데 도움이 되는 정보 및 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="a812d-106">참고</span><span class="sxs-lookup"><span data-stu-id="a812d-106">Note</span></span>**  
<span data-ttu-id="a812d-107">사용 하는 소프트웨어 배포 솔루션에 따라 특정 솔루션의 요구 사항에 대해 잘 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="a812d-108">System Center Configuration Manager 2007 R2 이상 버전을 사용 하는 경우 Microsoft 기술 라이브러리 ()의 [Configuration Manager 문서 라이브러리](https://go.microsoft.com/fwlink/?LinkId=66999) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="a812d-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="a812d-109">중요</span><span class="sxs-lookup"><span data-stu-id="a812d-109">Important</span></span>**  
<span data-ttu-id="a812d-110">System Center Configuration Manager 2007 SP2를 사용 하 고 있으며 MED-V 작업 영역이 **NAT** 모드에서 작동 하도록 구성 된 경우 가상 컴퓨터는 인터넷 기반 클라이언트로 분류 되며 콘텐츠를 다운로드할 가장 가까운 배포 지점을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="a812d-111">MED-V에서 관리 되는 [vm에 대 한 기능을 개선 하는 핫픽스](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) med-v에서 관리 하 고 **NAT** 모드에서 작동 하도록 구성 된 가상 컴퓨터에는 새 기능을 추가 합니다.)</span><span class="sxs-lookup"><span data-stu-id="a812d-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="a812d-112">새로운 기능을 통해 가상 머신은 가장 가까운 배포 지점에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="a812d-113">따라서 관리자는 동일한 방식으로 가상 컴퓨터와 호스트 컴퓨터를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="a812d-114">이 핫픽스는 사이트 서버, 그리고 클라이언트에 먼저 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="a812d-115">업데이트를 공개적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-115">The update is publicly available.</span></span> <span data-ttu-id="a812d-116">그러나 Microsoft 서비스에 대 한 계약을 수락 하 라는 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="a812d-117">후속 웹 페이지의 메시지에 따라이 핫픽스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="a812d-118">참고</span><span class="sxs-lookup"><span data-stu-id="a812d-118">Note</span></span>**  
<span data-ttu-id="a812d-119">소프트웨어 배포 시스템을 통해 MED-V 구성 요소를 배포 하려면 MED-V 작업 영역 포장기를 설치 하 고 MED-V 작업 영역을 빌드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="a812d-120">이미지를 준비 하 고 MED-V 작업 영역을 빌드하는 방법에 대 한 자세한 내용은 [med-v에 대 한 작업](operations-for-med-v.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="a812d-121">소프트웨어 배포 시스템을 사용 하 여 MED-V 구성 요소를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="a812d-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="a812d-122">전자 소프트웨어 배포 시스템의 컴퓨터 및 사용자 그룹을 컴퓨터/사용자의 대상 집합으로 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="a812d-123">배포 해야 하는 각 Microsoft 설치 파일에 대 한 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="a812d-124">다음은 필수 파일 및 설치 해야 하는 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="a812d-125">**Windows 가상 PC** – 아직 설치 되지 않은 경우 (컴퓨터를 다시 시작 해야 함).</span><span class="sxs-lookup"><span data-stu-id="a812d-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="a812d-126">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="a812d-127">**Windows 가상 PC 추가 및 업데이트** -아직 설치 되지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="a812d-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="a812d-128">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="a812d-129">**Med-v 호스트 에이전트 설치 파일** – 호스트 에이전트 (Med-v-v _HostAgent \ _Setup 설치 파일)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="a812d-130">자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="a812d-131">Warning</span><span class="sxs-lookup"><span data-stu-id="a812d-131">Warning</span></span>**  
        <span data-ttu-id="a812d-132">MED-V 호스트 에이전트를 설치 하기 전에 Internet Explorer를 닫은 경우 나중에 URL 리디렉션으로 충돌이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="a812d-133">배포 중에 컴퓨터 다시 시작을 지정 하 여이 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="a812d-134">Med-v 작업 **영역 설치 관리자, VHD, 설치 실행 파일** – **Med-v 작업 영역 포장기**에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="a812d-135">자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="a812d-136">중요</span><span class="sxs-lookup"><span data-stu-id="a812d-136">Important</span></span>**  
        <span data-ttu-id="a812d-137">압축 된 가상 하드 디스크 파일 (.sdv) 및 설치 실행 프로그램 (setup.exe)이 MED-V 작업 영역 설치 관리자와 같은 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="a812d-138">그런 다음 setup.exe를 실행 하 여 MED-V 작업 영역 설치 관리자를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="a812d-139">팁</span><span class="sxs-lookup"><span data-stu-id="a812d-139">Tip</span></span>**  
        <span data-ttu-id="a812d-140">네트워크 위치에서 MED-V를 설치할 때 발생할 수 있는 문제 때문에 MED-V 작업 영역 설정 파일을 로컬로 복사한 다음 setup.exe를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="a812d-141">패키지를 자동 모드로 실행 하도록 구성 합니다 (사용자 조작이 필요 없음).</span><span class="sxs-lookup"><span data-stu-id="a812d-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="a812d-142">자동 모드로 실행 하면 Internet Explorer가 실행 중이면 닫을 것인지 묻는 메시지가 표시 되 고 MED-V 호스트 에이전트를 시작 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="a812d-143">두 작업은 모두 컴퓨터를 다시 시작할 때 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="a812d-144">참고</span><span class="sxs-lookup"><span data-stu-id="a812d-144">Note</span></span>**  
    <span data-ttu-id="a812d-145">Windows 가상 PC를 설치 하려면 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="a812d-146">다시 시작을 억제 하 고 MED-V에 설치 하는 데 필요한 필수 구성 요소를 무시 하는 경우 단일 설치 프로세스를 만들고 모든 구성 요소를 동시에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="a812d-147">명령줄 인수를 사용 하 여이 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="a812d-148">이러한 인수의 예는 [배치 파일을 사용 하 여 med-v 구성 요소 설치를](#bkmk-batch)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="a812d-149">컴퓨터를 다시 시작 하면 MED-V가 자동으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="a812d-150">Windows 가상 PC를 설치 하기 전에 MED-V와 해당 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="a812d-151">이 항목의 뒷부분에 나오는 일괄 처리 파일 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="a812d-152">중요</span><span class="sxs-lookup"><span data-stu-id="a812d-152">Important</span></span>**  
    <span data-ttu-id="a812d-153">필수 VPC 구성 요소 보다 먼저 MED-V 구성 요소를 설치할 수 있도록 예제 배치 파일에 나와 있는 것 처럼 **무시 \ _PREREQUISITES** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="a812d-154">단일 다시 시작을 허용 하려면이 순서로 MED-V 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="a812d-155">설치에 필요한 기타 요구 사항과 대상 플랫폼, 빈 디스크 공간 등의 소프트웨어 배포 시스템을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="a812d-156">패키지를 컴퓨터/사용자의 대상 집합에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="a812d-157">컴퓨터가 실행 되 면 소프트웨어 배포 시스템 클라이언트에서 새 패키지를 사용할 수 있음을 인식 하 고 정의 및 요구 사항에 따라 패키지를 설치 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="a812d-158">설치는 자동 모드에서 순차적으로 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="a812d-159">모든 패키지가 설치 될 때까지 다시 시작 하지 않아도 되는 단일 프로세스로이 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="a812d-160">설치가 완료 되 면 업데이트 된 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="a812d-161">소프트웨어 배포 시스템에 따라 컴퓨터를 다시 시작 하도록 예약 하거나, 최종 사용자가 일반 작업 중에 수동으로 컴퓨터를 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="a812d-162">컴퓨터가 다시 시작 되 면 최종 사용자가 로그온 한 후에 MED-V가 자동으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="a812d-163">MED-V가 처음 시작 되 면 설치 프로그램이 처음으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="a812d-164">처음 설치를 시작할 때 지정한 가상 하드 디스크의 크기와 시작 시 MED-V 작업 영역에 적용 된 정책의 수에 따라 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="a812d-165">최종 사용자는 알림 영역에서 MED-V 아이콘을 시청 하 여 진행률을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="a812d-166">처음 설정 하는 방법에 대 한 자세한 내용은 [med-v 2.0 배포 개요](med-v-20-deployment-overview.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a812d-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="a812d-167">배치 파일을 사용 하 여 MED-V 구성 요소를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="a812d-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="a812d-168">관리 자격 증명을 사용 하 여 명령 프롬프트에서 설치를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="a812d-169">각 구성 요소를 단일 디렉터리에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="a812d-170">네트워크 공유에서 실행 하는 경우에는. a i a dv 파일의 압축을 푸는 데 시간이 더 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="a812d-171">가장 좋은 방법은 MED-V 호스트 에이전트 및 MED-V 작업 영역 패키지 파일을 설치한 후 Windows 가상 PC 및 Windows 가상 PC 핫픽스가 설치 되도록 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="a812d-172">즉, Windows Update는 다시 시작을 요구 하 여 설치 프로세스에 간섭이 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="a812d-173">일괄 처리 파일이 완료 된 후 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="a812d-174">다시 시작 하면 사용자에 게 처음 설정 하 고 MED-V의 구성을 완료 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="a812d-175">다음 예제에서는 지정 된 인수를 사용 하 여 단일 프로세스로 64 비트 MED-V 구성 요소를 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a812d-176">인수</span><span class="sxs-lookup"><span data-stu-id="a812d-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="a812d-177">설명</span><span class="sxs-lookup"><span data-stu-id="a812d-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a812d-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="a812d-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="a812d-179">Windows Virtual PC 및 Windows 가상 PC 업데이트 설치가 호스트 컴퓨터를 다시 시작 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a812d-180">/quiet</span><span class="sxs-lookup"><span data-stu-id="a812d-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="a812d-181">사용자 조작 없이 자동 모드로 MED-V 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a812d-182">/qn</span><span class="sxs-lookup"><span data-stu-id="a812d-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="a812d-183">사용자 인터페이스 없이 MED-V 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a812d-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="a812d-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="a812d-185">Windows 가상 PC를 확인 하지 않고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a812d-186">참고</span><span class="sxs-lookup"><span data-stu-id="a812d-186">Note</span></span></strong><br/><p><span data-ttu-id="a812d-187">이 설치의 일부로 Windows 가상 PC를 설치 하는 경우에만이 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a812d-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="a812d-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="a812d-189">MED-V 작업 영역을 강제로 설치 하 고 생성 될 수 있는 모든 메시지를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a812d-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a812d-190">예제</span><span class="sxs-lookup"><span data-stu-id="a812d-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="a812d-191">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a812d-191">Related topics</span></span>


[<span data-ttu-id="a812d-192">MED-V 2.0 배포 개요</span><span class="sxs-lookup"><span data-stu-id="a812d-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="a812d-193">MED-V 구성 요소 배포</span><span class="sxs-lookup"><span data-stu-id="a812d-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)









