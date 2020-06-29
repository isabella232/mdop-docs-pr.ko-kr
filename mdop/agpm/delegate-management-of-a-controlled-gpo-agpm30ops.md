---
title: 제어된 GPO의 관리 위임
description: 제어된 GPO의 관리 위임
author: dansimp
ms.assetid: 509b02e7-ce0b-4919-b58a-c3a33051152e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d34231f25c172951cd0176b3e490dab84b98f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818718"
---
# <span data-ttu-id="473ce-103">제어된 GPO의 관리 위임</span><span class="sxs-lookup"><span data-stu-id="473ce-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="473ce-104">승인자는 해당 승인자가 만든 제어 된 GPO (그룹 정책 개체)의 관리를 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="473ce-105">AGPM 관리자 (모든 권한)와 마찬가지로 승인자는 해당 GPO에 대 한 액세스 권한을 위임 하 여 선택한 편집자가 편집할 수 있도록 하 고, 검토자가 검토 하 고, 다른 승인자가 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="473ce-106">기본적으로 승인자는 다른 그룹 정책 관리자가 만든 Gpo에 대 한 액세스 권한을 위임할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="473ce-107">이 절차를 완료 하려면 AGPM 관리자 (전체 제어) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 AGPM (고급 그룹 정책 관리)에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="473ce-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="473ce-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="473ce-109">제어 된 GPO의 관리를 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="473ce-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="473ce-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="473ce-111">세부 정보 창의 **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 한 다음 gpo를 클릭 하 여 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="473ce-112">사용자 또는 그룹에 대 한 액세스 권한을 추가 하려면 **추가** 단추를 클릭 하 고 사용자 또는 그룹을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="473ce-113">**그룹 또는 사용자 추가** 대화 상자에서 역할을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="473ce-114">사용자 또는 그룹에 대 한 액세스 권한을 제거 하려면 해당 사용자 또는 그룹을 선택한 다음 **제거** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="473ce-115">**참고**  사용자 또는 그룹이 도메인 전체 액세스를 상속 하는 경우 **제거** 단추를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="473ce-116">**도메인 위임** 탭에서 도메인 전체 액세스를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="473ce-117">사용자 또는 그룹에 게 위임 된 역할 및 사용 권한을 수정 하려면 **고급** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="473ce-118">**사용 권한** 대화 상자에서 사용자 또는 그룹을 선택 하 고 해당 사용자 또는 그룹에 지정할 각 역할에 대 한 확인란을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="473ce-119">**참고**  편집자 및 승인자는 검토자 권한을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="473ce-120">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="473ce-120">Additional considerations</span></span>

-   <span data-ttu-id="473ce-121">기본적으로이 절차를 수행 하려면 GPO 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="473ce-122">특히 해당 도메인에 대 한 **콘텐츠 목록** 사용 권한과 GPO에 대 한 **보안 권한을 수정** 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="473ce-123">AGPM을 사용 하는 그룹 정책 관리자에 게 읽기 권한을 위임 하려면 **설정 읽기** 권한과 함께 **목록 콘텐츠** 를 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="473ce-124">이렇게 하면 AGPM의 **콘텐츠** 탭에서 gpo를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="473ce-125">다른 사용 권한은 명시적으로 위임 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="473ce-126">그룹 정책 소프트웨어 설치를 완전히 사용 하려면 편집자에 게 GPO의 배포 된 복사본에 대 한 **읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ce-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="473ce-127">추가 참조</span><span class="sxs-lookup"><span data-stu-id="473ce-127">Additional references</span></span>

-   [<span data-ttu-id="473ce-128">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="473ce-128">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





