---
title: 개략적인 아키텍처
description: 개략적인 아키텍처
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827293"
---
# <span data-ttu-id="a6245-103">개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="a6245-103">High-Level Architecture</span></span>


<span data-ttu-id="a6245-104">이 섹션에서는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0의 상위 수준 시스템 아키텍처 및 구성 요소 디자인에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="a6245-105">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="a6245-105">System Architecture</span></span>


<span data-ttu-id="a6245-106">MED-V는 Windows 가상 PC를 사용 하 여 한 장치에서 두 운영 체제를 실행 하 여 가상 이미지 배달, 그룹 정책 기반 프로비저닝, 중앙 집중식 관리를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="a6245-107">MED-V를 사용 하 여 Windows 7 Professional, Enterprise 또는 Windows 7 Ultimate를 실행 하는 모든 Windows 기반 데스크톱에서 회사 Windows 가상 PC 이미지를 쉽게 구성, 배포 및 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="a6245-108">MED-V 솔루션에는 다음 구성 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="a6245-109">MED-V 호스트</span><span class="sxs-lookup"><span data-stu-id="a6245-109">MED-V Host</span></span>**  
<span data-ttu-id="a6245-110">MED-V 호스트 에이전트, ESD (전자 소프트웨어 배포) 시스템, 레지스트리 관리 시스템, MED-V 게스트를 포함 하는 Windows 7 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="a6245-111">MED-V 호스트는 특정 설치 기능 및 시스템 정보를 처리할 수 있도록 MED-V 게스트와 상호 작용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="a6245-112">MED-V 호스트 에이전트</span><span class="sxs-lookup"><span data-stu-id="a6245-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="a6245-113">Med-v 게스트와 통신 하는 채널을 제공 하는 med-v 호스트에 포함 된 MED-V 소프트웨어입니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="a6245-114">또한 처음 설치 및 응용 프로그램 게시와 같은 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="a6245-115">**참고**  MED-V와 필수 구성 요소가 설치 된 후 MED-V를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="a6245-116">MED-V의 구성을 첫 번째 설정 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="a6245-117">ESD 시스템</span><span class="sxs-lookup"><span data-stu-id="a6245-117">ESD System</span></span>**  
<span data-ttu-id="a6245-118">MED-V가 만드는 MED-V 작업 영역 패키지 파일을 배포 하 고 설치할 수 있는 기존 소프트웨어 배포 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="a6245-119">레지스트리 관리 시스템</span><span class="sxs-lookup"><span data-stu-id="a6245-119">Registry Management System</span></span>**  
<span data-ttu-id="a6245-120">기존 그룹 정책 설정 및 기본 설정 관리 방법</span><span class="sxs-lookup"><span data-stu-id="a6245-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="a6245-121">Windows 가상 PC 이미지</span><span class="sxs-lookup"><span data-stu-id="a6245-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="a6245-122">관리자가 정의한 가상 컴퓨터에는 다음 구성 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="a6245-123">기업 운영 체제</span><span class="sxs-lookup"><span data-stu-id="a6245-123">Corporate Operating System</span></span>**  
<span data-ttu-id="a6245-124">표준 기업 운영 체제.</span><span class="sxs-lookup"><span data-stu-id="a6245-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="a6245-125">관리 및 보안 도구</span><span class="sxs-lookup"><span data-stu-id="a6245-125">Management and Security Tools</span></span>**  
<span data-ttu-id="a6245-126">사용자의 표준 관리 및 보안 도구 (예: 바이러스 방지)</span><span class="sxs-lookup"><span data-stu-id="a6245-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="a6245-127">MED-V 게스트</span><span class="sxs-lookup"><span data-stu-id="a6245-127">MED-V Guest</span></span>**  
<span data-ttu-id="a6245-128">Windows 7에서 실행 되는 windows XP SP3 환경으로 다음 구성 요소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="a6245-129">MED-V 게스트 에이전트</span><span class="sxs-lookup"><span data-stu-id="a6245-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="a6245-130">Med-v 호스트와 통신 하는 채널을 제공 하는 med-v 게스트에 포함 된 MED-V 소프트웨어입니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="a6245-131">이는 또한 MED-V 호스트 에이전트에 게 최초 설정 수행 등의 기능을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="a6245-132">**참고**  MED-V 게스트 에이전트는 처음 설정 하는 동안 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="a6245-133">ESD 클라이언트</span><span class="sxs-lookup"><span data-stu-id="a6245-133">ESD Client</span></span>**  
<span data-ttu-id="a6245-134">소프트웨어 패키지를 설치 하 고 ESD 시스템에 상태를 보고 하는 ESD 시스템의 선택적 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="a6245-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="a6245-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a6245-135">Related topics</span></span>


[<span data-ttu-id="a6245-136">응용 프로그램 운영 체제 호환성 계획</span><span class="sxs-lookup"><span data-stu-id="a6245-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="a6245-137">MED-V 배포 환경 준비</span><span class="sxs-lookup"><span data-stu-id="a6245-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





