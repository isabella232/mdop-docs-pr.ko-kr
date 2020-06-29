---
title: 응용 프로그램 게시 및 클라이언트 상호 작용
description: 응용 프로그램 게시 및 클라이언트 상호 작용
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814737"
---
# <span data-ttu-id="c2456-103">응용 프로그램 게시 및 클라이언트 상호 작용</span><span class="sxs-lookup"><span data-stu-id="c2456-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="c2456-104">이 문서에서는 일반적인 App-v 클라이언트 작업 및 로컬 운영 체제와의 통합에 대 한 기술 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="c2456-105">Sequencer에서 만든 앱-V 패키지 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="c2456-106">Appv 파일에는 무엇이 있나요?</span><span class="sxs-lookup"><span data-stu-id="c2456-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="c2456-107">App-v 클라이언트 데이터 저장소 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="c2456-108">패키지 레지스트리</span><span class="sxs-lookup"><span data-stu-id="c2456-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="c2456-109">앱-V 패키지 저장소 동작</span><span class="sxs-lookup"><span data-stu-id="c2456-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="c2456-110">로밍 레지스트리 및 데이터</span><span class="sxs-lookup"><span data-stu-id="c2456-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="c2456-111">앱-V 클라이언트 응용 프로그램 수명 주기 관리</span><span class="sxs-lookup"><span data-stu-id="c2456-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="c2456-112">앱-V 패키지의 통합</span><span class="sxs-lookup"><span data-stu-id="c2456-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="c2456-113">동적 구성 처리</span><span class="sxs-lookup"><span data-stu-id="c2456-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="c2456-114">Side-by-side 어셈블리</span><span class="sxs-lookup"><span data-stu-id="c2456-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="c2456-115">클라이언트 로깅</span><span class="sxs-lookup"><span data-stu-id="c2456-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="c2456-116">참조에 대 한 자세한 내용은 [Microsoft app-v (Application Virtualization) 설명서 리소스 다운로드 페이지](https://www.microsoft.com/download/details.aspx?id=27760)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="c2456-117">Sequencer에서 만든 앱-V 패키지 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="c2456-118">시퀀서는 App-v 패키지를 만들고 가상화 된 응용 프로그램을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="c2456-119">시퀀싱 프로세스는 다음 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-120">File</span><span class="sxs-lookup"><span data-stu-id="c2456-120">File</span></span></th>
<th align="left"><span data-ttu-id="c2456-121">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-122">appv</span><span class="sxs-lookup"><span data-stu-id="c2456-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-123">시퀀싱 프로세스의 캡처한 자산과 상태 정보를 포함 하는 기본 패키지 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="c2456-124">전달 시 컴퓨터와 특정 사용자에 게 다시 적용할 수 있는 토큰화 된 형식의 패키지 파일, 게시 정보 및 레지스트리 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c2456-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-125">. MSI</span><span class="sxs-lookup"><span data-stu-id="c2456-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-126">수동으로 또는 타사 배포 플랫폼을 사용 하 여 appv 파일을 배포 하는 데 사용할 수 있는 실행 가능 배포 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="c2456-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-128">App-v 클라이언트를 실행 하는 컴퓨터의 모든 사용자에 게 전역으로 배포 되는 패키지의 모든 응용 프로그램에 대 한 기본 게시 매개 변수를 사용자 지정 하는 데 사용 되는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="c2456-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-130">App-v 클라이언트를 실행 하는 컴퓨터에서 특정 사용자에 게 배포 되는 패키지의 모든 응용 프로그램에 대 한 게시 매개 변수를 사용자 지정 하는 데 사용 되는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-132">생략 된 드라이버, 파일, 레지스트리 위치를 포함 하 여 시퀀싱 프로세스에서 발생 하는 메시지에 대 한 요약입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-133">.CAB</span><span class="sxs-lookup"><span data-stu-id="c2456-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="c2456-134">선택 사항: </em> 이전에 시퀀싱 된 가상 응용 프로그램 패키지를 자동으로 다시 작성 하는 데 사용 되는 패키지 가속기 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-135">. appvt</span><span class="sxs-lookup"><span data-stu-id="c2456-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="c2456-136">선택 사항: </em> 일반적으로 재사용 되는 sequencer 설정을 유지 하는 데 사용 되는 sequencer 템플릿 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2456-137">시퀀싱에 대 한 자세한 내용은 [응용 프로그램 가상화 5.0 시퀀싱 가이드](https://www.microsoft.com/download/details.aspx?id=27760)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-137">For information about sequencing, see [Application Virtualization 5.0 Sequencing Guide](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="c2456-138">Appv 파일에는 무엇이 있나요?</span><span class="sxs-lookup"><span data-stu-id="c2456-138">What’s in the appv file?</span></span>


<span data-ttu-id="c2456-139">Appv 파일은 XML 및 XML이 아닌 파일을 단일 엔터티에 함께 저장 하는 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="c2456-140">이 파일은 OPC 형식을 사용 하 여 작성 됩니다 (기본적으로 제공 되는 패키징 규칙) 표준에 기반을 둔 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="c2456-141">Appv 파일 콘텐츠를 보려면 패키지 복사본을 만든 다음 복사 된 파일의 이름을 ZIP 확장명으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="c2456-142">Appv 파일에는 가상 응용 프로그램을 만들고 게시할 때 사용 되는 다음 폴더와 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-143">이름</span><span class="sxs-lookup"><span data-stu-id="c2456-143">Name</span></span></th>
<th align="left"><span data-ttu-id="c2456-144">유형</span><span class="sxs-lookup"><span data-stu-id="c2456-144">Type</span></span></th>
<th align="left"><span data-ttu-id="c2456-145">Description</span><span class="sxs-lookup"><span data-stu-id="c2456-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-146">루트</span><span class="sxs-lookup"><span data-stu-id="c2456-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-147">파일 폴더</span><span class="sxs-lookup"><span data-stu-id="c2456-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-148">시퀀싱 하는 동안 캡처한 가상화 된 응용 프로그램의 파일 시스템을 포함 하는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-149">[Content_Types]. xml</span><span class="sxs-lookup"><span data-stu-id="c2456-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-150">XML 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-151">Appv 파일의 핵심 콘텐츠 형식 (예: DLL, EXE, BIN)의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-153">XML 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-154">App-v 패키지에서 파일의 위치 및 유효성 검사를 가능 하 게 하는 File, Block 및 BlockMap 요소를 사용 하는 appv 파일의 레이아웃입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-156">XML 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-157">패키지를 추가, 게시 및 실행 하는 데 필요한 정보를 포함 하는 패키지에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="c2456-158">확장명 점 (파일 형식 연결 및 바로 가기)과 패키지와 연결 된 이름 및 Guid가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-160">XML 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-161">특성 (예: 디렉터리, 파일, 불투명 한 디렉터리, 빈 디렉터리 및 긴 이름과 짧은 이름)을 포함 하 여 시퀀싱 하는 동안 캡처한 파일의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-163">XML 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-164">시퀀싱 컴퓨터 (운영 체제 버전, Internet Explorer 버전, .Net Framework 버전) 및 프로세스 (업그레이드, 패키지 버전)에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-165">레지스트리 .dat</span><span class="sxs-lookup"><span data-stu-id="c2456-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-166">DAT 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-167">패키지에 대 한 시퀀싱 프로세스 중에 캡처한 레지스트리 키 및 값</span><span class="sxs-lookup"><span data-stu-id="c2456-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-169">XML 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-170">기본 및 게시 기능 블록에 대 한 파일 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="c2456-171">게시 기능 블록에는 패키지를 게시 하는 데 필요한 .ICO 파일 및 파일의 필수 부분 (EXE 및 DLL)이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="c2456-172">제공 되는 경우 기본 기능 블록에는 시퀀싱 프로세스 중에 스트리밍을 위해 최적화 된 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="c2456-173">App-v 클라이언트 데이터 저장소 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-173">App-V client data storage locations</span></span>


<span data-ttu-id="c2456-174">App-v 클라이언트는 가상 응용 프로그램이 제대로 실행 되 고 로컬에 설치 된 응용 프로그램 처럼 작동 하도록 하는 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="c2456-175">가상 응용 프로그램을 열고 실행 하는 프로세스는 응용 프로그램에 사용자가 기대 하는 기존 응용 프로그램의 필수 구성 요소가 있는지 확인 하기 위해 가상 파일 시스템 및 레지스트리의 매핑을 필요로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="c2456-176">이 섹션에서는 가상 응용 프로그램을 실행 하는 데 필요한 자산에 대해 설명 하 고 App-v에서 자산을 저장 하는 위치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-177">이름</span><span class="sxs-lookup"><span data-stu-id="c2456-177">Name</span></span></th>
<th align="left"><span data-ttu-id="c2456-178">위치</span><span class="sxs-lookup"><span data-stu-id="c2456-178">Location</span></span></th>
<th align="left"><span data-ttu-id="c2456-179">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-180">패키지 저장소</span><span class="sxs-lookup"><span data-stu-id="c2456-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="c2456-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-182">읽기 전용 패키지 파일의 기본 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-183">컴퓨터 카탈로그</span><span class="sxs-lookup"><span data-stu-id="c2456-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="c2456-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-185">컴퓨터 단위 구성 문서 포함</span><span class="sxs-lookup"><span data-stu-id="c2456-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-186">사용자 카탈로그</span><span class="sxs-lookup"><span data-stu-id="c2456-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="c2456-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-188">사용자별 구성 문서 포함</span><span class="sxs-lookup"><span data-stu-id="c2456-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-189">바로 가기 백업</span><span class="sxs-lookup"><span data-stu-id="c2456-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="c2456-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-191">패키지 게시 취소에서 복원을 가능 하 게 하는 이전 통합 지점을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-192">쓰기 시 복사 (COW) 로밍</span><span class="sxs-lookup"><span data-stu-id="c2456-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="c2456-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-194">패키지 수정에 대 한 쓰기 가능한 로밍 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-195">COW (기록 시 복사) 로컬</span><span class="sxs-lookup"><span data-stu-id="c2456-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="c2456-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-197">패키지 수정에 대해 쓰기 가능한 비 로밍 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-198">컴퓨터 레지스트리</span><span class="sxs-lookup"><span data-stu-id="c2456-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="c2456-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-200">컴퓨터 또는 전역적으로 게시 된 패키지 (컴퓨터 하이브)에 대 한 VReg를 포함 하 여 패키지 상태 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-201">사용자 레지스트리</span><span class="sxs-lookup"><span data-stu-id="c2456-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="c2456-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-203">VReg를 포함 하는 사용자 패키지 상태 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-204">사용자 레지스트리 클래스</span><span class="sxs-lookup"><span data-stu-id="c2456-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="c2456-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-206">추가 사용자 패키지 상태 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2456-207">표에 대 한 추가 세부 정보는이 문서의 아래 섹션 및 전체에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="c2456-208">패키지 저장소</span><span class="sxs-lookup"><span data-stu-id="c2456-208">Package store</span></span>

<span data-ttu-id="c2456-209">앱-V 클라이언트는 패키지 저장소에 탑재 된 응용 프로그램 자산을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="c2456-210">이 기본 저장소 위치는 `%ProgramData%\App-V` 사용자가 `Set-AppVClientConfiguration` 로컬 레지스트리 ( `PackageInstallationRoot` 키 아래의 값)를 수정 하는 PowerShell 명령을 사용 하 여 설정 중에 구성할 수 있습니다 `HKLM\Software\Microsoft\AppV\Client\Streaming` .</span><span class="sxs-lookup"><span data-stu-id="c2456-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="c2456-211">패키지 저장소는 클라이언트 운영 체제의 로컬 경로에 위치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="c2456-212">개별 패키지는 패키지 GUID 및 버전 GUID에 대해 이름이 지정 된 하위 디렉터리의 패키지 저장소에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="c2456-213">특정 응용 프로그램 경로의 예:</span><span class="sxs-lookup"><span data-stu-id="c2456-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="c2456-214">설치 하는 동안 패키지 저장소의 기본 위치를 변경 하려면 [App-v 클라이언트를 배포 하는 방법을](how-to-deploy-the-app-v-client-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

### <span data-ttu-id="c2456-215">공유 콘텐츠 저장소</span><span class="sxs-lookup"><span data-stu-id="c2456-215">Shared Content Store</span></span>

<span data-ttu-id="c2456-216">공유 콘텐츠 저장소 모드에서 App-v 클라이언트를 구성 하는 경우 스트림 오류가 발생할 때 디스크에 데이터가 기록 되지 않으며,이는 패키지에 최소 로컬 디스크 공간 (데이터 게시)이 필요 함을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="c2456-217">로컬 저장소를 제한할 수 있는 VDI 환경에서는 디스크 공간을 덜 사용 하는 것이 좋으며, 고성능 네트워크 위치 (SAN 등)에서 응용 프로그램을 스트리밍하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="c2456-218">공유 콘텐츠 저장소 모드에 대 한 자세한 내용은을 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="c2456-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="c2456-219">**참고**  컴퓨터 및 패키지 저장소는 App-v 클라이언트에 대 한 공유 콘텐츠 저장소 구성을 사용 하 고 있는 경우에도 로컬 드라이브에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="c2456-220">패키지 카탈로그</span><span class="sxs-lookup"><span data-stu-id="c2456-220">Package catalogs</span></span>

<span data-ttu-id="c2456-221">App-v 클라이언트는 다음 두 가지 파일 기반 위치를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="c2456-222">카탈로그 (사용자 및 컴퓨터).</span><span class="sxs-lookup"><span data-stu-id="c2456-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="c2456-223">**레지스트리 위치** -패키지가 게시 대상으로 지정 되는 방식에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="c2456-224">컴퓨터에 대 한 카탈로그 (데이터 저장소)와 각 개별 사용자에 대 한 카탈로그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="c2456-225">컴퓨터 카탈로그에는 모든 사용자 또는 모든 사용자에 게 적용 되는 전역 정보가 저장 되며, 사용자 카탈로그에는 특정 사용자에 게 적용 되는 정보가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="c2456-226">Catalog는 동적 구성 및 매니페스트 파일의 컬렉션입니다. 파일 및 레지스트리의 패키지 버전에 대 한 불연속 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="c2456-227">컴퓨터 카탈로그</span><span class="sxs-lookup"><span data-stu-id="c2456-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-228">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-229">패키지를 추가 하 고 게시할 때 컴퓨터에서 사용자가 사용할 수 있는 패키지 문서를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="c2456-230">그러나 게시 시 패키지가 "global" 이면 모든 사용자가 통합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="c2456-231">패키지가 전역이 아닌 경우에는 특정 사용자에 대해서만 통합이 게시 되지만, 클라이언트 컴퓨터의 모든 사용자에 게 수정 및 표시 되는 전역 리소스가 남아 있습니다 (예: 패키지 디렉터리는 공유 디스크 위치에 있음).</span><span class="sxs-lookup"><span data-stu-id="c2456-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="c2456-232">컴퓨터의 사용자가 패키지를 사용할 수 있는 경우 (전역 또는 비전역) 매니페스트는 컴퓨터 카탈로그에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="c2456-233">패키지가 전역으로 게시 되 면 컴퓨터 카탈로그에 저장 된 동적 구성 파일이 있는 것입니다. 따라서 패키지가 전역 인지 여부는 컴퓨터 카탈로그에 UserDeploymentConfiguration file (정책 파일)이 있는지 여부에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-234">기본 저장소 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="c2456-235">이 위치는 패키지 저장소 위치와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="c2456-236">패키지 저장소는 패키지 파일의 골든 또는 초기 복사본입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-237">컴퓨터 카탈로그의 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="c2456-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="c2456-240">UserManifest.xml (전역적으로 게시 된 패키지)</span><span class="sxs-lookup"><span data-stu-id="c2456-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="c2456-241">UserDeploymentConfiguration.xml (전역적으로 게시 된 패키지)</span><span class="sxs-lookup"><span data-stu-id="c2456-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-242">추가 컴퓨터 카탈로그 위치 (패키지가 연결 그룹의 일부인 경우 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="c2456-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-243">다음 위치는 위에서 설명한 특정 패키지 위치에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-244">패키지가 연결 그룹의 일부인 경우 컴퓨터 카탈로그의 추가 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="c2456-246">UserPackageGroupDescriptor.xml (전역적으로 게시 된 연결 그룹)</span><span class="sxs-lookup"><span data-stu-id="c2456-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2456-247">사용자 카탈로그</span><span class="sxs-lookup"><span data-stu-id="c2456-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-248">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-249">게시 프로세스 중에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-249">Created during the publishing process.</span></span> <span data-ttu-id="c2456-250">패키지를 게시 하는 데 사용 되는 정보를 포함 하며 패키지를 특정 사용자에 게 프로 비전 하는 데 사용 되기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="c2456-251">로밍 위치에서 만들어지고 사용자 관련 게시 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="c2456-252">사용자에 대 한 패키지를 게시 하면 정책 파일이 사용자 카탈로그에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="c2456-253">이와 동시에 매니페스트의 복사본도 사용자 카탈로그에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="c2456-254">사용자에 대 한 패키지 자격 자격이 제거 되 면 관련 패키지 파일이 사용자 카탈로그에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="c2456-255">사용자 카탈로그를 보면 관리자가 동적 구성 파일의 존재 여부를 볼 수 있으며,이는 패키지가 해당 사용자에 게 부여 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="c2456-256">로밍 사용자의 경우 사용자 카탈로그는 로밍 또는 공유 위치에 있어야 기본적으로 대상 사용자의 레거시 App-v 동작을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="c2456-257">자격 및 정책은 컴퓨터가 아닌 사용자에 연결 되므로 프로 비전 된 사용자와 로밍 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-258">기본 저장소 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-259">사용자 카탈로그의 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="c2456-261">DynamicConfiguration.xml 또는 UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-262">추가 사용자 카탈로그 위치 (패키지가 연결 그룹의 일부인 경우 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="c2456-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-263">다음 위치는 위에서 설명한 특정 패키지 위치에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-264">패키지가 연결 그룹의 일부인 경우 컴퓨터 카탈로그의 추가 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2456-265">바로 가기 백업</span><span class="sxs-lookup"><span data-stu-id="c2456-265">Shortcut backups</span></span>

<span data-ttu-id="c2456-266">게시 프로세스 중에 App-v 클라이언트가이 백업에 대 한 바로 가기 및 통합 지점을 백업 하면 `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` 패키지가 게시 취소 될 때 이러한 통합 지점을 이전 버전으로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="c2456-267">파일 쓰기 시 복사</span><span class="sxs-lookup"><span data-stu-id="c2456-267">Copy on Write files</span></span>

<span data-ttu-id="c2456-268">패키지 저장소에는 게시 서버에서 스트리밍된 패키지 파일의 초기 복사본이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="c2456-269">App-v 응용 프로그램이 정상적으로 작동 하는 동안 사용자 또는 서비스에서 파일을 변경 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="c2456-270">이러한 변경 사항은 해당 응용 프로그램 복구의 기능을 보존 하기 위해 패키지 저장소에서 변경 되지 않으며,이는 이러한 변경을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="c2456-271">이러한 위치 (COW)는 쓰기 시 복사 (이 하)는 로밍 위치나 비 로밍 위치를 모두 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="c2456-272">수정 내용이 저장 되는 위치는 응용 프로그램이 네이티브 환경에서 변경 내용을 작성 하도록 프로그래밍 된 위치에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="c2456-273">COW 로밍</span><span class="sxs-lookup"><span data-stu-id="c2456-273">COW roaming</span></span>

<span data-ttu-id="c2456-274">위에서 설명한 COW 로밍 위치는 일반적인% AppData% location 또는 \\Users\\{username}\\AppData\\Roaming 위치를 대상으로 하는 파일 및 디렉터리에 대 한 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="c2456-275">이러한 디렉터리와 파일은 운영 체제 설정에 따라 roamed.</span><span class="sxs-lookup"><span data-stu-id="c2456-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="c2456-276">COW 지역</span><span class="sxs-lookup"><span data-stu-id="c2456-276">COW local</span></span>

<span data-ttu-id="c2456-277">COW 로컬 위치는 로밍 위치와 비슷하지만, 로밍 지원이 구성 된 경우에도 디렉터리 및 파일은 다른 컴퓨터에 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="c2456-278">위에서 설명한 COW 로컬 위치는 표준 창에 적용 되는 변경 내용을 저장 하며% AppData% 위치는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="c2456-279">나열 된 디렉터리는 다를 수 있지만 일반적인 Windows 위치에는 두 위치 (예: 일반 AppData 및 일반 Appdatdatas)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="c2456-280">해당 **S** 는 가상 서비스가 로그온 한 사용자의 다른 관리자 권한으로 변경을 요청할 때 제한 된 위치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="c2456-281">비**S** 위치에는 사용자 기반 변경 내용이 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="c2456-282">패키지 레지스트리</span><span class="sxs-lookup"><span data-stu-id="c2456-282">Package registry</span></span>


<span data-ttu-id="c2456-283">응용 프로그램이 패키지 레지스트리 데이터에 액세스할 수 있으려면 App-v 클라이언트에서 패키지 레지스트리 데이터를 응용 프로그램에서 사용할 수 있도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="c2456-284">App-v 클라이언트는 모든 레지스트리 데이터에 대 한 백업 저장소로 실제 레지스트리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="c2456-285">새 패키지가 App-v 클라이언트에 추가 되 면 레지스트리의 복사본을 만듭니다. DAT 파일이 생성 됩니다 `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="c2456-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="c2456-286">파일 이름은이 (가) 포함 된 버전 GUID입니다. DAT 확장명.</span><span class="sxs-lookup"><span data-stu-id="c2456-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="c2456-287">이 복사본이 만들어지는 이유는 패키지의 실제 하이브 파일을 사용 하지 않도록 하 여 나중에 패키지를 제거 하는 것을 방지 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c2456-288">패키지 저장소의 레지스트리 .dat</span><span class="sxs-lookup"><span data-stu-id="c2456-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c2456-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid} .dat</span><span class="sxs-lookup"><span data-stu-id="c2456-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2456-290">패키지의 첫 번째 응용 프로그램이 클라이언트에서 시작 되 면 클라이언트는 하이브 파일의 내용을 단계적으로 진행 하거나 복사 하 여 대체 위치에 패키지 레지스트리 데이터를 다시 만듭니다 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="c2456-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="c2456-291">준비 된 레지스트리 데이터에는 서로 다른 두 가지 유형의 컴퓨터 데이터와 사용자 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="c2456-292">컴퓨터 데이터는 컴퓨터의 모든 사용자 간에 공유 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="c2456-293">사용자 데이터는 사용자에 대해 userspecific 위치에 대해 준비 됩니다 `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="c2456-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="c2456-294">컴퓨터 데이터는 패키지 제거 시간에 궁극적으로 제거 되며 사용자 데이터는 사용자의 게시 취소 작업에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="c2456-295">패키지 레지스트리 준비 및 연결 그룹 레지스트리 준비</span><span class="sxs-lookup"><span data-stu-id="c2456-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="c2456-296">연결 그룹이 있는 경우 레지스트리를 준비 하는 이전 프로세스는 true를 유지 하지만, 하이브 파일을 하나 이상 처리 하는 대신</span><span class="sxs-lookup"><span data-stu-id="c2456-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="c2456-297">파일은 연결 그룹 XML에 표시 되는 순서 대로 처리 되며 첫 번째 작성자가 충돌을 발생 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="c2456-298">준비 된 레지스트리는 단일 패키지 케이스와 동일한 방식으로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="c2456-299">사용 하지 않도록 설정 될 때까지 연결 그룹에 대해 준비 된 사용자 레지스트리 데이터가 유지 됩니다. 연결 그룹 제거 시 준비 된 컴퓨터 레지스트리 데이터가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="c2456-300">가상 레지스트리</span><span class="sxs-lookup"><span data-stu-id="c2456-300">Virtual registry</span></span>

<span data-ttu-id="c2456-301">가상 레지스트리 (VREG)의 용도는 패키지 레지스트리와 기본 레지스트리를 통합 하 여 응용 프로그램에 병합 된 단일 보기를 제공 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="c2456-302">또한 가상 프로세스의 컨텍스트에서 레지스트리를 변경한 내용이 별도의 COW 위치에 적용 되는 COW (write on copy) 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="c2456-303">즉, VREG는 레지스트리 COW-package-네이티브에서 채워진 위치를 기반으로 하는 단일 보기로 최대 세 개의 개별 레지스트리 위치를 결합 해야 합니다 &gt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="c2456-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="c2456-304">레지스트리 데이터에 대 한 요청이 이루어지면 요청 된 데이터를 찾을 때까지 순서 대로 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="c2456-305">COW 위치에 저장 된 값이 있는 경우 다른 위치로 진행 되지 않지만 COW 위치에 데이터가 없는 경우에는 해당 데이터를 찾을 때까지 원래 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="c2456-306">레지스트리 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-306">Registry locations</span></span>

<span data-ttu-id="c2456-307">두 개의 패키지 레지스트리 위치와 두 개의 연결 그룹 위치가 있는데,이는 패키지가 개별적으로 게시 되었는지 또는 연결 그룹의 일부분에 따라 App-v 클라이언트가 레지스트리 정보를 저장 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="c2456-308">패키지에는 세 가지 COW 위치, 연결 그룹의 경우 세 가지, 즉 VREG에서 만들고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="c2456-309">패키지 및 연결 그룹에 대 한 설정은 공유 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="c2456-310">단일 패키지 VReg:</span><span class="sxs-lookup"><span data-stu-id="c2456-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c2456-311">위치</span><span class="sxs-lookup"><span data-stu-id="c2456-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c2456-312">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c2456-313">COW</span><span class="sxs-lookup"><span data-stu-id="c2456-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-314">기계 Registry\Client\Packages\PkgGUID\REGISTRY (권한 상승 프로세스만 쓰기 가능)</span><span class="sxs-lookup"><span data-stu-id="c2456-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="c2456-315">사용자 로밍 (Registry\Client\Packages\PkgGUID\REGISTRY/수업을 제외한 HKCU에 작성 된 모든 항목</span><span class="sxs-lookup"><span data-stu-id="c2456-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="c2456-316">사용자 레지스트리 Classes\Client\Packages\PkgGUID\REGISTRY (관리자가 아닌 프로세스의 HKCU\Software\Classes 쓰기 및 HKLM)</span><span class="sxs-lookup"><span data-stu-id="c2456-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c2456-317">패키지</span><span class="sxs-lookup"><span data-stu-id="c2456-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-318">기계 Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span><span class="sxs-lookup"><span data-stu-id="c2456-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="c2456-319">사용자 레지스트리 Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span><span class="sxs-lookup"><span data-stu-id="c2456-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c2456-320">원본</span><span class="sxs-lookup"><span data-stu-id="c2456-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-321">기본 응용 프로그램 레지스트리 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="c2456-322">연결 그룹 VReg:</span><span class="sxs-lookup"><span data-stu-id="c2456-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c2456-323">위치</span><span class="sxs-lookup"><span data-stu-id="c2456-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c2456-324">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c2456-325">COW</span><span class="sxs-lookup"><span data-stu-id="c2456-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-326">기계 Registry\Client\PackageGroups\GrpGUID\REGISTRY (권한 상승 프로세스만 쓰기 가능)</span><span class="sxs-lookup"><span data-stu-id="c2456-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="c2456-327">사용자 Registry\Client\PackageGroups\GrpGUID\REGISTRY (\수업을 제외한 HKCU에 기록 된 모든 항목</span><span class="sxs-lookup"><span data-stu-id="c2456-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="c2456-328">사용자 레지스트리 Classes\Client\PackageGroups\GrpGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="c2456-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c2456-329">패키지</span><span class="sxs-lookup"><span data-stu-id="c2456-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-330">기계 Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="c2456-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="c2456-331">사용자 레지스트리 Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="c2456-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c2456-332">원본</span><span class="sxs-lookup"><span data-stu-id="c2456-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c2456-333">기본 응용 프로그램 레지스트리 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="c2456-334">HKLM에는 두 개의 COW 위치가 있습니다. 관리자 권한 및 비관리자 프로세스</span><span class="sxs-lookup"><span data-stu-id="c2456-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="c2456-335">관리자 권한 프로세스는 HKLM의 보안 COW에 HKLM 변경 내용을 항상 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="c2456-336">비 권한 프로세스는 항상 HKCU\\Software\\Classes. 아래의 비보안 COW에 HKLM 변경 내용을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="c2456-337">앱이 HKLM에서 변경 내용을 읽는 경우 관리자 권한 프로세스는 HKLM 아래의 보안 COW 변경 내용을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="c2456-338">두 가지 모두에서 비 권한 읽기는 보안 되지 않은 COW에서 변경한 내용을 먼저 favoring.</span><span class="sxs-lookup"><span data-stu-id="c2456-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="c2456-339">창구 키</span><span class="sxs-lookup"><span data-stu-id="c2456-339">Pass-through keys</span></span>

<span data-ttu-id="c2456-340">관리자는 창구 키를 사용 하 여 패키지 및 COW 위치를 우회 하 여 네이티브 레지스트리 에서만 읽을 수 있도록 특정 키를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="c2456-341">통과 위치는 패키지에 따라 달라 지 며, 키에 대 한 경로를 추가 하 여 구성할 수 있으며, 키의 **PassThroughPaths** 이라고 하는 **REG \ _MULTI \ _SZ** value에 대 한 통과로 처리 되어야 합니다 `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="c2456-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="c2456-342">이 다중 문자열 값 아래에 표시 되는 모든 키 (하위 항목)는 통과로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="c2456-343">다음 위치는 기본적으로 통과 위치로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="c2456-344">HKEY _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="c2456-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="c2456-345">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="c2456-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="c2456-346">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span><span class="sxs-lookup"><span data-stu-id="c2456-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="c2456-347">HKEY _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span><span class="sxs-lookup"><span data-stu-id="c2456-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="c2456-348">HKEY _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span><span class="sxs-lookup"><span data-stu-id="c2456-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="c2456-349">HKEY _CURRENT \ _USER \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet 설정</span><span class="sxs-lookup"><span data-stu-id="c2456-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="c2456-350">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="c2456-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="c2456-351">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="c2456-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="c2456-352">HKEY _CURRENT \ _USER \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="c2456-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="c2456-353">통과 키의 목적은 가상 응용 프로그램이 성공한 작업 또는 통합을 위해 비가상 응용 프로그램에 필요한 VReg의 레지스트리 데이터를 기록 하지 않도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="c2456-354">정책 키를 사용 하면 관리자가 설정한 그룹 정책 기반 설정이 패키지 설정 별로 사용 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="c2456-355">Windows 최신 UI 기반 응용 프로그램과 통합 하려면 AppModel 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="c2456-356">관리에서 기본 통과 키를 수정 하지 않는 것이 좋으며 일부 경우에는 응용 프로그램 동작에 따라 추가 통과 키를 추가 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="c2456-357">앱-V 패키지 저장소 동작</span><span class="sxs-lookup"><span data-stu-id="c2456-357">App-V package store behavior</span></span>


<span data-ttu-id="c2456-358">앱-V 5는 패키지 저장소를 관리 하며,이 위치는 appv 파일에서 확장 된 자산 파일이 저장 되는 장소입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="c2456-359">기본적으로이 위치 는%app Data%\\app-v에 저장 되며, 사용 가능한 디스크 공간에 의해서만 저장소 용량으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="c2456-360">패키지 저장소는 이전 섹션에서 설명한 대로 패키지 및 버전의 Guid를 기준으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="c2456-361">패키지 추가</span><span class="sxs-lookup"><span data-stu-id="c2456-361">Add packages</span></span>

<span data-ttu-id="c2456-362">App-v 패키지는 App-v 클라이언트를 사용 하 여 컴퓨터에 추가 될 때 준비 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="c2456-363">App-v 클라이언트는 주문형 스테이징을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="c2456-364">게시 또는 수동 추가 AppVClientPackage 경우 데이터 구조는 패키지 저장소 (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID})에 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="c2456-365">StreamMap.xml에 정의 된 게시 블록에서 식별 된 패키지 파일은 시스템에 추가 되 고, 시작 시 적절 한 응용 프로그램 자산을 확보 하기 위해 준비 된 최상위 폴더 및 하위 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="c2456-366">패키지 탑재</span><span class="sxs-lookup"><span data-stu-id="c2456-366">Mounting packages</span></span>

<span data-ttu-id="c2456-367">패키지는 PowerShell을 사용 `Mount-AppVClientPackage` 하거나 **APP-V 클라이언트 UI** 를 사용 하 여 패키지를 다운로드 하 여 명시적으로 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="c2456-368">이 작업은 전체 패키지를 패키지 저장소에 완전히 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="c2456-369">스트리밍 패키지</span><span class="sxs-lookup"><span data-stu-id="c2456-369">Streaming packages</span></span>

<span data-ttu-id="c2456-370">스트리밍의 기본 동작을 변경 하도록 App-v 클라이언트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="c2456-371">모든 스트리밍 정책은 다음 레지스트리 키 아래에 저장 됩니다 `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` .</span><span class="sxs-lookup"><span data-stu-id="c2456-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="c2456-372">정책은 PowerShell cmdlet을 사용 하 여 설정 `Set-AppvClientConfiguration` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="c2456-373">스트리밍에 적용 되는 정책은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-374">정책</span><span class="sxs-lookup"><span data-stu-id="c2456-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="c2456-375">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="c2456-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-377">Windows 8에서는 3G 및 셀룰러 네트워크를 통해 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-377">On Windows 8 it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-378">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="c2456-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-379">백그라운드 로드 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="c2456-380">0 </strong> - 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="c2456-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="c2456-381">1 </strong> – 이전에 사용한 패키지만 사용</span><span class="sxs-lookup"><span data-stu-id="c2456-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="c2456-382">2 </strong> – 모든 패키지</span><span class="sxs-lookup"><span data-stu-id="c2456-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-383">Package설치 루트</span><span class="sxs-lookup"><span data-stu-id="c2456-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-384">로컬 컴퓨터에 있는 패키지 저장소의 루트 폴더</span><span class="sxs-lookup"><span data-stu-id="c2456-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="c2456-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-386">패키지를 스트리밍할 위치 루트 재정의</span><span class="sxs-lookup"><span data-stu-id="c2456-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="c2456-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-388">VDI 시나리오에 공유 콘텐츠 저장소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="c2456-389">이러한 설정은 클라이언트에 대 한 스트리밍 앱-V 패키지 자산의 동작에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="c2456-390">기본적으로 App-v는 초기 게시 및 기본 기능 블록을 다운로드 한 후 필요한 자산만 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="c2456-391">스트리밍 패키지에 대해 설명 해야 하는 세 가지 특정 동작이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="c2456-392">백그라운드 스트리밍</span><span class="sxs-lookup"><span data-stu-id="c2456-392">Background Streaming</span></span>

-   <span data-ttu-id="c2456-393">최적화 된 스트리밍</span><span class="sxs-lookup"><span data-stu-id="c2456-393">Optimized Streaming</span></span>

-   <span data-ttu-id="c2456-394">스트림 오류</span><span class="sxs-lookup"><span data-stu-id="c2456-394">Stream Faults</span></span>

### <span data-ttu-id="c2456-395">백그라운드 스트리밍</span><span class="sxs-lookup"><span data-stu-id="c2456-395">Background streaming</span></span>

<span data-ttu-id="c2456-396">PowerShell cmdlet을 `Get-AppvClientConfiguration` 사용 하 여 AutoLoad 설정으로 백그라운드 스트리밍에 대 한 현재 모드를 결정 하 고 Cmdlet Set-AppvClientConfiguration 또는 registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming 키)를 사용 하 여 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="c2456-397">백그라운드 스트리밍은 이전에 사용 하 던 패키지를 다운로드 하도록 Autoload 설정을 설정한 기본 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="c2456-398">기본 설정 (값 = 1)을 기준으로 하는 동작은 응용 프로그램이 실행 된 후 백그라운드에서 App-v 데이터 블록을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="c2456-399">이 설정은 실행 되었는지 여부에 관계 없이 모든 패키지 (값 = 0)에 대해 모두 사용 하거나 사용 하지 않도록 설정할 수 있습니다 (value = 2).</span><span class="sxs-lookup"><span data-stu-id="c2456-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="c2456-400">최적화 된 스트리밍</span><span class="sxs-lookup"><span data-stu-id="c2456-400">Optimized streaming</span></span>

<span data-ttu-id="c2456-401">시퀀싱 하는 동안 기본 기능 블록을 사용 하 여 app-v 패키지를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="c2456-402">이 설정을 사용 하면 시퀀싱 엔지니어가 특정 응용 프로그램 또는 응용 프로그램에 대 한 시작 파일을 모니터링 하 고 패키지의 응용 프로그램을 처음 실행할 때 스트리밍을 위해 App-v 패키지의 데이터 블록을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="c2456-403">스트림 오류</span><span class="sxs-lookup"><span data-stu-id="c2456-403">Stream faults</span></span>

<span data-ttu-id="c2456-404">게시 데이터 및 기본 기능 블록의 초기 스트림 후에 추가 파일에 대 한 요청이 스트림 오류를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="c2456-405">이러한 데이터 블록은 필요한 기준에 따라 패키지 저장소에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="c2456-406">이를 통해 사용자는 패키지의 작은 부분만 다운로드할 수 있으며 일반적으로 패키지를 실행 하 고 일반 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="c2456-407">다른 모든 블록은 사용자가 현재 패키지 저장소에 없는 데이터가 필요한 작업을 시작할 때 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="c2456-408">App-v 패키지 스트리밍에 대 한 자세한 내용은 다음을 방문 <https://go.microsoft.com/fwlink/?LinkId=392770> 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="c2456-409">스트리밍 최적화의 순서는:에서 사용할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="c2456-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="c2456-410">패키지 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c2456-410">Package upgrades</span></span>

<span data-ttu-id="c2456-411">앱-V 패키지는 응용 프로그램의 수명 주기 전체에서 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="c2456-412">앱-V 패키지 업그레이드는 각 버전이 자체 PackageRoot 위치에 만들어지기 때문에 패키지 게시 작업과 유사 `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="c2456-413">업그레이드 작업은 동일한 패키지의 다른 버전에서 동일한 및 스트리밍된 파일에 대 한 하드 링크를 만들어 최적화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="c2456-414">패키지 제거</span><span class="sxs-lookup"><span data-stu-id="c2456-414">Package removal</span></span>

<span data-ttu-id="c2456-415">패키지가 제거 되는 경우 App-v 클라이언트의 동작은 제거에 사용 되는 방법에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="c2456-416">App-v full 인프라를 사용 하 여 응용 프로그램의 게시를 취소 하면 사용자 카탈로그 파일 (전역적으로 게시 된 응용 프로그램의 컴퓨터 카탈로그)은 제거 되지만 패키지 저장소 위치와 COW 위치는 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="c2456-417">PowerShell cmdlet을 `Remove-AppVClientPackge` 사용 하 여 App-v 패키지를 제거 하면 패키지 저장소 위치가 정리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="c2456-418">관리 서버에서 App-v 패키지를 게시 취소 해도 제거 작업이 수행 되지 않는다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="c2456-419">두 작업 모두 패키지 저장소 패키지 파일을 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="c2456-420">로밍 레지스트리 및 데이터</span><span class="sxs-lookup"><span data-stu-id="c2456-420">Roaming registry and data</span></span>


<span data-ttu-id="c2456-421">앱-V 5는 사용 중인 응용 프로그램이 작성 되는 방법에 따라 로밍할 때 가까운 기본 환경을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="c2456-422">기본적으로 App-v는 운영 체제의 로밍 구성을 기반으로 하 여 로밍 위치에 저장 된 AppData를 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="c2456-423">파일 기반 데이터를 저장 하는 다른 위치는 roamed 아닌 위치에 있으므로 컴퓨터에서 로밍 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="c2456-424">로밍 요구 사항 및 사용자 카탈로그 데이터 저장소</span><span class="sxs-lookup"><span data-stu-id="c2456-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="c2456-425">App-v는 사용자 카탈로그의 상태를 나타내는 데이터를 다음 형식으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="c2456-426">%Appdata%\\Microsoft\\AppV\\Client\\Catalog 아래에 있는 파일</span><span class="sxs-lookup"><span data-stu-id="c2456-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="c2456-427">레지스트리 설정</span><span class="sxs-lookup"><span data-stu-id="c2456-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="c2456-428">이러한 파일 및 레지스트리 설정은 사용자의 카탈로그를 나타내므로 둘 다 roamed 이거나 지정 된 사용자에 대해 roamed 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="c2456-429">App-v는 로밍% AppData%를 지원 하지 않지만 사용자 프로필 (레지스트리)을 로밍 하거나 그 반대로는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="c2456-430">**참고**  **AppvClientPackage** cmdlet은 사용자의 app-v 상태가 `HKEY_CURRENT_USER` 누락 되거나% appdata%의 데이터와 일치 하지 않는 패키지의 게시 상태를 복구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="c2456-431">레지스트리 기반 데이터</span><span class="sxs-lookup"><span data-stu-id="c2456-431">Registry-based data</span></span>

<span data-ttu-id="c2456-432">App-v 레지스트리 로밍은 다음 표에 표시 된 것 처럼 두 가지 시나리오가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-433">시나리오</span><span class="sxs-lookup"><span data-stu-id="c2456-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="c2456-434">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-435">표준 사용자로 실행 되는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c2456-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-436">표준 사용자가 app-v 응용 프로그램을 실행 하는 경우 앱-V 응용 프로그램에 대 한 HKLM 및 HKCU가 모두 컴퓨터의 HKCU 하이브에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="c2456-437">이는 서로 다른 두 개의 경로로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="c2456-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="c2456-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="c2456-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="c2456-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="c2456-440">위치는 운영 체제 설정에 따라 로밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-441">권한 상승으로 실행 되는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c2456-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-442">상승을 사용 하 여 응용 프로그램을 실행 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="c2456-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="c2456-443">HKLM 데이터는 로컬 컴퓨터의 HKLM hive에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="c2456-444">HKCU 데이터는 사용자 레지스트리 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="c2456-445">이 시나리오에서는 일반 운영 체제 로밍 구성을 사용 하 여 이러한 설정을 roamed, 결과 레지스트리 키 및 값이 다음 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="c2456-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="c2456-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="c2456-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="c2456-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2456-448">App-v 및 폴더 리디렉션</span><span class="sxs-lookup"><span data-stu-id="c2456-448">App-V and folder redirection</span></span>

<span data-ttu-id="c2456-449">앱-V 5.0 SP2는 로밍 AppData 폴더 (% AppData%)의 폴더 리디렉션을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-449">App-V 5.0SP2 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="c2456-450">가상 환경이 시작 되 면 사용자의 로밍 AppData 디렉터리에서 로밍 AppData 상태가 로컬 캐시에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="c2456-451">반대로, 가상 환경이 종료 되 면 특정 사용자의 로밍 AppData와 연결 된 로컬 캐시가 해당 사용자의 로밍 AppData 디렉터리의 실제 위치로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="c2456-452">일반적인 패키지에는 사용자의 지원 저장소에 여러 위치가 포함 되어 있으며,이 둘 다 AppData\\Local 및 AppData\\Roaming.의 설정에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="c2456-453">이러한 위치는 사용자 프로필에 사용자 당 저장 되는 쓰기 위치의 복사본 이며, 패키지 VFS 디렉터리에 대 한 변경 내용을 저장 하 고 기본 패키지 VFS를 보호 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="c2456-454">다음 표에서는 폴더 리디렉션이 구현 되지 않은 경우 로컬 및 로밍 위치를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-455">패키지의 VFS 디렉터리</span><span class="sxs-lookup"><span data-stu-id="c2456-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="c2456-456">백업 저장소의 매핑된 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="c2456-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-458">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="c2456-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="c2456-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-460">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Systemx86</span><span class="sxs-lookup"><span data-stu-id="c2456-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-461">Windows</span><span class="sxs-lookup"><span data-stu-id="c2456-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-462">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \windows</span><span class="sxs-lookup"><span data-stu-id="c2456-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="c2456-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-464">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="c2456-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-465">AppData</span><span class="sxs-lookup"><span data-stu-id="c2456-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-466">C:\users\jsmith\AppData &lt; 강력한 &gt; 로밍 </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="c2456-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="c2456-467">다음 표에서는 로컬 및 로밍 위치,% AppData%에 대해 폴더 리디렉션이 구현 되었고 위치가 리디렉션 됨 (일반적으로 네트워크 위치)을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-468">패키지의 VFS 디렉터리</span><span class="sxs-lookup"><span data-stu-id="c2456-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="c2456-469">백업 저장소의 매핑된 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="c2456-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-471">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="c2456-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="c2456-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-473">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Systemx86</span><span class="sxs-lookup"><span data-stu-id="c2456-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-474">Windows</span><span class="sxs-lookup"><span data-stu-id="c2456-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-475">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \windows</span><span class="sxs-lookup"><span data-stu-id="c2456-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="c2456-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-477">C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="c2456-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-478">AppData</span><span class="sxs-lookup"><span data-stu-id="c2456-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="c2456-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="c2456-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="c2456-480">현재 App-v 클라이언트 VFS 드라이버는 네트워크 위치에 쓸 수 없으므로 App-v 클라이언트는 폴더 리디렉션이 있는지 검색 하 고, 게시 하는 동안 로컬 드라이브에 데이터를 복사 하 고 가상 환경이 시작 되는 시기를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="c2456-481">사용자가 App-v 응용 프로그램을 닫고 App-v 클라이언트에서 가상 환경을 닫으면 VFS AppData의 로컬 저장소가 네트워크에 다시 복사 되어 프로세스가 반복 되는 추가 컴퓨터로 로밍이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="c2456-482">프로세스의 세부 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="c2456-483">게시 또는 가상 환경 시작 중에 App-v 클라이언트는 AppData 디렉터리의 위치를 감지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="c2456-484">로밍 AppData 경로가 local 또는 .ino AppData\\Roaming 위치가 매핑되면 아무런 작업도 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="c2456-485">로밍 AppData 경로가 local이 아니면 VFS AppData directory가 로컬 AppData 디렉터리로 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="c2456-486">이 프로세스는 App-v 클라이언트 VFS 드라이버에서 지원 하지 않는 비로컬% AppData%의 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="c2456-487">그러나이 새 위치에 저장 된 데이터는 폴더 리디렉션으로 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="c2456-488">응용 프로그램이 실행 되는 동안 모든 변경 내용은 로컬 AppData 위치에 있으며 리디렉션된 위치에 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="c2456-489">이 프로세스의 자세한 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="c2456-490">앱-V 응용 프로그램이 종료 되어 가상 환경을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="c2456-491">로밍 AppData 위치의 로컬 캐시는 압축 되어 ZIP 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="c2456-492">ZIP 패키지 프로세스 끝에 있는 타임 스탬프는 파일의 이름을 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="c2456-493">타임 스탬프는 HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime의 마지막으로 알려진 AppData timestamp로 레지스트리에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="c2456-494">폴더 리디렉션 프로세스가 호출 되어 로밍 AppData 디렉터리에 업로드 된 ZIP 파일을 평가 하 고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="c2456-495">타임 스탬프는 충돌이 있는 경우 "마지막 작성자 승리" 시나리오를 결정 하는 데 사용 되며, 앱이 게시 되거나 가상 환경이 시작 될 때 데이터 다운로드를 최적화 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="c2456-496">폴더 리디렉션은 지원 정책이 적용 되는 다른 모든 클라이언트로부터 데이터를 사용할 수 있게 하 고, AppData\\Roaming 데이터를 클라이언트의 로컬 AppData 위치에 저장 하는 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="c2456-497">세부 프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="c2456-498">사용자가 응용 프로그램을 시작 하 여 가상 환경을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="c2456-499">응용 프로그램의 가상 환경은 가장 최근에 스탬프가 지정 된 ZIP 파일 (있는 경우)을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="c2456-500">마지막으로 알려진 업로드 된 타임 스탬프가 있는 경우 레지스트리가 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="c2456-501">가장 최근의 ZIP 파일은 마지막으로 알려진 로컬 업로드 타임 스탬프가 ZIP 파일의 타임 스탬프 보다 크거나 같은 경우에만 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="c2456-502">마지막으로 알려진 로컬 업로드 타임 스탬프가 로밍 AppData 위치에서 가장 최근의 ZIP 파일 보다 이전인 경우 ZIP 파일은 사용자 프로필의 로컬 임시 디렉터리로 추출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="c2456-503">ZIP 파일이 성공적으로 추출 된 후에는 로밍 AppData 디렉터리의 로컬 캐시 이름이 바뀌고 새 데이터는 위치에 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="c2456-504">이름이 변경 된 디렉터리가 삭제 되 고 응용 프로그램이 가장 최근에 저장 된 로밍 AppData 데이터와 함께 열립니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="c2456-505">이렇게 하면 AppData\\Roaming 위치에 있는 응용 프로그램 설정의 성공적인 로밍이 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="c2456-506">해결 해야 하는 유일한 유일한 조건은 패키지 복구 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="c2456-507">프로세스에 대 한 세부 정보는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-507">The details of the process are:</span></span>

1.  <span data-ttu-id="c2456-508">복구 하는 동안 사용자의 로밍 AppData 디렉터리 경로가 로컬이 아닌 경우 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="c2456-509">로컬이 아닌 로밍 AppData 경로 대상이 예상 되는 로밍 및 로컬 AppData 위치에 다시 생성 됨을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="c2456-510">레지스트리에 저장 된 타임 스탬프가 있으면 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="c2456-511">이 프로세스는 AppData에 대 한 로컬 및 네트워크 위치를 모두 다시 만들고 타임 스탬프의 레지스트리 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="c2456-512">앱-V 클라이언트 응용 프로그램 수명 주기 관리</span><span class="sxs-lookup"><span data-stu-id="c2456-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="c2456-513">App-v 전체 인프라에서 응용 프로그램을 시퀀싱 한 후에는 앱-V 관리 및 게시 서버를 통해 사용자 또는 컴퓨터에 관리 되 고 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="c2456-514">이 섹션에서는 공용 App-v 응용 프로그램 수명 주기 작업 (추가, 게시, 시작, 업그레이드 및 제거) 중에 발생 하는 작업과 App-v 클라이언트 관점에서 변경 되 고 수정 된 파일 및 레지스트리 위치에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="c2456-515">App-v 클라이언트 작업은 App-v 클라이언트를 실행 하는 컴퓨터에서 시작 되는 일련의 PowerShell 명령으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="c2456-516">이 문서에서는 App-v 전체 인프라 솔루션에 대해 중점적으로 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="c2456-517">Configuration Manager 2012에서 앱-V 통합에 대 한 특정 정보는 다음 사이트를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=392773> .</span><span class="sxs-lookup"><span data-stu-id="c2456-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="c2456-518">앱-V 응용 프로그램 수명 주기 작업은 사용자 로그인 (기본값), 컴퓨터 시작 또는 백그라운드 시간 지정 작업으로 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="c2456-519">게시 서버, 새로 고침 간격, 패키지 스크립트 사용 등을 비롯 한 App-v 클라이언트 작업의 설정은 PowerShell 명령을 사용 하 여 클라이언트 설치 또는 설정 후에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="c2456-520">TechNet에서 클라이언트를 배포 하는 방법 섹션을 참조 하세요. [App-v 클라이언트를 배포](how-to-deploy-the-app-v-client-gb18030.md) 하거나 PowerShell을 활용 하는 방법:</span><span class="sxs-lookup"><span data-stu-id="c2456-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="c2456-521">게시 새로 고침</span><span class="sxs-lookup"><span data-stu-id="c2456-521">Publishing refresh</span></span>

<span data-ttu-id="c2456-522">게시 새로 고침 프로세스는 App-v 클라이언트에서 수행 되는 몇 가지 작은 작업으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="c2456-523">App-v는 작업 예약 기술이 아닌 응용 프로그램 가상화 기술 이므로, Windows 작업 스케줄러는 사용자 로그온, 컴퓨터 시작, 예약 된 간격으로 프로세스를 사용 하도록 설정 하는 데 이용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="c2456-524">클라이언트를 올바른 설정으로 대규모 컴퓨터 그룹에 배포 하는 경우 위에 나열 된 설정 중 클라이언트 구성을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="c2456-525">다음 PowerShell cmdlet을 사용 하 여 이러한 클라이언트 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="c2456-526">**추가-AppVPublishingServer:** 앱-V 패키지를 제공 하는 App-v 게시 서버를 사용 하 여 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="c2456-527">**Set-AppVPublishingServer:** App-v 게시 서버에 대 한 현재 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="c2456-528">**Set-AppVClientConfiguration:** App-v 클라이언트에 대 한 currents 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="c2456-529">**동기화-AppVPublishingServer:** 수동으로 앱 V 게시 새로 고침 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="c2456-530">이는 게시 서버를 구성 하는 동안 생성 되는 예약 된 작업에도 이용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="c2456-531">다음 섹션의 초점은 App-v 게시 새로 고침의 각 단계에서 발생 하는 작업을 자세히 설명 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="c2456-532">항목에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-532">The topics include:</span></span>

-   <span data-ttu-id="c2456-533">App-v 패키지 추가</span><span class="sxs-lookup"><span data-stu-id="c2456-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="c2456-534">App-v 패키지 게시</span><span class="sxs-lookup"><span data-stu-id="c2456-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="c2456-535">App-v 패키지 추가</span><span class="sxs-lookup"><span data-stu-id="c2456-535">Adding an App-V package</span></span>

<span data-ttu-id="c2456-536">게시 새로 고침 프로세스의 첫 번째 단계는 클라이언트에 App-v 패키지를 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="c2456-537">최종 결과는 `Add-AppVClientPackage` PowerShell의 cmdlet과 같으며, 게시 새로 고침 추가 프로세스 중에, 구성 된 게시 서버에 연결 되어 있으며, 응용 프로그램의 상위 수준 목록을 클라이언트에 다시 전달 하 여 자세한 정보를 가져와 단일 패키지 추가 작업을 수행 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="c2456-538">패키지 또는 연결 그룹 추가 또는 업데이트에 대 한 클라이언트를 구성한 다음 appv 파일에 액세스 하 여 프로세스가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="c2456-539">다음으로, appv 파일의 내용이 확장 되어 로컬 운영 체제의 적절 한 위치에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="c2456-540">다음은 패키지가 오류 스트리밍을 위해 구성 되었다고 가정 하 여 프로세스에 대 한 상세한 워크플로입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="c2456-541">App-v 패키지를 추가 하는 방법</span><span class="sxs-lookup"><span data-stu-id="c2456-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="c2456-542">PowerShell 또는 게시 새로 고침 프로세스의 작업 순서 시작을 통한 수동 시작입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="c2456-543">App-v 클라이언트는 HTTP 연결을 설정 하 고 대상에 따라 응용 프로그램 목록을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="c2456-544">게시 새로 고침 프로세스는 대상 컴퓨터 또는 사용자를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="c2456-545">App-v 게시 서버는 시작 하는 대상, 사용자 또는 컴퓨터의 id를 사용 하 고 데이터베이스를 쿼리 하 여 자격이 있는 응용 프로그램 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="c2456-546">패키지 기준에 대 한 자세한 내용은 서버에 추가 요청을 보내는 데 사용 하는 XML 응답으로 응용 프로그램 목록이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="c2456-547">App-v 클라이언트의 게시 에이전트는 직렬화 된 다음 모든 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="c2456-548">연결 그룹의 일부인 패키지 버전 업데이트를 처리할 수 없기 때문에 게시 취소 되거나 사용할 수 없는 모든 연결 그룹을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="c2456-549">추가 또는 업데이트 작업을 식별 하 여 패키지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="c2456-550">App-v 클라이언트는 Windows에서 AppX API를 이용 하 고 게시 서버에서 appv 파일에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="c2456-551">패키지 파일이 열리고 AppXManifest.xml 및 StreamMap.xml 패키지 저장소에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="c2456-552">StreamMap.xml에 정의 된 전체 스트림 게시 블록 데이터</span><span class="sxs-lookup"><span data-stu-id="c2456-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="c2456-553">패키지 Store\\PkgGUID\\VerGUID\\Root.에 게시 블록 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="c2456-554">아이콘: 확장 지점의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="c2456-555">PE 헤더 (이식 가능한 헤더): 디스크에서 이미지에 대 한 기본 정보를 포함 하는 확장 지점의 대상으로, 직접 액세스 하거나 파일 형식을 통해 사용할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="c2456-556">스크립트: 게시 프로세스 전체에서 사용할 스크립트 디렉터리를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="c2456-557">패키지 저장소 채우기:</span><span class="sxs-lookup"><span data-stu-id="c2456-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="c2456-558">나열 된 모든 디렉터리에 대해 압축을 푼 패키지를 나타내는 스파스 파일을 디스크에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="c2456-559">루트 아래 상위 수준 파일 및 디렉터리를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="c2456-560">디렉터리가 디스크에 스파스로 나열 되 고 요청 시 스트리밍된 경우 다른 모든 파일이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="c2456-561">컴퓨터 카탈로그 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-561">Create the machine catalog entries.</span></span> <span data-ttu-id="c2456-562">패키지 파일에서 Manifest.xml 및 DeploymentConfiguration.xml 만들기 (패키지에서 자리 표시자 DeploymentConfiguration.xml 파일을 만들 수 없는 경우)</span><span class="sxs-lookup"><span data-stu-id="c2456-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="c2456-563">레지스트리 HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog에서 패키지 저장소의 위치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="c2456-564">패키지 저장소 에서%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. .dat 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="c2456-565">앱-V 커널 모드 드라이버 HKLM\\Microsoft\\Software\\AppV\\MAV를 사용 하 여 패키지 등록</span><span class="sxs-lookup"><span data-stu-id="c2456-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="c2456-566">패키지 추가 타이밍에 대 한 AppxManifest.xml 또는 DeploymentConfig.xml 파일에서 스크립팅을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="c2456-567">추가 및 설정/해제를 통해 연결 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="c2456-568">대상에 게시 되지 않은 개체 (사용자 또는 컴퓨터)를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="c2456-569">**참고**  패키지 삭제는 수행 되지 않고 특정 대상 (사용자 또는 컴퓨터)의 통합 지점을 제거 하 고 사용자 카탈로그 파일 (전역으로 게시 된 컴퓨터 카탈로그 파일)을 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="c2456-570">클라이언트 구성을 기반으로 백그라운드 로드 탑재를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="c2456-571">컴퓨터 또는 사용자에 대 한 게시 정보가 이미 있는 패키지는 즉시 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="c2456-572">**참고**  이 상태는 패키지의 백그라운드 추가를 사용 하 여 게시 취소 하지 않고 제거 하는 제품으로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="c2456-573">이렇게 하면 게시 새로 고침 프로세스의 App-v 패키지 추가가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="c2456-574">다음 단계는 패키지를 특정 대상 (컴퓨터 또는 사용자)에 게시 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![패키지 파일 및 레지스트리 데이터 추가](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="c2456-576">App-v 패키지 게시</span><span class="sxs-lookup"><span data-stu-id="c2456-576">Publishing an App-V package</span></span>

<span data-ttu-id="c2456-577">게시 새로 고침 작업을 수행 하는 동안 특정 게시 작업 (AppVClientPackage)은 사용자 카탈로그에 항목을 추가 하 고, 사용자에 게 자격을 매핑하고, 로컬 저장소를 식별 하 고, 통합 단계를 완료 하 여 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="c2456-578">자세한 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="c2456-579">게시 하는 방법 및 App-v 패키지</span><span class="sxs-lookup"><span data-stu-id="c2456-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="c2456-580">패키지 항목이 사용자 카탈로그에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="c2456-581">사용자 대상 패키지: UserDeploymentConfiguration.xml 및 UserManifest.xml 사용자 카탈로그의 컴퓨터에 배치 됨</span><span class="sxs-lookup"><span data-stu-id="c2456-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="c2456-582">컴퓨터 대상 (전역) 패키지: UserDeploymentConfiguration.xml는 컴퓨터 카탈로그에 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="c2456-583">HKLM\\Software\\Microsoft\\AppV\\MAV에서 사용자에 대 한 커널 모드 드라이버를 사용 하 여 패키지 등록</span><span class="sxs-lookup"><span data-stu-id="c2456-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="c2456-584">통합 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="c2456-585">확장 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-585">Create extension points.</span></span>

    2.  <span data-ttu-id="c2456-586">백업 정보를 사용자의 레지스트리와 로밍 프로필에 저장 합니다 (바로 가기 백업).</span><span class="sxs-lookup"><span data-stu-id="c2456-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="c2456-587">**참고**  이렇게 하면 패키지가 게시 취소 된 경우 확장 지점을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="c2456-588">게시 타이밍을 대상으로 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="c2456-589">연결 그룹의 일부인 App-v 패키지를 게시 하는 것은 위의 프로세스와 매우 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="c2456-590">연결 그룹의 경우 특정 카탈로그 정보를 저장 하는 경로에는 PackageGroups가 Catalog 디렉터리의 자식으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="c2456-591">자세한 내용은 위의 컴퓨터 및 사용자 카탈로그 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-591">Review the machine and users catalog information above for details.</span></span>

![패키지 파일 및 레지스트리 데이터 추가-전역](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="c2456-593">응용 프로그램 시작</span><span class="sxs-lookup"><span data-stu-id="c2456-593">Application launch</span></span>

<span data-ttu-id="c2456-594">게시 새로 고침 프로세스 후 사용자가 App-v 응용 프로그램을 시작 하 고 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="c2456-595">이 프로세스는 매우 간단 하며 최소한의 네트워크 트래픽으로 빠르게 실행 하도록 최적화 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="c2456-596">App-v 클라이언트는 게시 중에 만들어진 파일에 대 한 사용자 카탈로그 경로를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="c2456-597">패키지를 시작할 수 있는 권한이 설정 되 면 App-v 클라이언트는 가상 환경을 만들고, 필요한 모든 데이터 스트리밍을 시작 하 고, 가상 환경 만들기 중 적절 한 매니페스트 및 배포 구성 파일을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="c2456-598">특정 패키지 및 응용 프로그램에 대해 가상 환경을 만들고 구성 하면 응용 프로그램이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="c2456-599">App-v 응용 프로그램을 시작 하는 방법</span><span class="sxs-lookup"><span data-stu-id="c2456-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="c2456-600">사용자가 바로 가기 또는 파일 형식 호출을 클릭 하 여 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="c2456-601">App-v 클라이언트는 다음 파일에 대 한 사용자 카탈로그의 존재를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="c2456-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="c2456-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="c2456-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="c2456-604">파일이 있으면 해당 특정 사용자에 대 한 응용 프로그램 자격이 제공 되 고 응용 프로그램에서 실행을 위해 프로세스가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="c2456-605">이 시점에 네트워크 소통량이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="c2456-606">그런 다음 App-v 클라이언트는 App-v 클라이언트 서비스에 대해 등록 된 패키지의 경로가 레지스트리에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="c2456-607">패키지 저장소의 경로를 찾을 때 가상 환경이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="c2456-608">첫 번째 실행 인 경우 기본 기능 블록이 있으면이를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="c2456-609">다운로드 한 후 App-v 클라이언트 서비스는 매니페스트 및 배포 구성 파일을 사용 하 여 가상 환경을 구성 하 고 모든 App-v 하위 시스템을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="c2456-610">응용 프로그램이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-610">The Application launches.</span></span> <span data-ttu-id="c2456-611">패키지 저장소 (스파스 파일)의 누락 된 파일에 대 한 앱-V는 필요한 기준에 따라 파일의 오류를 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![패키지 파일 및 레지스트리 데이터 추가-스트림](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="c2456-613">App-v 패키지 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c2456-613">Upgrading an App-V package</span></span>

<span data-ttu-id="c2456-614">앱-V 5 패키지 업그레이드 프로세스는 이전 버전의 App-v와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="c2456-615">App-v는 서로 다른 사용자에 게 해당 하는 컴퓨터에서 여러 버전의 동일한 패키지를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="c2456-616">패키지 저장소와 카탈로그는 새 리소스로 업데이트 되므로 언제 든 지 패키지 버전을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="c2456-617">새 버전 리소스 추가와 관련 된 유일한 프로세스는 저장소 최적화입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="c2456-618">업그레이드 중에 새 파일만 새 버전 저장소 위치에 추가 되 고 변경 되지 않은 파일에 대 한 하드 링크가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="c2456-619">이렇게 하면 파일을 하나의 디스크 위치에 표시 한 다음 디스크에 있는 파일 위치 항목이 있는 모든 폴더로 프로젝션 하 여 전체 저장소를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="c2456-620">App-v 패키지 업그레이드에 대 한 구체적인 정보는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="c2456-621">앱-V 패키지를 업그레이드 하는 방법</span><span class="sxs-lookup"><span data-stu-id="c2456-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="c2456-622">App-v 클라이언트는 게시 새로 고침을 수행 하 고 최신 버전의 App-v 패키지를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="c2456-623">새 버전의 적절 한 카탈로그에 패키지 항목이 추가 됨</span><span class="sxs-lookup"><span data-stu-id="c2456-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="c2456-624">사용자 대상 패키지: UserDeploymentConfiguration.xml 및 UserManifest.xml는 appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID 사용자 카탈로그의 컴퓨터에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="c2456-625">컴퓨터 대상 (전역) 패키지: UserDeploymentConfiguration.xml 는%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID의 컴퓨터 카탈로그에 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="c2456-626">HKLM\\Software\\Microsoft\\AppV\\MAV에서 사용자에 대 한 커널 모드 드라이버를 사용 하 여 패키지 등록</span><span class="sxs-lookup"><span data-stu-id="c2456-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="c2456-627">통합 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="c2456-628">매니페스트 및 동적 구성 파일에서 EP (확장 지점)를 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="c2456-629">파일 기반 EP 데이터는 패키지 저장소의 연결 지점을 활용 하 여 AppData 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="c2456-630">새 버전을 사용할 수 있게 되 면 버전 1 EPs가 이미 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="c2456-631">확장 지점은 컴퓨터 또는 사용자 카탈로그에서 최신 또는 업데이트 된 확장 지점에 대 한 버전 2 위치로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="c2456-632">게시 타이밍을 대상으로 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="c2456-633">필요에 따라 side-by-side 어셈블리를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="c2456-634">사용 중인 앱-V 패키지 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c2456-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="c2456-635">**App-v 5 SP2 시작**: 최종 사용자가 사용 중인 패키지를 업그레이드 하려고 하면 업그레이드 작업이 보류 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="c2456-636">업그레이드는 다음 규칙에 따라 나중에 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-637">작업 종류</span><span class="sxs-lookup"><span data-stu-id="c2456-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="c2456-638">해당 규칙</span><span class="sxs-lookup"><span data-stu-id="c2456-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-639">사용자 기반 작업 (예: 패키지를 사용자에 게 게시)</span><span class="sxs-lookup"><span data-stu-id="c2456-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-640">보류 중인 작업은 사용자가 로그 오프 한 다음 다시 로그온 하면 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-641">전역 기반 작업 (예: 연결 그룹을 전역적으로 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="c2456-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-642">보류 중인 작업은 컴퓨터를 종료 한 후 다시 시작 하면 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2456-643">작업이 보류 상태에 배치 되 면 App-v 클라이언트는 다음과 같이 보류 중인 작업에 대 한 레지스트리 키도 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-644">사용자 기반 또는 전역 기반 작업</span><span class="sxs-lookup"><span data-stu-id="c2456-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="c2456-645">레지스트리 키가 생성 되는 위치</span><span class="sxs-lookup"><span data-stu-id="c2456-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-646">사용자 기반 작업</span><span class="sxs-lookup"><span data-stu-id="c2456-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-647">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="c2456-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-648">전역 기반 작업</span><span class="sxs-lookup"><span data-stu-id="c2456-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-649">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="c2456-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2456-650">다음 작업을 완료 해야 사용자가 최신 버전의 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-651">작업</span><span class="sxs-lookup"><span data-stu-id="c2456-651">Task</span></span></th>
<th align="left"><span data-ttu-id="c2456-652">세부 정보</span><span class="sxs-lookup"><span data-stu-id="c2456-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-653">컴퓨터에 패키지 추가</span><span class="sxs-lookup"><span data-stu-id="c2456-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-654">이 작업은 컴퓨터에 따라 달라 지 며, 위의 패키지 추가 섹션의 단계를 완료 하 여 언제 든 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-655">패키지 게시</span><span class="sxs-lookup"><span data-stu-id="c2456-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-656">위의 단계에 대 한 패키지 게시 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="c2456-657">이 프로세스에서는 시스템의 확장 지점을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="c2456-658">이 작업을 완료 하면 최종 사용자가 응용 프로그램을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2456-659">패키지 업데이트에 대 한 지침으로 다음 예제 시나리오를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-660">시나리오</span><span class="sxs-lookup"><span data-stu-id="c2456-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="c2456-661">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c2456-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-662">업그레이드 하려고 할 때 app-v 패키지를 사용 하 고 있지 않음</span><span class="sxs-lookup"><span data-stu-id="c2456-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-663">패키지의 다음 구성 요소는 가상 응용 프로그램, COM 서버 또는 셸 확장 중 어느 것에도 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="c2456-664">관리자가 최신 버전의 패키지를 게시 하면 다음에 패키지 내의 구성 요소 또는 응용 프로그램을 실행할 때 업그레이드가 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="c2456-665">새 버전의 패키지를 스트리밍하 고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="c2456-666">앱-V 5 SP2의 이전 릴리스 버전에서의이 시나리오에서 변경 된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-667">관리자가 최신 버전의 패키지를 게시할 때 app-v 패키지가 사용 됨</span><span class="sxs-lookup"><span data-stu-id="c2456-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-668">업그레이드 작업은 App-v 클라이언트에 의해 보류 중으로 설정 되며,이는 패키지를 사용 하 고 있지 않을 때 나중에 대기열에 대기 상태를 나타내는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="c2456-669">패키지 응용 프로그램을 사용 중인 경우 사용자는 가상 응용 프로그램을 종료 한 후 업그레이드가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="c2456-670">패키지에 Windows 탐색기에서 영구적으로 로드 되는 셸 확장 (Office 2013)이 있는 경우 사용자는 로그인 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="c2456-671">사용자는 로그 오프 한 다음 다시 로그인 하 여 App-v 패키지 업그레이드를 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2456-672">전역 vs 사용자 게시</span><span class="sxs-lookup"><span data-stu-id="c2456-672">Global vs user publishing</span></span>

<span data-ttu-id="c2456-673">2 가지 방법 중 하나로 app-v 패키지를 게시할 수 있습니다. 앱-V 패키지를 특정 사용자 또는 사용자 그룹에 통해 하 고 컴퓨터의 모든 사용자에 대해 앱 V 패키지를 전체 컴퓨터에 통해 하는 사용자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="c2456-674">패키지 업그레이드를 보류 하 고 App-v 패키지를 사용 하 고 있지 않은 경우 두 가지 유형의 게시를 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="c2456-675">**전역으로 게시**됨: 응용 프로그램이 컴퓨터에 게시 됩니다. 해당 컴퓨터의 모든 사용자가 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="c2456-676">앱을 다시 시작 하는 것을 의미 하는 App-v 클라이언트 서비스가 시작 될 때 업그레이드가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="c2456-677">**사용자가 게시**됨: 응용 프로그램이 사용자에 게 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="c2456-678">컴퓨터에 여러 사용자가 있는 경우 해당 사용자의 하위 집합에 응용 프로그램을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="c2456-679">업그레이드는 사용자가 로그인 하거나 다시 게시 되는 경우 (정기적으로, ConfigMgr의 정책 새로 고침 및 평가 또는 App-v의 정기 게시/새로 고침 또는 PowerShell 명령을 명시적으로 통해)에 수행 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="c2456-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="c2456-680">App-v 패키지 제거</span><span class="sxs-lookup"><span data-stu-id="c2456-680">Removing an App-V package</span></span>

<span data-ttu-id="c2456-681">전체 인프라에서 App-v 응용 프로그램을 제거 하는 것은 게시 취소 작업 이므로 패키지 제거를 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="c2456-682">프로세스는 위의 게시 과정과 동일 하지만 제거 프로세스를 추가 하는 대신 App-v 패키지에 대해 변경한 내용을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="c2456-683">App-v 패키지 복구</span><span class="sxs-lookup"><span data-stu-id="c2456-683">Repairing an App-V package</span></span>

<span data-ttu-id="c2456-684">복구 작업은 매우 간단 하지만 컴퓨터의 여러 위치에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="c2456-685">앞에서 언급 한 COW (기록에서) 위치는 제거 되 고, 확장 지점은 통합 취소 된 다음 다시 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="c2456-686">COW 데이터 배치 위치는 레지스트리에서 등록 된 위치를 검토 하 여 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="c2456-687">이 작업은 자동으로 수행 되며 App-v 클라이언트 콘솔 또는 PowerShell (AppVClientPackage)을 통해 복구 작업을 시작 하는 것 외에는 관리 제어가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="c2456-688">앱-V 패키지의 통합</span><span class="sxs-lookup"><span data-stu-id="c2456-688">Integration of App-V packages</span></span>


<span data-ttu-id="c2456-689">앱-V 클라이언트 및 패키지 아키텍처는 패키지를 추가 하 고 게시 하는 동안 로컬 운영 체제와 특정 통합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="c2456-690">3 개의 파일은 App-v 패키지의 통합 또는 확장 지점을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="c2456-691">AppXManifest.xml: 패키지 저장소와 사용자 프로필에 저장 된 대체 복사본을 사용 하 여 패키지 내에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="c2456-692">시퀀싱 프로세스 중에 생성 된 옵션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="c2456-693">DeploymentConfig.xml: 컴퓨터 및 사용자 기반 통합 확장 지점의 구성 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="c2456-694">UserConfig.xml: 사용자 기반 구성만 제공 하 고 대상 사용자 기반 확장 지점은 있는 Deploymentconfig.xml의 하위 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="c2456-695">통합 규칙</span><span class="sxs-lookup"><span data-stu-id="c2456-695">Rules of integration</span></span>

<span data-ttu-id="c2456-696">App-v 클라이언트를 사용 하 여 컴퓨터에 앱 V 응용 프로그램을 게시할 때 아래 목록에서 설명 하는 대로 몇 가지 특정 동작이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="c2456-697">전역 게시: 바로 가기는 모든 사용자 프로필 위치에 저장 되며 다른 확장 지점은 HKLM hive의 레지스트리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="c2456-698">사용자 게시: 바로 가기는 현재 사용자 계정 프로필에 저장 되며 다른 확장 지점은 HKCU 하이브의 레지스트리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="c2456-699">백업 및 복원: 기존 네이티브 응용 프로그램 데이터 및 레지스트리 (예: FTA 등록)는 게시 하는 동안 백업 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="c2456-700">App-v 패키지에는 소유권이 최신 게시 된 App-v 응용 프로그램에 전달 되는 마지막 통합 패키지에 따라 소유권이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="c2456-701">소유 하 고 있는 App-v 패키지가 게시 취소 된 경우 한 App-v 패키지에서 다른 앱으로 소유권을 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="c2456-702">이는 데이터 나 레지스트리의 복원을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="c2456-703">마지막 패키지가 확장 지점을 기준으로 게시 취소 되거나 제거 될 때 백업 된 데이터를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="c2456-704">확장 지점</span><span class="sxs-lookup"><span data-stu-id="c2456-704">Extension points</span></span>

<span data-ttu-id="c2456-705">앱-V 게시 파일 (매니페스트 및 동적 구성)은 응용 프로그램이 로컬 운영 체제와 통합 될 수 있는 여러 확장 지점을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="c2456-706">이러한 확장 지점은 바로 가기 배치, 파일 형식 연결 만들기, 구성 요소 등록 등 일반적인 응용 프로그램 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="c2456-707">기존 응용 프로그램과 같은 방식으로 설치 되지 않은 가상화 된 응용 프로그램은 몇 가지 차이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="c2456-708">다음은이 섹션에서 설명 하는 확장 요점의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="c2456-709">정의</span><span class="sxs-lookup"><span data-stu-id="c2456-709">Shortcuts</span></span>

-   <span data-ttu-id="c2456-710">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="c2456-710">File Type Associations</span></span>

-   <span data-ttu-id="c2456-711">셸 확장</span><span class="sxs-lookup"><span data-stu-id="c2456-711">Shell Extensions</span></span>

-   <span data-ttu-id="c2456-712">COM</span><span class="sxs-lookup"><span data-stu-id="c2456-712">COM</span></span>

-   <span data-ttu-id="c2456-713">소프트웨어 클라이언트</span><span class="sxs-lookup"><span data-stu-id="c2456-713">Software Clients</span></span>

-   <span data-ttu-id="c2456-714">응용 프로그램 기능</span><span class="sxs-lookup"><span data-stu-id="c2456-714">Application capabilities</span></span>

-   <span data-ttu-id="c2456-715">URL 프로토콜 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="c2456-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="c2456-716">AppPath</span></span>

-   <span data-ttu-id="c2456-717">가상 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c2456-717">Virtual Application</span></span>

### <span data-ttu-id="c2456-718">정의</span><span class="sxs-lookup"><span data-stu-id="c2456-718">Shortcuts</span></span>

<span data-ttu-id="c2456-719">짧은 컷은 OS와 통합 되는 기본 요소 중 하나 이며, App-v 응용 프로그램의 직접 사용자 시작에 대 한 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="c2456-720">App-v 응용 프로그램을 게시 하 고 게시가 취소 되는 동안</span><span class="sxs-lookup"><span data-stu-id="c2456-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="c2456-721">패키지 매니페스트 및 동적 구성 XML 파일에서 특정 응용 프로그램 실행 파일의 경로는 다음과 같은 섹션에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="c2456-722">앞에서 설명한 대로 앱-V 바로 가기는 기본적으로 새로 고침 작업에 따라 사용자의 프로필에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="c2456-723">전역 새로 고침 바로 가기 모든 사용자 프로필에서 사용자를 새로 고치면 특정 사용자의 프로필에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="c2456-724">실제 실행 파일은 패키지 저장소에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="c2456-725">.ICO 파일의 위치는 App-v 패키지의 토큰화 된 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="c2456-726">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="c2456-726">File type associations</span></span>

<span data-ttu-id="c2456-727">App-v 클라이언트는 사용자가 파일 형식 호출을 사용 하거나 특수 하 게 등록 된 확장명 (.docx)이 있는 파일을 열어서 App-v 응용 프로그램을 시작할 수 있도록 게시 중에 로컬 운영 체제 파일 형식 연결을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="c2456-728">다음 예제에 표시 된 대로 매니페스트 및 동적 구성 파일에 파일 형식 연결이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="c2456-729">**참고**  이 예제에서는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="c2456-730">확장명</span><span class="sxs-lookup"><span data-stu-id="c2456-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="c2456-731">ProgId 값 (인접 한 ProgId를 가리키는)</span><span class="sxs-lookup"><span data-stu-id="c2456-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="c2456-732">는 응용 프로그램 실행 파일을 가리키는 명령줄입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="c2456-733">셸 확장</span><span class="sxs-lookup"><span data-stu-id="c2456-733">Shell extensions</span></span>

<span data-ttu-id="c2456-734">셸 확장은 시퀀싱 프로세스 중 패키지에 자동으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="c2456-735">패키지가 전역으로 게시 되 면 셸 확장에서는 응용 프로그램이 로컬에 설치 되어 있는 것과 동일한 기능을 사용자에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="c2456-736">셸 확장 기능을 사용 하도록 설정 하려면 응용 프로그램에 추가 설정이 나 클라이언트에 대 한 구성이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="c2456-737">셸 확장 사용에 대 한 요구 사항:</span><span class="sxs-lookup"><span data-stu-id="c2456-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="c2456-738">포함 된 셸 확장을 포함 하는 패키지는 전체적으로 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="c2456-739">응용 프로그램, Sequencer, App-v 클라이언트의 "비트"는 일치 해야 하며 그렇지 않으면 셸 확장이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="c2456-740">예:</span><span class="sxs-lookup"><span data-stu-id="c2456-740">For example:</span></span>

    -   <span data-ttu-id="c2456-741">응용 프로그램 버전은 64 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="c2456-742">Sequencer가 64 비트 컴퓨터에서 실행 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="c2456-743">패키지가 64 비트 App-v 클라이언트 컴퓨터로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="c2456-744">다음 표에서는 지원 되는 셸 확장을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-745">처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="c2456-746">설명</span><span class="sxs-lookup"><span data-stu-id="c2456-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-747">상황에 맞는 메뉴 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-748">상황에 맞는 메뉴에 메뉴 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="c2456-749">이 메서드는 상황에 맞는 메뉴가 표시 되기 전에 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-750">끌어서 놓기 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-751">끌어서 놓기를 마우스 오른쪽 단추로 클릭 하 고 표시 되는 상황에 맞는 메뉴를 수정할 때의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-752">놓기 대상 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-753">파일 등의 놓기 대상 위에 데이터 개체를 끌어서 놓은 후의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-754">데이터 개체 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-755">파일이 클립보드에 복사 되거나 놓기 대상 위에 끌어 놓은 후의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="c2456-756">놓기 대상에 추가 클립보드 형식을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-757">속성 시트 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-758">개체의 속성 시트 대화 상자에 페이지를 바꾸거나 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-759">정보 팁 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-760">마우스 포인터로 팝업 도구 설명 안에 항목에 대 한 플래그 및 정보 팁을 검색 하 고 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-761">열 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-762">Windows 탐색기 세부 정보 보기에서 사용자 지정 열을 만들고 표시할 수 있습니다 <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="c2456-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="c2456-763">이를 사용 하 여 정렬 및 그룹화를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-764">미리 보기 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-765">Windows 탐색기 미리 보기 창에 파일의 미리 보기를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2456-766">COM</span><span class="sxs-lookup"><span data-stu-id="c2456-766">COM</span></span>

<span data-ttu-id="c2456-767">App-v 클라이언트는 COM 통합 및 가상화에 대 한 지원이 포함 된 응용 프로그램 게시를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="c2456-768">COM 통합을 사용 하면 App-v 클라이언트가 로컬 운영 체제 및 개체의 가상화에 COM 개체를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="c2456-769">이 문서의 목적을 위해 COM 개체의 통합에는 추가 세부 정보가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="c2456-770">App-v는 패키지의 COM 개체를 두 가지 프로세스 유형 (out-of-process 및 in-process)으로 로컬 운영 체제에 등록할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="c2456-771">COM 개체 등록은 해제, 격리 및 통합이 포함 된 특정 App-v 패키지에 대 한 여러 작업 모드와 조합 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="c2456-772">통합 모드가 out-of-process 또는 in-process 형식 중 하나로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="c2456-773">COM 모드 및 형식의 구성은 동적 구성 파일 (deploymentconfig.xml 또는 userconfig.xml)을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="c2456-774">App-v 통합에 대 한 자세한 내용은 다음에서 확인할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="c2456-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="c2456-775">소프트웨어 클라이언트 및 응용 프로그램 기능</span><span class="sxs-lookup"><span data-stu-id="c2456-775">Software clients and application capabilities</span></span>

<span data-ttu-id="c2456-776">App-v는 운영 체제의 소프트웨어 클라이언트에 가상화 된 응용 프로그램을 등록할 수 있도록 하는 특정 소프트웨어 클라이언트 및 응용 프로그램 기능 확장 지점을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="c2456-777">이렇게 하면 사용자가 전자 메일, 인스턴트 메시지, 미디어 플레이어 등의 작업에 대 한 기본 프로그램을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="c2456-778">이 작업은 제어판에서 프로그램 액세스 및 컴퓨터 기본값 설정으로 수행 되며 매니페스트 또는 동적 구성 파일에서 시퀀싱 중에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="c2456-779">앱 기능은 App-v 응용 프로그램이 전역으로 게시 된 경우에만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="c2456-780">앱 V 기반 메일 클라이언트의 소프트웨어 클라이언트 등록의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="c2456-781">**참고**  이 예제에서는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="c2456-782">전자 메일 클라이언트 통합에 대 한 전반적인 소프트웨어 클라이언트 설정</span><span class="sxs-lookup"><span data-stu-id="c2456-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="c2456-783">특정 전자 메일 클라이언트를 기본 전자 메일 클라이언트로 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="c2456-784">MAPI dll 등록이</span><span class="sxs-lookup"><span data-stu-id="c2456-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="c2456-785">URL 프로토콜 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-785">URL Protocol handler</span></span>

<span data-ttu-id="c2456-786">응용 프로그램은 항상 파일 형식 호출을 활용 하는 가상화 된 응용 프로그램 이라고 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="c2456-787">예를 들어 문서 또는 웹 페이지 내에 mailto: link를 포함 하는 응용 프로그램에서 사용자는 mailto: 링크를 클릭 하 고 등록 된 메일 클라이언트를 가져올 것으로 간주 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="c2456-788">App-v는 로컬 운영 체제를 사용 하 여 패키지 별로 등록할 수 있는 URL 프로토콜 처리기를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="c2456-789">시퀀싱 하는 동안 URL 프로토콜 처리기가 패키지에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="c2456-790">특정 URL 프로토콜 처리기를 등록할 수 있는 응용 프로그램이 두 개 이상 있는 경우 동적 구성 파일을 사용 하 여 동작을 수정 하 고, 기본 응용 프로그램이 시작 되지 않아야 하는 응용 프로그램에 대해이 기능을 사용 하지 않도록 설정 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="c2456-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="c2456-791">AppPath</span></span>

<span data-ttu-id="c2456-792">AppPath 확장 지점은 운영 체제에서 직접 호출 하는 앱 V 응용 프로그램을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="c2456-793">이 작업은 일반적으로 운영 체제에 따라 실행 또는 시작 화면에서 수행 되며, 관리자는 실행 파일에 대 한 특정 경로를 호출 하지 않고 운영 체제 명령 또는 스크립트에서 앱 V 응용 프로그램에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="c2456-794">따라서 게시 하는 동안 수행 되는 모든 시스템에서 시스템 경로 환경 변수를 수정 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="c2456-795">AppPath 확장 지점은 매니페스트 또는 동적 구성 파일에 구성 되며 사용자 용으로 게시 하는 동안 로컬 컴퓨터의 레지스트리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="c2456-796">AppPath 검토에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=392835> 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="c2456-797">가상 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c2456-797">Virtual application</span></span>

<span data-ttu-id="c2456-798">이 하위 시스템은 다른 App-v 구성 요소에서 일반적으로 사용 되는 시퀀싱 중에 캡처한 응용 프로그램 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="c2456-799">특정 응용 프로그램에 속하는 확장 지점의 통합은 동적 구성 파일을 사용 하 여 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="c2456-800">예를 들어 패키지에 두 개의 응용 프로그램이 포함 된 경우 하나의 응용 프로그램에 속하는 모든 확장 지점을 사용 하지 않도록 설정 하 여 다른 응용 프로그램의 확장 지점 통합만 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="c2456-801">확장 점 규칙</span><span class="sxs-lookup"><span data-stu-id="c2456-801">Extension point rules</span></span>

<span data-ttu-id="c2456-802">위에서 설명한 확장 지점은 패키지가 게시 된 방식에 따라 운영 체제에 통합 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="c2456-803">전역 게시는 사용자가 사용자 위치에서 확장 지점을 배치할 공용 컴퓨터 위치에 확장 지점을 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="c2456-804">예를 들어 바탕 화면에 만들어지고 전역으로 게시 된 바로 가기는 바로 가기 (%Public%\\Desktop) 및 레지스트리 데이터 (HKLM\\Software\\Classes)에 대 한 파일 데이터를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="c2456-805">동일한 바로 가기에는 파일 데이터 (%UserProfile%\\Desktop)와 레지스트리 데이터 (HKCU\\Software\\Classes)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="c2456-806">확장 지점은 일부 확장 지점에는 전역 게시가 필요 하 고, 특정 운영 체제 및이를 전달 하는 아키텍처에 대 한 시퀀싱이 필요한 경우에는 모두 같은 방식으로 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="c2456-807">다음은 이러한 두 가지 키 규칙을 설명 하는 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2456-808">가상 확장</span><span class="sxs-lookup"><span data-stu-id="c2456-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="c2456-809">대상 OS 시퀀싱 필요</span><span class="sxs-lookup"><span data-stu-id="c2456-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="c2456-810">전역 게시 필요</span><span class="sxs-lookup"><span data-stu-id="c2456-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-811">키</span><span class="sxs-lookup"><span data-stu-id="c2456-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-812">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="c2456-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-813">URL 프로토콜</span><span class="sxs-lookup"><span data-stu-id="c2456-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-814">X</span><span class="sxs-lookup"><span data-stu-id="c2456-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="c2456-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-816">X</span><span class="sxs-lookup"><span data-stu-id="c2456-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-817">COM 모드</span><span class="sxs-lookup"><span data-stu-id="c2456-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-818">소프트웨어 클라이언트</span><span class="sxs-lookup"><span data-stu-id="c2456-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-819">X</span><span class="sxs-lookup"><span data-stu-id="c2456-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-820">응용 프로그램 기능</span><span class="sxs-lookup"><span data-stu-id="c2456-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-821">X</span><span class="sxs-lookup"><span data-stu-id="c2456-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-822">X</span><span class="sxs-lookup"><span data-stu-id="c2456-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-823">상황에 맞는 메뉴 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-824">X</span><span class="sxs-lookup"><span data-stu-id="c2456-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-825">X</span><span class="sxs-lookup"><span data-stu-id="c2456-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-826">끌어서 놓기 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-827">X</span><span class="sxs-lookup"><span data-stu-id="c2456-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-828">데이터 개체 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-829">X</span><span class="sxs-lookup"><span data-stu-id="c2456-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-830">속성 시트 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-831">X</span><span class="sxs-lookup"><span data-stu-id="c2456-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-832">정보 팁 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-833">X</span><span class="sxs-lookup"><span data-stu-id="c2456-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-834">열 처리기</span><span class="sxs-lookup"><span data-stu-id="c2456-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-835">X</span><span class="sxs-lookup"><span data-stu-id="c2456-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-836">셸 확장</span><span class="sxs-lookup"><span data-stu-id="c2456-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-837">X</span><span class="sxs-lookup"><span data-stu-id="c2456-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2456-838">브라우저 도우미 개체</span><span class="sxs-lookup"><span data-stu-id="c2456-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-839">X</span><span class="sxs-lookup"><span data-stu-id="c2456-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-840">X</span><span class="sxs-lookup"><span data-stu-id="c2456-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2456-841">Active X 개체</span><span class="sxs-lookup"><span data-stu-id="c2456-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-842">X</span><span class="sxs-lookup"><span data-stu-id="c2456-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2456-843">X</span><span class="sxs-lookup"><span data-stu-id="c2456-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="c2456-844">동적 구성 처리</span><span class="sxs-lookup"><span data-stu-id="c2456-844">Dynamic configuration processing</span></span>


<span data-ttu-id="c2456-845">하나의 컴퓨터 또는 사용자에 게 App-v 패키지를 배포 하는 것은 매우 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="c2456-846">그러나 조직이 비즈니스 회선 및 지역 및 정치적 경계를 넘어 AppV 응용 프로그램을 배포 하는 경우 한 설정 집합을 사용 하 여 응용 프로그램을 한 번 시퀀싱 하는 기능은 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="c2456-847">App-v는 매니페스트 파일에서 시퀀싱 하는 동안 특정 설정 및 구성을 캡처하며, 동적 구성 파일을 사용 하 여 수정도 지원 하므로이 시나리오를 위해 디자인 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="c2456-848">App-v 동적 구성은 컴퓨터 수준 또는 사용자 수준에서 패키지에 대 한 정책을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="c2456-849">동적 구성 파일을 사용 하면 시퀀싱 엔지니어가 패키지의 구성을 수정 하 여 개별 사용자 또는 컴퓨터 그룹의 요구를 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="c2456-850">일부 경우에는 App-v 환경에서 적절 한 기능을 제공 하기 위해 응용 프로그램을 수정 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="c2456-851">예를 들어 \ _ \ \* config.xml 파일을 수정 하 여 가상화 된 응용 프로그램이 다른 응용 프로그램에서 확장을 덮어쓰는 것을 방지 하기 위해 mailto 확장을 해제 하는 등 특정 작업을 지정 된 시간에 수행할 수 있도록 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="c2456-852">App-v 패키지에는 시퀀스 작업을 대표 하는 appv 패키지 파일 내부의 매니페스트 파일이 포함 되어 있으며, 동적 구성 파일이 특정 패키지에 할당 되지 않은 경우 선택 하는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="c2456-853">순서 사후 작업을 위해 동적 구성 파일을 수정 하 여 다양 한 데스크톱 또는 다른 확장 지점을 가진 사용자에 게 응용 프로그램을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="c2456-854">두 동적 구성 파일은 DDC (동적 배포 구성) 및 DUC (Dynamic User Configuration) 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="c2456-855">이 섹션에서는 매니페스트 및 동적 구성 파일의 조합에 대해 중점적으로 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="c2456-856">동적 구성 파일의 예</span><span class="sxs-lookup"><span data-stu-id="c2456-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="c2456-857">아래 예제에서는 게시 후와 정상적으로 작동 하는 동안 매니페스트, 배포 구성 및 사용자 구성 파일의 조합을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="c2456-858">이러한 예제는 각 파일의 간략 한 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="c2456-859">이 목적에는 파일의 조합이 표시 되며 각 파일에서 사용할 수 있는 특정 범주에 대 한 완전 한 설명이 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="c2456-860">자세한 내용은 다음에서 App-v 5 시퀀싱 가이드를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="c2456-861">매니페스트</span><span class="sxs-lookup"><span data-stu-id="c2456-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="c2456-862">배포 구성</span><span class="sxs-lookup"><span data-stu-id="c2456-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="c2456-863">사용자 구성</span><span class="sxs-lookup"><span data-stu-id="c2456-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="c2456-864">Side-by-side 어셈블리</span><span class="sxs-lookup"><span data-stu-id="c2456-864">Side-by-side assemblies</span></span>


<span data-ttu-id="c2456-865">App-v는 가상 응용 프로그램을 게시 하는 동안 클라이언트에서 시퀀싱 및 배포 하는 동안 SxS (나란히) 어셈블리의 자동 패키징을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="c2456-866">시퀀싱 컴퓨터에 없는 어셈블리를 시퀀싱 하는 동안 app-v 5 SP2는 SxS 어셈블리 캡처를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="c2456-867">Visual c + + (버전 8 이상) 및/또는 MSXML 런타임으로 구성 된 어셈블리의 경우, 모니터링 중에 설치 되지 않은 경우에도 Sequencer가 이러한 종속성을 자동으로 감지 하 여 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="c2456-868">Side-by-side 어셈블리 기능은 앱 V 시퀀서에서 시퀀싱 워크스테이션에 이미 있는 어셈블리를 캡처하지 않은 경우와 패키지 당 하나의 비트 버전으로 제한 되는 어셈블리를 privatizing 이전 버전의 App-v에 대 한 제한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="c2456-869">이 문제로 인해 클라이언트에 게 앱 V 응용 프로그램이 배포 되어 필요한 SxS 어셈블리가 없어 응용 프로그램 시작 실패가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="c2456-870">이렇게 하면 패키징 프로세스가 문서화 된 후 패키지에 필요한 모든 어셈블리가 사용자의 클라이언트 운영 체제에 로컬로 설치 되어 가상 응용 프로그램에 대 한 지원을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="c2456-871">어셈블리 수와 필요한 종속성에 대 한 응용 프로그램 설명서의 부족을 기준으로이 작업은 관리 및 구현 챌린지입니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="c2456-872">App-v의 side-by-side 어셈블리 지원에는 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="c2456-873">시퀀싱 하는 동안 어셈블리의 설치 여부에 관계 없이 SxS 어셈블리의 자동 캡처.</span><span class="sxs-lookup"><span data-stu-id="c2456-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="c2456-874">앱-V 클라이언트는 게시 시간에 필요한 SxS 어셈블리 (표시 되지 않은 경우)를 클라이언트 컴퓨터에 자동으로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="c2456-875">Sequencer는 Sequencer 보고 메커니즘에서 VC 런타임 종속성을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="c2456-876">시퀀서는 이전에 대상 컴퓨터에 어셈블리가 설치 되어 있는 시나리오를 지원 하 여 시퀀서에 이미 설치 되어 있는 어셈블리를 패키지 하지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="c2456-877">SxS 어셈블리 자동 게시</span><span class="sxs-lookup"><span data-stu-id="c2456-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="c2456-878">SxS 어셈블리가 있는 App-v 패키지를 게시 하는 동안 App-v 클라이언트는 컴퓨터에서 어셈블리가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="c2456-879">어셈블리가 없는 경우 클라이언트는 해당 어셈블리를 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="c2456-880">연결 그룹에 속하는 패키지는 어셈블리 설치에 대 한 정보를 포함 하지 않으므로 기본 패키지의 일부인 Side-by-side 어셈블리 설치에 의존 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="c2456-881">**참고**  어셈블리를 사용 하 여 패키지를 게시 취소 하거나 제거 해도 해당 패키지의 어셈블리는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="c2456-882">클라이언트 로깅</span><span class="sxs-lookup"><span data-stu-id="c2456-882">Client logging</span></span>


<span data-ttu-id="c2456-883">App-v 클라이언트는 표준 ETW 형식으로 Windows 이벤트 로그에 정보를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="c2456-884">특정 App-v 이벤트는 이벤트 뷰어, 응용 프로그램 및 서비스 Logs\\Microsoft\\AppV\\Client.에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="c2456-885">**참고**  App-v 5.0 SP3에서는 일부 로그가 통합 되어 다음 위치로 옮겨졌습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-885">**Note** In App-V 5.0 SP3, some logs have been consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="c2456-886">이동한 로그 목록은 [앱-V 5.0 SP3 정보](about-app-v-50-sp3.md#bkmk-event-logs-moved)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2456-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="c2456-887">세 가지 특정 범주의 이벤트가 아래에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="c2456-888">**관리자**: app-v 클라이언트에 적용 되는 구성에 대 한 이벤트를 기록 하 고 기본 경고 및 오류를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="c2456-889">**작동**: app-v 클라이언트에서 완료 된 app-v 작업의 감사 로그를 만드는 개별 구성 요소의 일반 app-v 실행 및 사용을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="c2456-890">**가상 응용 프로그램**: 가상화 하위 시스템을 시작 하 고 사용 하는 가상 응용 프로그램을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2456-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 





