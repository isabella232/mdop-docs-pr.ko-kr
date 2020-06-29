---
title: MBAM 2.5 데이터베이스를 구성하는 방법
description: MBAM 2.5 데이터베이스를 구성하는 방법
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826623"
---
# <span data-ttu-id="cf5f9-103">MBAM 2.5 데이터베이스를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5f9-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="cf5f9-104">이 항목에서는 다음을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="cf5f9-105">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf5f9-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="cf5f9-106">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="cf5f9-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="cf5f9-107">이 지침은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에서 권장 되는 아키텍처를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="cf5f9-108">구성을 시작 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cf5f9-109">단계</span><span class="sxs-lookup"><span data-stu-id="cf5f9-109">Step</span></span></th>
<th align="left"><span data-ttu-id="cf5f9-110">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5f9-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cf5f9-111">MBAM에 권장 되는 아키텍처를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="cf5f9-112">MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="cf5f9-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cf5f9-113">MBAM에 대해 지원 되는 구성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cf5f9-114">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="cf5f9-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cf5f9-115">각 서버에서 필수 구성 요소를 완성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cf5f9-116">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cf5f9-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="cf5f9-117">MBAM 2.5 구성 관리자 통합 토폴로지에만 적용 되는 서버 필수 구성 요소 </a> (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="cf5f9-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cf5f9-118">MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cf5f9-119">참고</span><span class="sxs-lookup"><span data-stu-id="cf5f9-119">Note</span></span></strong><br/><p><span data-ttu-id="cf5f9-120">Windows PowerShell 또는 내보낸 데이터 계층 응용 프로그램 (DAC) 패키지를 사용 하 여 원격 SQL Server 컴퓨터에 데이터베이스를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="cf5f9-121">DAC 패키지에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> 데이터 계층 응용 프로그램을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cf5f9-122">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="cf5f9-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cf5f9-123">Windows PowerShell cmdlet을 사용 하 여 MBAM 서버 기능을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 조건을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="cf5f9-124">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="cf5f9-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="cf5f9-125">Windows PowerShell을 사용 하 여 데이터베이스를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="cf5f9-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="cf5f9-126">구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="cf5f9-127">**사용-MbamDatabase** Windows PowerShell cmdlet을 사용 하 여 데이터베이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="cf5f9-128">이 Windows PowerShell cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamDatabase**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="cf5f9-129">마법사를 사용 하 여 준수 및 감사 데이터베이스를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="cf5f9-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="cf5f9-130">데이터베이스를 구성할 서버에서 **Mbam 서버 구성** 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="cf5f9-131">**시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="cf5f9-132">**새 기능 추가**를 클릭 하 **고 준수 및 감사 데이터베이스** 및 **복구 데이터베이스**를 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="cf5f9-133">마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="cf5f9-134">필수 구성 요소 확인에 성공 하면 **다음** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="cf5f9-135">그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="cf5f9-136">다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5f9-137">필드</span><span class="sxs-lookup"><span data-stu-id="cf5f9-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="cf5f9-138">설명</span><span class="sxs-lookup"><span data-stu-id="cf5f9-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-139">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="cf5f9-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-140">준수 및 감사 데이터베이스를 구성 하는 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cf5f9-141">참고</span><span class="sxs-lookup"><span data-stu-id="cf5f9-141">Note</span></span></strong><br/><p><span data-ttu-id="cf5f9-142">Microsoft SQL Server 포트에서 인바운드 트래픽을 사용 하려면 준수 및 감사 데이터베이스 컴퓨터에 예외를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="cf5f9-143">기본 포트 번호는 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-144">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="cf5f9-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-145">준수 및 감사 데이터가 저장 되는 데이터베이스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="cf5f9-146">또한 데이터베이스 정보 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-147">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="cf5f9-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-148">준수 데이터를 저장할 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cf5f9-149">참고</span><span class="sxs-lookup"><span data-stu-id="cf5f9-149">Note</span></span></strong><br/><p><span data-ttu-id="cf5f9-150">이전 버전의 MBAM에서 업그레이드 하는 경우 이전 배포에서 사용한 이름과 동일한 데이터베이스 이름을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-151">읽기/쓰기 액세스 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="cf5f9-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-152">웹 응용 프로그램이이 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록이 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="cf5f9-153">이 필드에 사용자를 입력 하는 경우 <strong> </strong> <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값과 동일 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="cf5f9-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="cf5f9-154">이 필드에 그룹을 입력 하는 경우 <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값 </strong> <strong> </strong> 이이 필드에 입력 하는 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-155">읽기 전용 액세스 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="cf5f9-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-156">보고서에서이 데이터베이스의 준수 데이터에 액세스할 수 있도록이 데이터베이스에 대 한 읽기 전용 권한을 가질 사용자 또는 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="cf5f9-157">이 필드에 사용자를 입력 하는 경우 <strong> </strong> <strong> 보고서 구성 페이지의 규정 준수 및 감사 데이터베이스 도메인 계정 필드에 지정 하는 사용자와 동일 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="cf5f9-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="cf5f9-158">이 필드에 그룹을 입력 하는 경우 <strong> 보고서 구성 페이지의 규정 준수 및 감사 데이터베이스 도메인 계정 필드에 지정한 값 </strong> <strong> </strong> 이이 필드에서 지정 하는 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="cf5f9-159">복구 데이터베이스를 구성 하려면 다음 섹션을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="cf5f9-160">마법사를 사용 하 여 복구 데이터베이스를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="cf5f9-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="cf5f9-161">다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5f9-162">필드</span><span class="sxs-lookup"><span data-stu-id="cf5f9-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="cf5f9-163">설명</span><span class="sxs-lookup"><span data-stu-id="cf5f9-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-164">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="cf5f9-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-165">복구 데이터베이스를 구성 하는 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cf5f9-166">참고</span><span class="sxs-lookup"><span data-stu-id="cf5f9-166">Note</span></span></strong><br/><p><span data-ttu-id="cf5f9-167">Microsoft SQL Server 포트에서 인바운드 트래픽을 사용 하려면 복구 데이터베이스 컴퓨터에 예외를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="cf5f9-168">기본 포트 번호는 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-169">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="cf5f9-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-170">복구 데이터를 저장할 데이터베이스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="cf5f9-171">또한 데이터베이스 정보 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-172">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="cf5f9-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-173">복구 데이터를 저장 하는 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cf5f9-174">참고</span><span class="sxs-lookup"><span data-stu-id="cf5f9-174">Note</span></span></strong><br/><p><span data-ttu-id="cf5f9-175">이전 버전의 MBAM에서 업그레이드 하는 경우 이전 배포에서 사용한 이름과 동일한 데이터베이스 이름을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="cf5f9-176">읽기/쓰기 액세스 도메인 사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="cf5f9-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="cf5f9-177">웹 응용 프로그램이이 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록이 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="cf5f9-178">이 필드에 사용자를 입력 하는 경우 <strong> </strong> <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값과 동일 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="cf5f9-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="cf5f9-179">이 필드에 그룹을 입력 하는 경우 <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값 </strong> <strong> </strong> 이이 필드에 입력 하는 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cf5f9-180">항목을 모두 마쳤으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="cf5f9-181">마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="cf5f9-182">필수 구성 요소 확인에 성공 하면 **다음** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="cf5f9-183">그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 다시 **다음** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="cf5f9-184">**요약** 페이지에서 추가 되는 기능을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="cf5f9-185">참고</span><span class="sxs-lookup"><span data-stu-id="cf5f9-185">Note</span></span>**  
   <span data-ttu-id="cf5f9-186">방금 만든 항목의 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기를**클릭 한 다음 스크립트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="cf5f9-187">**추가** 를 클릭 하 여 서버에 mbam 데이터베이스를 추가 하 고 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="cf5f9-188">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cf5f9-188">Related topics</span></span>


[<span data-ttu-id="cf5f9-189">서버 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="cf5f9-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="cf5f9-190">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="cf5f9-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="cf5f9-191">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5f9-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="cf5f9-192">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5f9-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="cf5f9-193">MBAM 2.5 서버 기능 구성의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="cf5f9-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="cf5f9-194">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="cf5f9-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="cf5f9-195">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="cf5f9-196">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5f9-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





