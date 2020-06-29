---
title: 도메인 위임 탭
description: 도메인 위임 탭
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818628"
---
# <span data-ttu-id="bd69a-103">도메인 위임 탭</span><span class="sxs-lookup"><span data-stu-id="bd69a-103">Domain Delegation Tab</span></span>


<span data-ttu-id="bd69a-104">**변경 제어** 창의 **도메인 위임** 탭에서는 보관 저장소에 대 한 도메인 수준 액세스 권한이 있는 그룹 정책 관리자 목록을 제공 하 고, 각각의 역할을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="bd69a-105">또한이 탭에서는 AGPM 관리자 (모든 권한)에서 편집자, 승인자, 검토자 및 기타 AGPM 관리자에 대 한 도메인 수준 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="bd69a-106">도메인 **위임** 탭에는 도메인 수준에서 AGPM (고급 그룹 정책 관리)에 대 한 전자 메일 알림 및 역할 기반 위임 구성 이라는 두 가지 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="bd69a-107">전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="bd69a-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="bd69a-108">이 탭의 전자 메일 알림 섹션에는 AGPM에서 작업이 보류 중일 때 알림을 받을 승인자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd69a-109">설정</span><span class="sxs-lookup"><span data-stu-id="bd69a-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="bd69a-110">설명</span><span class="sxs-lookup"><span data-stu-id="bd69a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bd69a-111">전</span><span class="sxs-lookup"><span data-stu-id="bd69a-111">From</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-112">알림을 승인자에 게 보내는 AGPM 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="bd69a-113">여러 도메인이 있는 환경에서이는 환경 전체에서 동일한 별칭 이거나 각 도메인에 대 한 다른 별칭 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bd69a-114">작업</span><span class="sxs-lookup"><span data-stu-id="bd69a-114">To</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-115">알림을 보낼 결재자의 전자 메일 주소 목록 (쉼표로 구분)</span><span class="sxs-lookup"><span data-stu-id="bd69a-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bd69a-116">SMTP 서버</span><span class="sxs-lookup"><span data-stu-id="bd69a-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-117">전자 메일 서버의 이름 (예: mail.contoso.com)</span><span class="sxs-lookup"><span data-stu-id="bd69a-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bd69a-118">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="bd69a-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-119">SMTP 서버에 대 한 액세스 권한이 있는 사용자</span><span class="sxs-lookup"><span data-stu-id="bd69a-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bd69a-120">암호</span><span class="sxs-lookup"><span data-stu-id="bd69a-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-121">SMTP 서버 인증을 위한 사용자 암호</span><span class="sxs-lookup"><span data-stu-id="bd69a-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bd69a-122">암호 확인</span><span class="sxs-lookup"><span data-stu-id="bd69a-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-123">사용자 암호 확인</span><span class="sxs-lookup"><span data-stu-id="bd69a-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bd69a-124">도메인 수준 역할 기반 위임</span><span class="sxs-lookup"><span data-stu-id="bd69a-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="bd69a-125">이 탭의 역할 기반 위임 섹션은 AGPM 관리자가 보관에 대 한 액세스 권한을 가진 각 그룹 및 사용자에 대해 허용, 거부 및 상속 된 사용 권한을 위임할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="bd69a-126">AGPM 관리자는 표준 AGPM 역할 (편집자, 승인자, 검토자, AGPM 관리자) 또는 각 그룹 정책 관리자에 대 한 사용자 지정 된 사용 권한 조합을 사용 하 여 도메인 전체 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd69a-127">단추</span><span class="sxs-lookup"><span data-stu-id="bd69a-127">Button</span></span></th>
<th align="left"><span data-ttu-id="bd69a-128">효과</span><span class="sxs-lookup"><span data-stu-id="bd69a-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bd69a-129">Add</span><span class="sxs-lookup"><span data-stu-id="bd69a-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-130">보안 설명자에 새 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="bd69a-131">Active Directory의 모든 사용자 또는 그룹은 그룹 정책 관리자로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bd69a-132">제거</span><span class="sxs-lookup"><span data-stu-id="bd69a-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-133">선택 된 그룹 정책 관리자를 액세스 제어 목록에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bd69a-134">특성</span><span class="sxs-lookup"><span data-stu-id="bd69a-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-135">선택한 그룹 정책 관리자의 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd69a-135">Display the properties for the selected Group Policy administrators.</span></span> <span data-ttu-id="bd69a-136">속성 페이지는 <strong> Active Directory 사용자 및 컴퓨터의 개체에 대해 표시 되는 것과 동일 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="bd69a-136">The properties page is the same one displayed for an object in <strong>Active Directory User and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bd69a-137">고급</span><span class="sxs-lookup"><span data-stu-id="bd69a-137">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bd69a-138"><strong>액세스 제어 목록 편집기를 엽니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="bd69a-138">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="bd69a-139">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="bd69a-139">Additional considerations</span></span>

-   <span data-ttu-id="bd69a-140">특정 작업과 관련 된 역할 및 권한에 대 한 자세한 내용은 [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks.md), [편집자 작업](performing-editor-tasks.md)수행, [승인자 작업 수행](performing-approver-tasks.md), [검토자 작업 수행](performing-reviewer-tasks.md)의 작업을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd69a-140">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="bd69a-141">추가 참조</span><span class="sxs-lookup"><span data-stu-id="bd69a-141">Additional references</span></span>

-   [<span data-ttu-id="bd69a-142">사용자 인터페이스: 고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="bd69a-142">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

-   [<span data-ttu-id="bd69a-143">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="bd69a-143">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





