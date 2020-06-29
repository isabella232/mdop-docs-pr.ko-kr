---
title: 고급 그룹 정책 관리 개요
description: 고급 그룹 정책 관리 개요
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822488"
---
# <span data-ttu-id="d8d1f-103">고급 그룹 정책 관리 개요</span><span class="sxs-lookup"><span data-stu-id="d8d1f-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="d8d1f-104">AGPM (고급 그룹 정책 관리)을 사용 하 여 GPMC (그룹 정책 관리 콘솔)의 기능을 확장 하 여 Gpo (그룹 정책 개체)에 대 한 포괄적인 변경 제어 및 향상 된 관리를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="d8d1f-105">변경 제어를 사용 하 여 그룹 정책 개체 개발</span><span class="sxs-lookup"><span data-stu-id="d8d1f-105">Group Policy object development with change control</span></span>


<span data-ttu-id="d8d1f-106">AGPM을 사용 하면 그룹 정책 관리자가 GPO의 배포 된 버전에 즉시 영향을 주지 않고 오프 라인으로 보고 변경할 수 있도록 각 GPO의 복사본을 중앙 보관 함에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="d8d1f-107">또한, AGPM은 필요에 따라 이전 버전으로 롤백할 수 있도록 저장소에 각 제어 된 GPO의 각 버전 복사본을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="d8d1f-108">"체크 인" 및 "체크 아웃" 이라는 용어는 라이브러리 (또는 프로그래밍 개발에 대 한 변경 제어, 버전 제어 또는 소스 제어를 제공 하는 응용 프로그램)에서와 마찬가지로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="d8d1f-109">라이브러리에 있는 북을 사용 하려면 라이브러리에서 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="d8d1f-110">다른 사용자가 체크 아웃 하는 동안에는 아무도 사용할 수 없습니다. 북이 끝나면 다른 사용자가 사용할 수 있도록 라이브러리에 다시 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="d8d1f-111">이러한 GPO 컨트롤 기능을 사용 하려면 그룹 정책 관리 편집기에서 변경 컨트롤 노드를 클릭 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-111">To use these GPO control features, you will click a Change Control node in the Group Policy Management editor.</span></span> <span data-ttu-id="d8d1f-112">사용자가 AGPM 클라이언트를 설치한 경우에만 변경 내용 제어 노드가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-112">The Change Control node appears only if you have installed the AGPM Client.</span></span>

<span data-ttu-id="d8d1f-113">AGPM을 사용 하 여 Gpo를 개발 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="d8d1f-113">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="d8d1f-114">새로운 제어 GPO를 만들거나 이전에 미제어 GPO를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-114">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="d8d1f-115">사용자만 변경할 수 있도록 GPO를 체크 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-115">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="d8d1f-116">GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-116">Edit the GPO.</span></span>

4.  <span data-ttu-id="d8d1f-117">다른 사용자가 변경할 수 있도록 편집 된 GPO를 체크 인 하거나 배포 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-117">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="d8d1f-118">변경 내용을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-118">Review the changes.</span></span>

6.  <span data-ttu-id="d8d1f-119">프로덕션 환경에 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-119">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="d8d1f-120">역할 기반 위임</span><span class="sxs-lookup"><span data-stu-id="d8d1f-120">Role-based delegation</span></span>


<span data-ttu-id="d8d1f-121">AGPM은 보관 저장소의 Gpo에 대 한 액세스를 관리 하기 위한 포괄적이 고 사용이 간편한 역할 기반 위임을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-121">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="d8d1f-122">도메인 수준 사용 권한은 AGPM 관리자가 다른 도메인에 대 한 액세스를 제공 하지 않고 개별 도메인에 대 한 액세스를 제공할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-122">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="d8d1f-123">GPO 기반 위임을 사용 하면 AGPM 관리자가 도메인 전체의 액세스 권한을 제공 하지 않고 특정 Gpo에 대 한 액세스를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-123">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="d8d1f-124">AGPM 내에는 AGPM 관리자 (모든 권한), 승인자, 편집자, 검토자 등 구체적으로 정의 된 역할이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-124">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="d8d1f-125">AGPM 관리자 역할에는 다른 모든 역할에 대 한 사용 권한이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-125">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="d8d1f-126">기본적으로 승인자는 도메인의 프로덕션 환경에 Gpo를 배포 하는 기능을 가지 며, 경험이 적은 편집기에서 환경을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-126">By default, only Approvers have the power to deploy GPOs to the production environment of a domain, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="d8d1f-127">또한 기본적으로 모든 역할에는 검토자 역할이 포함 되므로 보고서에서 GPO 설정을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-127">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="d8d1f-128">그러나 AGPM은 조직의 요구에 맞게 GPO 액세스를 사용자 지정 하는 유연성을 사용 하 여 AGPM 관리자에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-128">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="d8d1f-129">여러 그룹 정책 관리자 환경의 위임</span><span class="sxs-lookup"><span data-stu-id="d8d1f-129">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="d8d1f-130">여러 사람이 Gpo를 변경 하는 환경에서는 AGPM 관리자가 편집자, 승인자, 검토자에 게 권한을 그룹 또는 개인으로 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-130">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="d8d1f-131">편집기 및 승인자에 대 한 일반적인 GPO 개발 프로세스의 경우 [검사 목록: GPO 만들기, 편집 및 배포](checklist-create-edit-and-deploy-a-gpo-agpm40.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8d1f-131">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="d8d1f-132">추가 참조</span><span class="sxs-lookup"><span data-stu-id="d8d1f-132">Additional references</span></span>

-   [<span data-ttu-id="d8d1f-133">고급 그룹 정책 관리 4.0</span><span class="sxs-lookup"><span data-stu-id="d8d1f-133">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





