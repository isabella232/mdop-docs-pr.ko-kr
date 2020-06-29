---
title: 응용 프로그램 운영 체제 호환성 계획
description: 응용 프로그램 운영 체제 호환성 계획
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825468"
---
# <span data-ttu-id="8b6a0-103">응용 프로그램 운영 체제 호환성 계획</span><span class="sxs-lookup"><span data-stu-id="8b6a0-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="8b6a0-104">이 항목에서는 응용 프로그램 운영 체제 호환성 문제를 해결 하는 방법을 결정 하 고 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0을 조직의 솔루션으로 작동 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="8b6a0-105">이 항목에서는 MED-V에 대 한 비즈니스 요구 사항에 대해 설명 하 고 MED-V와 Windows XP 모드 및 Microsoft Application Virtualization (App-v)을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="8b6a0-106">MED-V에 대 한 비즈니스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="8b6a0-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="8b6a0-107">MED-V와 Windows XP 모드 비교의 이점</span><span class="sxs-lookup"><span data-stu-id="8b6a0-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="8b6a0-108">MED-V 대 app-v와의 이점-V</span><span class="sxs-lookup"><span data-stu-id="8b6a0-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="8b6a0-109">MED-V에 대 한 비즈니스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="8b6a0-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="8b6a0-110">회사의 IT 부서가 Windows 7로 업그레이드할지 여부를 결정 하는 경우, 해당 비즈니스 응용 프로그램 및 웹 기반 lob (기간 업무) 응용 프로그램에 주의를 기울여야 하며,이를 새 운영 체제에서 실행할 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="8b6a0-111">이러한 응용 프로그램 및 Url은 일반적으로 이전 버전의 Windows 또는 Internet Explorer를 사용 하 여 작동 하도록 만들어졌으며 새 운영 체제에서 사용 하려고 할 때 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="8b6a0-112">Microsoft는 ACT (응용 프로그램 호환성 도구 키트) 및 Windows 7 프로그램 호환성 도우미와 같이 업그레이드할 때 발생할 수 있는 다양 한 호환성 문제를 처리 하는 다양 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="8b6a0-113">모든 응용 프로그램이 호환성 및 수정 사항을 확인 한 후에도 Windows 7에서 일부 응용 프로그램이 올바르게 작동 하지 않거나 해결 하는 데 너무 많은 비용이 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="8b6a0-114">MED-V를 사용 하 여 Windows XP를 실행 하는 Windows 가상 PC 환경을 통해 이러한 레거시 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="8b6a0-115">업그레이드 하기 전에 새 운영 체제에서 이러한 문제가 발생 하는 응용 프로그램을 더 이상 테스트 하 고 유효성을 검사할 필요가 없기 때문에 Windows 7로 마이그레이션하는 것이 훨씬 더 빠르고 빠릅니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="8b6a0-116">MED-V 검사 목록 사용</span><span class="sxs-lookup"><span data-stu-id="8b6a0-116">Using MED-V Checklist</span></span>

<span data-ttu-id="8b6a0-117">다음 시나리오 중 하나가 적용 되는 경우 MED-V를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="8b6a0-118">예를 들어 500 사용자 등의 대규모 조직에서 Microsoft와 엔터프라이즈 계약을 체결 하 고 Windows 7로 업그레이드 계획을 수립할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="8b6a0-119">Lob (기간 업무) 응용 프로그램을 테스트 했 고 Windows 7과 호환 되지 않는 기능을 발견 했습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="8b6a0-120">응용 프로그램을 업그레이드 하거나 (ACT (응용 프로그램 호환성 도구 키트)와 같이 Microsoft에서 제공 하는 shim을 사용 하 여 이러한 문제에 대 한 호환성 문제를 해결 했지만 일부 응용 프로그램에 대해서는 호환성 문제가 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="8b6a0-121">호환 되지 않는 응용 프로그램을 제공 하기 위한 옵션으로 App-v를 사용 하 고 있지만 App-v를 구현한 후에는 처리 해야 하는 응용 프로그램 운영 체제 호환성 문제가 발생 하는 것으로 결론을 끝냈습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="8b6a0-122">Windows XP 모드를 솔루션으로 간주 하 고 다음 이유 때문에 효율적인 옵션이 아닌 것으로 확인 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="8b6a0-123">문제가 있는 응용 프로그램을 포함 하는 가상 이미지를 개별적으로 사용 하지 않고 동시에 모든 최종 사용자에 게 배포 하 고 가상 이미지가 자동으로 도메인에 연결 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="8b6a0-124">이러한 레거시 응용 프로그램 (실제로는이를 제공)을 관리 하 고 각 최종 사용자의 데스크톱이 아닌 중앙 위치에서 Windows 가상 PC 설정을 제어 하는 것이 훨씬 더 비용 효율적인 것으로 결정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="8b6a0-125">데스크톱 대신 크기 조정에서 가상 컴퓨터를 업데이트 하 고 지원할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="8b6a0-126">이전 버전의 Internet Explorer에서 더 잘 실행 되는 Url을 가상 컴퓨터로 리디렉션 하 고 나중에 간편 하 게 URL 리디렉션을 관리 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="8b6a0-127">더욱 비용 효율적이 고 가능한 한 빨리 Windows 7으로 업그레이드 하는 것이 좋습니다 .이는 MED-V에서 사용할 수 있는 솔루션이 있다는 사실을 감안 하 여 나중 날짜까지 나머지 응용 프로그램 호환성 문제를 해결 하기로 결정 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="8b6a0-128">MED-V와 Windows XP 모드 비교의 이점</span><span class="sxs-lookup"><span data-stu-id="8b6a0-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="8b6a0-129">Windows 7 용 windows 가상 PC를 사용 하면 단일 장치에서 여러 버전의 운영 체제를 동시에 실행 하 고 Windows 7 Professional Edition 이상에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="8b6a0-130">Windows XP 모드 기능은 가상 Windows XP 환경을 만들 수 있는 미리 구성 된 Windows XP 이미지를 제공 하 여 Windows 가상 PC를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="8b6a0-131">이 가상 환경에서는 Windows 7과 호환 되지 않으며 Windows 가상 PC를 통해 데스크톱에서 원활 하 게 실행 되는 응용 프로그램을 수동으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="8b6a0-132">Windows XP 모드를 사용 하 여 다음을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="8b6a0-133">Windows 가상 PC에서 실행 되는 가상 컴퓨터 내에서 Windows XP와 호환 되는 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="8b6a0-134">이러한 응용 프로그램을 호스트의 데스크톱 또는 프로그램 메뉴에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="8b6a0-135">Windows 7로 엔터프라이즈 마이그레이션의 일부로 이러한 가상 컴퓨터를 대규모으로 제공 하려는 경우 가상 컴퓨터를 빠르게 배포 하 고, 프로 비전 하 고, 효율적으로 사용자 지정 하 고, 설정을 제어 하 고, 쉽게 지원할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="8b6a0-136">MED-V는 엔터프라이즈 전체에 걸친 응용 프로그램 호환성을 제공 하기 위해 Windows XP 모드를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="8b6a0-137">Windows XP 모드는 개인 및 중소기업에 가상 응용 프로그램 기능을 제공 하도록 제한 된 반면 MED-V는 회사 네트워크 전체에서 미리 구성 된 Windows XP 이미지를 대규모으로 배포할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="8b6a0-138">이러한 가상 MED-V 작업 영역의 구성, 배포 및 유지 관리를 위한 엔터프라이즈 맞춤형 관리 솔루션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="8b6a0-139">MED-V는 또한 이미지 사용을 제어 하는 정책 집합을 enterpriseadministrators에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="8b6a0-140">여기에는 이러한 이미지 내의 특정 응용 프로그램에 액세스할 수 있는 사용자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="8b6a0-141">MED-V를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="8b6a0-142">호환 되지 않는 모든 응용 프로그램 및 URL을 테스트 하 고 해결할 필요 없이 새 운영 체제로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="8b6a0-143">사용자 당 자동으로 도메인에 가입 하 고 사용자 지정 된 가상 Windows XP 이미지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="8b6a0-144">사용자에 게 응용 프로그램 및 URL 리디렉션 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="8b6a0-145">Windows 가상 PC 설정을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="8b6a0-146">모니터링 및 문제 해결을 통해 끝점을 유지 관리 하 고 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="8b6a0-147">일시 중단 된 상태인 경우에도 게스트 컴퓨터에 패치가 적용 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="8b6a0-148">사용자별 가상 컴퓨터 만들기 및 sysprep 초기화를 자동화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="8b6a0-149">호스트 및 게스트 컴퓨터의 문제를 쉽게 진단할.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="8b6a0-150">Windows Virtual PC NAT 모드를 통해 연결 된 게스트 컴퓨터를 원활 하 게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="8b6a0-151">MED-V 대 app-v와의 이점-V</span><span class="sxs-lookup"><span data-stu-id="8b6a0-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="8b6a0-152">MED-V와 App-v는 서로 쉽게 상호 작용 하 여 응용 프로그램 운영 체제 호환성 문제를 해결할 수 있는 두 가지 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="8b6a0-153">App-v를 사용 하 여 각 응용 프로그램에 대 한 개별화 패키지를 만든 다음 다른 사용자와 별도로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="8b6a0-154">그러면 각 가상 응용 프로그램이 최종 사용자에 게 즉시 전달 될 수 있으며,이는 Windows 7 배포 전략에 매우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="8b6a0-155">MED-V는 응용 프로그램을 개별적으로 처리 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="8b6a0-156">대신 Windows 7을 실행 하는 동일한 데스크톱에 Windows XP의 추가 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="8b6a0-157">필요에 따라이 가상 이미지에 응용 프로그램을 설치 하 고 조직의 다른 데스크톱에서와 마찬가지로 이미지를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="8b6a0-158">또한 MED-V를 사용 하 여 app-v를 통해 시퀀싱 되는 가상 응용 프로그램을 설치 하 고, 게시 하 고 관리 하는 등의 기능을 App-v와 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b6a0-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="8b6a0-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8b6a0-159">Related topics</span></span>


[<span data-ttu-id="8b6a0-160">MED-V 배포 정의 및 계획</span><span class="sxs-lookup"><span data-stu-id="8b6a0-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 





