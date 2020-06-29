---
title: 새 추가 기능 또는 플러그 인 응용 프로그램(App-V 4.6 SP1)을 시퀀싱하는 방법
description: 새 추가 기능 또는 플러그 인 응용 프로그램(App-V 4.6 SP1)을 시퀀싱하는 방법
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816708"
---
# <span data-ttu-id="fa0f4-103">새 추가 기능 또는 플러그 인 응용 프로그램(App-V 4.6 SP1)을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa0f4-103">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span>


<span data-ttu-id="fa0f4-104">Application Virtualization (App-v) Sequencer를 사용 하 여 새 추가 기능 또는 플러그 인 가상 응용 프로그램 패키지를 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-104">Use the following procedure to create a new add-on or plug-in virtual application package by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="fa0f4-105">추가 기능 또는 플러그 인 응용 프로그램은 Microsoft Excel 용 플러그 인과 같은 응용 프로그램의 기능을 확장 하는 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-105">An add-on or plug-in application is an application that extends the functionality of an application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="fa0f4-106">순서를 지정할 수 있는 응용 프로그램 종류에 대 한 자세한 내용은 [시퀀싱 할 응용 프로그램 유형 (app-v 4.6 SP1)을 확인 하는 방법을](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-106">For more information about the types of applications you can sequence, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="fa0f4-107">중요</span><span class="sxs-lookup"><span data-stu-id="fa0f4-107">Important</span></span>**  
<span data-ttu-id="fa0f4-108">다음 절차를 수행 하기 전에 sequencer를 실행 하는 컴퓨터에 부모 응용 프로그램을 로컬로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-108">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="fa0f4-109">예를 들어 Microsoft Excel 용 플러그 인을 시퀀싱 하는 경우 시퀀서를 실행 하는 컴퓨터에 Microsoft Excel을 로컬로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-109">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="fa0f4-110">또한 대상 컴퓨터에 응용 프로그램이 설치 되어 있는 디렉터리에 부모 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-110">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="fa0f4-111">플러그 인 또는 추가 기능을 기존 가상 응용 프로그램 패키지와 함께 사용 하려는 경우 부모 가상 응용 프로그램 패키지를 만들 때 사용한 것과 동일한 가상 응용 프로그램 드라이브에 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-111">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



<span data-ttu-id="fa0f4-112">기존 가상 응용 프로그램 패키지를 상위 응용 프로그램으로 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-112">You can also use an existing virtual application package as the parent application.</span></span> <span data-ttu-id="fa0f4-113">기존 가상 응용 프로그램 패키지를 사용 하려면 새 추가 기능 또는 플러그 인을 시퀀싱 하기 전에 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-113">To use an existing virtual application package, use the following procedure before sequencing the new add-on or plug-in.</span></span>

1.  <span data-ttu-id="fa0f4-114">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-114">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="fa0f4-115">Sequencer를 실행 하는 컴퓨터로 기존 패키지를 확장 하려면 **도구**를 클릭 하 여  /  **로컬 시스템으로 패키지를 확장**합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-115">To expand an existing package to the computer running the sequencer, click **Tools** / **Expand Package to Local System**.</span></span>

3.  <span data-ttu-id="fa0f4-116">확장 하려는 패키지 (**sprj** 파일)를 찾아 선택한 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-116">Browse to and select the package (**.sprj** file) that you want to expand, and then click **Open**.</span></span> <span data-ttu-id="fa0f4-117">다음 절차를 계속 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-117">Continue with the following procedure.</span></span>

**<span data-ttu-id="fa0f4-118">새 추가 기능 또는 플러그 인 응용 프로그램의 순서를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="fa0f4-118">To sequence a new add-on or plug-in application</span></span>**

1.  <span data-ttu-id="fa0f4-119">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-119">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="fa0f4-120">**새 패키지 만들기 마법사**를 시작 하려면 **새 가상 응용 프로그램 패키지 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-120">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="fa0f4-121">패키지를 만들려면 **패키지 만들기 (기본값)** 를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-121">To create the package, select **Create Package (default)**, and click then **Next**.</span></span>

3.  <span data-ttu-id="fa0f4-122">**컴퓨터 준비** 페이지에서 패키지 만들기가 실패할 수 있는 문제를 검토 하거나 패키지에 불필요 한 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-122">On the **Prepare Computer** page, review the issues that might cause the package creation to fail, or for the package to contain unnecessary data.</span></span> <span data-ttu-id="fa0f4-123">계속 하기 전에 모든 잠재적인 문제를 해결 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-123">We strongly recommend that you resolve all potential issues before you continue.</span></span> <span data-ttu-id="fa0f4-124">충돌을 수정한 후 표시 되는 정보를 업데이트 하려면 **새로 고침**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-124">After you have fixed the conflicts, to update the information displayed, click **Refresh**.</span></span> <span data-ttu-id="fa0f4-125">발생할 수 있는 모든 문제를 해결 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-125">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="fa0f4-126">중요</span><span class="sxs-lookup"><span data-stu-id="fa0f4-126">Important</span></span>**  
    <span data-ttu-id="fa0f4-127">바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우 시퀀서를 실행 하는 컴퓨터를 검사 하 여 원치 않거나 악의적인 파일이 패키지에 추가 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-127">If you are required to disable virus scanning software, scan the computer running the sequencer to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="fa0f4-128">**응용 프로그램 종류** 페이지에서 **추가 기능 또는 플러그**인을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-128">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

    <span data-ttu-id="fa0f4-129">순서를 지정할 수 있는 응용 프로그램 종류에 대 한 자세한 내용은 [시퀀싱 할 응용 프로그램 유형 (app-v 4.6 SP1)을 확인 하는 방법을](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-129">For more information about the types of applications that you can sequence, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).</span></span>

5.  <span data-ttu-id="fa0f4-130">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 추가 기능 또는 플러그 인의 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-130">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="fa0f4-131">응용 프로그램에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행 하려는 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-131">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6.  <span data-ttu-id="fa0f4-132">**기본 선택** 페이지에서 **찾아보기를** 클릭 하 고 상위 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-132">On the **Select Primary** page, click **Browse** and specify the parent application.</span></span>

    **<span data-ttu-id="fa0f4-133">중요</span><span class="sxs-lookup"><span data-stu-id="fa0f4-133">Important</span></span>**  
    <span data-ttu-id="fa0f4-134">설치 하는 추가 기능 또는 플러그 인이 지원 되는 상위 응용 프로그램이 로컬로 설치 되지 않은 경우 여기를 중지 하 고 sequencer를 실행 하는 컴퓨터에 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-134">If the parent application that the add-on or plug-in you are installing is going to support has not been installed locally, stop here and install the application on the computer running the sequencer.</span></span> <span data-ttu-id="fa0f4-135">예를 들어 **Excel.exe** 프로그램 파일은 Microsoft Excel 플러그 인에 대해 로컬로 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-135">For example, the **Excel.exe** program file must be installed locally for a Microsoft Excel plug-in.</span></span>



~~~
Click **Next**.
~~~

7. <span data-ttu-id="fa0f4-136">**패키지 이름** 페이지에서 패키지와 연결 되는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-136">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="fa0f4-137">패키지에 추가 되는 응용 프로그램의 용도와 버전을 식별 하는 데 도움이 되는 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-137">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="fa0f4-138">패키지 이름이 App-v 관리 콘솔에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-138">The package name will also be displayed in the App-V management console.</span></span> <span data-ttu-id="fa0f4-139">**설치 위치** 에는 응용 프로그램이 설치 되는 응용 프로그램 가상화 경로가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-139">The **Installation Location** displays the Application Virtualization path where the application will be installed.</span></span> <span data-ttu-id="fa0f4-140">이 위치를 편집 하려면 **편집 (고급)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-140">To edit this location, select **Edit (Advanced)**.</span></span>

   **<span data-ttu-id="fa0f4-141">중요</span><span class="sxs-lookup"><span data-stu-id="fa0f4-141">Important</span></span>**  
   <span data-ttu-id="fa0f4-142">응용 프로그램 가상화 경로 편집은 고급 구성 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-142">Editing the Application Virtualization path is an advanced configuration task.</span></span> <span data-ttu-id="fa0f4-143">경로 변경의 의미를 완전히 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-143">You should fully understand the implications of changing the path.</span></span> <span data-ttu-id="fa0f4-144">대부분의 응용 프로그램에서는 기본 경로를 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-144">For most applications, we recommend the default path.</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="fa0f4-145">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자가 준비 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 플러그 인 또는 추가 기능 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-145">On the **Installation** page, when the sequencer and application installer are ready, install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="fa0f4-146">응용 프로그램의 설치 프로세스를 사용 하 여 설치를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-146">Perform the installation by using the application’s installation process.</span></span> <span data-ttu-id="fa0f4-147">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행** 을 클릭 하 고 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-147">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="fa0f4-148">설치가 완료 되 면 **설치 완료**를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-148">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="fa0f4-149">**설치 보고서** 페이지에서 방금 시퀀싱 한 가상 응용 프로그램 패키지에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-149">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="fa0f4-150">**추가 정보**에 표시 되는 정보에 대 한 자세한 설명을 보려면 이벤트를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-150">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="fa0f4-151">정보를 검토 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-151">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="fa0f4-152">**사용자 지정** 페이지에서 가상 응용 프로그램을 설치 하 고 구성 하는 작업을 마쳤으면 **지금 중지** 를 선택 하 고이 절차의 14 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-152">On the **Customize** page, if you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="fa0f4-153">다음 목록에 있는 항목을 사용자 지정 하려는 경우 **사용자 지정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-153">If you want to customize any of the items in the following list, select **Customize**.</span></span>

    -   <span data-ttu-id="fa0f4-154">응용 프로그램과 연결 된 파일 형식 연결을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-154">Edit the file type associations associated with an application.</span></span>

    -   <span data-ttu-id="fa0f4-155">스트리밍을 위해 가상 패키지를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-155">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="fa0f4-156">스트리밍을 통해 대상 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 때 환경이 개선 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-156">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="fa0f4-157">이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-157">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="fa0f4-158">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-158">Click **Next**.</span></span>

11. <span data-ttu-id="fa0f4-159">**바로 가기 편집** 페이지에서 패키지의 다양 한 응용 프로그램과 연결 되는 FTA (파일 형식 연결)를 선택적으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-159">On the **Edit Shortcuts** page, you can optionally configure the file type associations (FTA) that will be associated with the various applications in the package.</span></span> <span data-ttu-id="fa0f4-160">새 FTA를 만들려면 왼쪽 창에서 사용자 지정 하려는 응용 프로그램을 선택 하 고 확장 한 다음 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-160">To create a new FTA, in the left pane, select and expand the application that you want to customize, and then click **Add**.</span></span> <span data-ttu-id="fa0f4-161">**파일 형식 연결 추가** 대화 상자에서 새 FTA에 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-161">In the **Add File Type Association** dialog box, provide the necessary information for the new FTA.</span></span> <span data-ttu-id="fa0f4-162">응용 프로그램에서 **바로 가기를** 선택 하 여 응용 프로그램과 연결 된 바로 가기 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-162">Under the application, select **Shortcuts** to review the shortcut information associated with an application.</span></span> <span data-ttu-id="fa0f4-163">**위치** 창에서 아이콘 파일 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-163">In the **Location** pane, you can review the icon file information.</span></span> <span data-ttu-id="fa0f4-164">기존 FTA를 편집 하려면 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-164">To edit an existing FTA, click **Edit**.</span></span> <span data-ttu-id="fa0f4-165">FTA를 제거 하려면 FTA을 선택한 다음 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-165">To remove an FTA, select the FTA, and then click **Remove**.</span></span> <span data-ttu-id="fa0f4-166">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-166">Click **Next**.</span></span>

12. <span data-ttu-id="fa0f4-167">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-167">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="fa0f4-168">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-168">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="fa0f4-169">모든 응용 프로그램이 실행 된 후에 각 응용 프로그램을 닫고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-169">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="fa0f4-170">참고</span><span class="sxs-lookup"><span data-stu-id="fa0f4-170">Note</span></span>**  
   <span data-ttu-id="fa0f4-171">이 단계에서 응용 프로그램이 로드 되지 않도록 하려면 **응용 프로그램 실행** 대화 상자에서 **중지** 를 클릭 하 고 확인란 중 하나를 선택 하 고 **모든 응용 프로그램을 중지** 하거나 **이 응용 프로그램을 중지**합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-171">If you want to stop an application from loading during this step, in the **Application Launch** dialog box, click **Stop** and select one of the check boxes, **Stop all applications** or **Stop this application only**.</span></span>



13. <span data-ttu-id="fa0f4-172">**대상 OS** 페이지에서이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-172">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="fa0f4-173">해당 환경에서 지원 되는 모든 운영 체제에서이 패키지를 실행 하도록 설정 하려면 **모든 운영 체제에서이 패키지를 실행 하도록 허용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-173">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="fa0f4-174">특정 운영 체제 에서만이 패키지를 실행 하도록 구성 하려면 **다음 운영 체제 에서만이 패키지를 실행 하도록 허용** 확인란을 선택한 다음이 패키지를 실행할 수 있는 운영 체제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-174">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="fa0f4-175">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-175">Click **Next**.</span></span>

14. <span data-ttu-id="fa0f4-176">패키지 **만들기** 페이지에서 저장 하지 않고 패키지를 수정 하려면 **패키지 편집기를 사용 하 여 저장 하지 않고 패키지를 계속 수정** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-176">On the **Create Package** page, to modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="fa0f4-177">이 옵션을 선택 하면 패키지를 저장 하기 전에 수정할 수 있도록 Sequencer 콘솔에서 패키지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-177">Selecting this option opens the package in the Sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="fa0f4-178">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-178">Click **Next**.</span></span>

   <span data-ttu-id="fa0f4-179">패키지를 즉시 저장 하려면 **지금 기본 저장 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-179">To save the package immediately, select the default **Save the package now**.</span></span> <span data-ttu-id="fa0f4-180">필요에 따라 **메모** 를 선택 하 여 패키지와 연결 될 메모를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-180">Optionally, select **Comments** to add comments that will be associated with the package.</span></span> <span data-ttu-id="fa0f4-181">메모는 패키지에 대 한 버전 및 기타 정보를 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-181">Comments are useful for identifying version and other information about the package.</span></span> <span data-ttu-id="fa0f4-182">기본 **저장 위치** 도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-182">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="fa0f4-183">기본 위치를 변경 하려면 **찾아보기를** 클릭 하 고 새 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-183">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="fa0f4-184">압축 되지 않은 패키지 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-184">The uncompressed package size is displayed.</span></span> <span data-ttu-id="fa0f4-185">패키지 크기가 4gb (압축 해제)를 초과 하 고 대상 컴퓨터에 패키지를 스트리밍하는 경우 **패키지 압축**을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-185">If the package size exceeds 4 GB (uncompressed) and you plan to stream the package to target computers, you must select **Compress Package**.</span></span> <span data-ttu-id="fa0f4-186">**만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-186">Click **Create**.</span></span>

15. <span data-ttu-id="fa0f4-187">**완료** 페이지에서 **성공한 가상 응용 프로그램 패키지 보고서** 창에 표시 되는 정보를 검토 한 후 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-187">On the **Completion** page, after you have reviewed the information that is displayed in the **Successful Virtual Application Package Report** pane, click **Close**.</span></span> <span data-ttu-id="fa0f4-188">**성공한 가상 응용 프로그램 패키지 보고서** 창에 표시 되는 정보는이 절차의 14 단계에서 지정한 디렉터리 ( **Reports.xml**라는 파일) 에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-188">The information displayed in the **Successful Virtual Application Package Report** pane is also available in the directory specified in step 14 of this procedure, in a file named **Reports.xml**.</span></span>

   <span data-ttu-id="fa0f4-189">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-189">The package is now available in the sequencer.</span></span> <span data-ttu-id="fa0f4-190">**\ [패키지 이름 \] 편집** 을 클릭 하 여 패키지 속성을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-190">Click **Edit \[Package Name\]** to edit the package properties.</span></span> <span data-ttu-id="fa0f4-191">패키지를 수정 하는 방법에 대 한 자세한 내용은 [기존 가상 응용 프로그램 패키지 (app-v 4.6 SP1)를 수정 하는 방법을](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-191">For more information about modifying a package, see [How to Modify an Existing Virtual Application Package (App-V 4.6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).</span></span>

   **<span data-ttu-id="fa0f4-192">중요</span><span class="sxs-lookup"><span data-stu-id="fa0f4-192">Important</span></span>**  
   <span data-ttu-id="fa0f4-193">가상 응용 프로그램 패키지를 성공적으로 만들었으면 sequencer를 실행 하는 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa0f4-193">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



## <span data-ttu-id="fa0f4-194">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fa0f4-194">Related topics</span></span>


[<span data-ttu-id="fa0f4-195">Application Virtualization Sequencer(App-V 4.6 SP1)에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="fa0f4-195">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="fa0f4-196">시퀀싱 하는 응용 프로그램 유형을 확인 하는 방법 (App-v 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="fa0f4-196">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









