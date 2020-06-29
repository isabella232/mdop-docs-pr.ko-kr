---
title: 응용 프로그램 그룹을 제거하는 방법
description: 응용 프로그램 그룹을 제거하는 방법
author: dansimp
ms.assetid: 3016b373-f5a0-4c82-96e8-e5e7960f0cc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b392fe84f4318cf7f355de0c07e4d6f1f5108ed7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816783"
---
# <span data-ttu-id="0f29a-103">응용 프로그램 그룹을 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="0f29a-103">How to Remove an Application Group</span></span>


<span data-ttu-id="0f29a-104">다음 절차를 사용 하 여 응용 프로그램 가상화 서버 관리 콘솔에서 다음 두 가지 방법 중 하나로 응용 프로그램 그룹을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-104">You can use the following procedures to remove an application group in the Application Virtualization Server Management Console in one of two ways:</span></span>

<span data-ttu-id="0f29a-105">**주의**  사항 응용 프로그램을 사용 하 여 그룹을 삭제 하면 응용 프로그램 가상화 관리 서버에서 해당 응용 프로그램이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-105">**Caution** Deleting a group with its applications deletes those applications from the Application Virtualization Management Server.</span></span> <span data-ttu-id="0f29a-106">이 작업을 수행 하려고 하면 팝업 창에서 삭제를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-106">When you try to do this, you must confirm the deletion in a pop-up window.</span></span>

 

**<span data-ttu-id="0f29a-107">응용 프로그램 그룹을 비운 다음 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="0f29a-107">To empty and then delete an application group</span></span>**

1.  <span data-ttu-id="0f29a-108">Application Virtualization Server Management Console의 왼쪽 창에서 **응용 프로그램** 을 확장 하 고 제거 하려는 **응용 프로그램** 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-108">In the Application Virtualization Server Management Console, expand **Applications** in the left pane and select the **Application** group you want to remove.</span></span>

2.  <span data-ttu-id="0f29a-109">오른쪽 창에서 유지 하려는 응용 프로그램 및 응용 프로그램 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-109">In the right pane, select the applications and application groups you want to keep.</span></span> <span data-ttu-id="0f29a-110">**CTRL** 및 **Shift** 키를 사용 하 여 여러 응용 프로그램 및 응용 프로그램 그룹을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-110">You can use the **CTRL** and **Shift** keys to select multiple applications and application groups.</span></span>

3.  <span data-ttu-id="0f29a-111">선택한 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **이동을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-111">Right-click the selected applications, and choose **Move**.</span></span>

4.  <span data-ttu-id="0f29a-112">**대상 선택** 창에서 새 위치로 이동 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-112">In the **Select Target** window, navigate to the new location and click **OK**.</span></span> <span data-ttu-id="0f29a-113">여러 응용 프로그램을 둘 이상의 그룹으로 이동 하려면이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-113">Repeat this step if you want to move different applications to more than one group.</span></span>

5.  <span data-ttu-id="0f29a-114">유지 하려는 응용 프로그램 이동을 마쳤으면 응용 프로그램 그룹을 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-114">When you finish moving the applications you want to keep, right-click the application group and choose **Delete**.</span></span>

6.  <span data-ttu-id="0f29a-115">**예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-115">Click **Yes** to confirm.</span></span>

**<span data-ttu-id="0f29a-116">모든 자식 그룹과 해당 응용 프로그램을 사용 하 여 그룹을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="0f29a-116">To delete the group, with all its child groups and its applications</span></span>**

1.  <span data-ttu-id="0f29a-117">Application Virtualization Server Management Console의 왼쪽 창에서 **응용 프로그램** 을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-117">In the Application Virtualization Server Management Console, expand **Applications** in the left pane.</span></span>

2.  <span data-ttu-id="0f29a-118">제거 하려는 응용 프로그램 그룹을 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-118">Right-click the application group you want to remove, and choose **Delete**.</span></span>

3.  <span data-ttu-id="0f29a-119">**예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-119">Click **Yes** to confirm.</span></span>

    <span data-ttu-id="0f29a-120">**참고**  여러 응용 프로그램 그룹을 동시에 선택 및 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-120">**Note** You can select and remove multiple application groups simultaneously.</span></span> <span data-ttu-id="0f29a-121">오른쪽 창에서 **CTRL**+ 클릭 또는 **Shift**키 조합을 사용 하 여 두 개 이상의 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f29a-121">In the right pane, use the **CTRL**-click or **Shift**-click key combinations to select more than one group.</span></span>

     

## <span data-ttu-id="0f29a-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0f29a-122">Related topics</span></span>


[<span data-ttu-id="0f29a-123">Server Management Console에서 응용 프로그램 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="0f29a-123">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="0f29a-124">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="0f29a-124">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





