---
title: 전자 메일 알림 구성
description: 전자 메일 알림 구성
author: dansimp
ms.assetid: 06f19556-f296-4a80-86a4-4f446c992204
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b751a49d3d22f893c420be7fef9714b242d1f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818998"
---
# <span data-ttu-id="d12fb-103">전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="d12fb-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="d12fb-104">편집기나 검토자가 GPO (그룹 정책 개체)를 만들거나, 배포 하거나, 삭제 하려고 할 때 승인자가 요청을 평가 하 고이를 구현 하거나 거부할 수 있도록이 작업에 대 한 요청이 지정 된 전자 메일 주소 또는 주소로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy Object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="d12fb-105">알림이 전송 되는 전자 메일 주소 또는 주소와 알림을 보내는 별칭을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="d12fb-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="d12fb-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="d12fb-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d12fb-108">AGPM에 대 한 전자 메일 알림을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d12fb-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="d12fb-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d12fb-110">세부 정보 창에서 **도메인 위임** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="d12fb-111">보낸 사람 **전자 메일 주소** 필드에 알림을 보낼 AGPM의 전자 메일 별칭을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-111">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="d12fb-112">받는 사람 **전자 메일 주소** 필드에 승인 요청을 받을 승인자의 전자 메일 주소 목록을 쉼표로 구분 하 여 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-112">In the **To e-mail address** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="d12fb-113">**Smtp 서버** 필드에 유효한 SMTP 메일 서버를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="d12fb-114">**사용자 이름** 및 **암호** 필드에 SMTP 서비스에 대 한 액세스 권한이 있는 사용자의 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="d12fb-115">**적용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-115">Click **Apply**.</span></span>

### <span data-ttu-id="d12fb-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d12fb-116">Additional considerations</span></span>

-   <span data-ttu-id="d12fb-117">기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d12fb-118">특히 도메인에 대 한 **목록 콘텐츠** 및 **옵션 수정** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="d12fb-119">AGPM에 대 한 전자 메일 알림은 도메인 수준 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="d12fb-120">각 도메인의 **도메인 위임** 탭에 다른 승인자 전자 메일 주소 또는 AGPM 전자 메일 별칭을 제공 하거나 환경 전체에서 동일한 전자 메일 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

-   <span data-ttu-id="d12fb-121">기본적으로 AGPM (고급 그룹 정책 관리)에서 작업의 결과로 전송 된 전자 메일 메시지는 암호화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-121">By default, e-mail messages sent as a result of actions in Advanced Group Policy Management (AGPM) are not encrypted.</span></span> <span data-ttu-id="d12fb-122">그러나 레지스트리 설정을 사용 하 여 AGPM에 대 한 전자 메일 보안을 구성 하 여 SSL (Secure Sockets Layer) 암호화 사용 여부와 사용할 SMTP 포트를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d12fb-122">However, you can configure e-mail security for AGPM using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span> <span data-ttu-id="d12fb-123">자세한 내용은 [AGPM 용 전자 메일 보안 구성을](configure-e-mail-security-for-agpm-agpm40.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d12fb-123">For more information, see [Configure E-Mail Security for AGPM](configure-e-mail-security-for-agpm-agpm40.md).</span></span>

### <span data-ttu-id="d12fb-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="d12fb-124">Additional references</span></span>

-   [<span data-ttu-id="d12fb-125">고급 그룹 정책 관리 구성</span><span class="sxs-lookup"><span data-stu-id="d12fb-125">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





