---
title: MED-V 2.0의 새로운 기능
description: MED-V 2.0의 새로운 기능
author: dansimp
ms.assetid: 53b10bff-2b6f-463b-bdc2-5edc56526792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 78dba25fec7ae2bb41da00902b59dcd15030f2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823703"
---
# <span data-ttu-id="fcabb-103">MED-V 2.0의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="fcabb-103">What's New in MED-V 2.0</span></span>


<span data-ttu-id="fcabb-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0는 Windows 7에 대 한 응용 프로그램 호환성 지원을 발전 했으며이 시나리오에서는 필요 하지 않은 기능을 제거 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 has evolved the application compatibility support for Windows 7 and removed functionality that is not required for this scenario.</span></span> <span data-ttu-id="fcabb-105">예를 들어 MED-V 작업 영역의 암호화, 중앙 집중화 된 MED-V 서버, MED-V 작업 영역 트리밍 전송 등의 기능이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-105">For example, features such as encryption of the MED-V workspace, the centralized MED-V server, and MED-V workspace trim transfer have been removed.</span></span>

## <span data-ttu-id="fcabb-106">표준 기능 변경</span><span class="sxs-lookup"><span data-stu-id="fcabb-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="fcabb-107">이 섹션에서는 MED-V 2.0 기능이 변경 된 주요 영역에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-107">This section discusses the key areas where MED-V 2.0 functionality has changed.</span></span>

### <span data-ttu-id="fcabb-108">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="fcabb-108">MED-V Workspace Creation</span></span>

<span data-ttu-id="fcabb-109">이제 MED-V 작업 영역에 사용 되는 가상 하드 디스크가 Windows 가상 PC에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-109">The virtual hard disk used for the MED-V workspace is now created in Windows Virtual PC.</span></span> <span data-ttu-id="fcabb-110">MED-V 작업 영역을 만드는 데 사용 되는 방법에는 Windows XP SP3 설치, 운영 체제 업데이트, 소프트웨어 관리 인프라를 통해 관리 하도록 준비 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-110">The methods that are used to create the MED-V workspace include installing Windows XP SP3, updating the operating system, and preparing it to be managed through software management infrastructure.</span></span>

<span data-ttu-id="fcabb-111">전용 MED-V 작업 영역 암호화 및 압축 기능 외에도 오프 라인 관리 및 트리밍 전송 기능이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-111">The offline management and trim transfer functionality were removed, in addition to the proprietary MED-V workspace encryption and compression functionality.</span></span> <span data-ttu-id="fcabb-112">MED-V 작업 영역을 만들 때 관리자는 MED-V 1.0에서 제공 하는 가상 컴퓨터 준비 도구를 사용 하는 대신 이미지의 적절 한 응용 프로그램 및 관리 도구를 준비 하 고 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-112">When you create a MED-V workspace, an administrator should prepare and configure appropriate applications and management tools in the image instead of using the virtual machine preparation tool that is provided in MED-V 1.0.</span></span>

<span data-ttu-id="fcabb-113">Med-v 작업 영역을 패키지화 하는 동안 MED-V 이미지에서 Sysprep를 실행 하는 것은 이제 필수 이며 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-113">Running Sysprep on the MED-V image is now required and validated during the packaging of the MED-V workspace.</span></span> <span data-ttu-id="fcabb-114">MED-V 작업 영역 포장기는 패키지 프로세스를 통해 관리자를 안내 하는 GUI (그래픽 사용자 인터페이스)를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-114">The MED-V Workspace Packager provides a graphical user interface (GUI) that guides the administrator through the packaging process.</span></span> <span data-ttu-id="fcabb-115">MED-V 1.0의 콘솔은 이미지 관리 기능, MED-V 작업 영역 프로필 관리, MED-V 작업 영역을 단계별로 진행 하 고 암호화 하는 요구 사항과 함께 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-115">The console from MED-V 1.0 was removed together with the functionality of managing images, managing MED-V workspace profiles, and the requirement to stage and encrypt MED-V workspaces.</span></span>

### <span data-ttu-id="fcabb-116">MED-V 작업 영역 배포</span><span class="sxs-lookup"><span data-stu-id="fcabb-116">MED-V Workspace Deployment</span></span>

<span data-ttu-id="fcabb-117">MED-V 작업 영역을 배포 하기 위해 관리자는 이제 전자 소프트웨어 배포 도구를 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-117">To deploy a MED-V workspace, an administrator is now able to take advantage of their electronic software distribution tools.</span></span> <span data-ttu-id="fcabb-118">MED-V 1.0에서 사용할 수 있는 클라이언트 pull 메서드가 제거 되었으며 med-v 외부의 메서드를 사용 하 여 MED-V 작업 영역이 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-118">The client-pull method available in MED-V 1.0 was removed and the MED-V workspace is now delivered by using methods outside MED-V.</span></span> <span data-ttu-id="fcabb-119">관리자는 다른 응용 프로그램 패키지 에서처럼 MED-V 작업 영역을 처리 하 고 기존 도구 및 프로세스를 사용 하 여 MED-V의 배포 및 설치를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-119">Administrators can treat MED-V workspaces as they would any other application package and can schedule deployments and installations of MED-V by using their existing tools and processes.</span></span> <span data-ttu-id="fcabb-120">MED-V 설치는 자동으로 배포 될 수 있으며 기존 소프트웨어 배포 인프라 내에서 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-120">MED-V installations can be deployed silently and can easily be managed inside an existing software distribution infrastructure.</span></span>

### <span data-ttu-id="fcabb-121">MED-V 작업 영역 관리</span><span class="sxs-lookup"><span data-stu-id="fcabb-121">MED-V Workspace Management</span></span>

<span data-ttu-id="fcabb-122">MED-V 2.0의 MED-V 작업 영역은 Windows 가상 PC 가상 하드 디스크를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-122">The MED-V workspace in MED-V 2.0 is based on a Windows Virtual PC virtual hard disk.</span></span> <span data-ttu-id="fcabb-123">MED-V는 MED-V 작업 영역에 액세스 하는 데 암호화 또는 특수 도구가 필요 하지 않은 원활한 환경을 개선 하 여 Windows 가상 PC가 제공 하는 기능을 확장 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-123">MED-V has extended the capabilities that Windows Virtual PC provides by improving the seamless experience without requiring encryption or special tools to access the MED-V workspace.</span></span>

<span data-ttu-id="fcabb-124">MED-V가 워크스테이션에 배포 된 후에는 Windows 가상 PC를 사용 하 여 MED-V 작업 영역을 전체 화면 모드로 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-124">After MED-V is deployed to a workstation, the MED-V workspace can be opened in full-screen mode by using Windows Virtual PC.</span></span> <span data-ttu-id="fcabb-125">이 새로운 기능은 원활한 또는 전체 화면 모드에 대 한 기본 설정을 지정 하 고 진단 및 문제 해결을 위해 전체 화면을 강제로 제거 해야 하는 정책에 대 한 요구 사항을 제거 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-125">This new functionality removed the requirement for policies that set a preference for seamless or full-screen modes and also removed the need to force full-screen for diagnostics and troubleshooting.</span></span>

<span data-ttu-id="fcabb-126">MED-V 작업 영역에 대 한 응용 프로그램 게시는 프로필을 통해 더 이상 수행 되지 않으며 수동으로 응용 프로그램 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-126">Publishing applications to the MED-V workspace is no longer performed with profiles and by manually entering the path to applications.</span></span> <span data-ttu-id="fcabb-127">대신, 응용 프로그램이 게스트에 설치 되 면 자동으로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-127">Instead, it occurs automatically as applications are installed on the guest.</span></span> <span data-ttu-id="fcabb-128">트리밍 전송을 통해 제공 된 이미지 버전이 포함 된 중앙 이미지 리포지토리가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-128">The central image repository that included versions of the images that were delivered through trim transfer is removed.</span></span> <span data-ttu-id="fcabb-129">대신, MED-V는 전용 MED-V 인프라의 복잡성 없이 응용 프로그램 및 업데이트를 배포 하 여 실제 컴퓨터와 마찬가지로 관리자가 MED-V 작업 영역을 관리할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-129">Instead, MED-V enables administrators to manage the MED-V workspace as they would a physical computer, by letting applications and updates be distributed without the complexity of a dedicated MED-V infrastructure.</span></span>

## <span data-ttu-id="fcabb-130">MED-V 기능의 변경 내용</span><span class="sxs-lookup"><span data-stu-id="fcabb-130">Changes in MED-V Features</span></span>


<span data-ttu-id="fcabb-131">MED-V 2.0의 몇 가지 주요 영역에는 다음 기능에 대 한 개선 사항이 나 추가 내용이 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-131">Several key areas of MED-V 2.0 reflect improvements or additions to the following features.</span></span>

### <span data-ttu-id="fcabb-132">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="fcabb-132">MED-V Workspace Creation</span></span>

<span data-ttu-id="fcabb-133">MED-V 작업 영역은 Windows 가상 PC를 사용 하 여 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-133">MED-V workspaces must be created by using Windows Virtual PC.</span></span> <span data-ttu-id="fcabb-134">기존 Virtual PC 2007 이미지는 마이그레이션해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-134">Existing Virtual PC 2007 images must be migrated.</span></span> <span data-ttu-id="fcabb-135">가상 컴퓨터 준비 도구는 MED-V 2.0에 포함 되어 있지 않으며 관리자는 MED-V 2.0 도움말 파일에 따라 이미지를 구성, 업데이트 및 최적화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-135">The virtual machine Prep tool is not included in MED-V 2.0 and administrators should configure, update, and optimize their images according to the MED-V 2.0 Help file.</span></span> <span data-ttu-id="fcabb-136">MED-V 이미지에서 Sysprep를 실행 하는 것은 필수 단계 이므로 패키지 하기 전에 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-136">Running Sysprep on the MED-V image is a required step and must be performed before packaging.</span></span>

### <span data-ttu-id="fcabb-137">MED-V 작업 영역 패키징</span><span class="sxs-lookup"><span data-stu-id="fcabb-137">MED-V Workspace Packaging</span></span>

<span data-ttu-id="fcabb-138">Windows PowerShell은 MED-V 작업 영역 포장기의 기반입니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-138">Windows PowerShell is the foundation of the MED-V Workspace Packager.</span></span> <span data-ttu-id="fcabb-139">이 기능은 MED-V의 중앙 집중화 된 함수를 관리 하는 일부 이전 콘솔 기능을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-139">This functionality replaces some former console abilities and functionality that managed centralized functions of MED-V.</span></span> <span data-ttu-id="fcabb-140">MED-V 작업 영역 포장기는 관리자가 쉽게 배포할 수 있도록 적절 한 설정 및 이미지를 사용 하 여 가상 하드 디스크를 패키지화 하기만 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-140">The MED-V Workspace Packager merely packages the virtual hard disk with the appropriate settings and image so that it can be easily deployed by administrators.</span></span> <span data-ttu-id="fcabb-141">고급 기능은 Windows PowerShell을 사용 하 여 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-141">Advanced features are provided by using Windows PowerShell.</span></span>

### <span data-ttu-id="fcabb-142">MED-V 작업 영역 배포</span><span class="sxs-lookup"><span data-stu-id="fcabb-142">MED-V Workspace Distribution</span></span>

<span data-ttu-id="fcabb-143">전용 서버 인프라는 MED-V 2.0에 더 이상 필요 하지 않으며 MED-V 작업 영역을 배포 하기 위한 클라이언트 pull 메서드가 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-143">Dedicated server infrastructure is no longer required for MED-V 2.0 and the client pull method to deploy MED-V workspaces was removed.</span></span> <span data-ttu-id="fcabb-144">MED-V 작업 영역은 이제 전자 소프트웨어 배포 인프라를 사용 하 여 배포 되며 다른 설치 패키지에 사용 되는 일반 공유에 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-144">MED-V workspaces are now deployed using your electronic software distribution infrastructure and can be stored on common shares that are used for other installation packages.</span></span>

### <span data-ttu-id="fcabb-145">처음 설치 시</span><span class="sxs-lookup"><span data-stu-id="fcabb-145">First Time Setup</span></span>

<span data-ttu-id="fcabb-146">처음으로 설정 프로세스가 Sysprep의 표준 이미징 규칙과 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-146">The first time setup process is now integrated with the standard imaging convention of Sysprep.</span></span> <span data-ttu-id="fcabb-147">처음에 MED-V 작업 영역 설치 프로세스는 미니 설정 시작 시 MED-V 작업 영역 포장기에 지정 된 설정을 이미지에 동적으로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-147">The MED-V workspace first time setup process can dynamically apply settings specified in the MED-V Workspace Packager to the image as it begins Mini-Setup.</span></span> <span data-ttu-id="fcabb-148">콘솔의 스크립팅 도구가 제거 되었고, 이제 관리자가 MED-V 작업 영역 포장기에서 구성한 옵션에 따라 설정 프로세스가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-148">The scripting tool in the console was removed and the first time setup process is now based on options that are configured in the MED-V Workspace Packager by the administrator.</span></span>

### <span data-ttu-id="fcabb-149">응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="fcabb-149">Application Publishing</span></span>

<span data-ttu-id="fcabb-150">관리자는 MED-V 작업 영역이 배포 된 후 또는 둘 모두의 조합을 사용 하 여 패키지 하기 전에 MED-V 이미지에 응용 프로그램을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-150">Administrators can install applications on the MED-V image either before packaging, after the MED-V workspace is deployed, or by using a combination of both.</span></span> <span data-ttu-id="fcabb-151">MED-V는 더 이상 MED-V 작업 영역 정책을 검사 하 여 응용 프로그램을 게시 하지 않고 실제로 게스트에 설치 되어 있는 항목을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-151">MED-V no longer examines MED-V workspace policy to publish applications, but instead refers to what is actually installed on the guest.</span></span> <span data-ttu-id="fcabb-152">게스트에 응용 프로그램이 설치 되 면 자동으로 검색 되어 호스트 **시작** 메뉴에 게시 되며 최종 사용자가 시작할 준비가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-152">As applications are installed on the guest, they are automatically detected and published to the host **Start** menu and are ready to be started by the end user.</span></span>

### <span data-ttu-id="fcabb-153">URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="fcabb-153">URL Redirection</span></span>

<span data-ttu-id="fcabb-154">MED-V 2.0는 관리자가 구성 하 고 관리 하는 정책에 따라 원활한 호스트 대 게스트 웹 주소 리디렉션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-154">MED-V 2.0 provides seamless host-to-guest web address redirection based on the policies configured and managed by the administrator.</span></span> <span data-ttu-id="fcabb-155">URL이 게스트 브라우저로 리디렉션되는 경우 기본 환경은 사용자를 해당 리디렉션된 사이트로 제한 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-155">After a URL is redirected to the guest browser, the default experience is to attempt to limit the user to that redirected site.</span></span> <span data-ttu-id="fcabb-156">이렇게 하면 관리자가 의도 하지 않은 사용자가 수행할 수 있는 검색 작업이 최소화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-156">This minimizes the browsing activities that a user can perform that are not intended by the administrator.</span></span> <span data-ttu-id="fcabb-157">게스트-호스트 브라우저 리디렉션이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-157">Guest-to-host browser redirection was removed.</span></span>

### <span data-ttu-id="fcabb-158">문제 해결</span><span class="sxs-lookup"><span data-stu-id="fcabb-158">Troubleshooting</span></span>

<span data-ttu-id="fcabb-159">이제 MED-V는 문제 해결을 위해 표준 호스트 기반 프로세스를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-159">MED-V now takes advantage of standard host-based processes for troubleshooting.</span></span> <span data-ttu-id="fcabb-160">MED-V 작업 영역은 더 이상 암호화 되지 않으므로 표준 워크스테이션으로 보고 작업할 수 있는 Windows 가상 PC 콘솔 내의 전체 화면 모드로 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-160">Because the MED-V workspace is no longer encrypted, it can be opened in full-screen mode within the Windows Virtual PC console, where it can be viewed and worked with as a standard workstation.</span></span> <span data-ttu-id="fcabb-161">또한 로그가 더 이상 로컬로 암호화 되지 않고 중앙에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-161">In addition, the logs are no longer encrypted locally and logged centrally.</span></span> <span data-ttu-id="fcabb-162">이제 MED-V는 로컬 이벤트 로그를 광범위 하 게 사용 하 고, 알림에서 디버그 수준 까지의 출력에 대 한 로깅 수준을 쉽게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-162">MED-V now makes extensive use of the local event logs, and the logging level of the output, from informational to debug levels, can be easily configured.</span></span> <span data-ttu-id="fcabb-163">마지막으로, 문제 해결 도구 키트가 제공 되므로 관리자와 헬프 데스크 직원은 모든 문제 해결 옵션을 그래프로 집계 하 여 볼 수 있으며, 대부분의 요구 사항에 가장 적합 한 작업을 손쉽게 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-163">Finally, a troubleshooting toolkit is now provided so administrators and helpdesk personnel can have a graphical, aggregated view of all the troubleshooting options, and they can effortlessly select the activities that most suit their needs.</span></span>

<span data-ttu-id="fcabb-164">MED-V는 시스템 서비스로 더 이상 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-164">MED-V is no longer run as a system service.</span></span> <span data-ttu-id="fcabb-165">대신 사용자가 소유한 프로세스로 실행 되며 사용자가 로그온 할 때만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-165">Instead, it is run as user-owned processes, and it only runs when a user is logged on.</span></span><span data-ttu-id="fcabb-166">이전에 시스템 소유 서비스에서 제공 했던 기능은 이제 사용자 측 프로세스에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcabb-166">Functionality that was formerly provided by the system-owned service is now provided in the user-side processes.</span></span>

## <span data-ttu-id="fcabb-167">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fcabb-167">Related topics</span></span>


[<span data-ttu-id="fcabb-168">MED-V 배포</span><span class="sxs-lookup"><span data-stu-id="fcabb-168">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="fcabb-169">MED-V 작업</span><span class="sxs-lookup"><span data-stu-id="fcabb-169">Operations for MED-V</span></span>](operations-for-med-v.md)

 

 





