---
title: 분산 서버에서 MBAM을 설치 및 구성하는 방법
description: 분산 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824058"
---
# <span data-ttu-id="3d082-103">분산 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3d082-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="3d082-104">이 항목의 절차에서는 분산 서버의 독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0을 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="3d082-105">권장 아키텍처의 다이어그램을 보려면 데이터베이스 및 기능에 대 한 설명과 함께 [MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="3d082-106">Configuration Manager 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 하려면 [Configuration manager를 사용 하 여 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="3d082-107">각 서버 기능에는 특정 필수 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="3d082-108">필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md) 및 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="3d082-109">또한 일부 기능을 설치 하는 동안 특정 정보를 제공 해야 기능을 성공적으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="3d082-110">MBAM 배포를 시작 하기 전에 [mbam 2.0 서버 배포에 대 한 계획](planning-for-mbam-20-server-deployment-mbam-2.md) 도 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="3d082-111">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-111">Note</span></span>**  
<span data-ttu-id="3d082-112">설치 로그 파일을 얻으려면 Msiexec 패키지와 **/l** 위치 옵션을 사용 하 여 &lt; &gt; mbam을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="3d082-113">로그 파일은 사용자가 지정한 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="3d082-114">추가 설치 로그 파일은 MBAM을 설치 하는 사용자 서버의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="3d082-115">MBAM 서버 기능 배포</span><span class="sxs-lookup"><span data-stu-id="3d082-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="3d082-116">다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="3d082-117">MBAM 서버 설치 마법사 시작</span><span class="sxs-lookup"><span data-stu-id="3d082-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="3d082-118">Microsoft BitLocker 관리 및 모니터링을 설치 하려는 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="3d082-119">**시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3d082-120">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3d082-121">**토폴로지 선택** 페이지에서 **독립 실행형** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="3d082-122">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-122">Note</span></span>**  
    <span data-ttu-id="3d082-123">Configuration Manager 통합 토폴로지에 MBAM을 설치 하려면 [Configuration manager를 사용 하 여 Mbam 배포](deploying-mbam-with-configuration-manager-mbam2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="3d082-124">설치 하려는 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-124">Select the features that you want to install.</span></span> <span data-ttu-id="3d082-125">기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="3d082-126">다른 곳에 설치 하려는 기능을 선택 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="3d082-127">같은 컴퓨터에 설치 되는 기능은 동시에 함께 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="3d082-128">다음과 같은 순서로 MBAM 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="3d082-129">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="3d082-129">Recovery Database</span></span>

    -   <span data-ttu-id="3d082-130">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="3d082-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="3d082-131">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="3d082-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="3d082-132">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="3d082-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="3d082-133">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="3d082-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="3d082-134">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="3d082-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="3d082-135">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-135">Note</span></span>**  
    <span data-ttu-id="3d082-136">설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="3d082-137">모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="3d082-138">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="3d082-139">이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="3d082-140">복구 데이터베이스를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="3d082-141">**복구 데이터베이스 구성** 페이지에서 관리 및 모니터링 서버 기능을 실행 하는 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="3d082-142">관리 및 모니터링 서버 기능을 배포한 후에는 해당 도메인 계정을 사용 하 여 데이터베이스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="3d082-143">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="3d082-144">SQL Server 인스턴스 이름과 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="3d082-145">또한 데이터베이스를 찾을 위치와 로그 정보 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="3d082-146">MBAM 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="3d082-147">준수 및 감사 데이터베이스를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="3d082-148">**준수 및 감사 데이터베이스 구성** 페이지에서 보고서 데이터베이스에 액세스 하는 데 사용 될 사용자 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="3d082-149">관리 및 모니터링 서버를 실행 하는 컴퓨터의 컴퓨터 이름과 준수 및 감사 보고서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="3d082-150">관리 및 모니터링과 규정 준수 및 감사 보고서 서버는 배포 된 후 도메인 계정을 사용 하 여 데이터베이스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="3d082-151">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-151">Note</span></span>**  
    <span data-ttu-id="3d082-152">준수 및 감사 보고서 기능 없이 준수 및 감사 데이터베이스를 설치 하는 경우 준수 및 감사 데이터베이스 컴퓨터에 예외를 추가 하 여 Microsoft SQL Server 포트에서 인바운드 트래픽을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="3d082-153">기본 포트 번호는 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="3d082-154">SQL Server 인스턴스 이름과 규정 준수 및 감사 데이터를 저장할 데이터베이스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="3d082-155">또한 데이터베이스 및 로그 정보의 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="3d082-156">Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="3d082-157">준수 및 감사 보고서를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="3d082-158">**준수 및 감사 보고서 구성** 페이지에서 &lt; &gt; 규정 준수 및 감사 데이터베이스가 설치 된 원격 SQL Server 인스턴스 이름 (예: ServerName)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="3d082-159">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-159">Note</span></span>**  
    <span data-ttu-id="3d082-160">관리 및 모니터링 서버 없이 규정 준수 및 감사 보고서를 설치 하는 경우 준수 및 감사 보고서 컴퓨터에 예외를 추가 하 여 보고 서버 포트에서 인바운드 트래픽을 사용할 수 있도록 설정 해야 합니다 (기본 포트는 80).</span><span class="sxs-lookup"><span data-stu-id="3d082-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="3d082-161">준수 및 감사 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="3d082-162">데이터베이스 이름은 기본적으로 MBAM 준수 상태 이지만, 준수 및 감사 데이터베이스를 설치할 때 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="3d082-163">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="3d082-164">준수 및 감사 보고서가 설치 될 SQL Server Reporting Services 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="3d082-165">준수 및 감사 데이터베이스에 액세스 하려면 도메인 사용자 계정 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="3d082-166">이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="3d082-167">사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="3d082-168">Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="3d082-169">셀프 서비스 포털을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="3d082-170">**셀프 서비스 포털 구성** 페이지에서 셀프 서비스 포털 및 관리 및 모니터링 서버 간의 통신을 선택적으로 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="3d082-171">통신을 암호화 하는 옵션을 선택 하면 암호화에 사용할 인증 기관 프로 비전 된 인증서를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="3d082-172">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="3d082-173">준수 및 감사 데이터베이스가 설치 된 SQL Server (예: \* &lt; ServerName &gt; \*)의 원격 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="3d082-174">준수 및 감사 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="3d082-175">기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="3d082-176">그러나 준수 및 감사 데이터베이스를 설치할 때 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="3d082-177">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="3d082-178">복구 데이터베이스가 설치 된 SQL Server (예: \* &lt; ServerName &gt; \*)의 원격 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="3d082-179">복구 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="3d082-180">기본적으로 데이터베이스 이름은 **Mbam 복구 및 하드웨어**입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="3d082-181">그러나 복구 데이터베이스 기능을 설치할 때 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="3d082-182">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="3d082-183">**포트 번호**, **호스트 이름** (선택 사항), Mbam 관리 및 모니터링 서버의 **설치 경로** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="3d082-184">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-184">Note</span></span>**  
    <span data-ttu-id="3d082-185">고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="3d082-186">Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="3d082-187">셀프 서비스 포털의 SPN (서비스 사용자 이름)을 선택적으로 등록 하려면 **Active Directory를 사용 하 여이 컴퓨터의 spn (서비스 사용자 이름) 등록 (Windows 인증에 필요)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="3d082-188">이 확인란을 선택 하면 MBAM 설정이 기존 Spn을 등록 하려고 시도 하지 않으며, MBAM 설치 전이나 후에 SPN을 수동으로 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="3d082-189">수동으로 SPN을 등록 하는 방법에 대 한 지침은 [수동 SPN 등록](https://go.microsoft.com/fwlink/?LinkId=286758)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="3d082-190">Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="3d082-191">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="3d082-192">선택한 MBAM 기능 정보가 완료 되 면 설치 마법사를 사용 하 여 MBAM 설치를 시작할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="3d082-193">설치 설정을 검토 하거나 변경 해야 하는 경우 마법사를 이동 하려면 **뒤로** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="3d082-194">설치 **를 클릭 하** 여 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="3d082-195">마법사를 종료 하려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="3d082-196">설치 프로그램이 사용자가 선택한 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="3d082-197">**마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="3d082-198">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-198">Note</span></span>**  
    <span data-ttu-id="3d082-199">셀프 서비스 포털을 설치한 후 구성 하려면 회사 이름과 기타 회사 관련 정보를 사용 하 여 셀프 서비스 포털을 브랜딩 하는 방법에 대 한 자세한 내용은 [셀프 서비스 포털을 브랜딩](how-to-brand-the-self-service-portal.md) 하는 방법에 대 한 지침을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="3d082-200">클라이언트 컴퓨터가 특정 JavaScript 파일에 대 한 필수 액세스를 셀프 서비스 포털에 제공 하는 Microsoft Content Delivery Network (CDN)에 액세스할 수 있는 경우 셀프 서비스 포털 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="3d082-201">클라이언트 컴퓨터에 Microsoft CDN에 대 한 액세스 권한이 없는 경우 다음 섹션의 단계를 완료 하 여 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="3d082-202">최종 사용자가 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="3d082-203">클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크 (CDN)에 액세스할 수 있는 경우 셀프 서비스 포털에 특정 JavaScript 파일에 대 한 필수 액세스를 제공 하는 경우 셀프 서비스 포털 설치가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="3d082-204">클라이언트 컴퓨터에 Microsoft CDN에 대 한 액세스 권한이 없는 경우이 섹션의 나머지 단계를 완료 하 여 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="3d082-205">Microsoft CDN에서 4 개의 JavaScript 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="3d082-206">jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="3d082-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="3d082-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="3d082-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="3d082-208">MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="3d082-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="3d082-209">MicrosoftMvcValidation.js-</span><span class="sxs-lookup"><span data-stu-id="3d082-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="3d082-210">JavaScript 파일을 셀프 서비스 포털의 **Scripts** 디렉터리에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="3d082-211">이 디렉터리는 <em> &lt; mbam 셀프 서비스 설치 디렉터리 &gt; \\ </em> 셀프 서비스 Website\\Scripts.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="3d082-212">**IIS (인터넷 정보 서비스) 관리자**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="3d082-213">**사이트** &gt; **Microsoft BitLocker 관리 및 모니터링**을 확장 하 고 **SelfService**를 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="3d082-214">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-214">Note</span></span>**  
   <span data-ttu-id="3d082-215">*SelfService* 는 기본 가상 디렉터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="3d082-216">설치 중에이 디렉터리에 다른 이름을 선택한 경우에는이 지침의 나머지 부분에 있는 *SelfService* 을 선택한 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="3d082-217">가운데 창에서 **응용 프로그램 설정을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="3d082-218">다음 목록에 있는 각 항목에 대해 &lt; 가상 디렉터리를 &gt; /SelfService/(또는 설치 중 선택한 이름)로 대체 하 여 새 위치를 참조 하는 응용 프로그램 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="3d082-219">예를 들어 가상 디렉터리 경로는/selfservice/scripts/jquery-1.7.2.min.js와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="3d082-220">jQueryPath:/ &lt; virtual directory &gt; /Scripts/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="3d082-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="3d082-221">MicrosoftAjaxPath:/ &lt; virtual directory &gt; /Scripts/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="3d082-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="3d082-222">MicrosoftMvcAjaxPath:/ &lt; virtual directory &gt; /Scripts/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="3d082-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="3d082-223">MicrosoftMvcValidationPath:/ &lt; virtual directory &gt; /Scripts/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="3d082-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="3d082-224">관리 및 모니터링 서버 기능을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="3d082-225">MBAM은 웹 서비스와 관리 및 모니터링 서버 간의 통신을 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="3d082-226">통신을 암호화 하는 옵션을 선택 하면 암호화에 사용할 인증 기관 프로 비전 된 인증서를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="3d082-227">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="3d082-228">준수 및 감사 데이터베이스가 설치 된 SQL Server (예: \* &lt; ServerName &gt; \*)의 원격 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="3d082-229">준수 및 감사 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="3d082-230">기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="3d082-231">그러나 준수 및 감사 데이터베이스를 설치할 때 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="3d082-232">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="3d082-233">복구 데이터베이스가 설치 된 SQL Server의 원격 인스턴스 (예: \* &lt; ServerName &gt; \*)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="3d082-234">복구 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="3d082-235">기본적으로 데이터베이스 이름은 **Mbam 복구 및 하드웨어**입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="3d082-236">그러나 복구 데이터베이스 기능을 설치할 때 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="3d082-237">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="3d082-238">SQL Server Reporting Services (SRS) 사이트의 "홈"에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="3d082-239">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="3d082-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer</span><span class="sxs-lookup"><span data-stu-id="3d082-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="3d082-241">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-241">Note</span></span>**  
   <span data-ttu-id="3d082-242">SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; srsinstancename &gt; \*과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="3d082-243">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="3d082-244">**포트 번호**, **호스트 이름** (선택 사항), Mbam 관리 및 모니터링 서버의 **설치 경로** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="3d082-245">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-245">Note</span></span>**  
    <span data-ttu-id="3d082-246">고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="3d082-247">Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="3d082-248">셀프 서비스 포털의 SPN (서비스 사용자 이름)을 선택적으로 등록 하려면 **Active Directory를 사용 하 여이 컴퓨터의 spn (서비스 사용자 이름) 등록 (Windows 인증에 필요)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="3d082-249">이 확인란을 선택 하면 MBAM 설정이 기존 Spn을 등록 하려고 시도 하지 않으며, MBAM 설치 전이나 후에 SPN을 수동으로 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="3d082-250">수동으로 SPN을 등록 하는 방법에 대 한 지침은 [수동 SPN 등록](https://go.microsoft.com/fwlink/?LinkId=286758)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d082-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="3d082-251">Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="3d082-252">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="3d082-253">선택한 MBAM 기능 정보가 완료 되 면 설치 마법사를 사용 하 여 MBAM 설치를 시작할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="3d082-254">설치 설정을 검토 하거나 변경 해야 하는 경우 마법사를 이동 하려면 **뒤로** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="3d082-255">설치 하려면 **설치** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="3d082-256">마법사를 종료 하려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="3d082-257">설치 프로그램이 사용자가 선택한 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="3d082-258">**마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="3d082-259">설치 후 구성을 수행 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="3d082-260">관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 및 모니터링 웹 사이트의 기능에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="3d082-261">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="3d082-262">드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="3d082-263">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="3d082-264">고급 헬프데스크 사용자의 경우 드라이브 복구에 키 ID 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="3d082-265">**TPM 관리**에서 **컴퓨터 도메인** 필드 및 **컴퓨터 이름** 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="3d082-266">관리 및 모니터링 서버와 준수 및 감사 데이터베이스를 호스트 하는 서버와 규정 준수 및 감사 보고서를 호스팅하는 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 및 모니터링 웹 사이트의 보고서 기능에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="3d082-267">**Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트의 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="3d082-268">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-268">Note</span></span>**  
    <span data-ttu-id="3d082-269">**Mbam 보고서** 의 동일한 사용자 또는 그룹 구성원 자격을 가진 모든 컴퓨터에서 Mbam 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="3d082-270">MBAM 서버 기능 설치 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3d082-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="3d082-271">Microsoft BitLocker 관리 및 모니터링 서버 기능 설치가 완료 되 면 해당 설치가 MBAM에 대해 필요한 모든 기능을 성공적으로 설정 했는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="3d082-272">다음 절차를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 서비스가 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="3d082-273">MBAM 서버 설치의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="3d082-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="3d082-274">MBAM 기능이 배포 되는 각 서버에서 **제어판**을 열고 **프로그램**을 선택한 다음 **프로그램 및 기능**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="3d082-275">**Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="3d082-276">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-276">Note</span></span>**  
   <span data-ttu-id="3d082-277">MBAM 설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="3d082-278">복구 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="3d082-279">준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태 데이터베이스가** 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="3d082-280">준수 및 감사 보고서가 설치 된 서버에서 관리 자격 증명으로 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="3d082-281">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http://NameofMBAMReportsServer에서 찾을 수 있습니다 <em> &lt; &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="3d082-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="3d082-282">실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="3d082-283">**Microsoft BitLocker 관리 및 모니터링** 이라는 보고서 폴더에 **MaltaDataSource** 이라는 데이터 원본이 포함 되어 있고 **en-us** 폴더에 4 개의 보고서가 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="3d082-284">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-284">Note</span></span>**  
   <span data-ttu-id="3d082-285">SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; srsinstancename &gt; \*</span><span class="sxs-lookup"><span data-stu-id="3d082-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="3d082-286">관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="3d082-287">**웹 서버 (iis)** 를 선택한 다음 **Iis (인터넷 정보 서비스) 관리자**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="3d082-288">**연결**에서 \* &lt; computername &gt; \*으로 이동 하 여 **사이트**를 선택 하 고 **Microsoft BitLocker 관리 및 모니터링**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="3d082-289">**MBAMAdministrationService**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="3d082-290">관리 및 모니터링 기능 및 셀프 서비스 포털이 설치 되어 있는 서버에서 관리 자격 증명을 사용 하는 웹 브라우저를 열고 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="3d082-291">참고</span><span class="sxs-lookup"><span data-stu-id="3d082-291">Note</span></span>**  
   <span data-ttu-id="3d082-292">".Svc"로 끝나는 Url은 웹 사이트를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="3d082-293">성공 여부는 "이 서비스에 대 한 메타 데이터 게시가 현재 사용 하지 않도록 설정 되었습니다." 메시지나 코드와 유사한 정보로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="3d082-294">다른 오류 메시지가 표시 되거나 페이지를 찾을 수 없는 경우 페이지가 제대로 로드 되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="3d082-295">각 웹 페이지가 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d082-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="3d082-296">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3d082-296">Related topics</span></span>


[<span data-ttu-id="3d082-297">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="3d082-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









