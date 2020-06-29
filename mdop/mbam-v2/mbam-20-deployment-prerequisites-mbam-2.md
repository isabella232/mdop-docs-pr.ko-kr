---
title: MBAM 2.0 배포 필수 구성 요소
description: MBAM 2.0 배포 필수 구성 요소
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826013"
---
# <span data-ttu-id="e3a12-103">MBAM 2.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e3a12-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="e3a12-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하기 위한 전제 조건을 충족 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="e3a12-105">이 섹션에서는 Microsoft BitLocker 관리 및 모니터링 서버 기능 및 클라이언트를 배포 하기 전에 컴퓨팅 환경을 성공적으로 계획 하는 데 도움이 되는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="e3a12-106">구성 관리자를 사용 하 여 MBAM을 설치 하는 경우 추가 필수 구성 요소에 대해 [구성 관리자를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="e3a12-107">MBAM 서버 기능에 대 한 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="e3a12-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="e3a12-108">각 MBAM 서버 기능에는 MBAM 기능을 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="e3a12-109">MBAM 설치 프로그램이 설치를 시작 하기 전에 모든 필수 구성 요소를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="e3a12-110">관리 및 모니터링 서버용 필수 조건</span><span class="sxs-lookup"><span data-stu-id="e3a12-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3a12-111">요소일</span><span class="sxs-lookup"><span data-stu-id="e3a12-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e3a12-112">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e3a12-113">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="e3a12-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e3a12-114">이 역할은 관리 및 모니터링 서버 기능에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e3a12-115">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="e3a12-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e3a12-116"><strong>IIS 관리 스크립트 및 도구를 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e3a12-117">SSL 인증서</span><span class="sxs-lookup"><span data-stu-id="e3a12-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e3a12-118">선택 사항.</span><span class="sxs-lookup"><span data-stu-id="e3a12-118">Optional.</span></span> <span data-ttu-id="e3a12-119">클라이언트와 웹 서비스 간의 통신을 보호 하려면 신뢰할 수 있는 보안 기관에서 서명한 인증서를 얻고 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e3a12-120">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="e3a12-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="e3a12-121">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="e3a12-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e3a12-122">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="e3a12-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="e3a12-123">기본 문서</span><span class="sxs-lookup"><span data-stu-id="e3a12-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e3a12-124">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="e3a12-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e3a12-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="e3a12-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="e3a12-126">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="e3a12-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="e3a12-127">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="e3a12-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="e3a12-128">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="e3a12-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e3a12-129">보안이</span><span class="sxs-lookup"><span data-stu-id="e3a12-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e3a12-130">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="e3a12-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="e3a12-131">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="e3a12-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e3a12-132">Windows Server 기능</span><span class="sxs-lookup"><span data-stu-id="e3a12-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="e3a12-133">.NET Framework 3.5.1 기능:</span><span class="sxs-lookup"><span data-stu-id="e3a12-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e3a12-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="e3a12-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="e3a12-135">WCF 활성화</span><span class="sxs-lookup"><span data-stu-id="e3a12-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-136">HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="e3a12-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="e3a12-137">비 HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="e3a12-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="e3a12-138">Windows Process Activation Service:</span><span class="sxs-lookup"><span data-stu-id="e3a12-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e3a12-139">프로세스 모델</span><span class="sxs-lookup"><span data-stu-id="e3a12-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="e3a12-140">.NET 환경</span><span class="sxs-lookup"><span data-stu-id="e3a12-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="e3a12-141">구성 Api</span><span class="sxs-lookup"><span data-stu-id="e3a12-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="e3a12-142">참고</span><span class="sxs-lookup"><span data-stu-id="e3a12-142">Note</span></span>**  
<span data-ttu-id="e3a12-143">지원 되는 운영 체제 목록은 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="e3a12-144">규정 준수 및 감사 보고서의 필수 조건</span><span class="sxs-lookup"><span data-stu-id="e3a12-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3a12-145">요소일</span><span class="sxs-lookup"><span data-stu-id="e3a12-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e3a12-146">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-147">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="e3a12-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="e3a12-148"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-149">다음을 사용 하 여 SQL Server 설치:</span><span class="sxs-lookup"><span data-stu-id="e3a12-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-150">SQL_Latin1_General_CP1_CI_AS 데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="e3a12-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3a12-151">SSRS (SQL Server Reporting Services)</span><span class="sxs-lookup"><span data-stu-id="e3a12-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-152">SSRS 인스턴스 권한 – 보고서와 다른 별도의 서버에 데이터베이스를 설치 하는 경우에만 보고서를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-153">필요한 인스턴스 권한:</span><span class="sxs-lookup"><span data-stu-id="e3a12-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-154">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="e3a12-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="e3a12-155">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="e3a12-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="e3a12-156">MBAM 서버 설치 중에 SSRS를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="e3a12-157">"기본" 모드에서 SSRS를 구성 하 고, 설정 되지 않음 또는 "SharePoint" 모드를 설정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e3a12-158">복구 데이터베이스에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="e3a12-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3a12-159">요소일</span><span class="sxs-lookup"><span data-stu-id="e3a12-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e3a12-160">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-161">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="e3a12-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="e3a12-162"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-163">다음을 사용 하 여 SQL Server 설치:</span><span class="sxs-lookup"><span data-stu-id="e3a12-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-164">SQL_Latin1_General_CP1_CI_AS 데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="e3a12-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="e3a12-165">SQL Server 관리 도구</span><span class="sxs-lookup"><span data-stu-id="e3a12-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3a12-166">필요한 SQL Server 권한</span><span class="sxs-lookup"><span data-stu-id="e3a12-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-167">필요한 권한:</span><span class="sxs-lookup"><span data-stu-id="e3a12-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-168">SQL 인스턴스 로그인 서버 역할:</span><span class="sxs-lookup"><span data-stu-id="e3a12-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-169">dbcreator</span><span class="sxs-lookup"><span data-stu-id="e3a12-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="e3a12-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="e3a12-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="e3a12-171">SQL Server Reporting Services 인스턴스 권한:</span><span class="sxs-lookup"><span data-stu-id="e3a12-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-172">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="e3a12-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="e3a12-173">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="e3a12-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-174">선택 사항-SQL Server에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능 설치</span><span class="sxs-lookup"><span data-stu-id="e3a12-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-175">TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에서 설정 된 여러 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e3a12-176">참고</span><span class="sxs-lookup"><span data-stu-id="e3a12-176">Note</span></span></strong><br/><p><span data-ttu-id="e3a12-177">TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 하는데, 이것은 사용자가 로그온 한 계정에 SQL Server 테이블에서 복구 키 정보를 보는 동안 데이터베이스에 대 한 사용 권한이 있는 경우 복구 키 정보가 표시 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="e3a12-178">TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> mbam 2.0 보안 고려 사항에 대해 자세히 알아보세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="e3a12-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e3a12-179">준수 및 감사 데이터베이스에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="e3a12-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3a12-180">요소일</span><span class="sxs-lookup"><span data-stu-id="e3a12-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e3a12-181">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-182">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="e3a12-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="e3a12-183"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-184">다음을 사용 하 여 SQL Server 설치:</span><span class="sxs-lookup"><span data-stu-id="e3a12-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-185">SQL_Latin1_General_CP1_CI_AS 데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="e3a12-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="e3a12-186">SQL Server 관리 도구</span><span class="sxs-lookup"><span data-stu-id="e3a12-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3a12-187">필요한 SQL Server 권한</span><span class="sxs-lookup"><span data-stu-id="e3a12-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-188">필요한 권한:</span><span class="sxs-lookup"><span data-stu-id="e3a12-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-189">SQL 인스턴스 로그인 서버 역할:</span><span class="sxs-lookup"><span data-stu-id="e3a12-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-190">dbcreator</span><span class="sxs-lookup"><span data-stu-id="e3a12-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="e3a12-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="e3a12-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="e3a12-192">SQL Server Reporting Services 인스턴스 권한:</span><span class="sxs-lookup"><span data-stu-id="e3a12-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-193">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="e3a12-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="e3a12-194">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="e3a12-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-195">선택 사항-SQL Server의 TDE (투명 데이터 암호화) 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-196">TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에서 설정 된 여러 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e3a12-197">참고</span><span class="sxs-lookup"><span data-stu-id="e3a12-197">Note</span></span></strong><br/><p><span data-ttu-id="e3a12-198">TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 하는데, 이것은 사용자가 로그온 한 계정에 SQL Server 테이블에서 복구 키 정보를 보는 동안 데이터베이스에 대 한 사용 권한이 있는 경우 복구 키 정보가 표시 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="e3a12-199">TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> mbam 2.0 보안 고려 사항에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3a12-200">SQL Server는 MBAM 서버 설치 중에 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-201">SQL Server 에이전트 서비스가 실행 중이 고 선택한 SQL Server 인스턴스에서 자동 시작으로 설정 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e3a12-202">셀프 서비스 포털의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e3a12-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3a12-203">요소일</span><span class="sxs-lookup"><span data-stu-id="e3a12-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e3a12-204">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-205">지원 되는 Windows Server 버전</span><span class="sxs-lookup"><span data-stu-id="e3a12-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="e3a12-206"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> </a> 지원 되는 버전에 대해 mbam 2.0 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3a12-207">ASP.NET MVC 2.0</span><span class="sxs-lookup"><span data-stu-id="e3a12-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="e3a12-208">ASP.NET MVC 2 다운로드</span><span class="sxs-lookup"><span data-stu-id="e3a12-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e3a12-209">웹 서비스 IIS 관리 도구</span><span class="sxs-lookup"><span data-stu-id="e3a12-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e3a12-210">MBAM 클라이언트의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e3a12-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e3a12-211">요소일</span><span class="sxs-lookup"><span data-stu-id="e3a12-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e3a12-212">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e3a12-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e3a12-213">Windows 7 클라이언트 </strong> - 에는 TPM (신뢰할 수 있는 플랫폼 모듈) 기능이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-214">TPM 버전은 1.2 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e3a12-215">TPM 칩이 BIOS에서 켜져 있고 운영 체제에서 재설정 가능 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e3a12-216">자세한 내용은 BIOS 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3a12-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e3a12-217">Windows 8 클라이언트만 </strong> : mbam이 tpm 복구 키를 저장 하 고 관리 하도록 하려면 tpm 자동 프로비저닝이 꺼져 있어야 하 고 mbam을 배포 하기 전에 tpm 소유자로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="e3a12-218">TPM 자동 프로비저닝을 끄려면-TpmAutoProvisioning을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="e3a12-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="e3a12-219">TPM 자동 프로비저닝이 해제 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="e3a12-220">Mbam을 배포 하기 전에 \ AM을 TPM 소유자로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="e3a12-221">TPM 자동 프로비저닝을 끄려면-TpmAutoProvisioning을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="e3a12-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e3a12-222">참고</span><span class="sxs-lookup"><span data-stu-id="e3a12-222">Note</span></span></strong><br/><p><span data-ttu-id="e3a12-223">키보드, 비디오 또는 마우스가 키보드, 비디오 또는 마우스 (KVM) 스위치를 통해 직접 연결 되어 관리 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="e3a12-224">KVM 스위치는 컴퓨터의 실제 현재 상태를 감지 하는 기능을 방해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a12-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e3a12-225">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e3a12-225">Related topics</span></span>


[<span data-ttu-id="e3a12-226">MBAM 2.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="e3a12-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="e3a12-227">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="e3a12-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









