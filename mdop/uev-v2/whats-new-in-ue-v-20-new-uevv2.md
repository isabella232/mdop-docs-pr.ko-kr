---
title: UE-V 2.0의 새로운 기능
description: UE-V 2.0의 새로운 기능
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824963"
---
# <span data-ttu-id="466f6-103">UE-V 2.0의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="466f6-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="466f6-104">Microsoft UE-V (User Experience Virtualization) 2.0는 UE-V 1.0에 비해 이러한 새로운 기능과 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="466f6-105">[MICROSOFT ue-v (User Experience Virtualization) 2.0 릴리스](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) 정보는 ue-v 2.0 릴리스에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="466f6-106">CSC (클라이언트측 캐시)가 더 이상 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="466f6-107">이 버전의 UE-V를 통해 Windows 오프 라인 파일 기능에 대 한 요구 사항이 대체 되어 클라이언트측 설정 캐시를 지 원하는 **동기화 공급자**가 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="466f6-108">UE-V를 사용 하 여 응용 프로그램을 열거나 닫을 때 또는 Windows가 잠그거나 잠금 해제 또는 로그온 또는 로그 오프할 때에만 설정을 동기화 하는 것은 동기화 공급자입니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="466f6-109">"**트리거 이벤트**"를 사용 하 여 로컬 응용 프로그램 및 Windows 설정을 대역외 외부에 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="466f6-110">예약 된 **작업** 을 사용 하 여 엔터프라이즈 요구 사항에 대해 선택한 간격에 따라 설정 저장소 패키지를 동기화 합니다 (기본적으로 30 분 마다).</span><span class="sxs-lookup"><span data-stu-id="466f6-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="466f6-111">특정 조건을 충족 하면 동기화가 더 빈번 하 게 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="466f6-112">사용자가 새 회사 설정 센터 응용 프로그램의 **지금 동기화** 단추를 클릭 하면 설정이 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="466f6-113">동기화 공급자는 예약 된 동기화 작업을 기다리지 않고 단일 응용 프로그램에 대해서도 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="466f6-114">예를 들어 응용 프로그램을 닫을 때 모든 설정 변경 내용이 로컬 캐시에 기록 되 고, 동기화 공급자 프로세스가 비동기적으로 실행 되어 새 설정 변경 내용을 설정 저장소 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="466f6-115">Windows 앱 동기화</span><span class="sxs-lookup"><span data-stu-id="466f6-115">Windows app synchronization</span></span>


<span data-ttu-id="466f6-116">Windows 앱 개발자는 동기화 할 설정을 정의할 수 있으며, 이러한 설정을 이제 UE-V를 사용 하 여 캡처 및 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="466f6-117">기본적으로 UE-V는 Windows 8 및 Windows 8.1에 포함 된 많은 Windows 앱의 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="466f6-118">Windows PowerShell, WMI (Windows Management Instrumentation) 또는 그룹 정책을 사용 하 여 동기화 된 앱 목록을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="466f6-119">**참고**  도메인 사용자가 로그인 자격 증명을 Microsoft 계정에 연결 하는 경우 UE-V는 Windows 앱 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="466f6-120">이 링크는 Microsoft OneDrive에 설정을 동기화 하므로 UE-V-V는 데스크톱 응용 프로그램을 동기화 할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="466f6-121">Microsoft 계정 연결</span><span class="sxs-lookup"><span data-stu-id="466f6-121">Microsoft account linking</span></span>


<span data-ttu-id="466f6-122">OneDrive를 통한 설정 동기화는 Microsoft 계정으로 로그인 하거나 Microsoft 계정을 도메인 계정에 연결 하는 경우 Windows 8에 대 한 새로운 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="466f6-123">도메인 사용자가 UE-V를 사용 하 고 있고 Microsoft 계정에 로그인 한 경우 ...</span><span class="sxs-lookup"><span data-stu-id="466f6-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="466f6-124">UE-V는 데스크톱 응용 프로그램에 대 한 설정만 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="466f6-125">Microsoft 계정에서 Windows 앱 설정 및 Windows 바탕 화면 설정 처리</span><span class="sxs-lookup"><span data-stu-id="466f6-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="466f6-126">회사 설정 센터</span><span class="sxs-lookup"><span data-stu-id="466f6-126">Company Settings Center</span></span>


<span data-ttu-id="466f6-127">사용자에 게는 UE-V 2에서 회사 설정 센터 라는 응용 프로그램을 통해 동기화 되는 설정에 대 한 몇 가지 제어 기능을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="466f6-128">회사 설정 센터는 UE-V Agent와 함께 설치 되며, 사용자는 제어판, **시작** 메뉴, **시작** 화면, ue-v 알림 영역 아이콘에서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="466f6-129">회사 설정 센터에서는 동기화 되는 설정을 표시 하 고 사용자가 UE-V의 동기화 상태를 볼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="466f6-130">사용자가 허용할 경우 회사 설정 센터를 사용 하 여 동기화 할 설정을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="466f6-131">**지금 동기화** 단추를 클릭 하 여 모든 설정을 즉시 동기화 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466f6-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="466f6-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="466f6-132">Related topics</span></span>


[<span data-ttu-id="466f6-133">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="466f6-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="466f6-134">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="466f6-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="466f6-135">Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="466f6-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





