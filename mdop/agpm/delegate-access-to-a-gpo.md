---
title: GPO에 대한 액세스 권한 위임
description: GPO에 대한 액세스 권한 위임
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818783"
---
# <span data-ttu-id="b215f-103">GPO에 대한 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="b215f-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="b215f-104">승인자는 **해당 승인자가 만든**제어 된 GPO (그룹 정책 개체)의 관리를 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="b215f-105">AGPM 관리자 (모든 권한)와 마찬가지로 승인자는 해당 GPO에 대 한 액세스 권한을 위임할 수 있으므로, 선택한 편집자는 편집할 수 있으며, 검토자는이를 검토할 수 있으며, 다른 승인자는 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="b215f-106">기본적으로 승인자는 다른 그룹 정책 관리자가 만든 Gpo에 대 한 액세스 권한을 위임할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="b215f-107">이 절차를 완료 하려면 AGPM 관리자 (모든 권한) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 고급 그룹 정책 관리에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="b215f-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="b215f-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b215f-109">제어 된 GPO의 관리를 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="b215f-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="b215f-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b215f-111">세부 정보 창의 **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 한 다음 gpo를 클릭 하 여 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="b215f-112">**추가** 단추를 클릭 하 고 액세스를 허용할 사용자 또는 그룹을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="b215f-113">각 항목에 대 한 사용 권한을 사용자 지정 하려면 **콘텐츠** 탭에서 **고급** 단추를 클릭 하 고 역할 권한을 허용 하거나 거부 하도록 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="b215f-114">자세한 컨트롤은 **사용 권한** 대화 상자에서 **고급** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="b215f-115">**적용**을 클릭 한 다음 **사용 권한** 대화 상자에서 **확인** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="b215f-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="b215f-116">Additional considerations</span></span>

-   <span data-ttu-id="b215f-117">기본적으로이 절차를 수행 하려면 GPO 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b215f-118">특히 해당 도메인에 대 한 **콘텐츠 목록** 사용 권한과 GPO에 대 한 **보안 권한을 수정** 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b215f-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="b215f-119">추가 참조</span><span class="sxs-lookup"><span data-stu-id="b215f-119">Additional references</span></span>

-   [<span data-ttu-id="b215f-120">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="b215f-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





