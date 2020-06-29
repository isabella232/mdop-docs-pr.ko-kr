---
title: 오프라인에서 GPO 편집
description: 오프라인에서 GPO 편집
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820888"
---
# <span data-ttu-id="e127d-103">오프라인에서 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="e127d-103">Edit a GPO Offline</span></span>


<span data-ttu-id="e127d-104">제어 된 GPO (그룹 정책 개체)를 변경 하려면 먼저 보관 저장소에서 GPO 복사본을 체크 아웃 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-104">To make changes to a controlled Group Policy object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="e127d-105">다른 사용자는 다시 체크 인 될 때까지 GPO를 수정 하 여 여러 그룹 정책 관리자가 충돌 하는 변경 내용을 적용 하지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="e127d-106">GPO 수정이 완료 되 면 보관 저장소에 체크 하 여 프로덕션 환경에 검토 하 고 배포할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-106">When you have finished modifying the GPO, you check it into the archive, so it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="e127d-107">이 절차를 완료 하려면 편집기나 AGPM 관리자 (모든 권한) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 고급 그룹 정책 관리에서 필요한 사용 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="e127d-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="e127d-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="e127d-109">오프 라인으로 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="e127d-109">Editing a GPO offline</span></span>


<span data-ttu-id="e127d-110">GPO를 편집 하려면 보관 파일에서 GPO를 체크 아웃 하 고, gpo를 오프 라인으로 편집한 다음, 해당 GPO를 검토 및 배포 (또는 다른 편집기에서 수정) 할 수 있도록 저장소에 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive, so it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="e127d-111">GPO 체크 아웃</span><span class="sxs-lookup"><span data-stu-id="e127d-111">Check out a GPO</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="e127d-112">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="e127d-112">Edit a GPO</span></span>](#bkmk-edit)

-   [<span data-ttu-id="e127d-113">GPO 체크 인</span><span class="sxs-lookup"><span data-stu-id="e127d-113">Check in a GPO</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="e127d-114">편집을 위해 아카이브에 대해 GPO를 체크 아웃 하려면</span><span class="sxs-lookup"><span data-stu-id="e127d-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="e127d-115">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e127d-116">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-116">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e127d-117">편집할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="e127d-118">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-118">Type a comment to be displayed in the History of the GPO while it is checked out, then click **OK**.</span></span>

5.  <span data-ttu-id="e127d-119">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e127d-120">이제 **제어** 탭에서 GPO 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="e127d-121">오프 라인으로 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="e127d-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="e127d-122">**제어** 탭에서 편집할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="e127d-123">**그룹 정책 개체 편집기**에서 GPO의 오프 라인 복사본을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-123">In the **Group Policy Object Editor**, make changes to an offline copy of the GPO.</span></span>

3.  <span data-ttu-id="e127d-124">GPO 수정을 마쳤으면 **그룹 정책 개체 편집기**를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-124">When you have finished modifying the GPO, close the **Group Policy Object Editor**.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="e127d-125">GPO를 보관 함으로 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="e127d-125">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="e127d-126">**제어** 탭에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-126">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="e127d-127">GPO를 변경 하지 않은 경우 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크 아웃 취소**를 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-127">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="e127d-128">GPO를 변경한 경우 GPO를 마우스 오른쪽 단추로 클릭 하 고 **체크 인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-128">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="e127d-129">GPO의 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-129">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="e127d-130">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-130">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e127d-131">**제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-131">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="e127d-132">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="e127d-132">Additional considerations</span></span>

-   <span data-ttu-id="e127d-133">GPO를 체크 아웃 하 고 편집 하려면 기본적으로 GPO, 편집기 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-133">To check out and edit a GPO, by default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="e127d-134">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-134">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="e127d-135">또한 GPO를 편집 하려면 해당 GPO를 체크 아웃 한 개인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-135">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="e127d-136">GPO를 체크 인하려면 기본적으로 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-136">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="e127d-137">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 또는 **gpo 배포** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-137">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="e127d-138">승인자 또는 AGPM 관리자 (또는 **GPO 배포** 권한이 있는 다른 그룹 정책 관리자)가 아닌 경우 gpo를 체크 아웃 한 편집기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-138">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="e127d-139">GPO를 편집할 때 다른 GPO에 있는 패키지의 그룹 정책 소프트웨어 설치 업그레이드는 체크 아웃 된 복사본이 아닌 배포 된 GPO를 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e127d-139">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, not the checked-out copy.</span></span>

### <span data-ttu-id="e127d-140">추가 참조</span><span class="sxs-lookup"><span data-stu-id="e127d-140">Additional references</span></span>

-   [<span data-ttu-id="e127d-141">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="e127d-141">Editing a GPO</span></span>](editing-a-gpo.md)

-   <span data-ttu-id="e127d-142">GPO 검토</span><span class="sxs-lookup"><span data-stu-id="e127d-142">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="e127d-143">GPO 설정 검토</span><span class="sxs-lookup"><span data-stu-id="e127d-143">Review GPO Settings</span></span>](review-gpo-settings.md)

    -   [<span data-ttu-id="e127d-144">GPO 링크 검토</span><span class="sxs-lookup"><span data-stu-id="e127d-144">Review GPO Links</span></span>](review-gpo-links.md)

    -   [<span data-ttu-id="e127d-145">GPO, GPO 버전 또는 템플릿 간의 차이점 식별</span><span class="sxs-lookup"><span data-stu-id="e127d-145">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   <span data-ttu-id="e127d-146">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="e127d-146">Deploying a GPO</span></span>

    -   [<span data-ttu-id="e127d-147">GPO의 배포 요청</span><span class="sxs-lookup"><span data-stu-id="e127d-147">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo.md)

    -   [<span data-ttu-id="e127d-148">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="e127d-148">Deploy a GPO</span></span>](deploy-a-gpo.md)

 

 





