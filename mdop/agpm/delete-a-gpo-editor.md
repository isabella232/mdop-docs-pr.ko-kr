---
title: GPO 삭제
description: GPO 삭제
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820973"
---
# <span data-ttu-id="01ee2-103">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="01ee2-103">Delete a GPO</span></span>


<span data-ttu-id="01ee2-104">편집자는 GPO (그룹 정책 개체) 삭제를 완료 하기 위한 권한이 없을 수 있지만 프로세스를 시작 하 고 요청을 승인자에 게 제출 하는 데 필요한 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-104">As an Editor, you may not have permission to complete the deletion of a Group Policy object (GPO), but you do have the permission necessary to begin the process and submit your request to an Approver.</span></span>

<span data-ttu-id="01ee2-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집자 역할이 있거나 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="01ee2-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="01ee2-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="01ee2-107">제어 된 GPO의 삭제를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="01ee2-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="01ee2-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="01ee2-109">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="01ee2-110">삭제할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="01ee2-111">배포 된 버전의 GPO를 프로덕션 환경에 그대로 유지 하면서 보관 파일에서 GPO를 삭제 하려면 **보관 시에만 Gpo 삭제 (제어**되지 않음)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="01ee2-112">보관 및 프로덕션 환경에서 모두 GPO를 삭제 하려면 **보관 및 프로덕션에서 Gpo 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

        <span data-ttu-id="01ee2-113">Gpo를 삭제할 특별 한 권한이 없는 경우에는 배포 된 GPO 삭제 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="01ee2-114">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="01ee2-115">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

4.  <span data-ttu-id="01ee2-116">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="01ee2-117">GPO가 **보류** 탭의 gpo 목록에 표시 됩니다. 승인자가 요청을 승인 하면 **보류 중** 탭에서 **휴지통** 탭으로 GPO가 이동 되며,이 위치는 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="01ee2-118">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="01ee2-118">Additional considerations</span></span>

-   <span data-ttu-id="01ee2-119">기본적으로 배포 된 GPO의 삭제를 요청 하려면 편집자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-119">By default, you must be an Editor to request the deletion of a deployed GPO.</span></span> <span data-ttu-id="01ee2-120">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="01ee2-121">기본적으로 저장소에서 GPO를 삭제 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-121">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="01ee2-122">특히, GPO에 대 한 **목록 내용이** 있고 **설정을 편집** 하거나 **gpo** 사용 권한을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-122">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="01ee2-123">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-123">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="01ee2-124">GPO가 **제어** 탭으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-124">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="01ee2-125">관리 되지 않는 GPO를 먼저 제어 하지 않고 프로덕션 환경에서 삭제 하려면 **그룹 정책 관리 콘솔**에서 **포리스트**, **도메인**을 차례로 클릭 하 고 \*\* &lt; MyDomain &gt; \*\*을 클릭 한 다음 **그룹 정책 개체**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-125">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="01ee2-126">미제어 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ee2-126">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="01ee2-127">추가 참조</span><span class="sxs-lookup"><span data-stu-id="01ee2-127">Additional references</span></span>

-   [<span data-ttu-id="01ee2-128">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="01ee2-128">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

 

 





