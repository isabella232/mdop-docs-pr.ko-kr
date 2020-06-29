---
title: 단일 서버에서 MBAM을 설치 및 구성하는 방법
description: 단일 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824068"
---
# <span data-ttu-id="350d4-103">단일 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="350d4-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="350d4-104">이 항목의 절차에서는 단일 서버의 독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="350d4-105">단일 서버 구성은 테스트 환경 에서만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="350d4-106">프로덕션 환경의 경우 두 개 이상의 서버를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="350d4-107">Configuration Manager 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 하는 경우 [구성 관리자를 사용 하 여 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="350d4-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="350d4-108">다음 다이어그램에서는 단일 서버 아키텍처의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="350d4-109">데이터베이스 및 기능에 대 한 설명은 [MBAM 2.0의 상위 수준 아키텍처](high-level-architecture-for-mbam-20-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="350d4-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![mbam 2 단일 서버 배포 토폴로지](images/mbam2-1-server.gif)

<span data-ttu-id="350d4-111">각 서버 기능에는 특정 필수 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="350d4-112">필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md) 및 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="350d4-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="350d4-113">또한 일부 기능에는 설치 프로세스가 기능을 성공적으로 배포 하는 동안 제공 해야 하는 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="350d4-114">MBAM 배포를 시작 하기 전에 [mbam 2.0에 대 한 환경 준비](preparing-your-environment-for-mbam-20-mbam-2.md) 도 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="350d4-115">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-115">Note</span></span>**  
<span data-ttu-id="350d4-116">설치 로그 파일을 얻으려면 Msiexec package와/L location 옵션을 사용 하 여 **/L** &lt; &gt; mbam을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="350d4-117">로그 파일은 사용자가 지정한 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="350d4-118">추가 설치 로그 파일은 MBAM을 설치 하는 사용자 서버의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="350d4-119">단일 서버에 MBAM 서버 기능을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="350d4-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="350d4-120">다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="350d4-121">MBAM 서버 기능 설치를 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="350d4-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="350d4-122">MBAM을 설치 하려는 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="350d4-123">**시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="350d4-124">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="350d4-125">**토폴로지 선택** 페이지에서 **독립 실행형** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="350d4-126">**설치할 기능 선택** 페이지에서 설치할 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="350d4-127">기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="350d4-128">같은 컴퓨터에 설치할 기능을 동시에 함께 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="350d4-129">다른 곳에 설치 하려는 기능에 대 한 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="350d4-130">다음과 같은 순서로 MBAM 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="350d4-131">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="350d4-131">Recovery Database</span></span>

    -   <span data-ttu-id="350d4-132">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="350d4-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="350d4-133">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="350d4-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="350d4-134">셀프 서비스 서버</span><span class="sxs-lookup"><span data-stu-id="350d4-134">Self-Service Server</span></span>

    -   <span data-ttu-id="350d4-135">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="350d4-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="350d4-136">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="350d4-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="350d4-137">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-137">Note</span></span>**  
    <span data-ttu-id="350d4-138">설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="350d4-139">모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="350d4-140">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="350d4-141">이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="350d4-142">**네트워크 통신 보안 구성** 페이지에서 관리 및 모니터링 서버와 클라이언트의 웹 서비스 간 통신을 암호화할지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="350d4-143">통신을 암호화 하기로 결정 한 경우 암호화에 사용할 인증 기관 프로 비전 된 인증서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="350d4-144">이 단계를 수행 하기 전에 인증서를 만들어이 페이지에서 선택할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="350d4-145">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-145">Note</span></span>**  
    <span data-ttu-id="350d4-146">이 페이지는 **설치할 기능 선택** 페이지에서 셀프 서비스 포털 또는 관리 및 모니터링 서버 기능을 선택한 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="350d4-147">**다음**을 클릭 하 고 다음 단계 집합을 계속 진행 하 여 Mbam 서버 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="350d4-148">MBAM 서버 기능을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="350d4-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="350d4-149">**복구 데이터베이스 구성** 페이지에서 SQL Server 인스턴스 이름 및 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="350d4-150">또한 데이터베이스 파일의 위치와 로그 정보가 위치할 위치를 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="350d4-151">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="350d4-152">**준수 및 감사 데이터베이스 구성** 페이지에서 SQL Server 인스턴스 이름과 규정 준수 및 감사 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="350d4-153">또한 데이터베이스 파일을 어디에 저장 하 고 로그 정보가 어디에 있는지 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="350d4-154">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="350d4-155">준수 및 감사 **보고서 구성** 페이지에서 준수 및 감사 보고서가 설치 될 SQL Server Reporting Services 인스턴스를 지정 하 고 규정 준수 및 감사 데이터베이스에 액세스 하기 위한 도메인 사용자 계정 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="350d4-156">이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="350d4-157">사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="350d4-158">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="350d4-159">**셀프 서비스 포털 구성** 페이지에서 셀프 서비스 포털의 포트 번호, 호스트 이름, 가상 디렉터리 이름, 설치 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="350d4-160">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-160">Note</span></span>**  
    <span data-ttu-id="350d4-161">고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="350d4-162">Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="350d4-163">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="350d4-164">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="350d4-165">이 경우 Windows의 자동 업데이트는 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="350d4-166">**관리 및 모니터링 서버 구성** 페이지에서 지원 센터 웹 사이트의 포트 번호, 호스트 이름, 가상 디렉터리 이름, 설치 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="350d4-167">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-167">Note</span></span>**  
    <span data-ttu-id="350d4-168">고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="350d4-169">Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="350d4-170">**설치 요약** 페이지에서 설치할 기능 목록을 검토 하 고 **설치** 를 클릭 하 여 mbam 기능 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="350d4-171">설치 설정을 검토 하거나 변경 해야 하는 경우 **뒤로** 를 클릭 하 여 마법사를 뒤로 이동 하거나 **취소** 를 클릭 하 여 설치를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="350d4-172">설치 프로그램이 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="350d4-173">**마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="350d4-174">Microsoft BitLocker 관리 및 모니터링 서버 기능을 설치한 후에는 다음 섹션으로 이동 하 여 Microsoft BitLocker 관리 및 모니터링 역할에 사용자를 추가 하는 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="350d4-175">역할에 대 한 자세한 내용은 [MBAM 2.0 관리자 역할 계획](planning-for-mbam-20-administrator-roles-mbam-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="350d4-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="350d4-176">설치 후 구성을 수행 하려면</span><span class="sxs-lookup"><span data-stu-id="350d4-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="350d4-177">관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 지원 센터 웹 사이트 기능에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="350d4-178">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="350d4-179">드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="350d4-180">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="350d4-181">고급 헬프데스크 사용자의 경우 드라이브 복구에 **키 ID** 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="350d4-182">TPM 관리에서 **컴퓨터 도메인** 필드 및 **컴퓨터 이름** 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="350d4-183">관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 및 모니터링 웹 사이트의 보고서 기능에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="350d4-184">**Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트의 보고서 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="350d4-185">회사 이름, 고 지 사항 텍스트 및 기타 회사 관련 정보를 사용 하 여 셀프 서비스 포털에 브랜드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="350d4-186">자세한 내용은 [셀프 서비스 포털을 브랜딩 하는 방법](how-to-brand-the-self-service-portal.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="350d4-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="350d4-187">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-187">Note</span></span>**  
    <span data-ttu-id="350d4-188">**Mbam 보고서** 의 동일한 사용자 또는 그룹 구성원 자격 사용자 로컬 그룹은 Mbam 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 준수 및 감사 보고서가 설치 된 모든 컴퓨터에서 유지 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="350d4-189">이 작업을 수행 하는 데 권장 되는 방법은 도메인 보안 그룹을 만들고 해당 도메인 그룹을 각 로컬 MBAM 보고서 사용자 그룹에 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="350d4-190">이 프로세스를 사용 하는 경우 도메인 그룹을 통해 그룹 구성원 자격을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="350d4-191">MBAM 서버 기능 설치 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="350d4-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="350d4-192">Microsoft BitLocker 관리 및 모니터링 설치가 완료 되 면 설치 시 BitLocker 관리에 필요한 모든 필요한 MBAM 기능을 성공적으로 설정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="350d4-193">다음 절차를 사용 하 여 MBAM 서비스가 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="350d4-194">MBAM 서버 기능 설치의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="350d4-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="350d4-195">MBAM 기능이 배포 된 각 서버에서 **제어판**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="350d4-196">**프로그램**을 선택한 다음 **프로그램 및 기능**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="350d4-197">**Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="350d4-198">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-198">Note</span></span>**  
   <span data-ttu-id="350d4-199">설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="350d4-200">복구 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="350d4-201">준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태 데이터베이스가** 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="350d4-202">준수 및 감사 보고서가 설치 된 서버에서 관리 자격 증명으로 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="350d4-203">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.입니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="350d4-204">실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="350d4-205">Microsoft BitLocker 관리 및 모니터링 이라는 보고서 폴더에 **MaltaDataSource** 이라는 데이터 원본이 포함 되어 있고 **en-us** 폴더에 4 개의 보고서가 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="350d4-206">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-206">Note</span></span>**  
   <span data-ttu-id="350d4-207">SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 해야 합니다. http://\* &lt; NameofMBAMReportsServer &gt; */Reportent\_* &lt; srsinstancename &gt; \*</span><span class="sxs-lookup"><span data-stu-id="350d4-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="350d4-208">관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="350d4-209">**웹 서버 (iis)** 를 선택한 다음 **Iis (인터넷 정보 서비스) 관리자를 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="350d4-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="350d4-210">**연결** 에서 \* &lt; computername &gt; \*으로 이동 하 여 **사이트**를 선택한 다음 **Microsoft BitLocker 관리 및 모니터링**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="350d4-211">**MBAMAdministrationService**, **mbamusersupportservice**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="350d4-212">관리 및 모니터링 기능 및 셀프 서비스 포털이 설치 되어 있는 서버에서 관리 자격 증명을 사용 하는 웹 브라우저를 열고 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="350d4-213">*http:// &lt; 호스트 이름 &gt; /HelpDesk/default.aspx* 및 탐색 및 보고서에 대 한 각 링크 확인</span><span class="sxs-lookup"><span data-stu-id="350d4-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="350d4-214">http:// &lt; hostname &gt; /SelfService&gt;/</span><span class="sxs-lookup"><span data-stu-id="350d4-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="350d4-215">http:// &lt; computername &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="350d4-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="350d4-216">http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="350d4-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="350d4-217">http:// &lt; computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="350d4-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="350d4-218">http:// &lt; computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="350d4-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="350d4-219">참고</span><span class="sxs-lookup"><span data-stu-id="350d4-219">Note</span></span>**  
   <span data-ttu-id="350d4-220">네트워크 암호화 없이 기본 포트에 서버 기능이 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="350d4-221">다른 포트 또는 가상 디렉터리에 서버 기능을 설치한 경우 *http:// &lt; hostname &gt; : &lt; port &gt; /HelpDesk/default.asp*x 또는*http:// &lt; hostname &gt; : &lt; port &gt; / &lt; virtualdirectory &gt; /default.aspx* 와 같이 해당 포트를 포함 하도록 url을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="350d4-222">네트워크 암호화를 사용 하 여 서버 기능을 설치한 경우 http://을 https://로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="350d4-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="350d4-223">관련 항목</span><span class="sxs-lookup"><span data-stu-id="350d4-223">Related topics</span></span>


[<span data-ttu-id="350d4-224">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="350d4-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









