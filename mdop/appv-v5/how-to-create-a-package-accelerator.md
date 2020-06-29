---
title: 패키지 가속기를 만드는 방법
description: 패키지 가속기를 만드는 방법
author: dansimp
ms.assetid: dfe305e5-7cf8-498f-9581-4805ffc722bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0710bff5e5ea420119ac3c395c2e8917f7c582dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814276"
---
# <span data-ttu-id="b9c4c-103">패키지 가속기를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="b9c4c-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="b9c4c-104">App-v 5.0 패키지 가속기가 새 가상 응용 프로그램 패키지를 자동으로 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-104">App-V 5.0 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="b9c4c-105">참고</span><span class="sxs-lookup"><span data-stu-id="b9c4c-105">Note</span></span>**  
<span data-ttu-id="b9c4c-106">PowerShell을 사용 하 여 패키지 가속기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="b9c4c-107">자세한 내용은 [PowerShell을 사용 하 여 패키지 가속기를 만드는 방법을](how-to-create-a-package-accelerator-by-using-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span></span>



<span data-ttu-id="b9c4c-108">패키지 가속기를 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="b9c4c-109">중요</span><span class="sxs-lookup"><span data-stu-id="b9c4c-109">Important</span></span>**  
<span data-ttu-id="b9c4c-110">패키지 가속기에는 암호와 사용자 관련 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="b9c4c-111">따라서 패키지 가속기 및 관련 설치 미디어를 안전한 위치에 저장 해야 하며, 앱을 만든 후에는 패키지 가속기를 만들고 디지털 서명을 하 여 App-v 5.0 패키지 가속기가 적용 될 때 게시자를 확인할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>



**<span data-ttu-id="b9c4c-112">중요</span><span class="sxs-lookup"><span data-stu-id="b9c4c-112">Important</span></span>**  
<span data-ttu-id="b9c4c-113">다음 절차를 시작 하기 전에 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="b9c4c-114">시퀀서를 실행 하는 컴퓨터에 패키지 가속기를 로컬로 만드는 데 사용할 가상 응용 프로그램 패키지를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="b9c4c-115">가상 응용 프로그램 패키지와 연결 된 필요한 모든 설치 파일을 sequencer를 실행 하는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="b9c4c-116">패키지 가속기를 만들려면</span><span class="sxs-lookup"><span data-stu-id="b9c4c-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="b9c4c-117">중요</span><span class="sxs-lookup"><span data-stu-id="b9c4c-117">Important</span></span>**  
    <span data-ttu-id="b9c4c-118">App-v 5.0 Sequencer는 패키지 가속기를 만드는 데 사용 하는 소프트웨어 응용 프로그램에 대 한 라이선스 권한을 부여 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-118">The App-V 5.0 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="b9c4c-119">사용 중인 응용 프로그램에 대 한 모든 최종 사용자 사용권 조항을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="b9c4c-120">소프트웨어 응용 프로그램의 사용 조건에 따라 App-v 5.0 Sequencer를 사용 하 여 패키지 가속기를 만들 수 있는지를 확인 하는 것은 사용자의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.0 Sequencer.</span></span>



~~~
To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="b9c4c-121">App-v 5.0 **패키지 가속기 만들기** 마법사를 시작 하려면 app-v 5.0 sequencer 콘솔에서 **도구**  /  **바로 연결 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-121">To start the App-V 5.0 **Create Package Accelerator** wizard, in the App-V 5.0 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="b9c4c-122">**패키지 선택** 페이지에서 패키지 가속기를 만드는 데 사용할 기존 가상 응용 프로그램 패키지를 지정 하려면 **찾아보기를**클릭 하 고 기존 가상 응용 프로그램 패키지 (appv 파일)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="b9c4c-123">팁</span><span class="sxs-lookup"><span data-stu-id="b9c4c-123">Tip</span></span>**  
   <span data-ttu-id="b9c4c-124">시퀀서를 실행 하는 컴퓨터에 로컬로 사용할 가상 응용 프로그램 패키지와 연결 된 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="b9c4c-125">**설치 파일** 페이지에서 원래 가상 응용 프로그램 패키지를 만드는 데 사용한 설치 파일을 포함 하는 폴더를 지정 하려면 **찾아보기를**클릭 한 다음 설치 파일이 포함 된 디렉터리를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="b9c4c-126">팁</span><span class="sxs-lookup"><span data-stu-id="b9c4c-126">Tip</span></span>**  
   <span data-ttu-id="b9c4c-127">Sequencer를 실행 하는 컴퓨터에 필요한 설치 파일이 들어 있는 폴더를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="b9c4c-128">Sequencer를 실행 하는 컴퓨터에 응용 프로그램이 이미 설치 되어 있는 경우 설치 파일을 지정 하려면 **로컬 시스템에 설치 된 파일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="b9c4c-129">이 옵션을 사용 하려면 응용 프로그램이 기본 설치 위치에 이미 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="b9c4c-130">**수집 정보** 페이지에서이 마법사의 **설치 파일** 페이지에 지정 된 위치에서 찾을 수 없는 파일을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="b9c4c-131">파일이 표시 되지 않으면 **이 파일 제거**를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="b9c4c-132">파일이 필요한 경우 **이전** 을 클릭 하 고 필요한 파일을 **설치 파일** 페이지에 지정 된 디렉터리에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="b9c4c-133">참고</span><span class="sxs-lookup"><span data-stu-id="b9c4c-133">Note</span></span>**  
   <span data-ttu-id="b9c4c-134">필요 없는 파일을 제거 하거나, **이전** 을 클릭 하 고 필요한 파일을 찾아 마법사의 다음 페이지로 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="b9c4c-135">**파일 선택** 페이지에서 검색 된 파일을 신중 하 게 검토 하 고 패키지 가속기에서 제거 해야 하는 파일의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="b9c4c-136">응용 프로그램이 성공적으로 실행 되는 데 필요한 파일만 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="b9c4c-137">**응용 프로그램 확인** 페이지에서 패키지를 빌드하는 데 필요한 모든 설치 파일이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="b9c4c-138">패키지 가속기를 사용 하 여 새 패키지를 만드는 경우 패키지를 만들려면 **응용 프로그램** 창에 표시 되는 모든 설치 파일이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="b9c4c-139">필요한 경우 설치 관리자 파일을 추가 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="b9c4c-140">불필요 한 설치 파일을 제거 하려면 설치 관리자 파일을 선택 하 고 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="b9c4c-141">설치 관리자와 연결 된 속성을 편집 하려면 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="b9c4c-142">이 단계에서 지정한 설치 파일은 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 만들 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="b9c4c-143">표시 된 정보를 확인 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="b9c4c-144">**지침 선택** 페이지에서 패키지 가속기에 대 한 정보가 포함 된 파일을 지정 하려면 **찾아보기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="b9c4c-145">예를 들어이 파일에는 Sequencer를 실행 하는 컴퓨터를 구성 하는 방법, 대상 컴퓨터에 대 한 응용 프로그램 필수 정보, 일반 메모에 대 한 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="b9c4c-146">패키지 가속기가 성공적으로 적용 되는 데 필요한 모든 정보를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="b9c4c-147">선택한 파일은 서식 있는 텍스트 (.rtf) 또는 텍스트 파일 (.txt) 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="b9c4c-148">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-148">Click **Next**.</span></span>

10. <span data-ttu-id="b9c4c-149">**패키지 가속기 만들기** 페이지에서 패키지 가속기를 저장할 위치를 지정 하려면 **찾아보기를** 클릭 하 고 디렉터리를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="b9c4c-150">**완료** 페이지에서 **패키지 가속기 만들기** 마법사를 닫으려면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="b9c4c-151">중요</span><span class="sxs-lookup"><span data-stu-id="b9c4c-151">Important</span></span>**  
   <span data-ttu-id="b9c4c-152">패키지 가속기가 최대한 안전한 지 확인 하 고 패키지 가속기가 적용 될 때 게시자를 확인할 수 있도록 하려면 항상 패키지 가속기에 디지털 서명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c4c-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="b9c4c-153">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b9c4c-153">Related topics</span></span>


[<span data-ttu-id="b9c4c-154">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="b9c4c-154">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="b9c4c-155">App-V 패키지 가속기를 사용하여 가상 응용 프로그램 패키지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="b9c4c-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)









