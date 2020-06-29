---
title: MED-V 구성 요소를 제거하는 방법
description: MED-V 구성 요소를 제거하는 방법
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813028"
---
# <span data-ttu-id="13db6-103">MED-V 구성 요소를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="13db6-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="13db6-104">특정 상황에서 엔터프라이즈에서 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 구성 요소 전부 또는 일부를 제거 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="13db6-105">예를 들어 모든 응용 프로그램 운영 체제 호환성 문제를 해결 했거나 엔터프라이즈에 다른 MED-V 작업 영역을 배포 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="13db6-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="13db6-106">일반적으로 Windows 기반 설치 관리자를 사용 하 여 사용자의 MED-V 구성 요소를 제거 하도록 ESD (전자 소프트웨어 배포) 시스템을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="13db6-107">또는 일부 MED-V 구성 요소를 수동으로 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="13db6-108">**중요**  MED-V 호스트 에이전트를 제거 하려면 먼저 설치 된 MED-V 작업 영역을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="13db6-109">엔터프라이즈에서 MED-V 구성 요소를 제거 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="13db6-110">전자 소프트웨어 배포 시스템을 사용 하 여 MED-V를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="13db6-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="13db6-111">ESD 시스템을 사용 하 여 제거 하려는 모든 MED-V 작업 영역에 대해 uninstall.exe 실행 프로그램을 호출 하는 스크립트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="13db6-112">파일이 C:\\ProgramData\\Microsoft\\Medv\\Workspace.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="13db6-113">최종 사용자가 제거를 인식 하지 못하도록 제거 실행 프로그램을 자동으로 실행 하도록 플래그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="13db6-114">Med-v 작업 영역이 제거 된 각 컴퓨터에 MED-V 호스트 에이전트 설치 파일을 배포 하는 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="13db6-115">설치 제거를 자동 모드로 실행 하도록 패키지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="13db6-116">ESD 클라이언트는 새 패키지를 사용할 수 있는 시간을 인식 하 고 정의 및 요구 사항에 따라 패키지 제거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="13db6-117">MED-V 작업 영역을 수동으로 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="13db6-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="13db6-118">호스트 컴퓨터에서 **시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="13db6-119">**프로그램 및 기능** 창에서 제거 하려는 med-v 작업 영역을 선택한 다음 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="13db6-120">MED-V 작업 영역의 이름은 "MED-V-V Workspace- &lt; *작업 영역 \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="13db6-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="13db6-121">&lt; *작업 영역 \ _name* &gt; **설정 마법사** 가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="13db6-122">**설정 마법사**에서 **다음**을 클릭 한 다음 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="13db6-123">원하는 경우 확인란을 선택 하 여 MED-V로 만든 마스터 VHD 디스크 및 차이점 보관용 디스크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="13db6-124">이는 필수는 아니지만 제거가 완료 되 면 디스크 공간을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="13db6-125">**제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-125">Click **Remove**.</span></span>

    <span data-ttu-id="13db6-126">**참고**  MED-V가 현재 실행 중인 경우 대화 상자가 나타나고 종료 여부를 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="13db6-127">**예** 를 클릭 하 여 제거를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="13db6-128">제거를 취소 하려면 **아니요** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="13db6-129">또는 `uninstall.exe` 일반적으로 C:\\ProgramData\\Microsoft\\Medv\\Workspace.에 있는 파일을 실행 하 여 med-v 작업 영역을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="13db6-130">MED-V 호스트 에이전트를 수동으로 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="13db6-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="13db6-131">Windows 7 호스트 컴퓨터에서 **시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="13db6-132">**프로그램 및 기능** 창에서 **med-v 호스트 에이전트**를 선택한 다음 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="13db6-133">Windows Installer는 MED-V 호스트 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="13db6-134">**참고**  Med-v 작업 영역을 제거 하기 전에 MED-V 호스트 에이전트를 제거 하려고 하면 MED-V 작업 영역을 먼저 제거 해야 한다는 내용의 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="13db6-135">**확인**을 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="13db6-136">MED-V 작업 영역 포장기를 수동으로 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="13db6-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="13db6-137">호스트 컴퓨터에서 **시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="13db6-138">**프로그램 및 기능** 창에서 **Med-v 작업 영역 포장기**를 선택한 다음 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="13db6-139">Windows Installer는 MED-V 작업 영역 포장기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="13db6-140">**참고**  배포 된 MED-V 작업 영역에 영향을 주지 않고 언제 든 지 MED-V 작업 영역 포장기를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13db6-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="13db6-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="13db6-141">Related topics</span></span>


[<span data-ttu-id="13db6-142">MED-V 구성 요소 배포</span><span class="sxs-lookup"><span data-stu-id="13db6-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





