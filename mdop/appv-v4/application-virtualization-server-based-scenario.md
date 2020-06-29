---
title: Application Virtualization Server 기반 시나리오
description: Application Virtualization Server 기반 시나리오
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819528"
---
# <span data-ttu-id="8d33c-103">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="8d33c-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="8d33c-104">Microsoft App-v (Application Virtualization) 환경에 대 한 서버 기반 배포 시나리오를 사용 하려는 경우에는 응용 프로그램 가상화 관리 서버와 응용 프로그램 가상화 스트리밍 서버의 차이점을 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="8d33c-105">이 섹션의 항목에서는 이러한 차이점에 대해 설명 하 고 배포를 계속할 때 고려해 야 하는 패키지 배달 방법, 전송 프로토콜 및 외부 구성 요소에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="8d33c-106">또한이 섹션에서는 App-v 관리 서버와 Application Virtualization 스트리밍 서버를 설치 하 고 구성 하는 단계별 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="8d33c-107">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="8d33c-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="8d33c-108">Application Virtualization Server 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="8d33c-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="8d33c-109">응용 프로그램 가상화 관리 서버, 응용 프로그램 가상화 스트리밍 서버, 서버 기반 배포 계획과 관련 된 패키지 제공 메서드, 프로토콜 및 외부 구성 요소에 대 한 중요 한 배포 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="8d33c-110">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="8d33c-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="8d33c-111">서버 기반 배포에 필요한 Microsoft Application Virtualization 플랫폼 구성 요소를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="8d33c-112">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="8d33c-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="8d33c-113">응용 프로그램 가상화 관리 서버, 응용 프로그램 가상화 스트리밍 서버, 인터넷 정보 통합 (IIS) 서버, 파일 서버를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="8d33c-114">App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)</span><span class="sxs-lookup"><span data-stu-id="8d33c-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="8d33c-115">읽기 전용 캐시를 사용 하도록 앱-V 클라이언트를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="8d33c-116">App-V Client에서 읽기 전용 캐시를 구성하는 방법(RDS)</span><span class="sxs-lookup"><span data-stu-id="8d33c-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="8d33c-117">읽기 전용 캐시를 사용 하도록 앱-V 클라이언트를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="8d33c-118">App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="8d33c-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="8d33c-119">Microsoft SQL Server for App-v 시스템을 사용 하 여 데이터베이스 미러링을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d33c-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="8d33c-120">참고자료</span><span class="sxs-lookup"><span data-stu-id="8d33c-120">Reference</span></span>


[<span data-ttu-id="8d33c-121">Application Virtualization Client 설치 관리자 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8d33c-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="8d33c-122">관련 섹션</span><span class="sxs-lookup"><span data-stu-id="8d33c-122">Related Sections</span></span>


[<span data-ttu-id="8d33c-123">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="8d33c-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="8d33c-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8d33c-124">Related topics</span></span>


[<span data-ttu-id="8d33c-125">Application Virtualization 배포 및 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="8d33c-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="8d33c-126">Application Virtualization Client에 대한 독립 실행형 배달 시나리오</span><span class="sxs-lookup"><span data-stu-id="8d33c-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





