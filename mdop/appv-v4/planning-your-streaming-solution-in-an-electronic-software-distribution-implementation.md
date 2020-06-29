---
title: 전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획
description: 전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815858"
---
# <span data-ttu-id="36e3a-103">전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획</span><span class="sxs-lookup"><span data-stu-id="36e3a-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="36e3a-104">시스템을 사용 하 여 응용 프로그램 콘텐츠를 최종 사용자의 컴퓨터에서 사용할 수 있도록 하는 경우에는 기존에 있는 모든 인프라를 활용 하 여 여러 가지 대안 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="36e3a-105">예를 들어, ESD 시스템에 서버에 대 한 소프트웨어 배포 공유가 있는 경우 해당 서버에 응용 프로그램 가상화 \\CONTENT 공유를 배치 하 고 해당 콘텐츠 공유를 응용 프로그램 콘텐츠 원본으로 사용 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="36e3a-106">지원 되는 옵션에는 파일 서버나 IIS 서버를 사용 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="36e3a-107">기존 파일 서버나 IIS 서버에 응용 프로그램 가상화 스트리밍 서버를 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="36e3a-108">Application Virtualization 스트리밍 서버는 응용 프로그램 가상화의 활성 업그레이드 기능에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="36e3a-109">활성 업그레이드 기능을 사용 하면 현재 응용 프로그램을 실행 중인 사용자에 게 영향을 주지 않고 App-v 관리 서버 또는 스트리밍 서버에 새 버전의 응용 프로그램을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="36e3a-110">앱-V 클라이언트는 다음에 사용자가 응용 프로그램을 시작할 때 App-v 관리 서버 또는 스트리밍 서버에서 최신 버전의 응용 프로그램을 자동으로 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="36e3a-111">이 기능에는 RTSP (S) 프로토콜을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="36e3a-112">Application Virtualization 스트리밍 서버를 사용 하지 않도록 선택한 경우에는 ESD 시스템을 사용 하 여 응용 프로그램 패키지 업그레이드를 명시적으로 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="36e3a-113">**참고**  응용 프로그램에 대 한 액세스는 Active Directory 도메인 서비스의 보안 그룹을 통해 제어 되므로 각 가상 응용 프로그램에 대 한 보안 그룹을 설정 하 고 각 그룹에 추가 되는 사용자를 관리 하는 프로세스를 계획 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="36e3a-114">응용 프로그램 가상화 시스템 관리자는 Active Directory 그룹 구성원을 기반으로 하는 패키지에 대 한 액세스를 제어 하는 콘텐츠 공유 아래의 응용 프로그램 디렉터리에 Acl을 적용 하 여 이러한 Active Directory 그룹을 사용 하도록 각 스트리밍 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="36e3a-115">사용할 수 있는 스트리밍 옵션의 특성은 다음 표에 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

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
<th align="left"><span data-ttu-id="36e3a-116">서버 유형</span><span class="sxs-lookup"><span data-stu-id="36e3a-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="36e3a-117">프로토콜</span><span class="sxs-lookup"><span data-stu-id="36e3a-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="36e3a-118">장점</span><span class="sxs-lookup"><span data-stu-id="36e3a-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="36e3a-119">단점</span><span class="sxs-lookup"><span data-stu-id="36e3a-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="36e3a-120">링크</span><span class="sxs-lookup"><span data-stu-id="36e3a-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36e3a-121">파일 서버</span><span class="sxs-lookup"><span data-stu-id="36e3a-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="36e3a-122">SMB</span><span class="sxs-lookup"><span data-stu-id="36e3a-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="36e3a-123">\CONTENT share를 사용 하 여 기존 파일 서버를 구성 하는 간단한 저렴 한 솔루션</span><span class="sxs-lookup"><span data-stu-id="36e3a-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="36e3a-124">활성 업그레이드 없음</span><span class="sxs-lookup"><span data-stu-id="36e3a-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="36e3a-125">파일 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="36e3a-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36e3a-126">IIS 서버</span><span class="sxs-lookup"><span data-stu-id="36e3a-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="36e3a-127">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="36e3a-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="36e3a-128">HTTPS 프로토콜을 사용 하 여 향상 된 보안 지원</span><span class="sxs-lookup"><span data-stu-id="36e3a-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="36e3a-129">인터넷에서 원격 컴퓨터로의 스트리밍을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="36e3a-130">방화벽의 한 포트만 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="36e3a-131">가용성</span><span class="sxs-lookup"><span data-stu-id="36e3a-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="36e3a-132">친숙 한 프로토콜</span><span class="sxs-lookup"><span data-stu-id="36e3a-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="36e3a-133">IIS를 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="36e3a-134">활성 업그레이드 없음</span><span class="sxs-lookup"><span data-stu-id="36e3a-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="36e3a-135">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="36e3a-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36e3a-136">Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="36e3a-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="36e3a-137">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="36e3a-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="36e3a-138">활성 업그레이드</span><span class="sxs-lookup"><span data-stu-id="36e3a-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="36e3a-139">RTSPS 프로토콜을 사용 하 여 향상 된 보안 지원</span><span class="sxs-lookup"><span data-stu-id="36e3a-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="36e3a-140">방화벽의 한 포트만 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e3a-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="36e3a-141">이중 인프라</span><span class="sxs-lookup"><span data-stu-id="36e3a-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="36e3a-142">서버 관리 요구 사항</span><span class="sxs-lookup"><span data-stu-id="36e3a-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="36e3a-143">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="36e3a-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36e3a-144">관련 항목</span><span class="sxs-lookup"><span data-stu-id="36e3a-144">Related topics</span></span>


[<span data-ttu-id="36e3a-145">ESD 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="36e3a-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="36e3a-146">보안 및 보호 개요</span><span class="sxs-lookup"><span data-stu-id="36e3a-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="36e3a-147">전자 소프트웨어 배포를 사용하여 가상 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="36e3a-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





