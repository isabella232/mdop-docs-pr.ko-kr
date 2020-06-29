---
title: PowerShell을 사용하여 App-V 관리
description: PowerShell을 사용하여 App-V 관리
author: dansimp
ms.assetid: 1ff4686a-1e19-4eff-b648-ada091281094
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e7f9171e0ac5589d8f1935e715dfdb9c349192d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814860"
---
# <span data-ttu-id="e8dbb-103">PowerShell을 사용하여 App-V 관리</span><span class="sxs-lookup"><span data-stu-id="e8dbb-103">Administering App-V by Using PowerShell</span></span>


<span data-ttu-id="e8dbb-104">Microsoft Application Virtualization (App-v) 5.0는 관리자가 다양 한 App-v 5.0 작업을 수행 하는 데 도움이 되는 Windows PowerShell cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-104">Microsoft Application Virtualization (App-V) 5.0 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.0 tasks.</span></span> <span data-ttu-id="e8dbb-105">다음 섹션에서는 PowerShell을 App-v 5.0와 함께 사용 하는 방법에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-105">The following sections provide more information about using PowerShell with App-V 5.0.</span></span>

## <span data-ttu-id="e8dbb-106">PowerShell을 사용 하 여 App-v 5.0를 관리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-106">How to administer App-V 5.0 by using PowerShell</span></span>


<span data-ttu-id="e8dbb-107">다음 PowerShell 프로시저를 사용 하 여 다양 한 App-v 5.0 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-107">Use the following PowerShell procedures to perform various App-V 5.0 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8dbb-108">이름</span><span class="sxs-lookup"><span data-stu-id="e8dbb-108">Name</span></span></th>
<th align="left"><span data-ttu-id="e8dbb-109">설명</span><span class="sxs-lookup"><span data-stu-id="e8dbb-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md)"><span data-ttu-id="e8dbb-110">PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-111">PowerShell cmdlet을 설치 하 고 cmdlet 도움말 및 예제를 찾는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="e8dbb-112">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-112">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-113">PowerShell을 사용 하 여 독립 실행형 컴퓨터에서 클라이언트 패키지 수명 주기를 관리 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="e8dbb-114">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-115">PowerShell을 사용 하 여 연결 그룹을 관리 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md)"><span data-ttu-id="e8dbb-116">PowerShell을 사용하여 클라이언트 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-117">PowerShell을 사용 하 여 클라이언트를 수정 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)"><span data-ttu-id="e8dbb-118">PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-119">PowerShell을 사용 하 여 사용자 구성 파일을 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)"><span data-ttu-id="e8dbb-120">PowerShell을 사용하여 배포 구성 파일을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-121">PowerShell을 사용 하 여 배포 구성 파일을 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-50.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-50.md)"><span data-ttu-id="e8dbb-122">PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-123">PowerShell을 사용 하 여 새 패키지를 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md)"><span data-ttu-id="e8dbb-124">PowerShell을 사용하여 패키지 가속기를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-125">PowerShell을 사용 하 여 패키지 가속기를 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="e8dbb-126">패키지 가속기를 사용 하는 경우에는 복잡 한 대형 응용 프로그램을 자동으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)"><span data-ttu-id="e8dbb-127">PowerShell을 사용하여 App-V 5.0 Client에서 보고를 사용하도록 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-127">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-128">앱-V 5.0를 실행 하는 컴퓨터에서 보고 정보를 보낼 수 있도록 설정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-128">Describes how to enable the computer running the App-V 5.0 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md)"><span data-ttu-id="e8dbb-129">App-v 데이터베이스를 설치 하 고 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환 하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8dbb-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-130">계정 이름의 배열을 가져와 표준 및 16 진수 형식으로 해당 SID로 변환 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e8dbb-131">PowerShell 오류 처리</span><span class="sxs-lookup"><span data-stu-id="e8dbb-131">PowerShell Error Handling</span></span>


<span data-ttu-id="e8dbb-132">앱-V 5.0 PowerShell 오류 처리에 대 한 정보를 보려면 다음 표를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-132">Use the following table for information about App-V 5.0 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8dbb-133">Event</span><span class="sxs-lookup"><span data-stu-id="e8dbb-133">Event</span></span></th>
<th align="left"><span data-ttu-id="e8dbb-134">작업</span><span class="sxs-lookup"><span data-stu-id="e8dbb-134">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8dbb-135">포함 된 스크립트와 함께 RollbackOnError 특성 사용</span><span class="sxs-lookup"><span data-stu-id="e8dbb-135">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-136"><strong> </strong> 포함 된 스크립트와 함께 RollbackOnError 특성을 사용 하는 경우 다음 이벤트에 대 한 특성이 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-136">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="e8dbb-137">패키지 제거</span><span class="sxs-lookup"><span data-stu-id="e8dbb-137">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="e8dbb-138">패키지 게시 취소</span><span class="sxs-lookup"><span data-stu-id="e8dbb-138">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="e8dbb-139">가상 환경 종료</span><span class="sxs-lookup"><span data-stu-id="e8dbb-139">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="e8dbb-140">프로세스 종료</span><span class="sxs-lookup"><span data-stu-id="e8dbb-140">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8dbb-141">패키지 이름에<strong>$</span><span class="sxs-lookup"><span data-stu-id="e8dbb-141">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e8dbb-142">패키지 이름에 문자 ()가 포함 된 경우 <strong> $ </strong> 작은따옴표 (')를 사용 해야 합니다 <strong> ( </strong> 예:).</span><span class="sxs-lookup"><span data-stu-id="e8dbb-142">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="e8dbb-143">추가-AppvClientPackage ' Contoso $ App. e 1 '</span><span class="sxs-lookup"><span data-stu-id="e8dbb-143">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="e8dbb-144">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8dbb-144">Related topics</span></span>


[<span data-ttu-id="e8dbb-145">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="e8dbb-145">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





