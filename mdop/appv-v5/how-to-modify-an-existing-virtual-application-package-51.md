---
title: 기존 가상 응용 프로그램 패키지를 수정하는 방법
description: 기존 가상 응용 프로그램 패키지를 수정하는 방법
author: dansimp
ms.assetid: 6cdeec00-e4fe-4210-b4c7-6ca1ac643ddd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 95963610c8b725412f6d516ee22b1c2f4e186df6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813865"
---
# <span data-ttu-id="899e0-103">기존 가상 응용 프로그램 패키지를 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="899e0-103">How to Modify an Existing Virtual Application Package</span></span>


<span data-ttu-id="899e0-104">이 항목에서는 다음 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-104">This topic explains how to:</span></span>

-   [<span data-ttu-id="899e0-105">기존 가상 응용 프로그램 패키지의 응용 프로그램 업데이트</span><span class="sxs-lookup"><span data-stu-id="899e0-105">Update an application in an existing virtual application package</span></span>](#bkmk-update-app-in-pkg)

-   [<span data-ttu-id="899e0-106">기존 가상 응용 프로그램 패키지와 연결 된 속성 수정</span><span class="sxs-lookup"><span data-stu-id="899e0-106">Modify the properties associated with an existing virtual application package</span></span>](#bkmk-chg-props-in-pkg)

-   [<span data-ttu-id="899e0-107">기존 가상 응용 프로그램 패키지에 새 응용 프로그램 추가</span><span class="sxs-lookup"><span data-stu-id="899e0-107">Add a new application to an existing virtual application package</span></span>](#bkmk-add-app-to-pkg)

**<span data-ttu-id="899e0-108">패키지를 업데이트 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-108">Before you update a package:</span></span>**

-   <span data-ttu-id="899e0-109">가상 응용 프로그램 패키지를 수정 하는 데 필요한 Microsoft Application Virtualization (App-v) Sequencer를 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-109">Ensure that you’ve installed the Microsoft Application Virtualization (App-V) Sequencer, which is required for modifying a virtual application package.</span></span> <span data-ttu-id="899e0-110">App-v 시퀀서를 설치 하려면 Sequencer를 설치 하 [는 방법을](how-to-install-the-sequencer-51beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="899e0-110">To install the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

-   <span data-ttu-id="899e0-111">안전한 위치에 appv 파일을 저장 하 고, 편집을 위해 패키지를 열기 전에 항상 원본을 신뢰 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-111">Save the .appv file in a secure location and always trust the source before trying to open the package for editing.</span></span>

-   <span data-ttu-id="899e0-112">패키지를 업데이트 하면 배포 구성 파일에서 관리 권한 섹션이 실수로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-112">The Managing Authority section is erroneously removed from the deployment configuration file when you update a package.</span></span> <span data-ttu-id="899e0-113">업데이트를 시작 하기 전에 기존 배포 구성 파일에서 관리 기관 섹션을 복사한 다음 변환이 완료 된 후 복사 된 섹션을 새 구성 파일에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-113">Before starting the update, copy the Managing Authority section from the existing deployment configuration file, and then paste the copied section into the new configuration file after the conversion is complete.</span></span>

-   <span data-ttu-id="899e0-114">시퀀서에서 **기존 가상 응용 프로그램 패키지 수정을** 클릭 하 여 패키지를 편집 하 고 변경 내용을 적용 하지 않고 패키지를 닫으면 패키지의 스트리밍 동작이 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-114">If you click **Modify an Existing Virtual Application Package** in the Sequencer in order to edit a package, but then make no changes and close the package, the streaming behavior of the package is changed.</span></span> <span data-ttu-id="899e0-115">StreamMap.xml 파일에서 기본 기능 블록이 제거 되 고 게시 기능 블록에 나열 된 모든 파일이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-115">The primary feature block is removed from the StreamMap.xml file, and any files that were listed in the publishing feature block are removed.</span></span> <span data-ttu-id="899e0-116">원래 패키지의 구성 방법에 관계 없이 스트림 오류가 있는 것 처럼 패키지 하는 편집 된 패키지 환경을 받는 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-116">Users who receive the edited package experience that package as if it were stream-faulted, regardless of how the original package was configured.</span></span>

<a href="" id="bkmk-update-app-in-pkg"></a>**<span data-ttu-id="899e0-117">기존 가상 응용 프로그램 패키지의 응용 프로그램 업데이트</span><span class="sxs-lookup"><span data-stu-id="899e0-117">Update an application in an existing virtual application package</span></span>**

1.  <span data-ttu-id="899e0-118">Sequencer를 실행 하는 컴퓨터에서 **모든 프로그램**을 클릭 하 고 **Microsoft 응용 프로그램 가상화**를 가리킨 다음 **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-118">On the computer that runs the sequencer, click **All Programs**, point to **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="899e0-119">App-v 시퀀서에서 다음 **기존 가상 응용 프로그램 패키지 수정을** 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-119">In the App-V Sequencer, click **Modify an Existing Virtual Application Package** &gt; **Next**.</span></span>

3.  <span data-ttu-id="899e0-120">**작업 선택** 페이지에서 다음 **기존 패키지의 응용 프로그램 업데이트** 를 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-120">On the **Select Task** page, click **Update Application in Existing Package** &gt; **Next**.</span></span>

4.  <span data-ttu-id="899e0-121">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 여 업데이트할 응용 프로그램이 포함 된 가상 응용 프로그램 패키지를 찾은 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-121">On the **Select Package** page, click **Browse** to locate the virtual application package that contains the application to update, and then click **Next**.</span></span>

5.  <span data-ttu-id="899e0-122">**컴퓨터 준비** 페이지에서 응용 프로그램 업데이트가 실패할 수 있는 문제를 검토 하거나 업데이트 된 응용 프로그램에 불필요 한 데이터를 포함 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-122">On the **Prepare Computer** page, review the issues that could cause the application update to fail or cause the updated application to contain unnecessary data.</span></span> <span data-ttu-id="899e0-123">계속 하기 전에 발생할 수 있는 모든 문제를 해결 하세요.</span><span class="sxs-lookup"><span data-stu-id="899e0-123">Resolve all potential issues before you continue.</span></span> <span data-ttu-id="899e0-124">수정 하 고 모든 잠재적인 문제를 해결 한 후 다음 **새로 고침** 을 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-124">After making any corrections and resolving all potential issues, click **Refresh** &gt; **Next**.</span></span>

    <span data-ttu-id="899e0-125">**중요**  바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우에는 먼저 sequencer를 실행 하는 컴퓨터를 검사 하 여 불필요 한 파일이 나 악의적인 파일을 패키지에 추가 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-125">**Important** If you are required to disable virus scanning software, first scan the computer that runs the sequencer to ensure that no unwanted or malicious files are added to the package.</span></span>

6.  <span data-ttu-id="899e0-126">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 응용 프로그램의 업데이트 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-126">On the **Select Installer** page, click **Browse** and specify the update installation file for the application.</span></span> <span data-ttu-id="899e0-127">업데이트에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행할 계획인 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-127">If the update does not have an associated installer file, and if you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

7.  <span data-ttu-id="899e0-128">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자를 사용할 준비가 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 응용 프로그램 업데이트를 설치 하도록 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-128">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application update so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="899e0-129">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행**을 클릭 한 다음 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-129">If additional installation files must be run as part of the installation, click **Run**, and then locate and run the additional installation files.</span></span> <span data-ttu-id="899e0-130">설치가 완료 되 면 **설치 완료**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-130">When you are finished with the installation, select **I am finished installing**.</span></span> <span data-ttu-id="899e0-131">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-131">Click **Next**.</span></span>

    <span data-ttu-id="899e0-132">**참고**  Sequencer는 sequencer를 실행 하는 컴퓨터에서 발생 하는 모든 변경 및 설치를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-132">**Note** The sequencer monitors all changes and installations that occur on the computer that runs the sequencer.</span></span> <span data-ttu-id="899e0-133">여기에는 시퀀싱 마법사 외부에서 수행 되는 변경 및 설치가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-133">This includes any changes and installations that are performed outside of the sequencing wizard.</span></span>

8.  <span data-ttu-id="899e0-134">**설치 보고서** 페이지에서 업데이트 된 가상 응용 프로그램에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-134">On the **Installation Report** page, you can review information about the updated virtual application.</span></span> <span data-ttu-id="899e0-135">**추가 정보**에서 이벤트를 두 번 클릭 하 여 자세한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-135">In **Additional Information**, double-click the event to obtain more detailed information.</span></span> <span data-ttu-id="899e0-136">계속 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-136">To proceed, click **Next**.</span></span>

9.  <span data-ttu-id="899e0-137">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-137">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="899e0-138">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-138">It can take several minutes for all of the applications to run.</span></span> <span data-ttu-id="899e0-139">모든 응용 프로그램이 실행 된 후에 각 응용 프로그램을 닫고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-139">After all applications have run, close each of the applications, and then click **Next**.</span></span>

    <span data-ttu-id="899e0-140">**참고**  이 단계에서 응용 프로그램이 로드 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-140">**Note** You can stop an application from loading during this step.</span></span> <span data-ttu-id="899e0-141">**응용 프로그램 실행** 대화 상자에서 **중지**를 클릭 한 다음 **모든 응용 프로그램 중지** 또는 **이 응용 프로그램만 중지**중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-141">In the **Application Launch** dialog box, click **Stop**, and then select either **Stop all applications** or **Stop this application only**.</span></span>   

10. <span data-ttu-id="899e0-142">패키지 **만들기** 페이지에서 저장 하지 않고 패키지를 수정 하려면 패키지 **편집기를 사용 하 여 저장 하지 않고 계속 패키지를 수정 하려면**확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-142">On the **Create Package** page, to modify the package without saving it, select the check box for **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="899e0-143">이 옵션을 선택 하면 패키지를 저장 하기 전에 수정할 수 있는 앱-V 시퀀서 콘솔에서 패키지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-143">When you select this option, the package opens in the App-V Sequencer console, where you can modify the package before it is saved.</span></span> <span data-ttu-id="899e0-144">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-144">Click **Next**.</span></span>

    <span data-ttu-id="899e0-145">패키지를 즉시 저장 하려면 **지금 기본 저장 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-145">To save the package immediately, select the default **Save the package now**.</span></span> <span data-ttu-id="899e0-146">패키지와 연결할 선택적 **메모** 를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-146">Add optional **Comments** to associate with the package.</span></span> <span data-ttu-id="899e0-147">메모는 응용 프로그램 버전을 식별 하 고 패키지에 대 한 기타 정보를 제공 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-147">Comments are useful to identify the application version and provide other information about the package.</span></span> <span data-ttu-id="899e0-148">기본 **저장 위치** 도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-148">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="899e0-149">기본 위치를 변경 하려면 **찾아보기를** 클릭 하 고 새 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-149">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="899e0-150">**만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-150">Click **Create**.</span></span>

11. <span data-ttu-id="899e0-151">**완료** 페이지에서 **닫기를** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-151">On the **Completion** page, click **Close** to close the wizard.</span></span> <span data-ttu-id="899e0-152">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-152">The package is now available in the sequencer.</span></span>

<a href="" id="bkmk-chg-props-in-pkg"></a>**<span data-ttu-id="899e0-153">기존 가상 응용 프로그램 패키지와 연결 된 속성 수정</span><span class="sxs-lookup"><span data-stu-id="899e0-153">Modify the properties associated with an existing virtual application package</span></span>**

1.  <span data-ttu-id="899e0-154">Sequencer를 실행 하는 컴퓨터에서 **모든 프로그램**을 클릭 하 고 **Microsoft 응용 프로그램 가상화**를 가리킨 다음 **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-154">On the computer that runs the sequencer, click **All Programs**, point to **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="899e0-155">App-v 시퀀서에서 다음 **기존 가상 응용 프로그램 패키지 수정을** 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-155">In the App-V Sequencer, click **Modify an Existing Virtual Application Package** &gt; **Next**.</span></span>

3.  <span data-ttu-id="899e0-156">**작업 선택** 페이지에서 다음 **패키지 편집** 을 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-156">On the **Select Task** page, click **Edit Package** &gt; **Next**.</span></span>

4.  <span data-ttu-id="899e0-157">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 여 수정할 응용 프로그램 속성을 포함 하는 가상 응용 프로그램 패키지를 찾은 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-157">On the **Select Package** page, click **Browse** to locate the virtual application package that contains the application properties to modify, and then click **Edit**.</span></span>

5.  <span data-ttu-id="899e0-158">App-v Sequencer 콘솔에서 필요에 따라 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-158">In the App-V Sequencer console, perform any of the following tasks as needed:</span></span>

    -   <span data-ttu-id="899e0-159">매니페스트 파일을 가져오고 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-159">Import and export the manifest file.</span></span>

    -   <span data-ttu-id="899e0-160">브라우저 도우미 개체를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-160">Enable or disable Browser Helper Objects.</span></span>

    -   <span data-ttu-id="899e0-161">VFS 파일을 가져오거나 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-161">Import or export a VFS file.</span></span>

    -   <span data-ttu-id="899e0-162">디렉터리를 가상 파일 시스템으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-162">Import a directory into the virtual file system.</span></span>

    -   <span data-ttu-id="899e0-163">가상 레지스트리 키 가져오기 및 내보내기</span><span class="sxs-lookup"><span data-stu-id="899e0-163">Import and export virtual registry keys.</span></span>

    -   <span data-ttu-id="899e0-164">패키지 속성 보기.</span><span class="sxs-lookup"><span data-stu-id="899e0-164">View package properties.</span></span>

    -   <span data-ttu-id="899e0-165">연결 된 패키지 파일을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-165">View associated package files.</span></span>

    -   <span data-ttu-id="899e0-166">레지스트리 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-166">Edit registry settings.</span></span>

    -   <span data-ttu-id="899e0-167">추가 패키지 설정 검토 (운영 체제 파일 속성 제외)</span><span class="sxs-lookup"><span data-stu-id="899e0-167">Review additional package settings (except operating system file properties).</span></span>

    -   <span data-ttu-id="899e0-168">가상화 된 레지스트리 키 상태 (재정의 또는 병합)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-168">Set virtualized registry key state (override or merge).</span></span>

    -   <span data-ttu-id="899e0-169">가상화 된 폴더 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-169">Set virtualized folder state.</span></span>

    -   <span data-ttu-id="899e0-170">바로 가기 및 파일 형식 연결을 추가 하거나 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-170">Add or edit shortcuts and file type associations.</span></span>

        <span data-ttu-id="899e0-171">**참고**  바로 가기 또는 파일 형식 연결을 편집 하려면 먼저 업그레이드할 패키지를 열고 새 응용 프로그램을 추가한 다음 최종 편집 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-171">**Note** To edit shortcuts or file type associations, you must first open the package for upgrade to add a new application, and then proceed to the final editing page.</span></span>

6.  <span data-ttu-id="899e0-172">패키지 속성 변경을 마쳤으면 **파일** &gt; **저장** 을 클릭 하 여 패키지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-172">When you finish changing the package properties, click **File** &gt; **Save** to save the package.</span></span>

<a href="" id="bkmk-add-app-to-pkg"></a>**<span data-ttu-id="899e0-173">기존 가상 응용 프로그램 패키지에 새 응용 프로그램 추가</span><span class="sxs-lookup"><span data-stu-id="899e0-173">Add a new application to an existing virtual application package</span></span>**

1.  <span data-ttu-id="899e0-174">Sequencer를 실행 하는 컴퓨터에서 **모든 프로그램**을 클릭 하 고 **Microsoft 응용 프로그램 가상화**를 가리킨 다음 **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-174">On the computer that runs the sequencer, click **All Programs**, point to **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="899e0-175">App-v 시퀀서에서 다음 **기존 가상 응용 프로그램 패키지 수정을** 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-175">In the App-V Sequencer, click **Modify an Existing Virtual Application Package** &gt; **Next**.</span></span>

3.  <span data-ttu-id="899e0-176">**작업 선택** 페이지에서 다음 **새 응용 프로그램 추가** 를 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-176">On the **Select Task** page, click **Add New Application** &gt; **Next**.</span></span>

4.  <span data-ttu-id="899e0-177">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 여 응용 프로그램을 추가할 가상 응용 프로그램 패키지를 찾은 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-177">On the **Select Package** page, click **Browse** to locate the virtual application package to which you will add the application, and then click **Next**.</span></span>

5.  <span data-ttu-id="899e0-178">**컴퓨터 준비** 페이지에서 패키지 만들기에 실패 하거나 수정 된 패키지에 불필요 한 데이터를 포함 하도록 하는 문제를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-178">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or cause the revised package to contain unnecessary data.</span></span> <span data-ttu-id="899e0-179">계속 하기 전에 발생할 수 있는 모든 문제를 해결 하세요.</span><span class="sxs-lookup"><span data-stu-id="899e0-179">Resolve all potential issues before you continue.</span></span> <span data-ttu-id="899e0-180">수정 하 고 모든 잠재적인 문제를 해결 한 후 다음 **새로 고침** 을 클릭 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-180">After making any corrections and resolving all potential issues, click **Refresh** &gt; **Next**.</span></span>

    <span data-ttu-id="899e0-181">**중요**  바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우에는 먼저 sequencer를 실행 하는 컴퓨터를 검사 하 여 불필요 하거나 악의적인 파일이 패키지에 추가 될 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-181">**Important** If you are required to disable virus scanning software, first scan the computer that runs the sequencer to ensure that no unwanted or malicious files can be added to the package.</span></span>

6.  <span data-ttu-id="899e0-182">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 응용 프로그램의 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-182">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="899e0-183">응용 프로그램에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행 하려는 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-183">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

7.  <span data-ttu-id="899e0-184">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자가 준비 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-184">On the **Installation** page, when the sequencer and application installer are ready, install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="899e0-185">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행**을 클릭 하 고 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-185">If additional installation files must be run as part of the installation, click **Run**, and locate and run the additional installation files.</span></span> <span data-ttu-id="899e0-186">설치가 완료 되 면 다음을 **설치 완료** 를 선택 &gt; **Next**합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-186">When you finish the installation, select **I am finished installing** &gt; **Next**.</span></span> <span data-ttu-id="899e0-187">**폴더 찾아보기** 대화 상자에서 응용 프로그램을 설치할 기본 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-187">In the **Browse for Folder** dialog box, specify the primary directory where the application will be installed.</span></span> <span data-ttu-id="899e0-188">기존 버전의 가상 응용 프로그램 패키지를 덮어쓰지 않도록 새 위치에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-188">Ensure that this is a new location so that you don’t overwrite the existing version of the virtual application package.</span></span>

    <span data-ttu-id="899e0-189">**참고**  Sequencer는 sequencer를 실행 하는 컴퓨터에서 발생 하는 모든 변경 및 설치를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-189">**Note** The sequencer monitors all changes and installations that occur on the computer that runs the sequencer.</span></span> <span data-ttu-id="899e0-190">여기에는 시퀀싱 마법사 외부에서 수행 되는 변경 및 설치가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-190">This includes any changes and installations that are performed outside of the sequencing wizard.</span></span>

8.  <span data-ttu-id="899e0-191">**소프트웨어 구성** 페이지에서 패키지에 포함 된 프로그램을 선택적으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-191">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="899e0-192">이 단계에서는 대상 컴퓨터에서 패키지를 배포 하 고 실행 하기 전에 응용 프로그램을 실행 하는 데 필요한 연결 된 라이선스 또는 구성 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-192">This step completes any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="899e0-193">한 번에 모든 프로그램을 실행 하려면 하나 이상의 프로그램을 선택한 다음 **모두 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-193">To run all the programs at the same time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="899e0-194">특정 프로그램을 실행 하려면 실행할 프로그램을 선택한 다음, **선택한 프로그램 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-194">To run specific programs, select the program or programs you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="899e0-195">필요한 구성 작업을 완료 한 다음 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-195">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="899e0-196">모든 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-196">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="899e0-197">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-197">Click **Next**.</span></span>

9.  <span data-ttu-id="899e0-198">**설치 보고서** 페이지에서 업데이트 된 가상 응용 프로그램에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-198">On the **Installation Report** page, you can review information about the updated virtual application.</span></span> <span data-ttu-id="899e0-199">**추가 정보**에서 이벤트를 두 번 클릭 하 여 자세한 정보를 얻고 **다음** 을 클릭 하 여 **사용자 지정** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-199">In **Additional Information**, double-click the event to obtain more detailed information, and then click **Next** to open the **Customize** page.</span></span>

10. <span data-ttu-id="899e0-200">가상 응용 프로그램의 설치 및 구성을 완료 한 경우 **지금 중지** 를 선택 하 고이 절차의 13 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-200">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 13 of this procedure.</span></span> <span data-ttu-id="899e0-201">다음의 설명 된 사용자 지정을 수행 하려면 **사용자 지정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-201">If you want to perform the following described customization, click **Customize**.</span></span>

    <span data-ttu-id="899e0-202">사용자 지정 하는 경우 스트리밍을 위한 가상 패키지를 준비한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-202">If you are customizing, prepare the virtual package for streaming, and then click **Next**.</span></span> <span data-ttu-id="899e0-203">스트리밍을 통해 대상 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 때 환경이 개선 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-203">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

11. <span data-ttu-id="899e0-204">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-204">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="899e0-205">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-205">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="899e0-206">모든 응용 프로그램이 실행 된 후에 각 응용 프로그램을 닫고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-206">After all applications have run, close each of the applications, and then click **Next**.</span></span>

    <span data-ttu-id="899e0-207">**참고**  이 단계에서 응용 프로그램이 로드 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-207">**Note** You can stop an application from loading during this step.</span></span> <span data-ttu-id="899e0-208">**응용 프로그램 실행** 대화 상자에서 **중지** 를 클릭 한 다음 **모든 응용 프로그램 중지** 또는 **이 응용 프로그램만 중지**중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-208">In the **Application Launch** dialog box, click **Stop** and then select either **Stop all applications** or **Stop this application only**.</span></span>

12. <span data-ttu-id="899e0-209">패키지 **만들기** 페이지에서 저장 하지 않고 패키지를 수정 하려면 **패키지 편집기를 사용 하 여 저장 하지 않고 계속 패키지 수정** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-209">On the **Create Package** page, to modify the package without saving it, select the **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="899e0-210">이 옵션을 선택 하면 패키지를 저장 하기 전에 수정할 수 있는 앱-V 시퀀서 콘솔에서 패키지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-210">Selecting this option opens the package in the App-V Sequencer console, where you can modify the package before saving it.</span></span> <span data-ttu-id="899e0-211">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-211">Click **Next**.</span></span>

    <span data-ttu-id="899e0-212">패키지를 즉시 저장 하려면 **지금 기본 저장 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-212">To save the package immediately, select the default **Save the package now**.</span></span> <span data-ttu-id="899e0-213">패키지와 연결할 선택적 **메모** 를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-213">Add optional **Comments** to associate with the package.</span></span> <span data-ttu-id="899e0-214">주석은 패키지에 대 한 응용 프로그램 버전 및 기타 정보를 제공 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-214">Comments are useful for providing application versions and other information about the package.</span></span> <span data-ttu-id="899e0-215">기본 **저장 위치** 도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-215">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="899e0-216">기본 위치를 변경 하려면 **찾아보기를** 클릭 하 고 새 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-216">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="899e0-217">압축 되지 않은 패키지 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-217">The uncompressed package size is displayed.</span></span> <span data-ttu-id="899e0-218">**만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-218">Click **Create**.</span></span>

13. <span data-ttu-id="899e0-219">**완료** 페이지에서 **닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-219">On the **Completion** page, click **Close**.</span></span> <span data-ttu-id="899e0-220">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-220">The package is now available in the sequencer.</span></span>

    <span data-ttu-id="899e0-221">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="899e0-221">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="899e0-222">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-222">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="899e0-223">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="899e0-223">Got an App-V issue?</span></span>** <span data-ttu-id="899e0-224">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="899e0-224">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="899e0-225">관련 항목</span><span class="sxs-lookup"><span data-stu-id="899e0-225">Related topics</span></span>

[<span data-ttu-id="899e0-226">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="899e0-226">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





