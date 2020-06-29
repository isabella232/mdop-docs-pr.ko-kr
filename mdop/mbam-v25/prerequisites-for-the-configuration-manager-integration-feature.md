---
title: Configuration Manager 통합 기능의 필수 구성 요소
description: Configuration Manager 통합 기능의 필수 구성 요소
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825013"
---
# <span data-ttu-id="3d2c5-103">Configuration Manager 통합 기능의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="3d2c5-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="3d2c5-104">System Center Configuration Manager 통합 토폴로지에 MBAM을 배포 하는 경우 [구성 관리자 통합 토폴로지와 함께 mbam 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)에서 설명한 대로 3 서버 아키텍처를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="3d2c5-105">이 아키텍처는 50만 클라이언트 컴퓨터를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="3d2c5-106">중요</span><span class="sxs-lookup"><span data-stu-id="3d2c5-106">Important</span></span>**  
<span data-ttu-id="3d2c5-107">Windows To Go는 Configuration Manager 2007를 사용 중인 경우 Configuration Manager 통합 토폴로지 설치에 대해 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="3d2c5-108">Configuration Manager 통합 기능에 대 한 일반적인 전제 조건</span><span class="sxs-lookup"><span data-stu-id="3d2c5-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="3d2c5-109">구성 관리자를 사용 하 여 MBAM을 설치 하는 경우 독립 실행형 토폴로지의 필수 구성 요소 외에 다음과 같은 추가 필수 구성 요소가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d2c5-110">요소일</span><span class="sxs-lookup"><span data-stu-id="3d2c5-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="3d2c5-111">추가 정보</span><span class="sxs-lookup"><span data-stu-id="3d2c5-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-112">Configuration manager 서버는 Configuration Manager 시스템의 기본 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-113">해당 없음</span><span class="sxs-lookup"><span data-stu-id="3d2c5-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d2c5-114">하드웨어 인벤터리 클라이언트 에이전트는 Configuration Manager 서버에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-115">System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> 구성 관리자에서 하드웨어 인벤토리를 구성 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3d2c5-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="3d2c5-116">Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> 사이트의 하드웨어 인벤토리를 구성 하는 방법을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-117">사용 중인 Configuration Manager 버전에 따라 다음 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="3d2c5-118">준수 설정-(System Center 2012 구성 관리자)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="3d2c5-119">DCM (바람직한 구성 관리) 클라이언트 에이전트 – (구성 관리자 2007)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3d2c5-120">System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> 구성 관리자에서 준수 설정 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3d2c5-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="3d2c5-121">구성 관리자 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> 원하는 구성 관리 클라이언트 에이전트 속성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3d2c5-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d2c5-122">보고 서비스 지점은 구성 관리자에서 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="3d2c5-123">SQL Server Reporting Services (SSRS)에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-124">System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> 구성 관리자의 보고서에 대 한 필수 구성 요소를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3d2c5-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="3d2c5-125">Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> SQL Reporting services에 대 한 보고 서비스 지점을 만드는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3d2c5-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-126">Configuration Manager 2007에는 Microsoft .NET Framework 2.0이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-127">Configuration Manager 2007에서 필요한 DCM (구성 관리) 클라이언트 에이전트는 준수를 보고 하기 위해 .NET Framework 2.0를 필요로 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3d2c5-128">참고</span><span class="sxs-lookup"><span data-stu-id="3d2c5-128">Note</span></span></strong><br/><p><span data-ttu-id="3d2c5-129">.NET Framework 3.5을 설치 하면 .NET Framework 2.0가 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3d2c5-130">Configuration Manager에서 MBAM을 설치 하는 데 필요한 권한</span><span class="sxs-lookup"><span data-stu-id="3d2c5-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="3d2c5-131">구성 관리자를 사용 하 여 MBAM을 설치 하려면 다음 표에 나열 된 최소 권한을 사용 하는 보안 역할을 가진 Configuration Manager에 관리자가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="3d2c5-132">또한이 표에는 기본 컴퓨터 관리자 권한 이상의 사용자에 게는 MBAM 서버를 설치 하는 데 필요한 권한도 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="3d2c5-133">다음 표의 사용 권한은 두 버전의 Configuration Manager에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d2c5-134">사용 권한</span><span class="sxs-lookup"><span data-stu-id="3d2c5-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="3d2c5-135">MBAM 서버 기능</span><span class="sxs-lookup"><span data-stu-id="3d2c5-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-136">SQL Server 인스턴스 로그인 서버 역할:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="3d2c5-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="3d2c5-137">복구 데이터베이스-감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="3d2c5-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d2c5-138">SSRS 인스턴스 권한:-폴더 만들기-보고서 게시</span><span class="sxs-lookup"><span data-stu-id="3d2c5-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="3d2c5-139">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3d2c5-140">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3d2c5-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d2c5-141">사용 권한</span><span class="sxs-lookup"><span data-stu-id="3d2c5-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="3d2c5-142">Configuration Manager 서버 기능</span><span class="sxs-lookup"><span data-stu-id="3d2c5-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-143">Configuration Manager 사이트 권한:-읽기</span><span class="sxs-lookup"><span data-stu-id="3d2c5-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-144">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d2c5-145">Configuration Manager 컬렉션 권한:-만들기-삭제-읽기-수정-배포 구성 항목</span><span class="sxs-lookup"><span data-stu-id="3d2c5-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-146">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-147">Configuration Manager 구성 항목 권한:-만들기-삭제-읽기</span><span class="sxs-lookup"><span data-stu-id="3d2c5-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-148">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3d2c5-149">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="3d2c5-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d2c5-150">사용 권한</span><span class="sxs-lookup"><span data-stu-id="3d2c5-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="3d2c5-151">Configuration Manager 서버 기능</span><span class="sxs-lookup"><span data-stu-id="3d2c5-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-152">Configuration Manager 사이트 권한:-읽기</span><span class="sxs-lookup"><span data-stu-id="3d2c5-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-153">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d2c5-154">Configuration Manager 컬렉션 권한:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="3d2c5-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-155">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d2c5-156">Configuration Manager 구성 항목 권한:-만들기-삭제-읽기-배포</span><span class="sxs-lookup"><span data-stu-id="3d2c5-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d2c5-157">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="3d2c5-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3d2c5-158">.Mof 파일에 대 한 필수 변경 사항</span><span class="sxs-lookup"><span data-stu-id="3d2c5-158">Required changes for the .mof files</span></span>


<span data-ttu-id="3d2c5-159">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면 System Center 2012 Configuration Manager 및 Microsoft System Center Configuration Manager 2007에 대 한 구성. mof 파일과 Sms \ _def .mof 파일을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="3d2c5-160">지침은 [Configuration Manager 통합 토폴로지에만 적용 되는 Mbam 2.5 서버 필수 구성 요소](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="3d2c5-161">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3d2c5-161">Related topics</span></span>


[<span data-ttu-id="3d2c5-162">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="3d2c5-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="3d2c5-163">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="3d2c5-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="3d2c5-164">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="3d2c5-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3d2c5-165">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3d2c5-166">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





