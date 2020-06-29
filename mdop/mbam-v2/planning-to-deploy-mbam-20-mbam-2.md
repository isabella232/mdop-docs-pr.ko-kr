---
title: MBAM 2.0 배포 계획
description: MBAM 2.0 배포 계획
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825633"
---
# <span data-ttu-id="1ebd0-103">MBAM 2.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="1ebd0-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="1ebd0-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)에 대 한 배포 계획을 만들기 전에 여러 가지 배포 구성과 필수 구성 요소를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="1ebd0-105">이 섹션에는 비즈니스 요구 사항에 가장 적합 한 배포 계획을 공식화 하는 데 필요한 정보를 수집 하는 데 도움이 되는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="1ebd0-106">구성 관리자 토폴로지에 MBAM을 설치 하는 경우 추가 계획 정보에 대해 [구성 관리자를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="1ebd0-107">MBAM 2.0 지원 되는 구성 검토</span><span class="sxs-lookup"><span data-stu-id="1ebd0-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="1ebd0-108">MBAM 서버 및 클라이언트 기능 설치에 대 한 컴퓨팅 환경을 준비한 후에는 지원 되는 구성을 검토 하 여 MBAM을 설치 하는 컴퓨터가 최소 하드웨어 및 운영 체제 요구 사항을 충족 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="1ebd0-109">MBAM 배포 필수 구성 요소에 대 한 자세한 내용은 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="1ebd0-110">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="1ebd0-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="1ebd0-111">MBAM 2.0 서버 및 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="1ebd0-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="1ebd0-112">MBAM 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 서버 기능 집합에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="1ebd0-113">이러한 기능은 여러 서버에서 분산 구성으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="1ebd0-114">**참고**  단일 서버에 MBAM을 설치 하는 것은 랩 환경에만 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="1ebd0-115">관리자는 MBAM 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="1ebd0-116">엔터프라이즈 소프트웨어 전달 시스템을 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터에 클라이언트 에이전트를 설치 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="1ebd0-117">MBAM을 사용 하면 최종 사용자가 컴퓨터를 받기 전이나 나중에 그룹 정책을 사용 하는 방법으로 조직의 컴퓨터를 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="1ebd0-118">MBAM 2.0 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="1ebd0-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="1ebd0-119">MBAM 2.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="1ebd0-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="1ebd0-120">MBAM 계획에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="1ebd0-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="1ebd0-121">MBAM 2.0 계획</span><span class="sxs-lookup"><span data-stu-id="1ebd0-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





