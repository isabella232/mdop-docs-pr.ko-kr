---
title: 응용 프로그램을 시퀀싱하는 방법
description: 응용 프로그램을 시퀀싱하는 방법
author: dansimp
ms.assetid: bd643dd6-dbf6-4469-bc70-c43ad9c69da9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 318d19e0d2c77a12cf6d3b8beb3688ee936df490
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816623"
---
# <span data-ttu-id="05b39-103">응용 프로그램을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="05b39-103">How to Sequence an Application</span></span>


<span data-ttu-id="05b39-104">App-v (Application Virtualization) Sequencer는 가상 환경에서 실행할 수 있는 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-104">The Application Virtualization (App-V) Sequencer creates applications that can be run in a virtual environment.</span></span> <span data-ttu-id="05b39-105">App-v Sequencer는 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고, 가상 환경에서 응용 프로그램이 실행 되는 데 필요한 정보를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-105">The App-V Sequencer monitors the installation and setup process for an application, and it records the information necessary for the application to run in a virtual environment.</span></span> <span data-ttu-id="05b39-106">또한 App-v 시퀀서를 사용 하 여 모든 사용자에 게 적용 되는 파일 및 구성 및 사용자가 사용자 지정할 수 있는 파일 및 구성을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-106">You can also use the App-V Sequencer to configure which files and configurations are applicable to all users and which files and configurations users can customize.</span></span> <span data-ttu-id="05b39-107">응용 프로그램의 순서를 지정 하는 경우 시퀀싱 하려는 컴퓨터의 로컬 드라이브에 패키지를 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-107">When you sequence an application, you should save the package to a drive that is local to the computer you are sequencing on.</span></span>

<span data-ttu-id="05b39-108">시퀀싱 된 응용 프로그램은 각 응용 프로그램이 가상 환경에서 실행 되 고 대상 컴퓨터에서 설치 또는 실행 될 수 있는 다른 응용 프로그램과 격리 되므로 운영 체제와 상호 작용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-108">A sequenced application does not interact with the operating system because each application runs in a virtual environment and is isolated from other applications that might be installed or running on the target computer.</span></span> <span data-ttu-id="05b39-109">이러한 격리는 응용 프로그램 충돌을 크게 줄여 주며 필요한 응용 프로그램 사전 배포 테스트의 양을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-109">This isolation dramatically reduces application conflicts and decreases the required amount of application pre-deployment testing.</span></span>

<span data-ttu-id="05b39-110">응용 프로그램을 성공적으로 시퀀싱 한 후 App-v Sequencer 콘솔에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-110">After you successfully sequence the application, it is available in the App-V Sequencer Console.</span></span>

**<span data-ttu-id="05b39-111">새 응용 프로그램을 시퀀싱 하려면</span><span class="sxs-lookup"><span data-stu-id="05b39-111">To sequence a new application</span></span>**

1.  <span data-ttu-id="05b39-112">새 가상 응용 프로그램을 시퀀싱 하려면 Application 가상화 드라이브를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-112">You must create the Application Virtualization drive to sequence a new virtual application.</span></span> <span data-ttu-id="05b39-113">Application Virtualization drive를 만들려면 응용 프로그램을 시퀀싱 하는 동안 파일을 저장 하는 데 사용할 수 있는 위치에 Q:\\ drive를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-113">To create the Application Virtualization drive, map the Q:\\ drive to a location that can be used to save files while you are sequencing an application.</span></span> <span data-ttu-id="05b39-114">그런 다음 Q:\\ 드라이브에서 순서를 계획 하는 각 응용 프로그램에 대해 개별 디렉터리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-114">You must then create individual directories for each application you plan to sequence on the Q:\\ drive.</span></span> <span data-ttu-id="05b39-115">응용 프로그램을 시퀀싱 하기 전에 가상 응용 프로그램 대상 폴더를 만들거나이 절차의 5 단계에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-115">You can create the virtual application target folders before you sequence an application, or you can create it in step 5 of this procedure.</span></span>

2.  <span data-ttu-id="05b39-116">App-v sequencer 콘솔을 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **Programs**  /  **microsoft 응용 프로그램 가상화**  /  **microsoft application virtualization sequencer**프로그램 시작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-116">To start the App-V Sequencer Console, on the computer that is running the App-V Sequencer, select **Start** / **Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span> <span data-ttu-id="05b39-117">**시퀀싱 마법사**를 시작 하려면 **파일**  /  **새 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-117">To start the **Sequencing Wizard**, select **File** / **New Package**.</span></span>

3.  <span data-ttu-id="05b39-118">**패키지 정보** 페이지에서 가상 응용 프로그램에 할당 될 **패키지 이름을** 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-118">On the **Package Information** page, specify the **Package Name** that will be assigned to the virtual application.</span></span> <span data-ttu-id="05b39-119">연결 된 Windows Installer 파일을 생성 하려면 패키지 이름이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-119">The package name is required for generating the associated Windows Installer file.</span></span> <span data-ttu-id="05b39-120">또한 패키지에 할당 되 고 가상 응용 프로그램에 대 한 자세한 정보를 제공 하는 선택적 주석도 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-120">You should also add an optional comment that will be assigned to the package and that provides detailed information about the virtual application.</span></span> <span data-ttu-id="05b39-121">**고급 옵션** 페이지를 표시 하려면 **고급 모니터링 옵션 표시**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-121">To display the **Advanced Options** page, select **Show Advanced Monitoring Options**.</span></span> <span data-ttu-id="05b39-122">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-122">Click **Next**.</span></span>

    **<span data-ttu-id="05b39-123">참고</span><span class="sxs-lookup"><span data-stu-id="05b39-123">Note</span></span>**  
    <span data-ttu-id="05b39-124">**고급 옵션** 페이지를 표시 하려면 **고급 모니터링 옵션 표시**를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-124">To display the **Advanced Options** page, you must select **Show Advanced Monitoring Options**.</span></span> <span data-ttu-id="05b39-125">**고급 옵션** 페이지가 필요 하지 않은 경우 4 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-125">If you do not require the **Advanced Options** page, skip to step 4.</span></span>



4.  <span data-ttu-id="05b39-126">**고급 옵션** 페이지에서 가상 응용 프로그램의 **블록 크기** 를 지정 하려면 원하는 크기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-126">On the **Advanced Options** page, to specify the **Block Size** for the virtual application, select the size you want.</span></span> <span data-ttu-id="05b39-127">블록 크기는 네트워크를 통해 패키지를 대상 컴퓨터로 스트리밍하기 위해 **sft** 파일을 나누는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-127">The block size determines how the **.sft** file will be divided for streaming the package across the network to target computers.</span></span> <span data-ttu-id="05b39-128">Microsoft Update가 시퀀싱 되는 동안 응용 프로그램을 업데이트 하도록 허용 하려면 **모니터링 하는 동안 Microsoft Update를 실행할 수 있도록 허용을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-128">To allow Microsoft Update to update the application as it is being sequenced; select **Allow Microsoft Update to run during monitoring**.</span></span> <span data-ttu-id="05b39-129">이 옵션을 선택 하는 경우 모니터링 단계에서 Microsoft 업데이트를 설치할 수 있으며, 설치 될 관련 업데이트를 수락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-129">If you select this option, Microsoft Updates are allowed to be installed during the monitoring phase and you will need to accept the associated updates for them to be installed.</span></span> <span data-ttu-id="05b39-130">인접 한 RAM을 사용 하도록 지원 되는 동적 링크 라이브러리 (.dll) 파일을 다시 매핑하려면 **dll 다시 기준**다시 연결을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-130">To remap the supported dynamic link library (.dll) files so that they use a contiguous space of RAM, select **Rebase DLLs**.</span></span> <span data-ttu-id="05b39-131">이 옵션을 선택 하면 메모리를 절약 하 고 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-131">Selecting this option can conserve memory and help improve performance.</span></span> <span data-ttu-id="05b39-132">대부분의 응용 프로그램은이 옵션을 지원 하지 않지만, RD 세션 호스트 (원격 데스크톱 세션 호스트) 서버 시나리오와 같이 RAM이 제한 된 환경에서는 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-132">Many applications do not support this option, but it is useful in environments with limited RAM such as in Remote Desktop Session Host (RD Session Host) Server scenarios.</span></span> <span data-ttu-id="05b39-133">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-133">Click **Next**.</span></span>

5.  <span data-ttu-id="05b39-134">**모니터 설치** 페이지에서 응용 프로그램 설치를 모니터링 하려면 **모니터링 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-134">On the **Monitor Installation** page, to monitor the installation of an application, click **Begin Monitoring**.</span></span> <span data-ttu-id="05b39-135">**모니터링 시작**을 클릭 한 후 응용 프로그램을 설치할 Q:\\ 드라이브의 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-135">After you click **Begin Monitoring**, specify the directory on the Q:\\ drive where the application will be installed.</span></span> <span data-ttu-id="05b39-136">만들지 않은 폴더에 응용 프로그램을 설치 하려면 **새 폴더 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-136">To install the application to a folder that has not been created, click **Make New Folder**.</span></span> <span data-ttu-id="05b39-137">시퀀싱 하는 각 응용 프로그램을 별도의 디렉터리에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-137">You must install each application that you sequence into a separate directory.</span></span>

    **<span data-ttu-id="05b39-138">중요</span><span class="sxs-lookup"><span data-stu-id="05b39-138">Important</span></span>**  
    <span data-ttu-id="05b39-139">지정 하는 폴더 이름은 8 자이 하 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-139">The folder name you specify must not be longer than 8 characters.</span></span>



~~~
Wait for the virtual environment to load, and then install the application so that the App-V Sequencer can monitor the process. When you have completed the installation, click **Stop Monitoring**, and then click **Next**.
~~~

6. <span data-ttu-id="05b39-140">Vfs **(가상 파일 시스템에 매핑할 추가 파일)** 페이지에서 Vfs (가상 파일 시스템)에 추가할 추가 파일을 지정 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-140">On the **Additional Files to Map to Virtual File System (VFS)** page, to specify additional files to be added to the Virtual File System (VFS), click **Add**.</span></span> <span data-ttu-id="05b39-141">추가 하려는 파일을 찾아 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-141">Browse to the file you want to add and click **Open**.</span></span> <span data-ttu-id="05b39-142">추가 된 기존 파일을 지우려면 **원래 대로**를 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-142">To clear existing files that have been added, click **Reset**, and then click **Next**.</span></span>

7. <span data-ttu-id="05b39-143">**응용 프로그램 구성** 페이지에서 가상 응용 프로그램과 연결 될 바로 가기 및 파일 형식 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-143">On the **Configure Applications** page, configure the shortcuts and file type associations that will be associated with the virtual application.</span></span> <span data-ttu-id="05b39-144">업데이트 하려는 요소를 선택한 다음 **위치 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-144">Select the element that you want to update, and then click **Edit Locations**.</span></span> <span data-ttu-id="05b39-145">바로 가기 위치 대화 상자에서 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-145">Specify the configurations in the Shortcut Locations dialog box.</span></span> <span data-ttu-id="05b39-146">**확인**을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-146">Click **OK**, and then click **Next**.</span></span>

8. <span data-ttu-id="05b39-147">응용 프로그램 **시작 페이지에서** 해당 패키지가 스트리밍을 위해 최적화 되어 있는지 확인 하기 위해 해당 패키지를 선택 하 고 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-147">On the **Launch Applications** page, to start the application to ensure that the package is optimized for streaming, select the package and click **Launch**.</span></span> <span data-ttu-id="05b39-148">이 단계는 클라이언트가 대상 컴퓨터에서 처음으로 실행 되는 방법과 모든 관련 라이선스 계약을 사용할 수 있도록 구성 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-148">This step is useful for configuring how the application initially runs on target computers and for accepting any associated license agreements before the package is made available to clients.</span></span> <span data-ttu-id="05b39-149">이 패키지와 연결 된 여러 응용 프로그램이 있는 경우 **모두 시작** 을 선택 하 여 모든 응용 프로그램을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-149">If there are multiple applications associated with this package, you can select **Launch All** to open all of the applications.</span></span> <span data-ttu-id="05b39-150">패키지를 시퀀싱 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-150">To sequence the package, click **Next**.</span></span>

9. <span data-ttu-id="05b39-151">**시퀀스 패키지** 페이지에서 마법사를 닫으려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-151">On the **Sequence Package** page, to close the wizard, click **Finish**.</span></span>

10. <span data-ttu-id="05b39-152">패키지를 성공적으로 만든 후 패키지를 저장 하려면 app-v Sequencer 콘솔에서 **파일**저장을 선택 하 고  /  **Save** 패키지를 저장할 이름과 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b39-152">After you have successfully created the package, to save the package, in the App-V Sequencer Console, select **File** / **Save** and specify the name and the location where the package will be saved.</span></span>

## <span data-ttu-id="05b39-153">관련 항목</span><span class="sxs-lookup"><span data-stu-id="05b39-153">Related topics</span></span>


[<span data-ttu-id="05b39-154">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="05b39-154">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="05b39-155">명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="05b39-155">How to Sequence a New Application by Using the Command Line</span></span>](how-to-sequence-a-new-application-by-using-the-command-line.md)









