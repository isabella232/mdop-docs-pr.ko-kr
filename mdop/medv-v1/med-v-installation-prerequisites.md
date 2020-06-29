---
title: MED-V 설치 필수 구성 요소
description: MED-V 설치 필수 구성 요소
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824968"
---
# <span data-ttu-id="bc727-103">MED-V 설치 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="bc727-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="bc727-104">MED-V를 설치 하기 위한 전제 조건은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="bc727-105">Active Directory 요구 사항</span><span class="sxs-lookup"><span data-stu-id="bc727-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="bc727-106">보고서 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="bc727-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="bc727-107">바이러스 백신/백업 소프트웨어 구성</span><span class="sxs-lookup"><span data-stu-id="bc727-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="bc727-108">Microsoft Virtual PC 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="bc727-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="bc727-109">Active Directory 요구 사항</span><span class="sxs-lookup"><span data-stu-id="bc727-109">Active Directory Requirements</span></span>


<span data-ttu-id="bc727-110">MED-V 서버를 구성할 때 사용자가 서버가 속한 도메인의 일부가 아닌 경우 도메인 간에 신뢰를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="bc727-111">보고서 데이터베이스를 설치 하는 방법</span><span class="sxs-lookup"><span data-stu-id="bc727-111">How to Install the Report Database</span></span>


<span data-ttu-id="bc727-112">모든 MED-V 작업 영역 로그를 저장 하려면 보고서 데이터베이스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="bc727-113">로그 데이터베이스는 MED-V 보고서를 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="bc727-114">보고서에 대 한 자세한 내용은 [Med-v 보고](med-v-reporting.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="bc727-115">SQL Server는 MED-V 서버와 같은 서버나 원격 서버에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="bc727-116">원격 서버에 설치 하는 경우 [원격 서버에 SQL Server 설치](#bkmk-installingsqlserveronaremoteserver)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="bc727-117">원격 서버에 SQL Server 설치</span><span class="sxs-lookup"><span data-stu-id="bc727-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="bc727-118">원격 서버에 SQL Server를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="bc727-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="bc727-119">원격 서버에서 다음을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="bc727-120">인스턴스 이름-기본 인스턴스</span><span class="sxs-lookup"><span data-stu-id="bc727-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="bc727-121">인증 모드-혼합 모드</span><span class="sxs-lookup"><span data-stu-id="bc727-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="bc727-122">사용자 — 기본적으로 생성 되는 사용자는 "sa"입니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="bc727-123">비밀 번호-원하는 비밀 번호</span><span class="sxs-lookup"><span data-stu-id="bc727-123">Password—Desired password</span></span>

    -   <span data-ttu-id="bc727-124">데이터 정렬 설정-기본값</span><span class="sxs-lookup"><span data-stu-id="bc727-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="bc727-125">사용 현황 보고서 설정 오류-기본값</span><span class="sxs-lookup"><span data-stu-id="bc727-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="bc727-126">MED-V 서버에 다음 파일을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="bc727-127">Microsoft SQL Server2008 용 관리 팩 개체 컬렉션에 대 한 필수 구성 요소를 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server2008 네이티브 클라이언트](https://go.microsoft.com/fwlink/?LinkId=164039) 를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bc727-128">Microsoft SQL Server2005 용 관리 팩 개체 컬렉션에 대 한 필수 구성 요소를 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server2005 네이티브 클라이언트](https://go.microsoft.com/fwlink/?LinkId=164038) 를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bc727-129">Microsoft SQL Server2008에 필요한 dll 파일을 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server 2008 Management Objects 컬렉션](https://go.microsoft.com/fwlink/?LinkId=164041) 을 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bc727-130">Microsoft SQL Server2005에 필요한 dll 파일을 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server2005 Management 개체](https://go.microsoft.com/fwlink/?LinkId=164040) 를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bc727-131">SQL Server2008에 대 한 추가 값을 제공 하는 독립 실행형 설치 패키지를 설치 하려면 Microsoft 다운로드 센터에서 [MICROSOFT SQL Server2008 기능 팩](https://go.microsoft.com/fwlink/?LinkId=163960) 을 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="bc727-132">SQL Server2005에 대 한 추가 값을 제공 하는 독립 실행형 설치 패키지를 설치 하려면 Microsoft 다운로드 센터에서 [MICROSOFT SQL Server2005의 기능 팩]( https://go.microsoft.com/fwlink/?LinkId=163961) 을 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="bc727-133">이러한 파일에 대 한 자세한 내용은 microsoft 다운로드 센터에서 microsoft [Sql Server2008 기능 팩](https://go.microsoft.com/fwlink/?LinkId=163960) (또는 Microsoft https://go.microsoft.com/fwlink/?LinkId=163960) 다운로드 센터의 [microsoft sql Server2005에 대 한 기능 팩](https://go.microsoft.com/fwlink/?LinkId=163961) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="bc727-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="bc727-134">바이러스 백신/백업 소프트웨어 구성</span><span class="sxs-lookup"><span data-stu-id="bc727-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="bc727-135">바이러스 백신 활동이 가상 데스크톱의 성능에 영향을 주지 않도록 하려면 호스트에서 실행 되는 바이러스 백신 또는 백업 처리에서 다음 가상 머신 파일 형식을 제외 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="bc727-136">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="bc727-136">\*.VMC</span></span>

-   <span data-ttu-id="bc727-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="bc727-137">\*.VUD</span></span>

-   <span data-ttu-id="bc727-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="bc727-138">\*.VSV</span></span>

-   <span data-ttu-id="bc727-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="bc727-139">\*.CKM</span></span>

-   <span data-ttu-id="bc727-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="bc727-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="bc727-141">Microsoft Virtual PC2007 SP1을 설치 하 고 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="bc727-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="bc727-142">**중요**  Windows 용 가상 PC가 호스트 컴퓨터에 있는 경우 Virtual PC2007 SP1을 설치 하기 전에 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="bc727-143">Microsoft Virtual PC2007 SP1을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="bc727-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="bc727-144">Microsoft 다운로드 센터 [가상 PC 2007 sp1](https://go.microsoft.com/fwlink/?LinkId=142994)에서 VIRTUAL PC2007 SP1을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="bc727-145">호스트 컴퓨터에서 설치 파일을 실행 하 고 마법사의 지시를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="bc727-146">관리자 모드의 호스트 컴퓨터에 Virtual PC2007 SP1 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="bc727-147">자세한 내용은 [가상 PC 2007 SP1의 핫픽스 패키지](https://go.microsoft.com/fwlink/?LinkId=150575)에 대 한 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc727-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="bc727-148">**참고**  Virtual PC2007 SP1을 실행 하려면 Virtual PC2007 SP1 업데이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc727-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="bc727-149">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bc727-149">Related topics</span></span>


[<span data-ttu-id="bc727-150">지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="bc727-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





