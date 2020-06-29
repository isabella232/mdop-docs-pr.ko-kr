---
title: Microsoft User Experience Virtualization(UE-V) 1.0 SP1 릴리스 정보
description: Microsoft User Experience Virtualization(UE-V) 1.0 SP1 릴리스 정보
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812484"
---
# <span data-ttu-id="d9813-103">Microsoft User Experience Virtualization(UE-V) 1.0 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="d9813-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="d9813-104">Microsoft UE-V (사용자 환경 가상화) 1.0 서비스 팩 1 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d9813-105">UE-V를 설치 하기 전에이 릴리스 노트를 철저히 읽어 보아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="d9813-106">릴리스 정보에는 사용자 환경 가상화를 성공적으로 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 추가 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="d9813-107">이러한 릴리스 정보와 다른 UE-V 문서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d9813-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="d9813-109">UE-V의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="d9813-109">UE-V known issues</span></span>


<span data-ttu-id="d9813-110">이 섹션에서는 사용자 환경 가상화 1.0 SP1에 대 한 릴리스 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="d9813-111">동일한 컴퓨터에서 레지스트리 설정이 App-v와 기본 응용 프로그램 간에 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="d9813-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="d9813-112">컴퓨터에 Application Virtualization (App-v) 응용 프로그램을 통해 사용할 수 있는 응용 프로그램이 있고 Windows Installer (.msi 파일)와 함께 설치 된 네이티브 설치 응용 프로그램이 있는 경우 레지스트리 기반 설정이 기술 간에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="d9813-113">해결 방법:이 문제를 해결 하려면 두 기술 중 하나를 선택 하 여 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="d9813-114">네트워크 공유가 사용자의 도메인 외부에 있을 경우 Windows 8 설정 동기화 실패</span><span class="sxs-lookup"><span data-stu-id="d9813-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="d9813-115">Windows® 8에서 운영 체제 설정을 동기화 하려고 하면 synchrnization에서 다음 오류 메시지가 나타납니다. **부스트:: filesystem:: exists:: 잘못 된 사용자 이름 또는 암호**를 사용 하 여 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="d9813-116">이 오류는 네트워크 공유가 사용자의 도메인 외부에 있음을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="d9813-117">작동 로그 이벤트를 확인 하려면 **이벤트 뷰어** 를 열고 **응용 프로그램 및 서비스**를 탐색  /  합니다**Microsoft**  /  **사용자 환경 가상화**  /  **로깅이**  /  **작동**하도록 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="d9813-118">UE-V 설정 저장소 위치에 사용 되는 네트워크 공유는 사용자와 동일한 Active Directory 도메인에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="d9813-119">해결 방법: 사용자와 동일한 Active Directory 도메인의 네트워크 공유를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="d9813-120">.</span><span class="sxs-lookup"><span data-stu-id="d9813-120">.</span></span>

### <span data-ttu-id="d9813-121">Outlook 2010에 대 한 전자 메일 서명 로밍</span><span class="sxs-lookup"><span data-stu-id="d9813-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="d9813-122">UE-V는 장치 간에 Outlook 2010 서명 파일을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="d9813-123">그러나 새 메시지 및 회신/전달에 대 한 기본 서명 옵션은 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="d9813-124">이러한 두 설정은 Outlook 프로필에 저장 되며, 여기서 UE-V는 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="d9813-125">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="d9813-126">느린 연결 모드에서 실행 될 때 동기화 설정이 예상 간격 동안 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="d9813-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="d9813-127">일반 조건에서 빠른 연결 네트워크 연결을 통해 설정 저장소 위치를 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="d9813-128">느린 링크 모드에서는 동기화가 정기적 으로만 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="d9813-129">기본적으로 느린 연결 모드 동기화 일정은 360 분 마다 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="d9813-130">해결 방법: 느린 연결 모드의 컴퓨터에 대해 백그라운드 동기화 주기를 변경 하려면 **오프 라인 파일**의 백그라운드 동기화 정책에 대 한 그룹 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="d9813-131">특수 문자는 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-131">Special characters do not synchronize</span></span>

<span data-ttu-id="d9813-132">통화 기호 등의 특정 문자는 UE-V 에이전트를 실행 하는 windows 7 및 Windows 8 컴퓨터 간에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="d9813-133">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="d9813-134">UE-V는 32 비트와 64 비트 버전의 Microsoft Office 간 로밍 설정을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="d9813-135">32 비트 및 64 비트 운영 체제 모두에 대해 32 비트 버전의 Microsoft Office를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="d9813-136">필요한 Microsoft Office 버전을 선택 하려면 여기를 클릭 [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) 하세요 ().</span><span class="sxs-lookup"><span data-stu-id="d9813-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="d9813-137">UE-V는 동일한 아키텍처 버전의 Office 간에 로밍 설정을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="d9813-138">예를 들어 32 비트 Office 설정은 모든 32 비트 Office 인스턴스 간에 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="d9813-139">UE-V는 32 비트와 64 비트 버전의 Office 간에 로밍 설정을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="d9813-140">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="d9813-141">MSI는 지역화 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-141">MSI’s are not localized</span></span>

<span data-ttu-id="d9813-142">UE-V 1.0 SP1에는 UE-V Agent와 UE-V 생성기에 대 한 지역화 된 설치 프로그램이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="d9813-143">이러한 MSI 파일은 계속 사용할 수 있지만 사용자 인터페이스가 최소화 되 고 MSI의 영어로만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="d9813-144">파일이 영어로 되어 있더라도 설치 하는 동안 설치 프로그램이 지원 되는 모든 언어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="d9813-145">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-145">WORKAROUND: None</span></span>

### <span data-ttu-id="d9813-146">느린 연결 모드에서는 설정 저장소 위치가 있는 공유의 다른 폴더를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="d9813-147">설정 저장소 공유는 항상 사용할 수 있어야 하는 다른 폴더에 사용 되는 네트워크 공유에 위치 하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="d9813-148">설정 저장소 위치를 호스팅하는 네트워크 공유가 느린 연결 모드로 들어가면 설정 저장소 위치 폴더만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="d9813-149">느린 연결 모드에서는 공유에 있는 다른 폴더를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="d9813-150">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-150">Workaround: None</span></span>

### <span data-ttu-id="d9813-151">Internet Explorer 9 즐겨찾기에 연결 된 Favicons는 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="d9813-152">Internet Explorer 9 즐겨찾기에 연결 된 favicons는 사용자 환경 가상화에 의해 roamed 되지 않으며 즐겨찾기가 새 컴퓨터에 처음 나타날 때 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="d9813-153">해결 방법: Internet Explorer 9 브라우저에서 책갈피를 사용 하 고 캐시 하면 연결 된 즐겨찾기와 함께 Favicons 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="d9813-154">파일 설정 경로가 레지스트리에 저장 됨</span><span class="sxs-lookup"><span data-stu-id="d9813-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="d9813-155">일부 응용 프로그램 설정에서는 구성 및 설정 파일의 경로가 레지스트리의 값으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="d9813-156">컴퓨터 간에 설정이 roamed 되는 경우 레지스트리의 경로로 참조 되는 파일을 동기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="d9813-157">해결 방법: 폴더 리디렉션 또는 다른 기술을 사용 하 여 파일 설정 경로로 참조 되는 파일이 있고 설정이 로밍 되는 모든 컴퓨터의 동일한 위치에 배치 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="d9813-158">긴 설정 저장소 경로로 인해 오류가 발생할 수 있음</span><span class="sxs-lookup"><span data-stu-id="d9813-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="d9813-159">설정 저장소 경로를 최대한 짧게 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="d9813-160">경로가 길면 해상도 또는 동기화를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="d9813-161">UE-V는 설정 저장소 경로를 계산 된 경로의 일부로 사용 하 여 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="d9813-162">이 경로는 설정 저장소 경로 + "settingspackages" + 패키지 디렉터리 (템플릿 ID) + 패키지 이름 (템플릿 ID)으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="d9813-163">해당 계산 경로가 260 자를 초과 하는 경우 패키지 저장소에 오류가 발생 하 고 UE-V 작동 이벤트 로그에서 다음 오류 메시지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="d9813-164">작업 로그 이벤트를 확인 하려면 이벤트 뷰어를 열고 응용 프로그램 및 서비스 로그/Microsoft/사용자 환경 가상화/로깅/작동으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="d9813-165">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="d9813-166">로그 아웃 또는 로그인 시 UE-V 에이전트 지연</span><span class="sxs-lookup"><span data-stu-id="d9813-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="d9813-167">오프 라인 파일에서 느린 링크가 있는 것으로 확인 한 후에 로그온 또는 로그 아웃이 발생 하는 경우 로그 아웃 또는 로그인이 지연 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="d9813-168">오프 라인 파일 기능에서 현재 네트워크 상태를 검색 하는 데 최대 3 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="d9813-169">오프 라인 파일이 느린 링크에 연결 되어 있는 것으로 확인 된 후에 로그온 또는 종료가 발생 한 경우, UE-V 설정 패키지는 로컬 캐시 대신 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="d9813-170">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="d9813-171">Windows 8에서 운영 체제 설정을 로밍 하려고 할 때 설정이 충돌 함</span><span class="sxs-lookup"><span data-stu-id="d9813-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="d9813-172">Windows 8에서 운영 체제 설정에 대해 UE-V를 사용 하 여 Microsoft 계정 동기화를 사용 하도록 설정한 경우 적용 되는 설정이 일관성이 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="d9813-173">해결 방법: 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="d9813-174">UE-V를 사용 하 여 운영 체제 설정을 로밍 하는 경우 Microsoft 계정 동기화를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="d9813-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="d9813-175">운영 체제 설정에 대해 UE-V 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="d9813-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="d9813-176">일부 운영 체제 설정은 like 운영 체제 버전 간에만 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="d9813-177">로캘과 관련 된 내레이터 및 통화 문자에 대 한 운영 체제 설정은 Windows의 운영 체제 버전과 유사 하 게 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="d9813-178">예를 들어 통화 문자는 Windows 7에서 Windows 7으로 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="d9813-179">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="d9813-179">WORKAROUND: None</span></span>

 

 





