---
title: 전자 소프트웨어 배포 기반 시나리오 개요
description: 전자 소프트웨어 배포 기반 시나리오 개요
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821598"
---
# <span data-ttu-id="ce46e-103">전자 소프트웨어 배포 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="ce46e-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="ce46e-104">ESD (전자 소프트웨어 배포) 솔루션을 사용 하 여 가상 응용 프로그램을 배포 하려는 경우에는 해당 결정에 영향을 주는 요소를 이해 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="ce46e-105">이 항목에서는 ESD 기반 시나리오를 사용 하는 경우의 이점에 대해 설명 하 고 배포를 진행할 때 고려해 야 하는 게시 및 패키지 스트리밍 메서드에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="ce46e-106">**중요**  사용 하는 ESD 솔루션에 따라 특정 솔루션의 요구 사항에 대해 잘 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="ce46e-107">Microsoft Endpoint Configuration Manager를 사용 하는 경우에는에서 Configuration Manager 설명서를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="ce46e-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="ce46e-108">기존 ESD 시스템을 사용 하면 다음과 같은 이점을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="ce46e-109">듀얼 관리 인프라를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="ce46e-110">추가 하드웨어 비용 감소</span><span class="sxs-lookup"><span data-stu-id="ce46e-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="ce46e-111">추가 운영 체제 및 데이터베이스 라이선스의 비용 감소</span><span class="sxs-lookup"><span data-stu-id="ce46e-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="ce46e-112">게시 방법</span><span class="sxs-lookup"><span data-stu-id="ce46e-112">Publishing Methods</span></span>


<span data-ttu-id="ce46e-113">ESD 기반 시나리오를 사용 하는 경우 클라이언트에 응용 프로그램을 게시할 때 다음과 같은 옵션을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="ce46e-114">독립 실행형 Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ce46e-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="ce46e-115">Windows Installer 파일에는 클라이언트가 패키지를 구성 하는 데 사용 하는 매니페스트와 OSD 및 .ICO 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="ce46e-116">또한이 시나리오는 서버를 사용 하지 않으므로 Windows Installer 파일은 SFT 파일을 클라이언트에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="ce46e-117">패키지 매니페스트를 사용 하는 Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ce46e-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="ce46e-118">Windows Installer 파일에는 클라이언트가 패키지를 구성 하는 데 사용 하는 매니페스트와 OSD 및 .ICO 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="ce46e-119">SFT 파일은 서버에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="ce46e-120">명령줄 매개 변수는 클라이언트를 SFT 파일의 위치로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="ce46e-121">SFTMIME 명령</span><span class="sxs-lookup"><span data-stu-id="ce46e-121">SFTMIME commands.</span></span>** <span data-ttu-id="ce46e-122">SFTMIME 명령은 매니페스트, OSD, .ICO 및 SFT 파일과 함께 사용 되어 클라이언트에 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="ce46e-123">매니페스트 파일은 클라이언트 컴퓨터에 있거나 UNC 경로를 통해 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="ce46e-124">클라이언트 구성과 명령줄 옵션에 따라 OSD, .ICO 및 SFT 파일은 클라이언트 컴퓨터 또는 서버에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="ce46e-125">앞의 게시 방법에 대 한 자세한 내용은 [게시 방법 결정](determine-your-publishing-method.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce46e-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="ce46e-126">패키지 스트리밍 메서드</span><span class="sxs-lookup"><span data-stu-id="ce46e-126">Package Streaming Methods</span></span>


<span data-ttu-id="ce46e-127">응용 프로그램 가상화 시스템에서 서버에서 클라이언트로 클라이언트에 게 가상 응용 프로그램 패키지 또는 SFT 파일을 스트리밍하는 데 사용할 방법을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="ce46e-128">사용할 수 있는 스트리밍 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="ce46e-129">Application Virtualization 스트리밍 서버.</span><span class="sxs-lookup"><span data-stu-id="ce46e-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="ce46e-130">구성에서 응용 프로그램 가상화 스트리밍 서버를 사용 하는 경우 SFT 파일이 RTSP 또는 RTSPS 프로토콜을 사용 하 여 해당 서버의 클라이언트로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="ce46e-131">컴퓨터에 서버 소프트웨어를 설치 하 고 레지스트리를 통해 구성 해야 하지만이 구성은 SQL 또는 Active Directory 도메인 서비스와 같은 서비스에 종속 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="ce46e-132">SFT 파일은 클라이언트가 액세스할 수 있는 위치에 있는 서버에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="ce46e-133">배포 메커니즘을 통해 게시 정보를 클라이언트에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="ce46e-134">그러나 구성 되 면 클라이언트는 자동으로 패키지 업그레이드를 받고 활성 업그레이드가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="ce46e-135">응용 프로그램 가상화 관리 서버.</span><span class="sxs-lookup"><span data-stu-id="ce46e-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="ce46e-136">구성에서 응용 프로그램 가상화 관리 서버를 사용 하는 경우 SFT 파일이 RTSP 또는 RTSPS 프로토콜을 사용 하 여 해당 서버의 클라이언트로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="ce46e-137">응용 프로그램 가상화 관리 콘솔을 통해이 서버를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="ce46e-138">이 구성은 SQL 데이터베이스와 Active Directory 서비스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="ce46e-139">서버에서 게시 정보를 클라이언트에 배포할 수 있으므로 추가 게시 메커니즘이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="ce46e-140">파일 서버.</span><span class="sxs-lookup"><span data-stu-id="ce46e-140">File server.</span></span>** <span data-ttu-id="ce46e-141">구성에서 파일 서버를 사용 하는 경우, SFT 파일은 SMB 프로토콜을 사용 하 여 다른 클라이언트 컴퓨터로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="ce46e-142">이 구성에 사용 되는 파일 서버는 파일 공유 및 SFT 파일에 대 한 Acl (액세스 제어 목록)을 만들어 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="ce46e-143">클라이언트를 파일 서버의 올바른 파일로 이동 하려면 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="ce46e-144">IIS 서버.</span><span class="sxs-lookup"><span data-stu-id="ce46e-144">IIS server.</span></span>** <span data-ttu-id="ce46e-145">구성에서 IIS 서버를 사용 하는 경우 SFT 파일은 HTTP 또는 HTTPS 프로토콜을 사용 하 여 해당 서버의 클라이언트로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="ce46e-146">IIS 서버는 쉽게 구성 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="ce46e-147">IIS 서버에서 클라이언트를 올바른 파일로 보내도록 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce46e-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="ce46e-148">앞의 스트리밍 방법에 대 한 자세한 내용은 [스트리밍 방법 결정](determine-your-streaming-method.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce46e-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="ce46e-149">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ce46e-149">Related topics</span></span>


[<span data-ttu-id="ce46e-150">Application Virtualization Client 설치 관리자 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce46e-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="ce46e-151">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="ce46e-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="ce46e-152">게시 방법 결정</span><span class="sxs-lookup"><span data-stu-id="ce46e-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="ce46e-153">스트리밍 방법 결정</span><span class="sxs-lookup"><span data-stu-id="ce46e-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="ce46e-154">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="ce46e-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="ce46e-155">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="ce46e-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





