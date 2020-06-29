---
title: MBAM 2.5 보고서를 구성하는 방법
description: MBAM 2.5 보고서를 구성하는 방법
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826618"
---
# <span data-ttu-id="e8e9d-103">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8e9d-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="e8e9d-104">이 항목에서는 다음을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 보고서 기능을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="e8e9d-105">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="e8e9d-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="e8e9d-106">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="e8e9d-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="e8e9d-107">이 지침은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에서 권장 되는 아키텍처를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="e8e9d-108">구성을 시작 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8e9d-109">단계</span><span class="sxs-lookup"><span data-stu-id="e8e9d-109">Step</span></span></th>
<th align="left"><span data-ttu-id="e8e9d-110">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="e8e9d-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8e9d-111">MBAM에 권장 되는 아키텍처를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="e8e9d-112">MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="e8e9d-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8e9d-113">MBAM에 대해 지원 되는 구성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="e8e9d-114">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="e8e9d-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8e9d-115">각 서버에서 필수 구성 요소를 완성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="e8e9d-116">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e8e9d-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="e8e9d-117">MBAM 2.5 구성 관리자 통합 토폴로지에만 적용 되는 서버 필수 구성 요소 </a> (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="e8e9d-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8e9d-118">MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="e8e9d-119">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="e8e9d-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8e9d-120">Windows PowerShell cmdlet을 사용 하 여 MBAM 서버 기능을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 조건을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="e8e9d-121">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="e8e9d-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="e8e9d-122">Windows PowerShell을 사용 하 여 보고서를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="e8e9d-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="e8e9d-123">구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="e8e9d-124">**사용-MbamReport** Windows PowerShell cmdlet을 사용 하 여 보고서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="e8e9d-125">이 Windows PowerShell cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamReport**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="e8e9d-126">마법사를 사용 하 여 보고서를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="e8e9d-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="e8e9d-127">보고서를 구성할 서버에서 **Mbam 서버 구성** 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="e8e9d-128">**시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="e8e9d-129">**새 기능 추가**를 클릭 하 고 **보고서**를 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="e8e9d-130">마법사에서 보고서에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="e8e9d-131">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="e8e9d-132">다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="e8e9d-133">필드</span><span class="sxs-lookup"><span data-stu-id="e8e9d-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="e8e9d-134">설명</span><span class="sxs-lookup"><span data-stu-id="e8e9d-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e8e9d-135">SQL Server Reporting Services 인스턴스</span><span class="sxs-lookup"><span data-stu-id="e8e9d-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8e9d-136">보고서를 구성 하는 SQL Server Reporting Services의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e8e9d-137">보고 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="e8e9d-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8e9d-138">관리 및 모니터링 서버의 보고서에 액세스할 수 있는 권한이 있는 구성원의 도메인 사용자 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e8e9d-139">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="e8e9d-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8e9d-140">규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e8e9d-141">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="e8e9d-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8e9d-142"><em> </em> 규정 준수 및 감사 데이터베이스가 구성 된 SQL Server 인스턴스의 이름 (예: MSSQLSERVER)입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="e8e9d-143">참고</span><span class="sxs-lookup"><span data-stu-id="e8e9d-143">Note</span></span></strong><br/><p><span data-ttu-id="e8e9d-144">보고 서버의 포트에서 인바운드 트래픽을 사용 하도록 설정 하려면 보고서 컴퓨터에 예외를 추가 해야 합니다 (기본 포트는 80).</span><span class="sxs-lookup"><span data-stu-id="e8e9d-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e8e9d-145">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="e8e9d-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8e9d-146">준수 및 감사 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="e8e9d-147">기본적으로 데이터베이스 이름은 <strong> mbam 준수 상태 이지만 </strong> 준수 및 감사 데이터베이스를 구성할 때 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="e8e9d-148">참고</span><span class="sxs-lookup"><span data-stu-id="e8e9d-148">Note</span></span></strong><br/><p><span data-ttu-id="e8e9d-149">이전 버전의 MBAM에서 업그레이드 하는 경우 이전 배포에 사용 된 이름과 동일한 데이터베이스 이름을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e8e9d-150">준수 및 감사 데이터베이스 도메인 계정</span><span class="sxs-lookup"><span data-stu-id="e8e9d-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8e9d-151">도메인 사용자 계정 및 암호를 사용 하 여 규정 준수 및 감사 데이터베이스에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="e8e9d-152"><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 한 값이 사용자 인 경우 </strong> <strong> </strong> 에는이 필드에 같은 값을 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="e8e9d-153"><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 하는 값이 </strong> <strong> 그룹인 경우 </strong> 이 필드에 입력 하는 값은 해당 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="e8e9d-154">이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="e8e9d-155">사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="e8e9d-156">항목을 모두 마쳤으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="e8e9d-157">마법사에서 보고서 기능에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="e8e9d-158">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="e8e9d-159">**요약** 페이지에서 추가 되는 기능을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="e8e9d-160">참고</span><span class="sxs-lookup"><span data-stu-id="e8e9d-160">Note</span></span>**  
   <span data-ttu-id="e8e9d-161">방금 만든 항목의 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기를**클릭 한 다음 스크립트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="e8e9d-162">**추가** 를 클릭 하 여 서버에 보고서를 추가한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="e8e9d-163">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8e9d-163">Related topics</span></span>


[<span data-ttu-id="e8e9d-164">서버 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="e8e9d-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="e8e9d-165">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="e8e9d-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="e8e9d-166">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8e9d-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="e8e9d-167">MBAM 2.5 서버 기능 구성의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="e8e9d-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="e8e9d-168">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="e8e9d-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e8e9d-169">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e8e9d-170">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e9d-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






