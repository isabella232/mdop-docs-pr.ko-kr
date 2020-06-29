---
title: 사용자 BitLocker 암호화 예외를 관리하는 방법
description: 사용자 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812964"
---
# <span data-ttu-id="06b35-103">사용자 BitLocker 암호화 예외를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="06b35-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="06b35-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 드라이브를 암호화 하지 않아도 되는 사용자를 exempting BitLocker 보호를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="06b35-105">BitLocker 보호에서 사용자를 제외 하려면 먼저 조직이 해당 예외를 지원 하기 위한 인프라를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="06b35-106">지원 인프라에는 예외를 요청 하는 연락처 전화 번호, 웹 페이지 또는 메일 주소가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="06b35-107">또한 예외 사용자는 제외 된 사용자를 위해 특별히 만든 그룹 정책의 보안 그룹에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="06b35-108">이 보안 그룹의 구성원이 컴퓨터에 로그온 하면 사용자 그룹 정책에 의해 사용자가 BitLocker 보호에서 제외 된 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="06b35-109">사용자 정책은 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="06b35-110">**참고**  컴퓨터가 이미 BitLocker로 보호 되는 경우 사용자 예외 정책이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="06b35-111">다음 표에서는 예외를 설정 하는 방법에 따라 BitLocker 보호가 적용 되는 방식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="06b35-112">사용자 상태</span><span class="sxs-lookup"><span data-stu-id="06b35-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="06b35-113">컴퓨터가 제외 되지 않음</span><span class="sxs-lookup"><span data-stu-id="06b35-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="06b35-114">컴퓨터 예외</span><span class="sxs-lookup"><span data-stu-id="06b35-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="06b35-115">사용자 제외 되지 않음</span><span class="sxs-lookup"><span data-stu-id="06b35-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="06b35-116">컴퓨터에 BitLocker 보호가 적용 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="06b35-117">컴퓨터에 BitLocker 보호가 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="06b35-118">사용자 예외</span><span class="sxs-lookup"><span data-stu-id="06b35-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="06b35-119">컴퓨터에 BitLocker 보호가 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="06b35-120">컴퓨터에 BitLocker 보호가 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="06b35-121">BitLocker 암호화에서 사용자를 제외 하려면</span><span class="sxs-lookup"><span data-stu-id="06b35-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="06b35-122">BitLocker 암호화에서 사용자 예외를 관리 하는 데 사용 되는 ActiveDirectoryDomainServices 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="06b35-123">MBAM 그룹 정책 서식 파일을 사용 하 여 그룹 정책 개체 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="06b35-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="06b35-124">이전 단계에서 만든 Active Directory 그룹과 그룹 정책 개체를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="06b35-125">사용자가 BitLocker 암호화에서 예외를 요청할 수 있도록 하는 데 필요한 정책 설정에 대 한 자세한 내용은 [MBAM 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)의 사용자 예외 구성 정책 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06b35-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="06b35-126">BitLocker 제외 된 사용자에 대 한 보안 그룹을 만든 후이 그룹에 예외를 요청 하는 사용자의 이름을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="06b35-127">사용자가 BitLocker로 제어 되는 컴퓨터에 로그온 하면 MBAM 클라이언트가 사용자 예외 정책 설정을 확인 하 고 사용자가 BitLocker 예외 보안 그룹의 일부 인지 여부에 따라 보호를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="06b35-128">**참고**  공유 컴퓨터 시나리오는 사용자 예외에 대 한 특별 한 고려 사항이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="06b35-129">비 예외 사용자가 예외 사용자와 공유 된 컴퓨터에 로그온 하면 컴퓨터가 암호화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="06b35-130">사용자가 BitLocker 암호화에서 예외를 요청할 수 있도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="06b35-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="06b35-131">MBAM 정책 템플릿을 usingwith 하 여 사용자 예외 정책을 구성한 후에는 사용자가 MBAM 클라이언트를 통해 BitLocker 보호의 예외를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="06b35-132">사용자가 MBAM 하드웨어 호환성 목록에서 **호환** 되는 것으로 표시 된 컴퓨터에 로그온 하면 시스템은 컴퓨터를 암호화할 수 있는 알림을 사용자에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="06b35-133">사용자는 **예외 요청** 을 선택 하 고 **나중**에 선택 하 여 암호화를 연기 하거나 **시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="06b35-134">**참고**  **요청 예외** 를 선택 하면 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호가 연기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="06b35-135">사용자가 **예외 요청**을 선택 하면 조직의 BitLocker 관리 그룹에 게 연락할 수 있는 알림이 사용자에 게 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="06b35-136">사용자 예외 구성 정책이 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="06b35-137">전화 번호</span><span class="sxs-lookup"><span data-stu-id="06b35-137">Phone Number</span></span>

    -   <span data-ttu-id="06b35-138">웹 페이지 URL</span><span class="sxs-lookup"><span data-stu-id="06b35-138">Webpage URL</span></span>

    -   <span data-ttu-id="06b35-139">우편 주소</span><span class="sxs-lookup"><span data-stu-id="06b35-139">Mailing Address</span></span>

    <span data-ttu-id="06b35-140">요청을 제출 하 고 나면 MBAM 관리자는 BitLocker 예외 Active Directory 그룹에 사용자를 추가 하는 것이 적절 한지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="06b35-141">**참고**  사용자 예외 정책의 연기 시간 한도가 만료 된 후에는 사용자가 암호화 정책에 대 한 예외를 요청 하는 옵션이 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="06b35-142">이 시점에서 사용자는 BitLocker 보호에서 예외를 수신 하기 위해 MBAM 관리자에 게 직접 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b35-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="06b35-143">관련 항목</span><span class="sxs-lookup"><span data-stu-id="06b35-143">Related topics</span></span>


[<span data-ttu-id="06b35-144">MBAM 1.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="06b35-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





