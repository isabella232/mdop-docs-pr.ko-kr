---
title: UE-V 1.0 배포
description: UE-V 1.0 배포
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827148"
---
# <span data-ttu-id="7e6ae-103">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="7e6ae-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="7e6ae-104">Microsoft UE-V (User Experience Virtualization)에서 지 원하는 다양 한 배포 구성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="7e6ae-105">이 섹션에는 배포의 여러 단계에서 완료 해야 하는 작업을 성공적으로 수행 하는 데 도움이 되는 일반적인 정보와 단계별 절차가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="7e6ae-106">UE-V에 대 한 배포 정보</span><span class="sxs-lookup"><span data-stu-id="7e6ae-106">Deployment information for UE-V</span></span>


<span data-ttu-id="7e6ae-107">UE-V 배포의 경우 네트워크 공유에 설정 저장소 위치와 설정을 동기화 하는 모든 컴퓨터에 UE-V agent가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="7e6ae-108">Ue-v 그룹 정책 템플릿을 사용 하 여 UE-V 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="7e6ae-109">다음 항목에서는 이러한 기능을 배포 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="7e6ae-110">UE-V 1.0에 대한 설정 저장소 위치 배포</span><span class="sxs-lookup"><span data-stu-id="7e6ae-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="7e6ae-111">모든 UE-V 배포에는 동기화 된 설정 값이 포함 된 설정 패키지가 있는 설정 저장소 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="7e6ae-112">UE-V 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="7e6ae-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="7e6ae-113">UE-V를 사용 하 여 설정을 동기화 하려면 컴퓨터에 UE-V Agent가 설치 되어 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="7e6ae-114">UE-V 그룹 정책 ADMX 템플릿 설치</span><span class="sxs-lookup"><span data-stu-id="7e6ae-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="7e6ae-115">UE-V 에이전트 및 표준 UE-V 구성을 배포 하기 전에 그룹 정책을 사용 하 여 UE-V 설정을 미리 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="7e6ae-116">사용자 지정 서식 파일 배포 배포 정보</span><span class="sxs-lookup"><span data-stu-id="7e6ae-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="7e6ae-117">UE-V에 포함 된 Microsoft 응용 프로그램 (예: lob (기간 업무) 응용 프로그램)이 아닌 다른 응용 프로그램에 대 한 사용자 지정 설정 위치 템플릿을 만들려는 경우 설정 서식 파일 카탈로그를 배포 하 고 UE-V 생성기를 설치 하 여 해당 템플릿을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="7e6ae-118">자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="7e6ae-119">UE-V 생성기 설치</span><span class="sxs-lookup"><span data-stu-id="7e6ae-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="7e6ae-120">UE-V 생성기를 사용 하 여 기본 응용 프로그램 이외의 응용 프로그램 설정을 동기화 하는 데 도움이 되는 사용자 지정 설정 위치 템플릿을 만들고 편집 하 고 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="7e6ae-121">UE-V 1.0에 대한 설정 템플릿 카탈로그 배포</span><span class="sxs-lookup"><span data-stu-id="7e6ae-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="7e6ae-122">UE-V Agent의 기본 응용 프로그램이 아닌 다른 응용 프로그램을 지원 하기 위해 사용자 지정 설정 위치 템플릿을 배포 해야 하는 경우이를 저장할 설정 템플릿 카탈로그를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="7e6ae-123">UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="7e6ae-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="7e6ae-124">UE-V 에이전트의 기본 응용 프로그램이 아닌 다른 응용 프로그램을 동기화 해야 하는 경우 UE-V 생성기를 사용 하 여 만든 사용자 지정 설정 위치 템플릿을 UE-V 설정 템플릿 카탈로그에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="7e6ae-125">**참고**  사용자 지정 서식 파일을 배포 하려면 설정 서식 파일 카탈로그가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="7e6ae-126">기본 Microsoft 응용 프로그램 템플릿은 UE-V Agent를 사용 하 여 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6ae-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="7e6ae-127">이 제품에 대 한 항목</span><span class="sxs-lookup"><span data-stu-id="7e6ae-127">Topics for this product</span></span>


[<span data-ttu-id="7e6ae-128">Microsoft User Experience Virtualization(UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="7e6ae-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="7e6ae-129">User Experience Virtualization 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="7e6ae-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="7e6ae-130">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="7e6ae-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="7e6ae-131">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="7e6ae-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="7e6ae-132">UE-V 1.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7e6ae-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





