---
title: GPO 삭제
description: GPO 삭제
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820983"
---
# <span data-ttu-id="58cd3-103">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="58cd3-103">Delete a GPO</span></span>


<span data-ttu-id="58cd3-104">AGPM (고급 그룹 정책 관리)을 사용 하면 승인자가 제어 된 GPO (그룹 정책 개체)를 삭제 하 고 휴지통으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-104">Advanced Group Policy Management (AGPM) enables Approvers to delete a controlled Group Policy object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="58cd3-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="58cd3-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="58cd3-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="58cd3-107">제어 된 GPO를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="58cd3-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="58cd3-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="58cd3-109">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="58cd3-110">삭제할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="58cd3-111">배포 된 버전의 GPO를 프로덕션 환경에 그대로 유지 하면서 보관 파일에서 GPO를 삭제 하려면 **보관 시에만 Gpo 삭제 (제어**되지 않음)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="58cd3-112">보관 및 프로덕션 환경에서 모두 GPO를 삭제 하려면 **보관 및 프로덕션에서 Gpo 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="58cd3-113">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="58cd3-114">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="58cd3-115">GPO가 **제어** 탭에서 제거 되 고 **휴지통** 탭에 표시 되며 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="58cd3-116">보관 함 에서만 GPO를 삭제 하면 **제어** 되지 않은 탭에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="58cd3-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="58cd3-117">Additional considerations</span></span>

-   <span data-ttu-id="58cd3-118">배포 된 GPO를 삭제 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to delete a deployed GPO.</span></span> <span data-ttu-id="58cd3-119">특히 GPO에 대 한 **목록 콘텐츠와** **gpo** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="58cd3-120">기본적으로 저장소에서 GPO를 삭제 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-120">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="58cd3-121">특히, GPO에 대 한 **목록 내용이** 있고 **설정을 편집** 하거나 **gpo** 사용 권한을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-121">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="58cd3-122">관리 되지 않는 GPO를 먼저 제어 하지 않고 프로덕션 환경에서 삭제 하려면 **그룹 정책 관리 콘솔**에서 **포리스트**, **도메인**을 차례로 클릭 하 고 \*\* &lt; MyDomain &gt; \*\*을 클릭 한 다음 **그룹 정책 개체**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-122">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="58cd3-123">미제어 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58cd3-123">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="58cd3-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="58cd3-124">Additional references</span></span>

-   [<span data-ttu-id="58cd3-125">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="58cd3-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





