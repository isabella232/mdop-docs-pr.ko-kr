---
title: 새 응용 프로그램(App-V 4.6)을 시퀀싱하는 방법
description: 새 응용 프로그램(App-V 4.6)을 시퀀싱하는 방법
author: dansimp
ms.assetid: f2c398c6-9200-4be3-b502-e00386fcd150
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a36021adf45f0f4c80ab08bcabbf9f18bf6e66b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816698"
---
# <span data-ttu-id="b9892-103">새 응용 프로그램(App-V 4.6)을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="b9892-103">How to Sequence a New Application (App-V 4.6)</span></span>


<span data-ttu-id="b9892-104">Application Virtualization (App-v) Sequencer를 사용 하 여 새 가상 응용 프로그램을 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-104">Use the following procedure to create a new virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="b9892-105">또한 App-v 시퀀서를 사용 하 여 모든 사용자에 게 적용 되는 파일 및 구성 및 사용자가 사용자 지정할 수 있는 파일 및 구성을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-105">You can also use the App-V Sequencer to configure which files and configurations are applicable to all users and which files and configurations users can customize.</span></span> <span data-ttu-id="b9892-106">응용 프로그램을 성공적으로 시퀀싱 한 후 App-v Sequencer에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-106">After you successfully sequence the application, it is available in the App-V Sequencer.</span></span>

**<span data-ttu-id="b9892-107">중요</span><span class="sxs-lookup"><span data-stu-id="b9892-107">Important</span></span>**  
<span data-ttu-id="b9892-108">시퀀싱 하는 동안 시퀀서를 실행 하는 컴퓨터에서 windows Vista 또는 windows 7을 실행 하는 경우 시스템 종료 **시작**을 클릭 하는 등 가상 환경 외부에서 다시 시작이 시작 되 면  /  **Shut Down**Windows가 종료 되지 않도록 하는 프로그램을 닫으라는 메시지가 나타나면 **취소** 를 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-108">During sequencing, if the computer running the sequencer is running Windows Vista or Windows 7, and a restart is initiated outside of the virtual environment, for example, by clicking **Start** / **Shut Down**, you must click **Cancel** when prompted to close the program that is preventing Windows from shutting down.</span></span> <span data-ttu-id="b9892-109">**강제 종료**를 클릭 하면 패키지 만들기가 실패 하 고 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-109">If you click **Force shut down**, the package creation will fail, and the computer will restart.</span></span> <span data-ttu-id="b9892-110">**취소**를 클릭 하면 응용 프로그램이 시퀀싱 되는 동안 sequencer에서 다시 시작을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-110">When you click **Cancel**, the sequencer successfully records the restart while the application is being sequenced.</span></span>



**<span data-ttu-id="b9892-111">새 응용 프로그램을 시퀀싱 하려면</span><span class="sxs-lookup"><span data-stu-id="b9892-111">To sequence a new application</span></span>**

1.  <span data-ttu-id="b9892-112">App-v 드라이브를 만들려면 응용 프로그램을 시퀀싱 하는 동안 파일을 저장 하는 데 사용할 수 있는 위치로 drive Q를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-112">To create the App-V drive, configure drive Q as the location that can be used to save files while you are sequencing an application.</span></span> <span data-ttu-id="b9892-113">그런 다음 drive Q에서 순서를 계획 하는 각 응용 프로그램에 대해 개별 디렉터리를 만들어야 합니다. 응용 프로그램을 시퀀싱 하기 전에 가상 응용 프로그램 대상 폴더를 만들거나이 절차의 5 단계에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-113">You must then create individual directories for each application that you plan to sequence on drive Q. You can create the virtual application targeted folders before you sequence an application, or you can create them in step 5 of this procedure.</span></span>

    **<span data-ttu-id="b9892-114">참고</span><span class="sxs-lookup"><span data-stu-id="b9892-114">Note</span></span>**  
    <span data-ttu-id="b9892-115">사용자가 지정 하는 App-v 드라이브는 대상 컴퓨터에서 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-115">The App-V drive you specify must be accessible on targeted computers.</span></span> <span data-ttu-id="b9892-116">드라이브 Q에 액세스할 수 없는 경우 다른 드라이브 문자를 선택 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-116">If drive Q is not accessible, you can choose a different drive letter.</span></span>



2.  <span data-ttu-id="b9892-117">App-v sequencer 콘솔을 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **Programs**  /  **microsoft 응용 프로그램 가상화**  /  **microsoft application virtualization sequencer**프로그램 시작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-117">To start the App-V Sequencer Console, on the computer that is running the App-V Sequencer, select **Start** / **Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span> <span data-ttu-id="b9892-118">시퀀싱 마법사를 시작 하려면 **패키지 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-118">To start the Sequencing Wizard, click **Create a Package**.</span></span>

3.  <span data-ttu-id="b9892-119">**패키지 정보** 페이지에서 가상 응용 프로그램에 할당 될 **패키지 이름을** 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-119">On the **Package Information** page, specify the **Package Name** that will be assigned to the virtual application.</span></span> <span data-ttu-id="b9892-120">연결 된 Windows Installer 파일을 생성 하려면 패키지 이름이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-120">The package name is required for generating the associated Windows Installer file.</span></span> <span data-ttu-id="b9892-121">또한 패키지에 할당 되 고 가상 응용 프로그램에 대 한 자세한 정보를 제공 하는 선택적 주석도 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-121">You should also add an optional comment that will be assigned to the package and that provides detailed information about the virtual application.</span></span> <span data-ttu-id="b9892-122">**고급 옵션** 페이지를 표시 하려면 **고급 모니터링 옵션 표시**를 선택 하 고 **다음**을 클릭 합니다. 그렇지 않으면 5 단계로 넘어갑니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-122">To display the **Advanced Options** page, select **Show Advanced Monitoring Options**, and then click **Next**; otherwise, proceed to step 5.</span></span>

4.  <span data-ttu-id="b9892-123">Microsoft Update에서 시퀀싱 하는 동안 응용 프로그램을 업데이트할 수 있도록 **고급 옵션** 페이지에서 **모니터링 중 Microsoft update 실행 허용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-123">On the **Advanced Options** page, to allow Microsoft Update to update the application as it is being sequenced, select **Allow Microsoft Update to run during monitoring**.</span></span> <span data-ttu-id="b9892-124">이 옵션을 선택 하면 모니터링 단계 중에 Microsoft 업데이트를 설치할 수 있으며, 설치 될 관련 업데이트를 수락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-124">If you select this option, Microsoft Updates can be installed during the monitoring phase, and you have to accept the associated updates for them to be installed.</span></span> <span data-ttu-id="b9892-125">인접 한 RAM을 사용 하도록 지원 되는 동적 링크 라이브러리 (.dll) 파일을 다시 매핑하려면 **dll 다시 기준**다시 연결을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-125">To remap the supported dynamic link library (.dll) files so that they use a contiguous space of RAM, select **Rebase DLLs**.</span></span> <span data-ttu-id="b9892-126">이 옵션을 선택 하면 메모리를 절약 하 고 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-126">Selecting this option can conserve memory and help improve performance.</span></span> <span data-ttu-id="b9892-127">대부분의 응용 프로그램은이 옵션을 지원 하지 않지만 터미널 서버 시나리오와 같이 RAM이 제한 된 환경에서는 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-127">Many applications do not support this option, but it is useful in environments with limited RAM such as in Terminal Server scenarios.</span></span> <span data-ttu-id="b9892-128">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-128">Click **Next**.</span></span>

5.  <span data-ttu-id="b9892-129">**모니터 설치** 페이지에서 응용 프로그램을 설치할 준비가 되 면 **모니터링 시작**을 클릭 하 고 **폴더 찾아보기** 대화 상자에서 응용 프로그램이 설치 될 드라이브 Q의 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-129">On the **Monitor Installation** page, when you are ready to install the application, click **Begin Monitoring**, and in the **Browse for Folder** dialog box, specify the directory on drive Q where the application will be installed.</span></span> <span data-ttu-id="b9892-130">드라이브 Q를 구성 하지 않고 application 가상화 드라이브에 대해 다른 드라이브 문자를 사용 하는 경우이 절차의 1 단계에서 지정한 드라이브 문자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-130">If you did not configure drive Q and used a different drive letter for the application virtualization drive, select the drive letter you specified in step 1 of this procedure.</span></span> <span data-ttu-id="b9892-131">Application virtualization 드라이브에서 만들지 않은 폴더에 응용 프로그램을 설치 하려면 **새 폴더 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-131">To install the application to a folder that has not been created on the application virtualization drive, click **Make New Folder**.</span></span> <span data-ttu-id="b9892-132">폴더를 지정한 후 시퀀서에서 시퀀싱을 위해 컴퓨터를 구성 하는 동안 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-132">After you specify the folder, wait while the Sequencer configures the computer for sequencing.</span></span>

    **<span data-ttu-id="b9892-133">중요</span><span class="sxs-lookup"><span data-stu-id="b9892-133">Important</span></span>**  
    <span data-ttu-id="b9892-134">가상 응용 프로그램 드라이브의 별도의 디렉터리에 시퀀싱 하는 각 응용 프로그램을 설치 해야 하며, 연결 된 폴더 이름은 8 자이 하 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-134">You must install each application that you sequence into a separate directory on the virtual application drive, and the associated folder name must not be longer than eight characters.</span></span>



~~~
After the computer has been configured for sequencing, install the application so that the App-V Sequencer can monitor the installation; when you are finished, click **Stop Monitoring**, and then click **Next**.
~~~

6. <span data-ttu-id="b9892-135">필요한 경우 **응용 프로그램 구성** 페이지에서 가상 응용 프로그램과 연결 될 바로 가기 및 파일 형식 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-135">On the **Configure Applications** page, if necessary, configure the shortcuts and file type associations that will be associated with the virtual application.</span></span> <span data-ttu-id="b9892-136">새 파일 형식 연결 또는 바로 가기를 추가 하려면 **추가**를 클릭 하 고 **응용 프로그램 추가** 대화 상자에서 새 요소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-136">To add a new file type association or shortcut, click **Add**, and in the **Add Application** dialog box, specify the new element.</span></span> <span data-ttu-id="b9892-137">기존 바로 가기 또는 파일 형식 연결을 제거 하려면 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-137">To remove an existing shortcut or file type association, click **Remove**.</span></span> <span data-ttu-id="b9892-138">기존 요소를 편집 하려면 수정할 요소를 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-138">To edit an existing element, select the element you want to modify, and then click **Edit**.</span></span> <span data-ttu-id="b9892-139">**응용 프로그램 편집** 대화 상자에서 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-139">Specify the configurations in the **Edit Application** dialog box.</span></span> <span data-ttu-id="b9892-140">**저장**을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-140">Click **Save**, and then click **Next**.</span></span>

7. <span data-ttu-id="b9892-141">응용 프로그램 **시작 페이지에서** 패키지가 올바르게 설치 되었고 스트리밍을 위해 최적화 되어 있는지 확인 하려면 해당 패키지를 선택 하 고 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-141">On the **Launch Applications** page, to start the application to ensure that the package has been installed correctly and is optimized for streaming, select the package, and then click **Launch**.</span></span> <span data-ttu-id="b9892-142">이 단계는 대상 컴퓨터에서 응용 프로그램을 처음으로 실행 하는 방법과 관련 라이선스 계약을 허용 하는 방법을 구성 하는 데 유용 하며,이 경우 앱-V 클라이언트에서 패키지를 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-142">This step is useful for configuring how the application initially runs on targeted computers and for accepting any associated license agreements before the package becomes available to App-V clients.</span></span> <span data-ttu-id="b9892-143">여러 응용 프로그램이이 패키지와 연결 되어 있는 경우 **모두 시작** 을 선택 하 여 모든 응용 프로그램을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-143">If multiple applications are associated with this package, you can select **Launch All** to open all of the applications.</span></span> <span data-ttu-id="b9892-144">패키지를 시퀀싱 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-144">To sequence the package, click **Next**.</span></span>

8. <span data-ttu-id="b9892-145">패키지를 성공적으로 만들었으면 app-v Sequencer 콘솔에서 **파일**  /  **저장** 을 선택 하 고 패키지가 저장 될 이름과 가상 드라이브 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-145">After you have successfully created the package, in the App-V Sequencer Console, select **File** / **Save** and specify the name and the virtual drive location where the package will be saved.</span></span>

   <span data-ttu-id="b9892-146">필요에 따라 연결 된 Windows Installer 파일 (**.msi**)을 만들어 대상 컴퓨터에 가상 응용 프로그램 패키지를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-146">You can optionally create an associated Windows Installer file (**.msi**) to install the virtual application package on targeted computers.</span></span> <span data-ttu-id="b9892-147">Windows Installer 파일을 만들려면 Sequencer에서 패키지를 열고 **Tools**  /  **MSI 만들기**도구를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-147">To create a Windows Installer file, open the package in the Sequencer and select **Tools** / **Create MSI**.</span></span> <span data-ttu-id="b9892-148">Windows Installer 파일이 만들어지고 가상 응용 프로그램 패키지가 저장 된 디렉터리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-148">The Windows Installer file will be created and saved in the directory where the virtual application package is saved.</span></span>

   **<span data-ttu-id="b9892-149">중요</span><span class="sxs-lookup"><span data-stu-id="b9892-149">Important</span></span>**  
   <span data-ttu-id="b9892-150">가상 응용 프로그램 패키지를 성공적으로 만들었으면 sequencer를 실행 하는 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b9892-150">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer running the sequencer.</span></span>



## <span data-ttu-id="b9892-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b9892-151">Related topics</span></span>


[<span data-ttu-id="b9892-152">가상 응용 프로그램 패키지(App-V 4.6)를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="b9892-152">How to Upgrade a Virtual Application Package (App-V 4.6)</span></span>](how-to-upgrade-a-virtual-application-package--app-v-46-.md)









