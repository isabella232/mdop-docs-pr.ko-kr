---
title: Application Virtualization Client 설치 관리자 명령줄 매개 변수
description: Application Virtualization Client 설치 관리자 명령줄 매개 변수
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819718"
---
# <span data-ttu-id="a2cac-103">Application Virtualization Client 설치 관리자 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2cac-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="a2cac-104">다음 표에서는 사용 가능한 모든 Microsoft Application Virtualization 클라이언트 설치 관리자 명령줄 매개 변수, 해당 값, 각 매개 변수에 대 한 간략 한 설명을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="a2cac-105">매개 변수는 대/소문자를 구분 하며 모두 대문자로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="a2cac-106">모든 매개 변수 값은 큰따옴표로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="a2cac-107">참고</span><span class="sxs-lookup"><span data-stu-id="a2cac-107">Note</span></span>**  
-   <span data-ttu-id="a2cac-108">App-v 버전 4.6의 경우 클라이언트 업그레이드 중 명령줄 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="a2cac-109">*Swicachesize* 및 *MINFREESPACEMB* 매개 변수는 명령줄에서 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="a2cac-110">두 가지를 모두 사용 하는 경우 *Swicachesize* 매개 변수가 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2cac-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2cac-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a2cac-112">값</span><span class="sxs-lookup"><span data-stu-id="a2cac-112">Values</span></span></th>
<th align="left"><span data-ttu-id="a2cac-113">설명</span><span class="sxs-lookup"><span data-stu-id="a2cac-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="a2cac-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="a2cac-115">TRUE</span></span></p>
<p><span data-ttu-id="a2cac-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2cac-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-117">클라이언트가 <em> APPLICATIONSOURCEROOT 매개 변수를 사용 하 여 구성 된 방식에 관계 없이 파일에서 스트리밍을 사용할 수 있는지 여부를 나타냅니다 </em> .</span><span class="sxs-lookup"><span data-stu-id="a2cac-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="a2cac-118">FALSE로 설정 된 경우 OSD HREF 또는 <em> APPLICATIONSOURCEROOT </em> 매개 변수에 파일 경로가 포함 된 경우에도 트랜스포트가 파일에서 스트리밍을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="a2cac-119">가능한 값:</span><span class="sxs-lookup"><span data-stu-id="a2cac-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2cac-120">TRUE — 수동으로 배포 된 응용 프로그램이 디스크에서 로드 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="a2cac-121">FALSE — 모든 응용 프로그램은 원본 스트리밍 서버에서 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-122">APPLICATIONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="a2cac-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-123">RTSP:// <em> URL </em> (동적 패키지 배달의 경우)</span><span class="sxs-lookup"><span data-stu-id="a2cac-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="a2cac-124">File:// <em> URL </em> 또는 <em> UNC </em> (파일 패키지 배달의 로드)</span><span class="sxs-lookup"><span data-stu-id="a2cac-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-125">토폴로지 관리 체계를 준수 하 여 응용 프로그램 로드가 수행 되도록 관리자나 전자 소프트웨어 배포 시스템을 사용 하도록 설정 하려면 응용 프로그램 HREF 요소 (원본 위치)에 대 한 OSD 코드 베이스의 재정의를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="a2cac-126">값이 기본값인 "" 이면 기존 OSD 파일 설정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="a2cac-127">URL에는 다음과 같은 몇 가지 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="a2cac-128">&lt;프로토콜 &gt; // &lt; 서버 &gt; : &lt; 포트 &gt; / &lt; 경로 &gt; / &lt; ? 쿼리 &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="a2cac-129">UNC 경로에는 다음 세 가지 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="a2cac-130">&amp;lt; computername &gt; &amp; lt; 폴더 공유 &gt; &amp; lt; 리소스&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="a2cac-131"><em>APPLICATIONSOURCEROOT </em> 매개 변수가 클라이언트에 지정 되어 있는 경우 클라이언트는 osd 파일의 URL 또는 UNC 경로를 구성 요소로 나눠 osd 섹션을 해당 <em> APPLICATIONSOURCEROOT 섹션으로 바꿉니다 </em> .</span><span class="sxs-lookup"><span data-stu-id="a2cac-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-132">중요</span><span class="sxs-lookup"><span data-stu-id="a2cac-132">Important</span></span></strong><br/><p><span data-ttu-id="a2cac-133">UNC 경로에 file://를 사용할 때는 올바른 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="a2cac-134">올바른 형식은 file:// &amp; lt; 서버 &gt; &amp; lt; share입니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="a2cac-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-135">ICONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="a2cac-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="a2cac-136">UNC</span><span class="sxs-lookup"><span data-stu-id="a2cac-136">UNC</span></span></em></p>
<p><span data-ttu-id="a2cac-137">HTTP:// <em> url </em> 또는 HTTPS:// <em> url</span><span class="sxs-lookup"><span data-stu-id="a2cac-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-138">관리자가 게시 하는 동안 시퀀싱 된 응용 프로그램 패키지의 아이콘 검색에 대 한 원본 위치를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="a2cac-139">아이콘 원본 루트가 UNC 경로 및 Url (HTTP 또는 HTTPS)을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="a2cac-140">값이 기본값인 "" 이면 기존 OSD 파일 설정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="a2cac-141">URL에는 다음과 같은 몇 가지 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="a2cac-142">&lt;프로토콜 &gt; // &lt; 서버 &gt; : &lt; 포트 &gt; / &lt; 경로 &gt; / &lt; ? 쿼리 &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="a2cac-143">UNC 경로에는 다음 세 가지 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="a2cac-144">&amp;lt; computername &gt; &amp; lt; 폴더 공유 &gt; &amp; lt; 리소스&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-145">중요</span><span class="sxs-lookup"><span data-stu-id="a2cac-145">Important</span></span></strong><br/><p><span data-ttu-id="a2cac-146">UNC 경로를 사용 하는 경우 올바른 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="a2cac-147">허용 되는 형식은 &amp; lt, 서버 &gt; &amp; lt; share &gt; 또는 &lt; drive 문자 &gt; : &amp; lt; folder &gt; 입니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-148">OSDSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="a2cac-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="a2cac-149">UNC</span><span class="sxs-lookup"><span data-stu-id="a2cac-149">UNC</span></span></em></p>
<p><span data-ttu-id="a2cac-150">HTTP:// <em> url </em> 또는 HTTPS:// <em> url</span><span class="sxs-lookup"><span data-stu-id="a2cac-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-151">관리자가 게시 중에 응용 프로그램 패키지에 대 한 OSD 파일 검색의 원본 위치를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="a2cac-152">OSD 원본 루트는 UNC 경로 및 Url (HTTP 또는 HTTPS)을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="a2cac-153">값이 기본값인 "" 이면 기존 OSD 파일 설정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="a2cac-154">URL에는 다음과 같은 몇 가지 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="a2cac-155">&lt;프로토콜 &gt; // &lt; 서버 &gt; : &lt; 포트 &gt; / &lt; 경로 &gt; / &lt; ? 쿼리 &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="a2cac-156">UNC 경로에는 다음 세 가지 부분이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="a2cac-157">&amp;lt; computername &gt; &amp; lt; 폴더 공유 &gt; &amp; lt; 리소스&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-158">중요</span><span class="sxs-lookup"><span data-stu-id="a2cac-158">Important</span></span></strong><br/><p><span data-ttu-id="a2cac-159">UNC 경로를 사용 하는 경우 올바른 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="a2cac-160">허용 되는 형식은 &amp; lt, 서버 &gt; &amp; lt; share &gt; 또는 &lt; drive 문자 &gt; : &amp; lt; folder &gt; 입니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="a2cac-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="a2cac-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="a2cac-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="a2cac-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="a2cac-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a2cac-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-165">응용 프로그램의 자동 로드를 시작 하는 이벤트를 정의 하는 AutoLoad 트리거입니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="a2cac-166">AutoLoad는 백그라운드 스트리밍을 사용 하 여 응용 프로그램을 캐시에 완전히 로드할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="a2cac-167">기본 기능 블록이 최대한 빨리 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="a2cac-168">나머지 기능 블록은 백그라운드에서 로드 되어 응용 프로그램과 사용자의 상호 작용 등의 포그라운드 작업을 수행 하 고, 우선 순위를 사용 하 고, 최적의 성능을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-169">참고</span><span class="sxs-lookup"><span data-stu-id="a2cac-169">Note</span></span></strong><br/><p><span data-ttu-id="a2cac-170"><em>Autoloadtarget </em> 매개 변수는 자동으로 로드 되는 응용 프로그램을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="a2cac-171">기본적으로 <em> autoloadtarget이 설정 되지 않은 경우 사용 된 패키지는 자동으로 로드 됩니다 </em> .</span><span class="sxs-lookup"><span data-stu-id="a2cac-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="a2cac-172">각 매개 변수는 다음과 같이 로드 동작에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="a2cac-173">AUTOLOADONLOGIN </em> -사용자가 로그인 할 때 로드가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="a2cac-174">AUTOLOADONLAUNCH </em> -사용자가 응용 프로그램을 시작할 때 로드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="a2cac-175">AUTOLOADONREFRESH </em> -게시 새로 고침이 발생할 때 로드가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="a2cac-176">세 값을 조합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-176">The three values can be combined.</span></span> <span data-ttu-id="a2cac-177">다음 예제에서는 사용자 로그인에서 AutoLoad 트리거를 사용 하 고 새로 고침을 게시할 때 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="a2cac-178">AUTOLOADONLOGIN AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="a2cac-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-179">참고</span><span class="sxs-lookup"><span data-stu-id="a2cac-179">Note</span></span></strong><br/><p><span data-ttu-id="a2cac-180">클라이언트가 처음 설치할 때 이러한 값으로 구성 된 경우 다음에 사용자가 로그 오프 한 다음 다시 로그온 할 때까지 Autoload가 트리거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="a2cac-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-182">않아야</span><span class="sxs-lookup"><span data-stu-id="a2cac-182">NONE</span></span></p>
<p><span data-ttu-id="a2cac-183">모든</span><span class="sxs-lookup"><span data-stu-id="a2cac-183">ALL</span></span></p>
<p><span data-ttu-id="a2cac-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="a2cac-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-185">지정 된 AutoLoad 트리거가 발생할 때 자동으로 로드 되는 항목을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="a2cac-186">가능한 값:</span><span class="sxs-lookup"><span data-stu-id="a2cac-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2cac-187">없음-설정 될 수 있는 트리거에 관계 없이 자동으로 로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="a2cac-188">ALL (모두)-AutoLoad trigger를 사용 하는 경우 모든 패키지가 실행 되었는지 여부에 관계 없이 자동으로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-189">참고</span><span class="sxs-lookup"><span data-stu-id="a2cac-189">Note</span></span></strong><br/><p><span data-ttu-id="a2cac-190">이 설정은 SFTMIME <strong> 패키지 추가 </strong> 및 <strong> 패키지 구성 명령을 사용 하 여 개별 패키지에 대해 구성 됩니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="a2cac-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="a2cac-191">이러한 명령에 대 한 자세한 내용은 <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> sftmime 명령 참조를 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2cac-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="a2cac-192">PREVUSED-AutoLoad trigger를 사용 하는 경우 패키지에서 하나 이상의 응용 프로그램이 이전에 사용 된 패키지 (즉, 시작 또는 precached)만 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="a2cac-193">참고</span><span class="sxs-lookup"><span data-stu-id="a2cac-193">Note</span></span></strong><br/><p><span data-ttu-id="a2cac-194">읽기 전용 캐시 (예: VDI 서버 구현)를 사용 하도록 App-v 클라이언트를 설치 하는 경우에 <em> </em> 는 클라이언트가 읽기 전용 캐시에서 응용 프로그램을 업데이트 하는 것을 방지 하려면 autoloadtarget 매개 변수를 no로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="a2cac-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-196">29600 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a2cac-196">29600 (default)</span></span></p>
<p><span data-ttu-id="a2cac-197">1 – 1439998560 분 (범위)</span><span class="sxs-lookup"><span data-stu-id="a2cac-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-198">연결이 끊긴 작업에서 응용 프로그램을 사용할 수 있는 시간 (분)을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="a2cac-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-200">&lt;경로&gt;</span><span class="sxs-lookup"><span data-stu-id="a2cac-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-201">App-v 클라이언트의 설치 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="a2cac-202">예: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization 클라이언트&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-203">OPTIN</span><span class="sxs-lookup"><span data-stu-id="a2cac-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-204">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2cac-204">“TRUE”</span></span></p>
<p><span data-ttu-id="a2cac-205">“”</span><span class="sxs-lookup"><span data-stu-id="a2cac-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-206">일반 공용에서 업데이트를 사용할 수 있는 경우 microsoft Update를 통해 microsoft Application Virtualization 클라이언트 구성 요소를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="a2cac-207">Windows 운영 체제에 설치 된 Microsoft Update 에이전트는 사용자가 서비스를 사용 하도록 명시적으로 옵트인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="a2cac-208">이 옵트인은 디바이스의 모든 응용 프로그램에 대해 한 번만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="a2cac-209">Microsoft 업데이트에 이미 옵트인 한 경우 디바이스의 Microsoft Application Virtualization 구성 요소는 자동으로 서비스를 활용 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="a2cac-210">명령줄 설치의 경우 자동으로 Microsoft 업데이트를 허용 해야 하기 때문에 Microsoft 업데이트는 기본적으로 옵트아웃 (이전 응용 프로그램에서 옵트인 (opt in) 하도록 설정 되지 않은 경우)를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="a2cac-211">따라서 명령줄 설치의 경우에는 명시적으로 옵트인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="a2cac-212">명령줄 매개 변수 <em> OPTIN </em> 를 TRUE로 설정 하면 Microsoft Update 옵트인이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-213">REQUIREAUTHORIZATIONIFCACHED</span><span class="sxs-lookup"><span data-stu-id="a2cac-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="a2cac-214">TRUE</span></span></p>
<p><span data-ttu-id="a2cac-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2cac-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-216">응용 프로그램이 이미 캐시에 있는지 여부에 관계 없이 항상 인증이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="a2cac-217">가능한 값:</span><span class="sxs-lookup"><span data-stu-id="a2cac-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2cac-218">TRUE — 시작할 때 항상 응용 프로그램에 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="a2cac-219">RTSP로 스트리밍된 응용 프로그램의 경우 인증을 위해 사용자 인증 토큰이 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="a2cac-220">파일 기반 응용 프로그램의 경우 파일 Acl은 사용자가 응용 프로그램에 액세스할 수 있는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="a2cac-221">FALSE — 항상 서버 연결을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="a2cac-222">서버에 대 한 연결을 설정할 수 없는 경우에도 클라이언트는 사용자가 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="a2cac-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-224">캐시 크기 (MB)</span><span class="sxs-lookup"><span data-stu-id="a2cac-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-225">클라이언트 캐시의 크기 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="a2cac-226">기본 크기는 4096 MB 이며, 최대 크기는 1048576 MB (1TB)입니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="a2cac-227">시스템에서 설치할 때 사용 가능한 공간을 확인 하지만 공간은 예약 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="a2cac-228">예: <strong> swicachesize = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="a2cac-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-230">표시 이름</span><span class="sxs-lookup"><span data-stu-id="a2cac-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-231">게시 서버의 표시 된 이름을 지정 합니다. <em>SWIPUBSVRHOST </em> 를 사용할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="a2cac-232">예: <strong> SWIPUBSVRDISPLAY = &quot; 프로덕션 환경&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="a2cac-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-234">[HTTP | 플레이어가</span><span class="sxs-lookup"><span data-stu-id="a2cac-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-235">게시 서버 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-235">Specifies the publishing server type.</span></span> <span data-ttu-id="a2cac-236">기본 서버 유형은 Application Virtualization Server입니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="a2cac-237"><strong>/Secure </strong> 스위치는 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="a2cac-238">HTTP-표준 HTTP 서버</span><span class="sxs-lookup"><span data-stu-id="a2cac-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="a2cac-239">HTTP <strong> /secure </strong> -향상 된 보안 http 서버</span><span class="sxs-lookup"><span data-stu-id="a2cac-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="a2cac-240">RTSP-Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="a2cac-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="a2cac-241">RTSP <strong> /secure </strong> -향상 된 보안 애플리케이션 가상화 서버</span><span class="sxs-lookup"><span data-stu-id="a2cac-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="a2cac-242">예: <strong> SWIPUBSVRTYPE = &quot; HTTP/secure&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="a2cac-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-244">IP 주소 | 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="a2cac-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-245">서버&#39;s IP 주소로 확인 되는 서버의 호스트 이름 또는 응용 프로그램 가상화 서버의 IP 주소를 지정 합니다. <em>SWIPUBSVRDISPLAY </em> 를 사용할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="a2cac-246">예: <strong> SWIPUBSVRHOST = &quot; SERVER01&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="a2cac-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-248">포트 번호</span><span class="sxs-lookup"><span data-stu-id="a2cac-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-249">이 응용 프로그램 가상화 서버에서 클라이언트의 요청을 수신 대기 하는 데 사용 하는 논리 포트 (기본값 = 554)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="a2cac-250">표준 HTTP 서버-기본값 = 80.</span><span class="sxs-lookup"><span data-stu-id="a2cac-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="a2cac-251">향상 된 보안 HTTP 서버-기본값 = 443.</span><span class="sxs-lookup"><span data-stu-id="a2cac-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="a2cac-252">Application Virtualization Server-Default = 554.</span><span class="sxs-lookup"><span data-stu-id="a2cac-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="a2cac-253">향상 된 보안 애플리케이션 가상화 서버-기본값 = 322.</span><span class="sxs-lookup"><span data-stu-id="a2cac-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="a2cac-254">예: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="a2cac-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-256">경로 이름</span><span class="sxs-lookup"><span data-stu-id="a2cac-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-257">파일 형식 연결을 정의 하는 파일의 게시 서버 위치를 지정 합니다 (기본값 =/). <em>SWIPUBSVRTYPE </em> 매개 변수 값이 HTTP 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="a2cac-258">예: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="a2cac-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-260">[켜기] | 끄십시오</span><span class="sxs-lookup"><span data-stu-id="a2cac-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-261">사용자가 클라이언트에 로그인 할 때 파일 형식 연결 및 응용 프로그램에 대해 클라이언트가 게시 서버를 자동으로 쿼리할 지 여부를 지정 합니다 (기본값 = 설정).</span><span class="sxs-lookup"><span data-stu-id="a2cac-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="a2cac-262">예: <strong> SWIPUBSVRREFRESH = &quot; off&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="a2cac-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-264">전역 데이터 디렉터리</span><span class="sxs-lookup"><span data-stu-id="a2cac-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-265">특정 사용자와 관련 되지 않은 데이터를 저장할 디렉터리 (기본값 = C:\Documents 및 Settings\All Users\Documents)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="a2cac-266">예: <strong> SWIGLOBALDATA = &quot; D:\microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="a2cac-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-268">사용자 데이터 디렉터리</span><span class="sxs-lookup"><span data-stu-id="a2cac-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-269">특정 사용자와 관련 된 데이터가 저장 되는 디렉터리를 지정 합니다 (기본값 =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="a2cac-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="a2cac-270">예: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization 클라이언트&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="a2cac-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-272">기본 설정 드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="a2cac-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-273">가상 드라이브에 대해 선택한 드라이브 문자에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="a2cac-274">예: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="a2cac-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="a2cac-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-276">0 – 4</span><span class="sxs-lookup"><span data-stu-id="a2cac-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-277">로그 메시지가 NT 이벤트 로그에 기록 되는 로깅 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="a2cac-278">값은 기록 되는 항목의 임계값 (즉, 해당 값과 같거나 작은 모든 항목은 기록 됨)을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="a2cac-279">예를 들어 0x3 (경고) 값은 경고 (0x3), 오류 (0x2) 및 치명적 오류 (0x1)가 기록 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="a2cac-280">가능한 값:</span><span class="sxs-lookup"><span data-stu-id="a2cac-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2cac-281">0 = = 없음</span><span class="sxs-lookup"><span data-stu-id="a2cac-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="a2cac-282">1 = = 요주의</span><span class="sxs-lookup"><span data-stu-id="a2cac-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="a2cac-283">2 = = 오류</span><span class="sxs-lookup"><span data-stu-id="a2cac-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="a2cac-284">3 = = 경고</span><span class="sxs-lookup"><span data-stu-id="a2cac-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="a2cac-285">4 = = 정보</span><span class="sxs-lookup"><span data-stu-id="a2cac-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="a2cac-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="a2cac-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-287">(MB)</span><span class="sxs-lookup"><span data-stu-id="a2cac-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-288">캐시 크기가 증가 하기 전에 호스트에서 사용할 수 있는 사용 가능한 공간의 크기 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="a2cac-289">다음 예제에서는 캐시 크기를 늘리기 위해 디스크에서 5gb 이상의 여유 공간을 확보 하도록 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="a2cac-290">기본값은 설치 시 디스크에서 사용할 수 있는 5000 MB의 빈 공간입니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="a2cac-291">예: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</span><span class="sxs-lookup"><span data-stu-id="a2cac-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="a2cac-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="a2cac-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="a2cac-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="a2cac-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2cac-294">그룹 정책을 사용 하는 경우와 같이 클라이언트를 배포 하기 전에 레지스트리 설정을 적용 한 경우 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="a2cac-295">클라이언트가 배포 되 면이 매개 변수를 값 1로 설정 하 여 레지스트리 설정을 덮어쓰지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2cac-296">중요</span><span class="sxs-lookup"><span data-stu-id="a2cac-296">Important</span></span></strong><br/><p><span data-ttu-id="a2cac-297">값을 1로 설정 하면 다음 클라이언트 설치 관리자 명령줄 매개 변수가 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2cac-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="a2cac-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , <strong> ICONSOURCEROOT </strong> , <strong> OSDSOURCEROOT </strong> , <strong> systemeventloglevel </strong> , <strong> SWIGLOBALDATA </strong> , <strong> dotimeoutminutes </strong> , <strong> SWIFSDRIVE </strong> , <strong> autoloadtarget </strong> , <strong> autoloadtarget </strong> , <strong> SWIUSERDATA </strong> .</span><span class="sxs-lookup"><span data-stu-id="a2cac-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="a2cac-299">설치 후 이러한 값을 설정 하는 방법에 대 한 자세한 내용은 Application Virtualization (App-v) Operations Guide ()에서 "명령줄을 사용 하 여 App-v 클라이언트 레지스트리 설정을 구성 하는 방법"을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> .</span><span class="sxs-lookup"><span data-stu-id="a2cac-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a2cac-300">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a2cac-300">Related topics</span></span>


[<span data-ttu-id="a2cac-301">Application Virtualization Client를 수동으로 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="a2cac-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="a2cac-302">Application Virtualization Client를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="a2cac-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="a2cac-303">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="a2cac-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









