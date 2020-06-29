---
title: Configuration Manager에서 MBAM을 배포하는 계획
description: Configuration Manager에서 MBAM을 배포하는 계획
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825628"
---
# <span data-ttu-id="f83c2-103">Configuration Manager에서 MBAM을 배포하는 계획</span><span class="sxs-lookup"><span data-stu-id="f83c2-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="f83c2-104">Configuration Manager 토폴로지로 MBAM을 배포 하려면 20만 클라이언트를 지 원하는 3-서버 아키텍처가 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="f83c2-105">별도의 서버를 사용 하 여 구성 관리자를 실행 하 고 시작 하는 아키텍처 이미지에 표시 된 대로 두 서버에서 기본 관리 및 모니터링 기능을 설치 합니다 ( [구성 관리자와 함께 MBAM 사용)](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="f83c2-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="f83c2-106">중요</span><span class="sxs-lookup"><span data-stu-id="f83c2-106">Important</span></span>**  
<span data-ttu-id="f83c2-107">Windows To Go는 구성 관리자 2007와 함께 MBAM의 통합 토폴로지를 설치 하는 경우 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="f83c2-108">Configuration Manager에서 MBAM을 설치 하기 위한 배포 필수 작업</span><span class="sxs-lookup"><span data-stu-id="f83c2-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="f83c2-109">Configuration Manager를 사용 하 여 MBAM을 설치 하기 전에 다음 전제 조건을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-110">요소일</span><span class="sxs-lookup"><span data-stu-id="f83c2-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="f83c2-111">추가 정보</span><span class="sxs-lookup"><span data-stu-id="f83c2-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-112">Configuration manager 서버가 Configuration Manager 시스템의 기본 사이트 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-113">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f83c2-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-114">Configuration Manager 서버에서 하드웨어 인벤터리 클라이언트 에이전트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-115">Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> 사이트의 하드웨어 인벤토리를 구성 하는 방법을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="f83c2-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="f83c2-116">System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> 구성 관리자에서 하드웨어 인벤토리를 구성 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f83c2-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-117">사용 중인 Configuration Manager 버전에 따라 DCM (구성 관리) 에이전트 또는 준수 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-118">Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> 원하는 구성 관리 클라이언트 에이전트 속성 보기를 사용 하도록 설정 </a> 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="f83c2-119">System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> 구성 관리자에서 준수 설정 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f83c2-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-120">Configuration Manager에서 보고 서비스 시점을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="f83c2-121">SQL Reporting Services에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-122">Configuration Manager 2007의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> SQL Reporting services에 대 한 보고 서비스 지점을 만드는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f83c2-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="f83c2-123">System Center 2012 구성 관리자의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> 구성 관리자의 보고서에 대 한 필수 구성 요소를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f83c2-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="f83c2-124">Configuration Manager에서 지원 되는 버전</span><span class="sxs-lookup"><span data-stu-id="f83c2-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="f83c2-125">MBAM은 다음 버전의 Configuration Manager를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-126">지원 되는 버전</span><span class="sxs-lookup"><span data-stu-id="f83c2-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="f83c2-127">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="f83c2-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="f83c2-128">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="f83c2-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="f83c2-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-130">SP1 이상</span><span class="sxs-lookup"><span data-stu-id="f83c2-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-131">64비트</span><span class="sxs-lookup"><span data-stu-id="f83c2-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f83c2-132">참고</span><span class="sxs-lookup"><span data-stu-id="f83c2-132">Note</span></span></strong><br/><p><span data-ttu-id="f83c2-133">Configuration Manager 2007는 32 비트 이지만 64 비트 MBAM 소프트웨어와 일치 하려면 64 비트 운영 체제에 SQL Server를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-134">Microsoft System Center 2012 구성 관리자</span><span class="sxs-lookup"><span data-stu-id="f83c2-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-135">SP1</span><span class="sxs-lookup"><span data-stu-id="f83c2-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-136">64비트</span><span class="sxs-lookup"><span data-stu-id="f83c2-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f83c2-137">Configuration Manager 서버에서 지원 되는 구성 목록은 사용 중인 구성 관리자 버전에 해당 하는 웹 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f83c2-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="f83c2-138">MBAM에는 Configuration Manager 서버에 대 한 추가 시스템 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="f83c2-139">MBAM 및 SQL Server 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f83c2-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="f83c2-140">MBAM 서버 및 구성 관리자 토폴로지의 SQL Server에 대해 지원 되는 구성 및 시스템 요구 사항은 독립 실행형 토폴로지의 경우와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="f83c2-141">독립 실행형 시스템 요구 사항에 대해서는 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f83c2-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="f83c2-142">MBAM 서버 및 SQL Server 프로세서, RAM 및 구성 관리자 토폴로지의 디스크 공간 요구 사항에 대 한 자세한 내용은 다음 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f83c2-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="f83c2-143">Mbam 서버 프로세서, RAM, 디스크 공간 요구 사항 MBAM</span><span class="sxs-lookup"><span data-stu-id="f83c2-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="f83c2-144">다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 MBAM 서버의 서버 프로세서, RAM, 디스크 공간 요구 사항이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-145">하드웨어 구성 요소</span><span class="sxs-lookup"><span data-stu-id="f83c2-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="f83c2-146">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f83c2-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="f83c2-147">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f83c2-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-148">처리자</span><span class="sxs-lookup"><span data-stu-id="f83c2-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-149">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="f83c2-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-150">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="f83c2-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-151">RAM</span><span class="sxs-lookup"><span data-stu-id="f83c2-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-152">4GB</span><span class="sxs-lookup"><span data-stu-id="f83c2-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-153">8gb</span><span class="sxs-lookup"><span data-stu-id="f83c2-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-154">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="f83c2-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-155">1GB</span><span class="sxs-lookup"><span data-stu-id="f83c2-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-156">2GB</span><span class="sxs-lookup"><span data-stu-id="f83c2-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f83c2-157">SQL Server 프로세서, RAM 및 디스크 공간 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f83c2-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="f83c2-158">다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 SQL Server 컴퓨터에 대 한 서버 프로세서, RAM, 디스크 공간 요구 사항이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-159">하드웨어 구성 요소</span><span class="sxs-lookup"><span data-stu-id="f83c2-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="f83c2-160">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f83c2-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="f83c2-161">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f83c2-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-162">처리자</span><span class="sxs-lookup"><span data-stu-id="f83c2-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-163">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="f83c2-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-164">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="f83c2-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-165">RAM</span><span class="sxs-lookup"><span data-stu-id="f83c2-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-166">4GB</span><span class="sxs-lookup"><span data-stu-id="f83c2-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-167">8gb</span><span class="sxs-lookup"><span data-stu-id="f83c2-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-168">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="f83c2-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-169">5GB</span><span class="sxs-lookup"><span data-stu-id="f83c2-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-170">5gb 이상</span><span class="sxs-lookup"><span data-stu-id="f83c2-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f83c2-171">MBAM 서버를 설치 하는 데 필요한 권한</span><span class="sxs-lookup"><span data-stu-id="f83c2-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="f83c2-172">구성 관리자를 사용 하 여 MBAM을 설치 하려면 다음 표에 나열 된 최소 권한을 사용 하는 보안 역할을 가진 Configuration Manager에 관리자가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="f83c2-173">또한이 표에는 기본 컴퓨터 관리자 권한 이상의 사용자에 게는 MBAM 서버를 설치 하는 데 필요한 권한도 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-174">사용 권한</span><span class="sxs-lookup"><span data-stu-id="f83c2-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="f83c2-175">MBAM 서버 기능</span><span class="sxs-lookup"><span data-stu-id="f83c2-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-176">SQL 인스턴스 로그인 서버 역할:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="f83c2-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="f83c2-177">복구 데이터베이스-감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f83c2-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-178">SQL Server Reporting Services 인스턴스 권한:-폴더 만들기-보고서 게시</span><span class="sxs-lookup"><span data-stu-id="f83c2-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="f83c2-179">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f83c2-180">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f83c2-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-181">사용 권한</span><span class="sxs-lookup"><span data-stu-id="f83c2-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="f83c2-182">Configuration Manager 서버 기능</span><span class="sxs-lookup"><span data-stu-id="f83c2-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-183">Configuration Manager 사이트 권한:-읽기</span><span class="sxs-lookup"><span data-stu-id="f83c2-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-184">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-185">Configuration Manager 컬렉션 권한:-만들기-삭제-읽기-수정-배포 구성 항목</span><span class="sxs-lookup"><span data-stu-id="f83c2-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-186">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-187">Configuration Manager 구성 항목 권한:-만들기-삭제-읽기</span><span class="sxs-lookup"><span data-stu-id="f83c2-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-188">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f83c2-189">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="f83c2-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f83c2-190">사용 권한</span><span class="sxs-lookup"><span data-stu-id="f83c2-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="f83c2-191">Configuration Manager 서버 기능</span><span class="sxs-lookup"><span data-stu-id="f83c2-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-192">Configuration Manager 사이트 권한:-읽기</span><span class="sxs-lookup"><span data-stu-id="f83c2-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-193">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f83c2-194">Configuration Manager 컬렉션 권한:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="f83c2-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-195">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f83c2-196">Configuration Manager 구성 항목 권한:-만들기-삭제-읽기-배포</span><span class="sxs-lookup"><span data-stu-id="f83c2-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-197">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="f83c2-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f83c2-198">구성 관리자 토폴로지에 대 한 MBAM 기능 배포 순서</span><span class="sxs-lookup"><span data-stu-id="f83c2-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="f83c2-199">Configuration Manager 서버에 MBAM을 배포 하는 경우 다음 순서에 따라 배포 작업을 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="f83c2-200">Configuration Manager 서버에서 구성 .mof 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="f83c2-201">Sms \ _def .mof 파일 구성 관리자 서버를 만들거나 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="f83c2-202">Configuration Manager 서버에 MBAM을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="f83c2-203">데이터베이스 서버에 복구 데이터베이스와 감사 데이터베이스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="f83c2-204">관리 및 모니터링 서버에 MBAM 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="f83c2-205">Configuration Manager를 사용 하 여 MBAM을 설치 하기 위한 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="f83c2-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="f83c2-206">이 검사 목록에서는 Microsoft BitLocker 관리 및 Configuration Manager를 사용 하 여 배포 모니터링을 계획할 때 고려해 야 할 항목의 권장 단계 및 상위 수준 목록을 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="f83c2-207">이 검사 목록을 스프레드시트 프로그램에 복사 하 여 사용을 위해 사용자 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="f83c2-208">작업</span><span class="sxs-lookup"><span data-stu-id="f83c2-208">Task</span></span></th>
<th align="left"><span data-ttu-id="f83c2-209">참조</span><span class="sxs-lookup"><span data-stu-id="f83c2-209">References</span></span></th>
<th align="left"><span data-ttu-id="f83c2-210">참고</span><span class="sxs-lookup"><span data-stu-id="f83c2-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f83c2-211">Configuration Manager가 MBAM을 사용 하 여 작동 하는 방법과 권장 되는 상위 수준 아키텍처를 보여 주는 시작 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="f83c2-212">시작 - Configuration Manager를 통해 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="f83c2-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f83c2-213">배포 필수 구성 요소, 지원 되는 구성, 필요한 사용 권한, 각 기능에 대 한 배포 순서를 설명 하는 계획 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f83c2-214">Configuration Manager에서 MBAM을 배포하는 계획</span><span class="sxs-lookup"><span data-stu-id="f83c2-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f83c2-215">MBAM 그룹 정책 요구 사항 계획 및 구성</span><span class="sxs-lookup"><span data-stu-id="f83c2-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="f83c2-216">MBAM 2.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="f83c2-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f83c2-217">필요한 Active Directory 도메인 서비스 보안 그룹을 계획 하 고 만들고 MBAM 로컬 보안 그룹 구성원 요구 사항에 대 한 계획을 수립 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="f83c2-218">MBAM 2.0 관리자 역할 계획</span><span class="sxs-lookup"><span data-stu-id="f83c2-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f83c2-219">MBAM 클라이언트 배포 배포 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="f83c2-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="f83c2-220">MBAM 2.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="f83c2-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f83c2-221">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f83c2-221">Related topics</span></span>


[<span data-ttu-id="f83c2-222">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="f83c2-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









