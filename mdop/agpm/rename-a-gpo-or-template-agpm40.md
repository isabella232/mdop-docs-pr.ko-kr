---
title: GPO 또는 템플릿 이름 변경
description: GPO 또는 템플릿 이름 변경
author: dansimp
ms.assetid: 84293f7a-4ff7-497e-bdbc-cabb70189a03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 642622ae0242e614733e8f33ea5840c8b6758db8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818513"
---
# <span data-ttu-id="58150-103">GPO 또는 템플릿 이름 변경</span><span class="sxs-lookup"><span data-stu-id="58150-103">Rename a GPO or Template</span></span>


<span data-ttu-id="58150-104">제어 된 GPO (그룹 정책 개체) 또는 템플릿의 이름을 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58150-104">You can rename a controlled Group Policy Object (GPO) or a template.</span></span>

<span data-ttu-id="58150-105">이 절차를 완료 하려면 편집기 또는 AGPM 관리자 (모든 권한) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 AGPM (고급 그룹 정책 관리)에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="58150-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="58150-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="58150-107">GPO 또는 서식 파일의 이름을 바꾸려면</span><span class="sxs-lookup"><span data-stu-id="58150-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="58150-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="58150-109">**콘텐츠** 탭에서 **제어** 또는 **서식 파일** 탭을 클릭 하 여 이름을 바꿀 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="58150-110">이름을 바꿀 GPO 또는 템플릿을 마우스 오른쪽 단추로 클릭 하 고 **이름 바꾸기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="58150-111">GPO 또는 서식 파일과 메모의 새 이름을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-111">Type the new name for the GPO or template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="58150-112">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="58150-113">GPO 또는 템플릿이 **콘텐츠** 탭의 새 이름 아래에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="58150-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="58150-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="58150-114">Additional considerations</span></span>

-   <span data-ttu-id="58150-115">기본적으로이 절차를 수행 하려면 GPO, 편집기 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="58150-116">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58150-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="58150-117">배포 된 GPO의 이름을 바꾸면 보관 저장소에서 이름이 즉시 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58150-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="58150-118">이 이름은 GPO를 다시 배포 하는 경우에만 프로덕션 환경에서 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58150-118">The name is changed in the production environment only when the GPO is redeployed.</span></span> <span data-ttu-id="58150-119">GPO를 다시 배포 하거나 (프로덕션 복사본이 삭제 될 때까지) 이전 이름은 여전히 프로덕션 환경에서 사용 되 고 있으므로 다른 GPO에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58150-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="58150-120">마찬가지로, 보관 저장소의 GPO는 GPO를 배포 (프로덕션 복사본의 이름 변경) 하거나 프로덕션 복사본을 삭제 한 후에 다시 원래 이름으로 바꿀 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58150-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="58150-121">추가 참조</span><span class="sxs-lookup"><span data-stu-id="58150-121">Additional references</span></span>

-   [<span data-ttu-id="58150-122">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="58150-122">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

 

 





