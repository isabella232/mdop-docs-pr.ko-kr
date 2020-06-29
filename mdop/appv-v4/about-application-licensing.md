---
title: 응용 프로그램 라이선스 정보
description: 응용 프로그램 라이선스 정보
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820098"
---
# <span data-ttu-id="63702-103">응용 프로그램 라이선스 정보</span><span class="sxs-lookup"><span data-stu-id="63702-103">About Application Licensing</span></span>


<span data-ttu-id="63702-104">Application Virtualization 서버 관리 콘솔에서 직접 응용 프로그램 라이선스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="63702-105">라이선스 유형</span><span class="sxs-lookup"><span data-stu-id="63702-105">License Types</span></span>


<span data-ttu-id="63702-106">현재 System Center Application Virtualization System은 다음 라이선스 유형을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="63702-107">**무제한 라이선스**-동시 사용자 수에 관계 없이 응용 프로그램에 대 한 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="63702-108">이 라이선스 방법은 엔터프라이즈 차원의 라이선스를 응용 프로그램과 연결 하려는 경우에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="63702-109">**동시 라이선스**-응용 프로그램을 사용할 수 있는 최대 동시 사용자 수를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="63702-110">**라이선스 명명**— 개별 사용자에 게 라이선스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="63702-111">명명 된 라이선스를 사용 하 여 특정 사용자가 항상 응용 프로그램을 실행할 수 있도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="63702-112">동일한 응용 프로그램에 대해 동시 및 명명 된 라이선스를 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="63702-113">라이선스는 기본적으로 사용 하지 않도록 설정 되어 있지만, **공급자 속성** 대화 상자의 **공급자 파이프라인** 탭에서 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="63702-114">라이선스 사용 및 사용 안 함에 대 한 자세한 내용은 [응용 프로그램 라이선스 설정 또는 해제 방법을](how-to-set-up-or-disable-application-licensing.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63702-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="63702-115">공급자 정책</span><span class="sxs-lookup"><span data-stu-id="63702-115">Provider Policies</span></span>


<span data-ttu-id="63702-116">공급자 정책은 ASP (응용 프로그램 서비스 공급자) 모델에 맞게 개발 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="63702-117">이 모델에서 단일 ASP는 여러 클라이언트에 대해 단일 응용 프로그램 가상화 시스템을 호스트할 수 있으며, 각 클라이언트는 격리 된 상태를 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="63702-118">클라이언트는 요구 사항이 매우 다를 수 있으 나, 예를 들어 클라이언트가 인증을 요구 하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="63702-119">공급자 정책을 사용 하 여 사용 권한을 클라이언트와 연결 하 여 승인 된 사용자만 각 가상 응용 프로그램 또는 가상 응용 프로그램 패키지에 액세스할 수 있도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="63702-120">엔터프라이즈 고객의 경우 하나 이상의 응용 프로그램에 대해 엄격한 라이선스 요구 사항이 있는 경우이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="63702-121">이 상황에서는 **공급자 속성** 대화 상자의 **공급자 파이프라인** 탭에서 라이선스 구성 요소를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="63702-122">또한 **공급자 파이프라인** 탭에는 인증, 권한 부여 (**액세스 권한 설정 적용**), 계량 (**로그 사용 정보**)을 사용 하도록 설정 하는 확인란이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="63702-123">구성에 특별 한 요구 사항이 있는 경우 고유한 파이프라인 구성 요소를 작성 하 고 **고급** 단추를 클릭 하 여 시스템에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="63702-124">계정 기관</span><span class="sxs-lookup"><span data-stu-id="63702-124">Account Authorities</span></span>


<span data-ttu-id="63702-125">계정 기관은 응용 프로그램 가상화 서버가 설치 된 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="63702-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="63702-126">서버 설치를 진행할 때 도메인 이름을 제공 하 라는 메시지가 표시 됩니다. 컴퓨터가 설치 된 도메인이 검색 되 고 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63702-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="63702-127">사용자가 시스템에 로그인을 시도 하면 해당 도메인에 액세스할 수 있으려면 먼저 자격 증명을 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63702-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="63702-128">Application Virtualization System은 여러 도메인을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="63702-129">도메인 간에 신뢰 관계가 설정 된 경우 다른 도메인의 사용자 그룹에 대 한 응용 프로그램 액세스를 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="63702-130">사용자는 각 도메인에서 인식 하는 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="63702-131">Application Virtualization 서버 관리 콘솔에서 주 도메인 (계정 권한)과이에 액세스 하는 데 사용 되는 자격 증명을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="63702-132">인증</span><span class="sxs-lookup"><span data-stu-id="63702-132">Authentication</span></span>


<span data-ttu-id="63702-133">인증은 사용자의 id를 확인 하는 데 사용 되는 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="63702-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="63702-134">사용자 이름 및 암호를 인식 하는 모든 사용자에 게 액세스 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="63702-135">Application Virtualization 시스템에서는 **공급자 파이프라인** 탭의 확인란을 통해 인증을 사용 하거나 사용 하지 않도록 설정할 수 있습니다. 기본적으로 Windows 인증이 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="63702-136">권한 부여</span><span class="sxs-lookup"><span data-stu-id="63702-136">Authorization</span></span>


<span data-ttu-id="63702-137">권한 부여는 사용자의 id를 확인 하는 데 사용 되는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="63702-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="63702-138">사용자의 id를 확인 한 후 시스템은 사용자에 게 시스템에 대 한 액세스 권한을 부여 했는지 여부와 사용자에 게 액세스 권한이 부여 된 응용 프로그램을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="63702-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="63702-139">응용 프로그램 가상화 서버 관리 콘솔에는 권한 부여를 사용 하거나 사용 하지 않도록 설정 하는 **공급자 파이프라인** 탭의 **액세스 권한 설정 적용** 확인란이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63702-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="63702-140">응용 프로그램 가상화 시스템에서는 개별 사용자가 아닌 사용자 그룹에만 액세스 권한이 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63702-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="63702-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="63702-141">Related topics</span></span>


[<span data-ttu-id="63702-142">Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="63702-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="63702-143">응용 프로그램 라이선스를 설정 또는 사용 중지하는 방법</span><span class="sxs-lookup"><span data-stu-id="63702-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="63702-144">Server Management Console: 공급자 정책 노드</span><span class="sxs-lookup"><span data-stu-id="63702-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





