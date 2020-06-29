---
title: App-V 5.0 Sequencer 및 Client 배포
description: App-V 5.0 Sequencer 및 Client 배포
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814596"
---
# <span data-ttu-id="f4530-103">App-V 5.0 Sequencer 및 Client 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-103">Deploying the App-V 5.0 Sequencer and Client</span></span>


<span data-ttu-id="f4530-104">앱-V 5.0 시퀀서 및 클라이언트를 사용 하 여 관리자가 가상화 된 응용 프로그램을 가상화 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-104">The App-V 5.0 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="f4530-105">클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-105">Deploy the client</span></span>


<span data-ttu-id="f4530-106">앱-V 5.0 클라이언트는 대상 컴퓨터에서 가상화 된 응용 프로그램을 실행 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-106">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="f4530-107">클라이언트를 통해 사용자는 아이콘과 상호 작용 하 고 파일 형식을 두 번 클릭 하 여 가상화 된 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="f4530-108">클라이언트는 관리 서버에서 가상 응용 프로그램 콘텐츠를 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="f4530-109">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="f4530-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

[<span data-ttu-id="f4530-110">App-V 5.0 Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="f4530-110">How to Uninstall the App-V 5.0 Client</span></span>](how-to-uninstall-the-app-v-50-client.md)

[<span data-ttu-id="f4530-111">앱-V 4.6 및 앱-V 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f4530-111">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <span data-ttu-id="f4530-112">클라이언트 구성 설정</span><span class="sxs-lookup"><span data-stu-id="f4530-112">Client Configuration Settings</span></span>


<span data-ttu-id="f4530-113">앱-V 5.0 클라이언트는 레지스트리에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-113">The App-V 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="f4530-114">레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="f4530-115">레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="f4530-116">클라이언트 구성 설정 정보</span><span class="sxs-lookup"><span data-stu-id="f4530-116">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

## <span data-ttu-id="f4530-117">ADMX 템플릿 및 그룹 정책을 사용 하 여 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="f4530-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="f4530-118">Microsoft ADMX 서식 파일을 사용 하 여 App-v 5.0 클라이언트 및 원격 데스크톱 서비스 클라이언트에 대 한 클라이언트 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.0 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="f4530-119">ADMX 템플릿은 기존 그룹 정책 인프라를 사용 하 여 일반적인 클라이언트 구성을 관리 하며 App-v 5.0 클라이언트 구성에 대 한 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.0 client configuration.</span></span>

<span data-ttu-id="f4530-120">**중요**  Microsoft 다운로드 센터에서 앱-V 5.0 ADMX 서식 파일을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-120">**Important** You can obtain the App-V 5.0 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="f4530-121">ADMX 서식 파일을 다운로드 하 여 설치한 후에는 그룹 정책을 관리 하는 데 사용할 컴퓨터에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="f4530-122">일반적으로 도메인 컨트롤러입니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="f4530-123">다음 디렉터리에 **admx** 파일을 저장 합니다. **Windows \ \ policydefinitions**</span><span class="sxs-lookup"><span data-stu-id="f4530-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="f4530-124">**Adml** 파일을 다음 디렉터리에 저장: \*\*Windows \ \ policydefinitions \ \ &lt; 언어 디렉터리 &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="f4530-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="f4530-125">앞의 단계를 완료 한 후에는 **그룹 정책 관리** 콘솔을 사용 하 여 app-v 5.0 클라이언트 구성 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-125">After you have completed the preceding steps, you can manage the App-V 5.0 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="f4530-126">또한 App-v 5.0 클라이언트는 해당 구성을 레지스트리에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-126">The App-V 5.0 client also stores its configuration in the registry.</span></span> <span data-ttu-id="f4530-127">레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="f4530-128">레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="f4530-129">ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="f4530-129">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="f4530-130">공유 콘텐츠 저장소 모드를 사용 하 여 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="f4530-131">App-v 5.0 공유 콘텐츠 저장소 (SCS) 모드에서는 연결 된 패키지 데이터를 로컬에 저장 하지 않고 SCS App-v 5.0 클라이언트가 가상화 된 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-131">The App-V 5.0 Shared Content Store (SCS) mode enables the SCS App-V 5.0 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="f4530-132">필요한 모든 가상화 된 패키지 데이터는 네트워크를 통해 전송 됩니다. 따라서 빠른 연결 환경 에서만 SCS 모드를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="f4530-133">RDS (원격 데스크톱 서비스) 및 표준 버전의 App-v 5.0 클라이언트는 모두 SCS 모드에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.0 client are supported with SCS mode.</span></span>

<span data-ttu-id="f4530-134">**중요**  앱-V 5.0 클라이언트가 SCS 모드에서 실행 되도록 구성 된 경우 App-v 5.0 패키지를 스트리밍하는 위치를 사용할 수 있어야 하 고, 그렇지 않으면 가상화 된 패키지가 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-134">**Important** If the App-V 5.0 client is configured to run in the SCS mode, the location where the App-V 5.0 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="f4530-135">또한, 인터넷을 통해 SCS 모드에서 App-v 5.0 클라이언트를 실행 하는 컴퓨터에는 가상화 된 응용 프로그램을 배포 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.0 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="f4530-136">또한 SCS는 가상화 된 패키지가 포함 된 실제 위치가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="f4530-137">이 모드는 App-v 5.0 클라이언트를 사용 하 여 네트워크에서 필요한 가상화 된 패키지 데이터를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-137">It is a mode that allows the App-V 5.0 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="f4530-138">SCS 모드는 다음과 같은 시나리오에서 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="f4530-139">VDI (가상 데스크톱 인프라) 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="f4530-140">RDS (원격 데스크톱 서비스) 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="f4530-141">환경에서 SCS를 사용 하려면 SCS 모드에서 실행할 App-v 5.0 클라이언트를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-141">To use SCS in your environment, you must enable the App-V 5.0 client to run in SCS mode.</span></span> <span data-ttu-id="f4530-142">설치 중에이 설정을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-142">This setting should be specified during installation.</span></span> <span data-ttu-id="f4530-143">기본적으로 클라이언트는 SCS 모드를 사용 하도록 구성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="f4530-144">SCS를 사용할 계획인 경우 제안 된 절차를 사용 하 여 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="f4530-145">그러나 App-v 5.0 클라이언트를 실행 하는 컴퓨터에 다음 PowerShell 명령을 입력 하 여 SCS 모드에서 실행 되도록 기존 App-v 5.0 클라이언트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-145">However, you can configure an existing App-V 5.0 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.0 client:</span></span>

**<span data-ttu-id="f4530-146">set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="f4530-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="f4530-147">관리자가 SCS 모드 5.0 클라이언트를 실행 하는 컴퓨터에서 일부 가상 응용 프로그램을 미리 로드 하는 경우가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.0 client in SCS mode.</span></span> <span data-ttu-id="f4530-148">패키지를 추가, 게시 및 탑재 하는 PowerShell 명령을 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="f4530-149">예를 들어 패키지가 모든 컴퓨터에 미리 로드 된 경우 관리자는 PowerShell 명령을 사용 하 여 패키지를 추가, 게시 및 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="f4530-150">패키지는 로컬로 저장 되므로 네트워크를 통해 스트리밍할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="f4530-151">공유 콘텐츠 저장소 모드에서 App-V 5.0 Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="f4530-151">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## <span data-ttu-id="f4530-152">Sequencer 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-152">Deploy the Sequencer</span></span>


<span data-ttu-id="f4530-153">시퀀서는 표준 응용 프로그램을 배포용 가상 패키지로 (App-v 5.0 클라이언트를 실행 하는 컴퓨터) 변환 하는 데 사용 되는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="f4530-154">시퀀서는 이전 시퀀싱 워크플로를 최소한으로 변경 하 여 간단 하 고 예측 가능한 변환 프로세스를 제공할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="f4530-155">또한 시퀀서를 사용 하 여 가상화 된 응용 프로그램의 연결을 가능 하 게 하는 응용 프로그램을 보다 쉽게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="f4530-156">App-v 5.0 Sequencer의 변경 목록은 [app-v 5.0의 새로운 기능](whats-new-in-app-v-50.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4530-156">For a list of changes in the App-V 5.0 Sequencer, see [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

[<span data-ttu-id="f4530-157">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="f4530-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> <span data-ttu-id="f4530-158">앱-V 5.0 클라이언트 및 Sequencer 로그</span><span class="sxs-lookup"><span data-stu-id="f4530-158">App-V 5.0 Client and Sequencer logs</span></span>


<span data-ttu-id="f4530-159">App-v 5.0를 사용 하는 동안 시퀀서 설치 및 작동 이벤트 문제를 해결 하는 데 도움이 되는 앱-V 5.0 Sequencer 로그 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-159">You can use the App-V 5.0 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="f4530-160">**이벤트 뷰어**를 사용 하 여 Sequencer 관련 로그 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="f4530-161">다음 줄에는 시퀀서 관련 이벤트의 특정 경로가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="f4530-162">**이벤트 뷰어 \ \ 응용 프로그램 및 서비스 로그 \ \ Microsoft \\ App V**. Sequencer 관련 이벤트에는 **AppV \ _Sequencer**이 앞에 붙습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="f4530-163">클라이언트 관련 이벤트는 **AppV \ _Client**앞에 붙습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-163">Client-related events are prepended with **AppV\_Client**.</span></span>

<span data-ttu-id="f4530-164">App-v 5.0 SP3에서는 일부 로그가 통합 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f4530-164">In App-V 5.0 SP3, some logs have been consolidated.</span></span> <span data-ttu-id="f4530-165">[앱-V 5.0 SP3 정보](about-app-v-50-sp3.md#bkmk-event-logs-moved)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4530-165">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <span data-ttu-id="f4530-166">시퀀서 및 클라이언트 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="f4530-166">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="f4530-167">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="f4530-167">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="f4530-168">App-V 5.0 계획</span><span class="sxs-lookup"><span data-stu-id="f4530-168">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)






 

 





