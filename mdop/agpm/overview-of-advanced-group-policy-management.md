---
title: 고급 그룹 정책 관리 개요
description: 고급 그룹 정책 관리 개요
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822483"
---
# <span data-ttu-id="85753-103">고급 그룹 정책 관리 개요</span><span class="sxs-lookup"><span data-stu-id="85753-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="85753-104">AGPM (고급 그룹 정책 관리)을 사용 하 여 GPMC (그룹 정책 관리 콘솔)의 기능을 확장 하 여 Gpo (그룹 정책 개체)에 대 한 종합적인 변경 제어 및 향상 된 관리를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85753-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="85753-105">변경 제어를 사용 하 여 그룹 정책 개체 개발</span><span class="sxs-lookup"><span data-stu-id="85753-105">Group Policy object development with change control</span></span>


<span data-ttu-id="85753-106">AGPM을 사용 하면 각 GPO의 복사본을 중앙 보관 파일에 저장할 수 있으므로 그룹 정책 관리자는 GPO의 배포 된 버전에 즉시 영향을 주지 않고 오프 라인으로 보고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85753-106">With AGPM, you can store a copy of each GPO in a central archive, so Group Policy administrators can view and modify it offline without immediately impacting the deployed version of the GPO.</span></span> <span data-ttu-id="85753-107">또한, AGPM은 필요에 따라 이전 버전으로 롤백할 수 있도록 저장소에 각 제어 된 GPO의 각 버전 복사본을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if needed.</span></span>

<span data-ttu-id="85753-108">"체크 인" 및 "체크 아웃" 이라는 용어는 라이브러리 (또는 프로그래밍 개발에 대 한 소스 코드 컨트롤, 변경 컨트롤, 버전 제어 또는 참조 제어를 제공 하는 응용 프로그램에서)와 거의 동일한 방식으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85753-108">The terms "check in" and "check out" are used in much the same way as in a library (or in applications that provide change control, version control, or source code control for programming development).</span></span> <span data-ttu-id="85753-109">라이브러리에 있는 북을 사용 하려면 라이브러리에서 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="85753-110">다른 사용자가 체크 아웃 하는 동안에는 아무도 사용할 수 없습니다. 북이 끝나면 다른 사용자가 사용할 수 있도록 라이브러리에 다시 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="85753-111">AGPM을 사용 하 여 Gpo를 개발할 때:</span><span class="sxs-lookup"><span data-stu-id="85753-111">When developing GPOs using AGPM:</span></span>

1.  <span data-ttu-id="85753-112">새로운 제어 GPO를 만들거나 이전에 미제어 GPO를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="85753-113">사용자만 수정할 수 있도록 GPO를 체크 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-113">Check out the GPO, so you and only you can modify it.</span></span>

3.  <span data-ttu-id="85753-114">GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="85753-115">편집한 GPO를 체크 인하고 다른 사용자가 수정할 수 있도록 하거나 배포할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-115">Check in the edited GPO, so others can modify it, or so it can be deployed.</span></span>

5.  <span data-ttu-id="85753-116">변경 내용을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-116">Review the changes.</span></span>

6.  <span data-ttu-id="85753-117">프로덕션 환경에 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="85753-118">역할 기반 위임</span><span class="sxs-lookup"><span data-stu-id="85753-118">Role-based delegation</span></span>


<span data-ttu-id="85753-119">AGPM은 포괄적이 고 사용이 간편한 역할 기반 위임을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-119">AGPM provides comprehensive, easy-to-use role-based delegation.</span></span> <span data-ttu-id="85753-120">도메인 수준 권한을 사용 하 여 AGPM 관리자는 다른 도메인에 대 한 액세스를 제공 하지 않고 개별 도메인에 대 한 액세스를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85753-120">Domain-level permissions allow AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="85753-121">GPO 기반 위임을 사용 하면 AGPM 관리자가 특정 Gpo에 대 한 액세스만 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85753-121">GPO-based delegation enables AGPM Administrators to allow access only to specific GPOs.</span></span>

<span data-ttu-id="85753-122">AGPM 내에는 AGPM 관리자 (모든 권한), 승인자, 편집자, 검토자 등 구체적으로 정의 된 역할이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85753-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="85753-123">AGPM 관리자 역할에는 다른 모든 역할에 대 한 사용 권한이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85753-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="85753-124">기본적으로 승인자만 프로덕션 환경에 Gpo를 배포할 수 있으므로 경험이 적은 편집기에서 실수로 잘못 된 실수 로부터 환경을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from inadvertent mistakes by less experienced Editors.</span></span> <span data-ttu-id="85753-125">또한 기본적으로 모든 역할에는 검토자 역할이 포함 되므로 보고서에서 GPO 설정을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85753-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="85753-126">그러나 AGPM은 조직의 요구에 맞게 GPO 액세스를 사용자 지정 하는 유연성을 사용 하 여 AGPM 관리자에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="85753-127">여러 그룹 정책 관리자 환경의 위임</span><span class="sxs-lookup"><span data-stu-id="85753-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="85753-128">여러 사람이 Gpo를 변경 하는 환경에서는 AGPM 관리자가 편집자, 승인자, 검토자에 게 권한을 그룹 또는 개인으로 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="85753-128">In an environment where multiple people make changes to GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="85753-129">편집기 및 승인자에 대 한 일반적인 GPO 개발 프로세스의 경우 [검사 목록: GPO 만들기, 편집 및 배포](checklist-create-edit-and-deploy-a-gpo.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85753-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo.md).</span></span>

### <span data-ttu-id="85753-130">추가 참조</span><span class="sxs-lookup"><span data-stu-id="85753-130">Additional references</span></span>

-   [<span data-ttu-id="85753-131">검사 목록: GPO 만들기, 편집 및 배포</span><span class="sxs-lookup"><span data-stu-id="85753-131">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="85753-132">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="85753-132">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="85753-133">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="85753-133">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="85753-134">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="85753-134">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="85753-135">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="85753-135">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="85753-136">고급 그룹 정책 관리 문제 해결</span><span class="sxs-lookup"><span data-stu-id="85753-136">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="85753-137">사용자 인터페이스: 고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="85753-137">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





