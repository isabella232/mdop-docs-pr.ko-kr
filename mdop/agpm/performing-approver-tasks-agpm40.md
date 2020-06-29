---
title: 승인자 작업 수행
description: 승인자 작업 수행
author: dansimp
ms.assetid: e0a4b7fe-ce69-4755-9104-c7f523ea6b62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a0815bdd6c34a7a23b27075b3b5367757c1f84e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820468"
---
# <span data-ttu-id="9e388-103">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="9e388-103">Performing Approver Tasks</span></span>


<span data-ttu-id="9e388-104">승인자는 AGPM 관리자 (모든 권한)가 승인 하는 사람이 며, Gpo (그룹 정책 개체)를 만들고, 배포 하 고, 삭제 하 고, 요청 (일반적으로 편집자의)을 승인 또는 거부 하 여 Gpo를 만들거나 배포 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e388-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="9e388-105">**중요**  Gpo의 중앙 보관 파일에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e388-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="9e388-106">자세한 내용은 [AGPM 서버 연결 구성을](configure-an-agpm-server-connection-agpm40.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e388-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="9e388-107">보류 중인 작업 승인 또는 거부</span><span class="sxs-lookup"><span data-stu-id="9e388-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm40.md)

-   [<span data-ttu-id="9e388-108">GPO 만들기 또는 제어</span><span class="sxs-lookup"><span data-stu-id="9e388-108">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

-   [<span data-ttu-id="9e388-109">GPO 체크 인</span><span class="sxs-lookup"><span data-stu-id="9e388-109">Check In a GPO</span></span>](check-in-a-gpo-agpm40.md)

-   [<span data-ttu-id="9e388-110">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="9e388-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="9e388-111">이전 버전의 GPO로 롤백</span><span class="sxs-lookup"><span data-stu-id="9e388-111">Roll Back to an Earlier Version of a GPO</span></span>](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="9e388-112">GPO 삭제, 복원 또는 destroy</span><span class="sxs-lookup"><span data-stu-id="9e388-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

<span data-ttu-id="9e388-113">**참고**  GPO를 승인 하기 전에 승인자는 포함 된 정책 설정을 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e388-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="9e388-114">승인자 역할에는 검토자 역할에 대 한 사용 권한이 포함 되므로 승인자는 정책 설정을 검토 하 고 Gpo를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e388-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="9e388-115">자세한 내용은 [검토자 작업 수행](performing-reviewer-tasks-agpm40.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e388-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="9e388-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="9e388-116">Additional considerations</span></span>

<span data-ttu-id="9e388-117">기본적으로 승인자 역할에는 다음 사용 권한이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e388-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="9e388-118">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="9e388-118">List Contents</span></span>

-   <span data-ttu-id="9e388-119">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="9e388-119">Read Settings</span></span>

-   <span data-ttu-id="9e388-120">GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="9e388-120">Create GPO</span></span>

-   <span data-ttu-id="9e388-121">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="9e388-121">Deploy GPO</span></span>

-   <span data-ttu-id="9e388-122">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="9e388-122">Delete GPO</span></span>

<span data-ttu-id="9e388-123">또한 승인자는 자신이 만들었거나 제어 하는 Gpo에 대해 모든 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9e388-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





