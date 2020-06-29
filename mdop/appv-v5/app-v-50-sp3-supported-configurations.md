---
title: App-V 5.0 SP3 지원되는 구성
description: App-V 5.0 SP3 지원되는 구성
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814793"
---
# <span data-ttu-id="c1643-103">App-V 5.0 SP3 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="c1643-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="c1643-104">이 항목에서는 환경에서 Microsoft App-v (Application Virtualization) 5.0 SP3을 설치 하 고 실행 하기 위한 요구 사항을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="c1643-105">앱-V 서버 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-105">App-V Server system requirements</span></span>


<span data-ttu-id="c1643-106">이 섹션에는 모든 App-v 서버 구성 요소에 대 한 운영 체제 및 하드웨어 요구 사항이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="c1643-107">지원 되지 않는 앱-V 5.0 SP3 서버 시나리오</span><span class="sxs-lookup"><span data-stu-id="c1643-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="c1643-108">App-v 5.0 SP3 서버는 다음 시나리오를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="c1643-109">Microsoft Windows Server Core를 실행 하는 컴퓨터에 배포</span><span class="sxs-lookup"><span data-stu-id="c1643-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="c1643-110">이전 버전의 App-v 5.0 SP3 서버 구성 요소를 실행 하는 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="c1643-111">App-v 4.5 경량 스트리밍 서버 (LWS) 서버를 사용 하 여 App-v 5.0 SP3을 나란히 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="c1643-112">앱이 app-v를 통해 나란히 배포 됨-V 4.5 Application Virtualization 관리 서비스 (HWS) 서버는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="c1643-113">Microsoft SQL Server Express edition을 실행 하는 컴퓨터에 배포</span><span class="sxs-lookup"><span data-stu-id="c1643-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="c1643-114">관리 서버 데이터베이스 또는 보고 데이터베이스의 원격 배포</span><span class="sxs-lookup"><span data-stu-id="c1643-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="c1643-115">Microsoft SQL Server를 실행 하는 컴퓨터에서 직접 설치 관리자를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="c1643-116">도메인 컨트롤러에 배포.</span><span class="sxs-lookup"><span data-stu-id="c1643-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="c1643-117">짧은 경로.</span><span class="sxs-lookup"><span data-stu-id="c1643-117">Short paths.</span></span> <span data-ttu-id="c1643-118">짧은 경로를 사용할 계획 이라면 새 볼륨을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="c1643-119">관리 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-119">Management server operating system requirements</span></span>

<span data-ttu-id="c1643-120">다음 표에는 App-v 5.0 SP3 관리 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="c1643-121">**참고**  Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="c1643-122">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1643-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="c1643-123">자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1643-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-124">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c1643-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c1643-125">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-126">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-128">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1643-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-130">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-132">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-133">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c1643-134">**중요**  원격 데스크톱 공유 (RDS)를 사용 하도록 설정한 컴퓨터에 관리 서버 역할을 배포 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="c1643-135">관리 서버 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="c1643-136">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="c1643-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="c1643-137">RAM-1GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="c1643-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="c1643-138">디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="c1643-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="c1643-139">관리 서버 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-139">Management server database requirements</span></span>

<span data-ttu-id="c1643-140">다음 표에는 App-v 5.0 SP3 관리 데이터베이스 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-141">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="c1643-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="c1643-142">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-143">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-144">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="c1643-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-145">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-146">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1643-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-147">SP2</span><span class="sxs-lookup"><span data-stu-id="c1643-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-148">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-150">이상을</span><span class="sxs-lookup"><span data-stu-id="c1643-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-151">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c1643-152">서버 운영 체제 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="c1643-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="c1643-153">다음 표에는 App-v 5.0 SP3 게시 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-154">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c1643-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c1643-155">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-156">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-158">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1643-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-160">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-162">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-163">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="c1643-164">서버 하드웨어 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="c1643-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="c1643-165">App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="c1643-166">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="c1643-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="c1643-167">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="c1643-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="c1643-168">디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="c1643-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="c1643-169">보고 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="c1643-170">다음 표에는 App-v 5.0 SP3 Reporting server 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-171">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c1643-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c1643-172">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-173">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-175">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1643-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-177">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-179">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-180">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="c1643-181">보고 서버 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="c1643-182">App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="c1643-183">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="c1643-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="c1643-184">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="c1643-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="c1643-185">디스크 공간-200mb 사용 가능한 하드 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="c1643-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="c1643-186">보고 서버 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-186">Reporting server database requirements</span></span>

<span data-ttu-id="c1643-187">다음 표에는 App-v 5.0 SP3 보고 데이터베이스 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-188">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="c1643-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="c1643-189">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-190">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-191">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="c1643-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-192">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-193">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1643-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-194">SP2</span><span class="sxs-lookup"><span data-stu-id="c1643-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-195">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-197">이상을</span><span class="sxs-lookup"><span data-stu-id="c1643-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-198">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="c1643-199">App-v 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-199">App-V client system requirements</span></span>


<span data-ttu-id="c1643-200">다음 표에는 App-v 5.0 SP3 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-201">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c1643-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c1643-202">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-203">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c1643-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-205">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-206">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="c1643-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-207">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-208">Windows7</span><span class="sxs-lookup"><span data-stu-id="c1643-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-209">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-210">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c1643-211">다음 App-v 클라이언트 설치 시나리오가 지원 되지 않습니다 (언급 된 경우 제외).</span><span class="sxs-lookup"><span data-stu-id="c1643-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="c1643-212">Windows Server를 실행 하는 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="c1643-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="c1643-213">App-V 4.6 SP1 또는 이전 버전을 실행 하는 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="c1643-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="c1643-214">앱-V 5.0 SP3 원격 데스크톱 서비스 클라이언트는 RDS 사용 서버에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="c1643-215">App-v 클라이언트 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-215">App-V client hardware requirements</span></span>

<span data-ttu-id="c1643-216">다음 목록에는 App-v 5.0 SP3 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="c1643-217">프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="c1643-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="c1643-218">RAM (1 GB (32 비트) 또는 2gb (64 비트)</span><span class="sxs-lookup"><span data-stu-id="c1643-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="c1643-219">Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="c1643-220">원격 데스크톱 서비스 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="c1643-221">다음 표에는 App-v 5.0 SP3 원격 데스크톱 서비스 (RDS) 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-222">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c1643-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c1643-223">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-224">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-226">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1643-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-228">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-230">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-231">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c1643-232">원격 데스크톱 서비스 클라이언트 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="c1643-233">App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="c1643-234">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="c1643-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="c1643-235">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="c1643-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="c1643-236">디스크 공간-200mb 사용 가능한 하드 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="c1643-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="c1643-237">Sequencer 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-237">Sequencer system requirements</span></span>


<span data-ttu-id="c1643-238">다음 표에는 App-v 5.0 SP3 Sequencer 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1643-239">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c1643-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c1643-240">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c1643-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c1643-241">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c1643-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="c1643-243">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="c1643-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-245">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-246">Microsoft Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1643-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-247">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-248">64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c1643-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-250">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1643-251">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="c1643-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1643-252">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1643-253">Microsoft Windows7</span><span class="sxs-lookup"><span data-stu-id="c1643-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-254">SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1643-255">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="c1643-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c1643-256">시퀀서 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c1643-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="c1643-257">하드웨어 요구 사항에 대해서는 Windows 또는 Windows Server 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1643-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="c1643-258">앱-V는 추가 하드웨어 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="c1643-259">지원 되는 버전의 System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c1643-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="c1643-260">App-v 클라이언트는 다음 버전의 System Center Configuration Manager를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1643-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="c1643-261">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="c1643-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="c1643-262">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c1643-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="c1643-263">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="c1643-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="c1643-264">Configuration Manager를 App-v와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager를 사용 하 여 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1643-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="c1643-265">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c1643-265">Related topics</span></span>


[<span data-ttu-id="c1643-266">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="c1643-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="c1643-267">App-V 5.0 SP3 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="c1643-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





