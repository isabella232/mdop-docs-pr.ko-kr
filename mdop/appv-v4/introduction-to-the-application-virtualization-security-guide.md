---
title: Application Virtualization 보안 가이드 소개
description: Application Virtualization 보안 가이드 소개
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816268"
---
# <span data-ttu-id="67dcc-103">Application Virtualization 보안 가이드 소개</span><span class="sxs-lookup"><span data-stu-id="67dcc-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="67dcc-104">이 Microsoft App-v (Application Virtualization) 보안 가이드는 App-v 배포를 위해 선택한 보안 기능을 구성 하는 관리자를 위한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="67dcc-105">**참고**  이 설명서에서는 특정 보안 옵션 선택에 대 한 지침을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="67dcc-106">이 정보는에 있는 App-v 보안 모범 사례 백서에서 제공 됩니다 <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="67dcc-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="67dcc-107">이 가이드를 사용 하는 App-v 관리자는 다음 보안 관련 기술에 대해 잘 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="67dcc-108">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="67dcc-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="67dcc-109">PKI (공개 키 인프라)</span><span class="sxs-lookup"><span data-stu-id="67dcc-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="67dcc-110">IPsec (인터넷 프로토콜 보안)</span><span class="sxs-lookup"><span data-stu-id="67dcc-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="67dcc-111">그룹 정책</span><span class="sxs-lookup"><span data-stu-id="67dcc-111">Group Policies</span></span>

-   <span data-ttu-id="67dcc-112">IIS (인터넷 정보 서비스)</span><span class="sxs-lookup"><span data-stu-id="67dcc-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="67dcc-113">앱-V 인프라 구성 요소</span><span class="sxs-lookup"><span data-stu-id="67dcc-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="67dcc-114">향상 된 보안 App-v 환경을 계획할 때 여러 다른 인프라 모델을 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="67dcc-115">**참고**  앱-V 인프라 모델에 대 한 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="67dcc-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="67dcc-116">App-v 계획 및 배포 가이드</span><span class="sxs-lookup"><span data-stu-id="67dcc-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="67dcc-117">인프라 계획 및 디자인 가이드 시리즈</span><span class="sxs-lookup"><span data-stu-id="67dcc-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="67dcc-118">이러한 모델은 다음 그림에 표시 된 것과는 다른 일부 App-v 구성 요소를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![앱-v 분기 office 다이어그램](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="67dcc-120">Application Virtualization (App-v) 관리 서버</span><span class="sxs-lookup"><span data-stu-id="67dcc-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="67dcc-121">앱-V 관리 서버는 패키지 콘텐츠를 스트리밍하 고 바로 가기 키와 파일 형식 연결을 App-v 클라이언트에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="67dcc-122">또한 App-v 관리 서버는 활성 업그레이드, 라이선스 관리 및 보고에 사용할 수 있는 데이터베이스를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="67dcc-123">Application Virtualization (App-v) 스트리밍 서버</span><span class="sxs-lookup"><span data-stu-id="67dcc-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="67dcc-124">App-v 스트리밍 서버는 App-v 관리 서버 연결의 대역폭이 클라이언트에 게 패키지 콘텐츠를 스트리밍하는 데 충분 하지 않은 지점 등의 환경에서 App-v 클라이언트로 스트리밍할 패키지를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="67dcc-125">스트리밍 서버는 스트리밍 기능만 포함 하며 app-v 관리 콘솔 또는 App-v 관리 웹 서비스를 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="67dcc-126">App-v (Application Virtualization) 데이터 저장소</span><span class="sxs-lookup"><span data-stu-id="67dcc-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="67dcc-127">SQL 데이터베이스의 App-v 데이터 저장소는 App-v 인프라와 관련 된 정보를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="67dcc-128">App-v 데이터 저장소의 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 할당, 응용 프로그램 가상화 환경을 관리 하는 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="67dcc-129">Application Virtualization (App-v) 관리 서비스</span><span class="sxs-lookup"><span data-stu-id="67dcc-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="67dcc-130">App-v 관리 서비스는 Application Virtualization data store에 대 한 읽기/쓰기 요청을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="67dcc-131">이 구성 요소는 App-v 관리 서버와 같은 컴퓨터 또는 IIS가 설치 된 별도의 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="67dcc-132">App-v (Application Virtualization) 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="67dcc-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="67dcc-133">App-v 관리 콘솔은 App-v 서버 관리용 스냅인 관리 유틸리티입니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="67dcc-134">이 구성 요소는 App-v 서버와 같은 컴퓨터 또는 MMC 3.0 및이 있는 별도의 워크스테이션에 설치할 수 있습니다. NET 2.0이 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="67dcc-135">Application Virtualization (App-v) Sequencer</span><span class="sxs-lookup"><span data-stu-id="67dcc-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="67dcc-136">App-v 시퀀서는 응용 프로그램 설치를 모니터링 하 고 캡처하여 가상 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="67dcc-137">시퀀서의 출력은 응용 프로그램 아이콘, 응용 프로그램 정의 정보를 포함 하는 OSD 파일, 패키지 매니페스트 파일, 응용 프로그램의 콘텐츠 파일을 포함 하는 SFT 파일 등으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="67dcc-138">선택적으로, App-v 인프라를 사용 하지 않고 패키지를 설치 하기 위해 Windows Installer 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="67dcc-139">Application Virtualization (App-v) 클라이언트</span><span class="sxs-lookup"><span data-stu-id="67dcc-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="67dcc-140">App-v 클라이언트가 App-v 데스크톱 클라이언트 컴퓨터 또는 App-v 터미널 서비스 클라이언트 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="67dcc-141">가상 응용 프로그램 패키지에 대 한 가상 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="67dcc-142">App-v 클라이언트는 캐시 스트리밍, 가상 응용 프로그램 게시 새로 고침, 응용 프로그램 가상화 서버와의 상호 작용에 대 한 패키지 스트리밍을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="67dcc-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





