---
title: Sequencer 설치 방법
description: Sequencer 설치 방법
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813953"
---
# <span data-ttu-id="c743a-103">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="c743a-103">How to Install the Sequencer</span></span>


<span data-ttu-id="c743a-104">다음 절차를 사용 하 여 Microsoft App-v (Application Virtualization) 5.0 sequencer를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="c743a-105">Sequencer를 실행 하는 컴퓨터는 App-v 5.0 클라이언트 버전을 실행 하 고 있지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="c743a-106">이전에 App-v 시퀀서 설치를 업그레이드 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="c743a-107">**중요**  시퀀서 요구 사항의 전체 목록은 [app-v 5.0 필수 구성 요소](app-v-50-prerequisites.md) 및 [App-v 5.0 지원 되는 구성](app-v-50-supported-configurations.md)의 sequencer 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c743a-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="c743a-108">명령줄을 사용 하 여 App-v 5.0 sequencer를 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="c743a-109">다음 목록에는 명령줄 및 **appv\_sequencer\_setup.exe**를 사용 하 여 sequencer를 설치 하는 옵션에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c743a-110">명령</span><span class="sxs-lookup"><span data-stu-id="c743a-110">Command</span></span></th>
<th align="left"><span data-ttu-id="c743a-111">설명</span><span class="sxs-lookup"><span data-stu-id="c743a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c743a-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="c743a-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-113">설치 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c743a-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="c743a-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-115">Microsoft 사용자 환경 개선 프로그램에서 참여할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c743a-116">/Log</span><span class="sxs-lookup"><span data-stu-id="c743a-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-117">설치 로그를 저장할 위치를 지정 합니다. 기본 위치는 <strong> % Temp% </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="c743a-118">예를 들어 <strong> C:\ 로그 \ </strong> .log.</span><span class="sxs-lookup"><span data-stu-id="c743a-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c743a-119">/q</span><span class="sxs-lookup"><span data-stu-id="c743a-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-120">자동 또는 자동 설치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c743a-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="c743a-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-122">Sequencer의 제거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c743a-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="c743a-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-124">사용권 계약을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-124">Accepts the license agreement.</span></span> <span data-ttu-id="c743a-125">무인 설치에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-125">This is required for an unattended installation.</span></span> <span data-ttu-id="c743a-126">사용 예: <strong> /ACCEPTEULA </strong> 또는 <strong> /ACCEPTEULA = 1 </strong></span><span class="sxs-lookup"><span data-stu-id="c743a-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c743a-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="c743a-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-128">연결 된 레이아웃 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-128">Specifies the associated layout action.</span></span> <span data-ttu-id="c743a-129">또한 앱-V 5.0를 설치 하지 않고 Windows Installer (.msi) 및 스크립트 파일을 폴더로 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="c743a-130">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c743a-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="c743a-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-132">레이아웃 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-132">Specifies the layout directory.</span></span> <span data-ttu-id="c743a-133">문자열 값이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-133">Requires a string value.</span></span> <span data-ttu-id="c743a-134">사용 예: <strong> /Layoutdir = "C:\Application Virtualization Client" </strong> .</span><span class="sxs-lookup"><span data-stu-id="c743a-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c743a-135">/?</span><span class="sxs-lookup"><span data-stu-id="c743a-135">/?</span></span> <span data-ttu-id="c743a-136">또는/h 또는/help</span><span class="sxs-lookup"><span data-stu-id="c743a-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="c743a-137">관련 도움말을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c743a-138">App-v 5.0 sequencer를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="c743a-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="c743a-139">앱-V 5.0 sequencer 설치 파일을 설치 될 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="c743a-140">**appv\_sequencer\_setup.exe** 를 두 번 클릭 하 고 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="c743a-141">**소프트웨어 사용 조건** 페이지에서 사용 약관을 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="c743a-142">사용 조건에 동의 하려면 **사용 조건에 동의를 선택 합니다.**</span><span class="sxs-lookup"><span data-stu-id="c743a-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="c743a-143">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-143">Click **Next**.</span></span>

3.  <span data-ttu-id="c743a-144">Microsoft **update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고 최신 페이지를 사용 하도록 설정 하려면 microsoft 업데이트를 **확인 하려면 microsoft update 사용 (권장)을 선택 합니다.**</span><span class="sxs-lookup"><span data-stu-id="c743a-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="c743a-145">Microsoft 업데이트를 실행할 수 없도록 설정 하려면 **Microsoft Update를 사용 하지 않겠습니다**.를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="c743a-146">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-146">Click **Next**.</span></span>

4.  <span data-ttu-id="c743a-147">**사용자 환경 개선 프로그램** 페이지에서 프로그램에 참여 하려면 **사용자 환경 개선 프로그램 참여**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="c743a-148">이렇게 하면 App-v 5.0을 사용 하는 방법에 대 한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="c743a-149">프로그램에 참여 하지 않으려면 **지금 프로그램에 참여 하 고 싶지 않습니다를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="c743a-150">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-150">Click **Install**.</span></span>

5.  <span data-ttu-id="c743a-151">시퀀서를 열려면 **시작** 을 클릭 한 다음 **Microsoft Application Virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="c743a-152">App-v 5.0 sequencer 설치 문제를 해결 하려면</span><span class="sxs-lookup"><span data-stu-id="c743a-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="c743a-153">Sequencer 설치에 대 한 자세한 내용은 **% temp%** 폴더에서 오류 로그를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c743a-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="c743a-154">로그 파일을 검토 하려면 **시작**을 클릭 하 고 **% temp%** 를 입력 한 다음 **appv\_ 로그**를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="c743a-155">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="c743a-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c743a-156">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c743a-157">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="c743a-157">Got an App-V issue?</span></span>** <span data-ttu-id="c743a-158">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c743a-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c743a-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c743a-159">Related topics</span></span>


[<span data-ttu-id="c743a-160">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="c743a-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





