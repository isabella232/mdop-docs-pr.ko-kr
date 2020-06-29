---
title: MBAM 2.5 그룹 및 계정 계획
description: MBAM 2.5 그룹 및 계정 계획
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825803"
---
# <span data-ttu-id="18e0d-103">MBAM 2.5 그룹 및 계정 계획</span><span class="sxs-lookup"><span data-stu-id="18e0d-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="18e0d-104">이 항목에서는 Microsoft AD DS (Active Directory 도메인 서비스)에서 보안 및 액세스 권한을 제공 하 고 (예, MBAM) 데이터베이스, 보고서, 웹 응용 프로그램을 위해 만들어야 하는 역할 및 계정을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="18e0d-105">각 역할 및 계정에 대해 MBAM 서버 구성 마법사의 해당 필드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="18e0d-106">이러한 계정에 해당 하는 Windows PowerShell cmdlet 및 매개 변수 목록은 [Windows powershell을 사용 하 여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18e0d-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="18e0d-107">참고</span><span class="sxs-lookup"><span data-stu-id="18e0d-107">Note</span></span>**  
<span data-ttu-id="18e0d-108">MBAM은 관리 서비스 계정 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="18e0d-109">데이터베이스 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-109">Database accounts</span></span>


<span data-ttu-id="18e0d-110">준수 및 감사 데이터베이스와 복구 데이터베이스에 대해 다음 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18e0d-111">계정 이름 및 용도</span><span class="sxs-lookup"><span data-stu-id="18e0d-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="18e0d-112">계정 유형</span><span class="sxs-lookup"><span data-stu-id="18e0d-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="18e0d-113">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드</span><span class="sxs-lookup"><span data-stu-id="18e0d-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="18e0d-114">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="18e0d-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18e0d-115">준수 및 감사 데이터베이스 및 복구 데이터베이스 보고서에 대 한 사용자 또는 그룹 읽기/쓰기</span><span class="sxs-lookup"><span data-stu-id="18e0d-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-116">사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-117">읽기/쓰기 액세스 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-118">준수 및 감사 데이터베이스와 복구 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹으로, 웹 응용 프로그램에서 이러한 데이터베이스의 데이터 및 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="18e0d-119">이 필드에 사용자 이름을 입력 하는 경우 <strong> </strong> <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값과 동일 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="18e0d-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="18e0d-120">이 필드에 그룹 이름을 입력 하는 경우 <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값 </strong> <strong> </strong> 이이 필드에 입력 하는 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18e0d-121">보고서에 대 한 규정 준수 및 감사 데이터베이스 읽기 전용 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-122">사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-123">읽기 전용 액세스 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-124">규정 준수 및 감사 데이터베이스에 대 한 읽기 전용 액세스 권한을 가지는 사용자 또는 그룹의 이름으로, 보고서에서이 데이터베이스의 규정 준수 및 감사 데이터에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="18e0d-125">이 필드에 사용자 이름을 입력 하는 경우 <strong> </strong> <strong> 보고서 구성 페이지의 규정 준수 및 감사 데이터베이스 도메인 계정 필드에 지정 하는 사용자와 동일 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="18e0d-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="18e0d-126">이 필드에 그룹 이름을 입력 하는 경우 <strong> 보고서 구성 페이지의 규정 준수 및 감사 데이터베이스 도메인 계정 필드에 지정한 값 </strong> <strong> </strong> 이이 필드에서 지정 하는 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="18e0d-127">보고 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-127">Reporting accounts</span></span>


<span data-ttu-id="18e0d-128">보고서 기능에 대해 다음 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18e0d-129">계정 이름/용도</span><span class="sxs-lookup"><span data-stu-id="18e0d-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="18e0d-130">계정 유형</span><span class="sxs-lookup"><span data-stu-id="18e0d-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="18e0d-131">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드</span><span class="sxs-lookup"><span data-stu-id="18e0d-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="18e0d-132">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="18e0d-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18e0d-133">읽기 전용 도메인 액세스 그룹 보고</span><span class="sxs-lookup"><span data-stu-id="18e0d-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-134">Group</span><span class="sxs-lookup"><span data-stu-id="18e0d-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-135">보고 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-136">관리 및 모니터링 웹 사이트의 보고서에 대 한 읽기 전용 액세스 권한이 있는 도메인 사용자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="18e0d-137">지정 하는 그룹은 웹 앱을 사용할 수 있는 경우 보고서 읽기 전용 액세스 그룹 매개 변수에 대해 지정한 그룹과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18e0d-138">준수 및 감사 데이터베이스 도메인 사용자 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-139">사용자</span><span class="sxs-lookup"><span data-stu-id="18e0d-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-140">준수 및 감사 데이터베이스 도메인 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-141">로컬 SQL Server Reporting Services 인스턴스에서 준수 및 감사 데이터베이스에 액세스 하는 데 사용 하는 도메인 사용자 계정 및 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="18e0d-142">이 계정에 <strong> </strong> 는 SQL Server Reporting Services 서버에 일괄 처리 권한으로 로그온이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="18e0d-143"><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 하는 값이 </strong> <strong> </strong> 사용자 이름 이면이 필드에 같은 값을 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="18e0d-144"><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 하는 값이 </strong> <strong> </strong> 그룹 이름이 면이 필드에 입력 하는 값이 해당 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="18e0d-145">이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="18e0d-146">사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="18e0d-147">관리 및 모니터링 웹 사이트 (지원 센터) 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="18e0d-148">관리 및 모니터링 웹 사이트에 대해 다음 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18e0d-149">계정 이름/용도</span><span class="sxs-lookup"><span data-stu-id="18e0d-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="18e0d-150">계정 유형</span><span class="sxs-lookup"><span data-stu-id="18e0d-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="18e0d-151">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드</span><span class="sxs-lookup"><span data-stu-id="18e0d-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="18e0d-152">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="18e0d-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18e0d-153">웹 서비스 응용 프로그램 풀 도메인 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-154">사용자</span><span class="sxs-lookup"><span data-stu-id="18e0d-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-155">웹 서비스 응용 프로그램 풀 도메인 계정</span><span class="sxs-lookup"><span data-stu-id="18e0d-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-156">웹 응용 프로그램의 응용 프로그램 풀에서 사용할 도메인 사용자 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="18e0d-157"><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 사용자 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 같은 값을 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="18e0d-158"><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 그룹 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 입력 하는 값은 해당 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="18e0d-159">자격 증명을 지정 하지 않으면 이전에 사용 하도록 설정 된 웹 응용 프로그램에 대해 지정 된 자격 증명이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="18e0d-160">모든 웹 응용 프로그램은 동일한 응용 프로그램 풀 자격 증명을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="18e0d-161">여러 웹 응용 프로그램에 대해 다른 자격 증명을 지정 하는 경우 가장 최근에 지정 된 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="18e0d-162">중요</span><span class="sxs-lookup"><span data-stu-id="18e0d-162">Important</span></span></strong><br/><p><span data-ttu-id="18e0d-163">보안 향상을 위해 자격 증명에 지정 된 계정에 제한 된 사용자 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18e0d-164">MBAM 고급 헬프 데스크 사용자 액세스 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-165">Group</span><span class="sxs-lookup"><span data-stu-id="18e0d-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-166">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="18e0d-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-167">구성원이 관리 및 모니터링 웹 사이트의 모든 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="18e0d-168">이 역할을 사용 하는 사용자는 최종 사용자의 도메인 및 사용자 이름 대신 복구 키만 입력 해야 하는 데,이를 사용 하 여 엔드 사용자의 드라이브 복구를 도울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="18e0d-169">사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 그룹 사용 권한 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18e0d-170">MBAM 헬프데스크 사용자 액세스 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-171">Group</span><span class="sxs-lookup"><span data-stu-id="18e0d-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-172">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="18e0d-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-173">구성원이 MBAM 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="18e0d-174">이 역할이 있는 개인은 두 옵션 중 하나를 사용할 때 최종 사용자의 도메인 및 계정 이름을 포함 하 여 모든 필드를 채워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="18e0d-175">사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 그룹 사용 권한 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18e0d-176">MBAM 보고서 사용자 액세스 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-177">Group</span><span class="sxs-lookup"><span data-stu-id="18e0d-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-178">MBAM 보고서 사용자</span><span class="sxs-lookup"><span data-stu-id="18e0d-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-179">구성원이 관리 및 모니터링 웹 사이트의 보고서 영역에 있는 보고서에 대 한 읽기 전용 액세스 권한을 갖는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18e0d-180">MBAM 데이터 마이그레이션 사용자 그룹</span><span class="sxs-lookup"><span data-stu-id="18e0d-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-181">Group</span><span class="sxs-lookup"><span data-stu-id="18e0d-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-182">MBAM 데이터 마이그레이션 사용자</span><span class="sxs-lookup"><span data-stu-id="18e0d-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="18e0d-183">구성원이 mbam 서버에서 실행 되는 MBAM 복구와 하드웨어 서비스를 사용 하 여 MBAM에 데이터를 쓸 수 있는 권한이 있는 도메인 사용자 그룹 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="18e0d-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="18e0d-184">이 계정은 일반적으로 Active Directory에서 MBAM 데이터베이스로 복구 및 TPM 데이터를 쓰는 데 비 Mbam \* cmdlet과 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="18e0d-185">자세한 내용은 <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> mbam 2.5 보안 고려 사항을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="18e0d-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="18e0d-186">관련 항목</span><span class="sxs-lookup"><span data-stu-id="18e0d-186">Related topics</span></span>


[<span data-ttu-id="18e0d-187">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="18e0d-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="18e0d-188">MBAM 2.5 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="18e0d-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="18e0d-189">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="18e0d-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="18e0d-190">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="18e0d-191">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18e0d-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





