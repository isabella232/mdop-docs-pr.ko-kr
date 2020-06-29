---
title: 연결 그룹을 만드는 방법
description: 연결 그룹을 만드는 방법
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814340"
---
# <span data-ttu-id="5c744-103">연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="5c744-103">How to Create a Connection Group</span></span>


<span data-ttu-id="5c744-104">이 단계를 사용 하 여 App-v 관리 콘솔을 사용 하 여 연결 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="5c744-105">PowerShell을 사용 하 여 연결 그룹을 만들려면 [powershell을 사용 하 여 독립 실행형 컴퓨터에서 연결 그룹을 관리 하는 방법을](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c744-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span></span>

<span data-ttu-id="5c744-106">패키지를 연결 그룹에 배치 하면 패키지 루트 경로가 병합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="5c744-107">패키지를 제거 하는 경우 나머지 패키지만 병합 된 루트를 유지 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="5c744-108">연결 그룹을 만들려면</span><span class="sxs-lookup"><span data-stu-id="5c744-108">To create a connection group</span></span>**

1.  <span data-ttu-id="5c744-109">App-v 5.0 관리 콘솔에서 **패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-109">In the App-V 5.0 Management Console, select **Packages**.</span></span>

2.  <span data-ttu-id="5c744-110">연결 **그룹** 을 선택 하 여 연결 그룹 라이브러리를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-110">Select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

3.  <span data-ttu-id="5c744-111">**연결 그룹 추가** 를 선택 하 여 새 연결 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-111">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

4.  <span data-ttu-id="5c744-112">**새 연결 그룹** 창에서 그룹에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-112">In the **New Connection Group** pane, type a description for the group.</span></span>

5.  <span data-ttu-id="5c744-113">연결 **된 패키지** 창에서 **편집** 을 클릭 하 여 새 응용 프로그램을 연결 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-113">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

6.  <span data-ttu-id="5c744-114">**패키지 전체 라이브러리** 창에서 추가할 응용 프로그램을 선택 하 고 화살표를 클릭 하 여 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-114">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="5c744-115">응용 프로그램을 제거 하려면 **패키지** 창에서 제거할 응용 프로그램을 선택 하 고 화살표를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-115">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="5c744-116">연결 그룹의 응용 프로그램에 대 한 우선 순위를 해당 하려면 **패키지** 창의 화살표를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-116">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="5c744-117">**중요**  기본적으로 특정 응용 프로그램과 연결 된 Active Directory 도메인 서비스 액세스 구성은 연결 그룹에 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-117">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="5c744-118">Active Directory access 구성을 전송 하려면 다음 **의 패키지** 창에 있는 **그룹 액세스에 패키지 액세스 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-118">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

7.  <span data-ttu-id="5c744-119">모든 응용 프로그램을 추가 하 고 Active Directory 액세스를 구성한 후 **적용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-119">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="5c744-120">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="5c744-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5c744-121">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5c744-122">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="5c744-122">Got an App-V issue?</span></span>** <span data-ttu-id="5c744-123">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c744-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5c744-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5c744-124">Related topics</span></span>


[<span data-ttu-id="5c744-125">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="5c744-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="5c744-126">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="5c744-126">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





