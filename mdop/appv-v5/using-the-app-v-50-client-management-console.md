---
title: App-V 5.0 Client Management Console 사용
description: App-V 5.0 Client Management Console 사용
author: dansimp
ms.assetid: 36398307-57dd-40f3-9d4f-b09f44fd37c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8541e5bc59334b9074a3940dad7cdf0114205d4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813260"
---
# <span data-ttu-id="4d7c6-103">App-V 5.0 Client Management Console 사용</span><span class="sxs-lookup"><span data-stu-id="4d7c6-103">Using the App-V 5.0 Client Management Console</span></span>


<span data-ttu-id="4d7c6-104">이 항목에서는 App-v 5.0 클라이언트를 구성 하 고 관리 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-104">This topic provides information about how you can configure and manage the App-V 5.0 client.</span></span>

## <span data-ttu-id="4d7c6-105">앱-V 5.0 클라이언트 구성 수정</span><span class="sxs-lookup"><span data-stu-id="4d7c6-105">Modify App-V 5.0 client configuration</span></span>


<span data-ttu-id="4d7c6-106">App-v 5.0 클라이언트에는 환경에서 클라이언트가 실행 되는 방식을 결정 하도록 구성할 수 있는 설정이 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-106">The App-V 5.0 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="4d7c6-107">클라이언트를 실행 하는 컴퓨터 또는 PowerShell 또는 그룹 정책을 사용 하 여 이러한 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="4d7c6-108">PowerShell 또는 그룹 정책 구성을 사용 하 여 클라이언트를 수정 하는 방법에 대 한 자세한 내용은 [powershell을 사용 하 여 클라이언트 구성을 수정](how-to-modify-client-configuration-by-using-powershell.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span></span>

## <a href="" id="the-app-v-5-0-client-management-console-"></a><span data-ttu-id="4d7c6-109">App-v 5.0 클라이언트 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="4d7c6-109">The App-V 5.0 client management console</span></span>


<span data-ttu-id="4d7c6-110">App-v 5.0 클라이언트 관리 콘솔을 사용 하 여 App-v 5.0 클라이언트에 대 한 정보를 얻고 특정 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-110">You can obtain information about the App-V 5.0 client or perform specific tasks by using the App-V 5.0 client management console.</span></span> <span data-ttu-id="4d7c6-111">클라이언트 관리 콘솔에서 수행할 수 있는 많은 작업은 PowerShell을 사용 하 여 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="4d7c6-112">각 작업에 대해 연결 된 PowerShell cmdlet도 다음 표에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="4d7c6-113">PowerShell을 사용 하는 방법에 대 한 자세한 내용은 [powershell을 사용 하 여 App-v 관리](administering-app-v-by-using-powershell.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-113">For more information about how to use PowerShell, see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

<span data-ttu-id="4d7c6-114">클라이언트 관리 콘솔에는 다음의 설명 된 기본 탭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4d7c6-115">탭</span><span class="sxs-lookup"><span data-stu-id="4d7c6-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="4d7c6-116">설명</span><span class="sxs-lookup"><span data-stu-id="4d7c6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d7c6-117">개요</span><span class="sxs-lookup"><span data-stu-id="4d7c6-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d7c6-118"><strong>개요 </strong> 탭에는 다음 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="4d7c6-119">업데이트 – <strong> 업데이트 타일을 사용 </strong> 하 여 가상화 된 응용 프로그램을 새로 고치거 나 새 가상화 된 패키지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="4d7c6-120"><strong>마지막 새로 고침에는 </strong> 가상화 된 패키지의 현재 버전이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="4d7c6-121">모든 가상 응용 프로그램 다운로드- <strong> 다운로드 타일을 사용 </strong> 하 여 현재 사용자에 게 프로 비전 된 모든 패키지를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="4d7c6-122">(연결 된 PowerShell cmdlet: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="4d7c6-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="4d7c6-123">오프 라인으로 작업-이 타일을 사용 하 여 모든 자동 및 수동 가상 응용 프로그램 업데이트를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="4d7c6-124">(연결 된 PowerShell cmdlet: <strong> Set-AppvPublishServer-UserRefreshEnabled – GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="4d7c6-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d7c6-125">가상 앱</span><span class="sxs-lookup"><span data-stu-id="4d7c6-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d7c6-126"><strong>가상 앱 탭에는 </strong> 사용자에 게 게시 된 모든 패키지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="4d7c6-127">특정 패키지를 클릭 하 여 해당 패키지에 포함 된 모든 응용 프로그램을 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="4d7c6-128">이는 현재 사용 중인 패키지에 대 한 정보와 컴퓨터에 다운로드 된 각 패키지의 크기를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="4d7c6-129">패키지 다운로드를 시작 하 고 중지할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="4d7c6-130">또한 사용자 상태를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="4d7c6-131">복구는 패키지와 연결 된 모든 사용자 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d7c6-132">앱 연결 그룹</span><span class="sxs-lookup"><span data-stu-id="4d7c6-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d7c6-133"><strong>앱 연결 그룹 탭에는 </strong> 현재 사용자가 사용할 수 있는 모든 연결 그룹이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="4d7c6-134">특정 연결 그룹을 클릭 하 여 선택한 그룹의 일부인 모든 패키지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="4d7c6-135">이는 이미 사용 중인 연결 그룹에 대 한 정보와 컴퓨터에 다운로드 된 연결 그룹 콘텐츠의 양을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="4d7c6-136">또한 연결 그룹 다운로드를 시작 하 고 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="4d7c6-137">이 섹션을 사용 하 여 복구를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="4d7c6-138">복구는 연결 그룹과 연결 된 모든 사용자 상태를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d7c6-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="4d7c6-139">(연결 된 PowerShell cmdlet: 다운로드- <strong> Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="4d7c6-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="4d7c6-140">복구- <strong> AppvClientConnectionGroup </strong> .)</span><span class="sxs-lookup"><span data-stu-id="4d7c6-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="4d7c6-141">Client Management Console에 액세스하는 방법</span><span class="sxs-lookup"><span data-stu-id="4d7c6-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console.md)

[<span data-ttu-id="4d7c6-142">클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="4d7c6-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-beta.md)






## <span data-ttu-id="4d7c6-143">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4d7c6-143">Related topics</span></span>


[<span data-ttu-id="4d7c6-144">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="4d7c6-144">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





