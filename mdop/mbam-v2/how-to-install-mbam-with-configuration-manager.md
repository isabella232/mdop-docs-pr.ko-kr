---
title: Configuration Manager를 사용하여 MBAM을 설치하는 방법
description: Configuration Manager를 사용하여 MBAM을 설치하는 방법
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825128"
---
# <span data-ttu-id="8c0f3-103">Configuration Manager를 사용하여 MBAM을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="8c0f3-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="8c0f3-104">이 섹션에서는 구성 관리자 [와 함께 MBAM을 사용 하](getting-started---using-mbam-with-configuration-manager.md)여 표시 되는 권장 구성을 사용 하 여 구성 관리자에 mbam을 설치 하는 단계에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="8c0f3-105">단계는 다음 작업으로 나뉘어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="8c0f3-106">Configuration Manager 서버에 MBAM 설치 및 구성</span><span class="sxs-lookup"><span data-stu-id="8c0f3-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="8c0f3-107">데이터베이스 서버에 복구 및 감사 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="8c0f3-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="8c0f3-108">관리 및 모니터링 서버에 관리 및 모니터링 서버 기능 설치</span><span class="sxs-lookup"><span data-stu-id="8c0f3-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="8c0f3-109">설치를 시작 하기 전에 필요한 mof 파일을 편집 하거나 만들었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="8c0f3-110">자세한 내용은 [Mof 파일을 만들거나 편집 하는 방법을](how-to-create-or-edit-the-mof-files.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="8c0f3-111">**중요**  기본이 아닌 SQL Server Reporting Services (SSRS) 인스턴스를 사용 하는 경우 다음 명령줄을 사용 하 여 MBAM 설정을 시작 해야 SSRS 명명 인스턴스를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="8c0f3-112">Configuration Manager 서버에 MBAM 설치</span><span class="sxs-lookup"><span data-stu-id="8c0f3-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="8c0f3-113">Configuration Manager 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="8c0f3-114">**참고**  설치 로그 파일을 얻으려면 Msiexec 패키지와 **/l** 위치 옵션을 사용 하 여 &lt; &gt; Configuration Manager를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="8c0f3-115">로그 파일은 사용자가 지정한 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="8c0f3-116">추가 설치 로그 파일은 Configuration Manager를 설치 하는 사용자의 컴퓨터에 있는% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="8c0f3-117">**시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="8c0f3-118">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="8c0f3-119">**토폴로지 선택** 페이지에서 **System Center Configuration Manager 통합**을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="8c0f3-120">**설치할 기능 선택** 페이지에서 **System Center Configuration Manager 통합**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="8c0f3-121">**참고**  **필수 구성 요소 확인** 페이지에서 설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 것이 없는지 여부를 클릭 하 여 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="8c0f3-122">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인** 을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="8c0f3-123">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="8c0f3-124">Microsoft 업데이트를 사용 해도 Windows의 자동 업데이트는 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="8c0f3-125">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="8c0f3-126">**설치 요약** 페이지에서 설치할 기능 목록을 검토 하 고 **설치** 를 클릭 하 여 mbam 기능 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="8c0f3-127">설치 설정을 검토 하거나 변경 해야 하는 경우 **뒤로** 를 클릭 하 여 마법사를 뒤로 이동 하거나 **취소** 를 클릭 하 여 설치를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="8c0f3-128">설치 프로그램이 MBAM 기능을 설치 하 고 설치가 완료 되었음을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="8c0f3-129">**마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="8c0f3-130">데이터베이스 서버에 복구 및 감사 데이터베이스를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="8c0f3-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="8c0f3-131">데이터베이스 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="8c0f3-132">**시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="8c0f3-133">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="8c0f3-134">**토폴로지 선택** 페이지에서 **System Center Configuration Manager 통합** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="8c0f3-135">설치할 기능 목록에서 **복구 데이터베이스** 와 **감사 데이터베이스**를 선택 하 고 나머지 기능을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="8c0f3-136">**참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="8c0f3-137">모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="8c0f3-138">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="8c0f3-139">이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="8c0f3-140">**복구 데이터베이스 구성** 페이지에서 관리 및 모니터링 서버 기능을 실행 하는 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="8c0f3-141">관리 및 모니터링 서버 기능을 배포한 후에는 해당 도메인 계정을 사용 하 여 데이터베이스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="8c0f3-142">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="8c0f3-143">SQL Server 인스턴스 이름과 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="8c0f3-144">또한 데이터베이스를 찾을 위치와 로그 정보 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="8c0f3-145">MBAM 설정 설치 마법사를 계속 하려면 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="8c0f3-146">**감사 데이터베이스 구성** 페이지에서 보고서 데이터베이스에 액세스 하는 데 사용 될 사용자 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="8c0f3-147">관리 및 모니터링 서버와 감사 보고서를 실행 하는 컴퓨터의 컴퓨터 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="8c0f3-148">관리 및 모니터링 및 감사 보고서 기능을 배포한 후에는 해당 도메인 계정이 데이터베이스에 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="8c0f3-149">**참고**  감사 보고서 기능 없이 감사 데이터베이스를 설치 하는 경우 감사 데이터베이스 컴퓨터에 예외를 추가 하 여 Microsoft SQL Server 포트에서 인바운드 트래픽을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="8c0f3-150">기본 포트 번호는 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="8c0f3-151">SQL Server 인스턴스 이름과 감사 데이터를 저장 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="8c0f3-152">또한 데이터베이스 및 로그 정보의 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="8c0f3-153">설치 **를 클릭 하** 여 설치를 시작 하 고 **마침을** 클릭 하 여 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="8c0f3-154">관리 및 모니터링 서버에 관리 및 모니터링 서버 기능을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="8c0f3-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="8c0f3-155">관리 및 모니터링 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="8c0f3-156">**시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="8c0f3-157">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="8c0f3-158">**토폴로지 선택** 페이지에서 **System Center Configuration Manager 통합** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="8c0f3-159">설치할 기능 목록에서 **관리 및 모니터링 서버** 및 **셀프 서비스 포털**을 선택 하 고 나머지 기능을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="8c0f3-160">**참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="8c0f3-161">모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="8c0f3-162">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="8c0f3-163">이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="8c0f3-164">[분산 서버에 MBAM을 설치 하 고 구성 하는 방법](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md)에 대 한 **셀프 서비스 포털 설치** 섹션의 단계에 따라 셀프 서비스 포털을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="8c0f3-165">**참고**  클라이언트 컴퓨터에 CDN (Microsoft Content Delivery Network)에 대 한 액세스 권한이 없는 경우 특정 JavaScript 파일에 대 한 필수 액세스를 셀프 서비스 포털에 제공 하는 **경우, 최종 사용자가 Microsoft 콘텐츠 배달 네트워크 섹션에 액세스할 수 없는 경우 셀프 서비스 포털을 구성** 하려면 다음 단계를 완료 하세요. 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 하기 위해 [분산 된 서버에 Mbam을 설치 하 고 구성 하는 방법에 대해](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="8c0f3-166">[분산 서버에 MBAM을 설치 하 고 구성 하는 방법](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md)의 **관리 및 모니터링 서버 기능 설치** 방법 섹션에 나와 있는 단계를 따라 관리 및 모니터링 서버 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="8c0f3-167">**마침을** 클릭 하 여 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c0f3-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="8c0f3-168">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8c0f3-168">Related topics</span></span>


[<span data-ttu-id="8c0f3-169">Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법</span><span class="sxs-lookup"><span data-stu-id="8c0f3-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="8c0f3-170">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="8c0f3-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





