---
title: 고급 그룹 정책 관리 4.0
description: 고급 그룹 정책 관리 4.0
author: dansimp
ms.assetid: 9873a1f7-97fc-4546-9538-b4c0308529c0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 66dea6141430ee107ab85312b772d3c5ff3c5e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812604"
---
# <span data-ttu-id="fabf3-103">고급 그룹 정책 관리 4.0</span><span class="sxs-lookup"><span data-stu-id="fabf3-103">Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="fabf3-104">Microsoft AGPM (고급 그룹 정책 관리)를 사용 하 여 GPMC (그룹 정책 관리 콘솔)의 기능을 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="fabf3-105">AGPM은 광범위 한 변경 제어와 Gpo (그룹 정책 개체)의 향상 된 관리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="fabf3-106">AGPM을 사용 하 여 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="fabf3-107">프로덕션 환경에 배포 하기 전에 Gpo를 만들고 테스트할 수 있도록 오프 라인 편집을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="fabf3-108">문제가 발생 하는 경우 롤백할 수 있도록 중앙 보관 파일에 여러 버전의 GPO를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="fabf3-109">역할 기반 위임을 사용 하 여 여러 사람 간에 Gpo를 편집, 승인 및 검토 하는 책임을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="fabf3-110">여러 그룹 정책 관리자가 Gpo에 대 한 체크 인 및 체크 아웃 기능을 사용 하 여 다른 사람의 작업을 덮어쓸 위험성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="fabf3-111">GPO에 대 한 변경 내용을 분석 하 고 차이점 보고 기능을 사용 하 여 다른 GPO 또는 다른 버전의 동일한 GPO와 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="fabf3-112">GPO 템플릿을 사용 하 여 새 gpo 만들기를 간소화 하 고 새 Gpo의 시작 지점으로 사용할 일반적인 정책 설정 및 기본 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="fabf3-113">프로덕션 환경에 대 한 액세스를 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="fabf3-114">특정 특성을 가진 Gpo를 검색 하 고 표시 된 Gpo 목록을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="fabf3-115">테스트 포리스트의 도메인에서 프로덕션 포리스트의 도메인으로 복사할 수 있도록 GPO를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="fabf3-116">AGPM은 gpmc에 표시 되는 각 도메인 아래에 **변경 제어** 폴더를 추가 하 고 gpmc에 표시 되는 각 GPO 및 그룹 정책 링크에 대 한 **기록** 탭을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fabf3-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="fabf3-117">고급 그룹 정책 관리 개요</span><span class="sxs-lookup"><span data-stu-id="fabf3-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="fabf3-118">버전 제어의 모범 사례</span><span class="sxs-lookup"><span data-stu-id="fabf3-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="fabf3-119">검사 목록: AGPM 서버 및 아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="fabf3-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="fabf3-120">검사 목록: GPO 만들기, 편집 및 배포</span><span class="sxs-lookup"><span data-stu-id="fabf3-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="fabf3-121">GPO 목록 검색 및 필터링</span><span class="sxs-lookup"><span data-stu-id="fabf3-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="fabf3-122">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fabf3-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="fabf3-123">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fabf3-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="fabf3-124">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fabf3-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="fabf3-125">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fabf3-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="fabf3-126">AGPM 문제 해결</span><span class="sxs-lookup"><span data-stu-id="fabf3-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="fabf3-127">사용자 인터페이스: 고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="fabf3-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





