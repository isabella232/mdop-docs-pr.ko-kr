---
title: Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보
description: Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825283"
---
# <span data-ttu-id="aca99-103">Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="aca99-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="aca99-104">Microsoft UE-V (User Experience Virtualization) 2.0 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="aca99-105">UE-V를 설치 하기 전에이 릴리스 노트를 철저히 읽어 보아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="aca99-106">릴리스 정보에는 사용자 환경 가상화를 성공적으로 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 추가 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="aca99-107">이러한 릴리스 정보와 다른 UE-V 문서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="aca99-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="aca99-109">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="aca99-109">Providing feedback</span></span>


<span data-ttu-id="aca99-110">피드백과 설명을 제공 하 여 MDOP에 대 한 설명서에 대 한 의견을 알려주세요.</span><span class="sxs-lookup"><span data-stu-id="aca99-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="aca99-111">[Mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation)에 게 설명서 피드백을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="aca99-112">UE-V의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="aca99-112">UE-V known issues</span></span>


<span data-ttu-id="aca99-113">이 섹션에서는 사용자 환경 가상화에 대 한 릴리스 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="aca99-114">레지스트리 설정이 동일한 컴퓨터의 App-v와 네이티브 응용 프로그램 간에 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="aca99-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="aca99-115">컴퓨터에 Application Virtualization (App-v) 및 Windows Installer (.msi) 파일이 로컬로 설치 된 응용 프로그램이 있는 경우 레지스트리 기반 설정이 기술 간에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="aca99-116">**해결 방법:** 이 문제를 해결 하려면 두 기술 중 하나를 선택 하 여 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="aca99-117">네트워크 공유가 사용자의 도메인 외부에 있는 경우 설정이 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="aca99-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="aca99-118">Windows® 8에서 운영 체제 설정을 동기화 하려고 하면 다음과 같은 오류 메시지가 나타나면서 동기화에 실패 합니다. **부스트:: filesystem:: exists:: 잘못 된 사용자 이름 또는 비밀 번호**입니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="aca99-119">이 오류는 네트워크 공유가 사용자의 도메인 외부에 있음을 나타내거나 해당 도메인에 대 한 신뢰 관계의 도메인 인지 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="aca99-120">작동 로그 이벤트를 확인 하려면 **이벤트 뷰어** 를 열고 **응용 프로그램 및 서비스**를 탐색  /  합니다**Microsoft**  /  **사용자 환경 가상화**  /  **로깅이**  /  **작동**하도록 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="aca99-121">UE-V 설정 저장소 위치에 사용 되는 네트워크 공유는 사용자와 동일한 Active Directory 도메인 또는 사용자 도메인의 트러스트 된 도메인에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="aca99-122">**해결 방법:** 사용자와 동일한 Active Directory 도메인의 네트워크 공유를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="aca99-123">Office 2010 및 Office 2013가 설치 된 예기치 않은 결과</span><span class="sxs-lookup"><span data-stu-id="aca99-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="aca99-124">사용자에 게 Office 2010 및 Office 2013이 모두 설치 되어 있는 경우 두 Office 버전 간의 일반적인 설정은 UE-V를 사용 하 여 roamed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="aca99-125">이로 인해 Office 2010 패키지 크기가 매우 커질 수 있고, 특히 Office 365을 사용 하는 경우에는 2013에서 예기치 않은 충돌을 일으킵니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="aca99-126">**해결 방법:** 한 버전의 Office만 설치 하거나 UE-V를 통해 동기화 되는 설정을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="aca99-127">Windows 8 앱의 제거 및 다시 설치 초기 상태로 설정 되돌리기</span><span class="sxs-lookup"><span data-stu-id="aca99-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="aca99-128">Windows 8 앱에 대 한 UE-V 설정 동기화를 사용 하는 경우 사용자가 앱을 제거 하 고 앱을 다시 설치 하면 앱의 설정이 해당 기본값으로 되돌려집니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="aca99-129">이는 제거로 인해 앱 설정의 로컬 (캐시 된) 복사본이 제거 되 고 로컬 UE-V 설정 패키지는 제거 되지 않기 때문에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="aca99-130">앱을 다시 설치 하 고 실행할 때 UE-V는 앱 기본값으로 다시 설정 된 앱 설정을 수집 하 고 기본 설정을 중앙 저장소 위치에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="aca99-131">앱을 실행 하는 다른 컴퓨터에서 기본 설정을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="aca99-132">이 동작은 데스크톱 응용 프로그램의 동작과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="aca99-133">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="aca99-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="aca99-134">Outlook 2010에 대 한 전자 메일 서명 로밍</span><span class="sxs-lookup"><span data-stu-id="aca99-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="aca99-135">UE-V는 장치 간에 Outlook 2010 서명 파일을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="aca99-136">그러나 새 메시지 및 회신 또는 전달에 대 한 기본 서명 옵션은 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="aca99-137">이러한 두 설정은 Outlook 프로필에 저장 되며, 여기서 UE-V는 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="aca99-138">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="aca99-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="aca99-139">UE-V는 32 비트와 64 비트 버전의 Microsoft Office 간 로밍 설정을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="aca99-140">최신 컴퓨터에 64 비트 버전의 Microsoft Office를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="aca99-141">필요한 버전을 확인 하려면 여기를 [클릭](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions)하세요.</span><span class="sxs-lookup"><span data-stu-id="aca99-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="aca99-142">UE-V는 동일한 아키텍처 버전의 Office 간에 로밍 설정을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="aca99-143">예를 들어 32 비트 Office 설정은 모든 32 비트 Office 인스턴스 간에 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="aca99-144">UE-V는 32 비트와 64 비트 버전의 Office 간에 로밍 설정을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="aca99-145">**해결 방법:** 않아야</span><span class="sxs-lookup"><span data-stu-id="aca99-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="aca99-146">MSI는 지역화 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-146">MSI’s are not localized</span></span>

<span data-ttu-id="aca99-147">UE-V 2.0에는 ue-v 에이전트와 UE-V 생성기에 대 한 지역화 된 설치 프로그램이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="aca99-148">이러한 MSI 파일은 계속 사용할 수 있지만 사용자 인터페이스가 최소화 되 고 MSI의 영어로만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="aca99-149">파일이 영어로 되어 있더라도 설치 하는 동안 설치 프로그램이 지원 되는 모든 언어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="aca99-150">**해결 방법:** 않아야</span><span class="sxs-lookup"><span data-stu-id="aca99-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="aca99-151">Internet Explorer 9 즐겨찾기에 연결 된 Favicons는 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="aca99-152">Internet Explorer 9 즐겨찾기에 연결 된 favicons는 사용자 환경 가상화에 의해 roamed 되지 않으며 즐겨찾기가 새 컴퓨터에 처음 나타날 때 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="aca99-153">**해결 방법:** Internet Explorer 9 브라우저에서 책갈피를 사용 하 고 캐시 하면 연결 된 즐겨찾기에 Favicons 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="aca99-154">파일 설정 경로가 레지스트리에 저장 됨</span><span class="sxs-lookup"><span data-stu-id="aca99-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="aca99-155">일부 응용 프로그램 설정에서는 구성 및 설정 파일의 경로가 레지스트리의 값으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="aca99-156">컴퓨터 간에 설정이 roamed 되는 경우 레지스트리의 경로로 참조 되는 파일을 동기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="aca99-157">**해결 방법:** 폴더 리디렉션 또는 다른 기술을 사용 하 여 파일 설정 경로로 참조 되는 파일이 있고 설정이 로밍 되는 모든 컴퓨터의 동일한 위치에 배치 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="aca99-158">긴 설정 저장소 경로로 인해 오류가 발생할 수 있음</span><span class="sxs-lookup"><span data-stu-id="aca99-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="aca99-159">설정 저장소 경로를 최대한 짧게 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="aca99-160">경로가 길면 해상도 또는 동기화를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="aca99-161">UE-V는 설정 저장소 경로를 계산 된 경로의 일부로 사용 하 여 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="aca99-162">이 경로는 설정 저장소 경로 + "settingspackages" + 패키지 디렉터리 (템플릿 ID) + 패키지 이름 (템플릿 ID) + pkgx로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="aca99-163">해당 계산 경로가 260 자를 초과 하는 경우 패키지 저장소에 오류가 발생 하 고 UE-V 작동 이벤트 로그에서 다음 오류 메시지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="aca99-164">작업 로그 이벤트를 확인 하려면 이벤트 뷰어를 열고 응용 프로그램 및 서비스 로그/Microsoft/사용자 환경 가상화/로깅/작동으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="aca99-165">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="aca99-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="aca99-166">일부 운영 체제 설정은 like 운영 체제 버전 간에만 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="aca99-167">로캘과 관련 된 내레이터 및 통화 문자 (즉, 언어 및 국가별 설정)에 대 한 운영 체제 설정은 Windows의 운영 체제 버전과 유사 하 게 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="aca99-168">예를 들어 통화 문자는 Windows 7과 Windows 8 사이에서 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="aca99-169">**해결 방법:** 않아야</span><span class="sxs-lookup"><span data-stu-id="aca99-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="aca99-170">Windows 8 앱이 예기치 않게 닫힌 후 앱을 다시 시작할 때 설정을 동기화 하지 않음</span><span class="sxs-lookup"><span data-stu-id="aca99-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="aca99-171">Windows 8 앱이 시작 된 후 예기치 않게 종료 되 면 응용 프로그램을 다시 시작할 때 응용 프로그램 설정이 동기화 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="aca99-172">**해결 방법:** Windows 8 앱을 닫고 UevAppMonitor.exe 응용 프로그램 (TaskManager을 사용할 수 있음)을 닫았다가 다시 시작한 다음 Windows 8 앱을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="aca99-173">UE-V 2 템플릿을 실행 하는 경우 UE-V 1 agent가 오류를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="aca99-174">Ue-v 1 에이전트를 사용 하 여 설치한 컴퓨터에 UE-V 2 설정 위치 템플릿이 배포 되는 경우 일부 설정이 컴퓨터와 에이전트 오류 보고의 이벤트 로그에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="aca99-175">**해결 방법:** UE-V 1에서 UE-V 2로 마이그레이션할 때 이전 버전의 에이전트를 실행 하는 컴퓨터를 사용 하는 경우 UE-V 2.0 에이전트 및 템플릿을 지원 하기 위해 별도의 UE-V 2.0 catalog를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="aca99-176">UE-V 2.0에 대 한 핫픽스 및 지식 기본 문서</span><span class="sxs-lookup"><span data-stu-id="aca99-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="aca99-177">이 섹션에는 UE-V 2.0에 대 한 핫픽스와 KB 문서가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="aca99-178">기술 자료 문서</span><span class="sxs-lookup"><span data-stu-id="aca99-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="aca99-179">제목</span><span class="sxs-lookup"><span data-stu-id="aca99-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="aca99-180">Link</span><span class="sxs-lookup"><span data-stu-id="aca99-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-181">2927019</span><span class="sxs-lookup"><span data-stu-id="aca99-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-182">Microsoft 사용자 환경 가상화 2.0 핫픽스 패키지 1</span><span class="sxs-lookup"><span data-stu-id="aca99-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="aca99-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="aca99-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-184">2903501</span><span class="sxs-lookup"><span data-stu-id="aca99-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-185">UE-V: 사용자 프로필과의 사용자 환경 가상화 (UE-V) 호환성</span><span class="sxs-lookup"><span data-stu-id="aca99-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="aca99-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-187">2770042</span><span class="sxs-lookup"><span data-stu-id="aca99-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-188">UE-V 레지스트리 설정</span><span class="sxs-lookup"><span data-stu-id="aca99-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="aca99-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-190">2847017</span><span class="sxs-lookup"><span data-stu-id="aca99-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-191">Internet Explorer에서 복제 한 UE-V 설정</span><span class="sxs-lookup"><span data-stu-id="aca99-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="aca99-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-193">2930271</span><span class="sxs-lookup"><span data-stu-id="aca99-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-194">Microsoft UE-V에서 로밍 Outlook 서명의 제한 사항 이해</span><span class="sxs-lookup"><span data-stu-id="aca99-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="aca99-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-196">2769631</span><span class="sxs-lookup"><span data-stu-id="aca99-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-197">손상 된 UE-V 설치를 복구 하는 방법</span><span class="sxs-lookup"><span data-stu-id="aca99-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="aca99-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-199">2850989</span><span class="sxs-lookup"><span data-stu-id="aca99-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-200">Microsoft UE-V를 사용 하 여 MAPI 프로필을 마이그레이션하는 기능은 지원 되지 않음</span><span class="sxs-lookup"><span data-stu-id="aca99-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="aca99-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-202">2769586</span><span class="sxs-lookup"><span data-stu-id="aca99-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-203">UE-V가 빈 폴더 및 레지스트리 키를 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="aca99-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-205">2782997</span><span class="sxs-lookup"><span data-stu-id="aca99-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-206">Microsoft UE-V (User Experience Virtualization)에서 디버그 로깅을 사용 하도록 설정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="aca99-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="aca99-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-208">2769570</span><span class="sxs-lookup"><span data-stu-id="aca99-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-209">UE-V는 RDS 또는 VDI 세션에서 테마를 업데이트 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca99-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="aca99-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-211">2901856</span><span class="sxs-lookup"><span data-stu-id="aca99-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-212">UE-V를 사용 하는 컴퓨터에서 강제로 다시 시작 하면 응용 프로그램 설정이 동기화 되지 않음</span><span class="sxs-lookup"><span data-stu-id="aca99-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="aca99-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-214">2850582</span><span class="sxs-lookup"><span data-stu-id="aca99-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-215">Microsoft 사용자 환경 가상화를 사용 하는 방법 앱-V 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="aca99-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="aca99-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aca99-217">3041879</span><span class="sxs-lookup"><span data-stu-id="aca99-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-218">Microsoft 사용자 환경 가상화에 대 한 최신 파일 버전</span><span class="sxs-lookup"><span data-stu-id="aca99-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="aca99-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aca99-220">2843592</span><span class="sxs-lookup"><span data-stu-id="aca99-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="aca99-221">사용자 환경 가상화 및 고가용성에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="aca99-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="aca99-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="aca99-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





