---
title: MBAM 2.5에서 MBAM 2.5 SP1 서비스 릴리스 업데이트 업그레이드
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812769"
---
# <span data-ttu-id="35341-102">MBAM 2.5에서 MBAM 2.5 SP1 서비스 릴리스 업데이트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="35341-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="35341-103">이 문서에서는 microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 [Microsoft 데스크톱 최적화 팩 (MDOP)](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) 과 함께 mbam 2.5 서비스 팩 1 (SP1)으로 업그레이드 하는 단계별 지침을 제공 합니다. 독립 실행형 구성에서 서비스를 업데이트할 수 2019 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35341-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="35341-104">이 가이드에서는 2 서버 구성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="35341-105">한 서버는 Microsoft SQL Server 2016을 실행 하는 데이터베이스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="35341-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="35341-106">이 서버는 MBAM 데이터베이스와 보고서를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="35341-107">다른 서버는 Windows Server 2012 R2 웹 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="35341-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="35341-108">이 서버는 "관리 및 모니터링" 및 "셀프 서비스 포털"을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="35341-109">MBAM 2.5 SP1 업그레이드 준비</span><span class="sxs-lookup"><span data-stu-id="35341-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="35341-110">환경에서 MBAM 서버 파악</span><span class="sxs-lookup"><span data-stu-id="35341-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="35341-111">SQL Server 데이터베이스 엔진: MBAM 데이터베이스를 호스트 하는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="35341-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="35341-112">SQL Server Reporting Services: MBAM 보고서를 호스팅하는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="35341-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="35341-113">IIS (인터넷 정보 서비스) 웹 서버: MBAM 웹 응용 프로그램 및 MBAM 서비스를 호스팅하는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="35341-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="35341-114">) Microsoft System Center Configuration Manager 기본 사이트 서버: MBAM 구성 응용 프로그램은이 서버에서 실행 되어 MBAM 보고서를 구성 관리자와 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="35341-115">그런 다음이 보고서가 Configuration Manager의 SSRS (SQL Server Reporting Services) 인스턴스에 대 한 기존 Configuration Manager 보고서와 병합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35341-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="35341-116">서비스 계정, 그룹, 서버 이름, 보고서 URL 확인</span><span class="sxs-lookup"><span data-stu-id="35341-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="35341-117">IIS 웹 서버에서 MBAM 데이터베이스의 데이터를 읽고 쓰는 데 사용 하는 MBAM 응용 프로그램 풀 서비스 계정을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="35341-118">MBAM 웹 기능 구성 및 보고서 웹 서비스 URL 중 사용 되는 그룹을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="35341-119">SQL Server 이름 및 인스턴스 이름을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="35341-120">자세한 내용은이 비디오를 시청 하세요.</span><span class="sxs-lookup"><span data-stu-id="35341-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="35341-121">준수 및 감사 데이터베이스에서 규정 준수 데이터를 읽는 데 사용 되는 SQL Server Reporting Services 계정을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="35341-122">자세한 내용은이 비디오를 시청 하세요.</span><span class="sxs-lookup"><span data-stu-id="35341-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="35341-123">MBAM 인프라를 사용 가능한 최신 버전으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="35341-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="35341-124">MBAM 서버 인프라 설치 또는 업그레이드는 항상 아래 나열 된 순서 대로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35341-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="35341-125">SQL Server 데이터베이스 엔진: 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="35341-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="35341-126">SQL Server Reporting Services: 보고서</span><span class="sxs-lookup"><span data-stu-id="35341-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="35341-127">웹 서버: 웹 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="35341-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="35341-128">SCCM 서버: SCCM 통합 보고서 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="35341-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="35341-129">클라이언트: MBAM 에이전트 또는 클라이언트 업데이트</span><span class="sxs-lookup"><span data-stu-id="35341-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="35341-130">그룹 정책 서식 파일: 기존 그룹 정책을 새 템플릿으로 업데이트 하 고 기존 MBAM 그룹 정책에서 새 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35341-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="35341-131">업그레이드를 실행 하기 전에 MBAM 데이터베이스의 전체 데이터베이스 백업을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="35341-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="35341-132">MBAM SQL Server 업그레이드</span><span class="sxs-lookup"><span data-stu-id="35341-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="35341-133">이 비디오를 시청 하 여 MBAM SQL Server를 업그레이드 하는 방법을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="35341-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="35341-134">MBAM 웹 서버 업그레이드</span><span class="sxs-lookup"><span data-stu-id="35341-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="35341-135">이 비디오를 시청 하 여 MBAM 웹 서버를 업그레이드 하는 방법을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="35341-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="35341-136">추가 정보</span><span class="sxs-lookup"><span data-stu-id="35341-136">More information</span></span>

<span data-ttu-id="35341-137">MBAM 2.5 SP1의 알려진 문제에 대 한 자세한 내용은 [mbam 2.5 sp1에 대 한 릴리스 정보](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35341-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>
