---
title: UE-V 2.1 SP1의 새로운 기능
description: UE-V 2.1 SP1의 새로운 기능
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827428"
---
# <span data-ttu-id="91d21-103">UE-V 2.1 SP1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="91d21-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="91d21-104">사용자 환경 가상화 2.1 SP1은 UE-V 2.1에 비해 이러한 새로운 기능과 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="91d21-105">[MICROSOFT ue-v (User Experience Virtualization) 2.1 Sp1 릴리스](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) 정보는 UE-V 2.1 SP1 릴리스에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="91d21-106">Windows 10 지원</span><span class="sxs-lookup"><span data-stu-id="91d21-106">Support for Windows 10</span></span>


<span data-ttu-id="91d21-107">UE-V 2.1 SP1은 이전 버전의 UE-V에서 지원 되는 소프트웨어 외에도 Windows 10에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="91d21-108">Microsoft Azure와의 호환성</span><span class="sxs-lookup"><span data-stu-id="91d21-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="91d21-109">Windows 10에서 엔터프라이즈 사용자는 windows 앱 설정 및 Windows 운영 체제 설정을 OneDrive 대신 Azure로 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="91d21-110">Windows 10 enterprise 동기화 기능은 온-프레미스 도메인에 가입 된 컴퓨터에만 UE-V를 사용 하 여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="91d21-111">Windows 10 및 UE-V를 함께 사용할 수 있도록 설정 하려면 각 클라이언트 또는 그룹 정책의 PowerShell을 사용 하 여 다음 UE-V 템플릿을 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="91d21-112">그룹 정책의 Microsoft 사용자 환경 가상화 노드에서 다음 정책 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="91d21-113">"Windows 앱을 동기화 하지 않음" 사용</span><span class="sxs-lookup"><span data-stu-id="91d21-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="91d21-114">"Windows 설정 동기화" 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="91d21-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="91d21-115">Windows 10 지원에 대해 변경 된 설정 동기화 동작</span><span class="sxs-lookup"><span data-stu-id="91d21-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="91d21-116">UE-V 2.1 SP1은 Windows 10 장치 간의 작업 표시줄 설정을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="91d21-117">그러나 UE-V는 이전 운영 체제를 실행 하는 Windows 10 장치 및 장치 간에 작업 표시줄 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="91d21-118">또한 UE-V 2.1 SP1은 Windows 10의 Microsoft 계산기와 이전 운영 체제의 Microsoft 계산기 간 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="91d21-119">로밍 네트워크 프린터용 지원 추가</span><span class="sxs-lookup"><span data-stu-id="91d21-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="91d21-120">UE-V 2.1 SP1에서는 네트워크 프린터가 네트워크의 모든 장치에 로그온 되어 있는 경우 사용자가 네트워크 프린터에 액세스할 수 있도록 디바이스 간에 로밍이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="91d21-121">여기에는 기본값으로 설정 된 프린터를 로밍 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="91d21-122">UE-V의 Printer 로밍에는 다음 시나리오 중 하나가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="91d21-123">인쇄 서버는 새 장치로 로밍할 때 필요한 드라이버를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="91d21-124">로밍 네트워크 프린터용 드라이버는 해당 네트워크 프린터에 액세스 해야 하는 모든 장치에 사전 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="91d21-125">프린터 드라이버는 Windows 업데이트에서 구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="91d21-126">**참고**  UE-V 프린터 로밍 기능은 양면 인쇄와 같은 프린터 설정이 나 기본 **설정을 로밍하지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="91d21-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="91d21-127">Office 2013 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="91d21-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="91d21-128">UE-V 2.1 및 2.1 SP1에는 Outlook 서명 지원이 향상 된 Microsoft Office 2013 설정 위치 템플릿이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="91d21-129">새, 회신 및 전달 된 전자 메일에 대 한 기본 서명 설정을 동기화 했습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="91d21-130">고객은 더 이상 기본 서명 설정을 선택할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="91d21-131">**참고**  Outlook 프로필은 사용자가 Outlook 서명을 동기화 하려는 모든 장치에 대해 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="91d21-132">프로필이 아직 만들어지지 않은 경우 사용자가 프로필을 만든 다음 해당 장치에서 Outlook을 다시 시작 하 여 서명 동기화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="91d21-133">이전에는 UE-V 에이전트를 사용 하 여 자동으로 배포 되 고 등록 된 Microsoft Office 2010 설정 위치 템플릿이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="91d21-134">Office 365에서 UE-V 2.1를 사용 하 여 office 2013 설정이 office 365에서 roamed 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="91d21-135">설정이 Office 365에 의해 roamed 경우 UE-V를 통해 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="91d21-136">[Office 2013의 사용자 및 로밍 설정 개요](https://go.microsoft.com/fwlink/p/?LinkID=391220) 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="91d21-137">UE-V 2.1를 사용 하 여 설정 동기화를 사용 하도록 설정 하려면 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="91d21-138">그룹 정책을 사용 하 여 Office 365 동기화를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="91d21-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="91d21-139">Office 2013 설치 중에 Office 365 동기화 환경 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="91d21-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="91d21-140">UE-V 2.1은 [office 2013 및 office 2010 템플릿을](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="91d21-141">이 릴리스는 Office 2007 서식 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="91d21-142">사용자는 UE-V 2.0 또는 이전 버전의 Office 2007 서식 파일을 계속 사용할 수 있으며 [여기](https://go.microsoft.com/fwlink/p/?LinkID=246589)에 있는 ue-v 템플릿 갤러리에서 서식 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91d21-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="91d21-143">관련 항목</span><span class="sxs-lookup"><span data-stu-id="91d21-143">Related topics</span></span>


[<span data-ttu-id="91d21-144">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="91d21-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="91d21-145">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="91d21-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="91d21-146">Microsoft User Experience Virtualization(UE-V) 2.1 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="91d21-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





