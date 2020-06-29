---
title: App-V 5.0 지원되는 구성
description: App-V 5.0 지원되는 구성
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814788"
---
# <span data-ttu-id="2ff75-103">App-V 5.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="2ff75-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="2ff75-104">이 항목에서는 환경에서 Microsoft Application Virtualization (App-v) 5.0을 설치 하 고 실행 하는 데 필요한 요구 사항을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="2ff75-105">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-105">Important</span></span>**  
<span data-ttu-id="2ff75-106">**이 문서의 지원 되는 구성은 app-v 5.0에만 적용**됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="2ff75-107">App-v 5.0 서비스 팩에 적용 되는 지원 되는 구성에 대해서는 다음 웹 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="2ff75-108">App-V 5.0 SP1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="2ff75-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="2ff75-109">App-V 5.0 SP2 정보</span><span class="sxs-lookup"><span data-stu-id="2ff75-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="2ff75-110">App-V 5.0 SP3 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="2ff75-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="2ff75-111">앱-V 5.0 서버 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="2ff75-112">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-112">Important</span></span>**  
<span data-ttu-id="2ff75-113">App-v 5.0 서버는 다음 시나리오를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="2ff75-114">Microsoft Windows Server Core를 실행 하는 컴퓨터에 배포</span><span class="sxs-lookup"><span data-stu-id="2ff75-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="2ff75-115">이전 버전의 App-v 5.0 서버 구성 요소를 실행 하는 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="2ff75-116">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-116">Note</span></span>**  
    <span data-ttu-id="2ff75-117">App-v 4.5 경량 스트리밍 서버 (LWS) 서버를 사용 하 여 App-v 5.0를 나란히 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="2ff75-118">App-v 5.0 for HWS (Application Virtualization Management Service) 서버를 4.5 나란히 배치 하는 작업은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="2ff75-119">Microsoft SQL Server Express edition을 실행 하는 컴퓨터에 배포</span><span class="sxs-lookup"><span data-stu-id="2ff75-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="2ff75-120">관리 서버 데이터베이스 또는 보고 데이터베이스의 원격 배포</span><span class="sxs-lookup"><span data-stu-id="2ff75-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="2ff75-121">Microsoft SQL을 실행 하는 컴퓨터에서 설치 관리자를 직접 실행 하 여 데이터베이스를 성공적으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="2ff75-122">도메인 컨트롤러에 배포.</span><span class="sxs-lookup"><span data-stu-id="2ff75-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="2ff75-123">짧은 경로는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-123">Short paths are not supported.</span></span> <span data-ttu-id="2ff75-124">짧은 경로를 사용할 계획인 경우 새 볼륨을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="2ff75-125">관리 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-125">Management Server operating system requirements</span></span>

<span data-ttu-id="2ff75-126">다음 표에는 App-v 5.0 관리 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="2ff75-127">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-127">Note</span></span>**  
<span data-ttu-id="2ff75-128">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff75-129">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff75-130">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-131">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2ff75-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2ff75-132">버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff75-133">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2ff75-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2ff75-134">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2ff75-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter 또는 웹 서버)</span><span class="sxs-lookup"><span data-stu-id="2ff75-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-136">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-137">SP1 이상</span><span class="sxs-lookup"><span data-stu-id="2ff75-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-138">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-140">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-142">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-143">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="2ff75-144">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-144">Important</span></span>**  
<span data-ttu-id="2ff75-145">원격 데스크톱 공유 (RDS)를 사용 하도록 설정한 컴퓨터에 관리 서버 역할을 배포 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="2ff75-146">관리 서버 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="2ff75-147">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="2ff75-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="2ff75-148">RAM-1GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="2ff75-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="2ff75-149">디스크 공간-하드 디스크 공간-200mb 사용할 수 있습니다 (콘텐츠 디렉터리는 포함 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="2ff75-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="2ff75-150">서버 운영 체제 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="2ff75-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="2ff75-151">다음 표에는 App-v 5.0 게시 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="2ff75-152">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-152">Note</span></span>**  
<span data-ttu-id="2ff75-153">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff75-154">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff75-155">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-156">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2ff75-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2ff75-157">버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff75-158">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2ff75-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2ff75-159">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2ff75-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter 또는 웹 서버)</span><span class="sxs-lookup"><span data-stu-id="2ff75-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-161">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-162">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-164">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-166">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-167">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="2ff75-168">서버 하드웨어 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="2ff75-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="2ff75-169">프로세서-1.4 GHz 이상.</span><span class="sxs-lookup"><span data-stu-id="2ff75-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="2ff75-170">64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="2ff75-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="2ff75-171">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="2ff75-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="2ff75-172">디스크 공간 – 200mb의 하드 디스크 공간이 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="2ff75-173">콘텐츠 디렉터리 포함 안 함</span><span class="sxs-lookup"><span data-stu-id="2ff75-173">not including content directory</span></span>

### <span data-ttu-id="2ff75-174">보고 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="2ff75-175">다음 표에는 App-v 5.0 reporting server 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="2ff75-176">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-176">Note</span></span>**  
<span data-ttu-id="2ff75-177">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff75-178">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff75-179">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-180">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2ff75-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2ff75-181">버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff75-182">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2ff75-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2ff75-183">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2ff75-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter 또는 웹 서버)</span><span class="sxs-lookup"><span data-stu-id="2ff75-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-185">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-186">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-188">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-190">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-191">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="2ff75-192">보고 서버 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="2ff75-193">프로세서-1.4 GHz 이상.</span><span class="sxs-lookup"><span data-stu-id="2ff75-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="2ff75-194">64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="2ff75-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="2ff75-195">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="2ff75-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="2ff75-196">디스크 공간-200mb 사용 가능한 하드 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="2ff75-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="2ff75-197">SQL Server 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-197">SQL Server database requirements</span></span>

<span data-ttu-id="2ff75-198">다음 표에는 App-v 5.0 데이터베이스 및 서버 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-199">App-v 5.0 서버 유형</span><span class="sxs-lookup"><span data-stu-id="2ff75-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="2ff75-200">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="2ff75-201">버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff75-202">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2ff75-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2ff75-203">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2ff75-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-204">관리/보고</span><span class="sxs-lookup"><span data-stu-id="2ff75-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff75-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="2ff75-206">(표준, 엔터프라이즈, Datacenter 또는 Developer Edition은 다음 기능을 사용 합니다. <strong> 데이터베이스 엔진 서비스 </strong> .</span><span class="sxs-lookup"><span data-stu-id="2ff75-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-207">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-208">관리/보고</span><span class="sxs-lookup"><span data-stu-id="2ff75-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff75-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="2ff75-210">(표준, 엔터프라이즈, Datacenter 또는 Developer Edition은 다음 기능을 사용 합니다. <strong> 데이터베이스 엔진 서비스 </strong> .</span><span class="sxs-lookup"><span data-stu-id="2ff75-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-211">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-212">SP2</span><span class="sxs-lookup"><span data-stu-id="2ff75-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-213">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-214">관리/보고</span><span class="sxs-lookup"><span data-stu-id="2ff75-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-215">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ff75-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="2ff75-216">(표준, 엔터프라이즈, Datacenter 또는 Developer Edition은 다음 기능을 사용 합니다. <strong> 데이터베이스 엔진 서비스 </strong> .</span><span class="sxs-lookup"><span data-stu-id="2ff75-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-217">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="2ff75-218">앱-V 5.0 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="2ff75-219">다음 표에는 App-v 5.0 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="2ff75-220">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-220">Note</span></span>**  
<span data-ttu-id="2ff75-221">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff75-222">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff75-223">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-224">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2ff75-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2ff75-225">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2ff75-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2ff75-226">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2ff75-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ff75-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-228">SP1</span><span class="sxs-lookup"><span data-stu-id="2ff75-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-229">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ff75-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-231">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="2ff75-232">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-232">Important</span></span></strong><br/><p><span data-ttu-id="2ff75-233">Windows 8.1는 앱-V 5.0 SP2 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="2ff75-234">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2ff75-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-235">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2ff75-236">다음 App-v 클라이언트 설치 시나리오가 지원 되지 않습니다 (언급 된 경우 제외).</span><span class="sxs-lookup"><span data-stu-id="2ff75-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="2ff75-237">Windows Server를 실행 하는 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="2ff75-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="2ff75-238">App-v 4.6 SP1 또는 이전 버전을 실행 하는 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="2ff75-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="2ff75-239">앱-V 5.0 원격 데스크톱 서비스 클라이언트는 RDS 사용 서버에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="2ff75-240">클라이언트 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-240">Client hardware requirements</span></span>

<span data-ttu-id="2ff75-241">다음 목록에는 App-v 5.0 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="2ff75-242">프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="2ff75-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="2ff75-243">RAM (1 GB (32 비트) 또는 2gb (64 비트)</span><span class="sxs-lookup"><span data-stu-id="2ff75-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="2ff75-244">Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="2ff75-245">앱-V 5.0 원격 데스크톱 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="2ff75-246">다음 표에는 App-v 5.0 원격 데스크톱 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="2ff75-247">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-247">Note</span></span>**  
<span data-ttu-id="2ff75-248">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff75-249">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff75-250">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="2ff75-251">운영 체제 버전 서비스 팩 Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff75-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="2ff75-252">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-252">R2</span></span>

<span data-ttu-id="2ff75-253">SP1</span><span class="sxs-lookup"><span data-stu-id="2ff75-253">SP1</span></span>

<span data-ttu-id="2ff75-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ff75-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="2ff75-255">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-255">Important</span></span>**  
<span data-ttu-id="2ff75-256">Windows Server 2012 R2는 앱-V 5.0 SP2 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="2ff75-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="2ff75-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="2ff75-258">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-258">R2</span></span>

<span data-ttu-id="2ff75-259">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="2ff75-260">원격 데스크톱 클라이언트 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="2ff75-261">다음 목록에는 App-v 5.0 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="2ff75-262">프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="2ff75-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="2ff75-263">RAM (1 GB (32 비트) 또는 2gb (64 비트)</span><span class="sxs-lookup"><span data-stu-id="2ff75-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="2ff75-264">Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="2ff75-265">앱-V 5.0 Sequencer 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ff75-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="2ff75-266">다음 표에는 App-v 5.0 Sequencer 설치에 지원 되는 운영 체제 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="2ff75-267">참고</span><span class="sxs-lookup"><span data-stu-id="2ff75-267">Note</span></span>**  
<span data-ttu-id="2ff75-268">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff75-269">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff75-270">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-271">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2ff75-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2ff75-272">버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff75-273">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2ff75-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2ff75-274">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2ff75-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ff75-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-276">SP1</span><span class="sxs-lookup"><span data-stu-id="2ff75-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-277">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ff75-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-279">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="2ff75-280">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-280">Important</span></span></strong><br/><p><span data-ttu-id="2ff75-281">Windows 8.1는 앱-V 5.0 SP2 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="2ff75-282">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2ff75-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-283">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff75-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-285">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-286">SP1</span><span class="sxs-lookup"><span data-stu-id="2ff75-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-287">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ff75-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2ff75-289">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="2ff75-290">중요</span><span class="sxs-lookup"><span data-stu-id="2ff75-290">Important</span></span></strong><br/><p><span data-ttu-id="2ff75-291">Windows Server 2012 R2는 앱-V 5.0 SP2 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="2ff75-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ff75-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff75-293">R2</span><span class="sxs-lookup"><span data-stu-id="2ff75-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff75-294">64비트</span><span class="sxs-lookup"><span data-stu-id="2ff75-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="2ff75-295">지원 되는 버전의 System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2ff75-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="2ff75-296">Microsoft System Center 2012 구성 관리자 또는 System Center 2012 R2 구성 관리자를 사용 하 여 App-v 가상 응용 프로그램, 보고 및 기타 기능을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="2ff75-297">다음 표에는 해당 하는 각 App-v 버전에 대해 지원 되는 버전의 구성 관리자가 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ff75-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff75-298">지원 되는 Configuration Manager 버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="2ff75-299">App-V 버전</span><span class="sxs-lookup"><span data-stu-id="2ff75-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff75-300">Microsoft System Center 2012 구성 관리자</span><span class="sxs-lookup"><span data-stu-id="2ff75-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ff75-301">App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2ff75-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="2ff75-302">App-v 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="2ff75-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="2ff75-303">App-v 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="2ff75-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff75-304">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2ff75-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2ff75-305">App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2ff75-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="2ff75-306">App-v 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="2ff75-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="2ff75-307">App-v 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="2ff75-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2ff75-308">Configuration Manager를 App-v와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager를 사용 하 여 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ff75-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="2ff75-309">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2ff75-309">Related topics</span></span>


[<span data-ttu-id="2ff75-310">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="2ff75-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="2ff75-311">App-V 5.0 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="2ff75-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









