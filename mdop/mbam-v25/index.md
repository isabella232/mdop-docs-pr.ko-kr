---
title: Microsoft BitLocker 관리 및 모니터링 2.5
description: Microsoft BitLocker 관리 및 모니터링 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795697"
---
# <span data-ttu-id="5333e-103">Microsoft BitLocker 관리 및 모니터링 2.5</span><span class="sxs-lookup"><span data-stu-id="5333e-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="5333e-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5는 BitLocker 드라이브 암호화를 관리 하는 데 사용할 수 있는 간단한 관리 인터페이스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5333e-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="5333e-105">엔터프라이즈에 적합 한 BitLocker 드라이브 암호화 정책 옵션을 설정한 다음이를 사용 하 여 해당 정책에 대 한 클라이언트 준수를 모니터링할 수 있는 MBAM 그룹 정책 템플릿을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5333e-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="5333e-106">개별 컴퓨터와 엔터프라이즈 전체의 암호화 상태에 대 한 보고를 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5333e-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="5333e-107">또한 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5333e-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="5333e-108">MBAM에 대 한 자세한 설명은 [mbam 2.5](about-mbam-25.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5333e-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="5333e-109">MBAM을 얻으려면 MDOP를 [가져오는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5333e-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="5333e-110">개요</span><span class="sxs-lookup"><span data-stu-id="5333e-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="5333e-111">MBAM 2.5 시작</span><span class="sxs-lookup"><span data-stu-id="5333e-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="5333e-112">MBAM 2.5 정보</span><span class="sxs-lookup"><span data-stu-id="5333e-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="5333e-113">MBAM 2.5 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="5333e-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="5333e-114">MBAM 2.5 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="5333e-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="5333e-115">MBAM 2.5 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="5333e-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="5333e-116">테스트 환경에서 MBAM 2.5 평가</span><span class="sxs-lookup"><span data-stu-id="5333e-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="5333e-117">MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="5333e-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="5333e-118">MBAM 2.5에 대한 접근성</span><span class="sxs-lookup"><span data-stu-id="5333e-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="5333e-119">MBAM 2.5 계획</span><span class="sxs-lookup"><span data-stu-id="5333e-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="5333e-120">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="5333e-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="5333e-121">MBAM 2.5 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="5333e-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="5333e-122">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="5333e-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="5333e-123">MBAM 2.5 그룹 및 계정 계획</span><span class="sxs-lookup"><span data-stu-id="5333e-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="5333e-124">MBAM 웹 사이트를 보호하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="5333e-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="5333e-125">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="5333e-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="5333e-126">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="5333e-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="5333e-127">MBAM 2.5 고가용성 계획</span><span class="sxs-lookup"><span data-stu-id="5333e-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="5333e-128">MBAM 2.5 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="5333e-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="5333e-129">MBAM 2.5 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="5333e-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="5333e-130">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="5333e-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="5333e-131">MBAM 2.5 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="5333e-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="5333e-132">MBAM 2.5 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="5333e-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="5333e-133">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="5333e-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="5333e-134">MBAM 2.5 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="5333e-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="5333e-135">이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="5333e-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="5333e-136">MBAM 서버 기능 또는 소프트웨어 제거</span><span class="sxs-lookup"><span data-stu-id="5333e-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="5333e-137">MBAM 2.5 작업</span><span class="sxs-lookup"><span data-stu-id="5333e-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="5333e-138">MBAM 2.5 기능 관리</span><span class="sxs-lookup"><span data-stu-id="5333e-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="5333e-139">MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="5333e-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="5333e-140">MBAM 2.5를 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="5333e-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="5333e-141">MBAM 2.5 유지 관리</span><span class="sxs-lookup"><span data-stu-id="5333e-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="5333e-142">Windows PowerShell을 사용하여 MBAM 2.5 관리</span><span class="sxs-lookup"><span data-stu-id="5333e-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="5333e-143">MBAM 2.5 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5333e-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="5333e-144">MBAM 2.5에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="5333e-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="5333e-145">클라이언트 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="5333e-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="5333e-146">서버 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="5333e-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="5333e-147">추가 정보</span><span class="sxs-lookup"><span data-stu-id="5333e-147">More Information</span></span>

- [<span data-ttu-id="5333e-148">MDOP 정보 환경</span><span class="sxs-lookup"><span data-stu-id="5333e-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="5333e-149">MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="5333e-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="5333e-150">MBAM 배포 가이드</span><span class="sxs-lookup"><span data-stu-id="5333e-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="5333e-151">각 방법에 대 한 단계별 지침을 포함 하 여 MBAM에 대 한 배포 방법을 선택 하는 방법에 대 한 도움말을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="5333e-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="5333e-152">MBAM 2.5 SP1 서버에서 핫픽스 적용</span><span class="sxs-lookup"><span data-stu-id="5333e-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="5333e-153">MBAM 2.5 SP1 서버 핫픽스를 적용 하는 방법에 대 한 가이드</span><span class="sxs-lookup"><span data-stu-id="5333e-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
