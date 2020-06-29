---
title: 프로젝트 템플릿을 만들고 사용하는 방법
description: 프로젝트 템플릿을 만들고 사용하는 방법
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814249"
---
# <span data-ttu-id="ece1b-103">프로젝트 템플릿을 만들고 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="ece1b-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="ece1b-104">앱-V 5.1 프로젝트 템플릿을 사용 하 여 기존 가상 응용 프로그램 패키지와 연결 된 일반적으로 적용 되는 설정을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="ece1b-105">그런 다음 해당 환경에서 새 가상 응용 프로그램 패키지를 만들 때 이러한 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="ece1b-106">프로젝트 템플릿을 사용 하 여 가상 응용 프로그램 패키지를 만드는 프로세스를 간소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="ece1b-107">참고</span><span class="sxs-lookup"><span data-stu-id="ece1b-107">Note</span></span>**  
<span data-ttu-id="ece1b-108">패키지를 업그레이드 하는 동안 App-v 5.1 프로젝트 템플릿을 적용 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="ece1b-109">예를 들어 사용자 지정 제외 목록을 사용 하 여 응용 프로그램을 시퀀싱 한 경우에는 연결 된 템플릿을 만들고 저장 하 여 시퀀싱 된 응용 프로그램을 업그레이드 하는 동안 나중에 사용할 수 있도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="ece1b-110">App-v 5.1 Application 가속기는 응용 프로그램에 따라 다르며 앱-v 5.1 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있기 때문에 앱-V 5.1 프로젝트 템플릿은 앱-V 5.1 응용 프로그램 가속기와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="ece1b-111">새 서식 파일을 만들고 적용 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="ece1b-112">프로젝트 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="ece1b-112">To create a project template</span></span>**

1.  <span data-ttu-id="ece1b-113">App-v 5.1 sequencer를 시작 하려면 sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="ece1b-114">참고</span><span class="sxs-lookup"><span data-stu-id="ece1b-114">Note</span></span>**  
    <span data-ttu-id="ece1b-115">가상 응용 프로그램 패키지가 현재 App-v 5.1 Sequencer 콘솔에 열려 있는 경우이 절차의 3 단계로 건너뛰십시오.</span><span class="sxs-lookup"><span data-stu-id="ece1b-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="ece1b-116">앱-V 5.1 Sequencer 콘솔에서 서식 파일을 저장 하려면 파일을 서식 파일로 **File**  /  **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="ece1b-117">새 서식 파일과 함께 저장 되는 설정을 검토 한 후 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="ece1b-118">새 App-v 5.1 프로젝트 템플릿과 연결 되는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="ece1b-119">저장을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-119">Click Save.</span></span>

   <span data-ttu-id="ece1b-120">새 App-v 5.1 프로젝트 서식 파일은이 절차의 3 단계에서 지정한 디렉터리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="ece1b-121">프로젝트 서식 파일을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="ece1b-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="ece1b-122">중요</span><span class="sxs-lookup"><span data-stu-id="ece1b-122">Important</span></span>**  
    <span data-ttu-id="ece1b-123">패키지 가속기와 함께 프로젝트 템플릿을 사용 하 여 가상 응용 프로그램 패키지를 만드는 기능은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="ece1b-124">App-v 5.1 프로젝트 템플릿을 사용 하 여 새 가상 응용 프로그램 패키지를 만들거나 업그레이드 하려면 서식 **파일**  /  **에서 새로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="ece1b-125">사용할 프로젝트 서식 파일을 선택 하려면 프로젝트 서식 파일이 저장 된 디렉터리로 이동 하 여 프로젝트 템플릿을 선택한 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="ece1b-126">새 가상 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-126">Create the new virtual application package.</span></span> <span data-ttu-id="ece1b-127">지정 된 서식 파일을 사용 하 여 저장 한 설정이 만들려는 새 가상 응용 프로그램 패키지에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="ece1b-128">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="ece1b-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ece1b-129">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ece1b-130">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="ece1b-130">Got an App-V issue?</span></span>** <span data-ttu-id="ece1b-131">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece1b-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ece1b-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ece1b-132">Related topics</span></span>


[<span data-ttu-id="ece1b-133">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="ece1b-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









