---
title: GPO 링크 검토
description: GPO 링크 검토
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818348"
---
# <span data-ttu-id="d6d37-103">GPO 링크 검토</span><span class="sxs-lookup"><span data-stu-id="d6d37-103">Review GPO Links</span></span>


<span data-ttu-id="d6d37-104">선택한 GPO (그룹 정책 개체) 또는 gpo가 조직 구성 단위에 연결 된 위치를 표시 하는 다이어그램을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-104">You can display a diagram showing where a Group Policy Object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="d6d37-105">Gpo 연결 다이어그램은 GPO가 제어, 가져오기 또는 체크 인 될 때마다 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="d6d37-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에 대 한 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="d6d37-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6d37-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="d6d37-108">GPO 링크 검토</span><span class="sxs-lookup"><span data-stu-id="d6d37-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="d6d37-109">하나 이상의 Gpo</span><span class="sxs-lookup"><span data-stu-id="d6d37-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="d6d37-110">하나 이상의 GPO 버전</span><span class="sxs-lookup"><span data-stu-id="d6d37-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="d6d37-111">하나 이상의 Gpo에 대 한 GPO 링크를 표시 하려면</span><span class="sxs-lookup"><span data-stu-id="d6d37-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="d6d37-112">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d6d37-113">세부 정보 창의 **콘텐츠** 탭에서 **제어**됨, **보류 중**또는 **휴지통** 탭을 클릭 하 여 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="d6d37-114">링크를 표시할 하나 이상의 Gpo를 선택 하 고 선택한 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **설정을**클릭 하 고 **gpo 연결** 을 클릭 하 여 선택한 gpo에 대 한 링크가 있는 도메인 및 조직 구성 단위 다이어그램을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="d6d37-115">하나 이상의 GPO 버전에 대 한 GPO 링크를 표시 하려면</span><span class="sxs-lookup"><span data-stu-id="d6d37-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="d6d37-116">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d6d37-117">세부 정보 창의 **콘텐츠** 탭에서 **제어** 또는 **휴지통** 탭을 클릭 하 여 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="d6d37-118">해당 GPO를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="d6d37-119">설정을 검토할 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo 설정에 대 한 요약 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="d6d37-120">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d6d37-120">Additional considerations</span></span>

-   <span data-ttu-id="d6d37-121">이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d6d37-122">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="d6d37-123">또한 Gpo 목록을 표시 하려면 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6d37-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="d6d37-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="d6d37-124">Additional references</span></span>

-   [<span data-ttu-id="d6d37-125">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="d6d37-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





