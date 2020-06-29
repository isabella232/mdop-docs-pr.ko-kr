---
title: App-V 5.0을 사용한 고가용성 계획
description: App-V 5.0을 사용한 고가용성 계획
author: dansimp
ms.assetid: 6d9a6492-23f8-465c-82e5-49c863594156
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebf586de7cae19d40d76c9c0c845f93e7bd9021b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813492"
---
# <span data-ttu-id="6acdd-103">App-V 5.0을 사용한 고가용성 계획</span><span class="sxs-lookup"><span data-stu-id="6acdd-103">Planning for High Availability with App-V 5.0</span></span>


<span data-ttu-id="6acdd-104">Microsoft Application Virtualization 5.0 (App-v 5.0) 시스템 구성은 높은 수준의 사용 가능한 서비스를 유지 관리 하는 옵션을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-104">Microsoft Application Virtualization 5.0 (App-V 5.0) system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="6acdd-105">다음 섹션의 정보를 사용 하 여 고가용성 구성에서 App-v 5.0을 배포 하는 옵션을 이해 하는 데 도움을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-105">Use the information in the following sections to help you understand the options to deploy App-V 5.0 in a highly available configuration.</span></span>

-   [<span data-ttu-id="6acdd-106">Microsoft SQL Server 클러스터링에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="6acdd-107">IIS 네트워크 부하 분산에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="6acdd-108">(SCS) 모드를 실행할 때 클러스터 된 파일 서버 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="6acdd-109">Microsoft SQL Server 미러링에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="6acdd-110">Microsoft SQL Server에 대 한 지원이 항상 켜져 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="6acdd-111">Microsoft SQL Server 클러스터링에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="6acdd-112">Microsoft SQL Server 클러스터를 실행 하는 컴퓨터에서 App-v 관리 데이터베이스 및 보고 데이터베이스를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="6acdd-113">그러나 스크립트를 사용 하 여 데이터베이스를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="6acdd-114">지침은 [SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법을](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="6acdd-115">IIS 네트워크 부하 분산에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="6acdd-116">Iis (인터넷 정보 서비스) 네트워크 부하 분산을 사용 하 여 IIS를 통해 배포 되는 앱-V 5 x 관리, 게시 및 Reporting Services를 실행 하는 컴퓨터에 대해 고가용성 환경을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="6acdd-117">Windows Server 운영 체제를 실행 하는 컴퓨터의 IIS 및 네트워크 부하 분산을 구성 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="6acdd-118">IIS (인터넷 정보 서비스) 7.0을 구성 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="6acdd-119">고가용성 [및 확장성 구현-ARR 및 NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="6acdd-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="6acdd-120">Microsoft Windows Server 구성</span><span class="sxs-lookup"><span data-stu-id="6acdd-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="6acdd-121">[네트워크 부하 분산](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="6acdd-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="6acdd-122">이 정보는 Windows Server2008, Windows Server2008R2 또는 Windows Server2012의 IIS NLB (네트워크 부하 분산) 클러스터에도 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="6acdd-123">**참고**  Windows Server2012의 IIS 네트워크 부하 분산 기능은 일반적으로 Windows Server2008R2에서와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="6acdd-124">그러나 일부 작업 세부 정보는 Windows Server2012에서 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="6acdd-125">작업을 수행 하는 새로운 방법에 대 한 자세한 내용은 [Windows server 2012 R2 Preview 및 Windows server 2012 ()의 일반적인 관리 작업 및 탐색](https://go.microsoft.com/fwlink/?LinkId=316371) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="6acdd-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="6acdd-126">(SCS) 모드를 실행할 때 클러스터 된 파일 서버 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="6acdd-127">클러스터 된 파일 서버와 SCS (공유 콘텐츠 저장소) 모드에서 앱-V 5.0을 실행 하는 것이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-127">Running App-V 5.0 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="6acdd-128">다음 단계를 사용 하 여이 구성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="6acdd-129">클라이언트 SCS 모드로 실행 되도록 App-v 5.0을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-129">Configure App-V 5.0 to run in client SCS mode.</span></span> <span data-ttu-id="6acdd-130">App-v 5.0 SCS 모드 구성에 대 한 자세한 내용은 [공유 콘텐츠 저장소 모드에 대 한 app-v 5.0 클라이언트 설치 방법을](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-130">For more information about configuring App-V 5.0 SCS mode, see [How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="6acdd-131">가상 SAN을 사용 하 여 Microsoft Server2012 스케일 아웃 모드와 사전 **2012** 모드에서 구성 된 파일 서버 클러스터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="6acdd-132">다음 단계를 사용 하 여 구성의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="6acdd-133">게시 서버에 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-133">Add a package on the publishing server.</span></span> <span data-ttu-id="6acdd-134">패키지를 추가 하는 방법에 대 한 자세한 내용은 [관리 콘솔을 사용 하 여 패키지를 추가 하거나 업그레이드 하는 방법을](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="6acdd-135">App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 게시 새로 고침을 수행 하 고 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-135">Perform a publishing refresh on the computer running the App-V 5.0 client and open an application.</span></span>

3.  <span data-ttu-id="6acdd-136">클러스터 노드 중간 게시 새로 고침 및 중간 스트리밍을 전환 하 여 장애 조치가 올바르게 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="6acdd-137">Windows Server 장애 조치 클러스터를 구성 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="6acdd-138">[검사 목록: 클러스터 된 파일 서버 ()를 만듭니다](https://go.microsoft.com/fwlink/?LinkId=316372) https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="6acdd-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="6acdd-139">[Windows Server 2012 장애 조치 (Failover) 클러스터 ()에서 클러스터 공유 볼륨 사용](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="6acdd-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="6acdd-140">Microsoft SQL Server 미러링에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="6acdd-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="6acdd-141">두 개의 SQL Server 인스턴스를 사용 하 여 App-v 5.0 관리 서버 데이터베이스가 미러링 되는 Microsoft SQL Server 미러링 (App-v 5.0 management server 데이터베이스의 경우)이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-141">Using Microsoft SQL Server mirroring, where the App-V 5.0 management server database is mirrored utilizing two SQL Server instances, for App-V 5.0 management server databases is supported.</span></span>

<span data-ttu-id="6acdd-142">Microsoft SQL Server 미러링을 구성 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="6acdd-143">[방법: 미러링에 대 한 미러 데이터베이스 준비 (t-sql)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="6acdd-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="6acdd-144">[Windows 인증 (SQL Server Management Studio)을 사용 하 여 데이터베이스 미러링 세션 설정](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="6acdd-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="6acdd-145">다음 단계를 사용 하 여 구성의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="6acdd-146">Microsoft SQL Server 미러링 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="6acdd-147">**장애 조치 (Failover)** 를 선택 하 여 새 마스터 Microsoft SQL Server 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="6acdd-148">장애 조치 (failover) 후 App-v 5.0 관리 서버가 계속 정상적으로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-148">Verify that the App-V 5.0 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="6acdd-149">관리 서버의 연결 문자열을 수정 하 여 \*\*장애 조치 (failover) 파트너 = &lt; server2 &gt; \*\*를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="6acdd-150">이것은 미러의 기본이 보조로 장애 조치 되 고 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 새로운 연결을 수행 하는 경우에만 도움이 됩니다 (다시 부팅 후 말).</span><span class="sxs-lookup"><span data-stu-id="6acdd-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.0 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="6acdd-151">다음 단계를 사용 하 여 연결 문자열을 수정 하 여 \*\*장애 조치 파트너 = &lt; server2 &gt; \*\*:를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="6acdd-152">**중요**  이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="6acdd-153">Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="6acdd-154">레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="6acdd-155">Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="6acdd-156">레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="6acdd-157">관리 서버에 로그인 하 여 **regedit**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="6acdd-158">**HKEY \ _LOCAL \ _MACHINE**  \\  **Software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="6acdd-159">**장애 조치 (failover) 파트너 = &lt; &gt; server2**로 **관리 \ _SQL \ _CONNECTION \ _STRING** 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="6acdd-160">IIS 콘솔을 사용 하 여 관리 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="6acdd-161">**참고**  데이터베이스 미러링은 microsoft SQL Server 2012에서 사용할 수 있는 **AlwaysOn** 기능 때문에 Microsoft sql Server2012의 사용 되지 않는 데이터베이스 엔진 기능 목록에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="6acdd-162">자세한 내용을 보려면 다음 링크 중 하나를 클릭 하세요.</span><span class="sxs-lookup"><span data-stu-id="6acdd-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="6acdd-163">[방법: 미러링 (()을 위해 미러 데이터베이스 준비 (transact-sql)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="6acdd-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="6acdd-164">[방법: 데이터베이스 미러링 세션 구성 (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="6acdd-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="6acdd-165">[Windows 인증 (SQL Server Management Studio)을 사용 하 여 데이터베이스 미러링 세션을 설정](https://go.microsoft.com/fwlink/?LinkId=394237) https://go.microsoft.com/fwlink/?LinkId=394237) 합니다 (.</span><span class="sxs-lookup"><span data-stu-id="6acdd-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="6acdd-166">[SQL Server 2012 ()의 사용 되지 않는 데이터베이스 엔진 기능](https://go.microsoft.com/fwlink/?LinkId=394238) https://go.microsoft.com/fwlink/?LinkId=394238)</span><span class="sxs-lookup"><span data-stu-id="6acdd-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="6acdd-167">Microsoft SQL Server에 대 한 지원이 항상 구성</span><span class="sxs-lookup"><span data-stu-id="6acdd-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="6acdd-168">App-v 5.0 관리 서버 데이터베이스는 **Always On** 구성을 사용 하 여 Microsoft SQL server를 실행 하는 컴퓨터에 대 한 배포를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6acdd-168">The App-V 5.0 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>

## <span data-ttu-id="6acdd-169">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6acdd-169">Related topics</span></span>


[<span data-ttu-id="6acdd-170">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="6acdd-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





