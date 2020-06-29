---
title: MED-V 2.0에 대한 종단 간 배포 시나리오
description: MED-V 2.0에 대한 종단 간 배포 시나리오
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826173"
---
# <span data-ttu-id="61bbc-103">MED-V 2.0에 대한 종단 간 배포 시나리오</span><span class="sxs-lookup"><span data-stu-id="61bbc-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="61bbc-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0의이 샘플 시나리오는 여러 시나리오를 통해 종단간 구성 요소를 배포 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="61bbc-105">이 샘플 시나리오는 개별 시나리오 및 절차를 컨텍스트에 추가할 수 있도록 하는 사례 연구를 통해 생각 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="61bbc-106">이 섹션에서는 엔터프라이즈의 종단간 솔루션으로 MED-V 구성 요소를 배포 하는 데 필요한 기본 정보와 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="61bbc-107">MED-V 배포 단계별 시나리오</span><span class="sxs-lookup"><span data-stu-id="61bbc-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="61bbc-108">이 단계별 시나리오의 항목에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="61bbc-109">[Med-v 2.0 지원 되는 구성](med-v-20-supported-configurations.md) 환경에서 Microsoft 엔터프라이즈 데스크톱 가상화 (med-v) 2.0을 설치 하 고 실행 하는 데 필요한 요구 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="61bbc-110">이 항목에서는 운영 체제 요구 사항, 구성 요구 사항 및 MED-V 작업 영역 요구 사항을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="61bbc-111">이 항목에는 MED-V 2.0에서 지 원하는 언어에 대 한 지역화 정보도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="61bbc-112">[Med-v 2.0 배포 개요](med-v-20-deployment-overview.md) 엔터프라이즈 전체에 med-v를 설치 하 고 배포 하는 데 도움이 되는 일반적인 정보와 지침에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="61bbc-113">MED-V 구성 요소는 클라이언트 기반 이며 기존 엔터프라이즈 인프라 및 프로세스를 사용 하 여 전달 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="61bbc-114">이 항목에서는 MED-V 설치 파일 및 배포 하는 MED-V 구성 요소에 대 한 정보를 포함 하는 MED-V 솔루션에 대 한 개요를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="61bbc-115">이 항목에서는 MED-V 설치 및 배포 프로세스에 대 한 개략적인 수준의 개요도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="61bbc-116">[Med-v에 대 한 배포 환경 준비](prepare-the-deployment-environment-for-med-v.md) med-v 2.0 배포를 위해 환경을 준비 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="61bbc-117">이 섹션에서는 Microsoft Windows 7 및 그룹 정책을 사용 하 여 운영 체제, 응용 프로그램 및 사용자 설정의 중앙 집중화 된 관리 및 구성을 제공 하는 Active Directory 인프라와 같은 MED-V 환경에 필요한 필수 구성 요소에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="61bbc-118">또한이 섹션에서는 Windows 가상 PC 및 필요한 Windows 가상 PC 업데이트와 같이 엔터프라이즈 전체에 MED-V 2.0를 설치 하 고 배포 하기 위해 가져야 하는 필수 구성 요소에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="61bbc-119">[Med-v 구성 요소 배포](deploy-the-med-v-components.md) 엔터프라이즈 전체에 필요한 모든 설치 파일과 med-v 구성 요소를 설치할 수 있는 다양 한 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="61bbc-120">MED-V를 설치 및 배포 하려면 일반적으로 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="61bbc-121">Med-v 작업 영역 패키지를 작성 하는 데 사용 하는 관리자 컴퓨터에 **Med-v 작업 영역 포장기** 를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="61bbc-122">자세한 내용은 [Med-v 작업 영역 포장기를 설치 하는 방법을](how-to-install-the-med-v-workspace-packager.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61bbc-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="61bbc-123">MED-V 작업 영역 패키지를 만들고 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="61bbc-124">자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md) 및 [Med-v 작업 영역 패키지 테스트](testing-the-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61bbc-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="61bbc-125">회사의 기존 응용 프로그램 배포 방법을 사용 하 여 엔터프라이즈 전체에 MED-V를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bbc-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="61bbc-126">자세한 내용은 [Med-v 작업 영역 패키지 배포](deploying-the-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61bbc-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="61bbc-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="61bbc-127">Related topics</span></span>


[<span data-ttu-id="61bbc-128">MED-V 배포</span><span class="sxs-lookup"><span data-stu-id="61bbc-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="61bbc-129">MED-V 2.0에 대한 종단 간 계획 시나리오</span><span class="sxs-lookup"><span data-stu-id="61bbc-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="61bbc-130">MED-V 2.0 종단 간 작업 시나리오</span><span class="sxs-lookup"><span data-stu-id="61bbc-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





