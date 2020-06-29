---
title: App-V 5.0 SP3 필수 구성 요소
description: App-V 5.0 SP3 필수 구성 요소
author: dansimp
ms.assetid: fa8d5578-3a53-4e8a-95c7-e7a5f6e4a31c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e8318a71d2d3631b0ad47e3c3db3c569488790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814801"
---
# <span data-ttu-id="11278-103">App-V 5.0 SP3 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="11278-103">App-V 5.0 SP3 Prerequisites</span></span>


<span data-ttu-id="11278-104">Microsoft App-v (Application Virtualization) 5.0 SP3을 설치 하기 전에 다음 필수 필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-104">Before installing Microsoft Application Virtualization (App-V) 5.0 SP3, ensure that you have installed all of the following required prerequisite software.</span></span>

<span data-ttu-id="11278-105">App-v Server, Sequencer 및 클라이언트에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항 목록은 [app-v 5.0 SP3에서 지원 되는 구성을](app-v-50-sp3-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11278-105">For a list of supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client, see [App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md).</span></span>

## <span data-ttu-id="11278-106">각 운영 체제에 사전 설치 된 소프트웨어 요약</span><span class="sxs-lookup"><span data-stu-id="11278-106">Summary of software preinstalled on each operating system</span></span>


<span data-ttu-id="11278-107">다음 표에는 여러 운영 체제에 대해 이미 설치 된 소프트웨어가 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-107">The following table indicates the software that is already installed for different operating systems.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-108">운영 체제</span><span class="sxs-lookup"><span data-stu-id="11278-108">Operating system</span></span></th>
<th align="left"><span data-ttu-id="11278-109">필수 구성 요소 설명</span><span class="sxs-lookup"><span data-stu-id="11278-109">Prerequisite description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-110">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="11278-110">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-111">모든 필수 소프트웨어는 이미 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-111">All of the prerequisite software is already installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-112">Windows8</span><span class="sxs-lookup"><span data-stu-id="11278-112">Windows 8</span></span></p>
<p><span data-ttu-id="11278-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11278-113">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-114">다음 필수 소프트웨어는 이미 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-114">The following prerequisite software is already installed:</span></span></p>
<ul>
<li><p><span data-ttu-id="11278-115">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="11278-115">Microsoft .NET Framework 4.5</span></span></p></li>
<li><p><span data-ttu-id="11278-116">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="11278-116">Windows PowerShell 3.0</span></span></p>
<div class="alert">
<strong><span data-ttu-id="11278-117">참고</span><span class="sxs-lookup"><span data-stu-id="11278-117">Note</span></span></strong><br/><p><span data-ttu-id="11278-118">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-118">Installing PowerShell 3.0 requires a restart.</span></span></p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="11278-119">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-120">필수 소프트웨어는 아직 설치 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-120">The prerequisite software is not already installed.</span></span> <span data-ttu-id="11278-121">App-v를 설치 하려면 먼저 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-121">You must install it before you can install App-V.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="11278-122">App-v Server 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-122">App-V Server prerequisite software</span></span>


<span data-ttu-id="11278-123">App-v 5.0 SP3 서버 구성 요소에 필요한 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-123">Install the required prerequisite software for the App-V 5.0 SP3 Server components.</span></span>

### <span data-ttu-id="11278-124">시작 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="11278-124">What to know before you start</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-125">App-v 서버 설치 계정</span><span class="sxs-lookup"><span data-stu-id="11278-125">Account for installing the App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-126">App-v 서버 구성 요소를 설치 하는 데 사용 하는 계정에는 다음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-126">The account that you use to install the App-V Server components must have:</span></span></p>
<ul>
<li><p><span data-ttu-id="11278-127">구성 요소를 설치 하는 컴퓨터에 대 한 관리자 권한</span><span class="sxs-lookup"><span data-stu-id="11278-127">Administrative rights on the computer on which you are installing the components.</span></span></p></li>
<li><p><span data-ttu-id="11278-128">Active Directory 도메인 서비스를 쿼리 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-128">The ability to query Active Directory Domain Services.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-129">포트 및 방화벽</span><span class="sxs-lookup"><span data-stu-id="11278-129">Port and firewall</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="11278-130">각 구성 요소를 호스트할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-130">Specify a port where each component will be hosted.</span></span></p></li>
<li><p><span data-ttu-id="11278-131">지정 된 포트로 들어오는 요청을 허용 하는 연결 된 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-131">Add the associated firewall rules to allow incoming requests to the specified ports.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-132">WebDAV (웹 분산 작성 및 버전 관리)</span><span class="sxs-lookup"><span data-stu-id="11278-132">Web Distributed Authoring and Versioning (WebDAV)</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-133">WebDAV는 관리 서비스에 대해 자동으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-133">WebDAV is automatically disabled for the Management Service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-134">지원 되는 배포 시나리오</span><span class="sxs-lookup"><span data-stu-id="11278-134">Supported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="11278-135">모든 구성 요소가 동일한 서버에 배포 되는 독립 실행형 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-135">A stand-alone deployment, where all components are deployed on the same server.</span></span></p></li>
<li><p><span data-ttu-id="11278-136">분산 배포.</span><span class="sxs-lookup"><span data-stu-id="11278-136">A distributed deployment.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-137">지원 되지 않는 배포 시나리오</span><span class="sxs-lookup"><span data-stu-id="11278-137">Unsupported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="11278-138">앱-v의 이전 버전 또는 구성 요소를 실행 하는 컴퓨터에 App-v Server를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-138">Installing the App-V Server on a computer that runs any previous version or component of App-V.</span></span></p></li>
<li><p><span data-ttu-id="11278-139">Server core 또는 도메인 컨트롤러를 실행 하는 컴퓨터에 App-v 서버 구성 요소 설치</span><span class="sxs-lookup"><span data-stu-id="11278-139">Installing the App-V server components on a computer that runs server core or domain controller.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="11278-140">관리 서버 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-140">Management server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-141">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="11278-141">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="11278-142">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-143">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="11278-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-144">지원 되는 버전의 경우 <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> app-v 5.0 SP3에서 지원 되는 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="11278-144">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-145">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-145">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="11278-146">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="11278-146">Windows PowerShell 3.0</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="11278-147">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-147">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-148">KB2533623 다운로드 및 설치 <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"></span><span class="sxs-lookup"><span data-stu-id="11278-148">Download and install <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="11278-149">Windows 7에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11278-149">Applies to Windows 7 only.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-150">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-150">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-151">64 비트 ASP.NET 등록</span><span class="sxs-lookup"><span data-stu-id="11278-151">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-152">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="11278-152">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-153">이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-153">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-154">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="11278-154">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-155"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-155">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-156">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="11278-156">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="11278-157">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="11278-157">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-158">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="11278-158">Static Content</span></span></p></li>
<li><p><span data-ttu-id="11278-159">기본 문서</span><span class="sxs-lookup"><span data-stu-id="11278-159">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-160">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="11278-160">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-161">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="11278-161">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="11278-162">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="11278-162">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="11278-163">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="11278-163">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="11278-164">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="11278-164">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-165">보안이</span><span class="sxs-lookup"><span data-stu-id="11278-165">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-166">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="11278-166">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="11278-167">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="11278-167">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-168">관리 도구:</span><span class="sxs-lookup"><span data-stu-id="11278-168">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-169">IIS 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="11278-169">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-170">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="11278-170">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-171">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="11278-171">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-172">관리 데이터베이스의 위치</span><span class="sxs-lookup"><span data-stu-id="11278-172">Location of the Management database</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-173">SQL Server 데이터베이스 이름, SQL Server 데이터베이스 인스턴스 이름, 데이터베이스 이름.</span><span class="sxs-lookup"><span data-stu-id="11278-173">SQL Server database name, SQL Server database instance name, and database name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-174">관리 콘솔 및 관리 데이터베이스 권한</span><span class="sxs-lookup"><span data-stu-id="11278-174">Management console and Management database permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-175">배포 완료 후 관리 콘솔과 데이터베이스에 액세스할 수 있는 사용자 또는 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-175">A user or group that can access the Management console and database after the deployment is complete.</span></span> <span data-ttu-id="11278-176">관리 콘솔을 사용 하 여 추가 관리자가 추가 되지 않는 한 이러한 사용자 또는 그룹만 관리 콘솔과 데이터베이스에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-176">Only these users or groups will have access to the Management console and database unless additional administrators are added by using the Management console.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-177">관리 서비스 웹 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="11278-177">Management service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-178">관리 콘솔 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-178">Name for the Management console website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-179">관리 서비스 포트 바인딩</span><span class="sxs-lookup"><span data-stu-id="11278-179">Management service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-180">관리 서비스의 고유 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-180">Unique port number for the Management service.</span></span> <span data-ttu-id="11278-181">이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-181">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-182">Microsoft Silverlight 5</span><span class="sxs-lookup"><span data-stu-id="11278-182">Microsoft Silverlight 5</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-183">관리 콘솔은 Silverlight가 설치 된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-183">The Management console is available only if Silverlight is installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="11278-184">관리 서버 데이터베이스 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-184">Management server database prerequisite software</span></span>

<span data-ttu-id="11278-185">관리 데이터베이스는 App-v 5.0 SP3 관리 서버를 사용 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-185">The Management database is required only if you are using the App-V 5.0 SP3 Management server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-186">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="11278-186">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="11278-187">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-187">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-188">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-188">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-189">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-189">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-190">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="11278-190">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-191">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="11278-191">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-192">사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="11278-192">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-193">사용할 형식: <strong> INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="11278-193">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="11278-194">이 형식은 로컬 컴퓨터에 설치 되어 있다고 가정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11278-194">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="11278-195">SVR\INSTANCE 형식으로 이름을 지정 하면 <strong> </strong> 설치에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-195">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-196">사용자 지정 데이터베이스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="11278-196">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-197">고유한 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-197">Unique database name.</span></span></p>
<p><span data-ttu-id="11278-198">기본값: AppVManagement</span><span class="sxs-lookup"><span data-stu-id="11278-198">Default: AppVManagement</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-199">관리 서버 위치</span><span class="sxs-lookup"><span data-stu-id="11278-199">Management server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-200">관리 서버가 배포 된 컴퓨터 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-200">Machine account on which the Management server is deployed.</span></span></p>
<p><span data-ttu-id="11278-201">사용할 형식: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="11278-201">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-202">관리 서버 설치 관리자</span><span class="sxs-lookup"><span data-stu-id="11278-202">Management server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-203">관리 서버를 설치 하는 데 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-203">Account used to install the Management server.</span></span></p>
<p><span data-ttu-id="11278-204">사용할 형식: Domain\관리자 loginname</span><span class="sxs-lookup"><span data-stu-id="11278-204">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-205">Microsoft SQL Server 서비스 에이전트</span><span class="sxs-lookup"><span data-stu-id="11278-205">Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-206">Microsoft SQL Server 에이전트 서비스가 자동으로 다시 시작 되도록 관리 데이터베이스 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-206">Configure the Management database computer so that the Microsoft SQL Server Agent service is restarted automatically.</span></span> <span data-ttu-id="11278-207">지침은 <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> 서비스를 자동으로 다시 시작 하도록 SQL Server 에이전트 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="11278-207">For instructions, see <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)">Configure SQL Server Agent to Restart Services Automatically</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="11278-208">게시 서버 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-208">Publishing server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-209">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="11278-209">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="11278-210">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-210">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-211">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-211">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-212">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-212">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-213">64 비트 ASP.NET 등록</span><span class="sxs-lookup"><span data-stu-id="11278-213">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-214">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="11278-214">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-215">이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-215">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-216">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="11278-216">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-217"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-217">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-218">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="11278-218">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="11278-219">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="11278-219">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-220">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="11278-220">Static Content</span></span></p></li>
<li><p><span data-ttu-id="11278-221">기본 문서</span><span class="sxs-lookup"><span data-stu-id="11278-221">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-222">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="11278-222">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-223">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="11278-223">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="11278-224">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="11278-224">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="11278-225">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="11278-225">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="11278-226">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="11278-226">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-227">보안이</span><span class="sxs-lookup"><span data-stu-id="11278-227">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-228">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="11278-228">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="11278-229">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="11278-229">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-230">관리 도구:</span><span class="sxs-lookup"><span data-stu-id="11278-230">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-231">IIS 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="11278-231">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-232">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="11278-232">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-233">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="11278-233">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-234">관리 서비스 URL</span><span class="sxs-lookup"><span data-stu-id="11278-234">Management service URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-235">App-v 관리 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-235">URL of the App-V Management service.</span></span> <span data-ttu-id="11278-236">이 포트는 게시 서버와 통신 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11278-236">This is the port with which the Publishing server communicates.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-237">설치 아키텍처</span><span class="sxs-lookup"><span data-stu-id="11278-237">Installation architecture</span></span></th>
<th align="left"><span data-ttu-id="11278-238">URL에 사용할 형식</span><span class="sxs-lookup"><span data-stu-id="11278-238">Format to use for the URL</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-239">관리 서버와 게시 서버가 동일한 서버에 설치 되어 있는 경우</span><span class="sxs-lookup"><span data-stu-id="11278-239">Management server and Publishing server are installed on the same server</span></span></p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-240">관리 서버와 게시 서버가 서로 다른 서버에 설치 되어 있는 경우</span><span class="sxs-lookup"><span data-stu-id="11278-240">Management server and Publishing server are installed on different servers</span></span></p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-241">게시 서비스 웹 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="11278-241">Publishing service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-242">게시 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-242">Name for the Publishing website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-243">게시 서비스 포트 바인딩</span><span class="sxs-lookup"><span data-stu-id="11278-243">Publishing service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-244">게시 서비스에 대 한 고유 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-244">Unique port number for the Publishing service.</span></span> <span data-ttu-id="11278-245">이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-245">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="11278-246">보고 서버 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-246">Reporting server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-247">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="11278-247">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="11278-248">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-249">지원 되는 SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="11278-249">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-250">지원 되는 버전의 경우 <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> app-v 5.0 SP3에서 지원 되는 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="11278-250">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-251">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-251">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-252">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-252">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-253">64 비트 ASP.NET 등록</span><span class="sxs-lookup"><span data-stu-id="11278-253">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-254">Windows Server 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="11278-254">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-255">이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-255">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-256">웹 서버 (IIS) 관리 도구</span><span class="sxs-lookup"><span data-stu-id="11278-256">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-257"><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-257">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-258">웹 서버 역할 서비스</span><span class="sxs-lookup"><span data-stu-id="11278-258">Web Server Role Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-259">보고 서버로 원치 않거나 악의적인 데이터를 보내는 위험을 줄이려면 회사 보안 정책에 따라 보고 웹 서비스에 대 한 액세스를 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-259">To reduce the risk of unwanted or malicious data being sent to the Reporting server, you should restrict access to the Reporting Web Service per your corporate security policy.</span></span></p>
<p><strong><span data-ttu-id="11278-260">일반적인 HTTP 기능:</span><span class="sxs-lookup"><span data-stu-id="11278-260">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-261">정적 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="11278-261">Static Content</span></span></p></li>
<li><p><span data-ttu-id="11278-262">기본 문서</span><span class="sxs-lookup"><span data-stu-id="11278-262">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-263">응용 프로그램 개발:</span><span class="sxs-lookup"><span data-stu-id="11278-263">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-264">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="11278-264">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="11278-265">.NET 확장성</span><span class="sxs-lookup"><span data-stu-id="11278-265">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="11278-266">ISAPI 확장</span><span class="sxs-lookup"><span data-stu-id="11278-266">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="11278-267">ISAPI 필터</span><span class="sxs-lookup"><span data-stu-id="11278-267">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-268">보안이</span><span class="sxs-lookup"><span data-stu-id="11278-268">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-269">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="11278-269">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="11278-270">요청 필터링</span><span class="sxs-lookup"><span data-stu-id="11278-270">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="11278-271">관리 도구:</span><span class="sxs-lookup"><span data-stu-id="11278-271">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11278-272">IIS 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="11278-272">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-273">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="11278-273">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-274">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="11278-274">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-275">Reporting service 웹 사이트 이름</span><span class="sxs-lookup"><span data-stu-id="11278-275">Reporting service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-276">보고 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-276">Name for the Reporting website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-277">Reporting service 포트 바인딩</span><span class="sxs-lookup"><span data-stu-id="11278-277">Reporting service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-278">보고 서비스의 고유 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-278">Unique port number for the Reporting service.</span></span> <span data-ttu-id="11278-279">이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-279">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="11278-280">보고 데이터베이스 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-280">Reporting database prerequisite software</span></span>

<span data-ttu-id="11278-281">Reporting database는 App-v 5.0 SP3 보고 서버를 사용 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-281">The Reporting database is required only if you are using the App-V 5.0 SP3 Reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-282">필수 구성 요소 및 필수 설정</span><span class="sxs-lookup"><span data-stu-id="11278-282">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="11278-283">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-283">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-284">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-284">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-285">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-285">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-286">기본 설치 위치</span><span class="sxs-lookup"><span data-stu-id="11278-286">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-287">%PROGRAMFILES%\Microsoft Application Virtualization 서버</span><span class="sxs-lookup"><span data-stu-id="11278-287">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-288">사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="11278-288">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-289">사용할 형식: <strong> INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="11278-289">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="11278-290">이 형식은 로컬 컴퓨터에 설치 되어 있다고 가정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11278-290">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="11278-291">SVR\INSTANCE 형식으로 이름을 지정 하면 <strong> </strong> 설치에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-291">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-292">사용자 지정 데이터베이스 이름 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="11278-292">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-293">고유한 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-293">Unique database name.</span></span></p>
<p><span data-ttu-id="11278-294">기본값: AppVReporting</span><span class="sxs-lookup"><span data-stu-id="11278-294">Default: AppVReporting</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-295">보고 서버 위치</span><span class="sxs-lookup"><span data-stu-id="11278-295">Reporting server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-296">보고 서버가 배포 된 컴퓨터 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-296">Machine account on which the Reporting server is deployed.</span></span></p>
<p><span data-ttu-id="11278-297">사용할 형식: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="11278-297">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11278-298">보고 서버 설치 관리자</span><span class="sxs-lookup"><span data-stu-id="11278-298">Reporting server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-299">보고 서버를 설치 하는 데 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11278-299">Account used to install the Reporting server.</span></span></p>
<p><span data-ttu-id="11278-300">사용할 형식: Domain\관리자 loginname</span><span class="sxs-lookup"><span data-stu-id="11278-300">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11278-301">Microsoft SQL Server 서비스 및 Microsoft SQL Server 서비스 에이전트</span><span class="sxs-lookup"><span data-stu-id="11278-301">Microsoft SQL Server Service and Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="11278-302">이러한 서비스가 AD DS를 쿼리할 수 있는 액세스 권한이 있는 사용자 계정과 연결 되도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-302">Configure these services to be associated with user accounts that have access to query AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="11278-303">App-v 클라이언트 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-303">App-V client prerequisite software</span></span>


<span data-ttu-id="11278-304">App-v 클라이언트에 대해 다음 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-304">Install the following prerequisite software for the App-V client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-305">요소일</span><span class="sxs-lookup"><span data-stu-id="11278-305">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="11278-306">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-306">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-307">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-307">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="11278-308">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="11278-308">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="11278-309">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-309">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="11278-310">KB2533623</span><span class="sxs-lookup"><span data-stu-id="11278-310">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="11278-311">Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-311">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-312">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-312">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="11278-313">원격 데스크톱 서비스 클라이언트 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-313">Remote Desktop Services client prerequisite software</span></span>


<span data-ttu-id="11278-314">App-v 원격 데스크톱 서비스 클라이언트에 대 한 다음 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-314">Install the following prerequisite software for the App-V Remote Desktop Services client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-315">요소일</span><span class="sxs-lookup"><span data-stu-id="11278-315">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="11278-316">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-316">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-317">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-317">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="11278-318">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="11278-318">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="11278-319">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-319">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="11278-320">KB2533623</span><span class="sxs-lookup"><span data-stu-id="11278-320">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="11278-321">Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-321">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-322">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-322">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="11278-323">Sequencer 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="11278-323">Sequencer prerequisite software</span></span>


**<span data-ttu-id="11278-324">필수 조건을 설치 하기 전에 알아야 할 사항:</span><span class="sxs-lookup"><span data-stu-id="11278-324">What to know before installing the prerequisites:</span></span>**

-   <span data-ttu-id="11278-325">모범 사례: Sequencer를 실행 하는 컴퓨터는 가상 응용 프로그램을 실행 하는 컴퓨터와 하드웨어 및 소프트웨어 구성이 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-325">Best practice: The computer that runs the Sequencer should have the same hardware and software configurations as the computers that will run the virtual applications.</span></span>

-   <span data-ttu-id="11278-326">시퀀싱 프로세스는 리소스를 많이 사용 하므로 시퀀서를 실행 하는 컴퓨터에 메모리가 충분 하 고 빠른 프로세서와 빠른 하드 드라이브가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-326">The sequencing process is resource intensive, so make sure that the computer that runs the Sequencer has plenty of memory, a fast processor, and a fast hard drive.</span></span> <span data-ttu-id="11278-327">로컬에 설치 된 응용 프로그램의 시스템 요구 사항은 Sequencer를 초과할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11278-327">The system requirements of locally installed applications cannot exceed those of the Sequencer.</span></span> <span data-ttu-id="11278-328">자세한 내용은 [앱-V 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11278-328">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11278-329">요소일</span><span class="sxs-lookup"><span data-stu-id="11278-329">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="11278-330">세부 정보</span><span class="sxs-lookup"><span data-stu-id="11278-330">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="11278-331">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</span><span class="sxs-lookup"><span data-stu-id="11278-331">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="11278-332">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="11278-332">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="11278-333">PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-333">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="11278-334">KB2533623</span><span class="sxs-lookup"><span data-stu-id="11278-334">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="11278-335">Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11278-335">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="11278-336">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</span><span class="sxs-lookup"><span data-stu-id="11278-336">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="11278-337">관련 항목</span><span class="sxs-lookup"><span data-stu-id="11278-337">Related topics</span></span>


[<span data-ttu-id="11278-338">App-V 5.0 계획</span><span class="sxs-lookup"><span data-stu-id="11278-338">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

[<span data-ttu-id="11278-339">App-V 5.0 SP3 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="11278-339">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)









