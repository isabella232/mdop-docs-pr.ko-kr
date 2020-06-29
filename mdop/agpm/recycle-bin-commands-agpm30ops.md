---
title: 휴지통 명령
description: 휴지통 명령
author: dansimp
ms.assetid: ffe8f020-7aa9-40ad-8019-cc99901a7840
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6abf063c3255538142a2ca2728a034cbaa4a1c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818548"
---
# <span data-ttu-id="84808-103">휴지통 명령</span><span class="sxs-lookup"><span data-stu-id="84808-103">Recycle Bin Commands</span></span>


<span data-ttu-id="84808-104">**휴지통** 탭:</span><span class="sxs-lookup"><span data-stu-id="84808-104">The **Recycle Bin** tab:</span></span>

-   <span data-ttu-id="84808-105">보관 저장소에서 삭제 된 Gpo (그룹 정책 개체)의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-105">Displays a list of Group Policy Objects (GPOs) that have been deleted from the archive.</span></span>

-   <span data-ttu-id="84808-106">Gpo를 관리 하 고 Gpo에 대 한 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-106">Provides a shortcut menu with commands for managing GPOs and for displaying reports for GPOs.</span></span>

-   <span data-ttu-id="84808-107">선택한 GPO에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="84808-108">이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 다음 중 해당 되는 옵션을 비롯 한 바로 가기 메뉴가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84808-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable:</span></span>

## <span data-ttu-id="84808-109">보고</span><span class="sxs-lookup"><span data-stu-id="84808-109">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84808-110">명령</span><span class="sxs-lookup"><span data-stu-id="84808-110">Command</span></span></th>
<th align="left"><span data-ttu-id="84808-111">효과</span><span class="sxs-lookup"><span data-stu-id="84808-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="84808-112">설정</span><span class="sxs-lookup"><span data-stu-id="84808-112">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="84808-113">선택한 GPO 내의 설정을 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 하거나 Gpo가 최근에 제어, 가져오기 또는 체크 인 되었을 때의 조직 구성 단위에서 선택한 Gpo에 대 한 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-113">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPOs from organizational units as of when the GPOs were most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="84808-114">차이점</span><span class="sxs-lookup"><span data-stu-id="84808-114">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="84808-115">선택한 두 Gpo 내의 설정과 선택한 GPO 및 서식 파일을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-115">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="84808-116">버전 관리</span><span class="sxs-lookup"><span data-stu-id="84808-116">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84808-117">명령</span><span class="sxs-lookup"><span data-stu-id="84808-117">Command</span></span></th>
<th align="left"><span data-ttu-id="84808-118">효과</span><span class="sxs-lookup"><span data-stu-id="84808-118">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="84808-119">손상</span><span class="sxs-lookup"><span data-stu-id="84808-119">Destroy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="84808-120">선택한 GPO를 휴지통에서 제거 하면 <strong> </strong> 더 이상 복원할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="84808-120">Remove the selected GPO from the <strong>Recycle Bin</strong>, so it can no longer be restored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="84808-121">복원한</span><span class="sxs-lookup"><span data-stu-id="84808-121">Restore</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="84808-122">선택한 GPO를 <strong> 휴지통에서 </strong> <strong> 제어 탭으로 이동 </strong> 합니다. 이것은 GPO가 프로덕션 환경으로 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84808-122">Move the selected GPO from the <strong>Recycle Bin</strong> to the <strong>Controlled</strong> tab. This does not restore the GPO to the production environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="84808-123">기타</span><span class="sxs-lookup"><span data-stu-id="84808-123">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84808-124">명령</span><span class="sxs-lookup"><span data-stu-id="84808-124">Command</span></span></th>
<th align="left"><span data-ttu-id="84808-125">효과</span><span class="sxs-lookup"><span data-stu-id="84808-125">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="84808-126">새로 고침</span><span class="sxs-lookup"><span data-stu-id="84808-126">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="84808-127">변경 내용을 통합 하기 위해 GPMC (그룹 정책 관리) 콘솔의 표시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-127">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="84808-128">일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84808-128">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="84808-129">Help</span><span class="sxs-lookup"><span data-stu-id="84808-129">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="84808-130">AGPM (고급 그룹 정책 관리)에 대 한 도움말을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84808-130">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="84808-131">추가 참조</span><span class="sxs-lookup"><span data-stu-id="84808-131">Additional references</span></span>

-   [<span data-ttu-id="84808-132">내용 탭</span><span class="sxs-lookup"><span data-stu-id="84808-132">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="84808-133">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="84808-133">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="84808-134">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="84808-134">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





