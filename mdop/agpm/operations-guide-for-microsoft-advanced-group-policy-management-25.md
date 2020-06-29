---
title: Microsoft 고급 그룹 정책 관리 2.5 작업 가이드
description: Microsoft 고급 그룹 정책 관리 2.5 작업 가이드
author: dansimp
ms.assetid: 005f0bb5-789f-42a9-bcaf-7e8c31a8df66
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c0ae04e0e8dcf62d3ea840de28a9248827ec62e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822513"
---
# <span data-ttu-id="797ad-103">Microsoft 고급 그룹 정책 관리 2.5 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="797ad-103">Operations Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="797ad-104">Microsoft AGPM (고급 그룹 정책 관리)를 사용 하 여 GPMC (그룹 정책 관리) 콘솔의 기능을 확장 하 여 Gpo (그룹 정책 개체)에 대 한 종합적인 변경 제어 및 향상 된 관리를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

<span data-ttu-id="797ad-105">AGPM을 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-105">With AGPM you can:</span></span>

-   <span data-ttu-id="797ad-106">프로덕션 환경에 배포 하기 전에 Gpo를 만들고 테스트할 수 있도록 오프 라인 편집을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="797ad-107">문제가 발생 하는 경우 롤백할 수 있도록 중앙 보관 파일에 여러 버전의 GPO를 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="797ad-108">역할 기반 위임을 사용 하 여 여러 사용자 간에 Gpo를 편집, 승인 및 검토 하는 책임을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="797ad-109">여러 그룹 정책 관리자가 Gpo에 대 한 체크 인/체크 아웃 기능을 사용 하 여 서로 작업을 덮어쓸 위험성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="797ad-110">GPO에 대 한 변경 내용을 분석 하 여 다른 GPO 또는 차이점 보고 기능을 사용 하는 다른 버전의 동일한 GPO와 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="797ad-111">새 gpo의 시작 지점으로 사용할 표준 설정을 저장 하 여 GPO 템플릿을 사용 하 여 새 Gpo 만들기를 간소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="797ad-112">AGPM은 GPMC에 표시 된 각 도메인 아래에 **변경 관리** 노드를 추가 하 고 gpmc에 표시 되는 각 GPO 및 그룹 정책 링크에 대 한 **기록** 및 **확장** 탭을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="797ad-112">AGPM adds a **Change Control** node under each domain displayed in the GPMC, as well as **History** and **Extensions** tabs for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="797ad-113">고급 그룹 정책 관리 개요</span><span class="sxs-lookup"><span data-stu-id="797ad-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management.md)

-   [<span data-ttu-id="797ad-114">검사 목록: GPO 만들기, 편집 및 배포</span><span class="sxs-lookup"><span data-stu-id="797ad-114">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="797ad-115">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="797ad-115">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="797ad-116">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="797ad-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="797ad-117">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="797ad-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="797ad-118">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="797ad-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="797ad-119">고급 그룹 정책 관리 문제 해결</span><span class="sxs-lookup"><span data-stu-id="797ad-119">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="797ad-120">사용자 인터페이스: 고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="797ad-120">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





