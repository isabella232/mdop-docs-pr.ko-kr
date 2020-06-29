---
title: GPO 체크 인
description: GPO 체크 인
author: dansimp
ms.assetid: e428cfff-651f-4903-bf01-d742714d2fa9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6adbcfa1c2b0d79389bc16dd1dde5afc0a4ec4a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819148"
---
# <span data-ttu-id="5fd4a-103">GPO 체크 인</span><span class="sxs-lookup"><span data-stu-id="5fd4a-103">Check In a GPO</span></span>


<span data-ttu-id="5fd4a-104">일반적으로 편집자는 수정이 완료 되 면 편집한 Gpo (그룹 정책 개체)를 체크 인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-104">Ordinarily, Editors should check in Group Policy objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="5fd4a-105">자세한 내용은 [오프 라인으로 GPO 편집](edit-a-gpo-offline.md)을 참조 하세요. 그러나 편집기를 사용할 수 없는 경우에는 승인자가 GPO도 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="5fd4a-106">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="5fd4a-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5fd4a-108">편집기에 의해 체크 아웃 된 GPO를 체크 인하려면</span><span class="sxs-lookup"><span data-stu-id="5fd4a-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="5fd4a-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5fd4a-110">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-110">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="5fd4a-111">편집기에서 변경한 내용을 취소 하려면 해당 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크 아웃 취소**를 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="5fd4a-112">편집기에서 변경한 내용을 유지 하려면 해당 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크**인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="5fd4a-113">GPO의 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="5fd4a-114">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="5fd4a-115">**제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="5fd4a-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="5fd4a-116">Additional considerations</span></span>

-   <span data-ttu-id="5fd4a-117">기본적으로이 절차를 수행 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5fd4a-118">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 또는 **gpo 배포** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="5fd4a-119">승인자 또는 AGPM 관리자 (또는 **GPO 배포** 권한이 있는 다른 그룹 정책 관리자)가 아닌 경우 gpo를 체크 아웃 한 편집기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd4a-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="5fd4a-120">추가 참조</span><span class="sxs-lookup"><span data-stu-id="5fd4a-120">Additional references</span></span>

-   [<span data-ttu-id="5fd4a-121">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="5fd4a-121">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="5fd4a-122">오프라인에서 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="5fd4a-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline.md)

 

 





