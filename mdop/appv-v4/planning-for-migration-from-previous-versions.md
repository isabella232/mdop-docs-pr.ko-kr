---
title: 이전 버전에서 마이그레이션 계획
description: 이전 버전에서 마이그레이션 계획
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815928"
---
# <span data-ttu-id="70943-103">이전 버전에서 마이그레이션 계획</span><span class="sxs-lookup"><span data-stu-id="70943-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="70943-104">Microsoft Application Virtualization 4.5 이상 버전으로 업그레이드 하기 전에 4.1 이전 버전을 버전 4.1으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="70943-105">먼저 클라이언트를 업그레이드 한 다음 서버 구성 요소를 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="70943-106">4.5로 업그레이드 된 클라이언트는 아직 업그레이드 하지 않은 응용 프로그램 가상화 서버와 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="70943-107">이전 버전의 클라이언트는 4.5로 업그레이드 된 서버에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="70943-108">시스템 구성 요소를 업그레이드 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 배포 및 업그레이드 고려 사항을](application-virtualization-deployment-and-upgrade-considerations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70943-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="70943-109">마이그레이션을 성공적으로 수행 하기 위해 응용 프로그램 가상화 시스템 구성 요소를 다음 순서로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="70943-110">Microsoft Application Virtualization 클라이언트.</span><span class="sxs-lookup"><span data-stu-id="70943-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="70943-111">단계별 업그레이드 지침은 [Application Virtualization 클라이언트를 업그레이드 하는 방법을](how-to-upgrade-the-application-virtualization-client.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70943-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="70943-112">Microsoft Application Virtualization 서버 및 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="70943-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="70943-113">단계별 업그레이드 지침은 [서버 및 시스템 구성 요소를 업그레이드 하는 방법을](how-to-upgrade-the-servers-and-system-components.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70943-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="70943-114">**참고**  둘 이상의 서버에서 Application Virtualization 데이터베이스에 대 한 액세스를 공유 하는 경우에는 데이터베이스를 업그레이드 하는 동안 해당 서버를 모두 오프 라인 상태로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="70943-115">데이터베이스 업그레이드에 대 한 일반적인 비즈니스 관행을 준수 해야 하지만, 테스트 서버에서 먼저 데이터베이스의 백업 복사본을 사용 하 여 데이터베이스 업그레이드를 테스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="70943-116">그런 다음 데이터베이스 스키마를 업그레이드 하는 첫 번째 업그레이드에 대 한 서버 중 하나를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="70943-117">프로덕션 데이터베이스가 성공적으로 업그레이드 된 후에는 다른 서버를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="70943-118">Microsoft Application Virtualization 관리 웹 서비스.</span><span class="sxs-lookup"><span data-stu-id="70943-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="70943-119">이 단계는 관리 웹 서비스가 별도의 서버에 있는 경우에만 적용 되며, 웹 서비스를 업그레이드 하려면 별도의 서버에서 서버 설치 관리자 프로그램을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="70943-120">그렇지 않으면 이전 서버 업그레이드 단계에서 관리 웹 서비스를 자동으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="70943-121">Microsoft Application Virtualization 관리 콘솔.</span><span class="sxs-lookup"><span data-stu-id="70943-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="70943-122">이 단계는 관리 콘솔이 별도의 컴퓨터에 있는 경우에만 적용 되 고 콘솔을 업그레이드 하려면 별도의 컴퓨터에서 서버 설치 관리자 프로그램을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="70943-123">그렇지 않은 경우에는 이전 서버 업그레이드 단계에서 관리 콘솔을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="70943-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="70943-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="70943-125">단계별 지침은 [Application Virtualization Sequencer를 설치 하는 방법을](how-to-install-the-application-virtualization-sequencer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70943-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="70943-126">버전 4.2에 시퀀싱 된 모든 가상 응용 프로그램 패키지는 버전 4.5에서 사용할 수 있도록 다시 시퀀싱 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70943-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="70943-127">그러나 기본 Acl (액세스 제어 목록)을 적용 하거나 Windows Installer 파일을 생성 하려면 가상 패키지를 Microsoft Application Virtualization 4.5 형식으로 업그레이드 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="70943-128">이는 간단한 프로세스 이며 4.5 시퀀서를 사용 하 여 기존 가상 응용 프로그램 패키지를 열고 저장할 수만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="70943-129">이는 Application Virtualization Sequencer 명령줄 인터페이스를 사용 하 여 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="70943-130">앱-V 4.6 클라이언트 패키지 지원</span><span class="sxs-lookup"><span data-stu-id="70943-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="70943-131">이전 버전의 App-v 4.6 클라이언트에 만든 패키지를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="70943-132">그러나 적절 한 운영 체제 및 칩 아키텍처 정보가 포함 되도록 관련 된 **.osd** 파일을 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="70943-133">다음 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="70943-134">OS 값</span><span class="sxs-lookup"><span data-stu-id="70943-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-135">&lt;OS 값 = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-136">&lt;OS 값 = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-137">&lt;OS 값 = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-138">&lt;OS 값 = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-139">&lt;OS 값 = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-140">&lt;OS 값 = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-141">&lt;OS 값 = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-142">&lt;OS 값 = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-143">&lt;OS 값 = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-144">&lt;OS 값 = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-145">&lt;OS 값 = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="70943-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="70943-146">새로 만든 32 비트 패키지를 실행 하려면 App-V 4.6 Sequencer가 설치 된 32 비트 운영 체제를 실행 하는 컴퓨터에서 응용 프로그램을 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="70943-147">응용 프로그램을 시퀀싱 한 후에는 시퀀서 콘솔에서 **배포** 탭을 선택한 다음 필요에 따라 적절 한 운영 체제와 칩 아키텍처를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="70943-148">**중요**  64 비트 운영 체제를 실행 하는 컴퓨터에서 시퀀싱 된 응용 프로그램은 64 비트 운영 체제를 실행 하는 컴퓨터에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="70943-149">새 32-app-v 4.6 Sequencer를 사용 하 여 만든 비트 패키지는 App-v 4.5 클라이언트를 실행 하는 컴퓨터에서 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="70943-150">App-v 4.6 클라이언트에서 새 64 비트 패키지를 실행 하려면 App-v 4.6 Sequencer를 실행 하는 컴퓨터에서 응용 프로그램을 시퀀싱 하 고 64 비트 운영 체제를 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="70943-151">응용 프로그램을 시퀀싱 한 후에는 시퀀서 콘솔에서 **배포** 탭을 선택한 다음 필요에 따라 적절 한 운영 체제와 칩 아키텍처를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="70943-152">다음 표에는 다양 한 버전의 시퀀서를 사용 하 여 만든 패키지를 실행 하는 클라이언트 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="70943-153">App-V 4.2 Sequencer를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="70943-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="70943-154">App-V 4.5 Sequencer를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="70943-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="70943-155">32 비트 앱-V 4.6 시퀀서를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="70943-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="70943-156">64 비트 앱-V 4.6 시퀀서를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="70943-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="70943-157">32 비트 앱-V 4.6 SP1 시퀀서를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="70943-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="70943-158">64 비트 앱-V 4.6 SP1 시퀀서를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="70943-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-159">4.2 클라이언트</span><span class="sxs-lookup"><span data-stu-id="70943-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-160">예</span><span class="sxs-lookup"><span data-stu-id="70943-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-161">아니오</span><span class="sxs-lookup"><span data-stu-id="70943-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-162">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-163">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-164">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-165">아니오</span><span class="sxs-lookup"><span data-stu-id="70943-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-166">4.5 클라이언트 ¹</span><span class="sxs-lookup"><span data-stu-id="70943-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-167">예</span><span class="sxs-lookup"><span data-stu-id="70943-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-168">예</span><span class="sxs-lookup"><span data-stu-id="70943-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-169">아니오</span><span class="sxs-lookup"><span data-stu-id="70943-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-170">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-171">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-172">아니오</span><span class="sxs-lookup"><span data-stu-id="70943-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-173">4.6 클라이언트 (32 비트)</span><span class="sxs-lookup"><span data-stu-id="70943-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-174">예</span><span class="sxs-lookup"><span data-stu-id="70943-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-175">예</span><span class="sxs-lookup"><span data-stu-id="70943-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-176">예</span><span class="sxs-lookup"><span data-stu-id="70943-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-177">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-178">예</span><span class="sxs-lookup"><span data-stu-id="70943-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-179">아니오</span><span class="sxs-lookup"><span data-stu-id="70943-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-180">4.6 클라이언트 (64 비트)</span><span class="sxs-lookup"><span data-stu-id="70943-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-181">예</span><span class="sxs-lookup"><span data-stu-id="70943-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-182">예</span><span class="sxs-lookup"><span data-stu-id="70943-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-183">예</span><span class="sxs-lookup"><span data-stu-id="70943-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-184">예</span><span class="sxs-lookup"><span data-stu-id="70943-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-185">예</span><span class="sxs-lookup"><span data-stu-id="70943-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-186">예</span><span class="sxs-lookup"><span data-stu-id="70943-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70943-187">4.6 SP1 클라이언트</span><span class="sxs-lookup"><span data-stu-id="70943-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-188">예</span><span class="sxs-lookup"><span data-stu-id="70943-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-189">예</span><span class="sxs-lookup"><span data-stu-id="70943-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-190">예</span><span class="sxs-lookup"><span data-stu-id="70943-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-191">아니요</span><span class="sxs-lookup"><span data-stu-id="70943-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-192">예</span><span class="sxs-lookup"><span data-stu-id="70943-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-193">아니오</span><span class="sxs-lookup"><span data-stu-id="70943-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70943-194">4.6 SP1 클라이언트 (64 비트)</span><span class="sxs-lookup"><span data-stu-id="70943-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-195">예</span><span class="sxs-lookup"><span data-stu-id="70943-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-196">예</span><span class="sxs-lookup"><span data-stu-id="70943-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-197">예</span><span class="sxs-lookup"><span data-stu-id="70943-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-198">예</span><span class="sxs-lookup"><span data-stu-id="70943-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-199">예</span><span class="sxs-lookup"><span data-stu-id="70943-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="70943-200">예</span><span class="sxs-lookup"><span data-stu-id="70943-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="70943-201">¹ App-V 4.5, App-v 4.5 CU1 및 App-v 4.5 SP1을 비롯 한 모든 App-v 4.5 클라이언트 버전에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70943-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="70943-202">추가 마이그레이션 고려 사항</span><span class="sxs-lookup"><span data-stu-id="70943-202">Additional Migration Considerations</span></span>


<span data-ttu-id="70943-203">App-v 4.5 시퀀서의 기능 중 하나는 Microsoft 끝점 구성 관리자와 같은 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 가상 응용 프로그램 패키지의 제어 지점으로 Windows Installer 파일 (.msi)을 만드는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="70943-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="70943-204">Xxx 4.1 또는 4.2 클라이언트에 설치 되어 있으며 이후 4.5로 업그레이드 되는 응용 프로그램 가상화에 대 한 .msi 도구를 사용 하 여 만든 이전 Windows Installer 파일은 4.5 클라이언트에 설치 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="70943-205">그러나 4.5 시퀀서에서 업그레이드 하지 않는 한 제거 하거나 업그레이드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="70943-206">원본 사전 4.5 가상 응용 프로그램 패키지는 4.5 시퀀서에서 열고 Windows Installer 파일로 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="70943-207">**참고**  App-v 4.2 클라이언트가 4.5로 이미 업그레이드 된 경우 스크립트를 사용 하 여 4.5 클라이언트에서 4.2 패키지를 보존 하 고 관리 하도록 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70943-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="70943-208">이 스크립트는 msvcp71.dll 및 msvcr71.dll의 두 파일을 App-v 설치 폴더에 복사 하 고 레지스트리 키 \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\] 아래에 다음 레지스트리 키 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="70943-209">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="70943-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="70943-210">"GlobalDataDirectory" = "C:\\\\Documents 및 Settings\\\\All Users\\\\Documents\\\\" (전역적으로 쓰기 가능한 위치)</span><span class="sxs-lookup"><span data-stu-id="70943-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="70943-211">App-v 4.5 Sequencer에서 생성 된 Windows Installer 파일은 App-v 4.6 클라이언트에서 실행 하려고 할 때 "이 패키지에 Microsoft Application Virtualization 클라이언트 4.5 이상"이 필요 합니다. 라는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70943-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="70943-212">App-v 4.5 SP1 Sequencer 또는 App-v 4.6 Sequencer를 사용 하 여 이전 패키지를 열고 패키지에 대 한 새 .msi를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="70943-213">생성 및 저장 된 모든 4.2 보고서는 서버를 4.5로 업그레이드할 때 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="70943-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="70943-214">이러한 보고서를 유지 해야 하는 경우 서버의 SoftGrid 관리 콘솔 폴더에 있는 SftMMC .msc 파일의 백업 복사본을 저장 하 고 해당 복사본을 사용 하 여 업그레이드 중에 설치 된 새 SftMMC를 대체 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70943-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="70943-215">이전 버전에서 업그레이드 하는 방법에 대 한 자세한 내용은 [Microsoft Application Virtualization 4.5 질문과 대답 ()으로 업그레이드](https://go.microsoft.com/fwlink/?LinkId=120358) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="70943-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="70943-216">관련 항목</span><span class="sxs-lookup"><span data-stu-id="70943-216">Related topics</span></span>


[<span data-ttu-id="70943-217">Application Virtualization 시스템 배포 계획</span><span class="sxs-lookup"><span data-stu-id="70943-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





