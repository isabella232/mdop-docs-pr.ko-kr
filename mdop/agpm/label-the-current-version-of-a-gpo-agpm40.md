---
title: GPO의 현재 버전의 레이블 지정
description: GPO의 현재 버전의 레이블 지정
author: dansimp
ms.assetid: cadc8769-21da-44b0-8122-6cafdb448913
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b15a4d3ee006fb37db4ce7362a2f5c92d7c233e5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820663"
---
# <span data-ttu-id="03977-103">GPO의 현재 버전의 레이블 지정</span><span class="sxs-lookup"><span data-stu-id="03977-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="03977-104">현재 버전의 GPO (그룹 정책 개체)에 레이블을 지정 하 여 해당 기록에서 쉽게 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03977-104">You can label the current version of a Group Policy Object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="03977-105">레이블을 사용 하 여 문제가 발생 하는 경우 롤백할 수 있는 알려진 양호한 버전을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03977-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="03977-106">또한 한 번에 동일한 레이블을 사용 하 여 여러 Gpo에 레이블을 지정 하 여 나중에 롤백이 필요한 경우 동일한 지점으로 롤백해야 하는 관련 Gpo를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03977-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="03977-107">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="03977-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="03977-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="03977-109">기록에서 현재 버전의 Gpo에 레이블을 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="03977-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="03977-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="03977-111">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="03977-112">현재 버전에 레이블을 지정 하려는 GPO를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="03977-113">여러 Gpo를 선택 하려면 SHIFT 키를 누르고 인접 한 Gpo 그룹의 마지막 GPO를 클릭 하거나 CTRL 키를 누른 상태로 개별 Gpo를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="03977-114">선택한 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **레이블을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="03977-115">선택한 각 GPO의 기록에 표시할 레이블과 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="03977-116">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="03977-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="03977-117">Additional considerations</span></span>

-   <span data-ttu-id="03977-118">기본적으로이 절차를 수행 하려면 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="03977-119">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 또는 **gpo 배포** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03977-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="03977-120">추가 참조</span><span class="sxs-lookup"><span data-stu-id="03977-120">Additional references</span></span>

-   [<span data-ttu-id="03977-121">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="03977-121">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

 

 





