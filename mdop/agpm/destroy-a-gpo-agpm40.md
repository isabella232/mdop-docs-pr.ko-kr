---
title: GPO destroy
description: GPO destroy
author: dansimp
ms.assetid: 09bce8c4-f75b-4633-b80b-d894bbec95c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d93b95fceda99a5840705c33e8919d6d7414fe8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818653"
---
# <span data-ttu-id="5150f-103">GPO destroy</span><span class="sxs-lookup"><span data-stu-id="5150f-103">Destroy a GPO</span></span>


<span data-ttu-id="5150f-104">승인자는 GPO (그룹 정책 개체)를 파기 하 고 휴지통에서 제거 하 고 영구적으로 삭제 하 여 더 이상 복원할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-104">Approvers can destroy a Group Policy Object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="5150f-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="5150f-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="5150f-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5150f-107">더 이상 복원할 수 없도록 GPO를 영구적으로 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="5150f-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="5150f-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5150f-109">**콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="5150f-110">삭제할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="5150f-111">**예** 를 클릭 하 여 선택한 GPO 및 보관 저장소의 모든 백업을 영구적으로 삭제할 것인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="5150f-112">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="5150f-113">**휴지통** 탭에서 GPO가 제거 되 고 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="5150f-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="5150f-114">Additional considerations</span></span>

-   <span data-ttu-id="5150f-115">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5150f-116">특히 GPO에 대 한 **목록 콘텐츠와** **gpo** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5150f-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="5150f-117">추가 참조</span><span class="sxs-lookup"><span data-stu-id="5150f-117">Additional references</span></span>

-   [<span data-ttu-id="5150f-118">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="5150f-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





