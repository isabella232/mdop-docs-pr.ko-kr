---
title: Microsoft Application Virtualization 관리 시스템 릴리스 정보 4.5 SP1
description: Microsoft Application Virtualization 관리 시스템 릴리스 정보 4.5 SP1
author: dansimp
ms.assetid: 5d6b11ea-7b87-4084-9a7c-0d831f247aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c24d2e98ad09460ca22e4b29d75ae2b9c72d0bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816158"
---
# <span data-ttu-id="d054c-103">Microsoft Application Virtualization 관리 시스템 릴리스 정보 4.5 SP1</span><span class="sxs-lookup"><span data-stu-id="d054c-103">Microsoft Application Virtualization Management System Release Notes 4.5 SP1</span></span>


<span data-ttu-id="d054c-104">이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="d054c-105">**중요**  이 릴리스 정보는 응용 프로그램 가상화 관리 시스템을 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-105">**Important** Read these Release Notes thoroughly before you install the Application Virtualization Management System.</span></span> <span data-ttu-id="d054c-106">이러한 릴리스 정보에는 응용 프로그램 가상화 관리 시스템을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-106">These Release Notes contain information that you need to successfully install the Application Virtualization Management System.</span></span> <span data-ttu-id="d054c-107">본 릴리스 정보에는 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-107">These Release Notes contain information that is not available in the product documentation.</span></span> <span data-ttu-id="d054c-108">이러한 릴리스 노트와 다른 응용 프로그램 가상화 관리 시스템 설명서 사이에 차이가 있는 경우 최신 변경 내용을 신뢰할 수 있는 것으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-108">If there is a discrepancy between these Release Notes and other Application Virtualization Management System documentation, the latest change should be considered authoritative.</span></span>

 

<span data-ttu-id="d054c-109">알려진 문제점에 대 한 업데이트 된 정보를 보려면에서 Microsoft TechNet 라이브러리를 방문 하세요 <https://go.microsoft.com/fwlink/?LinkId=122918> .</span><span class="sxs-lookup"><span data-stu-id="d054c-109">For updated information about known issues, please visit the Microsoft TechNet Library at <https://go.microsoft.com/fwlink/?LinkId=122918>.</span></span>

## <span data-ttu-id="d054c-110">Microsoft Application Virtualization 4.5 서비스 팩 1 정보</span><span class="sxs-lookup"><span data-stu-id="d054c-110">About Microsoft Application Virtualization 4.5 Service Pack 1</span></span>


<span data-ttu-id="d054c-111">이 릴리스 정보는 Microsoft App-v (Application Virtualization) 4.5 서비스 Pack1 (SP1)에 도입 된 변경 내용을 반영 하도록 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-111">These Release Notes have been updated to reflect the changes introduced with Microsoft Application Virtualization (App-V)4.5 Service Pack1 (SP1).</span></span> <span data-ttu-id="d054c-112">이 서비스 팩에는 다음과 같은 변경 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-112">This service pack contains the following changes:</span></span>

-   <span data-ttu-id="d054c-113">Windows 7 및 Windows Server 2008 R2 지원: App-v 4.5 SP1은 작업 표시줄, AppLocker, BranchCache, BitLocker To Go 등의 Windows 7 기능에 대 한 지원을 포함 하 여 Windows 7 및 Windows Server 2008 R2에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-113">Support for Windows 7 and Windows Server 2008 R2: App-V 4.5 SP1 provides support for Windows 7 and Windows Server 2008 R2, including support for Windows 7 features such as the taskbar, AppLocker, BranchCache, and BitLocker To Go.</span></span><span data-ttu-id="d054c-114">Windows Server 2008 R2 지원은 Application Virtualization Server에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-114"> Windows Server 2008 R2 support is for the Application Virtualization Server only.</span></span> <span data-ttu-id="d054c-115">Windows 7의 AppLocker 지원에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkID=156732> 하세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-115">For more information on AppLocker support in Windows 7, see <https://go.microsoft.com/fwlink/?LinkID=156732>.</span></span>

-   <span data-ttu-id="d054c-116">타사 Kerberos 영역에 대 한 지원: App-v 4.5 SP1은 신뢰 관계와 Windows 도메인과 MIT Kerberos 영역 사이에 매핑된 사용자 계정이 있는 환경에 대 한 지원을 제공 하며,이는 여러 대학에서 공통적으로 사용 되는 시나리오입니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-116">Support for 3rd Party Kerberos Realms: App-V 4.5 SP1 provides support for environments that have a trust relationship and mapped user accounts between a Windows domain and an MIT Kerberos realm, which is a scenario that is common at many universities.</span></span> <span data-ttu-id="d054c-117">이 지원을 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 Microsoft TechNet 라이브러리를 방문 하세요 <https://go.microsoft.com/fwlink/?LinkId=166004> .</span><span class="sxs-lookup"><span data-stu-id="d054c-117">For information on how to enable this support, please visit the Microsoft TechNet Library at <https://go.microsoft.com/fwlink/?LinkId=166004>.</span></span>

-   <span data-ttu-id="d054c-118">HTTP/HTTPS를 통해 응용 프로그램 게시 및 스트리밍에 대 한 지원이 향상 되었습니다. App-v 4.5 SP1은 Windows XP Home Edition, Windows Vista Home Basic, Windows 7 Home Basic 용 HTTP/HTTPS 프로토콜을 통해 응용 프로그램 게시 및 스트리밍을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-118">Improved support for application publishing and streaming via HTTP/HTTPS: App-V 4.5 SP1 provides support for application publishing and streaming via the HTTP/HTTPS protocols for Windows XP Home Edition, Windows Vista Home Basic, and Windows 7 Home Basic.</span></span>

-   <span data-ttu-id="d054c-119">고객 의견 및 핫픽스 롤업: App-v 4.5 SP1에는 Microsoft Application Virtualization (App-v) 4.5 CU1 release 이후 발견 된 문제를 해결 하는 수정 사항에 대 한 롤업도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-119">Customer Feedback and Hotfix Rollup: App-V4.5 SP1 also includes a rollup up of fixes to address issues found since the Microsoft Application Virtualization (App-V)4.5 CU1 release.</span></span> <span data-ttu-id="d054c-120">이 업데이트는 알려진 문제점 및 사용자의 내부 팀, 파트너, 그리고 App-v 4.5를 사용 하는 고객의 피드백의 조합으로 인해 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-120">The updates are a result of a combination of known issues and customer feedback from our internal teams, partners, and customers who are using App-V4.5.</span></span> <span data-ttu-id="d054c-121">전체 업데이트 목록은 KB 문서를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=167121> .</span><span class="sxs-lookup"><span data-stu-id="d054c-121">For a full list of the updates, see the KB article at <https://go.microsoft.com/fwlink/?LinkId=167121>.</span></span>

## <span data-ttu-id="d054c-122">제품 설명서 정보</span><span class="sxs-lookup"><span data-stu-id="d054c-122">About the Product Documentation</span></span>


<span data-ttu-id="d054c-123">App-v (application virtualization)에 대 한 자세한 내용은 Microsoft TechNet에서 앱 (app-v) TechCenter을 참조 <https://go.microsoft.com/fwlink/?LinkId=122939> 하세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-123">Comprehensive documentation for Application Virtualization (App-V) is available on Microsoft TechNet in the Application Virtualization (App-V) TechCenter at <https://go.microsoft.com/fwlink/?LinkId=122939>.</span></span> <span data-ttu-id="d054c-124">이 TechNet 문서에는 Application Virtualization Sequencer, Application Virtualization 클라이언트, Application Virtualization Server에 대 한 온라인 도움말이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-124">The TechNet documentation includes the online Help for the Application Virtualization Sequencer, the Application Virtualization Client, and the Application Virtualization Server.</span></span> <span data-ttu-id="d054c-125">또한 응용 프로그램 가상화 계획 및 배포 가이드 및 응용 프로그램 가상화 운영 가이드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-125">It also includes the Application Virtualization Planning and Deployment Guide and the Application Virtualization Operations Guide.</span></span>

## <span data-ttu-id="d054c-126">보안 취약점 및 바이러스 방지</span><span class="sxs-lookup"><span data-stu-id="d054c-126">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="d054c-127">보안 취약점과 바이러스 로부터 보호 하려면 설치할 새 소프트웨어에 대해 사용 가능한 최신 보안 업데이트를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-127">To help protect against security vulnerabilities and viruses, we recommend that you install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="d054c-128">자세한 내용은의 Microsoft 보안 웹 사이트를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=3482> .</span><span class="sxs-lookup"><span data-stu-id="d054c-128">For more information, see the Microsoft Security Web site at <https://go.microsoft.com/fwlink/?LinkId=3482>.</span></span>

## <span data-ttu-id="d054c-129">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="d054c-129">Providing Feedback</span></span>


<span data-ttu-id="d054c-130">Microsoft Application Virtualization TechCenter ()의 커뮤니티 포럼을 통해 Microsoft Application Virtualization (App-v) 관리 시스템에 대 한 피드백을 제공 하거나, 제안을 하거나, 문제점을 보고할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=122917> .</span><span class="sxs-lookup"><span data-stu-id="d054c-130">You can provide feedback, make a suggestion, or report an issue with the Microsoft Application Virtualization (App-V) Management System via a community forum on the Microsoft Application Virtualization TechCenter (<https://go.microsoft.com/fwlink/?LinkId=122917>).</span></span>

<span data-ttu-id="d054c-131">또한 앱에 대 한 피드백을 문서에 직접 제공 하 여 App-v 문서 팀에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-131">You can also provide your feedback on the documentation directly to the App-V documentation team.</span></span> <span data-ttu-id="d054c-132">Appvdocs@microsoft.com에 게 설명서 피드백을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-132">Send your documentation feedback to appvdocs@microsoft.com.</span></span>

## <span data-ttu-id="d054c-133">Application Virtualization 4.5 SP1의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="d054c-133">Known Issues with Application Virtualization4.5 SP1</span></span>


<span data-ttu-id="d054c-134">이 섹션에서는 Microsoft Application Virtualization (App-v) 4.5 SP1의 문제에 대 한 최신 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-134">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.5 SP1.</span></span> <span data-ttu-id="d054c-135">이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-135">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="d054c-136">가능한 경우 이러한 문제는 소프트웨어의 이후 릴리스에서 해결 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-136">Whenever possible, these issues will be addressed in later releases of the software.</span></span>

### <span data-ttu-id="d054c-137">서버 관리 콘솔 설치 지침</span><span class="sxs-lookup"><span data-stu-id="d054c-137">Guidance for installing Server Management Console</span></span>

<span data-ttu-id="d054c-138">기본 응용 프로그램 가상화 게시 및 스트리밍 서버 이외의 시스템에 관리 소프트웨어를 설치 해야 하는 경우 서버 설치는 기본 App-v 관리 서버와는 별도의 서버에 관리 콘솔 및 관리 웹 서비스를 설치 하는 것을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-138">If you need to install management software onto systems other than the primary Application Virtualization publishing and streaming server, the server install supports installing the Management Console and Management Web service on separate servers from the primary App-V Management Server.</span></span> <span data-ttu-id="d054c-139">여러 서버에서 관리 구성 요소를 배포 하려면 웹 서비스가 설치 된 서버에서 Kerberos 위임을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-139">To distribute the management components across multiple servers, Kerberos delegation must be enabled on the server where the Web service is installed.</span></span> <span data-ttu-id="d054c-140">이 지원을 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 Microsoft TechNet 라이브러리를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-140">For information on how to enable this support, please visit the Microsoft TechNet Library at</span></span> <https://go.microsoft.com/fwlink/?LinkId=166682>

### <span data-ttu-id="d054c-141">setup.msi를 사용 하 여 클라이언트를 App-v 4.5 SP1로 설치 하거나 업그레이드 하기 위한 지침</span><span class="sxs-lookup"><span data-stu-id="d054c-141">Guidance for installing or upgrading clients to App-V4.5 SP1 using setup.msi</span></span>

<span data-ttu-id="d054c-142">setup.msi를 사용 하 여 app-v 클라이언트를 App-v 4.5 SP1에 설치 하거나 업그레이드 하는 경우 필수 조건이 자동으로 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-142">When installing or upgrading your App-V clients to App-V 4.5 SP1 by using setup.msi, the prerequisites are not installed automatically.</span></span>

<span data-ttu-id="d054c-143">WORKAROUNDYou는 App-v 클라이언트 toApp 4.5 SP1을 설치 하거나 업그레이드 하기 전에 필수 구성 요소를 수동으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-143">WORKAROUNDYou must manually install the prerequisites before installing or upgrading the App-V client toApp-V 4.5 SP1.</span></span> <span data-ttu-id="d054c-144">필수 구성 요소와 App-v 클라이언트를 설치 하는 방법에 대 한 자세한 절차는를 참조 <https://go.microsoft.com/fwlink/?LinkId=144106> 하세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-144">For detailed procedures for installing the prerequisites and the App-V client, see <https://go.microsoft.com/fwlink/?LinkId=144106>.</span></span>

<span data-ttu-id="d054c-145">이 작업이 완료 되 면 높은 권한으로 setup.msi를 사용 하 여 App-v 4.5 SP1 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-145">When this has been completed, install the App-V 4.5 SP1 client by using setup.msi with elevated privileges.</span></span> <span data-ttu-id="d054c-146">이 파일은 Installers\\Client 폴더의 App-v 4.5 SP1 릴리스 미디어에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-146">This file is available on the App-V 4.5 SP1 release media in the Installers\\Client folder.</span></span>

<span data-ttu-id="d054c-147">Microsoft 응용 프로그램 오류 보고를 설치 하는 경우 App-v 4.5 SP1 데스크톱 클라이언트로 설치 하거나 업그레이드 하는 경우 다음 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-147">When installing Microsoft Application Error Reporting, use the following command if you are installing or upgrading to the App-V 4.5 SP1 Desktop client:</span></span>

    msiexec /i dw20shared.msi APPGUID={93468B43-C19D-44F9-8BCC-114076DB0443}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

<span data-ttu-id="d054c-148">또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 4.5 SP1 클라이언트를 설치 하거나 업그레이드 하는 경우에는 다음 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-148">Alternatively, if you are installing or upgrading to the App-V 4.5 SP1 Client for Remote Desktop Services (formerly Terminal Services), use the following command:</span></span>

    msiexec /i dw20shared.msi APPGUID={0042AD3C-99A4-4E58-B5F0-744D5AD96E1C} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

<span data-ttu-id="d054c-149">**참고**  APPGUID 매개 변수는 설치 하거나 업그레이드 하는 App-v 클라이언트의 제품 코드를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-149">**Note** The APPGUID parameter references the product code of the App-V client that you install or upgrade.</span></span> <span data-ttu-id="d054c-150">제품 코드는 각 setup.msi에 대해 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-150">The product code is unique for each setup.msi.</span></span> <span data-ttu-id="d054c-151">Orca 데이터베이스 편집기 또는 유사한 도구를 사용 하 여 Windows Installer 파일을 검사 하 고 제품 코드를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-151">You can use the Orca database editor or a similar tool to examine Windows Installer files and determine the product code.</span></span> <span data-ttu-id="d054c-152">이 단계는 App-v 4.5 SP1의 모든 설치 또는 업그레이드에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-152">This step is required for all installations or upgrades to App-V 4.5 SP1.</span></span>

 

### <span data-ttu-id="d054c-153">.NET Framework 시퀀싱 시 성능 개선</span><span class="sxs-lookup"><span data-stu-id="d054c-153">Improving performance when sequencing the .NET Framework</span></span>

<span data-ttu-id="d054c-154">.NET Framework를 시퀀싱 하는 경우 Microsoft .NET Framework NGEN 서비스에서 어셈블리를 백그라운드 작업으로 미리 컴파일하 려는 데 있어서 시스템 성능이 저하 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-154">When sequencing the .NET Framework, you might experience reduced system performance because the Microsoft .NET Framework NGEN service attempts to precompile assemblies as a background task.</span></span>

<span data-ttu-id="d054c-155">.NET Framework WORKAROUNDWhen 시퀀싱 하는 경우 모니터링 단계를 완료 한 후 Microsoft .NET Framework NGEN 서비스 (mscorsvw.exe)를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-155">WORKAROUNDWhen sequencing the .NET Framework, disable the Microsoft .NET Framework NGEN service (mscorsvw.exe) after completing the monitoring phase.</span></span> <span data-ttu-id="d054c-156">Sequencer에서 **가상 서비스** 탭을 사용 하 여 시작 유형을 disabled로 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-156">You must use the **Virtual Services** tab in the Sequencer and change the startup type to disabled.</span></span>

### <span data-ttu-id="d054c-157">Microsoft Application Virtualization 클라이언트를 제거 하면 제거를 수행 하는 사용자와 연결 된 사용자 설정이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-157">When you uninstall the Microsoft Application Virtualization Client, user settings associated with the user performing the uninstall will be deleted</span></span>

<span data-ttu-id="d054c-158">App-v 클라이언트를 제거 하면 Windows Installer는 현재 사용자의 프로필에서 응용 프로그램 가상화 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-158">When you uninstall the App-V Client, the Windows Installer will remove Application Virtualization settings from the current user's profile.</span></span> <span data-ttu-id="d054c-159">컴퓨터에서 로밍 프로필을 사용 하는 경우에는 개인 네트워크 계정을 사용 하 여 모든 컴퓨터에서 가상 응용 프로그램에 대 한 설정을 제거 하므로 클라이언트를 제거 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-159">If your computer uses roaming profiles, do not use your personal network account to uninstall the client because it will remove settings for your virtual applications on all of your computers.</span></span>

<span data-ttu-id="d054c-160">WORKAROUNDYou는 가상 응용 프로그램을 실행 하는 데 사용 되지 않는 관리자 계정을 사용 하 여 App-v 클라이언트 제거를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-160">WORKAROUNDYou should perform the App-V Client uninstall with an administrative account that is not used for running virtual applications.</span></span>

### <span data-ttu-id="d054c-161">시퀀싱 마법사를 실행 하는 동안 가상 파일 시스템 및 가상 레지스트리 탭에 대 한 편집을 저장 해야 함</span><span class="sxs-lookup"><span data-stu-id="d054c-161">Edits made on the virtual file system and virtual registry tabs must be saved while running the Sequencing wizard</span></span>

<span data-ttu-id="d054c-162">업그레이드를 수행 하기 위해 패키지를 열거나 새 패키지로 시퀀싱 마법사를 이미 실행 하 여 가상 파일 시스템 또는 가상 레지스트리 탭에서 패키지를 변경 하는 경우 해당 변경 내용이 자동으로 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-162">If you open a package to perform an upgrade, or if you have already run the Sequencing wizard with a new package and make changes to the package in the virtual file system or virtual registry tabs, those changes are not automatically saved.</span></span>

<span data-ttu-id="d054c-163">마법사를 다시 실행 하기 전에 변경 내용을 WORKAROUNDSave 하 여 마법사의 가상 환경 내에 반영 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-163">WORKAROUNDSave the changes before re-running the wizard, to ensure that they are reflected inside the wizard’s virtual environment.</span></span>

### <span data-ttu-id="d054c-164">명령줄 시퀀서는 관리자 권한 명령 프롬프트에서 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-164">Command-line Sequencer must be run from an elevated command prompt</span></span>

<span data-ttu-id="d054c-165">명령줄 시퀀서를 사용 하는 경우 권한 상승을 묻지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-165">When you use the command-line Sequencer, it does not prompt for elevation.</span></span>

<span data-ttu-id="d054c-166">관리자 권한 명령 프롬프트를 사용 하 여 명령줄 시퀀서를 WORKAROUNDRun.</span><span class="sxs-lookup"><span data-stu-id="d054c-166">WORKAROUNDRun the command-line Sequencer using an elevated command prompt.</span></span>

### <span data-ttu-id="d054c-167">OSD 파일의 짧은 경로 변수 이름으로 인해 오류가 발생할 수 있음</span><span class="sxs-lookup"><span data-stu-id="d054c-167">Short path variable names in OSD files can cause errors</span></span>

<span data-ttu-id="d054c-168">450478-1F702339-0000010B "디렉터리 이름이 올바르지 않습니다." 라는 오류 메시지가 표시 되는 경우 클라이언트에서 가상 응용 프로그램을 시작할 때 OSD의 변수가 올바르게 설정 되지 않았을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-168">If you receive error 450478-1F702339-0000010B “The directory name is invalid” when starting a virtual application on the client, it is possible that the variable in the OSD is set incorrectly.</span></span> <span data-ttu-id="d054c-169">이 문제는 응용 프로그램의 설치 관리자가 시퀀싱 중에 짧은 경로 이름을 설정 하는 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-169">This can happen if the application’s installer sets a short path name during sequencing.</span></span>

<span data-ttu-id="d054c-170">OSD 파일에 있는 모든 CSIDL 변수에서 뒤쪽 물결표를 WORKAROUNDRemove.</span><span class="sxs-lookup"><span data-stu-id="d054c-170">WORKAROUNDRemove the trailing tilde from any CSIDL variable that exists in the OSD file.</span></span>

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a><span data-ttu-id="d054c-171">명령줄 시퀀서에 대 한 DECODEPATH 매개 변수에 대 한 올바른 구문</span><span class="sxs-lookup"><span data-stu-id="d054c-171">Correct syntax for DECODEPATH parameter for command-line Sequencer</span></span>

<span data-ttu-id="d054c-172">명령줄 시퀀서에서 업그레이드를 위해 패키지를 열고 Q 드라이브의 루트로 디코딩하는 경우 *DECODEPATH* 매개 변수에 대 한 구문에 후행 슬래시가 포함 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-172">In the command-line Sequencer, when opening a package for upgrade and decoding it to the root of the Q drive, the syntax for the *DECODEPATH* parameter should not include a trailing slash.</span></span>

<span data-ttu-id="d054c-173">WORKAROUNDYou는 **Q:\\** 대신 **Q:** 를 사용할 수 있습니다 (후행 "\\" 문자 생략).</span><span class="sxs-lookup"><span data-stu-id="d054c-173">WORKAROUNDYou can use **Q:** rather than **Q:\\** (omitting the trailing “\\” character).</span></span>

### <a href="" id="when-upgrading-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a><span data-ttu-id="d054c-174">4.2 패키지를 업그레이드 하는 경우 가상 파일 시스템의 Windows Installer 파일로 인해 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-174">When upgrading4.2 packages, you encounter problems caused by Windows Installer files in the Virtual File System</span></span>

<span data-ttu-id="d054c-175">4.2에서 패키지를 업그레이드할 때 4.2에 기본적으로 포함 되어 있는 Windows Installer 시스템 파일과 시퀀싱 워크스테이션에 로컬로 설치 된 Windows Installer 라이브러리와 관련 된 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-175">When upgrading a package from4.2, you might experience issues relating to a mismatch of Windows Installer system files that were included by default in4.2 and the Windows Installer libraries locally installed on your Sequencing workstation.</span></span> <span data-ttu-id="d054c-176">CSIDL \ _SYSTEM \\:에는 다음 파일이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-176">The following files are located in CSIDL\_SYSTEM\\:</span></span>

<span data-ttu-id="d054c-177">cabinet.dll</span><span class="sxs-lookup"><span data-stu-id="d054c-177">cabinet.dll</span></span>

<span data-ttu-id="d054c-178">msi.dll</span><span class="sxs-lookup"><span data-stu-id="d054c-178">msi.dll</span></span>

<span data-ttu-id="d054c-179">msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="d054c-179">msiexec.exe</span></span>

<span data-ttu-id="d054c-180">msihnd.dll</span><span class="sxs-lookup"><span data-stu-id="d054c-180">msihnd.dll</span></span>

<span data-ttu-id="d054c-181">msimsg.dlll</span><span class="sxs-lookup"><span data-stu-id="d054c-181">msimsg.dlll</span></span>

<span data-ttu-id="d054c-182">패키지에서 위의 모든 파일을 WORKAROUNDDelete.</span><span class="sxs-lookup"><span data-stu-id="d054c-182">WORKAROUNDDelete all of the preceding files from the package.</span></span> <span data-ttu-id="d054c-183">**VFS** 탭의 매핑과 디코드 경로의 CSIDL \ _SYSTEM 폴더에 있는 실제 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-183">Delete the mappings on the **VFS** tab as well as the actual files in the CSIDL\_SYSTEM folder in your decode path.</span></span>

### <a href="" id="on-windows-xp--client-install-logging-is-not-enabled-by-default-"></a><span data-ttu-id="d054c-184">WindowsXP에서는 클라이언트 설치 로깅이 기본적으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-184">On WindowsXP, client install logging is not enabled by default</span></span>

<span data-ttu-id="d054c-185">클라이언트를 설치할 때 문제 해결을 위해 설치 오류가 캡처 되었는지 확인 하려면 명령줄을 사용 하 여 로깅을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-185">When installing the client, to ensure that any install errors are captured for troubleshooting purposes, you should enable logging by using the command line.</span></span>

<span data-ttu-id="d054c-186">다음 예제와 같이 명령줄에 */l\ \* vx! log.txt* 매개 변수를 WORKAROUNDAdd 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-186">WORKAROUNDAdd the parameter */l\*vx! log.txt* to the command line, as shown in the following example:</span></span>

<span data-ttu-id="d054c-187">setup.exe/s/v "/qn/l\ \* vx!</span><span class="sxs-lookup"><span data-stu-id="d054c-187">setup.exe /s /v”/qn /l\*vx!</span></span> <span data-ttu-id="d054c-188">log.txt "</span><span class="sxs-lookup"><span data-stu-id="d054c-188">log.txt”</span></span>

<span data-ttu-id="d054c-189">msiexec.exe/i setup.msi/qn/l\ \* vx!</span><span class="sxs-lookup"><span data-stu-id="d054c-189">msiexec.exe /i setup.msi /qn /l\*vx!</span></span> <span data-ttu-id="d054c-190">log.txt</span><span class="sxs-lookup"><span data-stu-id="d054c-190">log.txt</span></span>

<span data-ttu-id="d054c-191">또는 레지스트리 키를 다음 값으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-191">Alternatively, you can set the registry key to the following value:</span></span>

<span data-ttu-id="d054c-192">\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"</span><span class="sxs-lookup"><span data-stu-id="d054c-192">\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging"="voicewarmupx!"</span></span>

### <span data-ttu-id="d054c-193">Kerberos 인증을 사용 하려면 IIS에 대해 Spn (서비스 사용자 이름)을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-193">For Kerberos authentication to work, Service Principal Names (SPNs) must be registered for IIS</span></span>

<span data-ttu-id="d054c-194">패키지의 아이콘 또는 OSD 파일 검색 및 스트리밍을 위해 IIS 6.0 또는 7.0을 사용 하는 경우, Kerberos 인증을 사용 하도록 설정 하려면 Spn을 다음과 같이 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-194">When using IIS6.0 or7.0 for icon or OSD file retrieval and streaming of packages, for Kerberos authentication to be enabled, the SPNs must be registered as follows:</span></span>

-   <span data-ttu-id="d054c-195">IIS 서버에서 SETSPN.EXE 리소스 키트 도구를 사용 하 여 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-195">On the IIS server, run the following commands by using the SETSPN.EXE Resource Kit tool.</span></span> <span data-ttu-id="d054c-196">서버 FQDN (정규화 된 도메인 이름)을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-196">The server fully qualified domain name (FQDN) must be used.</span></span>

    <span data-ttu-id="d054c-197">Setspn-r SOFTGRID/ &lt; 서버 FQDN&gt;</span><span class="sxs-lookup"><span data-stu-id="d054c-197">Setspn -r SOFTGRID/&lt;Server FQDN&gt;</span></span>

    <span data-ttu-id="d054c-198">Setspn-r HTTP/ &lt; 서버 FQDN&gt;</span><span class="sxs-lookup"><span data-stu-id="d054c-198">Setspn -r HTTP/&lt;Server FQDN&gt;</span></span>

<span data-ttu-id="d054c-199">자세한 내용은 <https://go.microsoft.com/fwlink/?LinkId=131407>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d054c-199">For more information, see <https://go.microsoft.com/fwlink/?LinkId=131407>.</span></span>

### <span data-ttu-id="d054c-200">.NET 호환성 변경</span><span class="sxs-lookup"><span data-stu-id="d054c-200">.NET compatibility changes</span></span>

<span data-ttu-id="d054c-201">Microsoft App-v (Application Virtualization) 누적 Update1 이상에서는 WindowsXP (SP2 이상)에서 .NET Framework 시퀀싱을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-201">Microsoft Application Virtualization (App-V) Cumulative Update1 or later supports sequencing the .NET Framework on WindowsXP (SP2 or later).</span></span> <span data-ttu-id="d054c-202">SoftGrid 4.2로 작성 된 .NET 응용 프로그램의 시퀀싱 루틴은 App-v 4.5 Sequencer와 함께 사용할 때 업데이트 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-202">Sequencing routines for .NET applications that were written for SoftGrid4.2 might need to be updated when used with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="d054c-203">자세한 내용 및 해결 방법은 기술 자료 문서를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=123412> .</span><span class="sxs-lookup"><span data-stu-id="d054c-203">For details and workarounds, please refer to the Knowledge Base article at <https://go.microsoft.com/fwlink/?LinkId=123412>.</span></span>

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a><span data-ttu-id="d054c-204">App-v 4.2에서 클라이언트 업그레이드 후 일부 응용 프로그램이 표시 되지 않는 경우</span><span class="sxs-lookup"><span data-stu-id="d054c-204">After client upgrade from App-V4.2, some applications are not shown</span></span>

<span data-ttu-id="d054c-205">"Application Virtualization 클라이언트가 OSD 파일을 구문 분석 하지 못했습니다." 로그에 다음 오류가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-205">Check for the following error in the log: ”The Application Virtualization Client could not parse the OSD file”.</span></span> <span data-ttu-id="d054c-206">App-v 4.5 클라이언트는 빈 OS 태그 ( &lt; os &gt; &lt; /os)가 포함 된 OSD 파일이 있는 응용 프로그램을 필터링 합니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="d054c-206">The App-V 4.5 client filters out applications that have an OSD file containing an empty OS tag (&lt;OS&gt;&lt;/OS&gt;).</span></span>

<span data-ttu-id="d054c-207">OSD 파일에서 빈 OS 태그를 WORKAROUNDDelete.</span><span class="sxs-lookup"><span data-stu-id="d054c-207">WORKAROUNDDelete the empty OS tag from the OSD file.</span></span>

### <span data-ttu-id="d054c-208">앱-V 서버는 특정 프로세스에 대해 방화벽에서 예외를 요구 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-208">The App-V server requires exemptions in its firewall for certain processes</span></span>

<span data-ttu-id="d054c-209">서버가 응용 프로그램을 올바르게 스트림 하려면 발송자를 포함 하 여 서버의 핵심 프로세스가 방화벽을 통해 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-209">For the server to stream applications correctly, the server's core processes, including the dispatcher, need access through the firewall.</span></span>

<span data-ttu-id="d054c-210">sghwsvr.exe 및 sghwdsptr.exe 프로세스에 대 한 서버의 방화벽에서 예외를 WORKAROUNDSet 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-210">WORKAROUNDSet exemptions in the server's firewall for the following processes: sghwsvr.exe and sghwdsptr.exe.</span></span> <span data-ttu-id="d054c-211">이는 App-v 관리 서버 및 App-v 스트리밍 서버에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-211">This applies to the App-V Management Server and App-V Streaming Server.</span></span>

### <span data-ttu-id="d054c-212">서버 설치 관리자가 자동 모드로 실행 되는 경우 MSXML6를 올바르게 검사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-212">When the server installer is run in silent mode, it does not correctly check for MSXML6</span></span>

<span data-ttu-id="d054c-213">App-v 관리 서버는 MSXML6에 종속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-213">The App-V Management Server depends on MSXML6.</span></span> <span data-ttu-id="d054c-214">그러나 MSXML6가 아직 설치 되지 않은 시스템에서 "msiexec-i setup.msi/qn" 명령을 사용 하 여 설치 관리자를 자동 모드로 실행 하는 경우에는 설치 관리자가 누락 된 종속성을 감지 하지 않고 그대로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-214">However, if you run the installer in silent mode—for example, by using the command “msiexec -i setup.msi /qn” on a system where MSXML6 is not already installed—the installer does not detect the missing dependency and installs anyway.</span></span> <span data-ttu-id="d054c-215">따라서 클라이언트는 App-v 관리 서버에서 게시 정보를 새로 고치려고 할 때 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-215">Therefore, when clients attempt to refresh publishing information from the App-V Management Server, they will see failures.</span></span>

<span data-ttu-id="d054c-216">App-v 관리 서버의 자동 설치를 시도 하기 전에 MSXML6가 시스템에 설치 WORKAROUNDVerify.</span><span class="sxs-lookup"><span data-stu-id="d054c-216">WORKAROUNDVerify that MSXML6 is installed on the system before attempting a silent install of the App-V Management Server.</span></span>

### <span data-ttu-id="d054c-217">Application Virtualization Management Console에 연결 하려고 할 때 발생 하는 오류 코드 000C800</span><span class="sxs-lookup"><span data-stu-id="d054c-217">Error code 000C800 when attempting to connect to the Application Virtualization Management Console</span></span>

<span data-ttu-id="d054c-218">앱-v 관리 콘솔에 연결 하려고 할 때 App-v 관리 웹 서비스 서버에서 로컬 관리자가 아닌 응용 프로그램 가상화 관리자가 오류 (오류 코드: 000C800)를 수신 하 고 sftmmc .log 항목에는 Sftmmc에 대 한 액세스가 거부 됨이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-218">An Application Virtualization administrator who is not a local administrator on the App-V Management Web Service server will receive an error (Error code: 000C800) when attempting to connect to the App-V Management Console, and the sftmmc.log entry will indicate that access to SftMgmt.udl is denied.</span></span> <span data-ttu-id="d054c-219">App-v 관리 콘솔에 성공적으로 연결 하려면 App-v 관리 웹 서비스 서버에 대 한 로컬 관리자 권한이 없는 관리자가 SftMgmt 파일에 대해 최소한 읽기 및 실행 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-219">To successfully connect to the App-V Management Console, an administrator who does not have local administrator rights on the App-V Management Web Service server must have at least read and execute permissions to the SftMgmt.udl file.</span></span>

<span data-ttu-id="d054c-220">Application Virtualization 관리자 는%systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt 관리 서비스 아래의 SftMgmt 파일에 대 한 읽기 및 실행 권한을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-220">The Application Virtualization administrators must be given read and execute permissions to the SftMgmt.UDL file under %systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service.</span></span>

### <span data-ttu-id="d054c-221">클라이언트 설치 관리자 명령줄 매개 변수는 KEEPCURRENTSETTINGS = 1과 함께 사용할 경우 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-221">Client installer command-line parameters are ignored when used in conjunction with KEEPCURRENTSETTINGS=1</span></span>

<span data-ttu-id="d054c-222">KEEPCURRENTSETTINGS = 1과 함께 사용 하는 경우, 다음 클라이언트 설치 관리자 명령줄 매개 변수는 SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTARGET, SWIUSERDATA 및 REQUIRESECURECONNECTION입니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-222">When used in conjunction with KEEPCURRENTSETTINGS=1, the following client installer command-line parameters are ignored: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA, and REQUIRESECURECONNECTION.</span></span>

<span data-ttu-id="d054c-223">보존 하려는 설정이 있는 WORKAROUNDIf에는 KEEPCURRENTSETTINGS = 1을 사용 하 고 배포 후 다른 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-223">WORKAROUNDIf you have settings you want to retain, use KEEPCURRENTSETTINGS=1 and then set the other parameters after deployment.</span></span> <span data-ttu-id="d054c-224">App-v ADM 템플릿을 사용 하 여 APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTARGET, DOTIMEOUTMINUTES, ALLOWINDEPENDENTFILESTREAMING 등의 클라이언트 설정을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-224">The App-V ADM Template can be used to set the following client settings: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES, and ALLOWINDEPENDENTFILESTREAMING.</span></span> <span data-ttu-id="d054c-225">ADM 템플릿은에서 찾을 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="d054c-225">The ADM Template can be found at <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

## <span data-ttu-id="d054c-226">릴리스 노트 저작권 정보</span><span class="sxs-lookup"><span data-stu-id="d054c-226">Release Notes Copyright Information</span></span>


<span data-ttu-id="d054c-227">URL 및 기타 인터넷 웹 사이트 참조를 포함 하 여,이 문서의 정보는 예 고 없이 변경 될 수 있으며, 정보 제공 목적 으로만 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-227">Information in this document, including URL and other Internet Web site references, is subject to change without notice and is provided for informational purposes only.</span></span> <span data-ttu-id="d054c-228">이 문서를 사용 하는 데 따른 모든 위험 또는 결과는 사용자에 게 남아 있으며 Microsoft Corporation은 명시적 이거나 묵시적인 어떠한 보증도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-228">The entire risk of the use or results from the use of this document remains with the user, and Microsoft Corporation makes no warranties, either express or implied.</span></span> <span data-ttu-id="d054c-229">다른 언급이 없는 한, 예제에 나와 있는 회사, 조직, 제품, 도메인 이름, 전자 메일 주소, 로고, 사람, 장소 및 이벤트는 실제 데이터가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-229">Unless otherwise noted, the companies, organizations, products, domain names, e-mail addresses, logos, people, places, and events depicted in examples herein are fictitious.</span></span> <span data-ttu-id="d054c-230">어떠한 실제 회사, 기관, 제품, 도메인 이름, 전자 메일 주소, 로고, 사람, 위치 또는 이벤트와도 연관 시킬 의도가 없으며 그렇게 유추 해서도 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-230">No association with any real company, organization, product, domain name, e-mail address, logo, person, place, or event is intended or should be inferred.</span></span> <span data-ttu-id="d054c-231">해당 저작권법을 준수하는 것은 사용자의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-231">Complying with all applicable copyright laws is the responsibility of the user.</span></span> <span data-ttu-id="d054c-232">저작권에서의 권리와는 별도로, 이 설명서의 어떠한 부분도 Microsoft의 명시적인 서면 승인 없이는 어떠한 형식이나 수단(전자적, 기계적, 복사기에 의한 복사, 디스크 복사 또는 다른 방법) 또는 목적으로도 복제되거나, 검색 시스템에 저장 또는 도입되거나, 전송될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-232">Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.</span></span>

<span data-ttu-id="d054c-233">Microsoft는 이 설명서 본안에 관련된 특허권, 상표권, 저작권, 또는 기타 지적 재산권 등을 보유할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-233">Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document.</span></span> <span data-ttu-id="d054c-234">서면 사용권 계약에 따라 Microsoft로부터 귀하에게 명시적으로 제공된 권리 이외에, 이 설명서의 제공은 귀하에게 이러한 특허권, 상표권, 저작권, 또는 기타 지적 재산권 등에 대한 어떠한 사용권도 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-234">Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.</span></span>



<span data-ttu-id="d054c-235">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer 및 Windows Vista는 Microsoft 회사 그룹의 상표입니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-235">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="d054c-236">다른 모든 상표는 해당 소유자의 재산입니다.</span><span class="sxs-lookup"><span data-stu-id="d054c-236">All other trademarks are property of their respective owners.</span></span>

 

 





