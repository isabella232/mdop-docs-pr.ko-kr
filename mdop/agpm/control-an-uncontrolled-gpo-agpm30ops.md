---
title: 제어되지 않은 GPO 제어
description: 제어되지 않은 GPO 제어
author: dansimp
ms.assetid: 603f00f9-1e65-4b2f-902a-e53dafedbd8d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 904c3f76ce89f3814b739ee958fc14198899fb14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818883"
---
# <span data-ttu-id="59238-103">제어되지 않은 GPO 제어</span><span class="sxs-lookup"><span data-stu-id="59238-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="59238-104">GPO (그룹 정책 개체)에 대 한 변경 제어권을 제공 하려면 먼저 GPO를 제어 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="59238-105">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)의 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="59238-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="59238-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="59238-107">미제어 GPO를 제어 하려면</span><span class="sxs-lookup"><span data-stu-id="59238-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="59238-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="59238-109">세부 정보 창의 **내용** 탭에서 **미제어** 탭을 클릭 하 여 제어 되지 않은 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="59238-110">AGPM을 사용 하 여 제어할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **Control**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="59238-111">GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="59238-112">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="59238-113">**미제어** 탭의 목록에서 GPO가 제거 되 고 **제어** 탭에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59238-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="59238-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="59238-114">Additional considerations</span></span>

-   <span data-ttu-id="59238-115">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="59238-116">특히, 도메인에 대 한 **목록 콘텐츠** 및 **GPO 만들기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="59238-117">추가 참조</span><span class="sxs-lookup"><span data-stu-id="59238-117">Additional references</span></span>

-   [<span data-ttu-id="59238-118">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="59238-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 




