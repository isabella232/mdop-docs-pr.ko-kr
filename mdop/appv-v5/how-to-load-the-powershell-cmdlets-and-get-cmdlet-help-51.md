---
title: PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법
description: PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813948"
---
# <span data-ttu-id="fdc1f-103">PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="fdc1f-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="fdc1f-104">이 주제에 대 한 설명:</span><span class="sxs-lookup"><span data-stu-id="fdc1f-104">What this topic covers:</span></span>

-   [<span data-ttu-id="fdc1f-105">PowerShell cmdlet 사용에 대 한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fdc1f-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="fdc1f-106">PowerShell cmdlet 로드</span><span class="sxs-lookup"><span data-stu-id="fdc1f-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="fdc1f-107">PowerShell cmdlet에 대 한 도움말 보기</span><span class="sxs-lookup"><span data-stu-id="fdc1f-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="fdc1f-108">PowerShell cmdlet에 대 한 도움말 표시</span><span class="sxs-lookup"><span data-stu-id="fdc1f-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="fdc1f-109">PowerShell cmdlet 사용에 대 한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fdc1f-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="fdc1f-110">App-v PowerShell cmdlet을 사용 하기 위해 다음 요구 사항을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdc1f-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="fdc1f-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="fdc1f-112">세부 정보</span><span class="sxs-lookup"><span data-stu-id="fdc1f-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-113">사용자는 다음 방법 중 하나를 사용 하 여 액세스 권한을 부여한 경우에만 App-v 서버 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="fdc1f-114">App-v 서버를 배포 하 고 구성 하는 경우 </strong> :</span><span class="sxs-lookup"><span data-stu-id="fdc1f-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="fdc1f-115">Active Directory 그룹 또는 App-v 환경을 관리할 수 있는 권한이 있는 개별 사용자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="fdc1f-116"><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">App-v 5.1 서버를 배포 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="fdc1f-116">See <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="fdc1f-117">App-v 서버를 배포한 후에는 다음을 </strong> 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="fdc1f-118">앱-V 관리 콘솔을 사용 하 여 추가 Active Directory 그룹 또는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="fdc1f-119"><a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)">관리 콘솔을 사용 하 여 관리자를 추가 하거나 제거 하는 방법에 대해 알아봅니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="fdc1f-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdc1f-120">관리자 권한 명령 프롬프트를 필요로 하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fdc1f-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fdc1f-121">추가-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="fdc1f-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-122">제거-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="fdc1f-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-123">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="fdc1f-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-124">추가-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="fdc1f-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-125">제거-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="fdc1f-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-126">추가-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-127">제거-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-128">송신-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="fdc1f-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-129">Set-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="fdc1f-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-130">Set-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="fdc1f-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-131">Set-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-132">관리자 권한 명령 프롬프트를 요구 하도록 구성 하지 않은 경우 최종 사용자가 실행할 수 있는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="fdc1f-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="fdc1f-133">게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="fdc1f-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-134">게시 취소-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="fdc1f-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="fdc1f-135">관리자 권한 명령 프롬프트가 필요 하도록 이러한 cmdlet을 구성 하려면 다음 방법 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdc1f-136">메서드</span><span class="sxs-lookup"><span data-stu-id="fdc1f-136">Method</span></span></th>
<th align="left"><span data-ttu-id="fdc1f-137">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="fdc1f-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-138"><strong> </strong> <strong> -RequireAppvClientConfiguration asadmin 매개 변수를 사용 하 여 Set-cmdlet을 실행 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="fdc1f-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="fdc1f-139">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="fdc1f-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="fdc1f-140">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.1 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="fdc1f-140">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdc1f-141">App-v 클라이언트에 대 한 "관리자 권한으로 게시 필요" 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)"><span data-ttu-id="fdc1f-142">관리 콘솔을 사용하여 패키지를 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="fdc1f-142">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="fdc1f-143">PowerShell cmdlet 로드</span><span class="sxs-lookup"><span data-stu-id="fdc1f-143">Loading the PowerShell cmdlets</span></span>

<span data-ttu-id="fdc1f-144">PowerShell cmdlet 모듈을 로드 하려면:</span><span class="sxs-lookup"><span data-stu-id="fdc1f-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="fdc1f-145">Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="fdc1f-146">다음 명령 중 하나를 입력 하 여 원하는 모듈에 대 한 cmdlet을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdc1f-147">App-v 구성 요소</span><span class="sxs-lookup"><span data-stu-id="fdc1f-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="fdc1f-148">명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-149">App-v Server</span><span class="sxs-lookup"><span data-stu-id="fdc1f-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-150">가져오기-모듈 AppvServer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdc1f-151">App-V 시퀀서</span><span class="sxs-lookup"><span data-stu-id="fdc1f-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-152">가져오기-모듈 AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-153">App-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="fdc1f-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-154">가져오기-모듈 AppvClient</span><span class="sxs-lookup"><span data-stu-id="fdc1f-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="fdc1f-155">PowerShell cmdlet에 대 한 도움말 보기</span><span class="sxs-lookup"><span data-stu-id="fdc1f-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="fdc1f-156">App-v 5.0 SP3에서 시작 하는 cmdlet 도움말은 두 가지 형식으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdc1f-157">형식</span><span class="sxs-lookup"><span data-stu-id="fdc1f-157">Format</span></span></th>
<th align="left"><span data-ttu-id="fdc1f-158">설명</span><span class="sxs-lookup"><span data-stu-id="fdc1f-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-159">다운로드 가능한 모듈</span><span class="sxs-lookup"><span data-stu-id="fdc1f-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-160">Cmdlet 모듈을 다운로드 한 후에 최신 도움말을 다운로드 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="fdc1f-161">Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="fdc1f-162">다음 명령 중 하나를 입력 하 여 원하는 모듈에 대 한 cmdlet을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdc1f-163">App-v 구성 요소</span><span class="sxs-lookup"><span data-stu-id="fdc1f-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="fdc1f-164">명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-165">App-v Server</span><span class="sxs-lookup"><span data-stu-id="fdc1f-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-166">업데이트-도움말-모듈 AppvServer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdc1f-167">App-V 시퀀서</span><span class="sxs-lookup"><span data-stu-id="fdc1f-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-168">업데이트-도움말-모듈 AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="fdc1f-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdc1f-169">App-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="fdc1f-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-170">업데이트-도움말-모듈 AppvClient</span><span class="sxs-lookup"><span data-stu-id="fdc1f-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdc1f-171">TechNet에서 웹 페이지로</span><span class="sxs-lookup"><span data-stu-id="fdc1f-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdc1f-172"><a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Windows PowerShell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화의 앱-V 노드를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="fdc1f-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="fdc1f-173">PowerShell cmdlet에 대 한 도움말 표시</span><span class="sxs-lookup"><span data-stu-id="fdc1f-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="fdc1f-174">특정 PowerShell cmdlet에 대 한 도움말을 표시 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="fdc1f-175">Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="fdc1f-176">Get-help **Get-Help** &lt; *cmdlet* &gt; 을 입력 합니다 (예: **AppvClientPackage 게시--help)**.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="fdc1f-177">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="fdc1f-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fdc1f-178">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fdc1f-179">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="fdc1f-179">Got an App-V issue?</span></span>** <span data-ttu-id="fdc1f-180">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc1f-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





