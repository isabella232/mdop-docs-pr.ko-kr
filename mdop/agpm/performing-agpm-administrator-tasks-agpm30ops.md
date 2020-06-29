---
title: AGPM 관리자 작업 수행
description: AGPM 관리자 작업 수행
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822423"
---
# <span data-ttu-id="ea950-103">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="ea950-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="ea950-104">AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한)는 도메인 전체 옵션을 구성 하 고 승인자, 편집자, 검토자 및 기타 AGPM 관리자에 게 권한을 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-104">In Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="ea950-105">기본적으로 AGPM 관리자는 모든 권한, 모든 사용자 및 모든 역할에 연결 된 작업을 수행할 수 있는 모든 권한이 있는 개인입니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-105">By default, an AGPM Administrator is an individual with Full Control—all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="ea950-106">여러 사용자가 Gpo (그룹 정책 개체)를 개발 하는 환경에서 모든 AGPM 사용자가 동일한 작업을 수행 하 고 동일한 수준의 액세스를 허용할지 여부 또는 AGPM 관리자가 Gpo를 변경 하는 편집자와 프로덕션 환경에 Gpo를 배포 하는 승인자에 게 권한을 위임할 것인지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose whether all AGPM users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="ea950-107">AGPM 관리자는 조직의 요구에 맞게 사용 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="ea950-108">[고급 그룹 정책 관리 구성](configuring-advanced-group-policy-management.md): AGPM 서버 연결 및 전자 메일 알림을 구성 하 고, 프로덕션 환경의 gpo에 대 한 액세스를 위임 하 고, 문제 해결을 위해 로깅 및 추적을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-108">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="ea950-109">[보관 관리](managing-the-archive.md): 보관 저장소의 gpo에 대 한 액세스 권한을 위임 하 고 저장 된 각 gpo의 버전 수를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-109">[Managing the Archive](managing-the-archive.md): Delegate access to GPOs in the archive and limit the number of versions of each GPO stored.</span></span>

-   <span data-ttu-id="ea950-110">[Agpm 서비스 관리](managing-the-agpm-service-agpm30ops.md): agpm 서비스를 중지 하 고 시작 하거나 보관 경로, Agpm 서비스 계정 또는 agpm 서비스가 수신 대기 하는 포트를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-110">[Managing the AGPM Service](managing-the-agpm-service-agpm30ops.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="ea950-111">[Agpm 서버와 보관 파일 이동](move-the-agpm-server-and-the-archive.md): agpm 서비스, 보관 또는 둘 다를 다른 서버로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-111">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="ea950-112">또한 AGPM 관리자 역할에 다른 모든 역할에 대 한 사용 권한이 포함 되기 때문에 AGPM 관리자가 다른 역할과 일반적으로 연결 되는 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-112">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="ea950-113">Gpo 만들기, 배포 또는 삭제와 같은 [승인자 작업 수행](performing-approver-tasks-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="ea950-113">[Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="ea950-114">편집, 이름 바꾸기, 레이블 지정, Gpo 가져오기, 서식 파일 만들기 또는 기본 서식 파일 설정 등의 [편집자 작업 수행](performing-editor-tasks-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="ea950-114">[Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="ea950-115">설정 검토 및 Gpo 비교와 같은 [검토자 작업 수행](performing-reviewer-tasks-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="ea950-115">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="ea950-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="ea950-116">Additional considerations</span></span>

<span data-ttu-id="ea950-117">기본적으로 AGPM 관리자 역할에는 모든 권한, 즉 모든 AGPM 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-117">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="ea950-118">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="ea950-118">List Contents</span></span>

-   <span data-ttu-id="ea950-119">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="ea950-119">Read Settings</span></span>

-   <span data-ttu-id="ea950-120">설정 편집</span><span class="sxs-lookup"><span data-stu-id="ea950-120">Edit Settings</span></span>

-   <span data-ttu-id="ea950-121">GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="ea950-121">Create GPO</span></span>

-   <span data-ttu-id="ea950-122">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="ea950-122">Deploy GPO</span></span>

-   <span data-ttu-id="ea950-123">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="ea950-123">Delete GPO</span></span>

-   <span data-ttu-id="ea950-124">옵션 수정</span><span class="sxs-lookup"><span data-stu-id="ea950-124">Modify Options</span></span>

-   <span data-ttu-id="ea950-125">보안 수정</span><span class="sxs-lookup"><span data-stu-id="ea950-125">Modify Security</span></span>

-   <span data-ttu-id="ea950-126">서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="ea950-126">Create Template</span></span>

<span data-ttu-id="ea950-127">**수정 옵션** 및 **보안 수정** 권한은 AGPM 관리자의 역할에 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea950-127">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





