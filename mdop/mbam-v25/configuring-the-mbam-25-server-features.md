---
title: MBAM 2.5 서버 기능 구성
description: MBAM 2.5 서버 기능 구성
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823058"
---
# <span data-ttu-id="63cde-103">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="63cde-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="63cde-104">이 정보를 사용 하 여 [mbam 2.5 서버 소프트웨어를 설치한](installing-the-mbam-25-server-software.md)후 Microsoft BitLocker 관리 및 모니터링 (mbam) 2.5 서버 기능을 구성할 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="63cde-105">MBAM을 구성 하는 데 사용할 수 있는 방법에는 다음 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="63cde-106">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="63cde-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="63cde-107">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="63cde-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="63cde-108">MBAM 서버 기능 구성을 시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="63cde-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="63cde-109">MBAM 서버 기능 구성을 시작 하기 전에 다음 단계를 검토 하 고 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63cde-110">단계</span><span class="sxs-lookup"><span data-stu-id="63cde-110">Step</span></span></th>
<th align="left"><span data-ttu-id="63cde-111">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="63cde-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63cde-112">MBAM에 권장 되는 아키텍처를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="63cde-113">MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="63cde-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63cde-114">MBAM에 대해 지원 되는 구성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="63cde-115">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="63cde-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63cde-116">각 서버에서 필수 구성 요소를 완성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="63cde-117">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="63cde-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="63cde-118">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="63cde-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63cde-119">MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="63cde-120">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="63cde-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63cde-121">이 메서드를 사용 하 여 MBAM 서버 기능을 구성 하는 경우 Windows PowerShell을 사용 하 여 필수 구성 요소를 검토 하 여 MBAM 서버 기능을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="63cde-122">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="63cde-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="63cde-123">MBAM 서버 기능을 구성 하는 단계</span><span class="sxs-lookup"><span data-stu-id="63cde-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="63cde-124">다음 표의 각 행은 [MBAM 2.5에 권장 되는 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에 따라 별도의 서버에서 구성할 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63cde-125">설치할 기능</span><span class="sxs-lookup"><span data-stu-id="63cde-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="63cde-126">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="63cde-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63cde-127">데이터베이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="63cde-128">MBAM 2.5 데이터베이스를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="63cde-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63cde-129">보고서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="63cde-130">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="63cde-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63cde-131">웹 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="63cde-132">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="63cde-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63cde-133">System Center Configuration Manager 통합을 구성 합니다 (해당 하는 경우).</span><span class="sxs-lookup"><span data-stu-id="63cde-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="63cde-134">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="63cde-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="63cde-135">MBAM 서버 기능 구성에 대 한 이벤트 목록은 [서버 이벤트 로그](server-event-logs.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63cde-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="63cde-136">관련 항목</span><span class="sxs-lookup"><span data-stu-id="63cde-136">Related topics</span></span>


<span data-ttu-id="63cde-137">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="63cde-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="63cde-138">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="63cde-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="63cde-139">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="63cde-140">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63cde-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




