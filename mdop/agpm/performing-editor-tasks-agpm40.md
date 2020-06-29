---
title: 편집기 작업 수행
description: 편집기 작업 수행
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820408"
---
# <span data-ttu-id="c5378-103">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="c5378-103">Performing Editor Tasks</span></span>


<span data-ttu-id="c5378-104">AGPM (고급 그룹 정책 관리)에서 편집기는 AGPM 관리자가 권한을 부여한 사람으로, Gpo (그룹 정책 개체)를 변경 하 고 GPO 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="c5378-105">또한, 편집자는 GPO를 만들거나, 삭제 하거나, 복원 하도록 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="c5378-106">승인자는 구현 요청을 승인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="c5378-107">편집자는 GPO를 파일로 내보내 다른 포리스트의 도메인에 복사 하 고 다른 도메인에서 복사한 GPO를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="c5378-108">**중요**  Gpo의 중앙 보관 파일에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="c5378-109">자세한 내용은 [AGPM 서버 연결 구성을](configure-an-agpm-server-connection-agpm40.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5378-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="c5378-110">GPO 만들기 또는 제어</span><span class="sxs-lookup"><span data-stu-id="c5378-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="c5378-111">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="c5378-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="c5378-112">테스트 환경 사용</span><span class="sxs-lookup"><span data-stu-id="c5378-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="c5378-113">GPO의 배포 요청</span><span class="sxs-lookup"><span data-stu-id="c5378-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="c5378-114">템플릿 만들기 및 기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="c5378-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="c5378-115">GPO 삭제 또는 복원</span><span class="sxs-lookup"><span data-stu-id="c5378-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="c5378-116">**참고**  편집자 역할에는 검토자 역할에 대 한 사용 권한이 포함 되므로, 편집자는 설정을 검토 하 고 Gpo를 비교할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="c5378-117">자세한 내용은 [검토자 작업 수행](performing-reviewer-tasks-agpm40.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5378-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="c5378-118">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="c5378-118">Additional considerations</span></span>

<span data-ttu-id="c5378-119">기본적으로 편집자 역할에 대해 다음 권한이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5378-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="c5378-120">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="c5378-120">List Contents</span></span>

-   <span data-ttu-id="c5378-121">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="c5378-121">Read Settings</span></span>

-   <span data-ttu-id="c5378-122">설정 편집</span><span class="sxs-lookup"><span data-stu-id="c5378-122">Edit Settings</span></span>

-   <span data-ttu-id="c5378-123">GPO 내보내기</span><span class="sxs-lookup"><span data-stu-id="c5378-123">Export GPO</span></span>

-   <span data-ttu-id="c5378-124">GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5378-124">Import GPO</span></span>

-   <span data-ttu-id="c5378-125">서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="c5378-125">Create Template</span></span>

 

 





