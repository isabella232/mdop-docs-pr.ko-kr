---
title: 제어되지 않은 GPO의 제어 요청
description: 제어되지 않은 GPO의 제어 요청
author: dansimp
ms.assetid: a34e0aeb-33a1-4c9f-b187-1d08493a785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfccd7285f82990c2447319485738131cf559f48
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818448"
---
# <span data-ttu-id="77d62-103">제어되지 않은 GPO의 제어 요청</span><span class="sxs-lookup"><span data-stu-id="77d62-103">Request Control of an Uncontrolled GPO</span></span>


<span data-ttu-id="77d62-104">기존 GPO (그룹 정책 개체)에 대 한 변경 제어권을 제공 하려면 GPO를 제어 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-104">To provide change control for an existing Group Policy Object (GPO), the GPO must be controlled.</span></span> <span data-ttu-id="77d62-105">승인자 또는 AGPM 관리자 (모든 권한)가 아닌 경우 GPO를 제어 하도록 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="77d62-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기나 검토자 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="77d62-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="77d62-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="77d62-108">미제어 GPO를 제어 하려면</span><span class="sxs-lookup"><span data-stu-id="77d62-108">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="77d62-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="77d62-110">세부 정보 창의 **내용** 탭에서 **미제어** 탭을 클릭 하 여 제어 되지 않은 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="77d62-111">AGPM을 사용 하 여 제어할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **Control**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="77d62-112">Gpo를 제어할 수 있는 특별 한 권한이 없는 경우 제어권 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="77d62-113">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="77d62-114">GPO **기록** 에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="77d62-115">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="77d62-116">**제어** 되지 않은 탭의 목록에서 GPO가 제거 되 고 **보류 중** 탭에 추가 됩니다. 승인자가 요청을 승인 하면 GPO가 **제어** 탭으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="77d62-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="77d62-117">Additional considerations</span></span>

-   <span data-ttu-id="77d62-118">기본적으로이 절차를 수행 하려면 편집기나 검토자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="77d62-119">특히, 도메인에 대 한 **목록 내용** 및 **설정 읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="77d62-120">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="77d62-121">GPO가 **미제어** 탭으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77d62-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="77d62-122">추가 참조</span><span class="sxs-lookup"><span data-stu-id="77d62-122">Additional references</span></span>

-   [<span data-ttu-id="77d62-123">GPO 만들기 또는 제어</span><span class="sxs-lookup"><span data-stu-id="77d62-123">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





