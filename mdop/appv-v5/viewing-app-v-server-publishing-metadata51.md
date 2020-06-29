---
title: App-V Server 게시 메타데이터 보기
description: App-V Server 게시 메타데이터 보기
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813233"
---
# <span data-ttu-id="19190-103">App-V Server 게시 메타데이터 보기</span><span class="sxs-lookup"><span data-stu-id="19190-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="19190-104">게시 관련 문제를 해결 하는 데 도움이 될 수 있는 게시 메타 데이터를 보려면이 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="19190-105">이 절차를 사용 하려면 App-v 관리 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="19190-106">이 문서에는 다음 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19190-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="19190-107">게시 메타 데이터 보기에 대 한 앱-V 5.1 요구 사항</span><span class="sxs-lookup"><span data-stu-id="19190-107">App-V 5.1 requirements for viewing publishing metadata</span></span>](#bkmk-51-reqs-pub-meta)

-   [<span data-ttu-id="19190-108">게시 메타 데이터를 보는 데 사용할 구문</span><span class="sxs-lookup"><span data-stu-id="19190-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="19190-109">클라이언트 운영 체제 및 버전에 대 한 쿼리 값</span><span class="sxs-lookup"><span data-stu-id="19190-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="19190-110">게시 메타 데이터의 정의</span><span class="sxs-lookup"><span data-stu-id="19190-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a><span data-ttu-id="19190-111">게시 메타 데이터 보기에 대 한 앱-V 5.1 요구 사항</span><span class="sxs-lookup"><span data-stu-id="19190-111">App-V 5.1 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="19190-112">App-v 5.1의 경우 메타 데이터에 대해 App-v 게시 서버를 쿼리하면 주소에 다음 값을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-112">In App-V 5.1, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19190-113">값</span><span class="sxs-lookup"><span data-stu-id="19190-113">Value</span></span></th>
<th align="left"><span data-ttu-id="19190-114">추가적인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="19190-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19190-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="19190-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19190-116"><strong>쿼리에서 clientversion 매개 변수를 생략 하면 </strong> 메타 데이터는 APP-V 5.0 SP3의 새로운 기능을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the features that were new in App-V 5.0 SP3.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19190-117">ClientOS</span><span class="sxs-lookup"><span data-stu-id="19190-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19190-118">패키지를 시퀀싱 할 때 특정 클라이언트 운영 체제를 선택 하는 경우에만이 값을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="19190-119">기본값 (모든 운영 체제)을 선택 하는 경우 쿼리에이 값을 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="19190-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="19190-120"><strong>쿼리에서 clientos 매개 변수를 생략 하면 </strong> 모든 운영 체제를 지원 하도록 시퀀싱 된 패키지만 메타 데이터에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19190-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="19190-121">게시 메타 데이터를 보기 위한 쿼리 구문</span><span class="sxs-lookup"><span data-stu-id="19190-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="19190-122">다음 표에서는 구문 및 쿼리 예제를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19190-123">앱 버전-V</span><span class="sxs-lookup"><span data-stu-id="19190-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="19190-124">쿼리 구문</span><span class="sxs-lookup"><span data-stu-id="19190-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="19190-125">매개 변수 설명</span><span class="sxs-lookup"><span data-stu-id="19190-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="19190-126">예</span><span class="sxs-lookup"><span data-stu-id="19190-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-127">App-v 5.0 SP3 및 App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="19190-127">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19190-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19190-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="19190-129">설명</span><span class="sxs-lookup"><span data-stu-id="19190-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="19190-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-131">App-v 게시 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19190-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-132">&lt;게시 포트 #&gt;</span><span class="sxs-lookup"><span data-stu-id="19190-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-133">게시 서버를 구성할 때 정의한 App-v 게시 서버 포트</span><span class="sxs-lookup"><span data-stu-id="19190-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="19190-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-135">App-V 클라이언트의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="19190-135">Version of the App-V client.</span></span> <span data-ttu-id="19190-136">사용할 올바른 값에 대해서는 다음 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19190-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-137">ClientOS = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="19190-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-138">App-v 클라이언트를 실행 하는 컴퓨터의 운영 체제입니다.</span><span class="sxs-lookup"><span data-stu-id="19190-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="19190-139">사용할 올바른 값에 대해서는 다음 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19190-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="19190-140">App-v 클라이언트에서 게시 서버의 이름과 포트 번호 (http:// &lt; pubserver &gt; : &lt; Publishing 포트 #)를 가져오려면 &gt; <strong> AppvPublishingServer PowerShell cmdlet의 URL 구성을 참조 하세요 </strong> .</span><span class="sxs-lookup"><span data-stu-id="19190-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="19190-141">예제:</span><span class="sxs-lookup"><span data-stu-id="19190-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="19190-142">"Pubsvr01" 이라는 Windows Server 2012 R2는 게시 서비스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="19190-143">Windows 클라이언트는 Windows 8.1 64 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="19190-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-144">앱-V 5.0-app-v 5.0 SP2를 통해</span><span class="sxs-lookup"><span data-stu-id="19190-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="19190-145">참고</span><span class="sxs-lookup"><span data-stu-id="19190-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="19190-146">ClientVersion </strong> 및 <strong> clientversion </strong> 는 app-v 5.0 SP3 및 app-v 5.1 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19190-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3 and App-V 5.1.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="19190-147">앱-V 5.0 SP3 및 App-v 5.1에 대 한 정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19190-147">See the information for App-V 5.0 SP3 and App-V 5.1.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="19190-148">이 예제에서 "pubsvr01" 라는 Windows Server 2012 R2는 관리 및 게시 서비스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="19190-149">클라이언트 운영 체제 및 버전에 대 한 쿼리 값</span><span class="sxs-lookup"><span data-stu-id="19190-149">Query values for client operating system and version</span></span>


<span data-ttu-id="19190-150">게시 메타 데이터 쿼리에서 사용 중인 클라이언트 운영 체제 및 버전에 해당 하는 문자열 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19190-151">운영 체제</span><span class="sxs-lookup"><span data-stu-id="19190-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="19190-152">아키텍처</span><span class="sxs-lookup"><span data-stu-id="19190-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="19190-153">작동 문자열 문자열 값</span><span class="sxs-lookup"><span data-stu-id="19190-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-154">Windows 10</span><span class="sxs-lookup"><span data-stu-id="19190-154">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-155">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-156">WindowsClient_10 0_x64</span><span class="sxs-lookup"><span data-stu-id="19190-156">WindowsClient_10.0_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-157">Windows 10</span><span class="sxs-lookup"><span data-stu-id="19190-157">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-158">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-159">WindowsClient_10 0_x86</span><span class="sxs-lookup"><span data-stu-id="19190-159">WindowsClient_10.0_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="19190-160">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-161">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-162">WindowsClient_6 2_x64</span><span class="sxs-lookup"><span data-stu-id="19190-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-163">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="19190-163">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-164">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-165">WindowsClient_6 2_x86</span><span class="sxs-lookup"><span data-stu-id="19190-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-166">Windows8</span><span class="sxs-lookup"><span data-stu-id="19190-166">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-167">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-168">WindowsClient_6 2_x64</span><span class="sxs-lookup"><span data-stu-id="19190-168">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-169">Windows8</span><span class="sxs-lookup"><span data-stu-id="19190-169">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-170">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-171">WindowsClient_6 2_x86</span><span class="sxs-lookup"><span data-stu-id="19190-171">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="19190-172">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-173">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-174">WindowsServer_6 2_x64</span><span class="sxs-lookup"><span data-stu-id="19190-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-175">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="19190-175">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-176">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-177">WindowsServer_6 2_x86</span><span class="sxs-lookup"><span data-stu-id="19190-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19190-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-179">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-180">WindowsServer_6 2_x64</span><span class="sxs-lookup"><span data-stu-id="19190-180">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19190-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-182">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-183">WindowsServer_6 2_x86</span><span class="sxs-lookup"><span data-stu-id="19190-183">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19190-184">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-185">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-186">WindowsClient_6 1_x64</span><span class="sxs-lookup"><span data-stu-id="19190-186">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-187">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19190-187">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-188">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-189">WindowsClient_6 1_x86</span><span class="sxs-lookup"><span data-stu-id="19190-189">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19190-190">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19190-190">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-191">64비트</span><span class="sxs-lookup"><span data-stu-id="19190-191">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-192">WindowsServer_6 1_x64</span><span class="sxs-lookup"><span data-stu-id="19190-192">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19190-193">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19190-193">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-194">32비트</span><span class="sxs-lookup"><span data-stu-id="19190-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="19190-195">WindowsServer_6 1_x86</span><span class="sxs-lookup"><span data-stu-id="19190-195">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="19190-196">게시 메타 데이터의 정의</span><span class="sxs-lookup"><span data-stu-id="19190-196">Definition of publishing metadata</span></span>


<span data-ttu-id="19190-197">패키지가 App-v 클라이언트를 실행 하는 컴퓨터에 게시 되 면 게시 되는 패키지 및 연결 그룹을 나타내는 메타 데이터가 해당 컴퓨터로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19190-197">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="19190-198">App-v 클라이언트는 다음에 대 한 두 개의 개별 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19190-198">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="19190-199">클라이언트 컴퓨터에 부여 되는 패키지 및 연결 그룹</span><span class="sxs-lookup"><span data-stu-id="19190-199">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="19190-200">현재 사용자에 게 부여 되는 패키지 및 연결 그룹</span><span class="sxs-lookup"><span data-stu-id="19190-200">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="19190-201">게시 서버는 관리 서버와 통신 하 여 요청자에 게 사용할 수 있는 패키지 및 연결 그룹을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-201">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="19190-202">메타 데이터를 생성 하려면 게시 서버를 관리 서버에 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19190-202">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="19190-203">특정 사용자 또는 컴퓨터의 컨텍스트에 있는 쿼리를 사용 하 여 인터넷 브라우저의 각 요청에 대 한 메타 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19190-203">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="19190-204">관련 항목</span><span class="sxs-lookup"><span data-stu-id="19190-204">Related topics</span></span>


[<span data-ttu-id="19190-205">App-V 5.1에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="19190-205">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)









