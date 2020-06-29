---
title: Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획
description: Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815868"
---
# <span data-ttu-id="fbbdf-103">Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획</span><span class="sxs-lookup"><span data-stu-id="fbbdf-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="fbbdf-104">Application virtualization 스트리밍 서버를 응용 프로그램 가상화 관리 서버 기반 구현과 함께 사용 하려는 경우에는 이미 사용 중인 모든 인프라를 활용 하 여 여러 대안 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="fbbdf-105">예를 들어 필드에 이미 서버가 있는 경우 해당 서버에 Application Virtualization \\CONTENT share를 배치 하 고 해당 콘텐츠 공유를 응용 프로그램 콘텐츠 원본으로 사용 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="fbbdf-106">예를 들어 단일 office만 있는 경우와 같이 응용 프로그램 가상화 관리 서버만 사용 하도록 선택한 경우 클라이언트는 해당 서버의 콘텐츠를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="fbbdf-107">지원 되는 옵션에는 파일 서버, IIS 서버 또는 응용 프로그램 가상화 스트리밍 서버를 사용 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="fbbdf-108">기존 파일 서버나 IIS 서버에 응용 프로그램 가상화 스트리밍 서버를 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="fbbdf-109">이러한 여러 옵션의 특성은 다음 표에 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="fbbdf-110">**참고**  활성 업그레이드 기능을 사용 하면 현재 응용 프로그램을 실행 중인 사용자에 게 영향을 주지 않고 App-v 관리 서버 또는 스트리밍 서버에 새 버전의 응용 프로그램을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="fbbdf-111">앱-V 클라이언트는 다음에 사용자가 응용 프로그램을 시작할 때 App-v 관리 서버 또는 스트리밍 서버에서 최신 버전의 응용 프로그램을 자동으로 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="fbbdf-112">이 기능에는 RTSP (S) 프로토콜을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

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
<th align="left"><span data-ttu-id="fbbdf-113">서버 유형</span><span class="sxs-lookup"><span data-stu-id="fbbdf-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="fbbdf-114">프로토콜</span><span class="sxs-lookup"><span data-stu-id="fbbdf-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="fbbdf-115">장점</span><span class="sxs-lookup"><span data-stu-id="fbbdf-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="fbbdf-116">단점</span><span class="sxs-lookup"><span data-stu-id="fbbdf-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="fbbdf-117">링크</span><span class="sxs-lookup"><span data-stu-id="fbbdf-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbbdf-118">파일 서버</span><span class="sxs-lookup"><span data-stu-id="fbbdf-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbbdf-119">SMB</span><span class="sxs-lookup"><span data-stu-id="fbbdf-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-120">\CONTENT share를 사용 하 여 기존 파일 서버를 구성 하는 간단한 저렴 한 솔루션</span><span class="sxs-lookup"><span data-stu-id="fbbdf-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-121">활성 업그레이드 없음</span><span class="sxs-lookup"><span data-stu-id="fbbdf-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="fbbdf-122">파일 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="fbbdf-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbbdf-123">IIS 서버</span><span class="sxs-lookup"><span data-stu-id="fbbdf-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbbdf-124">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="fbbdf-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-125">HTTPS 프로토콜을 사용 하 여 향상 된 보안 지원</span><span class="sxs-lookup"><span data-stu-id="fbbdf-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-126">인터넷에서 원격 컴퓨터로의 스트리밍을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-127">방화벽의 한 포트만 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-128">가용성</span><span class="sxs-lookup"><span data-stu-id="fbbdf-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-129">친숙 한 프로토콜</span><span class="sxs-lookup"><span data-stu-id="fbbdf-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-130">IIS를 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-131">활성 업그레이드 없음</span><span class="sxs-lookup"><span data-stu-id="fbbdf-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="fbbdf-132">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="fbbdf-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbbdf-133">Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="fbbdf-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbbdf-134">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="fbbdf-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-135">활성 업그레이드</span><span class="sxs-lookup"><span data-stu-id="fbbdf-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-136">RTSPS 프로토콜을 사용 하 여 향상 된 보안 지원</span><span class="sxs-lookup"><span data-stu-id="fbbdf-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-137">방화벽의 한 포트만 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-138">이중 인프라</span><span class="sxs-lookup"><span data-stu-id="fbbdf-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-139">서버 관리 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbbdf-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="fbbdf-140">Application Virtualization Streaming Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="fbbdf-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbbdf-141">Application Virtualization 관리 서버</span><span class="sxs-lookup"><span data-stu-id="fbbdf-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbbdf-142">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="fbbdf-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-143">활성 업그레이드</span><span class="sxs-lookup"><span data-stu-id="fbbdf-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-144">RTSPS 프로토콜을 사용 하 여 향상 된 보안 지원</span><span class="sxs-lookup"><span data-stu-id="fbbdf-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-145">방화벽의 한 포트만 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbbdf-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fbbdf-146">이중 인프라</span><span class="sxs-lookup"><span data-stu-id="fbbdf-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="fbbdf-147">서버 관리 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbbdf-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="fbbdf-148">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="fbbdf-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fbbdf-149">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fbbdf-149">Related topics</span></span>


[<span data-ttu-id="fbbdf-150">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="fbbdf-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="fbbdf-151">Application Virtualization 시스템 구성 요소 개요</span><span class="sxs-lookup"><span data-stu-id="fbbdf-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="fbbdf-152">Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="fbbdf-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





