---
title: Microsoft User Experience Virtualization(UE-V) 1.0 릴리스 정보
description: Microsoft User Experience Virtualization(UE-V) 1.0 릴리스 정보
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812489"
---
# <span data-ttu-id="fdd30-103">Microsoft User Experience Virtualization(UE-V) 1.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="fdd30-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="fdd30-104">Microsoft UE-V (사용자 환경 가상화) 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="fdd30-105">UE-V를 설치 하기 전에이 릴리스 노트를 철저히 읽어 보아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="fdd30-106">릴리스 정보에는 사용자 환경 가상화를 성공적으로 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 추가 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="fdd30-107">이러한 릴리스 정보와 다른 UE-V 문서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="fdd30-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="fdd30-109">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="fdd30-109">Providing feedback</span></span>


<span data-ttu-id="fdd30-110">피드백과 설명을 제공 하 여 MDOP에 대 한 설명서에 대 한 의견을 알려주세요.</span><span class="sxs-lookup"><span data-stu-id="fdd30-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="fdd30-111">[Mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation)에 게 설명서 피드백을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="fdd30-112">UE-V의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="fdd30-112">UE-V known issues</span></span>


<span data-ttu-id="fdd30-113">이 섹션에서는 사용자 환경 가상화에 대 한 릴리스 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="fdd30-114">동일한 컴퓨터에서 레지스트리 설정이 App-v와 기본 응용 프로그램 간에 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="fdd30-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="fdd30-115">컴퓨터에 Application Virtualization (App-v) 응용 프로그램과 네이티브 설치 응용 프로그램 (.msi 파일과 함께 설치)을 모두 통해 사용할 수 있는 응용 프로그램이 있는 경우 레지스트리 기반 설정이 기술 간에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="fdd30-116">해결 방법:이 문제를 해결 하려면 두 기술 중 하나를 선택 하 여 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="fdd30-117">Windows 8 설정 동기화가 오류로 인해 실패 함: "부스트:: filesystem:: exists:: 잘못 된 사용자 이름 또는 암호"</span><span class="sxs-lookup"><span data-stu-id="fdd30-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="fdd30-118">Windows® 8 운영 체제 설정 동기화는 다음 오류 메시지와 함께 실패 합니다. **부스트:: filesystem:: exists:: 잘못 된 사용자 이름 또는 비밀 번호**입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="fdd30-119">작동 로그 이벤트를 확인 하려면 **이벤트 뷰어** 를 열고 **응용 프로그램 및 서비스**를 탐색  /  합니다**Microsoft**  /  **사용자 환경 가상화**  /  **로깅이**  /  **작동**하도록 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="fdd30-120">UE-V 설정 저장소 위치에 사용 되는 네트워크 공유는 사용자와 동일한 Active Directory 도메인에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="fdd30-121">그렇지 않으면 "잘못 된 사용자 이름 또는 암호" 오류가 발생할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="fdd30-122">해결 방법: 사용자와 동일한 Active Directory 도메인의 네트워크 공유를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="fdd30-123">.</span><span class="sxs-lookup"><span data-stu-id="fdd30-123">.</span></span>

### <span data-ttu-id="fdd30-124">Outlook 2010에 대 한 전자 메일 서명 로밍</span><span class="sxs-lookup"><span data-stu-id="fdd30-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="fdd30-125">UE-V는 장치 간에 Outlook 2010 서명 파일을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="fdd30-126">그러나 새 메시지 및 회신/전달에 대 한 기본 서명 옵션은 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="fdd30-127">이러한 두 설정은 Outlook 프로필에 저장 되며,이는 UE-V가 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="fdd30-128">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="fdd30-129">느린 연결 모드에서 실행 될 때 동기화 설정이 예상 간격 동안 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="fdd30-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="fdd30-130">일반 조건에서 빠른 연결 네트워크 연결을 통해 설정 저장소 위치를 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="fdd30-131">느린 링크 모드에서는 동기화가 정기적 으로만 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="fdd30-132">기본적으로 느린 연결 모드 동기화 일정은 360 분 마다 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="fdd30-133">해결 방법: 느린 연결 모드의 컴퓨터에 대해 백그라운드 동기화 주기를 변경 하려면 **오프 라인 파일**의 백그라운드 동기화 정책에 대 한 그룹 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="fdd30-134">특수 문자는 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-134">Special characters do not synchronize</span></span>

<span data-ttu-id="fdd30-135">통화 기호 등의 특정 문자는 UE-V 에이전트를 실행 하는 windows 7 및 Windows 8 컴퓨터 간에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="fdd30-136">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="fdd30-137">UE-V는 32 비트와 64 비트 버전의 Microsoft Office 간 로밍 설정을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="fdd30-138">32 비트 및 64 비트 운영 체제 모두에 대해 32 비트 버전의 Microsoft Office를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="fdd30-139">필요한 Microsoft Office 버전을 선택 하려면 여기를 클릭 하세요.</span><span class="sxs-lookup"><span data-stu-id="fdd30-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="fdd30-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="fdd30-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="fdd30-141">UE-V는 동일한 아키텍처 버전의 Office 간에 로밍 설정을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="fdd30-142">예를 들어 32 비트 Office 설정은 모든 32 비트 Office 인스턴스 간에 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="fdd30-143">UE-V는 32 비트와 64 비트 버전의 Office 간에 로밍 설정을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="fdd30-144">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-144">WORKAROUND: None</span></span>

### <span data-ttu-id="fdd30-145">느린 연결 모드에서는 설정 저장소 위치가 있는 공유의 다른 폴더를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="fdd30-146">설정 저장소 공유는 항상 사용할 수 있어야 하는 다른 폴더에 사용 되는 네트워크 공유에 위치 하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="fdd30-147">설정 저장소 위치를 호스팅하는 네트워크 공유가 느린 연결 모드로 들어가면 설정 저장소 위치 폴더만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="fdd30-148">느린 연결 모드에서는 공유에 있는 다른 폴더를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="fdd30-149">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-149">Workaround: None</span></span>

### <span data-ttu-id="fdd30-150">Internet Explorer 9 즐겨찾기에 연결 된 Favicons는 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="fdd30-151">Internet Explorer 9 즐겨찾기에 연결 된 favicons는 사용자 환경 가상화에 의해 roamed 되지 않으며 즐겨찾기가 새 컴퓨터에 처음 나타날 때 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="fdd30-152">해결 방법: Internet Explorer 9 브라우저에서 책갈피를 사용 하 고 캐시 하면 연결 된 즐겨찾기와 함께 Favicons 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="fdd30-153">파일 설정 경로가 레지스트리에 저장 됨</span><span class="sxs-lookup"><span data-stu-id="fdd30-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="fdd30-154">일부 응용 프로그램 설정에서는 구성 및 설정 파일의 경로가 레지스트리의 값으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="fdd30-155">컴퓨터 간에 설정이 roamed 되는 경우 레지스트리의 경로로 참조 되는 파일을 동기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="fdd30-156">해결 방법: 폴더 리디렉션 또는 다른 기술을 사용 하 여 파일 설정 경로로 참조 되는 파일이 있고 설정이 로밍 되는 모든 컴퓨터의 동일한 위치에 배치 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="fdd30-157">260 자 보다 긴 경로는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="fdd30-158">260 자 보다 긴 설정 저장소 경로는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="fdd30-159">260 자 보다 긴 설정 저장소 경로에 UE-V 설정 패키지를 복사 하면 UE-V 작동 이벤트 로그에서 **\ [부스트:: filesystem:: copy \ _file: 시스템에서 지정 된 경로를 찾을 수 없습니다. \]** 라는 예외 메시지가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="fdd30-160">작동 로그 이벤트를 확인 하려면 **이벤트 뷰어** 를 열고 **응용 프로그램 및 서비스**를 탐색  /  합니다**Microsoft**  /  **사용자 환경 가상화**  /  **로깅이**  /  **작동**하도록 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="fdd30-161">260 자를 초과 하는 파일 설정 경로는 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="fdd30-162">UE-V 설정 위치 템플릿에서 참조 되는 파일 설정은 260 자를 초과 하는 디렉터리 경로에 있을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="fdd30-163">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="fdd30-164">로그 아웃 또는 로그인 시 UE-V 에이전트 지연</span><span class="sxs-lookup"><span data-stu-id="fdd30-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="fdd30-165">오프 라인 파일에서 느린 링크가 있는 것으로 확인 한 후에 로그온 또는 로그 아웃이 발생 하는 경우 로그 아웃 또는 로그인이 지연 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="fdd30-166">오프 라인 파일 기능에서 현재 네트워크 상태를 검색 하는 데 최대 3 분이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="fdd30-167">오프 라인 파일이 느린 링크에 연결 되어 있는 것으로 확인 된 후에 로그온 또는 종료가 발생 한 경우, UE-V 설정 패키지는 로컬 캐시 대신 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="fdd30-168">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="fdd30-169">Windows 8에서 운영 체제 설정을 로밍 하려고 할 때 설정이 충돌 함</span><span class="sxs-lookup"><span data-stu-id="fdd30-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="fdd30-170">Windows 8에서 운영 체제 설정에 대해 UE-V를 사용 하 여 Microsoft 계정 동기화를 사용 하도록 설정한 경우 적용 되는 설정이 일관성이 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="fdd30-171">해결 방법: 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="fdd30-172">UE-V를 사용 하 여 운영 체제 설정을 로밍 하는 경우 Microsoft 계정 동기화를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="fdd30-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="fdd30-173">운영 체제 설정에 대해 UE-V 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="fdd30-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="fdd30-174">일부 운영 체제 설정은 like 운영 체제 버전 간에만 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="fdd30-175">로캘과 관련 된 내레이터 및 통화 문자에 대 한 운영 체제 설정은 Windows의 운영 체제 버전과 유사 하 게 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="fdd30-176">예를 들어 통화 문자는 Windows 7에서 Windows 7으로 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="fdd30-177">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-177">WORKAROUND: None</span></span>

### <span data-ttu-id="fdd30-178">Internet explorer 책갈피가 Internet Explorer 스마트 막대에 나타나지 않음</span><span class="sxs-lookup"><span data-stu-id="fdd30-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="fdd30-179">Internet Explorer 책갈피가 한 컴퓨터에서 다른 컴퓨터로 로밍 하는 경우 두 번째 컴퓨터의 인덱스가 업데이트 되지 않으므로 주소 표시줄에 입력 하는 경우 즐겨찾기가 컴퓨터 2의 검색 결과로 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd30-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="fdd30-180">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="fdd30-180">WORKAROUND: None</span></span>

 

 





