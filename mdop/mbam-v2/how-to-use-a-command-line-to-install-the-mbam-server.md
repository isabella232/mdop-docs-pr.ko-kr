---
title: 명령줄을 사용하여 MBAM 서버를 설치하는 방법
description: 명령줄을 사용하여 MBAM 서버를 설치하는 방법
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825643"
---
# <span data-ttu-id="a9fd6-103">명령줄을 사용하여 MBAM 서버를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="a9fd6-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="a9fd6-104">명령줄을 사용 하 여 독립 실행형 또는 구성 관리자 토폴로지로 MBAM 서버를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="a9fd6-105">다음 명령줄 예제는 테스트 환경 에서만 사용 해야 하는 아키텍처 인 단일 서버에 MBAM을 배포 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="a9fd6-106">여러 서버가 있어야 하는 프로덕션 환경에 MBAM을 배포 하는 경우 적절 하 게 명령줄을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="a9fd6-107">단독 토폴로지를 사용 하 여 MBAM 2.0 서버를 배포 하기 위한 명령줄</span><span class="sxs-lookup"><span data-stu-id="a9fd6-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="a9fd6-108">다음과 비슷한 명령줄을 사용 하 여 독립 실행형 토폴로지에 MBAM 서버를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="a9fd6-109">다음 표에서는 독립 실행형 토폴로지와 함께 MBAM 서버를 배포 하기 위한 명령줄 매개 변수에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fd6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9fd6-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a9fd6-111">매개 변수 값</span><span class="sxs-lookup"><span data-stu-id="a9fd6-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="a9fd6-112">설명</span><span class="sxs-lookup"><span data-stu-id="a9fd6-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-113">대규모</span><span class="sxs-lookup"><span data-stu-id="a9fd6-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-114">0</span><span class="sxs-lookup"><span data-stu-id="a9fd6-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-115">0-독립 실행형 토폴로지</span><span class="sxs-lookup"><span data-stu-id="a9fd6-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-117">01</span><span class="sxs-lookup"><span data-stu-id="a9fd6-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-118">0 – 라이선스에 동의 안 함-사용권 계약에 동의 agreement1</span><span class="sxs-lookup"><span data-stu-id="a9fd6-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="a9fd6-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-120">서버에 설치할 기능</span><span class="sxs-lookup"><span data-stu-id="a9fd6-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-121">KeyDatabase</span><span class="sxs-lookup"><span data-stu-id="a9fd6-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-122">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a9fd6-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="a9fd6-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-124">준수 및 감사 보고서 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a9fd6-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-125">보고</span><span class="sxs-lookup"><span data-stu-id="a9fd6-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-126">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="a9fd6-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="a9fd6-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-128">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="a9fd6-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="a9fd6-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-130">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="a9fd6-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-131">PolicyTemplate</span><span class="sxs-lookup"><span data-stu-id="a9fd6-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-132">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="a9fd6-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-134">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="a9fd6-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-135">준수 및 감사 데이터베이스에 액세스할 수 있는 Reporting Services 서비스 계정의 도메인 및 사용자 계정</span><span class="sxs-lookup"><span data-stu-id="a9fd6-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="a9fd6-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="a9fd6-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-138">준수 및 감사 데이터베이스에 액세스 하는 Reporting Services 서비스 계정의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="a9fd6-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-140">이름은</span><span class="sxs-lookup"><span data-stu-id="a9fd6-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-141">준수 및 감사 데이터베이스용 SQL Server 인스턴스 이름 – <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="a9fd6-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-143">이름은</span><span class="sxs-lookup"><span data-stu-id="a9fd6-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-144">복구 데이터베이스용 SQL Server 인스턴스 이름 – <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="a9fd6-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-146">이름은</span><span class="sxs-lookup"><span data-stu-id="a9fd6-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-147">준수 및 감사 보고서가 설치 되는 SQL Server Reporting Server 인스턴스 – <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-149">83</span><span class="sxs-lookup"><span data-stu-id="a9fd6-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-150">관리 및 모니터링 웹 사이트의 포트입니다. "83"는 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-152">83</span><span class="sxs-lookup"><span data-stu-id="a9fd6-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-153">셀프 서비스 포털 웹 사이트의 포트 "83"는 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a9fd6-154">Configuration Manager 토폴로지로 MBAM 2.0 서버를 배포 하기 위한 명령줄</span><span class="sxs-lookup"><span data-stu-id="a9fd6-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="a9fd6-155">다음과 비슷한 명령줄을 사용 하 여 구성 관리자 토폴로지에 MBAM 서버를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="a9fd6-156">다음 표에서는 구성 관리자 토폴로지에 MBAM 2.0 서버를 설치 하기 위한 명령줄 매개 변수에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fd6-157">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9fd6-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a9fd6-158">매개 변수 값</span><span class="sxs-lookup"><span data-stu-id="a9fd6-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="a9fd6-159">설명</span><span class="sxs-lookup"><span data-stu-id="a9fd6-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-160">대규모</span><span class="sxs-lookup"><span data-stu-id="a9fd6-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-161">raid-1</span><span class="sxs-lookup"><span data-stu-id="a9fd6-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-162">1-구성 관리자 토폴로지</span><span class="sxs-lookup"><span data-stu-id="a9fd6-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-164">01</span><span class="sxs-lookup"><span data-stu-id="a9fd6-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-165">0 – 라이선스에 동의 안 함-사용권 계약에 동의 agreement1</span><span class="sxs-lookup"><span data-stu-id="a9fd6-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="a9fd6-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-167">이름은</span><span class="sxs-lookup"><span data-stu-id="a9fd6-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-168">감사 데이터베이스용 SQL Server 인스턴스 이름- <strong> % computername%를 </strong> 컴퓨터 이름으로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="a9fd6-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="a9fd6-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-170">이름은</span><span class="sxs-lookup"><span data-stu-id="a9fd6-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-171">복구 데이터베이스용 SQL Server 인스턴스 이름- <strong> % computername%를 </strong> 컴퓨터 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="a9fd6-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-173">이름은</span><span class="sxs-lookup"><span data-stu-id="a9fd6-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-174">감사 보고서가 설치 되는 SQL Server Reporting Server 인스턴스 –% computername%를 컴퓨터 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-176">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="a9fd6-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-177">준수 및 감사 데이터베이스에 액세스할 수 있는 Reporting Services 서비스 계정의 도메인 및 사용자 계정</span><span class="sxs-lookup"><span data-stu-id="a9fd6-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="a9fd6-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="a9fd6-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-180">준수 및 감사 데이터베이스에 액세스 하는 Reporting Services 서비스 계정의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fd6-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-182">83</span><span class="sxs-lookup"><span data-stu-id="a9fd6-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-183">관리 및 모니터링 웹 사이트의 포트입니다. "83"는 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fd6-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="a9fd6-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-185">83</span><span class="sxs-lookup"><span data-stu-id="a9fd6-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fd6-186">셀프 서비스 포털 웹 사이트의 포트 "83"는 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9fd6-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a9fd6-187">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a9fd6-187">Related topics</span></span>


[<span data-ttu-id="a9fd6-188">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="a9fd6-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





