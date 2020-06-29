---
title: User Experience Virtualization 1.0 시작
description: User Experience Virtualization 1.0 시작
author: dansimp
ms.assetid: 74a068dc-4f87-4cb4-b114-8ca2a37149f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 010cefc42c8f2d65ac7f815eff51ec2df42df4d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827118"
---
# <span data-ttu-id="a4314-103">User Experience Virtualization 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="a4314-103">Getting Started With User Experience Virtualization 1.0</span></span>


<span data-ttu-id="a4314-104">Microsoft UE-V (User Experience Virtualization)는 사용자에 대 한 응용 프로그램 설정 및 Windows 운영 체제 설정을 캡처하고 중앙 집중화 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-104">Microsoft User Experience Virtualization (UE-V) captures and centralizes application settings and Windows operating system settings for the user.</span></span> <span data-ttu-id="a4314-105">이러한 설정은 데스크톱 컴퓨터, 랩톱 컴퓨터, VDI (가상 데스크톱 인프라) 세션을 비롯 하 여 사용자가 액세스 하는 다른 컴퓨터에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-105">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="a4314-106">UE-V는 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 동기화를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-106">UE-V offers settings synchronization for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="a4314-107">또한 언제 든 지 기업 전체에서 작업 하는 모든 사용자에 게 설정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-107">It also delivers user settings at any time to wherever users work throughout the enterprise.</span></span> <span data-ttu-id="a4314-108">UE-V를 사용 하면 관리자가 로밍 하는 응용 프로그램 설정 및 Windows 설정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-108">UE-V allows administrators to specify which application settings and Windows settings roam.</span></span> <span data-ttu-id="a4314-109">UE-V를 사용 하면 관리자가 엔터프라이즈에서 사용 되는 타사 또는 lob (기간 업무) 응용 프로그램에 대 한 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-109">UE-V helps administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="a4314-110">사용자 환경 가상화는 향상 된 사용자 상태 가상화 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-110">User Experience Virtualization delivers an enhanced user state virtualization experience.</span></span> <span data-ttu-id="a4314-111">다음과 같은 시나리오에서 사용자의 설정에 대 한 일관 된 개인화를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-111">It provides consistent personalization of the user’s settings in the following scenarios:</span></span>

-   <span data-ttu-id="a4314-112">컴퓨터 간 로밍 사용자 응용 프로그램 및 Windows 설정</span><span class="sxs-lookup"><span data-stu-id="a4314-112">Roaming user application and Windows settings between computers.</span></span>

-   <span data-ttu-id="a4314-113">다른 메서드를 사용 하 여 배포 되는 응용 프로그램의 인스턴스 간 로밍 사용자 설정:</span><span class="sxs-lookup"><span data-stu-id="a4314-113">Roaming user settings between the instances of an application that are deployed by using different methods:</span></span>

    -   <span data-ttu-id="a4314-114">설치 된 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="a4314-114">Installed applications</span></span>

    -   <span data-ttu-id="a4314-115">App-v (Application Virtualization) 시퀀싱 된 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="a4314-115">Application Virtualization (App-V) sequenced applications</span></span>

    -   <span data-ttu-id="a4314-116">RemoteApp (원격 데스크톱 가상화) 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="a4314-116">RemoteApp (Remote Desktop Virtualization) applications</span></span>

-   <span data-ttu-id="a4314-117">교체, 하드웨어 업그레이드 또는 다시 설치한 후 컴퓨터에 대 한 설정을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-117">Recovering settings for a computer after replacement, hardware upgrade, or reimage.</span></span>

<span data-ttu-id="a4314-118">이 제품을 배포 하거나 해당 기능을 사용 하려면 철저 한 계획이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-118">This product requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="a4314-119">이 제품은 조직의 모든 컴퓨터에 영향을 줄 수 있으므로 배포를 신중 하 게 계획 하지 않으면 전체 네트워크를 방해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-119">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="a4314-120">그러나 비즈니스 요구에 맞게 배포를 신중 하 게 계획 하 고 관리 하는 경우이 제품을 통해 관리 오버 헤드와 총 소유 비용을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-120">However, if you plan your deployment carefully and manage it so that it meets your business needs, this product can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="a4314-121">이 제품을 처음 사용할 경우에는 문서를 주의 깊게 읽어 보는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-121">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="a4314-122">제품을 프로덕션 환경에 배포 하기 전에 테스트 네트워크 환경에서 배포 계획의 유효성을 검사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-122">Before you deploy the product to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="a4314-123">관련 기술에 대 한 수업을 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-123">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="a4314-124">Microsoft 교육 기회에 대 한 자세한 내용은의 Microsoft 교육 개요를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="a4314-124">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="a4314-125">**참고**  이 관리자 가이드의 다운로드 가능한 버전을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-125">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="a4314-126">그러나 문서를 선택 하 고, 컬렉션에서 그룹화 하 고, 인쇄 하거나, 파일 ()에 파일로 내보내는 기능을 제공 하는 TechNet 라이브러리의 특별 한 모드에 대해 배울 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=272497> https://go.microsoft.com/fwlink/?LinkId=272497) .</span><span class="sxs-lookup"><span data-stu-id="a4314-126">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272497> (https://go.microsoft.com/fwlink/?LinkId=272497).</span></span>

 

## <span data-ttu-id="a4314-127">Microsoft 사용자 환경 가상화 시작 항목</span><span class="sxs-lookup"><span data-stu-id="a4314-127">Getting started with Microsoft User Experience Virtualization topics</span></span>


-   [<span data-ttu-id="a4314-128">User Experience Virtualization 1.0 정보</span><span class="sxs-lookup"><span data-stu-id="a4314-128">About User Experience Virtualization 1.0</span></span>](about-user-experience-virtualization-10.md)

    <span data-ttu-id="a4314-129">사용자 환경 가상화의 기능 및 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-129">Describes the functionality and features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="a4314-130">UE-V 1.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="a4314-130">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

    <span data-ttu-id="a4314-131">사용자 환경 가상화의 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-131">Explains the features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="a4314-132">Microsoft User Experience Virtualization(UE-V) 1.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="a4314-132">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--10-release-notes.md)

    <span data-ttu-id="a4314-133">UE-V의 알려진 문제에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-133">Describes the known issues for UE-V.</span></span>

-   [<span data-ttu-id="a4314-134">UE-V에 대한 접근성</span><span class="sxs-lookup"><span data-stu-id="a4314-134">Accessibility for UE-V</span></span>](accessibility-for-ue-v.md)

    <span data-ttu-id="a4314-135">UE-V의 바로 가기 키 및 접근성 정보에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4314-135">Describes the keyboard shortcuts and accessibility information for UE-V.</span></span>

## <span data-ttu-id="a4314-136">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="a4314-136">Other resources for this product</span></span>


-   [<span data-ttu-id="a4314-137">Microsoft User Experience Virtualization(UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="a4314-137">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

-   [<span data-ttu-id="a4314-138">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="a4314-138">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

-   [<span data-ttu-id="a4314-139">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="a4314-139">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

-   [<span data-ttu-id="a4314-140">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="a4314-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

-   [<span data-ttu-id="a4314-141">UE-V 1.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a4314-141">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





