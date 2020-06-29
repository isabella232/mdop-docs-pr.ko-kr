---
title: App-V 5.x Server 를 설치하기 전에 레지스트리 키 확인
description: App-V 5.x Server 를 설치하기 전에 레지스트리 키 확인
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814708"
---
# <span data-ttu-id="c6523-103">App-V 5.x Server 를 설치하기 전에 레지스트리 키 확인</span><span class="sxs-lookup"><span data-stu-id="c6523-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="c6523-104">App-v 5.0 SP1 핫픽스 패키지 3 이상에서 App-v 서버를 업그레이드 하는 경우이 섹션의 단계를 완료 하 고 앱-V 5. x 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6523-105">이 단계가 필요한 경우</span><span class="sxs-lookup"><span data-stu-id="c6523-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6523-106">.Msp 파일을 사용 하 여 설치한 이후 핫픽스 패키지를 사용 하 여 App-v 5.0 SP1에서 업그레이드 하는 경우</span><span class="sxs-lookup"><span data-stu-id="c6523-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6523-107">이 단계를 수행 해야 하는 구성 요소</span><span class="sxs-lookup"><span data-stu-id="c6523-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6523-108">업그레이드 하는 App-v 서버 구성 요소만</span><span class="sxs-lookup"><span data-stu-id="c6523-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6523-109">이 단계를 수행 해야 하는 경우</span><span class="sxs-lookup"><span data-stu-id="c6523-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6523-110">App-v Server를 App-V 5. x로 업그레이드 하기 전에</span><span class="sxs-lookup"><span data-stu-id="c6523-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6523-111">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="c6523-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6523-112">다음 표의 정보를 사용 하 여 <code>HKLM\Software\Microsoft\AppV\Server</code> 원래 서버 설치에서 제공한 값으로 각 레지스트리 키 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="c6523-113">이 단계를 완료 하면 App-v 5.0 SP1 핫픽스 패키지를 설치할 때 제거 되었을 수 있는 레지스트리 값이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c6523-114">ManagementDatabase 키</span><span class="sxs-lookup"><span data-stu-id="c6523-114">ManagementDatabase key</span></span>**

<span data-ttu-id="c6523-115">관리 데이터베이스를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6523-116">키 이름</span><span class="sxs-lookup"><span data-stu-id="c6523-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="c6523-117">설명</span><span class="sxs-lookup"><span data-stu-id="c6523-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c6523-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-119">공용 액세스 계정이 비로컬 관리 데이터베이스에 액세스 하는 데 필요한 지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="c6523-120">필요한 경우 값이 "1"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c6523-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-122">관리 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-124">관리 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="c6523-125"><code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c6523-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-127">관리 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="c6523-128"><code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c6523-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-130">관리 데이터베이스용 SQL Server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="c6523-131">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-133">관리 데이터베이스에 대 한 쓰기 (관리자) 액세스에 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c6523-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-135">관리 데이터베이스에 대 한 쓰기 (관리자) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-137">관리 서버 원격 컴퓨터 계정 (계정).</span><span class="sxs-lookup"><span data-stu-id="c6523-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-139">관리 서버 (%0)에 대 한 설치 관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="c6523-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c6523-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-141">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="c6523-142">1 </strong> – 관리 서비스가 로컬 컴퓨터에 있으며,이는 MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="c6523-143">0 </strong> - 관리 서비스는 로컬 컴퓨터와 다른 컴퓨터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c6523-144">ManagementService 키</span><span class="sxs-lookup"><span data-stu-id="c6523-144">ManagementService key</span></span>**

<span data-ttu-id="c6523-145">관리 서버를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ManagementService` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6523-146">키 이름</span><span class="sxs-lookup"><span data-stu-id="c6523-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="c6523-147">설명</span><span class="sxs-lookup"><span data-stu-id="c6523-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-149">AD DS (Active Directory 도메인 서비스) 그룹 또는 App.config (App-v) 관리 권한이 있는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c6523-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-151">관리 데이터베이스를 포함 하는 SQL server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="c6523-152">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c6523-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-154">관리 데이터베이스를 사용 하는 원격 SQL 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="c6523-155">값이 비어 있으면 로컬 컴퓨터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c6523-156">ReportingDatabase 키</span><span class="sxs-lookup"><span data-stu-id="c6523-156">ReportingDatabase key</span></span>**

<span data-ttu-id="c6523-157">보고 데이터베이스를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6523-158">키 이름</span><span class="sxs-lookup"><span data-stu-id="c6523-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="c6523-159">설명</span><span class="sxs-lookup"><span data-stu-id="c6523-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c6523-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-161">로컬이 아닌 보고 데이터베이스에 액세스 하는 데 공개 액세스 계정이 필요한 지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="c6523-162">필요한 경우 값이 "1"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c6523-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-164">보고 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-166">보고 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="c6523-167"><code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c6523-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-169">보고 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="c6523-170"><code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c6523-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-172">보고 데이터베이스용 SQL Server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="c6523-173">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="c6523-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-177">Reporting server 컴퓨터 계정 (계정)</span><span class="sxs-lookup"><span data-stu-id="c6523-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c6523-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-179">Reporting server (%0)에 대 한 설치 관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="c6523-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c6523-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-181">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="c6523-182">1 </strong> – Reporting service가 로컬 컴퓨터에 있으며,이는 REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="c6523-183">0 </strong> - Reporting services가 로컬 컴퓨터와 다른 컴퓨터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c6523-184">ReportingService 키</span><span class="sxs-lookup"><span data-stu-id="c6523-184">ReportingService key</span></span>**

<span data-ttu-id="c6523-185">보고 서버를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ReportingService` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6523-186">키 이름</span><span class="sxs-lookup"><span data-stu-id="c6523-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="c6523-187">설명</span><span class="sxs-lookup"><span data-stu-id="c6523-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6523-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c6523-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-189">보고 데이터베이스용 SQL Server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="c6523-190">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6523-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c6523-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6523-192">보고 데이터베이스를 사용 하는 원격 SQL 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="c6523-193">값이 비어 있으면 로컬 컴퓨터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6523-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

