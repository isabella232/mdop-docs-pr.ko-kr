---
title: MED-V 2.0 배포 개요
description: MED-V 2.0 배포 개요
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826108"
---
# <span data-ttu-id="2ef37-103">MED-V 2.0 배포 개요</span><span class="sxs-lookup"><span data-stu-id="2ef37-103">MED-V 2.0 Deployment Overview</span></span>


<span data-ttu-id="2ef37-104">이 섹션에서는 MED-V (Enterprise 데스크톱 가상화) 2.0를 설치 하 고 배포 하는 방법에 대 한 일반적인 정보와 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-104">This section provides general information and instructions about how to install and deploy Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="2ef37-105">개요</span><span class="sxs-lookup"><span data-stu-id="2ef37-105">Overview</span></span>


<span data-ttu-id="2ef37-106">MED-V 2.0는 응용 프로그램을 배포 하는 데 사용 하는 것과 동일한 메서드를 사용 하 여 MED-V를 배포 하 고 관리 하는 응용 프로그램 모델을 기반으로 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-106">MED-V 2.0 is based on an application model, where the same methods that you use to deploy applications can be used to deploy and manage MED-V.</span></span> <span data-ttu-id="2ef37-107">배포 된 MED-V 솔루션에는 MED-V 호스트 에이전트와 게스트 에이전트의 두 가지 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-107">A deployed MED-V solution includes two components: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="2ef37-108">MED-V 호스트 에이전트는 Windows 7 데스크톱에 설치 되 고 med-v 게스트 에이전트는 MED-V 작업 영역 내의 Windows XP에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-108">The MED-V Host Agent is installed on the Windows 7 desktop and the MED-V Guest Agent is installed on Windows XP inside the MED-V workspace.</span></span> <span data-ttu-id="2ef37-109">MED-V에는 med-v 작업 영역을 만들고 구성 하는 데 필요한 정보와 도구를 제공 하는 MED-V 작업 영역 포장기도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-109">MED-V also includes a MED-V Workspace Packager that provides the information and tools necessary for creating and configuring MED-V workspaces.</span></span>

**<span data-ttu-id="2ef37-110">중요</span><span class="sxs-lookup"><span data-stu-id="2ef37-110">Important</span></span>**  
<span data-ttu-id="2ef37-111">MED-V는 MED-V 작업 영역 포장기, MED-V 호스트 에이전트, 모든 사용자에 대 한 MED-V 작업 영역의 설치만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-111">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="2ef37-112">**ALLUSERS = ""** 를 선택 해야만 현재 사용자에 대해 med-v를 설치 하면 구성 요소 설치와 med-v 작업 영역의 설정에 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-112">Installing MED-V for the current user only by selecting **ALLUSERS=””** causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>



### <span data-ttu-id="2ef37-113">MED-V 설치 파일</span><span class="sxs-lookup"><span data-stu-id="2ef37-113">The MED-V Installation Files</span></span>

<span data-ttu-id="2ef37-114">MED-V는 MED-V를 실행 하는 데 필요한 다음 설치 파일을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-114">MED-V includes the following installation files, required for running MED-V:</span></span>

**<span data-ttu-id="2ef37-115">MED-V 호스트 에이전트 설치 파일</span><span class="sxs-lookup"><span data-stu-id="2ef37-115">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="2ef37-116">호스트 에이전트 설치 파일의 이름은 MED-V\_HostAgent\_Setup.exe입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-116">The Host Agent installation file is named MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="2ef37-117">이 파일은 전사적 배포의 일부로 각각의 관련 최종 사용자 컴퓨터에 배포 및 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-117">This file is distributed and installed on each relevant end-user computer as part of your enterprise-wide deployment of MED-V.</span></span>

**<span data-ttu-id="2ef37-118">MED-V 작업 영역 포장기 설치 파일</span><span class="sxs-lookup"><span data-stu-id="2ef37-118">The MED-V Workspace Packager Installation File</span></span>**

<span data-ttu-id="2ef37-119">MED-V 작업 영역 포장기 설치 파일의 이름은 MED-V\_WorkspacePackager\_Setup.exe입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-119">The MED-V Workspace Packager installation file is named MED-V\_WorkspacePackager\_Setup.exe.</span></span> <span data-ttu-id="2ef37-120">이 파일을 사용 하 여 관리자 권한 및 사용 권한이 있는 컴퓨터에 MED-V 작업 영역 포장기를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-120">Use this file to install the MED-V Workspace Packager on a computer where you have administrator rights and permissions.</span></span> <span data-ttu-id="2ef37-121">데스크톱 관리자는 MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역을 만들고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-121">The desktop administrator uses the MED-V Workspace Packager to create and manage MED-V workspaces.</span></span>

**<span data-ttu-id="2ef37-122">참고</span><span class="sxs-lookup"><span data-stu-id="2ef37-122">Note</span></span>**  
<span data-ttu-id="2ef37-123">MED-V 게스트 에이전트는 처음 설정 하는 동안 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-123">The MED-V Guest Agent is installed automatically during first time setup.</span></span>



### <span data-ttu-id="2ef37-124">MED-V 배포 프로세스</span><span class="sxs-lookup"><span data-stu-id="2ef37-124">The MED-V Deployment Process</span></span>

<span data-ttu-id="2ef37-125">다음은 MED-V 설치 및 배포 프로세스의 상위 수준에 대 한 간략 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-125">The following is a high-level overview of the MED-V installation and deployment process:</span></span>

1.  <span data-ttu-id="2ef37-126">관리 자격 증명이 있고 MED-V 작업 영역 패키지를 작성 하는 데 사용할 컴퓨터에 MED-V 작업 영역 포장기를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-126">Install the MED-V Workspace Packager on the computer where you have administrative credentials and that you will be using to build the MED-V workspace packages.</span></span> <span data-ttu-id="2ef37-127">자세한 내용은 [Med-v 작업 영역 포장기를 설치 하는 방법을](how-to-install-the-med-v-workspace-packager.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-127">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

2.  <span data-ttu-id="2ef37-128">Med-v 이미지를 준비 하 고 MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-128">Prepare your MED-V image and create your MED-V workspace packages by using the MED-V Workspace Packager.</span></span> <span data-ttu-id="2ef37-129">자세한 내용은 [med-v에 대 한 작업](operations-for-med-v.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-129">For more information, see [Operations for MED-V](operations-for-med-v.md).</span></span>

3.  <span data-ttu-id="2ef37-130">엔터프라이즈 전체에 필요한 MED-V 구성 요소를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-130">Deploy the required MED-V components throughout your enterprise.</span></span> <span data-ttu-id="2ef37-131">MED-V의 필수 구성 요소는 Windows 가상 PC, MED-V 호스트 에이전트, MED-V 작업 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-131">The required components of MED-V are Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span>

**<span data-ttu-id="2ef37-132">중요</span><span class="sxs-lookup"><span data-stu-id="2ef37-132">Important</span></span>**  
<span data-ttu-id="2ef37-133">MED-V 구성 요소를 설치 하려면 관리 자격 증명이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-133">Installation of the MED-V components requires administrative credentials.</span></span> <span data-ttu-id="2ef37-134">최종 사용자가 MED-V를 설치 하는 경우 관리 자격 증명을 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-134">If an end user is installing MED-V, they are prompted to enter administrative credentials.</span></span> <span data-ttu-id="2ef37-135">또한, ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 설치 하는 경우에는 관리 자격 증명을 컨텍스트에서 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-135">Alternately, administrative credentials can be provided in context if you are installing by using an electronic software distribution (ESD) system.</span></span>



### <span data-ttu-id="2ef37-136">MED-V 구성 요소</span><span class="sxs-lookup"><span data-stu-id="2ef37-136">The MED-V Components</span></span>

<span data-ttu-id="2ef37-137">엔터프라이즈 전반에 걸쳐 배포 하는 MED-V 구성 요소는 다음과 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-137">The MED-V components that you deploy throughout your enterprise consist of the following:</span></span>

**<span data-ttu-id="2ef37-138">Windows 가상 PC</span><span class="sxs-lookup"><span data-stu-id="2ef37-138">Windows Virtual PC</span></span>**

<span data-ttu-id="2ef37-139">MED-V는 호환성 솔루션을 위해 Windows 가상 PC 이미지 내에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-139">MED-V functions inside Windows Virtual PC images for its compatibility solution.</span></span> <span data-ttu-id="2ef37-140">Windows 가상 PC 및 Windows 7 용 업데이트 (KB977206)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-140">Windows Virtual PC and the update for Windows 7 (KB977206) are required.</span></span> <span data-ttu-id="2ef37-141">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-141">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

**<span data-ttu-id="2ef37-142">MED-V 호스트 에이전트 설치 파일</span><span class="sxs-lookup"><span data-stu-id="2ef37-142">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="2ef37-143">MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="2ef37-143">MED-V\_HostAgent\_Setup.exe.</span></span>

**<span data-ttu-id="2ef37-144">MED-V 작업 영역 설치 파일</span><span class="sxs-lookup"><span data-stu-id="2ef37-144">The MED-V Workspace Installation Files</span></span>**

<span data-ttu-id="2ef37-145">MED-V 작업 영역 설치 파일은 다음과 같이 구성 된 MED-V 작업 영역 패키지를 빌드할 때 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-145">The MED-V workspace installation files are created when you build your MED-V workspace package that consists of the following:</span></span>

<span data-ttu-id="2ef37-146">MED-V 작업 영역 설치를 실행 하는 setup.exe 실행 프로그램</span><span class="sxs-lookup"><span data-stu-id="2ef37-146">A setup.exe executable program that executes the MED-V workspace installation</span></span>

<span data-ttu-id="2ef37-147">&lt;Med-v \ _workspace \ _name &gt; .msi 설치 관리자</span><span class="sxs-lookup"><span data-stu-id="2ef37-147">A &lt;MED-V\_workspace\_name&gt;.msi installer</span></span>

<span data-ttu-id="2ef37-148">&lt; &gt; 압축 된 가상 하드 디스크인 VHD \ _filename medv 파일</span><span class="sxs-lookup"><span data-stu-id="2ef37-148">A &lt;VHD\_filename&gt;.medv file, which is the compressed virtual hard disk</span></span>

<span data-ttu-id="2ef37-149">구성 설정 파일 ( &lt; 작업 영역 \ _name &gt; .reg 및 &lt; workspace \ _name &gt; . ps1)</span><span class="sxs-lookup"><span data-stu-id="2ef37-149">The files for configuration settings (&lt;workspace\_name&gt;.reg and &lt;workspace\_name&gt;.ps1)</span></span>

<span data-ttu-id="2ef37-150">MED-V를 배포 하려면 필요한 모든 설치 파일을 호스트 컴퓨터 또는 호스트 컴퓨터에서 액세스할 수 있는 공유에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-150">To deploy MED-V, copy all the required installation files to the host computer or to a share that can be accessed by the host computer.</span></span> <span data-ttu-id="2ef37-151">Windows 가상 PC, MED-V 호스트 에이전트, MED-V 작업 영역에 대 한 구성 요소 설치 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-151">Run the component installation files for Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span> <span data-ttu-id="2ef37-152">그런 다음 MED-V 호스트 에이전트를 시작 하 여 MED-V의 첫 번째 설정을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-152">Then start the MED-V Host Agent to complete the first time setup of MED-V.</span></span>

<span data-ttu-id="2ef37-153">수동으로 설치를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-153">You can perform the installation manually.</span></span> <span data-ttu-id="2ef37-154">그러나 전자 소프트웨어 배포 방법을 사용 하 여 구성 요소의 배포를 자동화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-154">However, we recommend that you use an electronic software distribution method to automate the deployment of the components.</span></span> <span data-ttu-id="2ef37-155">자세한 내용은 [전자 소프트웨어 배포 시스템을 통해 Med-v 작업 영역을 배포 하는 방법을](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-155">For more information, see [How to Deploy a MED-V Workspace Through an Electronic Software Distribution System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span></span>

**<span data-ttu-id="2ef37-156">참고</span><span class="sxs-lookup"><span data-stu-id="2ef37-156">Note</span></span>**  
<span data-ttu-id="2ef37-157">설치 옵션을 제어 하는 데 사용할 수 있는 명령줄 인수에 대 한 자세한 내용은 [Med-v 설치 파일의 명령줄 옵션](command-line-options-for-med-v-installation-files.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-157">For information about available command-line arguments to control install options, see [Command-Line Options for MED-V Installation Files](command-line-options-for-med-v-installation-files.md).</span></span>



## <span data-ttu-id="2ef37-158">배포 단계</span><span class="sxs-lookup"><span data-stu-id="2ef37-158">Deployment Steps</span></span>


<span data-ttu-id="2ef37-159">엔터프라이즈 전체에 MED-V를 배포 하는 경우 설치 및 최초 설정에는 두 가지 주요 고려 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-159">When you deploy MED-V throughout your enterprise, there are two main considerations: installation and first time setup.</span></span>

### <span data-ttu-id="2ef37-160">설치</span><span class="sxs-lookup"><span data-stu-id="2ef37-160">Installation</span></span>

1.  <span data-ttu-id="2ef37-161">**Windows 가상 PC** -설치 하는 동안 med-v는 WINDOWS 가상 Pc와 windows 7 (KB977206)에 대 한 필수 업데이트를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-161">**Windows Virtual PC** - During installation, MED-V checks for Windows Virtual PC and its required update for Windows 7 (KB977206).</span></span> <span data-ttu-id="2ef37-162">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-162">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    <span data-ttu-id="2ef37-163">MED-V를 설치 하기 전에 Windows 7 설치의 일부로 이러한 항목을 설치 하거나 MED-V 배포의 일부로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-163">You can install these as part of the Windows 7 installations before you install MED-V, or you can install them as part of the MED-V distribution.</span></span> <span data-ttu-id="2ef37-164">그러나 MED-V에는 해당 배포에 대 한 메커니즘이 포함 되어 있지 않습니다. ESD (전자 소프트웨어 배포) 시스템을 사용 하거나 Windows 7 이미지의 일부로 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-164">However, MED-V does not include a mechanism for their deployment; they must be deployed by using an electronic software distribution (ESD) system or as part of the Windows 7 image.</span></span>

    **<span data-ttu-id="2ef37-165">중요</span><span class="sxs-lookup"><span data-stu-id="2ef37-165">Important</span></span>**  
    <span data-ttu-id="2ef37-166">배치 파일을 사용 하 여 MED-V 구성 요소를 설치 하는 경우에는 MED-V 호스트 에이전트 및 MED-V 작업 영역 패키지 파일 뒤에 Windows 가상 PC 및 Windows 가상 PC 핫픽스가 설치 되도록 지정 하는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-166">When you install the MED-V components by using a batch file, a best practice is to specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="2ef37-167">즉, Windows Update는 다시 시작을 요구 하 여 설치 프로세스에 간섭이 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-167">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. <span data-ttu-id="2ef37-168">**Med-v 호스트 에이전트** – med-v가 실행 되는 Windows 7 컴퓨터에 Med-v 호스트 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-168">**MED-V Host Agent** – Install the MED-V Host Agent on the Windows 7 computer where MED-V will be run.</span></span> <span data-ttu-id="2ef37-169">MED-V 작업 영역을 설치 하기 전에이를 설치 하 고 Windows 가상 PC가 설치 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-169">This must be installed before installing the MED-V workspace and checks to make sure that Windows Virtual PC is installed.</span></span>

3. <span data-ttu-id="2ef37-170">**Med-v 작업 영역** – Med-v 작업 영역 포장기를 사용 하 여이 설치에 필요한 파일 (setup.exe, medv, .msi 파일)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-170">**MED-V workspace** – You create the files that are required in this installation by using the MED-V Workspace Packager: the setup.exe, .medv, and .msi files.</span></span> <span data-ttu-id="2ef37-171">MED-V 작업 영역을 설치 하려면 setup.exe를 실행 합니다. 이렇게 하면 다른 파일이 필요에 따라 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-171">To install the MED-V workspace, run setup.exe; this triggers the other files as required.</span></span> <span data-ttu-id="2ef37-172">설치는 Windows가 시작 될 때 항상 MED-V를 실행 하는 MED-V 호스트 에이전트를 시작 하는 로컬 컴퓨터 실행 키 아래에 레지스트리의 항목을 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-172">The installation places an entry in the registry under the local machine run key to start the MED-V Host Agent, which always runs MED-V when Windows is started.</span></span>

   **<span data-ttu-id="2ef37-173">중요</span><span class="sxs-lookup"><span data-stu-id="2ef37-173">Important</span></span>**  
   <span data-ttu-id="2ef37-174">MED-V 작업 영역의 설치는 최종 사용자가 대화형으로 실행 하거나 전자 소프트웨어 배포 시스템을 통해 자동으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-174">The installation of the MED-V workspace can be run interactively by the end user or silently through an electronic software distribution system.</span></span> <span data-ttu-id="2ef37-175">MED-V 작업 영역 설치에는 관리 자격 증명이 필요 하므로 최종 사용자가 MED-V 작업 영역을 설치 하려면 컴퓨터의 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-175">Installation of the MED-V workspace requires administrative credentials, so end users must be administrators of their computers to install the MED-V workspace.</span></span> <span data-ttu-id="2ef37-176">또는 전자 소프트웨어 배포 시스템은 일반적으로 시스템 컨텍스트에서 실행 되며 충분 한 사용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-176">Alternately, an electronic software distribution system typically runs in the system context and has sufficient permissions.</span></span>



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### <span data-ttu-id="2ef37-177">처음 설치 시</span><span class="sxs-lookup"><span data-stu-id="2ef37-177">First Time Setup</span></span>

<span data-ttu-id="2ef37-178">MED-V와 필수 구성 요소가 설치 된 후에는 MED-V를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-178">After MED-V and its required components are installed, MED-V must be configured.</span></span> <span data-ttu-id="2ef37-179">MED-V 구성을 처음 설정 하는 것으로 알려져 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-179">The configuration of MED-V is known as first time setup.</span></span> <span data-ttu-id="2ef37-180">**Med-v 작업 영역 포장기**를 사용 하 여 처음으로 자동 또는 대화형으로 실행 되도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-180">By using the **MED-V Workspace Packager**, you can configure first time setup to run silently or interactively.</span></span> <span data-ttu-id="2ef37-181">MED-V를 처음 설정 하는 경우에는 사용자가 MED-V 작업 영역에 대 한 인증을 위해 사용자의 암호를 입력 해야 하지만, 그렇지 않은 경우에는 거의 보이지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-181">First time setup of MED-V requires end users to enter their password to authenticate to the MED-V workspace, but otherwise can be almost invisible to the user.</span></span> <span data-ttu-id="2ef37-182">알림은 처음 설치를 완료 하 고 응용 프로그램을 사용할 수 있는 경우와 같이 알림 영역에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-182">Notifications are shown in the notification area, such as when first time setup is complete and applications are ready.</span></span> <span data-ttu-id="2ef37-183">다음은 MED-V를 처음 설정할 때 발생 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-183">The following are the actions that occur during first time setup of MED-V:</span></span>

1.  <span data-ttu-id="2ef37-184">가상 하드 디스크를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-184">The virtual hard disk must be configured.</span></span> <span data-ttu-id="2ef37-185">최소 설정이 실행 되 고 Windows XP 이미지가 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-185">Mini-Setup runs and expands the Windows XP image.</span></span> <span data-ttu-id="2ef37-186">일반적으로이는 숨겨진 창에서 발생 하지만 MED-V는이 구성 중에 표시 되도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-186">Typically, this occurs in a hidden window, but MED-V can be configured to display during this configuration.</span></span>

2.  <span data-ttu-id="2ef37-187">최소 설정이 완료 되 면 ESD 소프트웨어나 다른 응용 프로그램 설치, 이미지 구성 등 추가 구성에 필요한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-187">After Mini-Setup finishes, you can run commands that you must have for additional configuration, such as installing ESD software or other applications, or configuring the image.</span></span> <span data-ttu-id="2ef37-188">이는 Sysprep.inf 파일에서 호출할 수 있지만 필요 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-188">These can be called in the Sysprep.inf file, but are not required there.</span></span> <span data-ttu-id="2ef37-189">자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-189">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

3.  <span data-ttu-id="2ef37-190">Ftscompletion.exe는 구성의 마지막 단계로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-190">Ftscompletion.exe is run as the last step in configuration.</span></span> <span data-ttu-id="2ef37-191">이 프로세스는 MED-V 구성을 완료 하 고, MED-V 작업 영역에 액세스 하 고, 로그를 복사 하 고, med-v 작업 영역이 준비 되었음을 알리는 신호를 허용 하 고, MED-V 작업 영역을 다시 시작 하도록 RDP 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-191">This process completes the MED-V configuration, adds the user to the RDP group to let them access the MED-V workspace, copies logs, signals MED-V that the MED-V workspace is ready, and then restarts the MED-V workspace.</span></span> <span data-ttu-id="2ef37-192">이 프로세스는 MED-V 작업 영역을 만들 때이를 구성한 경우 MED-V 작업 영역의 관리자로 사용자를 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-192">This process can also add the user as an administrator of the MED-V workspace if this was configured when the MED-V workspace was created.</span></span> <span data-ttu-id="2ef37-193">Ftscompletion.exe는 일반적으로 Sysprep, inf 파일을 통해 호출 되지만, 스크립트와 같은 다른 메서드를 통해 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-193">Ftscompletion.exe is typically called through the Sysprep,inf file but can also be run through another method, such as a script.</span></span> <span data-ttu-id="2ef37-194">그러나 Ftscompletion.exe는 워크스테이션이 구성 되었을 때 수행 되는 마지막 동작 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-194">However, Ftscompletion.exe must be the last action that is performed when the workstation is configured.</span></span> <span data-ttu-id="2ef37-195">자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef37-195">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

4.  <span data-ttu-id="2ef37-196">Ftscompletion.exe에 의해 MED-V 작업 영역이 다시 시작 되 면 최종 사용자가 로그온 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-196">After the MED-V workspace is restarted by Ftscompletion.exe, the end user is logged on.</span></span> <span data-ttu-id="2ef37-197">처음 설정 하는 동안 암호를 저장 하지 않은 경우 다시 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-197">If they did not save their password during first time setup, they are prompted for it again.</span></span> <span data-ttu-id="2ef37-198">그런 다음 MED-V 작업 영역이 시작 되 고 사용자 용으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-198">The MED-V workspace is then started and configured for the user.</span></span> <span data-ttu-id="2ef37-199">구성에는 그룹 정책 적용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-199">Configuration includes applying Group Policy.</span></span>

    <span data-ttu-id="2ef37-200">Windows XP에 대 한 응용 프로그램 호환성 환경에 적합 한 정책만 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-200">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="2ef37-201">예를 들어 데스크톱 개인 설정 정책은 일반적으로 적용할 필요가 없으며 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-201">For example, desktop personalization policies do not typically need to be applied and should be disabled.</span></span> <span data-ttu-id="2ef37-202">로컬 프로필만 허용 하는 방법에 대 한 자세한 내용은 [로밍 사용자 프로필 ()에 대 한 그룹 정책 설정](https://go.microsoft.com/fwlink/?LinkId=205072) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="2ef37-202">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

<span data-ttu-id="2ef37-203">처음 설치를 완료 한 후 최종 사용자에 게는 게시 된 응용 프로그램이 준비 되었다는 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-203">After first time setup is complete, the end user is notified that the published applications are ready.</span></span> <span data-ttu-id="2ef37-204">그런 다음 **시작** 메뉴에서 med-v 작업 영역에 설치 된 응용 프로그램에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef37-204">They are then able to access the applications installed in the MED-V workspace from their **Start** menu.</span></span>

## <span data-ttu-id="2ef37-205">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2ef37-205">Related topics</span></span>


[<span data-ttu-id="2ef37-206">MED-V 배포 환경 준비</span><span class="sxs-lookup"><span data-stu-id="2ef37-206">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

[<span data-ttu-id="2ef37-207">MED-V 배포</span><span class="sxs-lookup"><span data-stu-id="2ef37-207">Deployment of MED-V</span></span>](deployment-of-med-v.md)









