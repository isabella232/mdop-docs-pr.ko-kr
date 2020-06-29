---
title: App-V 5.1 지원되는 구성
description: App-V 5.1 지원되는 구성
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814724"
---
# <span data-ttu-id="abad0-103">App-V 5.1 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="abad0-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="abad0-104">적용 대상: Windows 10, 버전 1607, Window 서버 2019; Windows Server 2016 Windows Server 2012 R2 Windows Server 2012 Windows Server 2008 R2 (확장 보안 업데이트)</span><span class="sxs-lookup"><span data-stu-id="abad0-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="abad0-105">이 항목에서는 환경에서 Microsoft App-v (Application Virtualization) 5.1를 설치 하 고 실행 하기 위한 요구 사항을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="abad0-106">앱-V 서버 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-106">App-V Server system requirements</span></span>

<span data-ttu-id="abad0-107">이 섹션에는 모든 App-v 서버 구성 요소에 대 한 운영 체제 및 하드웨어 요구 사항이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="abad0-108">지원 되지 않는 앱-V 5.1 서버 시나리오</span><span class="sxs-lookup"><span data-stu-id="abad0-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="abad0-109">App-v 5.1 서버는 다음 시나리오를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="abad0-110">Microsoft Windows Server Core를 실행 하는 컴퓨터에 배포</span><span class="sxs-lookup"><span data-stu-id="abad0-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="abad0-111">이전 버전의 App-v 5.1 서버 구성 요소를 실행 하는 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="abad0-112">App-v 4.5 경량 스트리밍 서버 (LWS) 서버만을 사용 하 여 App-v 5.1를 나란히 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="abad0-113">앱이 app-v를 통해 나란히 배포 됨-V 4.5 Application Virtualization 관리 서비스 (HWS) 서버는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="abad0-114">Microsoft SQL Server Express edition을 실행 하는 컴퓨터에 배포</span><span class="sxs-lookup"><span data-stu-id="abad0-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="abad0-115">도메인 컨트롤러에 배포.</span><span class="sxs-lookup"><span data-stu-id="abad0-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="abad0-116">짧은 경로.</span><span class="sxs-lookup"><span data-stu-id="abad0-116">Short paths.</span></span> <span data-ttu-id="abad0-117">짧은 경로를 사용할 계획 이라면 새 볼륨을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="abad0-118">관리 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-118">Management server operating system requirements</span></span>

<span data-ttu-id="abad0-119">다음 표에는 App-v 5.1 관리 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="abad0-120">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="abad0-121">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="abad0-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="abad0-122">자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="abad0-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="abad0-123">운영 체제</span><span class="sxs-lookup"><span data-stu-id="abad0-123">Operating System</span></span>                 | <span data-ttu-id="abad0-124">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-124">Service Pack</span></span> | <span data-ttu-id="abad0-125">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="abad0-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="abad0-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="abad0-127">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-127">64-bit</span></span>       |
| <span data-ttu-id="abad0-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="abad0-129">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-129">64-bit</span></span>       |
| <span data-ttu-id="abad0-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="abad0-131">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-131">64-bit</span></span>       |
| <span data-ttu-id="abad0-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="abad0-133">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-133">64-bit</span></span>       |
| <span data-ttu-id="abad0-134">Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates)</span><span class="sxs-lookup"><span data-stu-id="abad0-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="abad0-135">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-135">SP1</span></span>     |        <span data-ttu-id="abad0-136">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-136">64-bit</span></span>       |
 

<span data-ttu-id="abad0-137">**중요**  원격 데스크톱 공유 (RDS)를 사용 하도록 설정한 컴퓨터에 관리 서버 역할을 배포 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="abad0-138">관리 서버 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="abad0-139">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="abad0-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="abad0-140">RAM-1GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="abad0-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="abad0-141">디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="abad0-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="abad0-142">관리 서버 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-142">Management server database requirements</span></span>

<span data-ttu-id="abad0-143">다음 표에는 App-v 5.1 관리 데이터베이스 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abad0-144">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="abad0-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="abad0-145">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="abad0-146">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="abad0-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="abad0-148">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="abad0-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="abad0-150">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-151">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-152">SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-153">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-154">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="abad0-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-155">SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-156">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-157">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-158">SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-159">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-161">이상을</span><span class="sxs-lookup"><span data-stu-id="abad0-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-162">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="abad0-163">SQL server 2016 이상을 사용 하는 사용자 구성 파일에 대 한 자세한 내용은 [지원 문서](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="abad0-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="abad0-164">서버 운영 체제 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="abad0-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="abad0-165">다음 표에는 App-v 5.1 게시 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="abad0-166">운영 체제</span><span class="sxs-lookup"><span data-stu-id="abad0-166">Operating System</span></span>                 | <span data-ttu-id="abad0-167">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-167">Service Pack</span></span> | <span data-ttu-id="abad0-168">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="abad0-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="abad0-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="abad0-170">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-170">64-bit</span></span>       |
| <span data-ttu-id="abad0-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="abad0-172">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-172">64-bit</span></span>       |
| <span data-ttu-id="abad0-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="abad0-174">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-174">64-bit</span></span>       |
| <span data-ttu-id="abad0-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="abad0-176">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-176">64-bit</span></span>       |
| <span data-ttu-id="abad0-177">Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates)</span><span class="sxs-lookup"><span data-stu-id="abad0-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="abad0-178">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-178">SP1</span></span>     |        <span data-ttu-id="abad0-179">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="abad0-180">서버 하드웨어 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="abad0-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="abad0-181">App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="abad0-182">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="abad0-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="abad0-183">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="abad0-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="abad0-184">디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="abad0-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="abad0-185">보고 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="abad0-186">다음 표에는 App-v 5.1 Reporting server 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="abad0-187">운영 체제</span><span class="sxs-lookup"><span data-stu-id="abad0-187">Operating System</span></span>                 | <span data-ttu-id="abad0-188">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-188">Service Pack</span></span> | <span data-ttu-id="abad0-189">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="abad0-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="abad0-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="abad0-191">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-191">64-bit</span></span>       |
| <span data-ttu-id="abad0-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="abad0-193">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-193">64-bit</span></span>       |
| <span data-ttu-id="abad0-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="abad0-195">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-195">64-bit</span></span>       |
| <span data-ttu-id="abad0-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="abad0-197">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-197">64-bit</span></span>       |
| <span data-ttu-id="abad0-198">Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates)</span><span class="sxs-lookup"><span data-stu-id="abad0-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="abad0-199">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-199">SP1</span></span>     |        <span data-ttu-id="abad0-200">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="abad0-201">보고 서버 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="abad0-202">App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="abad0-203">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="abad0-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="abad0-204">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="abad0-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="abad0-205">디스크 공간-200mb 사용 가능한 하드 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="abad0-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="abad0-206">보고 서버 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-206">Reporting server database requirements</span></span>

<span data-ttu-id="abad0-207">다음 표에는 App-v 5.1 보고 데이터베이스 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abad0-208">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="abad0-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="abad0-209">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="abad0-210">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="abad0-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="abad0-212">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-213">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-214">SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-215">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-216">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="abad0-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-217">SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-218">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-219">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-220">SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-221">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-223">이상을</span><span class="sxs-lookup"><span data-stu-id="abad0-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-224">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="abad0-225">App-v 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-225">App-V client system requirements</span></span>

<span data-ttu-id="abad0-226">다음 표에는 App-v 5.1 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="abad0-227">Windows 10 예정일 릴리스 (라고도 함 1607 버전)를 사용 하는 경우 App-v 클라이언트가 box에 있으며, 이전 버전의 App-v 클라이언트에 대 한 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abad0-228">운영 체제</span><span class="sxs-lookup"><span data-stu-id="abad0-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="abad0-229">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="abad0-230">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-231">Microsoft Windows10 (1607 이전 버전)</span><span class="sxs-lookup"><span data-stu-id="abad0-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="abad0-232">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="abad0-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="abad0-234">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-235">Windows7</span><span class="sxs-lookup"><span data-stu-id="abad0-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-236">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-237">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="abad0-238">다음 App-v 클라이언트 설치 시나리오가 지원 되지 않습니다 (언급 된 경우 제외).</span><span class="sxs-lookup"><span data-stu-id="abad0-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="abad0-239">Windows Server를 실행 하는 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="abad0-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="abad0-240">App-V 4.6 SP1 또는 이전 버전을 실행 하는 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="abad0-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="abad0-241">앱-V 5.1 원격 데스크톱 서비스 클라이언트는 RDS 사용 서버에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="abad0-242">App-v 클라이언트 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-242">App-V client hardware requirements</span></span>

<span data-ttu-id="abad0-243">다음 목록에는 App-v 5.1 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="abad0-244">프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="abad0-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="abad0-245">RAM (1 GB (32 비트) 또는 2gb (64 비트)</span><span class="sxs-lookup"><span data-stu-id="abad0-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="abad0-246">Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="abad0-247">원격 데스크톱 서비스 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="abad0-248">다음 표에는 RDS (원격 데스크톱 서비스) 클라이언트 설치 5.1에 지원 되는 운영 체제 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="abad0-249">운영 체제</span><span class="sxs-lookup"><span data-stu-id="abad0-249">Operating System</span></span>                 | <span data-ttu-id="abad0-250">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-250">Service Pack</span></span> | <span data-ttu-id="abad0-251">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="abad0-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="abad0-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="abad0-253">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-253">64-bit</span></span>       |
| <span data-ttu-id="abad0-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="abad0-255">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-255">64-bit</span></span>       |
| <span data-ttu-id="abad0-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="abad0-257">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-257">64-bit</span></span>       |
| <span data-ttu-id="abad0-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="abad0-259">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-259">64-bit</span></span>       |
| <span data-ttu-id="abad0-260">Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates)</span><span class="sxs-lookup"><span data-stu-id="abad0-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="abad0-261">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-261">SP1</span></span>     |        <span data-ttu-id="abad0-262">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-262">64-bit</span></span>       |

### <span data-ttu-id="abad0-263">원격 데스크톱 서비스 클라이언트 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="abad0-264">App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="abad0-265">프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서</span><span class="sxs-lookup"><span data-stu-id="abad0-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="abad0-266">RAM-2GB RAM (64 비트)</span><span class="sxs-lookup"><span data-stu-id="abad0-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="abad0-267">디스크 공간-200mb 사용 가능한 하드 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="abad0-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="abad0-268">Sequencer 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-268">Sequencer system requirements</span></span>

<span data-ttu-id="abad0-269">다음 표에는 App-v 5.1 Sequencer 설치에 지원 되는 운영 체제 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="abad0-270">운영 체제</span><span class="sxs-lookup"><span data-stu-id="abad0-270">Operating System</span></span>                 | <span data-ttu-id="abad0-271">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="abad0-271">Service Pack</span></span> | <span data-ttu-id="abad0-272">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="abad0-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="abad0-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="abad0-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="abad0-274">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-274">64-bit</span></span>       |
| <span data-ttu-id="abad0-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abad0-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="abad0-276">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-276">64-bit</span></span>       |
| <span data-ttu-id="abad0-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="abad0-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="abad0-278">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-278">64-bit</span></span>       |
| <span data-ttu-id="abad0-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abad0-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="abad0-280">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-280">64-bit</span></span>       |
| <span data-ttu-id="abad0-281">Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates)</span><span class="sxs-lookup"><span data-stu-id="abad0-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="abad0-282">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-282">SP1</span></span>     |        <span data-ttu-id="abad0-283">64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-283">64-bit</span></span>       |
| <span data-ttu-id="abad0-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="abad0-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="abad0-285">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="abad0-286">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="abad0-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="abad0-287">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="abad0-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="abad0-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="abad0-289">SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-289">SP1</span></span>     | <span data-ttu-id="abad0-290">32비트 및 64비트</span><span class="sxs-lookup"><span data-stu-id="abad0-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="abad0-291">시퀀서 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="abad0-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="abad0-292">하드웨어 요구 사항에 대해서는 Windows 또는 Windows Server 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="abad0-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="abad0-293">앱-V는 추가 하드웨어 요구 사항을 추가 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="abad0-294">지원 되는 버전의 System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="abad0-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="abad0-295">App-v 클라이언트는 다음 버전의 System Center Configuration Manager를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="abad0-296">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="abad0-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="abad0-297">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="abad0-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="abad0-298">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="abad0-299">다음 App-v 및 System Center Configuration Manager 버전 매트릭스는 앱-V 및 구성 관리자의 공식적으로 지원 되는 조합을 모두 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="abad0-300">앱-V 4.5 및 4.6에서 기본 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="abad0-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abad0-301">App-V 버전</span><span class="sxs-lookup"><span data-stu-id="abad0-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="abad0-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="abad0-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="abad0-303">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="abad0-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="abad0-304">System Center 2012 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="abad0-305">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="abad0-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="abad0-306">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="abad0-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="abad0-307">System Center 2012 Configuration Manager SP2</span><span class="sxs-lookup"><span data-stu-id="abad0-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="abad0-308">System Center Configuration Manager 버전 1511</span><span class="sxs-lookup"><span data-stu-id="abad0-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abad0-309">App-v 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="abad0-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-310">MSI-래퍼만</span><span class="sxs-lookup"><span data-stu-id="abad0-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-311">아니오</span><span class="sxs-lookup"><span data-stu-id="abad0-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-312">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="abad0-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="abad0-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-314">예</span><span class="sxs-lookup"><span data-stu-id="abad0-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-315">예</span><span class="sxs-lookup"><span data-stu-id="abad0-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-316">예</span><span class="sxs-lookup"><span data-stu-id="abad0-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abad0-317">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="abad0-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-318">MSI-래퍼만</span><span class="sxs-lookup"><span data-stu-id="abad0-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-319">아니오</span><span class="sxs-lookup"><span data-stu-id="abad0-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-320">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="abad0-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="abad0-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-322">예</span><span class="sxs-lookup"><span data-stu-id="abad0-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-323">예</span><span class="sxs-lookup"><span data-stu-id="abad0-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="abad0-324">예</span><span class="sxs-lookup"><span data-stu-id="abad0-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="abad0-325">Configuration Manager를 App-v와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager를 사용 하 여 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="abad0-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="abad0-326">관련 항목</span><span class="sxs-lookup"><span data-stu-id="abad0-326">Related topics</span></span>

[<span data-ttu-id="abad0-327">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="abad0-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="abad0-328">App-V 5.1 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="abad0-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
