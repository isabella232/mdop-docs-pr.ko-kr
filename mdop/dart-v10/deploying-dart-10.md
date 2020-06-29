---
title: DaRT 10 배포
description: DaRT 10 배포
author: dansimp
ms.assetid: 92cf70fd-006f-4fdc-9fb3-78d9d223148d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2cca1d30fb8894d4244ca2601195bf8fccb01878
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813121"
---
# <span data-ttu-id="f32f9-103">DaRT 10 배포</span><span class="sxs-lookup"><span data-stu-id="f32f9-103">Deploying DaRT 10</span></span>


<span data-ttu-id="f32f9-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 10은 여러 다양 한 배포 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 supports a number of different deployment configurations.</span></span> <span data-ttu-id="f32f9-105">이 섹션에는 배포의 여러 단계에서 완료 해야 하는 작업을 성공적으로 수행 하는 데 도움이 되는 DaRT 10 및 단계별 절차 배포에 대해 고려해 야 할 내용이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-105">This section includes information you should consider about the deployment of DaRT 10 and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="f32f9-106">배포 정보</span><span class="sxs-lookup"><span data-stu-id="f32f9-106">Deployment Information</span></span>


-   [<span data-ttu-id="f32f9-107">관리자 컴퓨터에 DaRT 10 배포</span><span class="sxs-lookup"><span data-stu-id="f32f9-107">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

    <span data-ttu-id="f32f9-108">이 섹션에서는 요구 사항에 대 한 다양 한 DaRT 배포 옵션에 대해 설명 하 고 배포 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-108">This section describes the different DaRT deployment options for your requirements and explains how to deploy them.</span></span>

-   [<span data-ttu-id="f32f9-109">DaRT 10 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="f32f9-109">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

    <span data-ttu-id="f32f9-110">이 섹션에서는 dart 복구 이미지를 만드는 데 사용할 수 있는 방법에 대해 설명 하 고 DaRT 복구 이미지 마법사를 사용 하 여 복구 이미지 만들기에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-110">This section describes the methods you can use to create the DaRT recovery image and provides instructions to create the recovery image by using the DaRT Recovery Image wizard.</span></span>

-   [<span data-ttu-id="f32f9-111">DaRT 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="f32f9-111">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

    <span data-ttu-id="f32f9-112">이 섹션에서는 요구 사항에 가장 적합 한 DaRT 복구 이미지 배포 옵션을 결정 하는 데 도움이 되는 정보를 제공 하 고 복구 이미지를 배포 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-112">This section provides information to help you decide on the best DaRT recovery image deployment option for your requirements and provides instructions on how to deploy the recovery image.</span></span>

-   [<span data-ttu-id="f32f9-113">DaRT 10 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="f32f9-113">DaRT 10 Deployment Checklist</span></span>](dart-10-deployment-checklist.md)

    <span data-ttu-id="f32f9-114">이 섹션에는 DaRT를 배포 하는 데 도움이 되는 배포 검사 목록이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-114">This section contains a deployment checklist that can help you to deploy DaRT.</span></span>

### <span data-ttu-id="f32f9-115">DaRT를 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="f32f9-115">How to get DaRT</span></span>

<span data-ttu-id="f32f9-116">이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-116">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="f32f9-117">엔터프라이즈 고객은 Microsoft 소프트웨어 보증을 통해 MDOP를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f32f9-117">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="f32f9-118">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/p/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="f32f9-118">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

## <span data-ttu-id="f32f9-119">DaRT를 배포 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="f32f9-119">Other Resources for deploying DaRT</span></span>


[<span data-ttu-id="f32f9-120">Diagnostics and Recovery Toolset 10</span><span class="sxs-lookup"><span data-stu-id="f32f9-120">Diagnostics and Recovery Toolset 10</span></span>](index.md)

[<span data-ttu-id="f32f9-121">DaRT 10 시작</span><span class="sxs-lookup"><span data-stu-id="f32f9-121">Getting Started with DaRT 10</span></span>](getting-started-with-dart-10.md)

[<span data-ttu-id="f32f9-122">DaRT 10 계획</span><span class="sxs-lookup"><span data-stu-id="f32f9-122">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

[<span data-ttu-id="f32f9-123">DaRT 10 작업</span><span class="sxs-lookup"><span data-stu-id="f32f9-123">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="f32f9-124">DaRT 10 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f32f9-124">Troubleshooting DaRT 10</span></span>](troubleshooting-dart-10.md)

 

 





