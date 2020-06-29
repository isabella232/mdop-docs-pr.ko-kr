---
title: 관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법
description: 관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814468"
---
# <span data-ttu-id="aca12-103">관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="aca12-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="aca12-104">다음 절차에 따라 앱-V 5.0 관리 콘솔에 패키지를 추가 하거나 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-104">You can the following procedure to add or upgrade a package to the App-V 5.0 Management Console.</span></span> <span data-ttu-id="aca12-105">관리 콘솔에 이미 있는 패키지를 업그레이드 하려면 다음 단계를 사용 하 여 동일한 패키지 **이름을**사용 하 여 업그레이드 된 패키지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="aca12-106">관리 콘솔에 패키지를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="aca12-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="aca12-107">관리 콘솔 디스플레이의 탐색 창에서 **패키지** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="aca12-108">콘솔에는 각 패키지에 대 한 상태 정보와 함께 서버에 추가 된 패키지의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="aca12-109">패키지를 선택 하면 패키지에 대 한 자세한 정보가 **패키지** 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="aca12-110">**그룹화** 되지 않은 드롭다운 목록 상자를 클릭 하 고 패키지를 콘솔에 표시 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="aca12-111">연결 된 열 머리글을 클릭 하 여 패키지를 정렬할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="aca12-112">추가 하려는 패키지를 지정 하려면 **패키지 추가 또는 업그레이드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="aca12-113">추가 하려는 패키지의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="aca12-114">UNC 또는 HTTP 경로 형식 (예: **\\\\servername\\sharename\\foldername\\packagename.appv** 또는) **http://server.1234/file.appv** 을 사용 하 고 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="aca12-115">**중요**  파일 이름 확장명이 **appv** 인 패키지를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="aca12-116">페이지에 \*\* &lt; &gt; Packagename를 추가\*\*하는 상태 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="aca12-117">**가져오기 상태** 를 클릭 하 여 가져온 패키지의 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="aca12-118">**확인** 을 클릭 하 여 패키지를 추가 하 고 **패키지 추가** 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="aca12-119">가져오는 동안 오류가 발생 한 경우 **패키지 가져오기** 페이지에서 **세부** 정보를 클릭 하 여 자세한 내용을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="aca12-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="aca12-120">이제 **패키지** 창에서 새로 추가 된 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="aca12-121">**닫기를** 클릭 하 여 **패키지 추가 또는 업그레이드** 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="aca12-122">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="aca12-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="aca12-123">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="aca12-124">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="aca12-124">Got an App-V issue?</span></span>** <span data-ttu-id="aca12-125">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca12-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="aca12-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="aca12-126">Related topics</span></span>


[<span data-ttu-id="aca12-127">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="aca12-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





