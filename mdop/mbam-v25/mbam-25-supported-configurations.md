---
title: MBAM 2.5 지원되는 구성
description: MBAM 2.5 지원되는 구성
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182930"
---
# <span data-ttu-id="d9298-103">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="d9298-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="d9298-104">독립 실행형 토폴로지 또는 MBAM을 System Center Configuration Manager와 통합 하는 Configuration Manager 통합 토폴로지에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="d9298-105">프로덕션 환경의 토폴로지에 권장 되는 구성을 사용 하는 경우 MBAM은 최대 50만 MBAM 클라이언트를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="d9298-106">각 토폴로지에 대해 각 서버에 구성 되는 권장 아키텍처 및 기능에 대 한 자세한 내용은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="d9298-107">Configuration Manager 통합 토폴로지와 관련 된 추가 구성에 대 한 자세한 내용은 [MBAM이 지 원하는 구성 관리자 버전](#bkmk-cm-ramreqs)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="d9298-108">참고</span><span class="sxs-lookup"><span data-stu-id="d9298-108">Note</span></span>**  
<span data-ttu-id="d9298-109">Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="d9298-110">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="d9298-111">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="d9298-112">MBAM 지원 언어</span><span class="sxs-lookup"><span data-stu-id="d9298-112">MBAM Supported Languages</span></span>


<span data-ttu-id="d9298-113">다음 표에는 MBAM 클라이언트 (Self-Service 포털 포함) 및 MBAM 2.5 및 MBAM 2.5 SP1의 MBAM 서버에 대해 지원 되는 언어가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="d9298-114">MBAM 2.5 SP1의 지원 되는 언어:</span><span class="sxs-lookup"><span data-stu-id="d9298-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-115">클라이언트 언어</span><span class="sxs-lookup"><span data-stu-id="d9298-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="d9298-116">서버 언어</span><span class="sxs-lookup"><span data-stu-id="d9298-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-117">체코어 (체코 공화국) cs-CZ</span><span class="sxs-lookup"><span data-stu-id="d9298-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="d9298-118">덴마크어 (덴마크) da-진한</span><span class="sxs-lookup"><span data-stu-id="d9298-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="d9298-119">네덜란드어 (네덜란드) nl-NL</span><span class="sxs-lookup"><span data-stu-id="d9298-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="d9298-120">영어 (미국) en-us-US</span><span class="sxs-lookup"><span data-stu-id="d9298-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="d9298-121">핀란드어 (핀란드) fi</span><span class="sxs-lookup"><span data-stu-id="d9298-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="d9298-122">프랑스어 (프랑스) fr-fr</span><span class="sxs-lookup"><span data-stu-id="d9298-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="d9298-123">독일어 (독일) DE-DE</span><span class="sxs-lookup"><span data-stu-id="d9298-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="d9298-124">그리스어 (그리스) el-GR</span><span class="sxs-lookup"><span data-stu-id="d9298-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="d9298-125">헝가리어 (헝가리) hu-hu&platform-HU-HU&PLATFORM</span><span class="sxs-lookup"><span data-stu-id="d9298-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="d9298-126">이탈리아어 (이탈리아) it</span><span class="sxs-lookup"><span data-stu-id="d9298-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="d9298-127">일본어 (일본) ja-jp</span><span class="sxs-lookup"><span data-stu-id="d9298-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="d9298-128">한국어 (대한민국) ko-kr-KR</span><span class="sxs-lookup"><span data-stu-id="d9298-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="d9298-129">노르웨이어, 복말 (노르웨이) nb-아니요</span><span class="sxs-lookup"><span data-stu-id="d9298-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="d9298-130">폴란드어 (폴란드) pl-PL</span><span class="sxs-lookup"><span data-stu-id="d9298-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="d9298-131">포르투갈어 (브라질) pt-BR</span><span class="sxs-lookup"><span data-stu-id="d9298-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="d9298-132">포르투갈어 (포르투갈) pt-PT</span><span class="sxs-lookup"><span data-stu-id="d9298-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="d9298-133">러시아어 (러시아)의 기능</span><span class="sxs-lookup"><span data-stu-id="d9298-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="d9298-134">슬로바키아어 (슬로바키아) a/.</span><span class="sxs-lookup"><span data-stu-id="d9298-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="d9298-135">스페인어 (스페인) es</span><span class="sxs-lookup"><span data-stu-id="d9298-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="d9298-136">스웨덴 (스웨덴) sv-SE</span><span class="sxs-lookup"><span data-stu-id="d9298-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="d9298-137">터키어 (터키) tr-TR</span><span class="sxs-lookup"><span data-stu-id="d9298-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="d9298-138">슬로베니아어 (슬로베니아) sl-SI</span><span class="sxs-lookup"><span data-stu-id="d9298-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="d9298-139">중국어 간체 (중국) zh-cn-CN</span><span class="sxs-lookup"><span data-stu-id="d9298-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="d9298-140">중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</span><span class="sxs-lookup"><span data-stu-id="d9298-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="d9298-141">영어 (미국) en-us-US</span><span class="sxs-lookup"><span data-stu-id="d9298-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="d9298-142">프랑스어 (프랑스) fr-fr</span><span class="sxs-lookup"><span data-stu-id="d9298-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="d9298-143">독일어 (독일) DE-DE</span><span class="sxs-lookup"><span data-stu-id="d9298-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="d9298-144">이탈리아어 (이탈리아) it</span><span class="sxs-lookup"><span data-stu-id="d9298-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="d9298-145">일본어 (일본) ja-jp</span><span class="sxs-lookup"><span data-stu-id="d9298-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="d9298-146">한국어 (대한민국) ko-kr-KR</span><span class="sxs-lookup"><span data-stu-id="d9298-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="d9298-147">포르투갈어 (브라질) pt-BR</span><span class="sxs-lookup"><span data-stu-id="d9298-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="d9298-148">러시아어 (러시아)의 기능</span><span class="sxs-lookup"><span data-stu-id="d9298-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="d9298-149">스페인어 (스페인) es</span><span class="sxs-lookup"><span data-stu-id="d9298-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="d9298-150">중국어 간체 (중국) zh-cn-CN</span><span class="sxs-lookup"><span data-stu-id="d9298-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="d9298-151">중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</span><span class="sxs-lookup"><span data-stu-id="d9298-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d9298-152">MBAM 2.5에서 지원 되는 언어:</span><span class="sxs-lookup"><span data-stu-id="d9298-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-153">클라이언트 언어</span><span class="sxs-lookup"><span data-stu-id="d9298-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="d9298-154">서버 언어</span><span class="sxs-lookup"><span data-stu-id="d9298-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="d9298-155">영어 (미국) en-us-US</span><span class="sxs-lookup"><span data-stu-id="d9298-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="d9298-156">프랑스어 (프랑스) fr-fr</span><span class="sxs-lookup"><span data-stu-id="d9298-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="d9298-157">독일어 (독일) DE-DE</span><span class="sxs-lookup"><span data-stu-id="d9298-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="d9298-158">이탈리아어 (이탈리아) it</span><span class="sxs-lookup"><span data-stu-id="d9298-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="d9298-159">일본어 (일본) ja-jp</span><span class="sxs-lookup"><span data-stu-id="d9298-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="d9298-160">한국어 (대한민국) ko-kr-KR</span><span class="sxs-lookup"><span data-stu-id="d9298-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="d9298-161">포르투갈어 (브라질) pt-BR</span><span class="sxs-lookup"><span data-stu-id="d9298-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="d9298-162">러시아어 (러시아)의 기능</span><span class="sxs-lookup"><span data-stu-id="d9298-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="d9298-163">스페인어 (스페인) es</span><span class="sxs-lookup"><span data-stu-id="d9298-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="d9298-164">중국어 간체 (중국) zh-cn-CN</span><span class="sxs-lookup"><span data-stu-id="d9298-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="d9298-165">중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</span><span class="sxs-lookup"><span data-stu-id="d9298-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="d9298-166">영어 (미국) en-us-US</span><span class="sxs-lookup"><span data-stu-id="d9298-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="d9298-167">프랑스어 (프랑스) fr-fr</span><span class="sxs-lookup"><span data-stu-id="d9298-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="d9298-168">독일어 (독일) DE-DE</span><span class="sxs-lookup"><span data-stu-id="d9298-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="d9298-169">이탈리아어 (이탈리아) it</span><span class="sxs-lookup"><span data-stu-id="d9298-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="d9298-170">일본어 (일본) ja-jp</span><span class="sxs-lookup"><span data-stu-id="d9298-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="d9298-171">한국어 (대한민국) ko-kr-KR</span><span class="sxs-lookup"><span data-stu-id="d9298-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="d9298-172">포르투갈어 (브라질) pt-BR</span><span class="sxs-lookup"><span data-stu-id="d9298-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="d9298-173">러시아어 (러시아)의 기능</span><span class="sxs-lookup"><span data-stu-id="d9298-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="d9298-174">스페인어 (스페인) es</span><span class="sxs-lookup"><span data-stu-id="d9298-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="d9298-175">중국어 간체 (중국) zh-cn-CN</span><span class="sxs-lookup"><span data-stu-id="d9298-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="d9298-176">중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</span><span class="sxs-lookup"><span data-stu-id="d9298-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="d9298-177">MBAM 서버 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="d9298-178">MBAM 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="d9298-179">동일한 시스템의 운영 체제에서 MBAM 클라이언트와 MBAM 서버를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="d9298-180">예를 들어 windows 10이 포함 되어 있는 windows Server 2016, windows 8.1 windows Server 2012 R2 등</span><span class="sxs-lookup"><span data-stu-id="d9298-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="d9298-181">다음 표에는 MBAM 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-182">운영 체제</span><span class="sxs-lookup"><span data-stu-id="d9298-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="d9298-183">버전</span><span class="sxs-lookup"><span data-stu-id="d9298-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="d9298-184">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="d9298-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="d9298-185">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="d9298-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-186">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="d9298-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-187">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="d9298-188">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-189">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d9298-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-190">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="d9298-191">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-192">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d9298-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-193">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-194">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9298-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-196">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="d9298-197">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9298-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-199">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-200">SP1</span><span class="sxs-lookup"><span data-stu-id="d9298-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-201">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="d9298-202">엔터프라이즈 도메인은 적어도 하나 이상의 Windows Server 2008 (이상) 도메인 컨트롤러를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="d9298-203">MBAM 서버 프로세서, RAM, 디스크 공간 요구 사항-독립 실행형 토폴로지</span><span class="sxs-lookup"><span data-stu-id="d9298-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="d9298-204">이러한 요구 사항은 MBAM 독립 실행형 토폴로지에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="d9298-205">Configuration Manager 통합 토폴로지의 요구 사항에 대해서는 [Mbam 서버 프로세서, RAM 및 디스크 공간 요구 사항-구성 관리자 통합 토폴로지](#bkmk-cm-ramreqs)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-206">하드웨어 항목</span><span class="sxs-lookup"><span data-stu-id="d9298-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="d9298-207">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="d9298-208">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-209">프로세서</span><span class="sxs-lookup"><span data-stu-id="d9298-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-210">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="d9298-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-211">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="d9298-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-212">RAM</span><span class="sxs-lookup"><span data-stu-id="d9298-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-213">8gb</span><span class="sxs-lookup"><span data-stu-id="d9298-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-214">12gb</span><span class="sxs-lookup"><span data-stu-id="d9298-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-215">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="d9298-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-216">1GB</span><span class="sxs-lookup"><span data-stu-id="d9298-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-217">2GB</span><span class="sxs-lookup"><span data-stu-id="d9298-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="d9298-218">MBAM 서버 프로세서, RAM, 디스크 공간 요구 사항-구성 관리자 통합 토폴로지</span><span class="sxs-lookup"><span data-stu-id="d9298-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="d9298-219">다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 MBAM 서버의 서버 프로세서, RAM, 디스크 공간 요구 사항이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="d9298-220">독립 실행형 토폴로지에 대 한 요구 사항에 대해서는 [Mbam 서버 프로세서, RAM 및 디스크 공간 요구 사항-독립 실행형 토폴로지](#bkmk-stand-alone-ramreqs)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-221">하드웨어 항목</span><span class="sxs-lookup"><span data-stu-id="d9298-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="d9298-222">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="d9298-223">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-224">프로세서</span><span class="sxs-lookup"><span data-stu-id="d9298-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-225">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="d9298-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-226">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="d9298-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-227">RAM</span><span class="sxs-lookup"><span data-stu-id="d9298-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-228">4GB</span><span class="sxs-lookup"><span data-stu-id="d9298-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-229">8gb</span><span class="sxs-lookup"><span data-stu-id="d9298-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-230">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="d9298-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-231">1GB</span><span class="sxs-lookup"><span data-stu-id="d9298-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-232">2GB</span><span class="sxs-lookup"><span data-stu-id="d9298-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="d9298-233">MBAM이 지 원하는 Configuration Manager 버전</span><span class="sxs-lookup"><span data-stu-id="d9298-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="d9298-234">MBAM은 다음 버전의 Configuration Manager를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-235">지원 되는 버전</span><span class="sxs-lookup"><span data-stu-id="d9298-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="d9298-236">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="d9298-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="d9298-237">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="d9298-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-238">Microsoft System Center Configuration Manager (현재 분기), 버전이 최대 1902입니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-239">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="d9298-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-241">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-242">Microsoft System Center Configuration Manager (LTSB-버전 1606)</span><span class="sxs-lookup"><span data-stu-id="d9298-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-243">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-244">Microsoft System Center 2012 구성 관리자</span><span class="sxs-lookup"><span data-stu-id="d9298-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-245">SP1</span><span class="sxs-lookup"><span data-stu-id="d9298-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-246">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-247">Microsoft System Center Configuration Manager 2007 R2 이상</span><span class="sxs-lookup"><span data-stu-id="d9298-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-248">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-248">64-bit</span></span></p>

<span data-ttu-id="d9298-249">&gt;<strong>참고 </strong> Configuration Manager 2007 R2는 32 비트 이지만 64 비트 MBAM 소프트웨어와 일치 하려면 64 비트 운영 체제에 SQL Server를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="d9298-250">Configuration Manager 서버에서 지원 되는 구성 목록은 사용 중인 구성 관리자 버전에 해당 하는 TechNet 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="d9298-251">MBAM에는 Configuration Manager 서버에 대 한 추가 시스템 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="d9298-252">SQL Server 데이터베이스 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-252">SQL Server database requirements</span></span>

<span data-ttu-id="d9298-253">다음 표에는 복구 데이터베이스, 준수 및 감사 데이터베이스, 보고서 기능을 포함 하는 MBAM 서버 기능에 대해 지원 되는 Microsoft SQL Server 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="d9298-254">필요한 버전은 독립 실행형 또는 Configuration Manager 통합 토폴로지에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="d9298-255">Sql **\ _Latin1 \ _General \ _CP1 \ _CI \ _AS** 데이터 정렬을 사용 하 여 sql Server를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-256">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="d9298-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="d9298-257">버전</span><span class="sxs-lookup"><span data-stu-id="d9298-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="d9298-258">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="d9298-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="d9298-259">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="d9298-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="d9298-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-261">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-262">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="d9298-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="d9298-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-264">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-265">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="d9298-266">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="d9298-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-267">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-268">SP1</span><span class="sxs-lookup"><span data-stu-id="d9298-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="d9298-269">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-270">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="d9298-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-271">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-272">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="d9298-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-273">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-274">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9298-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-275">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-276">이상을</span><span class="sxs-lookup"><span data-stu-id="d9298-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-277">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9298-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-279">Standard 또는 Enterprise</span><span class="sxs-lookup"><span data-stu-id="d9298-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-280">이상을</span><span class="sxs-lookup"><span data-stu-id="d9298-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-281">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="d9298-282">참고</span><span class="sxs-lookup"><span data-stu-id="d9298-282">Note</span></span>**  
<span data-ttu-id="d9298-283">MBAM에는 지원 되는 최대 호환성 수준 140이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="d9298-284">SQL Server 2019에서 만든 새 데이터베이스의 기본 호환성 수준은 데이터베이스를 만든 후 ALTER DATABASE 명령을 사용 하 여 140 이하로 변경 해야 하는 150입니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="d9298-285">SQL server 2017 또는 아래에서 마이그레이션한 기존 데이터베이스는 이전 호환성 수준으로 유지 되며 변경할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="d9298-286">SQL 2016을 지원 하려면 MDOP 용 2017 서비스 릴리스를 설치 하 https://www.microsoft.com/download/details.aspx?id=54967  고 SQL 2017을 지원 하려면 mdop에 대해 7 월 2018 서비스 릴리스를 설치 해야 합니다 https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="d9298-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="d9298-287">일반적으로 최신 서비스 업데이트를 항상 사용 하는 것은 물론, 모든 버그 수정과 새로운 기능도 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="d9298-288">SQL Server 프로세서, RAM, 디스크 공간 요구 사항-독립 실행형 토폴로지</span><span class="sxs-lookup"><span data-stu-id="d9298-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="d9298-289">다음 표에는 독립 실행형 토폴로지를 사용 하는 경우 SQL Server 컴퓨터에 권장 되는 서버 프로세서, RAM, 디스크 공간 요구 사항이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="d9298-290">이러한 요구 사항을 지침으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-290">Use these requirements as a guide.</span></span> <span data-ttu-id="d9298-291">특정 요구 사항은 엔터프라이즈에서 지원 되는 클라이언트 컴퓨터 수에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="d9298-292">Configuration Manager 통합 토폴로지에 대 한 요구 사항을 보려면 [SQL Server 프로세서, RAM 및 디스크 공간 요구 사항-구성 관리자 통합 토폴로지](#bkmk-cm-sql-ramreqs)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-293">하드웨어 항목</span><span class="sxs-lookup"><span data-stu-id="d9298-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="d9298-294">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="d9298-295">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-296">프로세서</span><span class="sxs-lookup"><span data-stu-id="d9298-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-297">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="d9298-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-298">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="d9298-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-299">RAM</span><span class="sxs-lookup"><span data-stu-id="d9298-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-300">8gb</span><span class="sxs-lookup"><span data-stu-id="d9298-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-301">12gb</span><span class="sxs-lookup"><span data-stu-id="d9298-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-302">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="d9298-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-303">5GB</span><span class="sxs-lookup"><span data-stu-id="d9298-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-304">5gb 이상</span><span class="sxs-lookup"><span data-stu-id="d9298-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="d9298-305">SQL Server 프로세서, RAM 및 디스크 공간 요구 사항-구성 관리자 통합 토폴로지</span><span class="sxs-lookup"><span data-stu-id="d9298-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="d9298-306">다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 Microsoft SQL Server 컴퓨터에 대 한 서버 프로세서, RAM, 디스크 공간 요구 사항이 나와 있습니다. [SQL Server 프로세서, ram 및 디스크 공간 요구 사항-독립 실행형 토폴로지](#bkmk-sql-stand-alone-ramreqs)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9298-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-307">하드웨어 항목</span><span class="sxs-lookup"><span data-stu-id="d9298-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="d9298-308">최소 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="d9298-309">권장 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-310">프로세서</span><span class="sxs-lookup"><span data-stu-id="d9298-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-311">2.33 GHz</span><span class="sxs-lookup"><span data-stu-id="d9298-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-312">2.33 GHz 이상</span><span class="sxs-lookup"><span data-stu-id="d9298-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-313">RAM</span><span class="sxs-lookup"><span data-stu-id="d9298-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-314">4GB</span><span class="sxs-lookup"><span data-stu-id="d9298-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-315">8gb</span><span class="sxs-lookup"><span data-stu-id="d9298-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-316">사용 가능한 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="d9298-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-317">5GB</span><span class="sxs-lookup"><span data-stu-id="d9298-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-318">5GB</span><span class="sxs-lookup"><span data-stu-id="d9298-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="d9298-319">MBAM 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="d9298-320">클라이언트 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-320">Client operating system requirements</span></span>

<span data-ttu-id="d9298-321">동일한 시스템의 운영 체제에서 MBAM 클라이언트와 MBAM 서버를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="d9298-322">예를 들어 windows 10이 포함 되어 있는 windows Server 2016, windows 8.1 windows Server 2012 R2 등</span><span class="sxs-lookup"><span data-stu-id="d9298-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="d9298-323">다음 표에는 MBAM 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="d9298-324">독립 실행형 및 Configuration Manager 통합 토폴로지에도 동일한 요구 사항이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-325">운영 체제</span><span class="sxs-lookup"><span data-stu-id="d9298-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="d9298-326">버전</span><span class="sxs-lookup"><span data-stu-id="d9298-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="d9298-327">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="d9298-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="d9298-328">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="d9298-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="d9298-329">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="d9298-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d9298-330">엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="d9298-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="d9298-331">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-332">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d9298-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-333">엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="d9298-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-334">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d9298-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-336">엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="d9298-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-337">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-338">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9298-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-339">엔터프라이즈 또는 Ultimate</span><span class="sxs-lookup"><span data-stu-id="d9298-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-340">SP1</span><span class="sxs-lookup"><span data-stu-id="d9298-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-341">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-342">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="d9298-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-343">Windows 8.1 및 Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="d9298-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-344">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="d9298-345">클라이언트 RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-345">Client RAM requirements</span></span>

<span data-ttu-id="d9298-346">MBAM 클라이언트 설치와 관련 된 RAM 요구 사항은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="d9298-347">MBAM 그룹 정책 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="d9298-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="d9298-348">다음 표에는 MBAM 그룹 정책 서식 파일 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9298-349">운영 체제</span><span class="sxs-lookup"><span data-stu-id="d9298-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="d9298-350">버전</span><span class="sxs-lookup"><span data-stu-id="d9298-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="d9298-351">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="d9298-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="d9298-352">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="d9298-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="d9298-353">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="d9298-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="d9298-354">엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="d9298-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="d9298-355">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-356">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d9298-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-357">엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="d9298-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-358">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-359">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d9298-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-360">엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="d9298-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-361">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-362">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9298-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-363">Enterprise 또는 Ultimate</span><span class="sxs-lookup"><span data-stu-id="d9298-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-364">SP1</span><span class="sxs-lookup"><span data-stu-id="d9298-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-365">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-366">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d9298-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-367">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-368">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d9298-369">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9298-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-370">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d9298-371">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d9298-372">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9298-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-373">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="d9298-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-374">SP1</span><span class="sxs-lookup"><span data-stu-id="d9298-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d9298-375">64비트</span><span class="sxs-lookup"><span data-stu-id="d9298-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="d9298-376">Azure IaaS에서 MBAM</span><span class="sxs-lookup"><span data-stu-id="d9298-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="d9298-377">MBAM 서버는 위에 나열 된 지원 OS 버전의 IaaS (Azure 인프라 as Services)에 배포 될 수 있으며, 온-프레미스에서 호스트 되는 Active Directory 또는 Azure IaaS에 호스트 된 Active Directory에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="d9298-378">Azure IaaS에서 Active Directory를 설정 및 구성 하는 방법에 대 한 문서는 [다음과](https://msdn.microsoft.com/library/azure/jj156090.aspx)같습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="d9298-379">MBAM 클라이언트는 가상 머신에서 지원 되지 않으며, Azure IaaS 에서도 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="d9298-380">서비스 릴리스</span><span class="sxs-lookup"><span data-stu-id="d9298-380">Service releases</span></span> 

- [<span data-ttu-id="d9298-381">4 월 2016 핫픽스</span><span class="sxs-lookup"><span data-stu-id="d9298-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="d9298-382">2016 년 9 월</span><span class="sxs-lookup"><span data-stu-id="d9298-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="d9298-383">2016년 12월</span><span class="sxs-lookup"><span data-stu-id="d9298-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="d9298-384">2017년 3월</span><span class="sxs-lookup"><span data-stu-id="d9298-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="d9298-385">2017년 6월</span><span class="sxs-lookup"><span data-stu-id="d9298-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="d9298-386">2017년 9월</span><span class="sxs-lookup"><span data-stu-id="d9298-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="d9298-387">2018년 3월</span><span class="sxs-lookup"><span data-stu-id="d9298-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="d9298-388">2018 년 7 월</span><span class="sxs-lookup"><span data-stu-id="d9298-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="d9298-389">2019 년 5 월</span><span class="sxs-lookup"><span data-stu-id="d9298-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="d9298-390">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d9298-390">Related topics</span></span>


[<span data-ttu-id="d9298-391">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="d9298-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="d9298-392">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="d9298-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="d9298-393">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="d9298-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d9298-394">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d9298-395">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9298-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




