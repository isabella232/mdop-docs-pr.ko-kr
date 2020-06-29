---
title: App-V 5.0의 새로운 기능
description: App-V 5.0의 새로운 기능
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813220"
---
# <span data-ttu-id="d8b2c-103">App-V 5.0의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="d8b2c-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="d8b2c-104">이 섹션은 app-v에 대해 잘 알고 있고 App-v 5.0에서 변경 된 내용을 알고 싶은 사용자를 위한 것입니다. App-v에 익숙하지 않은 경우 앱-v [5.0에 대 한 읽기 계획](planning-for-app-v-50-rc.md)부터 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="d8b2c-105">표준 기능 변경</span><span class="sxs-lookup"><span data-stu-id="d8b2c-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="d8b2c-106">다음 섹션에는 앱-V 5.0의 표준 기능 변경 사항에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="d8b2c-107">지원 되는 운영 체제 변경</span><span class="sxs-lookup"><span data-stu-id="d8b2c-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="d8b2c-108">자세한 내용은 [앱-V 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="d8b2c-109">Sequencer 변경</span><span class="sxs-lookup"><span data-stu-id="d8b2c-109">Changes to the sequencer</span></span>


<span data-ttu-id="d8b2c-110">다음 섹션에는 App-v 5.0 sequencer의 변경 사항에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="d8b2c-111">시퀀서에 대 한 특정 변경</span><span class="sxs-lookup"><span data-stu-id="d8b2c-111">Specific change to the sequencer</span></span>

<span data-ttu-id="d8b2c-112">다음 표에서는 App-v 5.0 sequencer로 변경 된 사항에 대 한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d8b2c-113">Sequencer 기능</span><span class="sxs-lookup"><span data-stu-id="d8b2c-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="d8b2c-114">App-v 5.0 Sequencer 기능</span><span class="sxs-lookup"><span data-stu-id="d8b2c-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-115">다시 부팅 처리</span><span class="sxs-lookup"><span data-stu-id="d8b2c-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-116">응용 프로그램이 다시 시작에 대 한 메시지를 표시 하는 경우 응용 프로그램에서 sequencer를 실행 하는 컴퓨터를 다시 시작 하도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="d8b2c-117">Sequencer를 실행 하는 컴퓨터는 다시 시작 되 고 sequencer는 모니터링 모드로 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-118">가상 응용 프로그램 디렉터리 지정</span><span class="sxs-lookup"><span data-stu-id="d8b2c-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-119">가상 응용 프로그램 디렉터리는 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="d8b2c-120">최상의 결과를 위해서는 응용 프로그램 설치 관리자의 설치 디렉터리와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="d8b2c-121">이로 인해 성능이 최적화 되 고 응용 프로그램 호환성이 향상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-122">편집 바로 가기/FTAs</span><span class="sxs-lookup"><span data-stu-id="d8b2c-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-123"><strong> </strong> 시퀀싱 마법사를 완료 한 후에 고급 편집 페이지의 바로 가기/FTA 페이지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-124">변경 기록 탭</span><span class="sxs-lookup"><span data-stu-id="d8b2c-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-125">앱-V 5.0에 대 한 변경 내용 탭이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-126">OSD탭</span><span class="sxs-lookup"><span data-stu-id="d8b2c-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-127">OSD 탭이 App-v 5.0 용으로 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-128">가상 서비스 탭</span><span class="sxs-lookup"><span data-stu-id="d8b2c-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-129">앱-V 5.0에 대 한 가상 서비스 탭이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-130">파일/가상 파일 시스템 탭</span><span class="sxs-lookup"><span data-stu-id="d8b2c-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-131">이러한 탭을 결합 하 여 패키지 파일을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-132">배포 탭</span><span class="sxs-lookup"><span data-stu-id="d8b2c-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-133">패키지에서 서버 URL을 구성 하는 옵션이 더 이상 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="d8b2c-134">배포 구성 또는 관리 서버를 사용 하 여 지금이를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-135">패키지 변환기 도구</span><span class="sxs-lookup"><span data-stu-id="d8b2c-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-136">이제 PowerShell을 사용 하 여 이전 버전에서 만든 패키지를 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-137">추가 기능/미들웨어</span><span class="sxs-lookup"><span data-stu-id="d8b2c-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-138">추가 기능 또는 미들웨어 응용 프로그램을 시퀀싱 하는 경우 부모 패키지를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="d8b2c-139">앱-V 5.0의 연결 그룹을 사용 하 여 추가 기능 및 미들웨어 패키지를 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-140">파일 출력</span><span class="sxs-lookup"><span data-stu-id="d8b2c-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-141">앱-V 5.0, Windows Installer (.msi), appv, 배포 구성, 사용자 구성 및 Report.XML으로 생성 되는 파일은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-142">압축/보안 설명자/MSI 패키지</span><span class="sxs-lookup"><span data-stu-id="d8b2c-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-143">Windows Installer (.msi) 파일의 압축 및 만들기는 모든 패키지에 대해 자동 이므로 더 이상 보안 설명자를 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-144">도구/옵션</span><span class="sxs-lookup"><span data-stu-id="d8b2c-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-145">진단 창이 제거 되었으며 다른 몇 가지 설정도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-146">설치 드라이브</span><span class="sxs-lookup"><span data-stu-id="d8b2c-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-147">설치 드라이브는 응용 프로그램을 설치할 때 더 이상 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2c-148">OOS 스트리밍</span><span class="sxs-lookup"><span data-stu-id="d8b2c-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2c-149">스트림 최적화가 수행 되지 않으면 앱이 시작 될 때까지 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 요청 하는 경우 패키지에서 스트림 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2c-150">Q: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="d8b2c-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="d8b2c-151">App-v 5.0는 기본 파일 시스템을 사용 하며 더 이상 Q:. 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d8b2c-152">시퀀싱 오류 감지</span><span class="sxs-lookup"><span data-stu-id="d8b2c-152">Sequencing error detection</span></span>


<span data-ttu-id="d8b2c-153">App-v 5.0 시퀀서는 시퀀싱 중에 일반적인 시퀀싱 문제를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="d8b2c-154">시퀀싱 마법사의 끝에 있는 **설치 보고서** 페이지에는 문제의 심각도에 따라 **오류**, **경고**및 **정보** 로 분류 된 진단 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="d8b2c-155">이벤트에 대 한 자세한 정보를 표시 하려면 보고서에서 검토 하려는 항목을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="d8b2c-156">시퀀싱 문제는 물론 문제를 해결 하는 방법에 대 한 제안이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="d8b2c-157">패키지 만들기를 완료 하면 시스템 준비 보고서 및 설치 보고서의 정보가 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="d8b2c-158">다음 목록에는 보고서에서 사용할 수 있는 문제의 유형이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="d8b2c-159">제외 된 파일.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-159">Excluded files.</span></span>

-   <span data-ttu-id="d8b2c-160">드라이버 정보.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-160">Driver information.</span></span>

-   <span data-ttu-id="d8b2c-161">COM + 시스템 차이점.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-161">COM+ system differences.</span></span>

-   <span data-ttu-id="d8b2c-162">나란히 (SxS) 충돌</span><span class="sxs-lookup"><span data-stu-id="d8b2c-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="d8b2c-163">셸 확장.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-163">Shell Extensions.</span></span>

-   <span data-ttu-id="d8b2c-164">지원 되지 않는 서비스에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="d8b2c-165">DCOM-IN.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-165">DCOM.</span></span>

## <span data-ttu-id="d8b2c-166">연결 그룹</span><span class="sxs-lookup"><span data-stu-id="d8b2c-166">Connection Groups</span></span>


<span data-ttu-id="d8b2c-167">이전에 **동적 도구 모음 컴퍼지션** 으로 알려진 app-v 기능을 이제 app-v 5.0의 **연결 그룹** 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="d8b2c-168">연결 그룹 사용에 대 한 자세한 내용은 [연결 그룹 관리](managing-connection-groups.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="d8b2c-169">라이선스 및 계량 기능</span><span class="sxs-lookup"><span data-stu-id="d8b2c-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="d8b2c-170">Application 및 라이선스 기능은 App-v 5.0에서 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="d8b2c-171">사용자 환경의 실제 라이선스 위치는 관련 라이선스 조건에서 부여한 특정 소프트웨어 타이틀 라이선스 및 사용 권한에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="d8b2c-172">파일 및 응용 프로그램 캐시</span><span class="sxs-lookup"><span data-stu-id="d8b2c-172">File and Application Cache</span></span>


<span data-ttu-id="d8b2c-173">App-v 5.0에서 사용할 수 있는 파일 또는 응용 프로그램 캐시가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b2c-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="d8b2c-174">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d8b2c-174">Related topics</span></span>


[<span data-ttu-id="d8b2c-175">App-V 5.0 정보</span><span class="sxs-lookup"><span data-stu-id="d8b2c-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





