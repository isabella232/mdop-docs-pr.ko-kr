---
title: 이전 버전의 MBAM에서 업그레이드
description: 이전 버전의 MBAM에서 업그레이드
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823808"
---
# <span data-ttu-id="3ca68-103">이전 버전의 MBAM에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="3ca68-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="3ca68-104">다음을 수행 하 여 독립 실행형 토폴로지 또는 구성 관리자 토폴로지와 함께 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 MBAM 2.0으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="3ca68-105">**수동 현재 위치 서버 대체** – Mbam 서버를 업그레이드 하려면 설치 관리자 또는 제어판을 사용 하 여 mbam을 수동으로 제거한 다음 mbam 2.0 인프라를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="3ca68-106">데이터베이스를 제거할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-106">You do not have to remove the databases.</span></span> <span data-ttu-id="3ca68-107">MBAM 1.0 서버를 제거 하면 MBAM 데이터베이스가 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="3ca68-108">MBAM 1.0에서 사용 하는 것과 동일한 데이터베이스를 지정 하는 경우 MBAM 2.0 설치는 데이터베이스에서 MBAM 1.0 데이터를 유지 하 고 데이터베이스를 MBAM 2.0과 작동 하도록 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="3ca68-109">**분산 클라이언트 업그레이드** -단독 mbam 토폴로지를 사용 하는 경우 mbam 2.0 서버 인프라를 설치한 후에 Mbam 클라이언트를 점차적으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="3ca68-110">MBAM 2.0 서버는 기존 클라이언트의 버전을 감지 하 고 2.0 클라이언트로 업그레이드 하는 데 필요한 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="3ca68-111">MBAM 2.0 서버 인프라를 업그레이드 한 후에는 mbam 1.0 클라이언트가 MBAM 2.0 서버에 성공적으로 보고 하지만 복구 데이터를 escrowing, 준수는 MBAM 1.0의 정책에 기반 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="3ca68-112">클라이언트 컴퓨터가 MBAM 2.0 정책에 대 한 준수를 정확 하 게 보고 하도록 클라이언트를 MBAM 2.0으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="3ca68-113">이전 클라이언트를 제거 하지 않고 MBAM 2.0 클라이언트로 클라이언트를 업그레이드 하면 클라이언트가 MBAM 2.0 정책을 적용 하 고 보고 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="3ca68-114">구성 관리자에서 MBAM을 사용 하는 경우 mbam 클라이언트를 MBAM 2.0으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="3ca68-115">두 서버 아키텍처에서 MBAM 업그레이드</span><span class="sxs-lookup"><span data-stu-id="3ca68-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="3ca68-116">서버가 Microsoft SQL Server 구성 요소를 호스팅하고 다른 서버가 웹 사이트 및 서비스를 호스팅하는 두 서버 아키텍처를 사용 하는 경우 다음 지침을 사용 하 여 이전 버전의 MBAM에서 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="3ca68-117">두 서버 아키텍처에서 MBAM을 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="3ca68-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="3ca68-118">SQL Server 기능을 사용 하는 서버의 제어판에서 **프로그램 및 기능**을 선택한 다음 **Microsoft BitLocker 관리 및 모니터링**을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="3ca68-119">복구 데이터베이스 및 준수 및 감사 데이터베이스는 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="3ca68-120">버전 MBAM 2.0에 대해 **MBAMSetup.exe** 를 실행 하 고, 선택적으로 **사용자 환경 개선 프로그램**을 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3ca68-121">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3ca68-122">**토폴로지 선택** 페이지에서 **독립 실행형** 또는 **System Center Configuration Manager 통합** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="3ca68-123">**설치할 기능 선택** 페이지에서 **셀프 서비스 서버** 및 **관리 및 모니터링 서버** 기능을 선택 취소 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="3ca68-124">필수 구성 요소 검사가 완료 될 때까지 기다린 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="3ca68-125">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="3ca68-126">**MBAM 데이터베이스에 액세스 하는 데 사용 되는 계정 제공** 페이지에서 사이트 및 서비스를 호스팅할 서버의 컴퓨터 이름을 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="3ca68-127">**복구 데이터베이스 구성** 페이지에서 SQL Server 인스턴스 이름 및 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="3ca68-128">또한 데이터베이스 파일과 로그 정보가 위치할 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="3ca68-129">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="3ca68-130">**준수 및 감사 데이터베이스 구성** 페이지에서 SQL Server 인스턴스 이름과 규정 준수 및 감사 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="3ca68-131">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="3ca68-132">준수 및 감사 **보고서 구성** 페이지에서 준수 및 감사 보고서가 설치 될 SQL Server Reporting Services 인스턴스를 지정 하 고 규정 준수 및 감사 데이터베이스에 액세스 하는 데 도메인 사용자 계정 및 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="3ca68-133">이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="3ca68-134">사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="3ca68-135">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="3ca68-136">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="3ca68-137">이 경우 Windows의 자동 업데이트는 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="3ca68-138">이전에이 제품 또는 다른 제품에 Microsoft 업데이트를 사용 하도록 선택한 경우 Microsoft 업데이트 페이지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="3ca68-139">**설치 요약** 페이지에서 설치할 기능을 검토 한 다음 **설치** 를 클릭 하 여 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="3ca68-140">관리 및 모니터링 서버 기능을 제거 하 고 업그레이드를 완료 하려면</span><span class="sxs-lookup"><span data-stu-id="3ca68-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="3ca68-141">관리 및 모니터링 서버 기능을 호스트 하는 컴퓨터의 제어판에서 **프로그램 및 기능**을 선택한 다음 mbam을 제거 하 여 이전에 설치 된 웹 사이트 및 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="3ca68-142">버전 2.0에 대 한 **MBAMSetup.exe** 를 실행 하 고, 선택적으로 **사용자 환경 개선 프로그램**을 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3ca68-143">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3ca68-144">**토폴로지 선택** 페이지에서 **독립 실행형** 또는 **System Center Configuration Manager 통합** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="3ca68-145">**설치할 기능 선택** 페이지에서 **복구 데이터베이스** 및 **준수 및 감사 데이터베이스** 및 **준수 및 감사 보고서** 기능을 지운 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="3ca68-146">필수 구성 요소 검사가 완료 될 때까지 기다린 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="3ca68-147">누락 된 필수 구성 요소가 발견 되 면 누락 된 필수 조건을 먼저 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="3ca68-148">**네트워크 통신 보안 구성** 페이지에서 웹 사이트 및 서비스에 SSL (Secure Socket Layer) 암호화를 사용할지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="3ca68-149">통신을 암호화 하기로 결정 한 경우 암호화에 사용할 CA (인증 기관) 인증서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="3ca68-150">**참고**  이 페이지에서 선택 하려면이 단계 전에 인증서를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="3ca68-151">**준수 상태 데이터베이스의 위치 구성** 페이지에서 SQL Server 인스턴스 이름과 준수 및 감사 데이터를 저장 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="3ca68-152">또한 데이터베이스 파일과 로그 정보가 위치할 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="3ca68-153">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="3ca68-154">**복구 데이터베이스 위치 구성** 페이지에서 SQL Server 인스턴스 이름과 복구 데이터를 저장 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="3ca68-155">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="3ca68-156">**준수 및 감사 보고서 구성** 페이지에서 다른 서버에서 구성한 보고 인스턴스의 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="3ca68-157">**테스트** 단추를 사용 하 여 사이트에 연결할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="3ca68-158">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="3ca68-159">**셀프 서비스 포털 구성** 페이지에서 셀프 서비스 포털의 포트 번호, 호스트 이름, 가상 디렉터리 이름, 설치 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="3ca68-160">**참고**  고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="3ca68-161">**관리 및 모니터링 서버 구성** 페이지에서 지원 센터 웹 사이트에 대해 원하는 가상 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="3ca68-162">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="3ca68-163">이 단계는 Windows의 자동 업데이트를 설정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="3ca68-164">이전에이 제품 또는 다른 제품에 Microsoft 업데이트를 사용 하도록 선택한 경우 Microsoft 업데이트 페이지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="3ca68-165">**설치 요약** 페이지에서 설치할 기능을 검토 한 다음 **설치** 를 클릭 하 여 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="3ca68-166">업그레이드가 성공적으로 수행 되었는지 확인 하려면 도메인의 다른 컴퓨터에서 각 사이트에 연결할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="3ca68-167">최종 사용자 컴퓨터에서 MBAM 클라이언트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="3ca68-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="3ca68-168">최종 사용자 컴퓨터를 MBAM 2.0 클라이언트로 업그레이드 하려면 각 클라이언트 컴퓨터에서 **MbamClientSetup.exe** 를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="3ca68-169">설치 관리자가 자동으로 MBAM 2.0 클라이언트로 클라이언트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="3ca68-170">Active Directory 도메인 서비스 또는 System Center Configuration Manager와 같은 도구인 전자 소프트웨어 배포 시스템을 통해 MBAM 클라이언트를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="3ca68-171">클라이언트 업그레이드의 유효성을 검사 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="3ca68-172">구성 된 보고 주기가 완료 될 때까지 기다린 다음 SQL Server 컴퓨터에서 **Sql Server Management Studio** 를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="3ca68-173">SQL Server 컴퓨터에서 **Sql Server Management Studio**를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="3ca68-174">**Recoveryand하드 Waa 컴퓨터** 테이블에 최종 사용자의 컴퓨터 이름이 표시 되는 행이 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca68-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="3ca68-175">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3ca68-175">Related topics</span></span>


[<span data-ttu-id="3ca68-176">MBAM 2.0 배포</span><span class="sxs-lookup"><span data-stu-id="3ca68-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





