---
title: 스트리밍 방법 결정
description: 스트리밍 방법 결정
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821668"
---
# <span data-ttu-id="2ad44-103">스트리밍 방법 결정</span><span class="sxs-lookup"><span data-stu-id="2ad44-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="2ad44-104">사용자가 게시 프로세스를 통해 컴퓨터에 배치 된 아이콘을 처음으로 두 번 클릭할 때 응용 프로그램 가상화 클라이언트는 스트리밍 원본 위치에서 가상 응용 프로그램 패키지 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="2ad44-105">**참고** 
 *스트리밍은* 기본 기능 블록부터 시작 하 여 필요에 따라 추가 블록을 가져와 시퀀싱 된 응용 프로그램 패키지에서 콘텐츠를 가져오는 프로세스를 설명 하는 데 사용 되는 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="2ad44-106">스트리밍 원본 위치는 일반적으로 사용자의 컴퓨터에서 액세스할 수 있는 서버입니다. 그러나 Microsoft Endpoint Configuration Manager와 같은 일부 전자 배포 시스템은 사용자의 컴퓨터에 SFT 파일을 배포한 다음 해당 컴퓨터의 캐시에서 로컬로 가상 응용 프로그램 패키지를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="2ad44-107">**참고**  서버가 아닌 컴퓨터에서 가상 패키지의 스트리밍 원본 위치를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="2ad44-108">이는 서버가 없는 작은 지점에 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="2ad44-109">다음 표에서는 시퀀싱 된 응용 프로그램을 저장 하는 데 사용할 수 있는 스트리밍 소스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

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
<th align="left"><span data-ttu-id="2ad44-110">서버 유형</span><span class="sxs-lookup"><span data-stu-id="2ad44-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="2ad44-111">프로토콜</span><span class="sxs-lookup"><span data-stu-id="2ad44-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="2ad44-112">장점</span><span class="sxs-lookup"><span data-stu-id="2ad44-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="2ad44-113">단점</span><span class="sxs-lookup"><span data-stu-id="2ad44-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="2ad44-114">링크</span><span class="sxs-lookup"><span data-stu-id="2ad44-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ad44-115">파일 서버</span><span class="sxs-lookup"><span data-stu-id="2ad44-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ad44-116">File</span><span class="sxs-lookup"><span data-stu-id="2ad44-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ad44-117">\CONTENT share를 사용 하 여 기존 파일 서버를 구성 하는 간단한 저렴 한 솔루션</span><span class="sxs-lookup"><span data-stu-id="2ad44-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ad44-118">활성 업그레이드 없음</span><span class="sxs-lookup"><span data-stu-id="2ad44-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="2ad44-119">파일 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="2ad44-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ad44-120">IIS 서버</span><span class="sxs-lookup"><span data-stu-id="2ad44-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ad44-121">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="2ad44-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ad44-122">HTTPS 프로토콜을 사용 하 여 향상 된 보안을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="2ad44-123">인터넷에서 원격 컴퓨터로의 스트리밍을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="2ad44-124">방화벽의 한 포트만 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="2ad44-125">확장성 높은</span><span class="sxs-lookup"><span data-stu-id="2ad44-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="2ad44-126">친숙 한 프로토콜</span><span class="sxs-lookup"><span data-stu-id="2ad44-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ad44-127">IIS를 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad44-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="2ad44-128">활성 업그레이드 없음</span><span class="sxs-lookup"><span data-stu-id="2ad44-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="2ad44-129">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="2ad44-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ad44-130">Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="2ad44-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ad44-131">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="2ad44-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ad44-132">활성 업그레이드</span><span class="sxs-lookup"><span data-stu-id="2ad44-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="2ad44-133">RTSPS 프로토콜을 사용 하 여 향상 된 보안 지원</span><span class="sxs-lookup"><span data-stu-id="2ad44-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="2ad44-134">방화벽의 한 포트만 열 수 있습니다 (RTSPS에만 해당).</span><span class="sxs-lookup"><span data-stu-id="2ad44-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ad44-135">이중 인프라</span><span class="sxs-lookup"><span data-stu-id="2ad44-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="2ad44-136">서버 관리 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ad44-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="2ad44-137">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="2ad44-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2ad44-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2ad44-138">Related topics</span></span>


[<span data-ttu-id="2ad44-139">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="2ad44-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="2ad44-140">전자 소프트웨어 배포 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="2ad44-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="2ad44-141">게시 방법 결정</span><span class="sxs-lookup"><span data-stu-id="2ad44-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





