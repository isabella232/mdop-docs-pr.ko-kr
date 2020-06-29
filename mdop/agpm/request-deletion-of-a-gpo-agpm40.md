---
title: GPO의 삭제 요청
description: GPO의 삭제 요청
author: dansimp
ms.assetid: 2410f7a1-ccca-44cf-ab26-76ad474409e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfdb50fba872b76c82152b469f787f2e1a6fb539
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818428"
---
# <span data-ttu-id="ad48d-103">GPO의 삭제 요청</span><span class="sxs-lookup"><span data-stu-id="ad48d-103">Request Deletion of a GPO</span></span>


<span data-ttu-id="ad48d-104">승인자 또는 AGPM 관리자 (모든 권한)가 아닌 경우 GPO (그룹 정책 개체)의 삭제를 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the deletion of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="ad48d-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 역할이 나 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ad48d-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad48d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ad48d-107">제어 된 GPO의 삭제를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="ad48d-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="ad48d-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ad48d-109">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="ad48d-110">삭제 하려는 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="ad48d-111">Gpo의 배포 버전을 실제 환경에 그대로 유지 하면서 보관 파일에서 GPO를 삭제 하려면 **보관 파일 에서만 Gpo 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="ad48d-112">도메인의 보관 및 프로덕션 환경에서 모두 GPO를 삭제 하려면 **보관 및 프로덕션에서 Gpo 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-112">To delete the GPO from both the archive and production environment of the domain, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="ad48d-113">Gpo를 삭제할 특별 한 권한이 없는 경우에는 배포 된 GPO 삭제 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="ad48d-114">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="ad48d-115">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="ad48d-116">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ad48d-117">GPO가 **보류** 탭의 gpo 목록에 표시 됩니다. 승인자가 요청을 승인 하면 **보류 중** 탭에서 **휴지통** 탭으로 GPO가 이동 되며,이 위치는 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="ad48d-118">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="ad48d-118">Additional considerations</span></span>

-   <span data-ttu-id="ad48d-119">기본적으로이 절차를 수행 하려면 편집기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-119">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="ad48d-120">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="ad48d-121">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-121">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="ad48d-122">GPO가 **제어** 탭으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-122">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="ad48d-123">관리 되지 않는 GPO를 먼저 제어 하지 않고 프로덕션 환경에서 삭제 하려면 **그룹 정책 관리 콘솔**에서 **포리스트**, **도메인**을 차례로 클릭 하 고 \*\* &lt; MyDomain &gt; \*\*을 클릭 한 다음 **그룹 정책 개체**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-123">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="ad48d-124">미제어 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad48d-124">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="ad48d-125">추가 참조</span><span class="sxs-lookup"><span data-stu-id="ad48d-125">Additional references</span></span>

-   [<span data-ttu-id="ad48d-126">GPO 삭제 또는 복원</span><span class="sxs-lookup"><span data-stu-id="ad48d-126">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

 

 





