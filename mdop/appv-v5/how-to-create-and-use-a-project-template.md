---
title: 프로젝트 템플릿을 만들고 사용하는 방법
description: 프로젝트 템플릿을 만들고 사용하는 방법
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814260"
---
# <span data-ttu-id="764cc-103">프로젝트 템플릿을 만들고 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="764cc-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="764cc-104">앱-V 5.0 프로젝트 템플릿을 사용 하 여 기존 가상 응용 프로그램 패키지와 연결 된 일반적으로 적용 되는 설정을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-104">You can use an App-V 5.0 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="764cc-105">그런 다음 해당 환경에서 새 가상 응용 프로그램 패키지를 만들 때 이러한 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="764cc-106">프로젝트 템플릿을 사용 하 여 가상 응용 프로그램 패키지를 만드는 프로세스를 간소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="764cc-107">**참고**  패키지를 업그레이드 하는 동안 App-v 5.0 프로젝트 템플릿을 적용 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-107">**Note** You can, and often should apply an App-V 5.0 project template during a package upgrade.</span></span> <span data-ttu-id="764cc-108">예를 들어 사용자 지정 제외 목록을 사용 하 여 응용 프로그램을 시퀀싱 한 경우에는 연결 된 템플릿을 만들고 저장 하 여 시퀀싱 된 응용 프로그램을 업그레이드 하는 동안 나중에 사용할 수 있도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-108">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>

<span data-ttu-id="764cc-109">App-v 5.0 Application 가속기는 응용 프로그램에 따라 다르며 앱-v 5.0 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있기 때문에 앱-V 5.0 프로젝트 템플릿은 앱-V 5.0 응용 프로그램 가속기와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-109">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="764cc-110">새 서식 파일을 만들고 적용 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-110">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="764cc-111">프로젝트 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="764cc-111">To create a project template</span></span>**

1.  <span data-ttu-id="764cc-112">App-v 5.0 sequencer를 시작 하려면 sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-112">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

<span data-ttu-id="764cc-113">**참고**  가상 응용 프로그램 패키지가 현재 App-v 5.0 Sequencer 콘솔에 열려 있는 경우이 절차의 3 단계로 건너뛰십시오.</span><span class="sxs-lookup"><span data-stu-id="764cc-113">**Note** If the virtual application package is currently open in the App-V 5.0 Sequencer console, skip to step 3 of this procedure.</span></span>

2. <span data-ttu-id="764cc-114">App-v 5.0 프로젝트 템플릿을 사용 하 여 저장 하려는 설정이 포함 된 기존 가상 응용 프로그램 패키지를 열려면 **파일**  /  **열기**를 클릭 한 다음 **패키지 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-114">To open the existing virtual application package that contains the settings you want to save with the App-V 5.0 project template, click **File** / **Open**, and then click **Edit Package**.</span></span> <span data-ttu-id="764cc-115">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 고 열려고 하는 가상 응용 프로그램 패키지를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-115">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="764cc-116">**편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-116">Click **Edit**.</span></span>

3. <span data-ttu-id="764cc-117">앱-V 5.0 Sequencer 콘솔에서 서식 파일을 저장 하려면 파일을 서식 파일로 **File**  /  **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-117">In the App-V 5.0 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="764cc-118">새 서식 파일과 함께 저장 되는 설정을 검토 한 후 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-118">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="764cc-119">새 App-v 5.0 프로젝트 템플릿과 연결 되는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-119">Specify a name that will be associated with the new App-V 5.0 project template.</span></span> <span data-ttu-id="764cc-120">저장을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-120">Click Save.</span></span>
   <span data-ttu-id="764cc-121">새 App-v 5.0 프로젝트 서식 파일은이 절차의 3 단계에서 지정한 디렉터리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-121">The new App-V 5.0 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="764cc-122">프로젝트 서식 파일을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="764cc-122">To apply a project template</span></span>**

<span data-ttu-id="764cc-123">**중요**  패키지 가속기와 함께 프로젝트 템플릿을 사용 하 여 가상 응용 프로그램 패키지를 만드는 기능은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-123">**Important** Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>

1.  <span data-ttu-id="764cc-124">App-v 5.0 sequencer를 시작 하려면 sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-124">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="764cc-125">App-v 5.0 프로젝트 템플릿을 사용 하 여 새 가상 응용 프로그램 패키지를 만들거나 업그레이드 하려면 서식 **파일**  /  **에서 새로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-125">To create or upgrade a new virtual application package by using an App-V 5.0 project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="764cc-126">사용할 프로젝트 서식 파일을 선택 하려면 프로젝트 서식 파일이 저장 된 디렉터리로 이동 하 여 프로젝트 템플릿을 선택한 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-126">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

    <span data-ttu-id="764cc-127">새 가상 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-127">Create the new virtual application package.</span></span> <span data-ttu-id="764cc-128">지정 된 서식 파일을 사용 하 여 저장 한 설정이 만들려는 새 가상 응용 프로그램 패키지에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-128">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

    <span data-ttu-id="764cc-129">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="764cc-129">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="764cc-130">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-130">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="764cc-131">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="764cc-131">Got an App-V issue?</span></span>** <span data-ttu-id="764cc-132">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="764cc-132">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="764cc-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="764cc-133">Related topics</span></span>


[<span data-ttu-id="764cc-134">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="764cc-134">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









