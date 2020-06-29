---
title: AGPM 서버 연결 구성
description: AGPM 서버 연결 구성
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818913"
---
# <span data-ttu-id="1fc0a-103">AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="1fc0a-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="1fc0a-104">AGPM (고급 그룹 정책 관리)은 중앙 보관 저장소에 각 제어 된 GPO (그룹 정책 개체)의 모든 버전을 저장 하므로, 그룹 정책 관리자는 각 GPO의 배포 된 버전에 즉시 영향을 주지 않고 Gpo를 오프 라인으로 보고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="1fc0a-105">모든 그룹 정책 관리자에 대해 중앙 집중적으로 구성 하는 절차를 완료 하려면 AGPM 관리자 (전체 제어) 역할이 있는 사용자 계정, 이러한 절차에 사용 되는 GPO를 만든 승인자의 사용자 계정 또는 고급 그룹 정책 관리에서 필요한 사용 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="1fc0a-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="1fc0a-107">AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="1fc0a-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="1fc0a-108">AGPM 관리자 (모든 권한)로, 모든 그룹 정책 관리자가 설정을 중앙에서 구성 하 여 동일한 AGPM 서버에 연결 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="1fc0a-109">환경에 일부 또는 모든 도메인에 대 한 별도의 AGPM 서버가 필요한 경우 해당 추가 AGPM 서버를 기본값에 대 한 예외로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="1fc0a-110">사용자가 AGPM 서버 연결을 중앙에서 구성 하지 않는 경우 각 그룹 정책 관리자가 각 도메인에 대해 AGPM 서버를 수동으로 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="1fc0a-111">모든 그룹 정책 관리자를 위해 AGPM 서버 구성</span><span class="sxs-lookup"><span data-stu-id="1fc0a-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="1fc0a-112">모든 그룹 정책 관리자를 위한 추가 AGPM 서버 구성</span><span class="sxs-lookup"><span data-stu-id="1fc0a-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="1fc0a-113">계정에 대 한 AGPM 서버 수동 구성</span><span class="sxs-lookup"><span data-stu-id="1fc0a-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="1fc0a-114">모든 그룹 정책 관리자를 위해 AGPM 서버를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1fc0a-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="1fc0a-115">**그룹 정책 관리 콘솔** 트리에서 모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="1fc0a-116">(자세한 내용은 [GPO 편집](editing-a-gpo.md)을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="1fc0a-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="1fc0a-117">**그룹 정책 개체 편집기**에서 **사용자 구성**, **관리 템플릿**, **Windows 구성 요소**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="1fc0a-118">**Windows 구성 요소**아래에 **AGPM** 이 표시 되지 않으면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="1fc0a-119">**관리 서식 파일** 을 마우스 오른쪽 단추로 클릭 하 고 **서식 파일 추가/제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="1fc0a-120">**추가**를 클릭 하 고 **agpm** 또는 **Agpm**을 선택 하 고 **열기**를 클릭 한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="1fc0a-121">**Windows 구성 요소**에서 **AGPM**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="1fc0a-122">세부 정보 창에서 **AGPM 서버 (모든 도메인)** 를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="1fc0a-123">**AGPM 서버 (모든 도메인) 속성** 창에서 **사용** 확인란을 선택 하 고 정규화 된 컴퓨터 이름 및 포트 (예: server.contoso.com:4600)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="1fc0a-124">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-124">Click **OK**.</span></span> <span data-ttu-id="1fc0a-125">추가 AGPM 서버 연결을 구성 하려는 경우가 아니라면 **그룹 정책 개체 편집기** 를 닫고 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="1fc0a-126">(자세한 내용은 [GPO 배포](deploy-a-gpo.md)를 참조 하세요.) 그룹 정책이 업데이트 되 면 모든 그룹 정책 관리자에 게 AGPM 서버 연결이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="1fc0a-127">모든 그룹 정책 관리자에 대해 추가 AGPM 서버를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1fc0a-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="1fc0a-128">AGPM 서버 연결이 구성 되지 않은 경우 앞의 절차에 따라 모든 도메인에 대 한 기본 AGPM 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="1fc0a-129">일부 또는 모든 도메인 (기본 AGPM 서버 재정의)에 대해 별도의 AGPM 서버를 구성 하려면 **그룹 정책 관리 콘솔** 트리에서 모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="1fc0a-130">(자세한 내용은 [GPO 편집](editing-a-gpo.md)을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="1fc0a-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="1fc0a-131">**그룹 정책 개체 편집기**의 **사용자 구성** 에서 **관리 템플릿**, **Windows 구성 요소**, **AGPM**을 차례로 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="1fc0a-132">세부 정보 창에서 **AGPM 서버**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="1fc0a-133">**AGPM 서버 속성** 창에서 **사용** 확인란을 선택 하 고 **표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="1fc0a-134">**내용 표시** 창에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="1fc0a-135">**추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="1fc0a-136">**값 이름**에 도메인 이름 (예: server1.contoso.com)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="1fc0a-137">**Value**에 대해이 도메인에 사용할 AGPM 서버 이름 및 포트 (예: server2.contoso.com:4600)를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="1fc0a-138">(기본적으로 AGPM 서비스는 포트 4600에서 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="1fc0a-139">다른 포트를 사용 하려면 [AGPM 서비스에서 수신 대기 하는 포트 수정을](modify-the-port-on-which-the-agpm-service-listens.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="1fc0a-140">기본 AGPM 서버를 사용 하지 않는 각 도메인에 대해 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="1fc0a-141">**확인** 을 클릭 하 여 **콘텐츠** 및 **AGPM 서버 속성** 창 표시를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="1fc0a-142">**그룹 정책 개체 편집기**를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="1fc0a-143">(자세한 내용은 [GPO 배포](deploy-a-gpo.md)를 참조 하세요.) 그룹 정책이 업데이트 되 면 모든 그룹 정책 관리자에 대해 새 AGPM 서버 연결이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="1fc0a-144">AGPM 서버 연결을 중앙에서 구성한 경우 모든 그룹 정책 관리자에 게 수동으로 사용할 수 있는 옵션이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="1fc0a-145">계정에 대해 표시 하도록 AGPM 서버를 수동으로 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1fc0a-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="1fc0a-146">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1fc0a-147">세부 정보 창에서 **AGPM 서버** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="1fc0a-148">이 도메인에 사용 되는 보관 파일 (예: server.contoso.com) 및 AGPM 서비스가 수신 대기 하는 포트 (기본적으로 포트 4600)를 관리 하는 AGPM 서버의 정규화 된 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="1fc0a-149">**적용**을 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="1fc0a-150">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="1fc0a-150">Additional considerations</span></span>

-   <span data-ttu-id="1fc0a-151">모든 그룹 정책 관리자의 AGPM 서버 연결을 중앙에서 구성 하는 절차를 수행 하려면 GPO를 편집 하 고 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="1fc0a-152">추가 세부 정보는 [Gpo 편집](editing-a-gpo.md) 및 [gpo 배포](deploy-a-gpo.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="1fc0a-153">AGPM 서버를 선택 하면 **콘텐츠** 탭에 표시 되는 Gpo와 **도메인 위임** 탭 설정이 적용 되는 위치를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="1fc0a-154">관리 템플릿을 통해 중앙에서 관리 되지 않는 경우 각 그룹 정책 관리자는 해당 도메인의 AGPM 서버를 가리키도록이 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="1fc0a-155">AGPM의 Gpo에 대 한 액세스 관리를 우회 하는 데 사용 되지 않도록 그룹 정책 작성자 겸 소유자 그룹의 구성원을 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fc0a-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="1fc0a-156">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="1fc0a-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="1fc0a-157">추가 참조</span><span class="sxs-lookup"><span data-stu-id="1fc0a-157">Additional references</span></span>

-   [<span data-ttu-id="1fc0a-158">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="1fc0a-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





