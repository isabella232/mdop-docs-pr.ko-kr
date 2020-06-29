---
title: MBAM 2.5 서버 소프트웨어 설치
description: MBAM 2.5 서버 소프트웨어 설치
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823393"
---
# <span data-ttu-id="e8a2d-103">MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="e8a2d-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="e8a2d-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하거나 명령줄 매개 변수를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 서버 소프트웨어를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="e8a2d-105">MBAM 2.5 서버 기능을 구성 하는 각 서버에 대해 서버 설치 프로세스를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="e8a2d-106">설치를 완료 한 후 서버 기능 구성 단계에 대해 [MBAM 2.5 서버 기능 구성을](configuring-the-mbam-25-server-features.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8a2d-107">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="e8a2d-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="e8a2d-108">설명</span><span class="sxs-lookup"><span data-stu-id="e8a2d-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a2d-109">MBAM 2.5 계획 정보 검토</span><span class="sxs-lookup"><span data-stu-id="e8a2d-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="e8a2d-110">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e8a2d-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="e8a2d-111">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="e8a2d-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="e8a2d-112">MBAM 2.5의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="e8a2d-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a2d-113">로그 파일을 가져오는 방법 읽기</span><span class="sxs-lookup"><span data-stu-id="e8a2d-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-114">기본적으로 로그 파일은 로컬 컴퓨터 의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="e8a2d-115">% Temp% 폴더가 아닌 특정 위치에 로그 파일을 쓰려면 <strong> </strong> <strong> /log </strong> &lt; <em> location 인수를 사용 </em> &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="e8a2d-116">다른 이벤트가 <strong> mbam-설정 </strong> 또는 <strong> mbam- </strong> <strong> 응용 프로그램 및 서비스의 웹 노드에서 &gt; Microsoft Windows를 기록 &gt; </strong> 하는 이벤트 뷰어에 기록 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="e8a2d-117">예를 들어, MBAM을 제거 하면 제거 관리자가 EventViewer에서 MBAM-설정 및 MBAM 웹 로그를 제거 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e8a2d-118">Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하 여 MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="e8a2d-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="e8a2d-119">다음 단계를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하 여 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="e8a2d-120">마법사를 사용 하 여 MBAM 2.5 서버 소프트웨어를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="e8a2d-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="e8a2d-121">MBAM을 설치 하려는 서버에서 **MBAMserversetup.exe** 를 실행 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="e8a2d-122">**시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="e8a2d-123">Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="e8a2d-124">업데이트를 확인할 때 Microsoft 업데이트 사용 여부를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="e8a2d-125">사용자 환경 개선 프로그램 참여 여부를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="e8a2d-126">설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="e8a2d-127">MBAM 서버 소프트웨어 설치가 완료 된 후 서버 기능을 구성 하려면 **마법사를 닫은 후에 Mbam 서버 구성 실행** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="e8a2d-128">또는 서버 설치가 **시작** 메뉴에 생성 하는 **Mbam 서버 구성** 바로 가기를 사용 하 여 나중에 mbam을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="e8a2d-129">**마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-129">Click **Finish**.</span></span>

## <span data-ttu-id="e8a2d-130">명령 프롬프트 창을 사용 하 여 MBAM 2.5 서버 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="e8a2d-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="e8a2d-131">명령 프롬프트에서 다음 명령과 비슷한 명령을 입력 하 여 MBAM 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="e8a2d-132">다음 표에서는 MBAM 2.5 서버 소프트웨어를 설치 하기 위한 명령줄 매개 변수를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8a2d-133">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8a2d-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e8a2d-134">매개 변수 값</span><span class="sxs-lookup"><span data-stu-id="e8a2d-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="e8a2d-135">설명</span><span class="sxs-lookup"><span data-stu-id="e8a2d-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a2d-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="e8a2d-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-137">True False</span><span class="sxs-lookup"><span data-stu-id="e8a2d-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-138">True-향상 시킬 MBAM 기능을 확인 하는 데 도움이 되는 사용자 개선 경험 프로그램에 참여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="e8a2d-139">False-고객 개선 사항 프로그램에 참여 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a2d-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="e8a2d-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-141">True False</span><span class="sxs-lookup"><span data-stu-id="e8a2d-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-142">True-Microsoft Update를 사용 하 여 컴퓨터를 안전 하 게 보호 하 고 Windows 및 다른 Microsoft 제품 (MBAM 포함)을 최신 상태로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="e8a2d-143">False-Microsoft 업데이트 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e8a2d-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a2d-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="e8a2d-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-145">&lt;경로&gt;</span><span class="sxs-lookup"><span data-stu-id="e8a2d-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-146">MBAM을 설치 하려는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="e8a2d-147">예:</span><span class="sxs-lookup"><span data-stu-id="e8a2d-147">Example:</span></span></p>
<p><span data-ttu-id="e8a2d-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="e8a2d-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a2d-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="e8a2d-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-150">True False</span><span class="sxs-lookup"><span data-stu-id="e8a2d-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a2d-151">True-제거 되지 않은 기능이 있어도 MBAM을 제거 하는 프로세스를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="e8a2d-152">False (기본값) 제거 사용자 지정 작업이 추가 된 MBAM 서버 기능을 제거 하지 못하면 제거에 실패 하 고 MBAM은 설치 된 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="e8a2d-153">두 경우 모두 MBAM을 제거 하는 동안 성공적으로 제거한 기능은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="e8a2d-154">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8a2d-154">Related topics</span></span>


[<span data-ttu-id="e8a2d-155">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="e8a2d-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="e8a2d-156">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="e8a2d-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="e8a2d-157">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="e8a2d-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e8a2d-158">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e8a2d-159">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8a2d-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





