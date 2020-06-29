---
title: 관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법
description: 관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법
author: dansimp
ms.assetid: 7ff8c436-9d2e-446a-9ea2-bbab7e25bf21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8fbc1a532a39c8688b99c28a2e23b713b348967c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814492"
---
# <span data-ttu-id="8f9f9-103">관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="8f9f9-103">How to Add or Remove an Administrator by Using the Management Console</span></span>


<span data-ttu-id="8f9f9-104">Microsoft App-v (Application Virtualization) 5.1 서버에서 관리자를 추가 하거나 제거 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-104">Use the following procedures to add or remove an administrator on the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

**<span data-ttu-id="8f9f9-105">관리 콘솔을 사용 하 여 관리자를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="8f9f9-105">To add an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="8f9f9-106">Microsoft App-v (Application Virtualization) 5.1 관리 콘솔을 열고 탐색 창에서 **관리자** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-106">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="8f9f9-107">탐색 창에는 현재 App-v (Microsoft Application Virtualization) 5.1 서버에 대 한 관리자 액세스 권한이 있는 AD (Access 디렉터리) 사용자 및 그룹 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-107">The navigation pane displays a list of Access Directory (AD) users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="8f9f9-108">새 관리자를 추가 하려면 **관리자 추가** 를 클릭 합니다. **Active Directory 이름** 필드에 추가 하려는 관리자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-108">To add a new administrator, click **Add Administrator** Type the name of the administrator that you want to add in the **Active Directory Name** field.</span></span> <span data-ttu-id="8f9f9-109">연결 된 사용자 계정 도메인 이름을 제공 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-109">Ensure you provide the associated user account domain name.</span></span> <span data-ttu-id="8f9f9-110">예를 들어 **도메인**  \\  **사용자 이름**입니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-110">For example, **Domain** \\ **UserName**.</span></span>

3.  <span data-ttu-id="8f9f9-111">추가 하려는 계정을 선택 하 고 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-111">Select the account that you want to add and click **Add**.</span></span> <span data-ttu-id="8f9f9-112">서버 관리자 목록에 새 계정이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-112">The new account is displayed in the list of server administrators.</span></span>

**<span data-ttu-id="8f9f9-113">관리 콘솔을 사용 하 여 관리자를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="8f9f9-113">To remove an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="8f9f9-114">Microsoft App-v (Application Virtualization) 5.1 관리 콘솔을 열고 탐색 창에서 **관리자** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-114">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="8f9f9-115">탐색 창에는 현재 App-v (Microsoft Application Virtualization) 5.1 서버에 대 한 관리자 권한이 있는 광고 사용자 및 그룹 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-115">The navigation pane displays a list of AD users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="8f9f9-116">관리자 목록에서 제거할 계정을 마우스 오른쪽 단추로 클릭 하 고 **제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-116">Right-click the account to be removed from the list of administrators and select **Remove**.</span></span>

    <span data-ttu-id="8f9f9-117">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="8f9f9-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="8f9f9-118">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="8f9f9-119">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="8f9f9-119">Got an App-V issue?</span></span>** <span data-ttu-id="8f9f9-120">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f9f9-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="8f9f9-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8f9f9-121">Related topics</span></span>


[<span data-ttu-id="8f9f9-122">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="8f9f9-122">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





