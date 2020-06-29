---
title: MBAM 1.0 배포 필수 구성 요소
description: MBAM 1.0 배포 필수 구성 요소
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822663"
---
# <span data-ttu-id="48304-103">MBAM 1.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="48304-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="48304-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하는 데 필요한 필수 구성 요소를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="48304-105">이 섹션에서는 MBAM 클라이언트 및 서버 기능을 배포 하기 전에 컴퓨팅 환경을 성공적으로 준비 하는 데 도움이 되는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="48304-106">MBAM 서버 기능에 대 한 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="48304-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="48304-107">각 MBAM 서버 기능에는 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48304-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="48304-108">MBAM 설정 설치를 시작 하기 전에 모든 필수 구성 요소를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="48304-109">관리 및 모니터링 서버용 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="48304-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="48304-110">다음 표에는 MBAM 관리 및 모니터링 서버의 설치 필수 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48304-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="48304-111">요소일</span><span class="sxs-lookup"><span data-stu-id="48304-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="48304-112">세부 정보</span><span class="sxs-lookup"><span data-stu-id="48304-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="48304-113">Windows ServerWeb 서버 역할</span><span class="sxs-lookup"><span data-stu-id="48304-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="48304-114">이 역할은 mbam 관리 및 모니터링 서버 기능에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="48304-115">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="48304-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="48304-116">IIS 관리 스크립트 및 도구</span><span class="sxs-lookup"><span data-stu-id="48304-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="48304-117">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="48304-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="48304-118">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="48304-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="48304-119">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="48304-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="48304-120">기본 문서</span><span class="sxs-lookup"><span data-stu-id="48304-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="48304-121">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="48304-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="48304-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="48304-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="48304-123">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="48304-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="48304-124">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="48304-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="48304-125">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="48304-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="48304-126">보안이</span><span class="sxs-lookup"><span data-stu-id="48304-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="48304-127">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="48304-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="48304-128">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="48304-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="48304-129">Windows Server 기능</span><span class="sxs-lookup"><span data-stu-id="48304-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="48304-130">Microsoft .NET Framework 3.5.1 기능:</span><span class="sxs-lookup"><span data-stu-id="48304-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="48304-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="48304-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="48304-132">WCF 활성화</span><span class="sxs-lookup"><span data-stu-id="48304-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="48304-133">HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="48304-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="48304-134">비 HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="48304-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="48304-135">Windows Process Activation Service</span><span class="sxs-lookup"><span data-stu-id="48304-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="48304-136">프로세스 모델</span><span class="sxs-lookup"><span data-stu-id="48304-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="48304-137">.NET 환경</span><span class="sxs-lookup"><span data-stu-id="48304-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="48304-138">구성 Api</span><span class="sxs-lookup"><span data-stu-id="48304-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="48304-139">**참고**  지원 되는 운영 체제 목록은 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="48304-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="48304-140">규정 준수 및 감사 보고서 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="48304-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="48304-141">지원 되는 버전의 SQLServer에 준수 및 감사 보고서를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="48304-142">이 기능의 설치 전제 조건에는 SQL Server Reporting Services (SSRS)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="48304-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="48304-143">MBAM 서버 설치 중에 SSRS를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="48304-144">SSRS는 "구성 되지 않음" 또는 "SharePoint" 모드가 아니라 "기본" 모드 에서도 구성 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="48304-145">**참고**  지원 되는 운영 체제 및 SQLServer 버전 목록은 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="48304-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="48304-146">복구 및 하드웨어 데이터베이스용 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="48304-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="48304-147">복구 및 하드웨어 데이터베이스는 지원 되는 버전의 SQLServer에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="48304-148">SQL Server는 MBAM 서버 설치 중에 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="48304-149">TDE (투명 한 데이터 암호화) 기능을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="48304-150">**참고**  지원 되는 운영 체제 및 SQLServer 버전 목록은 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="48304-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="48304-151">TDE SQLServer 기능은 실시간 입/출력 (I/o) 암호화 및 데이터 및 로그 파일의 암호 해독을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="48304-152">TDE는 데이터와 로그 파일을 포함 하 여 "rest" 인 데이터를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="48304-153">다양 한 업계에서 설정 된 여러 법률, 규정 및 지침을 준수 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="48304-154">**참고**  TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 하기 때문에 로그인 하는 계정에 복구 키 정보 SQL 테이블을 볼 때 데이터베이스에 대 한 사용 권한이 있는 경우 복구 키 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="48304-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="48304-155">준수 및 감사 데이터베이스에 대 한 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="48304-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="48304-156">준수 및 감사 데이터베이스는 지원 되는 버전의 SQLServer에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="48304-157">SQL Server는 MBAM 서버 설치 중에 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="48304-158">**참고**  지원 되는 운영 체제 및 SQLServer 버전 목록은 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="48304-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="48304-159">MBAM 클라이언트에 대 한 설치 필수 조건</span><span class="sxs-lookup"><span data-stu-id="48304-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="48304-160">MBAM 클라이언트 설치를 시작 하기 전에 충족 해야 하는 필수 구성 요소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="48304-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="48304-161">TPM (신뢰할 수 있는 플랫폼 모듈) v 1.2의 기능</span><span class="sxs-lookup"><span data-stu-id="48304-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="48304-162">TPM 칩이 BIOS에서 켜져 있어야 하며 운영 체제에서 재설정 가능 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="48304-163">자세한 내용은 BIOS 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="48304-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="48304-164">**경고가**  키보드, 마우스 및 비디오가 키보드, 비디오, 마우스 (KVM) 스위치 대신 컴퓨터에 직접 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="48304-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="48304-165">KVM 스위치는 컴퓨터의 실제 현재 상태를 감지 하는 기능을 방해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48304-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="48304-166">관련 항목</span><span class="sxs-lookup"><span data-stu-id="48304-166">Related topics</span></span>


[<span data-ttu-id="48304-167">MBAM 1.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="48304-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="48304-168">MBAM 1.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="48304-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





