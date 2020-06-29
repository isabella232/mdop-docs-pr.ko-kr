---
title: 가상 환경 정보
description: 가상 환경 정보
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822393"
---
# <span data-ttu-id="e5888-103">가상 환경 정보</span><span class="sxs-lookup"><span data-stu-id="e5888-103">About Virtual Environments</span></span>


<span data-ttu-id="e5888-104">가상 응용 프로그램은 가상 환경에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="e5888-105">가상 환경은 호스트 운영 체제의 설치 및 변경 없이 각 응용 프로그램을 데스크톱, 랩톱 또는 원격 데스크톱 세션 호스트 (RDSession Host) 서버에서 실행할 수 있게 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="e5888-106">각 응용 프로그램은 가상 환경에서 고유한 구성 정보를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="e5888-107">결과적으로 많은 응용 프로그램이 충돌 없이 동일한 컴퓨터의 다른 응용 프로그램과 나란히 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="e5888-108">가상 응용 프로그램은 전체 성능, 기능, 로컬로 설치 된 모든 응용 프로그램에서 예상할 수 있는 로컬 서비스에 대 한 액세스 권한으로 실행 되도록 로컬에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="e5888-109">각 응용 프로그램이 가상 환경에서 실행 되므로 다음과 같은 문제가 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="e5888-110">응용 프로그램 충돌-응용 프로그램 가상화를 사용 하지 않는 환경에서는 설치 된 다른 응용 프로그램에 방해가 되지 않도록 모든 응용 프로그램을 철저히 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="e5888-111">재발 테스트-응용 프로그램에서 기본 운영 체제를 변경 하지 않으므로 장기 재발 테스트는 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="e5888-112">버전 비 호환성-같은 응용 프로그램의 여러 버전이 동일한 컴퓨터에서 동시에 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="e5888-113">다중 사용자 액세스-다중 사용자 모드에서 실행 되지 않아 RDSession Host 내에서 실행할 수 없는 응용 프로그램인 경우에는 단일 RDSession Host에서 여러 사용자에 대해 올바르게 작동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="e5888-114">Multitenancy 문제-서로 다른 구성을 사용 하는 동일한 응용 프로그램의 두 인스턴스가 동시에 같은 컴퓨터에서 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="e5888-115">서버 siloing-여러 개별 서버 팜에 대 한 요구 사항이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="e5888-116">가상 환경에는 각 응용 프로그램에 대 한 가상 레지스트리가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="e5888-117">한 응용 프로그램에서 만든 레지스트리 설정은 다른 응용 프로그램 또는 Regedit 등의 유틸리티를 통해 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="e5888-118">가상 레지스트리는 전체 레지스트리를 복사 하는 대신 *오버레이* 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="e5888-119">해당 레지스트리 항목의 가상 복사본이 가상 레지스트리에 포함 되어 있지 않은 경우에는 응용 프로그램에서 클라이언트 레지스트리의 항목을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="e5888-120">레지스트리에 대 한 모든 응용 프로그램 쓰기는 가상 레지스트리에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="e5888-121">가상 환경에는 가상 파일 시스템 및 가상 서비스와 가상 COM을 비롯 한 다른 가상 구성 요소도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5888-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="e5888-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e5888-122">Related topics</span></span>


[<span data-ttu-id="e5888-123">Application Virtualization Client Management Console 개요</span><span class="sxs-lookup"><span data-stu-id="e5888-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





