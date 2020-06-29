---
title: PowerShell을 사용하여 패키지 가속기를 만드는 방법
description: PowerShell을 사용하여 패키지 가속기를 만드는 방법
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814281"
---
# <span data-ttu-id="ab843-103">PowerShell을 사용하여 패키지 가속기를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="ab843-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="ab843-104">앱-V 5.1 패키지 가속기는 대규모의 복잡 한 응용 프로그램을 자동으로 시퀀싱 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-104">App-V 5.1 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="ab843-105">또한 App-v 5.1 패키지 가속기를 적용 하는 경우 가상화 된 패키지를 만들기 위해 수동으로 응용 프로그램을 설치 해야 하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-105">Additionally, when you apply an App-V 5.1 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="ab843-106">패키지 가속기를 만들려면</span><span class="sxs-lookup"><span data-stu-id="ab843-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="ab843-107">App-v 5.1 sequencer를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="ab843-108">Sequencer를 설치 하는 방법에 대 한 자세한 내용은 [sequencer를 설치 하는 방법을](how-to-install-the-sequencer-51beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab843-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="ab843-109">PowerShell 콘솔을 열려면 **시작** 을 클릭 하 고 **powershell**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="ab843-110">**Windows PowerShell**을 마우스 오른쪽 단추로 클릭하고 **관리자 권한으로 실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="ab843-111">**새로운 AppvPackageAccelerator** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="ab843-112">패키지 가속기를 만들려면, 설치 미디어 또는 설치 파일에서 바로 연결을 만들 수 있도록 하 고, 액셀러레이터 키를 사용 하는 사용자를 위한 추가 정보 파일을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="ab843-113">패키지 가속기 cmdlet을 사용 하려면 다음 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="ab843-114">**InstalledFilesPath** -응용 프로그램 설치 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="ab843-115">**설치 관리자** – 응용 프로그램 설치 미디어 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="ab843-116">**InputPackagePath** – appv 패키지의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="ab843-117">**Path** – 패키지의 출력 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="ab843-118">다음 예에서는 appv 패키지와 설치 미디어를 사용 하 여 패키지 가속기를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="ab843-119">New-AppvPackageAccelerator-InputPackagePath &lt; 경로에 대 한 설치 관리자 &gt; 경로- &lt; &gt; 출력 경로의 설치 관리자 실행 파일의 경로 &lt; 디렉터리&gt;</span><span class="sxs-lookup"><span data-stu-id="ab843-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="ab843-120">**AppvPackageAccelerator** cmdlet에 사용할 수 있는 추가 선택적 매개 변수는 다음 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="ab843-121">**AcceleratorDescriptionFile** -사용자가 만든 패키지 가속기 지침에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="ab843-122">패키지 가속기 지침은 패키지 가속기를 사용 하 여 만든 패키지와 함께 패키지 되는 **.txt** 또는 **.rtf** 설명 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="ab843-123">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="ab843-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ab843-124">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ab843-125">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="ab843-125">Got an App-V issue?</span></span>** <span data-ttu-id="ab843-126">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab843-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ab843-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ab843-127">Related topics</span></span>


[<span data-ttu-id="ab843-128">PowerShell을 사용하여 App-V 5.1 관리</span><span class="sxs-lookup"><span data-stu-id="ab843-128">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





