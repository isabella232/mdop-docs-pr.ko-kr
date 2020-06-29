---
title: 삭제된 GPO 복원
description: 삭제된 GPO 복원
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818413"
---
# <span data-ttu-id="787f3-103">삭제된 GPO 복원</span><span class="sxs-lookup"><span data-stu-id="787f3-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="787f3-104">AGPM (고급 그룹 정책 관리)을 사용 하면 승인자가 휴지통에서 삭제 된 GPO (그룹 정책 개체)를 복원 하 여 보관 저장소에 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-104">Advanced Group Policy Management (AGPM) enables Approvers to restore a deleted Group Policy object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="787f3-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-105">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="787f3-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="787f3-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="787f3-107">삭제 된 GPO를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="787f3-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="787f3-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="787f3-109">**콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="787f3-110">복원할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **복원을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="787f3-111">GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="787f3-112">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="787f3-113">**휴지통** 탭에서 GPO가 제거 되 고 **제어** 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="787f3-114">**참고**  프로덕션 환경에서 GPO가 삭제 된 경우 보관 저장소에 복원 하면 자동으로 프로덕션 환경으로 다시 배포 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="787f3-115">GPO를 프로덕션 환경으로 되돌리려면 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="787f3-116">자세한 내용은 [GPO 배포](deploy-a-gpo.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="787f3-116">For information, see [Deploy a GPO](deploy-a-gpo.md).</span></span>

 

### <span data-ttu-id="787f3-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="787f3-117">Additional considerations</span></span>

-   <span data-ttu-id="787f3-118">기본적으로이 절차를 수행 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="787f3-119">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집**, **gpo 배포**또는 gpo **삭제** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="787f3-119">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="787f3-120">추가 참조</span><span class="sxs-lookup"><span data-stu-id="787f3-120">Additional references</span></span>

-   [<span data-ttu-id="787f3-121">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="787f3-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





