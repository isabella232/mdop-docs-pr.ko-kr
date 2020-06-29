---
title: Microsoft 고급 그룹 정책 관리 3.0 단계별 가이드
description: Microsoft 고급 그룹 정책 관리 3.0 단계별 가이드
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818328"
---
# <span data-ttu-id="d41a5-103">Microsoft 고급 그룹 정책 관리 3.0 단계별 가이드</span><span class="sxs-lookup"><span data-stu-id="d41a5-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="d41a5-104">이 단계별 안내서는 GPMC (그룹 정책 관리 콘솔) 및 AGPM (고급 그룹 정책 관리)을 사용 하 여 그룹 정책 관리에 대 한 고급 기술을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="d41a5-105">AGPM은 다음을 제공 하는 GPMC의 기능을 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="d41a5-106">여러 그룹 정책 관리자가 Gpo (그룹 정책 개체)를 관리 하는 데 사용 권한을 위임 하는 표준 역할은 물론, 프로덕션 환경에서 Gpo에 대 한 액세스를 위임 하는 기능도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="d41a5-107">그룹 정책 관리자가 프로덕션 환경에 배포 하기 전에 오프 라인으로 Gpo를 만들고 수정할 수 있는 보관 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="d41a5-108">보관 저장소에 있는 이전 버전의 GPO로 롤백할 수 있는 기능 및 아카이브에 저장 된 버전 수를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="d41a5-109">Gpo에 대 한 체크 인/체크 아웃 기능을 통해 그룹 정책 관리자가 실수로 서로의 작업을 덮어쓰지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="d41a5-110">AGPM 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="d41a5-110">AGPM scenario overview</span></span>


<span data-ttu-id="d41a5-111">이 시나리오에서는 각 역할에 대해 개별 사용자 계정을 사용 하 여 다양 한 수준의 권한을 가진 여러 그룹 정책 관리자가 있는 환경에서 그룹 정책을 관리 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="d41a5-112">구체적으로 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="d41a5-113">Domain Admins 그룹의 구성원 인 계정을 사용 하 여 AGPM 서버를 설치 하 고 AGPM 관리자 역할을 계정이 나 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="d41a5-114">AGPM 역할을 할당 하는 계정을 사용 하 여 AGPM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="d41a5-115">AGPM 관리자 역할이 있는 계정을 사용 하 여 다른 계정에 역할을 할당 하 여 AGPM을 구성 하 고 Gpo에 대 한 액세스 권한을 대리인에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="d41a5-116">편집자 역할이 있는 계정을 사용 하 여 GPO 만들기를 요청한 다음 승인자 역할이 있는 계정을 사용 하 여 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="d41a5-117">편집자 계정으로 보관 함에서 GPO를 확인 하 고, GPO를 편집 하 고, GPO를 보관 함으로 확인 하 고, 배포를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="d41a5-118">승인자 역할이 있는 계정을 사용 하 여 GPO를 검토 하 고 프로덕션 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="d41a5-119">편집자 역할이 있는 계정을 사용 하 여 GPO 서식 파일을 만들고이를 시작 점으로 사용 하 여 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="d41a5-120">승인자 역할이 있는 계정을 사용 하 여 GPO를 삭제 하 고 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![그룹 정책 개체 개발 프로세스](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="d41a5-122">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d41a5-122">Requirements</span></span>


<span data-ttu-id="d41a5-123">AGPM을 설치 하려는 컴퓨터는 다음 요구 사항을 충족 해야 하며이 시나리오에서 사용할 계정을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="d41a5-124">**참고**  AGPM 2.5을 설치 하 고 Windows Server® 2003에서 Windows Server2008 또는 WindowsVista®으로 업그레이드 하는 경우 WindowsVista 서비스 Pack1에 설치 된 서비스 팩이 없는 경우 AGPM 3.0으로 업그레이드 하기 전에 운영 체제를 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="d41a5-125">AGPM 서버 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d41a5-125">AGPM Server requirements</span></span>

<span data-ttu-id="d41a5-126">AGPM Server 3.0에는 Windows Server2008 또는 WindowsVista for Service Pack1 및 office RSAT (원격 서버 관리 도구)의 GPMC가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="d41a5-127">32 비트와 64 비트 버전이 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="d41a5-128">AGPM Server를 설치 하기 전에 먼저 도메인 관리자 그룹의 구성원 이어야 하 고 다른 언급이 없는 한 다음 Windows 기능이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="d41a5-129">GPMC</span><span class="sxs-lookup"><span data-stu-id="d41a5-129">GPMC</span></span>

    -   <span data-ttu-id="d41a5-130">Windows Server 2008: GPMC는 존재 하지 않는 경우 AGPM에 의해 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="d41a5-131">Windows Vista: AGPM을 설치 하기 전에 RSAT에서 GPMC를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="d41a5-132">자세한 내용은 <https://go.microsoft.com/fwlink/?LinkID=116179>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="d41a5-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="d41a5-133">.NET Framework 3.5</span></span>

<span data-ttu-id="d41a5-134">다음 Windows 기능은 AGPM 서버에 필요 하며, 없는 경우 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="d41a5-135">WCF 활성화, 비 HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="d41a5-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="d41a5-136">Windows Process Activation Service</span><span class="sxs-lookup"><span data-stu-id="d41a5-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="d41a5-137">프로세스 모델</span><span class="sxs-lookup"><span data-stu-id="d41a5-137">Process Model</span></span>

    -   <span data-ttu-id="d41a5-138">.NET 환경</span><span class="sxs-lookup"><span data-stu-id="d41a5-138">.NET Environment</span></span>

    -   <span data-ttu-id="d41a5-139">구성 Api</span><span class="sxs-lookup"><span data-stu-id="d41a5-139">Configuration APIs</span></span>

### <span data-ttu-id="d41a5-140">AGPM 클라이언트 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d41a5-140">AGPM Client requirements</span></span>

<span data-ttu-id="d41a5-141">AGPM 클라이언트 3.0에는 Windows Server2008 또는 WindowsVista 서비스 팩 1과 원격 서버 관리 도구 (RSAT)의 GPMC가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="d41a5-142">32 비트와 64 비트 버전이 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="d41a5-143">Agpm 클라이언트는 AGPM 서버를 실행 하는 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="d41a5-144">다음 Windows 기능은 AGPM 클라이언트에 필요 하며 다른 언급이 없는 한 없는 경우 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="d41a5-145">GPMC</span><span class="sxs-lookup"><span data-stu-id="d41a5-145">GPMC</span></span>

    -   <span data-ttu-id="d41a5-146">Windows Server 2008: GPMC는 존재 하지 않는 경우 AGPM에 의해 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="d41a5-147">Windows Vista: AGPM을 설치 하기 전에 RSAT에서 GPMC를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="d41a5-148">자세한 내용은 <https://go.microsoft.com/fwlink/?LinkID=116179>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="d41a5-149">.NET Framework 3.0</span><span class="sxs-lookup"><span data-stu-id="d41a5-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="d41a5-150">시나리오 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d41a5-150">Scenario requirements</span></span>

<span data-ttu-id="d41a5-151">이 시나리오를 시작 하기 전에 4 개의 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="d41a5-152">시나리오를 진행 하는 동안 다음 AGPM 역할 중 하나를 각 계정 (예: AGPM 관리자 (모든 권한), 승인자, 편집자, 검토자)에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="d41a5-153">이러한 계정은 전자 메일 메시지를 보내고 받을 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="d41a5-154">AGPM 관리자, 승인자 및 (선택적) 편집기 역할이 있는 계정에 대 한 **링크 gpo** 할당 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="d41a5-155">**참고** 
 **Gpo 링크** 권한은 기본적으로 도메인 관리자와 엔터프라이즈 관리자의 구성원에 게 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="d41a5-156">추가 사용자 또는 그룹 (예: AGPM 관리자 또는 승인자 역할을 가진 계정)에 대 한 **Gpo 링크** 사용 권한을 할당 하려면 도메인 노드를 클릭 한 다음 **위임** 탭을 클릭 하 고 **gpo 연결**을 선택 하 고 **추가**를 클릭 한 다음 사용 권한을 할당할 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="d41a5-157">AGPM 설치 및 구성 단계</span><span class="sxs-lookup"><span data-stu-id="d41a5-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="d41a5-158">AGPM을 설치 하 고 구성 하려면 다음 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="d41a5-159">1 단계: AGPM 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d41a5-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="d41a5-160">2 단계: AGPM 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="d41a5-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="d41a5-161">3 단계: AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="d41a5-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="d41a5-162">4 단계: 전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="d41a5-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="d41a5-163">5 단계: 대리인 액세스</span><span class="sxs-lookup"><span data-stu-id="d41a5-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="d41a5-164">1 단계: AGPM 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d41a5-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="d41a5-165">이 단계에서는 AGPM 서비스를 실행할 구성원 서버나 도메인 컨트롤러에 AGPM Server를 설치 하 고 보관 파일을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="d41a5-166">모든 AGPM 작업은이 Windows 서비스를 통해 관리 되며 서비스의 자격 증명을 사용 하 여 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="d41a5-167">AGPM 서버에서 관리 하는 보관 파일은 해당 서버나 같은 포리스트의 다른 서버에서 호스팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="d41a5-168">AGPM 서비스를 호스트 하는 컴퓨터에 AGPM Server를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="d41a5-169">Domain Admins 그룹의 구성원 인 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="d41a5-170">Microsoft 데스크톱 최적화 팩 CD를 시작 하 고 화면의 지침에 따라 **고급 그룹 정책 관리-서버**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="d41a5-171">**시작** 대화 상자에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="d41a5-172">**Microsoft 소프트웨어 사용 조건** 대화 상자에서 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="d41a5-173">**응용 프로그램 경로** 대화 상자에서 AGPM 서버를 설치할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="d41a5-174">AGPM 서버를 설치 하는 컴퓨터는 AGPM 서비스를 호스팅하고 보관 파일을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="d41a5-175">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-175">Click **Next**.</span></span>

6.  <span data-ttu-id="d41a5-176">**보관 경로** 대화 상자에서 AGPM 서버와 관련 된 보관 파일의 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="d41a5-177">보관 경로는 AGPM 서버 또는 다른 위치에 있는 폴더를 가리킬 수 있지만,이 AGPM 서버에서 관리 하는 모든 Gpo 및 기록 데이터를 저장할 충분 한 공간이 있는 위치를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="d41a5-178">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-178">Click **Next**.</span></span>

7.  <span data-ttu-id="d41a5-179">Agpm 서비스 **계정** 대화 상자에서 agpm 서비스가 실행 될 서비스 계정을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="d41a5-180">**보관 소유자** 대화 상자에서 먼저 AGPM 관리자 (전체 제어) 역할을 지정할 계정이 나 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="d41a5-181">이 AGPM 관리자는 agpm 관리자의 역할을 포함 하 여 다른 그룹 정책 관리자에 게 AGPM 역할 및 사용 권한을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="d41a5-182">이 시나리오에서는 AGPM 관리자 역할에서 사용할 계정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="d41a5-183">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-183">Click **Next**.</span></span>

9.  <span data-ttu-id="d41a5-184">**포트 구성** 대화 상자에서 AGPM 서비스가 수신 대기할 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="d41a5-185">포트 예외를 수동으로 구성 하거나 포트 예외를 구성 하는 규칙을 사용 하지 않는 한 **방화벽에 포트 예외 추가** 확인란의 선택을 취소 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="d41a5-186">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-186">Click **Next**.</span></span>

10. <span data-ttu-id="d41a5-187">**언어** 대화 상자에서 AGPM 서버용으로 설치할 표시 언어를 하나 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="d41a5-188">**설치**를 클릭 한 다음 **마침을** 클릭 하 여 설정 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="d41a5-189">**주의**  사항 운영 체제의 **관리 도구** 및 **서비스** 를 통해 AGPM 서비스에 대 한 설정을 수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="d41a5-190">이렇게 하면 AGPM 서비스를 시작 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="d41a5-191">서비스에 대 한 설정을 수정 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="d41a5-192">2 단계: AGPM 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="d41a5-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="d41a5-193">Gpo를 만들고, 편집 하 고, 배포 하 고, 검토 하거나, 삭제 하는 모든 그룹 정책 관리자는 Gpo를 관리 하는 데 사용 하는 컴퓨터에 AGPM 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="d41a5-194">이 시나리오에서는 하나 이상의 컴퓨터에 AGPM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="d41a5-195">그룹 정책 관리를 수행 하지 않는 최종 사용자의 컴퓨터에 AGPM 클라이언트를 설치할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="d41a5-196">그룹 정책 관리자의 컴퓨터에 AGPM 클라이언트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="d41a5-197">Microsoft 데스크톱 최적화 팩 CD를 시작 하 고 화면의 지침에 따라 **고급 그룹 정책 관리-클라이언트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="d41a5-198">**시작** 대화 상자에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="d41a5-199">**Microsoft 소프트웨어 사용 조건** 대화 상자에서 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="d41a5-200">**응용 프로그램 경로** 대화 상자에서 AGPM 클라이언트를 설치할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="d41a5-201">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-201">Click **Next**.</span></span>

5.  <span data-ttu-id="d41a5-202">**Agpm 서버** 대화 상자에 agpm 서버의 정규화 된 컴퓨터 이름과 연결할 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="d41a5-203">AGPM 서비스의 기본 포트는 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="d41a5-204">포트 예외를 수동으로 구성 하거나 규칙을 사용 하 여 포트 예외를 구성 하지 않는 한 **방화벽을 통해 Microsoft 관리 콘솔 허용** 확인란을 선택 취소 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="d41a5-205">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-205">Click **Next**.</span></span>

6.  <span data-ttu-id="d41a5-206">**언어** 대화 상자에서 AGPM 클라이언트에 대해 설치할 표시 언어를 하나 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="d41a5-207">**설치**를 클릭 한 다음 **마침을** 클릭 하 여 설정 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="d41a5-208">3 단계: AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="d41a5-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="d41a5-209">AGPM은 중앙 보관 저장소의 각 제어 된 그룹 정책 개체 (GPO)에 대 한 모든 버전을 저장 하므로, 그룹 정책 관리자는 각 GPO의 배포 된 버전에 즉시 영향을 주지 않고 Gpo를 오프 라인으로 보고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="d41a5-210">이 단계에서는 AGPM 서버 연결을 구성 하 고 모든 그룹 정책 관리자가 동일한 AGPM 서버에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="d41a5-211">(여러 AGPM 서버를 구성 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="d41a5-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="d41a5-212">모든 그룹 정책 관리자에 대해 AGPM 서버 연결을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="d41a5-213">AGPM 클라이언트를 설치한 컴퓨터에서 보관 소유자로 선택한 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="d41a5-214">이 사용자는 AGPM 관리자의 역할을 합니다 (모든 권한).</span><span class="sxs-lookup"><span data-stu-id="d41a5-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="d41a5-215">**시작**을 클릭 하 고 **관리 도구**를 가리켜 **그룹 정책 관리** 를 클릭 하 여 GPMC를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="d41a5-216">모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="d41a5-217">**그룹 정책 관리 편집기** 창에서 **사용자 구성**, **정책**, **관리 템플릿**, **Windows 구성 요소**및 **AGPM**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="d41a5-218">세부 정보 창에서 **agpm: 기본 Agpm 서버 (모든 도메인) 지정**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="d41a5-219">**속성** 창에서 **사용** 을 선택 하 고 보관을 호스트 하는 서버에 대 한 정규화 된 컴퓨터 이름 및 포트 (예: **server.contoso.com:4600**)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="d41a5-220">기본적으로 AGPM 서비스는 포트 4600를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="d41a5-221">**확인**을 클릭 한 다음 **그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="d41a5-222">그룹 정책이 업데이트 되 면 각 그룹 정책 관리자에 대해 AGPM 서버 연결이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="d41a5-223">4 단계: 전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="d41a5-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="d41a5-224">AGPM 관리자 (모든 권한)로, 요청이 포함 된 전자 메일 메시지가 있는 승인자 및 AGPM 관리자의 전자 메일 주소를 지정 하면 편집자는 해당 GPO를 만들거나, 배포 하거나, 삭제 하려고 할 때 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="d41a5-225">또한 이러한 메시지가 보내지는 별칭을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="d41a5-226">AGPM에 대 한 전자 메일 알림을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="d41a5-227">세부 정보 창에서 **도메인 위임** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="d41a5-228">보낸 사람 **전자 메일 주소** 필드에 알림을 보낼 AGPM의 전자 메일 별칭을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="d41a5-229">**대상 전자 메일 주소** 필드에 승인자 역할을 할당할 사용자 계정의 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="d41a5-230">**Smtp 서버** 필드에 유효한 SMTP 메일 서버를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="d41a5-231">**사용자 이름** 및 **암호** 필드에 SMTP 서비스에 대 한 액세스 권한이 있는 사용자의 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="d41a5-232">**적용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="d41a5-233">5 단계: 대리인 액세스</span><span class="sxs-lookup"><span data-stu-id="d41a5-233">Step 5: Delegate access</span></span>

<span data-ttu-id="d41a5-234">AGPM 관리자 (모든 권한)로 Gpo에 대 한 도메인 수준의 액세스를 위임 하 고 각 그룹 정책 관리자의 계정에 역할을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="d41a5-235">**참고**  도메인 수준이 아닌 GPO 수준에서 액세스를 위임할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="d41a5-236">자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d41a5-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="d41a5-237">**중요**  Gpo에 대 한 액세스의 AGPM 관리를 우회 하는 데 사용할 수 없으므로 그룹 정책 작성자 겸 소유자 그룹에서 구성원을 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="d41a5-238">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="d41a5-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="d41a5-239">도메인 전체의 모든 Gpo에 대 한 액세스 권한을 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="d41a5-240">**도메인 위임** 탭에서 **추가** 단추를 클릭 하 고 승인자 역할을 할 그룹 정책 관리자의 사용자 계정을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="d41a5-241">**그룹 또는 사용자 추가** 대화 상자에서 **승인자** 역할을 선택 하 여 해당 역할을 계정에 할당 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="d41a5-242">(이 역할에는 검토자 역할이 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="d41a5-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="d41a5-243">**추가** 단추를 클릭 하 고, 편집자 역할을 할 그룹 정책 관리자의 사용자 계정을 선택한 다음, **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="d41a5-244">**그룹 또는 사용자 추가** 대화 상자에서 **편집기** 역할을 선택 하 여 해당 역할을 계정에 할당 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="d41a5-245">(이 역할에는 검토자 역할이 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="d41a5-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="d41a5-246">**추가** 단추를 클릭 하 고 검토자 역할을 할 그룹 정책 관리자의 사용자 계정을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="d41a5-247">**그룹 또는 사용자 추가** 대화 상자에서 **검토자** 역할을 선택 하 여 해당 역할만 계정에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="d41a5-248">Gpo 관리 단계</span><span class="sxs-lookup"><span data-stu-id="d41a5-248">Steps for managing GPOs</span></span>


<span data-ttu-id="d41a5-249">AGPM을 사용 하 여 Gpo를 만들고, 편집 하 고, 검토 하 고, 배포 하려면 다음 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="d41a5-250">또한 템플릿을 만들고, GPO를 삭제 하 고, 삭제 된 GPO를 복원 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="d41a5-251">1 단계: GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="d41a5-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="d41a5-252">2 단계: GPO 편집</span><span class="sxs-lookup"><span data-stu-id="d41a5-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="d41a5-253">3 단계: GPO 검토 및 배포</span><span class="sxs-lookup"><span data-stu-id="d41a5-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="d41a5-254">4 단계: 서식 파일을 사용 하 여 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="d41a5-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="d41a5-255">5 단계: GPO 삭제 및 복원</span><span class="sxs-lookup"><span data-stu-id="d41a5-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="d41a5-256">1 단계: GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="d41a5-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="d41a5-257">여러 그룹 정책 관리자가 있는 환경에서 편집자 역할을 사용 하는 사용자는 새 Gpo 만들기를 요청할 수 있지만, 새 GPO 만들기가 프로덕션 환경에 영향을 주므로 승인자 역할을 가진 누군가가 이러한 요청을 승인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="d41a5-258">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 새 GPO 만들기를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="d41a5-259">승인자 역할이 있는 계정을 사용 하 여이 요청을 승인 하 고 GPO 만들기를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="d41a5-260">AGPM을 통해 관리 되는 새 GPO 만들기를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="d41a5-261">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="d41a5-262">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d41a5-263">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="d41a5-264">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="d41a5-265">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="d41a5-266">**Mygpo** 를 새 GPO의 이름으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="d41a5-267">새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="d41a5-268">새 GPO를 승인 즉시 프로덕션 환경에 배포 하려면 **라이브 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="d41a5-269">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="d41a5-270">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-271">**보류** 탭에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="d41a5-272">보류 중인 요청을 승인 하 여 GPO를 만드시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="d41a5-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="d41a5-273">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="d41a5-274">계정의 전자 메일 받은 편지함을 열고, 편집기의 요청에 맞게 AGPM 별칭 으로부터 전자 메일 메시지를 받았으며 GPO를 만들 수 있다는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="d41a5-275">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="d41a5-276">**콘텐츠** 탭에서 **보류 중** 탭을 클릭 하 여 보류 중인 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="d41a5-277">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **승인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="d41a5-278">**예** 를 클릭 하 여 GPO 만들기 승인을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="d41a5-279">GPO가 **제어** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="d41a5-280">2 단계: GPO 편집</span><span class="sxs-lookup"><span data-stu-id="d41a5-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="d41a5-281">Gpo를 사용 하 여 컴퓨터 또는 사용자 설정을 구성 하 고이를 여러 컴퓨터 또는 사용자에 게 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="d41a5-282">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 보관 저장소에서 GPO를 체크 아웃 하 고, GPO를 오프 라인으로 편집 하 고, 편집한 GPO를 보관 함으로 확인 하 고, GPO를 프로덕션 환경에 배포 하도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="d41a5-283">이 시나리오에서는 암호의 길이가 8 자 이상 이어야 하도록 GPO의 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="d41a5-284">편집을 위해 아카이브에 대해 GPO를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="d41a5-285">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="d41a5-286">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d41a5-287">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="d41a5-288">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="d41a5-289">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="d41a5-290">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-291">**제어** 탭에서 GPO의 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="d41a5-292">오프 라인으로 GPO를 편집 하 고 최소 암호 길이를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="d41a5-293">**제어** 탭에서 **mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **편집** 을 클릭 하 여 **그룹 정책 관리 편집기** 창을 열고 GPO의 오프 라인 복사본을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="d41a5-294">이 시나리오에서는 최소 암호 길이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="d41a5-295">**컴퓨터 구성**에서 **정책**, **Windows 설정**, **보안 설정**, **계정 정책**, **암호 정책을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="d41a5-296">세부 정보 창에서 **최소 암호 길이**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="d41a5-297">속성 창에서 **이 정책 설정 정의** 확인란을 선택 하 고 문자 수를 **8**로 설정한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="d41a5-298">**그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="d41a5-299">GPO를 보관 함으로 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="d41a5-300">**제어** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 하 고 **체크**인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="d41a5-301">메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="d41a5-302">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-303">**제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="d41a5-304">프로덕션 환경에 GPO 배포를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="d41a5-305">**제어** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="d41a5-306">이 계정은 승인자 또는 AGPM 관리자가 아니기 때문에 배포 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="d41a5-307">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="d41a5-308">GPO 기록에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="d41a5-309">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-310">**Mygpo** 가 **보류** 탭의 gpo 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="d41a5-311">3 단계: GPO 검토 및 배포</span><span class="sxs-lookup"><span data-stu-id="d41a5-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="d41a5-312">이 단계에서는 승인자 역할을 수행 하 고, 보고서를 만들고, GPO의 설정에 대 한 설정 및 변경 사항을 분석 하 여 승인 해야 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="d41a5-313">GPO를 평가한 후에는 프로덕션 환경에 배포 하 고 도메인 또는 ou (조직 구성 단위)에 연결 하 여 해당 도메인 또는 OU의 컴퓨터에 대 한 그룹 정책이 새로 고쳐질 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="d41a5-314">GPO의 설정을 검토 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="d41a5-315">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="d41a5-316">다른 모든 역할에 포함 되어 있는 검토자 역할을 사용 하는 모든 그룹 정책 관리자는 GPO의 설정을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="d41a5-317">계정에 대 한 전자 메일 받은 편지함을 열고, 편집기의 요청에 맞게 AGPM 별칭 으로부터 전자 메일 메시지를 받았으며 GPO를 배포 하는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="d41a5-318">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="d41a5-319">세부 정보 창의 **내용** 탭에서 **보류 중** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="d41a5-320">**Mygpo** 를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="d41a5-321">최신 버전의 MyGPO에서 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="d41a5-322">**기록** 창에서 최신 타임 스탬프가 있는 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **HTML 보고서** 를 클릭 하 여 gpo 설정 요약을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="d41a5-323">웹 브라우저에서 **모두 표시** 를 클릭 하 여 GPO의 모든 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="d41a5-324">브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-324">Close the browser.</span></span>

7. <span data-ttu-id="d41a5-325">최신 버전의 MyGPO를 보관 함으로 체크 인 된 첫 번째 버전과 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="d41a5-326">**기록** 창에서 최신 타임 스탬프가 있는 GPO 버전을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="d41a5-327">CTRL 키를 누르고 **컴퓨터 버전이** \* \* \\ \* \* \*가 아닌 가장 오래 된 GPO 버전을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="d41a5-328">**차이점** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-328">Click the **Differences** button.</span></span> <span data-ttu-id="d41a5-329">**계정 정책/암호 정책** 섹션이 녹색으로 강조 표시 되 고 그 앞에 **\ [+ \]** 가 선택 되어 있으며,이 설정은 GPO의 이후 버전 에서만 구성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="d41a5-330">**계정 정책/암호 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="d41a5-331">**최소 비밀 번호 길이** 설정도 녹색으로 강조 표시 되 고 앞에 **\ [+ \]** 가 있으면 GPO의 후자 버전 으로만 구성 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="d41a5-332">웹 브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-332">Close the Web browser.</span></span>

**<span data-ttu-id="d41a5-333">프로덕션 환경에 GPO를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="d41a5-334">**보류** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 한 다음 **승인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="d41a5-335">GPO 기록에 포함할 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="d41a5-336">**예**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-336">Click **Yes**.</span></span> <span data-ttu-id="d41a5-337">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-338">GPO가 프로덕션 환경에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="d41a5-339">GPO를 도메인 또는 조직 구성 단위에 연결 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="d41a5-340">GPMC에서 구성 된 GPO를 적용할 도메인 또는 OU를 마우스 오른쪽 단추로 클릭 하 고 **기존 Gpo 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="d41a5-341">**GPO 선택** 대화 상자에서 **mygpo**를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="d41a5-342">4 단계: 서식 파일을 사용 하 여 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="d41a5-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="d41a5-343">이 단계에서는 편집기 역할이 있는 계정을 사용 하 여 새 Gpo를 만들기 위한 시작 위치로 사용할 수 있는 GPO의 고정 되지 않은 정적 버전인 템플릿을 만든 다음 해당 서식 파일을 기반으로 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="d41a5-344">서식 파일은 동일한 설정이 여러 개 포함 된 여러 Gpo를 빠르게 만드는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="d41a5-345">기존 GPO를 기반으로 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="d41a5-346">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="d41a5-347">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d41a5-348">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="d41a5-349">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **서식 파일로 저장** 을 클릭 하 여 현재 mygpo에 있는 모든 설정을 통합 하는 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="d41a5-350">서식 파일과 메모의 이름으로 **MyTemplate** 를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="d41a5-351">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-352">**서식** 파일 탭에 새 서식 파일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="d41a5-353">AGPM을 통해 관리 되는 새 GPO 만들기를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="d41a5-354">**제어** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="d41a5-355">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="d41a5-356">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="d41a5-357">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="d41a5-358">**Myothergpo** 를 새 gpo의 이름으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="d41a5-359">새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="d41a5-360">새 GPO가 승인 즉시 프로덕션 환경에 배포 되도록 하려면 **라이브 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="d41a5-361">**GPO 서식 파일에서** **MyTemplate**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="d41a5-362">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="d41a5-363">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-364">**보류** 탭에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="d41a5-365">승인자 역할을 할당 받은 계정으로 [1 단계: Gpo 만들기](#bkmk-manage1)와 같이 보류 중인 요청을 승인 하 여 gpo를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="d41a5-366">MyTemplate는 MyGPO에서 구성한 모든 설정을 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="d41a5-367">MyOtherGPO는 MyTemplate를 사용 하 여 만들어졌기 때문에, 처음에는 MyTemplate가 생성 된 시점에 MyGPO에 포함 된 모든 설정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="d41a5-368">이는 차이 보고서를 생성 하 여 MyOtherGPO를 MyTemplate로 비교 하 여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="d41a5-369">편집을 위해 아카이브에 대해 GPO를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="d41a5-370">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="d41a5-371">**Myothergpo**를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="d41a5-372">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="d41a5-373">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-374">**제어** 탭에서 GPO의 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="d41a5-375">오프 라인으로 GPO를 편집 하 고 계정 잠금 기간을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="d41a5-376">**제어** 탭에서 **myothergpo**를 마우스 오른쪽 단추로 클릭 한 다음 **편집** 을 클릭 하 여 **그룹 정책 관리 편집기** 창을 열고 GPO의 오프 라인 복사본을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="d41a5-377">이 시나리오에서는 최소 암호 길이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="d41a5-378">**컴퓨터 구성**에서 **정책**, **Windows 설정**, **보안 설정**, **계정 정책**, **계정 잠금 정책을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="d41a5-379">세부 정보 창에서 **계정 잠금 기간**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="d41a5-380">속성 창에서 **이 정책 정의 설정을**선택 하 고 기간을 **30** 분으로 설정한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="d41a5-381">**그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="d41a5-382">[2 단계: GPO 편집](#bkmk-manage2)에서 myothergpo를 보관 및 요청 배포로 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="d41a5-383">MyOtherGPO를 MyGPO와 비교 하거나 차이 보고서를 사용 하 여 MyTemplate 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="d41a5-384">검토자 역할을 포함 하는 계정 (AGPM 관리자 \ [모든 권한 \], 승인자, 편집자 또는 검토자)이 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="d41a5-385">GPO와 다른 GPO를 비교 하 여 서식 파일에</span><span class="sxs-lookup"><span data-stu-id="d41a5-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="d41a5-386">MyGPO와 MyOtherGPO를 비교 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="d41a5-387">**제어** 탭에서 **mygpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="d41a5-388">CTRL 키를 누른 다음 **Myothergpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="d41a5-389">**Myothergpo**를 마우스 오른쪽 단추로 클릭 하 고 **차이**를 가리켜 **HTML 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="d41a5-390">MyOtherGPO와 MyTemplate를 비교 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="d41a5-391">**제어** 탭에서 **myothergpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="d41a5-392">**Myothergpo**를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 가리키는 다음 **서식 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="d41a5-393">**MyTemplate** 및 **HTML 보고서**를 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="d41a5-394">5 단계: GPO 삭제 및 복원</span><span class="sxs-lookup"><span data-stu-id="d41a5-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="d41a5-395">이 단계에서는 GPO를 삭제 하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="d41a5-396">GPO를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="d41a5-397">AGPM 클라이언트를 설치한 컴퓨터에서 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="d41a5-398">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d41a5-399">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="d41a5-400">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="d41a5-401">**보관 및 프로덕션에서 Gpo 삭제** 를 클릭 하 여 보관 저장소의 버전과 프로덕션 환경에서 배포 된 버전의 gpo를 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="d41a5-402">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="d41a5-403">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-404">GPO가 **제어** 탭에서 제거 되 고 **휴지통** 탭에 표시 되며 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="d41a5-405">필요에 따라 GPO를 삭제 한 후에도 가끔 검색을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="d41a5-406">이 단계에서는 삭제 된 GPO를 복원 하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="d41a5-407">삭제 된 GPO를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="d41a5-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="d41a5-408">**콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="d41a5-409">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **복원을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="d41a5-410">GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="d41a5-411">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-412">**휴지통** 탭에서 GPO가 제거 되 고 **제어** 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="d41a5-413">**참고**  GPO를 보관 함으로 복원 해도 자동으로 프로덕션 환경에 다시 배포 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="d41a5-414">GPO를 프로덕션 환경으로 반환 하려면 [3 단계: Gpo 검토 및 배포](#bkmk-manage3)와 같이 gpo를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="d41a5-415">GPO를 편집 하 고 배포 하면 GPO에 대 한 최근 변경 내용으로 인해 문제가 발생 한 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="d41a5-416">이 단계에서는 이전 버전의 GPO로 롤백하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="d41a5-417">GPO 기록의 모든 버전으로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="d41a5-418">메모 및 레이블을 사용 하 여 알려진 좋은 버전을 식별 하 고 특정 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="d41a5-419">이전 버전의 GPO로 롤백하는 방법</span><span class="sxs-lookup"><span data-stu-id="d41a5-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="d41a5-420">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="d41a5-421">**Mygpo** 를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="d41a5-422">배포할 버전을 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 한 다음 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="d41a5-423">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d41a5-424">**기록** 창에서 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="d41a5-425">**참고**  재배포 한 버전이 의도 된 버전 인지 확인 하려면 두 버전의 차이점 보고서를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="d41a5-426">GPO의 **기록** 창에서 두 버전을 선택 하 고 마우스 오른쪽 단추로 클릭 한 다음 **차이**를 가리킨 다음 **HTML 보고서** 또는 **XML 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d41a5-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





