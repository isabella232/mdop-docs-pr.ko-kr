---
title: 저장된 GPO 버전 제한
description: 저장된 GPO 버전 제한
author: dansimp
ms.assetid: d802c7b6-f303-4b23-aefd-f19f1300b0ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: df6f6df2e2b1bae2cd972b67b76c27905622a723
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820618"
---
# <span data-ttu-id="104c6-103">저장된 GPO 버전 제한</span><span class="sxs-lookup"><span data-stu-id="104c6-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="104c6-104">기본적으로 제어 되는 모든 GPO (그룹 정책 개체)의 모든 버전이 AGPM 서버의 보관 저장소에 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="104c6-105">그러나 각 GPO에 대해 보존 되는 버전 수를 제한 하 고 해당 제한이 초과 되는 경우 이전 버전을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="104c6-106">GPO 버전이 삭제 되 면 버전 레코드가 GPO의 기록에 남아 있지만 GPO 버전 자체는 보관 저장소에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="104c6-107">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="104c6-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="104c6-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="104c6-109">저장 된 GPO 버전 수를 제한 하려면</span><span class="sxs-lookup"><span data-stu-id="104c6-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="104c6-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="104c6-111">세부 정보 창에서 **AGPM 서버** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="104c6-112">**보관 파일에서 이전 버전의 Gpo 삭제** 확인란을 선택 하 고, 현재 버전을 제외한 각 gpo에 대해 저장할 최대 gpo 버전 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="104c6-113">현재 버전만 보존 하려면 0을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="104c6-114">최대값은 999 보다 크지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="104c6-115">**중요**  **기록** 창의 **고유 버전** 탭에 표시 되는 GPO 버전만이 제한에 따라 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="104c6-116">**적용** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="104c6-117">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="104c6-117">Additional considerations</span></span>

-   <span data-ttu-id="104c6-118">기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="104c6-119">특히 도메인에 대 한 **목록 콘텐츠** 및 **옵션 수정** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="104c6-120">기록에 삭제 되지 않도록 표시 하 여 GPO 버전이 삭제 되는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="104c6-121">이렇게 하려면 GPO 기록의 버전을 마우스 오른쪽 단추로 클릭 하 고 **삭제 안 함**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="104c6-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="104c6-122">추가 참조</span><span class="sxs-lookup"><span data-stu-id="104c6-122">Additional references</span></span>

-   [<span data-ttu-id="104c6-123">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="104c6-123">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





