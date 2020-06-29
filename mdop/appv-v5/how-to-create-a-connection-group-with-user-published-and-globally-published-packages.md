---
title: 사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법
description: 사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814353"
---
# <span data-ttu-id="27dd5-103">사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="27dd5-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>
<span data-ttu-id="27dd5-104">다음 방법 중 하나를 사용 하 여 사용자가 게시 하 고 전역적으로 게시 된 패키지를 모두 포함 하는 사용자 관련 연결 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="27dd5-105">PowerShell cmdlet을 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="27dd5-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="27dd5-106">App-v 서버를 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="27dd5-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="27dd5-107">시작 하기 전에 알아야 할 사항:</span><span class="sxs-lookup"><span data-stu-id="27dd5-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27dd5-108">지원 되지 않는 시나리오 및 잠재적인 문제</span><span class="sxs-lookup"><span data-stu-id="27dd5-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="27dd5-109">결과</span><span class="sxs-lookup"><span data-stu-id="27dd5-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27dd5-110">사용자 게시 패키지는 전역으로 제공 되는 연결 그룹에 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="27dd5-111">연결 그룹이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27dd5-112">패키지를 전역적으로 게시 한 다음 해당 패키지를 선택 하지 않은 사용자가 게시 한 연결 그룹을 만드는 경우, <strong> &lt; &gt; 다른 연결 그룹에서 해당 패키지를 사용 하는 경우에도 게시 취소-AppvClientPackage 패키지-전역 </strong> 을 실행 하 여 패키지를 게시 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="27dd5-113">다른 연결 그룹이 해당 패키지를 사용 하는 경우 해당 연결 그룹에서 패키지가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="27dd5-114">다른 연결 그룹에서 사용 중인 비 선택적 패키지의 게시를 실수로 취소 하지 않도록 하려면 선택 사항 이외의 패키지를 사용한 연결 그룹을 추적 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="27dd5-115">PowerShell cmdlet을 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="27dd5-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="27dd5-116">다음 명령을 사용 하 여 패키지를 추가 하 고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="27dd5-117">추가-AppvClientPackage Package1 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="27dd5-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="27dd5-118">추가-AppvClientPackage Package2 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="27dd5-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="27dd5-119">게시-AppvClientPackage-PackageId Package1 \ _ID--~ Package1 \ _Version ID-전역</span><span class="sxs-lookup"><span data-stu-id="27dd5-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="27dd5-120">게시-AppvClientPackage-PackageId Package2 \ _ID-VersionIdPackage2 \ _ID</span><span class="sxs-lookup"><span data-stu-id="27dd5-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="27dd5-121">연결 그룹 XML 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-121">Create the connection group XML file.</span></span> <span data-ttu-id="27dd5-122">자세한 내용은 [연결 그룹 파일 정보](about-the-connection-group-file.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27dd5-122">For more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

3.  <span data-ttu-id="27dd5-123">다음 명령을 사용 하 여 연결 그룹을 추가 하 고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="27dd5-124">추가-AppvClientConnectionGroup 연결 \ _Group \ _XML \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="27dd5-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="27dd5-125">Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="27dd5-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="27dd5-126">App-v 서버를 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="27dd5-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="27dd5-127">App-v 5.0 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-127">Open the App-V 5.0 Management Console.</span></span>

2.  <span data-ttu-id="27dd5-128">[관리 콘솔을 사용](how-to-publish-a-package-by-using-the-management-console-50.md) 하 여 패키지를 게시 하는 방법의 지침에 따라 패키지를 전역 및 사용자에 게 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="27dd5-129">연결 [그룹을 만드는 방법](how-to-create-a-connection-group.md) 의 지침에 따라 연결 그룹을 만들고 사용자가 게시 하 고 전역적으로 게시 된 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="27dd5-130">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="27dd5-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="27dd5-131">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="27dd5-132">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="27dd5-132">Got an App-V issue?</span></span>** <span data-ttu-id="27dd5-133">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27dd5-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="27dd5-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="27dd5-134">Related topics</span></span>


[<span data-ttu-id="27dd5-135">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="27dd5-135">Managing Connection Groups</span></span>](managing-connection-groups.md)

[<span data-ttu-id="27dd5-136">연결 그룹에서 선택적 패키지를 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="27dd5-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups.md)

 

 





