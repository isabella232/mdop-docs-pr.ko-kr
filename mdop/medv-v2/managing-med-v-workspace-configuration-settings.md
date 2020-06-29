---
title: MED-V 작업 영역 구성 설정 관리
description: MED-V 작업 영역 구성 설정 관리
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826158"
---
# <span data-ttu-id="15815-103">MED-V 작업 영역 구성 설정 관리</span><span class="sxs-lookup"><span data-stu-id="15815-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="15815-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0은 레지스트리에 구성 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="15815-105">여기에 포함 된 정보는 MED-V 서비스를 더 잘 관리 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="15815-106">MED-V는 결과 설정 값을 찾을 때 다음 검색 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="15815-107">MED-V는 먼저 컴퓨터 정책을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="15815-108">값이 없는 경우 MED-V는 사용자 정책을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="15815-109">값이 없는 경우 MED-V는 HKEY \ _LOCAL \ _MACHINE \\System 하이브를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="15815-110">값이 없는 경우 MED-V는 HKEY \ _CURRENT 사용자 레지스트리 하이브를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="15815-111">여전히 값이 없는 경우 MED-V는 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="15815-112">일반적으로 HKEY \ _LOCAL \ _MACHINE \\System hive 또는 컴퓨터 정책에 값을 설정 하는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="15815-113">그러나 최종 사용자가 특정 설정을 구성할 수 있도록 하려면 종료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="15815-114">참고</span><span class="sxs-lookup"><span data-stu-id="15815-114">Note</span></span>**  
<span data-ttu-id="15815-115">MED-V 작업 영역을 배포 하기 전에, 스크립트 편집기를 사용 하 여 MED-V 작업 영역 포장기에서 만든 Windows PowerShell 스크립트 (ps1 파일)를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="15815-116">자세한 내용은 [Windows PowerShell을 사용 하 여 고급 설정 구성을](configuring-advanced-settings-by-using-windows-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15815-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="15815-117">MED-V 작업 영역을 배포한 후에는 레지스트리 항목을 편집 하 여 특정 MED-V 구성 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="15815-118">이 섹션에는 구성 가능한 모든 MED-V 레지스트리 키와 사용에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="15815-119">진단 키</span><span class="sxs-lookup"><span data-stu-id="15815-119">Diagnostics Key</span></span>


<span data-ttu-id="15815-120">다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15815-121">이름</span><span class="sxs-lookup"><span data-stu-id="15815-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="15815-122">유형</span><span class="sxs-lookup"><span data-stu-id="15815-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="15815-123">Data/Default</span><span class="sxs-lookup"><span data-stu-id="15815-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="15815-124">설명</span><span class="sxs-lookup"><span data-stu-id="15815-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="15815-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-127">기본값 = 3</span><span class="sxs-lookup"><span data-stu-id="15815-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-128">이벤트 로그에 기록 되는 정보의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="15815-129">수준에는 0 (없음), 1 (오류), 2 (경고), 3 (정보), 4 (디버그)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="15815-130">Fts 키</span><span class="sxs-lookup"><span data-stu-id="15815-130">Fts Key</span></span>


<span data-ttu-id="15815-131">다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15815-132">이름</span><span class="sxs-lookup"><span data-stu-id="15815-132">Name</span></span></th>
<th align="left"><span data-ttu-id="15815-133">유형</span><span class="sxs-lookup"><span data-stu-id="15815-133">Type</span></span></th>
<th align="left"><span data-ttu-id="15815-134">Data/Default</span><span class="sxs-lookup"><span data-stu-id="15815-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="15815-135">설명</span><span class="sxs-lookup"><span data-stu-id="15815-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-138">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-139">처음 설치 시 관리자에 게 자동으로 최종 사용자를 추가할지 여부를 구성&#39;s 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="15815-140">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-141">0 = false: 처음 설치 시 관리자에 게 최종 사용자를 자동으로 추가 하지 않습니다&#39;s 그룹에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-142">1 = true: 처음 설치 시 관리자&#39;s 그룹에 최종 사용자를 자동으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="15815-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-144">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-145">MEDV \*</span><span class="sxs-lookup"><span data-stu-id="15815-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-146">게스트 가상 컴퓨터를 만드는 데 사용 되는 컴퓨터 이름 마스크&#39;s 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-147">마스크에 는% username% 태그를 포함 하 여 컴퓨터 이름의 일부로 사용자 이름을 삽입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="15815-148">마찬가지로,% hostname% 태그는 호스트 컴퓨터의 이름을 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="15815-149">&quot; # &quot; 마스크의 모든 문자는 임의의 숫자로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="15815-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="15815-150">마스크 끝에 있는 별표 (\*) 문자는 임의의 영숫자 문자로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="15815-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="15815-151">괄호를 사용 하 여% hostname% 와% username%의 특정 문자 수를 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="15815-152">예를 들어, &quot; % username% [3]은 (는) &quot; 사용자 이름의 처음 세 문자를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-155">Default = 90</span><span class="sxs-lookup"><span data-stu-id="15815-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-156">처음 설치 시 가상 컴퓨터를 삭제 하 려 할 때 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="15815-157">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-160">기본값 = 120</span><span class="sxs-lookup"><span data-stu-id="15815-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-161">첫 설치 프로그램이 가상 컴퓨터에서 가상 플로피 디스크를 분리 하려고 할 때 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="15815-162">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="15815-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-164">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-165">내부 웹 페이지에 연결 되며 최초 설정 대화 상자 메시지에 표시 되는 사용자 지정 가능 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-168">기본값 = 900</span><span class="sxs-lookup"><span data-stu-id="15815-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-169">처음 설치 시 Windows 탐색기를 기다리는 시간 제한 값 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="15815-170">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="15815-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-173">메시지가 리소스 파일에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-174">처음 설치를 완료할 수 없을 때 최종 사용자에 게 표시 되는 사용자 지정 가능한 메시지</span><span class="sxs-lookup"><span data-stu-id="15815-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="15815-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-177">기본값 = 3</span><span class="sxs-lookup"><span data-stu-id="15815-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-178">MED-V가 최종 사용자 그룹 권한을 부여 하려고 할 때의 최대 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="15815-179">최종 사용자 그룹 권한을 성공적으로 제공할 수 없는 경우 지정 된 다시 시도 값을 초과 하면 가상 컴퓨터 준비 실패가 발생 하 여 MaxRetryCount 값에 적용 될 가능성이 큽니다.</span><span class="sxs-lookup"><span data-stu-id="15815-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="15815-180">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-183">기본값 = 300</span><span class="sxs-lookup"><span data-stu-id="15815-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-184">사용자 그룹 권한을 부여할 때의 제한 시간 값 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="15815-185">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="15815-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-188">처음 설정 하는 동안 MED-V가 수집 하는 로그 파일 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="15815-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-191">기본값 = 120</span><span class="sxs-lookup"><span data-stu-id="15815-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-192">최종 사용자가 처음 설치할 때 연기 될 수 있는 최대 시간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="15815-193">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="15815-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-196">기본값 = 3</span><span class="sxs-lookup"><span data-stu-id="15815-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-197">각 시도가 소프트웨어 오류 이외의 오류로 종료 되는 경우 MED-V가 가상 컴퓨터를 준비 하기 위해 시도할 수 있는 최대 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="15815-198">가상 컴퓨터에 대 한 준비가 실패 하 고 처음으로 설정 다시 시도 횟수가 초과 되는 경우 MED-V는 최종 사용자에 게 실패에 대해 알리고 다시 시도할 수 있는 옵션을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="15815-199">이 수는 MED-V가 시작 될 때마다 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="15815-200">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-201">모드</span><span class="sxs-lookup"><span data-stu-id="15815-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-202">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-203">기본값 = 무인</span><span class="sxs-lookup"><span data-stu-id="15815-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-204">첫 설정이 사용자와 상호 작용 하는 방법을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="15815-205">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-206">참석.</span><span class="sxs-lookup"><span data-stu-id="15815-206">Attended.</span></span></strong> <span data-ttu-id="15815-207">최종 사용자는 처음 설정 하는 동안 정보를 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15815-208">참고</span><span class="sxs-lookup"><span data-stu-id="15815-208">Note</span></span></strong><br/><p><span data-ttu-id="15815-209">미니 설치가 완료 되려면 사용자 입력이 필요 하도록 Sysprep.inf 파일을 만든 경우, <strong> </strong> 처음 설정 하는 동안 유인 모드 또는 문제가 발생할 수 있습니다 .를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-210">무인 설치 </strong> .</span><span class="sxs-lookup"><span data-stu-id="15815-210">Unattended</strong>.</span></span> <span data-ttu-id="15815-211">처음 설정 하는 동안에는 가상 컴퓨터가 최종 사용자에 게 표시 되지 않지만 최종 사용자에 게 처음 설치를 시작 하기 전에 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-212">자동 </strong> .</span><span class="sxs-lookup"><span data-stu-id="15815-212">Silent</strong>.</span></span> <span data-ttu-id="15815-213">가상 머신은 처음 설정 하는 동안에는 최종 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="15815-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-216">기본값 = 15</span><span class="sxs-lookup"><span data-stu-id="15815-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-217">설치를 다시 시도할 때 처음 설정 하는 대화형 모드에서 설치를 완료 해야 하는 시간 초과 값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="15815-218">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-221">기본값 = 45</span><span class="sxs-lookup"><span data-stu-id="15815-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-222">처음 설정 대화형 모드에서 설치를 완료 해야 하는 시간 초과 값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="15815-223">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="15815-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-225">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-226">처음 설정 연기를 할 수 있는 날짜 및 시간 (UTC DateTime 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="15815-227">&quot;Yyyy-mm-dd hh: MM 형식으로 &quot; 24 시간 시계 표준으로 지정 된 시간을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="15815-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-230">메시지가 리소스 파일에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-231">처음 설치를 다시 시도 해야 할 때 최종 사용자에 게 표시 되는 사용자 지정 가능한 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-234">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-235">게스트에서 Sysprep.inf 파일의 [UserData] 섹션 아래에 있는 ComputerName 항목을 지정 된 ComputerNameMask에 따라 업데이트 해야 하는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="15815-236">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-237">0 = false: Sysprep .inf 파일의 ComputerName 항목이 ComputerNameMask에 따라 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-238">1 = true: Sysprep .inf 파일의 ComputerName 항목이 ComputerNameMask에 따라 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-241">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-242">게스트에서 Sysprep.inf 파일의 [Id] 섹션 아래에 있는 JoinDomain 설정을 호스트의 설정에 맞게 업데이트 해야 하는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="15815-243">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-244">0 = false: Sysprep.inf 파일의 JoinDomain 설정이 호스트의 설정에 맞게 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-245">1 = true: Sysprep .inf 파일의 JoinDomain 설정이 호스트의 설정과 일치 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-248">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-249">게스트에서 Sysprep .inf 파일의 [Id] 구역 아래에 있는 MachineObjectOU 설정이 호스트와 일치 하도록 업데이트 되는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="15815-250">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-251">0 = false: Sysprep .inf 파일의 MachineObjectOU 설정이 호스트의 설정에 맞게 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-252">1 = true: Sysprep .inf 파일의 MachineObjectOU 설정이 호스트의 설정과 일치 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-253">Set국가 Alsettings사용</span><span class="sxs-lookup"><span data-stu-id="15815-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-255">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-256">게스트에서 Sysprep .inf 파일의 [지역 Alsettings] 섹션 아래에 있는 설정이 호스트에 맞게 업데이트 되는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="15815-257">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15815-258">참고</span><span class="sxs-lookup"><span data-stu-id="15815-258">Note</span></span></strong><br/><p><span data-ttu-id="15815-259">기본적으로 게스트의 표준 시간대 설정은 호스트의 TimeZone 설정과 항상 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-260">0 = false: 게스트에 있는 Sysprep.inf 파일의 [지역 Alsettings] 섹션 아래에 있는 설정이 호스트에 맞게 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-261">1 = true: 게스트에 있는 Sysprep.inf 파일의 [지역 Alsettings] 섹션 아래에 있는 설정이 호스트와 일치 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-264">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-265">게스트에서 Sysprep .inf 파일의 [UserData] 구역에 있는 FullName 및 OrgName 설정이 호스트의 설정과 일치 하도록 업데이트 되는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="15815-266">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-267">0 = false: Sysprep .inf 파일의 FullName 및 OrgName 설정이 호스트의 설정에 맞게 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-268">1 = true: Sysprep .inf 파일의 FullName 및 OrgName 설정이 호스트의 설정과 일치 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="15815-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-271">메시지가 리소스 파일에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-272">처음으로 설정을 시작할 준비가 되 면 최종 사용자에 게 표시 되는 사용자 지정 가능한 메시지</span><span class="sxs-lookup"><span data-stu-id="15815-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-275">기본값 = 30</span><span class="sxs-lookup"><span data-stu-id="15815-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-276">설치 프로그램이 취소 작업에 대 한 가상 컴퓨터의 응답을 처음 기다리는 시간 제한 값 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="15815-277">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-280">기본값 = 60</span><span class="sxs-lookup"><span data-stu-id="15815-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-281">처음 설치 시 가상 컴퓨터가 종료 될 때까지 대기 하는 시간 제한 값 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="15815-282">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-285">기본값 = 600</span><span class="sxs-lookup"><span data-stu-id="15815-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-286">MED-V 게스트 에이전트 소프트웨어의 업그레이드 시도가 시간 초과 되기 전의 시간 (초)입니다. 범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="15815-287">UserExperience 키</span><span class="sxs-lookup"><span data-stu-id="15815-287">UserExperience Key</span></span>


<span data-ttu-id="15815-288">다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key 및 HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15815-289">이름</span><span class="sxs-lookup"><span data-stu-id="15815-289">Name</span></span></th>
<th align="left"><span data-ttu-id="15815-290">유형</span><span class="sxs-lookup"><span data-stu-id="15815-290">Type</span></span></th>
<th align="left"><span data-ttu-id="15815-291">Data/Default</span><span class="sxs-lookup"><span data-stu-id="15815-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="15815-292">설명</span><span class="sxs-lookup"><span data-stu-id="15815-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-295">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-296">게스트의 응용 프로그램 게시를 호스트로 사용할 수 있는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="15815-297">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-298">0 = false: 게스트에서 호스트로의 응용 프로그램 게시를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-299">1 = true: 게스트에서 호스트로 응용 프로그램을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-302">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-303">게스트와 호스트 간에 오디오 i/o 장치 공유를 사용 하도록 설정 했는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="15815-304">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-305">0 = false: 게스트와 호스트 간의 오디오 i/o 장치 공유를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-306">1 = true: 게스트와 호스트 간에 오디오 i/o 장치를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-309">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-310">게스트와 호스트 간에 클립보드 공유를 사용 하도록 설정 했는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="15815-311">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-312">0 = false: 게스트와 호스트 간의 클립보드 공유를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-313">1 = true: 게스트와 호스트 간에 클립보드를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-316">기본값 = 300</span><span class="sxs-lookup"><span data-stu-id="15815-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-317">설정 시작 대화 상자가 처음 시간 초과 되기 전의 시간 (초)입니다. 범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-318">대기 시간 제한</span><span class="sxs-lookup"><span data-stu-id="15815-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-320">기본값 = 30</span><span class="sxs-lookup"><span data-stu-id="15815-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-321">긴 로그온 시도 중에 전체 화면 가상 컴퓨터 창이 최종 사용자에 게 숨겨지도록 하는 시간 초과 값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-324">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-325">최종 사용자가 바탕 화면에 로그온 할 때 또는 첫 번째 게스트 응용 프로그램이 시작 될 때 게스트를 시작할지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="15815-326">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-327">0 = false: 첫 번째 게스트 응용 프로그램이 시작 될 때 게스트가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-328">1 = true: 게스트는 최종 사용자가 바탕 화면에 로그온 할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-331">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-332">게스트와 호스트 간에 프린터 공유를 사용할 수 있는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="15815-333">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-334">0 = false: 게스트와 호스트 간 프린터 공유를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-335">1 = true: 게스트와 호스트 간의 프린터 공유를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-338">기본값 = 1440</span><span class="sxs-lookup"><span data-stu-id="15815-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-339">처음 설치 시 다시 시작을 기다리는 시간 초과 값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="15815-340">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="15815-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-343">지정 된 URL 목록</span><span class="sxs-lookup"><span data-stu-id="15815-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-344">호스트에서 게스트로 리디렉션할 Url 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-345">Smart(스마트) Logon사용</span><span class="sxs-lookup"><span data-stu-id="15815-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-347">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-348">사용자를 MED-V에 인증 하는 데 스마트 카드를 사용할 수 있는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="15815-349">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-350">0 = false: 스마트 카드가 MED-V에 대 한 최종 사용자를 인증 하도록 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-351">1 = true: 스마트 카드가 일반 사용자를 MED-V로 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15815-352">중요</span><span class="sxs-lookup"><span data-stu-id="15815-352">Important</span></span></strong><br/><p><span data-ttu-id="15815-353">Smart을 사용 하도록 설정 하 고 CredentialCacheEnabled를 모두 사용 하는 경우 Smart지 인 Logonenabled가 CredentialCacheEnabled를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-356">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-357">게스트와 호스트 간에 스마트 카드를 공유할 수 있는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="15815-358">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-359">0 = false: 게스트와 호스트 간 스마트 카드 공유를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-360">1 = true: 게스트와 호스트 간에 스마트 카드를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-363">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-364">게스트와 호스트 간에 USB 장치 공유를 사용 하도록 설정 했는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="15815-365">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-366">0 = false: 게스트와 호스트 간의 USB 장치 공유를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-367">1 = true: 게스트와 호스트 간의 USB 장치 공유를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="15815-368">VM 키</span><span class="sxs-lookup"><span data-stu-id="15815-368">VM Key</span></span>


<span data-ttu-id="15815-369">다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM key 및 HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15815-370">이름</span><span class="sxs-lookup"><span data-stu-id="15815-370">Name</span></span></th>
<th align="left"><span data-ttu-id="15815-371">유형</span><span class="sxs-lookup"><span data-stu-id="15815-371">Type</span></span></th>
<th align="left"><span data-ttu-id="15815-372">Data/Default</span><span class="sxs-lookup"><span data-stu-id="15815-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="15815-373">설명</span><span class="sxs-lookup"><span data-stu-id="15815-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-374">CloseAction</span><span class="sxs-lookup"><span data-stu-id="15815-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-375">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-376">기본값 = 최대 절전 모드</span><span class="sxs-lookup"><span data-stu-id="15815-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-377">실행 중인 마지막 응용 프로그램을 닫은 후에 가상 컴퓨터에서 수행 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="15815-378">LogonStartEnabled 값을 사용 하도록 설정한 경우이 설정은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="15815-379">사용할 수 있는 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-380">최대 절전 모드 </strong> .</span><span class="sxs-lookup"><span data-stu-id="15815-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="15815-381">이 옵션은 메모리 및 CPU와 같이 가상 컴퓨터에서 사용 중인 모든 물리적 리소스를 해제 하 고 실행 중인 모든 응용 프로그램 및 작업의 상태를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-382">종료 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="15815-383">이 옵션은 게스트 운영 체제를 안전 하 게 종료 한 다음 가상 컴퓨터에서 사용 중인 메모리 및 CPU 등의 실제 리소스를 모두 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-384">해제 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="15815-385">이 옵션을 선택 하면 전원 단추를 끄거나 물리적 컴퓨터에서 전원 코드를 잡아당겨 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="15815-386">다른 두 옵션 중 하나를 사용할 수 없는 경우에만이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="15815-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="15815-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-390">게스트에 대 한 메모리 (MB) 값의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="15815-391">이 값은 게스트에서 사용할 수 있는 RAM의 크기를 결정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="15815-392">HostMemToGuestMem와 결합 하 여 게스트 가상 컴퓨터에 할당할 RAM의 양을 결정 하기 위해 조회 테이블이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="15815-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="15815-393">가능한 값은 128 ~ 3712입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="15815-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-396">기본값 = 240</span><span class="sxs-lookup"><span data-stu-id="15815-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-397">GuestUpdateTime 값에 지정 된 시간에 시작 하 여 MED-V가 자동 업데이트를 위해 게스트 활성 상태를 유지 해야 하는 분 수입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="15815-398">범위는 0 ~ 1440입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-398">Range = 0 to 1440.</span></span> <span data-ttu-id="15815-399">이 값을 0으로 설정 하면 게스트 패치 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="15815-400">자동 업데이트의 게스트 패치에 대 한 자세한 내용은 <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Med-v 작업 영역에 대 한 자동 업데이트 관리를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="15815-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="15815-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-402">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-403">기본값 = 00:00</span><span class="sxs-lookup"><span data-stu-id="15815-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-404">MED-V가 자동 업데이트를 위해 24 시간 시계 표준으로 게스트를 종료 해야 하는 날짜의 시간 및 분입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="15815-405">HH: MM 형식으로 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="15815-406">자동 업데이트의 게스트 패치에 대 한 자세한 내용은 <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Med-v 작업 영역에 대 한 자동 업데이트 관리를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="15815-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="15815-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="15815-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="15815-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-410">호스트에서 사용할 수 있는 RAM에 따라 게스트에 대 한 메모리 (MB) 값의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="15815-411">GuestMemFromHostMem와 결합 하 여 게스트 가상 컴퓨터에 할당할 RAM의 양을 결정 하기 위해 조회 테이블이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="15815-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="15815-412">가능한 값은 1024 ~ 16384입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-415">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-416">게스트에 대해 할당 된 메모리가 호스트에 있는 메모리에서 계산 되는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="15815-417">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-418">0 = false: 게스트에 대해 할당 된 메모리가 호스트에 있는 메모리에서 계산 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-419">1 = true: 게스트에 대해 할당 된 메모리는 호스트에 있는 메모리를 기준으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-420">메모리</span><span class="sxs-lookup"><span data-stu-id="15815-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-422">기본값 = 512</span><span class="sxs-lookup"><span data-stu-id="15815-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-423">게스트 가상 머신에 할당할 RAM (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="15815-424">HostMemToGuestMemEnabled 설정을 사용 하는 경우이 설정은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15815-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="15815-425">범위 = 128 ~ 2048.</span><span class="sxs-lookup"><span data-stu-id="15815-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="15815-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-428">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="15815-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-429">여러 사용자가 동일한 MED-V 작업 영역을 공유 하는지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="15815-430">0 = false, 1 = true.</span><span class="sxs-lookup"><span data-stu-id="15815-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-431">0 = false: 여러 사용자가 동일한 MED-V 작업 영역을 공유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-432">1 = true: 여러 사용자가 동일한 MED-V 작업 영역을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15815-433">NetworkingMode</span><span class="sxs-lookup"><span data-stu-id="15815-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-434">SZ</span><span class="sxs-lookup"><span data-stu-id="15815-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-435">Default = NAT</span><span class="sxs-lookup"><span data-stu-id="15815-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-436">게스트에 사용 되는 네트워크 연결의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="15815-437">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-438">브리지 </strong> .</span><span class="sxs-lookup"><span data-stu-id="15815-438">Bridged</strong>.</span></span> <span data-ttu-id="15815-439">MED-V에는 일반적으로 DHCP를 통해 얻은 고유한 네트워크 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="15815-440">NAT </strong> .</span><span class="sxs-lookup"><span data-stu-id="15815-440">NAT</strong>.</span></span> <span data-ttu-id="15815-441">MED-V는 NAT (Network Address Translation)를 사용 하 여 송신 트래픽에 대 한 호스트&#39;s IP를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="15815-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-444">기본값 = 600</span><span class="sxs-lookup"><span data-stu-id="15815-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-445">시작 및 종료와 같은 작업이 완료 될 때까지 MED-V가 대기 하는 일반적인 시간 제한 값 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="15815-446">범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="15815-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="15815-447">게스트 레지스트리 설정</span><span class="sxs-lookup"><span data-stu-id="15815-447">Guest Registry Settings</span></span>


<span data-ttu-id="15815-448">이 섹션에서는 구성 가능한 MED-V 게스트 레지스트리 키를 나열 하 고 그 사용에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="15815-449">chapv2</span><span class="sxs-lookup"><span data-stu-id="15815-449">v2</span></span>

<span data-ttu-id="15815-450">다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\ key와 연결 된 게스트 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15815-451">이름</span><span class="sxs-lookup"><span data-stu-id="15815-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="15815-452">유형</span><span class="sxs-lookup"><span data-stu-id="15815-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="15815-453">Data/Default</span><span class="sxs-lookup"><span data-stu-id="15815-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="15815-454">설명</span><span class="sxs-lookup"><span data-stu-id="15815-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15815-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="15815-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="15815-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="15815-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-457">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="15815-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="15815-458">MED-V가 키 BufferPolicyReads 및 GroupPolicyMinTransferRate를 처리 하는 방법을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="15815-459">기본적으로 MED-V는 다음과 같이 이러한 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="15815-460">BufferPolicyReads = 1 및 GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="15815-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="15815-461">필요한 경우 EnableGPWorkarounds 키를 만들고, MED-V Policyreads 및 GroupPolicyMinTransferRate의 기본 설정을 변경 하지 않으려는 경우 키를 0으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15815-462">참고</span><span class="sxs-lookup"><span data-stu-id="15815-462">Note</span></span></strong><br/><p><span data-ttu-id="15815-463">MED-V 작업 영역이 NAT 모드로 실행 되는 경우 EnableGPWorkarounds 레지스트리 키 BufferPolicyReads 및 GroupPolicyMinTransferRate에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15815-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="15815-464">MED-V 작업 영역이 브리지 모드로 실행 되는 경우 EnableGPWorkarounds는 레지스트리 키 BufferPolicyReads에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15815-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="15815-465">1 = true: MED-V는 키 BufferPolicyReads = 1과 GroupPolicyMinTransferRate = 0 (NAT 모드로 실행 하는 경우) 또는 단순한 BufferPolicyReads = 1 (브리지 모드로 실행 되는 경우)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15815-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="15815-466">0 = false 인 경우 MED-V는 키 BufferPolicyReads 및 GroupPolicyMinTransferRate에 대 한 변경 작업을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15815-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="15815-467">관련 항목</span><span class="sxs-lookup"><span data-stu-id="15815-467">Related topics</span></span>


[<span data-ttu-id="15815-468">MED-V 작업 영역 응용 프로그램 관리</span><span class="sxs-lookup"><span data-stu-id="15815-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="15815-469">MED-V URL 리디렉션 관리</span><span class="sxs-lookup"><span data-stu-id="15815-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="15815-470">MED-V 작업 영역 설정 관리</span><span class="sxs-lookup"><span data-stu-id="15815-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









