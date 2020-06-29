---
title: 테스트 환경을 만드는 방법
description: 테스트 환경을 만드는 방법
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827288"
---
# <span data-ttu-id="73fea-103">테스트 환경을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="73fea-103">How to Create a Test Environment</span></span>


<span data-ttu-id="73fea-104">다음은 엔터프라이즈 전체에 MED-V 작업 영역 패키지를 배포 하기 전에 로컬로이를 테스트 하는 데 사용할 수 있는 테스트 환경을 만드는 데 도움이 되는 몇 가지 단계와 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="73fea-105">이 섹션에서는 수동 또는 전자 소프트웨어 배포 시스템을 사용 하 여 테스트 환경을 만드는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="73fea-106">ESD를 사용 하 여 테스트 환경을 만들려면</span><span class="sxs-lookup"><span data-stu-id="73fea-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="73fea-107">기업 전체에 소프트웨어를 배포 하는 회사의 방법을 사용 하 여 테스트 컴퓨터에 필요한 다음 구성 요소를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="73fea-108">다음 순서로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="73fea-109">**Windows 가상 PC** – 아직 설치 되지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="73fea-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="73fea-110">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73fea-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="73fea-111">**Windows 가상 PC 추가 및 업데이트**-아직 설치 되지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="73fea-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="73fea-112">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73fea-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="73fea-113">**Med-v 호스트 에이전트 설치 파일** – 호스트 에이전트 (Med-v-v _HostAgent \ _Setup 설치 파일)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="73fea-114">자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73fea-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="73fea-115">Med-v 작업 **영역 설치 관리자, VHD, 설치 실행 파일** – **Med-v 작업 영역 포장기**에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="73fea-116">자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73fea-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="73fea-117">**중요**  VHD 및 설치 실행 프로그램은 MED-V 작업 영역 설치 관리자와 같은 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="73fea-118">그런 다음 setup.exe를 실행 하 여 MED-V 작업 영역 설치 관리자를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="73fea-119">테스트 컴퓨터에 모든 구성 요소를 설치한 후에는 MED-V 호스트 에이전트를 실행 하 여 처음 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="73fea-120">**시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**, **med-v 호스트 에이전트**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="73fea-121">**참고**  테스트 컴퓨터에서 MED-V 호스트 에이전트를 실제로 실행할 수 없는 경우 다음에 컴퓨터가 다시 시작 될 때 설치가 처음으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="73fea-122">처음 설치를 시작 하 고 완료 하는 데 10 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="73fea-123">처음 설치를 실행할 때 구성 설정을 테스트 하는 방법에 대 한 자세한 내용은 [최초 설치 설정을 확인 하는 방법을](how-to-verify-first-time-setup-settings.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73fea-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="73fea-124">테스트 환경을 수동으로 만들려면</span><span class="sxs-lookup"><span data-stu-id="73fea-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="73fea-125">추가 및 업데이트를 포함 하는 Windows 가상 PC와 같은 MED-V 필수 구성 요소를 포함 하는 로컬 테스트 환경에 MED-V 호스트 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="73fea-126">자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73fea-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="73fea-127">MED-V 작업 영역 파일을 테스트 환경에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="73fea-128">MED-V 작업 영역 파일은 **Med-v 작업 영역 포장기**에서 지정한 대상 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="73fea-129">**중요**  VHD 및 설치 실행 프로그램은 MED-V 작업 영역 설치 관리자와 테스트 환경의 같은 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="73fea-130">setup.exe를 실행 하 여 MED-V 작업 영역을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="73fea-131">MED-V 호스트 에이전트를 실행 하 여 처음 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="73fea-132">**시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**, **med-v 호스트 에이전트**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="73fea-133">설치 프로그램이 시작 될 때 지정 된 VHD 크기에 따라 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="73fea-134">이제 MED-V 작업 영역에 대해 지정한 구성, 응용 프로그램 게시 및 URL 리디렉션에 대 한 다른 설정을 테스트할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="73fea-135">**참고**  기본적으로 MED-V는 게스트의 화면 잠금 정책을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="73fea-136">그러나 호스트 컴퓨터에서 화면 잠금 정책을 계속 해 서 준수 하기 때문에이는 보안 문제를 일으키지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73fea-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="73fea-137">관련 항목</span><span class="sxs-lookup"><span data-stu-id="73fea-137">Related topics</span></span>


[<span data-ttu-id="73fea-138">처음 설치 설정을 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="73fea-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="73fea-139">응용 프로그램 게시를 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="73fea-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="73fea-140">URL 리디렉션을 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="73fea-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 





