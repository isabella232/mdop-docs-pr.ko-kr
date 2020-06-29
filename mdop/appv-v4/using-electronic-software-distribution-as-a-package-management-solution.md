---
title: 패키지 관리 솔루션으로 전자 소프트웨어 배포 사용
description: 패키지 관리 솔루션으로 전자 소프트웨어 배포 사용
author: dansimp
ms.assetid: 7d96ea70-3e7e-49fa-89cc-586804a10657
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ec56d0fd52825a91a772e418ddd48b76294792
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815098"
---
# <span data-ttu-id="437ff-103">패키지 관리 솔루션으로 전자 소프트웨어 배포 사용</span><span class="sxs-lookup"><span data-stu-id="437ff-103">Using Electronic Software Distribution as a Package Management Solution</span></span>


<span data-ttu-id="437ff-104">응용 프로그램 가상화에서 패키지를 시퀀싱 하 고 테스트 한 후에는 가상 응용 프로그램 패키지를 대상 컴퓨터에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-104">In Application Virtualization, after you have sequenced and tested a package, you need to deploy the virtual application package to the target computers.</span></span> <span data-ttu-id="437ff-105">이를 위해 패키지 콘텐츠를 배치할 위치와 최종 사용자 컴퓨터에 제공 하는 방법을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-105">To accomplish this, you will need to determine where to put the package content and how to deliver it to the end user computers.</span></span> <span data-ttu-id="437ff-106">효율적이 고 효과적인 전자 소프트웨어 배포 기반 배포 계획을 사용 하면 많은 수의 최종 사용자 컴퓨터가 느린 네트워크 연결을 통해 패키지 콘텐츠를 검색 해야 하는 상황을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-106">An efficient, effective electronic software distribution–based deployment plan will help you avoid the situation where large numbers of end users computers need to retrieve the package content over slow network connections.</span></span>

<span data-ttu-id="437ff-107">현재 일일 작업에 전자 소프트웨어 배포 (ESD) 시스템이 있는 경우이를 사용 하 여 응용 프로그램 가상화의 필요한 모든 관리 작업을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-107">If you currently have an electronic software distribution (ESD) system in daily operation, you can use it to handle all necessary management tasks in Application Virtualization.</span></span> <span data-ttu-id="437ff-108">즉, 새 서버와 응용 프로그램 소프트웨어를 추가 하거나 필요에 따라 추가 관리 오버 헤드를 초래 하지 않고 기존 인프라를 효과적으로 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-108">This means that you can effectively use your existing infrastructure to the best advantage, without the need to add new servers and application software or incur the additional administrative overhead that these would require.</span></span> <span data-ttu-id="437ff-109">이상적으로 Microsoft 끝점 구성 관리자가 배포 되 고 작동 하는 경우 Configuration Manager에는 응용 프로그램 가상화 관리 작업을 수행할 수 있는 기능이 기본적으로 포함 되어 있음을 알게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-109">Ideally, if you have Microsoft Endpoint Configuration Manager deployed and operational, you will find that Configuration Manager has built-in capability for performing the Application Virtualization management tasks.</span></span>

<span data-ttu-id="437ff-110">ESD 기반 배포를 수행 하는 방법에 대 한 자세한 내용은 [전자 소프트웨어 배포 기반 시나리오를 사용](electronic-software-distribution-based-scenario.md)하세요.</span><span class="sxs-lookup"><span data-stu-id="437ff-110">For in-depth information about performing an ESD-based deployment, [Electronic Software Distribution-Based Scenario](electronic-software-distribution-based-scenario.md).</span></span>

## <span data-ttu-id="437ff-111">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="437ff-111">In This Section</span></span>


<a href="" id="publishing-virtual-applications-using-electronic-software-distribution"></a>[<span data-ttu-id="437ff-112">전자 소프트웨어 배포를 사용하여 가상 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="437ff-112">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)  
<span data-ttu-id="437ff-113">시퀀싱 된 응용 프로그램을 클라이언트에 배포 하는 데 사용할 수 있는 ESD 기반 메서드에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-113">Describes the available ESD-based methods for distributing your sequenced applications to clients.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-electronic-software-distribution-implementation"></a>[<span data-ttu-id="437ff-114">전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획</span><span class="sxs-lookup"><span data-stu-id="437ff-114">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)  
<span data-ttu-id="437ff-115">스트리밍 서버를 사용 하 여 시퀀싱 된 응용 프로그램을 클라이언트에 배포 하는 데 사용할 수 있는 옵션을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="437ff-115">Describes available options for using a streaming server to deploy your sequenced applications to clients.</span></span>

## <span data-ttu-id="437ff-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="437ff-116">Related topics</span></span>


[<span data-ttu-id="437ff-117">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="437ff-117">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="437ff-118">Application Virtualization 시스템 배포 계획</span><span class="sxs-lookup"><span data-stu-id="437ff-118">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





