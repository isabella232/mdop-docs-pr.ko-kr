---
title: App-V 5.1 필수 구성 요소
description: App-V 5.1 필수 구성 요소
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814740"
---
# <span data-ttu-id="af1b9-103">App-V 5.1 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="af1b9-103">App-V 5.1 Prerequisites</span></span>


<span data-ttu-id="af1b9-104">Microsoft App-v (Application Virtualization) 5.1을 설치 하기 전에 다음 필수 필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-104">Before installing Microsoft Application Virtualization (App-V) 5.1, ensure that you have installed all of the following required prerequisite software.</span></span>

<span data-ttu-id="af1b9-105">App-v Server, Sequencer 및 클라이언트에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항 목록은 [app-v 5.1 지원 구성을](app-v-51-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af1b9-105">For a list of supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client, see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

## <span data-ttu-id="af1b9-106">각 운영 체제에 사전 설치 된 소프트웨어 요약</span><span class="sxs-lookup"><span data-stu-id="af1b9-106">Summary of software preinstalled on each operating system</span></span>


<span data-ttu-id="af1b9-107">다음 표에는 여러 운영 체제에 대해 이미 설치 된 소프트웨어가 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-107">The following table indicates the software that is already installed for different operating systems.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-108">운영 체제</span><span class="sxs-lookup"><span data-stu-id="af1b9-108">Operating system</span></span></th>
<th align="left"><span data-ttu-id="af1b9-109">필수 구성 요소 설명</span><span class="sxs-lookup"><span data-stu-id="af1b9-109">Prerequisite description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-110">Windows 10</span><span class="sxs-lookup"><span data-stu-id="af1b9-110">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-111">모든 필수 소프트웨어는 이미 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-111">All of the prerequisite software is already installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="af1b9-112">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-113">모든 필수 소프트웨어는 이미 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-113">All of the prerequisite software is already installed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="af1b9-114">참고</span><span class="sxs-lookup"><span data-stu-id="af1b9-114">Note</span></span></strong><br/><p><span data-ttu-id="af1b9-115">Windows 8을 실행 하는 경우 App-v 5.1를 사용 하기 전에 Windows 8.1으로 업그레이드 하세요.</span><span class="sxs-lookup"><span data-stu-id="af1b9-115">If you are running Windows 8, upgrade to Windows 8.1 before using App-V 5.1.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-116">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af1b9-116">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-117">다음 필수 소프트웨어는 이미 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-117">The following prerequisite software is already installed:</span></span></p>
<ul>
<li><p><span data-ttu-id="af1b9-118">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="af1b9-118">Microsoft .NET Framework 4.5</span></span></p></li>
<li><p><span data-ttu-id="af1b9-119">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="af1b9-119">Windows PowerShell 3.0</span></span></p>
<div class="alert">
<strong><span data-ttu-id="af1b9-120">참고</span><span class="sxs-lookup"><span data-stu-id="af1b9-120">Note</span></span></strong><br/><p><span data-ttu-id="af1b9-121">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-121">Installing PowerShell 3.0 requires a restart.</span></span></p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af1b9-122">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-123">필수 소프트웨어는 아직 설치 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-123">The prerequisite software is not already installed.</span></span> <span data-ttu-id="af1b9-124">App-v를 설치 하려면 먼저 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-124">You must install it before you can install App-V.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="af1b9-125">App-v Server 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-125">App-V Server prerequisite software</span></span>


<span data-ttu-id="af1b9-126">App-v 5.1 서버 구성 요소에 필요한 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-126">Install the required prerequisite software for the App-V 5.1 Server components.</span></span>

### <span data-ttu-id="af1b9-127">시작 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="af1b9-127">What to know before you start</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-128">App-v 서버 설치 계정</span><span class="sxs-lookup"><span data-stu-id="af1b9-128">Account for installing the App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-129">App-v 서버 구성 요소를 설치 하는 데 사용 하는 계정에는 다음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-129">The account that you use to install the App-V Server components must have:</span></span></p>
<ul>
<li><p><span data-ttu-id="af1b9-130">구성 요소를 설치 하는 컴퓨터에 대 한 관리자 권한</span><span class="sxs-lookup"><span data-stu-id="af1b9-130">Administrative rights on the computer on which you are installing the components.</span></span></p></li>
<li><p><span data-ttu-id="af1b9-131">Active Directory 도메인 서비스를 쿼리 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-131">The ability to query Active Directory Domain Services.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-132">포트 및 방화벽</span><span class="sxs-lookup"><span data-stu-id="af1b9-132">Port and firewall</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="af1b9-133">각 구성 요소를 호스트할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-133">Specify a port where each component will be hosted.</span></span></p></li>
<li><p><span data-ttu-id="af1b9-134">지정 된 포트로 들어오는 요청을 허용 하는 연결 된 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-134">Add the associated firewall rules to allow incoming requests to the specified ports.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-135">WebDAV (웹 분산 작성 및 버전 관리)</span><span class="sxs-lookup"><span data-stu-id="af1b9-135">Web Distributed Authoring and Versioning (WebDAV)</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-136">WebDAV는 관리 서비스에 대해 자동으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-136">WebDAV is automatically disabled for the Management Service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-137">지원 되는 배포 시나리오</span><span class="sxs-lookup"><span data-stu-id="af1b9-137">Supported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="af1b9-138">모든 구성 요소가 동일한 서버에 배포 되는 독립 실행형 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-138">A stand-alone deployment, where all components are deployed on the same server.</span></span></p></li>
<li><p><span data-ttu-id="af1b9-139">분산 배포.</span><span class="sxs-lookup"><span data-stu-id="af1b9-139">A distributed deployment.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-140">지원 되지 않는 배포 시나리오</span><span class="sxs-lookup"><span data-stu-id="af1b9-140">Unsupported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="af1b9-141">동일한 서버에 여러 App-v Server 버전의 side-by-side 인스턴스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-141">Installing side-by-side instances of multiple App-V Server versions on the same server.</span></span></p></li>
<li><p><span data-ttu-id="af1b9-142">Server core 또는 도메인 컨트롤러를 실행 하는 컴퓨터에 App-v 서버 구성 요소 설치</span><span class="sxs-lookup"><span data-stu-id="af1b9-142">Installing the App-V server components on a computer that runs server core or domain controller.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="af1b9-143">관리 서버 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-143">Management server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-144">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="af1b9-144">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="af1b9-145">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-145">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-146">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="af1b9-146">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-147">지원 되는 버전은 <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> app-v 5.1 지원 되는 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="af1b9-147">For supported versions, see <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-148">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-148">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="af1b9-149">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="af1b9-149">Windows PowerShell 3.0</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="af1b9-150">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-150">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-151">KB2533623 다운로드 및 설치 <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"></span><span class="sxs-lookup"><span data-stu-id="af1b9-151">Download and install <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="af1b9-152">Windows 7에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-152">Applies to Windows 7 only.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-153">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-153">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-154">64 비트 ASP.NET 등록</span><span class="sxs-lookup"><span data-stu-id="af1b9-154">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-155">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="af1b9-155">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-156">이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-156">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-157">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="af1b9-157">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-158"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-158">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-159">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="af1b9-159">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="af1b9-160">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="af1b9-160">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-161">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="af1b9-161">Static Content</span></span></p></li>
<li><p><span data-ttu-id="af1b9-162">기본 문서</span><span class="sxs-lookup"><span data-stu-id="af1b9-162">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-163">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="af1b9-163">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-164">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="af1b9-164">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="af1b9-165">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="af1b9-165">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="af1b9-166">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="af1b9-166">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="af1b9-167">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="af1b9-167">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-168">보안이</span><span class="sxs-lookup"><span data-stu-id="af1b9-168">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-169">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="af1b9-169">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="af1b9-170">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="af1b9-170">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-171">관리 도구:</span><span class="sxs-lookup"><span data-stu-id="af1b9-171">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-172">IIS 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="af1b9-172">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-173">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-173">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-174">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="af1b9-174">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-175">관리 데이터베이스의 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-175">Location of the Management database</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-176">SQL Server 데이터베이스 이름, SQL Server 데이터베이스 인스턴스 이름, 데이터베이스 이름.</span><span class="sxs-lookup"><span data-stu-id="af1b9-176">SQL Server database name, SQL Server database instance name, and database name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-177">관리 콘솔 및 관리 데이터베이스 권한</span><span class="sxs-lookup"><span data-stu-id="af1b9-177">Management console and Management database permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-178">배포 완료 후 관리 콘솔과 데이터베이스에 액세스할 수 있는 사용자 또는 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-178">A user or group that can access the Management console and database after the deployment is complete.</span></span> <span data-ttu-id="af1b9-179">관리 콘솔을 사용 하 여 추가 관리자가 추가 되지 않는 한 이러한 사용자 또는 그룹만 관리 콘솔과 데이터베이스에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-179">Only these users or groups will have access to the Management console and database unless additional administrators are added by using the Management console.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-180">관리 서비스 웹 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="af1b9-180">Management service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-181">관리 콘솔 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-181">Name for the Management console website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-182">관리 서비스 포트 바인딩</span><span class="sxs-lookup"><span data-stu-id="af1b9-182">Management service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-183">관리 서비스의 고유 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-183">Unique port number for the Management service.</span></span> <span data-ttu-id="af1b9-184">이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-184">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="af1b9-185">중요</span><span class="sxs-lookup"><span data-stu-id="af1b9-185">Important</span></span>**  
<span data-ttu-id="af1b9-186">웹 관리 콘솔을 여는 브라우저에서 JavaScript를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-186">JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>



### <span data-ttu-id="af1b9-187">관리 서버 데이터베이스 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-187">Management server database prerequisite software</span></span>

<span data-ttu-id="af1b9-188">관리 데이터베이스는 App-v 5.1 관리 서버를 사용 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-188">The Management database is required only if you are using the App-V 5.1 Management server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-189">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="af1b9-189">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="af1b9-190">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-190">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-191">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-191">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-192">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-192">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-193">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-193">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-194">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="af1b9-194">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-195">사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="af1b9-195">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-196">사용할 형식: <strong> INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="af1b9-196">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="af1b9-197">이 형식은 로컬 컴퓨터에 설치 되어 있다고 가정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-197">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="af1b9-198">SVR\INSTANCE 형식으로 이름을 지정 하면 <strong> </strong> 설치에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-198">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-199">사용자 지정 데이터베이스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="af1b9-199">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-200">고유한 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-200">Unique database name.</span></span></p>
<p><span data-ttu-id="af1b9-201">기본값: AppVManagement</span><span class="sxs-lookup"><span data-stu-id="af1b9-201">Default: AppVManagement</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-202">관리 서버 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-202">Management server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-203">관리 서버가 배포 된 컴퓨터 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-203">Machine account on which the Management server is deployed.</span></span></p>
<p><span data-ttu-id="af1b9-204">사용할 형식: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="af1b9-204">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-205">관리 서버 설치 관리자</span><span class="sxs-lookup"><span data-stu-id="af1b9-205">Management server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-206">관리 서버를 설치 하는 데 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-206">Account used to install the Management server.</span></span></p>
<p><span data-ttu-id="af1b9-207">사용할 형식: Domain\관리자 loginname</span><span class="sxs-lookup"><span data-stu-id="af1b9-207">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-208">Microsoft SQL Server 서비스 에이전트</span><span class="sxs-lookup"><span data-stu-id="af1b9-208">Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-209">Microsoft SQL Server 에이전트 서비스가 자동으로 다시 시작 되도록 관리 데이터베이스 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-209">Configure the Management database computer so that the Microsoft SQL Server Agent service is restarted automatically.</span></span> <span data-ttu-id="af1b9-210">지침은 <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> 서비스를 자동으로 다시 시작 하도록 SQL Server 에이전트 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="af1b9-210">For instructions, see <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)">Configure SQL Server Agent to Restart Services Automatically</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="af1b9-211">게시 서버 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-211">Publishing server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-212">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="af1b9-212">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="af1b9-213">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-213">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-214">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-214">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-215">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-215">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-216">64 비트 ASP.NET 등록</span><span class="sxs-lookup"><span data-stu-id="af1b9-216">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-217">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="af1b9-217">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-218">이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-218">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-219">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="af1b9-219">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-220"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-220">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-221">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="af1b9-221">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="af1b9-222">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="af1b9-222">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-223">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="af1b9-223">Static Content</span></span></p></li>
<li><p><span data-ttu-id="af1b9-224">기본 문서</span><span class="sxs-lookup"><span data-stu-id="af1b9-224">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-225">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="af1b9-225">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-226">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="af1b9-226">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="af1b9-227">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="af1b9-227">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="af1b9-228">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="af1b9-228">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="af1b9-229">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="af1b9-229">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-230">보안이</span><span class="sxs-lookup"><span data-stu-id="af1b9-230">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-231">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="af1b9-231">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="af1b9-232">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="af1b9-232">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-233">관리 도구:</span><span class="sxs-lookup"><span data-stu-id="af1b9-233">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-234">IIS 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="af1b9-234">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-235">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-235">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-236">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="af1b9-236">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-237">관리 서비스 URL</span><span class="sxs-lookup"><span data-stu-id="af1b9-237">Management service URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-238">App-v 관리 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-238">URL of the App-V Management service.</span></span> <span data-ttu-id="af1b9-239">이 포트는 게시 서버와 통신 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-239">This is the port with which the Publishing server communicates.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-240">설치 아키텍처</span><span class="sxs-lookup"><span data-stu-id="af1b9-240">Installation architecture</span></span></th>
<th align="left"><span data-ttu-id="af1b9-241">URL에 사용할 형식</span><span class="sxs-lookup"><span data-stu-id="af1b9-241">Format to use for the URL</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-242">관리 서버와 게시 서버가 동일한 서버에 설치 되어 있는 경우</span><span class="sxs-lookup"><span data-stu-id="af1b9-242">Management server and Publishing server are installed on the same server</span></span></p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-243">관리 서버와 게시 서버가 서로 다른 서버에 설치 되어 있는 경우</span><span class="sxs-lookup"><span data-stu-id="af1b9-243">Management server and Publishing server are installed on different servers</span></span></p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-244">게시 서비스 웹 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="af1b9-244">Publishing service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-245">게시 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-245">Name for the Publishing website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-246">게시 서비스 포트 바인딩</span><span class="sxs-lookup"><span data-stu-id="af1b9-246">Publishing service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-247">게시 서비스에 대 한 고유 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-247">Unique port number for the Publishing service.</span></span> <span data-ttu-id="af1b9-248">이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-248">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="af1b9-249">보고 서버 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-249">Reporting server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-250">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="af1b9-250">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="af1b9-251">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-251">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-252">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="af1b9-252">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-253">지원 되는 버전은 <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> app-v 5.1 지원 되는 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="af1b9-253">For supported versions, see <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-254">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-254">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-255">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-255">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-256">64 비트 ASP.NET 등록</span><span class="sxs-lookup"><span data-stu-id="af1b9-256">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-257">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="af1b9-257">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-258">이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-258">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-259">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="af1b9-259">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-260"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-260">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-261">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="af1b9-261">Web Server Role Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-262">보고 서버로 원치 않거나 악의적인 데이터를 보내는 위험을 줄이려면 회사 보안 정책에 따라 보고 웹 서비스에 대 한 액세스를 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-262">To reduce the risk of unwanted or malicious data being sent to the Reporting server, you should restrict access to the Reporting Web Service per your corporate security policy.</span></span></p>
<p><strong><span data-ttu-id="af1b9-263">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="af1b9-263">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-264">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="af1b9-264">Static Content</span></span></p></li>
<li><p><span data-ttu-id="af1b9-265">기본 문서</span><span class="sxs-lookup"><span data-stu-id="af1b9-265">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-266">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="af1b9-266">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-267">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="af1b9-267">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="af1b9-268">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="af1b9-268">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="af1b9-269">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="af1b9-269">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="af1b9-270">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="af1b9-270">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-271">보안이</span><span class="sxs-lookup"><span data-stu-id="af1b9-271">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-272">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="af1b9-272">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="af1b9-273">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="af1b9-273">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="af1b9-274">관리 도구:</span><span class="sxs-lookup"><span data-stu-id="af1b9-274">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="af1b9-275">IIS 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="af1b9-275">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-276">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-276">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-277">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="af1b9-277">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-278">Reporting service 웹 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="af1b9-278">Reporting service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-279">보고 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-279">Name for the Reporting website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-280">Reporting service 포트 바인딩</span><span class="sxs-lookup"><span data-stu-id="af1b9-280">Reporting service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-281">보고 서비스의 고유 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-281">Unique port number for the Reporting service.</span></span> <span data-ttu-id="af1b9-282">이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-282">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="af1b9-283">보고 데이터베이스 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-283">Reporting database prerequisite software</span></span>

<span data-ttu-id="af1b9-284">보고 데이터베이스는 App-v 5.1 Reporting server를 사용 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-284">The Reporting database is required only if you are using the App-V 5.1 Reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-285">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="af1b9-285">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="af1b9-286">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-286">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-287">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-287">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-288">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-288">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-289">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-289">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-290">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="af1b9-290">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-291">사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="af1b9-291">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-292">사용할 형식: <strong> INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="af1b9-292">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="af1b9-293">이 형식은 로컬 컴퓨터에 설치 되어 있다고 가정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-293">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="af1b9-294">SVR\INSTANCE 형식으로 이름을 지정 하면 <strong> </strong> 설치에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-294">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-295">사용자 지정 데이터베이스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="af1b9-295">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-296">고유한 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-296">Unique database name.</span></span></p>
<p><span data-ttu-id="af1b9-297">기본값: AppVReporting</span><span class="sxs-lookup"><span data-stu-id="af1b9-297">Default: AppVReporting</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-298">보고 서버 위치</span><span class="sxs-lookup"><span data-stu-id="af1b9-298">Reporting server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-299">보고 서버가 배포 된 컴퓨터 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-299">Machine account on which the Reporting server is deployed.</span></span></p>
<p><span data-ttu-id="af1b9-300">사용할 형식: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="af1b9-300">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af1b9-301">보고 서버 설치 관리자</span><span class="sxs-lookup"><span data-stu-id="af1b9-301">Reporting server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-302">보고 서버를 설치 하는 데 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-302">Account used to install the Reporting server.</span></span></p>
<p><span data-ttu-id="af1b9-303">사용할 형식: Domain\관리자 loginname</span><span class="sxs-lookup"><span data-stu-id="af1b9-303">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="af1b9-304">Microsoft SQL Server 서비스 및 Microsoft SQL Server 서비스 에이전트</span><span class="sxs-lookup"><span data-stu-id="af1b9-304">Microsoft SQL Server Service and Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="af1b9-305">이러한 서비스가 AD DS를 쿼리할 수 있는 액세스 권한이 있는 사용자 계정과 연결 되도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-305">Configure these services to be associated with user accounts that have access to query AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="af1b9-306">App-v 클라이언트 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-306">App-V client prerequisite software</span></span>


<span data-ttu-id="af1b9-307">App-v 클라이언트에 대해 다음 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-307">Install the following prerequisite software for the App-V client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-308">요소일</span><span class="sxs-lookup"><span data-stu-id="af1b9-308">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="af1b9-309">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-309">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-310">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-310">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="af1b9-311">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="af1b9-311">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="af1b9-312">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-312">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="af1b9-313">KB2533623</span><span class="sxs-lookup"><span data-stu-id="af1b9-313">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="af1b9-314">Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-314">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-315">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-315">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="af1b9-316">원격 데스크톱 서비스 클라이언트 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-316">Remote Desktop Services client prerequisite software</span></span>


<span data-ttu-id="af1b9-317">App-v 원격 데스크톱 서비스 클라이언트에 대 한 다음 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-317">Install the following prerequisite software for the App-V Remote Desktop Services client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-318">요소일</span><span class="sxs-lookup"><span data-stu-id="af1b9-318">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="af1b9-319">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-319">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-320">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-320">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="af1b9-321">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="af1b9-321">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="af1b9-322">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-322">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="af1b9-323">KB2533623</span><span class="sxs-lookup"><span data-stu-id="af1b9-323">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="af1b9-324">Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-324">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="af1b9-325">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="af1b9-325">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="af1b9-326">Sequencer 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="af1b9-326">Sequencer prerequisite software</span></span>


**<span data-ttu-id="af1b9-327">필수 조건을 설치 하기 전에 알아야 할 사항:</span><span class="sxs-lookup"><span data-stu-id="af1b9-327">What to know before installing the prerequisites:</span></span>**

-   <span data-ttu-id="af1b9-328">모범 사례: Sequencer를 실행 하는 컴퓨터는 가상 응용 프로그램을 실행 하는 컴퓨터와 하드웨어 및 소프트웨어 구성이 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-328">Best practice: The computer that runs the Sequencer should have the same hardware and software configurations as the computers that will run the virtual applications.</span></span>

-   <span data-ttu-id="af1b9-329">시퀀싱 프로세스는 리소스를 많이 사용 하므로 시퀀서를 실행 하는 컴퓨터에 메모리가 충분 하 고 빠른 프로세서와 빠른 하드 드라이브가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-329">The sequencing process is resource intensive, so make sure that the computer that runs the Sequencer has plenty of memory, a fast processor, and a fast hard drive.</span></span> <span data-ttu-id="af1b9-330">로컬에 설치 된 응용 프로그램의 시스템 요구 사항은 Sequencer를 초과할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-330">The system requirements of locally installed applications cannot exceed those of the Sequencer.</span></span> <span data-ttu-id="af1b9-331">자세한 내용은 [앱-V 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af1b9-331">For more information, see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af1b9-332">요소일</span><span class="sxs-lookup"><span data-stu-id="af1b9-332">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="af1b9-333">세부 정보</span><span class="sxs-lookup"><span data-stu-id="af1b9-333">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="af1b9-334">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="af1b9-334">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="af1b9-335">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="af1b9-335">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="af1b9-336">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-336">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="af1b9-337">KB2533623</span><span class="sxs-lookup"><span data-stu-id="af1b9-337">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="af1b9-338">Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1b9-338">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="af1b9-339">관련 항목</span><span class="sxs-lookup"><span data-stu-id="af1b9-339">Related topics</span></span>


[<span data-ttu-id="af1b9-340">App-V 5.1 계획</span><span class="sxs-lookup"><span data-stu-id="af1b9-340">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)

[<span data-ttu-id="af1b9-341">App-V 5.1 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="af1b9-341">App-V 5.1 Supported Configurations</span></span>](app-v-51-supported-configurations.md)









