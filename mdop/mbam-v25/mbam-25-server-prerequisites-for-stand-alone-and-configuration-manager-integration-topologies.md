---
title: 독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소
description: 독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825998"
---
# <span data-ttu-id="da3f1-103">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="da3f1-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="da3f1-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 설치를 시작 하기 전에이 항목에 나열 된 전제 조건을 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="da3f1-105">이러한 전제 조건은 MBAM 독립 실행형 토폴로지와 System Center Configuration Manager 통합 토폴로지에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="da3f1-106">System Center Configuration Manager를 사용 하 여 MBAM을 배포 하는 경우에는 [구성 관리자 통합 토폴로지에만 적용 되는 mbam 2.5 서버 필수 구성](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)요소에 나열 된 추가 전제 조건을 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="da3f1-107">MBAM에 대해 지원 되는 하드웨어 및 운영 체제 목록은 [mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="da3f1-108">중요</span><span class="sxs-lookup"><span data-stu-id="da3f1-108">Important</span></span>**  
<span data-ttu-id="da3f1-109">MBAM 없이 BitLocker를 사용 하는 경우 드라이브를 해독 한 다음 services.msc를 사용 하 여 TPM을 지워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="da3f1-110">MBAM 클라이언트 PC가 이미 암호화 되어 있고 TPM 소유자 암호가 생성 된 경우 TPM의 소유권을 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="da3f1-111">필수 MBAM 역할 및 계정</span><span class="sxs-lookup"><span data-stu-id="da3f1-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-112">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-113">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-114">AD DS (Active Directory 도메인 서비스)에서 만든 그룹</span><span class="sxs-lookup"><span data-stu-id="da3f1-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-115"><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">이 그룹 및 계정에 대 한 설명은 MBAM 2.5 그룹 및 계정에 대 한 계획을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="da3f1-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="da3f1-116">복구 데이터베이스에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="da3f1-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-117">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-118">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-119">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="da3f1-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-120">SQL_Latin1_General_CP1_CI_AS 데이터 정렬을 사용 하 여 Microsoft SQL Server를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="da3f1-121"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-122">필요한 SQL Server 권한</span><span class="sxs-lookup"><span data-stu-id="da3f1-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-123">필요한 권한:</span><span class="sxs-lookup"><span data-stu-id="da3f1-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-124">SQL Server 인스턴스 로그인 서버 역할:</span><span class="sxs-lookup"><span data-stu-id="da3f1-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-125">dbcreator</span><span class="sxs-lookup"><span data-stu-id="da3f1-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="da3f1-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="da3f1-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="da3f1-127">SQL Server Reporting Services 인스턴스 권한:</span><span class="sxs-lookup"><span data-stu-id="da3f1-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-128">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="da3f1-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="da3f1-129">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="da3f1-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-130">선택 사항-SQL Server에서 사용할 수 있는 TDE (투명 데이터 암호화) 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-131">TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에 적용 되는 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="da3f1-132">참고</span><span class="sxs-lookup"><span data-stu-id="da3f1-132">Note</span></span></strong><br/><p><span data-ttu-id="da3f1-133">TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="da3f1-134">즉, SQL Server 데이터베이스에서 복구 키 정보를 보고 있고 해당 데이터베이스에 대 한 사용 권한이 있는 계정으로 로그온 한 경우 복구 키 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="da3f1-135">TDE에 대 한 자세한 내용은 <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> mbam 2.5 보안 고려 사항을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-136">SQL Server 데이터베이스 엔진 서비스</span><span class="sxs-lookup"><span data-stu-id="da3f1-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-137">MBAM 서버 설치 중에 SQL Server 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-138">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="da3f1-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-139">Windows PowerShell을 사용 하 여 원격 컴퓨터에서 데이터베이스를 구성 하는 경우 windows PowerShell을 복구 데이터베이스 서버에 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="da3f1-140">준수 및 감사 데이터베이스에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="da3f1-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-141">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-142">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-143">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="da3f1-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-144">SQL_Latin1_General_CP1_CI_AS 데이터 정렬을 사용 하 여 SQL Server를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="da3f1-145"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-146">필요한 SQL Server 권한</span><span class="sxs-lookup"><span data-stu-id="da3f1-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-147">필요한 권한:</span><span class="sxs-lookup"><span data-stu-id="da3f1-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-148">SQL Server 인스턴스 로그인 서버 역할:</span><span class="sxs-lookup"><span data-stu-id="da3f1-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-149">dbcreator</span><span class="sxs-lookup"><span data-stu-id="da3f1-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="da3f1-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="da3f1-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="da3f1-151">SQL Server Reporting Services 인스턴스 권한:</span><span class="sxs-lookup"><span data-stu-id="da3f1-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-152">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="da3f1-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="da3f1-153">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="da3f1-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-154">선택 사항-SQL Server에 TDE (투명 데이터 암호화) 기능 설치</span><span class="sxs-lookup"><span data-stu-id="da3f1-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-155">TDE SQL Server 기능은 데이터 및 로그 파일에 대 한 실시간 I/o 암호화 및 암호 해독을 수행 하 여 다양 한 업계에 적용 되는 법률, 규정 및 지침을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="da3f1-156">TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="da3f1-157">즉, SQL Server 데이터베이스에서 복구 키 정보를 보고 있고 해당 데이터베이스에 대 한 사용 권한이 있는 계정으로 로그온 한 경우 복구 키 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="da3f1-158">TDE에 대 한 자세한 내용은 <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> mbam 2.5 보안 고려 사항을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-159">SQL Server 데이터베이스 엔진 서비스</span><span class="sxs-lookup"><span data-stu-id="da3f1-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-160">MBAM 서버 설치 중에 SQL Server 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="da3f1-161">그러나 SQL Server는 원격으로 실행할 수 있습니다. MBAM 서버 소프트웨어를 설치 하는 것과 동일한 서버에 있을 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-162">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="da3f1-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-163">Windows PowerShell을 사용 하 여 원격 컴퓨터에서 데이터베이스를 구성 하는 경우 windows PowerShell을 준수 및 감사 데이터베이스 서버에 설치 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="da3f1-164">보고서에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="da3f1-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-165">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-166">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-167">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="da3f1-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-168">SQL_Latin1_General_CP1_CI_AS 데이터 정렬을 사용 하 여 SQL Server를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="da3f1-169"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-170">SSRS (SQL Server Reporting Services)</span><span class="sxs-lookup"><span data-stu-id="da3f1-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-171">MBAM 서버 설치 중에 SSRS를 설치 하 고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="da3f1-172">구성 &quot; &quot; 되지 않음 또는 SharePoint 모드가 아닌 기본 모드에서 SSRS를 구성할 수 &quot; &quot; 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-173">SSRS 인스턴스 권한 – 보고서를 구성 하는 서버에서 별도의 서버에 데이터베이스를 설치 하는 경우에만 보고서를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-174">필요한 인스턴스 권한:</span><span class="sxs-lookup"><span data-stu-id="da3f1-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3f1-175">폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="da3f1-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="da3f1-176">보고서 게시</span><span class="sxs-lookup"><span data-stu-id="da3f1-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-177">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="da3f1-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-178">Windows PowerShell을 사용 하 여 원격 컴퓨터에서 데이터베이스를 구성 하는 경우 windows PowerShell을이 데이터베이스 서버에 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="da3f1-179">관리 및 모니터링 서버용 필수 조건</span><span class="sxs-lookup"><span data-stu-id="da3f1-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="da3f1-180">다음 표에는 MBAM 관리 및 모니터링 서버의 설치 필수 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-181">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-182">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-183">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="da3f1-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-184">이 역할은 관리 및 모니터링 서버 기능에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-185">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="da3f1-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-186"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="da3f1-187">SSL 인증서</span><span class="sxs-lookup"><span data-stu-id="da3f1-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="da3f1-188">선택 사항.</span><span class="sxs-lookup"><span data-stu-id="da3f1-188">Optional.</span></span> <span data-ttu-id="da3f1-189">클라이언트 컴퓨터와 웹 서비스 간의 통신을 보호 하려면 신뢰할 수 있는 보안 기관에서 서명한 인증서를 얻고 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-190">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="da3f1-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="da3f1-191">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="da3f1-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="da3f1-192">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="da3f1-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="da3f1-193">기본 문서</span><span class="sxs-lookup"><span data-stu-id="da3f1-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="da3f1-194">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="da3f1-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="da3f1-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="da3f1-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="da3f1-196">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="da3f1-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="da3f1-197">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="da3f1-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="da3f1-198">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="da3f1-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="da3f1-199">보안이</span><span class="sxs-lookup"><span data-stu-id="da3f1-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="da3f1-200">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="da3f1-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="da3f1-201">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="da3f1-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-202">Windows Server 기능</span><span class="sxs-lookup"><span data-stu-id="da3f1-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="da3f1-203">.NET Framework 4.5 기능:</span><span class="sxs-lookup"><span data-stu-id="da3f1-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="da3f1-204">.NET Framework 4.5 또는 4.6</span><span class="sxs-lookup"><span data-stu-id="da3f1-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="da3f1-205"></strong> - 이 버전의 windows server에는 windows server 2016 .net Framework 4.6이 이미 설치 되어 있지만, 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="da3f1-206">Windows server 2012 또는 Windows Server 2012 R2 </strong> - .net Framework 4.5이 이러한 버전의 windows server에 대해 이미 설치 되어 있지만이를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="da3f1-207">Windows Server 2008 R2 </strong> - .net Framework 4.5는 windows Server 2008 r2에 포함 되어 있지 않으므로 <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Microsoft .net framework 4.5을 다운로드 </a> 하 여 별도로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="da3f1-208">참고</span><span class="sxs-lookup"><span data-stu-id="da3f1-208">Note</span></span></strong><br/><p><span data-ttu-id="da3f1-209">MBAM 2.0 또는 MBAM 2.0 SP1에서 업그레이드 하는 경우 .NET Framework 4.5을 설치 해야 하는 경우 <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> </a> 웹 사이트를 작동 하는 데 필요한 추가 단계는 mbam 2.5에 대 한 릴리스 정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="da3f1-210">WCF 활성화</span><span class="sxs-lookup"><span data-stu-id="da3f1-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="da3f1-211">HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="da3f1-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="da3f1-212">비 HTTP 정품 인증 (Windows Server 2008, 2012 및 2012 R2에만 해당)</span><span class="sxs-lookup"><span data-stu-id="da3f1-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="da3f1-213">TCP 활성화</span><span class="sxs-lookup"><span data-stu-id="da3f1-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="da3f1-214">Windows Process Activation Service:</span><span class="sxs-lookup"><span data-stu-id="da3f1-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="da3f1-215">프로세스 모델</span><span class="sxs-lookup"><span data-stu-id="da3f1-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="da3f1-216">.NET Framework 환경</span><span class="sxs-lookup"><span data-stu-id="da3f1-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="da3f1-217">구성 Api</span><span class="sxs-lookup"><span data-stu-id="da3f1-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-218">ASP.NET MVC 4.0</span><span class="sxs-lookup"><span data-stu-id="da3f1-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="da3f1-219">ASP.NET MVC 4 다운로드</span><span class="sxs-lookup"><span data-stu-id="da3f1-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-220">SPN (서비스 사용자 이름)</span><span class="sxs-lookup"><span data-stu-id="da3f1-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-221">웹 응용 프로그램에는 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 가상 호스트 이름에 대 한 SPN이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="da3f1-222">관리 권한이 Active Directory 도메인 서비스에서 Spn을 만들 수 있도록 허용 하는 경우 MBAM이 사용자를 위한 SPN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="da3f1-223"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Spn을 </a> 만드는 데 필요한 권한에 대 한 자세한 내용은 Setspn을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="da3f1-224">Spn을 만들 수 있는 관리자 권한이 없는 경우 다음 명령을 사용 하 여 조직의 Active Directory 관리자에 게 사용자의 SPN을 만들도록 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="da3f1-225">코드 예제에서 가상 호스트 이름은 mbamvirtual.contoso.com 웹 응용 프로그램 풀에 사용 되는 도메인 계정은 contoso\mbamapppooluser.입니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="da3f1-226">참고</span><span class="sxs-lookup"><span data-stu-id="da3f1-226">Note</span></span></strong><br/><p><span data-ttu-id="da3f1-227">부하 분산을 설정 하는 경우 모든 서버에서 동일한 응용 프로그램 풀 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="da3f1-228">정규화 된 NetBIOS 및 사용자 지정 호스트 이름에 대 한 Spn을 등록 하는 방법에 대 한 자세한 내용은 <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> MBAM 웹 사이트 보안 방법 계획을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="da3f1-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="da3f1-229">셀프 서비스 포털의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="da3f1-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-230">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-231">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-232">지원 되는 Windows Server 버전</span><span class="sxs-lookup"><span data-stu-id="da3f1-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-233"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> </a> 지원 되는 버전에 대해 mbam 2.5 지원 되는 구성을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-234">ASP.NET MVC 4.0</span><span class="sxs-lookup"><span data-stu-id="da3f1-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="da3f1-235">ASP.NET MVC 4 다운로드</span><span class="sxs-lookup"><span data-stu-id="da3f1-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-236">웹 서비스 IIS 관리 도구</span><span class="sxs-lookup"><span data-stu-id="da3f1-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-237">SPN (서비스 사용자 이름)</span><span class="sxs-lookup"><span data-stu-id="da3f1-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-238">웹 응용 프로그램에는 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 가상 호스트 이름에 대 한 SPN이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="da3f1-239">관리 권한이 Active Directory 도메인 서비스에서 Spn을 만들 수 있도록 허용 하는 경우 MBAM이 사용자를 위한 SPN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="da3f1-240"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Spn을 </a> 만드는 데 필요한 권한에 대 한 자세한 내용은 Setspn을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="da3f1-241">Spn을 만들 수 있는 관리자 권한이 없는 경우 다음 명령을 사용 하 여 조직의 관리자에 게 사용자를 위한 SPN을 만들어야 하는 Active Directory 관리자에 게 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="da3f1-242">코드 예제에서 가상 호스트 이름은 mbamvirtual.contoso.com 웹 응용 프로그램 풀에 사용 되는 도메인 계정은 contoso\mbamapppooluser.입니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="da3f1-243">참고</span><span class="sxs-lookup"><span data-stu-id="da3f1-243">Note</span></span></strong><br/><p><span data-ttu-id="da3f1-244">부하 분산을 설정 하는 경우 모든 서버에서 동일한 응용 프로그램 풀 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="da3f1-245">정규화 된 NetBIOS 및 사용자 지정 호스트 이름에 대 한 Spn을 등록 하는 방법에 대 한 자세한 내용은 <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> MBAM 웹 사이트 보안 방법 계획을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="da3f1-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="da3f1-246">관리 워크스테이션의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="da3f1-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-247">요소일</span><span class="sxs-lookup"><span data-stu-id="da3f1-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="da3f1-248">세부 정보</span><span class="sxs-lookup"><span data-stu-id="da3f1-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-249">MBAM 클라이언트를 설치 하기 전에, <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> MDOP 그룹 정책 (admx) 템플릿을 가져오는 방법과 </a> 엔터프라이즈에서 BitLocker 드라이브 암호화에 대해 구현 하려는 설정으로 구성 하는 방법에서 Mbam 그룹 정책 템플릿을 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="da3f1-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3f1-250">MBAM 클라이언트를 설치 하기 전에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3f1-251">수행할 작업</span><span class="sxs-lookup"><span data-stu-id="da3f1-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="da3f1-252">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="da3f1-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3f1-253">MBAM 그룹 정책 서식 파일 복사</span><span class="sxs-lookup"><span data-stu-id="da3f1-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="da3f1-254">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="da3f1-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3f1-255">그룹 정책 설정 편집</span><span class="sxs-lookup"><span data-stu-id="da3f1-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="da3f1-256">MBAM 2.5 그룹 정책 설정 편집</span><span class="sxs-lookup"><span data-stu-id="da3f1-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="da3f1-257">관련 항목</span><span class="sxs-lookup"><span data-stu-id="da3f1-257">Related topics</span></span>


[<span data-ttu-id="da3f1-258">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="da3f1-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="da3f1-259">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="da3f1-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="da3f1-260">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="da3f1-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="da3f1-261">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="da3f1-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="da3f1-262">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="da3f1-263">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da3f1-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




