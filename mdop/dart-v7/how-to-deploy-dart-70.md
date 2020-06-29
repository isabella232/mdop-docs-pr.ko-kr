---
title: DaRT 7.0을 배포하는 방법
description: DaRT 7.0을 배포하는 방법
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813049"
---
# <span data-ttu-id="16425-103">DaRT 7.0을 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="16425-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="16425-104">이 항목에서는 환경에 Microsoft 진단 및 복구 도구 집합 (DaRT) 7을 배포 하는 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="16425-105">이 항목의 첫 번째 절차에서는 한 관리자 컴퓨터에 모든 기능을 설치 하 고 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="16425-106">예를 들어 전자 소프트웨어 배포 시스템을 사용 하 여 여러 컴퓨터에서 DaRT를 배포 하거나 제거 해야 하는 경우 명령줄 설치 옵션을 사용 하는 것이 더 쉬울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16425-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="16425-107">이러한 옵션은 사용 가능한 명령줄 옵션에 대 한 사용 예를 제공 하는이 항목의 두 번째 절차에 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16425-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="16425-108">**중요**  DaRT를 설치 하기 전에 컴퓨터가 [DaRT 7.0 지원 구성](dart-70-supported-configurations-dart-7.md)에 나열 된 최소 시스템 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="16425-109">관리자 컴퓨터에 DaRT를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="16425-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="16425-110">소프트웨어 다운로드의 일부로 받은 DaRT 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="16425-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="16425-111">시스템 요구 사항에 해당 하는 DaRT 설치 파일을 32 비트 또는 64 비트 중에서 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="16425-112">DaRT 설치 파일의 이름은 **MSDaRT70.msi**입니다.</span><span class="sxs-lookup"><span data-stu-id="16425-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="16425-113">Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="16425-114">DaRT를 설치 하기 위한 대상 폴더를 선택 하 고 모든 사용자에 대해 DaRT를 설치 해야 하는지, 현재 사용자만 설치할 것인지를 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="16425-115">설치를 **일반**또는 **사용자 지정**또는 **완료**로 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="16425-116">**일반적** 으로 가장 자주 사용 되는 도구를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="16425-117">이 방법은 대부분의 사용자에 게 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="16425-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="16425-118">**사용자 지정** 을 사용 하면 설치 된 도구와 설치 위치를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16425-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="16425-119">이는 다른 헬프 데스크 컴퓨터에 서로 다른 DaRT 도구를 설치 하는 경우 고급 사용자에 게 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="16425-120">**완료** -모든 DaRT 도구를 설치 하 고 가장 많은 디스크 공간을 필요로 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="16425-121">설치 방법을 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="16425-122">설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="16425-123">설치가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="16425-124">명령 프롬프트에서 DaRT를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="16425-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="16425-125">다음 예제에서는 모든 DaRT 기능을 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16425-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="16425-126">다음 예제에서는 **DaRT 복구 이미지 마법사**만 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16425-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="16425-127">다음 예제에서는 충돌 분석기와 DaRT 원격 연결 뷰어만 설치 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16425-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="16425-128">다음 예제에서는 Windows Installer에 대 한 설치 로그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16425-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="16425-129">이는 디버깅 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16425-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="16425-130">**참고**  DaRT 설치 명령 프롬프트 옵션에/qn 또는/qb를 추가 하 여 자동 설치를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16425-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="16425-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="16425-131">Related topics</span></span>


[<span data-ttu-id="16425-132">관리자 컴퓨터에 DaRT 7.0 배포</span><span class="sxs-lookup"><span data-stu-id="16425-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





