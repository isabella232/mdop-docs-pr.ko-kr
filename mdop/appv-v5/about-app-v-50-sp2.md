---
title: App-V 5.0 SP2 정보
description: App-V 5.0 SP2 정보
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814988"
---
# <span data-ttu-id="37583-103">App-V 5.0 SP2 정보</span><span class="sxs-lookup"><span data-stu-id="37583-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="37583-104">App-v 5.0 SP2는 향상 된 통합 플랫폼, 유연한 가상화, 가상화 응용 프로그램에 대 한 강력한 관리 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="37583-105">자세한 내용은 [앱-V 5.0 개요](https://go.microsoft.com/fwlink/p/?LinkId=325265) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="37583-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="37583-106">표준 App-v 5.0 SP2 기능 변경 사항</span><span class="sxs-lookup"><span data-stu-id="37583-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="37583-107">다음 섹션에는 App-v 5.0 SP2의 표준 기능 변경 사항에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="37583-108">Windows Server 2012 R2 및 Windows 8.1에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="37583-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="37583-109">앱-V 5.0에는 Windows Server 2012 R2 및 Windows 8.1에 대 한 지원이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="37583-110">이제 app-v 5.0 SP2는 사용자 로밍 AppData 디렉터리에 대 한 폴더 리디렉션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="37583-111">App-v 5.0 SP2는 로밍 AppData (% AppData%)를 지원 합니다. 폴더 리디렉션.</span><span class="sxs-lookup"><span data-stu-id="37583-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="37583-112">자세한 내용은 [app-v에서 폴더 리디렉션 사용 계획](planning-to-use-folder-redirection-with-app-v.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37583-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="37583-113">패키지 업그레이드 개선 사항 및 보류 중인 작업</span><span class="sxs-lookup"><span data-stu-id="37583-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="37583-114">앱-V 5.0 SP2에서는 더 이상 최신 버전의 패키지 또는 연결 그룹을 게시할 때 실행 중인 가상 응용 프로그램을 닫을지 묻는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="37583-115">관련 작업을 수행 하려고 할 때 패키지 또는 연결 그룹이 사용 중인 경우 개체가 사용 중임을 나타내고 작업을 나중에 시도 한다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="37583-116">보류 상태에 배치 된 작업은 다음 규칙에 따라 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37583-117">작업 종류</span><span class="sxs-lookup"><span data-stu-id="37583-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="37583-118">해당 규칙</span><span class="sxs-lookup"><span data-stu-id="37583-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37583-119">사용자 기반 작업 (예: 패키지를 사용자에 게 게시)</span><span class="sxs-lookup"><span data-stu-id="37583-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="37583-120">보류 중인 작업은 사용자가 로그 오프 한 다음 다시 로그온 하면 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37583-121">전역 기반 작업 (예: 연결 그룹을 전역적으로 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="37583-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="37583-122">보류 중인 작업은 컴퓨터를 종료 한 후 다시 시작 하면 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="37583-123">작업이 보류 상태에 배치 되 면 App-v 클라이언트는 다음과 같이 보류 중인 작업에 대 한 레지스트리 키도 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37583-124">사용자 기반 또는 전역 기반 작업</span><span class="sxs-lookup"><span data-stu-id="37583-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="37583-125">레지스트리 키가 생성 되는 위치</span><span class="sxs-lookup"><span data-stu-id="37583-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37583-126">사용자 기반 작업</span><span class="sxs-lookup"><span data-stu-id="37583-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="37583-127">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="37583-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37583-128">전역 기반 작업</span><span class="sxs-lookup"><span data-stu-id="37583-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="37583-129">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="37583-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="37583-130">App-v 5.0을 사용 하 여 Microsoft Office 2013 및 Microsoft Office 2010 가상화</span><span class="sxs-lookup"><span data-stu-id="37583-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="37583-131">앱-V 5.0 지원 되는 Microsoft Office 시나리오에 대 한 자세한 내용은 다음 링크를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="37583-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="37583-132">Application Virtualization(App-V) 5.0을 위한 Microsoft Office 2013 가상화</span><span class="sxs-lookup"><span data-stu-id="37583-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="37583-133">**참고**  이 문서에서는 Microsoft Office 2013 App-v 5.0 패키지 만들기에 대해 중점적으로 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="37583-134">그러나 Microsoft Office 2010 for App-v 5.0에 대 한 시나리오에 대 한 정보도 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="37583-135">앱-V 5.0 클라이언트 관리 사용자 인터페이스 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="37583-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="37583-136">이전 버전의 App-v 5.0에서 클라이언트 관리 UI (사용자 인터페이스)는 App-v 5.0 클라이언트 설치와 함께 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="37583-137">App-v 5.0 SP2를 사용 하는 경우에는이 기능이 더 이상 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="37583-138">이제 관리자는 App-v 5.0 클라이언트 UI를 가상 응용 프로그램 (지원 되는 모든 앱-V 배포 구성 사용) 또는 설치 된 응용 프로그램으로 배포 하는 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="37583-139">자세한 내용은 [Microsoft Application Virtualization 5.0 클라이언트 UI 응용 프로그램](https://go.microsoft.com/fwlink/p/?LinkId=386345) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="37583-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="37583-140">나란히 (SxS) 어셈블리 자동 패키징 및 배포</span><span class="sxs-lookup"><span data-stu-id="37583-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="37583-141">이제 app-v 5.0 SP2는 자동으로 나란히 (SxS) 어셈블리를 감지 하 고 App-v 5.0 SP2 클라이언트를 실행 하는 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="37583-142">SxS 어셈블리는 주로 VC + + 런타임 종속성 또는 MSXML로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="37583-143">이전 버전의 App-v에서는 VC 런타임에 종속성이 있는 가상 응용 프로그램에서 이러한 종속성이 App-v 5.0 SP2 클라이언트를 실행 하는 컴퓨터에 로컬로 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="37583-144">이제 다음 기능이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37583-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="37583-145">앱-V 5.0 시퀀서는 VC 런타임이 시퀀서를 실행 하는 컴퓨터에 이미 설치 되었는지 여부에 관계 없이 패키지의 SxS 어셈블리를 자동으로 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="37583-146">App-v 5.0 클라이언트는 게시할 때 필요에 따라 클라이언트를 실행 하는 컴퓨터에 필요한 SxS 어셈블리를 자동으로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="37583-147">App-v 5.0 sequencer는 sequencer 보고 메커니즘을 사용 하 여 VC 런타임 종속성을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="37583-148">이제 App-v 5.0 sequencer를 사용 하 여 sequencer를 실행 하는 컴퓨터에서 종속성을 이미 사용할 수 있는 경우 VC 런타임 종속성을 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="37583-149">게시 새로 고침 개선</span><span class="sxs-lookup"><span data-stu-id="37583-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="37583-150">앱-V 5.0는 특정 사용자에 대 한 응용 프로그램 집합을 새로 고칠 때의 전반적인 환경을 개선 하기 위해 여러 기능을 추가할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="37583-151">다음 목록에는 게시 새로 고침 향상이 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="37583-152">다음 목록에는 새 게시 새로 고침 개선 기능을 사용 하도록 설정 하는 방법에 대 한 자세한 정보가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="37583-153">**EnablePublishingRefreshUI** -App-v 5.0 클라이언트를 실행 하는 컴퓨터에 대해 게시 새로 고침 진행률 표시줄을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="37583-154">**HideUI** -수동 동기화 중에 게시 새로 고침 진행률 표시줄을 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="37583-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="37583-155">새 클라이언트 구성 설정</span><span class="sxs-lookup"><span data-stu-id="37583-155">New Client Configuration Setting</span></span>

<span data-ttu-id="37583-156">다음과 같은 새 클라이언트 구성 설정은 App-v 5.0 SP2에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37583-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="37583-157">**Enabledynamicvirtualization** -지원 되는 셸 확장, 브라우저 도우미 개체 및 Active X 컨트롤을 가상 응용 프로그램을 사용 하 여 가상화 하 고 실행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="37583-158">자세한 내용은 [클라이언트 구성 설정](about-client-configuration-settings.md)정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37583-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="37583-159">앱-V 5.0 셸 확장</span><span class="sxs-lookup"><span data-stu-id="37583-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="37583-160">앱-V 5.0 SP2는 이제 셸 확장을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="37583-161">자세한 내용은 app-v **5.0 sp2 셸 확장 지원** 섹션을 참조 하세요 [-v 5.0 가상화 된 응용 프로그램 만들기 및 관리](creating-and-managing-app-v-50-virtualized-applications.md)</span><span class="sxs-lookup"><span data-stu-id="37583-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="37583-162">앱-V 5.0 문서 업데이트</span><span class="sxs-lookup"><span data-stu-id="37583-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="37583-163">App-v 5.0 SP2는 다음 시나리오에 대 한 업데이트 된 문서를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="37583-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="37583-164">이전 버전에서 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="37583-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="37583-165">App-V 5.0 정보</span><span class="sxs-lookup"><span data-stu-id="37583-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="37583-166">[앱-V 5.0 보고](about-app-v-50-reporting.md) (질문과 대답 섹션)</span><span class="sxs-lookup"><span data-stu-id="37583-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="37583-167">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="37583-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="37583-168">앱-V 5.0는 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="37583-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="37583-169">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="37583-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="37583-170">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="37583-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="37583-171">관련 항목</span><span class="sxs-lookup"><span data-stu-id="37583-171">Related topics</span></span>


[<span data-ttu-id="37583-172">App-V 5.0 SP2 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="37583-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





