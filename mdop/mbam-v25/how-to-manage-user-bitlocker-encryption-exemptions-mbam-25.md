---
title: 사용자 BitLocker 암호화 예외를 관리하는 방법
description: 사용자 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826793"
---
# <span data-ttu-id="6d816-103">사용자 BitLocker 암호화 예외를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="6d816-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="6d816-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하면 BitLocker 드라이브 암호화 요구 사항에서 사용자를 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="6d816-105">BitLocker 보호에서 사용자를 제외 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6d816-106">작업</span><span class="sxs-lookup"><span data-stu-id="6d816-106">Task</span></span></th>
<th align="left"><span data-ttu-id="6d816-107">세부 정보</span><span class="sxs-lookup"><span data-stu-id="6d816-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6d816-108">제외 된 사용자를 지원 하는 인프라를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6d816-109">이 인프라의 예로는 사용자에 게 예외를 요청 하는 데 사용할 수 있는 연락처 전화 번호, 웹 페이지 또는 메일 주소를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6d816-110">제외 된 사용자에 대해 특별히 구성 되어 있는 그룹 정책 개체에 대 한 보안 그룹에 제외 된 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6d816-111">이 보안 그룹의 구성원이 컴퓨터에 로그인 하면 사용자의 그룹 정책 설정이 BitLocker 보호에서 사용자를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="6d816-112">사용자의 그룹 정책 설정이 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6d816-113">참고</span><span class="sxs-lookup"><span data-stu-id="6d816-113">Note</span></span></strong><br/><p><span data-ttu-id="6d816-114">컴퓨터에 이미 BitLocker로 보호 되어 있고 사용자가 제외 된 경우에는 MBAM이 암호화 정책을 규정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="6d816-115">그러나 암호화 정책에서 제외 되지 않은 다른 사용자가 컴퓨터에 로그인 하는 경우에는 암호화가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="6d816-116">다음 단계에서는 최종 사용자가 MBAM 클라이언트를 통해 또는 조직에서 사용 하는 프로세스를 통해 BitLocker 드라이브 암호화 예외 프로세스에서 예외를 요청할 때 발생 하는 상황을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="6d816-117">최종 사용자가 BitLocker 드라이브 암호화에서 예외를 요청할 수 있도록 MBAM 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="6d816-118">최종 사용자가 암호화 해야 하는 컴퓨터에 로그인 하면 컴퓨터가 암호화 될 것임을 알리는 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="6d816-119">이를 통해 **예외 요청** 을 선택 하 고 **연기**를 선택 하 여 암호화를 연기 하거나, **암호화 시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="6d816-120">참고</span><span class="sxs-lookup"><span data-stu-id="6d816-120">Note</span></span>**  
    <span data-ttu-id="6d816-121">**요청 예외** 선택 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호를 연기 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="6d816-122">최종 사용자가 **예외 요청**을 선택 하는 경우 조직의 BitLocker 관리 그룹에 문의 하 라는 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="6d816-123">**사용자 예외 구성 정책이** 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="6d816-124">전화번호</span><span class="sxs-lookup"><span data-stu-id="6d816-124">Phone number</span></span>

    -   <span data-ttu-id="6d816-125">웹 페이지 URL</span><span class="sxs-lookup"><span data-stu-id="6d816-125">Webpage URL</span></span>

    -   <span data-ttu-id="6d816-126">우편 주소</span><span class="sxs-lookup"><span data-stu-id="6d816-126">Mailing address</span></span>

3.  <span data-ttu-id="6d816-127">예외 요청이 수신 된 후에는 MBAM 관리자가 사용자를 BitLocker 면제 AD DS (Active Directory 도메인 서비스) 그룹에 추가할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="6d816-128">최종 사용자가 예외 요청을 제출 하면 MBAM 클라이언트가 사용자에 게 "일시적으로 제외 됨"으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="6d816-129">그러면 클라이언트는 관리자가 구성 하는 지정 된 일 수를 기다린 후 컴퓨터의 규정 준수를 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="6d816-130">MBAM 관리자가 예외 요청을 거부 하는 경우 예외 요청 옵션이 비활성화 되어 사용자가 예외를 다시 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="6d816-131">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하면 BitLocker 드라이브 암호화 요구 사항에서 사용자를 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="6d816-132">BitLocker 보호에서 사용자를 제외 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6d816-133">작업</span><span class="sxs-lookup"><span data-stu-id="6d816-133">Task</span></span></th>
<th align="left"><span data-ttu-id="6d816-134">세부 정보</span><span class="sxs-lookup"><span data-stu-id="6d816-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6d816-135">제외 된 사용자를 지원 하는 인프라를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6d816-136">이 인프라의 예로는 사용자에 게 예외를 요청 하는 데 사용할 수 있는 연락처 전화 번호, 웹 페이지 또는 메일 주소를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6d816-137">제외 된 사용자에 대해 특별히 구성 되어 있는 그룹 정책 개체에 대 한 보안 그룹에 제외 된 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6d816-138">이 보안 그룹의 구성원이 컴퓨터에 로그인 하면 사용자의 그룹 정책 설정이 BitLocker 보호에서 사용자를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="6d816-139">사용자의 그룹 정책 설정이 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6d816-140">참고</span><span class="sxs-lookup"><span data-stu-id="6d816-140">Note</span></span></strong><br/><p><span data-ttu-id="6d816-141">컴퓨터가 이미 BitLocker로 보호 되는 경우 사용자 예외 정책이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="6d816-142">또한 다른 사용자가 암호화 정책에서 제외 되지 않은 컴퓨터에 로그인 하는 경우에는 암호화가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="6d816-143">다음 단계에서는 최종 사용자가 MBAM 클라이언트를 통해 또는 조직에서 사용 하는 프로세스를 통해 BitLocker 드라이브 암호화 예외 프로세스에서 예외를 요청할 때 발생 하는 상황을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="6d816-144">최종 사용자가 BitLocker 드라이브 암호화에서 예외를 요청할 수 있도록 MBAM 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="6d816-145">최종 사용자가 암호화 해야 하는 컴퓨터에 로그인 하면 컴퓨터가 암호화 될 것임을 알리는 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="6d816-146">이를 통해 **예외 요청** 을 선택 하 고 **연기**를 선택 하 여 암호화를 연기 하거나, **암호화 시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="6d816-147">참고</span><span class="sxs-lookup"><span data-stu-id="6d816-147">Note</span></span>**  
    <span data-ttu-id="6d816-148">**요청 예외** 선택 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호를 연기 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="6d816-149">최종 사용자가 **예외 요청**을 선택 하는 경우 조직의 BitLocker 관리 그룹에 문의 하 라는 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="6d816-150">**사용자 예외 구성 정책이** 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="6d816-151">전화번호</span><span class="sxs-lookup"><span data-stu-id="6d816-151">Phone number</span></span>

    -   <span data-ttu-id="6d816-152">웹 페이지 URL</span><span class="sxs-lookup"><span data-stu-id="6d816-152">Webpage URL</span></span>

    -   <span data-ttu-id="6d816-153">우편 주소</span><span class="sxs-lookup"><span data-stu-id="6d816-153">Mailing address</span></span>

3.  <span data-ttu-id="6d816-154">예외 요청이 수신 된 후에는 MBAM 관리자가 사용자를 BitLocker 면제 AD DS (Active Directory 도메인 서비스) 그룹에 추가할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="6d816-155">최종 사용자가 예외 요청을 제출 하면 MBAM 클라이언트가 사용자에 게 "일시적으로 제외 됨"으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="6d816-156">그러면 클라이언트는 관리자가 구성 하는 지정 된 일 수를 기다린 후 컴퓨터의 규정 준수를 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="6d816-157">MBAM 관리자가 예외 요청을 거부 하는 경우 예외 요청 옵션이 비활성화 되어 사용자가 예외를 다시 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="6d816-158">BitLocker 드라이브 암호화에서 사용자를 제외 하려면</span><span class="sxs-lookup"><span data-stu-id="6d816-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="6d816-159">BitLocker 암호화 요구 사항에서 사용자 예외를 관리 하는 데 사용 되는 AD DS 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="6d816-160">Microsoft BitLocker 관리 및 모니터링 그룹 정책 서식 파일을 사용 하 여 그룹 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="6d816-161">이전 단계에서 만든 AD DS 그룹과 그룹 정책 개체를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="6d816-162">사용자를 제외 하는 정책 설정은 **userconfiguration** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** 에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="6d816-163">BitLocker에 제외 된 사용자를 위해 만든 보안 그룹에 대해 예외를 요청 하는 사용자의 이름을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="6d816-164">사용자가 BitLocker로 제어 되는 컴퓨터에 로그인 하면 MBAM 클라이언트는 사용자 예외 정책 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="6d816-165">컴퓨터가 이미 암호화 된 경우에는 BitLocker 보호가 일시 중단 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="6d816-166">컴퓨터가 암호화 되어 있지 않으면 MBAM은 사용자에 게 암호화를 묻지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="6d816-167">중요</span><span class="sxs-lookup"><span data-stu-id="6d816-167">Important</span></span>**  
    <span data-ttu-id="6d816-168">공유 컴퓨터 시나리오는 BitLocker 사용자 예외를 사용 하는 경우 특별 한 고려 사항이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="6d816-169">예외 비 사용자가 예외 사용자와 공유 된 컴퓨터에 로그인 하는 경우 컴퓨터가 암호화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="6d816-170">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6d816-170">Related topics</span></span>


[<span data-ttu-id="6d816-171">MBAM 2.5 기능 관리</span><span class="sxs-lookup"><span data-stu-id="6d816-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="6d816-172">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="6d816-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="6d816-173">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="6d816-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6d816-174">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="6d816-175">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d816-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




