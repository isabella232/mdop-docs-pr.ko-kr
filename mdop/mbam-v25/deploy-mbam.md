---
title: 독립 실행형 구성에서 MBAM 2.5 배포
description: 독립 실행형 구성에서 MBAM 2.5를 배포 하는 방법을 소개 합니다.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826433"
---
# <span data-ttu-id="31333-103">독립 실행형 구성에서 MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="31333-103">Deploying MBAM 2.5 in a standalone configuration</span></span>

<span data-ttu-id="31333-104">이 문서에서는 독립 실행형 구성에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 설치 하는 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-104">This article provides step-by-step instructions for installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a standalone configuration.</span></span> <span data-ttu-id="31333-105">이 가이드에서는 2 서버 구성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-105">In this guide we will use a two-server configuration.</span></span> <span data-ttu-id="31333-106">두 서버 중 하나는 Microsoft SQL Server 2012를 실행 하는 데이터베이스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-106">One of the two servers will be a database server running Microsoft SQL Server 2012.</span></span> <span data-ttu-id="31333-107">이 서버는 MBAM 데이터베이스와 보고서를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-107">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="31333-108">추가 서버는 Windows Server 2012 웹 서버에서 "관리 및 모니터링 서버" 및 "셀프 서비스 포털"을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-108">The additional server will be a Windows Server 2012 web server hosting "Administration and Monitoring Server" and "Self-Service Portal."</span></span>

## <span data-ttu-id="31333-109">MBAM 2.5 서버 소프트웨어를 설치 하기 전의 준비 단계</span><span class="sxs-lookup"><span data-stu-id="31333-109">Preparation steps before installing MBAM 2.5 server software</span></span>

### <span data-ttu-id="31333-110">1 단계: 서버 설치 및 구성</span><span class="sxs-lookup"><span data-stu-id="31333-110">Step 1: Installation and configuration of servers</span></span>

<span data-ttu-id="31333-111">MBAM 2.5 구성을 시작 하기 전에 두 서버 모두 MBAM 시스템 요구 사항으로 구성 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-111">Before we start configuring MBAM 2.5, we have to make sure that both servers are configured as per MBAM system requirements.</span></span> <span data-ttu-id="31333-112">[Mbam 최소 시스템 요구 사항을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)확인 하 고 이러한 요구 사항을 충족 하는 구성을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-112">See the [MBAM minimum system requirements](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements), and select a configuration that meets these requirements.</span></span> 

#### <span data-ttu-id="31333-113">1.1 단계: 데이터베이스 및 보고 서버에 대 한 필수 구성 요소 배포</span><span class="sxs-lookup"><span data-stu-id="31333-113">Step 1.1: Deploying prerequisites for database and reporting server</span></span>

1. <span data-ttu-id="31333-114">Windows Server 2008 R2 이상) 운영 체제를 실행 하는 서버를 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-114">Install and configure a server running Windows Server 2008 R2 (or later) operating system.</span></span>

2. <span data-ttu-id="31333-115">Windows PowerShell 3.0를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-115">Install Windows PowerShell 3.0.</span></span>

3. <span data-ttu-id="31333-116">최신 서비스 팩이 포함 된 Microsoft SQL Server 2008 R2 이상 버전을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-116">Install Microsoft SQL Server 2008 R2 or a later version that includes the latest service pack.</span></span> <span data-ttu-id="31333-117">MBAM 용 SQL Server의 새 인스턴스를 설치 하는 경우 설치 하는 SQL Server에 SQL_Latin1_General_CP1_CI_AS 데이터 정렬이 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-117">If you are installing a new instance of SQL Server for MBAM, make sure the SQL Server you install includes the SQL_Latin1_General_CP1_CI_AS collation.</span></span> <span data-ttu-id="31333-118">다음 SQL Server 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-118">You’ll have to install the following SQL Server features:</span></span>

    * <span data-ttu-id="31333-119">데이터베이스 엔진</span><span class="sxs-lookup"><span data-stu-id="31333-119">Database Engine</span></span>
    * <span data-ttu-id="31333-120">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="31333-120">Reporting Services</span></span>
    * <span data-ttu-id="31333-121">클라이언트 도구 연결</span><span class="sxs-lookup"><span data-stu-id="31333-121">Client Tools Connectivity</span></span>
    * <span data-ttu-id="31333-122">관리 도구 – 완료</span><span class="sxs-lookup"><span data-stu-id="31333-122">Management Tools – Complete</span></span>

    > [!Note]
    > <span data-ttu-id="31333-123">필요에 따라 [SQL Server에 TDE (투명 데이터 암호화) 기능](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)을 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-123">Optionally, you can also install the [Transparent Data Encryption (TDE) feature in SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).</span></span>

    <span data-ttu-id="31333-124">SQL Server Reporting Services는 "기본" 모드에서 설치 및 구성 해야 하며,이는 설정 되지 않은 또는 "SharePoint" 모드에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-124">SQL Server Reporting Services must be installed and configured in "native" mode and not in unconfigured or "SharePoint" mode.</span></span>

    ![필요한 SQL Server 기능](images/deploying-MBAM-1.png)

4. <span data-ttu-id="31333-126">관리 및 모니터링 웹 사이트에 SSL을 사용 하려는 경우 관리 및 모니터링 웹 사이트를 구성 하기 전에 SSL (Secure Sockets layer) 프로토콜을 사용 하도록 SQL Server Reporting Services (SSRS)를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-126">If you plan to use SSL for the Administration and Monitoring website, make sure that you configure SQL Server Reporting Services (SSRS) to use the Secure Sockets Layer (SSL) protocol before you configure the Administration and Monitoring website.</span></span> <span data-ttu-id="31333-127">그렇지 않으면 보고서 기능에서 암호화 (HTTPS) 대신 부호화 되지 않은 (HTTP) 데이터 전송을 사용 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-127">Otherwise, the Reports feature will use unencrypted (HTTP) data transport instead of encrypted (HTTPS).</span></span>

    <span data-ttu-id="31333-128">기본 모드 보고서 서버에서 [Ssl 연결 구성을](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) 팔 로우 하 여 보고서 서버에서 ssl을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-128">You can follow [Configure SSL Connections](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) on a Native Mode Report Server to configure SSL on Report Server.</span></span>
    
    > [!Note]
    > <span data-ttu-id="31333-129">Sql server 설치 가이드의 각 버전의 SQL server를 참조 하 여 SQL Server를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-129">You can follow the SQL Server Installation Guide for your respective version of SQL Server to install SQL Server.</span></span> <span data-ttu-id="31333-130">링크는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-130">The links are as follows:</span></span>
        > * [<span data-ttu-id="31333-131">SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="31333-131">SQL Server 2014</span></span>](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [<span data-ttu-id="31333-132">SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="31333-132">SQL Server 2012</span></span>](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [<span data-ttu-id="31333-133">SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31333-133">SQL Server 2008 R2</span></span>](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. <span data-ttu-id="31333-134">SQL Server의 사후 설치에서 SQL Server에 사용자 계정을 프로 비전 하 고 데이터베이스 서버에서 MBAM 데이터베이스와 보고 역할을 구성할 사용자에 게 다음 사용 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-134">In the post-installation of SQL Server, make sure that you provision the user account in SQL Server, and assign the following permissions to the user who will configure the MBAM database and reporting roles on the database server.</span></span>

    <span data-ttu-id="31333-135">SQL Server 인스턴스의 역할:</span><span class="sxs-lookup"><span data-stu-id="31333-135">Roles for the instance of SQL Server:</span></span>
        
    * <span data-ttu-id="31333-136">dbcreator</span><span class="sxs-lookup"><span data-stu-id="31333-136">dbcreator</span></span>
    * <span data-ttu-id="31333-137">processadmin</span><span class="sxs-lookup"><span data-stu-id="31333-137">processadmin</span></span>

    <span data-ttu-id="31333-138">SQL Server Reporting Services 인스턴스에 대 한 권한:</span><span class="sxs-lookup"><span data-stu-id="31333-138">Rights for the instance of SQL Server Reporting Services:</span></span>
    
    * <span data-ttu-id="31333-139">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="31333-139">Create Folders</span></span>
    * <span data-ttu-id="31333-140">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="31333-140">Publish Reports</span></span>

<span data-ttu-id="31333-141">데이터베이스 서버는 MBAM 2.5 역할을 구성할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-141">Your database server is ready for configuration of MBAM 2.5 roles.</span></span> <span data-ttu-id="31333-142">다음 서버로 이동 하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-142">Let’s move to the next server.</span></span>

#### <span data-ttu-id="31333-143">1.2 단계: 관리 및 모니터링 서버에 대 한 필수 구성 요소 배포</span><span class="sxs-lookup"><span data-stu-id="31333-143">Step 1.2: Deploying prerequisites for administration and monitoring server</span></span>

<span data-ttu-id="31333-144">[Mbam 시스템 요구 사항 문서](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)에 설명 된 대로 하드웨어 구성을 충족 하는 서버를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-144">Choose a server that meets the hardware configuration as explained in the [MBAM system requirements document](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements).</span></span> <span data-ttu-id="31333-145">최신 서비스 팩과 업데이트를 사용 하 여 Windows Server 2008 R2 이상을 운영 체제에서 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-145">It must be running Windows Server 2008 R2 or a later operating system together with latest service pack and updates.</span></span> <span data-ttu-id="31333-146">서버가 준비 되 면 다음 역할 및 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-146">After the server is ready, install the following roles and features:</span></span>

##### <span data-ttu-id="31333-147">역할</span><span class="sxs-lookup"><span data-stu-id="31333-147">Roles</span></span>

* <span data-ttu-id="31333-148">웹 서버 (IIS) 관리 도구 (IIS 관리 스크립트 및 도구를 선택 합니다.)</span><span class="sxs-lookup"><span data-stu-id="31333-148">Web Server (IIS) Management Tools (Select IIS Management Scripts and Tools.)</span></span>

* <span data-ttu-id="31333-149">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="31333-149">Web Server Role Services</span></span>

    * <span data-ttu-id="31333-150">일반적인 HTTP 기능</span><span class="sxs-lookup"><span data-stu-id="31333-150">Common HTTP features</span></span><br />
      <span data-ttu-id="31333-151">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="31333-151">Static Content</span></span><br />
      <span data-ttu-id="31333-152">기본 문서</span><span class="sxs-lookup"><span data-stu-id="31333-152">Default Document</span></span>

    * <span data-ttu-id="31333-153">응용 프로그램 개발</span><span class="sxs-lookup"><span data-stu-id="31333-153">Application development</span></span><br />
      <span data-ttu-id="31333-154">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="31333-154">ASP.NET</span></span><br />
      <span data-ttu-id="31333-155">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="31333-155">.NET Extensibility</span></span><br />
      <span data-ttu-id="31333-156">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="31333-156">ISAPI Extensions</span></span><br />
      <span data-ttu-id="31333-157">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="31333-157">ISAPI Filters</span></span><br />
      <span data-ttu-id="31333-158">보안</span><span class="sxs-lookup"><span data-stu-id="31333-158">Security</span></span><br />
      <span data-ttu-id="31333-159">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="31333-159">Windows Authentication</span></span><br />
      <span data-ttu-id="31333-160">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="31333-160">Request Filtering</span></span>

    * <span data-ttu-id="31333-161">웹 서비스 IIS 관리 도구</span><span class="sxs-lookup"><span data-stu-id="31333-161">Web Service IIS Management Tools</span></span>

##### <span data-ttu-id="31333-162">기능</span><span class="sxs-lookup"><span data-stu-id="31333-162">Feature</span></span>

* <span data-ttu-id="31333-163">.NET Framework 4.5 기능</span><span class="sxs-lookup"><span data-stu-id="31333-163">.NET Framework 4.5 features</span></span>
  
  * <span data-ttu-id="31333-164">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="31333-164">Microsoft .NET Framework 4.5</span></span>
  
    <span data-ttu-id="31333-165">Windows Server 2012 또는 Windows Server 2012 R2의 경우 이러한 버전의 Windows Server에 대해 .NET Framework 4.5이 이미 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-165">For Windows Server 2012 or Windows Server 2012 R2, .NET Framework 4.5 is already installed for these versions of Windows Server.</span></span> <span data-ttu-id="31333-166">그러나이 기능을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-166">However, you must enable it.</span></span>
  
    <span data-ttu-id="31333-167">Windows Server 2008 R2의 경우 .NET Framework 4.5는 Windows Server 2008 R2에 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-167">For Windows Server 2008 R2, .NET Framework 4.5 is not included with Windows Server 2008 R2.</span></span> <span data-ttu-id="31333-168">따라서 .NET Framework 4.5을 다운로드 하 고 별도로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-168">So, you must download .NET Framework 4.5 and install it separately.</span></span>
  
  * <span data-ttu-id="31333-169">WCF 활성화</span><span class="sxs-lookup"><span data-stu-id="31333-169">WCF Activation</span></span><br />
    <span data-ttu-id="31333-170">HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="31333-170">HTTP Activation</span></span><br />
    <span data-ttu-id="31333-171">비 HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="31333-171">Non-HTTP Activation</span></span>
  
  * <span data-ttu-id="31333-172">TCP 활성화</span><span class="sxs-lookup"><span data-stu-id="31333-172">TCP Activation</span></span>
  
  * <span data-ttu-id="31333-173">Windows Process Activation Service:</span><span class="sxs-lookup"><span data-stu-id="31333-173">Windows Process Activation Service:</span></span><br />
    <span data-ttu-id="31333-174">프로세스 모델</span><span class="sxs-lookup"><span data-stu-id="31333-174">Process Model</span></span><br />
    <span data-ttu-id="31333-175">.NET Framework 환경</span><span class="sxs-lookup"><span data-stu-id="31333-175">.NET Framework Environment</span></span><br />
    <span data-ttu-id="31333-176">구성 Api</span><span class="sxs-lookup"><span data-stu-id="31333-176">Configuration APIs</span></span>

<span data-ttu-id="31333-177">셀프 서비스 포털을 사용 하려면 [ASP.NET MVC 4.0도 다운로드 하 여 설치](https://go.microsoft.com/fwlink/?linkid=392271)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-177">For the self-service portal to work, you should also [download and install ASP.NET MVC 4.0](https://go.microsoft.com/fwlink/?linkid=392271).</span></span>

<span data-ttu-id="31333-178">다음 단계는 Active Directory에서 필요한 MBAM 사용자 및 그룹을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-178">The next step is to create the required MBAM users and groups in Active Directory.</span></span>

### <span data-ttu-id="31333-179">2 단계: Active Directory 도메인 서비스에서 사용자 및 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="31333-179">Step 2: Creating users and groups in Active Directory Domain Services</span></span>
 
<span data-ttu-id="31333-180">필수 구성 요소의 일환으로, SQL Server 인스턴스에서 실행 되는 데이터베이스 및 관리 및 모니터링 서버에서 실행 되는 웹 응용 프로그램 등 특정 서버와 기능에 대 한 보안 및 액세스 권한을 제공 하기 위해 MBAM에서 사용 되는 특정 역할 및 계정을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-180">As part of the prerequisites, you must define certain roles and accounts that are used in MBAM to provide security and access rights to specific servers and features, such as the databases that are running on the instance of SQL Server and the web applications that are running on the Administration and Monitoring Server.</span></span>

<span data-ttu-id="31333-181">Active Directory에 다음 그룹 및 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31333-181">Create the following groups and users in Active Directory.</span></span> <span data-ttu-id="31333-182">(그룹 및 사용자에 대해 원하는 이름을 사용할 수 있습니다.) 사용자는 더 큰 사용자 권한을 가질 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-182">(You can use any name for the groups and users.) Users do not have to have greater user rights.</span></span> <span data-ttu-id="31333-183">도메인 사용자 계정으로 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-183">A domain user account is sufficient.</span></span> <span data-ttu-id="31333-184">MBAM 2.5 구성 중에 이러한 그룹의 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-184">You’ll have to specify the name of these groups during configuration of MBAM 2.5:</span></span>

* **<span data-ttu-id="31333-185">MBAMAppPool</span><span class="sxs-lookup"><span data-stu-id="31333-185">MBAMAppPool</span></span>**  

  <span data-ttu-id="31333-186">**유형**: 도메인 사용자</span><span class="sxs-lookup"><span data-stu-id="31333-186">**Type**: Domain User</span></span>

  <span data-ttu-id="31333-187">**설명**: 웹 응용 프로그램에서 해당 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록 준수 및 감사 데이터베이스와 복구 데이터베이스에 대 한 읽기 또는 쓰기 권한이 있는 도메인 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-187">**Description**: Domain user who has Read or Write permission to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span> <span data-ttu-id="31333-188">웹 응용 프로그램의 응용 프로그램 풀 에서도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-188">It will also be used by the application pool for the web applications.</span></span>

  <span data-ttu-id="31333-189">**계정 역할 (MBAM을 구성 하는 동안)**:</span><span class="sxs-lookup"><span data-stu-id="31333-189">**Account Roles (During Configuration of MBAM)**:</span></span>

  1. <span data-ttu-id="31333-190">웹 서비스 응용 프로그램 풀 도메인 계정</span><span class="sxs-lookup"><span data-stu-id="31333-190">Web service application pool domain account</span></span>

  2. <span data-ttu-id="31333-191">준수 및 감사 데이터베이스 및 복구 데이터베이스 보고서에 대 한 사용자 읽기/쓰기</span><span class="sxs-lookup"><span data-stu-id="31333-191">Compliance and Audit Database and Recovery Database read/write user for reports</span></span>

* **<span data-ttu-id="31333-192">MBAMROUser</span><span class="sxs-lookup"><span data-stu-id="31333-192">MBAMROUser</span></span>**

  <span data-ttu-id="31333-193">**유형**: 도메인 사용자</span><span class="sxs-lookup"><span data-stu-id="31333-193">**Type**: Domain User</span></span>

  <span data-ttu-id="31333-194">**설명**: 보고서에서이 데이터베이스의 규정 준수 및 감사 데이터에 액세스할 수 있도록 준수 및 감사 데이터베이스에 대 한 읽기 전용 액세스 권한을 갖는 도메인 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-194">**Description**: Domain user who will have Read-Only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span> <span data-ttu-id="31333-195">또한 로컬 SQL Server Reporting Services 인스턴스에서 규정 준수 및 감사 데이터베이스에 액세스 하는 데 사용 하는 도메인 사용자 계정도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-195">It will also be the domain user account that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span>

  <span data-ttu-id="31333-196">**계정 역할 (MBAM을 구성 하는 동안)**:</span><span class="sxs-lookup"><span data-stu-id="31333-196">**Account Roles (During Configuration of MBAM)**:</span></span>

  1. <span data-ttu-id="31333-197">보고서에 대 한 읽기 전용 사용자 준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="31333-197">Compliance and Audit Database read-only user for reports</span></span>

  2. <span data-ttu-id="31333-198">준수 및 감사 데이터베이스 도메인 사용자 계정</span><span class="sxs-lookup"><span data-stu-id="31333-198">Compliance and Audit Database domain user account</span></span>

* **<span data-ttu-id="31333-199">MBAMAdvHelpDsk</span><span class="sxs-lookup"><span data-stu-id="31333-199">MBAMAdvHelpDsk</span></span>**

  <span data-ttu-id="31333-200">**유형**: 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-200">**Type**: Domain Group</span></span>

  <span data-ttu-id="31333-201">**설명**: Mbam 헬프데스크 사용자 액세스 그룹: 구성원이 관리 및 모니터링 웹 사이트의 모든 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-201">**Description**: MBAM Advanced Helpdesk Users access group: Domain user group whose members have access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="31333-202">이 역할을 가진 사용자가 사용자의 도메인 및 사용자 이름 대신 복구 키만 입력 해야 하는 경우 사용자가 드라이브를 복구 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-202">Users who have this role have to enter only the recovery key, not the user’s domain and user name, when they are helping users recover their drives.</span></span> <span data-ttu-id="31333-203">사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 그룹 사용 권한 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-203">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span>

  <span data-ttu-id="31333-204">**계정 역할 (mbam을 구성 하는 동안)**: Mbam 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="31333-204">**Account Roles (During Configuration of MBAM)**: MBAM Advanced Helpdesk Users</span></span>

* **<span data-ttu-id="31333-205">Mbam</span><span class="sxs-lookup"><span data-stu-id="31333-205">MBAMHelpDsk</span></span>**

  <span data-ttu-id="31333-206">**유형**: 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-206">**Type**: Domain Group</span></span>

  <span data-ttu-id="31333-207">**설명**: Mbam 헬프데스크 사용자 액세스 그룹: 구성원이 mbam 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-207">**Description**: MBAM Helpdesk Users access group: Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="31333-208">이 역할이 있는 사용자는 두 옵션 중 하나를 사용할 때 모든 필드를 채워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-208">People who have this role must fill in all fields when they use either option.</span></span> <span data-ttu-id="31333-209">여기에는 사용자의 도메인 및 계정 이름이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-209">This includes the user’s domain and account name.</span></span>

  <span data-ttu-id="31333-210">**계정 역할 (mbam을 구성 하는 동안)**: Mbam 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="31333-210">**Account Roles (During Configuration of MBAM)**: MBAM Helpdesk Users</span></span>

* **<span data-ttu-id="31333-211">Mbam Grp</span><span class="sxs-lookup"><span data-stu-id="31333-211">MBAMRUGrp</span></span>**

  <span data-ttu-id="31333-212">**유형**: 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-212">**Type**: Domain Group</span></span>

  <span data-ttu-id="31333-213">**설명**: 구성원이 관리 및 모니터링 웹 사이트의 보고서 영역에 있는 보고서에 대해 읽기 전용으로 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-213">**Description**: Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span>

  <span data-ttu-id="31333-214">**계정 역할 (MBAM을 구성 하는 동안)**:</span><span class="sxs-lookup"><span data-stu-id="31333-214">**Account Roles (During Configuration of MBAM)**:</span></span>

  1. <span data-ttu-id="31333-215">읽기 전용 도메인 액세스 그룹 보고</span><span class="sxs-lookup"><span data-stu-id="31333-215">Reports read-only domain access group</span></span>

  2. <span data-ttu-id="31333-216">MBAM 보고서 사용자 액세스 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-216">MBAM Report Users access group</span></span>

### <span data-ttu-id="31333-217">3 단계 (선택 사항): 관리 및 모니터링 서버에 SSL 인증서 구성 및 설치</span><span class="sxs-lookup"><span data-stu-id="31333-217">Step 3 (Optional): Configure and install SSL certificate on administration and monitoring server</span></span>

<span data-ttu-id="31333-218">선택 사항 이지만, 인증서를 사용 하 여 MBAM 클라이언트와 관리 및 모니터링 웹 사이트와 셀프 서비스 포털 웹 사이트 간 통신을 보호 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-218">Although it’s optional, we highly recommend that you use a certificate to help secure the communication between the MBAM Client and the Administration and Monitoring Website and the Self-Service Portal websites.</span></span> <span data-ttu-id="31333-219">명백한 보안상의 이유로 자체 서명 된 인증서를 사용 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-219">We do not recommend that you use self-signed certificates because of obvious security reasons.</span></span> <span data-ttu-id="31333-220">신뢰할 수 있는 인증 기관에서 제공 하는 웹 서버 형식 인증서를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-220">We suggest that you use a Web Server Type Certificate from a trusted Certification Authority.</span></span> <span data-ttu-id="31333-221">이를 위해 [KB 2754259](https://support.microsoft.com/help/2754259)에서 "인증 기관에서 승인한 인증서 사용" 섹션을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-221">To do this, you can refer the "Using Certificate Approved by Certificate Authority" section from [KB 2754259](https://support.microsoft.com/help/2754259).</span></span>

<span data-ttu-id="31333-222">인증서가 발급 되 면 관리 및 모니터링 서버의 개인 저장소에 인증서를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-222">After the certificate is issued, you should add the certificate to the personal store of the Administration and Monitoring Server.</span></span> <span data-ttu-id="31333-223">인증서를 추가 하려면 로컬 컴퓨터에서 인증서 저장소를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="31333-223">To add the certificate, open the Certificates store on the local computer.</span></span> <span data-ttu-id="31333-224">이렇게 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="31333-224">To do this, follow these steps:</span></span>

1. <span data-ttu-id="31333-225">시작을 마우스 오른쪽 단추로 선택한 다음 실행을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-225">Right-select Start, and then select Run.</span></span>

   ![<span data-ttu-id="31333-226">선택</span><span class="sxs-lookup"><span data-stu-id="31333-226">Select</span></span> ](images/deploying-MBAM-2.png)

2. <span data-ttu-id="31333-227">"MMC.EXE" (따옴표 없이)을 입력 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-227">Type "MMC.EXE" (without the quotation marks), and then select **OK**.</span></span>

   ![실행 상자](images/deploying-MBAM-3.png) 

3. <span data-ttu-id="31333-229">새 MMC에서 연 **파일** 을 선택한 다음 **스냅인 추가/제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-229">Select **File** in the new MMC that you opened, and then select **Add/Remove Snap-in**.</span></span>
   
   ![선택](images/deploying-MBAM-4.png)

4. <span data-ttu-id="31333-231">**인증서** 스냅인을 강조 표시 한 다음 **추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-231">Highlight the **Certificates** snap-in, and then select **Add**.</span></span>

   ![스냅인 추가 또는 제거 창](images/deploying-MBAM-5.png)

5. <span data-ttu-id="31333-233">**컴퓨터 계정** 옵션을 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-233">Select the **Computer account** option, and then select **Next**.</span></span>
   
   ![인증서 스냅인 창](images/deploying-MBAM-6.png)

6. <span data-ttu-id="31333-235">다음 화면에서 **로컬 컴퓨터** 를 선택 하 고 **마침을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-235">Select **Local Computer** on the next screen, and then select **Finish**.</span></span>
   
   ![컴퓨터 창 선택](images/deploying-MBAM-7.png)

7. <span data-ttu-id="31333-237">이제 인증서 스냅인이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-237">You have now added the Certificates snap-in.</span></span> <span data-ttu-id="31333-238">이렇게 하면 컴퓨터의 인증서 저장소에 있는 모든 인증서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-238">This will enable you to work with any certificates in your computer's certificate store.</span></span>

   ![스냅인 추가 또는 제거 창](images/deploying-MBAM-8.png)

8. <span data-ttu-id="31333-240">컴퓨터의 인증서 저장소로 웹 서버 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31333-240">Import the web server certificate into your computer's certificate store.</span></span>

   <span data-ttu-id="31333-241">이제 인증서 스냅인에 대 한 액세스 권한이 있으므로, 웹 서버 인증서를 컴퓨터의 인증서 저장소로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-241">Now that you have access to the Certificates snap-in, you can import the web server certificate into your computer's certificate store.</span></span> <span data-ttu-id="31333-242">이렇게 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="31333-242">To do this, follow the next steps.</span></span>

9. <span data-ttu-id="31333-243">인증서 (로컬 컴퓨터) 스냅인을 열고 **Personal** 로 이동한 다음 **인증서**를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-243">Open the Certificates (Local Computer) snap-in, and browse to **Personal** and then **Certificates**.</span></span>
   
   ![인증서 (로컬 컴퓨터) 스냅인 창](images/deploying-MBAM-9.png)

   > [!Note]
   > <span data-ttu-id="31333-245">인증서 스냅인이 나열 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-245">The Certificates snap-in may not be listed.</span></span> <span data-ttu-id="31333-246">그렇지 않으면 인증서가 설치 되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-246">If it is not, no certificates are installed.</span></span>

10. <span data-ttu-id="31333-247">**인증서**를 마우스 오른쪽 단추로 선택 하 고 **모든 작업**을 선택한 다음 **가져오기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-247">Right-select **Certificates**, select **All Tasks**, and then select **Import**.</span></span>

    ![인증서 (로컬 컴퓨터) 스냅인 창](images/deploying-MBAM-10.png)

11. <span data-ttu-id="31333-249">마법사가 시작 되 면 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-249">When the wizard starts, select **Next**.</span></span> <span data-ttu-id="31333-250">서버 인증서와 개인 키를 포함 하 여 만든 파일을 찾은 후 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-250">Browse to the file that you created that contains your server certificate and private key, and then select **Next**.</span></span>

    ![인증서 가져오기 마법사 창](images/deploying-MBAM-11.png)

12. <span data-ttu-id="31333-252">파일을 만들 때 지정한 경우 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-252">Enter the password if you specified one for the file when you created it.</span></span>

   ![암호 입력 창](images/deploying-MBAM-12.png)

   > [!Note]
   > <span data-ttu-id="31333-254">이 컴퓨터에서 키 쌍을 다시 내보낼 수 있도록 하려면 내보내기 **가능한 키로 표시** 옵션이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-254">Make sure that the **Mark the key as exportable** option is selected if you want to be able to export the key pair again from this computer.</span></span> <span data-ttu-id="31333-255">보안을 강화 하기 위해이 옵션을 선택 하지 않고 개인 키를 백업할 수 없도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-255">As an added security measure, you may want to leave this option cleared to make sure that no one can make a backup of your private key.</span></span>
 
13. <span data-ttu-id="31333-256">**다음**을 선택 하 고 인증서를 저장 하려는 **인증서 저장소** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-256">Select **Next**, and then select the **Certificate Store** to which you want to save the certificate.</span></span>

    ![인증서 가져오기 마법사 창](images/deploying-MBAM-13.png)

    > [!Note]
    > <span data-ttu-id="31333-258">웹 서버 인증서 이기 때문에 **개인**을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-258">You should select **Personal**, because it is a web server certificate.</span></span> <span data-ttu-id="31333-259">인증서를 인증 계층 구조에 포함 한 경우에는이 저장소에도 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-259">If you included the certificate in the certification hierarchy, it will also be added to this store.</span></span>
 
14. <span data-ttu-id="31333-260">**다음**을 선택 하 고 **마침을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-260">Select **Next**, and then select **Finish**.</span></span>

    ![인증서 가져오기 마법사 창](images/deploying-MBAM-14.png)

<span data-ttu-id="31333-262">이제 웹 서버에 대 한 서버 인증서가 개인 인증서 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-262">You will now see the server certificate for your web server in the Personal Certificates list.</span></span> <span data-ttu-id="31333-263">서버의 일반 이름으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-263">It will be denoted by the common name of the server.</span></span> <span data-ttu-id="31333-264">(인증서의 제목 섹션에서 찾을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="31333-264">(You can find this in the subject section of the certificate.)</span></span>

<span data-ttu-id="31333-265">추가 참조:</span><span class="sxs-lookup"><span data-stu-id="31333-265">For further reference:</span></span>

[<span data-ttu-id="31333-266">MBAM 2.5 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="31333-266">MBAM 2.5 Security Considerations</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[<span data-ttu-id="31333-267">MBAM 웹 사이트를 보호하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="31333-267">Planning How to Secure the MBAM Websites</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

<span data-ttu-id="31333-268">다음 단계는 응용 프로그램 풀 계정에 대 한 서비스 주체 이름을 등록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-268">The next step is to register a service principle name for the application pool account.</span></span>

### <span data-ttu-id="31333-269">4 단계: MBAM 웹 서버용 SSL 인증서 구성</span><span class="sxs-lookup"><span data-stu-id="31333-269">Step 4: Configuring SSL certificate for MBAM Web Server</span></span>

<span data-ttu-id="31333-270">클라이언트와 서버 간의 SSL 통신을 사용 하는 경우 인증서에 확장 된 키 사용 Oid (1.3.6.1.5.5.7.3.1) 및 (1.3.6.1.5.5.7.3.2)가 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-270">If you are using SSL communication between the client and server, you should make sure that the certificate has Enhanced Key Usage OIDs (1.3.6.1.5.5.7.3.1) and (1.3.6.1.5.5.7.3.2).</span></span> <span data-ttu-id="31333-271">즉, 서버 인증 및 클라이언트 인증이 추가 되었는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-271">That is, you should make sure that Server Authentication and Client Authentication are added.</span></span>

<span data-ttu-id="31333-272">서비스 Url을 탐색 하려고 할 때 인증서 오류가 표시 되는 경우 다른 이름으로 발급 된 인증서를 사용 중이거나 잘못 된 URL을 사용 하 여 검색 하는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-272">If you receive a certificate error when you try to browse service URLs, you are using a certificate that was issued to a different name, or you are browsing by using an incorrect URL.</span></span>

<span data-ttu-id="31333-273">브라우저에 인증서 오류 메시지가 표시 되지만 계속할 수 있지만,이 경우 MBAM 웹 서비스는 인증서 오류를 무시 하지 않으며 연결이 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-273">Although the browser may prompt you with a certificate error message but let you continue, the MBAM web service will not ignore certificate errors and will block the connection.</span></span> <span data-ttu-id="31333-274">MBAM 클라이언트의 MBAM 관리자 이벤트 로그에서 인증서 관련 오류를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-274">You will notice certificate-related errors in the MBAM client’s MBAM Admin event log.</span></span> <span data-ttu-id="31333-275">별칭을 사용 하 여 관리 및 모니터링 서버에 연결 하는 경우 별칭 이름에 대 한 인증서를 발급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-275">If you are using an alias to connect to the Administration and Monitoring server, you should issue a certificate to the alias name.</span></span> <span data-ttu-id="31333-276">즉, 인증서의 주체 이름은 별칭 이름 이어야 하 고 로컬 서버의 DNS 이름은 인증서의 **주체 대체 이름** 필드에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-276">That is, the subject name of the certificate should be the alias name, and the local server’s DNS name should be added to the **Subject Alternative Name** field of the certificate.</span></span>

<span data-ttu-id="31333-277">예:</span><span class="sxs-lookup"><span data-stu-id="31333-277">Example:</span></span>

<span data-ttu-id="31333-278">가상 이름이 "bitlocker.contoso.com"이 고 MBAM 관리 및 모니터링 서버 이름이 "adminserver.contoso.com" 인 경우 인증서는 bitlocker.contoso.com (주체 이름)에 발급 되어야 하 고, adminserver.contoso.com는 인증서의 **주체 대체 이름** 필드에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-278">If the virtual name is "bitlocker.contoso.com" and the MBAM Administration and Monitoring server name is "adminserver.contoso.com," the certificate should be issued to bitlocker.contoso.com (subject name), and adminserver.contoso.com should be added to **Subject Alternative Name** field of the certificate.</span></span>

<span data-ttu-id="31333-279">마찬가지로 부하 분산 장치를 사용 하 여 부하의 균형을 유지 하기 위해 여러 관리 및 모니터링 서버가 설치 되어 있는 경우에는 가상 이름에 SSL 인증서를 발급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-279">Similarly, if you have multiple Administration and Monitoring servers installed to balance the load by using a load balancer, you should issue the SSL certificate to the virtual name.</span></span> <span data-ttu-id="31333-280">즉, 인증서의 주체 이름 필드에는 가상 이름이 있어야 하 고, 인증서의 **주체 대체 이름** 필드에 모든 로컬 서버의 이름이 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-280">That is, the subject name field of the certificate should have the virtual name, and the names of all the local servers should be added in the **Subject Alternative Name** field of the certificate.</span></span>

<span data-ttu-id="31333-281">예:</span><span class="sxs-lookup"><span data-stu-id="31333-281">Example:</span></span>

<span data-ttu-id="31333-282">가상 이름이 "bitlocker.contoso.com"이 고 서버가 "adminserver1.contoso.com"이 고 "adminiserver2.contoso.com" 인 경우 인증서는 bitlocker.contoso.com (주체 이름) 및 adminserver1.contoso.com에 발급 되어야 하 고, 인증서의 **주체 대체 이름** 필드에는 adminiserver2.contoso.com이 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-282">If the virtual name is "bitlocker.contoso.com" and the servers are "adminserver1.contoso.com" and "adminiserver2.contoso.com," the certificate should be issued to bitlocker.contoso.com (subject name) and adminserver1.contoso.com, and adminiserver2.contoso.com should be added to the **Subject Alternative Name** field of the certificate.</span></span>

<span data-ttu-id="31333-283">MBAM을 사용 하 여 SSL 통신을 구성 하는 단계는 다음 기술 자료 문서에 설명 되어 있습니다. [KB 2754259](https://support.microsoft.com/help/2754259).</span><span class="sxs-lookup"><span data-stu-id="31333-283">The steps to configure SSL communication by using MBAM are described in the following Knowledge Base article: [KB 2754259](https://support.microsoft.com/help/2754259).</span></span>

### <span data-ttu-id="31333-284">5 단계: 응용 프로그램 풀 계정에 대 한 SPN을 등록 하 고 제한 위임을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-284">Step 5: Register SPNS for the application pool account and configure constrained delegation</span></span>

> [!Note]
> <span data-ttu-id="31333-285">제한 된 위임은 2.5에만 필요 하며 2.5 서비스 팩 1 이상에는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-285">Constrained delegation is required only for 2.5 and is not required for 2.5 Service Pack 1 and later.</span></span>

<span data-ttu-id="31333-286">MBAM 서버에서 관리 및 모니터링 웹 사이트와 셀프 서비스 포털의 통신을 인증 하도록 설정 하려면 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 호스트 이름에 대 한 SPN (서비스 사용자 이름)을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-286">To enable the MBAM servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span> <span data-ttu-id="31333-287">Spn을 등록 하는 단계별 지침은 다음과 같습니다. [MBAM 웹 사이트의 보안을 유지 하는 방법 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)</span><span class="sxs-lookup"><span data-stu-id="31333-287">The following article contains step-by-step instructions to register SPNs: [Planning How to Secure the MBAM Websites](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)</span></span>

<span data-ttu-id="31333-288">SPN을 구성한 후에는 SPN에 대 한 제한 된 위임을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-288">After you have the SPN configured, you should set up constrained delegation on the SPN.</span></span> <span data-ttu-id="31333-289">이렇게 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="31333-289">To do this, follow these steps:</span></span>

1. <span data-ttu-id="31333-290">Active Directory로 이동 하 여 이전 단계에서 MBAM 웹 사이트에 대해 구성한 앱 풀 자격 증명을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-290">Go to Active Directory, and find the app pool credentials that you configured for MBAM websites in the previous steps.</span></span>

2. <span data-ttu-id="31333-291">자격 증명을 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-291">Right-click the credentials, and then select **properties**.</span></span>

3. <span data-ttu-id="31333-292">**위임** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-292">Select the **delegation** tab.</span></span>

4. <span data-ttu-id="31333-293">Kerberos 인증 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-293">Select the option for Kerberos authentication.</span></span>

5. <span data-ttu-id="31333-294">**찾아보기를**선택 하 고 앱 풀 자격 증명을 다시 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-294">Select **browse**, and browse again for your app pool credentials.</span></span> <span data-ttu-id="31333-295">그러면 앱 풀 자격 증명 계정에 설정 된 모든 Spn이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-295">You should then see the all the SPNs that are set up on the app pool creds account.</span></span> <span data-ttu-id="31333-296">(SPN은 "http/bitlocker. fqdn.")와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-296">(The SPN should resemble "http/bitlocker.fqdn.com").</span></span> <span data-ttu-id="31333-297">MBAM 설치 중에 지정한 호스트 이름과 동일한 SPN을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-297">Highlight the SPN that is the same as the host name that you specified during the MBAM installation.</span></span>

6. <span data-ttu-id="31333-298">**확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-298">Select **OK**.</span></span>

<span data-ttu-id="31333-299">이제 필수 구성 요소에 대해 잘 알고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-299">Now you are good with prerequisites.</span></span> <span data-ttu-id="31333-300">다음 단계에서는 서버에 MBAM 소프트웨어를 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-300">In the next steps, you will install the MBAM software on the servers and configure it.</span></span>

## <span data-ttu-id="31333-301">MBAM 2.5 서버 소프트웨어 설치 및 구성</span><span class="sxs-lookup"><span data-stu-id="31333-301">Installing and configuring MBAM 2.5 server software</span></span>

### <span data-ttu-id="31333-302">6 단계: MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="31333-302">Step 6: Install MBAM 2.5 server software</span></span> 

<span data-ttu-id="31333-303">데이터베이스 서버와 관리 및 모니터링 서버 모두에서 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하 여 MBAM 서버 소프트웨어를 설치 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="31333-303">To install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard both on Database Server and on Administration and Monitoring Server, follow these steps.</span></span>

1. <span data-ttu-id="31333-304">MBAM을 설치 하려는 서버에서 MBAMserversetup.exe를 실행 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-304">On the server on which you want to install MBAM, run MBAMserversetup.exe to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2. <span data-ttu-id="31333-305">시작 페이지에서 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-305">On the Welcome page, select **Next**.</span></span>

3. <span data-ttu-id="31333-306">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 선택 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-306">Read and accept the Microsoft Software License Agreement, and then select **Next** to continue the installation.</span></span>

4. <span data-ttu-id="31333-307">업데이트를 확인할 때 Microsoft Update를 사용할지 여부를 결정 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-307">Decide whether to use Microsoft Update when you check for updates, and then select **Next**.</span></span>

5. <span data-ttu-id="31333-308">사용자 환경 개선 프로그램에 참여할지 여부를 결정 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-308">Decide whether to participate in the Customer Experience Improvement Program, and then select **Next**.</span></span>

6. <span data-ttu-id="31333-309">설치를 시작 하려면 **설치**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-309">To start the installation, select **Install**.</span></span>

7. <span data-ttu-id="31333-310">MBAM 서버 소프트웨어 설치가 완료 된 후 서버 기능을 구성 하려면 **마법사를 닫은 후에 Mbam 서버 구성 실행** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-310">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="31333-311">또는 서버 설치가 **시작** 메뉴에 생성 하는 **Mbam 서버 구성** 바로 가기를 사용 하 여 나중에 mbam을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-311">Or, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8. <span data-ttu-id="31333-312">**마침을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-312">Select **Finish**.</span></span>

<span data-ttu-id="31333-313">자세한 내용은 [MBAM 2.5 서버 소프트웨어 설치](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-313">For more information, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

### <span data-ttu-id="31333-314">7 단계: MBAM 2.5 데이터베이스 및 보고서 역할 구성</span><span class="sxs-lookup"><span data-stu-id="31333-314">Step 7: Configure MBAM 2.5 database and reports role</span></span>

<span data-ttu-id="31333-315">이 단계에서는 MBAM 마법사를 사용 하 여 MBAM 2.5 데이터베이스 및 보고 구성 요소를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-315">In this step, we will configure the MBAM 2.5 databases and reporting component by using the MBAM Wizard:</span></span>

1. <span data-ttu-id="31333-316">마법사를 사용 하 여 준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-316">Configure the Compliance and Audit Database and the Recovery Database by using the wizard:</span></span>
   
   1. <span data-ttu-id="31333-317">데이터베이스를 구성 하려는 서버에서 **Mbam 서버 구성 마법사**를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-317">On the server on which you want to configure the databases, start the **MBAM Server Configuration wizard**.</span></span> <span data-ttu-id="31333-318">**시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-318">You can select **MBAM Server Configuration** on the **Start** menu to open the wizard.</span></span>

   2. <span data-ttu-id="31333-319">**새 기능 추가**, **준수 및 감사 데이터베이스**, **복구 데이터베이스 및 보고서**를 차례로 선택 하 고 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-319">Select **Add New Features**, select **Compliance and Audit Database**, **Recovery Database and Reports**, and then select **Next**.</span></span> <span data-ttu-id="31333-320">마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-320">The wizard checks that all prerequisites for the databases are met.</span></span>

   3. <span data-ttu-id="31333-321">필수 구성 요소 확인이 완료 되 면 **다음** 을 선택 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-321">If the prerequisite check is successful, select **Next** to continue.</span></span> <span data-ttu-id="31333-322">그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-322">Otherwise, resolve any missing prerequisites, and then select **Check prerequisites again**.</span></span>
   
   4. <span data-ttu-id="31333-323">다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-323">Using the following descriptions, enter the field values in the wizard:</span></span>

2. <span data-ttu-id="31333-324">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="31333-324">Compliance and audit database</span></span>

   |<span data-ttu-id="31333-325">필드</span><span class="sxs-lookup"><span data-stu-id="31333-325">Field</span></span>   |<span data-ttu-id="31333-326">설명</span><span class="sxs-lookup"><span data-stu-id="31333-326">Description</span></span>|
   |-------|-------|
   |<span data-ttu-id="31333-327">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="31333-327">SQL Server name</span></span> |<span data-ttu-id="31333-328">준수 및 감사 데이터베이스를 구성 중인 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-328">Name of the server on which you are configuring the Compliance and Audit Database.</span></span> <br /> <span data-ttu-id="31333-329">SQL Server 포트에서 수신 되는 인바운드 트래픽을 사용 하려면 준수 및 감사 데이터베이스 컴퓨터에 예외를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-329">You must add an exception on the Compliance and Audit Database computer to enable incoming inbound traffic on the SQL Server port.</span></span> <span data-ttu-id="31333-330">기본 포트 번호는 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-330">The default port number is 1433.</span></span>|
   |<span data-ttu-id="31333-331">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="31333-331">SQL Server database instance</span></span>    |<span data-ttu-id="31333-332">준수 및 감사 데이터가 저장 되는 데이터베이스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-332">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="31333-333">기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-333">If you are using the default instance, you must leave this field blank.</span></span> <span data-ttu-id="31333-334">또한 데이터베이스 정보 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-334">You must also specify where the database information will be located.</span></span>|
   |<span data-ttu-id="31333-335">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="31333-335">Database name</span></span>   |<span data-ttu-id="31333-336">준수 데이터를 저장할 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-336">Name of the database that will store the compliance data.</span></span> <span data-ttu-id="31333-337">나중에이 정보를 제공 해야 하므로 여기에서 지정 하는 데이터베이스의 이름을 기록해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-337">You must note the name of the database that you are specifying here because you will have to provide this information in later steps.</span></span>|
   |<span data-ttu-id="31333-338">읽기/쓰기 권한 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-338">Read/write permission domain user or group</span></span>  |<span data-ttu-id="31333-339">2 단계에서 구성한 MBAMAppPool 사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-339">Specify the name of the MBAMAppPool user as configured in step 2.</span></span>|
   |<span data-ttu-id="31333-340">읽기 전용 액세스 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-340">Read-only access domain user or group</span></span>   |<span data-ttu-id="31333-341">2 단계에서 구성한 MBAMROUser 사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-341">Specify the name of the MBAMROUser user as configured in step 2.</span></span>|

3. <span data-ttu-id="31333-342">복구 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="31333-342">Recovery database.</span></span>

   |<span data-ttu-id="31333-343">필드</span><span class="sxs-lookup"><span data-stu-id="31333-343">Field</span></span>   |<span data-ttu-id="31333-344">설명</span><span class="sxs-lookup"><span data-stu-id="31333-344">Description</span></span>|
   |-----|-----|
   |<span data-ttu-id="31333-345">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="31333-345">SQL Server name</span></span> |<span data-ttu-id="31333-346">복구 데이터베이스를 구성 중인 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-346">Name of the server on which you are configuring the Recovery Database.</span></span> <span data-ttu-id="31333-347">SQL Server 포트에서 수신 되는 인바운드 트래픽을 사용 하려면 복구 데이터베이스 컴퓨터에 예외를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-347">You must add an exception on the Recovery Database computer to enable incoming inbound traffic on the SQL Server port.</span></span> <span data-ttu-id="31333-348">기본 포트 번호는 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-348">The default port number is 1433.</span></span>|
   |<span data-ttu-id="31333-349">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="31333-349">SQL Server database instance</span></span>    |<span data-ttu-id="31333-350">복구 데이터를 저장할 데이터베이스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-350">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="31333-351">기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-351">If you are using the default instance, you must leave this field blank.</span></span> <span data-ttu-id="31333-352">또한 데이터베이스 정보 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-352">You must also specify where the database information will be located.</span></span>|
   |<span data-ttu-id="31333-353">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="31333-353">Database name</span></span>   |<span data-ttu-id="31333-354">복구 데이터를 저장 하는 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-354">Name of the database that will store the recovery data.</span></span>|
   |<span data-ttu-id="31333-355">읽기/쓰기 권한 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-355">Read/write permission domain user or group</span></span>  |<span data-ttu-id="31333-356">웹 응용 프로그램이이 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록이 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-356">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span> <br /><span data-ttu-id="31333-357">이 필드에 사용자를 입력 하는 경우 **웹 응용 프로그램 구성** 페이지의 **웹 서비스 응용 프로그램 풀 도메인 계정** 필드에 있는 값과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-357">If you enter a user in this field, it must be the same value as the value in the **Web service application pool domain account** field on the **Configure Web Applications** page.</span></span> <br /><span data-ttu-id="31333-358">이 필드에 그룹을 입력 하는 경우 **웹 응용 프로그램 구성** 페이지의 **웹 서비스 응용 프로그램 풀 도메인 계정** 필드에 있는 값이이 필드에 입력 하는 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-358">If you enter a group in this field, the value in the **Web service application pool domain account** field on the **Configure Web Applications** page must be a member of the group that you enter in this field.</span></span>|
   
   <span data-ttu-id="31333-359">항목을 모두 마쳤으면 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-359">When you finish your entries, select **Next**.</span></span> <span data-ttu-id="31333-360">마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-360">The wizard checks that all prerequisites for the databases are met.</span></span>
   
   <span data-ttu-id="31333-361">필수 구성 요소 확인이 완료 되 면 **다음** 을 선택 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-361">If the prerequisite check is successful, select **Next** to continue.</span></span> <span data-ttu-id="31333-362">그렇지 않으면 누락 된 필수 구성 요소를 해결 하 고 **다음** 을 다시 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-362">Otherwise, resolve any missing prerequisites, and then select **Next** again.</span></span>

4. <span data-ttu-id="31333-363">보고서.</span><span class="sxs-lookup"><span data-stu-id="31333-363">Reports.</span></span>

   |<span data-ttu-id="31333-364">필드</span><span class="sxs-lookup"><span data-stu-id="31333-364">Field</span></span>   |<span data-ttu-id="31333-365">설명</span><span class="sxs-lookup"><span data-stu-id="31333-365">Description</span></span>|
   |----|----|
   |<span data-ttu-id="31333-366">SQL Server Reporting Services 인스턴스</span><span class="sxs-lookup"><span data-stu-id="31333-366">SQL Server Reporting Services instance</span></span>  |<span data-ttu-id="31333-367">보고서를 구성 하는 SQL Server Reporting Services의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-367">Instance of SQL Server Reporting Services where the reports will be configured.</span></span> <span data-ttu-id="31333-368">기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-368">If you are using the default instance, you must leave this field blank.</span></span>|
   |<span data-ttu-id="31333-369">보고 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-369">Reporting role domain group</span></span> |<span data-ttu-id="31333-370">2 단계에서 설명한 대로 Mbam Grp의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-370">Specify the name of the MBAMRUGrp as mentioned in step 2.</span></span>|
   |<span data-ttu-id="31333-371">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="31333-371">SQL Server name</span></span> |<span data-ttu-id="31333-372">규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-372">Name of the server on which the Compliance and Audit Database is configured.</span></span>|
   |<span data-ttu-id="31333-373">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="31333-373">SQL Server database instance</span></span>    |<span data-ttu-id="31333-374">규정 준수 및 감사 데이터가 구성 된 데이터베이스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-374">Name of the database instance where the compliance and audit data is configured.</span></span> <span data-ttu-id="31333-375">기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-375">If you are using the default instance, you must leave this field blank.</span></span> <br /><span data-ttu-id="31333-376">보고 서버의 포트에서 들어오는 트래픽을 사용할 수 있도록 하려면 보고서 컴퓨터에 예외를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-376">You must add an exception on the Reports computer to enable incoming traffic on the port of the Reporting Server.</span></span> <span data-ttu-id="31333-377">(기본 포트는 80입니다.)</span><span class="sxs-lookup"><span data-stu-id="31333-377">(The default port is 80.)</span></span>|
   |<span data-ttu-id="31333-378">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="31333-378">Database name</span></span>|  <span data-ttu-id="31333-379">준수 및 감사 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-379">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="31333-380">기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-380">By default, the database name is MBAM Compliance Status.</span></span>|
   |<span data-ttu-id="31333-381">준수 및 감사 데이터베이스 도메인 계정</span><span class="sxs-lookup"><span data-stu-id="31333-381">Compliance and Audit Database domain account</span></span>    |<span data-ttu-id="31333-382">2 단계에서 구성한 MBAMROUser 사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-382">Specify the name of the MBAMROUser user as configured in step 2.</span></span>|
   
   <span data-ttu-id="31333-383">항목을 모두 마쳤으면 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-383">When you finish your entries, select **Next**.</span></span> <span data-ttu-id="31333-384">마법사가 보고서 기능에 대 한 모든 필수 구성 요소를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-384">The wizard checks that all prerequisites for the Reports feature are met.</span></span> <span data-ttu-id="31333-385">계속하려면 다음을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-385">Select Next to continue.</span></span> <span data-ttu-id="31333-386">**요약** 페이지에서 추가 되는 기능을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-386">On the **Summary** page, review the features that will be added.</span></span>
   
   <span data-ttu-id="31333-387">자세한 내용은 다음 문서를 참조 하세요. [MBAM 2.5 데이터베이스를 구성 하는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-387">For more information, see the following article: [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

### <span data-ttu-id="31333-388">8 단계: MBAM 2.5 웹 응용 프로그램 역할 구성</span><span class="sxs-lookup"><span data-stu-id="31333-388">Step 8: Configure the MBAM 2.5 Web applications role</span></span>

1. <span data-ttu-id="31333-389">웹 응용 프로그램을 구성 하려는 서버에서 MBAM 서버 구성 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-389">On the server on which you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="31333-390">**시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-390">You can select **MBAM Server Configuration** on the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="31333-391">**새 기능 추가**를 선택 하 **고 관리 및 모니터링 웹 사이트** 및 **셀프 서비스 포털**을 선택한 후 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-391">Select **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then select **Next**.</span></span> <span data-ttu-id="31333-392">마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-392">The wizard checks that all prerequisites for the databases are met.</span></span>

3. <span data-ttu-id="31333-393">필수 구성 요소 확인이 완료 되 면 **다음** 을 선택 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-393">If the prerequisite check is successful, select **Next** to continue.</span></span> <span data-ttu-id="31333-394">그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-394">Otherwise, resolve any missing prerequisites, and then select **Check prerequisites again**.</span></span>

4. <span data-ttu-id="31333-395">다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-395">Use the following descriptions to enter the field values in the wizard.</span></span>

   |<span data-ttu-id="31333-396">필드</span><span class="sxs-lookup"><span data-stu-id="31333-396">Field</span></span>   |<span data-ttu-id="31333-397">설명</span><span class="sxs-lookup"><span data-stu-id="31333-397">Description</span></span>|
   |-----|-----|
   |<span data-ttu-id="31333-398">보안 인증서</span><span class="sxs-lookup"><span data-stu-id="31333-398">Security certificate</span></span>    |<span data-ttu-id="31333-399">3 단계에서 이전에 만든 인증서를 선택 하 여 관리 및 모니터링 웹 사이트를 구성 하는 웹 서비스와 서버 간의 통신을 선택적으로 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-399">Select a previously created certificate in step 3 to optionally encrypt the communication between the web services and the server on which you are configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="31333-400">인증서 사용 안 함을 선택 하면 웹 통신이 안전 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-400">If you select Do not use a certificate, your web communication may not be secure.</span></span>|
   |<span data-ttu-id="31333-401">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="31333-401">Host name</span></span>   |<span data-ttu-id="31333-402">관리 및 모니터링 웹 사이트를 구성 하는 호스트 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-402">Name of the host computer on which you are configuring the Administration and Monitoring Website.</span></span> <br /><span data-ttu-id="31333-403">이는 컴퓨터의 호스트 이름이 될 필요는 없으며 모든 것이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-403">It does not have to be the hostname of the machine, it could be anything.</span></span> <span data-ttu-id="31333-404">그러나 호스트 이름이 컴퓨터의 netbios 이름과 다른 경우 A 레코드를 만들고 SPN이 netbios 이름이 아닌 사용자 지정 hostname을 사용 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-404">However, if the hostname is different than the netbios name of the computer, you have to create an A record and make sure the SPN uses the custom hostname, not the netbios name.</span></span> <span data-ttu-id="31333-405">이는 부하 분산 시나리오에서 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-405">This is common on load balancing scenarios.</span></span>|
   |<span data-ttu-id="31333-406">설치 경로</span><span class="sxs-lookup"><span data-stu-id="31333-406">Installation path</span></span>   |<span data-ttu-id="31333-407">관리 및 모니터링 웹 사이트를 설치 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-407">Path on which you are installing the Administration and Monitoring Website.</span></span>|
   |<span data-ttu-id="31333-408">Port</span><span class="sxs-lookup"><span data-stu-id="31333-408">Port</span></span>    |<span data-ttu-id="31333-409">웹 사이트 통신에 사용할 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-409">Port number to use for website communication.</span></span> <br /> <span data-ttu-id="31333-410">지정 된 포트를 통해 통신을 사용 하도록 설정 하려면 방화벽 예외를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-410">You must set a firewall exception to enable communication through the specified port.</span></span>|
   |<span data-ttu-id="31333-411">웹 서비스 응용 프로그램 풀 도메인 계정 및 암호</span><span class="sxs-lookup"><span data-stu-id="31333-411">Web service application pool domain account and password</span></span>    |<span data-ttu-id="31333-412">2 단계에서 구성한 MBAMAppPool 사용자의 사용자 계정 및 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-412">Specify the user account and password of the MBAMAppPool user as configured in step 2.</span></span> <br /> <span data-ttu-id="31333-413">보안 향상을 위해 자격 증명에 지정 된 계정에 제한 된 사용자 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-413">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="31333-414">또한 계정 암호가 만료 되지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-414">Also, set the password of the account to never expire.</span></span>|

5. <span data-ttu-id="31333-415">**인증 후** 에 기본 제공 IIS_IUSRS 계정 또는 응용 프로그램 풀 계정이 클라이언트 가장으로 추가 되었는지 확인 하 고 **일괄 작업으로 로그온** 로컬 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-415">Verify that the built-in IIS_IUSRS account or the application pool account was added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="31333-416">계정이 로컬 보안 설정에 추가 되었는지 여부를 확인 하려면 **로컬 보안 정책 편집기**를 열고, **로컬 정책** 노드를 확장 하 고, **사용자 권한 할당** 노드를 선택 하 고, **인증 후 클라이언트 가장** 을 두 번 선택 하 고 오른쪽 창에서 **일괄 작업으로 로그온** 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-416">To check whether the account was added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and double-select **Impersonate a client after authentication** and **Log on as a batch job** policies in the right-side pane.</span></span>

6. <span data-ttu-id="31333-417">마법사에서 준수 및 감사 데이터베이스에 대 한 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-417">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>
   |<span data-ttu-id="31333-418">필드</span><span class="sxs-lookup"><span data-stu-id="31333-418">Field</span></span>   |<span data-ttu-id="31333-419">설명</span><span class="sxs-lookup"><span data-stu-id="31333-419">Description</span></span>|
   |------|------|
   |<span data-ttu-id="31333-420">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="31333-420">SQL Server name</span></span> |<span data-ttu-id="31333-421">규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-421">Name of the server on which the Compliance and Audit Database is configured.</span></span>|
   |<span data-ttu-id="31333-422">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="31333-422">SQL Server database instance</span></span>    |<span data-ttu-id="31333-423">SQL Server 인스턴스의 이름 (예: \<Server Name\> )과 준수 및 감사 데이터베이스가 구성 된</span><span class="sxs-lookup"><span data-stu-id="31333-423">Name of the instance of SQL Server (for example, \<Server Name\>) and on which the Compliance and Audit Database is configured.</span></span> <span data-ttu-id="31333-424">기본 인스턴스를 사용 하는 경우이를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="31333-424">Leave this blank if you are using the default instance.</span></span>|
   |<span data-ttu-id="31333-425">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="31333-425">Database name</span></span>   |<span data-ttu-id="31333-426">준수 및 감사 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-426">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="31333-427">기본적으로 "MBAM 준수 상태"입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-427">By default, it’s "MBAM Compliance Status".</span></span>|

7. <span data-ttu-id="31333-428">복구 데이터베이스에 대 한 마법사에서 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-428">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>
   |<span data-ttu-id="31333-429">필드</span><span class="sxs-lookup"><span data-stu-id="31333-429">Field</span></span>   |<span data-ttu-id="31333-430">설명</span><span class="sxs-lookup"><span data-stu-id="31333-430">Description</span></span>|
   |----|----|
   |<span data-ttu-id="31333-431">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="31333-431">SQL Server name</span></span> |<span data-ttu-id="31333-432">복구 데이터베이스가 구성 된 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-432">Name of the server on which the Recovery Database is configured.</span></span>|
   |<span data-ttu-id="31333-433">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="31333-433">SQL Server database instance</span></span>    |<span data-ttu-id="31333-434">복구 데이터베이스가 구성 된 SQL Server 인스턴스의 이름 (예: \<Server Name\> )입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-434">Name of the instance of SQL Server (for example, \<Server Name\>) on which the Recovery Database is configured.</span></span> <span data-ttu-id="31333-435">기본 인스턴스를 사용 하는 경우이를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="31333-435">Leave this blank if you are using the default instance.</span></span>|
   |<span data-ttu-id="31333-436">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="31333-436">Database name</span></span>   |<span data-ttu-id="31333-437">복구 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-437">Name of the Recovery Database.</span></span> <span data-ttu-id="31333-438">기본적으로 "MBAM 복구 및 하드웨어"입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-438">By default, it’s "MBAM Recovery and Hardware".</span></span>|

8. <span data-ttu-id="31333-439">마법사에서 필드 값을 입력 하 여 관리 및 모니터링 웹 사이트를 구성 하려면 다음 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-439">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>
   |<span data-ttu-id="31333-440">필드</span><span class="sxs-lookup"><span data-stu-id="31333-440">Field</span></span>   |<span data-ttu-id="31333-441">설명</span><span class="sxs-lookup"><span data-stu-id="31333-441">Description</span></span>|
   |----|----|
   |<span data-ttu-id="31333-442">고급 헬프데스크 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-442">Advanced Helpdesk role domain group</span></span> |<span data-ttu-id="31333-443">2 단계에서 구성한 MBAMAdvHelpDsk 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-443">Specify the name of the MBAMAdvHelpDsk Group as configured in step 2.</span></span>|
   |<span data-ttu-id="31333-444">헬프데스크 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-444">Helpdesk role domain group</span></span>  |<span data-ttu-id="31333-445">2 단계에서 구성한 대로 Mbam 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-445">Specify the name of the MBAMHelpDsk Group as configured in step 2.</span></span>|
   |<span data-ttu-id="31333-446">System Center Configuration Manager 통합 사용</span><span class="sxs-lookup"><span data-stu-id="31333-446">Use System Center Configuration Manager Integration</span></span> |<span data-ttu-id="31333-447">이 확인란을 선택 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-447">Select to clear this check box.</span></span>     |
   |<span data-ttu-id="31333-448">보고 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="31333-448">Reporting role domain group</span></span> |<span data-ttu-id="31333-449">2 단계에서 구성한 대로 Mbam Grp Group의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-449">Specify the name of the MBAMRUGrp Group as configured in step 2.</span></span>    |
   |<span data-ttu-id="31333-450">SQL Server Reporting Services URL</span><span class="sxs-lookup"><span data-stu-id="31333-450">SQL Server Reporting Services URL</span></span>   |<span data-ttu-id="31333-451">MBAM 보고서가 구성 된 SSRS 서버의 웹 서비스 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-451">Specify the Web Service URL for the SSRS server on which the MBAM reports are configured.</span></span> <span data-ttu-id="31333-452">데이터베이스 서버에서 Reporting Services 구성 관리자에 로그인 하 여이 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-452">You can find this information by logging in to Reporting Services Configuration Manager on the Database Server.</span></span> <br /> <span data-ttu-id="31333-453">정규화 된 도메인 이름의 예:https://MyReportServer.Contoso.com/ReportServer</span><span class="sxs-lookup"><span data-stu-id="31333-453">Example of a fully qualified domain name: https://MyReportServer.Contoso.com/ReportServer</span></span> <br /><span data-ttu-id="31333-454">사용자 지정 호스트 이름의 예:https://MyReportServer/ReportServer</span><span class="sxs-lookup"><span data-stu-id="31333-454">Example of a custom host name: https://MyReportServer/ReportServer</span></span>|
   |<span data-ttu-id="31333-455">가상 디렉터리</span><span class="sxs-lookup"><span data-stu-id="31333-455">Virtual directory</span></span>   |<span data-ttu-id="31333-456">관리 및 모니터링 웹 사이트의 가상 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-456">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="31333-457">이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당 하며 웹 사이트의 호스트 이름에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-457">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name.</span></span> <span data-ttu-id="31333-458">예:</span><span class="sxs-lookup"><span data-stu-id="31333-458">For example:</span></span> <br /><span data-ttu-id="31333-459">http (s)// *\<host name\>* : *\<port\>* /HelpDesk/</span><span class="sxs-lookup"><span data-stu-id="31333-459">http(s)://*\<host name\>*:*\<port\>*/HelpDesk/</span></span> <br /><span data-ttu-id="31333-460">가상 디렉터리를 지정 하지 않으면 값 헬프데스크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-460">If you do not specify a virtual directory, the value HelpDesk will be used.</span></span>     |

9. <span data-ttu-id="31333-461">마법사에서 필드 값을 입력 하 여 셀프 서비스 포털을 구성 하려면 다음 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-461">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   |<span data-ttu-id="31333-462">필드</span><span class="sxs-lookup"><span data-stu-id="31333-462">Field</span></span>   |<span data-ttu-id="31333-463">설명</span><span class="sxs-lookup"><span data-stu-id="31333-463">Description</span></span>|
   |----|----|
   |<span data-ttu-id="31333-464">가상 디렉터리</span><span class="sxs-lookup"><span data-stu-id="31333-464">Virtual directory</span></span>   |<span data-ttu-id="31333-465">웹 응용 프로그램의 가상 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-465">Virtual directory of the web application.</span></span> <span data-ttu-id="31333-466">이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당 하며 웹 사이트의 호스트 이름에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-466">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name.</span></span> <span data-ttu-id="31333-467">예:</span><span class="sxs-lookup"><span data-stu-id="31333-467">For example:</span></span><br /><span data-ttu-id="31333-468">http (s)// *\<host name\>* : *\<port\>* /SelfService/</span><span class="sxs-lookup"><span data-stu-id="31333-468">http(s)://*\<host name\>*:*\<port\>*/SelfService/</span></span><br /> <span data-ttu-id="31333-469">가상 디렉터리를 지정 하지 않으면 "SelfService" 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-469">If you do not specify a virtual directory, the value "SelfService" will be used.</span></span>|

10. <span data-ttu-id="31333-470">항목을 모두 마쳤으면 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-470">When you finish your entries, select **Next**.</span></span> <span data-ttu-id="31333-471">마법사가 웹 응용 프로그램의 모든 필수 구성 요소를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-471">The wizard checks that all prerequisites for the web applications are met.</span></span>

11. <span data-ttu-id="31333-472">**Next (다음** )를 선택 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-472">Select **Next** to continue.</span></span>

12. <span data-ttu-id="31333-473">**요약** 페이지에서 추가 되는 기능을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-473">On the **Summary** page, review the features that will be added.</span></span>

13. <span data-ttu-id="31333-474">서버에 웹 응용 프로그램을 추가 하려면 **추가** 를 선택 하 고 **닫기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-474">Select **Add** to add the web applications to the server, and then select **Close**.</span></span>

## <span data-ttu-id="31333-475">MBAM 2.5 서버 소프트웨어 설치 후 단계 사용자 지정 및 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="31333-475">Customizing and validating steps after installing MBAM 2.5 server software</span></span>

### <span data-ttu-id="31333-476">9 단계: 조직에 대 한 셀프 서버 포털 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="31333-476">Step 9: Customizing the self-server portal for your organization</span></span>

<span data-ttu-id="31333-477">사용자 지정 알림 텍스트, 회사 이름, 추가 정보에 대 한 포인터 등을 추가 하 여 셀프 서비스 포털을 사용자 지정 하려면 [조직에 대 한 셀프 서비스 포털 사용자 지정](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-477">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).</span></span>
 
### <span data-ttu-id="31333-478">10 단계: 클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서버 포털 구성</span><span class="sxs-lookup"><span data-stu-id="31333-478">Step 10: Configure the self-server portal if client computers cannot access the CDN</span></span> 

<span data-ttu-id="31333-479">클라이언트 컴퓨터에 Microsoft CDN (콘텐츠 배달 네트워크)에 대 한 액세스 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-479">Determine whether your client computers have access to the Microsoft AJAX Content Delivery Network (CDN).</span></span> <span data-ttu-id="31333-480">CDN은 특정 JavaScript 파일에 필요한 액세스 권한을 셀프 서비스 포털에 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-480">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="31333-481">클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하지 않으면 사용자가 로그인 한 회사 이름과 계정만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-481">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the user signed in will be displayed.</span></span> <span data-ttu-id="31333-482">오류 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-482">No error message will be shown.</span></span>

<span data-ttu-id="31333-483">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-483">Do one of the following:</span></span>

* <span data-ttu-id="31333-484">클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 있는 경우 아무 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-484">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="31333-485">셀프 서비스 포털 구성이 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-485">Your Self-Service Portal configuration is complete.</span></span>

* <span data-ttu-id="31333-486">클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 없는 경우 [클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network)의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="31333-486">If your client computers do not have access to the CDN, follow the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).</span></span>

### <span data-ttu-id="31333-487">11 단계: MBAM 2.5 서버 기능 구성 확인</span><span class="sxs-lookup"><span data-stu-id="31333-487">Step 11: Validate the MBAM 2.5 server feature configuration</span></span> 

<span data-ttu-id="31333-488">단독 토폴로지를 사용 하기 위해 MBAM 서버 배포의 유효성을 검사 하려면 다음 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="31333-488">To validate your MBAM Server deployment to use the standalone topology, follow these steps.</span></span>

1. <span data-ttu-id="31333-489">Mbam 기능이 배포 된 각 서버에서 **제어판**  >  **프로그램**프로그램  >  **및 기능**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-489">On each server on which an MBAM feature is deployed, select **Control Panel** > **Programs** > **Programs and Features**.</span></span> <span data-ttu-id="31333-490">**Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-490">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>
   > [!Note]
   > <span data-ttu-id="31333-491">유효성 검사를 수행 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-491">To perform the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

2. <span data-ttu-id="31333-492">복구 데이터베이스가 구성 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-492">On the server on which the Recovery Database is configured, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3. <span data-ttu-id="31333-493">준수 및 감사 데이터베이스가 구성 된 서버 om에서 SQL Server Management Studio를 열고 MBAM 준수 상태 데이터베이스가 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-493">On the server om which the Compliance and Audit Database is configured, open SQL Server Management Studio, and verify that the MBAM Compliance Status Database is configured.</span></span>

4. <span data-ttu-id="31333-494">보고서 기능이 구성 된 서버 onm에서 관리 자격 증명을 사용 하 여 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 홈페이지를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-494">On the server onm which the Reports feature is configured, open a web browser by using administrative credentials, and browse to the homepage of the SQL Server Reporting Services site.</span></span>
   
   <span data-ttu-id="31333-495">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 페이지 위치는 다음과 같습니다. http (s)// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx</span><span class="sxs-lookup"><span data-stu-id="31333-495">The default homepage location of a SQL Server Reporting Services site instance is as follows: http(s)://*\<MBAM Reports Server Name\>*:*\<port\>*/Reports.aspx</span></span>
   
   <span data-ttu-id="31333-496">실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정한 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-496">To find the actual URL, use the Reporting Services Configuration Manager tool, and select the instances that you specified during setup.</span></span>
   
5. <span data-ttu-id="31333-497">Microsoft BitLocker 관리 및 모니터링 이라는 보고서 폴더에 MaltaDataSource 이라는 데이터 원본이 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-497">Verify that a reports folder that is named Microsoft BitLocker Administration and Monitoring contains a data source that is named MaltaDataSource.</span></span> <span data-ttu-id="31333-498">이 데이터 원본에는 언어 로캘을 나타내는 이름 (예: en-us)이 포함 된 폴더가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-498">This data source contains folders that have names that represent language locales (for example, en-us).</span></span> <span data-ttu-id="31333-499">보고서는 언어 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-499">The reports are in the language folders.</span></span>

   > [!Note]
   > <span data-ttu-id="31333-500">SQL Server Reporting Services (SSRS)가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http (s)// \<MBAM Reports Server Name\> : \<port\> /Reports_</span><span class="sxs-lookup"><span data-stu-id="31333-500">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://\<MBAM Reports Server Name\>:\<port\>/Reports_</span></span>\<SSRS Instance Name\>
   >
   > <span data-ttu-id="31333-501">SSL (Secure Socket Layer)을 사용 하도록 SSRS를 구성 하지 않은 경우, MBAM 서버를 설치할 때 보고서에 대 한 URL이 "HTTPS" 대신 "HTTP"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-501">If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to "HTTP" instead of "HTTPS" when you install the MBAM server.</span></span> <span data-ttu-id="31333-502">그런 다음 관리 및 모니터링 웹 사이트 (헬프데스크 라고도 함)로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="31333-502">If you then go to the Administration and Monitoring Website (also known as Helpdesk) and select a report, you receive the following message: "Only Secure Content is Displayed."</span></span> <span data-ttu-id="31333-503">보고서를 표시 하려면 **모든 콘텐츠 표시**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-503">To show the report, select **Show All Content**.</span></span>

6. <span data-ttu-id="31333-504">관리 및 모니터링 웹 사이트 기능이 구성 된 서버에서 서버 관리자를 실행 하 고 **역할**을 찾은 다음 **웹 서버 (iis**)  >  **iis (인터넷 정보 서비스** ) 관리자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-504">On the server on which the Administration and Monitoring Website feature is configured, run Server Manager, browse to **Roles**, and then select **Web Server (IIS)** > **Internet Information Services (IIS)** Manager.</span></span>

7. <span data-ttu-id="31333-505">**연결**에서 \<computer name\> **Sites**  >  **Microsoft BitLocker 관리 및 모니터링**사이트를 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-505">In **Connections**, browse to \<computer name\> and then select **Sites** > **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="31333-506">다음이 나열 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-506">Verify that the following are listed:</span></span>

   * <span data-ttu-id="31333-507">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="31333-507">MBAMAdministrationService</span></span>
   * <span data-ttu-id="31333-508">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="31333-508">MBAMComplianceStatusService</span></span>
   * <span data-ttu-id="31333-509">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="31333-509">MBAMRecoveryAndHardwareService</span></span>

8. <span data-ttu-id="31333-510">관리 및 모니터링 웹 사이트와 셀프 서비스 포털이 구성 된 서버에서 관리 자격 증명을 사용 하 여 웹 브라우저를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="31333-510">On the server on which the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser by using administrative credentials.</span></span>

9. <span data-ttu-id="31333-511">다음 웹 사이트를 탐색 하 여 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-511">Browse to the following websites to verify that they load successfully:</span></span>
   * <span data-ttu-id="31333-512">https:// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/(탐색 및 보고서에 대 한 각 링크 확인)</span><span class="sxs-lookup"><span data-stu-id="31333-512">https(s)://\<MBAM Administration Server Name\>:\<port\>/HelpDesk/ (confirm each link for navigation and reports)</span></span>
   * <span data-ttu-id="31333-513">http (s)// \<MBAM Administration Server Name\> : \<port\> /SelfService/</span><span class="sxs-lookup"><span data-stu-id="31333-513">http(s)://\<MBAM Administration Server Name\>:\<port\>/SelfService/</span></span>

   > [!Note]
   > <span data-ttu-id="31333-514">네트워크 암호화 없이 기본 포트에서 서버 기능을 구성한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-514">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="31333-515">다른 포트 또는 가상 디렉터리에서 서버 기능을 구성한 경우 해당 포트를 포함 하도록 Url을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-515">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="31333-516">예: http (s)// \<host name\> : \<port\> /HelpDesk/http (s)// \<host name\> : \<port\> / \<virtualdirectory\> /서버 기능이 네트워크 암호화를 사용 하도록 구성 된 경우 http://를 https://로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-516">For example: http(s)://\<host name\>:\<port\>/HelpDesk/ http(s)://\<host name\>:\<port\>/\<virtualdirectory\>/ If the server features were configured to use network encryption, change http:// to https://.</span></span>
   
10. <span data-ttu-id="31333-517">다음 웹 서비스를 찾아 제대로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-517">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="31333-518">서비스가 실행 중임을 나타내는 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="31333-518">A page opens to indicate that the service is running.</span></span> <span data-ttu-id="31333-519">그러나 페이지에는 메타 데이터가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-519">However, the page displays no metadata.</span></span>

    * <span data-ttu-id="31333-520">http (s)// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="31333-520">http(s)://\<MBAM Administration Server Name>:\<port>/MBAMAdministrationService/AdministrationService.svc</span></span>
    * <span data-ttu-id="31333-521">http (s)// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="31333-521">http(s)://\<MBAM Administration Server Name>:\<port>/MBAMUserSupportService/UserSupportService.svc</span></span>
    * <span data-ttu-id="31333-522">http (s)// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="31333-522">http(s)://\<MBAM Administration Server Name>:\<port>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>
    * <span data-ttu-id="31333-523">http (s)// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="31333-523">http(s)://\<MBAM Administration Server Name>:\<port>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

### <span data-ttu-id="31333-524">12 단계: MBAM 그룹 정책 서식 파일 구성</span><span class="sxs-lookup"><span data-stu-id="31333-524">Step 12: Configure the MBAM Group policy templates</span></span>

<span data-ttu-id="31333-525">MBAM을 배포 하려면 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-525">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="31333-526">이 작업을 완료 하려면 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 서버 또는 워크스테이션에 MBAM 그룹 정책 템플릿을 복사한 다음 설정을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-526">To complete this task, you must copy the MBAM Group Policy templates to a server or workstation that can run Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

> [!Important]
> <span data-ttu-id="31333-527">**BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-527">Do not change the Group Policy settings in the **BitLocker Drive Encryption** node or MBAM will not work correctly.</span></span> <span data-ttu-id="31333-528">**MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-528">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>
 
#### <span data-ttu-id="31333-529">MBAM 2.5 그룹 정책 서식 파일 복사</span><span class="sxs-lookup"><span data-stu-id="31333-529">Copying the MBAM 2.5 Group Policy templates</span></span>

<span data-ttu-id="31333-530">MBAM 클라이언트를 설치 하기 전에, 관리 워크스테이션에 MBAM Gpo (그룹 정책 개체)를 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-530">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the management workstation.</span></span> <span data-ttu-id="31333-531">이러한 Gpo는 BitLocker에 대 한 MBAM 구현 설정을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-531">These GPOs define MBAM implementation settings for BitLocker.</span></span> <span data-ttu-id="31333-532">그룹 정책 템플릿을 지원 되는 Windows 기반 서버 또는 클라이언트 컴퓨터인 모든 서버 또는 워크스테이션에 복사 하 여 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-532">You can copy the Group Policy templates to any server or workstation that is a supported Windows-based server or client computer and that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="31333-533">자세한 내용은 [MBAM 2.5 그룹 정책 서식 파일 복사](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-533">For more information, see [Copying the MBAM 2.5 Group Policy Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).</span></span>
 
#### <span data-ttu-id="31333-534">MBAM 2.5 GPO 설정 편집</span><span class="sxs-lookup"><span data-stu-id="31333-534">Editing MBAM 2.5 GPO settings</span></span>

<span data-ttu-id="31333-535">필요한 Gpo를 만든 후에는 조직의 클라이언트 컴퓨터에 MBAM 그룹 정책 설정을 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-535">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="31333-536">Gpo를 보고 만들려면 GPMC (그룹 정책 관리) 콘솔 또는 AGPM (고급 그룹 정책 관리)이 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-536">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

<span data-ttu-id="31333-537">자세한 내용은 [mbam 2.5 그룹 정책 설정](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) 및 [Mbam 2.5 그룹 정책 요구 사항에 대 한 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)편집을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-537">For more information, see [Editing the MBAM 2.5 Group Policy Settings](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) and [Planning for MBAM 2.5 Group Policy Requirements](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).</span></span>
 
### <span data-ttu-id="31333-538">13 단계: MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="31333-538">Step 13: Deploying the MBAM 2.5 Client</span></span>

<span data-ttu-id="31333-539">Microsoft BitLocker 관리 및 모니터링 클라이언트 소프트웨어를 배포 하는 경우 사용자가 컴퓨터를 받기 전이나 나중에 (또는 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여) MBAM 클라이언트 소프트웨어를 배포 하거나 그룹 정책을 구성 하 여 조직의 컴퓨터에서 BitLocker를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-539">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker on a computer in your organization either before the user receives the computer or afterward by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>
 
#### <span data-ttu-id="31333-540">데스크톱 또는 휴대용 컴퓨터에 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="31333-540">Deploy the MBAM Client to desktop or portable computers</span></span>

<span data-ttu-id="31333-541">그룹 정책 설정을 구성한 후 Microsoft System Center 2012 구성 관리자 또는 AD DS (Active Directory 도메인 서비스) 등의 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 대상 컴퓨터에 MBAM 클라이언트 설치 Windows Installer 파일을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-541">After you configure Group Policy settings, you can use an enterprise software deployment system product such as Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services (AD DS) to deploy the MBAM client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="31333-542">32 비트 또는 64 비트 MbamClientSetup.exe 파일을 사용 하거나 32 비트 또는 64 비트 MBAMClient.msi 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-542">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files.</span></span> <span data-ttu-id="31333-543">이는 MBAM 클라이언트 소프트웨어와 함께 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-543">These are provided together with the MBAM Client software.</span></span>

<span data-ttu-id="31333-544">자세한 내용은 [데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트를 배포 하는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-544">For more information, see [How to Deploy the MBAM Client to Desktop or Laptop Computers](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).</span></span>
 
#### <span data-ttu-id="31333-545">Windows 배포의 일부로 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="31333-545">Deploy the MBAM Client as part of a Windows deployment</span></span>

<span data-ttu-id="31333-546">컴퓨터를 중앙에서 받고 구성 하는 조직에서 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 드라이브 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-546">In organizations in which computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="31333-547">이 프로세스의 장점은 모든 컴퓨터가 BitLocker 규격을 준수 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-547">The benefit of this process is that every computer is then BitLocker-compliant.</span></span> <span data-ttu-id="31333-548">관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-548">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="31333-549">이 시나리오의 주요 전제는 조직의 정책이 사용자에 게 컴퓨터를 전달 하기 전에 회사 Windows 이미지를 설치 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="31333-549">A key assumption for this scenario is that the policy of the organization is to install a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="31333-550">PIN을 요구 하도록 그룹 정책 설정을 구성한 경우 사용자가 정책을 받은 후 PIN을 설정 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-550">If the Group Policy settings are configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

<span data-ttu-id="31333-551">자세한 내용은 [Windows 배포의 일부로 MBAM 클라이언트를 배포 하는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-551">For more information, see [How to Deploy the MBAM Client as Part of a Windows Deployment](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).</span></span>
 
#### <span data-ttu-id="31333-552">명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="31333-552">How to deploy the MBAM Client by using a command line</span></span>

<span data-ttu-id="31333-553">자세한 내용은 [명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-553">For more information see [How to Deploy the MBAM Client by Using a Command Line](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).</span></span>

#### <span data-ttu-id="31333-554">클라이언트 배포 후</span><span class="sxs-lookup"><span data-stu-id="31333-554">Post-deployment of clients</span></span>

<span data-ttu-id="31333-555">이제 배포 작업을 완료 했으므로 다음 로그를 검토 하 고 클라이언트가 MBAM 데이터베이스에 성공적으로 보고 되는지 여부를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-555">Now that you have finished the deployment activity, you should review the following logs and determine whether the clients are reporting successfully to the MBAM database.</span></span>

## <span data-ttu-id="31333-556">FAQ</span><span class="sxs-lookup"><span data-stu-id="31333-556">FAQ</span></span>

### <span data-ttu-id="31333-557">부하 분산 된 IIS 서버를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="31333-557">How to create a Load balanced IIS servers</span></span>

* <span data-ttu-id="31333-558">SPN은 친근 한 이름 (예: bitlocker.corp.net)에만 등록 해야 하며 개별 IIS 서버에 등록 되어 있지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-558">SPN must be registered only to the friendly name (for example: bitlocker.corp.net), and must not be registered to individual IIS servers.</span></span>

* <span data-ttu-id="31333-559">인증서를 사용 하는 경우 인증서에는 부하 분산 그룹의 모든 IIS 서버에 대 한 **주체 대체 이름** 필드에 입력 한 FQDN 및 NetBIOS 이름과 친근 한 이름 (예: bitlocker.corp.net)이 모두 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-559">If a certificate is used, the certificate must have both FQDN and NetBIOS names entered into the **Subject Alternative Name** field for all IIS servers in the load balance group and also as the Friendly Name (for example: bitlocker.corp.net).</span></span> <span data-ttu-id="31333-560">그렇지 않으면 부하 분산 된 주소를 검색할 때 인증서가 브라우저에서 신뢰할 수 없는 것으로 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-560">Otherwise, the certificate will be reported as not trusted by the browser when you browse load-balanced addresses.</span></span>

<span data-ttu-id="31333-561">자세한 내용은 [IIS 네트워크 부하 분산](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) 및 [응용 프로그램 풀 계정에 대 한 spn 등록](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-561">For more information, see [IIS Network Load Balancing](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) and [Registering SPNs for the application pool account](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).</span></span>

### <span data-ttu-id="31333-562">인증서를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="31333-562">How to configure a certificate</span></span>

* <span data-ttu-id="31333-563">두 개의 인증서가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-563">You’ll have to have two certificates.</span></span> <span data-ttu-id="31333-564">하나의 인증서가 SQL server에 사용 되 고 그 외에는 IIS에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-564">One certificate is used for SQL server, and the other is used for IIS.</span></span> <span data-ttu-id="31333-565">MBAM 설치를 시작 하기 전에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-565">They must be installed before starting MBAM installation.</span></span>

* <span data-ttu-id="31333-566">설치 관리자를 사용 하 여 web.config 파일을 수동으로 편집 하는 대신 IIS 구성에 인증서를 추가 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-566">We recommend that you use the installer to add the certificate to the IIS configuration instead of manually editing the web.config file.</span></span>

* <span data-ttu-id="31333-567">인증서의 "발급 대상" 필드가 서버 이름과 일치 하지 않는 경우 MBAM 구성자에서 인증서를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-567">The certificate will not be accepted by the MBAM Configurator if the “Issued To” field on the certificate does not match the name of the server.</span></span> <span data-ttu-id="31333-568">이 경우에는 IIS 콘솔에서 자체 서명 된 인증서를 임시로 만들고이를 구성자에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-568">In this case, temporarily create a self-signed certificate from the IIS Console, and use it in the Configurator.</span></span> <span data-ttu-id="31333-569">이렇게 하면 SSL 및 HTTPS에 대해 웹 앱이 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-569">This will make nsure that the Web Apps are installed for SSL and HTTPS.</span></span> <span data-ttu-id="31333-570">그 후에는 MBAM 웹 사이트에 대 한 IIS 바인딩에서 인증서를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-570">After that, you can change the certificate to one from IIS bindings for the MBAM Website.</span></span>

### <span data-ttu-id="31333-571">설치에 필요한 SQL 권한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="31333-571">The SQL permissions requirement for installation</span></span>

<span data-ttu-id="31333-572">MBAM 앱 풀에 대 한 계정을 만들고 SecurityAdmin, Public 및 DBCreator 권한만 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-572">Create an account for MBAM App Pool, and give it only SecurityAdmin, Public, and DBCreator permissions.</span></span>

<span data-ttu-id="31333-573">자세한 내용은 [Mbam 데이터베이스 구성 – 최소 사용 권한을](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-573">See [MBAM Database configuration – minimum permissions](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) for more information.</span></span>

> [!Note]
> * <span data-ttu-id="31333-574">경우에 따라 초기 설치 및 업그레이드 작업에 대 한 추가 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-574">In some situations, more permissions are required for the initial installation and upgrade operations.</span></span>
> * <span data-ttu-id="31333-575">설치에 임시 SA가 있는 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-575">Use an account that has temporary SA for the installation.</span></span>
> * <span data-ttu-id="31333-576">SQL Server에 대 한 변경을 수행할 수 있는 권한이 없는 사용자 계정 (실행)의 컨텍스트에서는 설치 오류를 초래 하므로 구성자를 시작 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="31333-576">Do not start the Configurator in the context of a user account (Run As) that does not have enough permissions to make changes to SQL Server because this will cause installation errors.</span></span>
> * <span data-ttu-id="31333-577">SQL Server에 대 한 사용 권한이 있는 계정을 사용 하 여 로그온 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-577">You must be logged on by using an account that has permissions on SQL Server.</span></span> <span data-ttu-id="31333-578">MBAM Configurator를 원격으로 실행 하 여 SQL Server 데이터베이스만 만들거나 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31333-578">Only SQL Server databases can be created or updated by running MBAM Configurator remotely.</span></span> <span data-ttu-id="31333-579">SSRS 서버의 경우 mbam을 설치 하 고 Configurator를 로컬로 실행 하 여 MBAM SSRS 보고서를 설치 하거나 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-579">For SSRS server, you must install MBAM and run Configurator locally to install or update the MBAM SSRS reports.</span></span>

### <span data-ttu-id="31333-580">SPN 등록에 필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="31333-580">The permission required for SPN Registration</span></span>

<span data-ttu-id="31333-581">IIS 포털 설치에 사용 되는 계정에는 쓰기 ServicePrincipalName 및 확인 된 SPN 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31333-581">An account that's used for IIS portal installation must have Write ServicePrincipalName and Write Validated SPN permissions.</span></span> <span data-ttu-id="31333-582">이러한 권한이 없으면 설치 시 SPN을 등록할 수 없다는 경고 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-582">Without these permissions, the installation will return a warning message that states that it cannot register the SPN.</span></span>

> [!Note]
> <span data-ttu-id="31333-583">이 경고 메시지가 두 번 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-583">You will this receive this warning message twice.</span></span> <span data-ttu-id="31333-584">이는 SPN에 등록 된 두 개체가 있어야 한다는 의미는 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="31333-584">This does not mean that the SPN must have two objects registered to it.</span></span>

<span data-ttu-id="31333-585">자세한 내용은 [Mbam 설정이 "SPN 지연 등록" 오류 메시지와 함께 실패](https://support.microsoft.com/help/2754138/)하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-585">For more information, see [MBAM Setup fails with “Register SPN Deferred” error message](https://support.microsoft.com/help/2754138/).</span></span>

### <span data-ttu-id="31333-586">ADMX 서식 파일을 최신 버전으로 업데이트 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="31333-586">Did I have to update the ADMX templates to the latest version?</span></span>

<span data-ttu-id="31333-587">ADMX 서식 파일을 최신 버전으로 업데이트 한 후 GPO에 대 한 MBAM 루트 노드에서 여러 OS 옵션이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31333-587">You'll see multiple OS options in the MBAM root node for GPO after you update the ADMX templates to their latest versions.</span></span> <span data-ttu-id="31333-588">예를 들어 Windows 7, Windows 8.1 및 Windows 10, 버전 1511 이상 버전.</span><span class="sxs-lookup"><span data-stu-id="31333-588">For example, Windows 7, Windows 8.1, and Windows 10, version 1511 and later versions.</span></span>

<span data-ttu-id="31333-589">ADMX 템플릿을 업데이트 하는 방법에 대 한 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31333-589">For more information about how to update the ADMX templates, see the following articles:</span></span>
* [<span data-ttu-id="31333-590">MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="31333-590">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [<span data-ttu-id="31333-591">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="31333-591">Planning for MBAM 2.5 Group Policy Requirements</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [<span data-ttu-id="31333-592">Microsoft 데스크톱 최적화 팩 그룹 정책 관리 서식 파일</span><span class="sxs-lookup"><span data-stu-id="31333-592">Microsoft Desktop Optimization Pack Group Policy Administrative Templates</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
