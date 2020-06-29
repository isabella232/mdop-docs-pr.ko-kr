---
title: App-V 5.1 정보
description: App-V 5.1 정보
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814948"
---
# <span data-ttu-id="f254b-103">App-V 5.1 정보</span><span class="sxs-lookup"><span data-stu-id="f254b-103">About App-V 5.1</span></span>


<span data-ttu-id="f254b-104">다음 섹션을 사용 하 여 Application Virtualization (App-v) 5.1에 적용 되는 중요 한 변경 사항에 대 한 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-104">Use the following sections to review information about significant changes that apply to Application Virtualization (App-V) 5.1:</span></span>

[<span data-ttu-id="f254b-105">앱-V 5.1 소프트웨어 필수 구성 요소 및 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="f254b-105">App-V 5.1 software prerequisites and supported configurations</span></span>](#bkmk-51-prereq-configs)

[<span data-ttu-id="f254b-106">App-V 5.1으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="f254b-106">Migrating to App-V 5.1</span></span>](#bkmk-migrate-to-51)

[<span data-ttu-id="f254b-107">앱-V 5.1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f254b-107">What’s New in App-V 5.1</span></span>](#bkmk-whatsnew)

[<span data-ttu-id="f254b-108">Windows 10 용 app-v 지원</span><span class="sxs-lookup"><span data-stu-id="f254b-108">App-V support for Windows 10</span></span>](#bkmk-win10support)

[<span data-ttu-id="f254b-109">앱-V 관리 콘솔 변경</span><span class="sxs-lookup"><span data-stu-id="f254b-109">App-V Management Console Changes</span></span>](#bkmk-mgmtconsole)

[<span data-ttu-id="f254b-110">Sequencer 개선 사항</span><span class="sxs-lookup"><span data-stu-id="f254b-110">Sequencer Improvements</span></span>](#bkmk-seqimprove)

[<span data-ttu-id="f254b-111">패키지 변환기 개선</span><span class="sxs-lookup"><span data-stu-id="f254b-111">Improvements to Package Converter</span></span>](#bkmk-pkgconvimprove)

[<span data-ttu-id="f254b-112">단일 이벤트 트리거에서 여러 스크립트에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="f254b-112">Support for multiple scripts on a single event trigger</span></span>](#bkmk-supmultscripts)

[<span data-ttu-id="f254b-113">설치 폴더에 대 한 하드 코드 경로가 가상 파일 시스템 루트에 리디렉션 됨</span><span class="sxs-lookup"><span data-stu-id="f254b-113">Hardcoded path to installation folder is redirected to virtual file system root</span></span>](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a><span data-ttu-id="f254b-114">앱-V 5.1 소프트웨어 필수 구성 요소 및 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="f254b-114">App-V 5.1 software prerequisites and supported configurations</span></span>


<span data-ttu-id="f254b-115">앱-V 5.1 소프트웨어 필수 구성 요소 및 지원 되는 구성에 대 한 다음 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-115">See the following links for the App-V 5.1 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-116">전제 조건과 지원 되는 구성에 대 한 링크</span><span class="sxs-lookup"><span data-stu-id="f254b-116">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="f254b-117">설명</span><span class="sxs-lookup"><span data-stu-id="f254b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)"><span data-ttu-id="f254b-118">App-V 5.1 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="f254b-118">App-V 5.1 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f254b-119">앱-V 5.1 설치를 시작 하기 전에 설치 해야 하는 필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="f254b-119">Prerequisite software that you must install before starting the App-V 5.1 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="f254b-120">App-V 5.1 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="f254b-120">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f254b-121">App-v Server, Sequencer 및 클라이언트 구성 요소에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f254b-121">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f254b-122">**Configuration Manager For App-V 사용에 대 한 지원:** 앱-V 5.1는 System Center 2012 R2 Configuration Manager SP1을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-122">**Support for using Configuration Manager with App-V:** App-V 5.1 supports System Center 2012 R2 Configuration Manager SP1.</span></span> <span data-ttu-id="f254b-123">앱-V 환경을 구성 관리자 및 구성 관리자와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager와 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-123">See [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) for information about integrating your App-V environment with Configuration Manager and Configuration Manager.</span></span>

## <a href="" id="bkmk-migrate-to-51"></a><span data-ttu-id="f254b-124">App-V 5.1으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="f254b-124">Migrating to App-V 5.1</span></span>


<span data-ttu-id="f254b-125">다음 정보를 사용 하 여 이전 버전의 App-v 5.1으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-125">Use the following information to upgrade to App-V 5.1 from earlier versions.</span></span> <span data-ttu-id="f254b-126">자세한 내용은 [이전 버전에서 앱-V 5.1으로 마이그레이션을](migrating-to-app-v-51-from-a-previous-version.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-126">See [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md) for more information.</span></span>

### <span data-ttu-id="f254b-127">업그레이드를 시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="f254b-127">Before you start the upgrade</span></span>

<span data-ttu-id="f254b-128">업그레이드를 시작 하기 전에 다음 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-128">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-129">업그레이드 하기 전에 검토할 항목</span><span class="sxs-lookup"><span data-stu-id="f254b-129">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="f254b-130">설명</span><span class="sxs-lookup"><span data-stu-id="f254b-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-131">업그레이드할 구성 요소 (순서에 관계 없음)</span><span class="sxs-lookup"><span data-stu-id="f254b-131">Components to upgrade, in any order</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f254b-132">App-v Server</span><span class="sxs-lookup"><span data-stu-id="f254b-132">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="f254b-133">않았음이</span><span class="sxs-lookup"><span data-stu-id="f254b-133">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="f254b-134">앱-V 클라이언트 또는 App-v (원격 데스크톱 서비스) 클라이언트</span><span class="sxs-lookup"><span data-stu-id="f254b-134">App-V Client or App-V Remote Desktop Services (RDS) Client</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="f254b-135">참고</span><span class="sxs-lookup"><span data-stu-id="f254b-135">Note</span></span></strong><br/><p><span data-ttu-id="f254b-136">App-v 5.0 SP2 이전에는 App-v 클라이언트 설치와 함께 클라이언트 관리 UI (사용자 인터페이스)가 제공 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-136">Prior to App-V 5.0 SP2, the Client Management User Interface (UI) was provided with the App-V Client installation.</span></span> <span data-ttu-id="f254b-137">App-v 5.0 SP2 설치 (이상)의 경우 <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> 응용 프로그램 가상화 5.0 클라이언트 UI 응용 프로그램에서 다운로드 하 여 클라이언트 관리 UI를 사용할 수 있습니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="f254b-137">For App-V 5.0 SP2 installations (or later), you can use the Client Management UI by downloading from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f254b-138">앱-V 4. x에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f254b-138">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-139">먼저 App-v 5.0으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-139">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="f254b-140">앱-V 4. x에서 App-v 5.1로 직접 업그레이드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-140">You cannot upgrade directly from App-V 4.x to App-V 5.1.</span></span> <span data-ttu-id="f254b-141">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-141">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="f254b-142">"App-v 4.6 및 App-v 5.0"의 차이점에 <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> 대 한 자세한 내용은 ' v e y e 5.0 "</span><span class="sxs-lookup"><span data-stu-id="f254b-142">“Differences between App-V 4.6 and App-V 5.0” in <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">About App-V 5.0</span></span></a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="f254b-143">App-V의 이전 버전에서 마이그레이션 계획</span><span class="sxs-lookup"><span data-stu-id="f254b-143">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-144">앱-V 5.0 이상에서 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f254b-144">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-145">다음 버전 중 하나에서 앱-V 5.1으로 직접 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-145">You can upgrade to App-V 5.1 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="f254b-146">App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f254b-146">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="f254b-147">App-v 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f254b-147">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="f254b-148">App-v 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f254b-148">App-V 5.0 SP2</span></span></p></li>
<li><p><span data-ttu-id="f254b-149">App-v 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="f254b-149">App-V 5.0 SP3</span></span></p></li>
</ul>
<p><span data-ttu-id="f254b-150">App-v 5.1으로 업그레이드 하려면이 항목의 나머지 섹션에 나와 있는 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-150">To upgrade to App-V 5.1, follow the steps in the remaining sections of this topic.</span></span></p>
<p><span data-ttu-id="f254b-151">패키지 및 연결 그룹은 현재 사용 중인 앱-V 5.1에서 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-151">Packages and connection groups will continue to work with App-V 5.1 as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="f254b-152">앱-V 인프라를 업그레이드 하는 단계</span><span class="sxs-lookup"><span data-stu-id="f254b-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="f254b-153">앱-v 인프라의 각 구성 요소를 App-v 5.1으로 업그레이드 하려면 다음 단계를 완료 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.1.</span></span> <span data-ttu-id="f254b-154">다음 주문은 제안 사항입니다. 구성 요소를 순서에 관계 없이 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-154">The following order is only a suggestion; you may upgrade components in any order.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-155">단계</span><span class="sxs-lookup"><span data-stu-id="f254b-155">Step</span></span></th>
<th align="left"><span data-ttu-id="f254b-156">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="f254b-156">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-157">1 단계: App-v Server를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-157">Step 1: Upgrade the App-V Server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f254b-158">참고</span><span class="sxs-lookup"><span data-stu-id="f254b-158">Note</span></span></strong><br/><p><span data-ttu-id="f254b-159">App-v 서버를 사용 하지 않는 경우에는이 단계를 건너뛰고 다음 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-159">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="f254b-160">다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="f254b-161">관리 데이터베이스 및/또는 보고 데이터베이스를 업그레이드 하는 데 사용 하는 방법에 따라 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-161">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-162">데이터베이스 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="f254b-162">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="f254b-163">단계</span><span class="sxs-lookup"><span data-stu-id="f254b-163">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-164">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f254b-164">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-165">이 단계를 건너뛰고 2 단계 ("App-v Server를 업그레이드 하는 경우 ...")로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-165">Skip this step and go to step 2, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f254b-166">SQL 스크립트</span><span class="sxs-lookup"><span data-stu-id="f254b-166">SQL scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-167"><a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법의 단계를 따릅니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="f254b-167">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<li><p><span data-ttu-id="f254b-168">App-v 5.0 SP1 핫픽스 패키지 3 이상에서 App-v 서버를 업그레이드 하는 경우 <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> app-v 5.0 SP3 서버 설치 후 레지스트리 키 확인 섹션의 단계를 완료 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-168">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="f254b-169"><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">App-v 5.1 서버를 배포 하는 방법의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-169">Follow the steps in <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f254b-170">2 단계: App-v Sequencer를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-170">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-171"><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">Sequencer를 설치 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f254b-171">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-172">3 단계: App-v 클라이언트 또는 App-v RDS 클라이언트를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-172">Step 3: Upgrade the App-V Client or App-V RDS Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-173"><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">App-v 클라이언트를 배포 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f254b-173">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f254b-174">이전 버전의 App-v를 사용 하 여 만든 패키지 변환</span><span class="sxs-lookup"><span data-stu-id="f254b-174">Converting packages created using a prior version of App-V</span></span>

<span data-ttu-id="f254b-175">패키지 변환기 유틸리티를 사용 하 여 앱-V 5.0 이전 버전의 app-v를 사용 하 여 만든 가상 응용 프로그램 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-175">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="f254b-176">패키지 변환기는 PowerShell을 사용 하 여 패키지를 변환 하며 변환이 필요한 패키지가 여러 개 있는 경우 프로세스를 자동화 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-176">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

**<span data-ttu-id="f254b-177">참고</span><span class="sxs-lookup"><span data-stu-id="f254b-177">Note</span></span>**  
<span data-ttu-id="f254b-178">App-v 5.1 패키지는 앱-v 5.0 패키지와 정확히 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-178">App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="f254b-179">버전 간에는 패키지 형식이 변경 되지 않으므로 App-v 5.0 패키지를 App-v 5.1 패키지로 변환할 필요가 없습니다..</span><span class="sxs-lookup"><span data-stu-id="f254b-179">There has been no change in the package format between the versions and so there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>



## <a href="" id="bkmk-whatsnew"></a><span data-ttu-id="f254b-180">앱-V 5.1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f254b-180">What’s New in App-V 5.1</span></span>


<span data-ttu-id="f254b-181">이 섹션은 app-v에 이미 익숙한 사용자를 위한 것 이며 App-v 5.1에서 변경 된 내용을 알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-181">These sections are for users who are already familiar with App-V and want to know what has changed in App-V 5.1.</span></span> <span data-ttu-id="f254b-182">App-v에 익숙하지 않은 경우 [에는 앱-v 5.1에 대 한 읽기 계획](planning-for-app-v-51.md)부터 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-182">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.1](planning-for-app-v-51.md).</span></span>

### <a href="" id="bkmk-win10support"></a><span data-ttu-id="f254b-183">Windows 10 용 app-v 지원</span><span class="sxs-lookup"><span data-stu-id="f254b-183">App-V support for Windows 10</span></span>

<span data-ttu-id="f254b-184">다음 표에는 App-v에 대 한 Windows 10 지원이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-184">The following table lists the Windows 10 support for App-V.</span></span> <span data-ttu-id="f254b-185">앱-V 5.1 이전 버전의 App-v에서는 Windows 10이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-185">Windows 10 is not supported in versions of App-V prior to App-V 5.1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-186">구성 요소</span><span class="sxs-lookup"><span data-stu-id="f254b-186">Component</span></span></th>
<th align="left"><span data-ttu-id="f254b-187">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f254b-187">App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="f254b-188">App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f254b-188">App-V 5.0</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-189">App-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="f254b-189">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-190">예</span><span class="sxs-lookup"><span data-stu-id="f254b-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-191">아니오</span><span class="sxs-lookup"><span data-stu-id="f254b-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f254b-192">App-v RDS 클라이언트</span><span class="sxs-lookup"><span data-stu-id="f254b-192">App-V RDS Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-193">예</span><span class="sxs-lookup"><span data-stu-id="f254b-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-194">아니오</span><span class="sxs-lookup"><span data-stu-id="f254b-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-195">App-V 시퀀서</span><span class="sxs-lookup"><span data-stu-id="f254b-195">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-196">예</span><span class="sxs-lookup"><span data-stu-id="f254b-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-197">아니오</span><span class="sxs-lookup"><span data-stu-id="f254b-197">No</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a><span data-ttu-id="f254b-198">앱-V 관리 콘솔 변경</span><span class="sxs-lookup"><span data-stu-id="f254b-198">App-V Management Console Changes</span></span>

<span data-ttu-id="f254b-199">이 섹션에서는 App-v 관리 콘솔의 현재 기능과 이전 기능을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-199">This section compares the App-V Management Console’s current and previous functionality.</span></span>

### <span data-ttu-id="f254b-200">Silverlight는 더 이상 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-200">Silverlight is no longer required</span></span>

<span data-ttu-id="f254b-201">관리 콘솔 UI에 더 이상 Silverlight가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-201">The Management Console UI no longer requires Silverlight.</span></span> <span data-ttu-id="f254b-202">5.1 관리 콘솔은 HTML5 및 Javascript에 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-202">The 5.1 Management Console is built on HTML5 and Javascript.</span></span>

### <span data-ttu-id="f254b-203">알림 및 메시지가 대화 상자에 개별적으로 표시 됨</span><span class="sxs-lookup"><span data-stu-id="f254b-203">Notifications and messages are displayed individually in a dialog box</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-204">앱의 새로운 기능-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f254b-204">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="f254b-205">앱-V 5.1 이전</span><span class="sxs-lookup"><span data-stu-id="f254b-205">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f254b-206">메시지 표시기 수:</span><span class="sxs-lookup"><span data-stu-id="f254b-206">Number of messages indicator:</span></span></strong></p>
<p><span data-ttu-id="f254b-207">앱-V 관리 콘솔의 제목 표시줄에서 플래그 아이콘 옆에 번호가 표시 되어 읽으려는 메시지 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-207">On the title bar of the App-V Management Console, a number is now displayed next to a flag icon to indicate the number of messages that are waiting to be read.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-208">메시지 또는 오류를 한 번에 하나만 볼 수 있으며 메시지 수를 확인할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-208">You could see only one message or error at a time, and you were unable to determine how many messages there were.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f254b-209">메시지 모양:</span><span class="sxs-lookup"><span data-stu-id="f254b-209">Message appearance:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="f254b-210">사용자 입력이 필요한 메시지가 표시 되는 현재 페이지의 맨 위에 표시 되는 별도의 대화 상자에 나타나고 해당 메시지를 해제 하기 전에 응답이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-210">Messages that require user input appear in a separate dialog box that displays on top of the current page that you were viewing, and require a response before you can dismiss them.</span></span></p></li>
<li><p><span data-ttu-id="f254b-211">메시지와 오류는 목록에 표시 되 고, 다른 하나 아래에는 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-211">Messages and errors appear in a list, with one beneath the other.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="f254b-212">한 번에 하나의 메시지나 오류만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-212">You could see only one message or error at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f254b-213">메시지 해제:</span><span class="sxs-lookup"><span data-stu-id="f254b-213">Dismissing messages:</span></span></strong></p>
<p><span data-ttu-id="f254b-214"><strong>모두 해제 링크를 사용 하 여 한 번에 </strong> 모든 메시지 및 오류를 해제 하거나 한 번에 하나씩 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-214">Use the <strong>Dismiss All</strong> link to dismiss all messages and errors at one time, or dismiss them one at a time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-215">메시지 및 오류를 한 번에 하나씩만 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-215">You could dismiss messages and errors only one at a time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f254b-216">이제 콘솔 페이지는 별도의 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-216">Console pages are now separate URLs</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-217">앱의 새로운 기능-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f254b-217">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="f254b-218">앱-V 5.1 이전</span><span class="sxs-lookup"><span data-stu-id="f254b-218">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-219">콘솔의 각 페이지에는 다른 URL이 있으므로, 앞으로 빠르게 액세스할 수 있도록 특정 페이지에 책갈피를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-219">Each page in the console has a different URL, which enables you to bookmark specific pages for quick access in the future.</span></span></p>
<p><span data-ttu-id="f254b-220">일부 Url에 표시 되는 번호는 특정 패키지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-220">The number that appears in some URLs indicates the specific package.</span></span> <span data-ttu-id="f254b-221">이러한 번호는 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-221">These numbers are unique.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-222">모든 콘솔 페이지에는 같은 URL을 통해 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-222">All console pages are accessed through the same URL.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f254b-223">새로 만들기, 별도의 연결 그룹 페이지 및 메뉴 옵션</span><span class="sxs-lookup"><span data-stu-id="f254b-223">New, separate CONNECTION GROUPS page and menu option</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-224">앱의 새로운 기능-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f254b-224">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="f254b-225">앱-V 5.1 이전</span><span class="sxs-lookup"><span data-stu-id="f254b-225">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-226">연결 그룹 페이지는 이제 패키지 페이지와 동일한 수준에 있는 주 메뉴의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-226">The CONNECTION GROUPS page is now part of the main menu, at the same level as the PACKAGES page.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-227">연결 그룹 페이지를 열려면 패키지 페이지를 탐색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-227">To open the CONNECTION GROUPS page, you navigate through the PACKAGES page.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f254b-228">패키지에 대 한 메뉴 옵션 변경 됨</span><span class="sxs-lookup"><span data-stu-id="f254b-228">Menu options for packages have changed</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f254b-229">앱의 새로운 기능-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f254b-229">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="f254b-230">앱-V 5.1 이전</span><span class="sxs-lookup"><span data-stu-id="f254b-230">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f254b-231">다음 옵션은 이제 패키지 페이지 아래쪽에 표시 되는 단추입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-231">The following options are now buttons that appear at the bottom of the PACKAGES page:</span></span></p>
<ul>
<li><p><span data-ttu-id="f254b-232">추가 또는 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f254b-232">Add or Upgrade</span></span></p></li>
<li><p><span data-ttu-id="f254b-233">게시</span><span class="sxs-lookup"><span data-stu-id="f254b-233">Publish</span></span></p></li>
<li><p><span data-ttu-id="f254b-234">문서만</span><span class="sxs-lookup"><span data-stu-id="f254b-234">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="f254b-235">삭제</span><span class="sxs-lookup"><span data-stu-id="f254b-235">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="f254b-236">드롭다운 상황에 맞는 메뉴를 열려면 패키지를 마우스 오른쪽 단추로 클릭 하면 다음 옵션이 계속 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-236">The following options will still appear when you right-click a package to open the drop-down context menu:</span></span></p>
<ul>
<li><p><span data-ttu-id="f254b-237">게시</span><span class="sxs-lookup"><span data-stu-id="f254b-237">Publish</span></span></p></li>
<li><p><span data-ttu-id="f254b-238">문서만</span><span class="sxs-lookup"><span data-stu-id="f254b-238">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="f254b-239">광고 액세스 편집</span><span class="sxs-lookup"><span data-stu-id="f254b-239">Edit AD Access</span></span></p></li>
<li><p><span data-ttu-id="f254b-240">배포 구성 편집</span><span class="sxs-lookup"><span data-stu-id="f254b-240">Edit Deployment Config</span></span></p></li>
<li><p><span data-ttu-id="f254b-241">배포 구성 전송</span><span class="sxs-lookup"><span data-stu-id="f254b-241">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="f254b-242">다음에서 액세스 및 구성 전송 ...</span><span class="sxs-lookup"><span data-stu-id="f254b-242">Transfer access and configuration from…</span></span></p></li>
<li><p><span data-ttu-id="f254b-243">삭제</span><span class="sxs-lookup"><span data-stu-id="f254b-243">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="f254b-244"><strong>삭제 </strong> 를 클릭 하 여 패키지를 제거 하면 대화 상자가 열리고 패키지를 삭제할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-244">When you click <strong>Delete</strong> to remove a package, a dialog box opens and asks you to confirm that you want to delete the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f254b-245"><strong>추가 또는 업그레이드 </strong> 옵션은 패키지 페이지 오른쪽 위에 있는 단추입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-245">The <strong>Add or Upgrade</strong> option was a button at the top right of the PACKAGES page.</span></span></p>
<p><span data-ttu-id="f254b-246"><strong>게시 </strong> , 게시 <strong> 취소 </strong> 및 <strong> 삭제 옵션은 </strong> 패키지 목록에서 패키지 이름을 마우스 오른쪽 단추로 클릭 한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-246">The <strong>Publish</strong>, <strong>Unpublish</strong>, and <strong>Delete</strong> options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f254b-247">다음 패키지 작업은 이제 각 패키지에 대 한 패키지 세부 정보 페이지의 단추입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-247">The following package operations are now buttons on the package details page for each package:</span></span></p>
<ul>
<li><p><span data-ttu-id="f254b-248">전송 (다음 옵션을 사용 하 여 드롭다운 메뉴):</span><span class="sxs-lookup"><span data-stu-id="f254b-248">Transfer (drop-down menu with the following options):</span></span></p>
<ul>
<li><p><span data-ttu-id="f254b-249">배포 구성 전송</span><span class="sxs-lookup"><span data-stu-id="f254b-249">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="f254b-250">다음에서 액세스 및 구성 전송 ...</span><span class="sxs-lookup"><span data-stu-id="f254b-250">Transfer access and configuration from…</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="f254b-251">편집 (연결 그룹 및 광고 액세스)</span><span class="sxs-lookup"><span data-stu-id="f254b-251">Edit (connection groups and AD Access)</span></span></p></li>
<li><p><span data-ttu-id="f254b-252">문서만</span><span class="sxs-lookup"><span data-stu-id="f254b-252">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="f254b-253">삭제</span><span class="sxs-lookup"><span data-stu-id="f254b-253">Delete</span></span></p></li>
<li><p><span data-ttu-id="f254b-254">기본 구성 편집</span><span class="sxs-lookup"><span data-stu-id="f254b-254">Edit Default Configuration</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="f254b-255">이러한 패키지 옵션은 패키지 목록에서 패키지 이름을 마우스 오른쪽 단추로 클릭 한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-255">These package options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f254b-256">왼쪽 창의 아이콘에는 새로운 색과 텍스트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-256">Icons in left pane have new colors and text</span></span>

<span data-ttu-id="f254b-257">왼쪽 창의 아이콘 색과 추가 된 텍스트가 변경 되어 다른 Microsoft 제품에서 아이콘을 일관 되 게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-257">The colors of the icons in the left pane have been changed, and text added, to make the icons consistent with other Microsoft products.</span></span>

### <span data-ttu-id="f254b-258">개요 페이지가 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-258">Overview page has been removed</span></span>

<span data-ttu-id="f254b-259">관리 콘솔의 왼쪽 창에서 개요 메뉴 옵션 및 관련 개요 페이지가 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-259">In the left pane of the Management Console, the OVERVIEW menu option and its associated OVERVIEW page have been removed.</span></span>

### <a href="" id="bkmk-seqimprove"></a><span data-ttu-id="f254b-260">Sequencer 개선 사항</span><span class="sxs-lookup"><span data-stu-id="f254b-260">Sequencer Improvements</span></span>

<span data-ttu-id="f254b-261">App-v 5.1 Sequencer의 패키지 편집기에 다음 개선 사항이 적용 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-261">The following improvements have been made to the package editor in the App-V 5.1 Sequencer.</span></span>

### <span data-ttu-id="f254b-262">매니페스트 파일 가져오기 및 내보내기</span><span class="sxs-lookup"><span data-stu-id="f254b-262">Import and export the manifest file</span></span>

<span data-ttu-id="f254b-263">AppxManifest.xml 파일을 가져오고 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-263">You can import and export the AppxManifest.xml file.</span></span> <span data-ttu-id="f254b-264">매니페스트 파일을 내보내려면 **고급** 탭을 선택 하 고 매니페스트 파일 상자에서 **내보내기를**클릭 합니다. 셸 확장 제거 또는 파일 형식 연결 편집과 같은 매니페스트 파일을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-264">To export the manifest file, select the **Advanced** tab and in the Manifest File box, click **Export...**. You can make changes to the manifest file, such as removing shell extensions or editing file type associations.</span></span>

<span data-ttu-id="f254b-265">변경 작업을 수행한 후 **가져오기** ...를 클릭 하 고 편집한 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-265">After you make your changes, click **Import...** and select the file you edited.</span></span> <span data-ttu-id="f254b-266">성공적으로 다시 가져오면 매니페스트 파일이 패키지 편집기 내에서 즉시 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-266">After you successfully import it back in, the manifest file is immediately updated within the package editor.</span></span>

**<span data-ttu-id="f254b-267">주의</span><span class="sxs-lookup"><span data-stu-id="f254b-267">Caution</span></span>**  
<span data-ttu-id="f254b-268">파일을 가져올 때 XML 스키마를 기준으로 변경 내용의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-268">When you import the file, your changes are validated against the XML schema.</span></span> <span data-ttu-id="f254b-269">파일이 유효 하지 않으면 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-269">If the file is not valid, you will receive an error.</span></span> <span data-ttu-id="f254b-270">XML 스키마에 대해 유효성을 검사 했지만 다른 이유 때문에 여전히 실행 되지 않을 수 있는 파일을 가져올 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-270">Be aware that it is possible to import a file that is validated against the XML schema, but that might still fail to run for other reasons.</span></span>



### <span data-ttu-id="f254b-271">Windows 10에서 운영 체제 목록 추가</span><span class="sxs-lookup"><span data-stu-id="f254b-271">Addition of Windows 10 to operating systems list</span></span>

<span data-ttu-id="f254b-272">배포 탭에서 패키지를 시퀀싱 할 수 있는 운영 체제 목록에 Windows 10 32 비트 및 Windows 10-64 비트가 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-272">In the Deployment tab, Windows 10 32-bit and Windows 10-64 bit have been added to the list of operating systems for which you can sequence a package.</span></span> <span data-ttu-id="f254b-273">**운영 체제**를 선택 하면 Windows 10이 시퀀싱 된 패키지에서 지원 되는 운영 체제에 자동으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-273">If you select **Any Operating System**, Windows 10 is automatically included among the operating systems that the sequenced package will support.</span></span>

### <span data-ttu-id="f254b-274">가상 레지스트리 편집기의 맨 아래에 표시 되는 현재 경로</span><span class="sxs-lookup"><span data-stu-id="f254b-274">Current path displays at bottom of virtual registry editor</span></span>

<span data-ttu-id="f254b-275">이제 가상 레지스트리 탭의 경로가 가상 레지스트리 편집기의 맨 아래에 표시 되며,이를 통해 현재 선택 된 키를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-275">In the Virtual Registry tab, the path now displays at the bottom of the virtual registry editor, which enables you to determine the currently selected key.</span></span> <span data-ttu-id="f254b-276">이전에는 레지스트리 트리를 스크롤하여 현재 선택 된 키를 찾아야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-276">Previously, you had to scroll through the registry tree to find the currently selected key.</span></span>

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a><span data-ttu-id="f254b-277">가상 레지스트리 편집기에 추가 된 "찾기 및 바꾸기" 대화 상자 및 바로 가기 키 조합</span><span class="sxs-lookup"><span data-stu-id="f254b-277">Combined “find and replace” dialog box and shortcut keys added in virtual registry editor</span></span>

<span data-ttu-id="f254b-278">가상 레지스트리 편집기에서 찾기 옵션 (Ctrl + F)에 대 한 바로 가기 키가 추가 되 고 "찾기" 및 "바꾸기" 작업을 결합 하 여 값과 데이터를 찾고 바꿀 수 있는 대화 상자가 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-278">In the virtual registry editor, shortcut keys have been added for the Find option (Ctrl+F), and a dialog box that combines the “find” and “replace” tasks has been added to enable you to find and replace values and data.</span></span> <span data-ttu-id="f254b-279">이 결합 된 대화 상자에 액세스 하려면 키를 선택 하 고 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-279">To access this combined dialog box, select a key and do one of the following:</span></span>

-   <span data-ttu-id="f254b-280">**Ctrl + H** 를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-280">Press **Ctrl+H**</span></span>

-   <span data-ttu-id="f254b-281">키를 마우스 오른쪽 단추로 클릭 하 고 **바꾸기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-281">Right-click a key and select **Replace**.</span></span>

-   <span data-ttu-id="f254b-282">**View** &gt; **가상 레지스트리** &gt; **바꾸기**보기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-282">Select **View** &gt; **Virtual Registry** &gt; **Replace**.</span></span>

<span data-ttu-id="f254b-283">이전에는 "바꾸기" 대화 상자가 없으므로 수동으로 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-283">Previously, the “Replace” dialog box did not exist, and you had to make changes manually.</span></span>

### <span data-ttu-id="f254b-284">레지스트리 키와 패키지 파일의 이름을 변경 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-284">Rename registry keys and package files successfully</span></span>

<span data-ttu-id="f254b-285">Sequencer 문제 없이 가상 레지스트리 키 및 파일의 이름을 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-285">You can rename virtual registry keys and files without experiencing Sequencer issues.</span></span> <span data-ttu-id="f254b-286">이전에는 키 이름을 바꾸려고 하면 Sequencer가 작동을 중지 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-286">Previously, the Sequencer stopped working if you tried to rename a key.</span></span>

### <span data-ttu-id="f254b-287">가상 레지스트리 키 가져오기 및 내보내기</span><span class="sxs-lookup"><span data-stu-id="f254b-287">Import and export virtual registry keys</span></span>

<span data-ttu-id="f254b-288">가상 레지스트리 키를 가져오고 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-288">You can import and export virtual registry keys.</span></span> <span data-ttu-id="f254b-289">키를 가져오려면 키를 가져올 노드를 마우스 오른쪽 단추로 클릭 하 고 가져올 키로 이동한 다음 **가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-289">To import a key, right-click the node under which to import the key, navigate to the key you want to import, and then click **Import**.</span></span> <span data-ttu-id="f254b-290">키를 내보내려면 키를 마우스 오른쪽 단추로 클릭 하 고 **내보내기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-290">To export a key, right-click the key and select **Export**.</span></span>

### <span data-ttu-id="f254b-291">가상 파일 시스템으로 디렉터리 가져오기</span><span class="sxs-lookup"><span data-stu-id="f254b-291">Import a directory into the virtual file system</span></span>

<span data-ttu-id="f254b-292">디렉터리를 VFS로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-292">You can import a directory into the VFS.</span></span> <span data-ttu-id="f254b-293">디렉터리를 가져오려면 **패키지 파일** 탭을 클릭 한 다음 **View** &gt; **가상 파일 시스템** &gt; **가져오기 디렉터리**보기를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-293">To import a directory, click the **Package Files** tab, and then click **View** &gt; **Virtual File System** &gt; **Import Directory**.</span></span> <span data-ttu-id="f254b-294">이미 VFS에 있는 파일을 포함 하는 디렉터리를 가져오려고 하면 가져오기에 실패 하 고 설명 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-294">If you try to import a directory that contains files that are already in the VFS, the import fails, and an explanatory message is displayed.</span></span> <span data-ttu-id="f254b-295">App-v 5.1 이전에는 디렉토리를 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-295">Prior to App-V 5.1, you could not import directories.</span></span>

### <span data-ttu-id="f254b-296">삭제할 필요 없이 VFS 파일을 가져오거나 내보내어 패키지에 다시 추가</span><span class="sxs-lookup"><span data-stu-id="f254b-296">Import or export a VFS file without having to delete and then add it back to the package</span></span>

<span data-ttu-id="f254b-297">파일을 삭제 한 다음 패키지에 다시 추가할 필요 없이 VFS에서 파일을 가져오거나 파일을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-297">You can import files to or export files from the VFS without having to delete the file and then add it back to the package.</span></span> <span data-ttu-id="f254b-298">예를 들어이 기능을 사용 하 여 변경 로그를 로컬 드라이브로 내보내고, 외부 편집기를 사용 하 여 파일을 편집 하 고, 파일을 VFS로 다시 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-298">For example, you might use this feature to export a change log to a local drive, edit the file using an external editor, and then re-import the file into the VFS.</span></span>

<span data-ttu-id="f254b-299">파일을 내보내려면 **패키지 파일** 탭을 선택 하 고 VFS에서 파일을 마우스 오른쪽 단추로 클릭 하 고 **내보내기를**클릭 한 다음 편집을 수행할 수 있는 내보내기 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-299">To export a file, select the **Package Files** tab, right-click the file in the VFS, click **Export**, and choose an export location from which you can make your edits.</span></span>

<span data-ttu-id="f254b-300">파일을 가져오려면 **패키지 파일** 탭을 선택 하 고 내보낸 파일을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-300">To import a file, select the **Package Files** tab and right-click the file that you had exported.</span></span> <span data-ttu-id="f254b-301">편집한 파일을 찾은 다음 **가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-301">Browse to the file that you edited, and then click **Import**.</span></span> <span data-ttu-id="f254b-302">가져온 파일은 기존 파일을 덮어쓰게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-302">The imported file will overwrite the existing file.</span></span>

<span data-ttu-id="f254b-303">파일을 가져온 후에는 **파일** 저장을 클릭 하 여 패키지를 저장 해야 합니다 &gt; **Save**.</span><span class="sxs-lookup"><span data-stu-id="f254b-303">After you import a file, you must save the package by clicking **File** &gt; **Save**.</span></span>

### <span data-ttu-id="f254b-304">패키지 파일 추가 메뉴가 이동 됨</span><span class="sxs-lookup"><span data-stu-id="f254b-304">Menu for adding a package file has moved</span></span>

<span data-ttu-id="f254b-305">패키지 파일을 추가 하기 위한 메뉴 옵션이 이동 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-305">The menu option for adding a package file has been moved.</span></span> <span data-ttu-id="f254b-306">추가 옵션을 찾으려면 **패키지 파일** 탭을 선택한 다음 **View** &gt; **가상 파일 시스템** &gt; **추가 파일**보기를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-306">To find the Add option, select the **Package Files** tab, then click **View** &gt; **Virtual File System** &gt; **Add File**.</span></span> <span data-ttu-id="f254b-307">이전에는 VFS 노드에서 폴더를 마우스 오른쪽 단추로 클릭 하 고 **파일 추가**를 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-307">Previously, you right-clicked a folder under the VFS node, and chose **Add File**.</span></span>

### <span data-ttu-id="f254b-308">가상 레지스트리 노드는 기본적으로 컴퓨터 및 사용자 하이브를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-308">Virtual registry node expands MACHINE and USER hives by default</span></span>

<span data-ttu-id="f254b-309">가상 레지스트리를 열면 컴퓨터 및 사용자 하이브는 최상위 수준 레지스트리 노드 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-309">When you open the virtual registry, the MACHINE and USER hives are shown below the top-level REGISTRY node.</span></span> <span data-ttu-id="f254b-310">이전에는 레지스트리 노드를 확장 하 여 아래에 있는 하이브를 표시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-310">Previously, you had to expand the REGISTRY node to show the hives beneath.</span></span>

### <span data-ttu-id="f254b-311">브라우저 도우미 개체 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f254b-311">Enable or disable Browser Helper Objects</span></span>

<span data-ttu-id="f254b-312">시퀀서 사용자 인터페이스의 고급 탭에서 새 확인란을 선택 하 고 브라우저 도우미 개체를 사용 하도록 설정 하 여 브라우저 도우미 개체를 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-312">You can enable or disable Browser Helper Objects by selecting a new check box, Enable Browser Helper Objects, on the Advanced tab of the Sequencer user interface.</span></span> <span data-ttu-id="f254b-313">브라우저 도우미 개체:</span><span class="sxs-lookup"><span data-stu-id="f254b-313">If Browser Helper Objects:</span></span>

-   <span data-ttu-id="f254b-314">패키지에 존재 하 고 사용 하도록 설정 되어 있으면 기본적으로 확인란이 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-314">Exist in the package and are enabled, the check box is selected by default.</span></span>

-   <span data-ttu-id="f254b-315">패키지에 존재 하며 사용 하지 않도록 설정 된 경우 확인란은 기본적으로 선택 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-315">Exist in the package and are disabled, the check box is clear by default.</span></span>

-   <span data-ttu-id="f254b-316">패키지에 하나 이상의 사용 가능 및 하나 이상의 사용 안 함이 있으면 기본적으로 확인란이 확정 되지 않음으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-316">Exist in the package, with one or more enabled and one or more disabled, the check box is set to indeterminate by default.</span></span>

-   <span data-ttu-id="f254b-317">패키지에 없는 경우 확인란을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-317">Do not exist in the package, the check box is disabled.</span></span>

### <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="f254b-318">패키지 변환기 개선</span><span class="sxs-lookup"><span data-stu-id="f254b-318">Improvements to Package Converter</span></span>

<span data-ttu-id="f254b-319">이제 패키지 변환기를 사용 하 여 스크립트를 포함 하는 App-v 4.6 패키지를 변환할 수 있으며, 이제 원본 osd 파일의 레지스트리 정보와 스크립트가 패키지 변환기 출력에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-319">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="f254b-320">예제를 비롯 한 자세한 내용은 [이전 버전에서 앱-V 5.1으로 마이그레이션을](migrating-to-app-v-51-from-a-previous-version.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-320">For more information including examples, see [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md).</span></span>

### <a href="" id="bkmk-supmultscripts"></a><span data-ttu-id="f254b-321">단일 이벤트 트리거에서 여러 스크립트에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="f254b-321">Support for multiple scripts on a single event trigger</span></span>

<span data-ttu-id="f254b-322">App-v 5.1는 app-v 4.6에서 App-v 5.0 이상으로 변환 하는 패키지를 포함 하 여 앱-V 패키지에 대 한 단일 이벤트 트리거에서 여러 스크립트의 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-322">App-V 5.1 supports the use of multiple scripts on a single event trigger for App-V packages, including packages that you are converting from App-V 4.6 to App-V 5.0 or later.</span></span> <span data-ttu-id="f254b-323">여러 스크립트를 사용할 수 있도록 앱-V 5.1는 App-v 클라이언트 설치의 일부로 설치 되는 ScriptRunner.exe 라는 스크립트 시작 관리자 응용 프로그램을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-323">To enable the use of multiple scripts, App-V 5.1 uses a script launcher application, named ScriptRunner.exe, which is installed as part of the App-V client installation.</span></span>

<span data-ttu-id="f254b-324">이벤트 트리거 목록과 스크립트를 실행할 수 있는 컨텍스트를 비롯 한 자세한 내용은 [app-v 5.1 동적 구성에 대 한](about-app-v-51-dynamic-configuration.md)스크립트 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-324">For more information, including a list of event triggers and the context under which scripts can be run, see the Scripts section in [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

### <a href="" id="bkmk-hardcodepath"></a><span data-ttu-id="f254b-325">설치 폴더에 대 한 하드 코드 경로가 가상 파일 시스템 루트에 리디렉션 됨</span><span class="sxs-lookup"><span data-stu-id="f254b-325">Hardcoded path to installation folder is redirected to virtual file system root</span></span>

<span data-ttu-id="f254b-326">앱-V 4.6에서 5.1로 패키지를 변환할 때 앱-V 5.1 패키지는 4.6 패키지를 만들 때 사용 하는 데 필요한 하드 코드 된 드라이브에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-326">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="f254b-327">드라이브 문자는 4.6 시퀀싱 시스템에서 설치 드라이브로 선택한 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-327">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="f254b-328">(기본 드라이브 문자는 Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="f254b-328">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="f254b-329">이전에는 4.6 루트 폴더가 인식 되지 않고 App-v 5.0 패키지에서 액세스할 수 없었습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-329">Previously, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="f254b-330">App-v 5.1 패키지는 전체 경로로 하드 코드 된 파일에 액세스 하거나 App-v 4.6 설치 루트 아래의 파일을 프로그래밍 방식으로 열거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-330">App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="f254b-331">**기술 정보:** App-v 5.1 패키지 변환기는 Filesystem 요소의 FilesystemMetadata.xml 파일에 App-v 4.6 설치 루트 폴더와 짧은 폴더 이름을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-331">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="f254b-332">App-v 5.1 클라이언트는 가상 프로세스를 만들 때 앱-V 4.6 설치 루트의 요청을 가상 파일 시스템 루트에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-332">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

## <span data-ttu-id="f254b-333">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f254b-333">How to Get MDOP Technologies</span></span>


<span data-ttu-id="f254b-334">앱-V는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-334">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="f254b-335">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f254b-335">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="f254b-336">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f254b-336">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="f254b-337">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f254b-337">Related topics</span></span>


[<span data-ttu-id="f254b-338">App-V 5.1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="f254b-338">Release Notes for App-V 5.1</span></span>](release-notes-for-app-v-51.md)









