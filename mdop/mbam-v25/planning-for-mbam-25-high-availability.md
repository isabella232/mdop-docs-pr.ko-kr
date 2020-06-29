---
title: MBAM 2.5 고가용성 계획
description: MBAM 2.5 고가용성 계획
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826943"
---
# <span data-ttu-id="b39a3-103">MBAM 2.5 고가용성 계획</span><span class="sxs-lookup"><span data-stu-id="b39a3-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="b39a3-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음 섹션에서 설명 하는 다음 기술 중 하나 이상을 사용 하 여 고가용성을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="b39a3-105">SQL Server AlwaysOn 가용성 그룹</span><span class="sxs-lookup"><span data-stu-id="b39a3-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="b39a3-106">Microsoft SQL Server 클러스터링</span><span class="sxs-lookup"><span data-stu-id="b39a3-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="b39a3-107">IIS 네트워크 부하 분산</span><span class="sxs-lookup"><span data-stu-id="b39a3-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="b39a3-108">SQL Server의 데이터베이스 미러링</span><span class="sxs-lookup"><span data-stu-id="b39a3-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="b39a3-109">VSS (볼륨 섀도 복사본 서비스)를 사용 하 여 MBAM 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="b39a3-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="b39a3-110">다음 섹션의 정보를 사용 하 여 항상 사용 가능한 구성에서 MBAM을 배포 하는 옵션을 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="b39a3-111">SQL Server AlwaysOn 가용성 그룹 지원</span><span class="sxs-lookup"><span data-stu-id="b39a3-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="b39a3-112">MBAM을 사용 하면 Microsoft SQL Server에서 데이터베이스에 대 한 가용성 그룹을 구성 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="b39a3-113">MBAM의 가용성 그룹은 규정 준수 및 감사 데이터베이스와 복구 데이터베이스가 개별적이 아니라 함께 작동 하지 않는 장애 조치 환경을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="b39a3-114">가용성 그룹은 읽기/쓰기 기본 데이터베이스 집합과 하나에서 네 개의 해당 보조 데이터베이스 집합을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="b39a3-115">선택적으로 보조 데이터베이스를 읽기 전용 권한, 일부 백업 작업 또는 둘 다에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="b39a3-116">가용성 그룹을 설정 하는 방법에 대 한 자세한 내용은 [AlwaysOn 가용성 그룹](https://go.microsoft.com/fwlink/?LinkId=393277)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b39a3-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="b39a3-117">Microsoft SQL Server 클러스터링</span><span class="sxs-lookup"><span data-stu-id="b39a3-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="b39a3-118">SQL Server 클러스터를 실행 하는 컴퓨터에서 MBAM 2.5 준수 및 감사 데이터베이스와 복구 데이터베이스를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="b39a3-119">IIS 네트워크 부하 분산</span><span class="sxs-lookup"><span data-stu-id="b39a3-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="b39a3-120">네트워크 로드 균형 조정을 사용 하 여 관리 및 모니터링 웹 사이트 (지원 센터 라고도 함), 셀프 서비스 포털 및 IIS (인터넷 정보 서비스)를 통해 배포 되는 웹 서비스를 실행 하는 컴퓨터에 대해 항상 사용 가능한 환경을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="b39a3-121">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="b39a3-121">Prerequisites</span></span>

<span data-ttu-id="b39a3-122">부하 분산을 구성 하기 전에 다음 필수 조건을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="b39a3-123">부하 분산 장치를 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-123">A load balancer must be available.</span></span> <span data-ttu-id="b39a3-124">Microsoft 또는 다른 회사의 부하 분산 장치를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="b39a3-125">Microsoft 부하 분산 장치 기술에 대 한 자세한 내용은 [IIS 서버로 웹 팜 빌드](https://go.microsoft.com/fwlink/?LinkId=393326)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b39a3-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="b39a3-126">적어도 두 대의 서버가 IIS를 실행 중이 고 ASP.NET MVC 4를 포함 하 여 웹 기능을 지원 하기 위해 모든 MBAM 전제 조건을 충족 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="b39a3-127">MBAM 데이터베이스와 보고서는 서버에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="b39a3-128">부하 분산을 사용 하는 데 필요한 MBAM 관련 변경 사항</span><span class="sxs-lookup"><span data-stu-id="b39a3-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="b39a3-129">다음 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="b39a3-130">웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 가상 호스트 이름에 대 한 SPN (서비스 사용자 이름)을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="b39a3-131">예를 들어 가상 호스트 이름이 mbamvirtual.contoso.com 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 contoso\\mbamapppooluser 이면 다음 명령은 SPN을 적절 하 게 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="b39a3-132">다음 MBAM 웹 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="b39a3-133">MBAM 웹 기능을 호스트할 각 서버에서 응용 프로그램 풀 관리 자격 증명에 동일한 도메인 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="b39a3-134">부하 분산 클러스터의 가상 호스트 이름 (DNS 이름)과 일치 하는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="b39a3-135">예를 들어 가상 호스트 이름을 **mbamvirtual.contoso.com**로 "NLB1" 라는 서버에 mbam을 설치 하는 경우 Windows PowerShell cmdlet에서 지정 하는 호스트 이름이 **mbamvirtual.contoso.com**있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="b39a3-136">부하 분산 장치를 사용 하 여 웹 팜에서 웹사이트를 구성 하는 경우에는 동일한 컴퓨터 키를 사용 하도록 웹사이트를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="b39a3-137">자세한 내용은 [MachineKey 요소 (ASP.NET Settings 스키마)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx)의 다음 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b39a3-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="b39a3-138">컴퓨터 키 설명</span><span class="sxs-lookup"><span data-stu-id="b39a3-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="b39a3-139">웹 팜 배포 고려 사항</span><span class="sxs-lookup"><span data-stu-id="b39a3-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="b39a3-140">키를 자동으로 생성 하는 방법에 대 한 지침은 [컴퓨터 키 생성 (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b39a3-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="b39a3-141">부하 분산에 대 한 정보는 Windows Server 2012 또는 Windows Server2008R2의 IIS NLB (네트워크 부하 분산) 클러스터에도 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="b39a3-142">Windows Server 2012의 IIS 네트워크 부하 분산 기능은 일반적으로 Windows Server2008R2에서와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="b39a3-143">그러나 일부 작업 세부 정보는 Windows Server 2012에서 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="b39a3-144">작업을 수행 하는 새로운 방법에 대 한 자세한 내용은 [Windows server 2012 R2 Preview 및 Windows server 2012의 일반적인 관리 작업 및 탐색](https://go.microsoft.com/fwlink/?LinkId=316371)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b39a3-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="b39a3-145">SQL Server의 데이터베이스 미러링</span><span class="sxs-lookup"><span data-stu-id="b39a3-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="b39a3-146">MBAM은 각 데이터베이스에 대해 두 개의 SQL Server 인스턴스를 사용 하 여 규정 준수 및 감사 데이터베이스와 복구 데이터베이스가 미러링 되는 SQL Server 미러링 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="b39a3-147">미러링을 구현 하기 전에이 항목의 앞부분에서 설명한 가용성 그룹의 우선 미러링이 느리게 진행 되는 것에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="b39a3-148">MBAM에 대 한 미러링을 구현 하려면 **Enable-MbamWebApplication** Windows PowerShell cmdlet을 사용 하 여 미러된 데이터베이스 구성에 대 한 적절 한 연결 문자열을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="b39a3-149">MBAM 2.5 Windows PowerShell cmdlet에 대 한 자세한 내용은 [Windows powershell을 사용 하 여 mbam 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b39a3-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="b39a3-150">Windows PowerShell을 사용 하 여 SQL Server 미러링을 구현 하는 예제</span><span class="sxs-lookup"><span data-stu-id="b39a3-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="b39a3-151">다음 예제에서는 Windows PowerShell cmdlet을 사용 하 여 SQL Server 미러링을 구현 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="b39a3-152">예제 1</span><span class="sxs-lookup"><span data-stu-id="b39a3-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="b39a3-153">예제 2</span><span class="sxs-lookup"><span data-stu-id="b39a3-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="b39a3-154">SQL Server 미러링에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="b39a3-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="b39a3-155">다음 링크는 SQL Server 미러링 구성에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="b39a3-156">방법: 미러링에 대 한 미러 데이터베이스 준비 (T-sql)</span><span class="sxs-lookup"><span data-stu-id="b39a3-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="b39a3-157">Windows 인증 (SQL Server Management Studio)을 사용 하 여 데이터베이스 미러링 세션 설정</span><span class="sxs-lookup"><span data-stu-id="b39a3-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="b39a3-158">VSS (볼륨 섀도 복사본 서비스)를 사용 하 여 MBAM 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="b39a3-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="b39a3-159">MBAM은 Microsoft BitLocker 관리 및 관리 작성자 라고 하는 VSS (볼륨 섀도 복사본 서비스) 기록기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="b39a3-160">이 VSS 기록기는 준수 및 감사 데이터베이스와 복구 데이터베이스를 쉽게 백업할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="b39a3-161">VSS 기록기는 MBAM 웹 응용 프로그램을 사용 하도록 설정 하는 모든 서버에 등록 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="b39a3-162">MBAM VSS 기록기는 Microsoft SQL Server 설치의 일부로 등록 된 SQL Server VSS 기록기에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="b39a3-163">백업을 수행 하기 위해 VSS 기록기를 사용 하는 모든 백업 기술은 MBAM VSS 기록기를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="b39a3-164">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b39a3-164">Related topics</span></span>


[<span data-ttu-id="b39a3-165">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="b39a3-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="b39a3-166">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="b39a3-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b39a3-167">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="b39a3-168">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b39a3-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




