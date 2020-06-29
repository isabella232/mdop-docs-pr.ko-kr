---
title: 파일에서 GPO 가져오기
description: 파일에서 GPO 가져오기
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820753"
---
# <span data-ttu-id="5b984-103">파일에서 GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b984-103">Import a GPO from a File</span></span>


<span data-ttu-id="5b984-104">AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한)를 사용 하 고 그룹 정책 개체 (GPO)를 CAB 파일로 내보낸 경우 해당 GPO의 정책 설정을 다른 포리스트의 도메인에 있는 새 gpo 또는 기존 GPO로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="5b984-105">GPO 설정을 CAB 파일로 내보내는 방법에 대 한 자세한 내용은 [파일로 Gpo 내보내기를](export-a-gpo-to-a-file.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b984-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="5b984-106">Agpm 관리자 역할 또는 AGPM의 필요한 권한이 있는 사용자 계정이 정책 설정을 새 제어 된 GPO로 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="5b984-107">정책 설정을 기존 GPO로 가져오려면 AGPM 또는 AGPM 관리자 역할이 있는 사용자 계정이 나 필요한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="5b984-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b984-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="5b984-109">파일에서 정책 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b984-109">Importing policy settings from a file</span></span>


<span data-ttu-id="5b984-110">파일에서 정책 설정을 가져올 때 새 GPO 또는 기존 GPO로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="5b984-111">그러나 정책 설정을 기존 GPO로 가져오면 그 안의 모든 정책 설정이 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="5b984-112">새 제어 GPO로 정책 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b984-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="5b984-113">기존 GPO로 정책 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b984-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="5b984-114">정책 설정을 새 제어 된 GPO로 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b984-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="5b984-115">**그룹 정책 관리 콘솔** 트리에서 정책 설정을 가져올 도메인의 **제어권 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="5b984-116">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="5b984-117">새로운 제어 된 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-117">Create a new controlled GPO.</span></span> <span data-ttu-id="5b984-118">**새 제어 된 GPO** 대화 상자에서 **가져오기를** 클릭 한 다음 **마법사 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="5b984-119">GPO를 만드는 방법에 대 한 자세한 내용은 제어 되 [는 새 GPO 만들기](create-a-new-controlled-gpo-agpm40.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b984-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="5b984-120">**설정 가져오기 마법사** 의 지침에 따라 GPO 백업을 선택 하 고 새 gpo에 대 한 정책 설정을 가져오고 새 gpo의 감사 추적에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="5b984-121">기존 GPO로 정책 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b984-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="5b984-122">**그룹 정책 관리 콘솔** 트리에서 정책 설정을 가져올 도메인의 **제어권 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="5b984-123">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="5b984-124">정책 설정을 가져올 대상 GPO를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="5b984-125">대상 GPO를 마우스 오른쪽 단추로 클릭 하 고 **가져올 원본**위치를 가리킨 다음 **파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="5b984-126">**설정 가져오기 마법사** 의 지침에 따라 GPO 백업을 선택 하 고, 대상 gpo의 정책 설정을 가져오고, 대상 gpo의 감사 추적에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="5b984-127">마법사가 완료 되 면 기본적으로 대상 GPO가 체크 인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="5b984-128">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="5b984-128">Additional considerations</span></span>

-   <span data-ttu-id="5b984-129">정책 설정을 새 관리 되는 GPO로 가져오려면 해당 도메인에 대 한 **콘텐츠 목록**, **GPO 가져오기**, **gpo 만들기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="5b984-130">기본적으로이 절차를 수행 하려면 AGPM 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="5b984-131">기존 GPO로 정책 설정을 가져오려면 도메인에 대 한 **목록 내용**, **설정 편집**, **GPO 가져오기** 권한이 있어야 하며 gpo는 사용자가 체크 아웃 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="5b984-132">이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b984-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="5b984-133">추가 참조</span><span class="sxs-lookup"><span data-stu-id="5b984-133">Additional references</span></span>

-   [<span data-ttu-id="5b984-134">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="5b984-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





