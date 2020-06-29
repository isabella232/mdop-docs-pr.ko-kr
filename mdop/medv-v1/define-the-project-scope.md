---
title: 프로젝트 범위 정의
description: 프로젝트 범위 정의
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823643"
---
# <span data-ttu-id="4c12a-103">프로젝트 범위 정의</span><span class="sxs-lookup"><span data-stu-id="4c12a-103">Define the Project Scope</span></span>


<span data-ttu-id="4c12a-104">프로젝트 범위를 정의할 때 다음을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="4c12a-105">Med-v 최종 사용자 (위치 및 최종 사용자의 수)는 med-v 클라이언트 설치 위치를 결정 하는 데 사용 되며 med-v 인스턴스 수는 물론 MED-V의 이미지 리포지토리의 수 및 배치에도 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="4c12a-106">이미지의 이미지 및 배치를 배포 하는 방법을 결정 하기 위해 MED-V에서 관리할 VM (가상 컴퓨터) 이미지</span><span class="sxs-lookup"><span data-stu-id="4c12a-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="4c12a-107">조직의 서비스 수준에 따라, MED-V 서버 및 데이터베이스에 대 한 성능 및 내결함성 요구 사항 및 이미지 리포지토리를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="4c12a-108">비즈니스에 대 한 유효성 검사-계획 된 인프라가 비즈니스에 영향을 주는 방식을 완벽 하 게 이해 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="4c12a-109">MED-V 최종 사용자 정의</span><span class="sxs-lookup"><span data-stu-id="4c12a-109">Define the MED-V End Users</span></span>


<span data-ttu-id="4c12a-110">먼저 최종 사용자가 어디에 있는지, 그리고 각 위치의 사용자 수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="4c12a-111">두 번째, 사용자 위치 및 해당 위치에 대 한 사용 가능한 대역폭을 표시 하는 네트워크 인프라 다이어그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="4c12a-112">셋째, 사용자가 다른 위치를 여행 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="4c12a-113">사용자가 출장 하는 경우 서버 인프라 및 이미지 리포지토리의 디자인에 추가 용량이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="4c12a-114">MED-V에서 관리할 MED-V 이미지 결정</span><span class="sxs-lookup"><span data-stu-id="4c12a-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="4c12a-115">MED-V 최종 사용자를 정의한 후에는 각 위치의 사용자에 대해 MED-V로 관리 되는 Vm을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="4c12a-116">Vm이 중앙 라이브러리에 저장 되어 있는 경우 MED-V 리포지토리로 사용할 수 있도록 라이브러리의 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="4c12a-117">조직의 서비스 수준 기대치 확인</span><span class="sxs-lookup"><span data-stu-id="4c12a-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="4c12a-118">각 MED-V 작업 영역에 대해 새 이미지를 로드할 수 있는 시간과 배포할 중요 업데이트의 기간을 기록해 둡니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="4c12a-119">해당 하는 경우 서버 인프라 디자인에 사용할 MED-V 보고에 대 한 서비스 수준 기대치를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="4c12a-120">비즈니스에의 한 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="4c12a-120">Validate with the Business</span></span>


<span data-ttu-id="4c12a-121">비즈니스 관련자와 응용 프로그램 소유자에 게 다음 질문을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="4c12a-122">결합할 수 있는 기존 이미지가 있나요?</span><span class="sxs-lookup"><span data-stu-id="4c12a-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="4c12a-123">예를 들어 WindowsXP의 응용 프로그램 A가 하나의 VPC 이미지이 고, WindowsXP의 응용 프로그램 B가 또 다른 VPC image 인 경우 단일 이미지에는 두 응용 프로그램이 모두 포함 될 수 있으며, 따라서 이미지 다운로드에 필요한 저장소 공간과 대역폭이 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c12a-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="4c12a-124">MED-V에서 VM으로 제공 되는 경우 범위 내 응용 프로그램이 임베디드 하 고 지 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="4c12a-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="4c12a-125">응용 프로그램을 MED-V를 통해 제공 하는 방법으로 라이선스 및 지원 약관에 대해 문의 하는 것을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="4c12a-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





