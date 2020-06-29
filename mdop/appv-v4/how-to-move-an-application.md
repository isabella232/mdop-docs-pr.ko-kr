---
title: 응용 프로그램을 이동하는 방법
description: 응용 프로그램을 이동하는 방법
author: dansimp
ms.assetid: 3ebbf30c-b435-4a69-a0ba-2313aaf0017c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01879cf5c1451d49475b1c1984f6881a3969eef2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816913"
---
# <span data-ttu-id="8a8d3-103">응용 프로그램을 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="8a8d3-103">How to Move an Application</span></span>


<span data-ttu-id="8a8d3-104">응용 프로그램 가상화 서버 관리 콘솔의 **응용 프로그램 노드 아래** 에 응용 프로그램 그룹이 있는 경우 그룹 간에 또는 주 노드에서 그룹으로 응용 프로그램을 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-104">If you have application groups under the **Applications** node in the Application Virtualization Server Management Console, you can move an application between groups or from the main node to a group.</span></span> <span data-ttu-id="8a8d3-105">응용 프로그램을 작업에 맞게 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-105">You can move the applications to suit your operations.</span></span> <span data-ttu-id="8a8d3-106">또한 중첩 된 그룹의 속성을 동시에 변경할 수 있도록 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-106">You also can group them so that you can change the properties of nested groups simultaneously.</span></span>

<span data-ttu-id="8a8d3-107">**중요**  응용 프로그램을 이동 **하려면 응용 프로그램 노드 아래** 에 응용 프로그램 그룹이 하나 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-107">**Important** You must have one or more application groups under the **Applications** node to move applications.</span></span>

 

**<span data-ttu-id="8a8d3-108">응용 프로그램을 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8a8d3-108">To move an application</span></span>**

1.  <span data-ttu-id="8a8d3-109">Application Virtualization Server 관리 콘솔의 왼쪽 창에서 **응용 프로그램**을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-109">In the left pane of the Application Virtualization Server Management Console, expand **Applications**.</span></span>

2.  <span data-ttu-id="8a8d3-110">이동 하려는 응용 프로그램을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-110">Highlight the application you want to move.</span></span>

3.  <span data-ttu-id="8a8d3-111">응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **이동을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-111">Right-click the application and choose **Move**.</span></span>

4.  <span data-ttu-id="8a8d3-112">**대상 선택** 창에서이 그룹을 추가할 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-112">In the **Select Target** window, navigate to the group in which you want to place this group.</span></span>

5.  <span data-ttu-id="8a8d3-113">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-113">Click **OK**.</span></span>

    <span data-ttu-id="8a8d3-114">이제 응용 프로그램이 대상 그룹 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-114">The applications now appear under the target group.</span></span> <span data-ttu-id="8a8d3-115">이 이동으로 인해 그룹 또는 해당 응용 프로그램의 속성은 변경 되지 않으며, 서버에 있는 응용 프로그램이 파일을 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-115">This move does not change the properties of the group or its applications, and it does not move any of the application's files on the server.</span></span>

    <span data-ttu-id="8a8d3-116">**참고**  여러 응용 프로그램 그룹을 동시에 선택 및 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-116">**Note** You can select and move multiple application groups simultaneously.</span></span> <span data-ttu-id="8a8d3-117">오른쪽 창에서 **CTRL**+ 클릭 또는 **Shift**키 조합을 사용 하 여 두 개 이상의 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-117">In the right pane, use the **CTRL**-click or **Shift**-click key combinations to select more than one group.</span></span>

     

## <span data-ttu-id="8a8d3-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8a8d3-118">Related topics</span></span>


[<span data-ttu-id="8a8d3-119">응용 프로그램 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="8a8d3-119">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)

[<span data-ttu-id="8a8d3-120">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="8a8d3-120">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





