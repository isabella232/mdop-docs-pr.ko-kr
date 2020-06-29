---
title: App-V 5.1 가상화된 응용 프로그램 만들기 및 관리
description: App-V 5.1 가상화된 응용 프로그램 만들기 및 관리
author: dansimp
ms.assetid: 26be4331-88eb-4cfb-9d82-e63d7ee54576
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 207529fb5d5333694d31a82f44f08b35513dd4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814689"
---
# <span data-ttu-id="e1829-103">App-V 5.1 가상화된 응용 프로그램 만들기 및 관리</span><span class="sxs-lookup"><span data-stu-id="e1829-103">Creating and Managing App-V 5.1 Virtualized Applications</span></span>


<span data-ttu-id="e1829-104">Microsoft Application Virtualization (App-v) 5.1 sequencer를 올바르게 배포한 후에는이를 사용 하 여 가상화 된 응용 프로그램으로 실행 되는 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.1 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="e1829-105">**참고**  App-v 5.1 sequencer, 모범 사례 시퀀싱, 가상 응용 프로그램을 만들고 업데이트 하는 예제를 구성 하는 방법에 대 한 자세한 내용은 [Microsoft Application Virtualization 5.0 시퀀싱 가이드](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V%205.0%20Sequencing%20Guide.docx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e1829-105">**Note** For more information about configuring the App-V 5.1 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V%205.0%20Sequencing%20Guide.docx).</span></span>

<span data-ttu-id="e1829-106">**참고** App-v 5. x 시퀀서는 파일 이름이 "CO_ x"가 일치 하는 응용 프로그램을 시퀀싱 할 수 없습니다 &lt; &gt; . 여기서 x는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-106">**Note** The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="e1829-107">오류 0x8007139F이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-107">Error 0x8007139F will be generated.</span></span>

## <span data-ttu-id="e1829-108">응용 프로그램 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="e1829-108">Sequencing an application</span></span>


<span data-ttu-id="e1829-109">앱-V 5.1 Sequencer를 사용 하 여 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-109">You can use the App-V 5.1 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="e1829-110">App-v 5.1 클라이언트를 실행 하는 컴퓨터에 배포할 수 있는 가상 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-110">Create virtual packages that can be deployed to computers running the App-V 5.1 client.</span></span>

-   <span data-ttu-id="e1829-111">기존 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-111">Upgrade existing packages.</span></span> <span data-ttu-id="e1829-112">시퀀서를 실행 하는 컴퓨터에 기존 패키지를 확장 한 다음 최신 버전을 만들기 위해 응용 프로그램을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-112">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="e1829-113">기존 패키지와 연결 된 구성 정보를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-113">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="e1829-114">예를 들어 바로 가기를 추가 하거나 파일 형식 연결을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-114">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="e1829-115">**참고**  로밍을 허용 하려면 바로 가기를 만들고 사용 가능한 네트워크 위치에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-115">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="e1829-116">바로 가기를 만들어 개인 위치에 저장 한 경우 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 패키지를 로컬로 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-116">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.1 client.</span></span>
 
-   <span data-ttu-id="e1829-117">기존 가상 패키지를 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-117">Convert existing virtual packages.</span></span>

<span data-ttu-id="e1829-118">시퀀서는 시퀀싱 하는 동안 임시 파일을 저장 **하는 데** **% TMP% \\ 긁힘** 또는 \**% temp% \** ? 임시 디렉터리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-118">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="e1829-119">Sequencer를 실행 하는 컴퓨터에서 예상 되는 응용 프로그램 설치 요구 사항에 해당 하는 무료 디스크 공간을 사용 하 여 이러한 디렉터리를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-119">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="e1829-120">다른 하드 드라이브 파티션에서 temp 디렉터리와 Temp 디렉터리를 구성 하면 시퀀싱 하는 동안 성능이 향상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-120">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="e1829-121">시퀀서를 사용 하 여 새 가상 응용 프로그램을 만들면 다음과 같은 나열 된 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-121">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="e1829-122">이러한 파일은 App-v 5.1 패키지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-122">These files comprise the App-V 5.1 package.</span></span>

-   <span data-ttu-id="e1829-123">.msi 파일.</span><span class="sxs-lookup"><span data-stu-id="e1829-123">.msi file.</span></span> <span data-ttu-id="e1829-124">이 Windows Installer (.msi) 파일은 시퀀서에서 생성 되며 대상 컴퓨터에 가상 패키지를 설치 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-124">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="e1829-125">파일을 Report.xml 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-125">Report.xml file.</span></span> <span data-ttu-id="e1829-126">이 파일에서 sequencer는 시퀀싱 중에 발견 된 모든 문제, 경고 및 오류를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-126">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="e1829-127">패키지를 만든 후에 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-127">It displays the information after the package has been created.</span></span> <span data-ttu-id="e1829-128">이 보고서에서 진단 및 문제 해결을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-128">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="e1829-129">appv 파일.</span><span class="sxs-lookup"><span data-stu-id="e1829-129">.appv file.</span></span> <span data-ttu-id="e1829-130">가상 응용 프로그램 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-130">This is the virtual application file.</span></span>

-   <span data-ttu-id="e1829-131">배포 구성 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-131">Deployment configuration file.</span></span> <span data-ttu-id="e1829-132">배포 구성 파일에서는 가상 응용 프로그램이 대상 컴퓨터에 배포 되는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-132">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="e1829-133">사용자 구성 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-133">User configuration file.</span></span> <span data-ttu-id="e1829-134">사용자 구성 파일은 대상 컴퓨터에서 가상 응용 프로그램을 실행 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-134">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="e1829-135">**중요**  패키지 변환기가 안전한 위치 및 디렉터리로 사용 하도록% TMP% 및% TEMP% 폴더를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-135">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="e1829-136">보안 위치는 관리자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-136">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="e1829-137">또한 패키지를 시퀀싱 하는 경우 안전한 위치에 패키지를 저장 하거나 변환 및 모니터링 프로세스 중에 다른 사용자가 로그인 할 수 없도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-137">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span> 

<span data-ttu-id="e1829-138">Sequencer 콘솔의 **옵션** 대화 상자에는 다음 탭이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-138">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="e1829-139">**일반**.</span><span class="sxs-lookup"><span data-stu-id="e1829-139">**General**.</span></span> <span data-ttu-id="e1829-140">이 탭을 사용 하면 시퀀싱 하는 동안 Microsoft Update를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-140">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="e1829-141">**패키지 버전을 파일 이름에** 추가를 선택 하 여 시퀀싱 되는 가상화 된 패키지에 버전 번호를 추가할 순서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-141">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="e1829-142">권한 부여 여부를 묻지 않고 패키지 가속기를 사용 하 여 가상화 된 패키지를 만들려면 **항상 Package accelerator 원본 신뢰** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-142">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="e1829-143">**중요**  App-V 4.6을 사용 하 여 만든 패키지 가속기는 App-v 5.1에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-143">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.1.</span></span>     

-   <span data-ttu-id="e1829-144">**항목 구문 분석**.</span><span class="sxs-lookup"><span data-stu-id="e1829-144">**Parse Items**.</span></span> <span data-ttu-id="e1829-145">이 탭에는 가상 환경에서 구문 분석 되거나 토큰화 되는 관련 파일 경로 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-145">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="e1829-146">토큰은 **고급 편집**의 **패키지 파일** 탭을 사용 하 여 파일을 추가 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-146">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="e1829-147">**제외 항목**</span><span class="sxs-lookup"><span data-stu-id="e1829-147">**Exclusion Items**.</span></span> <span data-ttu-id="e1829-148">이 탭을 사용 하 여 시퀀싱 하는 동안 모니터링할 수 없는 폴더와 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-148">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="e1829-149">패키지의 Local App Data 폴더에 저장 된 로컬 응용 프로그램 데이터를 추가 하려면 **새로 만들기** 를 클릭 하 고 위치 및 연결 된 **매핑 유형을**지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-149">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="e1829-150">일부 패키지에는이 옵션이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-150">This option is required for some packages.</span></span>

<span data-ttu-id="e1829-151">App-v 5.1는 Microsoft Windows 서비스를 포함 하는 응용 프로그램을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-151">App-V 5.1 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="e1829-152">응용 프로그램에 Windows 서비스가 포함 된 경우 시퀀서에서 모니터링 하는 동안 설치 되는 경우 서비스가 시퀀싱 된 가상 패키지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-152">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="e1829-153">가상 응용 프로그램이 처음 실행할 때 Windows 서비스를 만드는 경우 나중에 설치 후에 Windows 서비스가 패키지에 추가 되도록 sequencer가 모니터링 되는 동안 응용 프로그램이 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-153">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="e1829-154">로컬 시스템 계정으로 실행 되는 서비스만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-154">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="e1829-155">자동 시작 또는 지연 된 자동 시작에 대해 구성 된 서비스는 패키지의 첫 번째 가상 응용 프로그램이 패키지의 가상 환경 내에서 실행 되기 전에 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-155">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="e1829-156">응용 프로그램에서 요청 시 시작 하도록 구성 된 Windows 서비스는 패키지 내부의 가상 응용 프로그램이 API 호출을 통해 서비스를 시작할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-156">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="e1829-157">App-V 5.1을 사용하여 새 응용 프로그램을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="e1829-157">How to Sequence a New Application with App-V 5.1</span></span>](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)

## <a href="" id="---------app-v-5-1-shell-extension-support"></a> <span data-ttu-id="e1829-158">App-v 5.1 셸 확장 지원</span><span class="sxs-lookup"><span data-stu-id="e1829-158">App-V 5.1shell extension support</span></span>


<span data-ttu-id="e1829-159">앱-V 5.1은 셸 확장을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-159">App-V 5.1supports shell extensions.</span></span> <span data-ttu-id="e1829-160">시퀀싱 하는 동안 셸 확장이 검색 되 고 패키지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-160">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="e1829-161">셸 확장은 시퀀싱 프로세스 중 패키지에 자동으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-161">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="e1829-162">패키지를 게시 하면 사용자가 응용 프로그램이 로컬에 설치 되어 있는 것과 동일한 기능을 제공 하는 셸 확장이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-162">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="e1829-163">셸 확장 사용에 대 한 요구 사항:</span><span class="sxs-lookup"><span data-stu-id="e1829-163">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="e1829-164">포함 된 셸 확장을 포함 하는 패키지는 전체적으로 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-164">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="e1829-165">셸 확장 기능을 사용 하도록 설정 하려면 응용 프로그램에 추가 설정이 나 클라이언트에 대 한 구성이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-165">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="e1829-166">응용 프로그램, Sequencer, App-v 클라이언트의 "비트"는 일치 해야 하며 그렇지 않으면 셸 확장이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-166">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="e1829-167">예:</span><span class="sxs-lookup"><span data-stu-id="e1829-167">For example:</span></span>

    -   <span data-ttu-id="e1829-168">응용 프로그램 버전은 64 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-168">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="e1829-169">Sequencer가 64 비트 컴퓨터에서 실행 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-169">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="e1829-170">패키지가 64 비트 App-v 클라이언트 컴퓨터로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-170">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="e1829-171">다음 표에는 지원 되는 셸 확장이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-171">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1829-172">처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-172">Handler</span></span></th>
<th align="left"><span data-ttu-id="e1829-173">설명</span><span class="sxs-lookup"><span data-stu-id="e1829-173">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e1829-174">상황에 맞는 메뉴 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-174">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-175">상황에 맞는 메뉴에 메뉴 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-175">Adds menu items to the context menu.</span></span> <span data-ttu-id="e1829-176">이 메서드는 상황에 맞는 메뉴가 표시 되기 전에 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-176">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e1829-177">끌어서 놓기 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-177">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-178">마우스 오른쪽 단추를 클릭 하 고 끌어서 놓기 작업을 제어 하 고 표시 되는 상황에 맞는 메뉴를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-178">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e1829-179">놓기 대상 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-179">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-180">파일 등의 놓기 대상 위에 데이터 개체를 끌어서 놓은 후의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-180">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e1829-181">데이터 개체 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-181">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-182">파일을 클립보드에 복사 하거나 놓기 대상 위에 끌어 놓은 후의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-182">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="e1829-183">놓기 대상에 추가 클립보드 형식을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-183">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e1829-184">속성 시트 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-184">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-185">개체의 속성 시트 대화 상자에 페이지를 바꾸거나 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-185">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e1829-186">정보 팁 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-186">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-187">마우스 커서를 사용 하 여 항목에 대 한 플래그 및 정보 팁을 검색 하 고 팝업 도구 설명 내에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-187">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e1829-188">열 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-188">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-189"><strong>Windows 탐색기 세부 정보 보기에서 사용자 지정 열을 만들고 표시할 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e1829-189">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="e1829-190">이를 사용 하 여 정렬 및 그룹화를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-190">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e1829-191">미리 보기 처리기</span><span class="sxs-lookup"><span data-stu-id="e1829-191">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1829-192">Windows 탐색기 미리 보기 창에 파일의 미리 보기를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-192">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="e1829-193">CoW (Write on Copy) 파일 확장명 지원</span><span class="sxs-lookup"><span data-stu-id="e1829-193">Copy on Write (CoW) file extension support</span></span>

<span data-ttu-id="e1829-194">CoW (write on Copy) 파일 확장명을 사용 하면 앱-V 5.1를 사용할 때 가상 패키지에 포함 된 특정 위치에 동적으로 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-194">Copy on write (CoW) file extensions allow App-V 5.1 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="e1829-195">다음 표에서는 VFS 디렉터리 아래에 있는 가상 패키지에 있을 수 있지만 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 업데이트할 수 없는 파일 형식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-195">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="e1829-196">다른 모든 파일 및 디렉터리를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-196">All other files and directories can be modified.</span></span>

| <span data-ttu-id="e1829-197">파일 형식</span><span class="sxs-lookup"><span data-stu-id="e1829-197">File Type</span></span>     |               |               |               |               |               |
|------------   |-------------  |-------------  |------------   |------------   |------------   |
| <span data-ttu-id="e1829-198">acm</span><span class="sxs-lookup"><span data-stu-id="e1829-198">.acm</span></span>          | <span data-ttu-id="e1829-199">global.asa</span><span class="sxs-lookup"><span data-stu-id="e1829-199">.asa</span></span>          | <span data-ttu-id="e1829-200">.asp</span><span class="sxs-lookup"><span data-stu-id="e1829-200">.asp</span></span>          | <span data-ttu-id="e1829-201">.aspx</span><span class="sxs-lookup"><span data-stu-id="e1829-201">.aspx</span></span>         | <span data-ttu-id="e1829-202">ax</span><span class="sxs-lookup"><span data-stu-id="e1829-202">.ax</span></span>           | <span data-ttu-id="e1829-203">.bat</span><span class="sxs-lookup"><span data-stu-id="e1829-203">.bat</span></span>          |
| <span data-ttu-id="e1829-204">.cer</span><span class="sxs-lookup"><span data-stu-id="e1829-204">.cer</span></span>          | <span data-ttu-id="e1829-205">.chm</span><span class="sxs-lookup"><span data-stu-id="e1829-205">.chm</span></span>          | <span data-ttu-id="e1829-206">clb</span><span class="sxs-lookup"><span data-stu-id="e1829-206">.clb</span></span>          | <span data-ttu-id="e1829-207">.cmd</span><span class="sxs-lookup"><span data-stu-id="e1829-207">.cmd</span></span>          | <span data-ttu-id="e1829-208">.cnt</span><span class="sxs-lookup"><span data-stu-id="e1829-208">.cnt</span></span>          | <span data-ttu-id="e1829-209">cnv</span><span class="sxs-lookup"><span data-stu-id="e1829-209">.cnv</span></span>          |
| <span data-ttu-id="e1829-210">.com</span><span class="sxs-lookup"><span data-stu-id="e1829-210">.com</span></span>          | <span data-ttu-id="e1829-211">.cpl</span><span class="sxs-lookup"><span data-stu-id="e1829-211">.cpl</span></span>          | <span data-ttu-id="e1829-212">. cpx</span><span class="sxs-lookup"><span data-stu-id="e1829-212">.cpx</span></span>          | <span data-ttu-id="e1829-213">.crt</span><span class="sxs-lookup"><span data-stu-id="e1829-213">.crt</span></span>          | <span data-ttu-id="e1829-214">.dll</span><span class="sxs-lookup"><span data-stu-id="e1829-214">.dll</span></span>          | <span data-ttu-id="e1829-215">.drv</span><span class="sxs-lookup"><span data-stu-id="e1829-215">.drv</span></span>          |
| <span data-ttu-id="e1829-216">. esc</span><span class="sxs-lookup"><span data-stu-id="e1829-216">.esc</span></span>          | <span data-ttu-id="e1829-217">.exe</span><span class="sxs-lookup"><span data-stu-id="e1829-217">.exe</span></span>          | <span data-ttu-id="e1829-218">.fon</span><span class="sxs-lookup"><span data-stu-id="e1829-218">.fon</span></span>          | <span data-ttu-id="e1829-219">.grp</span><span class="sxs-lookup"><span data-stu-id="e1829-219">.grp</span></span>          | <span data-ttu-id="e1829-220">.hlp</span><span class="sxs-lookup"><span data-stu-id="e1829-220">.hlp</span></span>          | <span data-ttu-id="e1829-221">.hta</span><span class="sxs-lookup"><span data-stu-id="e1829-221">.hta</span></span>          |
| <span data-ttu-id="e1829-222">ime</span><span class="sxs-lookup"><span data-stu-id="e1829-222">.ime</span></span>          | <span data-ttu-id="e1829-223">.inf</span><span class="sxs-lookup"><span data-stu-id="e1829-223">.inf</span></span>          | <span data-ttu-id="e1829-224">.ins</span><span class="sxs-lookup"><span data-stu-id="e1829-224">.ins</span></span>          | <span data-ttu-id="e1829-225">.isp</span><span class="sxs-lookup"><span data-stu-id="e1829-225">.isp</span></span>          | <span data-ttu-id="e1829-226">. 해당</span><span class="sxs-lookup"><span data-stu-id="e1829-226">.its</span></span>          | <span data-ttu-id="e1829-227">.js</span><span class="sxs-lookup"><span data-stu-id="e1829-227">.js</span></span>           |
| <span data-ttu-id="e1829-228">.jse</span><span class="sxs-lookup"><span data-stu-id="e1829-228">.jse</span></span>          | <span data-ttu-id="e1829-229">.lnk</span><span class="sxs-lookup"><span data-stu-id="e1829-229">.lnk</span></span>          | <span data-ttu-id="e1829-230">.msc</span><span class="sxs-lookup"><span data-stu-id="e1829-230">.msc</span></span>          | <span data-ttu-id="e1829-231">.msi</span><span class="sxs-lookup"><span data-stu-id="e1829-231">.msi</span></span>          | <span data-ttu-id="e1829-232">.msp</span><span class="sxs-lookup"><span data-stu-id="e1829-232">.msp</span></span>          | <span data-ttu-id="e1829-233">.mst</span><span class="sxs-lookup"><span data-stu-id="e1829-233">.mst</span></span>          |
| <span data-ttu-id="e1829-234">.mui</span><span class="sxs-lookup"><span data-stu-id="e1829-234">.mui</span></span>          | <span data-ttu-id="e1829-235">nls</span><span class="sxs-lookup"><span data-stu-id="e1829-235">.nls</span></span>          | <span data-ttu-id="e1829-236">.ocx</span><span class="sxs-lookup"><span data-stu-id="e1829-236">.ocx</span></span>          | <span data-ttu-id="e1829-237">. p a l</span><span class="sxs-lookup"><span data-stu-id="e1829-237">.pal</span></span>          | <span data-ttu-id="e1829-238">.pcd</span><span class="sxs-lookup"><span data-stu-id="e1829-238">.pcd</span></span>          | <span data-ttu-id="e1829-239">.pif</span><span class="sxs-lookup"><span data-stu-id="e1829-239">.pif</span></span>          |
| <span data-ttu-id="e1829-240">.reg</span><span class="sxs-lookup"><span data-stu-id="e1829-240">.reg</span></span>          | <span data-ttu-id="e1829-241">.scf</span><span class="sxs-lookup"><span data-stu-id="e1829-241">.scf</span></span>          | <span data-ttu-id="e1829-242">.scr</span><span class="sxs-lookup"><span data-stu-id="e1829-242">.scr</span></span>          | <span data-ttu-id="e1829-243">sct</span><span class="sxs-lookup"><span data-stu-id="e1829-243">.sct</span></span>          | <span data-ttu-id="e1829-244">.shb</span><span class="sxs-lookup"><span data-stu-id="e1829-244">.shb</span></span>          | <span data-ttu-id="e1829-245">.shs</span><span class="sxs-lookup"><span data-stu-id="e1829-245">.shs</span></span>          |
| <span data-ttu-id="e1829-246">.sys</span><span class="sxs-lookup"><span data-stu-id="e1829-246">.sys</span></span>          | <span data-ttu-id="e1829-247">.tlb</span><span class="sxs-lookup"><span data-stu-id="e1829-247">.tlb</span></span>          | <span data-ttu-id="e1829-248">tsp</span><span class="sxs-lookup"><span data-stu-id="e1829-248">.tsp</span></span>          | <span data-ttu-id="e1829-249">.url</span><span class="sxs-lookup"><span data-stu-id="e1829-249">.url</span></span>          | <span data-ttu-id="e1829-250">.vb</span><span class="sxs-lookup"><span data-stu-id="e1829-250">.vb</span></span>           | <span data-ttu-id="e1829-251">.vbe</span><span class="sxs-lookup"><span data-stu-id="e1829-251">.vbe</span></span>          |
| <span data-ttu-id="e1829-252">.vbs</span><span class="sxs-lookup"><span data-stu-id="e1829-252">.vbs</span></span>          | <span data-ttu-id="e1829-253">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="e1829-253">.vsmacros</span></span>     | <span data-ttu-id="e1829-254">.ws</span><span class="sxs-lookup"><span data-stu-id="e1829-254">.ws</span></span>           | <span data-ttu-id="e1829-255">.wsf</span><span class="sxs-lookup"><span data-stu-id="e1829-255">.wsf</span></span>          | <span data-ttu-id="e1829-256">.wsh</span><span class="sxs-lookup"><span data-stu-id="e1829-256">.wsh</span></span>          |               |


## <span data-ttu-id="e1829-257">기존 가상 응용 프로그램 패키지 수정</span><span class="sxs-lookup"><span data-stu-id="e1829-257">Modifying an existing virtual application package</span></span>


<span data-ttu-id="e1829-258">시퀀서를 사용 하 여 기존 패키지를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-258">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="e1829-259">이 작업을 수행 하는 컴퓨터는 응용 프로그램을 만드는 데 사용한 컴퓨터의 칩 아키텍처와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-259">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="e1829-260">예를 들어 처음에 64 비트 운영 체제를 실행 하는 컴퓨터를 사용 하 여 패키지를 시퀀싱 한 경우 64 비트 운영 체제를 실행 하는 컴퓨터를 사용 하 여 패키지를 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-260">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="e1829-261">기존 가상 응용 프로그램 패키지를 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="e1829-261">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-51.md)

## <span data-ttu-id="e1829-262">프로젝트 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="e1829-262">Creating a project template</span></span>


<span data-ttu-id="e1829-263">Appvt 파일은 일반적으로 적용 되는 사용자 지정 설정을 저장 하는 데 사용할 수 있는 프로젝트 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-263">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="e1829-264">이후 sequencings 이러한 설정을 더 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-264">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="e1829-265">App-v 5.1 Application 가속기는 응용 프로그램에 따라 다르며 앱-v 5.1 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있기 때문에 앱-V 5.1 프로젝트 템플릿은 앱-V 5.1 응용 프로그램 가속기와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-265">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="e1829-266">또한 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들 때는 프로젝트 템플릿을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-266">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="e1829-267">다음과 같은 일반 설정은 App-v 5.1 프로젝트 템플릿과 함께 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-267">The following general settings are saved with an App-V 5.1 project template:</span></span>

<span data-ttu-id="e1829-268">템플릿에서 여러 설정을 지정 하 고 저장할 수 있는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-268">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="e1829-269">**고급 모니터링 옵션**</span><span class="sxs-lookup"><span data-stu-id="e1829-269">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="e1829-270">모니터링 하는 동안 Microsoft Update를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-270">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="e1829-271">로컬 조작 허용 옵션 설정 저장</span><span class="sxs-lookup"><span data-stu-id="e1829-271">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="e1829-272">**일반 옵션**</span><span class="sxs-lookup"><span data-stu-id="e1829-272">**General Options**.</span></span> <span data-ttu-id="e1829-273">**Windows Installer**를 사용 하도록 설정 하 고 **패키지 버전을 파일 이름에 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-273">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="e1829-274">제외 항목</span><span class="sxs-lookup"><span data-stu-id="e1829-274">Exclusion Items.</span></span>** <span data-ttu-id="e1829-275">제외 패턴 목록을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-275">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="e1829-276">프로젝트 템플릿을 만들고 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e1829-276">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template51.md)

## <span data-ttu-id="e1829-277">패키지 가속기 만들기</span><span class="sxs-lookup"><span data-stu-id="e1829-277">Creating a package accelerator</span></span>


<span data-ttu-id="e1829-278">**참고**  이전 버전의 App-v를 사용 하 여 만든 패키지 가속기를 App-V 5.1를 사용 하 여 다시 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-278">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.1.</span></span>

<span data-ttu-id="e1829-279">앱-V 5.1 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 자동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-279">You can use App-V 5.1 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="e1829-280">패키지 가속기를 성공적으로 만들었으면 패키지 가속기를 다시 사용 하 고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-280">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="e1829-281">일부 경우에는 패키지 가속기를 만들기 위해 시퀀서를 실행 하는 컴퓨터에 로컬로 응용 프로그램을 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-281">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="e1829-282">이러한 경우에는 먼저 설치 미디어를 사용 하 여 패키지 가속기를 만들려고 시도해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-282">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="e1829-283">누락 된 파일이 여러 개 필요한 경우 시퀀서를 실행 하는 컴퓨터에 로컬로 응용 프로그램을 설치한 다음 패키지 가속기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-283">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="e1829-284">패키지 가속기를 성공적으로 만들었으면 패키지 가속기를 다시 사용 하 고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-284">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="e1829-285">앱-V 5.1 패키지 가속기를 만드는 것은 고급 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-285">Creating App-V 5.1 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="e1829-286">패키지 가속기에는 암호와 사용자 관련 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-286">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="e1829-287">따라서 패키지 가속기 및 관련 설치 미디어를 안전한 위치에 저장 해야 하며, 앱을 만든 후에는 패키지 가속기를 만들고 디지털 서명을 하 여 App-v 5.1 패키지 가속기가 적용 될 때 게시자를 확인할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-287">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.1 Package Accelerator is applied.</span></span>

[<span data-ttu-id="e1829-288">패키지 가속기를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="e1829-288">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator51.md)

[<span data-ttu-id="e1829-289">App-V 패키지 가속기를 사용하여 가상 응용 프로그램 패키지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="e1829-289">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)

## <span data-ttu-id="e1829-290">Sequencer 오류 보고</span><span class="sxs-lookup"><span data-stu-id="e1829-290">Sequencer error reporting</span></span>


<span data-ttu-id="e1829-291">App-v 5.1 시퀀서는 시퀀싱 중에 일반적인 시퀀싱 문제를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-291">The App-V 5.1 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="e1829-292">시퀀싱 마법사의 끝에 있는 **설치 보고서** 페이지에는 문제의 심각도에 따라 **오류**, **경고**및 **정보** 로 분류 된 진단 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-292">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="e1829-293">Windows 이벤트 뷰어를 사용 하 여 시퀀싱 오류에 대 한 추가 정보를 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1829-293">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>


## <a href="" id="other-resources-for-the-app-v-5-1-sequencer-"></a><span data-ttu-id="e1829-294">앱-V 5.1 시퀀서에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="e1829-294">Other resources for the App-V 5.1 sequencer</span></span>


-   [<span data-ttu-id="e1829-295">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="e1829-295">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

