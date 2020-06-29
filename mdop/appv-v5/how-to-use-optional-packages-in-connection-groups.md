---
title: 연결 그룹에서 선택적 패키지를 사용하는 방법
description: 연결 그룹에서 선택적 패키지를 사용하는 방법
author: dansimp
ms.assetid: 4d08a81b-55e5-471a-91dc-9a684fb3c9a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 64a2c0758294bfa617d3d85f888cfce3a2c0d21e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813633"
---
# <span data-ttu-id="9bbaa-103">연결 그룹에서 선택적 패키지를 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="9bbaa-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="9bbaa-104">Microsoft Application Virtualization (App-v) 5.0 SP3에서 시작 하는 경우 연결 그룹에 선택적 패키지를 추가 하 여 연결 그룹 관리를 단순화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="9bbaa-105">다음 표에서는 선택적 패키지를 사용 하 여 더 쉽게 완료할 수 있는 작업을 요약 하 고 각 작업에 대 한 지침에 대 한 링크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="9bbaa-106">**참고** 
 **선택적 패키지는 app-v 5.0 SP3 에서만 지원 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="9bbaa-106">**Note**
**Optional packages are supported only in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="9bbaa-107">선택적 패키지를 사용 하기 전에 [연결 그룹에서 선택적 패키지를 사용 하기 위한 요구 사항을](#bkmk-reqs-using-cg)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bbaa-108">지침 링크</span><span class="sxs-lookup"><span data-stu-id="9bbaa-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="9bbaa-109">작업</span><span class="sxs-lookup"><span data-stu-id="9bbaa-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="9bbaa-110">다른 패키지를 포함 하는 여러 사용자에 대해 선택적 패키지와 하나의 연결 그룹을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-111">단일 연결 그룹을 사용 하 여 다른 최종 사용자가 사용할 수 있는 다른 응용 프로그램 그룹 및 플러그 인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="9bbaa-112">예를 들어 Microsoft Office를 모든 최종 사용자에 게 배포 하지만 다른 플러그 인을 다양 한 사용자 하위 집합에 배포 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="9bbaa-113">연결 그룹을 변경 하지 않고 선택적 패키지를 게시 취소 하거나 삭제 하거나 선택적 패키지를 게시 취소 하 고 나중에 다시 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-114">App-v 클라이언트에서 연결 그룹을 사용 하지 않도록 설정, 제거, 편집, 추가, 다시 사용 하지 않고 선택적 패키지를 게시 취소 하거나, 삭제 하거나, 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="9bbaa-115">선택 패키지를 게시 취소 하 고 나중에 연결 그룹을 사용 하지 않도록 설정 하거나 다시 게시할 필요 없이 다시 게시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="9bbaa-116">다른 패키지를 사용 하는 여러 사용자를 위해 선택적 패키지와 함께 하나의 연결 그룹을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bbaa-117">작업 설명</span><span class="sxs-lookup"><span data-stu-id="9bbaa-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="9bbaa-118">작업을 수행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9bbaa-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9bbaa-119">App-v 5.0 SP3 사용</span><span class="sxs-lookup"><span data-stu-id="9bbaa-119">With App-V 5.0 SP3</span></span></strong></p>
<p><span data-ttu-id="9bbaa-120">선택적 패키지를 연결 그룹에 추가 하 여 여러 최종 사용자에 게 서로 다른 응용 프로그램 및 플러그 인 조합을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="9bbaa-121">예 </strong> : Microsoft Office를 최종 사용자에 게 배포 하려고 하지만 사용자의 하위 집합에 대해서만 특정 플러그 인을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="9bbaa-122">이렇게 하려면 Office를 사용 하는 패키지와 Office 플러그 인을 사용 하는 다른 패키지가 포함 된 연결 그룹을 만든 다음 플러그 인 패키지를 선택적으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="9bbaa-123">플러그 인 패키지에 대 한 권한이 없는 최종 사용자는 Office를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bbaa-124">메서드</span><span class="sxs-lookup"><span data-stu-id="9bbaa-124">Method</span></span></th>
<th align="left"><span data-ttu-id="9bbaa-125">단계</span><span class="sxs-lookup"><span data-stu-id="9bbaa-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bbaa-126">App-v Server – 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="9bbaa-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="9bbaa-127">관리 콘솔에서 <strong> 패키지 </strong> 를 선택 하 여 패키지 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-127">In the Management Console, select <strong>PACKAGES</strong> to open the PACKAGES page.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-128">연결 <strong> 그룹을 선택 </strong> 하 여 연결 그룹 라이브러리를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-128">Select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-129">연결 그룹 라이브러리에서 올바른 연결 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-129">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-130"><strong> </strong> 연결 된 패키지 창에서 편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-130">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-131"><strong> </strong> 패키지 이름 옆에 있는 선택 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-131">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-132"><strong>그룹 액세스에 패키지 액세스 추가 확인란을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-132">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="9bbaa-133">이 필수 단계는 Active Directory 그룹에 패키지를 할당할 때 이전에 구성한 패키지 권리가 연결 그룹에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-133">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bbaa-134">App-v 서버-PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="9bbaa-134">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-135">다음 cmdlet을 사용 하 고 <strong> -Optional 매개 변수를 지정 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="9bbaa-135">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="9bbaa-136">추가-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="9bbaa-136">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="9bbaa-137">구문과</span><span class="sxs-lookup"><span data-stu-id="9bbaa-137">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="9bbaa-138">예:</span><span class="sxs-lookup"><span data-stu-id="9bbaa-138">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bbaa-139">독립 실행형 컴퓨터의 app-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="9bbaa-139">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="9bbaa-140">연결 그룹 XML 문서를 만들고 <strong> Package </strong> tag 특성 <strong> isoptional </strong> 을 <strong> "true"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-140">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="9bbaa-141">다음 cmdlet을 사용 하 여 연결 그룹을 추가 하 고 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-141">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="9bbaa-142">추가-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="9bbaa-142">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-143">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="9bbaa-143">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="9bbaa-144">선택적 패키지가 있는 연결 그룹 XML 문서 예:</span><span class="sxs-lookup"><span data-stu-id="9bbaa-144">Example connection group XML document with optional packages:</span></span></strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9bbaa-145">App-v 5.0 SP3 이전 버전을 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="9bbaa-145">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-146">특정 응용 프로그램 및 플러그 인 조합을 특정 사용자가 사용할 수 있도록 하기 위해 여러 연결 그룹을 만들어야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-146">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="9bbaa-147">연결 그룹을 변경 하지 않고 선택적 패키지를 게시 취소 하거나 삭제 하거나 선택적 패키지를 게시 취소 하 고 나중에 다시 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-147">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bbaa-148">작업 설명</span><span class="sxs-lookup"><span data-stu-id="9bbaa-148">Task description</span></span></th>
<th align="left"><span data-ttu-id="9bbaa-149">작업을 수행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9bbaa-149">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9bbaa-150">App-v 5.0 SP3 사용</span><span class="sxs-lookup"><span data-stu-id="9bbaa-150">With App-V 5.0 SP3</span></span></strong></p>
<p><span data-ttu-id="9bbaa-151">앱-V 클라이언트에서 연결 그룹을 사용 하지 않도록 설정 하거나 다시 사용 하지 않고 연결 그룹에 있는 선택적 패키지를 게시 취소 하거나, 삭제 하거나, 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-151">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="9bbaa-152">선택 패키지를 게시 취소 하 고 나중에 연결 그룹을 사용 하지 않도록 설정 하거나 다시 게시할 필요 없이 다시 게시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-152">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="9bbaa-153">예 </strong> : Microsoft Office 플러그 인이 포함 된 선택적 패키지를 게시 하는 경우 플러그 인을 제거 하려면 연결 그룹을 사용 하지 않도록 설정 하지 않고 패키지의 게시를 취소 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-153">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bbaa-154">메서드</span><span class="sxs-lookup"><span data-stu-id="9bbaa-154">Method</span></span></th>
<th align="left"><span data-ttu-id="9bbaa-155">단계</span><span class="sxs-lookup"><span data-stu-id="9bbaa-155">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bbaa-156">App-v Server – 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="9bbaa-156">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9bbaa-157">패키지의 게시를 취소 하려면 관리 콘솔에서 패키지 선택을 선택 <strong> 하 고 </strong> 게시 취소할 패키지를 마우스 오른쪽 단추로 클릭 한 다음 <strong> 게시 취소를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-157">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, right-click the package that you want to unpublish, and click <strong>unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-158">연결 그룹에서 선택적 패키지를 제거 하려면 <strong> 연결 그룹 페이지에서 제거 하려는 </strong> 패키지를 선택 하 고 오른쪽 화살표를 클릭 하 여 왼쪽 아래에 있는 연결 그룹 창에서 패키지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-158">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bbaa-159">독립 실행형 컴퓨터의 app-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="9bbaa-159">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-160">다음 기존 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-160">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="9bbaa-161">게시 취소-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9bbaa-161">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-162">제거-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9bbaa-162">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="9bbaa-163">자세한 내용은 <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> PowerShell을 사용 하 여 독립 실행형 컴퓨터에서 실행 되는 app-v 5.0 패키지를 관리 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="9bbaa-163">For more information, see <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9bbaa-164">App-v 5.0 SP3 이전 버전을 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="9bbaa-164">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-165">다음과 같은 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-165">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="9bbaa-166">사용 하도록 설정 된 각 App-v 클라이언트 컴퓨터에서 연결 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-166">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-167">패키지 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-167">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-168">연결 그룹 정의에서 패키지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-168">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-169">연결 그룹을 다시 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-169">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="9bbaa-170">연결 그룹에서 선택적 패키지를 사용 하기 위한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="9bbaa-170">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="9bbaa-171">연결 그룹에서 선택적 패키지를 사용 하기 전에 다음 요구 사항을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-171">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bbaa-172">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9bbaa-172">Requirement</span></span></th>
<th align="left"><span data-ttu-id="9bbaa-173">세부 정보</span><span class="sxs-lookup"><span data-stu-id="9bbaa-173">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bbaa-174">연결 그룹에는 선택 사항 외의 패키지가 하나 이상 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-174">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9bbaa-175">App-v 서버와 PowerShell cmdlet이 요구 사항이 충족 되었는지 확인 하지 않으므로이 요구 사항을 충족 하는 것이 신중 하 게 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-175">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-176">하나 이상의 선택적 패키지가 포함 되지 않은 연결 그룹을 실수로 만든 경우 최종 사용자가 해당 연결 그룹에서 패키지 된 응용 프로그램을 열려고 하면 연결 그룹이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-176">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="9bbaa-177">사용자 게시 된 연결 그룹에는 전역 또는 사용자에 게 게시 되는 패키지가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-177">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="9bbaa-178">전역 게시 된 연결 그룹에는 전역적으로 게시 된 패키지만 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-178">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="9bbaa-179">연결 그룹의 가상 환경을 시작할 때 패키지를 사용할 수 있도록 전역으로 게시 된 연결 그룹에는 전역으로 게시 되는 패키지가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-179">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="9bbaa-180">사용자가 게시 한 패키지를 포함 하는 전역으로 게시 된 연결 그룹을 추가 하거나 사용 하도록 설정 하려고 하면 연결 그룹이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-180">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bbaa-181">해당 패키지가 포함 된 연결 그룹을 게시 하기 전에 모든 비 선택적 패키지를 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-181">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-182">선택적 패키지가 없는 경우 연결 그룹의 가상 환경을 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-182">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="9bbaa-183">선택적 패키지가 게시 되지 않은 경우 App-v 클라이언트에서 연결 그룹을 추가 하거나 사용할 수 있도록 설정 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-183">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9bbaa-184">전역적으로 게시 된 패키지를 게시 취소 하기 전에 해당 컴퓨터의 모든 사용자에 게 부여 된 연결 그룹에 더 이상 패키지가 필요 하지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-184">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9bbaa-185">시스템이 다른 사용자의 연결 그룹에 속해 있는지 여부를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-185">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="9bbaa-186">전역 패키지를 게시 취소 하면 해당 컴퓨터의 모든 사용자가 사용할 수 없게 되므로 각 사용자의 연결 그룹이 더 이상 패키지를 포함 하 고 있지 않은지 확인 하거나 패키지를 선택적으로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bbaa-186">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="9bbaa-187">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9bbaa-187">Related topics</span></span>


[<span data-ttu-id="9bbaa-188">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="9bbaa-188">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





