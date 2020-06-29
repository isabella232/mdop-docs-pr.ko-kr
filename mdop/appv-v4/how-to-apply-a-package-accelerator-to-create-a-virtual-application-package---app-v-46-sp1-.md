---
title: 패키지 가속기를 적용 하 여 가상 응용 프로그램 패키지를 만드는 방법 (App-v 4.6 SP1)
description: 패키지 가속기를 적용 하 여 가상 응용 프로그램 패키지를 만드는 방법 (App-v 4.6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821383"
---
# <span data-ttu-id="db713-103">패키지 가속기를 적용 하 여 가상 응용 프로그램 패키지를 만드는 방법 (App-v 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="db713-103">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>


<span data-ttu-id="db713-104">앱-V 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 자동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="db713-105">패키지 가속기에 대 한 자세한 내용은 [앱-v 패키지 가속기 정보 (app-v 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db713-105">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="db713-106">중요</span><span class="sxs-lookup"><span data-stu-id="db713-106">Important</span></span>**  
<span data-ttu-id="db713-107">부인: Application Virtualization Sequencer는 패키지 가속기를 만드는 데 사용 하는 소프트웨어 응용 프로그램에 대 한 라이선스 권한을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-107">Disclaimer: The Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="db713-108">이러한 응용 프로그램에 대 한 모든 최종 사용자 사용권 계약을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-108">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="db713-109">소프트웨어 응용 프로그램의 사용권 조항에 따라 Application Virtualization Sequencer를 사용 하 여 패키지 가속기를 만들 수 있도록 하는 것은 사용자의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="db713-109">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="db713-110">참고</span><span class="sxs-lookup"><span data-stu-id="db713-110">Note</span></span>**  
<span data-ttu-id="db713-111">이 절차를 시작 하기 전에 필요한 패키지 가속기를 App-v Sequencer를 실행 하는 컴퓨터에 로컬로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-111">Before starting this procedure, copy the required Package Accelerator locally to the computer running the App-V Sequencer.</span></span> <span data-ttu-id="db713-112">또한 패키지의 필요한 모든 설치 파일을 Sequencer를 실행 하는 컴퓨터의 로컬 디렉터리로 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-112">You should also copy all required installation files for the package to a local directory on the computer running the Sequencer.</span></span> <span data-ttu-id="db713-113">이 디렉터리는이 절차의 5 단계에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-113">This is the directory that you have to specify in step 5 of this procedure.</span></span>



<span data-ttu-id="db713-114">패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-114">Use the following procedure to create a virtual application package by using a Package Accelerator.</span></span>

**<span data-ttu-id="db713-115">App-v 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="db713-115">To create a virtual application package by using an App-V Package Accelerator</span></span>**

1. <span data-ttu-id="db713-116">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-116">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="db713-117">**새 패키지 만들기 마법사**를 시작 하려면 **새 가상 응용 프로그램 패키지 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-117">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="db713-118">패키지를 만들려면 **패키지 가속기를 사용 하 여 패키지 만들기** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-118">To create the package, select the **Create Package using a Package Accelerator** check box, and then click **Next**.</span></span>

3. <span data-ttu-id="db713-119">**패키지 바로 연결 선택** 페이지에서 새 가상 응용 프로그램 패키지를 만드는 데 사용할 패키지 가속기를 지정 하려면 **찾아보기를** 클릭 하 여 사용할 패키지 가속기를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-119">On the **Select Package Accelerator** page, to specify the Package Accelerator that will be used to create the new virtual application package, click **Browse** to locate the Package Accelerator that you want to use.</span></span> <span data-ttu-id="db713-120">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-120">Click **Next**.</span></span>

   **<span data-ttu-id="db713-121">중요</span><span class="sxs-lookup"><span data-stu-id="db713-121">Important</span></span>**  
   <span data-ttu-id="db713-122">패키지 가속기의 게시자를 확인할 수 없고 유효한 디지털 서명이 포함 되어 있지 않은 경우에는 **보안 경고** 대화 상자에서 **실행**을 클릭 하기 전에 패키지 가속기의 출처를 신뢰할 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-122">If the publisher of the Package Accelerator cannot be verified and does not contain a valid digital signature, in the **Security Warning** dialog box, you must confirm that you trust the source of the Package Accelerator before you click **Run**.</span></span>



4. <span data-ttu-id="db713-123">**지침** 페이지에서 정보 창에 표시 된 게시 지침 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-123">On the **Guidance** page, review the publishing guidance information displayed in the information pane.</span></span> <span data-ttu-id="db713-124">패키지 가속기를 만들 때 표시 되는 정보는 추가 되었으며 패키지 만들기 및 게시에 대 한 정보를 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-124">The information displayed was added when the Package Accelerator was created and contains information about creating and publishing the package.</span></span> <span data-ttu-id="db713-125">지침 정보를 텍스트 (.txt) 파일로 내보내려면 **내보내기를** 클릭 하 고 파일을 저장할 위치를 지정한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-125">To export the guidance information to a text (.txt) file, click **Export** and specify the location where the file should be saved, and then click **Next**.</span></span>

5. <span data-ttu-id="db713-126">**설치 파일 선택** 페이지에서 패키지에 필요한 모든 설치 파일을 포함 하는 로컬 폴더를 만들려면 **새 폴더 만들기** 를 클릭 하 고 폴더를 저장할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-126">On the **Select Installation Files** page, to create a local folder that contains all required installation files for the package, click **Make New Folder** and specify where the folder should be saved.</span></span> <span data-ttu-id="db713-127">또한 폴더에 할당할 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-127">You must also specify a name to be assigned to the folder.</span></span> <span data-ttu-id="db713-128">그런 다음 필요한 모든 설치 파일을 지정한 위치에 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-128">You must then copy all required installation files to the location that you specified.</span></span> <span data-ttu-id="db713-129">설치 파일이 포함 된 폴더가 Sequencer를 실행 하는 컴퓨터에 이미 있는 경우 **찾아보기를** 클릭 하 여 폴더를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-129">If the folder that contains the installation files already exists on the computer running the Sequencer, click **Browse** to select the folder.</span></span>

   <span data-ttu-id="db713-130">또는이 컴퓨터의 디렉터리에 설치 파일을 이미 복사한 경우 **새 폴더 만들기**를 클릭 하 고 설치 파일이 들어 있는 폴더로 이동한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-130">Alternatively, if you have already copied the installation files to a directory on this computer, click **Make New Folder**, browse to the folder that contains the installation files, and then click **Next**.</span></span>

   **<span data-ttu-id="db713-131">참고</span><span class="sxs-lookup"><span data-stu-id="db713-131">Note</span></span>**  
   <span data-ttu-id="db713-132">다음과 같이 지원 되는 설치 파일 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-132">You can specify the following types of supported installation files:</span></span>

   -   <span data-ttu-id="db713-133">Windows Installer 파일 (**.msi**</span><span class="sxs-lookup"><span data-stu-id="db713-133">Windows Installer files(**.msi**</span></span>

   -   <span data-ttu-id="db713-134">.cab 파일</span><span class="sxs-lookup"><span data-stu-id="db713-134">.cab files</span></span>

   -   <span data-ttu-id="db713-135">.Zip 파일 이름 확장명을 가진 압축 파일</span><span class="sxs-lookup"><span data-stu-id="db713-135">Compressed files with a .zip file name extension</span></span>

   -   <span data-ttu-id="db713-136">실제 응용 프로그램 파일</span><span class="sxs-lookup"><span data-stu-id="db713-136">The actual application files</span></span>

   <span data-ttu-id="db713-137">**.Msp** 및 <strong> .exe 파일과 같은 파일 형식은 지원 되지 않습니다. </strong></span><span class="sxs-lookup"><span data-stu-id="db713-137">The following file types are not supported: **.msp** and<strong>.exe</strong> files.</span></span> <span data-ttu-id="db713-138">**.Exe** 파일을 지정 하는 경우 수동으로 설치 파일의 압축을 풀어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-138">If you specify an **.exe** file you must extract the installation files manually.</span></span>



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. <span data-ttu-id="db713-139">**패키지 이름** 페이지에서 패키지와 연결 되는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-139">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="db713-140">지정 된 이름은 App-v 관리 콘솔에서 패키지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-140">The name specified identifies the package in the App-V Management Console.</span></span> <span data-ttu-id="db713-141">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-141">Click **Next**.</span></span>

7. <span data-ttu-id="db713-142">**패키지 만들기** 페이지에서 패키지와 연결 되는 메모를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-142">On the **Create Package** page, provide comments that will be associated with the package.</span></span> <span data-ttu-id="db713-143">메모에는 만들려는 패키지에 대 한 식별 정보가 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-143">The comments should contain identifying information about the package you are creating.</span></span> <span data-ttu-id="db713-144">패키지를 만드는 위치를 확인 하려면 **저장 위치**에 표시 된 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-144">To confirm the location where the package is created, review the information displayed in **Save Location**.</span></span> <span data-ttu-id="db713-145">패키지를 압축 하려면 **패키지 압축**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-145">To compress the package, select **Compress Package**.</span></span> <span data-ttu-id="db713-146">네트워크를 통해 패키지를 스트리밍하는 경우 또는 패키지 크기가 4gb를 초과 하는 경우 **압축 패키지** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-146">Select the **Compress Package** check box if the package will be streamed across the network, or when the package size exceeds 4 GB.</span></span>

   <span data-ttu-id="db713-147">패키지를 만들려면 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-147">To create the package, click **Create**.</span></span> <span data-ttu-id="db713-148">패키지를 만든 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-148">After the package has been created, click **Next**.</span></span>

8. <span data-ttu-id="db713-149">**소프트웨어 구성** 페이지에서 Sequencer가 패키지에 포함 된 응용 프로그램을 구성할 수 있도록 설정 하려면 **소프트웨어 구성을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-149">On the **Configure Software** page, to enable the Sequencer to configure the applications contained in the package, select **Configure Software**.</span></span> <span data-ttu-id="db713-150">이 단계는 연결 된 라이선스 계약 구성과 같이 대상 컴퓨터에서 응용 프로그램을 실행 하기 위해 완료 해야 하는 연결 된 작업을 구성 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-150">This step is useful for configuring any associated tasks that must be completed to run the application on target computers, such as configuring any associated license agreements.</span></span>

   <span data-ttu-id="db713-151">**소프트웨어 구성을**선택 하면 다음 항목이이 단계의 일부로 시퀀서에 의해 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db713-151">If you select **Configure Software**, the following items are configured by the Sequencer as part of this step:</span></span>

   -   <span data-ttu-id="db713-152">**패키지를 로드**합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-152">**Load Package**.</span></span> <span data-ttu-id="db713-153">Sequencer는 패키지와 연결 된 파일을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-153">The Sequencer loads the files associated with the package.</span></span> <span data-ttu-id="db713-154">패키지를 디코딩하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-154">It can take several seconds to up to an hour to decode the package.</span></span>

   -   <span data-ttu-id="db713-155">**각 프로그램을 실행**합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-155">**Run Each Program**.</span></span> <span data-ttu-id="db713-156">선택적으로 패키지에 포함 된 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-156">Optionally run the programs contained in the package.</span></span> <span data-ttu-id="db713-157">이 단계는 대상 컴퓨터에서 패키지를 배포 하 고 실행 하기 전에 응용 프로그램을 실행 하는 데 필요한 연결 된 라이선스 또는 구성 작업을 완료 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-157">This step is helpful for completing any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="db713-158">한 번에 모든 프로그램을 실행 하려면 하나 이상의 프로그램을 선택한 다음 **모두 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-158">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="db713-159">특정 프로그램을 실행 하려면 실행할 프로그램을 선택한 다음, **선택한 프로그램 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-159">To run specific programs, select the program or programs you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="db713-160">필요한 구성 작업을 완료 한 다음 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-160">Complete the required configuration tasks, and then close the applications.</span></span> <span data-ttu-id="db713-161">모든 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-161">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="db713-162">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-162">Click **Next**.</span></span>

   -   <span data-ttu-id="db713-163">**패키지를 저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-163">**Save Package**.</span></span> <span data-ttu-id="db713-164">Sequencer는 패키지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-164">The Sequencer saves the package.</span></span>

   -   <span data-ttu-id="db713-165">**기본 기능 블록**.</span><span class="sxs-lookup"><span data-stu-id="db713-165">**Primary Feature Block**.</span></span> <span data-ttu-id="db713-166">시퀀서는 기본 기능 블록을 다시 빌드하여 스트리밍을 위한 패키지를 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-166">The Sequencer optimizes the package for streaming by rebuilding the primary feature block.</span></span>

   <span data-ttu-id="db713-167">응용 프로그램을 구성 하지 않으려면 **이 단계 건너뛰기를**클릭 하 고이 절차의 9 단계로 이동 하 여 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-167">If you do not want to configure the applications, click **Skip this step**, and to go to step 9 of this procedure, and then click **Next**.</span></span>

9. <span data-ttu-id="db713-168">**완료** 페이지에서 **가상 응용 프로그램 패키지 보고서** 창에 표시 된 정보를 검토 한 후 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-168">On the **Completion** page, after you have reviewed the information displayed in the **Virtual Application Package Report** pane, click **Close**.</span></span>

   <span data-ttu-id="db713-169">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db713-169">The package is now available in the Sequencer.</span></span> <span data-ttu-id="db713-170">패키지 속성을 편집 하려면 **\ [패키지 이름 \] 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db713-170">To edit the package properties, click **Edit \[Package Name\]**.</span></span> <span data-ttu-id="db713-171">패키지를 수정 하는 방법에 대 한 자세한 내용은 [기존 가상 응용 프로그램 패키지 (app-v 4.6 SP1)를 수정 하는 방법을](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db713-171">For more information about modifying a package, see [How to Modify an Existing Virtual Application Package (App-V 4.6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).</span></span>

## <span data-ttu-id="db713-172">관련 항목</span><span class="sxs-lookup"><span data-stu-id="db713-172">Related topics</span></span>


[<span data-ttu-id="db713-173">Application Virtualization Sequencer(App-V 4.6 SP1) 구성</span><span class="sxs-lookup"><span data-stu-id="db713-173">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="db713-174">App-V 패키지 가속기(App-V 4.6 SP1)를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="db713-174">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









