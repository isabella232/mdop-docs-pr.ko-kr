---
title: DaRT 7.0 정보
description: DaRT 7.0 정보
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823273"
---
# <span data-ttu-id="80ee7-103">DaRT 7.0 정보</span><span class="sxs-lookup"><span data-stu-id="80ee7-103">About DaRT 7.0</span></span>


<span data-ttu-id="80ee7-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7은 Windows 기반 데스크톱의 문제를 해결 하 고 복구 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 helps you troubleshoot and repair Windows-based desktops.</span></span> <span data-ttu-id="80ee7-105">여기에는 시작할 수 없는 데스크톱도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-105">This includes those desktops that cannot be started.</span></span> <span data-ttu-id="80ee7-106">DaRT는 Windows 복구 환경 (WinRE)을 확장 하는 강력한 도구 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-106">DaRT is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="80ee7-107">DaRT를 사용 하 여 컴퓨터의 이벤트 로그 또는 시스템 레지스트리를 검사 하는 등의 문제를 분석 하 여 원인을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span>

<span data-ttu-id="80ee7-108">DaRT는 원인을 파악 하는 즉시 문제를 해결 하는 데 도움이 되는 도구를 제공 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-108">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="80ee7-109">예를 들어 DaRT의 도구를 사용 하 여 결함이 있는 장치 드라이버를 사용 하지 않도록 설정 하 고, 삭제 된 파일을 복원 하 고, 컴퓨터에 맬웨어를 검색 하 여 설치 된 Windows 운영 체제를 시작할 수 없는 경우에도이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-109">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="80ee7-110">DaRT는 Windows 7의 32 비트 또는 64 비트 버전을 실행 하는 컴퓨터를 빠르게 복구 하는 데 도움이 될 수 있습니다. 일반적으로 컴퓨터를 이미지로 복원 하는 것 보다 시간이 짧습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-110">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 7, typically in less time than it would take to reimage the computer.</span></span>

## <span data-ttu-id="80ee7-111">DaRT 7 복구 이미지 정보</span><span class="sxs-lookup"><span data-stu-id="80ee7-111">About the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="80ee7-112">DaRT의 기능을 사용 하면 DaRT가 제공 하는 도구 집합과 함께 WinRE를 기반으로 하는 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-112">Functionality in DaRT lets you create a recovery image that is based on WinRE combined with a set of tools that DaRT provides.</span></span> <span data-ttu-id="80ee7-113">DaRT 복구 이미지는 **진단 및 복구 도구 집합** 창에 액세스할 수 있는 WinRE를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-113">The DaRT recovery image takes advantage of WinRE, from which you can access the **Diagnostics and Recovery Toolset** window.</span></span>

<span data-ttu-id="80ee7-114">Dart 복구 **이미지 마법사** 를 사용 하 여 dart 복구 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-114">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="80ee7-115">기본적으로 마법사에서는 다른 위치와 파일 이름을 지정할 수 있지만 DaRT70 이라는 이름의 국제 표준화 (ISO) 이미지 파일을 바탕 화면에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-115">By default, the wizard creates an International Organization for Standardization (ISO) image file on your desktop that is named DaRT70.iso, although you can specify a different location and file name.</span></span> <span data-ttu-id="80ee7-116">마법사를 사용 하 여 이미지를 CD 또는 DVD에 구울 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-116">The wizard also lets you burn the image to a CD or DVD.</span></span> <span data-ttu-id="80ee7-117">마법사를 완료 한 후에는 복구 이미지를 USB 플래시 드라이브에 저장 하거나 원격 파티션이나 복구 파티션을 만드는 데 사용할 수 있는 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-117">After you have finished the wizard, you can save the recovery image to a USB flash drive or save it in a format that you can use to create a remote partition or a recovery partition.</span></span>

<span data-ttu-id="80ee7-118">DaRT를 사용 하 여 시작 되지 않는 최종 사용자 컴퓨터를 시작 해야 하는 경우 [Dart 복구 이미지를 사용 하 여 로컬 컴퓨터를 복구 하는 방법](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)에 대 한 지침을 따를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-118">When you have to use DaRT to startup an end-user computer that will not start, you can follow the instructions at [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="80ee7-119">DaRT의 도구에 대 한 자세한 내용은 [dart 7.0의 도구 개요](overview-of-the-tools-in-dart-70-new-ia.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80ee7-119">For detailed information about the tools in DaRT, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

## <a href="" id="what-s-new-in-dart-7"></a><span data-ttu-id="80ee7-120">DaRT 7의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="80ee7-120">What’s New in DaRT 7</span></span>


<span data-ttu-id="80ee7-121">DaRT7는 이전 버전에 포함 된 모든 시나리오를 계속 지원 하 고 새로운 원격 연결 기능을 세 가지 새 배포 옵션 외에도 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-121">DaRT7 continues to support all the scenarios included in previous versions and it adds a new Remote Connection feature in addition to three new deployment options.</span></span>

### <span data-ttu-id="80ee7-122">DaRT 7 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="80ee7-122">DaRT 7 Image Creation</span></span>

<span data-ttu-id="80ee7-123">DaRT ISO 이미지를 만드는 데 사용 하는 마법사를 이제 **Dart 복구 이미지** 라고 하며, 이제 새 원격 연결 기능을 사용 하거나 사용 하지 않도록 설정할 수 있는 옵션이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-123">The wizard that you use to create DaRT ISO images is now called **DaRT Recovery Image** and it now supports an option to enable or disable the new Remote Connection feature.</span></span> <span data-ttu-id="80ee7-124">원격 연결을 통해 헬프데스크 에이전트는 원격 위치에서 DaRT 도구를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-124">Remote Connection lets a helpdesk agent run the DaRT tools from a remote location.</span></span> <span data-ttu-id="80ee7-125">이전 릴리스에서는 기술 지원팀 상담원을 물리적으로 최종 사용자 컴퓨터에 설치 하 여 DaRT 도구를 실행할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-125">In previous releases, the helpdesk agent had to be physically present at the end-user computer to run the DaRT tools.</span></span>

<span data-ttu-id="80ee7-126">마법사를 사용 하 여 원격 연결 기능에 대 한 환영 메시지를 사용자 지정할 수도 있습니다 (메시지는 최종 사용자가 원격 연결 도구를 실행할 때 표시 됨).</span><span class="sxs-lookup"><span data-stu-id="80ee7-126">The wizard also lets you customize the Welcome message for the Remote Connection feature (the message is shown when end users run the Remote Connection tool).</span></span> <span data-ttu-id="80ee7-127">또한 관리자는 원격 연결에서 사용 해야 하는 포트 번호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-127">IT Admins can also configure which Port Number should be used by Remote Connection.</span></span>

<span data-ttu-id="80ee7-128">**Dart 복구 이미지 마법사** 또는 원격 연결에 대 한 자세한 내용은 [Dart 7.0 복구 이미지 만들기](creating-the-dart-70-recovery-image-dart-7.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80ee7-128">For more information about the **DaRT Recovery Image Wizard** or Remote Connection, see [Creating the DaRT 7.0 Recovery Image](creating-the-dart-70-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="80ee7-129">DaRT 7 ISO 배포</span><span class="sxs-lookup"><span data-stu-id="80ee7-129">DaRT 7 ISO Deployment</span></span>

<span data-ttu-id="80ee7-130">CD 또는 DVD에 굽는 것 외에도 DaRT7는 DaRT 복구 이미지가 포함 된 ISO를 배포할 때 다음과 같은 세 가지 새로운 옵션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-130">In addition to burning to a CD or DVD, DaRT7 adds three new options when you deploy the ISO that contains the DaRT recovery image:</span></span>

-   <span data-ttu-id="80ee7-131">USB 플래시 드라이브 배포</span><span class="sxs-lookup"><span data-stu-id="80ee7-131">USB flash drive deployment</span></span>

-   <span data-ttu-id="80ee7-132">원격 파티션 배포</span><span class="sxs-lookup"><span data-stu-id="80ee7-132">Remote partition deployment</span></span>

-   <span data-ttu-id="80ee7-133">복구 파티션 배포</span><span class="sxs-lookup"><span data-stu-id="80ee7-133">Recovery partition deployment</span></span>

<span data-ttu-id="80ee7-134">USB 플래시 드라이브 배포 옵션을 사용 하면 회사가 CD 또는 DVD 드라이브를 사용할 수 없는 컴퓨터에서 DaRT를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-134">The USB flash drive deployment option lets a company use DaRT on computers that do not have CD or DVD drives available.</span></span> <span data-ttu-id="80ee7-135">복구 및 원격 파티션 옵션을 통해 최종 사용자가 DaRT 이미지에 쉽게 액세스 하 고 원격 연결 기능을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee7-135">The recovery and remote partition options let end users have easy access to the DaRT image and to enable the Remote Connection functionality.</span></span>

<span data-ttu-id="80ee7-136">DaRT 복구 이미지를 배포 하는 방법에 대 한 자세한 내용은 [dart 7.0 복구 이미지 배포](deploying-the-dart-70-recovery-image-dart-7.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80ee7-136">For more information about how to deploy DaRT recovery images, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="80ee7-137">관련 항목</span><span class="sxs-lookup"><span data-stu-id="80ee7-137">Related topics</span></span>


[<span data-ttu-id="80ee7-138">DaRT 7.0 시작</span><span class="sxs-lookup"><span data-stu-id="80ee7-138">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

[<span data-ttu-id="80ee7-139">DaRT 7.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="80ee7-139">Release Notes for DaRT 7.0</span></span>](release-notes-for-dart-70-new-ia.md)

 

 





