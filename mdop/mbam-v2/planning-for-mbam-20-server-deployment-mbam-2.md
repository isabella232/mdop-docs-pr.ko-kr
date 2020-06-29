---
title: MBAM 2.0 서버 배포 계획
description: MBAM 2.0 서버 배포 계획
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812612"
---
# <span data-ttu-id="d0213-103">MBAM 2.0 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="d0213-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="d0213-104">MBAM (Microsoft BitLocker 관리 및 모니터링) 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 서버 기능 집합에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="d0213-105">Configuration Manager 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 하는 경우 [구성 관리자를 사용 하 여 MBAM 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0213-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="d0213-106">**참고**  Microsoft BitLocker 관리 및 모니터링을 단일 서버에 설치 하는 것은 테스트 환경에만 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="d0213-107">MBAM 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="d0213-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="d0213-108">MBAM 서버 배포의 인프라에는 다음 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="d0213-109">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="d0213-109">Recovery Database</span></span>

-   <span data-ttu-id="d0213-110">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="d0213-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="d0213-111">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="d0213-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="d0213-112">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="d0213-112">Self-Service Portal</span></span>

-   <span data-ttu-id="d0213-113">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="d0213-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="d0213-114">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="d0213-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="d0213-115">MBAM 서버 데이터베이스 및 기능은 확장성 요구 사항에 따라 다른 구성으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="d0213-116">모든 MBAM 서버 기능은 단일 서버에 설치 되거나 여러 서버에 걸쳐 배포 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="d0213-117">프로덕션 환경에 대 한 두 서버 구성을 사용 하는 것이 좋으며, 컴퓨팅 요구 사항에 따라 두 개에서 4 개 서버의 구성을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="d0213-118">각 MBAM 기능에는 특정 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="d0213-119">전체 서버 기능 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항 목록은 [mbam 2.0 배포 전제 조건](mbam-20-deployment-prerequisites-mbam-2.md) 및 [Mbam 2.0 지원 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0213-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="d0213-120">서버 관련 MBAM 기능 외에도 서버 설정 응용 프로그램에는 MBAM 그룹 정책 서식 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="d0213-121">이 서식 파일에는 엔터프라이즈에서 BitLocker 드라이브 암호화를 관리 하도록 구성 된 GPO (그룹 정책 개체) 설정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="d0213-122">GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 컴퓨터에이 서식 파일을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="d0213-123">MBAM 서버 배포를 계획할 때, 모든 복구 키가 만료 되는 경우 MBAM의 BitLocker 복구 키가 단일 용도로만 사용 됨을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="d0213-124">키를 사용한 후에 만료 되도록 하려면 지원 센터 포털 또는 셀프 서비스 포털을 통해 검색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="d0213-125">MBAM 서버 기능 배포 순서</span><span class="sxs-lookup"><span data-stu-id="d0213-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="d0213-126">여러 서버에 MBAM 기능을 배포 하려면 다음 순서로 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="d0213-127">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="d0213-127">Recovery Database</span></span>

2.  <span data-ttu-id="d0213-128">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="d0213-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="d0213-129">준수 감사 및 보고서</span><span class="sxs-lookup"><span data-stu-id="d0213-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="d0213-130">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="d0213-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="d0213-131">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="d0213-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="d0213-132">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="d0213-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="d0213-133">**참고**  각 기능을 설치 하는 컴퓨터의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0213-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="d0213-134">이 정보는 설치 프로세스 전체에서 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="d0213-135">이 작업을 위해 배포 검사 목록을 인쇄 하 고 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0213-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="d0213-136">MBAM 배포 검사 목록에 대 한 자세한 내용은 [mbam 2.0 배포 검사 목록을](mbam-20-deployment-checklist-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0213-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="d0213-137">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d0213-137">Related topics</span></span>


[<span data-ttu-id="d0213-138">MBAM 2.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="d0213-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="d0213-139">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="d0213-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





