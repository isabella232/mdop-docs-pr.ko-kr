---
title: MED-V 작업 영역을 시작, 중지 및 다시 시작하는 방법
description: MED-V 작업 영역을 시작, 중지 및 다시 시작하는 방법
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825723"
---
# <span data-ttu-id="32335-103">MED-V 작업 영역을 시작, 중지 및 다시 시작하는 방법</span><span class="sxs-lookup"><span data-stu-id="32335-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="32335-104">MED-V 작업 영역을 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="32335-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="32335-105">알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="32335-106">하위 메뉴에서 **시작 작업 영역**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="32335-107">컴퓨터에서 실행 중인 MED-V 작업 영역이 여러 개인 경우 **작업 영역 선택** 창이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="32335-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="32335-108">MED-V 작업 영역을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="32335-109">다음에 **묻지 않고 선택한 작업 영역 시작** 확인란을 선택 하 여 다음에 클라이언트가 시작 될 때이 창을 건너뛰고 선택한 med-v 작업 영역을 자동으로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="32335-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="32335-110">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-110">Click **OK**.</span></span>

    <span data-ttu-id="32335-111">**작업 영역 인증 시작** 창이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="32335-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="32335-112">컴퓨터에 MED-V 작업 영역이 여러 개 있고 지정 된 MED-V 작업 영역을 사용 하기로 결정 한 경우 다음 그림에 표시 된 창이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="32335-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="32335-113">컴퓨터에 MED-V 작업 영역이 하나만 있는 경우 "마지막으로 사용한 작업 영역 시작" 옵션을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32335-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="32335-114">도메인 사용자 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="32335-115">**참고**  Med-v 작업 영역이 처음 시작 될 때 사용자 이름은 &lt; 도메인 이름 &gt; \\ &lt; 사용자 이름 형식 이어야 &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="32335-116">**내 비밀 번호 저장** 을 선택 하 여 세션 간에 비밀 번호를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="32335-117">**참고**  암호 저장 기능을 사용 하도록 설정 하려면 ClientSettings.xml 파일에서 EnableSavePassword 특성을 True로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="32335-118">이 파일은 *Servers\\configuration Server\\* 폴더에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32335-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="32335-119">다른 MED-V 작업 영역을 선택 하려면 **마지막으로 사용한 작업 영역 시작** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="32335-120">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-120">Click **OK**.</span></span>

    <span data-ttu-id="32335-121">MED-V 작업 영역 구성에 따라 몇 가지 상태 화면이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32335-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="32335-122">**작업 영역 시작** 화면이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="32335-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="32335-123">MED-V 작업 영역을 다시 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="32335-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="32335-124">클라이언트가 실행 되는 경우 알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="32335-125">하위 메뉴에서 **작업 영역 다시 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="32335-126">MED-V 작업 영역이 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32335-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="32335-127">영구 MED-V 작업 영역에서 가상 컴퓨터를 종료 한 다음 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="32335-128">Revertible MED-V 작업 영역에서 가상 컴퓨터는 실제로 종료 되지 않습니다. 그 대신 원래 상태로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="32335-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="32335-129">MED-V 작업 영역을 중지 하려면</span><span class="sxs-lookup"><span data-stu-id="32335-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="32335-130">알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="32335-131">하위 메뉴에서 **작업 영역 중지**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="32335-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="32335-132">MED-V 작업 영역이 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32335-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="32335-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="32335-133">Related topics</span></span>


[<span data-ttu-id="32335-134">MED-V 클라이언트를 시작 및 종료하는 방법</span><span class="sxs-lookup"><span data-stu-id="32335-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 





