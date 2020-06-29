---
title: Application Virtualization 개요
description: Application Virtualization 개요
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816063"
---
# <span data-ttu-id="2973d-103">Application Virtualization 개요</span><span class="sxs-lookup"><span data-stu-id="2973d-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="2973d-104">Microsoft App-v (Application Virtualization)를 사용 하면 응용 프로그램을 해당 컴퓨터에 직접 설치 하지 않고도 응용 프로그램을 최종 사용자 컴퓨터에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="2973d-105">이 작업은 *응용 프로그램 시퀀싱*이라고 하는 프로세스를 통해 가능 하며, 이렇게 하면 클라이언트 컴퓨터의 자체 자체 포함 가상 환경에서 각 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="2973d-106">시퀀싱 된 응용 프로그램은 서로 격리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="2973d-107">이렇게 하면 응용 프로그램 충돌이 해결 되지만 응용 프로그램이 클라이언트 컴퓨터와 계속 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="2973d-108">App-v 클라이언트는 최종 사용자가 컴퓨터에 게시 된 후 응용 프로그램을 조작할 수 있도록 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="2973d-109">클라이언트는 각 컴퓨터에서 가상화 된 응용 프로그램이 실행 되는 가상 환경을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="2973d-110">컴퓨터에 클라이언트를 설치한 후에는 최종 사용자가 가상 응용 프로그램을 실행할 수 있도록 *게시*라는 프로세스를 통해 컴퓨터에서 응용 프로그램을 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="2973d-111">게시 프로세스는 가상 응용 프로그램 아이콘 및 바로 가기를 컴퓨터 (일반적으로 Windows 바탕 화면 또는 **시작** 메뉴)에 복사 하 고 패키지 정의 및 파일 형식 연결 정보를 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="2973d-112">게시는 또한 최종 사용자의 컴퓨터에서 응용 프로그램 패키지 콘텐츠를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="2973d-113">가상 응용 프로그램 패키지 콘텐츠는 요청에 따라 클라이언트로 스트림 하 고 로컬로 캐시할 수 있도록 하나 이상의 응용 프로그램 가상화 서버에 복사 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="2973d-114">파일 서버와 웹 서버는 스트리밍 서버로도 사용할 수 있으며, 예를 들어 Microsoft 끝점 구성 관리자와 같은 전자 소프트웨어 배포 시스템을 사용 하는 경우와 같이 콘텐츠를 최종 사용자의 컴퓨터에 직접 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="2973d-115">다중 서버 구현에서 모든 스트리밍 서버에서 패키지 콘텐츠를 유지 관리 하 고 최신 상태로 유지 하려면 종합적인 패키지 관리 솔루션이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="2973d-116">조직의 규모에 따라 전세계의 모든 사용자에 게 제공 되는 가상 응용 프로그램이 여러 개 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="2973d-117">패키지를 관리 하 여 모든 사용자가 적절 한 응용 프로그램을 사용할 수 있도록 하는 것이 중요 한 이유는 어디서 든 액세스 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="2973d-118">Microsoft Application Virtualization 시스템 기능</span><span class="sxs-lookup"><span data-stu-id="2973d-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="2973d-119">다음 표에서는 Microsoft Application Virtualization 관리 시스템의 기본 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2973d-120">기능</span><span class="sxs-lookup"><span data-stu-id="2973d-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="2973d-121">함수</span><span class="sxs-lookup"><span data-stu-id="2973d-121">Function</span></span></th>
<th align="left"><span data-ttu-id="2973d-122">추가 정보</span><span class="sxs-lookup"><span data-stu-id="2973d-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2973d-123">Microsoft Application Virtualization 관리 서버</span><span class="sxs-lookup"><span data-stu-id="2973d-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-124">패키지 콘텐츠 스트리밍을 수행 하 고 바로 가기 및 파일 형식 연결을 응용 프로그램 가상화 클라이언트에 게시 하는 책임을 집니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-125">응용 프로그램 가상화 관리 서버는 활성 업그레이드, 라이선스 관리 및 보고에 사용할 수 있는 데이터베이스를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2973d-126">콘텐츠 </strong> 폴더</span><span class="sxs-lookup"><span data-stu-id="2973d-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-127">스트리밍을 위한 응용 프로그램 가상화 패키지의 위치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-128">이 폴더는 응용 프로그램 가상화 관리 서버의 공유 위치에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2973d-129">Microsoft Application Virtualization 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="2973d-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-130">이 콘솔은 Microsoft Application Virtualization 서버 관리에 사용 되는 MMC 3.0 스냅인 관리 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-131">이 도구는 Microsoft Application Virtualization server에 설치 하거나 MMC (Microsoft Management Console) 3.0과 Microsoft가 있는 별도의 워크스테이션에 배치할 수 있습니다. NETFramework 2.0이 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2973d-132">Microsoft Application Virtualization 관리 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="2973d-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-133">Application Virtualization data store에 대 한 읽기 및 쓰기 요청을 통신 하는 책임을 집니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-134">Microsoft 응용 프로그램 가상화 관리 서버 또는 Microsoft IIS (인터넷 정보 서비스)가 설치 된 별도의 컴퓨터에 관리 웹 서비스를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2973d-135">Microsoft Application Virtualization Data Store</span><span class="sxs-lookup"><span data-stu-id="2973d-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-136">응용 프로그램 가상화 인프라와 관련 된 모든 정보를 저장 해야 하는 App-v SQL Server 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-137">이 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 지정, 응용 프로그램 가상화 환경 관리를 담당 하는 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2973d-138">Microsoft Application Virtualization 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="2973d-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-139">응용 프로그램 가상화 관리 서버로 다시 연결 되는 WAN (광역 네트워크) 연결로 간주 되는 지점에서 클라이언트에 스트리밍하는 데 사용할 수 있는 응용 프로그램 가상화 패키지 호스팅을 담당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-140">이 서버는 스트리밍 기능만 포함 하며 응용 프로그램 가상화 관리 콘솔 및 응용 프로그램 가상화 관리 웹 서비스를 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2973d-141">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2973d-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-142">Sequencer는 가상 응용 프로그램 패키지를 만들기 위한 응용 프로그램 설치를 모니터링 하 고 캡처하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-143">출력은 응용 프로그램 아이콘, 패키지 정의 정보, 패키지 매니페스트 파일, 응용 프로그램 프로그램의 콘텐츠 파일을 포함 하는 sft 파일 등이 포함 된 .osd 파일로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2973d-144">Microsoft Application Virtualization 클라이언트</span><span class="sxs-lookup"><span data-stu-id="2973d-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-145">Application Virtualization 데스크톱 클라이언트 및 원격 데스크톱 서비스용 응용 프로그램 가상화 클라이언트는 가상화 된 응용 프로그램의 가상 환경을 제공 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2973d-146">Microsoft 응용 프로그램 가상화 클라이언트는 패키지 스트리밍을 캐시로, 게시 새로 고침, 전송, 응용 프로그램 가상화 서버와의 모든 조작을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2973d-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





