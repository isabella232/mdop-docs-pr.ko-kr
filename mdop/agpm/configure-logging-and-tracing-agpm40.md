---
title: 로깅 및 추적 구성
description: 로깅 및 추적 구성
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818968"
---
# <span data-ttu-id="260a8-103">로깅 및 추적 구성</span><span class="sxs-lookup"><span data-stu-id="260a8-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="260a8-104">관리 템플릿을 사용 하 여 선택적 로깅 및 추적을 중앙에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="260a8-105">이는 AGPM (고급 그룹 정책 관리)과 관련 된 문제를 진단할 때 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="260a8-106">이 절차를 완료 하려면 agpm 관리자 (전체 제어) 역할이 있는 사용자 계정, 이러한 프로시저에 사용 되는 GPO (그룹 정책 개체)를 만든 승인자의 사용자 계정 또는 AGPM에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="260a8-107">또한 agpm 서버에 대 한 로깅을 시작 하려면 AGPM 서버에 대 한 액세스 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="260a8-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="260a8-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="260a8-109">AGPM에 대 한 로깅 및 추적을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="260a8-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="260a8-110">**그룹 정책 관리 콘솔** 트리에서 로깅 및 추적을 설정 하려는 모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="260a8-111">(자세한 내용은 [GPO 편집](editing-a-gpo-agpm40.md)을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="260a8-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="260a8-112">**그룹 정책 관리 편집기** 창에서 **컴퓨터 구성**, **정책**, **관리 템플릿**, **Windows 구성 요소**및 **AGPM**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="260a8-113">세부 정보 창에서 **AGPM: 로깅 구성을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="260a8-114">**속성** 창에서 **사용**을 클릭 하 고 로그에 기록할 세부 정보 수준을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="260a8-115">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-115">Click **OK**.</span></span>

6.  <span data-ttu-id="260a8-116">**그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="260a8-117">(자세한 내용은 [GPO 배포](deploy-a-gpo-agpm40.md)를 참조 하세요.) 그룹 정책이 업데이트 되 면 agpm 서비스를 다시 시작 하 여 AGPM 서버에서 로깅을 시작, 수정 또는 중지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="260a8-118">그룹 정책 관리자는 컴퓨터에 대 한 로깅을 시작, 수정 또는 중지 하려면 GPMC를 닫았다가 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="260a8-119">**추적 파일 위치**:</span><span class="sxs-lookup"><span data-stu-id="260a8-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="260a8-120">클라이언트:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="260a8-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="260a8-121">서버:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="260a8-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="260a8-122">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="260a8-122">Additional considerations</span></span>

-   <span data-ttu-id="260a8-123">AGPM 로깅 및 추적을 구성 하려면 GPO를 편집 하 고 배포할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="260a8-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="260a8-124">추가 세부 정보는 [Gpo 편집](editing-a-gpo-agpm40.md) 및 [gpo 배포](deploy-a-gpo-agpm40.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="260a8-124">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="260a8-125">추가 참조</span><span class="sxs-lookup"><span data-stu-id="260a8-125">Additional references</span></span>

-   [<span data-ttu-id="260a8-126">고급 그룹 정책 관리 구성</span><span class="sxs-lookup"><span data-stu-id="260a8-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





