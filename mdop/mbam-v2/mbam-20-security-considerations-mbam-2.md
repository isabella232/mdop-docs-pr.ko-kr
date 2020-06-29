---
title: MBAM 2.0 보안 고려 사항
description: MBAM 2.0 보안 고려 사항
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823913"
---
# <span data-ttu-id="0206e-103">MBAM 2.0 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="0206e-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="0206e-104">이 항목에서는 계정 및 그룹, 로그 파일, Microsoft BitLocker 관리 및 모니터링 (MBAM)에 대 한 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="0206e-105">자세한 내용은이 문서에 나와 있는 링크를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="0206e-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="0206e-106">일반 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="0206e-106">General Security Considerations</span></span>


**<span data-ttu-id="0206e-107">보안 위험을 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-107">Understand the security risks.</span></span>** <span data-ttu-id="0206e-108">Microsoft BitLocker 관리 및 모니터링의 가장 심각한 위험은 BitLocker 암호화를 다시 구성 하 고 MBAM 클라이언트에서 BitLocker 암호화 키 데이터를 얻을 수 있는 권한이 없는 사용자가 해당 기능을 도용 했을 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="0206e-109">그러나 서비스 거부 공격으로 인해 짧은 시간 동안에는 MBAM 기능이 손실 되는 것은 일반적으로 전자 메일, 네트워크 통신, 라이트, 전력 등의 경우와 달리 심각한 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="0206e-110">**컴퓨터를 물리적으로 보호**합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-110">**Physically secure your computers**.</span></span> <span data-ttu-id="0206e-111">물리적 보안 없이 보안이 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-111">There is no security without physical security.</span></span> <span data-ttu-id="0206e-112">MBAM 서버에 물리적으로 액세스 하는 공격자는이를 사용 하 여 전체 클라이언트 기반을 공격할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="0206e-113">모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="0206e-114">MBAM 서버는 액세스 권한이 있는 안전한 서버 방에 저장 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="0206e-115">운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.</span><span class="sxs-lookup"><span data-stu-id="0206e-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="0206e-116">**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="0206e-117">보안 알림 서비스 ()에 가입 하 여 운영 체제, Microsoft SQL Server 및 MBAM에 대 한 새 업데이트에 대 한 정보를 지속적으로 유지 <https://go.microsoft.com/fwlink/?LinkId=28819> 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="0206e-118">**강력한 암호 또는 암호 문구를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="0206e-119">항상 모든 MBAM 및 MBAM 관리자 계정에 대해 15 개 이상의 문자로 강력한 암호를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="0206e-120">빈 암호를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0206e-120">Never use blank passwords.</span></span> <span data-ttu-id="0206e-121">암호 개념에 대 한 자세한 내용은 TechNet ()의 "계정 암호 및 정책" 백서를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=30009> .</span><span class="sxs-lookup"><span data-stu-id="0206e-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="0206e-122">MBAM의 계정 및 그룹</span><span class="sxs-lookup"><span data-stu-id="0206e-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="0206e-123">사용자 계정을 관리 하는 가장 좋은 방법은 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="0206e-124">그런 다음 MBAM 서버의 필요한 MBAM 로컬 그룹에 도메인 글로벌 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="0206e-125">ActiveDirectoryDomainServices 그룹</span><span class="sxs-lookup"><span data-stu-id="0206e-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="0206e-126">MBAM 설정 프로세스 중에 자동으로 생성 되는 Active Directory 그룹은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="0206e-127">그러나 MBAM 작업을 관리 하기 위해 다음과 같은 ActiveDirectoryDomainServices 전역 그룹을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0206e-128">그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0206e-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="0206e-129">세부 정보</span><span class="sxs-lookup"><span data-stu-id="0206e-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-130">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="0206e-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-131">이 그룹을 만들어 MBAM 설정 중에 만든 MBAM 고급 헬프 데스크 사용자 로컬 그룹의 구성원을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0206e-132">MBAM 준수 감사 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="0206e-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-133">MBAM 설정 중에 만든 MBAM 준수 감사 DB 액세스 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-134">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="0206e-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-135">이 그룹을 만들어 MBAM 설정 중에 만든 MBAM 헬프데스크 사용자 로컬 그룹의 구성원을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0206e-136">MBAM 복구 및 하드웨어 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="0206e-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-137">MBAM 설정 중에 만든 MBAM 복구 및 하드웨어 DB 액세스 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-138">MBAM 보고서 사용자</span><span class="sxs-lookup"><span data-stu-id="0206e-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-139">이 그룹을 만들어 MBAM 설정 중에 만든 MBAM 보고서 사용자 로컬 그룹의 구성원을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0206e-140">MBAM 시스템 관리자</span><span class="sxs-lookup"><span data-stu-id="0206e-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-141">MBAM 설정 중에 만든 MBAM 시스템 관리자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-142">BitLocker 암호화 예외</span><span class="sxs-lookup"><span data-stu-id="0206e-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-143">이 그룹을 만들어 로그온 하는 컴퓨터에서 시작 하는 BitLocker 암호화에서 제외 해야 하는 사용자 계정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="0206e-144">MBAM 서버 로컬 그룹</span><span class="sxs-lookup"><span data-stu-id="0206e-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="0206e-145">MBAM 설치는 MBAM 작업을 지 원하는 로컬 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="0206e-146">ActiveDirectoryDomainServices 글로벌 그룹을 해당 MBAM 로컬 그룹에 추가 하 여 MBAM 보안 및 데이터 액세스 권한을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0206e-147">그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0206e-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="0206e-148">세부 정보</span><span class="sxs-lookup"><span data-stu-id="0206e-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-149">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="0206e-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-150">이 그룹의 구성원은 MBAM의 지원 센터 기능에 대 한 액세스 권한이 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0206e-151">MBAM 준수 감사 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="0206e-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-152">MBAM 준수 및 감사 데이터베이스에 액세스할 수 있는 컴퓨터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-153">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="0206e-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-154">이 그룹의 구성원은 MBAM의 몇 가지 지원 센터 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0206e-155">MBAM 복구 및 하드웨어 DB 액세스</span><span class="sxs-lookup"><span data-stu-id="0206e-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-156">MBAM 복구 데이터베이스에 액세스할 수 있는 컴퓨터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0206e-157">MBAM 보고서 사용자</span><span class="sxs-lookup"><span data-stu-id="0206e-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-158">이 그룹의 구성원은 MBAM의 규정 준수 및 감사 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0206e-159">MBAM 시스템 관리자</span><span class="sxs-lookup"><span data-stu-id="0206e-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="0206e-160">이 그룹의 구성원은 모든 MBAM 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0206e-161">SSRS 보고서 서비스 계정</span><span class="sxs-lookup"><span data-stu-id="0206e-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="0206e-162">SSRS 보고서 서비스 계정은 보안 컨텍스트를 제공 하 여 SSRS를 통해 사용할 수 있는 MBAM 보고서를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="0206e-163">이는 MBAM 설정 중에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="0206e-164">SSRS 보고서 서비스 계정을 구성 하는 경우 도메인 사용자 계정을 지정 하 고 암호가 만료 되지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="0206e-165">**참고**  MBAM을 배포한 후 서비스 계정의 이름을 변경 하는 경우 새 서비스 계정 자격 증명을 사용 하도록 보고 데이터 원본을 다시 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="0206e-166">그렇지 않은 경우에는 지원 센터 포털에 액세스할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="0206e-167">MBAM 로그 파일</span><span class="sxs-lookup"><span data-stu-id="0206e-167">MBAM Log Files</span></span>


<span data-ttu-id="0206e-168">다음 MBAM 설정 로그 파일은 MBAM 설정 중 설치 사용자 의% temp% 폴더에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="0206e-169">MBAM 서버 설정 로그 파일</span><span class="sxs-lookup"><span data-stu-id="0206e-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="0206e-170">MSI <em> &lt; 5 임의 문자 &gt; </em> 로그</span><span class="sxs-lookup"><span data-stu-id="0206e-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="0206e-171">MBAM 설정 및 MBAM 서버 기능 설치 중 취한 동작을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="0206e-172">InstallComplianceDatabase</span><span class="sxs-lookup"><span data-stu-id="0206e-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="0206e-173">MBAM 준수 및 감사 데이터베이스 설정을 만들기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="0206e-174">InstallKeyComplianceDatabase</span><span class="sxs-lookup"><span data-stu-id="0206e-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="0206e-175">MBAM 복구 데이터베이스를 만들기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="0206e-176">AddHelpDeskDbAuditUsers</span><span class="sxs-lookup"><span data-stu-id="0206e-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="0206e-177">MBAM 준수 및 감사 데이터베이스에서 SQL Server 로그인을 만들고 보고서 데이터베이스에 대 한 헬프 데스크 웹 서비스에 권한을 부여 하기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="0206e-178">AddHelpDeskDbUsers</span><span class="sxs-lookup"><span data-stu-id="0206e-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="0206e-179">키 복구를 위해 데이터베이스에 웹 서비스를 부여 하 고 MBAM 복구 데이터베이스에 대 한 로그인을 만들기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="0206e-180">AddKeyComplianceDbUsers</span><span class="sxs-lookup"><span data-stu-id="0206e-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="0206e-181">웹 서비스에 권한을 부여 하기 위해 수행한 작업을 정책 준수 보고를 위해 MBAM 준수 및 감사 데이터베이스로 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="0206e-182">AddRecoveryAndHardwareDbUsers</span><span class="sxs-lookup"><span data-stu-id="0206e-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="0206e-183">키 복구를 위해 웹 서비스를 MBAM 데이터베이스에 부여 하기 위해 수행한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="0206e-184">**참고**  추가 MBAM 설치 로그 파일을 얻으려면 msiexec 패키지 및/L 위치 옵션을 사용 하 여 MBAM을 설치 해야 &lt; &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="0206e-185">로그 파일은 지정 된 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="0206e-186">MBAM 클라이언트 설치 로그 파일</span><span class="sxs-lookup"><span data-stu-id="0206e-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="0206e-187">MSI <em> &lt; 5 임의 문자 &gt; </em> 로그</span><span class="sxs-lookup"><span data-stu-id="0206e-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="0206e-188">MBAM 클라이언트 설치 중 수행 되는 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="0206e-189">MBAM 데이터베이스 TDE 고려 사항</span><span class="sxs-lookup"><span data-stu-id="0206e-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="0206e-190">SQL Server에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능은 MBAM 데이터베이스 기능을 호스트할 데이터베이스 인스턴스의 선택적 설치입니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="0206e-191">TDE를 사용 하 여 실시간 전체 데이터베이스 수준의 암호화를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="0206e-192">TDE는 규정 준수 또는 기업 데이터 보안 표준을 충족 하기 위해 일괄 암호화를 위한 최적의 선택입니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="0206e-193">TDE는 파일 수준에서 작동 하며, EFS (암호화 파일 시스템) 및 BitLocker 드라이브 암호화 (둘 다 하드 드라이브의 데이터를 암호화 하는 두 가지 Windows 기능)와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="0206e-194">TDE는 셀 수준 암호화, EFS 또는 BitLocker를 대체 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="0206e-195">데이터베이스에서 TDE를 사용 하도록 설정 하면 모든 백업이 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="0206e-196">따라서 데이터베이스 암호화 키를 보호 하는 데 사용 된 인증서가 데이터베이스 백업과 함께 백업 되 고 유지 되도록 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="0206e-197">이 인증서 (또는 인증서)가 손실 되 면 데이터를 읽을 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="0206e-198">데이터베이스와 함께 인증서를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="0206e-199">각 인증서 백업에는 두 개의 파일이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="0206e-200">이러한 파일은 모두 보안을 위해 데이터베이스 백업 파일과 별도로 보관 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="0206e-201">또는 TDE에 사용 되는 키 저장소 및 유지 관리에 대 한 EKM (확장 가능한 키 관리) 기능을 사용 하 여 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0206e-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="0206e-202">MBAM 데이터베이스 인스턴스의 TDE를 사용 하도록 설정 하는 방법에 대 한 예제는 [mbam 2.0 계산](evaluating-mbam-20-mbam-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0206e-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="0206e-203">SQLServer 2008의 TDE에 대 한 자세한 내용은 [SQL Server 암호화]( https://go.microsoft.com/fwlink/?LinkId=299883)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0206e-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="0206e-204">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0206e-204">Related topics</span></span>


[<span data-ttu-id="0206e-205">MBAM 2.0에 대한 보안 및 개인 정보</span><span class="sxs-lookup"><span data-stu-id="0206e-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





