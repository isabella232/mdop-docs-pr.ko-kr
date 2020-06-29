---
title: 오프라인에서 GPO 편집
description: 오프라인에서 GPO 편집
author: dansimp
ms.assetid: 9c75eb3c-d4d5-41e0-b65e-8b4464a42cd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7ba0f72d7bfa8e2c597f62f7675a754807525ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820893"
---
# <span data-ttu-id="05d9d-103">오프라인에서 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="05d9d-103">Edit a GPO Offline</span></span>


<span data-ttu-id="05d9d-104">제어 된 GPO (그룹 정책 개체)를 변경 하려면 먼저 보관 저장소에서 GPO 복사본을 체크 아웃 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-104">To make changes to a controlled Group Policy Object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="05d9d-105">다른 사용자는 다시 체크 인 될 때까지 GPO를 수정 하 여 여러 그룹 정책 관리자가 충돌 하는 변경 내용을 적용 하지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="05d9d-106">GPO 수정을 완료 하면 프로덕션 환경에 검토 하 고 배포할 수 있도록 보관 저장소에 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-106">When you have finished modifying the GPO, you check it into the archive so that it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="05d9d-107">이 절차를 완료 하려면 편집기 또는 AGPM 관리자 (모든 권한) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 AGPM (고급 그룹 정책 관리)에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="05d9d-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="05d9d-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="05d9d-109">오프 라인으로 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="05d9d-109">Editing a GPO offline</span></span>


<span data-ttu-id="05d9d-110">GPO를 편집 하려면 보관 파일에서 GPO를 체크 아웃 하 고, gpo를 오프 라인으로 편집한 다음, 해당 GPO를 검토 및 배포 하거나 다른 편집기에서 수정할 수 있도록 보관 저장소에 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive so that it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="05d9d-111">편집을 위해 아카이브에 대해 GPO 체크 아웃</span><span class="sxs-lookup"><span data-stu-id="05d9d-111">Check out a GPO from the archive for editing</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="05d9d-112">오프 라인으로 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="05d9d-112">Edit a GPO offline</span></span>](#bkmk-edit)

-   [<span data-ttu-id="05d9d-113">보관 함에 있는 GPO 확인</span><span class="sxs-lookup"><span data-stu-id="05d9d-113">Check a GPO into the archive</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="05d9d-114">편집을 위해 아카이브에 대해 GPO를 체크 아웃 하려면</span><span class="sxs-lookup"><span data-stu-id="05d9d-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="05d9d-115">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="05d9d-116">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="05d9d-117">편집할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="05d9d-118">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-118">Type a comment to be displayed in the History of the GPO while it is checked out, and then click **OK**.</span></span>

5.  <span data-ttu-id="05d9d-119">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05d9d-120">이제 **제어** 탭에서 GPO 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="05d9d-121">오프 라인으로 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="05d9d-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="05d9d-122">**제어** 탭에서 편집할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="05d9d-123">**그룹 정책 관리 편집기** 창에서 GPO의 오프 라인 복사본을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-123">In the **Group Policy Management Editor** window, make changes to an offline copy of the GPO.</span></span>

    <span data-ttu-id="05d9d-124">**참고**  모든 컴퓨터 구성 설정 또는 모든 사용자 구성 설정을 사용 하지 않도록 설정 하려면 **그룹 정책 관리 편집기** 창에서 GPO를 마우스 오른쪽 단추로 클릭 하 고 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-124">**Note** To disable all Computer Configuration settings or all User Configuration settings, right-click the GPO in the **Group Policy Management Editor** window and click **Properties**.</span></span> <span data-ttu-id="05d9d-125">**컴퓨터 구성 설정 사용 안 함을** 선택 하거나 필요에 따라 **사용자 구성 설정을 사용 하지 않도록** 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-125">Select **Disable Computer Configuration settings** or **Disable User Configuration settings** as appropriate.</span></span>

     

3.  <span data-ttu-id="05d9d-126">GPO 수정을 마쳤으면 **그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-126">When you have finished modifying the GPO, close the **Group Policy Management Editor** window.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="05d9d-127">GPO를 보관 함으로 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="05d9d-127">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="05d9d-128">**제어** 탭에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-128">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="05d9d-129">GPO를 변경 하지 않은 경우 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크 아웃 취소**를 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-129">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="05d9d-130">GPO를 변경한 경우 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크 인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-130">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="05d9d-131">GPO의 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-131">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="05d9d-132">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-132">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05d9d-133">**제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-133">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="05d9d-134">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="05d9d-134">Additional considerations</span></span>

-   <span data-ttu-id="05d9d-135">GPO를 체크 아웃 하 고 편집 하려면 기본적으로 GPO, 편집기 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-135">To check out and edit a GPO, by default you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="05d9d-136">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-136">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="05d9d-137">또한 GPO를 편집 하려면 해당 GPO를 체크 아웃 한 개인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-137">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="05d9d-138">GPO를 체크 인하려면 기본적으로 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-138">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="05d9d-139">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 또는 **gpo 배포** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-139">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="05d9d-140">승인자 또는 AGPM 관리자 (또는 **GPO 배포** 권한이 있는 다른 그룹 정책 관리자)가 아닌 경우 gpo를 체크 아웃 한 편집기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-140">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="05d9d-141">GPO를 편집할 때 다른 GPO에 있는 패키지의 그룹 정책 소프트웨어 설치 업그레이드는 체크 아웃 된 복사본이 아니라 배포 된 GPO를 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05d9d-141">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, and not the checked-out copy.</span></span>

### <span data-ttu-id="05d9d-142">추가 참조</span><span class="sxs-lookup"><span data-stu-id="05d9d-142">Additional references</span></span>

-   [<span data-ttu-id="05d9d-143">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="05d9d-143">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   <span data-ttu-id="05d9d-144">GPO 검토</span><span class="sxs-lookup"><span data-stu-id="05d9d-144">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="05d9d-145">GPO 설정 검토</span><span class="sxs-lookup"><span data-stu-id="05d9d-145">Review GPO Settings</span></span>](review-gpo-settings-agpm40.md)

    -   [<span data-ttu-id="05d9d-146">GPO 링크 검토</span><span class="sxs-lookup"><span data-stu-id="05d9d-146">Review GPO Links</span></span>](review-gpo-links-agpm40.md)

    -   [<span data-ttu-id="05d9d-147">GPO, GPO 버전 또는 템플릿 간의 차이점 식별</span><span class="sxs-lookup"><span data-stu-id="05d9d-147">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md)

-   <span data-ttu-id="05d9d-148">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="05d9d-148">Deploying a GPO</span></span>

    -   [<span data-ttu-id="05d9d-149">GPO의 배포 요청</span><span class="sxs-lookup"><span data-stu-id="05d9d-149">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

    -   [<span data-ttu-id="05d9d-150">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="05d9d-150">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

 

 





