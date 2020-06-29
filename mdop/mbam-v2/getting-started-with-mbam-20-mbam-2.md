---
title: MBAM 2.0 시작
description: MBAM 2.0 시작
author: dansimp
ms.assetid: 29f5c9af-5bbf-4d37-aa0f-0716046904af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7c683e3d8718da24ebd2164328bda0dab0123037
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825648"
---
# <span data-ttu-id="3003e-103">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="3003e-103">Getting Started with MBAM 2.0</span></span>


<span data-ttu-id="3003e-104">Microsoft BitLockerAdministration 및 모니터링 (MBAM) 2.0을 사용 하 여 배포 하거나 해당 기능을 사용 하기 전에 철저 한 계획이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="3003e-105">이 제품은 조직의 모든 컴퓨터에 영향을 줄 수 있으므로 배포를 신중 하 게 계획 하지 않으면 전체 네트워크를 방해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-105">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="3003e-106">그러나 비즈니스 요구 사항에 맞게 배포를 신중 하 게 계획 하 고 관리 하는 경우 BitLockerAdministration 및 모니터링 2.0을 사용 하 여 관리 오버 헤드와 총 소유 비용을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-106">However, if you plan your deployment carefully and manage it so that it meets your business requirements, BitLockerAdministration and Monitoring2.0 can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="3003e-107">이 제품을 처음 사용할 경우에는 문서를 주의 깊게 읽어 보는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-107">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="3003e-108">MBAM 소프트웨어를 얻으려면 [MDOP를 구입 하는 방법은 무엇 인가요?](https://go.microsoft.com/fwlink/p/?LinkId=322049)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3003e-108">To get the MBAM software, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span> <span data-ttu-id="3003e-109">MBAM을 프로덕션 환경에 배포 하기 전에 테스트 환경에서 배포 계획의 유효성을 검사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-109">Before you deploy MBAM to a production environment, we also recommend that you validate your deployment plan in a test environment.</span></span> <span data-ttu-id="3003e-110">관련 기술에 대 한 수업을 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-110">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="3003e-111">Microsoft 교육 기회에 대 한 자세한 내용은의 Microsoft 교육 개요를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="3003e-111">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="3003e-112">MBAM 2.0 관리자 가이드의이 섹션에서는 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 지식을 제공 하는 MBAM 2.0에 대 한 상위 수준 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-112">This section of the MBAM2.0 Administrator’s Guide includes high-level information about MBAM2.0 to provide a basic understanding of the product before you begin to plan deployment.</span></span> <span data-ttu-id="3003e-113">Configuration Manager 통합 토폴로지로 MBAM을 배포 하는 방법에 대 한 자세한 내용은 [구성 관리자에서 Mbam 사용](using-mbam-with-configuration-manager.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3003e-113">For specific information about deploying MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="3003e-114">Microsoft BitLocker 관리 및 모니터링 (MBAM) 설명서 리소스 다운로드 페이지에서 추가 MBAM 설명서를 찾을 수 있습니다 <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="3003e-114">You can find additional MBAM documentation on the Microsoft BitLocker Administration and Monitoring (MBAM) Documentation Resources Download Page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="3003e-115">MBAM 2.0 시작 하기</span><span class="sxs-lookup"><span data-stu-id="3003e-115">Getting Started with MBAM2.0</span></span>


-   [<span data-ttu-id="3003e-116">MBAM 2.0 정보</span><span class="sxs-lookup"><span data-stu-id="3003e-116">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

    <span data-ttu-id="3003e-117">MBAM 2.0의 상위 수준 개요를 제공 하 고 조직에서 사용할 수 있는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-117">Provides a high-level overview of MBAM2.0 and describes how it can be used in your organization.</span></span>

-   [<span data-ttu-id="3003e-118">MBAM 2.0 평가</span><span class="sxs-lookup"><span data-stu-id="3003e-118">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)

    <span data-ttu-id="3003e-119">조직에서 사용할 MBAM 2.0을 가장 잘 평가할 수 있는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-119">Provides information about how you can best evaluate MBAM2.0 for use in your organization.</span></span>

-   [<span data-ttu-id="3003e-120">MBAM 2.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="3003e-120">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)

    <span data-ttu-id="3003e-121">MBAM 2.0 기능 및 프로덕션 환경에 권장 되는 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-121">Describes the MBAM2.0 features and the recommended architecture for a production environment.</span></span>

-   [<span data-ttu-id="3003e-122">MBAM 2.0에 대한 접근성</span><span class="sxs-lookup"><span data-stu-id="3003e-122">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)

    <span data-ttu-id="3003e-123">MBAM 2.0에서 사용할 수 있는 바로 가기 키에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3003e-123">Describes the keyboard shortcuts that are available for MBAM2.0.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="3003e-124">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="3003e-124">Other Resources for this Product</span></span>


[<span data-ttu-id="3003e-125">Microsoft BitLocker 관리 및 모니터링 2 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="3003e-125">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="3003e-126">MBAM 2.0 계획</span><span class="sxs-lookup"><span data-stu-id="3003e-126">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="3003e-127">MBAM 2.0 배포</span><span class="sxs-lookup"><span data-stu-id="3003e-127">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

[<span data-ttu-id="3003e-128">MBAM 2.0 작업</span><span class="sxs-lookup"><span data-stu-id="3003e-128">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="3003e-129">MBAM 2.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="3003e-129">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





