---
title: App-V 패키지 가속기(App-V 4.6 SP1)를 만드는 방법
description: App-V 패키지 가속기(App-V 4.6 SP1)를 만드는 방법
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817638"
---
# <span data-ttu-id="dc629-103">App-V 패키지 가속기(App-V 4.6 SP1)를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="dc629-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="dc629-104">앱-V 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 자동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="dc629-105">패키지 가속기를 성공적으로 만들었으면 패키지 가속기를 다시 사용 하 고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="dc629-106">패키지 가속기에 대 한 자세한 내용은 [앱-v 패키지 가속기 정보 (app-v 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc629-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="dc629-107">App-v 패키지 가속기를 만드는 것은 고급 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="dc629-108">패키지 가속기에는 암호와 사용자 관련 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="dc629-109">따라서 패키지 가속기 및 연결 된 설치 미디어를 안전한 위치에 저장 해야 하며, 앱을 만든 후에는 패키지 가속기가 적용 될 때 게시자를 확인할 수 있도록 먼저 디지털 서명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="dc629-110">일부 경우에는 패키지 가속기를 만들기 위해 Sequencer를 실행 하는 컴퓨터에 응용 프로그램을 로컬로 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="dc629-111">먼저 설치 미디어를 사용 하 여 패키지 가속기를 만들고, 필요한 파일이 없는 경우, Sequencer를 실행 하는 컴퓨터에 로컬로 응용 프로그램을 설치한 다음 패키지 가속기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="dc629-112">중요</span><span class="sxs-lookup"><span data-stu-id="dc629-112">Important</span></span>**  
<span data-ttu-id="dc629-113">다음 절차를 시작 하기 전에 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="dc629-114">시퀀서를 실행 하는 컴퓨터에서 로컬로 패키지 가속기를 만드는 데 사용 해야 하는 가상 응용 프로그램 패키지를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="dc629-115">가상 응용 프로그램 패키지와 연결 된 필요한 모든 설치 파일을 Sequencer를 실행 하는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="dc629-116">중요</span><span class="sxs-lookup"><span data-stu-id="dc629-116">Important</span></span>**  
<span data-ttu-id="dc629-117">부인: Microsoft Application Virtualization Sequencer는 패키지 가속기를 만드는 데 사용 하는 소프트웨어 응용 프로그램에 대 한 라이선스 권한을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="dc629-118">이러한 응용 프로그램에 대 한 모든 최종 사용자 사용권 계약을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="dc629-119">소프트웨어 응용 프로그램의 사용권 조항에 따라 Application Virtualization Sequencer를 사용 하 여 패키지 가속기를 만들 수 있도록 하는 것은 사용자의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="dc629-120">App-v 패키지 가속기를 만들려면</span><span class="sxs-lookup"><span data-stu-id="dc629-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="dc629-121">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="dc629-122">App-v Sequencer **패키지 가속기 만들기** 마법사를 시작 하려면 **도구**  /  **패키지 가속기 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="dc629-123">**패키지 선택** 페이지에서 패키지 가속기를 만드는 데 사용할 기존 가상 응용 프로그램 패키지를 지정 하려면 **찾아보기를**클릭 하 고 기존 가상 응용 프로그램 패키지 (sprj 파일)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="dc629-124">팁</span><span class="sxs-lookup"><span data-stu-id="dc629-124">Tip</span></span>**  
    <span data-ttu-id="dc629-125">시퀀서를 실행 하는 컴퓨터에 로컬로 사용할 가상 응용 프로그램 패키지와 연결 된 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="dc629-126">**설치 파일** 페이지에서 원래 가상 응용 프로그램 패키지를 만드는 데 사용한 설치 파일을 포함 하는 폴더를 지정 하려면 **찾아보기를**클릭 한 다음 설치 파일이 포함 된 디렉터리를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="dc629-127">팁</span><span class="sxs-lookup"><span data-stu-id="dc629-127">Tip</span></span>**  
   <span data-ttu-id="dc629-128">Sequencer를 실행 하는 컴퓨터에 필요한 설치 파일이 들어 있는 폴더를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="dc629-129">**수집 정보** 페이지에서이 마법사의 **설치 파일** 페이지에 지정 된 위치에서 찾을 수 없는 파일을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="dc629-130">파일이 표시 되지 않으면 **이 파일 제거**를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="dc629-131">파일이 필요한 경우 **이전** 을 클릭 하 고 필요한 파일을 **설치 파일** 페이지에 지정 된 디렉터리에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="dc629-132">참고</span><span class="sxs-lookup"><span data-stu-id="dc629-132">Note</span></span>**  
   <span data-ttu-id="dc629-133">필요 없는 파일을 제거 하거나, **이전** 을 클릭 하 고 필요한 파일을 찾아 마법사의 다음 페이지로 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="dc629-134">**파일 선택** 페이지에서 검색 된 파일을 신중 하 게 검토 하 고 패키지 가속기에서 제거 해야 하는 파일의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="dc629-135">응용 프로그램이 성공적으로 실행 되는 데 필요한 파일만 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="dc629-136">**응용 프로그램 확인** 페이지에서 패키지를 빌드하는 데 필요한 모든 설치 파일이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="dc629-137">패키지 가속기를 사용 하 여 새 패키지를 만드는 경우 패키지를 만들려면 **응용 프로그램** 창에 표시 되는 모든 설치 파일이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="dc629-138">필요한 경우 설치 관리자 파일을 추가 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="dc629-139">불필요 한 설치 파일을 제거 하려면 설치 관리자 파일을 선택 하 고 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="dc629-140">설치 관리자와 연결 된 속성을 편집 하려면 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="dc629-141">이 단계에서 지정한 설치 파일은 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 만들 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="dc629-142">표시 된 정보를 확인 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="dc629-143">**지침 선택** 페이지에서 패키지 가속기에 대 한 정보가 포함 된 파일을 지정 하려면 **찾아보기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="dc629-144">예를 들어이 파일에는 Sequencer를 실행 하는 컴퓨터를 구성 하는 방법, 대상 컴퓨터에 대 한 응용 프로그램 필수 정보, 일반 메모에 대 한 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="dc629-145">패키지 가속기가 성공적으로 적용 되는 데 필요한 모든 정보를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="dc629-146">선택한 파일은 서식 있는 텍스트 (.rtf) 또는 텍스트 파일 (.txt) 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="dc629-147">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-147">Click **Next**.</span></span>

9. <span data-ttu-id="dc629-148">**패키지 가속기 만들기** 페이지에서 패키지 가속기를 저장할 위치를 지정 하려면 **찾아보기를** 클릭 하 고 디렉터리를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="dc629-149">**완료** 페이지에서 **패키지 가속기 만들기** 마법사를 닫으려면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="dc629-150">중요</span><span class="sxs-lookup"><span data-stu-id="dc629-150">Important</span></span>**  
   <span data-ttu-id="dc629-151">패키지 가속기가 최대한 안전한 지 확인 하 고 패키지 가속기가 적용 될 때 게시자를 확인할 수 있도록 하려면 항상 패키지 가속기에 디지털 서명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc629-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="dc629-152">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dc629-152">Related topics</span></span>


<span data-ttu-id="dc629-153">Application Virtualization Sequencer (App-v 4.6 SP1) 구성 [패키지 가속기를 적용 하 여 가상 응용 프로그램 패키지를 만드는 방법 (app-v 4.6 sp1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="dc629-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>









