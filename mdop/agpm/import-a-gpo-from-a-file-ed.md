---
title: 파일에서 GPO 가져오기
description: 파일에서 GPO 가져오기
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820723"
---
# <span data-ttu-id="e07c0-103">파일에서 GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="e07c0-103">Import a GPO from a File</span></span>


<span data-ttu-id="e07c0-104">AGPM (고급 그룹 정책 관리)에서 GPO (그룹 정책 개체)를 CAB 파일로 내보낸 경우 해당 GPO의 정책 설정을 다른 포리스트의 도메인에 있는 기존 GPO로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="e07c0-105">정책 설정을 기존 GPO로 가져오면 해당 GPO 내의 모든 정책 설정이 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="e07c0-106">GPO 설정을 CAB 파일로 내보내는 방법에 대 한 자세한 내용은 [파일로 Gpo 내보내기를](export-a-gpo-to-a-file.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e07c0-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="e07c0-107">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="e07c0-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="e07c0-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="e07c0-109">기존 GPO로 정책 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="e07c0-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="e07c0-110">**그룹 정책 관리 콘솔** 트리에서 정책 설정을 가져올 도메인의 **제어권 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="e07c0-111">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e07c0-112">정책 설정을 가져올 대상 GPO를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="e07c0-113">대상 GPO를 마우스 오른쪽 단추로 클릭 하 고 **가져올 원본**위치를 가리킨 다음 **파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="e07c0-114">**설정 가져오기 마법사** 의 지침에 따라 GPO 백업을 선택 하 고, 대상 gpo의 정책 설정을 가져오고, 대상 gpo의 감사 추적에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="e07c0-115">마법사가 완료 되 면 기본적으로 대상 GPO가 체크 인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="e07c0-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="e07c0-116">Additional considerations</span></span>

-   <span data-ttu-id="e07c0-117">이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e07c0-118">특히 도메인에 대 한 **목록 내용**, **설정 편집**, **GPO 가져오기** 권한이 있어야 하며 gpo는 사용자가 체크 아웃 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="e07c0-119">편집기가 만드는 동안 정책 설정을 새 GPO로 가져올 수는 없지만, 편집기에서 새 GPO 만들기를 요청한 다음 만든 후에는 정책 설정을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07c0-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="e07c0-120">추가 참조</span><span class="sxs-lookup"><span data-stu-id="e07c0-120">Additional references</span></span>

-   [<span data-ttu-id="e07c0-121">테스트 환경 사용</span><span class="sxs-lookup"><span data-stu-id="e07c0-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





