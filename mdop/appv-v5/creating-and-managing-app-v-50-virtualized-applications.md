---
title: App-V 5.0 가상화된 응용 프로그램 만들기 및 관리
description: App-V 5.0 가상화된 응용 프로그램 만들기 및 관리
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814700"
---
# <span data-ttu-id="73b06-103">App-V 5.0 가상화된 응용 프로그램 만들기 및 관리</span><span class="sxs-lookup"><span data-stu-id="73b06-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="73b06-104">Microsoft Application Virtualization (App-v) 5.0 sequencer를 올바르게 배포한 후에는이를 사용 하 여 가상화 된 응용 프로그램으로 실행 되는 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="73b06-105">**참고**  Microsoft Application Virtualization (App-v) 5.0 시퀀서, 모범 사례 순서, 가상 응용 프로그램을 만들고 업데이트 하는 예제를 구성 하는 방법에 대 한 자세한 내용은 [Microsoft Application Virtualization 5.0 시퀀싱 가이드](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 시퀀싱 Guide.docx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73b06-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="73b06-106">응용 프로그램 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="73b06-106">Sequencing an application</span></span>


<span data-ttu-id="73b06-107">앱-V 5.0 Sequencer를 사용 하 여 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="73b06-108">App-v 5.0 클라이언트를 실행 하는 컴퓨터에 배포할 수 있는 가상 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="73b06-109">기존 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-109">Upgrade existing packages.</span></span> <span data-ttu-id="73b06-110">시퀀서를 실행 하는 컴퓨터에 기존 패키지를 확장 한 다음 최신 버전을 만들기 위해 응용 프로그램을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="73b06-111">기존 패키지와 연결 된 구성 정보를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="73b06-112">예를 들어 바로 가기를 추가 하거나 파일 형식 연결을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="73b06-113">**참고**  로밍을 허용 하려면 바로 가기를 만들고 사용 가능한 네트워크 위치에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="73b06-114">바로 가기를 만들어 개인 위치에 저장 한 경우 App-v 5.0 클라이언트를 실행 하는 컴퓨터에 패키지를 로컬로 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="73b06-115">기존 가상 패키지를 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="73b06-116">시퀀서는 시퀀싱 하는 동안 임시 파일을 저장 **하는 데** **% TMP% \\ 긁힘** 또는 \**% temp% \** ? 임시 디렉터리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="73b06-117">Sequencer를 실행 하는 컴퓨터에서 예상 되는 응용 프로그램 설치 요구 사항에 해당 하는 무료 디스크 공간을 사용 하 여 이러한 디렉터리를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="73b06-118">다른 하드 드라이브 파티션에서 temp 디렉터리와 Temp 디렉터리를 구성 하면 시퀀싱 하는 동안 성능이 향상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="73b06-119">시퀀서를 사용 하 여 새 가상 응용 프로그램을 만들면 다음과 같은 나열 된 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="73b06-120">이러한 파일은 App-v 5.0 패키지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="73b06-121">.msi 파일.</span><span class="sxs-lookup"><span data-stu-id="73b06-121">.msi file.</span></span> <span data-ttu-id="73b06-122">이 Windows Installer (.msi) 파일은 시퀀서에서 생성 되며 대상 컴퓨터에 가상 패키지를 설치 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="73b06-123">파일을 Report.xml 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-123">Report.xml file.</span></span> <span data-ttu-id="73b06-124">이 파일에서 sequencer는 시퀀싱 중에 발견 된 모든 문제, 경고 및 오류를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="73b06-125">패키지를 만든 후에 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="73b06-126">이 보고서에서 진단 및 문제 해결을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="73b06-127">appv 파일.</span><span class="sxs-lookup"><span data-stu-id="73b06-127">.appv file.</span></span> <span data-ttu-id="73b06-128">가상 응용 프로그램 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="73b06-129">배포 구성 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-129">Deployment configuration file.</span></span> <span data-ttu-id="73b06-130">배포 구성 파일에서는 가상 응용 프로그램이 대상 컴퓨터에 배포 되는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="73b06-131">사용자 구성 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-131">User configuration file.</span></span> <span data-ttu-id="73b06-132">사용자 구성 파일은 대상 컴퓨터에서 가상 응용 프로그램을 실행 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="73b06-133">**중요**  패키지 변환기가 안전한 위치 및 디렉터리로 사용 하도록% TMP% 및% TEMP% 폴더를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="73b06-134">보안 위치는 관리자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="73b06-135">또한 패키지를 시퀀싱 하는 경우 안전한 위치에 패키지를 저장 하거나 변환 및 모니터링 프로세스 중에 다른 사용자가 로그인 할 수 없도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="73b06-136">Sequencer 콘솔의 **옵션** 대화 상자에는 다음 탭이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="73b06-137">**일반**.</span><span class="sxs-lookup"><span data-stu-id="73b06-137">**General**.</span></span> <span data-ttu-id="73b06-138">이 탭을 사용 하면 시퀀싱 하는 동안 Microsoft Update를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="73b06-139">**패키지 버전을 파일 이름에** 추가를 선택 하 여 시퀀싱 되는 가상화 된 패키지에 버전 번호를 추가할 순서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="73b06-140">권한 부여 여부를 묻지 않고 패키지 가속기를 사용 하 여 가상화 된 패키지를 만들려면 **항상 Package accelerator 원본 신뢰** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="73b06-141">**중요**  App-V 4.6을 사용 하 여 만든 패키지 가속기는 App-v 5.0에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="73b06-142">**항목 구문 분석**.</span><span class="sxs-lookup"><span data-stu-id="73b06-142">**Parse Items**.</span></span> <span data-ttu-id="73b06-143">이 탭에는 가상 환경에서 구문 분석 되거나 토큰화 되는 관련 파일 경로 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="73b06-144">토큰은 **고급 편집**의 **패키지 파일** 탭을 사용 하 여 파일을 추가 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="73b06-145">**제외 항목**</span><span class="sxs-lookup"><span data-stu-id="73b06-145">**Exclusion Items**.</span></span> <span data-ttu-id="73b06-146">이 탭을 사용 하 여 시퀀싱 하는 동안 모니터링할 수 없는 폴더와 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="73b06-147">패키지의 Local App Data 폴더에 저장 된 로컬 응용 프로그램 데이터를 추가 하려면 **새로 만들기** 를 클릭 하 고 위치 및 연결 된 **매핑 유형을**지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="73b06-148">일부 패키지에는이 옵션이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-148">This option is required for some packages.</span></span>

<span data-ttu-id="73b06-149">App-v 5.0는 Microsoft Windows 서비스를 포함 하는 응용 프로그램을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="73b06-150">응용 프로그램에 Windows 서비스가 포함 된 경우 시퀀서에서 모니터링 하는 동안 설치 되는 경우 서비스가 시퀀싱 된 가상 패키지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="73b06-151">가상 응용 프로그램이 처음 실행할 때 Windows 서비스를 만드는 경우 나중에 설치 후에 Windows 서비스가 패키지에 추가 되도록 sequencer가 모니터링 되는 동안 응용 프로그램이 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="73b06-152">로컬 시스템 계정으로 실행 되는 서비스만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="73b06-153">자동 시작 또는 지연 된 자동 시작에 대해 구성 된 서비스는 패키지의 첫 번째 가상 응용 프로그램이 패키지의 가상 환경 내에서 실행 되기 전에 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="73b06-154">응용 프로그램에서 요청 시 시작 하도록 구성 된 Windows 서비스는 패키지 내부의 가상 응용 프로그램이 API 호출을 통해 서비스를 시작할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="73b06-155">App-V 5.0을 사용하여 새 응용 프로그램을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="73b06-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="73b06-156">앱-V 5.0 SP2 셸 확장 지원</span><span class="sxs-lookup"><span data-stu-id="73b06-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="73b06-157">앱-V 5.0 SP2는 셸 확장을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="73b06-158">시퀀싱 하는 동안 셸 확장이 검색 되 고 패키지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="73b06-159">셸 확장은 시퀀싱 프로세스 중 패키지에 자동으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="73b06-160">패키지를 게시 하면 사용자가 응용 프로그램이 로컬에 설치 되어 있는 것과 동일한 기능을 제공 하는 셸 확장이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="73b06-161">셸 확장 사용에 대 한 요구 사항:</span><span class="sxs-lookup"><span data-stu-id="73b06-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="73b06-162">포함 된 셸 확장을 포함 하는 패키지는 전체적으로 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="73b06-163">셸 확장 기능을 사용 하도록 설정 하려면 응용 프로그램에 추가 설정이 나 클라이언트에 대 한 구성이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="73b06-164">응용 프로그램, Sequencer, App-v 클라이언트의 "비트"는 일치 해야 하며 그렇지 않으면 셸 확장이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="73b06-165">예:</span><span class="sxs-lookup"><span data-stu-id="73b06-165">For example:</span></span>

    -   <span data-ttu-id="73b06-166">응용 프로그램 버전은 64 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="73b06-167">Sequencer가 64 비트 컴퓨터에서 실행 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="73b06-168">패키지가 64 비트 App-v 클라이언트 컴퓨터로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="73b06-169">다음 표에는 지원 되는 셸 확장이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="73b06-170">처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="73b06-171">설명</span><span class="sxs-lookup"><span data-stu-id="73b06-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="73b06-172">상황에 맞는 메뉴 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-173">상황에 맞는 메뉴에 메뉴 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="73b06-174">이 메서드는 상황에 맞는 메뉴가 표시 되기 전에 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="73b06-175">끌어서 놓기 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-176">마우스 오른쪽 단추를 클릭 하 고 끌어서 놓기 작업을 제어 하 고 표시 되는 상황에 맞는 메뉴를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="73b06-177">놓기 대상 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-178">파일 등의 놓기 대상 위에 데이터 개체를 끌어서 놓은 후의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="73b06-179">데이터 개체 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-180">파일을 클립보드에 복사 하거나 놓기 대상 위에 끌어 놓은 후의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="73b06-181">놓기 대상에 추가 클립보드 형식을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="73b06-182">속성 시트 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-183">개체의 속성 시트 대화 상자에 페이지를 바꾸거나 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="73b06-184">정보 팁 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-185">마우스 커서를 사용 하 여 항목에 대 한 플래그 및 정보 팁을 검색 하 고 팝업 도구 설명 내에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="73b06-186">열 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-187"><strong>Windows 탐색기 세부 정보 보기에서 사용자 지정 열을 만들고 표시할 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="73b06-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="73b06-188">이를 사용 하 여 정렬 및 그룹화를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="73b06-189">미리 보기 처리기</span><span class="sxs-lookup"><span data-stu-id="73b06-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="73b06-190">Windows 탐색기 미리 보기 창에 파일의 미리 보기를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="73b06-191">CoW (Write on Copy) 파일 확장명 지원</span><span class="sxs-lookup"><span data-stu-id="73b06-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="73b06-192">CoW (write on Copy) 파일 확장명을 사용 하면 앱-V 5.0를 사용할 때 가상 패키지에 포함 된 특정 위치에 동적으로 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="73b06-193">다음 표에서는 VFS 디렉터리 아래에 있는 가상 패키지에 있을 수 있지만 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 업데이트할 수 없는 파일 형식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="73b06-194">다른 모든 파일 및 디렉터리를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="73b06-195">acm</span><span class="sxs-lookup"><span data-stu-id="73b06-195">.acm</span></span>

<span data-ttu-id="73b06-196">global.asa</span><span class="sxs-lookup"><span data-stu-id="73b06-196">.asa</span></span>

<span data-ttu-id="73b06-197">.asp</span><span class="sxs-lookup"><span data-stu-id="73b06-197">.asp</span></span>

<span data-ttu-id="73b06-198">.aspx</span><span class="sxs-lookup"><span data-stu-id="73b06-198">.aspx</span></span>

<span data-ttu-id="73b06-199">ax</span><span class="sxs-lookup"><span data-stu-id="73b06-199">.ax</span></span>

<span data-ttu-id="73b06-200">.bat</span><span class="sxs-lookup"><span data-stu-id="73b06-200">.bat</span></span>

<span data-ttu-id="73b06-201">.cer</span><span class="sxs-lookup"><span data-stu-id="73b06-201">.cer</span></span>

<span data-ttu-id="73b06-202">.chm</span><span class="sxs-lookup"><span data-stu-id="73b06-202">.chm</span></span>

<span data-ttu-id="73b06-203">clb</span><span class="sxs-lookup"><span data-stu-id="73b06-203">.clb</span></span>

<span data-ttu-id="73b06-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="73b06-204">.cmd</span></span>

<span data-ttu-id="73b06-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="73b06-205">.cnt</span></span>

<span data-ttu-id="73b06-206">cnv</span><span class="sxs-lookup"><span data-stu-id="73b06-206">.cnv</span></span>

<span data-ttu-id="73b06-207">.com</span><span class="sxs-lookup"><span data-stu-id="73b06-207">.com</span></span>

<span data-ttu-id="73b06-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="73b06-208">.cpl</span></span>

<span data-ttu-id="73b06-209">. cpx</span><span class="sxs-lookup"><span data-stu-id="73b06-209">.cpx</span></span>

<span data-ttu-id="73b06-210">.crt</span><span class="sxs-lookup"><span data-stu-id="73b06-210">.crt</span></span>

<span data-ttu-id="73b06-211">.dll</span><span class="sxs-lookup"><span data-stu-id="73b06-211">.dll</span></span>

<span data-ttu-id="73b06-212">.drv</span><span class="sxs-lookup"><span data-stu-id="73b06-212">.drv</span></span>

<span data-ttu-id="73b06-213">.exe</span><span class="sxs-lookup"><span data-stu-id="73b06-213">.exe</span></span>

<span data-ttu-id="73b06-214">.fon</span><span class="sxs-lookup"><span data-stu-id="73b06-214">.fon</span></span>

<span data-ttu-id="73b06-215">.grp</span><span class="sxs-lookup"><span data-stu-id="73b06-215">.grp</span></span>

<span data-ttu-id="73b06-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="73b06-216">.hlp</span></span>

<span data-ttu-id="73b06-217">.hta</span><span class="sxs-lookup"><span data-stu-id="73b06-217">.hta</span></span>

<span data-ttu-id="73b06-218">ime</span><span class="sxs-lookup"><span data-stu-id="73b06-218">.ime</span></span>

<span data-ttu-id="73b06-219">.inf</span><span class="sxs-lookup"><span data-stu-id="73b06-219">.inf</span></span>

<span data-ttu-id="73b06-220">.ins</span><span class="sxs-lookup"><span data-stu-id="73b06-220">.ins</span></span>

<span data-ttu-id="73b06-221">.isp</span><span class="sxs-lookup"><span data-stu-id="73b06-221">.isp</span></span>

<span data-ttu-id="73b06-222">. 해당</span><span class="sxs-lookup"><span data-stu-id="73b06-222">.its</span></span>

<span data-ttu-id="73b06-223">.js</span><span class="sxs-lookup"><span data-stu-id="73b06-223">.js</span></span>

<span data-ttu-id="73b06-224">.jse</span><span class="sxs-lookup"><span data-stu-id="73b06-224">.jse</span></span>

<span data-ttu-id="73b06-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="73b06-225">.lnk</span></span>

<span data-ttu-id="73b06-226">.msc</span><span class="sxs-lookup"><span data-stu-id="73b06-226">.msc</span></span>

<span data-ttu-id="73b06-227">.msi</span><span class="sxs-lookup"><span data-stu-id="73b06-227">.msi</span></span>

<span data-ttu-id="73b06-228">.msp</span><span class="sxs-lookup"><span data-stu-id="73b06-228">.msp</span></span>

<span data-ttu-id="73b06-229">.mst</span><span class="sxs-lookup"><span data-stu-id="73b06-229">.mst</span></span>

<span data-ttu-id="73b06-230">.mui</span><span class="sxs-lookup"><span data-stu-id="73b06-230">.mui</span></span>

<span data-ttu-id="73b06-231">nls</span><span class="sxs-lookup"><span data-stu-id="73b06-231">.nls</span></span>

<span data-ttu-id="73b06-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="73b06-232">.ocx</span></span>

<span data-ttu-id="73b06-233">. p a l</span><span class="sxs-lookup"><span data-stu-id="73b06-233">.pal</span></span>

<span data-ttu-id="73b06-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="73b06-234">.pcd</span></span>

<span data-ttu-id="73b06-235">.pif</span><span class="sxs-lookup"><span data-stu-id="73b06-235">.pif</span></span>

<span data-ttu-id="73b06-236">.reg</span><span class="sxs-lookup"><span data-stu-id="73b06-236">.reg</span></span>

<span data-ttu-id="73b06-237">.scf</span><span class="sxs-lookup"><span data-stu-id="73b06-237">.scf</span></span>

<span data-ttu-id="73b06-238">.scr</span><span class="sxs-lookup"><span data-stu-id="73b06-238">.scr</span></span>

<span data-ttu-id="73b06-239">sct</span><span class="sxs-lookup"><span data-stu-id="73b06-239">.sct</span></span>

<span data-ttu-id="73b06-240">.shb</span><span class="sxs-lookup"><span data-stu-id="73b06-240">.shb</span></span>

<span data-ttu-id="73b06-241">.shs</span><span class="sxs-lookup"><span data-stu-id="73b06-241">.shs</span></span>

<span data-ttu-id="73b06-242">.sys</span><span class="sxs-lookup"><span data-stu-id="73b06-242">.sys</span></span>

<span data-ttu-id="73b06-243">.tlb</span><span class="sxs-lookup"><span data-stu-id="73b06-243">.tlb</span></span>

<span data-ttu-id="73b06-244">tsp</span><span class="sxs-lookup"><span data-stu-id="73b06-244">.tsp</span></span>

<span data-ttu-id="73b06-245">.url</span><span class="sxs-lookup"><span data-stu-id="73b06-245">.url</span></span>

<span data-ttu-id="73b06-246">.vb</span><span class="sxs-lookup"><span data-stu-id="73b06-246">.vb</span></span>

<span data-ttu-id="73b06-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="73b06-247">.vbe</span></span>

<span data-ttu-id="73b06-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="73b06-248">.vbs</span></span>

<span data-ttu-id="73b06-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="73b06-249">.vsmacros</span></span>

<span data-ttu-id="73b06-250">.ws</span><span class="sxs-lookup"><span data-stu-id="73b06-250">.ws</span></span>

<span data-ttu-id="73b06-251">. esc</span><span class="sxs-lookup"><span data-stu-id="73b06-251">.esc</span></span>

<span data-ttu-id="73b06-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="73b06-252">.wsf</span></span>

<span data-ttu-id="73b06-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="73b06-253">.wsh</span></span>

 

## <span data-ttu-id="73b06-254">기존 가상 응용 프로그램 패키지 수정</span><span class="sxs-lookup"><span data-stu-id="73b06-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="73b06-255">시퀀서를 사용 하 여 기존 패키지를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="73b06-256">이 작업을 수행 하는 컴퓨터는 응용 프로그램을 만드는 데 사용한 컴퓨터의 칩 아키텍처와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="73b06-257">예를 들어 처음에 64 비트 운영 체제를 실행 하는 컴퓨터를 사용 하 여 패키지를 시퀀싱 한 경우 64 비트 운영 체제를 실행 하는 컴퓨터를 사용 하 여 패키지를 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="73b06-258">기존 가상 응용 프로그램 패키지를 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="73b06-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="73b06-259">프로젝트 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="73b06-259">Creating a project template</span></span>


<span data-ttu-id="73b06-260">Appvt 파일은 일반적으로 적용 되는 사용자 지정 설정을 저장 하는 데 사용할 수 있는 프로젝트 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="73b06-261">이후 sequencings 이러한 설정을 더 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="73b06-262">App-v 5.0 Application 가속기는 응용 프로그램에 따라 다르며 앱-v 5.0 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있기 때문에 앱-V 5.0 프로젝트 템플릿은 앱-V 5.0 응용 프로그램 가속기와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="73b06-263">또한 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들 때는 프로젝트 템플릿을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="73b06-264">다음과 같은 일반 설정은 App-v 5.0 프로젝트 템플릿과 함께 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="73b06-265">템플릿에서 여러 설정을 지정 하 고 저장할 수 있는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="73b06-266">**고급 모니터링 옵션**</span><span class="sxs-lookup"><span data-stu-id="73b06-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="73b06-267">모니터링 하는 동안 Microsoft Update를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="73b06-268">로컬 조작 허용 옵션 설정 저장</span><span class="sxs-lookup"><span data-stu-id="73b06-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="73b06-269">**일반 옵션**</span><span class="sxs-lookup"><span data-stu-id="73b06-269">**General Options**.</span></span> <span data-ttu-id="73b06-270">**Windows Installer**를 사용 하도록 설정 하 고 **패키지 버전을 파일 이름에 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="73b06-271">제외 항목</span><span class="sxs-lookup"><span data-stu-id="73b06-271">Exclusion Items.</span></span>** <span data-ttu-id="73b06-272">제외 패턴 목록을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="73b06-273">프로젝트 템플릿을 만들고 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="73b06-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="73b06-274">패키지 가속기 만들기</span><span class="sxs-lookup"><span data-stu-id="73b06-274">Creating a package accelerator</span></span>


<span data-ttu-id="73b06-275">**참고**  이전 버전의 App-v를 사용 하 여 만든 패키지 가속기를 App-V 5.0를 사용 하 여 다시 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="73b06-276">앱-V 5.0 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 자동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="73b06-277">패키지 가속기를 성공적으로 만들었으면 패키지 가속기를 다시 사용 하 고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="73b06-278">일부 경우에는 패키지 가속기를 만들기 위해 시퀀서를 실행 하는 컴퓨터에 로컬로 응용 프로그램을 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="73b06-279">이러한 경우에는 먼저 설치 미디어를 사용 하 여 패키지 가속기를 만들려고 시도해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="73b06-280">누락 된 파일이 여러 개 필요한 경우 시퀀서를 실행 하는 컴퓨터에 로컬로 응용 프로그램을 설치한 다음 패키지 가속기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="73b06-281">패키지 가속기를 성공적으로 만들었으면 패키지 가속기를 다시 사용 하 고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="73b06-282">앱-V 5.0 패키지 가속기를 만드는 것은 고급 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="73b06-283">패키지 가속기에는 암호와 사용자 관련 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="73b06-284">따라서 패키지 가속기 및 관련 설치 미디어를 안전한 위치에 저장 해야 하며, 앱을 만든 후에는 패키지 가속기를 만들고 디지털 서명을 하 여 App-v 5.0 패키지 가속기가 적용 될 때 게시자를 확인할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="73b06-285">패키지 가속기를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="73b06-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="73b06-286">App-V 패키지 가속기를 사용하여 가상 응용 프로그램 패키지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="73b06-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="73b06-287">Sequencer 오류 보고</span><span class="sxs-lookup"><span data-stu-id="73b06-287">Sequencer error reporting</span></span>


<span data-ttu-id="73b06-288">App-v 5.0 시퀀서는 시퀀싱 중에 일반적인 시퀀싱 문제를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="73b06-289">시퀀싱 마법사의 끝에 있는 **설치 보고서** 페이지에는 문제의 심각도에 따라 **오류**, **경고**및 **정보** 로 분류 된 진단 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="73b06-290">Windows 이벤트 뷰어를 사용 하 여 시퀀싱 오류에 대 한 추가 정보를 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73b06-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="73b06-291">앱-V 5.0 시퀀서에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="73b06-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="73b06-292">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="73b06-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





