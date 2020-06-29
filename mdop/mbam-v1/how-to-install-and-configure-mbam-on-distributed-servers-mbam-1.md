---
title: 분산 서버에서 MBAM을 설치 및 구성하는 방법
description: 분산 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825658"
---
# <span data-ttu-id="577d2-103">분산 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="577d2-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="577d2-104">이 항목의 절차에서는 분산 서버의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능을 모두 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="577d2-105">각 서버 기능에는 특정 필수 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="577d2-106">필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="577d2-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="577d2-107">또한 일부 기능을 설치 하는 동안 특정 정보를 제공 해야 기능을 성공적으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="577d2-108">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-108">Note</span></span>**  
<span data-ttu-id="577d2-109">설치 로그 파일을 얻으려면 **msiexec** 패키지 및 \*\*/l &lt; 위치 &gt; \*\* 옵션을 사용 하 여 mbam을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="577d2-110">로그 파일은 사용자가 지정한 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="577d2-111">추가 설치 로그 파일은 MBAM 설치를 실행 하는 사용자 의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="577d2-112">MBAM 서버 기능 배포</span><span class="sxs-lookup"><span data-stu-id="577d2-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="577d2-113">다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="577d2-114">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-114">Note</span></span>**  
<span data-ttu-id="577d2-115">32 비트 서버와 64 비트 서버에서 64 비트 설정으로 32 비트 설치를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="577d2-116">MBAM 서버 기능을 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="577d2-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="577d2-117">MBAM 설치 마법사를 시작 하 고 시작 페이지에서 **설치** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="577d2-118">Microsoft 소프트웨어 사용 조건을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="577d2-119">기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="577d2-120">다른 곳에 설치 하려는 기능을 선택 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="577d2-121">동일한 컴퓨터에 설치 하려는 기능은 모두 동시에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="577d2-122">MBAM 기능은 다음 순서로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="577d2-123">복구 및 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="577d2-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="577d2-124">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="577d2-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="577d2-125">준수 감사 및 보고서</span><span class="sxs-lookup"><span data-stu-id="577d2-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="577d2-126">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="577d2-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="577d2-127">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="577d2-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="577d2-128">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-128">Note</span></span>**  
    <span data-ttu-id="577d2-129">설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="577d2-130">모든 필수 조건이 충족 되 면 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="577d2-131">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="577d2-132">이 시간에 모든 전제 조건이 충족 되 면 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="577d2-133">MBAM 설정 마법사가 선택한 기능에 대 한 설치 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="577d2-134">다음 섹션에서는 각 기능에 대 한 설치 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="577d2-135">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-135">Note</span></span>**  
    <span data-ttu-id="577d2-136">일반적으로 각 기능은 별도의 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="577d2-137">단일 서버에 여러 기능을 설치 하려는 경우 다음 단계 중 일부를 변경 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="577d2-138">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="577d2-139">선택한 MBAM 기능 정보가 완료 되 면 설치 마법사를 사용 하 여 MBAM 설치를 시작할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="577d2-140">설치 설정을 검토 하거나 변경 해야 하는 경우 마법사를 이동 하려면 **뒤로** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="577d2-141">설치를 **클릭 하 여 설치를 시작** 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="577d2-142">마법사를 종료 하려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="577d2-143">설치 프로그램이 사용자가 선택한 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="577d2-144">**마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="577d2-145">MBAM 서버 기능이 설치 된 후 적절 한 MBAM 역할에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="577d2-146">자세한 내용은 [MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="577d2-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="577d2-147">설치 후 구성</span><span class="sxs-lookup"><span data-stu-id="577d2-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="577d2-148">MBAM 설정이 완료 되 면 사용자가 MBAM 관리 웹 사이트의 기능에 액세스할 수 있으려면 먼저 사용자 역할을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="577d2-149">관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="577d2-150">**Mbam 하드웨어 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 하드웨어 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="577d2-151">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 드라이브 복구 및 TPM (신뢰할 수 있는 플랫폼 모듈) 기능을 관리 하는 방법에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="577d2-152">드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="577d2-153">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="577d2-154">고급 헬프데스크 사용자의 경우 드라이브 복구에 키 ID 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="577d2-155">TPM 관리에서 컴퓨터 도메인 필드 및 컴퓨터 이름 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="577d2-156">관리 및 모니터링 서버, 준수 및 감사 데이터베이스에서 준수 및 감사 보고서를 호스팅하는 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 웹 사이트의 보고서 기능에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="577d2-157">**Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="577d2-158">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-158">Note</span></span>**  
    <span data-ttu-id="577d2-159">**Mbam 보고서** 의 동일한 사용자 또는 그룹 구성원 자격을 가진 모든 컴퓨터에서 Mbam 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="577d2-160">MBAM 서버 기능 설치의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="577d2-161">MBAM 서버 기능 설치가 완료 되 면 해당 설치가 MBAM에 대해 필요한 모든 기능을 성공적으로 설정 했는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="577d2-162">다음 절차를 사용 하 여 MBAM 서비스가 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="577d2-163">MBAM 설치의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="577d2-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="577d2-164">MBAM 기능이 배포 되는 각 서버에서 **제어판**을 열고 **프로그램**을 클릭 한 다음 **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="577d2-165">**Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="577d2-166">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-166">Note</span></span>**  
   <span data-ttu-id="577d2-167">MBAM 설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="577d2-168">복구 및 하드웨어 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="577d2-169">준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태** 데이터베이스가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="577d2-170">준수 및 감사 보고서가 설치 된 서버에서 관리자 권한이 있는 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="577d2-171">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="577d2-172">실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="577d2-173">**몰타 호환성 보고서** 가 나열 되어 있고 다섯 개의 보고서와 하나의 데이터 원본을 포함 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="577d2-174">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-174">Note</span></span>**  
   <span data-ttu-id="577d2-175">SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; srsinstancename &gt; \*</span><span class="sxs-lookup"><span data-stu-id="577d2-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="577d2-176">관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾아 **웹 서버 (IIS)** 를 선택한 다음 **iis (인터넷 정보 서비스) 관리자**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="577d2-177">**연결** 에서 \* &lt; computername &gt; \*으로 이동 하 고 **사이트**를 클릭 한 다음 **Microsoft BitLocker 관리 및 모니터링**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="577d2-178">**MBAMAdministrationService**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="577d2-179">관리 및 모니터링 기능이 설치 된 서버에서 관리자 권한으로 웹 브라우저를 열고 MBAM 웹 사이트에서 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="577d2-180">*http:// &lt; computername &gt; /default.aspx* 및 탐색 및 보고서에 대 한 각 링크 확인</span><span class="sxs-lookup"><span data-stu-id="577d2-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="577d2-181">http:// &lt; computername &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="577d2-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="577d2-182">http:// &lt; computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="577d2-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="577d2-183">http:// &lt; computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="577d2-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="577d2-184">참고</span><span class="sxs-lookup"><span data-stu-id="577d2-184">Note</span></span>**  
   <span data-ttu-id="577d2-185">일반적으로 서비스는 네트워크 암호화 없이 기본 포트 80에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="577d2-186">서비스가 다른 포트에 설치 되어 있는 경우 해당 포트를 포함 하도록 Url을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="577d2-187">예를 들어 http://\* &lt; computername &gt; : &lt; port &gt; \*/default.aspx 또는 http:// <em> &lt; hostheadername &gt; / </em> default.aspx</span><span class="sxs-lookup"><span data-stu-id="577d2-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="577d2-188">네트워크 암호화를 사용 하 여 서비스를 설치한 경우 http://를 https://로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="577d2-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="577d2-189">관련 항목</span><span class="sxs-lookup"><span data-stu-id="577d2-189">Related topics</span></span>


[<span data-ttu-id="577d2-190">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="577d2-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









