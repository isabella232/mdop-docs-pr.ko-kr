---
title: GPO 배포
description: GPO 배포
author: dansimp
ms.assetid: a6febeaa-144b-4c02-99af-d972f0f2b544
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 208fd95ec48f81b6c3a2a59bf92f53128eb3d529
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818703"
---
# <span data-ttu-id="19d71-103">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="19d71-103">Deploy a GPO</span></span>


<span data-ttu-id="19d71-104">승인자는 신규 또는 편집한 GPO (그룹 정책 개체)를 프로덕션 환경에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-104">An Approver can deploy a new or edited Group Policy Object (GPO) to the production environment.</span></span> <span data-ttu-id="19d71-105">이전 버전의 GPO 다시 배포에 대 한 자세한 내용은 [이전 버전의 gpo로 롤백을](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19d71-105">For information about redeploying an earlier version of a GPO, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

<span data-ttu-id="19d71-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="19d71-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="19d71-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="19d71-108">프로덕션 환경에 GPO를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="19d71-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="19d71-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="19d71-110">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="19d71-111">배포할 GPO를 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="19d71-112">GPO에 대 한 링크를 검토 하려면 **고급**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="19d71-113">트리 항목에 마우스 포인터를 잠시 두면 세부 정보를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="19d71-114">기본적으로 GPO에 대 한 모든 연결이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="19d71-115">링크가 복원 되지 않도록 하려면 해당 링크에 대 한 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="19d71-116">모든 링크가 복원 되는 것을 방지 하려면 **GPO 배포** 대화 상자에서 **링크 복원** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="19d71-117">**예**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-117">Click **Yes**.</span></span> <span data-ttu-id="19d71-118">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="19d71-119">**참고**  최신 버전의 GPO가 배포 되었는지 확인 하려면 **제어** 탭에서 GPO를 두 번 클릭 하 여 **기록을**표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="19d71-120">GPO의 **기록** 에서 **상태** 열은 gpo가 배포 되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="19d71-121">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="19d71-121">Additional considerations</span></span>

-   <span data-ttu-id="19d71-122">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="19d71-123">특히 GPO에 대 한 **목록 콘텐츠** 및 **gpo** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d71-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="19d71-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="19d71-124">Additional references</span></span>

-   [<span data-ttu-id="19d71-125">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="19d71-125">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





