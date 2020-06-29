---
title: PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법
description: PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813700"
---
# <span data-ttu-id="893e3-103">PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법</span><span class="sxs-lookup"><span data-stu-id="893e3-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="893e3-104">PowerShell을 사용 하 여 새 App-v 5.0 패키지를 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-104">Use the following procedure to create a new App-V 5.0 package using PowerShell.</span></span>

<span data-ttu-id="893e3-105">**참고**  이 절차를 사용 하기 전에 연결 된 설치 관리자 파일을 sequencer를 실행 하는 컴퓨터에 복사 하 고 [app-v 5.0 시퀀서 및 클라이언트 배포에 대 한 계획](planning-for-the-app-v-50-sequencer-and-client-deployment.md)의 sequencer 섹션을 읽고 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="893e3-106">PowerShell을 사용 하 여 새 가상 응용 프로그램을 만들려면</span><span class="sxs-lookup"><span data-stu-id="893e3-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="893e3-107">App-v 5.0 sequencer를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-107">Install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="893e3-108">Sequencer를 설치 하는 방법에 대 한 자세한 내용은 [sequencer를 설치 하는 방법을](how-to-install-the-sequencer-beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="893e3-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="893e3-109">PowerShell 콘솔을 열려면 **시작** 을 클릭 하 고 **powershell**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="893e3-110">**Windows PowerShell**을 마우스 오른쪽 단추로 클릭하고 **관리자 권한으로 실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="893e3-111">PowerShell 콘솔을 사용 하 여 **appvsequencer: import 모듈**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="893e3-112">패키지를 만들려면 **New AppvSequencerPackage** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="893e3-113">패키지를 만들려면 다음 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="893e3-114">**Name** -패키지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="893e3-115">**Primaryvirtualapplicationdirectory** -응용 프로그램을 설치 하는 데 사용 되는 디렉터리 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="893e3-116">이 경로는 반드시 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-116">This path must exist.</span></span>

    -   <span data-ttu-id="893e3-117">**설치 관리자** -연결 된 응용 프로그램 설치 관리자의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="893e3-118">**Path** -패키지의 출력 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="893e3-119">예:</span><span class="sxs-lookup"><span data-stu-id="893e3-119">For example:</span></span>

    **<span data-ttu-id="893e3-120">AppvSequencerPackage-패키지 &lt; &gt; 루트-설치 관리자 경로에 대 한 package의 virtualapplicationdirectory 경로의 이름입니다. &lt; &gt; &lt; 출력 경로의 설치 관리자 실행 파일 이름 &gt; -OutputPath &lt; 디렉터리&gt;</span><span class="sxs-lookup"><span data-stu-id="893e3-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="893e3-121">Sequencer가 패키지를 만들 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="893e3-122">PowerShell을 사용 하 여 패키지를 만들면 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="893e3-123">패키지가 제대로 만들어지지 않은 경우 오류가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="893e3-124">다음 목록에는 **새 AppvSequencerPackage** cmdlet에 사용할 수 있는 추가 선택적 매개 변수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="893e3-125">AcceleratorFilePath – 패키지를 생성 하는 데 대 한 가속기 .cab 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="893e3-126">InstalledFilesPath-로컬에 설치 된 응용 프로그램 파일이 저장 되는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="893e3-127">InstallMediaPath-설치 미디어가 있는 위치에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="893e3-128">서식 파일 경로 수-시퀀싱 프로세스를 사용자 지정 하려는 경우 서식 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="893e3-129">FullLoad-패키지를 열기 전에 앱-V 5.0를 실행 하는 컴퓨터에 완전히 다운로드 되도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.0 before it can be opened.</span></span>

    <span data-ttu-id="893e3-130">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="893e3-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="893e3-131">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="893e3-132">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="893e3-132">Got an App-V issue?</span></span>** <span data-ttu-id="893e3-133">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="893e3-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="893e3-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="893e3-134">Related topics</span></span>


[<span data-ttu-id="893e3-135">PowerShell을 사용하여 App-V 관리</span><span class="sxs-lookup"><span data-stu-id="893e3-135">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





