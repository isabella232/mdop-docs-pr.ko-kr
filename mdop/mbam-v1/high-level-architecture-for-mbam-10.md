---
title: MBAM 1.0의 개략적인 아키텍처
description: MBAM 1.0의 개략적인 아키텍처
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825238"
---
# <span data-ttu-id="9e5c2-103">MBAM 1.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="9e5c2-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="9e5c2-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 프로비저닝 및 배포를 간소화 하 고, BitLocker 준수 및 보고 기능을 개선 하 고, 지원 비용을 줄이는 데 도움이 되는 클라이언트/서버 데이터 암호화 솔루션입니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="9e5c2-105">MBAM에는이 항목에서 설명 하는 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="9e5c2-106">또한 MBAM 아키텍처와 MBAM 설정에 대 한 개요를 제공 하는 비디오가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="9e5c2-107">자세한 내용은 [Mbam 배포 및 아키텍처 개요](https://go.microsoft.com/fwlink/p/?LinkId=258392)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="9e5c2-108">아키텍처 개요</span><span class="sxs-lookup"><span data-stu-id="9e5c2-108">Architecture Overview</span></span>


<span data-ttu-id="9e5c2-109">다음 다이어그램에는 MBAM 아키텍처가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="9e5c2-110">MBAM 기능을 소개 하는 단일 서버 MBAM 배포 토폴로지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="9e5c2-111">그러나이 MBAM 배포 토폴로지는 랩 환경에만 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="9e5c2-112">**참고**  프로덕션 배포에는 최소 3 대의 컴퓨터 MBAM 배포 토폴로지가 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="9e5c2-113">MBAM 배포 토폴로지에 대 한 자세한 내용은 [mbam 1.0 서버 인프라 배포](deploying-the-mbam-10-server-infrastructure.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![mbam 단일 서버 배포 토폴로지](images/mbam-1-server.jpg)

1.  <span data-ttu-id="9e5c2-115">**관리 및 모니터링 서버**.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="9e5c2-116">MBAM 관리 및 모니터링 서버는 Windows Server에 설치 되어 있으며 MBAM 관리 및 관리 웹 사이트와 모니터링 웹 서비스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="9e5c2-117">MBAM 관리 및 관리 웹 사이트는 엔터프라이즈 준수 상태를 확인 하 고, 활동을 감사 하 고, 하드웨어 기능을 관리 하 고, BitLocker 복구 키와 같은 복구 데이터에 액세스 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="9e5c2-118">관리 및 모니터링 서버는 다음 데이터베이스 및 서비스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="9e5c2-119">복구 및 하드웨어 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="9e5c2-120">복구 및 하드웨어 데이터베이스가 Windows 기반 서버 및 지원 되는 SQLServer 인스턴스에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="9e5c2-121">이 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터 및 하드웨어 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="9e5c2-122">준수 및 감사 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-122">Compliance and Audit Database.</span></span> <span data-ttu-id="9e5c2-123">준수 및 감사 데이터베이스가 Windows server 및 지원 되는 SQLServer 인스턴스에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="9e5c2-124">이 데이터베이스는 MBAM 클라이언트 컴퓨터에 대 한 규정 준수 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="9e5c2-125">이 데이터는 주로 SSRS (SQL Server Reporting Services)에서 호스팅되는 보고서에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="9e5c2-126">준수 및 감사 보고서.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="9e5c2-127">규정 준수 및 감사 보고서는 SSRS 기능이 설치 된 Windows 기반 서버 및 지원 되는 SQLServer 인스턴스에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="9e5c2-128">이러한 보고서는 Microsoft BitLocker 관리 및 모니터링 보고서를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="9e5c2-129">이 보고서는 MBAM 관리 및 관리 웹 사이트에서 또는 SSRS 서버에서 직접 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="9e5c2-130">**Mbam 클라이언트**.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-130">**MBAM Client**.</span></span> <span data-ttu-id="9e5c2-131">Microsoft BitLocker 관리 및 모니터링 클라이언트는 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="9e5c2-132">그룹 정책을 사용 하 여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="9e5c2-133">세 가지 BitLocker 데이터 드라이브 유형 (운영 체제 드라이브, 고정 데이터 드라이브, 이동식 데이터 (USB) 드라이브)에 대 한 복구 키를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="9e5c2-134">클라이언트 컴퓨터에 대 한 복구 정보 및 하드웨어 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="9e5c2-135">컴퓨터에 대 한 규정 준수 데이터를 수집 하 고 보고 시스템으로 데이터를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="9e5c2-136">**정책 서식 파일**.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-136">**Policy Template**.</span></span> <span data-ttu-id="9e5c2-137">MBAM 그룹 정책 템플릿은 지원 되는 Windows 기반 서버 또는 클라이언트 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="9e5c2-138">이 템플릿은 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5c2-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="9e5c2-139">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9e5c2-139">Related topics</span></span>


[<span data-ttu-id="9e5c2-140">MBAM 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="9e5c2-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





