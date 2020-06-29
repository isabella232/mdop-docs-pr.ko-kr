---
title: App-V 5.0 Sequencer 및 Client 배포 계획
description: App-V 5.0 Sequencer 및 Client 배포 계획
author: dansimp
ms.assetid: 57a604ad-90e1-4d32-86bb-eafff59aa43a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8c6f7c4d717acad014f079e51a7013a57766d9ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813465"
---
# <span data-ttu-id="90f0c-103">App-V 5.0 Sequencer 및 Client 배포 계획</span><span class="sxs-lookup"><span data-stu-id="90f0c-103">Planning for the App-V 5.0 Sequencer and Client Deployment</span></span>


<span data-ttu-id="90f0c-104">Microsoft App-v (Application Virtualization) 5.0를 사용 하기 전에 App-v 5.0 sequencer, App-v 5.0 클라이언트, 선택적으로 App-v 5.0 공유 콘텐츠 저장소를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-104">Before you can start to use Microsoft Application Virtualization (App-V) 5.0, you must install the App-V 5.0 sequencer, the App-V 5.0 client, and optionally the App-V 5.0 shared content store.</span></span> <span data-ttu-id="90f0c-105">다음 섹션에서는 이러한 설치에 대 한 계획을 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-105">The following sections address planning for these installations.</span></span>

## <span data-ttu-id="90f0c-106">앱에 대 한 계획-V 5.0 sequencer 배포</span><span class="sxs-lookup"><span data-stu-id="90f0c-106">Planning for App-V 5.0 sequencer deployment</span></span>


<span data-ttu-id="90f0c-107">App-v 5.0는 시퀀싱 이라는 프로세스를 사용 하 여 가상화 된 응용 프로그램 및 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-107">App-V 5.0 uses a process called sequencing to create virtualized applications and application packages.</span></span> <span data-ttu-id="90f0c-108">시퀀싱을 위해서는 App-v 5.0 sequencer를 실행 하는 컴퓨터를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-108">Sequencing requires the use of a computer that runs the App-V 5.0 sequencer.</span></span>

<span data-ttu-id="90f0c-109">**참고**  App-V 5.0 시퀀서의 새로운 기능에 대 한 자세한 내용은 [app-v 5.0의 새로운](whats-new-in-app-v-50.md)기능에 대 한 시퀀서 섹션의 **변경 내용을** 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90f0c-109">**Note** For information about the new functionality of App-V 5.0 sequencer, see the **Changes to the sequencer** section of [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

 

<span data-ttu-id="90f0c-110">App-v 5.0 sequencer를 실행 하는 컴퓨터는 최소 시스템 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-110">The computer that runs the App-V 5.0 sequencer must meet the minimum system requirements.</span></span> <span data-ttu-id="90f0c-111">이러한 요구 사항의 목록은 [앱-V 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90f0c-111">For a list of these requirements, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="90f0c-112">원칙적으로는 가상 컴퓨터로 실행 되는 컴퓨터에 시퀀서를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-112">Ideally, you should install the sequencer on a computer running as a virtual machine.</span></span> <span data-ttu-id="90f0c-113">이를 통해 다른 응용 프로그램을 시퀀싱 하기 전에 시퀀서를 실행 하는 컴퓨터를 "clean" 상태로 쉽게 되돌릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-113">This enables you to more easily revert the computer running the sequencer to a “clean” state before sequencing another application.</span></span> <span data-ttu-id="90f0c-114">가상 컴퓨터를 사용 하 여 sequencer를 설치 하는 경우 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-114">When you install the sequencer using a virtual machine, you should perform the following steps:</span></span>

1.  <span data-ttu-id="90f0c-115">연결 된 모든 sequencer 필수 조건을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-115">Install all associated sequencer prerequisites.</span></span>

2.  <span data-ttu-id="90f0c-116">시퀀서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-116">Install the sequencer.</span></span>

3.  <span data-ttu-id="90f0c-117">환경에 대 한 "스냅샷"을 찍습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-117">Take a “snapshot” of the environment.</span></span>

<span data-ttu-id="90f0c-118">**중요**  조직의 보안 팀이 시퀀싱 프로세스 계획을 검토 하 고 승인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-118">**Important** You should have your corporate security team review and approve the sequencing process plan.</span></span> <span data-ttu-id="90f0c-119">보안상의 이유로 프로덕션 환경과는 별도의 랩에서 시퀀서 작업을 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-119">For security reasons, you should keep the sequencer operations in a lab that is separate from the production environment.</span></span> <span data-ttu-id="90f0c-120">구분 정렬은 비즈니스 요구 사항에 따라 간단 하거나 필요한 경우 포괄적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-120">The separation arrangement can be as simple or as comprehensive as necessary, based on your business requirements.</span></span> <span data-ttu-id="90f0c-121">시퀀싱 하는 컴퓨터는 완료 된 패키지를 프로덕션 서버로 복사 하기 위해 회사 네트워크에 연결할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-121">The sequencing computers must be able to connect to the corporate network to copy finished packages to the production servers.</span></span> <span data-ttu-id="90f0c-122">그러나 시퀀싱 하는 컴퓨터는 일반적으로 바이러스 백신 보호 없이 작동 하기 때문에 회사 네트워크에 보호 되지 않는 것이 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-122">However, because the sequencing computers are typically operated without antivirus protection, they must not be on the corporate network unprotected.</span></span> <span data-ttu-id="90f0c-123">예를 들어 방화벽이 나 격리 된 네트워크 세그먼트 뒤에서 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-123">For example, you might be able to operate behind a firewall or on an isolated network segment.</span></span> <span data-ttu-id="90f0c-124">격리 된 가상 네트워크를 공유 하도록 구성 되어 있는 가상 컴퓨터를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-124">You might also be able to use virtual machines that are configured to share an isolated virtual network.</span></span> <span data-ttu-id="90f0c-125">이러한 문제를 안전 하 게 해결 하려면 회사 보안 정책에 따르세요.</span><span class="sxs-lookup"><span data-stu-id="90f0c-125">Follow your corporate security policies to safely address these concerns.</span></span>

 

[<span data-ttu-id="90f0c-126">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="90f0c-126">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <span data-ttu-id="90f0c-127">앱-V 5.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="90f0c-127">Planning for App-V 5.0 client deployment</span></span>


<span data-ttu-id="90f0c-128">대상 컴퓨터에서 가상화 된 패키지를 실행 하려면 대상 컴퓨터에 App-v 5.0 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-128">To run virtualized packages on target computers, you must install the App-V 5.0 client on the target computers.</span></span> <span data-ttu-id="90f0c-129">앱-V 5.0 클라이언트는 대상 컴퓨터에서 가상화 된 응용 프로그램을 실행 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-129">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="90f0c-130">클라이언트를 통해 사용자는 아이콘과 특정 파일 형식을 조작 하 여 가상화 된 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-130">The client enables users to interact with icons and specific file types to start virtualized applications.</span></span> <span data-ttu-id="90f0c-131">클라이언트는 또한 관리 서버에서 응용 프로그램 콘텐츠를 가져와 클라이언트가 응용 프로그램을 시작 하기 전에 콘텐츠를 캐시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-131">The client also helps obtain application content from the management server and caches the content before the client starts the application.</span></span> <span data-ttu-id="90f0c-132">원격 데스크톱 서비스에 대 한 클라이언트 (RD 세션 호스트) 서버 시스템 및 다른 모든 컴퓨터에 사용 되는 App-v 5.0 클라이언트에 사용 되는 두 가지 클라이언트 유형</span><span class="sxs-lookup"><span data-stu-id="90f0c-132">There are two different client types: the client for Remote Desktop Services, which is used on Remote Desktop Session Host (RD Session Host) server systems and the App-V 5.0 client, which is used for all other computers.</span></span>

<span data-ttu-id="90f0c-133">App-v 5.0 클라이언트는 installer 명령줄을 사용 하거나 설치가 완료 된 후 PowerShell 스크립트를 사용 하 여 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-133">The App-V 5.0 client should be configured by using either the installer command line or by using a PowerShell script after the installation has been completed.</span></span>

<span data-ttu-id="90f0c-134">App-v 5.0 클라이언트 소프트웨어를 신속 하 게 배포 하기 위해 설정을 미리 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-134">The settings must be defined carefully in advance in order to expedite the deployment of the App-V 5.0 client software.</span></span> <span data-ttu-id="90f0c-135">다른 원본 위치를 사용 하도록 클라이언트를 구성 해야 하는 다른 사무실에 컴퓨터가 있는 경우 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-135">This is especially important when you have computers in different offices where the clients must be configured to use different source locations.</span></span>

<span data-ttu-id="90f0c-136">또한 클라이언트 소프트웨어를 배포 하는 방법을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-136">You must also determine how you will deploy the client software.</span></span> <span data-ttu-id="90f0c-137">각 컴퓨터에 수동으로 클라이언트를 배포할 수 있지만 대부분의 조직에서는 자동화 된 프로세스를 통해 클라이언트를 배포 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-137">Although it is possible to deploy the client manually on each computer, most organizations prefer to deploy the client through an automated process.</span></span> <span data-ttu-id="90f0c-138">대규모 조직에는 이상적인 클라이언트 배포 시스템으로 운영 하는 ESD (전자 소프트웨어 배포) 시스템을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-138">A larger organization might have an operational Electronic Software Distribution (ESD) system, which is an ideal client deployment system.</span></span> <span data-ttu-id="90f0c-139">ESD 시스템이 없는 경우 조직의 표준 소프트웨어 설치 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-139">If no ESD system exists, you can use your organization’s standard method of installing software.</span></span> <span data-ttu-id="90f0c-140">사용할 수 있는 방법에는 그룹 정책 또는 다양 한 스크립팅 기술이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-140">Possible methods include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="90f0c-141">클라이언트 컴퓨터의 수량과 다른 위치에 따라이 배포 프로세스는 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-141">Depending on the quantity and disparate locations of your client computers, this deployment process can be complex.</span></span> <span data-ttu-id="90f0c-142">모든 컴퓨터에서 올바른 구성을 사용 하 여 클라이언트가 설치 되도록 하려면 구조적 접근 방식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-142">You must use a structured approach to ensure that all computers get the client installed with the correct configuration.</span></span>

<span data-ttu-id="90f0c-143">클라이언트 최소 요구 사항의 목록은 [app-v 5.0 필수 구성 요소](app-v-50-prerequisites.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90f0c-143">For a list of the client minimum requirements see [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

[<span data-ttu-id="90f0c-144">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="90f0c-144">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

## <a href="" id="bkmk-client-coexist"></a><span data-ttu-id="90f0c-145">App-v 클라이언트 공존 계획</span><span class="sxs-lookup"><span data-stu-id="90f0c-145">Planning for App-V client coexistence</span></span>


<span data-ttu-id="90f0c-146">App-v 4.6 클라이언트를 사용 하 여 App-v 5.0 클라이언트를 나란히 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-146">You can deploy the App-V 5.0 client side by side with the App-V 4.6 client.</span></span> <span data-ttu-id="90f0c-147">클라이언트 공존 기능을 사용 하려면 app-v 5.0에서 app-v 4.6 클라이언트와 작동 하도록 구성 해야 하는 이러한 구성 파일에 대 한 특정 설정이 있으므로 배포 구성 파일 또는 사용자 구성 파일을 통해 가상화 된 응용 프로그램을 추가 하거나 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-147">Client coexistence requires that you add or publish virtualized applications by using either a deployment configuration file or a user configuration file, because there are certain settings in these configuration files that must be configured in order for App-V 5.0 to function with App-V4.6 clients.</span></span> <span data-ttu-id="90f0c-148">클라이언트나 서버 중 하나를 사용 하 여 패키지를 업그레이드 한 경우 패키지는 구성 파일을 다시 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-148">When a package is upgraded by using either the client or the server, the package must resubmit the configuration file.</span></span> <span data-ttu-id="90f0c-149">이는 해당 하는 구성 파일이 있는 패키지에 대해 적용 되므로 클라이언트 공존에 국한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-149">This is true for any package that has a corresponding configuration file, so it is not specific to client coexistence.</span></span> <span data-ttu-id="90f0c-150">그러나 패키지 업그레이드 중에 구성 파일을 제출 하지 않으면 패키지 상태가 공존 시나리오에서 예상 대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-150">However, if you do not submit the configuration file during the package upgrade, then the package state will not function as expected in coexistence scenarios.</span></span>

<span data-ttu-id="90f0c-151">App-v 5.0 동적 구성 파일은 특정 사용자를 위한 패키지를 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-151">App-V 5.0 dynamic configuration files customize a package for a specific user.</span></span> <span data-ttu-id="90f0c-152">동적 사용자 구성 (.xml) 파일이 나 동적 배포 구성 파일을 사용 하려면 먼저 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-152">You must create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use them.</span></span> <span data-ttu-id="90f0c-153">파일을 만들려면 고급 수동 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-153">To create the file it requires an advanced manual operation.</span></span>

<span data-ttu-id="90f0c-154">동적 사용자 구성 파일을 사용 하는 경우 매니페스트 파일의 확장명에 대 한 App-v 5.0 정보가 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-154">When a dynamic user configuration file is used, none of the App-V 5.0 information for the extension in the manifest file is used.</span></span> <span data-ttu-id="90f0c-155">즉, 동적 사용자 구성 파일에 매니페스트 파일의 앱-V 5.0에만 해당 하는 확장명에 대 한 모든 항목과 변경 내용 (예: 삭제 및 업데이트)이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-155">This means that the dynamic user configuration file must include everything for the extension that is specific to App-V 5.0 in the manifest file, as well as the changes that you want to make, such as, deletions and updates.</span></span> <span data-ttu-id="90f0c-156">사용자 지정 구성 파일을 만드는 방법에 대 한 자세한 내용은 [app-v 5.0 관리 콘솔을 사용 하 여 사용자 지정 구성 파일을 만드는 방법을](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90f0c-156">For more information about how to create a custom configuration file, see [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

[<span data-ttu-id="90f0c-157">앱-V 4.6 및 앱-V 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="90f0c-157">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <a href="" id="bkmk-plan-for-scs"></a><span data-ttu-id="90f0c-158">앱-V 5.0 공유 콘텐츠 저장소 (SCS) 계획</span><span class="sxs-lookup"><span data-stu-id="90f0c-158">Planning for the App-V 5.0 Shared Content Store (SCS)</span></span>


<span data-ttu-id="90f0c-159">App-v 5.0 공유 콘텐츠 저장소 모드는 app-v 5.0 클라이언트를 실행 하는 컴퓨터가 가상화 된 응용 프로그램을 실행할 수 있도록 허용 하며, 앱-V 5.0 클라이언트를 실행 하는 컴퓨터에는 어떠한 패키지 콘텐츠도 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-159">The App-V 5.0 shared content store mode allows the computer running the App-V 5.0 client to run virtualized applications and none of the package contents is saved on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="90f0c-160">가상 응용 프로그램은 클라이언트가 요청할 때만 대상 컴퓨터로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-160">Virtual applications are streamed to target computers only when requested by the client.</span></span>

<span data-ttu-id="90f0c-161">다음 목록에는 App-v 5.0 공유 콘텐츠 저장소를 사용할 때의 몇 가지 이점이 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f0c-161">The following list displays some of the benefits of using the App-V 5.0 shared content store:</span></span>

-   <span data-ttu-id="90f0c-162">앱에서 앱으로 및 다중 사용자 응용 프로그램 충돌 때문에 재발 테스트 필요성 감소</span><span class="sxs-lookup"><span data-stu-id="90f0c-162">Reduced app-to-app and multi-user application conflicts and hence a reduced need for regression testing</span></span>

-   <span data-ttu-id="90f0c-163">배포 위험 감소를 통한 가속화 된 응용 프로그램 배포</span><span class="sxs-lookup"><span data-stu-id="90f0c-163">Accelerated application deployment by reduction of deployment risk</span></span>

-   <span data-ttu-id="90f0c-164">간편한 프로필 관리</span><span class="sxs-lookup"><span data-stu-id="90f0c-164">Simplified profile management</span></span>

[<span data-ttu-id="90f0c-165">공유 콘텐츠 저장소 모드에서 App-V 5.0 Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="90f0c-165">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)






## <a href="" id="other-resources-for-the-app-v-5-0-deployment-"></a><span data-ttu-id="90f0c-166">App-v 5.0 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="90f0c-166">Other resources for the App-V 5.0 deployment</span></span>


[<span data-ttu-id="90f0c-167">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="90f0c-167">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





