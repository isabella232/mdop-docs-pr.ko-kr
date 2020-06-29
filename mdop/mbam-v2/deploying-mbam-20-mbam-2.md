---
title: MBAM 2.0 배포
description: MBAM 2.0 배포
author: dansimp
ms.assetid: 4b0eaf10-81b4-427e-9d43-eb833de935a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba4423de5306e1ca204ef3b9fd31424bb8f2630f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823473"
---
# <span data-ttu-id="7b1db-103">MBAM 2.0 배포</span><span class="sxs-lookup"><span data-stu-id="7b1db-103">Deploying MBAM 2.0</span></span>


<span data-ttu-id="7b1db-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다양 한 배포 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-104">Microsoft BitLocker Administration and Monitoring (MBAM) supports a number of different deployment configurations.</span></span> <span data-ttu-id="7b1db-105">이 섹션에는 배포의 여러 단계에서 완료 해야 하는 작업을 성공적으로 수행 하는 데 도움이 되는 MBAM 및 단계별 절차 배포에 대해 고려해 야 할 내용이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-105">This section includes information that you should consider about the deployment of MBAM and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

<span data-ttu-id="7b1db-106">독립 실행형 토폴로지에서 또는 Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager와 MBAM을 통합 하는 토폴로지를 사용 하 여 MBAM을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-106">You can deploy MBAM either in a Stand-alone topology, or with a topology that integrates MBAM with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="7b1db-107">Configuration Manager 통합 토폴로지에 MBAM을 설치 하는 방법에 대 한 자세한 내용은 [구성 관리자에서 Mbam 사용](using-mbam-with-configuration-manager.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b1db-107">For information about installing MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

## <span data-ttu-id="7b1db-108">배포 정보</span><span class="sxs-lookup"><span data-stu-id="7b1db-108">Deployment Information</span></span>


-   [<span data-ttu-id="7b1db-109">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="7b1db-109">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

    <span data-ttu-id="7b1db-110">이 섹션에서는 여러 가지 MBAM 배포 토폴로지 옵션 및 MBAM 설치를 사용 하 여 MBAM 서버 기능을 배포 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-110">This section describes the different MBAM deployment topology options and how to use MBAM Setup to deploy MBAM Server features.</span></span>

-   [<span data-ttu-id="7b1db-111">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="7b1db-111">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

    <span data-ttu-id="7b1db-112">이 섹션에서는 엔터프라이즈 전체에서 MBAM 클라이언트 및 BitLocker 암호화 정책을 관리 하는 데 필요한 MBAM 그룹 정책 개체를 만들고 배포 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-112">This section describes how to create and deploy MBAM Group Policy Objects that are required for managing MBAM Clients and BitLocker encryption policies throughout the enterprise.</span></span>

-   [<span data-ttu-id="7b1db-113">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="7b1db-113">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

    <span data-ttu-id="7b1db-114">이 섹션에서는 MBAM 클라이언트 설치 관리자 파일을 사용 하 여 MBAM 클라이언트 소프트웨어를 배포 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-114">This section describes how to use the MBAM Client Installer files to deploy the MBAM Client software.</span></span>

-   [<span data-ttu-id="7b1db-115">MBAM 2.0 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="7b1db-115">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)

    <span data-ttu-id="7b1db-116">이 섹션에서는 MBAM 서버 기능 및 MBAM 클라이언트 배포를 지원 하기 위해 사용할 수 있는 배포 검사 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-116">This section provides a deployment checklist that can be used to assist in MBAM Server feature and MBAM Client deployment.</span></span>

-   [<span data-ttu-id="7b1db-117">이전 버전의 MBAM에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="7b1db-117">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)

    <span data-ttu-id="7b1db-118">이 섹션에서는 이전 버전에서 MBAM을 업그레이드 하는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1db-118">This section provides instructions for upgrading MBAM from previous versions.</span></span>

## <span data-ttu-id="7b1db-119">MBAM 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="7b1db-119">Other Resources for Deploying MBAM</span></span>


[<span data-ttu-id="7b1db-120">Microsoft BitLocker 관리 및 모니터링 2 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="7b1db-120">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="7b1db-121">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="7b1db-121">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

[<span data-ttu-id="7b1db-122">MBAM 2.0 계획</span><span class="sxs-lookup"><span data-stu-id="7b1db-122">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="7b1db-123">MBAM 2.0 작업</span><span class="sxs-lookup"><span data-stu-id="7b1db-123">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="7b1db-124">MBAM 2.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7b1db-124">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





