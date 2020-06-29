---
title: App-V 패키지 가속기를 사용하여 가상 응용 프로그램 패키지를 만드는 방법
description: App-V 패키지 가속기를 사용하여 가상 응용 프로그램 패키지를 만드는 방법
author: dansimp
ms.assetid: 715e7526-e100-419c-8fc1-75cbfe433835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 547cb93f334e025243937a97a1f904410fe2d504
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814268"
---
# <span data-ttu-id="31d5f-103">App-V 패키지 가속기를 사용하여 가상 응용 프로그램 패키지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="31d5f-103">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>


**<span data-ttu-id="31d5f-104">중요</span><span class="sxs-lookup"><span data-stu-id="31d5f-104">Important</span></span>**  
<span data-ttu-id="31d5f-105">App-v 5.0 Sequencer는 패키지 가속기를 만드는 데 사용 하는 소프트웨어 응용 프로그램에 대 한 라이선스 권한을 부여 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-105">The App-V 5.0 Sequencer does not grant any license rights to the software application that you use to create the Package Accelerator.</span></span> <span data-ttu-id="31d5f-106">사용 하는 응용 프로그램에 대 한 모든 최종 사용자 사용권 조항을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-106">You must abide by all end user license terms for the application that you use.</span></span> <span data-ttu-id="31d5f-107">소프트웨어 응용 프로그램의 사용 조건에 따라 App-v 5.0 Sequencer를 사용 하 여 패키지 가속기를 만들 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-107">It is your responsibility to make sure that the software application’s license terms allow you to create a Package Accelerator with the App-V 5.0 Sequencer.</span></span>



<span data-ttu-id="31d5f-108">다음 절차에 따라 App-v 5.0 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-108">Use the following procedure to create a virtual application package with the App-V 5.0 Package Accelerator.</span></span>

**<span data-ttu-id="31d5f-109">참고</span><span class="sxs-lookup"><span data-stu-id="31d5f-109">Note</span></span>**  
<span data-ttu-id="31d5f-110">이 절차를 시작 하기 전에 필요한 패키지 가속기를 App-v 5.0 Sequencer를 실행 하는 컴퓨터에 로컬로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-110">Before you start this procedure, copy the required Package Accelerator locally to the computer that runs the App-V 5.0 Sequencer.</span></span> <span data-ttu-id="31d5f-111">또한 패키지의 필요한 모든 설치 파일을 Sequencer를 실행 하는 컴퓨터의 로컬 디렉터리로 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-111">You should also copy all required installation files for the package to a local directory on the computer that runs the Sequencer.</span></span> <span data-ttu-id="31d5f-112">이 디렉터리는이 절차의 5 단계에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-112">This is the directory that you have to specify in step 5 of this procedure.</span></span>



**<span data-ttu-id="31d5f-113">앱-V 5.0 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="31d5f-113">To create a virtual application package with an App-V 5.0 Package Accelerator</span></span>**

1.  <span data-ttu-id="31d5f-114">App-v Sequencer를 시작 하려면 app-v 5.0 Sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-114">To start the App-V Sequencer, on the computer that runs the App-V 5.0 Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="31d5f-115">**새 패키지 만들기 마법사**를 시작 하려면 **새 가상 응용 프로그램 패키지 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-115">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="31d5f-116">패키지를 만들려면 **패키지 가속기를 사용 하 여 패키지 만들기** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-116">To create the package, select the **Create Package using a Package Accelerator** check box, and then click **Next**.</span></span>

3.  <span data-ttu-id="31d5f-117">새 가상 응용 프로그램 패키지를 만드는 데 사용 되는 패키지 가속기를 지정 하려면 **패키지 바로 가기 선택** 페이지에서 **찾아보기를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-117">To specify the package accelerator that will be used to create the new virtual application package, click **Browse** on the **Select Package Accelerator** page.</span></span> <span data-ttu-id="31d5f-118">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-118">Click **Next**.</span></span>

    **<span data-ttu-id="31d5f-119">중요</span><span class="sxs-lookup"><span data-stu-id="31d5f-119">Important</span></span>**  
    <span data-ttu-id="31d5f-120">패키지 가속기의 게시자를 확인할 수 없고 유효한 디지털 서명이 포함 되어 있지 않은 경우 **실행**을 클릭 하기 전에 패키지 가속기의 출처를 신뢰할 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-120">If the publisher of the package accelerator cannot be verified and does not contain a valid digital signature, then before you click **Run**, you must confirm that you trust the source of the package accelerator.</span></span> <span data-ttu-id="31d5f-121">**보안 경고** 대화 상자에서 선택 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-121">Confirm your choice in the **Security Warning** dialog box.</span></span>



4.  <span data-ttu-id="31d5f-122">**지침** 페이지에서 정보 창에 표시 되는 게시 지침 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-122">On the **Guidance** page, review the publishing guidance information that is displayed in the information pane.</span></span> <span data-ttu-id="31d5f-123">이 정보는 패키지 가속기를 만들 때 추가 되었으며 패키지를 만들고 게시 하는 방법에 대 한 지침을 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-123">This information was added when the Package Accelerator was created and it contains guidance about how to create and publish the package.</span></span> <span data-ttu-id="31d5f-124">지침 정보를 텍스트 (.txt) 파일로 내보내려면 **내보내기를** 클릭 하 고 파일을 저장할 위치를 지정한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-124">To export the guidance information to a text (.txt) file, click **Export** and specify the location where the file should be saved, and then click **Next**.</span></span>

5.  <span data-ttu-id="31d5f-125">**설치 파일 선택** 페이지에서 **새 폴더** 만들기를 클릭 하 여 패키지에 필요한 모든 설치 파일을 포함 하는 로컬 폴더를 만들고 폴더를 저장할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-125">On the **Select Installation Files** page, click **Make New Folder** to create a local folder that contains all required installation files for the package, and specify where the folder should be saved.</span></span> <span data-ttu-id="31d5f-126">또한 폴더에 할당할 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-126">You must also specify a name to be assigned to the folder.</span></span> <span data-ttu-id="31d5f-127">그런 다음 필요한 모든 설치 파일을 지정한 위치에 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-127">You must then copy all required installation files to the location that you specified.</span></span> <span data-ttu-id="31d5f-128">설치 파일이 포함 된 폴더가 Sequencer를 실행 하는 컴퓨터에 이미 있는 경우 **찾아보기를** 클릭 하 여 폴더를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-128">If the folder that contains the installation files already exists on the computer that runs the Sequencer, click **Browse** to select the folder.</span></span>

    <span data-ttu-id="31d5f-129">또는이 컴퓨터의 디렉터리에 설치 파일을 이미 복사한 경우 **새 폴더 만들기**를 클릭 하 고 설치 파일이 들어 있는 폴더로 이동한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-129">Alternatively, if you have already copied the installation files to a directory on this computer, click **Make New Folder**, browse to the folder that contains the installation files, and then click **Next**.</span></span>

    **<span data-ttu-id="31d5f-130">참고</span><span class="sxs-lookup"><span data-stu-id="31d5f-130">Note</span></span>**  
    <span data-ttu-id="31d5f-131">다음과 같이 지원 되는 설치 파일 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-131">You can specify the following types of supported installation files:</span></span>

    -   <span data-ttu-id="31d5f-132">Windows Installer 파일 (**.msi**)</span><span class="sxs-lookup"><span data-stu-id="31d5f-132">Windows Installer files (**.msi**)</span></span>

    -   <span data-ttu-id="31d5f-133">캐비닛 파일 (.cab)</span><span class="sxs-lookup"><span data-stu-id="31d5f-133">Cabinet files (.cab)</span></span>

    -   <span data-ttu-id="31d5f-134">.Zip 파일 이름 확장명을 가진 압축 파일</span><span class="sxs-lookup"><span data-stu-id="31d5f-134">Compressed files with a .zip file name extension</span></span>

    -   <span data-ttu-id="31d5f-135">실제 응용 프로그램 파일</span><span class="sxs-lookup"><span data-stu-id="31d5f-135">The actual application files</span></span>

    <span data-ttu-id="31d5f-136">**.Msp** 및 **.exe** 파일과 같은 파일 형식은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-136">The following file types are not supported: **.msp** and **.exe** files.</span></span> <span data-ttu-id="31d5f-137">**.Exe** 파일을 지정 하는 경우 수동으로 설치 파일의 압축을 풀어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-137">If you specify an **.exe** file, you must extract the installation files manually.</span></span>



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. <span data-ttu-id="31d5f-138">**패키지 이름** 페이지에서 패키지와 연결 되는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-138">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="31d5f-139">지정 하는 이름은 App-v 관리 콘솔에서 패키지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-139">The name that you specify identifies the package in the App-V Management Console.</span></span> <span data-ttu-id="31d5f-140">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-140">Click **Next**.</span></span>

7. <span data-ttu-id="31d5f-141">**패키지 만들기** 페이지에서 패키지와 연결 되는 메모를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-141">On the **Create Package** page, provide comments that will be associated with the package.</span></span> <span data-ttu-id="31d5f-142">메모에는 만들려는 패키지에 대 한 식별 정보가 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-142">The comments should contain identifying information about the package that you are creating.</span></span> <span data-ttu-id="31d5f-143">패키지를 만드는 위치를 확인 하려면 **저장 위치**에 표시 되는 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-143">To confirm the location where the package is created, review the information that is displayed in **Save Location**.</span></span> <span data-ttu-id="31d5f-144">패키지를 압축 하려면 **패키지 압축**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-144">To compress the package, select **Compress Package**.</span></span> <span data-ttu-id="31d5f-145">네트워크를 통해 패키지를 스트리밍하는 경우 또는 패키지 크기가 4gb를 초과 하는 경우 **압축 패키지** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-145">Select the **Compress Package** check box if the package will be streamed across the network, or when the package size exceeds 4 GB.</span></span>

   <span data-ttu-id="31d5f-146">패키지를 만들려면 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-146">To create the package, click **Create**.</span></span> <span data-ttu-id="31d5f-147">패키지를 만든 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-147">After the package is created, click **Next**.</span></span>

8. <span data-ttu-id="31d5f-148">**소프트웨어 구성** 페이지에서 Sequencer가 패키지에 포함 된 응용 프로그램을 구성할 수 있도록 설정 하려면 **소프트웨어 구성을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-148">On the **Configure Software** page, to enable the Sequencer to configure the applications that are contained in the package, select **Configure Software**.</span></span> <span data-ttu-id="31d5f-149">이 단계에서는 대상 컴퓨터에서 응용 프로그램을 실행 하기 위해 완료 해야 하는 관련 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-149">In this step you can configure any associated tasks that must be completed in order to run the application on the target computers.</span></span> <span data-ttu-id="31d5f-150">예를 들어 관련 라이선스 계약을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-150">For example, you can configure any associated license agreements.</span></span>

   <span data-ttu-id="31d5f-151">**소프트웨어 구성을**선택 하면이 단계의 일부로 Sequencer를 사용 하 여 다음 항목을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-151">If you select **Configure Software**, the following items can be configured using the Sequencer as part of this step:</span></span>

   -   <span data-ttu-id="31d5f-152">**패키지를 로드**합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-152">**Load Package**.</span></span> <span data-ttu-id="31d5f-153">시퀀서는 패키지와 연결 된 파일을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-153">The Sequencer loads the files that are associated with the package.</span></span> <span data-ttu-id="31d5f-154">패키지를 디코딩하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-154">It can take several seconds to an hour to decode the package.</span></span>

   -   <span data-ttu-id="31d5f-155">**각 프로그램을 실행**합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-155">**Run Each Program**.</span></span> <span data-ttu-id="31d5f-156">선택적으로 패키지에 포함 된 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-156">Optionally run the programs that are contained in the package.</span></span> <span data-ttu-id="31d5f-157">이 단계는 대상 컴퓨터에서 패키지를 배포 하 고 실행 하기 전에 응용 프로그램을 실행 하는 데 필요한 연결 된 라이선스 또는 구성 작업을 완료 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-157">This step is helpful to complete any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="31d5f-158">모든 프로그램을 한 번에 실행 하려면 하나 이상의 프로그램을 선택한 다음 **모두 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-158">To run all the programs at once, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="31d5f-159">특정 프로그램을 실행 하려면 실행할 프로그램을 선택한 다음, **선택한 프로그램 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-159">To run specific programs, select the program or programs that you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="31d5f-160">필요한 구성 작업을 완료 한 다음 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-160">Complete the required configuration tasks, and then close the applications.</span></span> <span data-ttu-id="31d5f-161">모든 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-161">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="31d5f-162">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-162">Click **Next**.</span></span>

   -   <span data-ttu-id="31d5f-163">**패키지를 저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-163">**Save Package**.</span></span> <span data-ttu-id="31d5f-164">Sequencer는 패키지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-164">The Sequencer saves the package.</span></span>

   -   <span data-ttu-id="31d5f-165">**기본 기능 블록**.</span><span class="sxs-lookup"><span data-stu-id="31d5f-165">**Primary Feature Block**.</span></span> <span data-ttu-id="31d5f-166">시퀀서는 기본 기능 블록을 다시 빌드하여 스트리밍을 위한 패키지를 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-166">The Sequencer optimizes the package for streaming by rebuilding the primary feature block.</span></span>

   <span data-ttu-id="31d5f-167">응용 프로그램을 구성 하지 않으려면 **이 단계 건너뛰기를**클릭 하 고이 절차의 9 단계로 이동 하 여 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-167">If you do not want to configure the applications, click **Skip this step**, and to go to step 9 of this procedure, and then click **Next**.</span></span>

9. <span data-ttu-id="31d5f-168">**완료** 페이지에서 **가상 응용 프로그램 패키지 보고서** 창에 표시 되는 정보를 검토 한 후 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-168">On the **Completion** page, after you review the information that is displayed in the **Virtual Application Package Report** pane, click **Close**.</span></span>

   <span data-ttu-id="31d5f-169">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-169">The package is now available in the Sequencer.</span></span> <span data-ttu-id="31d5f-170">패키지 속성을 편집 하려면 **\ [패키지 이름 \] 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-170">To edit the package properties, click **Edit \[Package Name\]**.</span></span> <span data-ttu-id="31d5f-171">패키지를 수정 하는 방법에 대 한 자세한 내용은 [기존 가상 응용 프로그램 패키지를 수정](how-to-modify-an-existing-virtual-application-package-beta.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31d5f-171">For more information about how to modify a package, see [How to Modify an Existing Virtual Application Package](how-to-modify-an-existing-virtual-application-package-beta.md).</span></span>

   <span data-ttu-id="31d5f-172">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="31d5f-172">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="31d5f-173">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-173">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="31d5f-174">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="31d5f-174">Got an App-V issue?</span></span>** <span data-ttu-id="31d5f-175">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d5f-175">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="31d5f-176">관련 항목</span><span class="sxs-lookup"><span data-stu-id="31d5f-176">Related topics</span></span>


[<span data-ttu-id="31d5f-177">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="31d5f-177">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









