---
title: 테스트 환경에서 MBAM 2.5 평가
description: 테스트 환경에서 MBAM 2.5 평가
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823153"
---
# <span data-ttu-id="cf5ce-103">테스트 환경에서 MBAM 2.5 평가</span><span class="sxs-lookup"><span data-stu-id="cf5ce-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="cf5ce-104">이 항목에서는 독립 실행형 또는 System Center Configuration Manager 통합 토폴로지에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 평가 하도록 테스트 환경을 설정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="cf5ce-105">독립 실행형 토폴로지를 사용 하 여 MBAM 2.5 평가</span><span class="sxs-lookup"><span data-stu-id="cf5ce-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="cf5ce-106">독립 실행형 토폴로지를 사용 하 여 MBAM을 평가 하려면 다음 표의 정보를 사용 하 여 MBAM 서버 소프트웨어를 설치한 다음 테스트 환경에서 MBAM 서버 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="cf5ce-107">독립 실행형 토폴로지를 사용 하 여 MBAM 2.5을 평가 하려면</span><span class="sxs-lookup"><span data-stu-id="cf5ce-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="cf5ce-108">MBAM을 설치 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5ce-109">작업</span><span class="sxs-lookup"><span data-stu-id="cf5ce-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="cf5ce-110">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-111">필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cf5ce-112">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cf5ce-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-113">필수 하드웨어, RAM 및 기타 사양을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cf5ce-114">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="cf5ce-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-115">Cmdlet을 사용 하 여 MBAM을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="cf5ce-116">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="cf5ce-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cf5ce-117">MBAM 서버 소프트웨어를 설치한 다음 원하는 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5ce-118">작업</span><span class="sxs-lookup"><span data-stu-id="cf5ce-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="cf5ce-119">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-120">MBAM 서버 기능을 구성 하려는 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cf5ce-121">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-122">준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="cf5ce-123">MBAM 2.5 데이터베이스를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-124">보고서 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="cf5ce-125">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-126">웹 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="cf5ce-127">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="cf5ce-128">클라이언트 컴퓨터에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-129">클라이언트 컴퓨터에 MBAM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="cf5ce-130">컴퓨터에 MBAM Gpo (그룹 정책 개체)를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="cf5ce-131">다음 레지스트리 키를 설정 하 여 MBAM 클라이언트가 정기적인 간격으로 더 빠르게 절전 모드를 해제 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="cf5ce-132">참고</span><span class="sxs-lookup"><span data-stu-id="cf5ce-132">Note</span></span>**  
       <span data-ttu-id="cf5ce-133">이러한 키는 약 MBAM 클라이언트를 종료 하므로 테스트 환경 에서만 이러한 레지스트리 키 설정을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="cf5ce-134">**BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="cf5ce-135">System Center 2012 Configuration Manager 통합 토폴로지를 사용 하 여 MBAM 2.5 평가</span><span class="sxs-lookup"><span data-stu-id="cf5ce-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="cf5ce-136">Configuration Manager 통합 토폴로지를 사용 하 여 MBAM을 평가 하려면 다음 표의 정보를 사용 하 여 MBAM 서버 소프트웨어를 설치한 다음 테스트 환경에서 MBAM 서버 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="cf5ce-137">클라이언트 컴퓨터에 MBAM 클라이언트를 설치한 후에는 MBAM 클라이언트가 컴퓨터의 상태를 MBAM에 더 빠르게 보고 하도록 하는 추가 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="cf5ce-138">System Center 2012 Configuration Manager 통합 토폴로지를 사용 하 여 MBAM 2.5을 평가 하려면</span><span class="sxs-lookup"><span data-stu-id="cf5ce-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="cf5ce-139">MBAM을 설치 하기 전에 필수 구성 요소 소프트웨어 및 지원 되는 구성을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5ce-140">작업</span><span class="sxs-lookup"><span data-stu-id="cf5ce-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="cf5ce-141">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-142">필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cf5ce-143">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cf5ce-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="cf5ce-144">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cf5ce-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-145">필수 하드웨어, RAM 및 기타 사양을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cf5ce-146">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="cf5ce-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-147">Cmdlet을 사용 하 여 MBAM을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="cf5ce-148">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="cf5ce-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-149">.Mof 파일을 만들거나 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="cf5ce-150">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="cf5ce-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="cf5ce-151">Sms_def.mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="cf5ce-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cf5ce-152">MBAM 서버 소프트웨어를 설치한 다음 원하는 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5ce-153">작업</span><span class="sxs-lookup"><span data-stu-id="cf5ce-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="cf5ce-154">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-155">MBAM 서버 기능을 구성 하려는 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cf5ce-156">참고</span><span class="sxs-lookup"><span data-stu-id="cf5ce-156">Note</span></span></strong><br/><p><span data-ttu-id="cf5ce-157">Windows PowerShell 또는 내보낸 데이터 계층 응용 프로그램 (DAC) 패키지를 사용 하 여 원격 SQL Server 컴퓨터에 데이터베이스를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="cf5ce-158">DAC 패키지에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> 데이터 계층 응용 프로그램을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cf5ce-159">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-160">준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="cf5ce-161">MBAM 2.5 데이터베이스를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-162">보고서 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="cf5ce-163">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-164">웹 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="cf5ce-165">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-166">System Center Configuration Manager를 구성 하 여 Configuration Manager 개체를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="cf5ce-167">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="cf5ce-168">클라이언트 컴퓨터에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-169">클라이언트 컴퓨터에 MBAM 클라이언트와 Configuration Manager 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="cf5ce-170">컴퓨터에 MBAM 그룹 정책 개체를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="cf5ce-171">다음 레지스트리 키를 설정 하 여 MBAM 클라이언트가 정기적인 간격으로 더 빠르게 절전 모드를 해제 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="cf5ce-172">참고</span><span class="sxs-lookup"><span data-stu-id="cf5ce-172">Note</span></span>**  
       <span data-ttu-id="cf5ce-173">이러한 키는 약 MBAM 클라이언트를 종료 하므로 테스트 환경 에서만 이러한 레지스트리 키 설정을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="cf5ce-174">**BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="cf5ce-175">제어판에서 **구성 관리자**를 연 다음 **작업** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="cf5ce-176">**하드웨어 인벤토리 주기**를 선택한 다음 **지금 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="cf5ce-177">이 단계에서는 .mof 파일로 가져온 새 클래스를 사용 하 여 하드웨어 인벤토리를 실행 한 다음 데이터를 Configuration Manager 서버로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="cf5ce-178">**컴퓨터 정책 검색 & 평가 주기**를 선택한 다음 **지금 실행** 을 클릭 하 여 해당 클라이언트 컴퓨터와 관련 된 그룹 정책 개체를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="cf5ce-179">Configuration Manager 콘솔에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-180">탐색 창에서 **Mbam 지원 컴퓨터**를 마우스 오른쪽 단추로 클릭 하 고 **구성원 업데이트**를 클릭 한 다음 **예** 를 클릭 하 여 클라이언트 컴퓨터가 구성원 자격을 즉시 보고 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="cf5ce-181">탐색 창에서 **Mbam (지원 되는 컴퓨터** )을 클릭 하 여 클라이언트 컴퓨터가 컬렉션에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="cf5ce-182">클라이언트 컴퓨터의 제어판에서 **구성 관리자** 를 다시 열고 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-183">**동작** 탭을 클릭 한 다음 **컴퓨터 정책 검색 & 평가 주기**를 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="cf5ce-184">**구성** 탭을 클릭 하 고 BitLocker 기준을 선택한 다음 **평가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="cf5ce-185">Configuration Manager 콘솔에서 다음과 같이 엔터프라이즈 준수 보고서에 클라이언트 컴퓨터가 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="cf5ce-186">탐색 창에서 **모니터링** 작업 영역을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="cf5ce-187">콘솔 트리에서 " **개요** &gt; **보고** &gt; **보고서** " &gt; **mbam**을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="cf5ce-188">보고서를 표시할 언어를 나타내는 폴더를 선택한 다음 결과 창에서 보고서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="cf5ce-189">System Center Configuration Manager 2007 통합 토폴로지를 사용 하 여 MBAM 2.5 평가</span><span class="sxs-lookup"><span data-stu-id="cf5ce-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="cf5ce-190">Configuration Manager 통합 토폴로지를 사용 하 여 MBAM을 평가 하려면 프로덕션 환경에서 사용 하는 것과 동일한 단계를 따라 테스트 환경에 MBAM을 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="cf5ce-191">클라이언트 컴퓨터에 MBAM 클라이언트를 설치한 후에이 항목의 추가 단계를 완료 하 여 MBAM 클라이언트가 컴퓨터의 상태를 MBAM에 더 빠르게 보고 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="cf5ce-192">Configuration Manager 2007 통합 토폴로지를 사용 하 여 MBAM을 평가 하려면</span><span class="sxs-lookup"><span data-stu-id="cf5ce-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="cf5ce-193">MBAM을 설치 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5ce-194">작업</span><span class="sxs-lookup"><span data-stu-id="cf5ce-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="cf5ce-195">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-196">필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cf5ce-197">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cf5ce-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="cf5ce-198">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cf5ce-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-199">필수 하드웨어, RAM 및 기타 사양을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cf5ce-200">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="cf5ce-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-201">.Mof 파일을 만들거나 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="cf5ce-202">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="cf5ce-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="cf5ce-203">Sms_def.mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="cf5ce-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cf5ce-204">MBAM 서버 소프트웨어를 설치한 다음 원하는 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cf5ce-205">작업</span><span class="sxs-lookup"><span data-stu-id="cf5ce-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="cf5ce-206">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-207">MBAM 서버 기능을 구성 하려는 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cf5ce-208">참고</span><span class="sxs-lookup"><span data-stu-id="cf5ce-208">Note</span></span></strong><br/><p><span data-ttu-id="cf5ce-209">Windows PowerShell 또는 내보낸 데이터 계층 응용 프로그램 (DAC) 패키지를 사용 하 여 원격 SQL Server 컴퓨터에 데이터베이스를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="cf5ce-210">DAC 패키지에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> 데이터 계층 응용 프로그램을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cf5ce-211">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="cf5ce-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-212">준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="cf5ce-213">MBAM 2.5 데이터베이스를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-214">보고서 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="cf5ce-215">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cf5ce-216">웹 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="cf5ce-217">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cf5ce-218">System Center Configuration Manager를 구성 하 여 Configuration Manager 개체를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="cf5ce-219">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf5ce-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="cf5ce-220">클라이언트 컴퓨터에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-221">클라이언트 컴퓨터에 MBAM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="cf5ce-222">컴퓨터에 MBAM 그룹 정책 개체를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="cf5ce-223">다음 레지스트리 키를 설정 하 여 MBAM 클라이언트가 더 빨리 종료 되 고 더 빠른 간격으로 절전 모드를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="cf5ce-224">참고</span><span class="sxs-lookup"><span data-stu-id="cf5ce-224">Note</span></span>**  
       <span data-ttu-id="cf5ce-225">이러한 키는 기본적으로 약 MBAM 클라이언트를 사용 하기 때문에 평가 환경 에서만 이러한 레지스트리 키 설정을 사용할 것을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="cf5ce-226">**BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="cf5ce-227">제어판에서 **구성 관리자**를 연 다음 **작업** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="cf5ce-228">**컴퓨터 정책 검색 & 평가 주기**를 선택한 다음 **지금 실행** 을 클릭 하 여 해당 클라이언트 컴퓨터와 관련 된 그룹 정책 개체를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="cf5ce-229">**하드웨어 인벤토리 주기**를 선택한 다음 **지금 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="cf5ce-230">이 단계에서는 .mof 파일로 가져온 새 클래스를 사용 하 여 하드웨어 인벤토리를 실행 한 다음 데이터를 Configuration Manager 서버로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="cf5ce-231">Configuration Manager 콘솔에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-232">탐색 창에서 **Mbam 지원 컴퓨터**를 마우스 오른쪽 단추로 클릭 하 고 **구성원 업데이트**를 클릭 한 다음 **예** 를 클릭 하 여 클라이언트 컴퓨터가 구성원 자격을 즉시 보고 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="cf5ce-233">탐색 창에서 **Mbam (지원 되는 컴퓨터** )을 클릭 하 여 클라이언트 컴퓨터가 컬렉션에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="cf5ce-234">클라이언트 컴퓨터의 제어판에서 **구성 관리자** 를 다시 열고 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="cf5ce-235">**동작** 탭을 클릭 한 다음 **컴퓨터 정책 검색 & 평가 주기**를 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="cf5ce-236">**구성** 탭을 클릭 하 고 BitLocker 기준선을 선택한 다음 **평가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="cf5ce-237">Configuration Manager 콘솔에서 다음과 같이 엔터프라이즈 준수 보고서에 클라이언트 컴퓨터가 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="cf5ce-238">탐색 창에서 **컴퓨터 관리** &gt; **reporting** &gt; **Services** &gt; \*\* &lt; 서버 이름 &gt; mbam\*\*을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="cf5ce-239">**Mbam** 노드 내에서 보고서를 볼 언어를 나타내는 폴더를 선택한 다음 결과 창에서 보고서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="cf5ce-240">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cf5ce-240">Related topics</span></span>


[<span data-ttu-id="cf5ce-241">MBAM 2.5 시작</span><span class="sxs-lookup"><span data-stu-id="cf5ce-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="cf5ce-242">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="cf5ce-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="cf5ce-243">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="cf5ce-244">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf5ce-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





