---
title: Application Virtualization Client 배포 계획
description: Application Virtualization Client 배포 계획
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815953"
---
# <span data-ttu-id="429bc-103">Application Virtualization Client 배포 계획</span><span class="sxs-lookup"><span data-stu-id="429bc-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="429bc-104">가상 응용 프로그램 패키지를 최종 사용자 컴퓨터에 게시 하 고 배포 하는 방법을 결정 한 후에는 응용 프로그램 가상화 클라이언트 소프트웨어의 배포를 계획 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="429bc-105">응용 프로그램 가상화 클라이언트는 가상 응용 프로그램을 실제로 실행 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="429bc-106">응용 프로그램 가상화 클라이언트는 사용자가 아이콘과 상호 작용 하 고 파일 형식을 두 번 클릭 하 여 가상 응용 프로그램을 시작할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="429bc-107">또한 응용 프로그램을 시작 하기 전에 스트리밍 서버에서 응용 프로그램 콘텐츠의 스트리밍을 처리 하 고 캐시 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="429bc-108">응용 프로그램 콘텐츠는 응용 프로그램을 시작 하 고 초기 사용자 조작을 처리 하는 데 필요한 모든 콘텐츠가 최종 사용자 컴퓨터에 먼저 스트리밍되는지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="429bc-109">Application Virtualization 클라이언트 소프트웨어에는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 응용 프로그램 가상화 클라이언트 (원격 데스크톱 세션 호스트 (RDSession Host) 서버 시스템 및 다른 모든 컴퓨터에 사용 되는 Application Virtualization 데스크톱 클라이언트에서 사용 됨)의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="429bc-110">응용 프로그램 가상화 클라이언트는 응용 프로그램 가상화 관리 콘솔에서 또는 설치 시 명령줄을 통해 다음을 포함 하 여 여러 가지 중요 한 설정으로 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="429bc-111">모든 응용 프로그램에 대 한 아이콘의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="429bc-112">패키지 정의 정보를 포함 하는 OSD 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="429bc-113">응용 프로그램 콘텐츠 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-113">The application content source.</span></span>

-   <span data-ttu-id="429bc-114">이전 항목을 검색할 때 사용할 통신 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="429bc-115">사용할 캐시 크기 및 캐시 크기 관리 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="429bc-116">ESD (전자 소프트웨어 배포) 솔루션을 사용 하는 경우 응용 프로그램 가상화 클라이언트 소프트웨어를 신속 하 게 배포 하기 위해 앞의 설정을 신중 하 게 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="429bc-117">이는 서로 다른 사무실에 컴퓨터를 설치 하 고 다른 원본 위치를 사용 하도록 클라이언트를 구성 해야 하는 경우 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="429bc-118">참고</span><span class="sxs-lookup"><span data-stu-id="429bc-118">Note</span></span>**  
-   <span data-ttu-id="429bc-119">아이콘 위치 및 OSD 파일 값은 Windows Installer 또는 SFTMIME을 사용 하는지 여부에 관계 없이 게시 방법을 선택할 때 고려해 야 하는 중요 한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="429bc-120">응용 프로그램 콘텐츠 원본에 대 한 설정은 스트리밍 방법 선택에 따라 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="429bc-121">캐시에 배포할 수 있는 모든 패키지에 대해 충분 한 공간이 할당 되었는지 확인 하려면 필요에 따라 캐시를 확장할 수 있도록 클라이언트를 구성할 때 사용 **가능한 디스크 공간 임계값** 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="429bc-122">또는, App-v 캐시에 필요한 디스크 공간을 미리 결정 하 고 설치 시간에 캐시 크기를 적절 하 게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="429bc-123">캐시 공간 관리 기능에 대 한 자세한 내용은 Microsoft App-v (Application Virtualization) 운영 가이드의 **캐시 공간 관리 기능을 사용** 하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="429bc-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="429bc-124">게시 및 HTTP (S) 스트리밍 작업 중에 App-v 4.5 SP1 클라이언트는 사용자 컴퓨터의 Internet Explorer에서 구성한 프록시 서버 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="429bc-125">클라이언트 설치 매개 변수를 구성 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="429bc-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="429bc-126">마지막으로 데스크톱 클라이언트에 대 한 Application Virtualization 데스크톱 클라이언트 소프트웨어를 배포 하는 방법을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="429bc-127">각 컴퓨터에 응용 프로그램 가상화 데스크톱 클라이언트를 수동으로 배포할 수 있지만 대부분의 조직에서는 자동화 된 프로세스를 통해이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="429bc-128">중간 규모 또는 대규모 조직의 경우 운영에 ESD 시스템을 사용 하는 것 이며, 클라이언트를 배포 하는 데 이상적인 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="429bc-129">ESD 시스템이 없는 경우 조직에 소프트웨어를 설치 하는 표준 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="429bc-130">그룹 정책 또는 다양 한 스크립팅 기술이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="429bc-131">보유 하 고 있는 사무실의 수와 크기에 따라이 배포 프로세스는 복잡할 수 있으며, 모든 컴퓨터에서 올바른 구성으로 클라이언트를 설치 하도록 구조적 접근 방식을 사용 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="429bc-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="429bc-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="429bc-132">Related topics</span></span>


[<span data-ttu-id="429bc-133">Application Virtualization 시스템 배포 계획</span><span class="sxs-lookup"><span data-stu-id="429bc-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="429bc-134">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="429bc-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="429bc-135">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="429bc-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="429bc-136">Application Virtualization Client를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="429bc-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="429bc-137">App-V Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="429bc-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





