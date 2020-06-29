---
title: 새 제어된 GPO 만들기
description: 새 제어된 GPO 만들기
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821093"
---
# <span data-ttu-id="11995-103">새 제어된 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="11995-103">Create a New Controlled GPO</span></span>


<span data-ttu-id="11995-104">**변경 제어** 노드를 통해 만든 새 Gpo (그룹 정책 개체)가 자동으로 제어 되므로 사용자가 AGPM (고급 그룹 정책 관리)을 사용 하 여 관리 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11995-104">New Group Policy objects (GPOs) created through the **Change Control** node will automatically be controlled, enabling you to manage them with Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="11995-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="11995-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="11995-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="11995-107">AGPM을 통해 변경 제어가 관리 되는 새 GPO를 만들려면</span><span class="sxs-lookup"><span data-stu-id="11995-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="11995-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="11995-109">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-109">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="11995-110">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-110">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="11995-111">새 GPO의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-111">Type a name for the new GPO.</span></span>

    2.  <span data-ttu-id="11995-112">선택 사항: GPO에 대 한 **기록** 에 표시할 새 gpo에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-112">Optional: Type a comment for the new GPO to be displayed in the **History** for the GPO.</span></span>

    3.  <span data-ttu-id="11995-113">새 GPO를 즉시 프로덕션 환경에 배포 하려면 **라이브 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-113">To immediately deploy the new GPO to the production environment, click **Create live**.</span></span> <span data-ttu-id="11995-114">새 GPO를 즉시 배포 하지 않고 오프 라인으로 만들려면 **오프 라인으로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-114">To create the new GPO offline without immediately deploying it, click **Create offline**.</span></span>

    4.  <span data-ttu-id="11995-115">새 GPO의 시작 점으로 사용할 GPO 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-115">Select the GPO template to use as a starting point for the new GPO.</span></span>

    5.  <span data-ttu-id="11995-116">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-116">Click **OK**.</span></span>

4.  <span data-ttu-id="11995-117">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-117">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="11995-118">**제어** 탭의 gpo 목록에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11995-118">The new GPO is displayed in the list of GPOs on the **Controlled** tab.</span></span>

### <span data-ttu-id="11995-119">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="11995-119">Additional considerations</span></span>

-   <span data-ttu-id="11995-120">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-120">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="11995-121">특히, 도메인에 대 한 **목록 콘텐츠** 및 **GPO 만들기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11995-121">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="11995-122">추가 참조</span><span class="sxs-lookup"><span data-stu-id="11995-122">Additional references</span></span>

-   [<span data-ttu-id="11995-123">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="11995-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





