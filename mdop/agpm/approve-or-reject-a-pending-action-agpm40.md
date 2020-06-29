---
title: 보류 중인 작업 승인 또는 거부
description: 보류 중인 작업 승인 또는 거부
author: dansimp
ms.assetid: 078ea8b5-9ac5-45fc-9ac1-a1aa629c10b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61014ec46db2beb9a525abe8d9b2b0902b3aa78d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819223"
---
# <span data-ttu-id="8b131-103">보류 중인 작업 승인 또는 거부</span><span class="sxs-lookup"><span data-stu-id="8b131-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="8b131-104">승인자는 해당 작업을 완료할 수 있는 권한이 없는 편집기나 검토자의 GPO (그룹 정책 개체) 만들기, 배포 및 삭제에 대 한 요청을 평가한 다음 승인 하거나 거부 하는 것이 주요 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy Object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="8b131-105">보고서는 새 버전의 GPO를 평가 하는 승인자를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-105">Reports can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="8b131-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="8b131-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b131-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8b131-108">대기 중인 요청을 승인 하거나 거부 하려면</span><span class="sxs-lookup"><span data-stu-id="8b131-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="8b131-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8b131-110">**콘텐츠** 탭에서 **보류 중** 탭을 클릭 하 여 보류 중인 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="8b131-111">보류 중인 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **승인** 또는 **거부**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="8b131-112">배포를 승인 하는 경우 **보류 중인 작업 승인** 대화 상자에서 **고급** 을 클릭 하 여 GPO에 대 한 링크를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="8b131-113">트리 항목에 마우스 포인터를 잠시 두면 세부 정보를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="8b131-114">기본적으로 GPO에 대 한 모든 연결이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="8b131-115">링크가 복원 되지 않도록 하려면 해당 링크에 대 한 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="8b131-116">모든 링크가 복원 되는 것을 방지 하려면 **GPO 배포** 대화 상자에서 **링크 복원** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="8b131-117">**예** 또는 **확인** 을 클릭 하 여 보류 중인 작업의 승인 또는 거부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="8b131-118">요청을 승인한 경우 GPO는 수행 된 작업에 대 한 적절 한 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="8b131-119">**참고**  승인자의 전자 메일 주소가 **도메인** **위임** 탭의 **받는 사람 전자 메일 주소** 필드에 포함 되어 있는 경우 승인자는 편집기나 검토자가 요청을 제출할 때 AGPM 별칭에서 전자 메일을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-119">**Note** If an Approver's e-mail address is included in the **To e-mail address** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="8b131-120">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="8b131-120">Additional considerations</span></span>

-   <span data-ttu-id="8b131-121">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8b131-122">특히, 승인 하려는 요청을 수행 하는 데 필요한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b131-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="8b131-123">추가 참조</span><span class="sxs-lookup"><span data-stu-id="8b131-123">Additional references</span></span>

-   [<span data-ttu-id="8b131-124">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8b131-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





