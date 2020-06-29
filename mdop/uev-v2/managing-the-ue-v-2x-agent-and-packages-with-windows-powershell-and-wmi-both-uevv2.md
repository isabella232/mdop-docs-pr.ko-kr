---
title: Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 에이전트 및 패키지 관리
description: Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 에이전트 및 패키지 관리
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826803"
---
# <span data-ttu-id="25d90-103">Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 에이전트 및 패키지 관리</span><span class="sxs-lookup"><span data-stu-id="25d90-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="25d90-104">WMI (Windows Management Instrumentation) 및 Windows PowerShell을 사용 하 여 Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1 에이전트 구성 및 동기화 동작을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="25d90-105">UE-V PowerShell cmdlet의 전체 목록은 [ue-v 2 Cmdlet 참조](https://go.microsoft.com/fwlink/?LinkId=393495) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="25d90-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="25d90-106">Windows PowerShell을 사용 하 여 UE-V 에이전트를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="25d90-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="25d90-107">액세스 가능한 네트워크 공유에서 UE-V 설치 관리자 파일을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="25d90-108">참고</span><span class="sxs-lookup"><span data-stu-id="25d90-108">Note</span></span>**  
    <span data-ttu-id="25d90-109">AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="25d90-110">각 아키텍처에 대해 Windows Installer 패키지, AgentSetupx86.msi 및 AgentSetupx64.msi를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="25d90-111">나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="25d90-112">다음 Windows PowerShell 명령 중 하나를 사용 하 여 UE-V 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="25d90-113">Windows PowerShell을 사용 하 여 UE-V 에이전트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="25d90-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="25d90-114">Windows PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="25d90-115">*컴퓨터 매개 변수* 를 사용 하 여 컴퓨터의 모든 사용자에 게 영향을 주는 컴퓨터 설정을 관리 하려면 관리자 권한이 있는 계정을 사용 하 여 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="25d90-116">다음 Windows PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="25d90-117">Windows PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="25d90-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="25d90-118">설명</span><span class="sxs-lookup"><span data-stu-id="25d90-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="25d90-119">유효한 UE-V Agent 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="25d90-120">사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="25d90-121">현재 사용자에 대해서만 UE-V 에이전트 설정 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-122">컴퓨터의 모든 사용자에 대 한 UE-V 에이전트 구성 설정 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-123">각 구성 설정에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="25d90-124">설정이 구성 된 위치를 표시 하거나 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="25d90-125">현재 설정이 유효한 경우 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-126">도움말 링크에 대 한 회사 설정 센터에 표시 되는 텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-127">도움말 링크에 대 한 회사 설정 센터의 링크에 대 한 URL을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="25d90-128">모든 URL 프로토콜을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-129">컴퓨터의 모든 사용자에 대해 Windows 앱을 동기화 하지 않도록 UE-V Agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-130">현재 컴퓨터 사용자에 대 한 Windows 앱을 동기화 하지 않도록 UE-V Agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-131">컴퓨터의 모든 사용자가 처음으로 에이전트를 실행할 때 UE-V Agent에서 알림을 표시 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-132">컴퓨터의 모든 사용자가 처음으로 에이전트를 실행할 때 UE-V Agent가 알림을 표시 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-133">설정 동기화가 지연 될 때 UE-V Agent를 구성 하 여 컴퓨터의 모든 사용자에 게 알립니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="25d90-134"><em>DisableSettingsImportNotify </em> 매개 변수를 사용 하 여 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-135">설정 동기화가 지연 될 때 현재 사용자에 게 알리기 위해 UE-V Agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="25d90-136"><em>DisableSettingsImportNotify </em> 매개 변수를 사용 하 여 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-137">컴퓨터의 모든 사용자에 대해 Windows 앱 목록에서 명시적으로 사용 하지 않도록 설정 하지 않은 모든 Windows 앱을 동기화 하도록 UE-V Agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="25d90-138">자세한 내용은 &quot; &quot; <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> WINDOWS PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿을 관리 UevAppxPackage을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="25d90-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="25d90-139"><em>DisableSyncUnlistedWindows8Apps </em> 매개 변수를 사용 하 여 Windows 앱 목록에서 명시적으로 사용 하도록 설정 된 windows 앱만 동기화 하도록 ue-v agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-140">컴퓨터의 현재 사용자에 대해 Windows 앱 목록에서 명시적으로 사용 하지 않도록 설정 되지 않은 모든 Windows 앱을 동기화 하도록 UE-V Agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="25d90-141">자세한 내용은 &quot; &quot; <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> WINDOWS PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿을 관리 UevAppxPackage을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="25d90-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="25d90-142"><em>DisableSyncUnlistedWindows8Apps </em> 매개 변수를 사용 하 여 Windows 앱 목록에서 명시적으로 사용 하도록 설정 된 windows 앱만 동기화 하도록 ue-v agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-143">컴퓨터의 모든 사용자에 대해 UE-V를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="25d90-144"><em>EnableSync </em> 매개 변수를 사용 하 여 활성화 하거나 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-145">컴퓨터에서 현재 사용자에 대 한 UE-V를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="25d90-146"><em>EnableSync </em> 매개 변수를 사용 하 여 활성화 하거나 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-147">컴퓨터의 모든 사용자에 대 한 알림 영역에서 UE-V 아이콘을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="25d90-148"><em>DisableTrayIcon </em> 매개 변수를 사용 하 여 아이콘을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-149">설정 패키지 파일 크기가 컴퓨터의 모든 사용자에 대해 정의 된 임계값에 도달 하는 경우 UE-V agent가 보고 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="25d90-150">임계값 패키지 크기 (바이트)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-151">설정 패키지 파일 크기가 정의 된 임계값에 도달할 때이를 보고 하도록 UE-V agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="25d90-152">현재 사용자에 대 한 패키지 크기 경고 임계값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-153">사용자가 컴퓨터의 모든 사용자에 게 알림을 보내기 전의 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-154">현재 사용자에 대 한 알림을 보내는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-155">컴퓨터의 모든 사용자에 대 한 컴퓨터별 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-156">사용자별 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-157">컴퓨터의 모든 사용자에 대 한 설정 템플릿 카탈로그 경로를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-158">컴퓨터의 모든 사용자에 대 한 동기화 방법 (SyncProvider 또는 없음)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-159">현재 사용자: SyncProvider 또는 없음에 대 한 동기화 방법을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-160">컴퓨터의 모든 사용자에 대 한 동기화 시간 초과 (밀리초)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-161">현재 사용자에 대 한 동기화 시간 초과 설정</span><span class="sxs-lookup"><span data-stu-id="25d90-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-162">컴퓨터의 모든 사용자에 대해 지정 된 설정을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-163">현재 사용자에 대해서만 지정 된 설정을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-164">UE-V 컴퓨터 구성을 설정 마이그레이션 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="25d90-165">파일 이름 확장명은 uev 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="25d90-166"><code>Export</code>Cmdlet은 <em> 컴퓨터 매개 변수를 사용 하 여 구성할 수 있는 모든 ue-v agent 설정을 내보냅니다 </em> .</span><span class="sxs-lookup"><span data-stu-id="25d90-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="25d90-167">설정 마이그레이션 파일에서 UE-V 컴퓨터 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="25d90-168">파일 이름 확장명은 uev 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="25d90-169">Windows PowerShell을 사용 하 여 UE-V 패키지 설정을 내보내고 UE-V 템플릿을 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="25d90-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="25d90-170">Windows PowerShell 창을 관리자로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="25d90-171">다음 Windows PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="25d90-172">Windows PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="25d90-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="25d90-173">설명</span><span class="sxs-lookup"><span data-stu-id="25d90-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="25d90-174">Export-UevPackage MicrosoftCalculator6.</span><span class="sxs-lookup"><span data-stu-id="25d90-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25d90-175">Microsoft 계산기 패키지 파일에서 설정을 추출 하 여 XML에서 사람이 읽을 수 있는 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="25d90-176">복구-Uev서식 색인</span><span class="sxs-lookup"><span data-stu-id="25d90-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25d90-177">UE-V 설정 위치 템플릿의 인덱스를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="25d90-178">WMI를 사용 하 여 UE-V 에이전트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="25d90-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="25d90-179">사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="25d90-180">관리자는이 인터페이스를 사용 하 여 명령줄에서 UE-V agent를 구성 하 고 일반적인 구성 작업을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="25d90-181">관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="25d90-182">다음 WMI 명령을 사용 하 여 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="25d90-183">설명</span><span class="sxs-lookup"><span data-stu-id="25d90-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="25d90-184">활성 UE-V Agent 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="25d90-185">사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-186">사용자에 대해 정의 된 UE-V Agent 구성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-187">컴퓨터에 대해 정의 된 UE-V Agent 구성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-188">각 구성 항목에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="25d90-189">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="25d90-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="25d90-190">컴퓨터당 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-191">사용자별 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-192">컴퓨터의 모든 사용자에 대 한 동기화 시간 초과 (밀리초)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-193">설정 패키지 파일 크기가 정의 된 임계값에 도달할 때이를 보고 하도록 UE-V Agent를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="25d90-194">컴퓨터의 모든 사용자에 대 한 임계값 패키지 파일 크기 (바이트)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-195">컴퓨터의 모든 사용자에 대 한 동기화 방법 (SyncProvider 또는 없음)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-196">특정 컴퓨터별 설정을 사용 하도록 설정 하려면 설정을 지우고 <em> $null를 </em> 설정 값으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="25d90-197">사용자 단위 설정에 UserConfiguration을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-198">특정 컴퓨터별 설정을 사용 하지 않도록 설정 하려면 설정을 지우고 <em> $null를 </em> 설정 값으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="25d90-199">사용자별 설정에 대해 사용자 구성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-200">컴퓨터 별로 특정 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="25d90-201">설정을 지우려면 <em> </em> 설정 값으로 $null를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="25d90-202">$config. &lt; 설정 이름 &gt;  =  &lt; 설정 값&gt;</span><span class="sxs-lookup"><span data-stu-id="25d90-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-203">컴퓨터의 모든 사용자에 대해 특정 사용자별 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="25d90-204">설정을 지우려면 <em> </em> 설정 값으로 $null를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="25d90-205">WMI를 사용 하 여 UE-V 패키지 설정을 내보내고 UE-V 서식 파일을 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="25d90-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="25d90-206">UE-V는 다음과 같은 WMI 명령 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="25d90-207">관리자는이 인터페이스를 사용 하 여 패키지를 내보내거나 UE-V 템플릿을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="25d90-208">다음 WMI 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="25d90-209">WMI 명령</span><span class="sxs-lookup"><span data-stu-id="25d90-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="25d90-210">설명</span><span class="sxs-lookup"><span data-stu-id="25d90-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-211">패키지 파일에서 설정을 추출 하 여 XML에서 사람이 읽을 수 있는 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="25d90-212">UE-V 설정 위치 템플릿의 인덱스를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="25d90-213">관리자 권한으로 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25d90-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="25d90-214">관련 항목</span><span class="sxs-lookup"><span data-stu-id="25d90-214">Related topics</span></span>


[<span data-ttu-id="25d90-215">Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="25d90-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="25d90-216">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="25d90-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









