---
title: MBAM 2.5 배포 계획
description: MBAM 2.5 배포 계획
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826693"
---
# <span data-ttu-id="e7d95-103">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="e7d95-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="e7d95-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)에 대 한 배포 계획을 만들기 전에 여러 가지 배포 구성과 필수 구성 요소를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="e7d95-105">이 섹션에는 비즈니스 요구 사항에 가장 적합 한 배포 계획을 공식화 하는 데 필요한 정보를 수집 하는 데 도움이 되는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="e7d95-106">MBAM 2.5 지원 되는 구성 검토</span><span class="sxs-lookup"><span data-stu-id="e7d95-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="e7d95-107">MBAM 서버 및 클라이언트 기능 배포에 대 한 컴퓨팅 환경을 준비한 후에는 지원 되는 구성을 검토 하 여 MBAM이 설치 되어 있는 컴퓨터가 최소 하드웨어 및 운영 체제 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="e7d95-108">MBAM 배포 필수 구성 요소에 대 한 자세한 내용은 [mbam 2.5 배포 필수 구성 요소](mbam-25-deployment-prerequisites.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7d95-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="e7d95-109">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="e7d95-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="e7d95-110">MBAM 2.5 서버 및 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="e7d95-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="e7d95-111">MBAM 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에서 구성할 수 있는 서버 기능 집합에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="e7d95-112">이러한 기능은 여러 서버에서 분산 구성으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="e7d95-113">**참고**  단일 서버에 MBAM을 설치 하는 것은 랩 환경에만 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="e7d95-114">관리자는 MBAM 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="e7d95-115">엔터프라이즈 소프트웨어 전달 시스템을 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터에 클라이언트를 설치 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="e7d95-116">MBAM을 사용 하면 최종 사용자가 컴퓨터를 받기 전이나 나중에 그룹 정책을 사용 하는 방법으로 조직의 컴퓨터를 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="e7d95-117">MBAM 2.5 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="e7d95-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="e7d95-118">MBAM 2.5 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="e7d95-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="e7d95-119">MBAM 계획에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="e7d95-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="e7d95-120">MBAM 2.5 계획</span><span class="sxs-lookup"><span data-stu-id="e7d95-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="e7d95-121">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="e7d95-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e7d95-122">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e7d95-123">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d95-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





