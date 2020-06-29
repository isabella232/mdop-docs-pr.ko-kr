---
title: MBAM 1.0 서버 배포 계획
description: MBAM 1.0 서버 배포 계획
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812428"
---
# <span data-ttu-id="7ed64-103">MBAM 1.0 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="7ed64-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="7ed64-104">MBAM (Microsoft BitLocker 관리 및 모니터링) 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 서버 기능 집합에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="7ed64-105">MBAM 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="7ed64-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="7ed64-106">다음 MBAM 기능은 MBAM 서버 배포에 대 한 서버 인프라를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="7ed64-107">복구 및 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7ed64-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="7ed64-108">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7ed64-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="7ed64-109">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="7ed64-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="7ed64-110">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="7ed64-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="7ed64-111">MBAM 서버 데이터베이스 및 기능은 사용자의 확장성 요구에 따라 다른 구성으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="7ed64-112">모든 MBAM 서버 기능은 단일 서버에 설치 되거나 여러 서버에 걸쳐 배포 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="7ed64-113">일반적으로 실제 요구 사항에 따라 2 개 또는 4 개 서버의 구성을 사용할 수도 있지만, 프로덕션 환경에는 3 대의 서버 또는 5 서버 구성을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="7ed64-114">**참고**  MBAM 및 권장 배포 토폴로지의 성능 확장성에 대 한 자세한 내용은의 MBAM 확장성 및 고가용성 가이드 백서 백서를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="7ed64-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="7ed64-115">각 MBAM 기능에는 특정 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="7ed64-116">전체 서버 기능 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항 목록은 [mbam 1.0 배포 전제 조건](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ed64-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="7ed64-117">서버 관련 MBAM 기능 외에도 서버 설정 응용 프로그램에는 MBAM 그룹 정책 서식 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="7ed64-118">이 서식 파일은 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 모든 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="7ed64-119">MBAM 서버 기능 배포 순서</span><span class="sxs-lookup"><span data-stu-id="7ed64-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="7ed64-120">MBAM 서버 기능을 배포 하는 경우 다음 순서로 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="7ed64-121">복구 및 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7ed64-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="7ed64-122">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7ed64-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="7ed64-123">준수 감사 및 보고서</span><span class="sxs-lookup"><span data-stu-id="7ed64-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="7ed64-124">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="7ed64-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="7ed64-125">정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="7ed64-125">Policy Template</span></span>

<span data-ttu-id="7ed64-126">**참고**  각 기능을 설치 하는 컴퓨터의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ed64-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="7ed64-127">이 정보는 설치 프로세스 전체에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="7ed64-128">배포 검사 목록을 인쇄 하 고 사용 하 여 설치 과정을 도울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ed64-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="7ed64-129">MBAM 배포 검사 목록에 대 한 자세한 내용은 [mbam 1.0 배포 검사 목록을](mbam-10-deployment-checklist.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ed64-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="7ed64-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7ed64-130">Related topics</span></span>


[<span data-ttu-id="7ed64-131">MBAM 1.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="7ed64-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="7ed64-132">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="7ed64-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





