---
title: 경계 네트워크에 대한 인터넷 연결 서버 시나리오
description: 경계 네트워크에 대한 인터넷 연결 서버 시나리오
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816283"
---
# <span data-ttu-id="63a5c-103">경계 네트워크에 대한 인터넷 연결 서버 시나리오</span><span class="sxs-lookup"><span data-stu-id="63a5c-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="63a5c-104">App-v 4.5는 회사 네트워크에 연결 되어 있지 않거나 네트워크 연결을 끊는 사용자가 여전히 App-v를 사용할 수 있는 인터넷 지향 서버 시나리오를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="63a5c-105">다음 그림에 표시 된 대로 인터넷 (RTSPS 및 HTTPS)의 보안 프로토콜 사용만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![앱-v 방화벽 위치 지정 다이어그램](images/appvfirewalls.gif)

<span data-ttu-id="63a5c-107">다음과 같은 방법으로 내부 네트워크 상에 서 App-v 인프라가 있는 ISA 서버를 사용 하 여 인터넷 연결 솔루션을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="63a5c-108">.ICO 및 OSD 파일을 호스트 하는 IIS 서버와 내부 네트워크에 있는 선택적으로 스트리밍을 위한 패키지 등의 웹 게시 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="63a5c-109">자세한 단계는에 제공 됩니다 <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="63a5c-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="63a5c-110">RTSPS (앱-V 웹 관리 서버)에 대 한 서버 게시 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="63a5c-111">자세한 단계는에 제공 됩니다 [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="63a5c-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="63a5c-112">다음 그림에 표시 된 대로 인프라에서 클라이언트와 ISA Server 사이 또는 ISA Server와 내부 네트워크 간에 다른 방화벽을 구현한 경우, 트래픽 흐름을 지원 하기 위해 RTSPS (TCP 322) 및 HTTPS (TCP 443) 방화벽 규칙을 모두 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="63a5c-113">또한 ISA Server와 내부 네트워크 간에 방화벽이 구현 된 경우 도메인 구성원에 필요한 기본 트래픽은 방화벽 (DNS, LDAP, Kerberos, SMB/CIFS)을 통해 터널링 될 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![앱-v 경계 네트워크 방화벽 다이어그램](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="63a5c-115">방화벽 솔루션은 환경 마다 다르기 때문에이 항목에 제공 되는 지침에서는 주변 네트워크에서 인터넷 연결 App-v 환경을 구성 하는 데 필요한 트래픽에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="63a5c-116">이 정보에는 권장 되는 내부 네트워크 서버도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="63a5c-117">주변 네트워크에 다음 서버를 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="63a5c-118">App-v 관리 서버</span><span class="sxs-lookup"><span data-stu-id="63a5c-118">App-V Management Server</span></span>

-   <span data-ttu-id="63a5c-119">게시 및 스트리밍을 위한 IIS 서버</span><span class="sxs-lookup"><span data-stu-id="63a5c-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="63a5c-120">**참고**  관리 서버와 IIS 서버를 별도의 컴퓨터에 배치 하는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="63a5c-121">내부 네트워크에 다음 서버를 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="63a5c-122">콘텐츠 서버</span><span class="sxs-lookup"><span data-stu-id="63a5c-122">Content server</span></span>

-   <span data-ttu-id="63a5c-123">데이터 저장소 (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="63a5c-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="63a5c-124">Active Directory 도메인 컨트롤러</span><span class="sxs-lookup"><span data-stu-id="63a5c-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="63a5c-125">트래픽 요구 사항</span><span class="sxs-lookup"><span data-stu-id="63a5c-125">Traffic Requirements</span></span>


<span data-ttu-id="63a5c-126">다음 표에는 인터넷 및 경계 네트워크와 주변 네트워크에서 내부 네트워크로 통신 하기 위한 트래픽 요구 사항이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63a5c-127">인터넷에서 주변 네트워크 까지의 트래픽 요구 사항</span><span class="sxs-lookup"><span data-stu-id="63a5c-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="63a5c-128">세부 정보</span><span class="sxs-lookup"><span data-stu-id="63a5c-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63a5c-129">RTSPS (게시 새로 고침 및 스트리밍 패키지)</span><span class="sxs-lookup"><span data-stu-id="63a5c-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-130">기본적으로 TCP 322 App-v 관리 서버에서 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63a5c-131">HTTPS (.ICO 및 OSD 파일 및 스트리밍 패키지 게시)</span><span class="sxs-lookup"><span data-stu-id="63a5c-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-132">기본적으로 TCP 443 이는 IIS 구성에서 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63a5c-133">경계 네트워크에서 내부 네트워크 까지의 트래픽 요구 사항</span><span class="sxs-lookup"><span data-stu-id="63a5c-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="63a5c-134">세부 정보</span><span class="sxs-lookup"><span data-stu-id="63a5c-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63a5c-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="63a5c-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-136">TCP 1433은 기본값으로, SQL Server에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a5c-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63a5c-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="63a5c-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-138">콘텐츠 디렉터리가 관리 서버 (들) 또는 IIS 서버에서 원격으로 있는 경우 (권장)</span><span class="sxs-lookup"><span data-stu-id="63a5c-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63a5c-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="63a5c-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-140">TCP 및 UDP 88</span><span class="sxs-lookup"><span data-stu-id="63a5c-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63a5c-141">DAP</span><span class="sxs-lookup"><span data-stu-id="63a5c-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-142">TCP 및 UDP 389</span><span class="sxs-lookup"><span data-stu-id="63a5c-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63a5c-143">DNS</span><span class="sxs-lookup"><span data-stu-id="63a5c-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="63a5c-144">내부 리소스의 이름 확인 (외곽 네트워크 서버에서 호스트의 파일을 사용 하 여 제거할 수 있음)</span><span class="sxs-lookup"><span data-stu-id="63a5c-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





