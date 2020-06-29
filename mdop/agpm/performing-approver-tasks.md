---
title: 승인자 작업 수행
description: 승인자 작업 수행
author: dansimp
ms.assetid: 6f6310b3-19c1-47c9-8615-964ddd10ce14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc77a1dd9a3d54e637ae4baeb452d327672ed250
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820428"
---
# <span data-ttu-id="e5bb3-103">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="e5bb3-103">Performing Approver Tasks</span></span>


<span data-ttu-id="e5bb3-104">승인자는 AGPM 관리자 (모든 권한)가 승인 하는 사람이 며, Gpo (그룹 정책 개체)를 만들고, 배포 하 고, 삭제 하 고, 요청 (일반적으로 편집자의)을 승인 또는 거부 하 여 Gpo를 만들거나 배포 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="e5bb3-105">**중요**  Gpo의 중앙 보관 파일에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-105">**Important** Ensure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="e5bb3-106">자세한 내용은 [AGPM 서버 연결 구성을](configure-the-agpm-server-connection-reviewer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-106">For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

 

-   [<span data-ttu-id="e5bb3-107">보류 중인 작업 승인 또는 거부</span><span class="sxs-lookup"><span data-stu-id="e5bb3-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action.md)

-   [<span data-ttu-id="e5bb3-108">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="e5bb3-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

-   [<span data-ttu-id="e5bb3-109">GPO 체크 인</span><span class="sxs-lookup"><span data-stu-id="e5bb3-109">Check In a GPO</span></span>](check-in-a-gpo-approver.md)

-   [<span data-ttu-id="e5bb3-110">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="e5bb3-110">Deploy a GPO</span></span>](deploy-a-gpo.md)

-   [<span data-ttu-id="e5bb3-111">이전 버전의 GPO로 롤백</span><span class="sxs-lookup"><span data-stu-id="e5bb3-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo.md)

-   [<span data-ttu-id="e5bb3-112">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="e5bb3-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

<span data-ttu-id="e5bb3-113">**참고**  승인자 역할에는 검토자 역할에 대 한 사용 권한이 포함 되므로 승인자는 설정을 검토 하 고 Gpo를 비교할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-113">**Note** Because the Approver role includes the permissions for the Reviewer role, an Approver can also review settings and compare GPOs.</span></span> <span data-ttu-id="e5bb3-114">자세한 내용은 [검토자 작업 수행](performing-reviewer-tasks.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-114">See [Performing Reviewer Tasks](performing-reviewer-tasks.md) for more information.</span></span>

 

### <span data-ttu-id="e5bb3-115">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="e5bb3-115">Additional considerations</span></span>

<span data-ttu-id="e5bb3-116">기본적으로 승인자 역할에는 다음 사용 권한이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-116">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="e5bb3-117">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="e5bb3-117">List Contents</span></span>

-   <span data-ttu-id="e5bb3-118">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="e5bb3-118">Read Settings</span></span>

-   <span data-ttu-id="e5bb3-119">GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="e5bb3-119">Create GPO</span></span>

-   <span data-ttu-id="e5bb3-120">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="e5bb3-120">Deploy GPO</span></span>

-   <span data-ttu-id="e5bb3-121">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="e5bb3-121">Delete GPO</span></span>

<span data-ttu-id="e5bb3-122">또한 승인자는 자신이 만들었거나 제어 하는 Gpo에 대해 모든 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="e5bb3-122">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





