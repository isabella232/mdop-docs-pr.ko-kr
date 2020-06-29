---
title: 이전 버전의 GPO로 롤백
description: 이전 버전의 GPO로 롤백
author: dansimp
ms.assetid: 028631c0-4cb9-4642-90ad-04cd813051b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a71740eaa60a4b1292e47ca8aa57d4657231ab57
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820283"
---
# <span data-ttu-id="740c6-103">이전 버전의 GPO로 롤백</span><span class="sxs-lookup"><span data-stu-id="740c6-103">Roll Back to a Previous Version of a GPO</span></span>


<span data-ttu-id="740c6-104">AGPM (고급 그룹 정책 관리)을 사용 하면 승인자가 이전 버전의 GPO를 기록에 다시 배포 하 여 GPO (그룹 정책 개체)의 변경 내용을 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-104">Advanced Group Policy Management (AGPM) enables an Approver to roll back changes to a Group Policy object (GPO) by redeploying an earlier version of the GPO from its history.</span></span> <span data-ttu-id="740c6-105">이전 버전의 GPO를 배포 하면 현재 프로덕션 중인 GPO 버전이 덮어써집니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-105">Deploying an earlier version of a GPO overwrites the version of the GPO currently in production.</span></span>

<span data-ttu-id="740c6-106">이 절차를 완료 하려면 고급 그룹 정책 관리에서 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="740c6-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="740c6-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="740c6-108">이전 버전의 GPO를 프로덕션 환경에 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="740c6-108">To deploy a previous version of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="740c6-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="740c6-110">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="740c6-111">배포할 GPO를 두 번 클릭 하 여 **기록을**표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-111">Double-click the GPO to be deployed to display its **History**.</span></span>

4.  <span data-ttu-id="740c6-112">배포할 버전을 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 한 다음 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-112">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

5.  <span data-ttu-id="740c6-113">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="740c6-114">**기록** 창에서 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-114">In the **History** window, click **Close**.</span></span>

<span data-ttu-id="740c6-115">**참고**  다시 배포 된 버전이 의도 한 버전과 일치 하는지 확인 하려면 두 버전의 차이점 보고서를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-115">**Note** To verify that the version that has been redeployed matches the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="740c6-116">GPO의 **기록** 창에서 두 버전을 강조 표시 한 다음 마우스 오른쪽 단추를 클릭 하 고 **차이점** 및 **HTML 보고서** 또는 **XML 보고서**중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-116">In the **History** window for the GPO, highlight the two versions, and then right-click and select **Difference** and either **HTML Report** or **XML Report**.</span></span>

 

### <span data-ttu-id="740c6-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="740c6-117">Additional considerations</span></span>

-   <span data-ttu-id="740c6-118">이 절차를 수행 하려면 기본적으로 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="740c6-119">특히 GPO에 대 한 **목록 콘텐츠** 및 **gpo** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="740c6-119">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="740c6-120">추가 참조</span><span class="sxs-lookup"><span data-stu-id="740c6-120">Additional references</span></span>

-   [<span data-ttu-id="740c6-121">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="740c6-121">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





