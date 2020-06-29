---
title: App-V Client 배포 방법
description: App-V Client 배포 방법
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814124"
---
# <span data-ttu-id="2aae6-103">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="2aae6-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="2aae6-104">다음 절차를 사용 하 여 Microsoft App-v (Application Virtualization) 5.1 클라이언트 및 원격 데스크톱 서비스 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="2aae6-105">대상 컴퓨터의 운영 체제와 일치 하는 클라이언트 버전을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="2aae6-106">시작 하기 전에 수행할 작업</span><span class="sxs-lookup"><span data-stu-id="2aae6-106">What to do before you start</span></span>**

1. <span data-ttu-id="2aae6-107">소프트웨어 필수 구성 요소를 검토 하 고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="2aae6-108">설치 하는 App-v 버전에 해당 하는 필수 구성 요소 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="2aae6-109">App-V 5.1 정보</span><span class="sxs-lookup"><span data-stu-id="2aae6-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="2aae6-110">App-V 5.1 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="2aae6-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="2aae6-111">설치에 적용 가능한 경우 클라이언트 공존 및 지원 되지 않는 시나리오를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-112">공존할 때의 App-v 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="2aae6-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="2aae6-113">App-V 5.1 Sequencer 및 Client 배포 계획</span><span class="sxs-lookup"><span data-stu-id="2aae6-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-114">지원 되지 않거나 제한 된 설치 시나리오</span><span class="sxs-lookup"><span data-stu-id="2aae6-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-115"><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-v 5.1에서 지원 되는 구성의 클라이언트 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2aae6-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="2aae6-116">클라이언트 레지스트리, 로그 및 문제 해결 정보에 대 한 위치를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2aae6-117">클라이언트 레지스트리 정보</span><span class="sxs-lookup"><span data-stu-id="2aae6-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2aae6-118">기본적으로 App-v 5.1 클라이언트를 설치 하 고 나면 클라이언트 정보가 다음 레지스트리 키의 레지스트리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="2aae6-119">HKEY_LOCAL_MACHINE \ 소프트웨어 \ MICROSOFT \ APPV \ 클라이언트</span><span class="sxs-lookup"><span data-stu-id="2aae6-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="2aae6-120">가상화 된 패키지를 App-v 클라이언트를 실행 하는 컴퓨터에 배포 하는 경우 연결 된 패키지 데이터는 다음 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="2aae6-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="2aae6-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="2aae6-122">그러나 다음 레지스트리 키를 사용 하 여이 위치를 다시 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="2aae6-123">HKEY_LOCAL_MACHINE \ 소프트웨어 \ MICROSOFT \ 소프트웨어 \ MICROSOFT \ APPV \ 클라이언트 \ 스트리밍 \ 패키지 설치 루트</span><span class="sxs-lookup"><span data-stu-id="2aae6-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2aae6-124">클라이언트 로그 파일</span><span class="sxs-lookup"><span data-stu-id="2aae6-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2aae6-125">App-v 5.1 클라이언트와 연결 된 로그 파일 정보는 다음 로그에서 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="2aae6-126">이벤트 로그/응용 프로그램 및 서비스 로그/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="2aae6-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="2aae6-127">App-v 5.0 SP3에서는 일부 로그가 통합 되어 다음 위치로 이동 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="2aae6-128">이벤트 로그/응용 프로그램 및 서비스 로그/Microsoft/AppV/ServiceLog</span><span class="sxs-lookup"><span data-stu-id="2aae6-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="2aae6-129">이동한 로그 목록은 <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> 앱-V 5.0 SP3 정보를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="2aae6-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="2aae6-130">App-v 5.1 클라이언트를 실행 하는 컴퓨터에 현재 저장 된 패키지는 다음 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="2aae6-131">C:\ProgramData\App-V &amp; lt; 패키지 id &gt; &amp; lt; 버전 id&gt;</span><span class="sxs-lookup"><span data-stu-id="2aae6-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2aae6-132">클라이언트 설치 문제 해결 정보</span><span class="sxs-lookup"><span data-stu-id="2aae6-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="2aae6-133"><strong>% Temp% 폴더에 오류 로그를 표시 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="2aae6-134">로그 파일을 검토 하려면 시작을 클릭 하 고 <strong> </strong> <strong> % temp% </strong> 를 입력 한 다음 <strong> appv_ 로그를 찾습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="2aae6-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="2aae6-135">App-v 5.1 클라이언트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="2aae6-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="2aae6-136">앱-V 5.1 클라이언트 설치 파일을 설치할 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="2aae6-137">다음 클라이언트 유형 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2aae6-138">클라이언트 유형</span><span class="sxs-lookup"><span data-stu-id="2aae6-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="2aae6-139">사용할 파일</span><span class="sxs-lookup"><span data-stu-id="2aae6-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2aae6-140">표준 버전의 클라이언트</span><span class="sxs-lookup"><span data-stu-id="2aae6-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="2aae6-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="2aae6-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2aae6-142">클라이언트의 원격 데스크톱 서비스 버전</span><span class="sxs-lookup"><span data-stu-id="2aae6-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="2aae6-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="2aae6-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="2aae6-144">설치 파일을 두 번 클릭 하 고 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="2aae6-145">설치가 시작 되기 전에 설치 관리자는 컴퓨터에 누락 된 [app-v 5.1 필수 조건이](app-v-51-prerequisites.md)있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="2aae6-146">소프트웨어 사용 조건을 검토 하 고 동의 하 고 Microsoft 업데이트 사용 여부와 Microsoft 사용자 환경 개선 프로그램에 참여할지 여부를 선택한 후 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="2aae6-147">**설정 완료** 됨 페이지에서 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="2aae6-148">설치 **프로그램**에서 앱-V 클라이언트에 대해 다음 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="2aae6-149">.exe</span><span class="sxs-lookup"><span data-stu-id="2aae6-149">.exe</span></span>**

    -   **<span data-ttu-id="2aae6-150">.msi</span><span class="sxs-lookup"><span data-stu-id="2aae6-150">.msi</span></span>**

    -   **<span data-ttu-id="2aae6-151">언어 팩</span><span class="sxs-lookup"><span data-stu-id="2aae6-151">language pack</span></span>**

        **<span data-ttu-id="2aae6-152">참고</span><span class="sxs-lookup"><span data-stu-id="2aae6-152">Note</span></span>**  
        <span data-ttu-id="2aae6-153">설치 후에는 .exe 파일만 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="2aae6-154">스크립트를 사용 하 여 App-v 5.1 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="2aae6-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="2aae6-155">대상 컴퓨터에 필수 구성 요소 소프트웨어를 모두 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="2aae6-156">[시작 하기 전에 수행할 작업을](#bkmk-clt-install-prereqs)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2aae6-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="2aae6-157">.Msi 파일을 사용 하 여 클라이언트를 설치 하는 경우 필수 구성 요소가 누락 되 면 설치에 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="2aae6-158">스크립트를 사용 하 여 App-v 5.1 클라이언트를 설치 하려면 **appv\_client\_setup.exe**에 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="2aae6-159">참고</span><span class="sxs-lookup"><span data-stu-id="2aae6-159">Note</span></span>**  
   <span data-ttu-id="2aae6-160">클라이언트 Windows Installer (.msi)는 **/log** 매개 변수를 제외 하 고 동일한 스위치 집합을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="2aae6-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-162">설치 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-162">Specifies the installation directory.</span></span> <span data-ttu-id="2aae6-163">사용 예: <strong> /INSTALLDIR = C:\Program Files\AppV Client</span><span class="sxs-lookup"><span data-stu-id="2aae6-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="2aae6-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-165">사용자 환경 개선 프로그램의 참여를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="2aae6-166">사용 예: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="2aae6-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-168">Microsoft 업데이트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-168">Enables Microsoft Update.</span></span> <span data-ttu-id="2aae6-169">사용 예: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-170">/REPACKAGE설치 루트</span><span class="sxs-lookup"><span data-stu-id="2aae6-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-171">모든 새 응용 프로그램 및 업데이트를 설치할 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="2aae6-172">사용 예: <strong> /Package설치 루트 =&#39;C:\App-V 패키지&#39;</span><span class="sxs-lookup"><span data-stu-id="2aae6-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="2aae6-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-174">패키지 콘텐츠를 다운로드 하는 데 사용할 원본 위치를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="2aae6-175">사용 예: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="2aae6-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="2aae6-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-177">앱-V 5.1에서 새 패키지를 특정 컴퓨터에 로드 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="2aae6-178">다음 옵션을 사용할 수 있습니다: [1]. 모든 패키지 [2]을 (를) 자동으로 로드 합니다. 또는 자동으로 패키지 [0]을 (를) 로드 합니다. <strong> 사용 예:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="2aae6-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="2aae6-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-180">스트리밍된 패키지 콘텐츠를 로컬 하드 디스크에 저장 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="2aae6-181">사용 예: <strong> /Sharedcontentstoremode = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="2aae6-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-183">이전 버전을 사용 하 여 만든 패키지와 연결 되는 것 처럼 App-v 5.1 클라이언트에서 바로 가기 및 FTAs 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="2aae6-184">사용 예: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="2aae6-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-186">패키지 매니페스트 파일에 정의 된 스크립트 또는 실행 해야 하는 구성 파일을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="2aae6-187">사용 예: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="2aae6-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-189">사용자 프로필과 로밍할 수 없는 레지스트리 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="2aae6-190">사용 예: <strong> /ROAMINGREGISTRYEXCLUSIONS = \\수업, \클라이언트</span><span class="sxs-lookup"><span data-stu-id="2aae6-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="2aae6-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-192">사용자&#39;s 프로필을 사용 하 여 로밍 하지 않는% userprofile%를 기준으로 하는 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="2aae6-193">사용 예: <strong> /ROAMINGFILEEXCLUSIONS &#39;desktop, 내 사진&#39;</span><span class="sxs-lookup"><span data-stu-id="2aae6-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="2aae6-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-195">게시 서버의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="2aae6-196">사용 예: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="2aae6-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="2aae6-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-198">게시 서버의 URL을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="2aae6-199">사용 예: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="2aae6-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="2aae6-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-201">전역 게시 새로 고침을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="2aae6-202">사용 예: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="2aae6-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-204">사용자가 로그온 할 때 전역 게시 새로 고침을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="2aae6-205">사용 예: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="2aae6-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-207">게시 새로 고침 간격을 지정 합니다 <strong> . 여기서 0 </strong> 은 주기적으로 새로 고쳐지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="2aae6-208">사용 예: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="2aae6-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="2aae6-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-210">간격 단위 (시 [0], 일 [1])를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="2aae6-211">사용 예: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="2aae6-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-213">사용자 게시 새로 고침을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-213">Enables user publishing refresh.</span></span> <span data-ttu-id="2aae6-214">사용 예: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="2aae6-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-216">사용자가 로그온 할 때 사용자 게시 새로 고침을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="2aae6-217">사용 예: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="2aae6-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-219">게시 새로 고침 간격을 지정 합니다 <strong> . 여기서 0 </strong> 은 주기적으로 새로 고쳐지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="2aae6-220">사용 예: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="2aae6-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="2aae6-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-222">간격 단위 (시 [0], 일 [1])를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="2aae6-223">사용 예: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2aae6-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-224">/Log</span><span class="sxs-lookup"><span data-stu-id="2aae6-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-225">로그 정보가 저장 되는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="2aae6-226">기본 위치 는% Temp%입니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-226">The default location is %Temp%.</span></span> <span data-ttu-id="2aae6-227">사용 예: <strong> /Log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="2aae6-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-228">/q</span><span class="sxs-lookup"><span data-stu-id="2aae6-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-229">무인 설치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-230">/REPAIR</span><span class="sxs-lookup"><span data-stu-id="2aae6-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-231">이전 클라이언트 설치를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="2aae6-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-233">클라이언트 설치 후 컴퓨터가 다시 부팅 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="2aae6-234">이 매개 변수는 각 업데이트가 설치 된 후 최종 사용자 컴퓨터가 다시 부팅 되지 않도록 하 고, 편리한 시간에 재부팅을 예약할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="2aae6-235">예를 들어 App-v 5.1를 설치한 다음 서비스 팩 설치 후 재부팅 하지 않고 핫픽스 패키지 Y를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="2aae6-236">설치 후에는 App-v를 사용 하기 전에 다시 부팅 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-237">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="2aae6-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-238">클라이언트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="2aae6-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-240">사용권 계약을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-240">Accepts the license agreement.</span></span> <span data-ttu-id="2aae6-241">무인 설치에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-241">This is required for an unattended installation.</span></span> <span data-ttu-id="2aae6-242">사용 예: <strong> /ACCEPTEULA </strong> 또는 <strong> /ACCEPTEULA = 1 </strong></span><span class="sxs-lookup"><span data-stu-id="2aae6-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="2aae6-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-244">연결 된 레이아웃 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-244">Specifies the associated layout action.</span></span> <span data-ttu-id="2aae6-245">또한 앱-V 5.1를 설치 하지 않고 Windows Installer (.msi) 및 스크립트 파일을 폴더로 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="2aae6-246">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2aae6-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="2aae6-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-248">레이아웃 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-248">Specifies the layout directory.</span></span> <span data-ttu-id="2aae6-249">문자열 값이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-249">Requires a string value.</span></span> <span data-ttu-id="2aae6-250">사용 예: <strong> /Layoutdir = "C:\Application Virtualization Client" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2aae6-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2aae6-251">/?,/h,/help</span><span class="sxs-lookup"><span data-stu-id="2aae6-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2aae6-252">이전 설치 매개 변수에 대 한 도움말을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="2aae6-253">Windows Installer (.msi) 파일을 사용 하 여 App-v 5.1 클라이언트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="2aae6-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="2aae6-254">대상 컴퓨터에 필수 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="2aae6-255">[시작 하기 전에 수행할 작업을](#bkmk-clt-install-prereqs)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2aae6-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="2aae6-256">전제 조건이 충족 되지 않으면 설치가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="2aae6-257">앱-V 5.1 Windows Installer (.msi) 파일을 사용 하 여 클라이언트를 설치 하기 전에 대상 컴퓨터에 보류 중인 다시 시작이 없는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="2aae6-258">Windows Installer 파일은 보류 중인 다시 시작에 플래그를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="2aae6-259">다음 Windows Installer 파일 중 하나를 대상 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="2aae6-260">지정 하는 파일은 대상 컴퓨터의 구성과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2aae6-261">배포 유형</span><span class="sxs-lookup"><span data-stu-id="2aae6-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="2aae6-262">이 파일 배포</span><span class="sxs-lookup"><span data-stu-id="2aae6-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2aae6-263">컴퓨터에서 32 비트 Microsoft Windows 운영 체제를 실행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aae6-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="2aae6-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2aae6-265">컴퓨터에서 64 비트 Microsoft Windows 운영 체제를 실행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aae6-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="2aae6-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2aae6-267">App-v 5.1 원격 데스크톱 서비스 클라이언트를 배포 하는 경우</span><span class="sxs-lookup"><span data-stu-id="2aae6-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aae6-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="2aae6-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="2aae6-269">다음 표의 정보를 사용 하 여 대상 컴퓨터에 대해 원하는 언어를 기반으로 설치할 해당 언어 팩 (.msi)을 선택 합니다 **.**</span><span class="sxs-lookup"><span data-stu-id="2aae6-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="2aae6-270">테이블의 **xxxx** 는 언어 팩의 대상 로캘을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="2aae6-271">시작 하기 전에 알아야 할 사항:</span><span class="sxs-lookup"><span data-stu-id="2aae6-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="2aae6-272">언어 팩은 표준 App-v 5.1 클라이언트와 App-v 5.1 클라이언트의 원격 데스크톱 서비스 버전에 모두 공통으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="2aae6-273">**.Exe**를 사용 하 여 app-v 5.1 클라이언트를 설치 하면 설치 관리자가 대상 컴퓨터에서 실행 중인 운영 체제와 일치 하는 언어 팩만 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="2aae6-274">대상 컴퓨터에 추가 언어 팩을 배포 하려면 **Windows Installer (.msi) 파일을 사용 하 여 app-v 5.1 클라이언트를 설치 하**는 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2aae6-275">배포 유형</span><span class="sxs-lookup"><span data-stu-id="2aae6-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="2aae6-276">이 파일 배포</span><span class="sxs-lookup"><span data-stu-id="2aae6-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2aae6-277">컴퓨터에서 32 비트 Microsoft Windows 운영 체제를 실행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aae6-278">appv_client_LP_xxxx_ x86.msi</span><span class="sxs-lookup"><span data-stu-id="2aae6-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2aae6-279">컴퓨터에서 64 비트 Microsoft Windows 운영 체제를 실행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="2aae6-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aae6-280">appv_client_LP_xxxx_ x64.msi</span><span class="sxs-lookup"><span data-stu-id="2aae6-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="2aae6-281">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2aae6-281">Related topics</span></span>


[<span data-ttu-id="2aae6-282">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="2aae6-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="2aae6-283">클라이언트 구성 설정 정보</span><span class="sxs-lookup"><span data-stu-id="2aae6-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="2aae6-284">App-V 5.1 Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="2aae6-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









