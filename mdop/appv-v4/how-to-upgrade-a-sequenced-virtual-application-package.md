---
title: 시퀀싱된 가상 응용 프로그램 패키지를 업그레이드하는 방법
description: 시퀀싱된 가상 응용 프로그램 패키지를 업그레이드하는 방법
author: dansimp
ms.assetid: ffa989f3-6621-4c59-9599-e3c3b3332f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45f7b3370e7989bfa860c25fd4ac81f2c2eb0959
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816483"
---
# <span data-ttu-id="6a77e-103">시퀀싱된 가상 응용 프로그램 패키지를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="6a77e-103">How to Upgrade a Sequenced Virtual Application Package</span></span>


<span data-ttu-id="6a77e-104">Application Virtualization (App-v) Sequencer를 사용 하 여 기존 가상 응용 프로그램을 새 버전으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-104">You can upgrade an existing virtual application to a new version by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="6a77e-105">업그레이드 프로세스는 새 가상 응용 프로그램 만들기와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-105">The upgrade process is similar to creating a new virtual application.</span></span> <span data-ttu-id="6a77e-106">업그레이드를 위해 기존 가상 응용 프로그램을 열고 필요한 업데이트를 만든 다음 업데이트 된 가상 응용 프로그램을 패키지 루트 디렉터리의 새 위치에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-106">You must open the existing virtual application for an upgrade, make the necessary updates, and then save the updated virtual application to a new location in the package root directory.</span></span> <span data-ttu-id="6a77e-107">또한 앱-V 시퀀서 콘솔을 사용 하 여 업그레이드를 수행 하지 않고 기존 가상 응용 프로그램을 변경할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-107">You can also use the App-V Sequencer Console to make changes to an existing virtual application without performing an upgrade.</span></span> <span data-ttu-id="6a77e-108">그러나 App-v Sequencer는 연결 된 sft 파일을 실제로 디코드 하지 않기 때문에이 방법을 사용 하 여 가상 응용 프로그램의 파일 시스템을 수정할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-108">However, you cannot make modifications to the virtual application’s file system by using this method because the App-V Sequencer does not actually decode the associated .sft file.</span></span> <span data-ttu-id="6a77e-109">예를 들어 **파일** 메뉴에서 **열기** 를 선택 하 여 앱-V 시퀀서 콘솔에서 기존 가상 응용 프로그램을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-109">For example; you can open an existing virtual application in the App-V Sequencer Console by selecting **Open** on the **File** menu.</span></span> <span data-ttu-id="6a77e-110">**패키지 이름** 및 관련 **설명을**업데이트할 수 있으며 가상 파일 시스템 및 가상 레지스트리를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-110">You can update the **Package Name** and the associated **Comments**, and you can make changes to the virtual file system and virtual registry.</span></span> <span data-ttu-id="6a77e-111">Windows Installer 파일을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-111">You can also create a Windows Installer file.</span></span>

<span data-ttu-id="6a77e-112">**주의**  사항 기존 가상 응용 프로그램 패키지를 업그레이드 하는 동안 이전 버전의 sft 파일이 수정 되기 때문에 이전 버전의 Windows Installer (.msi) 파일을 참조 해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-112">**Caution** You should not reference a previous version of the Windows Installer (.msi) file when you upgrade an existing virtual application package because the previous version of the .sft file will be modified during the upgrade.</span></span>

 

<span data-ttu-id="6a77e-113">다음 절차를 사용 하 여 기존 가상 응용 프로그램을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-113">Use the following procedure to upgrade an existing virtual application.</span></span>

**<span data-ttu-id="6a77e-114">기존 가상 응용 프로그램을 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="6a77e-114">To upgrade an existing virtual application</span></span>**

1.  <span data-ttu-id="6a77e-115">App-v sequencer 콘솔을 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start** / **Programs** / **microsoft 응용 프로그램 가상화** / **microsoft application virtualization sequencer**시작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-115">To start the App-V Sequencer Console, on the computer running the App-V Sequencer, select **Start**/**Programs**/**Microsoft Application Virtualization**/**Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="6a77e-116">기존 가상 응용 프로그램을 열려면 app-v 콘솔에서 **File** / **패키지 업그레이드에 대 한 파일 열기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-116">To open the existing virtual application, in the App-V Console, select **File**/**Open for Package Upgrade**.</span></span> <span data-ttu-id="6a77e-117">**패키지 업그레이드 용** 으로 열기 대화 상자를 사용 하 여 업그레이드를 위해 열려는 연결 된 SPRJ 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-117">Use the **Open For Package Upgrade** dialog box to locate the associated SPRJ file you want to open for upgrade.</span></span>

3.  <span data-ttu-id="6a77e-118">업데이트 된 패키지가 디코딩되는 위치를 지정 하려면 **폴더 찾아보기** 대화 상자를 사용 하 여 위치를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-118">To specify the location of where the updated package will be decoded, browse to the location by using the **Browse For Folder** dialog box.</span></span> <span data-ttu-id="6a77e-119">연결 된 SFT 파일에 지정 된 대로 패키지 루트 디렉터리가 생성 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-119">This is the location where the package root directory will be created as specified in the associated SFT file.</span></span> <span data-ttu-id="6a77e-120">지정 하는 디렉터리는 가상 응용 프로그램의 원래 버전이 저장 되는 위치와 달라 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-120">The directory that you specify must be a different location from where the original version of the virtual application is saved.</span></span> <span data-ttu-id="6a77e-121">새 대상 폴더가 아직 만들어지지 않은 경우 **새 폴더 만들기** 를 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-121">You can click **Make New Folder** if the new target folder has not been created yet.</span></span> <span data-ttu-id="6a77e-122">폴더를 만들려면 Application Virtualization 드라이브의 루트를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-122">You should select the root of the Application Virtualization drive to create the folder.</span></span> <span data-ttu-id="6a77e-123">업데이트 된 버전의 패키지를 만들면 디렉터리 이름에 대 한 순차적인 추가가 표시 됩니다 (예: "**0.1**"이 Q:\\ 드라이브에 있는 디렉터리 이름에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-123">When you create the updated version of the package, it will be denoted with a sequential addition to the directory name—for example, “**.1**” will be added to the directory name located on the Q:\\ drive.</span></span>

    <span data-ttu-id="6a77e-124">**중요**  지정 하는 디렉터리는 Q:\\ 드라이브의 패키지 루트 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-124">**Important** The directory that you specify must be located in the package root directory on the Q:\\ drive.</span></span> <span data-ttu-id="6a77e-125">새 폴더를 만들거나 원본 가상 응용 프로그램이 저장 된 디렉터리 아래에 하위 폴더를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-125">You can create a new folder, or you can create a subfolder under the directory where the original virtual application is saved.</span></span> <span data-ttu-id="6a77e-126">새 폴더에 할당 된 이름은 8 8 자를 넘지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-126">The name assigned to the new folder must not be longer than 8 eight characters.</span></span>

     

4.  <span data-ttu-id="6a77e-127">시퀀싱 마법사를 열려면 **도구** / **시퀀싱 마법사**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-127">To open the Sequencing Wizard, select **Tools**/**Sequencing Wizard**.</span></span> <span data-ttu-id="6a77e-128">**패키지 정보** 페이지에서 선택적으로 새 **패키지 이름을** 지정 하 고 업데이트 된 가상 응용 프로그램과 연결 될 선택적 주석을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-128">On the **Package Information** page, optionally specify the new **Package Name** and add optional comments that will be associated with the updated virtual application.</span></span> <span data-ttu-id="6a77e-129">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-129">Click **Next**.</span></span>

5.  <span data-ttu-id="6a77e-130">**모니터 설치** 페이지에서 새로 설치 모니터링을 시작 하려면 **모니터링 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-130">On the **Monitor Installation** page, to begin monitoring the new installation, click **Begin Monitoring**.</span></span> <span data-ttu-id="6a77e-131">가상 환경의 로드가 완료 되 면 업데이트 된 버전의 응용 프로그램을 설치 하거나 기존 응용 프로그램에 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-131">After the virtual environment has finished loading, install the updated version of the application, or apply updates to the existing application.</span></span> <span data-ttu-id="6a77e-132">가상 응용 프로그램 업데이트를 완료 한 후 **모니터링 중지**를 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-132">After you have finished updating the virtual application, click **Stop Monitoring**, and then click **Next**.</span></span>

6.  <span data-ttu-id="6a77e-133">Vfs **(가상 파일 시스템에 매핑할 추가 파일)** 페이지에서 Vfs (가상 파일 시스템)에 추가할 추가 파일을 지정 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-133">On the **Additional Files to Map to Virtual File System (VFS)** page, to specify additional files to be added to the Virtual File System (VFS), click **Add**.</span></span> <span data-ttu-id="6a77e-134">추가 하려는 파일을 찾아 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-134">Browse to the file you want to add, and click **Open**.</span></span> <span data-ttu-id="6a77e-135">추가 된 기존 파일을 지우려면 **원래 대로**를 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-135">To clear existing files that have been added, click **Reset**, and then click **Next**.</span></span>

7.  <span data-ttu-id="6a77e-136">**응용 프로그램 구성** 페이지에서 업데이트 된 가상 응용 프로그램과 연결 될 바로 가기 및 파일 형식 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-136">On the **Configure Applications** page, configure the shortcuts and file type associations that will be associated with the updated virtual application.</span></span> <span data-ttu-id="6a77e-137">업데이트 하려는 요소를 선택한 다음 **위치 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-137">Select the element you want to update, and then click **Edit Locations**.</span></span> <span data-ttu-id="6a77e-138">**바로 가기 위치** 대화 상자에서 구성을 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-138">Specify the configurations in the **Shortcut Locations** dialog box, and then click **Next**.</span></span>

8.  <span data-ttu-id="6a77e-139">응용 프로그램 **시작 페이지에서** 해당 패키지가 스트리밍을 위해 최적화 되어 있는지 확인 하기 위해 해당 패키지를 선택 하 고 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-139">On the **Launch Applications** page, to start the application to ensure that the package is optimized for streaming, select the package and click **Launch**.</span></span> <span data-ttu-id="6a77e-140">이 단계는 클라이언트가 대상 컴퓨터에서 처음으로 실행 되는 방법과 모든 관련 라이선스 계약을 사용할 수 있도록 구성 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-140">This step is useful for configuring how the application initially runs on target computers and for accepting any associated license agreements before the package is made available to clients.</span></span> <span data-ttu-id="6a77e-141">이 패키지와 연결 된 여러 응용 프로그램이 있는 경우 **모두 시작** 을 선택 하 여 모든 응용 프로그램을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-141">If there are multiple applications associated with this package, you can select **Launch All** to open all of the applications.</span></span> <span data-ttu-id="6a77e-142">새 버전의 가상 응용 프로그램을 시퀀싱 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-142">To sequence the new version of the virtual application, click **Next**.</span></span>

9.  <span data-ttu-id="6a77e-143">시퀀싱 마법사를 완료 하 고 닫으려면 **시퀀스 패키지** 페이지에서 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-143">To finish and to close the Sequencing Wizard, on the **Sequence Package** page, click **Finish**.</span></span>

10. <span data-ttu-id="6a77e-144">가상 응용 프로그램을 성공적으로 업데이트 한 후 패키지를 저장 하려면 App-v Sequencer 콘솔의 **파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-144">After you have successfully updated the virtual application, to save the package, in the App-V Sequencer Console, on the **File** menu, select **Save**.</span></span> <span data-ttu-id="6a77e-145">3 단계에서 지정한 디렉터리에서 가상 응용 프로그램에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a77e-145">The virtual application can be accessed in the directory specified in step 3.</span></span>

## <span data-ttu-id="6a77e-146">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6a77e-146">Related topics</span></span>


[<span data-ttu-id="6a77e-147">Application Virtualization Sequencer에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="6a77e-147">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





