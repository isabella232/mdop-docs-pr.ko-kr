---
title: 편집기 작업 수행
description: 편집기 작업 수행
author: dansimp
ms.assetid: d4ac3277-2557-41cf-ac90-5adb6c30687c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e70a56ff01313e3b502ebde5bb486ec18db60643
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820398"
---
# <span data-ttu-id="aab5b-103">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="aab5b-103">Performing Editor Tasks</span></span>


<span data-ttu-id="aab5b-104">편집자는 사용자가 AGPM 관리자 (모든 권한)가 승인 하 여 그룹 정책 개체 (Gpo)를 변경 하 고 GPO 템플릿을 만들 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab5b-104">An Editor is a person authorized by an AGPM Administrator (Full Control) to make changes to Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="aab5b-105">또한, 편집자는 GPO를 만들거나, 삭제 하거나, 복원 하는 프로세스를 시작할 수 있지만 기본적으로 승인자의 승인을 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab5b-105">Additionally, an Editor can initiate the process of creating, deleting, or restoring a GPO, but by default must request approval from an Approver.</span></span>

<span data-ttu-id="aab5b-106">**중요**  Gpo의 중앙 보관 파일에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab5b-106">**Important** Ensure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="aab5b-107">자세한 내용은 [AGPM 서버 연결 구성을](configure-an-agpm-server-connection-reviewer-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab5b-107">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

 

-   [<span data-ttu-id="aab5b-108">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="aab5b-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="aab5b-109">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="aab5b-109">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="aab5b-110">템플릿 만들기 및 기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="aab5b-110">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [<span data-ttu-id="aab5b-111">GPO 삭제 또는 복원</span><span class="sxs-lookup"><span data-stu-id="aab5b-111">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm30ops.md)

<span data-ttu-id="aab5b-112">**참고**  편집자 역할에는 검토자 역할에 대 한 사용 권한이 포함 되므로, 편집자는 설정을 검토 하 고 Gpo를 비교할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab5b-112">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="aab5b-113">자세한 내용은 [검토자 작업 수행](performing-reviewer-tasks-agpm30ops.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab5b-113">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md) for more information.</span></span>

 

### <span data-ttu-id="aab5b-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="aab5b-114">Additional considerations</span></span>

<span data-ttu-id="aab5b-115">기본적으로 편집자 역할에 대해 다음 권한이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aab5b-115">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="aab5b-116">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="aab5b-116">List Contents</span></span>

-   <span data-ttu-id="aab5b-117">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="aab5b-117">Read Settings</span></span>

-   <span data-ttu-id="aab5b-118">설정 편집</span><span class="sxs-lookup"><span data-stu-id="aab5b-118">Edit Settings</span></span>

-   <span data-ttu-id="aab5b-119">서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="aab5b-119">Create Template</span></span>

 

 





