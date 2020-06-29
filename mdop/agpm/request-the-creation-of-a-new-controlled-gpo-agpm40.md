---
title: 새 제어된 GPO 만들기 요청
description: 새 제어된 GPO 만들기 요청
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820318"
---
# <span data-ttu-id="772a5-103">새 제어된 GPO 만들기 요청</span><span class="sxs-lookup"><span data-stu-id="772a5-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="772a5-104">승인자 또는 AGPM 관리자 (모든 권한)가 아닌 경우 새 GPO (그룹 정책 개체) 만들기를 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="772a5-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기나 검토자 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="772a5-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="772a5-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="772a5-107">AGPM을 통해 변경 제어가 관리 되는 새 GPO를 만들려면</span><span class="sxs-lookup"><span data-stu-id="772a5-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="772a5-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="772a5-109">**변경 컨트롤**을 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="772a5-110">Gpo를 만들 수 있는 특별 한 권한이 없는 경우 생성 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="772a5-111">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="772a5-112">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="772a5-113">새 GPO의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="772a5-114">선택 사항: 새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="772a5-115">승인 즉시 새 GPO를 도메인의 프로덕션 환경에 배포 하려면 **라이브 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-115">To deploy the new GPO to the production environment of the domain immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="772a5-116">승인을 받을 때 새 GPO를 즉시 배포 하지 않고 오프 라인으로 만들려면 **오프 라인으로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="772a5-117">새 GPO의 시작 점으로 사용할 GPO 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="772a5-118">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="772a5-119">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="772a5-120">**보류** 탭의 gpo 목록에 새 GPO가 표시 됩니다. 승인자가 요청을 승인 하면 GPO가 **제어** 탭으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="772a5-121">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="772a5-121">Additional considerations</span></span>

-   <span data-ttu-id="772a5-122">기본적으로이 절차를 수행 하려면 편집기나 검토자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="772a5-123">특히, 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="772a5-124">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="772a5-125">GPO가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="772a5-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="772a5-126">추가 참조</span><span class="sxs-lookup"><span data-stu-id="772a5-126">Additional references</span></span>

-   [<span data-ttu-id="772a5-127">GPO 만들기 또는 제어</span><span class="sxs-lookup"><span data-stu-id="772a5-127">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





