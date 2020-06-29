---
title: 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
description: 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826558"
---
# <span data-ttu-id="9b1d0-103">독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="9b1d0-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="9b1d0-104">이 항목에서는 Configuration Manager 독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포 하는 데 권장 되는 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="9b1d0-105">이 토폴로지에서 MBAM은 독립 실행형 제품으로 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="9b1d0-106">또한 configuration manager와 MBAM을 통합 하는 Configuration Manager 통합 토폴로지로 MBAM을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="9b1d0-107">자세한 내용은 [Configuration Manager 통합 토폴로지에 있는 MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="9b1d0-108">이 항목에 설명 된 소프트웨어의 지원 되는 버전 목록은 [Mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="9b1d0-109">**참고**  테스트 환경 에서만 단일 서버 아키텍처를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="9b1d0-110">권장 서버 수 및 지원 되는 클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="9b1d0-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="9b1d0-111">프로덕션 환경에서 권장 되는 서버 수 및 지원 되는 클라이언트 수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1d0-112">프로덕션 환경의 권장 아키텍처</span><span class="sxs-lookup"><span data-stu-id="9b1d0-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="9b1d0-113">세부 정보</span><span class="sxs-lookup"><span data-stu-id="9b1d0-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1d0-114">서버 및 다른 컴퓨터 수</span><span class="sxs-lookup"><span data-stu-id="9b1d0-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1d0-115">두 서버</span><span class="sxs-lookup"><span data-stu-id="9b1d0-115">Two servers</span></span></p>
<p><span data-ttu-id="9b1d0-116">하나의 워크스테이션</span><span class="sxs-lookup"><span data-stu-id="9b1d0-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1d0-117">지원 되는 클라이언트 컴퓨터 수</span><span class="sxs-lookup"><span data-stu-id="9b1d0-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1d0-118">50만</span><span class="sxs-lookup"><span data-stu-id="9b1d0-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9b1d0-119">독립 실행형 토폴로지가 있는 권장 MBAM 상위 수준 아키텍처</span><span class="sxs-lookup"><span data-stu-id="9b1d0-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="9b1d0-120">다음 다이어그램 및 표에서는 독립 실행형 토폴로지에 대 한 MBAM에 대해 권장 되는 높은 수준의 두 서버 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="9b1d0-121">MBAM 다중 포리스트 배포에는 단방향 또는 양방향 트러스트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="9b1d0-122">단방향 트러스트의 경우 서버 도메인이 클라이언트 도메인을 신뢰 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="9b1d0-124">이 서버 설명 데이터베이스 서버에 구성할 서버 기능</span><span class="sxs-lookup"><span data-stu-id="9b1d0-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="9b1d0-125">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="9b1d0-125">Compliance and Audit Database</span></span>

<span data-ttu-id="9b1d0-126">이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="9b1d0-127">**규정 준수 및 감사 데이터베이스** 는 SQL Server Reporting Services가 호스트 하는 보고서에 주로 사용 되는 규정 준수 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="9b1d0-128">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="9b1d0-128">Recovery Database</span></span>

<span data-ttu-id="9b1d0-129">이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="9b1d0-130">**복구 데이터베이스** 는 mbam 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="9b1d0-131">보고</span><span class="sxs-lookup"><span data-stu-id="9b1d0-131">Reports</span></span>

<span data-ttu-id="9b1d0-132">이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="9b1d0-133">**보고서** 는 엔터프라이즈의 클라이언트 컴퓨터에 대 한 복구 감사 및 준수 상태 데이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="9b1d0-134">관리 및 모니터링 웹 사이트에서 또는 SQL Server Reporting Services에서 직접 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="9b1d0-135">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="9b1d0-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="9b1d0-136">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="9b1d0-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="9b1d0-137">이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="9b1d0-138">**관리 및 모니터링 웹 사이트** 는 다음 작업을 수행 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="9b1d0-139">최종 사용자가 잠겨 있는 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있도록 지원 합니다. (이 웹 사이트의이 영역을 일반적으로 지원 센터 라고 합니다.)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="9b1d0-140">클라이언트 컴퓨터에 대 한 호환성 상태 및 복구 작업을 표시 하는 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="9b1d0-141">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="9b1d0-141">Self-Service Portal</span></span>

<span data-ttu-id="9b1d0-142">이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="9b1d0-143">**셀프 서비스 포털** 은 클라이언트 컴퓨터의 최종 사용자가 자신의 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 사용 하 여 개별적으로 웹 사이트에 로그온 할 수 있도록 하는 웹 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="9b1d0-144">이 웹 사이트의 웹 서비스 모니터링</span><span class="sxs-lookup"><span data-stu-id="9b1d0-144">Monitoring web services for this website</span></span>

<span data-ttu-id="9b1d0-145">이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="9b1d0-146">**모니터링 웹 서비스** 는 Mbam 클라이언트와 웹 사이트에서 데이터베이스와 통신 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="9b1d0-147">**중요**  MBAM 웹 사이트는 복구 데이터베이스와 직접 통신 하므로 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1에서는 모니터링 웹 서비스를 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="9b1d0-148">관리 워크스테이션</span><span class="sxs-lookup"><span data-stu-id="9b1d0-148">Management workstation</span></span>

<span data-ttu-id="9b1d0-149">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="9b1d0-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="9b1d0-150">MBAM 그룹 정책 템플릿은 MBAM에 대 한 구현 설정을 정의 하는 그룹 정책 설정으로, BitLocker 드라이브 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="9b1d0-151">MBAM을 실행 하기 전에, [MDOP 그룹 정책 (admx) 템플릿을 가져오고](https://go.microsoft.com/fwlink/p/?LinkId=393941) 지원 되는 Windows Server 또는 Windows 운영 체제를 실행 하는 서버 또는 워크스테이션에 복사 하는 방법에서 그룹 정책 템플릿을 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="9b1d0-152">워크스테이션이 전용 컴퓨터 일 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="9b1d0-153">MBAM 클라이언트 및 Configuration Manager 클라이언트 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="9b1d0-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="9b1d0-154">MBAM 클라이언트 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="9b1d0-154">MBAM Client software</span></span>

<span data-ttu-id="9b1d0-155">MBAM 클라이언트:</span><span class="sxs-lookup"><span data-stu-id="9b1d0-155">The MBAM Client:</span></span>

-   <span data-ttu-id="9b1d0-156">그룹 정책 개체를 사용 하 여 엔터프라이즈의 클라이언트 컴퓨터에 BitLocker 드라이브 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="9b1d0-157">운영 체제 드라이브, 고정 데이터 드라이브, 이동식 (USB) 데이터 드라이브 등 세 가지 데이터 드라이브 유형의 Bitlocker 복구 키를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="9b1d0-158">클라이언트 컴퓨터에 대 한 복구 정보 및 컴퓨터 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="9b1d0-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9b1d0-159">Related topics</span></span>


[<span data-ttu-id="9b1d0-160">MBAM 2.5 시작</span><span class="sxs-lookup"><span data-stu-id="9b1d0-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="9b1d0-161">Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="9b1d0-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="9b1d0-162">MBAM 2.5 배포의 예시된 기능</span><span class="sxs-lookup"><span data-stu-id="9b1d0-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="9b1d0-163">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="9b1d0-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9b1d0-164">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9b1d0-165">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





