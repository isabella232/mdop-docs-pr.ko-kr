---
title: App-V 5.1 Server배포 계획
description: App-V 5.1 Server배포 계획
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813436"
---
# <span data-ttu-id="5fe13-103">App-V 5.1 Server배포 계획</span><span class="sxs-lookup"><span data-stu-id="5fe13-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="5fe13-104">Microsoft App-v (Application Virtualization) 5.1 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 특수화 된 기능 집합으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="5fe13-105">앱-V 5.1 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="5fe13-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="5fe13-106">App-v 5.1 서버는 다음 기능으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="5fe13-107">관리 서버-App-v 5.1 인프라에 대 한 전반적인 관리 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="5fe13-108">관리 데이터베이스 – App-v 5.1 management에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="5fe13-109">게시 서버 – 가상 응용 프로그램에 대 한 호스팅 및 스트리밍 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="5fe13-110">보고 서버-App-v 5.1 reporting services를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="5fe13-111">보고 데이터베이스-App-v 5.1 reporting에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="5fe13-112">다음 목록에는 App-v 5.1 서버 인프라를 설치 하는 데 권장 되는 방법이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="5fe13-113">App-v 5.1 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="5fe13-114">자세한 내용은 [app-v 5.1 서버를 배포 하는 방법을](how-to-deploy-the-app-v-51-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5fe13-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="5fe13-115">데이터베이스, 보고 및 관리 기능을 별도의 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="5fe13-116">자세한 내용은 관리 및 보고 [서비스와 별도의 컴퓨터에 관리 데이터베이스를 설치](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5fe13-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="5fe13-117">전자 소프트웨어 배포 (ESD)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="5fe13-118">자세한 내용은 [전자 소프트웨어 배포를 사용 하 여 app-v 5.1 패키지를 배포 하는 방법을](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5fe13-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="5fe13-119">모든 서버 기능을 단일 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="5fe13-120">App-v 5.1 서버 조작</span><span class="sxs-lookup"><span data-stu-id="5fe13-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="5fe13-121">이 섹션에는 다양 한 App-v 5.1 서버 역할이 상호 작용 하는 방법에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="5fe13-122">App-v 5.1 관리 서버에는 패키지 및 할당 된 구성의 리포지토리가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="5fe13-123">관리 서버에 등록 된 서버를 게시 하는 경우 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 게시 새로 고침 요청을 받을 때 사용할 게시 서버에 연결 된 메타 데이터가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="5fe13-124">단일 관리 서버에서 관리 하는 app-v 5.1 게시 서버는 서로 다른 클라이언트를 서비스할 수 있으며 다른 웹 사이트 이름과 포트 바인딩을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="5fe13-125">또한 동일한 관리 서버에서 관리 하는 모든 게시 서버는 서로 복제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="5fe13-126">**참고**  관리 서버는 부하 분산을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="5fe13-127">연결 된 메타 데이터는 클라이언트 요청을 처리할 때 사용할 수 있도록 게시 서버로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="5fe13-128">서버 관련 프로토콜 및 외부 기능</span><span class="sxs-lookup"><span data-stu-id="5fe13-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="5fe13-129">다음은 App-v 5.1 서버에 사용 되는 서버 관련 프로토콜에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="5fe13-130">또한이 표에는 각 서버 유형에 대 한 보고 메커니즘도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="5fe13-131">서버 유형</span><span class="sxs-lookup"><span data-stu-id="5fe13-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="5fe13-132">프로토콜</span><span class="sxs-lookup"><span data-stu-id="5fe13-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="5fe13-133">필요한 외부 기능</span><span class="sxs-lookup"><span data-stu-id="5fe13-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="5fe13-134">보고</span><span class="sxs-lookup"><span data-stu-id="5fe13-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5fe13-135">IIS 서버</span><span class="sxs-lookup"><span data-stu-id="5fe13-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fe13-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="5fe13-136">HTTP</span></span></p>
<p><span data-ttu-id="5fe13-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5fe13-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fe13-138">이 서버 프로토콜 조합에는 관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 메커니즘이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="5fe13-139">HTTP 또는 HTTPS를 사용 하는 경우 IIS 서버와 방화벽을 사용 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fe13-140">내부</span><span class="sxs-lookup"><span data-stu-id="5fe13-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5fe13-141">File</span><span class="sxs-lookup"><span data-stu-id="5fe13-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fe13-142">SMB</span><span class="sxs-lookup"><span data-stu-id="5fe13-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fe13-143">이 서버 프로토콜 조합에는 관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 지원이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="5fe13-144">파일 공유 또는 스트리밍 기능과 함께 클라이언트 컴퓨터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe13-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fe13-145">내부</span><span class="sxs-lookup"><span data-stu-id="5fe13-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="5fe13-146">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5fe13-146">Related topics</span></span>


[<span data-ttu-id="5fe13-147">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="5fe13-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="5fe13-148">App-V 5.1 Server 배포</span><span class="sxs-lookup"><span data-stu-id="5fe13-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





