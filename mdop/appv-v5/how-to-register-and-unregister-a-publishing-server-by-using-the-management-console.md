---
title: 관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법
description: 관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법
author: dansimp
ms.assetid: c24f3b43-4888-41a9-9a39-973657f2b917
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5241af748029b7976c49b6474e5ef7c050699dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813764"
---
# <span data-ttu-id="80416-103">관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="80416-103">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>


<span data-ttu-id="80416-104">App-v 5.0 관리 서버와 동기화 되는 게시 서버를 등록 및 등록 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80416-104">You can register and unregister publishing servers that will synchronize with the App-V 5.0 management server.</span></span> <span data-ttu-id="80416-105">게시 서버에서 관리 서버와 정보를 동기화 하기 위해 마지막으로 시도한 시도도 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80416-105">You can also see the last attempt that the publishing server made to synchronize the information with the management server.</span></span>

<span data-ttu-id="80416-106">게시 서버를 등록 하거나 등록 취소 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-106">Use the following procedure to register or unregister a publishing server.</span></span>

**<span data-ttu-id="80416-107">관리 콘솔을 사용 하 여 게시 서버를 등록 하려면</span><span class="sxs-lookup"><span data-stu-id="80416-107">To register a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="80416-108">관리 콘솔에 연결 하 고 **서버**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-108">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="80416-109">관리 콘솔에 연결 하는 방법에 대 한 자세한 내용은 [관리 콘솔에 연결](how-to-connect-to-the-management-console-beta.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80416-109">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-beta.md).</span></span>

2.  <span data-ttu-id="80416-110">관리 서버와 이미 동기화 하는 게시 서버 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80416-110">A list of publishing servers that already synchronize with the management server is displayed.</span></span> <span data-ttu-id="80416-111">새 서버 등록을 클릭 하 여 새 서버 등록</span><span class="sxs-lookup"><span data-stu-id="80416-111">Click Register New Server to register a new server.</span></span>

3.  <span data-ttu-id="80416-112">**서버 이름 줄에** 도메인에 가입 된 컴퓨터 이름을 입력 하 여 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-112">Type a computer name of a domain joined computer on the **Server Name** line, to specify a name for the server.</span></span> <span data-ttu-id="80416-113">도메인 이름 (예: **MyDomain\\TestServer**)도 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-113">You should also include a domain name, for example, **MyDomain\\TestServer**.</span></span> <span data-ttu-id="80416-114">**확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-114">Click **Check**.</span></span>

4.  <span data-ttu-id="80416-115">컴퓨터를 선택 하 고 **추가** 를 클릭 하 여 서버 목록에 컴퓨터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-115">Select the computer and click **Add** to add the computer to the list of servers.</span></span> <span data-ttu-id="80416-116">목록에 새 서버가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80416-116">The new server will be displayed in the list.</span></span>

**<span data-ttu-id="80416-117">관리 콘솔을 사용 하 여 게시 서버 등록 취소</span><span class="sxs-lookup"><span data-stu-id="80416-117">To unregister a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="80416-118">관리 콘솔에 연결 하 고 **서버**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-118">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="80416-119">관리 콘솔에 연결 하는 방법에 대 한 자세한 내용은 [관리 콘솔에 연결](how-to-connect-to-the-management-console-beta.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80416-119">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-beta.md).</span></span>

2.  <span data-ttu-id="80416-120">관리 서버와 동기화 하는 게시 서버 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80416-120">A list of publishing servers that synchronize with the management server is displayed.</span></span>

3.  <span data-ttu-id="80416-121">서버를 등록 취소 하려면 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 하 고 컴퓨터 이름을 선택한 다음 **서버 등록 취소**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-121">To unregister the server, right-click the computer name and select the computer name and select **unregister server**.</span></span>

    <span data-ttu-id="80416-122">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="80416-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="80416-123">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="80416-124">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="80416-124">Got an App-V issue?</span></span>** <span data-ttu-id="80416-125">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80416-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="80416-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="80416-126">Related topics</span></span>


[<span data-ttu-id="80416-127">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="80416-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





