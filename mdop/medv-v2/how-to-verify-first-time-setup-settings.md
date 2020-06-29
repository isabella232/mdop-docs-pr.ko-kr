---
title: 처음 설치 설정을 확인하는 방법
description: 처음 설치 설정을 확인하는 방법
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813025"
---
# <span data-ttu-id="d27c9-103">처음 설치 설정을 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="d27c9-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="d27c9-104">설정의 첫 번째 테스트가 실행 되는 동안 또는 완료 된 후에 다음 작업을 수행 하 여 MED-V 작업 영역에서 구성한 설정을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="d27c9-105">**참고**  배포 후 엔터프라이즈에서 처음 설치의 성공적 완료를 모니터링 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 배포 모니터링](monitoring-med-v-workspace-deployments.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d27c9-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="d27c9-106">처음 설정 하는 동안 설정을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="d27c9-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="d27c9-107">처음 설정 하는 동안 다음 사항을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="d27c9-108">**무인** 모드를 지정한 경우 처음 설치를 실행 하는 동안에는 가상 컴퓨터가 표시 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="d27c9-109">유인 모드를 지정한 경우 가상 컴퓨터가 나타나고 사용자 입력이 필요한 모든 필드가 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="d27c9-110">처음으로 설치를 실행 하는 경우 가상 컴퓨터를 보면서 처음 설치 프로세스를 완전히 모니터링할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="d27c9-111">이렇게 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="d27c9-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="d27c9-112">Windows 가상 PC 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="d27c9-113">**시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **windows 가상 Pc**를 클릭 하 고 **windows 가상 pc**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="d27c9-114">아직 실행 중이지 않은 경우 MED-V를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="d27c9-115">아직 표시 되지 않으면 짧은 시간에 배포 된 MED-V 작업 영역의 이름이 있는 가상 컴퓨터가 가상 컴퓨터 목록에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="d27c9-116">MED-V 가상 컴퓨터를 두 번 클릭 하 여 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="d27c9-117">MED-V 가상 컴퓨터를 설정 하면 관찰할 수 있으며, 최소 설치 절차 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="d27c9-118">네트워크 설정, 컴퓨터 도메인 참가 정보 구성, 게스트 에이전트 구성, 개인 설정 설정, 시스템 종료 등의 다양 한 화면에서 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="d27c9-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="d27c9-119">처음으로 설치가 완료 되 면 가상 컴퓨터가 자동으로 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="d27c9-120">**참고**  설치를 계속 하는 동안 언제 든 지 가상 컴퓨터 창을 닫을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="d27c9-121">처음 설치를 완료 한 후 설정을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="d27c9-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="d27c9-122">첫 번째 설치가 성공적으로 완료 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="d27c9-123">MED-V 작업 영역이 올바르게 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="d27c9-124">Windows 가상 PC 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="d27c9-125">**시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **windows 가상 Pc**를 클릭 하 고 **windows 가상 pc**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="d27c9-126">설치 된 MED-V 작업 영역을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="d27c9-127">MED-V 작업 영역에서 가상 응용 프로그램을 이미 실행 중인 경우 가상 컴퓨터를 열기 전에 응용 프로그램을 닫으라는 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="d27c9-128">MED-V 작업 영역에서 **내 컴퓨터**를 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="d27c9-129">MED-V 작업 영역이 올바른 도메인에 가입 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="d27c9-130">조직에 해당 하는 경우 두 개의 다른 도메인을 지정 하 여 도메인 가입을 테스트 하 여 게스트 도메인이 호스트 도메인에 의해 재정의 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="d27c9-131">MED-V 작업 영역이 지정 된 도메인 조직 구성 단위에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="d27c9-132">컴퓨터 이름 마스크를 지정한 경우 새 컴퓨터 이름이 지정 된 이름과 일치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="d27c9-133">지정한 로캘 설정이 올바른지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="d27c9-134">MED-V 작업 영역에서 **시작** 을 클릭 한 다음 **제어판**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="d27c9-135">지정 된 구성 설정 (예: **날짜 및 시간** , **지역 및 언어**)을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="d27c9-136">**참고**  처음 설치 설정을 확인할 때 문제가 발생 하는 경우에는 [작업 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d27c9-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="d27c9-137">첫 번째 설정 설정이 올바른지 확인 한 후에는 다른 MED-V 작업 영역 구성을 테스트 하 여 응용 프로그램 게시 및 URL 리디렉션과 같이 의도 한 대로 작동 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="d27c9-138">MED-V 작업 영역 패키지의 모든 테스트를 완료 하 고 의도 한 대로 작동 하는지 확인 한 후에 MED-V 작업 영역을 enterprise에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d27c9-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="d27c9-139">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d27c9-139">Related topics</span></span>


[<span data-ttu-id="d27c9-140">응용 프로그램 게시를 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="d27c9-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="d27c9-141">URL 리디렉션을 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="d27c9-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="d27c9-142">MED-V 작업 영역 패키지 배포</span><span class="sxs-lookup"><span data-stu-id="d27c9-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="d27c9-143">MED-V 작업 영역 설정 관리</span><span class="sxs-lookup"><span data-stu-id="d27c9-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





