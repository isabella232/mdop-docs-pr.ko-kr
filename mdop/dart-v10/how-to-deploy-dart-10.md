---
title: DaRT 10을 배포하는 방법
description: DaRT 10을 배포하는 방법
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813073"
---
# <span data-ttu-id="7b217-103">DaRT 10을 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="7b217-103">How to Deploy DaRT 10</span></span>


<span data-ttu-id="7b217-104">다음 지침에서는 사용자 환경에서 Microsoft 진단 및 복구 도구 집합 (DaRT) 10을 배포 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="7b217-105">DaRT 소프트웨어를 다운로드 하려면 MDOP를 [얻는 방법을](https://go.microsoft.com/fwlink/?LinkId=322049)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b217-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="7b217-106">한 관리자 컴퓨터에 모든 기능을 설치 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="7b217-107">예를 들어 전자 소프트웨어 배포 시스템을 사용 하 여 여러 컴퓨터에서 DaRT 10을 배포 하거나 제거 해야 하는 경우 명령줄 설치 옵션을 사용 하는 것이 더 쉬울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-107">If you need to deploy or uninstall DaRT 10 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="7b217-108">사용 가능한 명령줄 옵션에 대 한 설명과 예제는이 섹션에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="7b217-109">**중요**  DaRT를 설치 하기 전에 [dart 10 지원 구성을](dart-10-supported-configurations.md) 참조 하 여 모든 필수 소프트웨어를 설치 하 고 컴퓨터가 최소 시스템 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-109">**Important** Before you install DaRT, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="7b217-110">DaRT를 설치 하는 컴퓨터는 Windows 10을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-110">The computer onto which you install DaRT must be running Windows 10.</span></span>

 

<span data-ttu-id="7b217-111">다음 두 가지 구성 중 하나를 사용 하 여 DaRT를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="7b217-112">Pc에 DaRT와 모든 DaRT 도구를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="7b217-113">DaRT 복구 이미지를 만드는 데 필요한 도구만 관리자 컴퓨터에 설치한 다음 **원격 연결 뷰어** 를 설치 하 고 필요한 경우에는 헬프 데스크 컴퓨터에 **충돌 분석기** 를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="7b217-114">DaRT 설치 파일은 32 비트 및 64 비트 버전에서 모두 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="7b217-115">DaRT 복구 이미지 마법사를 실행 하는 컴퓨터의 아키텍처와 일치 하는 버전을 설치 합니다 (만들려는 복구 이미지의 컴퓨터 아키텍처가 아님).</span><span class="sxs-lookup"><span data-stu-id="7b217-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="7b217-116">DaRT 설치 파일 버전 중 하나를 사용 하 여 32 비트 또는 64 비트 컴퓨터에 대 한 복구 이미지를 만들 수 있지만, 32 비트 및 64 비트 컴퓨터에 대해 하나의 복구 이미지를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="7b217-117">관리자 컴퓨터에 DaRT 및 모든 DaRT 도구를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="7b217-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="7b217-118">32 비트 또는 64 비트 버전의 DaRT 10 installer 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-118">Download the 32-bit or 64-bit version of the DaRT 10 installer file.</span></span> <span data-ttu-id="7b217-119">DaRT를 설치 하는 컴퓨터와 일치 하는 아키텍처를 선택 하 고 DaRT 복구 이미지 마법사를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="7b217-120">DaRT 10을 다운로드 한 폴더에서 시스템 요구 사항에 해당 하는 **MSDaRT.msi** 설치 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-120">From the folder into which you downloaded DaRT 10, run the **MSDaRT.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="7b217-121">**Microsoft DaRT 10 설치 마법사 시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-121">On the **Welcome to the Microsoft DaRT 10 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="7b217-122">Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="7b217-123">**Microsoft 업데이트** 페이지에서 **업데이트를 확인할 때 microsoft Update 사용**을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="7b217-124">**설치 폴더 선택** 페이지에서 폴더를 선택 하거나 **다음** 을 클릭 하 여 기본 설치 위치에 DaRT를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="7b217-125">**설치 옵션** 페이지에서 설치 하려는 dart 기능을 선택 하거나 **다음** 을 클릭 하 여 모든 기능과 함께 DaRT를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="7b217-126">설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="7b217-127">설치가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="7b217-128">명령 프롬프트를 사용 하 여 관리자 컴퓨터에 DaRT 및 모든 DaRT 도구를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="7b217-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="7b217-129">DaRT를 설치 하거나 제거 하는 경우 명령 프롬프트에서 설치 파일을 실행 하는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="7b217-130">이 섹션에서는 명령 프롬프트에 DaRT를 설치 하거나 제거할 때 지정할 수 있는 다양 한 옵션의 몇 가지 예를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="7b217-131">다음 예제에서는 모든 DaRT 기능을 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="7b217-132">다음 예제에서는 DaRT 복구 이미지 마법사만 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="7b217-133">다음 예제에서는 충돌 분석기와 DaRT 원격 연결 뷰어만 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="7b217-134">다음 예제에서는 Windows Installer에 대 한 설치 로그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="7b217-135">이는 디버깅 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

<span data-ttu-id="7b217-136">**참고**  /Qn 또는/qb를 추가 하 여 자동 설치를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="7b217-137">DaRT 설치의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="7b217-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="7b217-138">**시작**을 클릭 하 고 **진단 및 복구 도구 집합**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="7b217-139">**진단 및 복구 도구 집합** 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="7b217-140">설치를 위해 선택한 모든 DaRT 도구가 성공적으로 설치 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b217-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="7b217-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7b217-141">Related topics</span></span>


[<span data-ttu-id="7b217-142">관리자 컴퓨터에 DaRT 10 배포</span><span class="sxs-lookup"><span data-stu-id="7b217-142">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

 

 





