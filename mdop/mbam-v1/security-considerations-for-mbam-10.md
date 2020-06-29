---
title: MBAM 1.0에 대한 보안 고려 사항
description: MBAM 1.0에 대한 보안 고려 사항
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826193"
---
# <span data-ttu-id="94fee-103">MBAM 1.0에 대한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="94fee-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="94fee-104">이 항목에서는 계정 및 그룹, 로그 파일, Microsoft BitLocker 관리 및 모니터링 (MBAM)에 대 한 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="94fee-105">자세한 내용은이 문서의 링크를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="94fee-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="94fee-106">일반 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="94fee-106">General security considerations</span></span>


**<span data-ttu-id="94fee-107">보안 위험을 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-107">Understand the security risks.</span></span>** <span data-ttu-id="94fee-108">MBAM의 가장 심각한 위험은 BitLocker 암호화를 다시 구성 하 고 MBAM 클라이언트에서 BitLocker 암호화 키 데이터를 얻을 수 있는 권한이 없는 사용자가 해당 기능을 도용 했을 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="94fee-109">그러나 서비스 거부 공격으로 인해 짧은 시간 동안에는 MBAM 기능이 손실 되는 것은 일반적으로 치명적인 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="94fee-110">**컴퓨터를 물리적으로 보호**합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-110">**Physically secure your computers**.</span></span> <span data-ttu-id="94fee-111">보안이 완전 하지 않음 (물리적 보안 없음).</span><span class="sxs-lookup"><span data-stu-id="94fee-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="94fee-112">MBAM 서버에 대 한 실제 액세스 권한이 있는 사용자는 모두 클라이언트 기반을 공격할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="94fee-113">모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="94fee-114">MBAM 서버는 제어 된 액세스 권한이 있는 물리적으로 안전한 서버 방에 저장 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="94fee-115">운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.</span><span class="sxs-lookup"><span data-stu-id="94fee-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="94fee-116">**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="94fee-117">보안 알림 서비스 ()에 가입 하 여 운영 체제, Microsoft SQL Server 및 MBAM에 대 한 새 업데이트에 대 한 정보를 지속적으로 유지 <https://go.microsoft.com/fwlink/p/?LinkId=28819> 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="94fee-118">**강력한 암호 또는 암호 문구를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="94fee-119">항상 모든 MBAM 및 MBAM 관리자 계정에 대해 15 개 이상의 문자로 강력한 암호를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="94fee-120">빈 암호를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="94fee-120">Never use blank passwords.</span></span> <span data-ttu-id="94fee-121">암호 개념에 대 한 자세한 내용은 TechNet ()의 "계정 암호 및 정책" 백서를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=30009> .</span><span class="sxs-lookup"><span data-stu-id="94fee-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="94fee-122">MBAM의 계정 및 그룹</span><span class="sxs-lookup"><span data-stu-id="94fee-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="94fee-123">사용자 계정 관리에 대 한 모범 사례는 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="94fee-124">그런 다음 MBAM 서버의 필요한 MBAM 로컬 그룹에 도메인 글로벌 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="94fee-125">ActiveDirectoryDomainServices 그룹</span><span class="sxs-lookup"><span data-stu-id="94fee-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="94fee-126">MBAM 설정 중 그룹이 자동으로 만들어지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="94fee-127">그러나 MBAM 작업을 관리 하려면 다음 ActiveDirectoryDomainServices 전역 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="94fee-128">그룹 이름</span><span class="sxs-lookup"><span data-stu-id="94fee-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="94fee-129">세부 정보</span><span class="sxs-lookup"><span data-stu-id="94fee-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-130">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-131">이 그룹을 만들어 MBAM 설정 중에 만든 MBAM 고급 헬프 데스크 사용자 로컬 그룹의 구성원을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-132">MBAM 준수 감사 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="94fee-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-133">MBAM 설정 중에 만든 MBAM 준수 감사 DB 액세스 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-134">MBAM 하드웨어 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-135">MBAM 설정 중에 만든 MBAM 하드웨어 사용자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-136">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-137">MBAM 설정 중에 만든 MBAM 헬프데스크 사용자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-138">MBAM 복구 및 하드웨어 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="94fee-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-139">MBAM 설정 중에 만든 MBAM 복구 및 하드웨어 DB 액세스 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-140">MBAM 보고서 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-141">MBAM 설정 중에 만든 MBAM 보고서 사용자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-142">MBAM 시스템 관리자</span><span class="sxs-lookup"><span data-stu-id="94fee-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-143">MBAM 설정 중에 만든 MBAM 시스템 관리자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-144">BitLocker 암호화 예외</span><span class="sxs-lookup"><span data-stu-id="94fee-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-145">이 그룹을 만들어 로그온 하는 컴퓨터에서 시작 하는 BitLocker 암호화에서 제외 해야 하는 사용자 계정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="94fee-146">MBAM 서버 로컬 그룹</span><span class="sxs-lookup"><span data-stu-id="94fee-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="94fee-147">MBAM 설치는 MBAM 작업을 지 원하는 로컬 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="94fee-148">ActiveDirectoryDomainServices 글로벌 그룹을 해당 MBAM 로컬 그룹에 추가 하 여 MBAM 보안 및 데이터 액세스 권한을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="94fee-149">그룹 이름</span><span class="sxs-lookup"><span data-stu-id="94fee-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="94fee-150">세부 정보</span><span class="sxs-lookup"><span data-stu-id="94fee-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-151">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-152">이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 헬프데스크 기능에 대 한 액세스를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-153">MBAM 준수 감사 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="94fee-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-154">이 그룹에는 MBAM 준수 감사 데이터베이스에 액세스할 수 있는 컴퓨터가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-155">MBAM 하드웨어 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-156">이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 몇 가지 하드웨어 기능 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-157">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-158">이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 일부 헬프 데스크 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-159">MBAM 복구 및 하드웨어 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="94fee-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-160">이 그룹에는 MBAM 복구 및 하드웨어 데이터베이스에 액세스할 수 있는 컴퓨터가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94fee-161">MBAM 보고서 사용자</span><span class="sxs-lookup"><span data-stu-id="94fee-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-162">이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 규정 준수 및 감사 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94fee-163">MBAM 시스템 관리자</span><span class="sxs-lookup"><span data-stu-id="94fee-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="94fee-164">이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 모든 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="94fee-165">SSRS 보고서 액세스 계정</span><span class="sxs-lookup"><span data-stu-id="94fee-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="94fee-166">SSRS (SQL Server Reporting Services) 보고서 서비스 계정은 보안 컨텍스트를 제공 하 여 SSRS를 통해 사용할 수 있는 MBAM 보고서를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="94fee-167">이 계정은 MBAM 설정 중에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="94fee-168">MBAM 로그 파일</span><span class="sxs-lookup"><span data-stu-id="94fee-168">MBAM Log Files</span></span>


<span data-ttu-id="94fee-169">MBAM 설정 중에 다음 MBAM 설정 로그 파일은 다음을 설치 하는 사용자 의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="94fee-170">MBAM 서버 설정 로그 파일</span><span class="sxs-lookup"><span data-stu-id="94fee-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="94fee-171">MSI <em> &lt; 5 임의 문자 &gt; </em> 로그</span><span class="sxs-lookup"><span data-stu-id="94fee-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="94fee-172">MBAM 설정 및 MBAM 서버 기능 설치 중 취한 동작을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="94fee-173">InstallComplianceDatabase</span><span class="sxs-lookup"><span data-stu-id="94fee-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="94fee-174">MBAM 준수 상태 데이터베이스 설정을 만들기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="94fee-175">InstallKeyComplianceDatabase</span><span class="sxs-lookup"><span data-stu-id="94fee-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="94fee-176">MBAM 복구 및 하드웨어 데이터베이스를 만들기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="94fee-177">AddHelpDeskDbAuditUsers</span><span class="sxs-lookup"><span data-stu-id="94fee-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="94fee-178">MBAM 준수 상태 데이터베이스에서 SQL Server 로그인을 만들기 위해 수행한 작업을 기록 하 고 보고서에 대 한 데이터베이스에 헬프데스크 웹 서비스를 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="94fee-179">AddHelpDeskDbUsers</span><span class="sxs-lookup"><span data-stu-id="94fee-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="94fee-180">키 복구용으로 웹 서비스에 권한을 부여 하기 위해 수행한 작업을 로그 하 고 MBAM 복구 및 하드웨어 데이터베이스에 대 한 로그인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="94fee-181">AddKeyComplianceDbUsers</span><span class="sxs-lookup"><span data-stu-id="94fee-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="94fee-182">웹 서비스를 준수 보고를 위해 MBAM 준수 상태 데이터베이스에 대 한 권한을 부여 하기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="94fee-183">AddRecoveryAndHardwareDbUsers</span><span class="sxs-lookup"><span data-stu-id="94fee-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="94fee-184">웹 서비스에 대 한 MBAM 및 키 복구에 대 한 하드웨어 데이터베이스 권한을 부여 하기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="94fee-185">**참고**  추가 MBAM 설치 로그 파일을 얻으려면 **msiexec** 패키지 및 **/l** 위치 옵션을 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 해야 합니다 &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="94fee-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="94fee-186">로그 파일은 지정 된 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="94fee-187">MBAM 클라이언트 설치 로그 파일</span><span class="sxs-lookup"><span data-stu-id="94fee-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="94fee-188">MSI <em> &lt; 5 임의 문자 &gt; </em> 로그</span><span class="sxs-lookup"><span data-stu-id="94fee-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="94fee-189">MBAM 클라이언트 설치 중 수행 되는 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="94fee-190">MBAM 데이터베이스 TDE 고려 사항</span><span class="sxs-lookup"><span data-stu-id="94fee-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="94fee-191">SQL Server 2008에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능은 MBAM 데이터베이스 기능을 호스팅하는 데이터베이스 인스턴스의 필수 설치 필수 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="94fee-192">TDE를 사용 하 여 실시간 전체 데이터베이스 수준의 암호화를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="94fee-193">TDE는 규정 준수 또는 기업 데이터 보안 표준을 충족 하기 위해 일괄 암호화를 위해 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="94fee-194">TDE는 파일 수준에서 작동 하며, EFS (암호화 파일 시스템) 및 BitLocker 드라이브 암호화 (둘 다 하드 드라이브의 데이터를 암호화 하는 두 가지 Windows 기능)와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="94fee-195">TDE는 셀 수준 암호화, EFS 또는 BitLocker를 대체 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="94fee-196">데이터베이스에서 TDE를 사용 하도록 설정 하면 모든 백업이 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="94fee-197">따라서 데이터베이스 암호화 키 (DEK)를 보호 하는 데 사용 된 인증서가 데이터베이스 백업과 함께 백업 되 고 유지 되도록 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="94fee-198">인증서가 없으면 데이터를 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="94fee-199">데이터베이스와 함께 인증서를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="94fee-200">각 인증서 백업에는 두 개의 파일이 있어야 합니다. 이러한 파일은 모두 보관 되어야 합니다. 보안을 위해 데이터베이스 백업 파일과 별도로 보관 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="94fee-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="94fee-201">MBAM 데이터베이스 인스턴스의 TDE를 사용 하도록 설정 하는 방법에 대 한 예제는 [mbam 1.0 계산](evaluating-mbam-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94fee-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="94fee-202">SQLServer 2008의 TDE에 대 한 자세한 내용은 [SQL Server 2008 Enterprise Edition에서 데이터베이스 암호화](https://go.microsoft.com/fwlink/?LinkId=269703)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94fee-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="94fee-203">관련 항목</span><span class="sxs-lookup"><span data-stu-id="94fee-203">Related topics</span></span>


[<span data-ttu-id="94fee-204">MBAM 1.0에 대한 보안 및 개인 정보</span><span class="sxs-lookup"><span data-stu-id="94fee-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 





