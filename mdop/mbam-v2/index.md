---
title: Microsoft BitLocker 관리 및 모니터링 2 관리자 가이드
description: Microsoft BitLocker 관리 및 모니터링 2 관리자 가이드
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795753"
---
# <span data-ttu-id="c9366-103">Microsoft BitLocker 관리 및 모니터링 2 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="c9366-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="c9366-104">Microsoft BitLockerAdministration 및 모니터링 (MBAM) 2.0은 BitLocker 드라이브 암호화를 관리 하는 데 사용할 수 있는 간단한 관리 인터페이스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9366-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="c9366-105">BitLockerAdministration 및 모니터링 2.0에서 엔터프라이즈에 적합 한 BitLocker 드라이브 암호화 정책 옵션을 선택한 다음 해당 정책을 사용 하 여 클라이언트 준수를 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9366-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="c9366-106">개별 컴퓨터와 엔터프라이즈 전체의 암호화 상태에 대 한 보고를 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9366-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="c9366-107">또한 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9366-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="c9366-108">개요</span><span class="sxs-lookup"><span data-stu-id="c9366-108">Outline</span></span>

- [<span data-ttu-id="c9366-109">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="c9366-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-110">MBAM 2.0 정보</span><span class="sxs-lookup"><span data-stu-id="c9366-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-111">MBAM 2.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="c9366-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-112">MBAM 2.0 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="c9366-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="c9366-113">MBAM 2.0 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="c9366-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="c9366-114">MBAM 2.0 평가</span><span class="sxs-lookup"><span data-stu-id="c9366-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-115">MBAM 2.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c9366-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-116">MBAM 2.0에 대한 접근성</span><span class="sxs-lookup"><span data-stu-id="c9366-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="c9366-117">MBAM 2.0 계획</span><span class="sxs-lookup"><span data-stu-id="c9366-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-118">MBAM 2.0용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="c9366-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-119">MBAM 2.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="c9366-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="c9366-120">MBAM 2.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="c9366-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-121">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="c9366-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="c9366-122">MBAM 2.0 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="c9366-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="c9366-123">MBAM 2.0 배포</span><span class="sxs-lookup"><span data-stu-id="c9366-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-124">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="c9366-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="c9366-125">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="c9366-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="c9366-126">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="c9366-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="c9366-127">MBAM 2.0 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="c9366-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="c9366-128">이전 버전의 MBAM에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c9366-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="c9366-129">MBAM 2.0 작업</span><span class="sxs-lookup"><span data-stu-id="c9366-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-130">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="c9366-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="c9366-131">MBAM 2.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="c9366-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="c9366-132">MBAM 2.0으로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="c9366-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-133">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="c9366-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="c9366-134">MBAM 2.0 유지 관리</span><span class="sxs-lookup"><span data-stu-id="c9366-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-135">MBAM 2.0에 대한 보안 및 개인 정보</span><span class="sxs-lookup"><span data-stu-id="c9366-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="c9366-136">PowerShell을 사용하여 MBAM 2.0 관리</span><span class="sxs-lookup"><span data-stu-id="c9366-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="c9366-137">MBAM 2.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c9366-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="c9366-138">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c9366-138">More Information</span></span>

- [<span data-ttu-id="c9366-139">MDOP 정보 환경</span><span class="sxs-lookup"><span data-stu-id="c9366-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="c9366-140">MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c9366-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





