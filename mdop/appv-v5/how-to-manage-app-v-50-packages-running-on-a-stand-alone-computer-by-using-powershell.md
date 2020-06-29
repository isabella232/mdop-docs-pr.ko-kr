---
title: PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법
description: PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813921"
---
# <span data-ttu-id="21ba5-103">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="21ba5-103">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="21ba5-104">다음 섹션에서는 PowerShell을 사용 하 여 독립 실행형 클라이언트 컴퓨터에서 다양 한 관리 작업을 수행 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="21ba5-105">패키지 목록을 반환 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="21ba5-106">패키지를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="21ba5-107">패키지 게시</span><span class="sxs-lookup"><span data-stu-id="21ba5-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="21ba5-108">특정 사용자에 게 패키지를 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="21ba5-109">패키지를 추가 하 고 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="21ba5-110">기존 패키지의 게시를 취소 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="21ba5-111">특정 사용자에 대 한 패키지의 게시를 취소 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="21ba5-112">기존 패키지를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="21ba5-113">관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="21ba5-114">보류 중인 패키지 이해 (UserPending 및 GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="21ba5-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="21ba5-115">패키지 목록을 반환 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-115">To return a list of packages</span></span>


<span data-ttu-id="21ba5-116">다음 정보를 사용 하 여 특정 사용자에 게 부여 되는 패키지 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="21ba5-117">**Cmdlet**: Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-118">**매개 변수**:-Name-Version-PackageID-이름</span><span class="sxs-lookup"><span data-stu-id="21ba5-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="21ba5-119">**예**: Get-help – Name "ContosoApplication"-Version 2 AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="21ba5-120">패키지를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-120">To add a package</span></span>


<span data-ttu-id="21ba5-121">다음 정보를 사용 하 여 패키지를 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="21ba5-122">**중요**  이 예제에서는 패키지만 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="21ba5-123">사용자 또는 컴퓨터에 패키지를 게시 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="21ba5-124">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-125">**예**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span><span class="sxs-lookup"><span data-stu-id="21ba5-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="21ba5-126">패키지 게시</span><span class="sxs-lookup"><span data-stu-id="21ba5-126">To publish a package</span></span>


<span data-ttu-id="21ba5-127">다음 정보를 사용 하 여 특정 사용자에 게 추가 된 패키지 또는 컴퓨터의 모든 사용자에 게 전역적으로 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21ba5-128">게시 방법</span><span class="sxs-lookup"><span data-stu-id="21ba5-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="21ba5-129">Cmdlet 및 예제</span><span class="sxs-lookup"><span data-stu-id="21ba5-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21ba5-130">사용자에 게 게시</span><span class="sxs-lookup"><span data-stu-id="21ba5-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="21ba5-131">Cmdlet </strong> : 게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="21ba5-132">예 </strong> : Publish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="21ba5-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21ba5-133">전역 게시</span><span class="sxs-lookup"><span data-stu-id="21ba5-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="21ba5-134">Cmdlet </strong> : 게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="21ba5-135">예 </strong> : 게시-AppvClientPackage "ContosoApplication"-Global</span><span class="sxs-lookup"><span data-stu-id="21ba5-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="21ba5-136">특정 사용자에 게 패키지를 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-136">To publish a package to a specific user</span></span>


<span data-ttu-id="21ba5-137">**참고**  이 매개 변수를 사용 하려면 App-v 5.0 SP2 핫픽스 패키지 5 이상을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="21ba5-138">관리자는 **AppvClientPackage** cmdlet을 사용 하 여 Optional **– usersid** 매개 변수를 지정 하 여 특정 사용자에 게 패키지를 게시할 수 있습니다. 여기서 **-USERSID** 는 최종 사용자의 SID (보안 식별자)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="21ba5-139">이 매개 변수를 사용 하려면:</span><span class="sxs-lookup"><span data-stu-id="21ba5-139">To use this parameter:</span></span>

-   <span data-ttu-id="21ba5-140">사용자 또는 관리자 세션에서이 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="21ba5-141">매개 변수를 사용 하려면 관리 자격 증명으로 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="21ba5-142">최종 사용자는 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="21ba5-143">최종 사용자의 SID (보안 식별자)를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="21ba5-144">**Cmdlet**: 게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-145">**예**: 게시-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="21ba5-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="21ba5-146">패키지를 추가 하 고 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-146">To add and publish a package</span></span>


<span data-ttu-id="21ba5-147">다음 정보를 사용 하 여 패키지를 컴퓨터에 추가 하 고 사용자에 게 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="21ba5-148">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-149">**예**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | 게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="21ba5-150">기존 패키지의 게시를 취소 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-150">To unpublish an existing package</span></span>


<span data-ttu-id="21ba5-151">다음 정보를 사용 하 여 사용자에 게 자격이 있는 패키지를 게시 취소 하지만 컴퓨터에서 패키지를 제거할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="21ba5-152">**Cmdlet**: 게시 취소-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-153">**예**: 게시 취소-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="21ba5-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="21ba5-154">특정 사용자에 대 한 패키지의 게시를 취소 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="21ba5-155">**참고**  이 매개 변수를 사용 하려면 App-v 5.0 SP2 핫픽스 패키지 5 이상을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="21ba5-156">관리자는 **AppvClientPackage** cmdlet을 사용 하 여 Optional **– usersid** 매개 변수를 사용 하 여 특정 사용자에 대 한 패키지를 게시 취소할 수 있으며, 여기서 **-USERSID** 는 최종 사용자의 SID (보안 식별자)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="21ba5-157">이 매개 변수를 사용 하려면:</span><span class="sxs-lookup"><span data-stu-id="21ba5-157">To use this parameter:</span></span>

-   <span data-ttu-id="21ba5-158">사용자 또는 관리자 세션에서이 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="21ba5-159">매개 변수를 사용 하려면 관리 자격 증명으로 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="21ba5-160">최종 사용자는 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="21ba5-161">최종 사용자의 SID (보안 식별자)를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="21ba5-162">**Cmdlet**: 게시 취소-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-163">**예**: 게시 취소-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="21ba5-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="21ba5-164">기존 패키지를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-164">To remove an existing package</span></span>


<span data-ttu-id="21ba5-165">다음 정보를 사용 하 여 컴퓨터에서 패키지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="21ba5-166">**Cmdlet**: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="21ba5-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="21ba5-167">**예**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="21ba5-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="21ba5-168">**참고**  위의 예제에서 명확 하 게만 사용할 수 있도록 app-v cmdlet이 변수에 할당 되었습니다. 과제는 요구 사항이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="21ba5-169">대부분의 cmdlet은에 표시 된 대로 결합 [하 여 패키지를 추가 하 고 게시할](#bkmk-add-pub-pkg-standalone-posh)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="21ba5-170">자세한 자습서는 [app-v 5.0 클라이언트 PowerShell 딥](https://go.microsoft.com/fwlink/?LinkId=324466)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21ba5-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="21ba5-171">관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="21ba5-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="21ba5-172">**참고** 
 **이 기능은 app-v 5.0 SP3에서 시작 하는 것으로 지원 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="21ba5-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="21ba5-173">다음 cmdlet 및 매개 변수를 사용 하 여 패키지를 게시 하거나 게시 취소 하는 관리자 (최종 사용자 아님)만 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="21ba5-174">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21ba5-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="21ba5-175">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="21ba5-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="21ba5-176">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21ba5-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="21ba5-177">-Require# asadmin</span><span class="sxs-lookup"><span data-stu-id="21ba5-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="21ba5-178">매개 변수 값:</span><span class="sxs-lookup"><span data-stu-id="21ba5-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="21ba5-179">0-거짓</span><span class="sxs-lookup"><span data-stu-id="21ba5-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="21ba5-180">1-참</span><span class="sxs-lookup"><span data-stu-id="21ba5-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="21ba5-181">예: </strong> : Set-AppvClientConfiguration-RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="21ba5-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21ba5-182">앱-V 관리 콘솔을 사용 하 여이 구성을 설정 하려면 [관리 콘솔을 사용 하 여 패키지를 게시 하는 방법을](how-to-publish-a-package-by-using-the-management-console-50.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21ba5-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="21ba5-183">보류 중인 패키지 이해 (UserPending 및 GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="21ba5-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="21ba5-184">**App-v 5.0 SP2에서 시작**: 현재 사용 중인 패키지에 영향을 주는 PowerShell cmdlet을 실행 하는 경우 수행 하려는 작업이 보류 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="21ba5-185">예를 들어 해당 패키지의 응용 프로그램을 사용 중인 경우 패키지를 게시 하려고 하면 **AppvClientPackage**를 실행 하 고 다음과 같이 보류 상태를 cmdlet 출력에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21ba5-186">Cmdlet 출력 항목</span><span class="sxs-lookup"><span data-stu-id="21ba5-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="21ba5-187">설명</span><span class="sxs-lookup"><span data-stu-id="21ba5-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21ba5-188">UserPending</span><span class="sxs-lookup"><span data-stu-id="21ba5-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="21ba5-189">나열 된 패키지에 사용자에 게 적용 되는 보류 중인 작업이 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="21ba5-190">True</span><span class="sxs-lookup"><span data-stu-id="21ba5-190">True</span></span></p></li>
<li><p><span data-ttu-id="21ba5-191">False</span><span class="sxs-lookup"><span data-stu-id="21ba5-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21ba5-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="21ba5-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="21ba5-193">나열 된 패키지에 컴퓨터에 전역적으로 적용 되는 보류 중인 작업이 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="21ba5-194">True</span><span class="sxs-lookup"><span data-stu-id="21ba5-194">True</span></span></p></li>
<li><p><span data-ttu-id="21ba5-195">False</span><span class="sxs-lookup"><span data-stu-id="21ba5-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21ba5-196">보류 중인 작업은 다음 규칙에 따라 나중에 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21ba5-197">작업 종류</span><span class="sxs-lookup"><span data-stu-id="21ba5-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="21ba5-198">해당 규칙</span><span class="sxs-lookup"><span data-stu-id="21ba5-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21ba5-199">사용자 기반 작업 (예: 패키지를 사용자에 게 게시)</span><span class="sxs-lookup"><span data-stu-id="21ba5-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="21ba5-200">보류 중인 작업은 사용자가 로그 오프 한 다음 다시 로그온 하면 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21ba5-201">전역 기반 작업 (예: 연결 그룹을 전역적으로 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="21ba5-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="21ba5-202">보류 중인 작업은 컴퓨터를 종료 한 후 다시 시작 하면 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21ba5-203">보류 중인 작업에 대 한 자세한 내용은 [앱-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks)정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21ba5-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="21ba5-204">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="21ba5-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="21ba5-205">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="21ba5-206">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="21ba5-206">Got an App-V issue?</span></span>** <span data-ttu-id="21ba5-207">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba5-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="21ba5-208">관련 항목</span><span class="sxs-lookup"><span data-stu-id="21ba5-208">Related topics</span></span>


[<span data-ttu-id="21ba5-209">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="21ba5-209">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="21ba5-210">PowerShell을 사용하여 App-V 관리</span><span class="sxs-lookup"><span data-stu-id="21ba5-210">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





