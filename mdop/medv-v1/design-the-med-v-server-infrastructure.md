---
title: MED-V 서버 인프라 디자인
description: MED-V 서버 인프라 디자인
author: dansimp
ms.assetid: 2781040f-880e-4e16-945d-a38c0adb4151
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4ba4c38328c5484b7daa292f9fc33a4e59824327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824183"
---
# <span data-ttu-id="1e177-103">MED-V 서버 인프라 디자인</span><span class="sxs-lookup"><span data-stu-id="1e177-103">Design the MED-V Server Infrastructure</span></span>


<span data-ttu-id="1e177-104">이 항목에서는 각 MED-V 인스턴스에 대 한 서버 인프라를 디자인 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-104">In this topic, you will design the server infrastructure for each MED-V instance.</span></span> <span data-ttu-id="1e177-105">여기에는 sql Server 인스턴스가 MED-V 서버에 있는지 아니면 원격 서버에 있고 SQL Server 데이터베이스의 크기와 동일한 지를 결정 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-105">This includes determining whether the SQL Server instance will exist on the MED-V server or on a remote server, as well as the size of the SQL Server database.</span></span> <span data-ttu-id="1e177-106">또한 관리 콘솔의 위치도 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-106">You will also determine the location of the management console.</span></span>

## <span data-ttu-id="1e177-107">각 MED-V 인스턴스의 서버를 디자인 하 고 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-107">Design and Place the Server for Each MED-V Instance</span></span>


<span data-ttu-id="1e177-108">MED-V 서버는 정책을 구현 하 고 해당 클라이언트에 대 한 상태 및 기록 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-108">The MED-V server implements policies and stores state and history data about its clients.</span></span>

### <span data-ttu-id="1e177-109">폼 팩터</span><span class="sxs-lookup"><span data-stu-id="1e177-109">Form Factor</span></span>

<span data-ttu-id="1e177-110">MED-V는 RAM이 2GB 인 2.8 GHz 듀얼 코어 CPU 서버를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-110">MED-V recommends using a 2.8-GHz dual core CPU server with 2GB of RAM.</span></span> <span data-ttu-id="1e177-111">이 권장 사항은 MED-V 서버가 전용 컴퓨터에서 실행 되 고 SQL Server와 MED-V 관리 콘솔이 별도의 컴퓨터에서 실행 된다는 가정을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-111">This recommendation is based on the assumption that the MED-V server will run on a dedicated machine and that SQL Server and the MED-V management console will run on separate machines.</span></span>

<span data-ttu-id="1e177-112">이 작업을 수행 하는 경우 MED-V 서버는 상대적으로 약간 로드 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-112">Given this workload, the MED-V server should be relatively lightly loaded.</span></span> <span data-ttu-id="1e177-113">서버 폼 팩터에 대 한 특정 아키텍처 지침이 없는 경우 MED-V 권고안을 사용 하 여 서버를 디자인 하 고 조직의 표준 폼 팩터와 일치 하는 메모리를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-113">In the absence of specific architectural guidance on the server form factor, design the server using the MED-V recommendation, with memory that matches the organization’s standard form factor.</span></span> <span data-ttu-id="1e177-114">MED-V 서버는 Windows Server2008 Hyper-v의 VM (가상 컴퓨터)에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-114">The MED-V server can be run on a virtual machine (VM) on Windows Server2008 Hyper-V.</span></span> <span data-ttu-id="1e177-115">VM이 사용 되는 경우 물리적 컴퓨터에 대해 지정 된 것과 동등한 CPU 및 메모리 리소스에 액세스할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-115">If a VM will be used, ensure that it has access to CPU and memory resources equivalent to those specified for a physical machine.</span></span>

<span data-ttu-id="1e177-116">MED-V 서버의 디스크 용량으로 MED-V 작업 영역 구성 파일을 저장 하는 데 충분 한 공간이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-116">The disk capacity the MED-V server requires must be sufficient to store the MED-V workspace configuration files.</span></span> <span data-ttu-id="1e177-117">MED-V 작업 영역은 한 명 이상의 사용자에 대해 하나의 VM 및 하나의 정책만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-117">A MED-V workspace can only use one VM, and one policy, for one or more users.</span></span> <span data-ttu-id="1e177-118">따라서 저장 해야 하는 MED-V 작업 영역의 수는 동일한 VM의 여러 사용자에 게 서로 다른 정책이 필요한 정도 및 사용할 Vm 수에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-118">Therefore, the number of MED-V workspaces that must be stored depends on the degree to which different policies are required for different users of the same VM, as well as the number of VMs that will be used.</span></span> <span data-ttu-id="1e177-119">MED-V 작업 영역 XML 파일은 일반적인 MED-V 작업 영역에 대 한 크기가 30KB를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-119">The MED-V workspace XML files are around 30KB in size for a typical MED-V workspace.</span></span> <span data-ttu-id="1e177-120">필요한 디스크 용량을 확인 하려면 MED-V 서버가 저장 하는 MED-V 작업 영역의 수에 30KB를 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-120">To determine the required disk capacity, multiply 30 KB by the number of MED-V workspaces that the MED-V server will store.</span></span>

<span data-ttu-id="1e177-121">MED-V 서버의 가장 중요 한 네트워크 연결은 해당 클라이언트에 대 한 링크 이므로 사용할 수 있는 가장 높은 대역폭과 해당 클라이언트에 대 한 가장 강력한 링크를 제공 하는 네트워크 위치에 서버를 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-121">The MED-V server’s most important network connections are the links to its clients, therefore place the server in a network location that provides the most available bandwidth and the most robust links to its clients.</span></span>

### <span data-ttu-id="1e177-122">내결함성은</span><span class="sxs-lookup"><span data-stu-id="1e177-122">Fault Tolerance</span></span>

<span data-ttu-id="1e177-123">MED-V 인스턴스에는 활성 MED-V 서버 하나만 있을 수 있으며, MED-V에는 내결함성 제공을 위해 MSCS (Microsoft 클러스터 서버) 클러스터에 서버를 배치 하는 표준 기능이 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-123">There can only be one active MED-V server in a MED-V instance, and MED-V does not include standard capabilities to place the server in a Microsoft Cluster Server (MSCS) cluster to provide fault tolerance.</span></span> <span data-ttu-id="1e177-124">수동 백업 서버는 수동으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-124">A passive backup server can be manually configured.</span></span>

<span data-ttu-id="1e177-125">MED-V 인스턴스에 수동 백업 서버를 수동으로 구성 해야 하는지 여부를 결정 하려면 사용자가 오프 라인 모드에서 MED-V 이미지를 사용할 수 있는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-125">To decide whether a passive backup server should be manually configured for the MED-V instance, determine whether users will be permitted to use the MED-V images in offline mode.</span></span> <span data-ttu-id="1e177-126">오프 라인 모드에 대 한 자세한 내용은 [도메인 사용자 또는 그룹을 구성 하는 방법을](how-to-configure-a-domain-user-or-groupmedvv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e177-126">For information on offline mode, see [How to Configure a Domain User or Group](how-to-configure-a-domain-user-or-groupmedvv2.md).</span></span> <span data-ttu-id="1e177-127">사용자가 오프 라인으로 작업 하도록 허용 되지 않는 경우 med-v 작업 영역이 클라이언트에서 이미 시작 된 경우에도이 경우 MED-V 서버 장애가 발생할 경우 작업을 계속할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-127">If users are not allowed to work offline, they will be unable to continue working in the event of a MED-V server failure, even if the MED-V workspace has already been started on the client.</span></span> <span data-ttu-id="1e177-128">오프 라인 작업을 허용 하는 경우 각 MED-V 작업 영역에 대해 클라이언트가 인증을 수행 하기 전에 오프 라인으로 작업할 수 있는 기간을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-128">If offline work is permitted, for each MED-V workspace, determine how long the client is allowed to work offline before it must authenticate.</span></span> <span data-ttu-id="1e177-129">서버를 사용할 수 없는 최대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-129">This is the maximum amount of time that the server can be unavailable.</span></span>

## <span data-ttu-id="1e177-130">SQL Server 데이터베이스 디자인 및 배치</span><span class="sxs-lookup"><span data-stu-id="1e177-130">Design and Place the SQL Server Database</span></span>


<span data-ttu-id="1e177-131">MED-V 서버는 SQL Server 데이터베이스를 사용 하 여 클라이언트 상태 및 이벤트를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-131">The MED-V server uses the SQL Server database to store client status and events.</span></span> <span data-ttu-id="1e177-132">MED-V 서버와 같은 컴퓨터에 SQL Server 데이터베이스를 설치 하거나 선택적으로 원격 일 수 있는 SQL Server를 실행 하는 별도의 서버에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-132">You can install the SQL Server database on the same machine as the MED-V server or you can place it on a separate server running SQL Server, which can optionally be remote.</span></span> <span data-ttu-id="1e177-133">다른 MED-V 인스턴스와 데이터베이스를 공유할 수 있으며,이 경우 해당 인스턴스의 이벤트와 경고가 같은 데이터베이스에 저장 되며 보고서에는 모든 인스턴스의 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-133">You can share the database with other MED-V instances, in which case events and alerts from those instances will be stored in the same database, and reports will include events from all instances.</span></span> <span data-ttu-id="1e177-134">기존 SQL Server 인스턴스에 데이터베이스를 설치 하 고 다른 MED-V 서버의 데이터베이스만 같은 인스턴스에 상주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-134">You can install the database in an existing SQL Server instance, and the databases of other MED-V servers can reside in that same instance.</span></span>

<span data-ttu-id="1e177-135">데이터베이스 서버를 MED-V 서버의 원격 위치에 배치 하는 경우 충분 한 대역폭을 사용할 수 없는 네트워크 링크는 콘솔에서 로드 하는 데 시간이 오래 걸릴 수 있으며 클라이언트의 최신 데이터를 표시 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-135">If you place the database server in a location that is remote from the MED-V server, across networks links that do not have sufficient bandwidth available, reports may be slow to load in the console and may not display the latest data from clients.</span></span> <span data-ttu-id="1e177-136">[프로젝트 범위 정의](define-the-project-scope.md) 에서 결정 한 조직 서비스 수준 기대치를 참조 하 고 해당 정보를 사용 하 여 SQL Server 데이터베이스를 배치할 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-136">Refer to the organization service level expectations that you determined in [Define the Project Scope](define-the-project-scope.md) and use that information to decide where to place the SQL Server database.</span></span>

### <span data-ttu-id="1e177-137">폼 팩터</span><span class="sxs-lookup"><span data-stu-id="1e177-137">Form Factor</span></span>

<span data-ttu-id="1e177-138">MED-V와 동일한 서버에서 SQL Server를 실행 하는 경우 SQL Server가 해당 서버에 대 한 데이터를 저장 하는 데만 사용 되는 경우 MED-V 권장 사항으로 시작 하 여 SQL Server 부하에 대 한 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-138">If you will run SQL Server on the same server as MED-V, and if SQL Server will only be used to store data for that server, start with the MED-V recommendation and add resources for the SQL Server load.</span></span> <span data-ttu-id="1e177-139">SQL Server에서 두 개 이상의 MED-V 인스턴스의 이벤트와 알림을 저장 하는 경우 서버 폼 팩터를 확장 하는 방법에 대 한 자세한 내용은 [MICROSOFT SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) 가이드 (http://go.microsoft.com/fwlink/?LinkId=163302)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e177-139">If SQL Server will store events and alerts from more than one MED-V instance, for information on how to scale up the server form factor, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide (http:// go.microsoft.com/fwlink/?LinkId=163302).</span></span>

<span data-ttu-id="1e177-140">데이터베이스의 크기는 데이터베이스가 저장할 클라이언트 이벤트 수에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-140">The size of the database depends on the number of client events that the database will store.</span></span> <span data-ttu-id="1e177-141">이벤트는 MED-V 작업 영역이 시작 되는 경우 또는 MED-V 작업 영역에 오류가 있는 경우와 같이 클라이언트의 정상 작동에 의해 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-141">Events are created by normal operation of the client, such as when a MED-V workspace is started, or when there is an error in the MED-V workspace.</span></span> <span data-ttu-id="1e177-142">클라이언트가 이벤트를 보내는 기본 간격은 1 분입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-142">The default interval at which the client sends events is 1 minute.</span></span>

<span data-ttu-id="1e177-143">데이터베이스의 크기를 예상 하려면 다음을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-143">To estimate the size of the database, determine the following:</span></span>

-   <span data-ttu-id="1e177-144">MED-V 인스턴스의 클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-144">Number of clients in the MED-V instance.</span></span> <span data-ttu-id="1e177-145">최대값은 5000입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-145">The maximum is 5,000.</span></span>

-   <span data-ttu-id="1e177-146">일반적인 이벤트 도착 율입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-146">Typical event arrival rate.</span></span> <span data-ttu-id="1e177-147">이 속도는 클라이언트 사용 동작에 따라 다르며, 클라이언트 당 매일 약 15 ~ 20 개의 이벤트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-147">This rate depends on client usage behavior but is approximately 15 to 20 events per day per client.</span></span>

-   <span data-ttu-id="1e177-148">이벤트 크기</span><span class="sxs-lookup"><span data-stu-id="1e177-148">Event size.</span></span> <span data-ttu-id="1e177-149">크기는 일반적으로 200 바이트를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-149">The size is typically around 200 bytes.</span></span>

-   <span data-ttu-id="1e177-150">저장 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-150">Storage amount.</span></span> <span data-ttu-id="1e177-151">이벤트를 저장할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-151">The number of days for which events will be stored.</span></span>

<span data-ttu-id="1e177-152">이러한 값을 서로 곱하여 필요한 데이터 저장소의 크기 (바이트)를 계산 하 고 다음을 고려 하는 안전 계수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-152">Multiply these values together to calculate the size of the required data storage in bytes, and then add a safety factor to account for the following:</span></span>

-   <span data-ttu-id="1e177-153">오류가 발생 하 여 짧은 시간 동안 클라이언트에서 많은 수의 이벤트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-153">Errors, which could create a large number of events from a client in a short period of time.</span></span>

-   <span data-ttu-id="1e177-154">데이터베이스 테이블 및 조직 공간.</span><span class="sxs-lookup"><span data-stu-id="1e177-154">Database table and organizational space.</span></span>

<span data-ttu-id="1e177-155">초당 인프라 최적화 (IOPs) 요구 사항에 근사값을 적용 하려면 위의 값을 사용 하 여 일반적인 이벤트 도착 속도를 인스턴스의 클라이언트 수로 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-155">To approximate the infrastructure optimization per second (IOPs) requirement, use the above values, multiplying the typical event arrival rate by the number of clients in the instance.</span></span> <span data-ttu-id="1e177-156">이렇게 하면 하루에 기록할 수 있는 레코드 수가 산출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-156">This yields the number of records that can be written per day.</span></span> <span data-ttu-id="1e177-157">1 초에 한 번 기록 되는 레코드 수를 86400 숫자로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-157">Divide that number by 86,400 to derive the number of records written per second.</span></span> <span data-ttu-id="1e177-158">쓰기 작업을 단일 인프라 최적화 (IO) 작업으로 equated 수 있는 경우이 번호는 필요한 쓰기 IOPs입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-158">If a write operations can be equated with a single infrastructure optimization (IO) operation, this number is the write IOPs required.</span></span> <span data-ttu-id="1e177-159">보고 활동을 위한 버퍼를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-159">Add a buffer to that for reporting activity.</span></span> <span data-ttu-id="1e177-160">이는 결정 하기 어려운 일 이지만 인스턴스와 함께 사용 되는 콘솔 수 및 보고서를 생성 하는 데 사용 되는 빈도에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-160">This is difficult to determine but depends on the number of consoles in use with the instance and the frequency with which they are used to generate reports.</span></span>

### <span data-ttu-id="1e177-161">내결함성은</span><span class="sxs-lookup"><span data-stu-id="1e177-161">Fault Tolerance</span></span>

<span data-ttu-id="1e177-162">MED-V 클라이언트가 실행 되는 경우 서버를 사용할 수 없는 경우 클라이언트에서 이벤트가 백업 되 고 관리 콘솔에서 보고서를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-162">When MED-V client is running, if the server is unavailable, events will be backed up on the client and reports will be unavailable in the management console.</span></span> <span data-ttu-id="1e177-163">[프로젝트 범위 정의](define-the-project-scope.md) 에서 예상 되는 조직의 서비스 수준 기대치를 참조 하 여 결함 허용 SQL Server 인프라의 설계가 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-163">Refer to the organization’s service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to decide whether the design of a fault-tolerant SQL Server infrastructure is necessary.</span></span>

<span data-ttu-id="1e177-164">MED-V는 MSCS 클러스터에서 SQL Server를 실행 하는 데 필요한 기능을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-164">MED-V does not provide support for running SQL Server in an MSCS cluster.</span></span> <span data-ttu-id="1e177-165">웜 대기를 제공 하 고 오류가 발생할 경우 데이터 손실을 방지 하기 위해 로그 전달 구성에 SQL Server를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-165">In order to provide warm standby and to avoid data loss in the event of a failure, you can place SQL Server in a log shipping configuration.</span></span> <span data-ttu-id="1e177-166">로그 전달에 대 한 자세한 내용은 [MICROSOFT SQL Server 2008 가이드 ()의 인프라 계획 및 디자인](https://go.microsoft.com/fwlink/?LinkId=163302) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="1e177-166">For information on log shipping, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide (https://go.microsoft.com/fwlink/?LinkId=163302).</span></span>

## <span data-ttu-id="1e177-167">관리 콘솔 디자인</span><span class="sxs-lookup"><span data-stu-id="1e177-167">Design the Management Console</span></span>


<span data-ttu-id="1e177-168">MED-V 관리 콘솔의 기능 중 일부는 MED-V 클라이언트에 배포 하기 전에 Vm을 테스트 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-168">Part of the functionality of the MED-V management console is to test VMs before they are packed for distribution to MED-V clients.</span></span> <span data-ttu-id="1e177-169">따라서 관리 콘솔은 일반적인 MED-V 클라이언트 컴퓨터의 폼 팩터 등 최대한 비슷한 폼 팩터를 사용 하 여 디자인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-169">Therefore, the management console should be designed with a form factor that resembles, as closely as possible, the form factor of a typical MED-V client machine.</span></span>

<span data-ttu-id="1e177-170">관리 콘솔 응용 프로그램은 MED-V 클라이언트와 함께 설치 되며 Microsoft 기술 자료 문서 974918에서 설명 하는 핫픽스를 사용 하 여 Microsoft Virtual PC2007 SP1을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-170">The management console application is installed together with the MED-V client and uses Microsoft Virtual PC2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918.</span></span> <span data-ttu-id="1e177-171">클라이언트 운영 체제를 사용 해야 합니다. med-v 관리 콘솔은 MED-V 서버와 동일한 시스템에서 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-171">A client operating system must be used; the MED-V management console cannot run on the same system as the MED-V server.</span></span>

<span data-ttu-id="1e177-172">관리 콘솔은 여러 MED-V 서버 인스턴스와 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-172">You cannot share a management console with multiple MED-V server instances.</span></span> <span data-ttu-id="1e177-173">MED-V 서버의 주소는 관리 콘솔의 MED-V 클라이언트를 설치 하는 동안 지정 됩니다. 이 작업은 설치 후에 변경할 수 있지만, 언제 든 지 관리 콘솔이 단일 MED-V 서버 에서만 작동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-173">The address of the MED-V server is specified during the installation of the management console’s MED-V client; this can be changed after installation, but at any time the management console can only work with a single MED-V server.</span></span>

<span data-ttu-id="1e177-174">단일 MED-V 서버에서 여러 관리 콘솔을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-174">You can use multiple management consoles with a single MED-V server.</span></span> <span data-ttu-id="1e177-175">충돌을 방지 하기 위해 한 콘솔에서 MED-V 작업 영역을 변경한 경우 다른 콘솔 사용자에 게 알리는 메커니즘을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-175">To avoid conflicts, a mechanism is available that notifies other console users when one console has made changes to a MED-V workspace.</span></span>

<span data-ttu-id="1e177-176">각 MED-V 인스턴스에 대해 필요한 관리 콘솔의 수와 저장할 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-176">For each MED-V instance, determine how many management consoles will be needed and where they will be placed.</span></span> <span data-ttu-id="1e177-177">관리 콘솔에 사용할 일반적인 MED-V 클라이언트 폼 인수를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e177-177">Select a typical MED-V client form factor to be used for the management console.</span></span>

## <span data-ttu-id="1e177-178">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1e177-178">Related topics</span></span>


[<span data-ttu-id="1e177-179">MED-V 1.0 SP1 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="1e177-179">MED-V 1.0 SP1 Supported Configurations</span></span>](med-v-10-sp1-supported-configurationsmedv-10-sp1.md)

[<span data-ttu-id="1e177-180">클러스터 모드용 MED-V 서버 구성</span><span class="sxs-lookup"><span data-stu-id="1e177-180">Configuring MED-V Server for Cluster Mode</span></span>](configuring-med-v-server-for-cluster-mode.md)

[<span data-ttu-id="1e177-181">MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e177-181">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="1e177-182">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="1e177-182">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





