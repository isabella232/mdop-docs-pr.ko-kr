---
title: UE-V용 환경 준비
description: UE-V용 환경 준비
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824648"
---
# <span data-ttu-id="981a7-103">UE-V용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="981a7-103">Preparing Your Environment for UE-V</span></span>


<span data-ttu-id="981a7-104">Microsoft UE-V (User Experience Virtualization)는 설정 저장소 위치를 사용 하 여 컴퓨터 간에 설정을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-104">Microsoft User Experience Virtualization (UE-V) roams settings between computers by the use of a settings storage location.</span></span> <span data-ttu-id="981a7-105">설정 저장소 위치는 파일 공유 이므로 UE-V 에이전트 배포 중에 구성 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-105">The settings storage location is a file share and should be configured during the UE-V Agent deployment.</span></span> <span data-ttu-id="981a7-106">설정 저장소 위치 또는 Active Directory 홈 디렉터리로 정의 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-106">It must be defined either as a settings storage location or as an Active Directory home directory.</span></span> <span data-ttu-id="981a7-107">또한 관리자는 일관성 있는 동기화를 지원 하도록 시간 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-107">In addition, the administrator should configure a time server to support consistent synchronization.</span></span> <span data-ttu-id="981a7-108">UE-V를 사용할 수 있도록 환경을 준비 하려면 다음 사항을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-108">To prepare your environment for UE-V, you should consider the following:</span></span>

-   <span data-ttu-id="981a7-109">[Ue-v 설정 저장소](#bkmk-uevsettingsstorage):</span><span class="sxs-lookup"><span data-stu-id="981a7-109">[UE-V Settings Storage](#bkmk-uevsettingsstorage):</span></span>

    -   [<span data-ttu-id="981a7-110">설정 저장소 위치 정의</span><span class="sxs-lookup"><span data-stu-id="981a7-110">Defining a Settings Storage Location</span></span>](#bkmk-definingsettingsstoragelocation)

    -   [<span data-ttu-id="981a7-111">UE-V를 사용 하 여 Active Directory Home 디렉터리 사용</span><span class="sxs-lookup"><span data-stu-id="981a7-111">Using Active Directory Home Directory with UE-V</span></span>](#bkmk-usingactivedirectoryhomedirectory)

-   [<span data-ttu-id="981a7-112">UE-V 설정 동기화에 대 한 컴퓨터 시계 동기화</span><span class="sxs-lookup"><span data-stu-id="981a7-112">Synchronize Computer Clocks for UE-V Settings Synchronization</span></span>](#bkmk-synchronizecomputerclocks)

-   [<span data-ttu-id="981a7-113">성능 및 용량 계획</span><span class="sxs-lookup"><span data-stu-id="981a7-113">Performance and Capacity Planning</span></span>](#bkmk-performancecapacityplanning)

<span data-ttu-id="981a7-114">운영 체제 및 컴퓨터 요구 사항에 대 한 자세한 내용은 [ue-v 1.0에서 지원 되는 구성을](supported-configurations-for-ue-v-10.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="981a7-114">For more information about operating system and computer requirements, see [Supported Configurations for UE-V 1.0](supported-configurations-for-ue-v-10.md).</span></span>

## <a href="" id="bkmk-uevsettingsstorage"></a><span data-ttu-id="981a7-115">UE-V 설정 저장소</span><span class="sxs-lookup"><span data-stu-id="981a7-115">UE-V settings storage</span></span>


<span data-ttu-id="981a7-116">설정 저장소 위치 또는 Active Directory 홈 디렉터리인 두 가지 구성 중 하나를 사용 하 여 사용자 환경 가상화 설정 저장소를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-116">You can define the User Experience Virtualization settings storage in one of two configurations: a settings storage location or an Active Directory home directory.</span></span>

### <a href="" id="bkmk-definingsettingsstoragelocation"></a><span data-ttu-id="981a7-117">설정 저장소 위치 정의</span><span class="sxs-lookup"><span data-stu-id="981a7-117">Define a settings storage location</span></span>

<span data-ttu-id="981a7-118">UE-V 설정 저장소 위치는 UE-V 사용자가 액세스할 수 있는 표준 네트워크 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-118">The UE-V settings storage location is a standard network share that is accessible by UE-V users.</span></span> <span data-ttu-id="981a7-119">설정 저장소 위치를 정의 하기 전에 루트 디렉터리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-119">Before you define the settings storage location, you must create a root directory.</span></span> <span data-ttu-id="981a7-120">공유에 설정을 저장할 사용자에 게는 저장소 위치에 대 한 읽기/쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-120">Users who will store settings on the share must have read/write permissions to the storage location.</span></span> <span data-ttu-id="981a7-121">UE-V Agent가이 루트 디렉터리 아래에 사용자 관련 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-121">The UE-V Agent will create user-specific folders under this root directory.</span></span> <span data-ttu-id="981a7-122">설정 저장소 위치는 **Settingsstoragepath** 구성 옵션을 설정 하 여 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-122">The settings storage location is defined by setting the **SettingsStoragePath** configuration option.</span></span> <span data-ttu-id="981a7-123">이 옵션은 다음과 같은 방법으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-123">This option can be configured in the following ways:</span></span>

-   <span data-ttu-id="981a7-124">명령줄 매개 변수 또는 일괄 처리 스크립트를 통해 UE-V 에이전트를 설치 하는 동안</span><span class="sxs-lookup"><span data-stu-id="981a7-124">During the installation of the UE-V agent through a command-line parameter or in a batch script.</span></span>

-   <span data-ttu-id="981a7-125">그룹 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-125">Using Group Policy.</span></span>

-   <span data-ttu-id="981a7-126">설치 후 PowerShell 또는 WMI를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-126">After installation, by using PowerShell or WMI.</span></span>

<span data-ttu-id="981a7-127">경로는 서버 및 공유의 UNC (범용 명명 규칙) 경로에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-127">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="981a7-128">예를 **\\\\server\\settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="981a7-128">For example, **\\\\server\\settingsshare\\**.</span></span> <span data-ttu-id="981a7-129">이 구성 옵션은 특정 로밍 시나리오를 사용 하도록 설정 하는 변수 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-129">This configuration option supports the use of variables to enable specific roaming scenarios.</span></span>

<span data-ttu-id="981a7-130">서버의 UNC 경로와 공유 하는 변수를 사용할 수 있습니다 `%username%` .</span><span class="sxs-lookup"><span data-stu-id="981a7-130">You can use the `%username%` variable with the UNC path of the server and share.</span></span> <span data-ttu-id="981a7-131">이렇게 하면 사용자가 로그인 하는 모든 컴퓨터 또는 세션에 동일한 설정 환경이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-131">This will provide the same settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="981a7-132">다음과 같은 시나리오를 위해이 구성을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-132">Consider this configuration for the following scenarios:</span></span>

1.  <span data-ttu-id="981a7-133">기업의 사용자는 유사 하 게 구성 된 여러 물리적 컴퓨터를 가질 수 있으며 각 사용자의 설정은 모든 컴퓨터에서 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-133">Users in the enterprise have multiple, similarly configured physical computers and each user’s settings should be the same across all computers.</span></span>

2.  <span data-ttu-id="981a7-134">엔터프라이즈의 사용자는 각 사용자의 VDI 세션에서 설정이 유지 되어야 하는 VDI (가상 데스크톱 인프라) 풀을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-134">Users in the enterprise use virtual desktop infrastructure (VDI) pools where settings should be retained across each user’s VDI sessions.</span></span>

3.  <span data-ttu-id="981a7-135">기업의 사용자는 하나의 물리적 컴퓨터를 보유 하 고 있으며 추가적으로 VDI를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-135">Users in the enterprise have one physical computer and additionally use a VDI.</span></span> <span data-ttu-id="981a7-136">각 사용자의 설정 환경은 물리적 컴퓨터 또는 VDI 세션을 사용 하 든 관계 없이 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-136">Each user’s settings experience should be the same whether using the physical computer or VDI session.</span></span>

4.  <span data-ttu-id="981a7-137">여러 엔터프라이즈 컴퓨터는 여러 사용자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-137">Multiple enterprise computers are used by multiple users.</span></span> <span data-ttu-id="981a7-138">각 사용자의 설정 환경은 모든 컴퓨터에서 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-138">Each user’s settings experience should be the same across all computers.</span></span>

<span data-ttu-id="981a7-139">**%Username%\\%computername%** 변수를 서버의 UNC 경로와 공유 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-139">You can use the **%username%\\%computername%** variables with the UNC path of the server and share.</span></span> <span data-ttu-id="981a7-140">이렇게 하면 각 컴퓨터에 대 한 설정 환경이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-140">This will preserve the settings experience for each computer.</span></span> <span data-ttu-id="981a7-141">다음과 같은 시나리오를 위해이 구성을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-141">Consider this configuration for the following scenarios:</span></span>

1.  <span data-ttu-id="981a7-142">기업의 사용자는 여러 개의 물리적 컴퓨터를 보유 하 고 있으며 각 컴퓨터에 대 한 설정 환경을 유지 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-142">Users in the enterprise have multiple physical computers and you want to preserve the settings experience for each computer.</span></span>

2.  <span data-ttu-id="981a7-143">엔터프라이즈 컴퓨터는 여러 사용자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-143">The enterprise computers are used by multiple users.</span></span> <span data-ttu-id="981a7-144">설정 환경은 사용자가 로그인 하는 각 컴퓨터에 대해 유지 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-144">The settings experience should be preserved for each computer that the user logs into.</span></span>

<span data-ttu-id="981a7-145">UE-V agent는 UE-V `SettingsStoragePath` 구성 설정 및 정의 된 변수를 기반으로 사용자 관련 설정 저장소 경로를 동적으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-145">The UE-V agent dynamically creates the user-specific settings storage path based on a UE-V `SettingsStoragePath` configuration setting and the variables that are defined.</span></span>

<span data-ttu-id="981a7-146">UE-V agent `SettingsPackages` 가 각 사용자 관련 저장소 위치 내에서 이름이 지정 된 숨겨진 시스템 폴더를 동적으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-146">The UE-V agent dynamically creates a hidden system folder named `SettingsPackages` within each user-specific storage location.</span></span> <span data-ttu-id="981a7-147">UE-V agent는 등록 된 UE-V 설정 위치 템플릿에서 정의한 대로이 위치에 대 한 설정을 읽고 씁니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-147">The UE-V agent reads and writes settings to this location as defined by registered UE-V settings location templates.</span></span>

<span data-ttu-id="981a7-148">설정 저장소 위치가 사용자의 관리 컴퓨터 집합에 대해 동일 하면 해당 UE-V 설정이 "마지막 쓰기 wins" 규칙에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-148">If the settings storage location is the same for a set of managed computers of a user, the applicable UE-V settings are determined by a “Last write wins” rule.</span></span> <span data-ttu-id="981a7-149">한 컴퓨터에서 실행 되는 에이전트는 다른 컴퓨터에서 실행 되는 에이전트와 독립적으로 설정 위치를 읽고 씁니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-149">The agent that runs on one computer reads and writes to the settings location independently of agents that run on other computers.</span></span> <span data-ttu-id="981a7-150">마지막으로 작성 된 설정 및 값은 다음 에이전트가 설정 저장소 위치에서 읽을 때 적용 되는 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-150">The last settings and values written are the settings that are applied when the next agent reads from the settings storage location.</span></span> <span data-ttu-id="981a7-151">자세한 내용은 [ue-v 1.0에 대 한 설정 저장소 위치 배포](deploying-the-settings-storage-location-for-ue-v-10.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="981a7-151">For more information, see [Deploying the Settings Storage Location for UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md).</span></span>

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a><span data-ttu-id="981a7-152">UE-V를 사용 하 여 Active Directory home 디렉터리 사용</span><span class="sxs-lookup"><span data-stu-id="981a7-152">Use Active Directory home directory with UE-V</span></span>

<span data-ttu-id="981a7-153">에이전트가 배포 될 때 UE-V-V에 대해 구성 된 설정 저장소 위치가 없으면 사용자의 Active Directory (AD) 홈 디렉터리가 설정 위치 패키지를 저장 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-153">If no settings storage location is configured for UE-V when the agent is deployed, then the user’s Active Directory (AD) home directory is used to store settings location packages.</span></span> <span data-ttu-id="981a7-154">UE-V agent가 각 사용자의 AD home 디렉터리 아래에 있는 설정 저장소 폴더를 동적으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-154">The UE-V agent dynamically creates the settings storage folder below the root of the AD home directory of each user.</span></span> <span data-ttu-id="981a7-155">설정 저장소 위치 (SettingsStoragePath)가 달리 정의 되지 않은 경우 에이전트는 Active Directory 홈 디렉터리만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-155">The agent only uses the Active Directory home directory if a settings storage location (SettingsStoragePath) is not otherwise defined.</span></span>

## <a href="" id="bkmk-synchronizecomputerclocks"></a><span data-ttu-id="981a7-156">UE-V 설정 동기화에 대 한 컴퓨터 시계 동기화</span><span class="sxs-lookup"><span data-stu-id="981a7-156">Synchronize computer clocks for UE-V settings synchronization</span></span>


<span data-ttu-id="981a7-157">UE-V agent를 실행 하 여 설정을 동기화 하는 컴퓨터는 시간 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-157">Computers that run the UE-V agent to synchronize settings must use a time server.</span></span> <span data-ttu-id="981a7-158">타임 스탬프는 설정 저장소 위치에서 설정을 동기화 해야 하는지 여부를 결정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-158">Time stamps are used to determine if settings need to be synchronized from the settings storage location.</span></span> <span data-ttu-id="981a7-159">컴퓨터 시계가 정확 하지 않으면 이전 설정이 최신 설정을 덮어쓰거나 새 설정이 설정 저장소 위치에 저장 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-159">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span> <span data-ttu-id="981a7-160">시간 서버를 사용 하면 UE-V가 일관 된 설정 환경을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-160">The use of a time server enables UE-V to maintain a consistent settings experience.</span></span>

## <a href="" id="bkmk-performancecapacityplanning"></a><span data-ttu-id="981a7-161">성능 및 용량 계획</span><span class="sxs-lookup"><span data-stu-id="981a7-161">Performance and capacity planning</span></span>


<span data-ttu-id="981a7-162">UE-V의 용량 요구 사항은 표준 디스크 용량 및 네트워크 상태 모니터링을 사용 하 여 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-162">Capacity requirements for UE-V can be determined by use of standard disk capacity and network health monitoring.</span></span> <span data-ttu-id="981a7-163">UE-V가 설정 패키지 저장소에 대 한 SMB (서버 메시지 블록) 공유를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-163">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="981a7-164">설정 패키지의 크기는 특정 응용 프로그램에 대 한 설정 정보에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-164">The size of settings packages varies depending on the settings information for a specific application.</span></span> <span data-ttu-id="981a7-165">대부분의 설정 패키지는 작지만 데스크톱 이미지와 같은 잠재적으로 크기가 큰 파일을 동기화 하면 성능이 저하 될 수 있으며, 특히 네트워크 속도가 느릴 때 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-165">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span> <span data-ttu-id="981a7-166">네트워크 지연 문제를 최소화 하려면 사용자 컴퓨터가 있는 동일한 로컬 네트워크에 설정 저장소 위치를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-166">To minimize problems with network latency, you should create settings storage locations on the same local networks where the users’ computers reside.</span></span>

<span data-ttu-id="981a7-167">기본적으로 UE-V 동기화는 네트워크가 느리거나 설정 패키지가 큰 경우 2 초 후에 시간이 초과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-167">By default, the UE-V synchronization will time out after 2 seconds if the network is slow or the settings package is large.</span></span> <span data-ttu-id="981a7-168">그룹 정책을 사용 하 여 시간 제한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="981a7-168">You can configure the timeout with Group Policy.</span></span> <span data-ttu-id="981a7-169">시간 제한을 설정 하는 방법에 대 한 자세한 내용은 [그룹 정책 개체를 사용 하 여 Ue-v 구성을](configuring-ue-v-with-group-policy-objects.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="981a7-169">For more information about how to set the timeout, see [Configuring UE-V with Group Policy Objects](configuring-ue-v-with-group-policy-objects.md).</span></span>

## <span data-ttu-id="981a7-170">관련 항목</span><span class="sxs-lookup"><span data-stu-id="981a7-170">Related topics</span></span>


[<span data-ttu-id="981a7-171">Microsoft User Experience Virtualization(UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="981a7-171">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="981a7-172">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="981a7-172">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="981a7-173">UE-V 1.0에 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="981a7-173">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

 

 





