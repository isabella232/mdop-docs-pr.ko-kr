---
title: App-V 5.0 SP3 정보
description: App-V 5.0 SP3 정보
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814973"
---
# <span data-ttu-id="cb23b-103">App-V 5.0 SP3 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="cb23b-104">다음 섹션을 사용 하 여 Microsoft Application Virtualization (App-v) 5.0 SP3에 적용 되는 중요 한 변경 사항에 대 한 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="cb23b-105">앱-V 5.0 SP3 소프트웨어 필수 구성 요소 및 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="cb23b-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="cb23b-106">App-V 5.0 SP3으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="cb23b-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="cb23b-107">수동으로 만든 연결 그룹 xml 파일에는 스키마 업데이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="cb23b-108">연결 그룹 개선</span><span class="sxs-lookup"><span data-stu-id="cb23b-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="cb23b-109">관리자가 특정 사용자를 위해 패키지를 게시 하 고 게시 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="cb23b-110">패키지 게시 및 게시 취소를 위해 관리자만 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="cb23b-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="cb23b-111">RunVirtual registry 키는 사용자에 게 게시 되는 패키지를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="cb23b-112">새 PowerShell cmdlet 및 업데이트 가능한 cmdlet 도움말</span><span class="sxs-lookup"><span data-stu-id="cb23b-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="cb23b-113">PVAD (주 가상 응용 프로그램 디렉터리)가 숨겨져 있지만 켤 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="cb23b-114">App-v 게시 메타 데이터를 보려면 ClientVersion이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="cb23b-115">App-v 이벤트 로그가 통합 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="cb23b-116">앱-V 5.0 SP3 소프트웨어 필수 구성 요소 및 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="cb23b-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="cb23b-117">App-v 5.0 SP3 소프트웨어 요구 사항 및 지원 되는 구성에 대 한 다음 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-118">전제 조건과 지원 되는 구성에 대 한 링크</span><span class="sxs-lookup"><span data-stu-id="cb23b-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="cb23b-119">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="cb23b-120">App-V 5.0 SP3 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cb23b-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="cb23b-121">App-v 5.0 SP3 설치를 시작 하기 전에 설치 해야 하는 필수 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="cb23b-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="cb23b-122">App-V 5.0 SP3 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="cb23b-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="cb23b-123">App-v Server, Sequencer 및 클라이언트 구성 요소에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="cb23b-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="cb23b-124">App-V 5.0 SP3으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="cb23b-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="cb23b-125">다음 정보를 사용 하 여 이전 버전의 App-v 5.0 SP3으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="cb23b-126">업그레이드를 시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="cb23b-126">Before you start the upgrade</span></span>

<span data-ttu-id="cb23b-127">업그레이드를 시작 하기 전에 다음 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-128">업그레이드 하기 전에 검토할 항목</span><span class="sxs-lookup"><span data-stu-id="cb23b-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="cb23b-129">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-130">업그레이드할 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cb23b-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="cb23b-131">App-v Server</span><span class="sxs-lookup"><span data-stu-id="cb23b-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="cb23b-132">않았음이</span><span class="sxs-lookup"><span data-stu-id="cb23b-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="cb23b-133">앱-V 클라이언트 또는 App-v (원격 데스크톱 서비스) 클라이언트</span><span class="sxs-lookup"><span data-stu-id="cb23b-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="cb23b-134">연결 그룹</span><span class="sxs-lookup"><span data-stu-id="cb23b-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="cb23b-135">참고</span><span class="sxs-lookup"><span data-stu-id="cb23b-135">Note</span></span></strong><br/><p><span data-ttu-id="cb23b-136">App-v 클라이언트 사용자 인터페이스를 사용 하려면 <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> Microsoft Application Virtualization 5.0 클라이언트 UI 응용 프로그램에서 기존 버전을 다운로드 </a> 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-137">앱-V 4. x에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="cb23b-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-138">먼저 App-v 5.0으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="cb23b-139">앱-V 4. x에서 App-v 5.0 SP3으로 직접 업그레이드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="cb23b-140">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="cb23b-141">App-V 5.0 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="cb23b-142">App-V의 이전 버전에서 마이그레이션 계획</span><span class="sxs-lookup"><span data-stu-id="cb23b-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-143">앱-V 5.0 이상에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="cb23b-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-144">다음 버전 중 하나에서 앱-V 5.0 SP3으로 직접 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="cb23b-145">App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="cb23b-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="cb23b-146">App-v 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="cb23b-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="cb23b-147">App-v 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="cb23b-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="cb23b-148">App-v 5.0 SP3으로 업그레이드 하려면이 문서의 나머지 섹션에 나와 있는 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-149">업그레이드 후 패키지 및 연결 그룹의 필수 변경 사항</span><span class="sxs-lookup"><span data-stu-id="cb23b-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-150">없음.</span><span class="sxs-lookup"><span data-stu-id="cb23b-150">None.</span></span> <span data-ttu-id="cb23b-151">패키지 및 연결 그룹은 현재 처럼 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="cb23b-152">앱-V 인프라를 업그레이드 하는 단계</span><span class="sxs-lookup"><span data-stu-id="cb23b-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="cb23b-153">앱-V 인프라의 각 구성 요소를 App-v 5.0 SP3으로 업그레이드 하려면 다음 단계를 완료 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-154">단계</span><span class="sxs-lookup"><span data-stu-id="cb23b-154">Step</span></span></th>
<th align="left"><span data-ttu-id="cb23b-155">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-156">1 단계: App-v Server를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="cb23b-157">App-v 서버를 사용 하지 않는 경우에는이 단계를 건너뛰고 다음 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cb23b-158">참고</span><span class="sxs-lookup"><span data-stu-id="cb23b-158">Note</span></span></strong><br/><p><span data-ttu-id="cb23b-159">App-v 5.0 SP3 클라이언트는 App-v 5.0 SP1 서버와 호환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="cb23b-160">다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="cb23b-161">App-v <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> </a> Server 설치에 영향을 줄 수 있는 문제에 대 한 앱-v 5.0 SP3 릴리스 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="cb23b-162">관리 데이터베이스 및/또는 보고 데이터베이스를 업그레이드 하는 데 사용 하는 방법에 따라 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-163">데이터베이스 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="cb23b-164">단계</span><span class="sxs-lookup"><span data-stu-id="cb23b-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-165">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb23b-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-166">이 단계를 건너뛰고 3 단계 ("App-v Server를 업그레이드 하는 경우 ...")로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-167">SQL 스크립트</span><span class="sxs-lookup"><span data-stu-id="cb23b-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cb23b-168">관리 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="cb23b-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-169">설치 또는 업그레이드 하려면 <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> SQL 스크립트를 설치 또는 업그레이드 (app-v 5.0 SP3 관리 서버 데이터베이스 실패)를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cb23b-170">보고 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="cb23b-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-171"><a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법의 단계를 따릅니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="cb23b-172">App-v 5.0 SP1 핫픽스 패키지 3 이상에서 App-v 서버를 업그레이드 하는 경우 <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> app-v 5.0 SP3 서버 설치 후 레지스트리 키 확인 섹션의 단계를 완료 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="cb23b-173"><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">App-v 5.0 서버를 배포 하는 방법의 단계를 따릅니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-174">2 단계: App-v Sequencer를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-175"><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">Sequencer를 설치 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-176">3 단계: App-v 클라이언트 또는 App-v RDS 클라이언트를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-177"><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">App-v 클라이언트를 배포 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="cb23b-178">App-v 5.0 SP3 서버를 설치 하기 전에 레지스트리 키 확인</span><span class="sxs-lookup"><span data-stu-id="cb23b-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="cb23b-179">앞의 표에 있는 3 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cb23b-180">이 단계가 필요한 경우</span><span class="sxs-lookup"><span data-stu-id="cb23b-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-181">.Msp 파일을 사용 하 여 설치한 이후 핫픽스 패키지를 사용 하 여 App-v SP1에서 업그레이드 하는 경우</span><span class="sxs-lookup"><span data-stu-id="cb23b-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cb23b-182">이 단계를 수행 해야 하는 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cb23b-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-183">업그레이드 하는 App-v 서버 구성 요소만</span><span class="sxs-lookup"><span data-stu-id="cb23b-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cb23b-184">이 단계를 수행 해야 하는 경우</span><span class="sxs-lookup"><span data-stu-id="cb23b-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-185">앱-V 5.0 SP3으로 업그레이드 하기 전에</span><span class="sxs-lookup"><span data-stu-id="cb23b-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cb23b-186">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="cb23b-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-187">다음 표의 정보를 사용 하 여 <code>HKLM\Software\Microsoft\AppV\Server</code> 원래 서버 설치에서 제공한 값으로 각 레지스트리 키 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="cb23b-188">이 단계를 완료 하면 App-v SP1 핫픽스 패키지를 설치할 때 제거 되었을 수 있는 레지스트리 값이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="cb23b-189">ManagementDatabase 키</span><span class="sxs-lookup"><span data-stu-id="cb23b-189">ManagementDatabase key</span></span>**

<span data-ttu-id="cb23b-190">관리 데이터베이스를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-191">키 이름</span><span class="sxs-lookup"><span data-stu-id="cb23b-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="cb23b-192">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="cb23b-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-194">공용 액세스 계정이 비로컬 관리 데이터베이스에 액세스 하는 데 필요한 지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="cb23b-195">필요한 경우 값이 "1"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="cb23b-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-197">관리 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-199">관리 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="cb23b-200"><code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="cb23b-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-202">관리 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="cb23b-203"><code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cb23b-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-205">관리 데이터베이스용 SQL Server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="cb23b-206">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-208">관리 데이터베이스에 대 한 쓰기 (관리자) 액세스에 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="cb23b-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-210">관리 데이터베이스에 대 한 쓰기 (관리자) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-212">관리 서버 원격 컴퓨터 계정 (계정).</span><span class="sxs-lookup"><span data-stu-id="cb23b-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-214">관리 서버 (%0)에 대 한 설치 관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="cb23b-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="cb23b-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-216">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="cb23b-217">1 </strong> – 관리 서비스가 로컬 컴퓨터에 있으며,이는 MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="cb23b-218">0 </strong> - 관리 서비스는 로컬 컴퓨터와 다른 컴퓨터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="cb23b-219">ManagementService 키</span><span class="sxs-lookup"><span data-stu-id="cb23b-219">ManagementService key</span></span>**

<span data-ttu-id="cb23b-220">관리 서버를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ManagementService` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-221">키 이름</span><span class="sxs-lookup"><span data-stu-id="cb23b-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="cb23b-222">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-224">AD DS (Active Directory 도메인 서비스) 그룹 또는 App.config (App-v) 관리 권한이 있는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cb23b-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-226">관리 데이터베이스를 포함 하는 SQL server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="cb23b-227">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="cb23b-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-229">관리 데이터베이스를 사용 하는 원격 SQL 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="cb23b-230">값이 비어 있으면 로컬 컴퓨터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="cb23b-231">ReportingDatabase 키</span><span class="sxs-lookup"><span data-stu-id="cb23b-231">ReportingDatabase key</span></span>**

<span data-ttu-id="cb23b-232">보고 데이터베이스를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-233">키 이름</span><span class="sxs-lookup"><span data-stu-id="cb23b-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="cb23b-234">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="cb23b-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-236">로컬이 아닌 보고 데이터베이스에 액세스 하는 데 공개 액세스 계정이 필요한 지 여부를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="cb23b-237">필요한 경우 값이 "1"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="cb23b-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-239">보고 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-241">보고 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="cb23b-242"><code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="cb23b-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-244">보고 데이터베이스에 대 한 읽기 (공개) 액세스에 사용 되는 계정의 SID (보안 식별자)입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="cb23b-245"><code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code>이 1로 설정 된 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cb23b-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-247">보고 데이터베이스용 SQL Server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="cb23b-248">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="cb23b-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-252">Reporting server 컴퓨터 계정 (계정)</span><span class="sxs-lookup"><span data-stu-id="cb23b-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="cb23b-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-254">Reporting server (%0)에 대 한 설치 관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="cb23b-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="cb23b-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-256">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="cb23b-257">1 </strong> – Reporting service가 로컬 컴퓨터에 있으며,이는 REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="cb23b-258">0 </strong> - Reporting services가 로컬 컴퓨터와 다른 컴퓨터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="cb23b-259">ReportingService 키</span><span class="sxs-lookup"><span data-stu-id="cb23b-259">ReportingService key</span></span>**

<span data-ttu-id="cb23b-260">보고 서버를 설치 하는 경우 다음 레지스트리 키를 설정 `HKLM\Software\Microsoft\AppV\Server\ReportingService` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-261">키 이름</span><span class="sxs-lookup"><span data-stu-id="cb23b-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="cb23b-262">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cb23b-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-264">보고 데이터베이스용 SQL Server 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="cb23b-265">값이 비어 있으면 기본 데이터베이스 인스턴스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="cb23b-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-267">보고 데이터베이스를 사용 하는 원격 SQL 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="cb23b-268">값이 비어 있으면 로컬 컴퓨터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="cb23b-269">수동으로 만든 연결 그룹 xml 파일에는 스키마 업데이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="cb23b-270">연결 그룹 XML 파일을 수동으로 만들고 [연결 그룹 개선](#bkmk-cg-improvements)에 설명 된 새 "선택적 패키지" 및 "모든 버전 사용" 기능을 사용 하려는 경우 XML 파일에서 다음 스키마를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="cb23b-271">예제 및 자세한 내용은 [연결 그룹 파일 정보](about-the-connection-group-file.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="cb23b-272">연결 그룹 개선</span><span class="sxs-lookup"><span data-stu-id="cb23b-272">Improvements to connection groups</span></span>


<span data-ttu-id="cb23b-273">앱-V 5.0 SP3에 추가 된 선택적 패키지 및 기타 개선 기능을 사용 하 여 연결 그룹을 더욱 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="cb23b-274">다음 표에서는 새 연결 그룹 기능을 사용 하 여 수행할 수 있는 작업과 각 작업에 대 한 자세한 정보에 대 한 링크를 요약 하 여 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-275">작업/기능</span><span class="sxs-lookup"><span data-stu-id="cb23b-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="cb23b-276">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-276">Description</span></span></th>
<th align="left"><span data-ttu-id="cb23b-277">추가 정보 링크</span><span class="sxs-lookup"><span data-stu-id="cb23b-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-278">연결 그룹이 선택적 패키지를 포함 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="cb23b-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-279">연결 그룹에 선택적 패키지를 포함 하면 사용자가 제공 하는 응용 프로그램에 따라 연결 그룹의 가상 환경에 포함 될 응용 프로그램을 동적으로 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="cb23b-280">여러 개의 연결 그룹을 관리 하는 것은 동일한 연결 그룹에서 선택적 및 선택 사항이 아닌 패키지를 혼합할 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="cb23b-281">패키지를 혼합 하면 사용자가 공통 된 패키지를 하나만 가질 수 있지만 서로 다른 사용자 그룹이 동일한 연결 그룹을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="cb23b-282">예 </strong> : 모든 사용자에 대해 Microsoft Office를 사용 하 여 패키지를 사용 하도록 설정할 수 있지만 다양 한 Office 플러그 인을 사용자의 다른 하위 집합에 포함 하는 다양 한 선택적 패키지를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="cb23b-283">연결 그룹에서 선택적 패키지를 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-284">연결 그룹을 변경 하지 않고 선택 패키지 게시 취소 또는 삭제</span><span class="sxs-lookup"><span data-stu-id="cb23b-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-285">앱-V 클라이언트에서 연결 그룹을 비활성화 하거나 다시 사용 하도록 설정 하지 않고 연결 그룹에 있는 선택적 패키지를 게시 취소 하거나 게시 취소 하 고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="cb23b-286">연결 그룹에서 선택적 패키지를 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-287">사용자 게시 및 전역 게시 패키지가 포함 된 연결 그룹 게시</span><span class="sxs-lookup"><span data-stu-id="cb23b-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-288">사용자가 게시 하 고 전역적으로 게시 된 패키지를 포함 하는 사용자 게시 연결 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="cb23b-289">사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-290">연결 그룹에서 패키지 버전을 무시 하도록 만들기</span><span class="sxs-lookup"><span data-stu-id="cb23b-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-291">연결 그룹을 사용 하지 않도록 설정 하지 않고 패키지를 업그레이드할 수 있도록 모든 버전의 패키지를 받아들이도록 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="cb23b-292">또한 연결 그룹에 잘못 된 버전이 있는 선택적 패키지가 있는 경우 패키지가 무시 되 고 연결 그룹의 가상 환경이 만들어지지 않도록 차단 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="cb23b-293">연결 그룹에서 패키지 버전을 무시하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-294">최종 사용자의 게시 기능 제한</span><span class="sxs-lookup"><span data-stu-id="cb23b-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-295">관리자 (최종 사용자가 아님)만 패키지를 게시 하 고 연결 그룹을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-296">연결 그룹에 대 한 자세한 내용은 <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> 관리자만 연결 그룹을 사용 하도록 허용 하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="cb23b-297">패키지에 대 한 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-298">메서드</span><span class="sxs-lookup"><span data-stu-id="cb23b-298">Method</span></span></th>
<th align="left"><span data-ttu-id="cb23b-299">추가 정보 링크</span><span class="sxs-lookup"><span data-stu-id="cb23b-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-300">관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="cb23b-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="cb23b-301">관리 콘솔을 사용하여 패키지를 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb23b-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="cb23b-303">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-304">타사 전자 소프트웨어 전달 시스템</span><span class="sxs-lookup"><span data-stu-id="cb23b-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="cb23b-305">ESD를 사용하여 관리자만 패키지를 게시할 수 있도록 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-306">특정 사용자에 대 한 연결 그룹을 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-307">관리자는 다음 cmdlet을 사용 하 여 optional <strong> – UserSID 매개 변수를 사용 하 여 특정 사용자에 대 한 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="cb23b-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="cb23b-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="cb23b-309">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="cb23b-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="cb23b-310">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-311">연결 그룹의 하나의 가상 디렉터리에 동일한 패키지 경로 병합</span><span class="sxs-lookup"><span data-stu-id="cb23b-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-312">연결 그룹에 있는 둘 이상의 패키지에 동일한 디렉터리 경로가 포함 된 경우 경로가 연결 그룹 가상 환경 내의 단일 가상 디렉터리로 병합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="cb23b-313">이러한 경로 병합을 통해 한 패키지의 응용 프로그램이 다른 패키지의 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="cb23b-314">연결 그룹 가상 환경 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="cb23b-315">관리자가 특정 사용자를 위해 패키지를 게시 하 고 게시 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="cb23b-316">관리자는 다음 cmdlet을 사용 하 여 특정 사용자에 대 한 패키지를 게시 하거나 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="cb23b-317">Cmdlet을 사용 하려면 **– UserSID** 매개 변수를 입력 하 고 그 뒤에 사용자의 SID (보안 식별자)가와 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="cb23b-318">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-318">For more information, see:</span></span>

-   [<span data-ttu-id="cb23b-319">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="cb23b-320">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-321">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb23b-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="cb23b-322">예</span><span class="sxs-lookup"><span data-stu-id="cb23b-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-323">게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb23b-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-324">게시-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="cb23b-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-325">게시 취소-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cb23b-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-326">게시 취소-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="cb23b-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="cb23b-327">패키지 게시 및 게시 취소를 위해 관리자만 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="cb23b-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="cb23b-328">다음 방법 중 하나를 사용 하 여 패키지를 게시 하거나 게시가 취소 하는 경우에만 관리자 (최종 사용자가 아님)만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-329">메서드</span><span class="sxs-lookup"><span data-stu-id="cb23b-329">Method</span></span></th>
<th align="left"><span data-ttu-id="cb23b-330">추가 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-331">그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="cb23b-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-332">다음 그룹 정책 개체 노드로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="cb23b-333">컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시 </strong> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="cb23b-334"><strong>관리자 권한으로 게시 </strong> 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb23b-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="cb23b-336">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="cb23b-337">RunVirtual registry 키는 사용자에 게 게시 되는 패키지를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="cb23b-338">App-v 5.0 SP3은 사용자 게시 된 패키지에 있는 가상화 된 응용 프로그램에서 **Runvirtual** 레지스트리 키를 사용 하는 데 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="cb23b-339">**Runvirtual** registry 키를 사용 하 여 가상 환경에서 로컬에 설치 된 응용 프로그램을 실행할 수 있으며, app-v를 통해 가상화 된 응용 프로그램과 함께</span><span class="sxs-lookup"><span data-stu-id="cb23b-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="cb23b-340">이전에는 App-v 패키지의 가상화 된 응용 프로그램을 전역으로 게시 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="cb23b-341">가상 응용 프로그램을 사용 하 여 가상 환경에서 **로컬에 설치** 된 응용 프로그램을 실행 하는 다른 방법에 대 한 자세한 내용은 가상 [응용 프로그램을 사용 하 여 로컬에 설치 된 응용 프로그램 실행](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="cb23b-342">새 PowerShell cmdlet 및 업데이트 가능한 cmdlet 도움말</span><span class="sxs-lookup"><span data-stu-id="cb23b-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="cb23b-343">앱-V 5.0 SP3에는 새 PowerShell cmdlet 및 업데이트 가능한 cmdlet 도움말이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="cb23b-344">Cmdlet 모듈을 다운로드 하려면 [PowerShell cmdlet을 로드 하는 방법과 Cmdlet 도움말](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="cb23b-345">새 앱-V 5.0 SP3 Server PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb23b-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="cb23b-346">연결 그룹을 관리 하는 데 도움이 되도록 App-v 서버에 대 한 새 Windows PowerShell cmdlet이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-347">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb23b-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="cb23b-348">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-349">추가-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="cb23b-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-350">연결 그룹의 끝에 패키지를 추가 하 여 패키지를 선택 및/또는 연결 그룹 내에 있는 버전이 없는 상태로 구성할 수 있도록 합니다&#39;s 패키지 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-351">Set-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="cb23b-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-352">연결 그룹 패키지에 대 한 세부 정보 (예: 선택 사항)를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-353">제거-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="cb23b-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-354">연결 그룹에서 패키지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="cb23b-355">PowerShell cmdlet에 대 한 도움말 보기</span><span class="sxs-lookup"><span data-stu-id="cb23b-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="cb23b-356">Cmdlet 도움말은 다음 형식으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-357">형식</span><span class="sxs-lookup"><span data-stu-id="cb23b-357">Format</span></span></th>
<th align="left"><span data-ttu-id="cb23b-358">설명</span><span class="sxs-lookup"><span data-stu-id="cb23b-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-359">다운로드 가능한 모듈</span><span class="sxs-lookup"><span data-stu-id="cb23b-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-360">Cmdlet 모듈을 다운로드 한 후 최신 도움말을 확인 하려면 다음을 수행 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="cb23b-361">Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="cb23b-362">다음 명령 중 하나를 입력 하 여 원하는 모듈에 대 한 cmdlet을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-363">App-v 구성 요소</span><span class="sxs-lookup"><span data-stu-id="cb23b-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="cb23b-364">명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-365">App-v Server</span><span class="sxs-lookup"><span data-stu-id="cb23b-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-366">업데이트-도움말-모듈 AppvServer</span><span class="sxs-lookup"><span data-stu-id="cb23b-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-367">App-V 시퀀서</span><span class="sxs-lookup"><span data-stu-id="cb23b-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-368">업데이트-도움말-모듈 AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="cb23b-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-369">App-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="cb23b-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-370">업데이트-도움말-모듈 AppvClient</span><span class="sxs-lookup"><span data-stu-id="cb23b-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-371">TechNet에서 웹 페이지로</span><span class="sxs-lookup"><span data-stu-id="cb23b-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-372"><a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Windows PowerShell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화의 앱-V 노드를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="cb23b-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="cb23b-373">자세한 내용은 [PowerShell cmdlet을 로드 하는 방법과 Cmdlet 도움말](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="cb23b-374">PVAD (주 가상 응용 프로그램 디렉터리)가 숨겨져 있지만 켤 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="cb23b-375">App-v 5.0 SP3에서 기본 virtual application directory (PVAD)가 숨겨져 있지만, 다시 켜고 다음 방법 중 하나를 사용 하 여 표시 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-376">메서드</span><span class="sxs-lookup"><span data-stu-id="cb23b-376">Method</span></span></th>
<th align="left"><span data-ttu-id="cb23b-377">단계</span><span class="sxs-lookup"><span data-stu-id="cb23b-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cb23b-378">명령줄 매개 변수 사용</span><span class="sxs-lookup"><span data-stu-id="cb23b-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="cb23b-379"><strong>– EnablePVADControl </strong> 매개 변수를Sequencer.exe에 <strong> 전달 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cb23b-380">레지스트리 하위 키 만들기</span><span class="sxs-lookup"><span data-stu-id="cb23b-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="cb23b-381">레지스트리 편집기에서 다음으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="cb23b-382">참고</span><span class="sxs-lookup"><span data-stu-id="cb23b-382">Note</span></span></strong><br/><p><span data-ttu-id="cb23b-383"><code>Compatibility</code>하위 키가 없으면 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="cb23b-384">EnablePVADControl 이라는 DWORD 값을 <strong> 만들고 </strong> 값을 1로 설정 <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="cb23b-385">값 <strong> </strong> 이 0 이면 PVAD가 숨겨져 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="cb23b-386">**PVAD에 대 한 자세한 정보:** 시퀀서를 사용 하 여 패키지를 만드는 경우 패키지의 설치 경로를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="cb23b-387">이전 버전의 App-v에서는 응용 프로그램의 PVAD (주 가상 응용 프로그램 디렉터리)를 경로로 지정 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="cb23b-388">PVAD는 앱을 사용 하지 않는 경우 일반적으로 로컬 컴퓨터에 응용 프로그램을 설치 하는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="cb23b-389">예를 들어 컴퓨터에 Office를 설치 하는 경우 일반적으로 PVAD는 C:\\program files Files\\Microsoft Office\\.입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="cb23b-390">App-v 게시 메타 데이터를 보려면 ClientVersion이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="cb23b-391">App-v 5.0 SP3에서는 메타 데이터에 대해 App-v 게시 서버를 쿼리할 때 주소에 다음 값을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cb23b-392">값</span><span class="sxs-lookup"><span data-stu-id="cb23b-392">Value</span></span></th>
<th align="left"><span data-ttu-id="cb23b-393">추가적인 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cb23b-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="cb23b-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-395"><strong>쿼리에서 clientversion 매개 변수를 생략 하면 </strong> 메타 데이터가 새 APP-V 5.0 SP3 기능을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cb23b-396">ClientOS</span><span class="sxs-lookup"><span data-stu-id="cb23b-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cb23b-397">패키지를 시퀀싱 할 때 특정 클라이언트 운영 체제를 선택 하는 경우에만이 값을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="cb23b-398">기본값 (모든 운영 체제)을 선택 하는 경우 쿼리에이 값을 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="cb23b-399"><strong>쿼리에서 clientos 매개 변수를 생략 하면 </strong> 모든 운영 체제를 지원 하도록 시퀀싱 된 패키지만 메타 데이터에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="cb23b-400">이 쿼리의 구문 및 예제는 [App-v Server 게시 메타 데이터 보기](viewing-app-v-server-publishing-metadata.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="cb23b-401">App-v 이벤트 로그가 통합 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="cb23b-402">이전에 \*\*응용 프로그램 및 서비스 로그/microsoft/appv/app-v &lt; 구성 요소 &gt; \*\*에 있는 다음 이벤트 로그가 **응용 프로그램 및 서비스 로그/Microsoft/appv/servicelog**로 이동 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="cb23b-403">로그를 보려면 **View** &gt; 이벤트 뷰어 응용 프로그램에서 **분석 표시 및 디버그 로그** 보기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="cb23b-404">클라이언트-카탈로그 클라이언트-통합 클라이언트-PackageConfig 클라이언트-스크립팅 클라이언트-서비스 클라이언트-Vemgr 클라이언트-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary 하위 시스템-ActiveX 하위 시스템-AppPath 하위 시스템-Com 하위 시스템-fta</span><span class="sxs-lookup"><span data-stu-id="cb23b-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="cb23b-405">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb23b-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="cb23b-406">앱-V는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="cb23b-407">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="cb23b-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="cb23b-408">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb23b-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="cb23b-409">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cb23b-409">Related topics</span></span>


[<span data-ttu-id="cb23b-410">App-V 5.0 SP3 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="cb23b-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)









