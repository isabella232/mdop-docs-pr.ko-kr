---
title: MBAM 2.0 SP1 정보
description: MBAM 2.0 SP1 정보
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823553"
---
# <span data-ttu-id="1f4f0-103">MBAM 2.0 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="1f4f0-103">About MBAM 2.0 SP1</span></span>

<span data-ttu-id="1f4f0-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)의 변경 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-104">This topic describes the changes in Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="1f4f0-105">MBAM에 대 한 일반적인 설명은 [mbam 2.0 시작](getting-started-with-mbam-20-mbam-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-105">For a general description of MBAM, see [Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md).</span></span>

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a><span data-ttu-id="1f4f0-106">MBAM 2.0 SP1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-106">What’s new in MBAM 2.0 SP1</span></span>

<span data-ttu-id="1f4f0-107">이 MBAM 버전은 다음과 같은 새로운 기능과 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-107">This version of MBAM provides the following new features and functionality.</span></span>

### <span data-ttu-id="1f4f0-108">Windows 8.1, Windows Server 2012 R2 및 System Center 2012 R2 구성 관리자에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="1f4f0-108">Support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager</span></span>

<span data-ttu-id="1f4f0-109">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)은 Windows 8.1, Windows Server 2012 R2 및 System Center 2012 R2 구성 관리자에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager.</span></span>

### <span data-ttu-id="1f4f0-110">Microsoft SQL Server 2008 R2 SP2에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="1f4f0-110">Support for Microsoft SQL Server 2008 R2 SP2</span></span>

<span data-ttu-id="1f4f0-111">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 서비스 팩 1(sp1)은 Microsoft SQL Server 2008 R2 SP2에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Microsoft SQL Server 2008 R2 SP2.</span></span> <span data-ttu-id="1f4f0-112">Microsoft System Center Configuration Manager 2007 R2를 실행 하는 경우 Microsoft SQL Server 2008 R2 이상을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-112">You must use Microsoft SQL Server 2008 R2 or higher if you are running Microsoft System Center Configuration Manager 2007 R2.</span></span>

### <span data-ttu-id="1f4f0-113">고객 의견 롤업</span><span class="sxs-lookup"><span data-stu-id="1f4f0-113">Customer feedback rollup</span></span>

<span data-ttu-id="1f4f0-114">MBAM 2.0 SP1에는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 출시 이후 발견 된 문제를 해결 하기 위한 해결 방법에 대 한 롤업을 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-114">MBAM 2.0 SP1 includes a rollup of fixes to address issues that were found since the Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 release.</span></span> <span data-ttu-id="1f4f0-115">이러한 변경 사항으로 인해 Microsoft System Center Configuration Manager 2007에서 MBAM을 실행 하면 컴퓨터 이름 필드가 BitLocker 컴퓨터 준수 및 BitLocker 엔터프라이즈 준수 세부 정보 보고서에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-115">As part of these changes, the Computer Name field now appears in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007.</span></span>

### <span data-ttu-id="1f4f0-116">셀프 서비스 포털의 포트와 관리 및 모니터링 웹 사이트에 대 한 방화벽 예외를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-116">Firewall exception must be set on ports for the Self-Service Portal and the Administration and Monitoring website</span></span>

<span data-ttu-id="1f4f0-117">셀프 서비스 포털 및 관리 및 모니터링 웹 사이트를 구성 하는 경우 지정 된 포트를 통해 통신을 사용 하도록 방화벽 예외를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-117">When you configure the Self-Service Portal and the Administration and Monitoring website, you must set a firewall exception to enable communication through the specified ports.</span></span> <span data-ttu-id="1f4f0-118">이전에는 MBAM 서버 설치가 Windows 방화벽에서 자동으로 포트를 열었습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-118">Previously, the MBAM server installation opened the ports automatically in Windows Firewall.</span></span>

### <span data-ttu-id="1f4f0-119">Configuration Manager에서 MBAM 보고서의 위치가 변경 됨</span><span class="sxs-lookup"><span data-stu-id="1f4f0-119">Location of MBAM reports has changed in Configuration Manager</span></span>

<span data-ttu-id="1f4f0-120">이제 MBAM 노드 내의 하위 폴더에서 Configuration Manager 통합 토폴로지에 대 한 MBAM 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-120">MBAM reports for the Configuration Manager integrated topology are now available under subfolders within the MBAM node.</span></span> <span data-ttu-id="1f4f0-121">하위 폴더 이름은 하위 폴더 내의 보고서 언어를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-121">The subfolder names represent the language of the reports within the subfolder.</span></span>

### <span data-ttu-id="1f4f0-122">Configuration Manager에서 MBAM을 설치할 때 기본 사이트 서버에 MBAM을 설치할 수 있는 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-122">Ability to install MBAM on a primary site server when you install MBAM with Configuration Manager</span></span>

<span data-ttu-id="1f4f0-123">Configuration Manager 통합 토폴로지로 MBAM을 설치할 때 기본 사이트 서버나 중앙 관리 사이트 서버에 MBAM을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-123">You can install MBAM on a primary site server or a central administration site server when you install MBAM with the Configuration Manager integrated topology.</span></span> <span data-ttu-id="1f4f0-124">이전에는 중앙 관리 사이트 서버에 MBAM을 설치 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-124">Previously, you were required to install MBAM on a central administration site server.</span></span>

**<span data-ttu-id="1f4f0-125">중요</span><span class="sxs-lookup"><span data-stu-id="1f4f0-125">Important</span></span>**  
<span data-ttu-id="1f4f0-126">MBAM을 설치 하는 서버는 계층 구조의 최상위 계층 서버 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-126">The server on which you install MBAM must be the top-tier server in your hierarchy.</span></span>



<span data-ttu-id="1f4f0-127">MBAM 설치는 다음과 같이 Microsoft System Center Configuration Manager 2007 및 Microsoft System Center 2012 Configuration Manager에 대해 다르게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-127">The MBAM installation works differently for Microsoft System Center Configuration Manager 2007 and Microsoft System Center 2012 Configuration Manager as follows:</span></span>

-   <span data-ttu-id="1f4f0-128">**구성 관리자 2007** : 크기가 더 크고, 중앙 사이트 상위 서버가 있는 주 사이트 서버에 mbam을 설치 하는 경우, mbam은 중앙 사이트 상위 서버를 확인 하 고 해당 상위 서버의 모든 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-128">**Configuration Manager 2007** : If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy and has a central site parent server, MBAM resolves the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="1f4f0-129">설치 작업에는 필수 조건을 확인 하 고 Configuration Manager 개체 및 보고서를 설치 하는 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-129">The installation actions include checking prerequisites and installing the Configuration Manager objects and reports.</span></span> <span data-ttu-id="1f4f0-130">예를 들어, 중앙 사이트 상위 서버의 자식인 주 사이트 서버에 MBAM을 설치 하는 경우 MBAM은 상위 서버에 모든 Configuration Manager 개체와 보고서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-130">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="1f4f0-131">부모 서버에 MBAM을 설치 하는 경우 MBAM은 해당 상위 서버의 모든 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-131">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span>

-   <span data-ttu-id="1f4f0-132">**System Center 2012 구성 관리자** : 주 사이트 서버나 중앙 관리 서버에 mbam을 설치 하는 경우 mbam은 해당 사이트 서버에서 모든 설치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-132">**System Center 2012 Configuration Manager** : If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span>

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> <span data-ttu-id="1f4f0-133">MBAM 서버를 설치 하는 컴퓨터에 Configuration Manager 콘솔을 설치 해야 함</span><span class="sxs-lookup"><span data-stu-id="1f4f0-133">Configuration Manager Console must be installed on the computer on which you install the MBAM Server</span></span>

<span data-ttu-id="1f4f0-134">Configuration Manager 통합 토폴로지로 MBAM을 설치 하는 경우 MBAM이 설치 될 컴퓨터에 Configuration Manager 콘솔을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-134">When you install MBAM with the Configuration Manager integrated topology, you must install the Configuration Manager Console on the same computer on which MBAM will be installed.</span></span> <span data-ttu-id="1f4f0-135">[구성 관리자에서 MBAM을 사용 하 여 시작](getting-started---using-mbam-with-configuration-manager.md)하는 데 권장 되는 아키텍처를 사용 하는 경우 Configuration Manager 기본 사이트 서버에 mbam을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-135">If you use the recommended architecture, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), you would install MBAM on the Configuration Manager Primary Site Server.</span></span>

### <span data-ttu-id="1f4f0-136">Configuration Manager 통합 토폴로지의 새 설정 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f4f0-136">New setup command-line parameters for the Configuration Manager integrated topology</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1f4f0-137">명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f4f0-137">Command-Line Parameter</span></span></th>
<th align="left"><span data-ttu-id="1f4f0-138">설명</span><span class="sxs-lookup"><span data-stu-id="1f4f0-138">Description</span></span></th>
<th align="left"><span data-ttu-id="1f4f0-139">예</span><span class="sxs-lookup"><span data-stu-id="1f4f0-139">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f4f0-140">CM_SSRS_REMOTE_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="1f4f0-140">CM_SSRS_REMOTE_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f4f0-141">MBAM이 설치 된 것과 동일한 Configuration Manager 사이트의 일부인 원격 SQL Server Reporting Services (SSRS) 서버에 Configuration Manager 보고서를 설치할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-141">Enables you to install the Configuration Manager reports on a remote SQL Server Reporting Services (SSRS) server that is part of the same Configuration Manager site to which MBAM is installed.</span></span> <span data-ttu-id="1f4f0-142">값을 원격 SSRS 지점간 역할 서버의 정규화 된 도메인 이름으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-142">You can set the value to the fully qualified domain name of the remote SSRS point role server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f4f0-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME ssrsServer =. m a c.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME=ssrsServer.Contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f4f0-144">CM_REPORTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="1f4f0-144">CM_REPORTS_ONLY</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f4f0-145">기준, 컬렉션 및 구성 항목과 같은 다른 Configuration Manager 개체 없이 Configuration Manager 보고서만 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-145">Enables you to install only the Configuration Manager reports, without other Configuration Manager objects, such as the baseline, collection, and configuration items.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1f4f0-146">참고</span><span class="sxs-lookup"><span data-stu-id="1f4f0-146">Note</span></span></strong><br/><p><span data-ttu-id="1f4f0-147">이 매개 변수를 CM_REPORTS_COLLECTION_ID 매개 변수와 결합 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-147">You must combine this parameter with the CM_REPORTS_COLLECTION_ID parameter.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="1f4f0-148">유효한 매개 변수 값:</span><span class="sxs-lookup"><span data-stu-id="1f4f0-148">Valid parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="1f4f0-149">True</span><span class="sxs-lookup"><span data-stu-id="1f4f0-149">True</span></span></p></li>
<li><p><span data-ttu-id="1f4f0-150">False</span><span class="sxs-lookup"><span data-stu-id="1f4f0-150">False</span></span></p></li>
</ul>
<p><span data-ttu-id="1f4f0-151">이 매개 변수를 CM_SSRS_REMOTE_SERVER_NAME 매개 변수와 결합 하 여 원격 SSRS 요점 역할 서버에만 보고서를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-151">You can combine this parameter with the CM_SSRS_REMOTE_SERVER_NAME parameter if you want to install the reports only to a remote SSRS point role server.</span></span></p>
<p><span data-ttu-id="1f4f0-152">매개 변수를 설정 하지 않거나 False로 설정한 경우 MBAM 설정에서는 보고서를 포함 하 여 모든 Configuration Manager 개체를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-152">If you do not set the parameter or if you set it to False, MBAM Setup installs all of the Configuration Manager objects, including the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f4f0-153">MbamSetup.exe CM_REPORTS_ONLY = True</span><span class="sxs-lookup"><span data-stu-id="1f4f0-153">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="1f4f0-154">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="1f4f0-154">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f4f0-155">CM_REPORTS_COLLECTION_ID</span><span class="sxs-lookup"><span data-stu-id="1f4f0-155">CM_REPORTS_COLLECTION_ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f4f0-156">보고 준수 데이터를 표시할 컬렉션을 식별 하는 기존 컬렉션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-156">An existing collection ID that identifies the collection for which reporting compliance data will be displayed.</span></span> <span data-ttu-id="1f4f0-157">모든 컬렉션 ID를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-157">You can specify any collection ID.</span></span> <span data-ttu-id="1f4f0-158">"MBAM 지원 컴퓨터" 컬렉션 ID를 사용할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-158">You are not required to use the “MBAM Supported Computers” collection ID.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f4f0-159">MbamSetup.exe CM_REPORTS_ONLY = True</span><span class="sxs-lookup"><span data-stu-id="1f4f0-159">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="1f4f0-160">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="1f4f0-160">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1f4f0-161">셀프 서비스 포털 알림 텍스트를 설정 또는 해제 하는 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-161">Ability to turn Self-Service Portal notice text on or off</span></span>

<span data-ttu-id="1f4f0-162">MBAM 2.0 SP1에서는 셀프 서비스 포털에서 알림 텍스트를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-162">MBAM 2.0 SP1 enables you to turn off the notice text on the Self-Service Portal.</span></span> <span data-ttu-id="1f4f0-163">이전에는 기본적으로 표시 되는 알림 텍스트 이므로 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-163">Previously, the notice text displayed by default, and you could not turn it off.</span></span>

**<span data-ttu-id="1f4f0-164">알림 텍스트를 해제 하려면</span><span class="sxs-lookup"><span data-stu-id="1f4f0-164">To turn off the notice text</span></span>**

1.  <span data-ttu-id="1f4f0-165">셀프 서비스 포털을 설치한 서버에서 IIS (인터넷 정보 서비스)를 열고 \*\* &gt; Microsoft BitLocker 관리 및 모니터링 &gt; SelfService &gt; 응용 프로그램 설정을\*\*찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-165">On the server where you installed the Self-Service Portal, open Internet Information Services (IIS) and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="1f4f0-166">**이름** 열에서 **displaynotice**a를 선택 하 고 값을 **false**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-166">From the **Name** column, select **DisplayNotice**, and set the value to **false**.</span></span>

### <span data-ttu-id="1f4f0-167">사용자에 게 셀프 서비스 포털 정보를 가리키는 HelpdeskText 문을 지역화 하는 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-167">Ability to localize the HelpdeskText statement that points users to more Self-Service Portal information</span></span>

<span data-ttu-id="1f4f0-168">최종 사용자가 셀프 서비스 포털을 사용 하는 경우 추가 도움말을 가져오는 방법을 알려 주는 셀프 서비스 포털 "HelpdeskText" 문의 지역화 된 버전을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-168">You can configure a localized version of the Self-Service Portal “HelpdeskText” statement, which tells end users how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="1f4f0-169">문에 대해 지역화 된 텍스트를 구성 하는 경우 다음 지침에 설명 된 대로 MBAM에는 지역화 버전이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-169">If you configure localized text for the statement, as described in the following instructions, MBAM will display the localized version.</span></span> <span data-ttu-id="1f4f0-170">MBAM이 지역화 된 버전을 찾지 못하면 **HelpdeskText** 매개 변수에 있는 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-170">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

**<span data-ttu-id="1f4f0-171">HelpdeskText 문의 지역화 된 버전을 표시 하려면</span><span class="sxs-lookup"><span data-stu-id="1f4f0-171">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="1f4f0-172">셀프 서비스 포털을 설치한 서버에서 IIS를 열고 \*\* &gt; Microsoft BitLocker 관리 및 모니터링 &gt; SelfService &gt; 응용 프로그램 설정을\*\*찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-172">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="1f4f0-173">**작업** 창에서 **추가** 를 클릭 하 여 **응용 프로그램 설정 추가** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-173">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="1f4f0-174">**이름** 필드에 **HelpdeskText**\ _ &lt; *언어* &gt; 를 입력 &lt; *language* &gt; 합니다. 여기서 해당 언어는 텍스트에 적합 한 언어 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-174">In the **Name** field, type **HelpdeskText**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the text.</span></span> <span data-ttu-id="1f4f0-175">예를 들어 스페인어로 지역화 된 HelpdeskText 문을 만들려면 HelpdeskText \ _es 매개 변수에 이름을 name으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-175">For example, to create a localized HelpdeskText statement in Spanish, you would name the parameter HelpdeskText\_es-es.</span></span> <span data-ttu-id="1f4f0-176">사용할 수 있는 유효한 언어 코드 목록은 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-176">For a list of the valid language codes that you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="1f4f0-177">**값** 필드에 최종 사용자에 게 표시 하려는 지역화 된 텍스트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-177">In the **Value** field, type the localized text that you want to display to end users.</span></span>

### <span data-ttu-id="1f4f0-178">셀프 서비스 포털 HelpdeskURL를 지역화 하는 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-178">Ability to localize the Self-Service Portal HelpdeskURL</span></span>

<span data-ttu-id="1f4f0-179">최종 사용자에 게 기본적으로 표시 되도록 자체 서비스 포털 HelpdeskURL의 지역화 된 버전을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-179">You can configure a localized version of the Self-Service Portal HelpdeskURL to display to end users by default.</span></span> <span data-ttu-id="1f4f0-180">다음 지침에 설명 된 바와 같이 지역화 된 버전을 만드는 경우 MBAM에서 지역화 된 버전을 찾고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-180">If you create a localized version, as described in the following instructions, MBAM finds and displays the localized version.</span></span> <span data-ttu-id="1f4f0-181">MBAM이 지역화 된 버전을 찾지 못하면 HelpDeskURL 매개 변수에 대해 구성 된 URL이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-181">If MBAM does not find a localized version, it displays the URL that is configured for the HelpDeskURL parameter.</span></span>

**<span data-ttu-id="1f4f0-182">지역화 된 HelpdeskURL를 표시 하려면</span><span class="sxs-lookup"><span data-stu-id="1f4f0-182">To display a localized HelpdeskURL</span></span>**

1.  <span data-ttu-id="1f4f0-183">셀프 서비스 포털을 설치한 서버에서 IIS를 열고 \*\* &gt; Microsoft BitLocker 관리 및 모니터링 &gt; SelfService &gt; 응용 프로그램 설정을\*\*찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-183">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="1f4f0-184">**작업** 창에서 **추가** 를 클릭 하 여 **응용 프로그램 설정 추가** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-184">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="1f4f0-185">**이름** 필드에 **HelpdeskURL**\ _ &lt; *언어* &gt; 를 입력 &lt; *language* &gt; 합니다. 여기서 해당 언어는 해당 URL에 대 한 언어 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-185">In the **Name** field, type **HelpdeskURL**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the URL.</span></span> <span data-ttu-id="1f4f0-186">예를 들어 스페인어로 지역화 된 HelpdeskURL를 만들려면 매개 변수의 이름을 HelpdeskURL \ _es로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-186">For example, to create a localized HelpdeskURL in Spanish, you would name the parameter HelpdeskURL\_es-es.</span></span> <span data-ttu-id="1f4f0-187">사용할 수 있는 유효한 언어 코드 목록은 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-187">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="1f4f0-188">**값** 필드에 최종 사용자에 게 표시 하려는 지역화 된 HelpdeskURL를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-188">In the **Value** field, type the localized HelpdeskURL that you want to display to end users.</span></span>

### <span data-ttu-id="1f4f0-189">셀프 서비스 포털 알림 텍스트를 지역화 하는 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-189">Ability to localize the Self-Service Portal notice text</span></span>

<span data-ttu-id="1f4f0-190">셀프 서비스 포털에서 기본적으로 최종 사용자에 게 표시 되도록 지역화 된 알림 텍스트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-190">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="1f4f0-191">알림 텍스트를 표시 하는 notice.txt 파일은 다음 루트 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-191">The notice.txt file, which displays the notice text, is located in the following root directory:</span></span>

<span data-ttu-id="1f4f0-192">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="1f4f0-192">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="1f4f0-193">지역화 된 알림 텍스트를 표시 하려면 지역화 notice.txt 파일을 만들고 다음 디렉터리의 특정 언어 폴더 아래에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-193">To display localized notice text, you create a localized notice.txt file and save it under a specific language folder in the following directory:</span></span>

<span data-ttu-id="1f4f0-194">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="1f4f0-194">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="1f4f0-195">MBAM은 다음 규칙에 따라 알림 텍스트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-195">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="1f4f0-196">적절 한 언어 폴더에서 지역화 된 notice.txt 파일을 만드는 경우 MBAM은 지역화 된 알림 텍스트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-196">If you create a localized notice.txt file in the appropriate language folder, MBAM displays the localized notice text.</span></span>

-   <span data-ttu-id="1f4f0-197">MBAM이 notice.txt 파일의 지역화 된 버전을 찾지 못하면 기본 notice.txt 파일에 텍스트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-197">If MBAM does not find a localized version of the notice.txt file, it displays the text in the default notice.txt file.</span></span>

-   <span data-ttu-id="1f4f0-198">MBAM이 기본 notice.txt 파일을 찾지 못하면 셀프 서비스 포털에 기본 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-198">If MBAM does not find a default notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

**<span data-ttu-id="1f4f0-199">참고</span><span class="sxs-lookup"><span data-stu-id="1f4f0-199">Note</span></span>**  
<span data-ttu-id="1f4f0-200">최종 사용자의 브라우저가 해당 언어 하위 폴더 또는 notice.txt 없는 언어로 설정 된 경우에는 다음 루트 디렉터리의 notice.txt 파일에 있는 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-200">If an end user’s browser is set to a language that does not have a corresponding language subfolder or notice.txt, the text that is in the notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="1f4f0-201">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="1f4f0-201">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\



**<span data-ttu-id="1f4f0-202">지역화 된 notice.txt 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="1f4f0-202">To create a localized notice.txt file</span></span>**

1.  <span data-ttu-id="1f4f0-203">셀프 서비스 포털을 설치한 서버에서 &lt; *language* &gt; 다음 디렉터리에 언어 폴더를 만듭니다. 여기서 &lt; *언어* 는 &gt; 지역화 된 언어의 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-203">On the server where you installed the Self-Service Portal, create a &lt;*language*&gt; folder in the following directory, where &lt;*language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="1f4f0-204">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="1f4f0-204">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    **<span data-ttu-id="1f4f0-205">참고</span><span class="sxs-lookup"><span data-stu-id="1f4f0-205">Note</span></span>**  
    <span data-ttu-id="1f4f0-206">일부 언어 폴더가 이미 있으므로이를 만들 필요가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-206">Some language folders already exist, so you may not have to create one.</span></span> <span data-ttu-id="1f4f0-207">언어 폴더를 만들어야 하는 경우 언어 폴더에 사용할 수 있는 유효한 이름 목록에 대 한 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947) 를 참조 하세요 &lt; *language* &gt; .</span><span class="sxs-lookup"><span data-stu-id="1f4f0-207">If you do need to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*language*&gt; folder.</span></span>



2.  <span data-ttu-id="1f4f0-208">지역화 된 알림 텍스트를 포함 하는 notice.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-208">Create a notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="1f4f0-209">notice.txt 파일을 &lt; *언어* &gt; 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-209">Save the notice.txt file in the &lt;*language*&gt; folder.</span></span> <span data-ttu-id="1f4f0-210">예를 들어 스페인어로 지역화 된 notice.txt 파일을 만들려면 다음 폴더에 지역화 된 notice.txt 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-210">For example, to create a localized notice.txt file in Spanish, you would save the localized notice.txt file in the following folder:</span></span>

    <span data-ttu-id="1f4f0-211">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\es-es</span><span class="sxs-lookup"><span data-stu-id="1f4f0-211">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\es-es</span></span>

## <span data-ttu-id="1f4f0-212">MBAM 2.0 SP1으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1f4f0-212">Upgrading to MBAM 2.0 SP1</span></span>


<span data-ttu-id="1f4f0-213">이전 버전의 MBAM에서 MBAM 2.0 SP1로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-213">You can upgrade to MBAM 2.0 SP1 from any previous version of MBAM.</span></span>

### <span data-ttu-id="1f4f0-214">MBAM 인프라 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1f4f0-214">Upgrading the MBAM infrastructure</span></span>

<span data-ttu-id="1f4f0-215">다음과 같이 MBAM 서버 인프라를 mbam SP1로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-215">You can upgrade the MBAM Server infrastructure to MBAM 2.0 SP1 as follows:</span></span>

<span data-ttu-id="1f4f0-216">**수동 현재 위치 서버 대체**: 기존 Mbam 서버 인프라를 수동으로 제거한 다음 mbam 2.0 SP1 서버 인프라를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-216">**Manual in-place server replacement**: You must manually uninstall the existing MBAM Server infrastructure, and then install the MBAM 2.0 SP1 Server infrastructure.</span></span> <span data-ttu-id="1f4f0-217">업그레이드를 수행 하기 위해 데이터베이스를 제거할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-217">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="1f4f0-218">대신 이전 버전의 MBAM이 생성 되는 기존 데이터베이스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-218">Instead, you select the existing databases, which the previous version of MBAM created.</span></span> <span data-ttu-id="1f4f0-219">MBAM 2.0 SP1 업그레이드 설치는 기존 데이터베이스를 MBAM 2.0 SP1로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-219">The MBAM 2.0 SP1 upgrade installation then migrates the existing databases to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="1f4f0-220">**분산 클라이언트 업그레이드**: 독립 실행형 mbam 토폴로지를 사용 하는 경우 mbam 2.0 SP1 서버 인프라를 설치한 후 Mbam 클라이언트를 점차적으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-220">**Distributed client upgrade**: If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 SP1 Server infrastructure.</span></span>

<span data-ttu-id="1f4f0-221">MBAM 서버 인프라를 업그레이드 하면 mbam 1.0 또는 2.0 클라이언트가 MBAM 2.0 SP1 서버에 성공적으로 보고 되지만 복구 데이터는 저장 되지만, 준수는 현재 설치 된 MBAM 클라이언트 버전에서 사용할 수 있는 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-221">After you upgrade the MBAM Server infrastructure, MBAM 1.0 or 2.0 Clients will report to the MBAM 2.0 SP1 Server successfully and will store the recovery data, but compliance will be based on the policies available for the MBAM Client version that is currently installed.</span></span> <span data-ttu-id="1f4f0-222">MBAM 2.0 SP1 정책에 대 한 보고 기능을 사용 하도록 설정 하려면 클라이언트 컴퓨터를 MBAM 2.0 SP1로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-222">To enable reporting against MBAM 2.0 SP1 policies, you must upgrade client computers to MBAM 2.0 SP1.</span></span> <span data-ttu-id="1f4f0-223">이전 클라이언트를 제거 하지 않고 MBAM 2.0 SP1 클라이언트로 클라이언트 컴퓨터를 업그레이드할 수 있으며, 클라이언트는 MBAM 2.0 SP1 정책에 따라 적용 하 고 보고 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-223">You can upgrade the client computers to the MBAM 2.0 SP1 Client without uninstalling the previous Client, and the Client will start to apply and report, based on the MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="1f4f0-224">MBAM 서버 업그레이드에 대 한 자세한 내용은 [이전 버전의 mbam에서 업그레이드](upgrading-from-previous-versions-of-mbam.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-224">For more information about upgrading the MBAM servers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

### <span data-ttu-id="1f4f0-225">MBAM 클라이언트를 MBAM 2.0 SP1로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1f4f0-225">Upgrading the MBAM Client to MBAM 2.0 SP1</span></span>

<span data-ttu-id="1f4f0-226">최종 사용자 컴퓨터를 MBAM 2.0 SP1 클라이언트로 업그레이드 하려면 각 클라이언트 컴퓨터에서 **MbamClientSetup.exe** 를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-226">To upgrade end-user computers to the MBAM 2.0 SP1 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="1f4f0-227">설치 관리자가 자동으로 MBAM 2.0 SP1 클라이언트로 클라이언트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-227">The installer automatically updates the Client to the MBAM 2.0 SP1 Client.</span></span> <span data-ttu-id="1f4f0-228">설치 후에는 클라이언트 컴퓨터를 다시 부팅할 필요가 없으며 mbam 2.0 SP1 클라이언트는 MBAM 2.0 SP1 정책에 대해 적용 하 고 보고 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-228">After the installation, client computers do not have to be rebooted, and the MBAM 2.0 SP1 Client starts to apply and report against MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="1f4f0-229">구성 관리자에 MBAM을 사용 하는 경우 mbam 클라이언트 컴퓨터를 MBAM 2.0 SP1로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-229">If you are using MBAM with Configuration Manager, you must upgrade the MBAM client computers to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="1f4f0-230">MBAM 클라이언트 컴퓨터를 업그레이드 하는 방법에 대 한 자세한 내용은 [이전 버전의 mbam에서 업그레이드](upgrading-from-previous-versions-of-mbam.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-230">For more information about upgrading the MBAM client computers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

## <span data-ttu-id="1f4f0-231">Configuration Manager에서 MBAM 2.0 SP1 설치 또는 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1f4f0-231">Installing or upgrading to MBAM 2.0 SP1 with Configuration Manager</span></span>


<span data-ttu-id="1f4f0-232">이 섹션에서는 MBAM 2.0 SP1을 새 설치로 설치 하거나 이전의 MBAM 2.0 SP1 설치로 업그레이드할 때 요구 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-232">This section describes the requirements when you are installing MBAM 2.0 SP1 as a new installation or as an upgrade to a previous MBAM 2.0 SP1 installation.</span></span>

### <span data-ttu-id="1f4f0-233">Configuration Manager에서 MBAM을 사용 하는 경우 MBAM 2.0 SP1을 설치 하는 데 필요한 파일</span><span class="sxs-lookup"><span data-stu-id="1f4f0-233">Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager</span></span>

<span data-ttu-id="1f4f0-234">MBAM을 처음으로 설치 하 고 System Center Configuration Manager와 함께 MBAM 2.0 SP1을 사용 하는 경우, Configuration Manager에서 MBAM이 올바르게 작동 하도록 mof 파일을 만들거나 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-234">If you are installing MBAM for the first time and you are using MBAM 2.0 SP1 with System Center Configuration Manager, you must create or edit mof files to enable MBAM to work correctly with Configuration Manager.</span></span>

-   **<span data-ttu-id="1f4f0-235">구성 .mof 파일</span><span class="sxs-lookup"><span data-stu-id="1f4f0-235">configuration.mof file</span></span>**

    -   <span data-ttu-id="1f4f0-236">Configuration Manager 2007를 사용 하는 경우에는 항목에서 3 단계를 완료 하 여 configuration .mof 파일을 편집 해야 하며,이 항목 다음에 오는 **Configuration Manager 2007에서 MBAM을 사용 하는 2.0 경우**에만 구성 파일을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-236">If you are using Configuration Manager 2007, you must edit the configuration.mof file by completing step 3 from the item **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**, which follows this item.</span></span>

    -   <span data-ttu-id="1f4f0-237">System Center 2012 구성 관리자를 사용 하는 경우에는 [구성 .Mof 파일 편집](edit-the-configurationmof-file.md)의 지침에 따라 구성 .mof 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-237">If you are using System Center 2012 Configuration Manager, edit the configuration.mof file by following the instructions in [Edit the Configuration.mof File](edit-the-configurationmof-file.md).</span></span>

-   <span data-ttu-id="1f4f0-238">**sms \ _def mof 파일** - [Sms \ _def 파일 만들기 또는 편집](create-or-edit-the-sms-defmof-file.md)의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-238">**sms\_def.mof file** – follow the instructions in [Create or Edit the Sms\_def.mof File](create-or-edit-the-sms-defmof-file.md).</span></span>

### <span data-ttu-id="1f4f0-239">MBAM 2.0 SP1로 업그레이드 하 고 Configuration Manager 2007에서 MBAM을 사용 하는 경우에는 구성 .mof 파일을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-239">Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007</span></span>

<span data-ttu-id="1f4f0-240">MBAM 2.0 SP1로 업그레이드 하는 경우 구성 관리자 2007에서 MBAM을 사용 하는 경우에는 MBAM 2.0 SP1이 올바르게 작동 하도록 구성 .mof 파일을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-240">If you are upgrading to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007, you must update the configuration.mof file to ensure that MBAM 2.0 SP1 works correctly.</span></span>

**<span data-ttu-id="1f4f0-241">구성 .mof 파일을 업데이트 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-241">To update the configuration.mof file:</span></span>**

1.  <span data-ttu-id="1f4f0-242">Configuration Manager 서버에서 Configuration .mof 파일의 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-242">On the Configuration Manager Server, browse to the location of the Configuration.mof file:</span></span>

    <span data-ttu-id="1f4f0-243">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="1f4f0-243">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="1f4f0-244">기본 설치의 경우 설치 위치 는%systemdrive%\\Program Files (x86) \\Microsoft 구성 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-244">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="1f4f0-245">구성 .mof 파일에 추가한 코드 블록을 검토 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-245">Review the block of code that you appended to the configuration.mof file, and delete it.</span></span> <span data-ttu-id="1f4f0-246">코드 블록은 다음 단계에 표시 되는 것과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-246">The block of code will be similar to the one shown in the following step.</span></span>

3.  <span data-ttu-id="1f4f0-247">다음 코드 블록을 복사한 다음이를 구성 .mof 파일에 추가 하 여 다음 필수 MBAM 클래스를 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-247">Copy the following block of code, and then append it to the configuration.mof file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### <span data-ttu-id="1f4f0-248">MBAM 2.0 SP1 번역</span><span class="sxs-lookup"><span data-stu-id="1f4f0-248">Translation of MBAM 2.0 SP1</span></span>

<span data-ttu-id="1f4f0-249">현재 MBAM 2.0 SP1은 다음 언어로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-249">MBAM 2.0 SP1 is now available in the following languages:</span></span>

-   <span data-ttu-id="1f4f0-250">영어 (미국) en-us-US</span><span class="sxs-lookup"><span data-stu-id="1f4f0-250">English (United States) en-US</span></span>
-   <span data-ttu-id="1f4f0-251">프랑스어 (프랑스) fr-fr</span><span class="sxs-lookup"><span data-stu-id="1f4f0-251">French (France) fr-FR</span></span>
-   <span data-ttu-id="1f4f0-252">이탈리아어 (이탈리아) it</span><span class="sxs-lookup"><span data-stu-id="1f4f0-252">Italian (Italy) it-IT</span></span>
-   <span data-ttu-id="1f4f0-253">독일어 (독일) DE-DE</span><span class="sxs-lookup"><span data-stu-id="1f4f0-253">German (Germany) de-DE</span></span>
-   <span data-ttu-id="1f4f0-254">스페인어, 국제 정렬 (스페인-ES)</span><span class="sxs-lookup"><span data-stu-id="1f4f0-254">Spanish, International Sort (Spain) es-ES</span></span>
-   <span data-ttu-id="1f4f0-255">한국어 (대한민국) ko-kr-KR</span><span class="sxs-lookup"><span data-stu-id="1f4f0-255">Korean (Korea) ko-KR</span></span>
-   <span data-ttu-id="1f4f0-256">일본어 (일본) ja-jp</span><span class="sxs-lookup"><span data-stu-id="1f4f0-256">Japanese (Japan) ja-JP</span></span>
-   <span data-ttu-id="1f4f0-257">포르투갈어 (브라질) pt-BR</span><span class="sxs-lookup"><span data-stu-id="1f4f0-257">Portuguese (Brazil) pt-BR</span></span>
-   <span data-ttu-id="1f4f0-258">러시아어 (러시아)의 기능</span><span class="sxs-lookup"><span data-stu-id="1f4f0-258">Russian (Russia) ru-RU</span></span>
-   <span data-ttu-id="1f4f0-259">중국어 번체 zh-cn-hy 얕은 샘물 a</span><span class="sxs-lookup"><span data-stu-id="1f4f0-259">Chinese Traditional zh-TW</span></span>
-   <span data-ttu-id="1f4f0-260">중국어 간체 zh-cn-CN</span><span class="sxs-lookup"><span data-stu-id="1f4f0-260">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="1f4f0-261">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1f4f0-261">How to Get MDOP Technologies</span></span>

<span data-ttu-id="1f4f0-262">MBAM 2.0 SP1은 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-262">MBAM 2.0 SP1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="1f4f0-263">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f0-263">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="1f4f0-264">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="1f4f0-264">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="1f4f0-265">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1f4f0-265">Related topics</span></span>

[<span data-ttu-id="1f4f0-266">MBAM 2.0 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="1f4f0-266">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)









