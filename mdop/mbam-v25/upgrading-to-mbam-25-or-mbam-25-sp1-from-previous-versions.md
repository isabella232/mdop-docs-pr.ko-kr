---
title: 이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드
description: 이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812753"
---
# <span data-ttu-id="1f76b-103">이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1f76b-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="1f76b-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 및 이전 버전의 MBAM 클라이언트를 업그레이드 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="1f76b-105">**참고**  이전 버전의 MBAM에서 MBAM 2.5 또는 MBAM 2.5 SP1로 직접 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="1f76b-106">업그레이드를 시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="1f76b-106">Before you start the upgrade</span></span>


<span data-ttu-id="1f76b-107">업그레이드를 시작 하기 전에 다음 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1f76b-108">시작 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="1f76b-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="1f76b-109">세부 정보</span><span class="sxs-lookup"><span data-stu-id="1f76b-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f76b-110">한 서버에 MBAM 웹 사이트를 설치 하는 경우 다른 서버의 웹 서비스에 Windows PowerShell cmdlet을 사용 하 여 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f76b-111">MBAM 서버 구성 마법사는 한 서버에서 웹 사이트를 구성 하는 작업과 다른 서버의 웹 서비스는 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f76b-112">Windows Server2008 R2에서 MBAM 2.0 또는 2.0 SP1에서 MBAM 2.5 또는 2.5 SP1로 업그레이드 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="1f76b-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="1f76b-113">IIS (인터넷 정보 서비스)가 이미 설치 된 후 필요한 .NET Framework 4.5 소프트웨어를 설치 하는 경우 관리 및 모니터링 웹 사이트와 셀프 서비스 포털이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="1f76b-114">이 문제는 IIS가 이미 설치 된 후 .NET Framework가 설치 된 경우 ASP.NET에서 IIS에 올바르게 등록할 수 없기 때문에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="1f76b-115">이 문제를 해결 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="1f76b-116"><strong>다음 위치에서 aspnet_regiis 실행 – i </strong> :</span><span class="sxs-lookup"><span data-stu-id="1f76b-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="1f76b-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="1f76b-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="1f76b-118">자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.NET IIS 등록 도구를 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f76b-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f76b-119">다음이 모두 참일 경우 응용 프로그램 풀 계정에 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="1f76b-120">이전 버전의 MBAM에서 업그레이드 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="1f76b-121">현재 부하 분산 또는 분산 구성에서 MBAM 웹 사이트를 실행 하 고 있지는 않지만, MBAM 2.5 또는 2.5 SP1으로 업그레이드 하는 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1f76b-122">지침은 <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> MBAM 웹 사이트 보안 방법 계획을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="1f76b-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1f76b-123">권장 사항</span><span class="sxs-lookup"><span data-stu-id="1f76b-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1f76b-124">컴퓨터 계정에 대 한 Spn (서비스 사용자 이름)을 이미 등록 한 경우에도 해당 계정을 해당 계정에 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1f76b-125">추천 이유</span><span class="sxs-lookup"><span data-stu-id="1f76b-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1f76b-126">부하 분산 또는 분산 구성에서 웹 사이트를 구성 하려면 응용 프로그램 풀 계정에 SPN을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1f76b-127">Spn이 컴퓨터 계정에 이미 구성 되어 있는 경우 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="1f76b-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1f76b-128">MBAM은 이미 등록 한 Spn을 사용 하지만 추가 Spn을 구성할 필요는 없지만 부하 분산 또는 분산 구성에서 웹 사이트를 구성할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1f76b-129">MBAM 서버 인프라를 업그레이드 하는 단계</span><span class="sxs-lookup"><span data-stu-id="1f76b-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="1f76b-130">다음 섹션의 단계를 사용 하 여 독립 실행형 토폴로지 또는 System Center Configuration Manager 통합 토폴로지에 대해 MBAM을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="1f76b-131">독립 실행형 토폴로지에 대해 MBAM 서버 인프라를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="1f76b-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="1f76b-132">이전 버전의 MBAM을 **프로그램 및 기능** , 웹 서버에서 제거 하 여 정보가 mbam 클라이언트에서 mbam 인프라로 기록 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="1f76b-133">지침은 [MBAM 서버 기능 또는 소프트웨어 제거](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f76b-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="1f76b-134">데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-134">Back up your databases.</span></span>

3.  <span data-ttu-id="1f76b-135">Sql Server Reporting Services를 통해 MBAM 보고서를 호스팅하는 SQL server를 비롯 하 여 **프로그램 및 기능**을 사용 하 여 이전 버전의 mbam을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="1f76b-136">데이터베이스 서버 및 reporting services에서 남아 있는 MBAM 서버 임시 파일 또는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="1f76b-137">**참고**  데이터베이스는 제거 되지 않으며 모든 준수 및 복구 데이터는 데이터베이스에서 유지 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="1f76b-138">MBAM 또는 2.5 SP1 데이터베이스, 보고서, 웹 응용 프로그램을 순서 대로 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="1f76b-139">데이터베이스가 현재 위치에서 업그레이드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="1f76b-140">MBAM 2.5 서식 파일을 사용 하 여 Gpo (그룹 정책 개체)를 업데이트 하 여 mbam 암호화와 같은 새로운 기능을 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="1f76b-141">Gpo와 MBAM 클라이언트를 MBAM 2.5으로 업데이트 하지 않으면 이전 버전의 MBAM 클라이언트는 기능 제한으로 현재 Gpo에 대해 계속 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="1f76b-142">최신 ADMX 서식 파일을 다운로드 하려면 [MDOP 그룹 정책 (admx) 서식 파일을 가져오는 방법을](https://www.microsoft.com/download/details.aspx?id=41183) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f76b-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="1f76b-143">MBAM 서버 인프라를 업그레이드 하면 기존 클라이언트 컴퓨터가 여전히 MBAM 2.5 또는 2.5 SP1 서버에 성공적으로 보고 하 고 복구 데이터는 계속 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="1f76b-144">최신 MBAM 2.5 또는 2.5 SP1 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="1f76b-145">배포 후 클라이언트 컴퓨터를 다시 부팅할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="1f76b-146">System Center Configuration Manager 통합 토폴로지에 대해 MBAM 인프라를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="1f76b-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="1f76b-147">이전 버전의 MBAM을 **프로그램 및 기능** , 웹 서버에서 제거 하 여 정보가 mbam 클라이언트에서 mbam 인프라로 기록 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="1f76b-148">지침은 [MBAM 서버 기능 또는 소프트웨어 제거](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f76b-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="1f76b-149">데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-149">Back up your databases.</span></span>

3.  <span data-ttu-id="1f76b-150">Sql Server Reporting Services를 통해 MBAM 보고서를 호스팅하는 SQL server를 비롯 하 여 **프로그램 및 기능**을 사용 하 여 이전 버전의 mbam을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="1f76b-151">데이터베이스 서버 및 reporting services에서 남아 있는 MBAM 서버 임시 파일 또는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="1f76b-152">Configuration Manager 서버에서 MBAM을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="1f76b-153">**참고**  데이터베이스 및 Configuration Manager 개체 (기준, MBAM 지원 컴퓨터 모음 및 보고서)는 제거 되지 않으며 모든 준수 및 복구 데이터는 데이터베이스에서 유지 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="1f76b-154">.Mof 파일을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="1f76b-155">MBAM 또는 2.5 SP1 데이터베이스, 보고서, 웹 응용 프로그램, 구성 관리자 통합을 순서 대로 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="1f76b-156">데이터베이스 및 구성 관리자 개체가 현재 위치에서 업그레이드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="1f76b-157">선택적으로, Gpo (그룹 정책 개체)를 업데이트 하 고 암호화를 적용 하는 등의 새 기능을 MBAM에 구현 하려는 경우 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="1f76b-158">Gpo를 업데이트 하지 않으면 MBAM은 현재 Gpo에 대해 계속 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="1f76b-159">최신 ADMX 서식 파일을 다운로드 하려면 [MDOP 그룹 정책 (admx) 서식 파일을 가져오는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f76b-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="1f76b-160">MBAM 서버 인프라를 업그레이드 하면 기존 클라이언트 컴퓨터가 여전히 MBAM 2.5 또는 2.5 SP1 서버에 성공적으로 보고 하 고 복구 데이터는 계속 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="1f76b-161">최신 MBAM 2.5 또는 2.5 SP1 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="1f76b-162">배포 후 클라이언트 컴퓨터를 다시 부팅할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="1f76b-163">MBAM 클라이언트에 대 한 업그레이드 지원</span><span class="sxs-lookup"><span data-stu-id="1f76b-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="1f76b-164">MBAM은 모든 이전 버전의 MBAM 클라이언트에서 MBAM 2.5 클라이언트로의 업그레이드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="1f76b-165">MBAM 클라이언트를 설치 하는 방법:</span><span class="sxs-lookup"><span data-stu-id="1f76b-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="1f76b-166">Mbam 클라이언트를 실행 하는 컴퓨터를 모두 한 번에 업그레이드 하거나 MBAM 2.5 서버 인프라를 설치한 후 점진적으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="1f76b-167">전자 소프트웨어 배포 시스템을 통해 MBAM 클라이언트를 설치 하거나 Active Directory 도메인 서비스 또는 System Center Configuration Manager 등의 도구를 통해 가상으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="1f76b-168">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1f76b-168">Related topics</span></span>


[<span data-ttu-id="1f76b-169">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="1f76b-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="1f76b-170">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="1f76b-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="1f76b-171">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="1f76b-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="1f76b-172">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="1f76b-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1f76b-173">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="1f76b-174">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f76b-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





