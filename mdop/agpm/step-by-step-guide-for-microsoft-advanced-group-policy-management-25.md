---
title: Microsoft 고급 그룹 정책 관리 2.5 단계별 가이드
description: Microsoft 고급 그룹 정책 관리 2.5 단계별 가이드
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820193"
---
# <span data-ttu-id="719eb-103">Microsoft 고급 그룹 정책 관리 2.5 단계별 가이드</span><span class="sxs-lookup"><span data-stu-id="719eb-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="719eb-104">이 단계별 안내서는 GPMC (그룹 정책 관리 콘솔) 및 AGPM (고급 그룹 정책 관리)을 사용 하 여 그룹 정책 관리에 대 한 고급 기술을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="719eb-105">AGPM은 다음을 제공 하는 GPMC의 기능을 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="719eb-106">여러 그룹 정책 관리자에 대 한 Gpo (그룹 정책 개체)를 관리 하기 위한 사용 권한을 위임 하는 표준 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="719eb-107">그룹 정책 관리자가 프로덕션 환경에 배포 하기 전에 오프 라인으로 Gpo를 만들고 수정할 수 있는 보관 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="719eb-108">이전 버전의 GPO로 롤백하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="719eb-109">Gpo에 대 한 체크 인/체크 아웃 기능을 통해 그룹 정책 관리자가 실수로 서로의 작업을 덮어쓰지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="719eb-110">AGPM 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="719eb-110">AGPM scenario overview</span></span>


<span data-ttu-id="719eb-111">이 시나리오에서는 각 역할에 대해 개별 사용자 계정을 사용 하 여 다양 한 수준의 권한을 가진 여러 그룹 정책 관리자가 있는 환경에서 그룹 정책을 관리 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="719eb-112">구체적으로 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="719eb-113">Domain Admins 그룹의 구성원 인 계정을 사용 하 여 AGPM 서버를 설치 하 고 AGPM 관리자 역할을 계정이 나 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="719eb-114">AGPM 역할을 할당 하는 계정을 사용 하 여 AGPM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="719eb-115">AGPM 관리자 역할이 있는 계정을 사용 하 여 다른 계정에 역할을 할당 하 여 AGPM을 구성 하 고 Gpo에 대 한 액세스 권한을 대리인에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="719eb-116">편집자 역할이 있는 계정을 사용 하 여 GPO 만들기를 요청한 다음 승인자 역할이 있는 계정을 사용 하 여 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="719eb-117">편집자 계정으로 보관 함에서 GPO를 확인 하 고, GPO를 편집 하 고, GPO를 보관 함으로 확인 하 고, 배포를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="719eb-118">승인자 역할이 있는 계정을 사용 하 여 GPO를 검토 하 고 프로덕션 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="719eb-119">편집자 역할이 있는 계정을 사용 하 여 GPO 서식 파일을 만들고이를 시작 점으로 사용 하 여 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="719eb-120">승인자 역할이 있는 계정을 사용 하 여 GPO를 삭제 하 고 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![그룹 정책 개체 개발 프로세스](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="719eb-122">요구 사항</span><span class="sxs-lookup"><span data-stu-id="719eb-122">Requirements</span></span>


<span data-ttu-id="719eb-123">AGPM을 설치 하려는 컴퓨터는 다음 요구 사항을 충족 해야 하며이 시나리오에서 사용할 계정을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="719eb-124">AGPM 서버 요구 사항</span><span class="sxs-lookup"><span data-stu-id="719eb-124">AGPM Server requirements</span></span>

<span data-ttu-id="719eb-125">AGPM Server 2.5의 경우 서비스 팩이 설치 되어 있지 않거나 Windows Server® 2003 (32 비트 버전) 및 GPMC와 함께 WindowsVista® (32 비트 버전)이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="719eb-126">또한 AGPM 서버를 설치 하려면 Domain Admins 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="719eb-127">사용자에 게 제공 되 고 AGPM에서 지원 되는 최신 버전의 GPMC를 사용 하 여 구성원 서버나 도메인 컨트롤러에 AGPM 서버를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="719eb-128">AGPM은 GPMC를 사용 하 여 Gpo를 백업 및 복원 하 고 최신 버전의 GPMC는 이전 버전에서 사용할 수 없는 추가 정책 설정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="719eb-129">AGPM 서버의 GPMC 버전이 관리자가 그룹 정책을 관리 하는 데 사용 하는 컴퓨터의 버전 보다 오래 된 경우 AGPM 서버는 이전 버전의 GPMC에서 사용할 수 없는 정책 설정을 저장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="719eb-130">특히, AGPM 서버에서 Windows Server2003를 실행 하 고 있고 함께 제공 되는 GPMC 버전을 사용할 경우 그룹 정책 관리자의 컴퓨터에 WindowsVista와 함께 제공 되는 GPMC 버전이 실행 되 고 있는 경우에도 대부분의 정책 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="719eb-131">그러나 windows Vista의 GPMC에서 사용할 수 없는 windows Vista의 정책 설정 (예: 폴더 리디렉션, 무선 네트워킹 (IEEE 802.11) 및 배포 된 프린터)은 관리자가 컴퓨터에서 AGPM을 사용 하 여 구성할 수 있는 경우에도 AGPM 서버에서 저장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="719eb-132">이전 버전의 GPMC를 사용 하 여 그룹 정책 관리자가 실행 중인 컴퓨터에 AGPM Server를 설치 해야 하는 경우 그룹 정책 설정 참조를 참조 하 여 어떤 운영 체제에서 사용할 수 있는 정책 설정에 대 한 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="719eb-133">그룹 정책 설정 참조를 다운로드 하려면을 참조 <https://go.microsoft.com/fwlink/?LinkID=106147> 하세요.</span><span class="sxs-lookup"><span data-stu-id="719eb-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="719eb-134">**참고**  보관 파일은 AGPM 서버에서 마이그레이션하거나 Windows Server2003를 실행 하는 GPOVault 서버에서 WindowsVista를 실행 하는 AGPM 서버로 마이그레이션할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="719eb-135">Windows Server2003의 경우 AGPM 서버를 설치 하려는 컴퓨터에 GPOVault Server가 설치 되어 있으면 설치를 시작 하기 전에 GPOVault 서버를 제거 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="719eb-136">AGPM 서버를 설치 하면 GPOVault 서버가 제거 되 고 자동으로 기존 GPOVault 보관 데이터가 AGPM 보관 함으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="719eb-137">AGPM 클라이언트 요구 사항</span><span class="sxs-lookup"><span data-stu-id="719eb-137">AGPM Client requirements</span></span>

<span data-ttu-id="719eb-138">AGPM 클라이언트 2.5에는 서비스 팩이 설치 되어 있지 않거나 Windows Server2003 (32 비트 버전) 및 GPMC와 함께 WindowsVista (32 비트 버전)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="719eb-139">Agpm 클라이언트는 AGPM 서버를 실행 하는 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="719eb-140">시나리오 요구 사항</span><span class="sxs-lookup"><span data-stu-id="719eb-140">Scenario requirements</span></span>

<span data-ttu-id="719eb-141">이 시나리오를 시작 하기 전에 4 개의 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="719eb-142">시나리오를 진행 하는 동안 다음 AGPM 역할 중 하나를 각 계정 (예: AGPM 관리자 (모든 권한), 승인자, 편집자, 검토자)에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="719eb-143">이러한 계정은 전자 메일 메시지를 보내고 받을 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="719eb-144">AGPM 관리자, 승인자 및 (선택적) 편집기 역할이 있는 계정에 대 한 **링크 gpo** 할당 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="719eb-145">**참고** 
 **Gpo 링크** 권한은 기본적으로 도메인 관리자와 엔터프라이즈 관리자의 구성원에 게 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="719eb-146">추가 사용자 또는 그룹 (예: AGPM 관리자 또는 승인자 역할을 가진 계정)에 대 한 **Gpo 링크** 사용 권한을 할당 하려면 도메인 노드를 클릭 한 다음 **위임** 탭을 클릭 하 고 **gpo 연결**을 선택 하 고 **추가**를 클릭 한 다음 사용 권한을 할당할 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="719eb-147">이 시나리오에서는 다른 계정으로 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="719eb-148">표시 된 각 계정으로 로그온 하거나 다음 **으로 실행** 명령을 사용 하 여 표시 된 계정으로 GPMC를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="719eb-149">**참고**  Windows Server2003의 GPMC에서 다음 **으로 실행** 명령을 사용 하려면 **시작**을 클릭 하 고 **관리 도구**를 가리켜 **그룹 정책 관리**를 마우스 오른쪽 단추로 클릭 한 다음 다음 **으로 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="719eb-150">**다음 사용자** 를 클릭 하 고 계정에 대 한 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="719eb-151">Windows Vista의 GPMC에서 다음 **으로 실행** 명령을 사용 하려면 **시작** 단추를 클릭 하 고 **실행**을 선택한 다음 **runas/user:** <em> DomainName\\UserName </em> **"mmc%windir%\\system32\\gpmc.msc"** 를 입력 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="719eb-152">메시지가 표시 되 면 계정에 대 한 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="719eb-153">AGPM 설치 및 구성 단계</span><span class="sxs-lookup"><span data-stu-id="719eb-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="719eb-154">AGPM을 설치 하 고 구성 하려면 다음 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="719eb-155">1 단계: AGPM 서버 설치</span><span class="sxs-lookup"><span data-stu-id="719eb-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="719eb-156">2 단계: AGPM 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="719eb-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="719eb-157">3 단계: AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="719eb-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="719eb-158">4 단계: 전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="719eb-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="719eb-159">5 단계: 대리인 액세스</span><span class="sxs-lookup"><span data-stu-id="719eb-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="719eb-160">1 단계: AGPM 서버 설치</span><span class="sxs-lookup"><span data-stu-id="719eb-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="719eb-161">이 단계에서는 AGPM 서비스를 실행할 구성원 서버나 도메인 컨트롤러에 AGPM Server를 설치 하 고 보관 파일을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="719eb-162">모든 AGPM 작업은이 Windows 서비스를 통해 관리 되며 서비스의 자격 증명을 사용 하 여 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="719eb-163">AGPM 서버에서 관리 하는 보관 파일은 해당 서버나 같은 포리스트의 다른 서버에서 호스팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="719eb-164">AGPM 서비스를 호스트 하는 컴퓨터에 AGPM Server를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="719eb-165">Domain Admins 그룹의 구성원 인 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="719eb-166">Microsoft 데스크톱 최적화 팩 CD를 시작 하 고 화면의 지침에 따라 **고급 그룹 정책 관리-서버**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="719eb-167">**시작** 대화 상자에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="719eb-168">**Microsoft 소프트웨어 사용 조건** 대화 상자에서 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="719eb-169">**응용 프로그램 경로** 대화 상자에서 AGPM 서버를 설치할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="719eb-170">AGPM 서버를 설치 하는 컴퓨터는 AGPM 서비스를 호스팅하고 보관 파일을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="719eb-171">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-171">Click **Next**.</span></span>

6.  <span data-ttu-id="719eb-172">**보관 경로** 대화 상자에서 AGPM 서버와 관련 된 보관 파일의 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="719eb-173">보관 경로는 AGPM 서버 또는 다른 위치에 있는 폴더를 가리킬 수 있지만,이 AGPM 서버에서 관리 하는 모든 Gpo 및 기록 데이터를 저장할 충분 한 공간이 있는 위치를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="719eb-174">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-174">Click **Next**.</span></span>

7.  <span data-ttu-id="719eb-175">Agpm 서비스 **계정** 대화 상자에서 agpm 서비스가 실행 될 서비스 계정을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="719eb-176">**보관 소유자** 대화 상자에서 먼저 AGPM 관리자 (전체 제어) 역할을 지정할 계정이 나 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="719eb-177">이 AGPM 관리자는 agpm 관리자의 역할을 포함 하 여 다른 그룹 정책 관리자에 게 AGPM 역할 및 사용 권한을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="719eb-178">이 시나리오에서는 AGPM 관리자 역할에서 사용할 계정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="719eb-179">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-179">Click **Next**.</span></span>

9.  <span data-ttu-id="719eb-180">**설치**를 클릭 한 다음 **마침을** 클릭 하 여 설정 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="719eb-181">**주의**  사항 운영 체제의 **관리 도구** 및 **서비스** 를 통해 AGPM 서비스에 대 한 설정을 수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="719eb-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="719eb-182">이렇게 하면 AGPM 서비스를 시작 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="719eb-183">서비스에 대 한 설정을 수정 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="719eb-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="719eb-184">2 단계: AGPM 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="719eb-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="719eb-185">Gpo를 만들고, 편집 하 고, 배포 하 고, 검토 하거나, 삭제 하는 모든 그룹 정책 관리자는 Gpo를 관리 하는 데 사용 하는 컴퓨터에 AGPM 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="719eb-186">이 시나리오에서는 하나 이상의 컴퓨터에 AGPM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="719eb-187">그룹 정책 관리를 수행 하지 않는 최종 사용자의 컴퓨터에 AGPM 클라이언트를 설치할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="719eb-188">그룹 정책 관리자의 컴퓨터에 AGPM 클라이언트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="719eb-189">Microsoft 데스크톱 최적화 팩 CD를 시작 하 고 화면의 지침에 따라 **고급 그룹 정책 관리-클라이언트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="719eb-190">**시작** 대화 상자에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="719eb-191">**Microsoft 소프트웨어 사용 조건** 대화 상자에서 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="719eb-192">**응용 프로그램 경로** 대화 상자에서 AGPM 클라이언트를 설치할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="719eb-193">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-193">Click **Next**.</span></span>

5.  <span data-ttu-id="719eb-194">**Agpm 서버** 대화 상자에서 정규화 된 컴퓨터 이름과 연결할 AGPM 서버의 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="719eb-195">AGPM 서비스의 기본 포트는 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="719eb-196">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-196">Click **Next**.</span></span>

6.  <span data-ttu-id="719eb-197">**설치**를 클릭 한 다음 **마침을** 클릭 하 여 설정 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="719eb-198">3 단계: AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="719eb-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="719eb-199">AGPM은 중앙 보관 저장소의 각 제어 된 그룹 정책 개체 (GPO)에 대 한 모든 버전을 저장 하므로, 그룹 정책 관리자는 각 GPO의 배포 된 버전에 즉시 영향을 주지 않고 Gpo를 오프 라인으로 보고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="719eb-200">이 단계에서는 AGPM 서버 연결을 구성 하 고 모든 그룹 정책 관리자가 동일한 AGPM 서버에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="719eb-201">(여러 AGPM 서버를 구성 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="719eb-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="719eb-202">모든 그룹 정책 관리자에 대해 AGPM 서버 연결을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="719eb-203">AGPM 클라이언트를 설치한 컴퓨터에서 보관 소유자로 선택한 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="719eb-204">이 사용자는 AGPM 관리자의 역할을 합니다 (모든 권한).</span><span class="sxs-lookup"><span data-stu-id="719eb-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="719eb-205">**시작**을 클릭 하 고 **관리 도구**를 가리킵니다 **그룹 정책 관리** 를 클릭 하 여 **그룹 정책 관리 콘솔 (GPMC)** 을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="719eb-206">**그룹 정책 관리 콘솔** 트리에서 모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="719eb-207">**그룹 정책 개체 편집기** 창에서 **사용자 구성**, **관리 템플릿**, **Windows 구성 요소**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="719eb-208">**Windows 구성 요소**아래에 **AGPM** 이 표시 되지 않으면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="719eb-209">**관리 서식 파일** 을 마우스 오른쪽 단추로 클릭 하 고 **서식 파일 추가/제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="719eb-210">**추가**를 클릭 하 고 **agpm** 또는 **Agpm**을 선택 하 고 **열기**를 클릭 한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="719eb-211">**Windows 구성 요소**에서 **AGPM**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="719eb-212">세부 정보 창에서 **AGPM 서버 (모든 도메인)** 를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="719eb-213">**AGPM 서버 (모든 도메인) 속성** 창에서 **사용** 을 선택 하 고 보관을 호스트 하는 서버에 대 한 정규화 된 컴퓨터 이름 및 포트 (예: server.contoso.com:4600)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="719eb-214">AGPM 서비스에서 사용 되는 포트는 포트 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="719eb-215">**확인**을 클릭 한 다음 **그룹 정책 개체 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="719eb-216">그룹 정책이 업데이트 되 면 각 그룹 정책 관리자에 대해 AGPM 서버 연결이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="719eb-217">4 단계: 전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="719eb-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="719eb-218">AGPM 관리자 (모든 권한)로, 요청이 포함 된 전자 메일 메시지가 있는 승인자 및 AGPM 관리자의 전자 메일 주소를 지정 하면 편집자는 해당 GPO를 만들거나, 배포 하거나, 삭제 하려고 할 때 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="719eb-219">또한 이러한 메시지가 보내지는 별칭을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="719eb-220">AGPM에 대 한 전자 메일 알림을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="719eb-221">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="719eb-222">세부 정보 창에서 **도메인 위임** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="719eb-223">보낸 **사람** 필드에 알림을 보낼 AGPM의 전자 메일 별칭을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="719eb-224">**대상** 필드에 승인자 역할을 할당할 사용자 계정의 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="719eb-225">**Smtp 서버** 필드에 유효한 SMTP 메일 서버를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="719eb-226">**사용자 이름** 및 **암호** 필드에 SMTP 서비스에 대 한 액세스 권한이 있는 사용자의 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="719eb-227">**적용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="719eb-228">5 단계: 대리인 액세스</span><span class="sxs-lookup"><span data-stu-id="719eb-228">Step 5: Delegate access</span></span>

<span data-ttu-id="719eb-229">AGPM 관리자 (모든 권한)로 Gpo에 대 한 도메인 수준의 액세스를 위임 하 고 각 그룹 정책 관리자의 계정에 역할을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="719eb-230">**참고**  도메인 수준이 아닌 GPO 수준에서 액세스를 위임할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="719eb-231">자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="719eb-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="719eb-232">**중요**  Gpo에 대 한 액세스의 AGPM 관리를 우회 하는 데 사용할 수 없으므로 그룹 정책 작성자 겸 소유자 그룹에서 구성원을 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="719eb-233">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="719eb-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="719eb-234">도메인 전체의 모든 Gpo에 대 한 액세스 권한을 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="719eb-235">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="719eb-236">**도메인 위임** 탭에서 **고급** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="719eb-237">**사용 권한** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="719eb-238">그룹 정책 관리자의 사용자 계정을 클릭 한 다음 **승인자** 확인란을 선택 하 여 해당 역할을 계정에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="719eb-239">**편집기** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="719eb-240">(이 역할에는 검토자 역할이 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="719eb-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="719eb-241">다른 그룹 정책 관리자의 사용자 계정을 클릭 한 다음 **편집기** 확인란을 선택 하 여 해당 역할을 계정에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="719eb-242">(이 역할에는 검토자 역할이 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="719eb-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="719eb-243">세 번째 계정을 클릭 한 다음 **검토자** 확인란을 선택 하 여 검토자 역할만 해당 그룹 정책 관리자의 계정에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="719eb-244">**편집기** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="719eb-245">**고급** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="719eb-246">**고급 보안 설정** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="719eb-247">그룹 정책 관리자를 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="719eb-248">**적용 대상**에서 **이 개체 및 중첩 된 개체**를 선택 하 고 **사용 권한** **항목** 대화 상자에서 **확인** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="719eb-249">각 그룹 정책 관리자에 대해 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="719eb-250">**고급 보안 설정** 대화 상자에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="719eb-251">**사용 권한** 대화 상자에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="719eb-252">Gpo 관리 단계</span><span class="sxs-lookup"><span data-stu-id="719eb-252">Steps for managing GPOs</span></span>


<span data-ttu-id="719eb-253">AGPM을 사용 하 여 Gpo를 만들고, 편집 하 고, 검토 하 고, 배포 하려면 다음 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="719eb-254">또한 템플릿을 만들고, GPO를 삭제 하 고, 삭제 된 GPO를 복원 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="719eb-255">1 단계: GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="719eb-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="719eb-256">2 단계: GPO 편집</span><span class="sxs-lookup"><span data-stu-id="719eb-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="719eb-257">3 단계: GPO 검토 및 배포</span><span class="sxs-lookup"><span data-stu-id="719eb-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="719eb-258">4 단계: 서식 파일을 사용 하 여 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="719eb-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="719eb-259">5 단계: GPO 삭제 및 복원</span><span class="sxs-lookup"><span data-stu-id="719eb-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="719eb-260">1 단계: GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="719eb-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="719eb-261">여러 그룹 정책 관리자가 있는 환경에서 편집자 역할을 사용 하는 사용자는 새 Gpo 만들기를 요청할 수 있지만, 새 GPO 만들기가 프로덕션 환경에 영향을 주므로 승인자 역할을 가진 누군가가 이러한 요청을 승인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="719eb-262">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 새 GPO 만들기를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="719eb-263">승인자 역할이 있는 계정을 사용 하 여이 요청을 승인 하 고 GPO 만들기를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="719eb-264">AGPM을 통해 관리 되는 새 GPO 만들기를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="719eb-265">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="719eb-266">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="719eb-267">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="719eb-268">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="719eb-269">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="719eb-270">**Mygpo** 를 새 GPO의 이름으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="719eb-271">새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="719eb-272">새 GPO를 승인 즉시 프로덕션 환경에 배포 하려면 **라이브 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="719eb-273">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="719eb-274">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-275">**보류** 탭에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="719eb-276">보류 중인 요청을 승인 하 여 GPO를 만드시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="719eb-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="719eb-277">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="719eb-278">계정의 전자 메일 받은 편지함을 열고, 편집기의 요청에 맞게 AGPM 별칭 으로부터 전자 메일 메시지를 받았으며 GPO를 만들 수 있다는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="719eb-279">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="719eb-280">**콘텐츠** 탭에서 **보류 중** 탭을 클릭 하 여 보류 중인 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="719eb-281">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **승인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="719eb-282">**예** 를 클릭 하 여 GPO 만들기 승인을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="719eb-283">GPO가 **제어** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="719eb-284">2 단계: GPO 편집</span><span class="sxs-lookup"><span data-stu-id="719eb-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="719eb-285">Gpo를 사용 하 여 컴퓨터 또는 사용자 설정을 구성 하 고이를 여러 컴퓨터 또는 사용자에 게 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="719eb-286">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 보관 저장소에서 GPO를 체크 아웃 하 고, GPO를 오프 라인으로 편집 하 고, 편집한 GPO를 보관 함으로 확인 하 고, GPO를 프로덕션 환경에 배포 하도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="719eb-287">이 시나리오에서는 암호의 길이가 8 자 이상 이어야 하도록 GPO의 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="719eb-288">편집을 위해 아카이브에 대해 GPO를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="719eb-289">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="719eb-290">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="719eb-291">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="719eb-292">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="719eb-293">체크 아웃 된 동안 GPO **기록** 에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="719eb-294">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-295">**제어** 탭에서 GPO의 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="719eb-296">오프 라인으로 GPO를 편집 하 고 최소 암호 길이를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="719eb-297">**제어** 탭에서 **mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **편집** 을 클릭 하 여 **그룹 정책 개체 편집기** 창을 열고 GPO의 오프 라인 복사본을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="719eb-298">이 시나리오에서는 최소 암호 길이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="719eb-299">**컴퓨터 구성**에서 **Windows 설정을**두 번 클릭 하 고 **보안 설정을**두 번 클릭 한 다음 **계정 정책을**두 번 클릭 하 고 **암호 정책을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="719eb-300">세부 정보 창에서 **최소 암호 길이**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="719eb-301">속성 창에서 **이 정책 설정 정의** 확인란을 선택 하 고 문자 수를 **8**로 설정한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="719eb-302">**그룹 정책 개체 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="719eb-303">GPO를 보관 함으로 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="719eb-304">**제어** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 하 고 **체크**인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="719eb-305">메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="719eb-306">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-307">**제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="719eb-308">프로덕션 환경에 GPO 배포를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="719eb-309">**제어** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="719eb-310">이 계정은 승인자 또는 AGPM 관리자가 아니기 때문에 배포 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="719eb-311">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="719eb-312">GPO **기록** 에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="719eb-313">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-314">**Mygpo** 가 **보류** 탭의 gpo 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="719eb-315">3 단계: GPO 검토 및 배포</span><span class="sxs-lookup"><span data-stu-id="719eb-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="719eb-316">이 단계에서는 승인자 역할을 수행 하 고, 보고서를 만들고, GPO의 설정에 대 한 설정 및 변경 사항을 분석 하 여 승인 해야 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="719eb-317">GPO를 평가한 후에는 프로덕션 환경에 배포 하 고 도메인 또는 ou (조직 구성 단위)에 연결 하 여 해당 도메인 또는 OU의 컴퓨터에 대 한 그룹 정책이 새로 고쳐질 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="719eb-318">GPO의 설정을 검토 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="719eb-319">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="719eb-320">다른 모든 역할에 포함 되어 있는 검토자 역할을 사용 하는 모든 그룹 정책 관리자는 GPO의 설정을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="719eb-321">계정에 대 한 전자 메일 받은 편지함을 열고, 편집기의 요청에 맞게 AGPM 별칭 으로부터 전자 메일 메시지를 받았으며 GPO를 배포 하는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="719eb-322">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="719eb-323">세부 정보 창의 **내용** 탭에서 **보류 중** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="719eb-324">**Mygpo** 를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="719eb-325">최신 버전의 MyGPO에서 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="719eb-326">**기록** 창에서 최신 타임 스탬프가 있는 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **HTML 보고서** 를 클릭 하 여 gpo 설정 요약을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="719eb-327">웹 브라우저에서 **모두 표시** 를 클릭 하 여 GPO의 모든 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="719eb-328">브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-328">Close the browser.</span></span>

7.  <span data-ttu-id="719eb-329">최신 버전의 MyGPO를 보관 함으로 체크 인 된 첫 번째 버전과 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="719eb-330">**기록** 창에서 최신 타임 스탬프가 있는 GPO 버전을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="719eb-331">**CTRL** 키를 누르고 **체크**인 상태의 가장 오래 된 GPO 버전을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="719eb-332">**차이점** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-332">Click the **Differences** button.</span></span> <span data-ttu-id="719eb-333">**계정 정책/암호 정책** 섹션이 녹색으로 강조 표시 되 고 그 앞에 **\ [+ \]** 가 선택 되어 있으며,이 설정은 GPO의 이후 버전 에서만 구성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="719eb-334">**계정 정책/암호 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="719eb-335">**최소 비밀 번호 길이** 설정도 녹색으로 강조 표시 되 고 앞에 **\ [+ \]** 가 있으면 GPO의 후자 버전 으로만 구성 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="719eb-336">웹 브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-336">Close the Web browser.</span></span>

**<span data-ttu-id="719eb-337">프로덕션 환경에 GPO를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="719eb-338">**보류** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 한 다음 **승인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="719eb-339">GPO 기록에 포함할 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="719eb-340">**예**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-340">Click **Yes**.</span></span> <span data-ttu-id="719eb-341">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-342">GPO가 프로덕션 환경에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="719eb-343">GPO를 도메인 또는 조직 구성 단위에 연결 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="719eb-344">GPMC에서 구성 된 GPO를 적용할 도메인 또는 OU를 마우스 오른쪽 단추로 클릭 하 고 **기존 Gpo 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="719eb-345">**GPO 선택** 대화 상자에서 **mygpo**를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="719eb-346">4 단계: 서식 파일을 사용 하 여 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="719eb-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="719eb-347">이 단계에서는 편집기 역할이 있는 계정을 사용 하 여 새 Gpo를 만들기 위한 시작 위치로 사용할 수 있는 GPO의 고정 되지 않은 정적 버전인 템플릿을 만든 다음 해당 서식 파일을 기반으로 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="719eb-348">서식 파일은 동일한 설정이 여러 개 포함 된 여러 Gpo를 빠르게 만드는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="719eb-349">기존 GPO를 기반으로 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="719eb-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="719eb-350">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="719eb-351">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="719eb-352">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="719eb-353">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **서식 파일로 저장** 을 클릭 하 여 현재 mygpo에 있는 모든 설정을 통합 하는 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="719eb-354">서식 파일과 메모의 이름으로 **MyTemplate** 를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="719eb-355">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-356">**서식** 파일 탭에 새 서식 파일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="719eb-357">AGPM을 통해 관리 되는 새 GPO 만들기를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="719eb-358">**제어** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="719eb-359">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="719eb-360">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="719eb-361">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="719eb-362">**Myothergpo** 를 새 gpo의 이름으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="719eb-363">새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="719eb-364">새 GPO가 승인 즉시 프로덕션 환경에 배포 되도록 하려면 **라이브 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="719eb-365">**GPO 서식 파일에서** **MyTemplate**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="719eb-366">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="719eb-367">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-368">**보류** 탭에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="719eb-369">승인자 역할을 할당 받은 계정으로 [1 단계: Gpo 만들기](#bkmk-manage1)와 같이 보류 중인 요청을 승인 하 여 gpo를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="719eb-370">MyTemplate는 MyGPO에서 구성한 모든 설정을 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="719eb-371">MyOtherGPO는 MyTemplate를 사용 하 여 만들어졌기 때문에, 처음에는 MyTemplate가 생성 된 시점에 MyGPO에 포함 된 모든 설정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="719eb-372">이는 차이 보고서를 생성 하 여 MyOtherGPO를 MyTemplate로 비교 하 여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="719eb-373">편집을 위해 아카이브에 대해 GPO를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="719eb-374">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="719eb-375">**Myothergpo**를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="719eb-376">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="719eb-377">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-378">**제어** 탭에서 GPO의 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="719eb-379">오프 라인으로 GPO를 편집 하 고 계정 잠금 기간을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="719eb-380">**제어** 탭에서 **myothergpo**를 마우스 오른쪽 단추로 클릭 한 다음 **편집** 을 클릭 하 여 **그룹 정책 개체 편집기** 창을 열고 GPO의 오프 라인 복사본을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="719eb-381">이 시나리오에서는 최소 암호 길이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="719eb-382">**컴퓨터 구성**에서 **Windows 설정을**두 번 클릭 하 고 **보안 설정을**두 번 클릭 한 다음 **계정 정책을**두 번 클릭 하 고 **계정 잠금 정책을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="719eb-383">세부 정보 창에서 **계정 잠금 기간**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="719eb-384">속성 창에서 **이 정책 정의 설정을**선택 하 고 기간을 **30** 분으로 설정한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="719eb-385">**그룹 정책 개체 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="719eb-386">[2 단계: GPO 편집](#bkmk-manage2)에서 myothergpo를 보관 및 요청 배포로 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="719eb-387">MyOtherGPO를 MyGPO와 비교 하거나 차이 보고서를 사용 하 여 MyTemplate 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="719eb-388">검토자 역할을 포함 하는 계정 (AGPM 관리자 \ [모든 권한 \], 승인자, 편집자 또는 검토자)이 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="719eb-389">GPO와 다른 GPO를 비교 하 여 서식 파일에</span><span class="sxs-lookup"><span data-stu-id="719eb-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="719eb-390">MyGPO와 MyOtherGPO를 비교 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="719eb-391">**제어** 탭에서 **mygpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="719eb-392">**Ctrl** 키를 누른 다음 **myothergpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="719eb-393">**Myothergpo**를 마우스 오른쪽 단추로 클릭 하 고 **차이**를 가리켜 **HTML 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="719eb-394">MyOtherGPO와 MyTemplate를 비교 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="719eb-395">**제어** 탭에서 **myothergpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="719eb-396">**Myothergpo**를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 가리키는 다음 **서식 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="719eb-397">**MyTemplate** 및 **HTML 보고서**를 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="719eb-398">5 단계: GPO 삭제 및 복원</span><span class="sxs-lookup"><span data-stu-id="719eb-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="719eb-399">이 단계에서는 GPO를 삭제 하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="719eb-400">GPO를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="719eb-401">AGPM 클라이언트를 설치한 컴퓨터에서 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="719eb-402">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="719eb-403">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="719eb-404">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="719eb-405">**보관 및 프로덕션에서 Gpo 삭제** 를 클릭 하 여 보관 저장소의 버전과 프로덕션 환경에서 배포 된 버전의 gpo를 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="719eb-406">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="719eb-407">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-408">GPO가 **제어** 탭에서 제거 되 고 **휴지통** 탭에 표시 되며 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="719eb-409">필요에 따라 GPO를 삭제 한 후에도 가끔 검색을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="719eb-410">이 단계에서는 삭제 된 GPO를 복원 하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="719eb-411">삭제 된 GPO를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="719eb-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="719eb-412">**콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="719eb-413">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **복원을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="719eb-414">GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="719eb-415">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-416">**휴지통** 탭에서 GPO가 제거 되 고 **제어** 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="719eb-417">**참고**  GPO를 보관 함으로 복원 해도 자동으로 프로덕션 환경에 다시 배포 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="719eb-418">GPO를 프로덕션 환경으로 반환 하려면 [3 단계: Gpo 검토 및 배포](#bkmk-manage3)와 같이 gpo를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="719eb-419">GPO를 편집 하 고 배포 하면 GPO에 대 한 최근 변경 내용으로 인해 문제가 발생 한 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="719eb-420">이 단계에서는 이전 버전의 GPO로 롤백하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="719eb-421">GPO 기록의 모든 버전으로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="719eb-422">메모 및 레이블을 사용 하 여 알려진 좋은 버전을 식별 하 고 특정 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="719eb-423">이전 버전의 GPO로 롤백하는 방법</span><span class="sxs-lookup"><span data-stu-id="719eb-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="719eb-424">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="719eb-425">**Mygpo** 를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="719eb-426">배포할 버전을 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 한 다음 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="719eb-427">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="719eb-428">**기록** 창에서 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="719eb-429">**참고**  재배포 한 버전이 의도 된 버전 인지 확인 하려면 두 버전의 차이점 보고서를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="719eb-430">GPO의 **기록** 창에서 두 버전을 선택 하 고 마우스 오른쪽 단추로 클릭 한 다음 **차이**를 가리킨 다음 **HTML 보고서** 또는 **XML 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="719eb-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





