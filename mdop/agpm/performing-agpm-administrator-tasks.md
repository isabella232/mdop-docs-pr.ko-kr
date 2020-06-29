---
title: AGPM 관리자 작업 수행
description: AGPM 관리자 작업 수행
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820478"
---
# <span data-ttu-id="c8a10-103">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="c8a10-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="c8a10-104">AGPM 관리자 (모든 권한)는 도메인 전체 옵션을 구성 하 고 승인자, 편집자, 검토자 및 기타 AGPM 관리자에 게 권한을 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="c8a10-105">기본적으로 AGPM 관리자는 모든 권한이 있는 개인 (모든 고급 그룹 정책 관리 \ [AGPM \] 권한) 이므로 역할에 연결 된 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="c8a10-106">여러 사용자가 Gpo (그룹 정책 개체)를 개발 하는 환경에서 모든 AGPM (고급 그룹 정책 관리) 사용자가 동일한 작업을 수행 하 고 동일한 수준의 액세스를가지고 있는지, 아니면 AGPM 관리자가 Gpo를 변경 하는 편집자와 프로덕션 환경에 Gpo를 배포 하는 승인자에 게 권한을 위임할 것인지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="c8a10-107">AGPM 관리자는 조직의 요구에 맞게 사용 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="c8a10-108">AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="c8a10-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="c8a10-109">전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="c8a10-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="c8a10-110">도메인 수준 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="c8a10-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="c8a10-111">개별 GPO에 대한 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="c8a10-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="c8a10-112">로깅 및 추적 구성</span><span class="sxs-lookup"><span data-stu-id="c8a10-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="c8a10-113">AGPM 서비스 관리</span><span class="sxs-lookup"><span data-stu-id="c8a10-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="c8a10-114">AGPM 서비스 시작 및 중지</span><span class="sxs-lookup"><span data-stu-id="c8a10-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="c8a10-115">아카이브 경로 수정</span><span class="sxs-lookup"><span data-stu-id="c8a10-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="c8a10-116">AGPM 서비스 계정 수정</span><span class="sxs-lookup"><span data-stu-id="c8a10-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="c8a10-117">AGPM 서비스를 수신할 포트 수정</span><span class="sxs-lookup"><span data-stu-id="c8a10-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="c8a10-118">또한 AGPM 관리자 역할에 다른 모든 역할에 대 한 사용 권한이 포함 되기 때문에 AGPM 관리자가 다른 역할과 일반적으로 연결 되는 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="c8a10-119">Gpo 만들기, 배포 또는 삭제와 같은 [승인자 작업 수행](performing-approver-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="c8a10-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="c8a10-120">편집, 이름 바꾸기, 레이블 지정, Gpo 가져오기, 서식 파일 만들기 또는 기본 서식 파일 설정 등의 [편집자 작업 수행](performing-editor-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="c8a10-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="c8a10-121">설정 검토 및 Gpo 비교와 같은 [검토자 작업 수행](performing-reviewer-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="c8a10-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="c8a10-122">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="c8a10-122">Additional considerations</span></span>

<span data-ttu-id="c8a10-123">기본적으로 AGPM 관리자 역할에는 모든 권한, 즉 모든 AGPM 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="c8a10-124">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="c8a10-124">List Contents</span></span>

-   <span data-ttu-id="c8a10-125">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="c8a10-125">Read Settings</span></span>

-   <span data-ttu-id="c8a10-126">설정 편집</span><span class="sxs-lookup"><span data-stu-id="c8a10-126">Edit Settings</span></span>

-   <span data-ttu-id="c8a10-127">GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="c8a10-127">Create GPO</span></span>

-   <span data-ttu-id="c8a10-128">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="c8a10-128">Deploy GPO</span></span>

-   <span data-ttu-id="c8a10-129">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="c8a10-129">Delete GPO</span></span>

-   <span data-ttu-id="c8a10-130">옵션 수정</span><span class="sxs-lookup"><span data-stu-id="c8a10-130">Modify Options</span></span>

-   <span data-ttu-id="c8a10-131">보안 수정</span><span class="sxs-lookup"><span data-stu-id="c8a10-131">Modify Security</span></span>

-   <span data-ttu-id="c8a10-132">서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="c8a10-132">Create Template</span></span>

<span data-ttu-id="c8a10-133">**수정 옵션** 및 **보안 수정** 권한은 AGPM 관리자의 역할에 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a10-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





