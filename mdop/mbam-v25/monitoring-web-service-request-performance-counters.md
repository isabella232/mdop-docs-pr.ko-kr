---
title: 웹 서비스 요청 성능 카운터 모니터링
description: 웹 서비스 요청 성능 카운터 모니터링
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823878"
---
# <span data-ttu-id="38999-103">웹 서비스 요청 성능 카운터 모니터링</span><span class="sxs-lookup"><span data-stu-id="38999-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="38999-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음 웹 서비스로 전송 되는 요청의 성능을 기록 하는 성능 카운터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="38999-105">**StatusReportingService** – 준수 상태에 대 한 요청을 수신 하는 서비스</span><span class="sxs-lookup"><span data-stu-id="38999-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="38999-106">**CoreService** – 키 복구 시도에 대 한 요청을 수신 하는 서비스</span><span class="sxs-lookup"><span data-stu-id="38999-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="38999-107">MBAM이 제공 하는 성능 카운터</span><span class="sxs-lookup"><span data-stu-id="38999-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="38999-108">MBAM은 해당 StatusReportingService 및 CoreService 웹 서비스에서 구현 하는 각 공용 메서드에 대해 다음과 같은 성능 카운터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="38999-109">성능 카운터 형식</span><span class="sxs-lookup"><span data-stu-id="38999-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="38999-110">설명</span><span class="sxs-lookup"><span data-stu-id="38999-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38999-111">총 요청 수</span><span class="sxs-lookup"><span data-stu-id="38999-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="38999-112">서버를 시작 하거나 다시 시작할 때 0부터 시작 하는 증분 수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="38999-113">시스템 활동의 전체 보기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="38999-114">서버의 상태를 확인 하 고 지정 된 기간 동안 카운터가 지속적으로 증가 하는지 확인 하기 위해 자동 도구를 통해 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38999-115">초당 요청 수</span><span class="sxs-lookup"><span data-stu-id="38999-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="38999-116">Mbam 서버의 현재 처리량을 MBAM 클라이언트 베이스를 지원 하는 것으로 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="38999-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="38999-117">사이트 관리자가 다음을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="38999-118">MBAM 클라이언트 수 및 보고 빈도를 기준으로 초당 평균 요청 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="38999-119">초당 계산 된 평균 요청 수와 광범위 하 게 연관 되는 초당 요청 수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="38999-120">상당한 분산으로 인해 MBAM 클라이언트가 클라이언트 기반 백분율에 설치 되지 않았거나 MBAM 그룹 정책 개체가 성공적으로 배포 되지 않았음을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38999-121">요청 기간</span><span class="sxs-lookup"><span data-stu-id="38999-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="38999-122">요청 기간 (밀리초)을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="38999-123">이 카운터는 각 요청의 기간에 따라 업데이트 되지만, Windows 성능 모니터는 정기적으로 (일반적으로 매 초)에만 해당 값의 가변성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="38999-124">이 때문에 성능 모니터에 표시 되는 평균값을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="38999-125">성능 카운터 결과 및 권장 사항</span><span class="sxs-lookup"><span data-stu-id="38999-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="38999-126">여분 용량으로 새 MBAM 클라이언트를 MBAM 서버에 추가 하는 경우 초당 요청 수가 증가 하는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="38999-127">이러한 증가는 새 클라이언트 컴퓨터 수에 비례하여 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38999-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="38999-128">평균 요청 기간은 상대적으로 정적으로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38999-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="38999-129">서버가 최대 용량에 도달 함에 따라 초당 요청 수는 수준 아웃을 시작 하 고, 평균 요청 기간이 길어질 때까지 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38999-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="38999-130">MBAM 서버가 클라이언트 기반을 지원할 수 있는지 걱정 하는 경우 다양 한 클라이언트 컴퓨터 컬렉션에서 MBAM을 배포 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="38999-131">클라이언트 컴퓨터의 각 컬렉션에 MBAM을 배포할 때 성능 카운터의 스냅숏을 만들어 각 새 클라이언트 컬렉션에 배포 하는 상대적인 영향을 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="38999-132">초당 요청 수가 수준 끄기를 시작 하 고 평균 요청 기간이 늘어나면 다음 중 하나를 수행 하 여 MBAM 서버 인프라를 향상 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="38999-133">MBAM 데이터베이스를 전용 Microsoft SQL Server 또는 SQL Server 클러스터로 이동</span><span class="sxs-lookup"><span data-stu-id="38999-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="38999-134">여러 IIS (인터넷 정보 서비스) 웹 서버에 걸친 MBAM 분산</span><span class="sxs-lookup"><span data-stu-id="38999-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="38999-135">보다 강력한 서버 하드웨어에 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="38999-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="38999-136">성능 카운터 보기</span><span class="sxs-lookup"><span data-stu-id="38999-136">Viewing performance counters</span></span>


<span data-ttu-id="38999-137">MBAM 성능 카운터를 보는 데 권장 되는 도구는 Windows와 함께 제공 되는 Windows 성능 모니터입니다.</span><span class="sxs-lookup"><span data-stu-id="38999-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="38999-138">Windows PowerShell을 사용 하는 경우 Windows PowerShell **enable-webapplication** cmdlet에서 자동으로 등록 되므로 표시 하기 전에 카운터를 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="38999-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="38999-139">성능 카운터를 보는 방법에 대 한 자세한 지침은 [MBAM 성능 카운터를 보는 방법을](https://go.microsoft.com/fwlink/?LinkId=393457)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="38999-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="38999-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="38999-140">Related topics</span></span>


[<span data-ttu-id="38999-141">MBAM 2.5 유지 관리</span><span class="sxs-lookup"><span data-stu-id="38999-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="38999-142">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="38999-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="38999-143">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="38999-144">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="38999-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>


