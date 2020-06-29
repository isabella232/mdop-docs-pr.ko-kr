---
title: MBAM 2.5 서버 배포 계획
description: MBAM 2.5 서버 배포 계획
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826213"
---
# <span data-ttu-id="85937-103">MBAM 2.5 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="85937-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="85937-104">이 항목에서는 MBAM 독립 실행형 및 구성 관리자 토폴로지에 대해 배포 하는 기능을 나열 하 고 배포 해야 하는 순서를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="85937-105">각 토폴로지에 대해 권장 되는 구성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85937-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="85937-106">그러나 확장 요구 사항에 따라 다양 한 구성 및 여러 서버에서 MBAM 서버 데이터베이스 및 기능을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85937-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="85937-107">두 토폴로지에 대 한 중요 한 계획 고려 사항</span><span class="sxs-lookup"><span data-stu-id="85937-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="85937-108">고려 사항</span><span class="sxs-lookup"><span data-stu-id="85937-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="85937-109">세부 정보 또는 목적</span><span class="sxs-lookup"><span data-stu-id="85937-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85937-110">배포를 시작 하기 전에 다음을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="85937-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="85937-111">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="85937-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="85937-112">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="85937-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="85937-113">각 MBAM 기능에는 MBAM 설치를 시작 하기 전에 충족 해야 하는 특정 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85937-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85937-114">MBAM의 BitLocker 복구 키는 한 번 사용 후 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85937-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="85937-115">단일 사용은 관리 및 모니터링 웹 사이트 (헬프 데스크 라고도 함), 셀프 서비스 포털 또는 <strong> MbamBitLockerRecoveryKey Windows PowerShell cmdlet을 사용 하 여 복구 키가 검색 되었음을 의미 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="85937-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85937-116">각 기능을 구성 하는 컴퓨터의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="85937-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="85937-117">이 정보는 구성 프로세스 전체에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="85937-118"><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">이 용도로 mbam 2.5 배포 검사 목록을 사용할 수 있습니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="85937-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85937-119">MDOP (BitLocker Management) 노드에서 그룹 정책 설정만 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="85937-120">BitLocker 드라이브 암호화 노드에서 그룹 정책 설정을 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="85937-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="85937-121">BitLocker 드라이브 암호화 노드에서 그룹 정책 설정을 변경 하는 경우 MBAM이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85937-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="85937-122">MBAM 서버 배포 계획-독립 실행형 토폴로지</span><span class="sxs-lookup"><span data-stu-id="85937-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="85937-123">독립 실행형 토폴로지의 경우 프로덕션 환경에는 두 대의 서버 구성을 사용 하는 것이 좋지만,이는 3 ~ 4 개 서버의 구성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85937-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="85937-124">MBAM 독립 실행형 토폴로지의 서버 인프라에는 다음 기능이 포함 되어 있으며 나열 된 순서 대로 구성 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="85937-125">데이터베이스 (준수 및 감사 데이터베이스 및 복구 데이터베이스)</span><span class="sxs-lookup"><span data-stu-id="85937-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="85937-126">보고</span><span class="sxs-lookup"><span data-stu-id="85937-126">Reports</span></span>

3.  <span data-ttu-id="85937-127">웹 응용 프로그램 및 해당 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="85937-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="85937-128">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="85937-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="85937-129">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="85937-129">Self-Service Portal</span></span>

<span data-ttu-id="85937-130">이러한 기능에 대 한 설명은 [독립 실행형 토폴로지와 함께 MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85937-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="85937-131">MBAM 서버 배포 계획 – 구성 관리자 토폴로지</span><span class="sxs-lookup"><span data-stu-id="85937-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="85937-132">구성 관리자 통합 토폴로지의 경우 추가 서버 구성을 사용할 수 있지만 프로덕션 환경에는 3 서버 구성이 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85937-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="85937-133">MBAM 구성 관리자 토폴로지에 대 한 서버 인프라에는 다음 기능이 포함 되어 있으며, 여기에는 나열 된 순서 대로 구성 하거나 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="85937-134">데이터베이스 (준수 및 감사 데이터베이스 및 복구 데이터베이스)</span><span class="sxs-lookup"><span data-stu-id="85937-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="85937-135">보고</span><span class="sxs-lookup"><span data-stu-id="85937-135">Reports</span></span>

3.  <span data-ttu-id="85937-136">웹 응용 프로그램 및 해당 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="85937-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="85937-137">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="85937-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="85937-138">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="85937-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="85937-139">System Center Configuration Manager 통합</span><span class="sxs-lookup"><span data-stu-id="85937-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="85937-140">이러한 기능에 대 한 설명은 [구성 관리자 통합 토폴로지와 MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85937-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="85937-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="85937-141">Related topics</span></span>


[<span data-ttu-id="85937-142">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="85937-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="85937-143">MBAM 2.5 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="85937-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="85937-144">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="85937-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="85937-145">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="85937-146">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="85937-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





