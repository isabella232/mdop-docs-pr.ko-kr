---
title: GPO 설정 검토
description: GPO 설정 검토
author: dansimp
ms.assetid: e82570b2-d8ce-4bf0-8ad7-8910409f3041
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 681492f423266ce3722bb1a657ee93527c6bdd7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818333"
---
# <span data-ttu-id="4b052-103">GPO 설정 검토</span><span class="sxs-lookup"><span data-stu-id="4b052-103">Review GPO Settings</span></span>


<span data-ttu-id="4b052-104">모든 버전의 GPO (그룹 정책 개체) 내에서 설정을 검토 하는 HTML 기반 보고서와 XML 기반 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-104">You can generate HTML-based and XML-based reports for reviewing settings within any version of a Group Policy object (GPO).</span></span>

<span data-ttu-id="4b052-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="4b052-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b052-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="4b052-107">모든 버전의 GPO에 대 한 설정을 검토 하려면</span><span class="sxs-lookup"><span data-stu-id="4b052-107">To review settings in any version of a GPO</span></span>**

1.  <span data-ttu-id="4b052-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4b052-109">세부 정보 창의 **콘텐츠** 탭에서 탭을 클릭 하 여 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-109">On the **Contents** tab in the details pane, click a tab to display GPOs.</span></span>

3.  <span data-ttu-id="4b052-110">해당 GPO를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-110">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="4b052-111">설정을 검토할 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **HTML 보고서** 또는 **XML 보고서** 를 클릭 하 여 gpo 설정에 대 한 요약 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-111">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="4b052-112">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="4b052-112">Additional considerations</span></span>

-   <span data-ttu-id="4b052-113">이 절차를 수행 하려면 기본적으로 검토자, 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-113">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="4b052-114">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-114">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="4b052-115">또한 Gpo 목록을 표시 하려면 도메인에 대 한 **목록 내용** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b052-115">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="4b052-116">추가 참조</span><span class="sxs-lookup"><span data-stu-id="4b052-116">Additional references</span></span>

-   [<span data-ttu-id="4b052-117">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="4b052-117">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





