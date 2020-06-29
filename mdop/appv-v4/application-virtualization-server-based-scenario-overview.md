---
title: Application Virtualization Server 기반 시나리오 개요
description: Application Virtualization Server 기반 시나리오 개요
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822093"
---
# <span data-ttu-id="ae4cc-103">Application Virtualization Server 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="ae4cc-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="ae4cc-104">Microsoft 응용 프로그램 가상화 환경에 대해 서버 기반 배포 시나리오를 사용 하려는 경우에는 *응용 프로그램 가상화 관리 서버* 와 *응용 프로그램 가상화 스트리밍 서버의*차이점을 이해 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="ae4cc-105">이 항목에서는 이러한 차이점에 대해 설명 하 고 배포를 진행할 때 고려해 야 하는 패키지 배달 방법, 전송 프로토콜 및 외부 구성 요소에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="ae4cc-106">Application Virtualization 관리 서버</span><span class="sxs-lookup"><span data-stu-id="ae4cc-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="ae4cc-107">Application Virtualization Management Server는 게시 함수와 스트리밍 함수를 모두 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="ae4cc-108">서버는 승인 된 사용자를 위해 App-v 클라이언트에 응용 프로그램 아이콘, 바로 가기 및 파일 형식 연결을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="ae4cc-109">응용 프로그램에 대 한 사용자 요청이 수신 되 면 서버는 RTSP 또는 RTSPS 프로토콜을 사용 하는 승인 된 사용자에 게 요청 시 데이터를 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="ae4cc-110">이 서버를 사용 하는 대부분의 구성에서 하나 이상의 관리 서버가 구성 및 패키지 정보에 대 한 공통 데이터 저장소를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="ae4cc-111">응용 프로그램 가상화 관리 서버는 Active Directory 그룹을 사용 하 여 사용자 인증을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="ae4cc-112">Active Directory 도메인 서비스 외에도 이러한 서버에는 데이터베이스 및 데이터 저장소를 관리 하는 SQL Server가 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="ae4cc-113">관리 서버는 Microsoft Management Console의 스냅인 인 Application Virtualization 관리 콘솔을 통해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="ae4cc-114">응용 프로그램 가상화 관리 서버는 응용 프로그램을 필요할 때 최종 사용자에 게 스트리밍할 수 있기 때문에, 이러한 서버는 안정적인 고대역폭 Lan이 있는 시스템 구성에 이상적입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="ae4cc-115">Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="ae4cc-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="ae4cc-116">Application Virtualization 스트리밍 서버는 관리 서버에서 제공 하는 것과 동일한 스트리밍 및 패키지 업그레이드 기능을 제공 하지만 Active Directory 또는 SQL Server 요구 사항은 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="ae4cc-117">그러나 스트리밍 서버에는 게시 서비스가 없으며 라이선스 또는 계량 기능도 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="ae4cc-118">별도의 App-v 관리 서버의 게시 서비스는 App-v 스트리밍 서버와 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="ae4cc-119">App-v 스트리밍 서버는 기본 서버 구성의 스트리밍 기능을 사용 하 여 여러 위치에 응용 프로그램 가상화를 사용 하려고 하지만 모든 위치에서 App-v 관리 서버를 지 원하는 인프라를 보유 하 고 있지 않은 기업에 대 한 요구 사항을 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="ae4cc-120">응용 프로그램 가상화 스트리밍 서버는 기존 전자 소프트웨어 배포 시스템 (ESD)을 사용 하는 환경 에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="ae4cc-121">ESD를 사용 하 여 스트리밍 응용 프로그램을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="ae4cc-122">응용 프로그램 가상화 관리 서버와 달리 스트리밍 서버는 SQL 또는 관리 콘솔을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="ae4cc-123">이러한 서버는 Acl (액세스 제어 목록)을 사용 하 여 사용자 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="ae4cc-124">패키지 배달 방법</span><span class="sxs-lookup"><span data-stu-id="ae4cc-124">Package Delivery Methods</span></span>


<span data-ttu-id="ae4cc-125">응용 프로그램 가상화 서버를 게시 배달 방법으로 사용 하려는 경우 시나리오에 따라 다음과 같은 패키지 배달 방법을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="ae4cc-126">동적 패키지 배달</span><span class="sxs-lookup"><span data-stu-id="ae4cc-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="ae4cc-127">파일 패키지 배달에서 로드</span><span class="sxs-lookup"><span data-stu-id="ae4cc-127">Load from file package delivery</span></span>*

### <span data-ttu-id="ae4cc-128">동적 패키지 배달</span><span class="sxs-lookup"><span data-stu-id="ae4cc-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="ae4cc-129">동적 패키지를 전달 하는 동안 서버 (응용 프로그램 가상화 관리 서버, 응용 프로그램 가상화 스트리밍 서버 또는 IIS 서버)는 주문형 배포를 통해 가상화 된 응용 프로그램을 최종 사용자에 게 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="ae4cc-130">서버는 사용자가 응용 프로그램을 처음 시작 하려고 할 때 (요청 시)에만 가상화 된 응용 프로그램 및 패키지를 클라이언트 컴퓨터에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="ae4cc-131">서버는 응용 프로그램을 시작 하는 데 필요한 블록만 스트리밍합니다 (기본 기능 블록).</span><span class="sxs-lookup"><span data-stu-id="ae4cc-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="ae4cc-132">기본 기능 블록이 클라이언트에 게 전달 되 면 응용 프로그램이 실행 됩니다. 클라이언트가 기본 기능 블록에 포함 되지 않은 응용 프로그램 부분에 대 한 액세스 권한을 필요로 하는 경우가 아니면 클라이언트는 전체 응용 프로그램 (증분 배포)을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="ae4cc-133">이 문제가 발생 하면 클라이언트가 순서 없는 요청을 수행 하 고 보조 기능 블록이 클라이언트로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="ae4cc-134">동적 패키지 전달을 통해 신속한 응용 프로그램 실행을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="ae4cc-135">파일 패키지 배달에서 로드</span><span class="sxs-lookup"><span data-stu-id="ae4cc-135">Load from File Package Delivery</span></span>

<span data-ttu-id="ae4cc-136">파일 패키지 배달에서 로드 하는 경우 서버는 사용자가 응용 프로그램을 시작 하기 전에 가상화 된 전체 응용 프로그램 패키지를 클라이언트 컴퓨터에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="ae4cc-137">이 시나리오에서는 가상화 된 응용 프로그램이 동적 배달 모델에 사용 되는 동적, 증분 메서드 대신 전체 패키지로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="ae4cc-138">**참고**  각 배달 방법에 대해 초기 가상 응용 프로그램 배달 프로세스와 가상 응용 프로그램 업데이트 프로세스가 동일 합니다. 업데이트 된 가상 응용 프로그램 패키지가 원래 응용 프로그램 패키지를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="ae4cc-139">다음 표에서는 각 패키지 배달 방법의 장점과 단점을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4cc-140">메서드</span><span class="sxs-lookup"><span data-stu-id="ae4cc-140">Method</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-141">장점</span><span class="sxs-lookup"><span data-stu-id="ae4cc-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-142">단점</span><span class="sxs-lookup"><span data-stu-id="ae4cc-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-143">설명</span><span class="sxs-lookup"><span data-stu-id="ae4cc-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4cc-144">동적 패키지 배달</span><span class="sxs-lookup"><span data-stu-id="ae4cc-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-145">요청에 따라 응용 프로그램이 전달 되 고 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="ae4cc-146">응용 프로그램은 시작 시간을 최적화 하기 위해 점진적으로 전달 및 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="ae4cc-147">업데이트는 자동으로 클라이언트 데스크톱에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-148">서버 요구 사항으로 인해 엔터프라이즈 토폴로지의 공간이 큽니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="ae4cc-149">응용 프로그램 스트리밍은 LAN을 통해 수행 되어야 합니다. WAN을 통해 또는 서버와 클라이언트 간에 불안정 하거나 간헐적인 연결을 사용 하는 배포 시나리오를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-150">스트리밍 인프라가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="ae4cc-151">Windows Installer는 응용 프로그램 가상화 데스크톱 클라이언트 소프트웨어를 최종 사용자 컴퓨터에 배포 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="ae4cc-152">대규모 엔터프라이즈는 응용 프로그램 가상화 스트리밍 서버를 배포 지점으로 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4cc-153">파일 패키지 배달에서 로드</span><span class="sxs-lookup"><span data-stu-id="ae4cc-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-154">일반적인 엔터프라이즈 관리 방법과 일관성을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="ae4cc-155">독립 실행형 구성 시나리오를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="ae4cc-156">마이크로 지점 문제에 대 한 해결 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-157">응용 프로그램 배달과 업데이트는 주문형으로 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="ae4cc-158">응용 프로그램 배달과 업데이트는 증분 되지 않습니다. 동적 전달을 기준으로 리소스 소모를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-159">IT 조직은 종종 응용 프로그램 라이선스, 사용자 권한 부여, 인증을 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ae4cc-160">서버 관련 프로토콜 및 외부 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ae4cc-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="ae4cc-161">다음 표에는 응용 프로그램 가상화 서버 기반 시나리오에서 사용할 수 있는 서버 유형과 해당 전송 프로토콜 및 특정 서버 구성을 지 원하는 데 필요한 외부 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="ae4cc-162">또한이 표에는 보고 메커니즘과 각 서버 유형에 대 한 활성 업그레이드 메커니즘도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="ae4cc-163">이러한 시나리오는 모두 응용 프로그램 가상화 관리 서버를 사용 하기 때문에 시스템에 기본으로 제공 되는 내부 보고 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="ae4cc-164">응용 프로그램 가상화 관리 또는 응용 프로그램 가상화 스트리밍 서버를 사용 하 여 클라이언트에 패키지를 제공 하는 경우, 사용자가 클라이언트에 로그인 할 때 서버의 패키지가 자동으로 업그레이드 됩니다. IIS 서버나 파일을 사용 하 여 패키지를 클라이언트에 게 전달 하는 경우 클라이언트의 패키지를 수동으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4cc-165">서버 유형</span><span class="sxs-lookup"><span data-stu-id="ae4cc-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-166">프로토콜</span><span class="sxs-lookup"><span data-stu-id="ae4cc-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-167">외부 구성 요소 필요</span><span class="sxs-lookup"><span data-stu-id="ae4cc-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-168">보고</span><span class="sxs-lookup"><span data-stu-id="ae4cc-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="ae4cc-169">활성 업그레이드</span><span class="sxs-lookup"><span data-stu-id="ae4cc-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4cc-170">Application Virtualization 관리 서버</span><span class="sxs-lookup"><span data-stu-id="ae4cc-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-171">플레이어가</span><span class="sxs-lookup"><span data-stu-id="ae4cc-171">RTSP</span></span></p>
<p><span data-ttu-id="ae4cc-172">RTSPS</span><span class="sxs-lookup"><span data-stu-id="ae4cc-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-173">HTTPS를 사용 하는 경우 IIS 서버를 사용 하 여 .ICO 및 OSD 파일과 방화벽을 다운로드 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-174">내부</span><span class="sxs-lookup"><span data-stu-id="ae4cc-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-175">지원함</span><span class="sxs-lookup"><span data-stu-id="ae4cc-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4cc-176">Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="ae4cc-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-177">플레이어가</span><span class="sxs-lookup"><span data-stu-id="ae4cc-177">RTSP</span></span></p>
<p><span data-ttu-id="ae4cc-178">RTSPS</span><span class="sxs-lookup"><span data-stu-id="ae4cc-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-179">관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="ae4cc-180">HTTPS를 사용 하는 경우 IIS 서버를 사용 하 여 .ICO 및 OSD 파일을 다운로드 하 고 방화벽을 사용 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-181">내부</span><span class="sxs-lookup"><span data-stu-id="ae4cc-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-182">지원함</span><span class="sxs-lookup"><span data-stu-id="ae4cc-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4cc-183">IIS 서버</span><span class="sxs-lookup"><span data-stu-id="ae4cc-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="ae4cc-184">HTTP</span></span></p>
<p><span data-ttu-id="ae4cc-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="ae4cc-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-186">관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="ae4cc-187">HTTP 또는 HTTPS를 사용 하는 경우 IIS 서버를 사용 하 여 .ICO 및 OSD 파일과 방화벽을 다운로드 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-188">내부</span><span class="sxs-lookup"><span data-stu-id="ae4cc-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-189">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="ae4cc-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4cc-190">File</span><span class="sxs-lookup"><span data-stu-id="ae4cc-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-191">SMB</span><span class="sxs-lookup"><span data-stu-id="ae4cc-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-192">관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 방법이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="ae4cc-193">파일 공유 또는 스트리밍 기능이 있는 클라이언트 컴퓨터가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4cc-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-194">내부</span><span class="sxs-lookup"><span data-stu-id="ae4cc-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4cc-195">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="ae4cc-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ae4cc-196">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ae4cc-196">Related topics</span></span>


[<span data-ttu-id="ae4cc-197">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="ae4cc-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="ae4cc-198">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="ae4cc-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="ae4cc-199">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="ae4cc-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





