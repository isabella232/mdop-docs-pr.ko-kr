---
title: 시작 - Configuration Manager를 통해 MBAM 사용
description: 시작 - Configuration Manager를 통해 MBAM 사용
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825168"
---
# <span data-ttu-id="c41a2-103">시작 - Configuration Manager를 통해 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="c41a2-103">Getting Started - Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="c41a2-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하는 경우 구성 관리자 2007 또는 SystemCenter2012 ConfigurationManager와 MBAM을 통합 하는 토폴로지를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose a topology that integrates MBAM with Configuration Manager 2007 or SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="c41a2-105">Mbam에서 지원 되는 구성 관리자의 목록은 [구성 관리자로 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c41a2-105">For a list of the supported versions of Configuration Manager that MBAM supports, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span> <span data-ttu-id="c41a2-106">통합 토폴로지에서는 하드웨어 준수 및 보고 기능이 MBAM에서 제거 되 고 Configuration Manager에서 액세스 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-106">In the integrated topology, the hardware compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

<span data-ttu-id="c41a2-107">**중요**  Windows To Go는 구성 관리자 2007와 함께 MBAM의 통합 토폴로지를 설치 하는 경우 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-107">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="c41a2-108">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="c41a2-108">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="c41a2-109">MBAM의 통합은 다음 섹션에서 자세히 설명 하는 구성 관리자 2007 또는 SystemCenter2012 ConfigurationManager에 다음 세 항목을 설치 하는 새 구성 팩을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-109">The integration of MBAM is based on a new Configuration Pack that installs the following three items into Configuration Manager 2007 or SystemCenter2012 ConfigurationManager, which are described in detail in the following sections:</span></span>

<span data-ttu-id="c41a2-110">구성 항목 및 구성 기준으로 구성 된 구성 데이터</span><span class="sxs-lookup"><span data-stu-id="c41a2-110">Configuration data that consists of configuration items and a configuration baseline</span></span>

<span data-ttu-id="c41a2-111">컬렉션</span><span class="sxs-lookup"><span data-stu-id="c41a2-111">Collection</span></span>

<span data-ttu-id="c41a2-112">보고</span><span class="sxs-lookup"><span data-stu-id="c41a2-112">Reports</span></span>

### <span data-ttu-id="c41a2-113">구성 데이터</span><span class="sxs-lookup"><span data-stu-id="c41a2-113">Configuration Data</span></span>

<span data-ttu-id="c41a2-114">구성 데이터를 통해 "bitlocker 보호" 라고 하는 구성 기준을 설치 하는데, 여기에는 "BitLocker 운영 체제 드라이브 보호" 및 "BitLocker 고정 데이터 드라이브 보호"의 두 가지 구성 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-114">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items: “BitLocker Operating System Drive Protection” and “BitLocker Fixed Data Drives Protection.”</span></span> <span data-ttu-id="c41a2-115">구성 기준은 컬렉션에 배포 되며,이는 MBAM이 설치 되어 있는 경우에도 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-115">The configuration baseline is deployed to the collection, which is also created when MBAM is installed.</span></span> <span data-ttu-id="c41a2-116">두 개의 구성 항목은 클라이언트 컴퓨터의 준수 상태를 평가 하기 위한 기반을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-116">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="c41a2-117">이 정보는 구성 관리자에서 캡처, 저장 및 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-117">This information is captured, stored, and evaluated in Configuration Manager.</span></span> <span data-ttu-id="c41a2-118">구성 항목은 os (운영 체제 드라이브) 및 FDDs (탑재형 Data Drives)에 대 한 규정 준수 요구 사항에 기반을 둔 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-118">The configuration items are based on the compliance requirements for operating system drives (OSDs) and Fixed Data Drives (FDDs).</span></span> <span data-ttu-id="c41a2-119">이러한 드라이브 유형에 대 한 준수를 평가할 수 있도록 배포 된 컴퓨터에 대 한 필수 세부 정보가 수집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-119">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span> <span data-ttu-id="c41a2-120">기본적으로 구성 기준은 12 시간 마다 준수 상태를 평가 하 고 규정 준수 데이터를 구성 관리자에 게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-120">By default, the configuration baseline evaluates the compliance status every 12 hours and sends the compliance data to Configuration Manager.</span></span>

### <span data-ttu-id="c41a2-121">컬렉션</span><span class="sxs-lookup"><span data-stu-id="c41a2-121">Collection</span></span>

<span data-ttu-id="c41a2-122">MBAM 지원 컴퓨터 라고 하는 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-122">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="c41a2-123">구성 기준은이 컬렉션에 있는 클라이언트 컴퓨터를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-123">The configuration baseline is targeted to client computers that are in this collection.</span></span> <span data-ttu-id="c41a2-124">기본적으로 12 시간 마다 실행 되며 구성원 자격을 평가 하는 동적 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-124">This is a dynamic collection that, by default, runs every 12 hours and evaluates membership.</span></span> <span data-ttu-id="c41a2-125">구성원 자격은 다음 세 가지 조건을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-125">Membership is based on three criteria:</span></span>

-   <span data-ttu-id="c41a2-126">지원 되는 버전의 Windows 운영 체제입니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-126">It is a supported version of the Windows operating system.</span></span> <span data-ttu-id="c41a2-127">현재 MBAM은 windows 365 enterprise 및 windows 365 to go를 지원 합니다. windows를 Go 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-127">Currently, MBAM supports only Windows 7 Enterprise and Windows 7 Ultimate, Windows 8 Enterprise, and Windows To Go, when Windows To Go is running on Windows 8 Enterprise.</span></span>

-   <span data-ttu-id="c41a2-128">물리적 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-128">It is a physical computer.</span></span> <span data-ttu-id="c41a2-129">가상 머신은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-129">Virtual machines are not supported.</span></span>

-   <span data-ttu-id="c41a2-130">TPM (신뢰할 수 있는 플랫폼 모듈)을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-130">Trusted Platform Module (TPM) is available.</span></span> <span data-ttu-id="c41a2-131">Windows 7에는 호환 가능한 TPM 1.2 이상 버전이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-131">A compatible version of TPM 1.2 or later is required for Windows 7.</span></span> <span data-ttu-id="c41a2-132">Windows 8 및 Windows To Go에는 TPM이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-132">Windows 8 and Windows To Go do not require a TPM.</span></span>

<span data-ttu-id="c41a2-133">컬렉션은 모든 컴퓨터에 대해 평가 되며 정책 준수 평가와 MBAM 통합에 대 한 보고를 위한 기반을 제공 하는 호환 컴퓨터의 하위 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-133">The collection is evaluated against all computers and creates the subset of compatible computers that provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span>

### <span data-ttu-id="c41a2-134">보고</span><span class="sxs-lookup"><span data-stu-id="c41a2-134">Reports</span></span>

<span data-ttu-id="c41a2-135">준수를 보는 데 사용할 수 있는 네 개의 보고서가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-135">There are four reports that you can use to view compliance.</span></span> <span data-ttu-id="c41a2-136">채널은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-136">They are:</span></span>

-   <span data-ttu-id="c41a2-137">**BitLocker 엔터프라이즈 준수 대시보드** -단일 보고서에 대 한 정보 보기 (준수 상태 배포, 비규격 – 오류 발생), 드라이브 유형별 준수 상태 배포 등의 세 가지 다양 한 보고 정보가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-137">**BitLocker Enterprise Compliance Dashboard** – gives IT administrators three different views of information on a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="c41a2-138">보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-138">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the state that you select.</span></span>

-   <span data-ttu-id="c41a2-139">**Bitlocker 엔터프라이즈 준수 세부 정보** – IT 관리자가 엔터프라이즈의 BitLocker 암호화 준수 상태에 대 한 정보를 보고 각 컴퓨터의 준수 상태를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-139">**BitLocker Enterprise Compliance Details** – lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="c41a2-140">보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-140">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the state that you select.</span></span>

-   <span data-ttu-id="c41a2-141">**BitLocker 컴퓨터 준수** – it 관리자가 개별 컴퓨터를 보고 특정 상태의 준수 여부 또는 비규격에 대해 보고 된 이유를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-141">**BitLocker Computer Compliance** – lets IT administrators view an individual computer and determine why it was reported with a given status of compliant or not compliant.</span></span> <span data-ttu-id="c41a2-142">또한이 보고서에는 OSD (운영 체제 드라이브) 및 FDDs (고정식 data drives)의 암호화 상태도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-142">The report also displays the encryption state of the operating system drives (OSD) and fixed data drives (FDDs).</span></span>

-   <span data-ttu-id="c41a2-143">**BitLocker Enterprise 준수 요약** -IT 관리자는 mbam 정책을 사용 하 여 엔터프라이즈의 규정 준수 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-143">**BitLocker Enterprise Compliance Summary** – lets IT administrators view the status of the compliance of the enterprise with MBAM policy.</span></span> <span data-ttu-id="c41a2-144">각 컴퓨터의 상태가 평가 되며,이 보고서에는 정책에 대 한 엔터프라이즈의 모든 컴퓨터 준수에 대 한 요약이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-144">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="c41a2-145">보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-145">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the state that you select.</span></span>

## <span data-ttu-id="c41a2-146">구성 관리자와 함께 MBAM의 상위 수준 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c41a2-146">High-Level Architecture of MBAM with Configuration Manager</span></span>


<span data-ttu-id="c41a2-147">다음 이미지는 구성 관리자 토폴로지와 함께 MBAM 아키텍처를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-147">The following image shows the MBAM architecture with the Configuration Manager topology.</span></span> <span data-ttu-id="c41a2-148">이 구성은 프로덕션 환경에서 최대 20만 MBAM 클라이언트를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-148">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span>

![구성 관리자를 사용 하 여 mbam 아키텍처](images/mbam2-cmserver.gif)

<span data-ttu-id="c41a2-150">이 아키텍처의 서버, 데이터베이스 및 기능에 대 한 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-150">A description of the servers, databases, and features of this architecture follows.</span></span> <span data-ttu-id="c41a2-151">아키텍처 이미지의 서버 기능 및 데이터베이스는 설치 하는 것이 좋습니다. 컴퓨터 또는 서버 아래에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-151">The server features and databases in the architecture image are listed under the computer or server where we recommend that you install them.</span></span>

-   <span data-ttu-id="c41a2-152">**데이터베이스 서버** – **복구 데이터베이스**, **감사 데이터베이스**및 **감사 보고서** 가 Windows Server 및 지원 되는 SQLServer 인스턴스에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-152">**Database Server** – The **Recovery Database**, **Audit Database**, and **Audit Reports** are installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="c41a2-153">복구 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-153">The Recovery database stores recovery data that is collected from MBAM client computers.</span></span> <span data-ttu-id="c41a2-154">감사 데이터베이스는 복구 데이터에 액세스 한 클라이언트 컴퓨터에서 수집 된 감사 활동 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-154">The Audit Database stores audit activity data that is collected from client computers that have accessed recovery data.</span></span> <span data-ttu-id="c41a2-155">감사 보고서는 엔터프라이즈에서 클라이언트 컴퓨터의 준수 상태에 대 한 데이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-155">The Audit Reports provide data about the compliance status of client computers in your enterprise.</span></span>

-   <span data-ttu-id="c41a2-156">Configuration **Manager 주 사이트 서버** – Configuration manager 서버에 System Center Configuration manager 통합 토폴로지와 함께 mbam 서버 설치가 포함 되어 있으며,이는 configuration manager 기본 사이트 서버에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-156">**Configuration Manager Primary Site Server** – The Configuration Manager Server contains of the MBAM server installation with the System Center Configuration Manager Integration topology, which must be installed on a Configuration Manager primary site server.</span></span> <span data-ttu-id="c41a2-157">Configuration Manager 서버는 클라이언트 컴퓨터에서 하드웨어 인벤터리 정보를 수집 하 고 클라이언트 컴퓨터의 BitLocker 규격을 보고 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-157">The Configuration Manager Server collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span> <span data-ttu-id="c41a2-158">MBAM 설정 서버 설치를 실행 하면 컬렉션 및 구성 데이터가 Configuration Manager 기본 사이트 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-158">When you run the MBAM Setup server installation, a collection and the configuration data are installed on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="c41a2-159">**관리** 및 모니터링 서버- **관리 및 모니터링 서버** 는 Windows Server에 설치 되며 관리 및 모니터링 웹 사이트와 모니터링 웹 서비스로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-159">**Administration and Monitoring Server** - The **Administration and Monitoring Server** is installed on a Windows server and consists of the Administration and Monitoring website and the monitoring web services.</span></span> <span data-ttu-id="c41a2-160">관리 및 모니터링 웹 사이트는 활동을 감사 하 고 복구 데이터 (예: BitLocker 복구 키)에 액세스 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-160">The Administration and Monitoring website is used to audit activity and to access recovery data (for example, BitLocker recovery keys).</span></span> <span data-ttu-id="c41a2-161">**셀프 서비스 포털** 도 관리 및 모니터링 서버에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-161">The **Self-Service Portal** is also installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="c41a2-162">포털을 사용 하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그인 하 여 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-162">The Portal enables end users on client computers to independently log onto a website to get a recovery key if they lose or forget their BitLocker password.</span></span> <span data-ttu-id="c41a2-163">감사 보고서는 관리 및 모니터링 서버에도 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-163">The Audit reports are also installed on the Administration and Monitoring Server.</span></span>

-   <span data-ttu-id="c41a2-164">**관리 워크스테이션** - **정책 템플릿은** BitLocker 드라이브 암호화에 대 한 mbam 구현 설정을 정의 하는 그룹 정책 개체로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-164">**Management Workstation** - The **Policy Template** consists of Group Policy Objects that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="c41a2-165">모든 서버 또는 워크스테이션에 정책 템플릿을 설치할 수 있지만, 일반적으로 지원 되는 Windows server 또는 클라이언트 컴퓨터인 관리 워크스테이션에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-165">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation that is a supported Windows server or client computer.</span></span> <span data-ttu-id="c41a2-166">워크스테이션이 전용 컴퓨터 일 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-166">The workstation does not have to be a dedicated computer.</span></span>

-   <span data-ttu-id="c41a2-167">**Mbam 클라이언트** 및 **Configuration Manager 클라이언트** 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="c41a2-167">**MBAM Client** and **Configuration Manager Client** computer</span></span>

    -   <span data-ttu-id="c41a2-168">**Mbam 클라이언트** 는 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-168">The **MBAM Client** performs the following tasks:</span></span>

        -   <span data-ttu-id="c41a2-169">그룹 정책 개체를 사용 하 여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-169">Uses Group Policy Objects to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

        -   <span data-ttu-id="c41a2-170">세 가지 BitLocker 데이터 드라이브 유형 (운영 체제 드라이브, 고정 데이터 드라이브, 이동식 데이터 (USB) 드라이브)에 대 한 복구 키를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-170">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

        -   <span data-ttu-id="c41a2-171">클라이언트 컴퓨터에 대 한 복구 정보 및 컴퓨터 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-171">Collects recovery information and computer information about the client computers.</span></span>

    -   <span data-ttu-id="c41a2-172">Configuration manager **클라이언트** – configuration manager 클라이언트를 사용 하 여 클라이언트 컴퓨터에 대 한 하드웨어 호환성 데이터를 수집 하 고 구성 관리자가 준수 정보를 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41a2-172">**Configuration Manager Client** – The Configuration Manager client enables Configuration Manager to collect hardware compatibility data about the client computers, and enables Configuration Manager to report compliance information.</span></span>

## <span data-ttu-id="c41a2-173">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c41a2-173">Related topics</span></span>


[<span data-ttu-id="c41a2-174">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="c41a2-174">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





