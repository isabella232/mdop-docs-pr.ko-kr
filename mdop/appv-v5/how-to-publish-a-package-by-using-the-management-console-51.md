---
title: 관리 콘솔을 사용하여 패키지를 게시하는 방법
description: 관리 콘솔을 사용하여 패키지를 게시하는 방법
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813769"
---
# <span data-ttu-id="a69a4-103">관리 콘솔을 사용하여 패키지를 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="a69a4-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="a69a4-104">App-v 5.1 패키지를 게시 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="a69a4-105">패키지를 게시 하면 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 해당 패키지의 응용 프로그램에 액세스 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="a69a4-106">**참고**  앱-V 5.0 SP3에서 시작 하는 경우에는 관리자만 패키지를 게시 하거나 게시 취소할 수 있는 기능이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="a69a4-107">App-v 5.1 패키지 게시</span><span class="sxs-lookup"><span data-stu-id="a69a4-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="a69a4-108">앱-V 5.1 관리 콘솔에서</span><span class="sxs-lookup"><span data-stu-id="a69a4-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="a69a4-109">게시할 패키지의 이름을 클릭 하거나 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="a69a4-110">**게시**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="a69a4-111">**상태** 열을 검토 하 여 패키지가 게시 되었고 현재 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="a69a4-112">패키지를 사용할 수 있는 경우 **게시** 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="a69a4-113">패키지가 성공적으로 게시 되지 않으면 **게시** 되지 않은 상태와 함께 패키지를 사용할 수 없는 이유를 설명 하는 오류 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="a69a4-114">관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="a69a4-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="a69a4-115">다음 그룹 정책 개체 노드로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="a69a4-116">**컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시**.</span><span class="sxs-lookup"><span data-stu-id="a69a4-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="a69a4-117">**관리자 권한으로 게시** 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="a69a4-118">또는 PowerShell을 사용 하 여이 항목을 설정 하려면 [powershell을 사용 하 여 독립 실행형 컴퓨터에서 실행 되는 app-v 5.1 패키지를 관리 하는 방법을](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a69a4-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="a69a4-119">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="a69a4-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a69a4-120">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a69a4-121">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="a69a4-121">Got an App-V issue?</span></span>** <span data-ttu-id="a69a4-122">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69a4-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a69a4-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a69a4-123">Related topics</span></span>


[<span data-ttu-id="a69a4-124">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="a69a4-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="a69a4-125">관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a69a4-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





