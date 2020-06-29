---
title: MBAM 1.0 서버 인프라 배포
description: MBAM 1.0 서버 인프라 배포
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825178"
---
# <span data-ttu-id="d54aa-103">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="d54aa-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="d54aa-104">하나 ~ 다섯 개의 서버를 사용 하 여 다양 한 구성에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 기능을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="d54aa-105">일반적으로 사용자의 확장성 요구에 따라 프로덕션 환경에 대해 3 ~ 5 대의 서버 구성을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="d54aa-106">MBAM 및 권장 배포 토폴로지의 성능 확장성에 대 한 자세한 내용은 [Mbam 확장성 및 고가용성 가이드 백서](https://go.microsoft.com/fwlink/p/?LinkId=258314)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d54aa-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="d54aa-107">모든 MBAM 1.0를 단일 서버에 배포</span><span class="sxs-lookup"><span data-stu-id="d54aa-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="d54aa-108">이 구성에서는 모든 MBAM 기능이 단일 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="d54aa-109">이 MBAM 서버 인프라에 대 한이 배포 토폴로지에서는 최대 21000 MBAM 클라이언트 컴퓨터를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="d54aa-110">**중요**  이 구성은 지원 되지만 테스트에만 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="d54aa-111">이 섹션의 절차는 모든 MBAM 기능을 단일 서버에 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="d54aa-112">단일 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d54aa-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="d54aa-113">분산 서버에 MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="d54aa-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="d54aa-114">MBAM 기능은 사용자의 확장성 요구에 따라 다른 구성으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="d54aa-115">MBAM 서버 기능 배포를 계획 하는 방법에 대 한 자세한 내용은 [mbam 1.0 서버 배포 계획](planning-for-mbam-10-server-deployment.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d54aa-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="d54aa-116">이 섹션의 절차에서는 분산 서버의 MBAM 기능을 모두 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="d54aa-117">3-컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="d54aa-117">Three-computer configuration</span></span>

<span data-ttu-id="d54aa-118">다음 다이어그램에는 MBAM에 대 한 세 가지 컴퓨터 배포 토폴로지가 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="d54aa-119">최대 55000 MBAM 클라이언트를 지 원하는 프로덕션 환경에이 토폴로지를 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![mbam 3 대의 컴퓨터 배포 토폴로지](images/mbam-3-server.jpg)

<span data-ttu-id="d54aa-121">이 구성에서 MBAM 기능은 다음 구성으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="d54aa-122">복구 및 하드웨어 데이터베이스, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="d54aa-123">서버에 관리 및 모니터링 서버 기능이 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="d54aa-124">MBAM 그룹 정책 템플릿은 GPO (그룹 정책 개체)를 수정할 수 있는 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="d54aa-125">4 컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="d54aa-125">Four-computer configuration</span></span>

<span data-ttu-id="d54aa-126">다음 다이어그램에는 MBAM에 대 한 4 개의 컴퓨터 배포 토폴로지가 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="d54aa-127">11만 MBAM 클라이언트를 지 원하는 프로덕션 환경에이 토폴로지를 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![mbam 4 개의 컴퓨터 배포 토폴로지.](images/mbam-4-computer.jpg)

<span data-ttu-id="d54aa-129">이 구성에서 MBAM 기능은 다음 구성으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="d54aa-130">복구 및 하드웨어 데이터베이스, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="d54aa-131">관리 및 모니터링 서버 기능은 NLB (네트워크 부하 분산) 서버 클러스터에 구성 된 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="d54aa-132">MBAM 그룹 정책 템플릿은 그룹 정책 개체를 수정할 수 있는 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="d54aa-133">5 대의 컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="d54aa-133">Five-computer configuration</span></span>

<span data-ttu-id="d54aa-134">다음 다이어그램에는 MBAM에 대 한 5 컴퓨터 배포 토폴로지가 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="d54aa-135">최대 135000 MBAM 클라이언트를 지 원하는 프로덕션 환경에이 토폴로지를 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![mbam 컴퓨터 배포 토폴로지](images/mbam-5-computer.jpg)

<span data-ttu-id="d54aa-137">이 구성에서 MBAM 기능은 다음 구성으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="d54aa-138">복구 및 하드웨어 데이터베이스가 서버에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="d54aa-139">준수 및 감사 데이터베이스와 규정 준수 및 감사 보고서가 서버에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="d54aa-140">관리 및 모니터링 서버 기능은 NLB (네트워크 부하 분산) 서버 클러스터에 구성 된 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="d54aa-141">MBAM 그룹 정책 템플릿은 그룹 정책 개체를 수정할 수 있는 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d54aa-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="d54aa-142">분산 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d54aa-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="d54aa-143">MBAM에 대한 네트워크 부하 분산을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d54aa-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="d54aa-144">MBAM 1.0 서버 기능 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="d54aa-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="d54aa-145">MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="d54aa-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





