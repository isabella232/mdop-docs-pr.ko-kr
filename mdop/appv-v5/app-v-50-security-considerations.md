---
title: App-V 5.0 보안 고려 사항
description: App-V 5.0 보안 고려 사항
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814809"
---
# <span data-ttu-id="82aad-103">App-V 5.0 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="82aad-103">App-V 5.0 Security Considerations</span></span>


<span data-ttu-id="82aad-104">이 항목에서는 계정 및 그룹, 로그 파일 및 앱-V 5.0에 대 한 기타 보안 관련 고려 사항에 대해 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for App-V 5.0.</span></span>

**<span data-ttu-id="82aad-105">중요</span><span class="sxs-lookup"><span data-stu-id="82aad-105">Important</span></span>**  
<span data-ttu-id="82aad-106">App-v 5.0는 보안 제품이 아니므로 보안 환경에 대 한 보증을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-106">App-V 5.0 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="82aad-107">PackageStoreAccessControl (PSAC) 기능은 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="82aad-108">유효 6 월, 2014, Microsoft Application Virtualization (App-v) 5.0 서비스 팩 2(SP2)에 도입 된 PackageStoreAccessControl (PSAC) 기능은 단일 사용자 및 다중 사용자 환경에서 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="82aad-109">일반 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="82aad-109">General security considerations</span></span>


**<span data-ttu-id="82aad-110">보안 위험을 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-110">Understand the security risks.</span></span>** <span data-ttu-id="82aad-111">App-v 5.0의 가장 심각한 위험은 앱 V 5.0 클라이언트에서 키 데이터를 다시 구성할 수 있는 권한이 없는 사용자가 해당 기능을 도용 했을 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-111">The most serious risk to App-V 5.0 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.0 clients.</span></span> <span data-ttu-id="82aad-112">서비스 거부 공격으로 인해 짧은 기간 동안 App-v 5.0 기능이 손실 되는 것은 일반적으로 치명적이 지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-112">The loss of App-V 5.0 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="82aad-113">**컴퓨터를 물리적으로 보호**합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-113">**Physically secure your computers**.</span></span> <span data-ttu-id="82aad-114">보안이 완전 하지 않음 (물리적 보안 없음).</span><span class="sxs-lookup"><span data-stu-id="82aad-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="82aad-115">App-v 5.0 서버에 대 한 실제 액세스 권한이 있는 사람은 누구나 전체 클라이언트 기반을 공격할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-115">Anyone with physical access to an App-V 5.0 server could potentially attack the entire client base.</span></span> <span data-ttu-id="82aad-116">모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="82aad-117">App-v 5.0 서버는 제어 된 액세스 권한이 있는 물리적으로 안전한 서버 방에 저장 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-117">App-V 5.0 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="82aad-118">운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.</span><span class="sxs-lookup"><span data-stu-id="82aad-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="82aad-119">**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="82aad-120">운영 체제, Microsoft SQL Server 및 App-v 5.0 최신 업데이트에 대 한 정보를 확인 하려면 보안 알림 서비스 ()를 구독 합니다 <https://go.microsoft.com/fwlink/p/?LinkId=28819> .</span><span class="sxs-lookup"><span data-stu-id="82aad-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.0, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="82aad-121">**강력한 암호 또는 암호 문구를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="82aad-122">모든 App-v 5.0 및 App-v 5.0 administrator 계정에는 항상 15 개 이상의 문자로 강력한 암호를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-122">Always use strong passwords with 15 or more characters for all App-V 5.0 and App-V 5.0 administrator accounts.</span></span> <span data-ttu-id="82aad-123">빈 암호를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="82aad-123">Never use blank passwords.</span></span> <span data-ttu-id="82aad-124">암호 개념에 대 한 자세한 내용은 TechNet ()의 "계정 암호 및 정책" 백서를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=30009> .</span><span class="sxs-lookup"><span data-stu-id="82aad-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="82aad-125">앱-V 5.0의 계정 및 그룹</span><span class="sxs-lookup"><span data-stu-id="82aad-125">Accounts and groups in App-V 5.0</span></span>


<span data-ttu-id="82aad-126">사용자 계정 관리에 대 한 모범 사례는 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="82aad-127">그런 다음 App-v 5.0 서버의 필수 App-v 5.0 로컬 그룹에 도메인 글로벌 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-127">Then, add the domain global accounts to the necessary App-V 5.0 local groups on the App-V 5.0 servers.</span></span>

**<span data-ttu-id="82aad-128">참고</span><span class="sxs-lookup"><span data-stu-id="82aad-128">Note</span></span>**  
<span data-ttu-id="82aad-129">게시 서버에 연결 해야 하는 app-v 클라이언트 컴퓨터 계정은 게시 서버의 **사용자** 로컬 그룹의 일부 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="82aad-130">기본적으로 도메인의 모든 컴퓨터는 **사용자** 로컬 그룹의 일부인 **승인 된 사용자** 그룹의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-0-server-security"></a> <span data-ttu-id="82aad-131">앱-V 5.0 서버 보안</span><span class="sxs-lookup"><span data-stu-id="82aad-131">App-V 5.0 server security</span></span>

<span data-ttu-id="82aad-132">App-v 5.0를 설정 하는 동안 그룹이 자동으로 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-132">No groups are created automatically during App-V 5.0 Setup.</span></span> <span data-ttu-id="82aad-133">App-v 5.0 서버 작업을 관리 하려면 다음 Active Directory 도메인 서비스 글로벌 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.0 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="82aad-134">그룹 이름</span><span class="sxs-lookup"><span data-stu-id="82aad-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="82aad-135">세부 정보</span><span class="sxs-lookup"><span data-stu-id="82aad-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82aad-136">App-v 관리 관리자 그룹</span><span class="sxs-lookup"><span data-stu-id="82aad-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="82aad-137">App-v 5.0 관리 서버를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-137">Used to manage the App-V 5.0 management server.</span></span> <span data-ttu-id="82aad-138">이 그룹은 App-v 5.0 관리 서버 설치 중에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-138">This group is created during the App-V 5.0 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="82aad-139">중요</span><span class="sxs-lookup"><span data-stu-id="82aad-139">Important</span></span></strong><br/><p><span data-ttu-id="82aad-140">설치를 완료 한 후 관리 콘솔을 사용 하 여 그룹을 만들 수 있는 방법은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82aad-141">관리 서비스 계정에 대 한 데이터베이스 읽기/쓰기</span><span class="sxs-lookup"><span data-stu-id="82aad-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="82aad-142">관리 데이터베이스에 대 한 읽기/쓰기 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="82aad-143">이 계정은 App-v 5.0 관리 데이터베이스 설치 중에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-143">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82aad-144">앱-V 관리 서비스 관리자 계정 설치</span><span class="sxs-lookup"><span data-stu-id="82aad-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="82aad-145">참고</span><span class="sxs-lookup"><span data-stu-id="82aad-145">Note</span></span></strong><br/><p><span data-ttu-id="82aad-146">이는 관리 데이터베이스가 서비스와 별도로 설치 되는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="82aad-147">관리 데이터베이스의 스키마 버전 테이블에 대 한 공용 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="82aad-148">이 계정은 App-v 5.0 관리 데이터베이스 설치 중에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-148">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82aad-149">앱-V Reporting Service 관리자 계정 설치</span><span class="sxs-lookup"><span data-stu-id="82aad-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="82aad-150">참고</span><span class="sxs-lookup"><span data-stu-id="82aad-150">Note</span></span></strong><br/><p><span data-ttu-id="82aad-151">이는 보고 데이터베이스가 서비스와 별도로 설치 되는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="82aad-152">보고 데이터베이스의 스키마 버전 테이블에 대 한 공용 액세스</span><span class="sxs-lookup"><span data-stu-id="82aad-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="82aad-153">이 계정은 App-v 5.0 reporting 데이터베이스 설치 중에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-153">This account should be created during the App-V 5.0 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="82aad-154">다음과 같은 추가 정보를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="82aad-155">패키지 공유에 대 한 액세스-관리 서버와 같은 컴퓨터에 공유가 있는 경우 **네트워크** 서비스에서 공유에 대 한 읽기 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="82aad-156">또한 각 App-v 클라이언트 컴퓨터에는 패키지 공유에 대 한 읽기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="82aad-157">참고</span><span class="sxs-lookup"><span data-stu-id="82aad-157">Note</span></span>**  
    <span data-ttu-id="82aad-158">이전 버전의 App-v-V에서는 패키지 공유를 콘텐츠 공유 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="82aad-159">관리 서버에 게시 서버 등록-게시 서버는 관리 서버에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="82aad-160">예를 들어 게시 서버 컴퓨터 계정이 관리 서비스 API로 호출할 수 있도록 데이터베이스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-0-package-security"></a> <span data-ttu-id="82aad-161">앱-V 5.0 패키지 보안</span><span class="sxs-lookup"><span data-stu-id="82aad-161">App-V 5.0 package security</span></span>

<span data-ttu-id="82aad-162">다음은 가상화 된 패키지의 안전성을 확인 하는 방법을 계획 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="82aad-163">응용 프로그램 설치 관리자가 ACL (액세스 제어 목록)을 파일 또는 디렉터리에 적용 하는 경우 해당 ACL이 패키지에 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="82aad-164">패키지를 배포 하는 경우 사용자가 파일 또는 디렉터리를 수정 하는 경우 **% userprofile%** 의 acl을 상속 하거나 대상 컴퓨터의 acl을 상속 받습니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="82aad-165">이전 경우는 파일 또는 디렉터리가 가상 파일 시스템 위치에 없는 경우에 발생 합니다. 후자의 경우 파일 또는 디렉터리가 가상 파일 시스템 위치 (예: **% windir%**)에 있는 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-0-log-files"></a> <span data-ttu-id="82aad-166">앱-V 5.0 로그 파일</span><span class="sxs-lookup"><span data-stu-id="82aad-166">App-V 5.0 log files</span></span>


<span data-ttu-id="82aad-167">App-v 5.0 설정을 사용 하는 동안 설치 사용자의 **% temp%** 폴더에 설정 로그 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="82aad-167">During App-V 5.0 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>
