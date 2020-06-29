---
title: 버전 제어의 모범 사례
description: 버전 제어의 모범 사례
author: dansimp
ms.assetid: 89067f6a-f7ea-4dad-999d-118284cf6c5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ed91408faeb8968175976382f9dd97d45becddb5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819203"
---
# <span data-ttu-id="c9c8b-103">버전 제어의 모범 사례</span><span class="sxs-lookup"><span data-stu-id="c9c8b-103">Best Practices for Version Control</span></span>


<span data-ttu-id="c9c8b-104">Microsoft AGPM (고급 그룹 정책 관리)에서는 Microsoft Visual SourceSafe® 버전이 소스 코드에 대 한 버전 제어를 제공 하는 것과 같이 Gpo (그룹 정책 개체)에 대 한 버전 제어권을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-104">Microsoft Advanced Group Policy Management (AGPM) provides version control for Group Policy Objects (GPOs) much like Microsoft Visual SourceSafe® provides version control for source code.</span></span> <span data-ttu-id="c9c8b-105">개발자는 Visual SourceSafe를 사용 하 여 각 원본 파일의 여러 버전을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-105">Developers can use Visual SourceSafe to manage multiple versions of each source file.</span></span> <span data-ttu-id="c9c8b-106">그룹 정책 관리자는 AGPM을 사용 하 여 Gpo에 대해 동일한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-106">Group Policy administrators can use AGPM to do the same for GPOs.</span></span> <span data-ttu-id="c9c8b-107">AGPM을 사용 하는 경우 그룹 정책 관리자는 모든 버전 제어 시스템에 적용 되는 모범 사례를 인식 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-107">When you use AGPM, Group Policy administrators should be aware of best practices that apply to any version control system:</span></span>

-   <span data-ttu-id="c9c8b-108">**날짜 및 시간:** AGPM에서 각 버전의 GPO를 날짜 및 시간으로 스탬프 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-108">**Date and time:** AGPM stamps each version of a GPO with the date and time.</span></span> <span data-ttu-id="c9c8b-109">특히 두 대 이상의 컴퓨터에서 Gpo를 편집할 때 기록이 정확 하 게 표시 되도록 하려면 각 컴퓨터가 해당 시계를 신뢰할 수 있는 한 개의 시간 원본과 동기화 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-109">To ensure that history is accurate, especially when you edit GPOs on more than one computer, make sure that each computer synchronizes its clock with one authoritative time source.</span></span>

-   <span data-ttu-id="c9c8b-110">**편집이 완료 되 면 gpo를 체크 인 합니다.** 편집자는 일반적으로 Gpo를 확인 하 여 보관 파일로 다시 체크 인하는 것을 잊지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-110">**Check in GPOs when you are finished editing them:** It is common for Editors to check out GPOs and forget to check them back into the archive.</span></span> <span data-ttu-id="c9c8b-111">그러나 이렇게 하면 다른 그룹 정책 관리자가 GPO를 변경 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-111">However, this can prevent other Group Policy administrators from changing the GPO.</span></span> <span data-ttu-id="c9c8b-112">편집이 완료 되 면 항상 AGPM에 대 한 Gpo를 즉시 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-112">Always check GPOs back in to AGPM immediately when you are finished editing.</span></span>

-   <span data-ttu-id="c9c8b-113">**자주 변경 내용 저장:** GPO를 편집할 때 변경 내용을 자주 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-113">**Save changes frequently:** When you edit a GPO, save changes frequently.</span></span> <span data-ttu-id="c9c8b-114">대부분의 편집자는 GPO를 체크 아웃 하 고 많은 내용을 변경한 다음 GPO를 보관 함으로 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-114">Most Editors check out a GPO, make many changes, and then check the GPO into the archive.</span></span> <span data-ttu-id="c9c8b-115">대신, 보관 저장소에 대 한 GPO를 정기적으로 확인 한 다음 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-115">Instead, check the GPO into the archive regularly, and then check it out again.</span></span> <span data-ttu-id="c9c8b-116">모든 설정을 변경 (권장 하지 않음) 하거나 관련 변경 그룹을 만든 후 GPO를 체크 인하면 GPO를 체크 인하는 것 만큼이 세부 정보를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-116">The detail can be as small as checking in the GPO after you change every setting (not recommended) or checking in the GPO after you make groups of related changes.</span></span> <span data-ttu-id="c9c8b-117">결과는 문제 해결에 도움이 될 수 있는 각 GPO에 대해 더 나은 문서화 된 기록입니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-117">The result is a better-documented history for each GPO that can help when troubleshooting issues.</span></span>

-   <span data-ttu-id="c9c8b-118">**자주 Gpo 배포:** 아직 배포 되지 않은 신규 및 편집한 Gpo는 보관 저장소에 큰 숫자로 누적 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-118">**Deploy GPOs frequently:** Do not let new and edited GPOs that have not yet been deployed accumulate in large numbers in the archive.</span></span> <span data-ttu-id="c9c8b-119">대신, 새 Gpo와 편집 된 Gpo를 가능한 한 빨리 배포 하 여 프로덕션 환경에 최소한의 영향을 미칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-119">Instead, deploy new and edited GPOs as soon as possible so that they have a minimum effect on the production environment.</span></span> <span data-ttu-id="c9c8b-120">한 번에 여러 개의 새 Gpo를 배포 하면 프로덕션 환경이 위험 해질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-120">Deploying many new and edited GPOs at one time can jeopardize the production environment.</span></span>

-   <span data-ttu-id="c9c8b-121">**Gpo를 체크 인할 때 변경의 목적을 문서화 합니다.** 모든 검토자는 GPO의 버전을 비교 하 여 둘 간의 특정 변경 내용을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-121">**Document the purpose of changes when you check in GPOs:** Any Reviewer can compare versions of a GPO to see specific changes between the two.</span></span> <span data-ttu-id="c9c8b-122">이러한 특정 변경 내용을 문서화 하면 값이 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-122">Documenting those specific changes adds no value.</span></span> <span data-ttu-id="c9c8b-123">대신 변경의 용도와 목적을 문서화 하 고 차이 보고서를 보고 검토자가 볼 수 있는 내용을 문서화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-123">Instead, document the intent and purpose of a change instead of documenting what Reviewers can see by viewing difference reports.</span></span> <span data-ttu-id="c9c8b-124">버전 메모는 비교 보고서에 값을 추가 하 고, 검토자가 GPO를 변경한 이유를 이해 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-124">Version comments should add value to the comparison report and help a Reviewer understand why the Editor changed the GPO.</span></span>

-   <span data-ttu-id="c9c8b-125">**배포 하기 전에 랩에서 gpo를 테스트 합니다.** 먼저 Gpo를 테스트 하지 않고 프로덕션 환경에 배포 하는 것은 위험한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-125">**Test GPOs in a lab before you deploy:** Deploying GPOs to the production environment without first testing them is risky.</span></span> <span data-ttu-id="c9c8b-126">대신 테스트 컴퓨터와 사용자를 포함 하는 조직 구성 단위에 연결 하 고 올바르게 작동 하는지 확인 하 여 랩 환경에서 Gpo를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-126">Instead, test GPOs in a lab environment by linking them to an organizational unit that contains test computers and users, and then verifying that they function correctly.</span></span> <span data-ttu-id="c9c8b-127">랩에서 각 GPO를 확인 한 후 프로덕션 환경에 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c8b-127">After verifying each GPO in the lab, deploy the GPO to the production environment.</span></span>

### <span data-ttu-id="c9c8b-128">추가 참조</span><span class="sxs-lookup"><span data-stu-id="c9c8b-128">Additional references</span></span>

-   [<span data-ttu-id="c9c8b-129">Microsoft 고급 그룹 정책 관리 3.0 작업 가이드</span><span class="sxs-lookup"><span data-stu-id="c9c8b-129">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





