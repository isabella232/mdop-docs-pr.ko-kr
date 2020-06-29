---
title: PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법
description: PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813889"
---
# <span data-ttu-id="343d1-103">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="343d1-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="343d1-104">App-v 연결 그룹을 사용 하면 모든 가상 응용 프로그램을 단일 가상 환경에서 정의 된 패키지 집합으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="343d1-105">예를 들어 별도의 패키지를 사용 하 여 응용 프로그램 및 플러그 인을 가상화 하 고 단일 연결 그룹에서 함께 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="343d1-106">연결 그룹 XML 파일은 App-v 클라이언트를 설치한 컴퓨터에서 실행 되는 연결 그룹을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="343d1-107">연결 그룹 XML 파일과이 파일을 구성 하는 방법에 대 한 자세한 내용은 [연결 그룹 파일](about-the-connection-group-file51.md)정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="343d1-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

<span data-ttu-id="343d1-108">이 항목에서는 다음 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="343d1-109">연결 그룹에 App-v 패키지를 추가 하 고 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="343d1-110">App-v 클라이언트에서 연결 그룹을 추가 하 고 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="343d1-111">특정 사용자에 대 한 연결 그룹을 설정 하거나 해제 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="343d1-112">관리자만 연결 그룹을 사용할 수 있도록 허용 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a><span data-ttu-id="343d1-113">*연결 그룹에 App-v 패키지를 추가 하 고 게시 하려면*\*</span><span class="sxs-lookup"><span data-stu-id="343d1-113">*To add and publish the App-V packages in the connection group*\*</span></span>

1.  <span data-ttu-id="343d1-114">App-v 클라이언트를 실행 하는 컴퓨터에 App-v 5.1 패키지를 추가 하 고 게시 하려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-114">To add and publish the App-V 5.1 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="343d1-115">추가-AppvClientPackage-path c:\\tmpstore\\quartfin.appv | 게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="343d1-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="343d1-116">연결 그룹의 각 패키지에 대해이 절차의 **1 단계** 를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="343d1-117">App-v 클라이언트에서 연결 그룹을 추가 하 고 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="343d1-118">다음 명령을 입력 하 여 연결 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="343d1-119">추가-AppvClientConnectionGroup – 경로 c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="343d1-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="343d1-120">다음 명령을 입력 하 여 연결 그룹을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="343d1-121">Enable-AppvClientConnectionGroup – name "재무 응용 프로그램"</span><span class="sxs-lookup"><span data-stu-id="343d1-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="343d1-122">구성원 패키지에 있는 가상 응용 프로그램이 대상 컴퓨터에서 실행 되는 경우 연결 그룹의 가상 환경 내에서 실행 되며 연결 그룹의 다른 패키지에 있는 모든 가상 응용 프로그램에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="343d1-123">특정 사용자에 대 한 연결 그룹을 설정 하거나 해제 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="343d1-124">매개 변수 설명 및 요구 사항을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="343d1-125">관리자는이 매개 변수를 사용 하 여 특정 사용자에 대 한 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="343d1-126">이 매개 변수를 사용 하려면 App-v 5.0 SP2 핫픽스 패키지 5 이상을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="343d1-127">사용자 또는 관리자 세션에서이 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="343d1-128">매개 변수를 사용 하려면 관리 자격 증명으로 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="343d1-129">최종 사용자는 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="343d1-130">최종 사용자의 SID (보안 식별자)를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="343d1-131">다음 cmdlet을 사용 하 고 선택적 **– usersid** 매개 변수를 추가 합니다. 여기서 **-usersid** 는 최종 사용자의 SID (보안 식별자)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="343d1-132">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="343d1-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="343d1-133">예</span><span class="sxs-lookup"><span data-stu-id="343d1-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="343d1-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="343d1-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="343d1-135">Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="343d1-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="343d1-136">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="343d1-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="343d1-137">Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="343d1-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="343d1-138">관리자만 연결 그룹을 사용할 수 있도록 허용 하려면</span><span class="sxs-lookup"><span data-stu-id="343d1-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="343d1-139">이 cmdlet을 사용 하는 데 필요한 설명과 요구 사항을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="343d1-140">이 cmdlet 및 매개 변수를 사용 하 여 관리자 (최종 사용자가 아님)만 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있도록 App-v 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="343d1-141">이 cmdlet을 사용 하려면 앱-V 5.0 SP3 이상을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="343d1-142">다음 cmdlet 및 매개 변수를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="343d1-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="343d1-143">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="343d1-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="343d1-144">매개 변수 및 값</span><span class="sxs-lookup"><span data-stu-id="343d1-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="343d1-145">예</span><span class="sxs-lookup"><span data-stu-id="343d1-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="343d1-146">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="343d1-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="343d1-147">– Require# asadmin</span><span class="sxs-lookup"><span data-stu-id="343d1-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="343d1-148">0-거짓</span><span class="sxs-lookup"><span data-stu-id="343d1-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="343d1-149">1-참</span><span class="sxs-lookup"><span data-stu-id="343d1-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="343d1-150">Set-AppvClientConfiguration-RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="343d1-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="343d1-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="343d1-151">Related topics</span></span>


[<span data-ttu-id="343d1-152">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="343d1-152">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="343d1-153">PowerShell을 사용하여 App-V 5.1 관리</span><span class="sxs-lookup"><span data-stu-id="343d1-153">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









