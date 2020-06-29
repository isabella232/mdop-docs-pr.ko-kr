---
title: MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법
description: MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812444"
---
# <span data-ttu-id="4e242-103">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="4e242-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="4e242-104">이 항목에서는 구성 관리자와 MBAM을 통합 하는 System Center Configuration Manager 통합 토폴로지를 사용 하도록 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="4e242-105">이 지침에서는 다음을 사용 하 여 Configuration Manager 통합을 구성 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="4e242-106">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="4e242-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="4e242-107">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="4e242-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="4e242-108">이 지침은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에서 권장 되는 아키텍처를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="4e242-109">구성을 시작 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e242-110">단계</span><span class="sxs-lookup"><span data-stu-id="4e242-110">Step</span></span></th>
<th align="left"><span data-ttu-id="4e242-111">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="4e242-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e242-112">MBAM에 권장 되는 아키텍처를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="4e242-113">Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="4e242-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e242-114">MBAM에 대해 지원 되는 구성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="4e242-115">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="4e242-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e242-116">각 서버에서 필수 구성 요소를 완성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="4e242-117">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="4e242-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="4e242-118">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="4e242-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e242-119">MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4e242-120">참고</span><span class="sxs-lookup"><span data-stu-id="4e242-120">Note</span></span></strong><br/><p><span data-ttu-id="4e242-121">이 토폴로지의 경우, MBAM 서버 소프트웨어를 설치 하는 컴퓨터에 Configuration Manager 콘솔을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="4e242-122">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="4e242-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e242-123">Windows powershell 필수 구성 요소 검토 (Windows PowerShell cmdlet을 사용 하 여 MBAM 구성에만 해당 하는 경우에만 적용)</span><span class="sxs-lookup"><span data-stu-id="4e242-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="4e242-124">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="4e242-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="4e242-125">Windows PowerShell을 사용 하 여 Configuration Manager 통합을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="4e242-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="4e242-126">구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4e242-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="4e242-127">**사용-MbamCMIntegration** Windows PowerShell cmdlet을 사용 하 여 보고서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="4e242-128">이 cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamCMIntegration**을 입력 하세요.</span><span class="sxs-lookup"><span data-stu-id="4e242-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="4e242-129">마법사를 사용 하 여 System Center Configuration Manager 통합을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="4e242-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="4e242-130">System Center Configuration Manager 통합 기능을 구성할 서버에서 MBAM 서버 구성 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="4e242-131">**시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="4e242-132">**새 기능 추가**를 클릭 하 고 **System Center Configuration Manager 통합**을 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="4e242-133">마법사에서 구성 관리자 통합에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="4e242-134">필수 구성 요소 확인에 성공 하면 **다음** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="4e242-135">그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="4e242-136">마법사에서 필드 값을 입력 하려면 다음 설명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4e242-137">필드</span><span class="sxs-lookup"><span data-stu-id="4e242-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="4e242-138">설명</span><span class="sxs-lookup"><span data-stu-id="4e242-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="4e242-139">SQL Server Reporting Services 서버</span><span class="sxs-lookup"><span data-stu-id="4e242-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="4e242-140">보고 서비스 지점의 역할을 가진 서버의 FQDN (정규화 된 도메인 이름)</span><span class="sxs-lookup"><span data-stu-id="4e242-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="4e242-141">MBAM Configuration Manager 보고서가 배포 되는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="4e242-142">서버를 지정 하지 않으면 구성 관리자 보고서가 로컬 서버에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="4e242-143">SQL Server Reporting Services 인스턴스</span><span class="sxs-lookup"><span data-stu-id="4e242-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="4e242-144">Configuration Manager 보고서가 배포 되는 SSRS (SQL Server Reporting Services) 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="4e242-145">인스턴스를 지정 하지 않으면 Configuration Manager 보고서가 기본 SSRS 인스턴스 이름에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="4e242-146">서버에 System Center 2012 Configuration Manager가 설치 되어 있으면 입력 하는 값이 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="4e242-147">**요약** 페이지에서 추가 되는 기능을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="4e242-148">참고</span><span class="sxs-lookup"><span data-stu-id="4e242-148">Note</span></span>**  
    <span data-ttu-id="4e242-149">방금 만든 항목의 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기** 및 스크립트 저장을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="4e242-150">**추가** 를 클릭 하 여 서버에 Configuration Manager 통합 기능을 추가한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="4e242-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4e242-151">Related topics</span></span>


[<span data-ttu-id="4e242-152">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="4e242-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="4e242-153">MBAM 2.5 서버 기능 구성의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="4e242-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="4e242-154">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="4e242-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4e242-155">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4e242-156">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e242-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






