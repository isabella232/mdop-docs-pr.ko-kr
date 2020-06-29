---
title: 새 제어된 GPO 만들기 요청
description: 새 제어된 GPO 만들기 요청
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820313"
---
# <span data-ttu-id="40843-103">새 제어된 GPO 만들기 요청</span><span class="sxs-lookup"><span data-stu-id="40843-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="40843-104">사용자가 승인자 또는 AGPM 관리자 (모든 권한)가 아닌 경우, 사용자가 AGPM (고급 그룹 정책 관리)을 사용 하 여 관리 되는 경우 새 GPO (그룹 정책 개체) 만들기를 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy object (GPO) if it is to be managed using Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="40843-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집기 또는 검토자 역할이 있거나 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="40843-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="40843-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="40843-107">AGPM을 통해 변경 제어가 관리 되는 새 GPO를 만들려면</span><span class="sxs-lookup"><span data-stu-id="40843-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="40843-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="40843-109">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-109">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="40843-110">Gpo를 만들 수 있는 특별 한 권한이 없는 경우 생성 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="40843-111">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="40843-112">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="40843-113">새 GPO의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="40843-114">선택 사항: 새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="40843-115">승인 즉시 새 GPO를 프로덕션 환경에 배포 하려면 **라이브 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-115">To deploy the new GPO to the production environment immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="40843-116">승인을 받을 때 새 GPO를 즉시 배포 하지 않고 오프 라인으로 만들려면 **오프 라인으로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="40843-117">새 GPO의 시작 점으로 사용할 GPO 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="40843-118">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="40843-119">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="40843-120">**보류** 탭의 gpo 목록에 새 GPO가 표시 됩니다. 승인자가 요청을 승인 하면 GPO가 **제어** 탭으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40843-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="40843-121">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="40843-121">Additional considerations</span></span>

-   <span data-ttu-id="40843-122">기본적으로이 절차를 수행 하려면 편집기나 검토자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="40843-123">특히, 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="40843-124">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="40843-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="40843-125">GPO가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40843-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="40843-126">추가 참조</span><span class="sxs-lookup"><span data-stu-id="40843-126">Additional references</span></span>

-   [<span data-ttu-id="40843-127">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="40843-127">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





