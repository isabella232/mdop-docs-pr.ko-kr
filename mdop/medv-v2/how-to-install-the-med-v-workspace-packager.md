---
title: MED-V 작업 영역 패키지 관리자를 설치하는 방법
description: MED-V 작업 영역 패키지 관리자를 설치하는 방법
author: dansimp
ms.assetid: 627478e9-6798-4b32-9a50-7a1b72bea295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e23492852813752f028ae2201e656162d6189642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824848"
---
# <span data-ttu-id="3f075-103">MED-V 작업 영역 패키지 관리자를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="3f075-103">How to Install the MED-V Workspace Packager</span></span>


<span data-ttu-id="3f075-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에는 데스크톱 관리자가 최종 사용자에 게 배포 되는 MED-V 작업 영역 배포 패키지를 만드는 데 사용 하는 **Med-v 작업 패키지 포장기**가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 includes a **MED-V Workspace Packager**, which the desktop administrator uses to create the MED-V workspace deployment packages that are distributed to the end users.</span></span> <span data-ttu-id="3f075-105">포장기는 MED-V 작업 영역을 만드는 방법과 프로세스에 도움이 되는 마법사를 포함 하는 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-105">The packager provides step-by-step guidance on how to create MED-V workspaces and contains wizards that help in the process.</span></span>

<span data-ttu-id="3f075-106">**중요**  마법사를 실행 하기 전에 준비 된 VHD를 설치할 준비가 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-106">**Important** Before you start to run the wizards, make sure that you have a prepared VHD ready to install.</span></span> <span data-ttu-id="3f075-107">자세한 내용은 [Med-v 이미지 준비](prepare-a-med-v-image.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f075-107">For more information, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

 

<span data-ttu-id="3f075-108">이 섹션에서는 **Med-v 작업 영역 포장기**를 설치 또는 복구 하기 위한 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-108">This section provides step-by-step instructions for installing or repairing the **MED-V Workspace Packager**.</span></span>

**<span data-ttu-id="3f075-109">MED-V 작업 영역 포장기를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="3f075-109">To install the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="3f075-110">소프트웨어 다운로드의 일부로 받은 MED-V 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-110">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="3f075-111">MED-V \ _WorkspacePackager \ _Setup 설치 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-111">Double-click the MED-V\_WorkspacePackager\_Setup installation file.</span></span>

    <span data-ttu-id="3f075-112">**MICROSOFT med-v (Enterprise 데스크톱 가상화) 작업 영역 포장기 설정** 마법사가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-112">The **Microsoft Enterprise Desktop Virtualization (MED-V) Workspace Packager Setup** wizard opens.</span></span> <span data-ttu-id="3f075-113">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-113">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="3f075-114">Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-114">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="3f075-115">MED-V 작업 영역 포장기를 설치할 대상 폴더를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-115">Select the destination folder for installing the MED-V Workspace Packager, and then click **Next**.</span></span>

5.  <span data-ttu-id="3f075-116">설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-116">To begin the installation, click **Install**.</span></span>

6.  <span data-ttu-id="3f075-117">설치가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-117">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="3f075-118">패키지를 성공적으로 설치 했는지 확인 하려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 작업 영역 포장기를 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="3f075-118">To verify that the installation of the packager was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager.**</span></span>

    <span data-ttu-id="3f075-119">**Med-v 작업 영역 포장기**를 사용 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f075-119">For information about how to use the **MED-V Workspace Packager**, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="3f075-120">포장기가 예상 대로 열리지 않으면 설치 복구를 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-120">If the packager does not open as expected, you can try to repair the installation.</span></span>

**<span data-ttu-id="3f075-121">MED-V 작업 영역 포장기 설치를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="3f075-121">To repair the MED-V Workspace Packager installation</span></span>**

1.  <span data-ttu-id="3f075-122">MED-V \ _WorkspacePackager \ _Setup 설치 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-122">Double-click the MED-V\_WorkspacePackager\_Setup installation file.</span></span>

    <span data-ttu-id="3f075-123">**MICROSOFT med-v (Enterprise 데스크톱 가상화) 작업 영역 포장기 설정** 마법사가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-123">The **Microsoft Enterprise Desktop Virtualization (MED-V) Workspace Packager Setup** wizard opens.</span></span> <span data-ttu-id="3f075-124">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-124">Click **Next** to continue.</span></span>

2.  <span data-ttu-id="3f075-125">설치에 발생할 수 있는 오류를 해결 하려면 **복구**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-125">To repair errors that might have occurred in the installation, click **Repair**.</span></span>

3.  <span data-ttu-id="3f075-126">복구 프로세스를 시작 하려면 **복구** 를 다시 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-126">To begin the repair process, click **Repair** again.</span></span>

4.  <span data-ttu-id="3f075-127">복구가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="3f075-127">After the repair is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="3f075-128">패키지의 복구가 성공적으로 수행 되었는지 확인 하려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 작업 영역 포장기를 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="3f075-128">To verify that the repair of the packager was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager.**</span></span>

## <span data-ttu-id="3f075-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3f075-129">Related topics</span></span>


[<span data-ttu-id="3f075-130">수동으로 MED-V 호스트 에이전트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="3f075-130">How to Manually Install the MED-V Host Agent</span></span>](how-to-manually-install-the-med-v-host-agent.md)

[<span data-ttu-id="3f075-131">MED-V 구성 요소를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="3f075-131">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





