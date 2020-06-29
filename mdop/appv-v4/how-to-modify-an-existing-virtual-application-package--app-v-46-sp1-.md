---
title: 기존 가상 응용 프로그램 패키지(App-V 4.6 SP1)를 시퀀싱하는 방법
description: 기존 가상 응용 프로그램 패키지(App-V 4.6 SP1)를 시퀀싱하는 방법
author: dansimp
ms.assetid: f43a9927-4325-4b2d-829f-3068e4e84349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e9d45a32afa240ce7f6fb2ee5dfbc51889c1fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817038"
---
# <span data-ttu-id="5cde5-103">기존 가상 응용 프로그램 패키지(App-V 4.6 SP1)를 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="5cde5-103">How to Modify an Existing Virtual Application Package (App-V 4.6 SP1)</span></span>


<span data-ttu-id="5cde5-104">다음 절차를 사용 하 여 기존 가상 응용 프로그램 패키지를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-104">Use the following procedures to modify an existing virtual application package.</span></span> <span data-ttu-id="5cde5-105">이 절차를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-105">You can use these procedures to:</span></span>

-   <span data-ttu-id="5cde5-106">기존 가상 응용 프로그램 패키지의 일부인 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-106">Update an application that is part of an existing virtual application package.</span></span> <span data-ttu-id="5cde5-107">이 작업을 수행 하려면이 문서의 **"기존 응용 프로그램 패키지에서 응용 프로그램을 업데이트 하려면"** 절차를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="5cde5-107">To perform this task, use the procedure **"To update an application in an existing application package"** in this document.</span></span>

-   <span data-ttu-id="5cde5-108">기존 가상 응용 프로그램 패키지와 연결 된 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-108">Modify the properties associated with an existing virtual application package.</span></span> <span data-ttu-id="5cde5-109">이 작업을 수행 하려면이 문서의 **"기존 가상 응용 프로그램 패키지와 연결 된 속성을 수정 하려면"** 절차를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="5cde5-109">To perform this task, use the procedure **"To modify the properties associated with an existing virtual application package"** in this document.</span></span>

-   <span data-ttu-id="5cde5-110">기존 가상 응용 프로그램 패키지에 새 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-110">Add a new application to an existing virtual application package.</span></span> <span data-ttu-id="5cde5-111">이 작업을 수행 하려면이 문서의 **"기존 가상 응용 프로그램 패키지에 새 응용 프로그램을 추가 하려면"** 절차를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="5cde5-111">To perform this task, use the procedure **"To add a new application to an existing virtual application package"** in this document.</span></span>

<span data-ttu-id="5cde5-112">가상 응용 프로그램 패키지를 수정 하려면 App-v Sequencer가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-112">You must have the App-V Sequencer installed to modify a virtual application package.</span></span> <span data-ttu-id="5cde5-113">App-v 시퀀서를 설치 하는 방법에 대 한 자세한 내용은 [Sequencer를 설치 하는 방법 (app-v 4.6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5cde5-113">For more information about installing the App-V Sequencer, see [How to Install the Sequencer (App-V 4.6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="5cde5-114">기존 가상 응용 프로그램 패키지에서 응용 프로그램을 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="5cde5-114">To update an application in an existing virtual application package</span></span>**

1.  <span data-ttu-id="5cde5-115">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-115">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5cde5-116">App-v 시퀀서에서 **기존 가상 응용 프로그램 패키지 수정을**클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-116">In the App-V Sequencer, click **Modify an Existing Virtual Application Package**, and then click **Next**.</span></span>

3.  <span data-ttu-id="5cde5-117">**작업 선택** 페이지에서 **기존 패키지의 응용 프로그램 업데이트**를 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-117">On the **Select Task** page, click **Update Application in Existing Package**, and then click **Next**.</span></span>

4.  <span data-ttu-id="5cde5-118">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 여 업데이트 하려는 응용 프로그램이 포함 된 가상 응용 프로그램 패키지를 찾은 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-118">On the **Select Package** page, click **Browse** to locate the virtual application package that contains the application that you want to update, and then click **Next**.</span></span>

5.  <span data-ttu-id="5cde5-119">**컴퓨터 준비** 페이지에서 응용 프로그램 업데이트가 실패할 수 있는 문제를 검토 하거나 응용 프로그램 업데이트에 불필요 한 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-119">On the **Prepare Computer** page, review the issues that could cause the application update to fail, or for the application update to contain unnecessary data.</span></span> <span data-ttu-id="5cde5-120">계속 하기 전에 모든 잠재적인 문제를 해결 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-120">We strongly recommend that you resolve all potential issues before you continue.</span></span> <span data-ttu-id="5cde5-121">충돌을 수정한 후 표시 되는 정보를 업데이트 하려면 **새로 고침**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-121">After you have fixed the conflicts, to update the information that is displayed, click **Refresh**.</span></span> <span data-ttu-id="5cde5-122">발생할 수 있는 모든 문제를 해결 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-122">After you have resolved all potential issues, click **Next**.</span></span>

    <span data-ttu-id="5cde5-123">**중요**  바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우 시퀀서를 실행 하는 컴퓨터를 검사 하 여 원치 않는 파일이 나 악의적인 파일을 패키지에 추가 하지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-123">**Important** If you are required to disable virus scanning software, scan the computer running the sequencer to ensure that no unwanted or malicious files are added to the package.</span></span>

     

6.  <span data-ttu-id="5cde5-124">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 응용 프로그램의 업데이트 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-124">On the **Select Installer** page, click **Browse** and specify the update installation file for the application.</span></span> <span data-ttu-id="5cde5-125">업데이트에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행 하려는 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-125">If the update does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

7.  <span data-ttu-id="5cde5-126">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자가 준비 되 면 응용 프로그램 업데이트를 설치 하 여 sequencer가 설치 프로세스를 모니터링할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-126">On the **Installation** page, when the sequencer and application installer are ready, install the application update so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="5cde5-127">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행** 을 클릭 하 고 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-127">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="5cde5-128">설치가 완료 되 면 **설치 완료**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-128">When you are finished with the installation, select **I am finished installing**.</span></span> <span data-ttu-id="5cde5-129">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-129">Click **Next**.</span></span>

    <span data-ttu-id="5cde5-130">**참고**  Sequencer는 시퀀싱 마법사 외부에서 수행 되는 변경 및 설치를 비롯 하 여 sequencer를 실행 하는 컴퓨터에 모든 변경 및 설치를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-130">**Note** The sequencer monitors all changes and installations to the computer running the sequencer, including the changes and installations that are performed outside of the sequencing wizard.</span></span>

     

8.  <span data-ttu-id="5cde5-131">**설치 보고서** 페이지에서 방금 업데이트 한 가상 응용 프로그램에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-131">On the **Installation Report** page, you can review information about the virtual application you just updated.</span></span> <span data-ttu-id="5cde5-132">**추가 정보**에 표시 되는 정보에 대 한 자세한 설명을 보려면 이벤트를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-132">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="5cde5-133">정보를 검토 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-133">After you have reviewed the information, click **Next**.</span></span>

9.  <span data-ttu-id="5cde5-134">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-134">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="5cde5-135">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-135">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="5cde5-136">모든 응용 프로그램이 실행 된 후에 각 응용 프로그램을 닫고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-136">After all applications have run, close each of the applications, and then click **Next**.</span></span>

    <span data-ttu-id="5cde5-137">**참고**  이 단계에서 응용 프로그램이 로드 되지 않도록 하려면 **응용 프로그램 실행** 대화 상자에서 **중지**를 클릭 한 후 다음 옵션 중 하나를 클릭 하 고, **모든 응용 프로그램을 중지** 하거나, 원하는 항목에 따라 **이 응용 프로그램**을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-137">**Note** If you want to stop an application from loading during this step, in the **Application Launch** dialog box, click **Stop**, and then click one of the following options, **Stop all applications** or **Stop this application only**, depending on what you want.</span></span>

     

10. <span data-ttu-id="5cde5-138">패키지 **만들기** 페이지에서 저장 하지 않고 패키지를 수정 하려면 **패키지 편집기를 사용 하 여 저장 하지 않고 계속 패키지 수정** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-138">On the **Create Package** page, to modify the package without saving it, select the **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="5cde5-139">이 옵션을 선택 하면 패키지를 저장 하기 전에 수정할 수 있도록 Sequencer 콘솔의 패키지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-139">When you select this option, the package in the Sequencer console opens so that you can modify the package before it is saved.</span></span> <span data-ttu-id="5cde5-140">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-140">Click **Next**.</span></span>

    <span data-ttu-id="5cde5-141">패키지를 즉시 저장 하려면 **지금 기본 저장 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-141">To save the package immediately, select the default **Save the package now**.</span></span> <span data-ttu-id="5cde5-142">패키지와 연결 되는 선택적 **메모** 를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-142">Add optional **Comments** that will be associated with the package.</span></span> <span data-ttu-id="5cde5-143">메모는 패키지에 대 한 버전 및 기타 정보를 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-143">Comments are useful for identifying version and other information about the package.</span></span> <span data-ttu-id="5cde5-144">기본 **저장 위치** 도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-144">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="5cde5-145">기본 위치를 변경 하려면 **찾아보기를** 클릭 하 고 새 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-145">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="5cde5-146">압축 되지 않은 패키지 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-146">The uncompressed package size is displayed.</span></span> <span data-ttu-id="5cde5-147">패키지 크기가 4gb (압축 해제)를 초과 하 고 대상 컴퓨터에 패키지를 스트리밍하는 경우 **패키지 압축**을 선택한 다음 **만들기**를 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-147">If the package size exceeds 4 GB (uncompressed) and you plan to stream the package to target computers, you must select **Compress Package**, and then click **Create**.</span></span>

11. <span data-ttu-id="5cde5-148">**완료** 페이지에서 **닫기를** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-148">On the **Completion** page, click **Close** to close the wizard.</span></span> <span data-ttu-id="5cde5-149">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-149">The package is now available in the sequencer.</span></span>

**<span data-ttu-id="5cde5-150">기존 가상 응용 프로그램 패키지와 연결 된 속성을 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="5cde5-150">To modify the properties associated with an existing virtual application package</span></span>**

1.  <span data-ttu-id="5cde5-151">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-151">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5cde5-152">App-v 시퀀서에서 **기존 가상 응용 프로그램 패키지 수정을**클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-152">In the App-V Sequencer, click **Modify an Existing Virtual Application Package**, and then click **Next**.</span></span>

3.  <span data-ttu-id="5cde5-153">**작업 선택** 페이지에서 **패키지 편집**을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-153">On the **Select Task** page, click **Edit Package**, and then click **Next**.</span></span>

4.  <span data-ttu-id="5cde5-154">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 여 수정 하려는 응용 프로그램 속성을 포함 하는 가상 응용 프로그램 패키지를 찾은 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-154">On the **Select Package** page, click **Browse** to locate the virtual application package that contains the application properties that you want to modify, and then click **Edit**.</span></span>

5.  <span data-ttu-id="5cde5-155">Sequencer 콘솔에서 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-155">In the Sequencer console, you can perform any of the following tasks:</span></span>

    -   <span data-ttu-id="5cde5-156">패키지 속성 보기.</span><span class="sxs-lookup"><span data-stu-id="5cde5-156">View package properties.</span></span>

    -   <span data-ttu-id="5cde5-157">패키지 변경 내용 보기</span><span class="sxs-lookup"><span data-stu-id="5cde5-157">View package change history.</span></span>

    -   <span data-ttu-id="5cde5-158">연결 된 패키지 파일을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-158">View associated package files.</span></span>

    -   <span data-ttu-id="5cde5-159">레지스트리 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-159">Edit registry settings.</span></span>

    -   <span data-ttu-id="5cde5-160">추가 패키지 설정 검토 (운영 체제 파일 속성 제외)</span><span class="sxs-lookup"><span data-stu-id="5cde5-160">Review additional package settings (except operating system file properties).</span></span>

    -   <span data-ttu-id="5cde5-161">관련 Windows Installer (MSI)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-161">Create an associated Windows Installer (MSI).</span></span>

    -   <span data-ttu-id="5cde5-162">OSD 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-162">Modify OSD file.</span></span>

    -   <span data-ttu-id="5cde5-163">패키지를 압축 및 압축 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-163">Compress and uncompress package.</span></span>

    -   <span data-ttu-id="5cde5-164">파일 형식 연결을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-164">Add file type associations.</span></span>

    -   <span data-ttu-id="5cde5-165">가상화 된 레지스트리 키 상태 (재정의 또는 병합)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-165">Set virtualized registry key state (override or merge).</span></span>

    -   <span data-ttu-id="5cde5-166">가상화 된 폴더 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-166">Set virtualized folder state.</span></span>

    -   <span data-ttu-id="5cde5-167">가상 파일 시스템 매핑 편집</span><span class="sxs-lookup"><span data-stu-id="5cde5-167">Edit virtual file system mappings.</span></span>

6.  <span data-ttu-id="5cde5-168">패키지 속성 수정이 완료 되 면 **파일**  /  **저장** 을 클릭 하 여 패키지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-168">When you have finished modifying the package properties, click **File** / **Save** to save the package,.</span></span>

**<span data-ttu-id="5cde5-169">기존 가상 응용 프로그램 패키지에 새 응용 프로그램을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="5cde5-169">To add a new application to an existing virtual application package</span></span>**

1.  <span data-ttu-id="5cde5-170">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-170">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5cde5-171">App-v 시퀀서에서 **기존 가상 응용 프로그램 패키지 수정을**클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-171">In the App-V Sequencer, click **Modify an Existing Virtual Application Package**, and then click **Next**.</span></span>

3.  <span data-ttu-id="5cde5-172">**작업 선택** 페이지에서 **새 응용 프로그램 추가**를 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-172">On the **Select Task** page, click **Add New Application**, and then click **Next**.</span></span>

4.  <span data-ttu-id="5cde5-173">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 여 응용 프로그램을 추가 하려는 가상 응용 프로그램 패키지를 찾은 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-173">On the **Select Package** page, click **Browse** to locate the virtual application package that you want to add the application to, and then click **Next**.</span></span>

5.  <span data-ttu-id="5cde5-174">**컴퓨터 준비** 페이지에서 패키지 만들기가 실패 하거나 업데이트가 불필요 한 데이터를 포함 하 게 될 수 있는 문제를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-174">On the **Prepare Computer** page, review the issues that could cause the package creation to fail, or for the update to contain unnecessary data.</span></span> <span data-ttu-id="5cde5-175">계속 하기 전에 모든 잠재적인 문제를 해결 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-175">We strongly recommend that you resolve all potential issues before you continue.</span></span> <span data-ttu-id="5cde5-176">충돌을 수정한 후 표시 되는 정보를 업데이트 하려면 **새로 고침**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-176">After you have fixed the conflicts, to update the information that is displayed, click **Refresh**.</span></span> <span data-ttu-id="5cde5-177">발생할 수 있는 모든 문제를 해결 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-177">After you have resolved all potential issues, click **Next**.</span></span>

    <span data-ttu-id="5cde5-178">**중요**  바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우 시퀀서를 실행 하는 컴퓨터를 검사 하 여 불필요 하거나 악의적인 파일이 패키지에 추가 될 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-178">**Important** If you are required to disable virus scanning software, scan the computer running the sequencer to ensure that no unwanted or malicious files can be added to the package.</span></span>

     

6.  <span data-ttu-id="5cde5-179">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 응용 프로그램의 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-179">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="5cde5-180">응용 프로그램에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행 하려는 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-180">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

7.  <span data-ttu-id="5cde5-181">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자가 준비 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-181">On the **Installation** page, when the sequencer and application installer are ready, install the application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="5cde5-182">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행**을 클릭 하 고 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-182">If additional installation files must be run as part of the installation, click **Run**, and locate and run the additional installation files.</span></span> <span data-ttu-id="5cde5-183">설치가 완료 되 면 **설치 완료**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-183">When you are finished with the installation, select **I am finished installing**.</span></span> <span data-ttu-id="5cde5-184">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-184">Click **Next**.</span></span> <span data-ttu-id="5cde5-185">**폴더 찾아보기** 대화 상자에서 응용 프로그램을 설치할 기본 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-185">In the **Browse for Folder** dialog box, specify the primary directory where the application will be installed.</span></span> <span data-ttu-id="5cde5-186">기존 버전의 가상 응용 프로그램 패키지를 덮어쓰지 않도록 새 위치 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-186">This should be a new location so that you do not overwrite the existing version of the virtual application package.</span></span>

    <span data-ttu-id="5cde5-187">**참고**  Sequencer를 실행 하는 컴퓨터에 대 한 모든 변경 및 설치는 시퀀싱 마법사 외부에서 수행 되는 변경 및 설치를 포함 하 여 시퀀서에 의해 모니터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-187">**Note** All changes and installations to the computer running the sequencer are monitored by the sequencer, including the changes and installations that are performed outside of the sequencing wizard.</span></span>

     

8.  <span data-ttu-id="5cde5-188">**소프트웨어 구성** 페이지에서 패키지에 포함 된 프로그램을 선택적으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-188">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="5cde5-189">이 단계는 대상 컴퓨터에서 패키지를 배포 하 고 실행 하기 전에 응용 프로그램을 실행 하는 데 필요한 연결 된 라이선스 또는 구성 작업을 완료 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-189">This step helps complete any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="5cde5-190">한 번에 모든 프로그램을 실행 하려면 하나 이상의 프로그램을 선택한 다음 **모두 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-190">To run all the programs at the same time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="5cde5-191">특정 프로그램을 실행 하려면 실행할 프로그램을 선택한 다음, **선택한 프로그램 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-191">To run specific programs, select the program or programs you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="5cde5-192">필요한 구성 작업을 완료 한 다음 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-192">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="5cde5-193">모든 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-193">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="5cde5-194">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-194">Click **Next**.</span></span>

9.  <span data-ttu-id="5cde5-195">**설치 보고서** 페이지에서 방금 업데이트 한 가상 응용 프로그램에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-195">On the **Installation Report** page, you can review information about the virtual application you just updated.</span></span> <span data-ttu-id="5cde5-196">**추가 정보**에 표시 되는 정보에 대 한 자세한 설명을 보려면 이벤트를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-196">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="5cde5-197">정보를 검토 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-197">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="5cde5-198">**사용자 지정** 페이지에서 가상 응용 프로그램을 설치 하 고 구성 하는 작업을 마쳤으면 **지금 중지** 를 선택 하 고이 절차의 14 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-198">On the **Customize** page, if you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="5cde5-199">다음 목록에 있는 항목을 사용자 지정 하려는 경우 **사용자 지정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-199">If you want to customize any of the items in the following list, click **Customize**.</span></span>

    -   <span data-ttu-id="5cde5-200">응용 프로그램과 연결 된 파일 형식 연결을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-200">Edit the file type associations associated with an application.</span></span>

    -   <span data-ttu-id="5cde5-201">스트리밍을 위해 가상 패키지를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-201">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="5cde5-202">스트리밍을 통해 대상 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 때 환경이 개선 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-202">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    <span data-ttu-id="5cde5-203">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-203">Click **Next**.</span></span>

11. <span data-ttu-id="5cde5-204">**바로 가기 편집** 페이지에서 패키지의 다양 한 응용 프로그램과 연결 되는 FTA (파일 형식 연결)를 선택적으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-204">On the **Edit Shortcuts** page, you can optionally configure the file type associations (FTA) that will be associated with the various applications in the package.</span></span> <span data-ttu-id="5cde5-205">새 FTA를 만들려면 왼쪽 창에서 사용자 지정 하려는 응용 프로그램을 선택 하 고 확장 한 다음 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-205">To create a new FTA, select and expand the application that you want to customize in the left pane, and then click **Add**.</span></span> <span data-ttu-id="5cde5-206">**파일 형식 연결 추가** 대화 상자에서 새 FTA에 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-206">In the **Add File Type Association** dialog box, provide the necessary information for the new FTA.</span></span> <span data-ttu-id="5cde5-207">응용 프로그램과 관련 된 바로 가기 정보를 검토 하려면 응용 프로그램에서 **바로 가기** 확인란을 선택 하 고 **위치** 창에서 아이콘 파일 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-207">To review the shortcut information associated with an application, under the application, select the **Shortcuts** check box, and in the **Location** pane, you can review the icon file information.</span></span> <span data-ttu-id="5cde5-208">기존 FTA를 편집 하려면 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-208">To edit an existing FTA, click **Edit**.</span></span> <span data-ttu-id="5cde5-209">FTA를 제거 하려면 FTA을 선택한 다음 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-209">To remove an FTA, select the FTA, and then click **Remove**.</span></span> <span data-ttu-id="5cde5-210">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-210">Click **Next**.</span></span>

12. <span data-ttu-id="5cde5-211">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-211">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="5cde5-212">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-212">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="5cde5-213">모든 응용 프로그램이 실행 된 후에 각 응용 프로그램을 닫고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-213">After all applications have run, close each of the applications, and then click **Next**.</span></span>

    <span data-ttu-id="5cde5-214">**참고**  이 단계를 수행 하는 동안 응용 프로그램이 로드 되지 않도록 하려면 **응용 프로그램 실행** 대화 상자에서 **중지** 를 클릭 하 고 원하는 작업에 따라 **모든 응용 프로그램 중지** 또는 **이 응용 프로그램을 중지** 확인란 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-214">**Note** If you want to stop an application from loading during this step, in the **Application Launch** dialog box, click **Stop** and select either the **Stop all applications** or the **Stop this application only** check box, depending on what you want.</span></span>

     

13. <span data-ttu-id="5cde5-215">패키지 **만들기** 페이지에서 패키지 **편집기를 사용 하 여 저장 하지 않고 계속 패키지를 수정** 합니다 확인란을 선택 하 여 패키지를 저장 하지 않고 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-215">On the **Create Package** page, select the **Continue to modify package without saving using the package editor** check box, to modify the package without saving it.</span></span> <span data-ttu-id="5cde5-216">이 옵션을 선택 하면 패키지를 저장 하기 전에 수정할 수 있도록 sequencer 콘솔의 패키지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-216">When you select this option, the package in the sequencer console opens so that you can modify the package before it is saved.</span></span> <span data-ttu-id="5cde5-217">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-217">Click **Next**.</span></span>

    <span data-ttu-id="5cde5-218">패키지를 즉시 저장 하려면 **지금 패키지를 저장**합니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-218">Select the default **Save the package now**, to save the package immediately.</span></span> <span data-ttu-id="5cde5-219">패키지와 연결 되는 선택적 **메모** 를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-219">Add optional **Comments** that will be associated with the package.</span></span> <span data-ttu-id="5cde5-220">메모는 패키지에 대 한 버전 및 기타 정보를 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-220">Comments are useful for identifying version and other information about the package.</span></span> <span data-ttu-id="5cde5-221">기본 **저장 위치** 도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-221">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="5cde5-222">기본 위치를 변경 하려면 **찾아보기를** 클릭 하 고 새 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-222">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="5cde5-223">압축 되지 않은 패키지 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-223">The uncompressed package size is displayed.</span></span> <span data-ttu-id="5cde5-224">패키지 크기가 4gb (압축 해제)를 초과 하 고 대상 컴퓨터에 패키지를 스트리밍하는 경우 **패키지 압축**을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-224">If the package size exceeds 4 GB (uncompressed) and you plan to stream the package to target computers, you must select **Compress Package**.</span></span> <span data-ttu-id="5cde5-225">**만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-225">Click **Create**.</span></span>

14. <span data-ttu-id="5cde5-226">**완료** 페이지에서 **닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-226">On the **Completion** page, click **Close**.</span></span> <span data-ttu-id="5cde5-227">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cde5-227">The package is now available in the sequencer.</span></span>

## <span data-ttu-id="5cde5-228">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5cde5-228">Related topics</span></span>


[<span data-ttu-id="5cde5-229">Application Virtualization Sequencer(App-V 4.6 SP1)에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="5cde5-229">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





