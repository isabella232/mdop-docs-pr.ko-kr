---
title: 게시 서버 노드
description: 게시 서버 노드
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815798"
---
# <span data-ttu-id="dbd16-103">게시 서버 노드</span><span class="sxs-lookup"><span data-stu-id="dbd16-103">Publishing Servers Node</span></span>


<span data-ttu-id="dbd16-104">**게시 서버** 노드는 응용 프로그램 가상화 클라이언트 관리 콘솔의 **범위** 창에서 **응용 프로그램 가상화** 노드 보다 한 수준 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="dbd16-105">이 노드를 선택 하면 **결과** 창에 게시 서버 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="dbd16-106">**게시 서버** 노드를 마우스 오른쪽 단추로 클릭 하 여 다음 요소를 포함 하는 팝업 메뉴를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="dbd16-107">새 서버</span><span class="sxs-lookup"><span data-stu-id="dbd16-107">New Server</span></span>**  
<span data-ttu-id="dbd16-108">이 메뉴 항목에는 새 서버 마법사가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="dbd16-109">이 마법사는 다음 두 페이지로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="dbd16-110">서버 표시 이름 및 서버 유형 입력:</span><span class="sxs-lookup"><span data-stu-id="dbd16-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="dbd16-111">**표시 이름**-서버에 대해 표시 하려는 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="dbd16-112">이 필드는 기본적으로 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="dbd16-113">**유형 (Type**)-서버 유형 드롭다운 목록에서 서버 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="dbd16-114">서버의 연결 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="dbd16-115">**호스트 이름**-서버의 이름 또는 IP 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="dbd16-116">**포트 (port**)-포트 번호에 해당 하는 숫자 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="dbd16-117">서버 종류가 "Application Virtualization Server" 이면 기본값은 554이 고, 서버 유형이 "Standard HTTP Server" 이면 80입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="dbd16-118">**경로**—이 필드는 "/"로 기본 설정 되며 서버 종류가 "응용 프로그램 가상화 서버" 또는 "향상 된 보안 응용 프로그램 가상화 서버" 인 경우 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="dbd16-119">서버 종류가 "표준 HTTP 서버" 또는 "확장 보안 HTTP 서버" 인 경우 **경로** 필드도 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="dbd16-120">여기에서 새 창</span><span class="sxs-lookup"><span data-stu-id="dbd16-120">New Window from Here</span></span>**  
<span data-ttu-id="dbd16-121">이 메뉴 항목을 선택 하 여 선택한 노드를 루트 노드로 하는 새 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="dbd16-122">목록 내보내기</span><span class="sxs-lookup"><span data-stu-id="dbd16-122">Export List</span></span>**  
<span data-ttu-id="dbd16-123">이 메뉴 항목을 사용 하 여 **결과** 창의 내용이 들어 있는 탭으로 구분 된 텍스트 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="dbd16-124">이 항목에는 만드는 텍스트 파일의 위치를 지정 하는 표준 **파일 저장** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="dbd16-125">보기</span><span class="sxs-lookup"><span data-stu-id="dbd16-125">View</span></span>**  
<span data-ttu-id="dbd16-126">메뉴 항목의이 팝업 목록을 통해 **결과** 창의 모양과 내용을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="dbd16-127">새로 고침</span><span class="sxs-lookup"><span data-stu-id="dbd16-127">Refresh</span></span>**  
<span data-ttu-id="dbd16-128">관리 콘솔을 새로 고치려면이 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="dbd16-129">Help</span><span class="sxs-lookup"><span data-stu-id="dbd16-129">Help</span></span>**  
<span data-ttu-id="dbd16-130">이 항목은 관리 콘솔에 대 한 도움말 시스템을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd16-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="dbd16-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dbd16-131">Related topics</span></span>


[<span data-ttu-id="dbd16-132">게시 서버 결과 창</span><span class="sxs-lookup"><span data-stu-id="dbd16-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="dbd16-133">게시 서버 결과 창 열</span><span class="sxs-lookup"><span data-stu-id="dbd16-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





