---
title: 제어된 GPO 삭제
description: 제어된 GPO 삭제
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818713"
---
# <span data-ttu-id="f42e6-103">제어된 GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="f42e6-103">Delete a Controlled GPO</span></span>


<span data-ttu-id="f42e6-104">승인자는 제어 된 GPO (그룹 정책 개체)를 휴지통으로 이동 하 여 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-104">Approvers can delete a controlled Group Policy Object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="f42e6-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f42e6-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="f42e6-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f42e6-107">제어 된 GPO를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="f42e6-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="f42e6-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f42e6-109">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f42e6-110">삭제 하려는 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="f42e6-111">Gpo의 배포 버전을 실제 환경에 그대로 유지 하면서 보관 파일에서 GPO를 삭제 하려면 **보관 파일 에서만 Gpo 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="f42e6-112">보관 및 프로덕션 환경에서 모두 GPO를 삭제 하려면 **보관 및 프로덕션에서 Gpo 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="f42e6-113">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="f42e6-114">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f42e6-115">GPO가 **제어** 탭에서 제거 되 고 **휴지통** 탭에 표시 되며 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="f42e6-116">보관 함 에서만 GPO를 삭제 하면 **제어** 되지 않은 탭에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="f42e6-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="f42e6-117">Additional considerations</span></span>

-   <span data-ttu-id="f42e6-118">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f42e6-119">특히 GPO에 대 한 **목록 콘텐츠와** **gpo** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="f42e6-120">관리 되지 않는 GPO를 먼저 제어 하지 않고 프로덕션 환경에서 삭제 하려면 **그룹 정책 관리 콘솔**에서 **포리스트**, **도메인**을 차례로 클릭 하 고 \*\* &lt; MyDomain &gt; \*\*을 클릭 한 다음 **그룹 정책 개체**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-120">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="f42e6-121">미제어 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f42e6-121">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="f42e6-122">추가 참조</span><span class="sxs-lookup"><span data-stu-id="f42e6-122">Additional references</span></span>

-   [<span data-ttu-id="f42e6-123">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="f42e6-123">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





