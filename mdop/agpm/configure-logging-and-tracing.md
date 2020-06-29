---
title: 로깅 및 추적 구성
description: 로깅 및 추적 구성
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818973"
---
# <span data-ttu-id="8d8cd-103">로깅 및 추적 구성</span><span class="sxs-lookup"><span data-stu-id="8d8cd-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="8d8cd-104">관리 템플릿을 사용 하 여 AGPM (고급 그룹 정책 관리)에 대 한 선택적 로깅 및 추적을 중앙에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="8d8cd-105">이 절차를 완료 하려면 AGPM 관리자 (전체 제어) 역할이 있는 사용자 계정, 이러한 절차에 사용 되는 GPO를 만든 승인자의 사용자 계정 또는 고급 그룹 정책 관리에서 필요한 사용 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="8d8cd-106">또한 agpm 서버에 대 한 로깅을 시작 하려면 AGPM 서버에 대 한 액세스 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="8d8cd-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8d8cd-108">AGPM에 대 한 로깅 및 추적을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="8d8cd-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="8d8cd-109">**그룹 정책 관리 콘솔** 트리에서 로깅 및 추적을 설정 하려는 모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="8d8cd-110">(자세한 내용은 [GPO 편집](editing-a-gpo.md)을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="8d8cd-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="8d8cd-111">**그룹 정책 개체 편집기**에서 **컴퓨터 구성**, **관리 템플릿**, **Windows 구성 요소**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="8d8cd-112">**Windows 구성 요소**아래에 **AGPM** 이 표시 되지 않으면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="8d8cd-113">**관리 서식 파일** 을 마우스 오른쪽 단추로 클릭 하 고 **서식 파일 추가/제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="8d8cd-114">**추가**를 클릭 하 고 **agpm** 또는 **Agpm**을 선택 하 고 **열기**를 클릭 한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="8d8cd-115">**Windows 구성 요소**에서 **AGPM**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="8d8cd-116">세부 정보 창에서 **AGPM 로깅을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="8d8cd-117">**AGPM 로깅 속성** 창에서 **사용**을 클릭 하 고 로그에 기록할 세부 정보 수준을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="8d8cd-118">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-118">Click **OK**.</span></span>

8.  <span data-ttu-id="8d8cd-119">**그룹 정책 개체 편집기**를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="8d8cd-120">(자세한 내용은 [GPO 배포](deploy-a-gpo.md)를 참조 하세요.) 그룹 정책이 업데이트 되 면 agpm 서비스를 다시 시작 하 여 AGPM 서버에서 로깅을 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="8d8cd-121">그룹 정책 관리자는 컴퓨터에 대 한 로깅을 시작 하려면 GPMC를 닫았다가 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="8d8cd-122">**추적 파일 위치**:</span><span class="sxs-lookup"><span data-stu-id="8d8cd-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="8d8cd-123">클라이언트:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="8d8cd-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="8d8cd-124">서버:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="8d8cd-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="8d8cd-125">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="8d8cd-125">Additional considerations</span></span>

-   <span data-ttu-id="8d8cd-126">AGPM 로깅 및 추적을 구성 하려면 GPO를 편집 하 고 배포할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="8d8cd-127">추가 세부 정보는 [Gpo 편집](editing-a-gpo.md) 및 [gpo 배포](deploy-a-gpo.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d8cd-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="8d8cd-128">추가 참조</span><span class="sxs-lookup"><span data-stu-id="8d8cd-128">Additional references</span></span>

-   [<span data-ttu-id="8d8cd-129">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8d8cd-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





