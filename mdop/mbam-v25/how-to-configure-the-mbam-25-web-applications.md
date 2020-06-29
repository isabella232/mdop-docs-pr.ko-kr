---
title: MBAM 2.5 웹 응용 프로그램을 구성하는 방법
description: MBAM 2.5 웹 응용 프로그램을 구성하는 방법
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824498"
---
# <span data-ttu-id="53f1c-103">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="53f1c-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="53f1c-104">이 항목에서는 다음 방법 중 하나를 사용 하 여 [mbam 2.5의 권장 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md) 에 대해 Microsoft BitLocker 관리 및 모니터링 (mbam) 2.5 웹 응용 프로그램을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="53f1c-105">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f1c-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="53f1c-106">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="53f1c-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="53f1c-107">웹 응용 프로그램에는 다음 웹 사이트와 해당 웹 서비스가 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="53f1c-108">Website</span><span class="sxs-lookup"><span data-stu-id="53f1c-108">Website</span></span></th>
<th align="left"><span data-ttu-id="53f1c-109">설명</span><span class="sxs-lookup"><span data-stu-id="53f1c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53f1c-110">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="53f1c-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="53f1c-111">지정 된 사용자가 보고서를 볼 수 있고 사용자가 PIN 또는 암호를 잊어버린 경우 컴퓨터를 복구 하는 데 도움이 되는 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="53f1c-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53f1c-112">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="53f1c-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="53f1c-113">자신의 PIN 또는 암호를 잊어버린 경우 최종 사용자가 개별적으로 액세스할 수 있는 웹 사이트의 컴퓨터에 대 한 액세스 권한 다시 가져오기</span><span class="sxs-lookup"><span data-stu-id="53f1c-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="53f1c-114">구성을 시작 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="53f1c-115">단계</span><span class="sxs-lookup"><span data-stu-id="53f1c-115">Step</span></span></th>
<th align="left"><span data-ttu-id="53f1c-116">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="53f1c-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53f1c-117">MBAM에 권장 되는 아키텍처를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="53f1c-118">MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="53f1c-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53f1c-119">MBAM에 대해 지원 되는 구성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="53f1c-120">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="53f1c-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53f1c-121">각 서버에서 필수 구성 요소를 완성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53f1c-122">참고</span><span class="sxs-lookup"><span data-stu-id="53f1c-122">Note</span></span></strong><br/><p><span data-ttu-id="53f1c-123">관리 및 모니터링 웹 사이트를 구성 하기 전에 SSL (Secure Sockets layer)을 사용 하도록 SQL ServerReporting Services (SSRS)를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="53f1c-124">그렇지 않으면 보고서 기능이 HTTPS 대신 HTTP를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="53f1c-125">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="53f1c-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="53f1c-126">MBAM 2.5 구성 관리자 통합 토폴로지에만 적용 되는 서버 필수 구성 요소 </a> (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="53f1c-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53f1c-127">웹 사이트의 응용 프로그램 풀 계정에 대 한 Spn (서비스 사용자 이름)을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="53f1c-128">AD DS (Active Directory 도메인 서비스)에 관리 도메인 권한이 없는 경우에만이 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="53f1c-129">AD DS에 이러한 권한이 있으면 MBAM이 사용자를 위한 Spn을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="53f1c-130">MBAM 웹 사이트를 보호하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="53f1c-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53f1c-131">MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53f1c-132">참고</span><span class="sxs-lookup"><span data-stu-id="53f1c-132">Note</span></span></strong><br/><p><span data-ttu-id="53f1c-133">웹 사이트를 한 대의 서버에 설치 하는 경우에는 <strong> 사용-MbamWebApplication Windows PowerShell cmdlet을 사용 하는 것 으로만 구성할 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="53f1c-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="53f1c-134">MBAM 서버 구성 마법사는 별도의 서버에서 이러한 항목을 구성 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="53f1c-135">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="53f1c-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53f1c-136">Cmdlet을 사용 하 여 MBAM 서버 기능을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 조건을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="53f1c-137">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="53f1c-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="53f1c-138">Windows PowerShell을 사용 하 여 웹 응용 프로그램을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="53f1c-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="53f1c-139">구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53f1c-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="53f1c-140">**Enable-MbamWebApplication** cmdlet을 사용 하 여 Windows PowerShell을 사용 하 여 웹 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="53f1c-141">이 cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamWebApplication**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="53f1c-142">마법사를 사용 하 여 모든 웹 응용 프로그램에 대 한 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="53f1c-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="53f1c-143">웹 응용 프로그램을 구성할 서버에서 MBAM 서버 구성 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="53f1c-144">**시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="53f1c-145">**새 기능 추가**를 클릭 하 **고 관리 및 모니터링 웹 사이트** 및 **셀프 서비스 포털**을 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="53f1c-146">마법사는 웹 응용 프로그램에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="53f1c-147">필수 구성 요소 확인에 성공 하면 **다음** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="53f1c-148">그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="53f1c-149">다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="53f1c-150">필드</span><span class="sxs-lookup"><span data-stu-id="53f1c-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="53f1c-151">설명</span><span class="sxs-lookup"><span data-stu-id="53f1c-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-152">보안 인증서</span><span class="sxs-lookup"><span data-stu-id="53f1c-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-153">이전에 만든 인증서를 선택 하 여 웹 사이트를 구성 하는 웹 서비스와 서버 간의 통신을 선택적으로 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="53f1c-154"><strong>인증서 사용 안 함을 선택 하면 </strong> 웹 통신이 안전 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="53f1c-155">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="53f1c-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-156">웹 사이트를 구성 하는 호스트 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-157">설치 경로</span><span class="sxs-lookup"><span data-stu-id="53f1c-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-158">웹 사이트를 설치 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="53f1c-159">Port</span><span class="sxs-lookup"><span data-stu-id="53f1c-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-160">웹 사이트 및 서비스 통신에 사용 하는 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="53f1c-161">참고</span><span class="sxs-lookup"><span data-stu-id="53f1c-161">Note</span></span></strong><br/><p><span data-ttu-id="53f1c-162">지정 된 포트를 통해 통신을 사용 하도록 설정 하려면 방화벽 예외를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-163">웹 서비스 응용 프로그램 풀 도메인 계정 및 암호</span><span class="sxs-lookup"><span data-stu-id="53f1c-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-164">웹 서비스 응용 프로그램 풀에 대 한 도메인 사용자 계정 및 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="53f1c-165"><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 사용자 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 같은 값을 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="53f1c-166"><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 그룹 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 입력 하는 값은 해당 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="53f1c-167">자격 증명을 지정 하지 않으면 이전에 사용 하도록 설정 된 웹 응용 프로그램에 대해 지정 된 자격 증명이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="53f1c-168">모든 웹 응용 프로그램은 동일한 응용 프로그램 풀 자격 증명을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="53f1c-169">여러 웹 응용 프로그램에 대해 다른 자격 증명을 지정 하는 경우 가장 최근에 지정 된 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="53f1c-170">중요</span><span class="sxs-lookup"><span data-stu-id="53f1c-170">Important</span></span></strong><br/><p><span data-ttu-id="53f1c-171">보안 향상을 위해 자격 증명에 지정 된 계정에 제한 된 사용자 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="53f1c-172">또한 계정 암호가 만료 되지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="53f1c-173">**인증 후** 기본 제공 IIS \ _IUSRS 계정이 나 응용 프로그램 풀 계정이 클라이언트 가장으로 추가 되었는지 확인 하 고 **일괄 작업으로 로그온** 로컬 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="53f1c-174">로컬 보안 설정에 추가 되었는지 여부를 확인 하려면 **로컬 보안 정책 편집기**를 열고, **로컬 정책** 노드를 확장 하 고, **사용자 권한 할당** 노드를 클릭 하 고, **인증 후 클라이언트로 가장** 을 두 번 클릭 하 고 권한으로 로그인 한 다음에는, **일괄 작업으로 로그온** 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="53f1c-175">마법사를 사용 하 여 데이터베이스에 대 한 연결 정보를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="53f1c-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="53f1c-176">마법사에서 준수 및 감사 데이터베이스에 대 한 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="53f1c-177">필드</span><span class="sxs-lookup"><span data-stu-id="53f1c-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="53f1c-178">설명</span><span class="sxs-lookup"><span data-stu-id="53f1c-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="53f1c-179">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="53f1c-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="53f1c-180">규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="53f1c-181">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="53f1c-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="53f1c-182">규정 준수 및 감사 데이터베이스가 구성 된 SQL Server 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="53f1c-183">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="53f1c-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="53f1c-184">준수 및 감사 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="53f1c-185">복구 데이터베이스에 대 한 마법사에서 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="53f1c-186">필드</span><span class="sxs-lookup"><span data-stu-id="53f1c-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="53f1c-187">설명</span><span class="sxs-lookup"><span data-stu-id="53f1c-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="53f1c-188">SQL Server 이름</span><span class="sxs-lookup"><span data-stu-id="53f1c-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="53f1c-189">복구 데이터베이스가 구성 된 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="53f1c-190">SQL Server 데이터베이스 인스턴스</span><span class="sxs-lookup"><span data-stu-id="53f1c-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="53f1c-191">복구 데이터베이스가 구성 된 SQL Server 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="53f1c-192">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="53f1c-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="53f1c-193">복구 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="53f1c-194">마법사를 사용 하 여 웹 응용 프로그램을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="53f1c-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="53f1c-195">마법사에서 필드 값을 입력 하 여 관리 및 모니터링 웹 사이트를 구성 하려면 다음 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="53f1c-196">필드</span><span class="sxs-lookup"><span data-stu-id="53f1c-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="53f1c-197">설명</span><span class="sxs-lookup"><span data-stu-id="53f1c-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-198">고급 헬프데스크 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="53f1c-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-199">구성원이 보고서 영역을 제외한 관리 및 모니터링 웹 사이트의 모든 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="53f1c-200">헬프데스크 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="53f1c-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-201">구성원이 <strong> </strong> <strong> </strong> 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-202">System Center Configuration Manager 통합 사용</span><span class="sxs-lookup"><span data-stu-id="53f1c-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-203">Configuration Manager 통합 토폴로지에서 MBAM을 구성 하는 경우이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="53f1c-204">이 확인란을 선택 하면 복구 감사 보고서를 제외한 모든 보고서가 관리 및 모니터링 웹 사이트 대신 구성 관리자에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="53f1c-205">보고 역할 도메인 그룹</span><span class="sxs-lookup"><span data-stu-id="53f1c-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-206">구성원에 게 관리 및 모니터링 웹 사이트의 보고서 영역에 대 한 읽기 전용 액세스 권한이 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-207">SQL Server Reporting Services URL</span><span class="sxs-lookup"><span data-stu-id="53f1c-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-208">MBAM 보고서가 구성 된 SSRS 서버의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="53f1c-209">보고서 Url의 예:</span><span class="sxs-lookup"><span data-stu-id="53f1c-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="53f1c-210">호스트 이름 유형</span><span class="sxs-lookup"><span data-stu-id="53f1c-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="53f1c-211">예</span><span class="sxs-lookup"><span data-stu-id="53f1c-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="53f1c-212">정규화 된 도메인 이름의 예</span><span class="sxs-lookup"><span data-stu-id="53f1c-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="53f1c-213">사용자 지정 호스트 이름을 사용 하는 예제</span><span class="sxs-lookup"><span data-stu-id="53f1c-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="53f1c-214">가상 디렉터리</span><span class="sxs-lookup"><span data-stu-id="53f1c-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-215">관리 및 모니터링 웹 사이트의 가상 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="53f1c-216">이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당 하 고 웹 사이트의 호스트 이름 (예:)에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="53f1c-217">http (s)// &lt; <em> 호스트 이름 </em> &gt; : &lt; <em> 포트 </em> &gt; /HelpDesk/</span><span class="sxs-lookup"><span data-stu-id="53f1c-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="53f1c-218">가상 디렉터리를 지정 하지 않으면 값 <strong> 헬프데스크를 </strong> 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-219">데이터 마이그레이션 역할 도메인 그룹 </strong> (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53f1c-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-220">해당 멤버가이 끝점을 통해 복구 정보를 기록할 수 있는 액세스 권한이 있는 도메인 사용자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="53f1c-221">마법사에서 필드 값을 입력 하 여 셀프 서비스 포털을 구성 하려면 다음 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="53f1c-222">필드</span><span class="sxs-lookup"><span data-stu-id="53f1c-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="53f1c-223">설명</span><span class="sxs-lookup"><span data-stu-id="53f1c-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="53f1c-224">가상 디렉터리</span><span class="sxs-lookup"><span data-stu-id="53f1c-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-225">웹 응용 프로그램의 가상 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-225">Virtual directory of the web application.</span></span> <span data-ttu-id="53f1c-226">이 이름은 서버의 실제 디렉터리에 해당 하 고 웹 사이트의 호스트 이름에 추가 됩니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="53f1c-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="53f1c-227">http (s)// &lt; <em> 호스트 이름 </em> &gt; : &lt; <em> 포트 </em> &gt; /SelfService/</span><span class="sxs-lookup"><span data-stu-id="53f1c-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="53f1c-228">가상 디렉터리를 지정 하지 않으면 <strong> SelfService 값 </strong> 이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="53f1c-229">회사 이름</span><span class="sxs-lookup"><span data-stu-id="53f1c-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-230">셀프 서비스 포털의 회사 이름을 지정 합니다 예:</span><span class="sxs-lookup"><span data-stu-id="53f1c-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="53f1c-231">Contoso IT</span><span class="sxs-lookup"><span data-stu-id="53f1c-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="53f1c-232">이 회사 이름은 모든 셀프 서비스 포털 사용자가 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="53f1c-233">헬프 데스크 URL 텍스트</span><span class="sxs-lookup"><span data-stu-id="53f1c-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-234">사용자를 조직의 헬프데스크 웹 사이트로 연결 하는 텍스트 문을 지정 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="53f1c-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="53f1c-235">헬프데스크 또는 IT 부서에 문의</span><span class="sxs-lookup"><span data-stu-id="53f1c-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="53f1c-236">헬프데스크 URL</span><span class="sxs-lookup"><span data-stu-id="53f1c-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-237">조직의 헬프 데스크 웹 사이트 URL을 다음과 같이 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="53f1c-238">http (s)// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="53f1c-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="53f1c-239">주목 텍스트 파일</span><span class="sxs-lookup"><span data-stu-id="53f1c-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-240">셀프 서비스 포털 랜딩 페이지에서 사용자에 게 표시 하려는 알림이 포함 된 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="53f1c-241">사용자에 게 알림 텍스트 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="53f1c-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="53f1c-242">알림 텍스트가 사용자에 게 표시 되지 않도록 지정 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="53f1c-243">항목을 모두 마쳤으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="53f1c-244">마법사는 웹 응용 프로그램에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="53f1c-245">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="53f1c-246">**요약** 페이지에서 추가 되는 기능을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="53f1c-247">참고</span><span class="sxs-lookup"><span data-stu-id="53f1c-247">Note</span></span>**  
   <span data-ttu-id="53f1c-248">입력 한 항목에 대 한 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기** 및 스크립트 저장을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="53f1c-249">**추가** 를 클릭 하 여 웹 응용 프로그램을 서버에 추가 하 고 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="53f1c-250">사용자 지정 알림 텍스트, 회사 이름, 추가 정보에 대 한 포인터 등을 추가 하 여 셀프 서비스 포털을 사용자 지정 하려면 [조직에 대 한 셀프 서비스 포털 사용자 지정](customizing-the-self-service-portal-for-your-organization.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53f1c-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="53f1c-251">클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="53f1c-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="53f1c-252">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1을 실행 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="53f1c-253">그럴 경우 아무 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-253">If so, do nothing.</span></span> <span data-ttu-id="53f1c-254">셀프 서비스 포털 구성이 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="53f1c-255">참고</span><span class="sxs-lookup"><span data-stu-id="53f1c-255">Note</span></span>**  
    <span data-ttu-id="53f1c-256">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1은 설치 프로그램에서 JavaScript 파일을 설치 하므로 셀프 서비스 포털을 구성 하기 위해 Microsoft Ajax 콘텐츠 배달 네트워크에 연결 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="53f1c-257">다음 단계는 SP1 이전 버전의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 사용 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="53f1c-258">클라이언트 컴퓨터에 Microsoft CDN (콘텐츠 배달 네트워크)에 대 한 액세스 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="53f1c-259">CDN은 특정 JavaScript 파일에 필요한 액세스 권한을 셀프 서비스 포털에 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="53f1c-260">클라이언트 컴퓨터가 CDN에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하지 않은 경우에는 최종 사용자가 로그인 한 회사 이름과 계정만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="53f1c-261">오류 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="53f1c-262">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-262">Do one of the following:</span></span>

    -   <span data-ttu-id="53f1c-263">클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 있는 경우 아무 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="53f1c-264">셀프 서비스 포털 구성이 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="53f1c-265">클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 없는 경우 [클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하는 방법](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)에 대 한 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="53f1c-266">관련 항목</span><span class="sxs-lookup"><span data-stu-id="53f1c-266">Related topics</span></span>


[<span data-ttu-id="53f1c-267">서버 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="53f1c-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="53f1c-268">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="53f1c-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="53f1c-269">클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="53f1c-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="53f1c-270">조직에 대한 셀프 서비스 포털 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="53f1c-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="53f1c-271">MBAM 2.5 서버 기능 구성의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="53f1c-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="53f1c-272">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="53f1c-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="53f1c-273">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="53f1c-274">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f1c-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





