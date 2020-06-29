---
title: SFTTRAY 명령 참조
description: SFTTRAY 명령 참조
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815353"
---
# <span data-ttu-id="bbd9a-103">SFTTRAY 명령 참조</span><span class="sxs-lookup"><span data-stu-id="bbd9a-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="bbd9a-104">Microsoft App-v (Application Virtualization) 클라이언트 트레이 응용 프로그램 sfttray.exe는 사용자가 일반적으로 사용 하는 동안 상호 작용 하는 App-v 클라이언트의 기본 사용자 인터페이스 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="bbd9a-105">이 프로그램은 모든 가상 응용 프로그램의 스트리밍 및 시작을 제어 하며 알림 영역에 표시 된 아이콘을 마우스 오른쪽 단추로 클릭 하 여 클라이언트 함수의 메뉴를 표시 하는 방법으로 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="bbd9a-106">이 메뉴를 통해 사용자는 응용 프로그램을 로드 하거나, 게시 새로 고침을 시작 하거나, 요청을 취소 하거나, 클라이언트를 오프 라인 모드로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="bbd9a-107">또한 사용자는 **끝내기**를 클릭 하 여 응용 프로그램 가상화 클라이언트 트레이 응용 프로그램과 모든 활성 응용 프로그램을 닫을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="bbd9a-108">기본적으로 가상 응용 프로그램이 시작 될 때마다 아이콘이 표시 되지만 SFTTRAY 명령을 사용 하 여이 동작을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="bbd9a-109">또한 응용 프로그램 가상화 클라이언트 트레이 응용 프로그램에는 시작 된 각 응용 프로그램에 대 한 진행률 표시줄과 활성 응용 프로그램에 대 한 상태 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="bbd9a-110">진행률 표시줄을 클릭 하면 응용 프로그램의 로드 또는 시작을 취소할 수 있는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="bbd9a-111">SFTTRAY 명령</span><span class="sxs-lookup"><span data-stu-id="bbd9a-111">SFTTRAY Commands</span></span>


<span data-ttu-id="bbd9a-112">명령 창에서 다음 명령을 실행 하 여 명령 및 명령줄 스위치의 목록을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="bbd9a-113">참고</span><span class="sxs-lookup"><span data-stu-id="bbd9a-113">Note</span></span>**  
<span data-ttu-id="bbd9a-114">각 사용자 컨텍스트에 대해 응용 프로그램 가상화 클라이언트 트레이 인스턴스가 하나 밖에 없기 때문에 새 SFTTRAY 명령을 시작 하면 이미 실행 중인 프로그램으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="bbd9a-115">명령 사용법</span><span class="sxs-lookup"><span data-stu-id="bbd9a-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="bbd9a-116">명령줄 스위치</span><span class="sxs-lookup"><span data-stu-id="bbd9a-116">Command-Line Switches</span></span>

<span data-ttu-id="bbd9a-117">SFTTRAY 명령줄 스위치는 다음 표에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bbd9a-118">스위치</span><span class="sxs-lookup"><span data-stu-id="bbd9a-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="bbd9a-119">설명</span><span class="sxs-lookup"><span data-stu-id="bbd9a-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbd9a-120">/CHIDE</span><span class="sxs-lookup"><span data-stu-id="bbd9a-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-121">Windows 알림 영역에서 SFTTRAY 아이콘을 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbd9a-122">Drivers</span><span class="sxs-lookup"><span data-stu-id="bbd9a-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-123">Windows 알림 영역에 SFTTRAY 아이콘을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbd9a-124">/QUIET</span><span class="sxs-lookup"><span data-stu-id="bbd9a-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-125">오류를 방지 하 여 사용자 승인이 필요한 메시지 상자를 표시 하지 못하게 하 여 무인 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbd9a-126">/EXE &lt; 대체 EXE&gt;</span><span class="sxs-lookup"><span data-stu-id="bbd9a-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-127">/LAUNCH와 함께 사용 하 여 OSD에 지정 된 대상 파일 대신 가상 응용 프로그램이 시작 될 때 가상 환경에서 실행 프로그램을 시작 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bbd9a-128">참고</span><span class="sxs-lookup"><span data-stu-id="bbd9a-128">Note</span></span></strong><br/><p><span data-ttu-id="bbd9a-129">예를 들어 "SFTTRAY.EXE/EXE REGEDIT.EXE/LAUNCH &lt; app"를 사용 &gt; 하 여 응용 프로그램이 실행 되 고 있는 가상 환경의 레지스트리를 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbd9a-130">/LAUNCH &lt; app &gt; [ &lt; args &gt; ]</span><span class="sxs-lookup"><span data-stu-id="bbd9a-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-131">가상 응용 프로그램을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-131">Starts a virtual application.</span></span> <span data-ttu-id="bbd9a-132">응용 프로그램의 이름 및 버전 또는 OSD 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="bbd9a-133">선택적으로 명령줄 인수를 가상 응용 프로그램에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bbd9a-134">참고</span><span class="sxs-lookup"><span data-stu-id="bbd9a-134">Note</span></span></strong><br/><p><span data-ttu-id="bbd9a-135">"SFTMIME.EXE/QUERY OBJ: APP/SHORT" 명령을 사용 하 여 사용 가능한 가상 응용 프로그램의 이름 및 버전 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbd9a-136">/CLOAD</span><span class="sxs-lookup"><span data-stu-id="bbd9a-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-137">가상 응용 프로그램을 로드 하거나 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbd9a-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="bbd9a-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-139">모든 응용 프로그램을 캐시로 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbd9a-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="bbd9a-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-141">모든 응용 프로그램에 대 한 게시 새로 고침을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbd9a-142">/LAUNCHRESULT &lt; 고유 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="bbd9a-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-143">고유 ID에 대해 지정 된 루트 이름을 기반으로 하는 메모리 매핑된 파일 및 전역 이벤트를 사용 하 여 sfttray.exe를 실행 하는 프로세스에 대 한 시작 결과 코드를 반환 합니다. ¹</span><span class="sxs-lookup"><span data-stu-id="bbd9a-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbd9a-144">/SFTFILE &lt; sft&gt;</span><span class="sxs-lookup"><span data-stu-id="bbd9a-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-145">선택 사항인 스위치는/TLOAD와 함께 사용 하 여 응용 프로그램의 SFT 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="bbd9a-146">지정 된 경우 응용 프로그램을 로드 하지 않고 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbd9a-147">/CEXIT</span><span class="sxs-lookup"><span data-stu-id="bbd9a-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbd9a-148">SFTTRAY 프로그램과 모든 활성 가상 응용 프로그램을 닫고 Windows 알림 영역에서 아이콘을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bbd9a-149">참고</span><span class="sxs-lookup"><span data-stu-id="bbd9a-149">Note</span></span>**  
<span data-ttu-id="bbd9a-150">¹ */Prresult* 명령줄 매개 변수는 전역 이벤트의 루트 이름을 지정 하 고 프로세스에 대 한 실행 결과 코드를 반환 하는 데 사용 되는 메모리 매핑된 파일을 sfttray.exe를 시작 하는 프로세스에 대 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="bbd9a-151">가상 환경 내에서 시작 프로세스가 호출 될 때 이벤트 이름이 가상화 되지 않도록 하려면 고유 식별자 이름을 "SFT-"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="bbd9a-152">메모리 매핑 영역의 크기는 64 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="bbd9a-153">이 매개 변수를 사용 하기 위해 시작 프로세스가 "고유 id-결과 \ _event" 라는 이름을 가진 이벤트와 "고유 id- &lt; &gt; 결과 \ _value" 라는 이름을 가진 메모리 매핑 파일을 만들고, &lt; 선택적으로 &gt; 이벤트에 " &lt; 고유 id &gt; -종료 \ _event"를 추가한 다음 시작 프로세스가 sfttray.exe를 실행 하 고 이벤트 신호를 받을 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="bbd9a-154">" &lt; 고유 ID &gt; -결과 \ _event" 이벤트가 신호를 받은 후에는 시작 프로세스가 메모리 매핑된 영역에서 64 비트 반환 코드를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="bbd9a-155">&lt; &gt; 가상 응용 프로그램이 종료 될 때 선택적 이벤트 "고유 ID-종료 \ _event"가 있는 경우 sfttray.exe가 이벤트를 열고 신호를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="bbd9a-156">시작 프로세스는 가상 응용 프로그램이 종료 되는 시점을 확인 해야 하는 경우이 종료 이벤트를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="bbd9a-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











