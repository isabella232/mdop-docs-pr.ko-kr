---
title: 가상 응용 프로그램 패키지(App-V 4.6)를 업그레이드하는 방법
description: 가상 응용 프로그램 패키지(App-V 4.6)를 업그레이드하는 방법
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816458"
---
# <span data-ttu-id="67e2b-103">가상 응용 프로그램 패키지(App-V 4.6)를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="67e2b-103">How to Upgrade a Virtual Application Package (App-V 4.6)</span></span>


<span data-ttu-id="67e2b-104">Application Virtualization (App-v) Sequencer를 사용 하 여 기존 가상 응용 프로그램을 업그레이드 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-104">Use the following procedure to upgrade an existing virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="67e2b-105">또한 앱-V 시퀀서 콘솔을 사용 하 여 업그레이드를 수행 하지 않고 기존 가상 응용 프로그램을 변경할 수 있지만,이 메서드를 사용 하 여 가상 응용 프로그램의 파일 시스템을 수정할 수는 없습니다 (App-v 시퀀서는 실제로 연결 된 sft 파일을 디코드 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="67e2b-105">You can also use the App-V Sequencer Console to make changes to an existing virtual application without performing an upgrade, but you cannot make modifications to the virtual application’s file system by using this method because the App-V Sequencer does not actually decode the associated .sft file.</span></span> <span data-ttu-id="67e2b-106">기존 패키지 편집에 대 한 자세한 내용은 [가상 응용 프로그램 패키지를 수정 하는 방법 (app-v 4.6)](how-to-modify-a-virtual-application-package--app-v-46-.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="67e2b-106">For more information about editing an existing package, see [How to Modify a Virtual Application Package (App-V 4.6)](how-to-modify-a-virtual-application-package--app-v-46-.md).</span></span>

**<span data-ttu-id="67e2b-107">기존 가상 응용 프로그램을 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="67e2b-107">To upgrade an existing virtual application</span></span>**

1.  <span data-ttu-id="67e2b-108">App-v sequencer 콘솔을 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **Programs**  /  **microsoft 응용 프로그램 가상화**  /  **microsoft application virtualization sequencer**시작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-108">To start the App-V Sequencer Console, on the computer running the App-V Sequencer, select **Start** / **Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="67e2b-109">기존 가상 응용 프로그램 패키지를 열고 **시퀀싱 마법사**를 시작 하려면 **패키지 업그레이드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-109">To open the existing virtual application package and start the **Sequencing Wizard**, select **Upgrade a Package**.</span></span> <span data-ttu-id="67e2b-110">업그레이드 하려는 패키지를 찾아 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-110">Locate the package you want to upgrade, and click **Open**.</span></span> <span data-ttu-id="67e2b-111">**폴더 찾아보기** 대화 상자에서 업그레이드 된 버전의 패키지를 배치할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-111">In the **Browse For Folder** dialog box, specify the location where the upgraded version of the package will be placed.</span></span> <span data-ttu-id="67e2b-112">지정 된이 위치는 응용 프로그램 가상화 드라이브로 지정 된 드라이브에 있어야 하며, 일반적으로 Q:\\ 드라이브에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-112">This location specified must be located on the drive specified as the application virtualization drive, which is typically the Q:\\ drive.</span></span> <span data-ttu-id="67e2b-113">새 폴더를 만들려면 **새 폴더**만들기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-113">To create a new folder, select **Make New Folder**.</span></span>

    <span data-ttu-id="67e2b-114">**경고가**  기존 가상 응용 프로그램의 루트 폴더를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-114">**Warning** You must specify the root folder of the existing virtual application.</span></span> <span data-ttu-id="67e2b-115">하위 폴더를 수동으로 만들지는 않지만 업그레이드가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-115">Do not manually create a subfolder or the upgrade will fail.</span></span>

     

3.  <span data-ttu-id="67e2b-116">**패키지 정보** 페이지에서 업데이트 된 패키지에 할당 될 **패키지 이름을** 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-116">On the **Package Information** page, specify the **Package Name** that will be assigned to the updated package.</span></span> <span data-ttu-id="67e2b-117">연결 된 Windows Installer 파일을 생성 하려면 패키지 이름이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-117">The package name is required for generating the associated Windows Installer file.</span></span> <span data-ttu-id="67e2b-118">또한 패키지에 할당할 선택적 설명을 추가 하 고 가상 응용 프로그램에 대 한 자세한 정보 (예: 버전 번호)를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-118">You should also add an optional comment that will be assigned to the package and that provides detailed information about the virtual application—for example, a version number.</span></span> <span data-ttu-id="67e2b-119">**고급 옵션** 페이지를 표시 하려면 **고급 모니터링 옵션 표시** 를 선택 하 고 **다음**을 클릭 합니다. 그렇지 않으면 5 단계로 넘어갑니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-119">To display the **Advanced Options** page, select **Show Advanced Monitoring Options** and click **Next**; otherwise, proceed to step 5.</span></span>

4.  <span data-ttu-id="67e2b-120">Microsoft Update에서 시퀀싱 하는 동안 응용 프로그램을 업데이트할 수 있도록 **고급 옵션** 페이지에서 **모니터링 중 Microsoft update 실행 허용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-120">On the **Advanced Options** page, to allow Microsoft Update to update the application as it is being sequenced, select **Allow Microsoft Update to run during monitoring**.</span></span> <span data-ttu-id="67e2b-121">이 옵션을 선택 하는 경우 모니터링 단계에서 Microsoft 업데이트를 설치할 수 있으며, 설치 될 관련 업데이트를 수락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-121">If you select this option, Microsoft Updates are allowed to be installed during the monitoring phase and you will need to accept the associated updates for them to be installed.</span></span> <span data-ttu-id="67e2b-122">인접 한 RAM을 사용 하도록 지원 되는 동적 연결 라이브러리 (.dll) 파일을 다시 매핑하려면 **dll 다시 기준**변경을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-122">To remap the supported dynamic-link library (.dll) files so that they use a contiguous space of RAM, select **Rebase DLLs**.</span></span> <span data-ttu-id="67e2b-123">이 옵션을 선택 하면 메모리를 절약 하 고 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-123">Selecting this option can conserve memory and help improve performance.</span></span> <span data-ttu-id="67e2b-124">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-124">Click **Next**.</span></span>

5.  <span data-ttu-id="67e2b-125">**모니터 설치** 페이지에서 응용 프로그램을 업데이트할 준비가 되었으면 **모니터링 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-125">On the **Monitor Installation** page, when you are ready to update the application, click **Begin Monitoring**.</span></span>

    <span data-ttu-id="67e2b-126">응용 프로그램에 대 한 업데이트를 적용 한 경우 **모니터링 중지**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-126">When the updates to the application have been applied, click **Stop Monitoring**.</span></span> <span data-ttu-id="67e2b-127">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-127">Click **Next**.</span></span>

6.  <span data-ttu-id="67e2b-128">필요한 경우 **응용 프로그램 구성** 페이지에서 가상 응용 프로그램과 연결 될 바로 가기 및 파일 형식 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-128">On the **Configure Applications** page, if necessary, configure the shortcuts and file type associations that will be associated with the virtual application.</span></span> <span data-ttu-id="67e2b-129">새 파일 형식 연결 또는 바로 가기를 추가 하려면 **추가**를 클릭 하 고 **응용 프로그램 추가** 대화 상자에서 새 요소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-129">To add a new file type association or shortcut, click **Add**, and in the **Add Application** dialog box, specify the new element.</span></span> <span data-ttu-id="67e2b-130">기존 바로 가기 또는 파일 형식 연결을 제거 하려면 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-130">To remove an existing shortcut or file type association, click **Remove**.</span></span> <span data-ttu-id="67e2b-131">기존 요소를 편집 하려면 수정할 요소를 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-131">To edit an existing element, select the element you want to modify, and then click **Edit**.</span></span> <span data-ttu-id="67e2b-132">**응용 프로그램 편집** 대화 상자에서 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-132">Specify the configurations in the **Edit Application** dialog box.</span></span> <span data-ttu-id="67e2b-133">**Save**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-133">Click **Save**.</span></span> <span data-ttu-id="67e2b-134">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-134">Click **Next**.</span></span>

7.  <span data-ttu-id="67e2b-135">응용 프로그램 시작 페이지에서 패키지가 올바르게 설치 되었고 스트리밍을 위해 최적화 되어 있는지 확인 하는 **애플리케이션을** 실행 하려면 패키지를 선택 하 고 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-135">On the **Launch Applications** page, to start the application to ensure that the package has been installed correctly and is optimized for streaming, select the package and click **Launch**.</span></span> <span data-ttu-id="67e2b-136">이 단계는 앱이 대상 컴퓨터에서 처음으로 실행 되는 방법과 연결 된 라이선스 계약을 허용 하는 방법을 구성 하는 데 유용 하며, 해당 패키지를 App-v 클라이언트에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-136">This step is useful for configuring how the application initially runs on target computers and for accepting any associated license agreements before the package is made available to App-V clients.</span></span> <span data-ttu-id="67e2b-137">여러 응용 프로그램이이 패키지와 연결 되어 있는 경우 **모두 시작** 을 선택 하 여 모든 응용 프로그램을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-137">If multiple applications are associated with this package, you can select **Launch All** to open all of the applications.</span></span> <span data-ttu-id="67e2b-138">패키지를 시퀀싱 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-138">To sequence the package, click **Next**.</span></span>

8.  <span data-ttu-id="67e2b-139">시퀀싱 마법사를 닫으려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-139">To close the Sequencing Wizard, click **Finish**.</span></span> <span data-ttu-id="67e2b-140">업데이트 된 패키지를 저장 하려면 Sequencer 콘솔에서 **파일**  /  **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-140">To save the updated package, in the Sequencer Console, select **File** / **Save**.</span></span>

    <span data-ttu-id="67e2b-141">Windows Installer 파일 (.msi)을 사용 하 여 업데이트 된 패키지를 배포 하려는 경우 다음과 같이 새 항목을 만들어야 합니다. Sequencer 콘솔에서 **도구**  /  **msi 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-141">If you plan to deploy the updated package by using a Windows Installer file (.msi), you must create new one as follows: in the Sequencer Console, select **Tools** / **Create MSI**.</span></span> <span data-ttu-id="67e2b-142">새 Windows Installer 파일이 만들어지고 업데이트 된 가상 응용 프로그램 패키지가 저장 되는 디렉터리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67e2b-142">The new Windows Installer file will be created and saved in the directory where the updated virtual application package is saved.</span></span>

## <span data-ttu-id="67e2b-143">관련 항목</span><span class="sxs-lookup"><span data-stu-id="67e2b-143">Related topics</span></span>


[<span data-ttu-id="67e2b-144">새 응용 프로그램(App-V 4.6)을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="67e2b-144">How to Sequence a New Application (App-V 4.6)</span></span>](how-to-sequence-a-new-application--app-v-46-.md)

 

 





