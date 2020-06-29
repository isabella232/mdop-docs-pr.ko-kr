---
title: 사용자 BitLocker 암호화 예외를 관리하는 방법
description: 사용자 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825073"
---
# <span data-ttu-id="193b1-103">사용자 BitLocker 암호화 예외를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="193b1-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="193b1-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 드라이브를 암호화 하지 않아도 되는 사용자가 있는 경우 exempting 사용자가 BitLocker 보호를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="193b1-105">BitLocker 보호에서 사용자를 제외 하려면 조직에서 사용자에 게 예외를 요청 하는 데 사용할 연락처 전화 번호, 웹 페이지 또는 메일 주소를 제공 하는 등 제외 된 사용자를 지원 하는 인프라를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="193b1-106">또한 예외 사용자는 제외 된 사용자를 위해 특별히 만든 그룹 정책 개체에 대 한 보안 그룹에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="193b1-107">이 보안 그룹의 구성원이 컴퓨터에 로그온 하면 사용자의 그룹 정책 설정에 따라 사용자가 BitLocker 보호에서 제외 되었다는 것이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="193b1-108">사용자의 그룹 정책 설정이 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="193b1-109">**참고**  컴퓨터가 이미 BitLocker로 보호 되는 경우 사용자 예외 정책이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="193b1-110">다음 표에서는 예외를 설정 하는 방법에 따라 BitLocker 보호가 적용 되는 방식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="193b1-111">사용자 상태</span><span class="sxs-lookup"><span data-stu-id="193b1-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="193b1-112">컴퓨터가 제외 되지 않음</span><span class="sxs-lookup"><span data-stu-id="193b1-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="193b1-113">컴퓨터 예외</span><span class="sxs-lookup"><span data-stu-id="193b1-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="193b1-114">사용자 제외 되지 않음</span><span class="sxs-lookup"><span data-stu-id="193b1-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="193b1-115">컴퓨터에 BitLocker 보호가 적용 됨</span><span class="sxs-lookup"><span data-stu-id="193b1-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="193b1-116">컴퓨터에 BitLocker 보호가 적용 되지 않음</span><span class="sxs-lookup"><span data-stu-id="193b1-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="193b1-117">사용자 예외</span><span class="sxs-lookup"><span data-stu-id="193b1-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="193b1-118">컴퓨터에 BitLocker 보호가 적용 되지 않음</span><span class="sxs-lookup"><span data-stu-id="193b1-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="193b1-119">컴퓨터에 BitLocker 보호가 적용 되지 않음</span><span class="sxs-lookup"><span data-stu-id="193b1-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="193b1-120">BitLocker 암호화에서 사용자를 제외 하려면</span><span class="sxs-lookup"><span data-stu-id="193b1-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="193b1-121">BitLocker 암호화 요구 사항에서 사용자 예외를 관리 하는 데 사용 되는 ActiveDirectoryDomainServices 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="193b1-122">Microsoft BitLocker 관리 및 모니터링 그룹 정책 서식 파일을 사용 하 여 그룹 정책 개체 설정을 만들고 이전 단계에서 만든 Active Directory 그룹과 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="193b1-123">사용자를 제외 하는 정책 설정은 **Userconfiguration\\administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)** 에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="193b1-124">BitLocker 제외 된 사용자에 대 한 보안 그룹을 만든 후이 그룹에 예외를 요청 하는 사용자의 이름을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="193b1-125">사용자가 BitLocker로 제어 되는 컴퓨터에 로그온 하면 MBAM 클라이언트가 사용자 예외 정책 설정을 확인 하 고 사용자가 BitLocker 예외 보안 그룹의 일부 인지 여부에 따라 보호를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="193b1-126">**중요**  공유 컴퓨터 시나리오는 사용자 예외를 사용할 때 특별 한 고려 사항이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="193b1-127">비 예외 사용자가 예외 사용자와 공유 된 컴퓨터에 로그온 하면 컴퓨터가 암호화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="193b1-128">사용자가 BitLocker 암호화에서 예외를 요청할 수 있도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="193b1-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="193b1-129">MBAM 정책 템플릿을 사용 하 여 사용자 예외 정책을 구성한 경우 사용자는 MBAM 클라이언트를 통해 BitLocker 보호에서 예외를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="193b1-130">사용자가 암호화 해야 하는 컴퓨터에 로그온 할 때 컴퓨터가 암호화 될 것임을 알리는 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="193b1-131">**예외 요청** 을 선택 하 고 **나중**에 선택 하 여 암호화를 연기 하거나 **시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="193b1-132">**참고**  **요청 예외** 선택 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호를 연기 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="193b1-133">사용자가 **예외 요청**을 선택 하는 경우 조직의 BitLocker 관리 그룹에 문의 하 라는 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="193b1-134">사용자 예외 구성 정책이 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="193b1-135">전화 번호</span><span class="sxs-lookup"><span data-stu-id="193b1-135">Phone Number</span></span>

    -   <span data-ttu-id="193b1-136">웹 페이지 URL</span><span class="sxs-lookup"><span data-stu-id="193b1-136">Webpage URL</span></span>

    -   <span data-ttu-id="193b1-137">우편 주소</span><span class="sxs-lookup"><span data-stu-id="193b1-137">Mailing Address</span></span>

    <span data-ttu-id="193b1-138">예외 요청이 수신 된 후에는 MBAM 관리자가 사용자를 BitLocker 예외 Active Directory 그룹에 추가 하는 것이 적절 한지 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="193b1-139">**참고**  사용자가 예외 요청을 제출 하면 MBAM 에이전트는 사용자를 "일시적으로 예외"로 보고 하 고 구성 가능한 일 수를 기다린 후 컴퓨터의 준수를 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="193b1-140">MBAM 관리자가 예외 요청을 거부 하는 경우 예외 요청 옵션이 비활성화 되어 사용자가 예외를 다시 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="193b1-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="193b1-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="193b1-141">Related topics</span></span>


[<span data-ttu-id="193b1-142">MBAM 2.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="193b1-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





