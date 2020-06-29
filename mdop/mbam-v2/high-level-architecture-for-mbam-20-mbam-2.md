---
title: MBAM 2.0의 개략적인 아키텍처
description: MBAM 2.0의 개략적인 아키텍처
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824703"
---
# <span data-ttu-id="97e02-103">MBAM 2.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="97e02-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="97e02-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 프로비저닝 및 배포를 간소화 하 고, BitLocker에서 준수 및 보고 기능을 개선 하 고, 지원 비용을 줄이는 데 도움이 되는 클라이언트/서버 솔루션입니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="97e02-105">Microsoft BitLocker 관리 및 모니터링에는이 항목에서 설명 하는 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="97e02-106">Microsoft BitLocker 관리 및 모니터링은 독립 실행형 토폴로지에서 또는 Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager와 통합 된 토폴로지에서 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="97e02-107">이 항목에서는 독립 실행형 토폴로지의 아키텍처에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="97e02-108">통합 된 구성 관리자 토폴로지에 배포 하는 방법에 대 한 자세한 내용은 [구성 관리자에서 MBAM 사용](using-mbam-with-configuration-manager.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97e02-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="97e02-109">다음 다이어그램에는 두 개의 서버와 관리 워크스테이션으로 구성 되는 프로덕션 환경의 MBAM 권장 아키텍처가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="97e02-110">이 아키텍처는 최대 20만 MBAM 클라이언트를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="97e02-111">아키텍처 이미지의 서버 기능 및 데이터베이스는 다음 섹션에 설명 되어 있으며, 설치 하는 것이 좋습니다. 컴퓨터 또는 서버 아래에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="97e02-112">**참고**  단일 서버 아키텍처는 테스트 환경 에서만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![mbam 2 2-서버 배포 토폴로지](images/mbam2-3-servers.gif)

## <span data-ttu-id="97e02-114">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="97e02-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="97e02-115">다음 기능이이 서버에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="97e02-116">**관리 및 모니터링 서버**.</span><span class="sxs-lookup"><span data-stu-id="97e02-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="97e02-117">관리 및 모니터링 서버 기능은 Windows Server에 설치 되어 있으며 보고서 및 지원 센터 포털, 모니터링 웹 서비스를 포함 하는 관리 및 모니터링 웹 사이트로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="97e02-118">**셀프 서비스 포털**.</span><span class="sxs-lookup"><span data-stu-id="97e02-118">**Self-Service Portal**.</span></span> <span data-ttu-id="97e02-119">셀프 서비스 포털이 Windows server에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="97e02-120">셀프 서비스 포털을 사용 하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그온 할 수 있으며, 여기에서 잠금 BitLocker 볼륨을 복구 하는 데 복구 키를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="97e02-121">데이터베이스 서버</span><span class="sxs-lookup"><span data-stu-id="97e02-121">Database Server</span></span>


<span data-ttu-id="97e02-122">다음 기능이이 서버에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="97e02-123">**복구 데이터베이스**.</span><span class="sxs-lookup"><span data-stu-id="97e02-123">**Recovery Database**.</span></span> <span data-ttu-id="97e02-124">복구 데이터베이스는 Windows server와 Microsoft SQLServer의 지원 되는 인스턴스에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="97e02-125">이 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="97e02-126">**준수 및 감사 데이터베이스**.</span><span class="sxs-lookup"><span data-stu-id="97e02-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="97e02-127">준수 및 감사 데이터베이스는 Windows server와 SQLServer의 지원 되는 인스턴스에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="97e02-128">이 데이터베이스는 MBAM 클라이언트 컴퓨터에 대 한 규정 준수 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="97e02-129">이 데이터는 주로 SQL Server Reporting Services (SSRS) 호스트가 보고 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="97e02-130">**준수 및 감사 보고서**.</span><span class="sxs-lookup"><span data-stu-id="97e02-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="97e02-131">규정 준수 및 감사 보고서는 Windows server에 설치 되어 있으며, SQL Server Reporting Services (SSRS) 기능이 설치 된 SQLServer의 지원 되는 인스턴스에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="97e02-132">이러한 보고서는 관리 및 모니터링 웹 사이트에서 또는 SSRS 서버에서 직접 액세스할 수 있는 MBAM 보고서를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="97e02-133">관리 워크스테이션</span><span class="sxs-lookup"><span data-stu-id="97e02-133">Management Workstation</span></span>


<span data-ttu-id="97e02-134">다음 기능은 Windows server 또는 클라이언트 컴퓨터 일 수 있는 관리 워크스테이션에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="97e02-135">**정책 서식 파일**.</span><span class="sxs-lookup"><span data-stu-id="97e02-135">**Policy Template**.</span></span> <span data-ttu-id="97e02-136">정책 템플릿은 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="97e02-137">모든 서버 또는 워크스테이션에 정책 템플릿을 설치할 수 있지만, 일반적으로 지원 되는 Windows server 또는 클라이언트 컴퓨터인 관리 워크스테이션에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="97e02-138">워크스테이션이 전용 컴퓨터 일 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="97e02-139">MBAM 클라이언트</span><span class="sxs-lookup"><span data-stu-id="97e02-139">MBAM Client</span></span>


<span data-ttu-id="97e02-140">MBAM 클라이언트는 Windows 컴퓨터에 설치 되어 있으며 다음과 같은 특징이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="97e02-141">그룹 정책을 사용 하 여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 드라이브 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="97e02-142">세 가지 BitLocker 데이터 드라이브 유형 (운영 체제 드라이브, 고정 데이터 드라이브, 이동식 데이터 (USB) 드라이브)에 대 한 복구 키를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="97e02-143">컴퓨터에 대 한 규정 준수 데이터를 수집 하 고 보고 시스템으로 데이터를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e02-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="97e02-144">관련 항목</span><span class="sxs-lookup"><span data-stu-id="97e02-144">Related topics</span></span>


[<span data-ttu-id="97e02-145">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="97e02-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





