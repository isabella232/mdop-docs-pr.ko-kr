---
title: 가상화된 응용 프로그램이 있는 가상 환경에서 로컬로 설치된 응용 프로그램 실행
description: 가상화된 응용 프로그램이 있는 가상 환경에서 로컬로 설치된 응용 프로그램 실행
author: dansimp
ms.assetid: 71baf193-a9e8-4ffa-aa7f-e0bffed2e4b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 384a1325b2f363595971f70f25fe0a25cade448d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813297"
---
# <span data-ttu-id="90f44-103">가상화된 응용 프로그램이 있는 가상 환경에서 로컬로 설치된 응용 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="90f44-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="90f44-104">Microsoft Application Virtualization (App-v)를 사용 하 여 가상화 된 응용 프로그램과 함께 가상 환경에서 로컬에 설치 된 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="90f44-105">다음과 같은 경우에이 작업을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="90f44-106">클라이언트 컴퓨터에 로컬로 응용 프로그램을 설치 하 고 실행 하지만 해당 로컬 응용 프로그램을 사용 하는 특정 플러그 인을 가상화 하 고 실행 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="90f44-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="90f44-107">App-v 클라이언트 패키지의 문제를 해결 하 고 App-v 가상 환경 내에서 로컬 응용 프로그램을 열려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="90f44-108">다음 메서드 중 하나를 사용 하 여 App-v 가상 환경 내에서 로컬 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="90f44-109">가상 레지스트리 키 run</span><span class="sxs-lookup"><span data-stu-id="90f44-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="90f44-110">AppvClientPackage PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="90f44-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="90f44-111">명령줄 전환/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="90f44-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="90f44-112">명령줄 후크 스위치/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="90f44-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="90f44-113">각 메서드는 본질적으로 동일한 작업을 수행 하지만 일부 메서드는 가상화 된 응용 프로그램이 이미 실행 중인지 여부에 따라 다른 응용 프로그램에 적합 한 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="90f44-114">가상 레지스트리 키 run</span><span class="sxs-lookup"><span data-stu-id="90f44-114">RunVirtual registry key</span></span>


<span data-ttu-id="90f44-115">패키지 또는 연결 그룹의 가상 환경에 로컬로 설치 된 응용 프로그램을 추가 하려면 `RunVirtual` 다음 섹션에서 설명 하는 대로 레지스트리 편집기에서 레지스트리 키에 하위 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="90f44-116">이 레지스트리 키를 관리 하는 데 사용할 수 있는 그룹 정책 설정이 없으므로 System Center Configuration Manager 또는 다른 전자 소프트웨어 배포 (ESD) 시스템을 사용 하거나 수동으로 레지스트리를 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="90f44-117">RunVirtual을 사용할 때 패키지를 게시 하는 지원 되는 방법</span><span class="sxs-lookup"><span data-stu-id="90f44-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="90f44-118">App-V 버전</span><span class="sxs-lookup"><span data-stu-id="90f44-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="90f44-119">지원 되는 게시 방법</span><span class="sxs-lookup"><span data-stu-id="90f44-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90f44-120">App-v 5.0 SP3 및 App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="90f44-120">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="90f44-121">전역 또는 사용자에 게 게시</span><span class="sxs-lookup"><span data-stu-id="90f44-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90f44-122">앱-V 5.0-app-v 5.0 SP2를 통해</span><span class="sxs-lookup"><span data-stu-id="90f44-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="90f44-123">전체적 으로만 게시</span><span class="sxs-lookup"><span data-stu-id="90f44-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="90f44-124">하위 키를 만드는 단계</span><span class="sxs-lookup"><span data-stu-id="90f44-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="90f44-125">다음 표의 정보를 사용 하 여 **MyApp.exe**같은 실행 파일의 이름을 사용 하 여 새 레지스트리 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="90f44-126">패키지 게시 방법</span><span class="sxs-lookup"><span data-stu-id="90f44-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="90f44-127">레지스트리 키를 만드는 위치</span><span class="sxs-lookup"><span data-stu-id="90f44-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="90f44-128">전역 게시</span><span class="sxs-lookup"><span data-stu-id="90f44-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90f44-129">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="90f44-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="90f44-130">예 </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="90f44-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="90f44-131">사용자에 게 게시</span><span class="sxs-lookup"><span data-stu-id="90f44-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90f44-132">HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="90f44-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="90f44-133">예 </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="90f44-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="90f44-134">연결 그룹에는 다음이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="90f44-135">사용자에 게 전역 또는 단순한 방법 으로만 게시 되는 패키지</span><span class="sxs-lookup"><span data-stu-id="90f44-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="90f44-136">전역 및 사용자에 게 게시 되는 패키지</span><span class="sxs-lookup"><span data-stu-id="90f44-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="90f44-137">HKEY_LOCAL_MACHINE 또는 HKEY_CURRENT_USER 키 중 하나를 사용할 수 있지만 다음 조건이 모두 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="90f44-138">가상 환경에 여러 패키지를 포함 하려는 경우 사용 하도록 설정 된 연결 그룹에 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="90f44-139">연결 그룹의 패키지 중 하나에 대 한 하위 키를 하나만 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="90f44-140">예를 들어 전역에 게시 된 하나의 패키지와 사용자에 게 게시 되는 다른 패키지가 있는 경우 이러한 패키지 중 하나에 대해서만 하위 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="90f44-141">패키지 중 하나에 대해서만 하위 키를 만들 수 있지만, 연결 그룹의 모든 패키지와 로컬 응용 프로그램은 가상 환경에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="90f44-142">하위 키를 만드는 키는 패키지에 사용 하는 게시 방법과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="90f44-143">예를 들어 사용자에 게 패키지를 게시 한 경우에서 하위 키를 만들어야 합니다 <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="90f44-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="90f44-144">새 레지스트리 하위 키의 값을 패키지의 PackageId 및 인수로 설정 하 여 값을 밑줄로 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="90f44-145">**구문**: &lt; PackageId &gt; \ _ &lt; 로&gt;</span><span class="sxs-lookup"><span data-stu-id="90f44-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="90f44-146">**예**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="90f44-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="90f44-147">이전 예제의 응용 프로그램에서는 다음과 같이 레지스트리 내보내기 파일 (.reg 파일)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="90f44-148">AppvClientPackage PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="90f44-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="90f44-149">**시작 AppVVirtualProcess** cmdlet을 사용 하 여 패키지 이름을 검색 한 다음 지정 된 패키지의 가상 환경 내에서 프로세스를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="90f44-150">이 메서드를 사용 하면 패키지가 현재 실행 중인지 여부와 상관 없이 App-v 패키지의 컨텍스트 내에서 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="90f44-151">\*\* &lt; &gt; 패키지의\*\*이름 대신 다음 예제 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="90f44-152">패키지의 정확한 이름을 모르는 경우 명령줄 **get-AppvClientPackage \ \* executable\\**를 사용할 수 있습니다. <em> 여기서 \*\*executable </em> \* 은 응용 프로그램의 이름입니다 (예: Get-AppvClientPackage \ \* Word \ \*).</span><span class="sxs-lookup"><span data-stu-id="90f44-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="90f44-153">명령줄 전환/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="90f44-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="90f44-154">\*\*/Appvpid: &lt; pid &gt; \*\* 스위치를 모든 명령에 적용 하 여 pid (프로세스 ID)를 지정 하 여 선택한 가상 프로세스 내에서 명령이 실행 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="90f44-155">이 메서드를 사용 하면 이미 실행 중인 실행 파일을 비롯 하 여 동일한 App-v 환경에서 새 실행 파일이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="90f44-156">예:</span><span class="sxs-lookup"><span data-stu-id="90f44-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="90f44-157">앱-V 프로세스의 PID (프로세스 ID)를 찾으려면 관리자 권한 명령 프롬프트에서 **tasklist.exe** 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="90f44-158">명령줄 후크 스위치/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="90f44-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="90f44-159">이 스위치를 사용 하 여 App-v 패키지의 가상 환경 내에서 로컬 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="90f44-160">가상 환경이 이미 실행 되 고 있어야 하는 **/appvid** 스위치와 달리이 스위치를 사용 하 여 가상 환경을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="90f44-161">구문과</span><span class="sxs-lookup"><span data-stu-id="90f44-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="90f44-162">예:</span><span class="sxs-lookup"><span data-stu-id="90f44-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="90f44-163">패키지 GUID 및 응용 프로그램의 버전 GUID를 가져오려면 **AppvClientPackage** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="90f44-164">다음과 같이 **/appvve** 스위치를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="90f44-165">콜론</span><span class="sxs-lookup"><span data-stu-id="90f44-165">A colon</span></span>

-   <span data-ttu-id="90f44-166">원하는 패키지의 패키지 GUID</span><span class="sxs-lookup"><span data-stu-id="90f44-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="90f44-167">밑줄</span><span class="sxs-lookup"><span data-stu-id="90f44-167">An underscore</span></span>

-   <span data-ttu-id="90f44-168">원하는 패키지의 버전 ID</span><span class="sxs-lookup"><span data-stu-id="90f44-168">Version ID of the desired package</span></span>

<span data-ttu-id="90f44-169">패키지의 정확한 이름을 모르는 경우 명령줄 **get-AppvClientPackage \ \* executable\\** <em> 를 사용 하세요. 여기서 \*\*executable </em> \* 은 응용 프로그램의 이름입니다 (예: Get-AppvClientPackage \ \* Word \ \*).</span><span class="sxs-lookup"><span data-stu-id="90f44-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="90f44-170">이 메서드를 사용 하면 패키지가 현재 실행 중인지 여부와 상관 없이 App-v 패키지의 컨텍스트 내에서 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90f44-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="90f44-171">관련 항목</span><span class="sxs-lookup"><span data-stu-id="90f44-171">Related topics</span></span>


[<span data-ttu-id="90f44-172">App-V 5.1에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="90f44-172">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)

 

 





