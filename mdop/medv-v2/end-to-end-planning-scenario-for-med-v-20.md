---
title: MED-V 2.0에 대한 종단 간 계획 시나리오
description: MED-V 2.0에 대한 종단 간 계획 시나리오
author: dansimp
ms.assetid: e7833883-be93-4b42-9fa3-5c4d9a919058
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f34dcccade7987b8b01269caa667018a74d020c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827178"
---
# <span data-ttu-id="f7768-103">MED-V 2.0에 대한 종단 간 계획 시나리오</span><span class="sxs-lookup"><span data-stu-id="f7768-103">End-to-End Planning Scenario for MED-V 2.0</span></span>


<span data-ttu-id="f7768-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에 대 한이 샘플 시나리오는 여러 시나리오를 통해 종단간 배포를 계획 하는 목표를 달성 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you achieve your goal of planning your MED-V deployment by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="f7768-105">이 샘플 시나리오는 개별 시나리오 및 절차를 컨텍스트에 추가할 수 있도록 하는 사례 연구를 통해 생각 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="f7768-106">이 섹션에서는 엔터프라이즈의 엔드 투 엔드 솔루션으로 MED-V 배포를 계획 하기 위한 기본 정보 및 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-106">This section provides basic information and directions for planning you MED-V deployment as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="f7768-107">MED-V 계획 단계별 시나리오</span><span class="sxs-lookup"><span data-stu-id="f7768-107">MED-V Planning Step-by-Step Scenario</span></span>


<span data-ttu-id="f7768-108">이 단계별 시나리오의 항목에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="f7768-109">[상위 수준 아키텍처](high-level-architecturemedv2.md) 는 med-v 2.0의 상위 수준 시스템 아키텍처 및 구성 요소 디자인에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-109">[High-Level Architecture](high-level-architecturemedv2.md) discusses the high-level system architecture and component design of MED-V 2.0.</span></span> <span data-ttu-id="f7768-110">MED-V는 Windows 가상 PC를 사용 하 여 한 장치에서 두 운영 체제를 실행 하 여 가상 이미지 배달, 그룹 정책 기반 프로비저닝, 중앙 집중식 관리를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-110">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="f7768-111">MED-V를 사용 하 여 Windows 7 Professional, Enterprise 또는 Windows 7 Ultimate를 실행 하는 모든 Windows 기반 데스크톱에서 회사 Windows 가상 PC 이미지를 쉽게 구성, 배포 및 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-111">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span>

-   <span data-ttu-id="f7768-112">[Med-v 배포 정의 및 계획](define-and-plan-your-med-v-deployment.md) med-v 2.0 배포를 계획할 때 고려해 야 할 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-112">[Define and Plan your MED-V Deployment](define-and-plan-your-med-v-deployment.md) discusses the considerations for planning your MED-V 2.0 deployment.</span></span> <span data-ttu-id="f7768-113">이 항목에서는 엔터프라이즈에서 MED-V를 수신 하 고 디스크 공간 요구 사항을 계산 하는 시스템을 식별 하는 방향에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-113">This topic provides direction about identifying the systems in your enterprise that receive MED-V and calculating disk space requirements.</span></span> <span data-ttu-id="f7768-114">이 항목에서는 기존 인프라를 평가 하 고 MED-V 배포에 사용할 수 있는 방법을 결정 하는 데도 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-114">This topic also helps evaluate your existing infrastructure and determines how it can be used for MED-V deployment.</span></span>

-   <span data-ttu-id="f7768-115">[Med-v 2.0 모범 사례](med-v-20-best-practices.md) 는 환경에서 med-v 2.0을 계획, 설치, 배포 및 관리 하는 데 권장 되는 모범 사례에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-115">[MED-V 2.0 Best Practices](med-v-20-best-practices.md) discusses the recommended best practices for planning, installing, deploying, and managing MED-V 2.0 in your environment.</span></span> <span data-ttu-id="f7768-116">이러한 모범 사례에는 빠른 실행 시간을 생성 하 고, 처음 설정 하는 동안 매우 효율적으로 작동 하 고, 성능이 향상 되며, 가상 컴퓨터를 관리 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7768-116">These best practices include recommendations that produce faster run times, better operability during first time setup, increased performance, and better virtual machine management.</span></span>

## <span data-ttu-id="f7768-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f7768-117">Related topics</span></span>


[<span data-ttu-id="f7768-118">MED-V 계획</span><span class="sxs-lookup"><span data-stu-id="f7768-118">Planning for MED-V</span></span>](planning-for-med-v.md)

[<span data-ttu-id="f7768-119">MED-V 2.0에 대한 종단 간 배포 시나리오</span><span class="sxs-lookup"><span data-stu-id="f7768-119">End-to-End Deployment Scenario for MED-V 2.0</span></span>](end-to-end-deployment-scenario-for-med-v-20.md)

[<span data-ttu-id="f7768-120">MED-V 2.0 종단 간 작업 시나리오</span><span class="sxs-lookup"><span data-stu-id="f7768-120">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





