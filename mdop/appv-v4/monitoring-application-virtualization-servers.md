---
title: Application Virtualization Server 모니터링
description: Application Virtualization Server 모니터링
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816143"
---
# <span data-ttu-id="3bec6-103">Application Virtualization Server 모니터링</span><span class="sxs-lookup"><span data-stu-id="3bec6-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="3bec6-104">App-v (Application Virtualization) 서버 관리를 간소화 하기 위해 System Center Operations Manager2007 관리 팩을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="3bec6-105">이 관리 팩은 Application Virtualization (App-v) 4.5 서버만 지원 합니다. 이전 서버 버전을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="3bec6-106">관리 팩은 app-v 클라이언트 요청을 처리 하기 위해 App-v 서버 가용성을 극대화 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="3bec6-107">상태 표시기</span><span class="sxs-lookup"><span data-stu-id="3bec6-107">Status Indicators</span></span>


<span data-ttu-id="3bec6-108">App-v 서버의 상태 표시기가 색으로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="3bec6-109">색은 다음 상태 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="3bec6-110">색 없음은 서버가 복구할 수 없는 오류 없이 실행 되 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="3bec6-111">노란색은 구성 요소 중 하나가 제대로 작동 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="3bec6-112">서버의 전반적인 기능이 저하 되지만 서버는 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="3bec6-113">빨간색은 서버를 사용할 수 없으며 키 서비스를 제공 하거나 외부 서비스 종속성과 통신할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="3bec6-114">모니터링 기준</span><span class="sxs-lookup"><span data-stu-id="3bec6-114">Monitoring Criteria</span></span>


<span data-ttu-id="3bec6-115">관리 팩은 서버 상태의 다음 측면을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="3bec6-116">서버 상태-서버에서 예상 서비스를 제공 하 고 있는지 확인 하기 위해 서버 이벤트를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="3bec6-117">데이터 저장소 액세스 — 앱-v 데이터 저장소에 액세스 하 고 통신 하는 하나 이상의 App-v 관리 서버 기능을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="3bec6-118">콘텐츠 데이터 액세스-\\Content 디렉터리에 대 한 액세스를 모니터링 합니다 (로컬 디렉터리 또는 네트워크 공유 일 수 있음) 및 요청 된 파일을 읽을 수 있는 기능</span><span class="sxs-lookup"><span data-stu-id="3bec6-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="3bec6-119">보안-app-v 서버의 인증서 및 보안 통신을 사용 하 여 오류를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="3bec6-120">클라이언트 요청 처리-하나 이상의 App-v 서버가 클라이언트 요청에 대해 처리 하 고 올바르게 응답할 수 있는 능력을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="3bec6-121">이러한 요청에는 구성 요청, 패키지 로드 요청, 순서 없는 요청 등의 항목을 게시 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="3bec6-122">서버 구성-App-v 서버의 구성 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="3bec6-123">이러한 구성 설정에는 레지스트리와 App-v 데이터 저장소의 설정이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="3bec6-124">서버 차이점</span><span class="sxs-lookup"><span data-stu-id="3bec6-124">Server Differences</span></span>


<span data-ttu-id="3bec6-125">App-v 관리 서버와 App-v 스트리밍 서버의 주요 차이점은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="3bec6-126">앱-V 관리 서버는 게시, 스트리밍, 관리 및 보고 서비스를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="3bec6-127">따라서 관리 팩은 패키지 스트리밍을 제공 하는 App-v 스트리밍 서버에서 관리할 수 있는 App-v 관리 서버의 많은 측면을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="3bec6-128">App-v 스트리밍 서버에는 App-v 데이터 저장소가 없으므로 데이터 저장소 액세스가 모니터링 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="3bec6-129">App-v 스트리밍 서버에 대 한 구성 정보는 레지스트리에서 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="3bec6-130">App-v 스트리밍 서버는 App-v 서버 관리 콘솔 인터페이스를 사용 하지 않습니다. 다른 도구를 사용 하 여 구성을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bec6-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="3bec6-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3bec6-131">Related topics</span></span>


[<span data-ttu-id="3bec6-132">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="3bec6-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





