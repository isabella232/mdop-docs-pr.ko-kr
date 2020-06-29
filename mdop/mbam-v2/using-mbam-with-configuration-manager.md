---
title: Configuration Manager와 함께 MBAM 사용
description: Configuration Manager와 함께 MBAM 사용
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823788"
---
# <span data-ttu-id="34349-103">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="34349-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="34349-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치할 때 Microsoft BitLocker 관리 및 모니터링을 System Center Configuration Manager와 통합 하는 설치를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34349-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="34349-105">지원 되는 버전의 Configuration Manager에 대 한 목록은 [Configuration manager를 사용 하 여 MBAM 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34349-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="34349-106">이 통합에서는 Microsoft BitLocker 관리 및 모니터링 준수 및 보고 인프라를 Microsoft System Center Configuration Manager의 기본 환경으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="34349-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="34349-107">IT 관리자는 구성 관리자 토폴로지를 사용 하 여 Configuration Manager 관리 콘솔에서 해당 엔터프라이즈의 보고서 및 준수 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34349-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="34349-108">**중요**  Windows To Go는 구성 관리자 2007와 함께 MBAM의 통합 토폴로지를 설치 하는 경우 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34349-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="34349-109">시작 하기-구성 관리자에서 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="34349-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="34349-110">이 섹션에서는 Configuration Manager에서 MBAM이 작동 하는 방식에 대해 설명 하 고 Configuration Manager 통합 토폴로지에 MBAM을 배포 하기 위한 권장 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="34349-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="34349-111">시작 - Configuration Manager를 통해 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="34349-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="34349-112">Configuration Manager에서 MBAM을 배포하는 계획</span><span class="sxs-lookup"><span data-stu-id="34349-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="34349-113">이 섹션에서는 구성 관리자 토폴로지에 MBAM을 설치 하기 전에 고려해 야 하는 설치 필수 구성 요소, 지원 되는 구성 및 하드웨어 및 소프트웨어 요구 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="34349-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="34349-114">Configuration Manager에서 MBAM을 배포하는 계획</span><span class="sxs-lookup"><span data-stu-id="34349-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="34349-115">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="34349-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="34349-116">이 섹션에서는 구성 관리자를 사용 하 여 MBAM을 배포 하는 방법을 설명 하 고 관리 및 모니터링 서버 및 Configuration Manager 서버에 MBAM을 설치 하 고 구성 하는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="34349-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="34349-117">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="34349-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="34349-118">Configuration Manager에서 MBAM 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="34349-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="34349-119">이 섹션에서는 엔터프라이즈의 개별 컴퓨터에 대 한 엔터프라이즈 및 규정 준수를 보여 주기 위해 Configuration Manager에서 실행할 수 있는 MBAM 보고서에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="34349-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="34349-120">Configuration Manager에서 MBAM 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="34349-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="34349-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="34349-121">Related topics</span></span>


[<span data-ttu-id="34349-122">MBAM 2.0 작업</span><span class="sxs-lookup"><span data-stu-id="34349-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





