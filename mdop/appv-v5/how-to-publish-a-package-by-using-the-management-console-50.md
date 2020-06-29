---
title: 관리 콘솔을 사용하여 패키지를 게시하는 방법
description: 관리 콘솔을 사용하여 패키지를 게시하는 방법
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813785"
---
# <span data-ttu-id="b519f-103">관리 콘솔을 사용하여 패키지를 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="b519f-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="b519f-104">App-v 5.0 패키지를 게시 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="b519f-105">패키지를 게시 하면 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 해당 패키지의 응용 프로그램에 액세스 하 고 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="b519f-106">**참고**  앱-V 5.0 SP3에서 시작 하는 경우에는 관리자만 패키지를 게시 하거나 게시 취소할 수 있는 기능이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="b519f-107">App-v 5.0 패키지 게시</span><span class="sxs-lookup"><span data-stu-id="b519f-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="b519f-108">앱-V 5.0 관리 콘솔에서</span><span class="sxs-lookup"><span data-stu-id="b519f-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="b519f-109">게시할 패키지의 이름을 마우스 오른쪽 단추로 클릭 하 고 **게시**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="b519f-110">**상태** 열을 검토 하 여 패키지가 게시 되었고 현재 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="b519f-111">패키지를 사용할 수 있는 경우 **게시** 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="b519f-112">패키지가 성공적으로 게시 되지 않으면 **게시** 되지 않은 상태와 함께 패키지를 사용할 수 없는 이유를 설명 하는 오류 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="b519f-113">관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b519f-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="b519f-114">다음 그룹 정책 개체 노드로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="b519f-115">**컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시**.</span><span class="sxs-lookup"><span data-stu-id="b519f-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="b519f-116">**관리자 권한으로 게시** 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="b519f-117">또는 PowerShell을 사용 하 여이 항목을 설정 하려면 [powershell을 사용 하 여 독립 실행형 컴퓨터에서 실행 되는 app-v 5.0 패키지를 관리 하는 방법을](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b519f-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="b519f-118">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="b519f-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b519f-119">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b519f-120">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="b519f-120">Got an App-V issue?</span></span>** <span data-ttu-id="b519f-121">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b519f-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b519f-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b519f-122">Related topics</span></span>


[<span data-ttu-id="b519f-123">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="b519f-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="b519f-124">관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="b519f-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





