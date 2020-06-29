---
title: 삭제된 GPO의 복원 요청
description: 삭제된 GPO의 복원 요청
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820368"
---
# <span data-ttu-id="79ca6-103">삭제된 GPO의 복원 요청</span><span class="sxs-lookup"><span data-stu-id="79ca6-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="79ca6-104">승인자 또는 AGPM 관리자 (모든 권한)가 아닌 경우 휴지통에서 삭제 된 GPO (그룹 정책 개체)의 복원을 요청 하 여 보관 저장소에 반환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="79ca6-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 역할이 나 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="79ca6-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="79ca6-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="79ca6-107">삭제 된 GPO의 복원을 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="79ca6-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="79ca6-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="79ca6-109">**콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="79ca6-110">복원 하려는 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **복원을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="79ca6-111">Gpo를 복원할 특별 한 권한이 없는 경우 삭제 된 GPO 복원 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="79ca6-112">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="79ca6-113">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="79ca6-114">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="79ca6-115">**휴지통** 탭에서 GPO가 제거 되 고 **제어** 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="79ca6-116">**참고**  프로덕션 환경에서 GPO가 삭제 된 경우 보관 저장소에 복원 하면 자동으로 프로덕션 환경으로 다시 배포 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="79ca6-117">GPO를 프로덕션 환경으로 되돌리려면 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="79ca6-118">자세한 내용은 [GPO 배포](deploy-a-gpo-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79ca6-118">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="79ca6-119">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="79ca6-119">Additional considerations</span></span>

-   <span data-ttu-id="79ca6-120">기본적으로이 절차를 수행 하려면 편집기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="79ca6-121">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="79ca6-122">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="79ca6-123">GPO가 **휴지통** 탭으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79ca6-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="79ca6-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="79ca6-124">Additional references</span></span>

-   [<span data-ttu-id="79ca6-125">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="79ca6-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





