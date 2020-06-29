---
title: Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
description: Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825763"
---
# <span data-ttu-id="308df-103">Configuration Manager 통합 토폴로지와 함께 MBAM 2.5의 상위 수준 아키텍처</span><span class="sxs-lookup"><span data-stu-id="308df-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="308df-104">이 항목에서는 Configuration Manager 통합 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포 하는 데 권장 되는 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="308df-105">이 토폴로지는 MBAM을 System Center Configuration Manager와 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="308df-106">독립 실행형 토폴로지에 MBAM을 배포 하려면 [독립 실행형 토폴로지와 함께 mbam 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="308df-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="308df-107">이 항목에 설명 된 소프트웨어의 지원 되는 버전 목록은 [Mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="308df-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="308df-108">**중요**  Windows To Go는 Configuration Manager 2007를 사용 중인 경우 Configuration Manager 통합 토폴로지 설치에 대해 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="308df-109">권장 서버 수 및 지원 되는 클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="308df-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="308df-110">프로덕션 환경에서 권장 되는 서버 수 및 지원 되는 클라이언트 수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="308df-111">권장 아키텍처</span><span class="sxs-lookup"><span data-stu-id="308df-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="308df-112">세부 정보</span><span class="sxs-lookup"><span data-stu-id="308df-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="308df-113">서버 및 다른 컴퓨터 수</span><span class="sxs-lookup"><span data-stu-id="308df-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-114">3 대의 서버</span><span class="sxs-lookup"><span data-stu-id="308df-114">Three servers</span></span></p>
<p><span data-ttu-id="308df-115">하나의 워크스테이션</span><span class="sxs-lookup"><span data-stu-id="308df-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="308df-116">지원 되는 클라이언트 컴퓨터 수</span><span class="sxs-lookup"><span data-stu-id="308df-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-117">50만</span><span class="sxs-lookup"><span data-stu-id="308df-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="308df-118">구성 관리자 통합 및 독립 실행형 토폴로지 간의 차이점</span><span class="sxs-lookup"><span data-stu-id="308df-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="308df-119">토폴로지 간의 주요 차이점은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="308df-120">준수 및 보고 기능은 MBAM에서 제거 되며 구성 관리자에서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="308df-121">보고서는 MBAM 관리 및 모니터링 웹 사이트에서 계속 볼 수 있는 복구 감사 보고서에 대 한 예외를 포함 하 여 Configuration Manager 관리 콘솔에서 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="308df-122">Configuration Manager 통합 토폴로지가 있는 권장 MBAM 상위 수준 아키텍처</span><span class="sxs-lookup"><span data-stu-id="308df-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="308df-123">다음 다이어그램 및 표에서는 Configuration Manager 통합 토폴로지와 함께 MBAM에 권장 되는 상위 수준 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="308df-124">MBAM 다중 포리스트 배포에는 단방향 또는 양방향 트러스트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="308df-125">단방향 트러스트의 경우 서버 도메인이 클라이언트 도메인을 신뢰 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="308df-127">데이터베이스 서버</span><span class="sxs-lookup"><span data-stu-id="308df-127">Database server</span></span>

#### <span data-ttu-id="308df-128">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="308df-128">Recovery database</span></span>

<span data-ttu-id="308df-129">이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 컴퓨터에서 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="308df-130">**복구 데이터베이스** 는 Mbam 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="308df-131">데이터베이스 감사</span><span class="sxs-lookup"><span data-stu-id="308df-131">Audit database</span></span>

<span data-ttu-id="308df-132">이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 컴퓨터에서 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="308df-133">**감사 데이터베이스** 는 복구 데이터에 액세스 한 클라이언트 컴퓨터에서 수집 된 감사 활동 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="308df-134">보고</span><span class="sxs-lookup"><span data-stu-id="308df-134">Reports</span></span>

<span data-ttu-id="308df-135">이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 컴퓨터에서 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="308df-136">**보고서** 는 엔터프라이즈의 클라이언트 컴퓨터에 대 한 복구 감사 데이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="308df-137">Configuration Manager 콘솔에서 또는 SQL Server Reporting Services에서 직접 보고서를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="308df-138">Configuration Manager 주 사이트 서버</span><span class="sxs-lookup"><span data-stu-id="308df-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="308df-139">System Center Configuration Manager 통합 기능</span><span class="sxs-lookup"><span data-stu-id="308df-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="308df-140">이 기능은 configuration manager 인프라의 최상위 계층 서버인 Configuration Manager 기본 사이트 서버에서 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="308df-141">**Configuration Manager 서버** 는 클라이언트 컴퓨터에서 하드웨어 인벤터리 정보를 수집 하 고 클라이언트 컴퓨터의 BitLocker 규격을 보고 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="308df-142">Microsoft BitLocker 관리 및 모니터링 설정 마법사를 실행 하 여 서버 소프트웨어를 설치 하는 경우 MBAM 지원 컴퓨터 모음, 구성 기준 및 보고서가 Configuration Manager 기본 사이트 서버에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="308df-143">**Configuration Manager 콘솔** 은 Mbam 서버 소프트웨어를 설치 하는 동일한 컴퓨터에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="308df-144">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="308df-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="308df-145">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="308df-145">Administration and monitoring website</span></span>

<span data-ttu-id="308df-146">이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="308df-147">**관리 및 모니터링 웹 사이트** 는 다음 작업을 수행 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="308df-148">최종 사용자가 잠겨 있는 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있도록 지원 합니다. (이 웹 사이트의이 영역을 일반적으로 지원 센터 라고 합니다.)</span><span class="sxs-lookup"><span data-stu-id="308df-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="308df-149">클라이언트 컴퓨터에 대 한 복구 작업을 보여 주는 복구 감사 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="308df-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="308df-150">다른 보고서는 Configuration Manager 콘솔에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="308df-151">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="308df-151">Self-service portal</span></span>

<span data-ttu-id="308df-152">이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="308df-153">**셀프 서비스 포털** 은 클라이언트 컴퓨터의 최종 사용자가 자신의 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 사용 하 여 개별적으로 웹 사이트에 로그온 할 수 있도록 하는 웹 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="308df-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="308df-154">이 웹 사이트의 웹 서비스 모니터링</span><span class="sxs-lookup"><span data-stu-id="308df-154">Monitoring web services for this website</span></span>

<span data-ttu-id="308df-155">이 기능은 Windows Server를 실행 하는 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="308df-156">**모니터링 웹 서비스** 는 Mbam 클라이언트와 웹 사이트에서 데이터베이스와 통신 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="308df-157">중요</span><span class="sxs-lookup"><span data-stu-id="308df-157">Important</span></span>**<br><span data-ttu-id="308df-158">MBAM 웹 사이트는 복구 데이터베이스와 직접 통신 하므로 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1에서는 모니터링 웹 서비스를 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="308df-159">관리 워크스테이션</span><span class="sxs-lookup"><span data-stu-id="308df-159">Management workstation</span></span>

#### <span data-ttu-id="308df-160">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="308df-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="308df-161">**Mbam 그룹 정책 템플릿은** mbam에 대 한 구현 설정을 정의 하는 그룹 정책 설정으로, BitLocker 드라이브 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="308df-162">MBAM을 실행 하기 전에, [MDOP 그룹 정책 (admx) 템플릿을 가져오고](https://go.microsoft.com/fwlink/p/?LinkId=393941) 지원 되는 Windows Server 또는 Windows 운영 체제를 실행 하는 서버 또는 워크스테이션에 복사 하는 방법에서 그룹 정책 템플릿을 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="308df-163">참고</span><span class="sxs-lookup"><span data-stu-id="308df-163">NOTE</span></span>**<br><span data-ttu-id="308df-164">워크스테이션이 전용 컴퓨터 일 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="308df-165">MBAM 클라이언트 및 Configuration Manager 클라이언트 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="308df-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="308df-166">MBAM 클라이언트 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="308df-166">MBAM Client software</span></span>

<span data-ttu-id="308df-167">**Mbam 클라이언트**:</span><span class="sxs-lookup"><span data-stu-id="308df-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="308df-168">그룹 정책 개체를 사용 하 여 엔터프라이즈의 클라이언트 컴퓨터에 BitLocker 드라이브 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="308df-169">운영 체제 드라이브, 고정 데이터 드라이브, 이동식 (USB) 데이터 드라이브 등 세 가지 데이터 드라이브 유형의 BitLocker 복구 키를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="308df-170">클라이언트 컴퓨터에 대 한 복구 정보 및 컴퓨터 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="308df-171">구성 관리자 클라이언트</span><span class="sxs-lookup"><span data-stu-id="308df-171">Configuration Manager Client</span></span>

<span data-ttu-id="308df-172">Configuration manager **클라이언트** 는 구성 관리자가 클라이언트 컴퓨터에 대 한 하드웨어 호환성 데이터를 수집 하 고 규정 준수 정보를 보고할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="308df-173">지원 되는 Configuration Manager 버전에 대 한 MBAM 배포의 차이점</span><span class="sxs-lookup"><span data-stu-id="308df-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="308df-174">Configuration Manager 통합 토폴로지로 MBAM을 배포 하는 경우 기본 사이트 서버에 MBAM을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="308df-175">그러나 MBAM 설치는 시스템 Center2012 구성 관리자 및 구성 Manager2007에 따라 다르게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="308df-176">Configuration Manager 버전</span><span class="sxs-lookup"><span data-stu-id="308df-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="308df-177">설명</span><span class="sxs-lookup"><span data-stu-id="308df-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="308df-178">System Center2012 R2 구성 관리자</span><span class="sxs-lookup"><span data-stu-id="308df-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="308df-179">시스템 Center2012 구성 관리자</span><span class="sxs-lookup"><span data-stu-id="308df-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-180">주 사이트 서버 또는 중앙 관리 서버에 MBAM을 설치 하는 경우 MBAM은 해당 사이트 서버에서 모든 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="308df-181">구성 Manager2007 R2</span><span class="sxs-lookup"><span data-stu-id="308df-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="308df-182">구성 Manager2007</span><span class="sxs-lookup"><span data-stu-id="308df-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-183">중앙 사이트 상위 서버를 사용 하 여 더 큰 구성 관리자 계층 구조의 일부인 주 사이트 서버에 MBAM을 설치 하는 경우 MBAM은 중앙 사이트 상위 서버를 식별 하 고 해당 상위 서버의 모든 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="308df-184">설치에는 필수 조건을 확인 하 고 Configuration Manager 개체 및 보고서를 설치 하는 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="308df-185">예를 들어, 중앙 사이트 상위 서버의 자식인 주 사이트 서버에 MBAM을 설치 하는 경우 MBAM은 상위 서버에 모든 Configuration Manager 개체와 보고서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="308df-186">부모 서버에 MBAM을 설치 하는 경우 MBAM은 해당 상위 서버의 모든 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="308df-187">MBAM이 구성 관리자와 작동 하는 방식</span><span class="sxs-lookup"><span data-stu-id="308df-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="308df-188">Configuration Manager와 MBAM의 통합은 다음 표에 설명 된 항목을 설치 하는 구성 팩을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="308df-189">Configuration Manager에 설치 된 항목</span><span class="sxs-lookup"><span data-stu-id="308df-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="308df-190">설명</span><span class="sxs-lookup"><span data-stu-id="308df-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="308df-191">구성 데이터</span><span class="sxs-lookup"><span data-stu-id="308df-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-192">구성 데이터는 두 개의 구성 항목을 포함 하는 "BitLocker Protection" 이라는 구성 기준을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="308df-193">BitLocker 운영 체제 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="308df-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="308df-194">BitLocker 고정 데이터 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="308df-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="308df-195">구성 기준은 MBAM이 설치 되어 있는 경우에도 만들어지는 MBAM 지원 컴퓨터 컬렉션에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="308df-196">두 개의 구성 항목은 클라이언트 컴퓨터의 준수 상태를 평가 하기 위한 기반을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="308df-197">이 정보는 구성 관리자에서 캡처, 저장 및 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="308df-198">구성 항목은 운영 체제 드라이브 및 고정 데이터 드라이브에 대 한 규정 준수 요구 사항에 기반을 둔 것입니다.</span><span class="sxs-lookup"><span data-stu-id="308df-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="308df-199">이러한 드라이브 유형에 대 한 준수를 평가할 수 있도록 배포 된 컴퓨터에 대 한 필수 세부 정보가 수집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="308df-200">기본적으로 구성 기준은 준수 상태 every12 시간을 평가 하 고 규정 준수 데이터를 구성 관리자에 게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="308df-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="308df-201">MBAM 지원 컴퓨터 모음</span><span class="sxs-lookup"><span data-stu-id="308df-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-202">MBAM 지원 컴퓨터 라고 하는 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="308df-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="308df-203">구성 기준은이 컬렉션에 있는 클라이언트 컴퓨터를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="308df-204">이것은 동적 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="308df-204">This is a dynamic collection.</span></span> <span data-ttu-id="308df-205">기본적으로 every12 시간을 실행 하 고 다음 세 가지 조건을 기준으로 멤버 자격을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="308df-206">컴퓨터가 지원 되는 Windows 운영 체제 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="308df-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="308df-207">컴퓨터가 물리적 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="308df-207">The computer is a physical computer.</span></span> <span data-ttu-id="308df-208">가상 머신은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="308df-209">컴퓨터에 사용할 수 있는 TPM (신뢰할 수 있는 플랫폼 모듈)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="308df-210">Windows7에 대해 호환 되는 버전의 TPM 1.2 이상이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="308df-211">Windows10, Windows 8.1, Windows8 및 Windows To Go는 TPM이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="308df-212">컬렉션이 모든 컴퓨터에 대해 평가 되 고 호환 컴퓨터의 하위 집합이 만들어지고, 준수 평가 및 MBAM 통합에 대 한 보고를 위한 기반을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="308df-213">보고</span><span class="sxs-lookup"><span data-stu-id="308df-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-214">Configuration Manager 통합 토폴로지로 MBAM을 구성 하는 경우 복구 감사 보고서를 제외한 모든 보고서를 볼 수 있으며,이는 MBAM 관리 및 모니터링 웹 사이트에서 계속 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="308df-215">Configuration Manager에서 사용할 수 있는 보고서는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="308df-216">보고서</span><span class="sxs-lookup"><span data-stu-id="308df-216">Report</span></span></th>
<th align="left"><span data-ttu-id="308df-217">설명</span><span class="sxs-lookup"><span data-stu-id="308df-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="308df-218">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="308df-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-219">IT 관리자에 게 단일 보고서 (준수 상태 배포, 비규격-오류 배포, 드라이브 유형별 준수 상태 배포)의 세 가지 정보 보기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="308df-220">보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="308df-221">BitLocker 엔터프라이즈 준수 세부 정보</span><span class="sxs-lookup"><span data-stu-id="308df-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-222">IT 관리자가 엔터프라이즈의 BitLocker 암호화 준수 상태에 대 한 정보를 볼 수 있으며 각 컴퓨터에 대 한 준수 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="308df-223">보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="308df-224">BitLocker 컴퓨터 준수</span><span class="sxs-lookup"><span data-stu-id="308df-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-225">IT 관리자가 개별 컴퓨터를 보고 규격 상태 또는 비규격으로 보고 된 이유를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="308df-226">또한이 보고서에는 운영 체제 드라이브 및 고정 데이터 드라이브의 암호화 상태도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="308df-227">BitLocker Enterprise 규정 준수 요약</span><span class="sxs-lookup"><span data-stu-id="308df-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="308df-228">IT 관리자가 엔터프라이즈에서 MBAM 정책 준수 상태를 볼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="308df-229">각 컴퓨터의 상태가 평가 되며,이 보고서에는 정책에 대 한 엔터프라이즈의 모든 컴퓨터 준수에 대 한 요약이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="308df-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="308df-230">보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="308df-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="308df-231">관련 항목</span><span class="sxs-lookup"><span data-stu-id="308df-231">Related topics</span></span>


[<span data-ttu-id="308df-232">MBAM 2.5 시작</span><span class="sxs-lookup"><span data-stu-id="308df-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="308df-233">독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="308df-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="308df-234">MBAM 2.5 배포의 예시된 기능</span><span class="sxs-lookup"><span data-stu-id="308df-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="308df-235">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="308df-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="308df-236">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="308df-237">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="308df-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




