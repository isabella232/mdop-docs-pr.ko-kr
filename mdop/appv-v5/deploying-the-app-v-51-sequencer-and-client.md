---
title: App-V 5.1 Sequencer 및 Client 배포
description: App-V 5.1 Sequencer 및 Client 배포
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814569"
---
# <span data-ttu-id="a0c2d-103">App-V 5.1 Sequencer 및 Client 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-103">Deploying the App-V 5.1 Sequencer and Client</span></span>


<span data-ttu-id="a0c2d-104">Microsoft App-v (Application Virtualization) 5.1 시퀀서 및 클라이언트를 사용 하 여 관리자가 가상화 된 응용 프로그램을 가상화 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-104">The Microsoft Application Virtualization (App-V) 5.1 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="a0c2d-105">클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-105">Deploy the client</span></span>


<span data-ttu-id="a0c2d-106">앱-V 5.1 클라이언트는 대상 컴퓨터에서 가상화 된 응용 프로그램을 실행 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-106">The App-V 5.1 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="a0c2d-107">클라이언트를 통해 사용자는 아이콘과 상호 작용 하 고 파일 형식을 두 번 클릭 하 여 가상화 된 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="a0c2d-108">클라이언트는 관리 서버에서 가상 응용 프로그램 콘텐츠를 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="a0c2d-109">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="a0c2d-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-51gb18030.md)

[<span data-ttu-id="a0c2d-110">App-V 5.1 Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="a0c2d-110">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)

[<span data-ttu-id="a0c2d-111">앱-V 4.6 및 앱-V 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="a0c2d-111">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## <span data-ttu-id="a0c2d-112">클라이언트 구성 설정</span><span class="sxs-lookup"><span data-stu-id="a0c2d-112">Client Configuration Settings</span></span>


<span data-ttu-id="a0c2d-113">앱-V 5.1 클라이언트는 레지스트리에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-113">The App-V 5.1 client stores its configuration in the registry.</span></span> <span data-ttu-id="a0c2d-114">레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="a0c2d-115">레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="a0c2d-116">클라이언트 구성 설정 정보</span><span class="sxs-lookup"><span data-stu-id="a0c2d-116">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

## <span data-ttu-id="a0c2d-117">ADMX 템플릿 및 그룹 정책을 사용 하 여 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="a0c2d-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="a0c2d-118">Microsoft ADMX 서식 파일을 사용 하 여 App-v 5.1 클라이언트 및 원격 데스크톱 서비스 클라이언트에 대 한 클라이언트 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.1 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="a0c2d-119">ADMX 템플릿은 기존 그룹 정책 인프라를 사용 하 여 일반적인 클라이언트 구성을 관리 하며 App-v 5.1 클라이언트 구성에 대 한 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.1 client configuration.</span></span>

<span data-ttu-id="a0c2d-120">**중요**  Microsoft 다운로드 센터에서 앱-V 5.1 ADMX 서식 파일을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-120">**Important** You can obtain the App-V 5.1 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="a0c2d-121">ADMX 서식 파일을 다운로드 하 여 설치한 후에는 그룹 정책을 관리 하는 데 사용할 컴퓨터에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="a0c2d-122">일반적으로 도메인 컨트롤러입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="a0c2d-123">다음 디렉터리에 **admx** 파일을 저장 합니다. **Windows \ \ policydefinitions**</span><span class="sxs-lookup"><span data-stu-id="a0c2d-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="a0c2d-124">**Adml** 파일을 다음 디렉터리에 저장: \*\*Windows \ \ policydefinitions \ \ &lt; 언어 디렉터리 &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="a0c2d-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="a0c2d-125">앞의 단계를 완료 한 후에는 **그룹 정책 관리** 콘솔을 사용 하 여 app-v 5.1 클라이언트 구성 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-125">After you have completed the preceding steps, you can manage the App-V 5.1 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="a0c2d-126">또한 App-v 5.1 클라이언트는 해당 구성을 레지스트리에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-126">The App-V 5.1 client also stores its configuration in the registry.</span></span> <span data-ttu-id="a0c2d-127">레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="a0c2d-128">레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="a0c2d-129">ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.1 Client 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="a0c2d-129">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="a0c2d-130">공유 콘텐츠 저장소 모드를 사용 하 여 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="a0c2d-131">App-v 5.1 공유 콘텐츠 저장소 (SCS) 모드에서는 연결 된 패키지 데이터를 로컬에 저장 하지 않고 SCS App-v 5.1 클라이언트가 가상화 된 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-131">The App-V 5.1 Shared Content Store (SCS) mode enables the SCS App-V 5.1 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="a0c2d-132">필요한 모든 가상화 된 패키지 데이터는 네트워크를 통해 전송 됩니다. 따라서 빠른 연결 환경 에서만 SCS 모드를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="a0c2d-133">RDS (원격 데스크톱 서비스) 및 표준 버전의 App-v 5.1 클라이언트는 모두 SCS 모드에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.1 client are supported with SCS mode.</span></span>

<span data-ttu-id="a0c2d-134">**중요**  앱-V 5.1 클라이언트가 SCS 모드에서 실행 되도록 구성 된 경우 App-v 5.1 패키지를 스트리밍하는 위치를 사용할 수 있어야 하 고, 그렇지 않으면 가상화 된 패키지가 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-134">**Important** If the App-V 5.1 client is configured to run in the SCS mode, the location where the App-V 5.1 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="a0c2d-135">또한, 인터넷을 통해 SCS 모드에서 App-v 5.1 클라이언트를 실행 하는 컴퓨터에는 가상화 된 응용 프로그램을 배포 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.1 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="a0c2d-136">또한 SCS는 가상화 된 패키지가 포함 된 실제 위치가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="a0c2d-137">이 모드는 App-v 5.1 클라이언트를 사용 하 여 네트워크에서 필요한 가상화 된 패키지 데이터를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-137">It is a mode that allows the App-V 5.1 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="a0c2d-138">SCS 모드는 다음과 같은 시나리오에서 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="a0c2d-139">VDI (가상 데스크톱 인프라) 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="a0c2d-140">RDS (원격 데스크톱 서비스) 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="a0c2d-141">환경에서 SCS를 사용 하려면 SCS 모드에서 실행할 App-v 5.1 클라이언트를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-141">To use SCS in your environment, you must enable the App-V 5.1 client to run in SCS mode.</span></span> <span data-ttu-id="a0c2d-142">설치 중에이 설정을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-142">This setting should be specified during installation.</span></span> <span data-ttu-id="a0c2d-143">기본적으로 클라이언트는 SCS 모드를 사용 하도록 구성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="a0c2d-144">SCS를 사용할 계획인 경우 제안 된 절차를 사용 하 여 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="a0c2d-145">그러나 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 다음 PowerShell 명령을 입력 하 여 SCS 모드에서 실행 되도록 기존 App-v 5.1 클라이언트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-145">However, you can configure an existing App-V 5.1 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.1 client:</span></span>

**<span data-ttu-id="a0c2d-146">set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="a0c2d-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="a0c2d-147">관리자가 SCS 모드 5.1 클라이언트를 실행 하는 컴퓨터에서 일부 가상 응용 프로그램을 미리 로드 하는 경우가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.1 client in SCS mode.</span></span> <span data-ttu-id="a0c2d-148">패키지를 추가, 게시 및 탑재 하는 PowerShell 명령을 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="a0c2d-149">예를 들어 패키지가 모든 컴퓨터에 미리 로드 된 경우 관리자는 PowerShell 명령을 사용 하 여 패키지를 추가, 게시 및 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="a0c2d-150">패키지는 로컬로 저장 되므로 네트워크를 통해 스트리밍할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="a0c2d-151">공유 콘텐츠 저장소 모드에서 App-V 5.1 Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="a0c2d-151">How to Install the App-V 5.1 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## <span data-ttu-id="a0c2d-152">Sequencer 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-152">Deploy the Sequencer</span></span>


<span data-ttu-id="a0c2d-153">시퀀서는 표준 응용 프로그램을 배포용 가상 패키지로 (App-v 5.1 클라이언트를 실행 하는 컴퓨터) 변환 하는 데 사용 되는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="a0c2d-154">시퀀서는 이전 시퀀싱 워크플로를 최소한으로 변경 하 여 간단 하 고 예측 가능한 변환 프로세스를 제공할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="a0c2d-155">또한 시퀀서를 사용 하 여 가상화 된 응용 프로그램의 연결을 가능 하 게 하는 응용 프로그램을 보다 쉽게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="a0c2d-156">App-v 5.1 Sequencer의 변경 목록은 [앱-v 5.1 정보](about-app-v-51.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-156">For a list of changes in the App-V 5.1 Sequencer, see [About App-V 5.1](about-app-v-51.md).</span></span>

[<span data-ttu-id="a0c2d-157">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="a0c2d-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> <span data-ttu-id="a0c2d-158">앱-V 5.1 클라이언트 및 Sequencer 로그</span><span class="sxs-lookup"><span data-stu-id="a0c2d-158">App-V 5.1 Client and Sequencer logs</span></span>


<span data-ttu-id="a0c2d-159">App-v 5.1를 사용 하는 동안 시퀀서 설치 및 작동 이벤트 문제를 해결 하는 데 도움이 되는 앱-V 5.1 Sequencer 로그 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-159">You can use the App-V 5.1 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.1.</span></span> <span data-ttu-id="a0c2d-160">**이벤트 뷰어**를 사용 하 여 Sequencer 관련 로그 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="a0c2d-161">다음 줄에는 시퀀서 관련 이벤트의 특정 경로가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="a0c2d-162">**이벤트 뷰어 \ \ 응용 프로그램 및 서비스 로그 \ \ Microsoft \\ App V**. Sequencer 관련 이벤트에는 **AppV \ _Sequencer**이 앞에 붙습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="a0c2d-163">클라이언트 관련 이벤트는 **AppV \ _Client**앞에 붙습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c2d-163">Client-related events are prepended with **AppV\_Client**.</span></span>

## <span data-ttu-id="a0c2d-164">시퀀서 및 클라이언트 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="a0c2d-164">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="a0c2d-165">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="a0c2d-165">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="a0c2d-166">App-V 5.1 계획</span><span class="sxs-lookup"><span data-stu-id="a0c2d-166">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)






 

 





