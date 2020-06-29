---
title: MBAM 2.0 지원되는 구성
description: MBAM 2.0 지원되는 구성
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823908"
---
# <span data-ttu-id="be024-103">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="be024-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="be024-104">이 항목에서는 독립 실행형 토폴로지를 사용 하 여 사용자 환경에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0을 설치 하 고 실행 하기 위한 요구 사항을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be024-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="be024-105">이후 릴리스에 적용 되는 지원 되는 구성에 대해서는 해당 릴리스에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be024-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="be024-106">구성 관리자 토폴로지를 사용 하 여 MBAM 2.0을 설치 하 고 시스템 요구 사항 목록을 검토 하려면 [구성 관리자를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be024-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="be024-107">프로덕션 환경에서 MBAM을 실행 하는 데 권장 되는 구성은 확장성 요구 사항에 따라 두 개의 서버를 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="be024-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="be024-108">이 구성은 최대 20만 MBAM 클라이언트를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be024-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="be024-109">독립 실행형 MBAM 서버 인프라에 대 한 이미지 및 설명은 [mbam 2.0의 상위 수준 아키텍처](high-level-architecture-for-mbam-20-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be024-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="be024-110">**참고**  Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be024-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="be024-111">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be024-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="be024-112">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be024-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="be024-113">MBAM 서버 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="be024-114">서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-114">Server Operating System Requirements</span></span>

<span data-ttu-id="be024-115">다음 표에는 Microsoft BitLocker 관리 및 모니터링 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be024-116">운영 체제</span><span class="sxs-lookup"><span data-stu-id="be024-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="be024-117">버전</span><span class="sxs-lookup"><span data-stu-id="be024-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="be024-118">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="be024-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="be024-119">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="be024-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="be024-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-121">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="be024-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-122">SP1</span><span class="sxs-lookup"><span data-stu-id="be024-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-123">64비트</span><span class="sxs-lookup"><span data-stu-id="be024-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="be024-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-125">스탠더드 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="be024-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="be024-126">64비트</span><span class="sxs-lookup"><span data-stu-id="be024-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="be024-127">**참고**  도메인 컨트롤러 컴퓨터에는 MBAM 서비스, 보고서 또는 데이터베이스를 설치 하는 기능이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="be024-128">서버 프로세서, RAM 및 디스크 공간 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be024-129">하드웨어 구성 요소</span><span class="sxs-lookup"><span data-stu-id="be024-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="be024-130">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="be024-131">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-132">처리자</span><span class="sxs-lookup"><span data-stu-id="be024-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-133">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="be024-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-134">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="be024-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-135">RAM</span><span class="sxs-lookup"><span data-stu-id="be024-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-136">8gb</span><span class="sxs-lookup"><span data-stu-id="be024-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-137">12gb</span><span class="sxs-lookup"><span data-stu-id="be024-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-138">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="be024-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-139">1GB</span><span class="sxs-lookup"><span data-stu-id="be024-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-140">2GB</span><span class="sxs-lookup"><span data-stu-id="be024-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="be024-141">SQLServer 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="be024-142">다음 표에는 복구 데이터베이스, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 포함 된 관리 및 모니터링 서버 기능 설치에 대해 지원 되는 SQLServer 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="be024-143">데이터베이스에는 추가적으로 SQL Server 관리 도구를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be024-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="be024-144">**참고**  MBAM은 기본적으로 SQL 클러스터링, 미러링 또는 가용성 그룹을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="be024-145">데이터베이스를 설치 하려면 독립 실행형 SQL server에서 MBAM 서버 설치를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be024-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be024-146">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="be024-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="be024-147">버전</span><span class="sxs-lookup"><span data-stu-id="be024-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="be024-148">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="be024-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="be024-149">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="be024-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="be024-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-151">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="be024-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-152">SP1</span><span class="sxs-lookup"><span data-stu-id="be024-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-153">64비트</span><span class="sxs-lookup"><span data-stu-id="be024-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="be024-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-155">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="be024-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-156">SP1</span><span class="sxs-lookup"><span data-stu-id="be024-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-157">64비트</span><span class="sxs-lookup"><span data-stu-id="be024-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be024-158">하드웨어 구성 요소</span><span class="sxs-lookup"><span data-stu-id="be024-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="be024-159">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="be024-160">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-161">처리자</span><span class="sxs-lookup"><span data-stu-id="be024-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-162">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="be024-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-163">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="be024-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-164">RAM</span><span class="sxs-lookup"><span data-stu-id="be024-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-165">8gb</span><span class="sxs-lookup"><span data-stu-id="be024-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-166">12gb</span><span class="sxs-lookup"><span data-stu-id="be024-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-167">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="be024-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-168">5GB</span><span class="sxs-lookup"><span data-stu-id="be024-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-169">5gb 이상</span><span class="sxs-lookup"><span data-stu-id="be024-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="be024-170">MBAM 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="be024-171">클라이언트 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-171">Client Operating System Requirements</span></span>

<span data-ttu-id="be024-172">다음 표에는 Microsoft BitLocker 관리 및 모니터링 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be024-173">운영 체제</span><span class="sxs-lookup"><span data-stu-id="be024-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="be024-174">버전</span><span class="sxs-lookup"><span data-stu-id="be024-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="be024-175">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="be024-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="be024-176">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="be024-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-177">Windows7</span><span class="sxs-lookup"><span data-stu-id="be024-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-178">Enterprise 또는 Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="be024-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-179">SP1</span><span class="sxs-lookup"><span data-stu-id="be024-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-180">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="be024-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-181">Windows8</span><span class="sxs-lookup"><span data-stu-id="be024-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-182">Enterprise 버전</span><span class="sxs-lookup"><span data-stu-id="be024-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be024-183">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="be024-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-184">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="be024-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-185">Windows 8 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="be024-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be024-186">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="be024-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="be024-187">클라이언트 RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-187">Client RAM Requirements</span></span>

<span data-ttu-id="be024-188">Microsoft BitLocker 관리 및 모니터링 클라이언트 설치와 관련 된 RAM 요구 사항은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="be024-189">MBAM 그룹 정책 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="be024-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="be024-190">다음 표에는 Microsoft BitLocker 관리 및 그룹 정책 템플릿 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be024-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be024-191">운영 체제</span><span class="sxs-lookup"><span data-stu-id="be024-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="be024-192">버전</span><span class="sxs-lookup"><span data-stu-id="be024-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="be024-193">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="be024-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="be024-194">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="be024-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-195">Windows7</span><span class="sxs-lookup"><span data-stu-id="be024-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-196">Enterprise 또는 Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="be024-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-197">SP1</span><span class="sxs-lookup"><span data-stu-id="be024-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-198">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="be024-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-199">Windows8</span><span class="sxs-lookup"><span data-stu-id="be024-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-200">Enterprise 버전</span><span class="sxs-lookup"><span data-stu-id="be024-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be024-201">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="be024-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be024-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be024-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-203">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="be024-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-204">SP1</span><span class="sxs-lookup"><span data-stu-id="be024-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-205">64비트</span><span class="sxs-lookup"><span data-stu-id="be024-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be024-206">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be024-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="be024-207">스탠더드 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="be024-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be024-208">64비트</span><span class="sxs-lookup"><span data-stu-id="be024-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="be024-209">관련 항목</span><span class="sxs-lookup"><span data-stu-id="be024-209">Related topics</span></span>


[<span data-ttu-id="be024-210">MBAM 2.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="be024-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="be024-211">MBAM 2.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="be024-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





