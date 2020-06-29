---
title: MBAM 1.0 시작
description: MBAM 1.0 시작
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825273"
---
# <span data-ttu-id="15439-103">MBAM 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="15439-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="15439-104">**중요** MBAM 1.0는 2021 년 9 월 14 일에 지원 종료에 도달 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="15439-105">자세한 내용은 [수명 주기 페이지](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15439-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="15439-106">[Mbam 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) 또는 지원 되는 다른 버전의 Mbam 또는 BitLocker 관리를 [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager)로 마이그레이션하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="15439-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="15439-107">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 배포 하거나 해당 기능을 사용 하기 전에 철저 한 계획이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="15439-108">이 제품은 조직의 모든 컴퓨터에 영향을 줄 수 있으므로 배포를 신중 하 게 계획 하지 않으면 전체 네트워크를 방해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15439-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="15439-109">그러나 비즈니스 요구에 맞게 배포를 신중 하 게 계획 하 고 관리 하는 경우 MBAM은 관리 오버 헤드와 총 소유 비용을 줄이는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15439-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="15439-110">이 제품을 처음 사용할 경우에는 문서를 철저히 읽어 보는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="15439-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="15439-111">프로덕션 환경에 배포 하기 전에 테스트 네트워크 환경에서 배포 계획의 유효성을 검사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="15439-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="15439-112">관련 기술에 대 한 수업을 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15439-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="15439-113">Microsoft 교육 기회에 대 한 자세한 내용은의 Microsoft 교육 개요를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="15439-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="15439-114">**참고**  이 설명서의 다운로드 가능한 버전과의 MBAM 평가 가이드를 찾을 수 있습니다 <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="15439-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="15439-115">이 MBAM 관리자 가이드의이 섹션에서는 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 이해를 제공 하기 위해 MBAM에 대 한 상위 수준 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="15439-116">Mbam 문서 리소스에 대 한 자세한 내용은의 MBAM 문서 자원 다운로드 페이지를 참조 <https://go.microsoft.com/fwlink/p/?LinkId=258391> 하세요.</span><span class="sxs-lookup"><span data-stu-id="15439-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="15439-117">MBAM 1.0 시작 하기</span><span class="sxs-lookup"><span data-stu-id="15439-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="15439-118">MBAM 1.0 정보</span><span class="sxs-lookup"><span data-stu-id="15439-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="15439-119">MBAM의 상위 수준 개요와 조직에서 사용할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="15439-120">MBAM 1.0 평가</span><span class="sxs-lookup"><span data-stu-id="15439-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="15439-121">조직에서 사용할 수 있도록 MBAM을 최대한 평가 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="15439-122">MBAM 1.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="15439-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="15439-123">MBAM 기능 및 이들이 함께 작동 하는 방식에 대 한 설명을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="15439-124">MBAM 1.0에 대한 접근성</span><span class="sxs-lookup"><span data-stu-id="15439-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="15439-125">장애가 있는 사용자가이 제품 및 해당 문서에 더욱 쉽게 액세스할 수 있도록 하는 기능 및 서비스에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15439-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="15439-126">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="15439-126">Other resources for this product</span></span>


-   [<span data-ttu-id="15439-127">Microsoft BitLocker 관리 및 모니터링 1 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="15439-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="15439-128">MBAM 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="15439-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="15439-129">MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="15439-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="15439-130">MBAM 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="15439-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="15439-131">MBAM 1.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="15439-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





