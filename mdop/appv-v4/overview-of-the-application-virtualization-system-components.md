---
title: Application Virtualization 시스템 구성 요소 개요
description: Application Virtualization 시스템 구성 요소 개요
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816053"
---
# <span data-ttu-id="abe70-103">Application Virtualization 시스템 구성 요소 개요</span><span class="sxs-lookup"><span data-stu-id="abe70-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="abe70-104">다음 표에서는 Microsoft Application Virtualization 관리 시스템의 기본 구성 요소에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="abe70-105">이러한 시스템 구성 요소를 배포 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 서버 기반 시나리오](application-virtualization-server-based-scenario.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="abe70-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abe70-106">구성 요소</span><span class="sxs-lookup"><span data-stu-id="abe70-106">Component</span></span></th>
<th align="left"><span data-ttu-id="abe70-107">함수</span><span class="sxs-lookup"><span data-stu-id="abe70-107">Function</span></span></th>
<th align="left"><span data-ttu-id="abe70-108">추가 정보</span><span class="sxs-lookup"><span data-stu-id="abe70-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abe70-109">Microsoft Application Virtualization 관리 서버</span><span class="sxs-lookup"><span data-stu-id="abe70-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-110">패키지 콘텐츠 스트리밍을 수행 하 고 바로 가기 및 파일 형식 연결을 응용 프로그램 가상화 클라이언트에 게시 하는 역할을 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-111">응용 프로그램 가상화 관리 서버는 활성 업그레이드, 라이선스 관리 및 보고에 사용할 수 있는 데이터베이스를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="abe70-112">콘텐츠 </strong> 폴더</span><span class="sxs-lookup"><span data-stu-id="abe70-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-113">스트리밍을 위한 응용 프로그램 가상화 패키지의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-114">이 폴더는 응용 프로그램 가상화 관리 서버의 공유 위치에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="abe70-115">폴더는 SAN (저장 영역 네트워크)에 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abe70-116">Microsoft Application Virtualization 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="abe70-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-117">Microsoft Application Virtualization 서버 관리용 MMC 3.0 스냅인 관리 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="abe70-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-118">이 구성 요소는 Microsoft Application Virtualization server에 설치 하거나 MMC 3.0 및이 있는 별도의 워크스테이션에 배치할 수 있습니다. NET 2.0이 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abe70-119">Microsoft Application Virtualization 관리 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="abe70-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-120">응용 프로그램 가상화 데이터 저장소에 대 한 읽기/쓰기 요청을 통신 하는 데 책임이 있는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-121">이 구성 요소는 Microsoft Application Virtualization Server 또는 IIS가 설치 된 별도의 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abe70-122">Microsoft Application Virtualization Data Store</span><span class="sxs-lookup"><span data-stu-id="abe70-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-123">SQL 데이터베이스에 저장 되 고 응용 프로그램 가상화 인프라와 관련 된 모든 정보를 저장 하는 역할을 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-124">이 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 지정, 응용 프로그램 가상화 환경 관리를 담당 하는 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abe70-125">Microsoft Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="abe70-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-126">응용 프로그램 가상화 관리 서버로 다시 연결 하는 WAN으로 간주 되는 지점에서 클라이언트에 스트리밍하는 응용 프로그램 가상화 패키지 호스팅을 담당 하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-127">이 서버는 스트리밍 기능만 포함 하며 응용 프로그램 가상화 관리 콘솔 및 응용 프로그램 가상화 관리 웹 서비스를 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abe70-128">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="abe70-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-129">가상 응용 프로그램 패키지를 만들기 위한 응용 프로그램 설치를 모니터링 하 고 캡처하는 데 사용 되는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-130">출력은 응용 프로그램 아이콘, 패키지 정의 정보를 포함 하는 OSD 파일, 패키지 매니페스트 파일, 응용 프로그램 프로그램의 콘텐츠 파일이 포함 된 SFT 파일 등으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abe70-131">Microsoft Application Virtualization 클라이언트</span><span class="sxs-lookup"><span data-stu-id="abe70-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-132">응용 프로그램 가상화 데스크톱 클라이언트에 설치 된 구성 요소 또는 원격 데스크톱 서비스에 대 한 Application Virtualization 클라이언트 (이전의 터미널 서비스) 및 가상화 된 응용 프로그램에 대 한 가상 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="abe70-133">Microsoft 응용 프로그램 가상화 클라이언트는 패키지 스트리밍을 캐시로, 게시 새로 고침, 전송, 응용 프로그램 가상화 서버와의 모든 조작을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="abe70-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="abe70-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="abe70-134">Related topics</span></span>


[<span data-ttu-id="abe70-135">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="abe70-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="abe70-136">Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획</span><span class="sxs-lookup"><span data-stu-id="abe70-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="abe70-137">Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="abe70-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





