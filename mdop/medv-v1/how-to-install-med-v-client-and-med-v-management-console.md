---
title: MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법
description: MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826983"
---
# <span data-ttu-id="23c2a-103">MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="23c2a-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="23c2a-104">다음 MED-V 구성 요소는 클라이언트 .msi 패키지에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="23c2a-105">MED-V 클라이언트 — MED-V 작업 영역을 실행 하기 위해 클라이언트 컴퓨터에 설치 해야 하는 MED-V 소프트웨어입니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="23c2a-106">MED-V 관리 콘솔-관리자가 이미지, MED-V 작업 영역, 정책을 만들고 유지 관리 하는 데 사용할 수 있는 관리 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="23c2a-107">MED-V 관리 콘솔과 MED-V 클라이언트는 둘 다 MED-V 클라이언트 .msi 패키지에서 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="23c2a-108">그러나 med-v 클라이언트는 설치 중에 **Med-v 관리 응용 프로그램 설치** 확인란의 선택을 취소 하 여 med-v 관리 콘솔 없이 독립적으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="23c2a-109">참고</span><span class="sxs-lookup"><span data-stu-id="23c2a-109">Note</span></span>**  
<span data-ttu-id="23c2a-110">MED-V 클라이언트와 MED-V 관리 콘솔은 Windows 7, Windows Vista 및 Windows XP 기반 컴퓨터에만 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="23c2a-111">서버 제품에 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="23c2a-112">참고</span><span class="sxs-lookup"><span data-stu-id="23c2a-112">Note</span></span>**  
<span data-ttu-id="23c2a-113">Windows **runas** 명령을 사용 하 여 med-v 클라이언트를 설치 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="23c2a-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="23c2a-114">MED-V 클라이언트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="23c2a-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="23c2a-115">로컬 컴퓨터에서 로컬 관리자 권한이 있는 사용자로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="23c2a-116">MED-V 패키지를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="23c2a-117">MED-V 패키지는 *MED-V\_x.msi*호출 되며 여기서 *x* 는 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="23c2a-118">예를 들어 *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="23c2a-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="23c2a-119">**InstallShield 마법사 시작** 화면이 나타나면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="23c2a-120">**사용권 계약** 화면에서 사용권 계약을 **읽고 동의 함을 클릭 한**후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="23c2a-121">기본 설치 폴더가 표시 된 **대상 폴더** 화면이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="23c2a-122">기본 설치 폴더는 운영 체제가 설치 된 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="23c2a-123">MED-V가 설치 될 폴더를 변경 하려면 **변경을**클릭 하 고 기존 폴더를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="23c2a-124">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-124">Click **Next**.</span></span>

6.  <span data-ttu-id="23c2a-125">**Med-v 설정** 화면에서 다음과 같이 med-v 설치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="23c2a-126">' **Med-v 관리 응용 프로그램 설치** ' 확인란을 선택 하 여 설치에 관리 구성 요소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="23c2a-127">참고</span><span class="sxs-lookup"><span data-stu-id="23c2a-127">Note</span></span>**  
        <span data-ttu-id="23c2a-128">엔터프라이즈 데스크톱 가상화 관리자는 MED-V 관리 응용 프로그램을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="23c2a-129">이 응용 프로그램은 데스크톱 이미지 및 MED-V 작업 영역을 구성 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="23c2a-130">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-130">Click **Next**.</span></span>

8. <span data-ttu-id="23c2a-131">**프로그램 설치 준비 완료** 화면에서 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="23c2a-132">MED-V 클라이언트 설치가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-132">The MED-V client installation starts.</span></span> <span data-ttu-id="23c2a-133">이 경우 몇 분 정도 걸릴 수 있으며 화면에 텍스트가 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="23c2a-134">설치 중에 몇 가지 진행 화면이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="23c2a-135">메시지가 표시 되 면 제공 된 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="23c2a-136">성공적으로 설치 되 면 **InstallShield 마법사 완료** 화면이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="23c2a-137">**마침을** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="23c2a-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="23c2a-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="23c2a-138">Related topics</span></span>


[<span data-ttu-id="23c2a-139">지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="23c2a-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="23c2a-140">설치 및 업그레이드 검사 목록</span><span class="sxs-lookup"><span data-stu-id="23c2a-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









