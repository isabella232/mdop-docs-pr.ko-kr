---
title: Microsoft BitLocker 관리 및 모니터링 1 관리자 가이드
description: Microsoft BitLocker 관리 및 모니터링 1 관리자 가이드
author: dansimp
ms.assetid: 4086e721-db24-4439-bdcd-ac5ef901811f
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 5336108e12738a21441df8062fbcd8bd98933945
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795761"
---
# <span data-ttu-id="d74ff-103">Microsoft BitLocker 관리 및 모니터링 1 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="d74ff-103">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>

<span data-ttu-id="d74ff-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 드라이브 암호화를 관리 하는 데 사용할 수 있는 간단한 관리 인터페이스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ff-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="d74ff-105">MBAM을 사용 하는 경우 엔터프라이즈에 적합 한 BitLocker 암호화 정책 옵션을 선택한 다음 해당 정책으로 클라이언트 준수를 모니터링 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ff-105">With MBAM, you can select BitLocker encryption policy options that are appropriate to your enterprise and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="d74ff-106">개별 컴퓨터 및 전체 엔터프라이즈의 암호화 상태에 대해 보고할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ff-106">You can also report on the encryption status of an individual computer and on the entire enterprise.</span></span> <span data-ttu-id="d74ff-107">또한 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ff-107">In addition, you can access recovery key information when users forget their PIN or password, or when their BIOS or boot record changes.</span></span>

- [<span data-ttu-id="d74ff-108">MBAM 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="d74ff-108">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)  
  - [<span data-ttu-id="d74ff-109">MBAM 1.0 정보</span><span class="sxs-lookup"><span data-stu-id="d74ff-109">About MBAM 1.0</span></span>](about-mbam-10.md)
  - [<span data-ttu-id="d74ff-110">MBAM 1.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="d74ff-110">Release Notes for MBAM 1.0</span></span>](release-notes-for-mbam-10.md)
  - [<span data-ttu-id="d74ff-111">MBAM 1.0 평가</span><span class="sxs-lookup"><span data-stu-id="d74ff-111">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)
  - [<span data-ttu-id="d74ff-112">MBAM 1.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="d74ff-112">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)
  - [<span data-ttu-id="d74ff-113">MBAM 1.0에 대한 접근성</span><span class="sxs-lookup"><span data-stu-id="d74ff-113">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)
  - [<span data-ttu-id="d74ff-114">MBAM 1.0 개인정보처리방침</span><span class="sxs-lookup"><span data-stu-id="d74ff-114">Privacy Statement for MBAM 1.0</span></span>](privacy-statement-for-mbam-10.md)
- [<span data-ttu-id="d74ff-115">MBAM 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="d74ff-115">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)  
  - [<span data-ttu-id="d74ff-116">MBAM 1.0용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="d74ff-116">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)
  - [<span data-ttu-id="d74ff-117">MBAM 1.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="d74ff-117">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)
  - [<span data-ttu-id="d74ff-118">MBAM 1.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="d74ff-118">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)
  - [<span data-ttu-id="d74ff-119">MBAM 1.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="d74ff-119">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)
  - [<span data-ttu-id="d74ff-120">MBAM 1.0 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="d74ff-120">MBAM 1.0 Planning Checklist</span></span>](mbam-10-planning-checklist.md)
- [<span data-ttu-id="d74ff-121">MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="d74ff-121">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)  
  - [<span data-ttu-id="d74ff-122">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="d74ff-122">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)
  - [<span data-ttu-id="d74ff-123">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="d74ff-123">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)
  - [<span data-ttu-id="d74ff-124">MBAM 1.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="d74ff-124">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)
  - [<span data-ttu-id="d74ff-125">MBAM 1.0 언어 릴리스 업데이트 배포</span><span class="sxs-lookup"><span data-stu-id="d74ff-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)
  - [<span data-ttu-id="d74ff-126">MBAM 1.0 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="d74ff-126">MBAM 1.0 Deployment Checklist</span></span>](mbam-10-deployment-checklist.md)
- [<span data-ttu-id="d74ff-127">MBAM 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="d74ff-127">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)  
  - [<span data-ttu-id="d74ff-128">MBAM 1.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="d74ff-128">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)
  - [<span data-ttu-id="d74ff-129">MBAM 1.0으로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="d74ff-129">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)
  - [<span data-ttu-id="d74ff-130">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="d74ff-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)
  - [<span data-ttu-id="d74ff-131">PowerShell을 사용하여 MBAM 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="d74ff-131">Administering MBAM 1.0 by Using PowerShell</span></span>](administering-mbam-10-by-using-powershell.md)
- [<span data-ttu-id="d74ff-132">MBAM 1.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d74ff-132">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)  

## <span data-ttu-id="d74ff-133">추가 정보</span><span class="sxs-lookup"><span data-stu-id="d74ff-133">More Information</span></span>
- [<span data-ttu-id="d74ff-134">MDOP 정보 환경</span><span class="sxs-lookup"><span data-stu-id="d74ff-134">MDOP Information Experience</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=236032)  
  <span data-ttu-id="d74ff-135">MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ff-135">Find documentation, videos, and other resources for MDOP technologies.</span></span>
