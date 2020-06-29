---
title: MBAM 2.5 서버 기능 구성의 유효성 검사
description: MBAM 2.5 서버 기능 구성의 유효성 검사
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827083"
---
# <span data-ttu-id="a662e-103">MBAM 2.5 서버 기능 구성의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="a662e-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="a662e-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 서버 기능 배포를 완료 한 경우 모든 기능이 성공적으로 구성 되었는지 배포의 유효성을 검사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="a662e-105">배포한 토폴로지 (독립 실행형 또는 System Center Configuration Manager 통합)와 일치 하는 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="a662e-106">독립 실행형 토폴로지를 사용 하 여 MBAM 서버 배포 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="a662e-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="a662e-107">다음 단계를 사용 하 여 단독 토폴로지로 MBAM 서버 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="a662e-108">독립 실행형 MBAM 서버 배포의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="a662e-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="a662e-109">Mbam 기능이 배포 되는 각 서버에서 **제어판** &gt; **프로그램** 프로그램 &gt; **및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="a662e-110">**Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="a662e-111">참고</span><span class="sxs-lookup"><span data-stu-id="a662e-111">Note</span></span>**  
    <span data-ttu-id="a662e-112">유효성 검사를 수행 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="a662e-113">복구 데이터베이스가 구성 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="a662e-114">준수 및 감사 데이터베이스가 구성 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태 데이터베이스가** 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="a662e-115">보고서 기능이 구성 된 서버에서 관리 자격 증명을 사용 하는 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="a662e-116">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="a662e-117">http (s)// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /Reports.aspx</span><span class="sxs-lookup"><span data-stu-id="a662e-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="a662e-118">실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정한 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="a662e-119">**Microsoft BitLocker 관리 및 모니터링** 이라는 보고서 폴더에 **MaltaDataSource** 이라는 데이터 원본과 언어 폴더가 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="a662e-120">데이터 원본에는 언어를 나타내는 이름 (예: en-us)이 포함 된 폴더가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="a662e-121">보고서는 언어 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="a662e-122">참고</span><span class="sxs-lookup"><span data-stu-id="a662e-122">Note</span></span>**  
    <span data-ttu-id="a662e-123">SQL Server Reporting Services (SSRS)가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http (s)// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="a662e-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="a662e-124">관리 및 모니터링 웹 사이트 기능이 구성 된 서버에서 **서버 관리자**를 실행 하 고 **역할**을 찾은 다음 **웹 서버 (iis** ) &gt; **iis (인터넷 정보 서비스) 관리자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="a662e-125">**연결**에서 \* &lt; 컴퓨터 이름 &gt; \* 으로 이동 하 여 **Sites** &gt; **Microsoft BitLocker 관리 및 모니터링**사이트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="a662e-126">다음이 나열 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="a662e-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="a662e-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="a662e-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="a662e-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="a662e-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="a662e-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="a662e-130">관리 및 모니터링 웹 사이트와 셀프 서비스 포털이 구성 된 서버에서 관리 자격 증명을 사용 하 여 웹 브라우저를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="a662e-131">다음 웹 사이트를 탐색 하 여 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="a662e-132">https// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /HelpDesk/-탐색 및 보고서에 대 한 각 링크 확인</span><span class="sxs-lookup"><span data-stu-id="a662e-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="a662e-133">http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /SelfService/</span><span class="sxs-lookup"><span data-stu-id="a662e-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="a662e-134">참고</span><span class="sxs-lookup"><span data-stu-id="a662e-134">Note</span></span>**  
   <span data-ttu-id="a662e-135">네트워크 암호화 없이 기본 포트에서 서버 기능을 구성한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="a662e-136">다른 포트 또는 가상 디렉터리에 서버 기능을 구성한 경우에는 다음과 같이 해당 포트를 포함 하도록 Url을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="a662e-137">http (s)// &lt; *호스트 이름* &gt; : &lt; *포트* &gt; /HelpDesk/</span><span class="sxs-lookup"><span data-stu-id="a662e-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="a662e-138">http (s)// &lt; *호스트 이름* &gt; : &lt; *포트* &gt; / &lt; *virtualdirectory*&gt;/</span><span class="sxs-lookup"><span data-stu-id="a662e-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="a662e-139">네트워크 암호화를 사용 하 여 서버 기능을 구성한 경우 http://를 https://로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="a662e-140">다음 웹 서비스를 찾아 제대로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="a662e-141">서비스가 실행 중임을 나타내는 페이지가 열리고, 페이지에 메타 데이터가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="a662e-142">http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="a662e-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="a662e-143">http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="a662e-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="a662e-144">http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="a662e-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="a662e-145">http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="a662e-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="a662e-146">Configuration Manager 통합 토폴로지를 사용 하 여 MBAM 서버 배포 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="a662e-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="a662e-147">다음 단계를 사용 하 여 Configuration Manager 통합 토폴로지로 MBAM 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="a662e-148">사용 중인 구성 관리자 버전과 일치 하는 유효성 검사 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="a662e-149">System Center 2012 구성 관리자를 사용 하 여 MBAM 서버 배포 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="a662e-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="a662e-150">시스템 센터 2012 구성 관리자에서 MBAM을 사용 하는 경우 다음 단계를 사용 하 여 MBAM 서버 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="a662e-151">Configuration Manager 통합의 유효성을 검사 하려면 MBAM 서버 배포 – 시스템 센터 2012 구성 관리자</span><span class="sxs-lookup"><span data-stu-id="a662e-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="a662e-152">System Center 2012 구성 관리자가 배포 되는 서버에서 **제어판**의 **프로그램 및 기능** 을 열고 **Microsoft BitLocker 관리 및 모니터링** 이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="a662e-153">참고</span><span class="sxs-lookup"><span data-stu-id="a662e-153">Note</span></span>**  
    <span data-ttu-id="a662e-154">구성의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="a662e-155">Configuration Manager 콘솔에서 **자산 및 준수** 작업 영역 &gt; **디바이스 모음**을 클릭 하 고 **Mbam이 지원** 되는 컴퓨터 라는 새 컬렉션이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="a662e-156">Configuration Manager 콘솔에서 **모니터링** 작업 영역 &gt; **보고** &gt; **보고서** ( &gt; **mbam**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="a662e-157">**Mbam** 폴더에 다른 언어를 나타내는 이름을 가진 하위 폴더가 있고 각 언어 하위 폴더에 다음 보고서가 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="a662e-158">BitLocker 컴퓨터 준수</span><span class="sxs-lookup"><span data-stu-id="a662e-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="a662e-159">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="a662e-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="a662e-160">BitLocker 엔터프라이즈 준수 세부 정보</span><span class="sxs-lookup"><span data-stu-id="a662e-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="a662e-161">BitLocker Enterprise 규정 준수 요약</span><span class="sxs-lookup"><span data-stu-id="a662e-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="a662e-162">Configuration Manager 콘솔에서 **자산 및 준수** 작업 영역 &gt; **준수 설정** &gt; **구성 기준을**클릭 하 고 구성 기준 **BitLocker 보호가** 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="a662e-163">Configuration Manager 콘솔에서 **자산 및 준수** 작업 영역 &gt; **준수 설정** &gt; **구성 항목**을 클릭 하 고 다음 새 구성 항목이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="a662e-164">BitLocker 고정 데이터 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="a662e-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="a662e-165">BitLocker 운영 체제 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="a662e-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="a662e-166">Configuration Manager 2007를 사용 하 여 MBAM 서버 배포 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="a662e-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="a662e-167">이 단계를 사용 하 여 구성 관리자 2007에서 MBAM을 사용 하는 경우 MBAM 서버 배포의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="a662e-168">Configuration Manager 통합의 유효성을 검사 하려면 MBAM 서버 배포-구성 관리자 2007</span><span class="sxs-lookup"><span data-stu-id="a662e-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="a662e-169">Configuration Manager 2007을 배포한 서버에서 **제어판** 의 **프로그램 및 기능** 을 열고 **Microsoft BitLocker 관리 및 모니터링** 이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="a662e-170">참고</span><span class="sxs-lookup"><span data-stu-id="a662e-170">Note</span></span>**  
    <span data-ttu-id="a662e-171">구성의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="a662e-172">Configuration Manager 콘솔에서 **사이트 데이터베이스 &lt; SiteCode &gt;  -  &lt; ServerName &gt; , &lt; SiteName &gt; ), 컴퓨터 관리**를 차례로 클릭 하 고 **mbam 지원 컴퓨터** 라는 새 컬렉션이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="a662e-173">Configuration Manager 콘솔에서 reporting **Reporting** &gt; **Services** &gt; \*\* \\\\ &lt; 서버 이름 &gt; \*\* 보고 &gt; **보고서 폴더** 를 클릭 &gt; **MBAM**합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="a662e-174">**Mbam** 폴더에 다른 언어를 나타내는 이름을 가진 하위 폴더가 있고 각 언어 하위 폴더에 다음 보고서가 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="a662e-175">BitLocker 컴퓨터 준수</span><span class="sxs-lookup"><span data-stu-id="a662e-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="a662e-176">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="a662e-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="a662e-177">BitLocker 엔터프라이즈 준수 세부 정보</span><span class="sxs-lookup"><span data-stu-id="a662e-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="a662e-178">BitLocker Enterprise 규정 준수 요약</span><span class="sxs-lookup"><span data-stu-id="a662e-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="a662e-179">Configuration Manager 콘솔에서 **원하는 구성 관리** &gt; **구성 기준을**클릭 하 고 구성 기준 **BitLocker 보호가** 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="a662e-180">Configuration Manager 콘솔에서 **원하는 구성 관리** &gt; **구성 항목**을 클릭 하 고 다음 새 구성 항목이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="a662e-181">BitLocker 고정 데이터 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="a662e-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="a662e-182">BitLocker 운영 체제 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="a662e-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="a662e-183">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a662e-183">Related topics</span></span>


[<span data-ttu-id="a662e-184">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="a662e-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="a662e-185">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="a662e-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a662e-186">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a662e-187">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a662e-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






