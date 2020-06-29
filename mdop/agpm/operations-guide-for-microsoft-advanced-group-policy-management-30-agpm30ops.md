---
title: Microsoft 고급 그룹 정책 관리 3.0 작업 가이드
description: Microsoft 고급 그룹 정책 관리 3.0 작업 가이드
author: dansimp
ms.assetid: aaefe6d1-a9e5-43eb-b4d8-85880798cb8b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4958609444a62560060a565fb8626bcc9680fd9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822508"
---
# <span data-ttu-id="8384d-103">Microsoft 고급 그룹 정책 관리 3.0 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="8384d-103">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="8384d-104">Microsoft AGPM (고급 그룹 정책 관리)를 사용 하 여 GPMC (그룹 정책 관리) 콘솔의 기능을 확장 하 여 Gpo (그룹 정책 개체)에 대 한 종합적인 변경 제어 및 향상 된 관리를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="8384d-105">AGPM을 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-105">With AGPM you can:</span></span>

-   <span data-ttu-id="8384d-106">프로덕션 환경에 배포 하기 전에 Gpo를 만들고 테스트할 수 있도록 오프 라인 편집을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="8384d-107">문제가 발생 하는 경우 롤백할 수 있도록 중앙 보관 파일에 여러 버전의 GPO를 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="8384d-108">역할 기반 위임을 사용 하 여 여러 사용자 간에 Gpo를 편집, 승인 및 검토 하는 책임을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="8384d-109">여러 그룹 정책 관리자가 Gpo에 대 한 체크 인/체크 아웃 기능을 사용 하 여 서로 작업을 덮어쓸 위험성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="8384d-110">GPO에 대 한 변경 내용을 분석 하 여 다른 GPO 또는 차이점 보고 기능을 사용 하는 다른 버전의 동일한 GPO와 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="8384d-111">새 gpo의 시작 지점으로 사용할 표준 설정을 저장 하 여 GPO 템플릿을 사용 하 여 새 Gpo 만들기를 간소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="8384d-112">AGPM은 GPMC에 표시 되는 각 도메인 아래에 **변경 제어** 폴더를 추가 하 고 gpmc에 표시 된 각 GPO 및 그룹 정책 링크에 대 한 **기록** 탭입니다.</span><span class="sxs-lookup"><span data-stu-id="8384d-112">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, as well as a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="8384d-113">고급 그룹 정책 관리 개요</span><span class="sxs-lookup"><span data-stu-id="8384d-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="8384d-114">버전 제어의 모범 사례</span><span class="sxs-lookup"><span data-stu-id="8384d-114">Best Practices for Version Control</span></span>](best-practices-for-version-control.md)

-   [<span data-ttu-id="8384d-115">검사 목록: AGPM 서버 및 아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="8384d-115">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive.md)

-   [<span data-ttu-id="8384d-116">검사 목록: GPO 만들기, 편집 및 배포</span><span class="sxs-lookup"><span data-stu-id="8384d-116">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="8384d-117">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8384d-117">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="8384d-118">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8384d-118">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="8384d-119">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8384d-119">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="8384d-120">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8384d-120">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

-   [<span data-ttu-id="8384d-121">고급 그룹 정책 관리 문제 해결</span><span class="sxs-lookup"><span data-stu-id="8384d-121">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="8384d-122">사용자 인터페이스: 고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="8384d-122">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

 

 





