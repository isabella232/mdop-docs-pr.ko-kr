---
title: 공급자 정책 노드
description: 공급자 정책 노드
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815833"
---
# <span data-ttu-id="d9a73-103">공급자 정책 노드</span><span class="sxs-lookup"><span data-stu-id="d9a73-103">Provider Policies Node</span></span>


<span data-ttu-id="d9a73-104">**공급자 정책** 노드는 응용 프로그램 가상화 서버 관리 콘솔의 **범위** 창에서 응용 프로그램 가상화 시스템 노드 보다 한 수준 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-104">The **Provider Policies** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="d9a73-105">이 노드를 선택 하면 **결과** 창에 공급자 정책 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-105">When you select this node, the **Results** pane displays a list of provider policies.</span></span> <span data-ttu-id="d9a73-106">**공급자 정책** 노드를 마우스 오른쪽 단추로 클릭 하 여 다음 요소를 포함 하는 팝업 메뉴를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-106">Right-click the **Provider Policies** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-provider-policy"></a>**<span data-ttu-id="d9a73-107">새 공급자 정책</span><span class="sxs-lookup"><span data-stu-id="d9a73-107">New Provider Policy</span></span>**  
<span data-ttu-id="d9a73-108">새 공급자 정책 마법사를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-108">Displays the New Provider Policy Wizard.</span></span> <span data-ttu-id="d9a73-109">이 마법사는 다음 페이지로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-109">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="d9a73-110">**공급자 정책 이름** 필드에 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-110">Enter a name in the **Provider Policy Name** field.</span></span> <span data-ttu-id="d9a73-111">해당 권한을 원할 경우 **관리 콘솔을 사용 하 여 클라이언트 데스크톱 관리** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-111">Select the **Manage client desktop using the Management Console** check box if you want that capability.</span></span> <span data-ttu-id="d9a73-112">연결 된 기능을 원하는 경우 다음 확인란 중 하나 또는 모두를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-112">Select one or both of the following check boxes if you want the associated functionality:</span></span>

    -   **<span data-ttu-id="d9a73-113">사용자가 로그인 할 때 게시 구성 새로 고침</span><span class="sxs-lookup"><span data-stu-id="d9a73-113">Refresh publishing configuration when a user logs in</span></span>**

    -   <span data-ttu-id="d9a73-114">**구성 새로 고침 간격**</span><span class="sxs-lookup"><span data-stu-id="d9a73-114">**Refresh configuration every**.</span></span> <span data-ttu-id="d9a73-115">이 옵션을 선택한 후에 숫자를 입력 하 고 드롭다운 메뉴에서 단위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-115">After selecting this option, enter a number and select the unit from the drop-down menu.</span></span> <span data-ttu-id="d9a73-116">유효한 항목은 최소 **30 분** 에서 최대 **999 일**까지입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-116">Valid entries range from a minimum of **30 minutes** to a maximum of **999 days**.</span></span>

2.  <span data-ttu-id="d9a73-117">**추가** 또는 **제거** 를 클릭 하 여 그룹 배정을 추가 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-117">Click **Add** or **Remove** to add or remove a group assignment.</span></span> <span data-ttu-id="d9a73-118">표준 **Windows 찾아보기** 대화 상자를 사용 하 여 사용자 그룹을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-118">Use the standard **Windows Browse** dialog box to find a user group.</span></span>

3.  <span data-ttu-id="d9a73-119">**공급자 파이프라인 구성** 대화 상자에서 다음 확인란 중 하나를 선택 하 여 연결 된 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-119">Select one of the following check boxes on the **Provider Pipeline Configuration** dialog box to enable the associated feature:</span></span>

    -   <span data-ttu-id="d9a73-120">**인증**— 드롭다운 목록에서 인증 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-120">**Authentication**—Select the type of authentication from the drop-down list.</span></span>

    -   **<span data-ttu-id="d9a73-121">액세스 권한 설정 적용</span><span class="sxs-lookup"><span data-stu-id="d9a73-121">Enforce Access Permission Settings</span></span>**

    -   **<span data-ttu-id="d9a73-122">로그 사용 정보</span><span class="sxs-lookup"><span data-stu-id="d9a73-122">Log Usage Information</span></span>**

    -   <span data-ttu-id="d9a73-123">**라이선스**-드롭다운 목록에서 적용 체계를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-123">**Licensing**—Select an enforcement scheme from the drop-down list.</span></span>

4.  <span data-ttu-id="d9a73-124">**마침을** 클릭 하 여 새 공급자 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-124">Click **Finish** to add the new provider policy.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="d9a73-125">보기</span><span class="sxs-lookup"><span data-stu-id="d9a73-125">View</span></span>**  
<span data-ttu-id="d9a73-126">**결과** 창의 모양 및 콘텐츠를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-126">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="d9a73-127">여기에서 새 창</span><span class="sxs-lookup"><span data-stu-id="d9a73-127">New Window from Here</span></span>**  
<span data-ttu-id="d9a73-128">선택한 노드를 루트 노드로 하 여 새 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-128">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="d9a73-129">새로 고침</span><span class="sxs-lookup"><span data-stu-id="d9a73-129">Refresh</span></span>**  
<span data-ttu-id="d9a73-130">서버 뷰를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-130">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="d9a73-131">목록 내보내기</span><span class="sxs-lookup"><span data-stu-id="d9a73-131">Export List</span></span>**  
<span data-ttu-id="d9a73-132">**결과** 창의 내용이 들어 있는 탭으로 구분 된 텍스트 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-132">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="d9a73-133">이 항목에는 만드는 텍스트 파일의 위치를 지정 하는 표준 **파일 저장** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-133">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="d9a73-134">Help</span><span class="sxs-lookup"><span data-stu-id="d9a73-134">Help</span></span>**  
<span data-ttu-id="d9a73-135">응용 프로그램 가상화 서버 관리 콘솔에 대 한 도움말 시스템을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a73-135">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="d9a73-136">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d9a73-136">Related topics</span></span>


[<span data-ttu-id="d9a73-137">Server Management Console: 공급자 정책 노드</span><span class="sxs-lookup"><span data-stu-id="d9a73-137">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





