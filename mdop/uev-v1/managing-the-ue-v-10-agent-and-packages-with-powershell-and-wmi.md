---
title: PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리
description: PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819298"
---
# <span data-ttu-id="1c577-103">PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리</span><span class="sxs-lookup"><span data-stu-id="1c577-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="1c577-104">WMI 및 PowerShell을 사용 하 여 Microsoft UE-V (User Experience Virtualization) 에이전트 구성 및 동기화 동작을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="1c577-105">PowerShell을 사용 하 여 UE-V 에이전트를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1c577-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="1c577-106">액세스 가능한 네트워크 공유에서 UE-V 설치 관리자 파일을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="1c577-107">참고</span><span class="sxs-lookup"><span data-stu-id="1c577-107">Note</span></span>**  
    <span data-ttu-id="1c577-108">AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="1c577-109">각 아키텍처에 대해 Windows Installer 파일 버전, AgentSetupx86.msi 및 AgentSetupx64.msi를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="1c577-110">나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="1c577-111">다음 PowerShell 명령 중 하나를 사용 하 여 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="1c577-112">PowerShell을 사용 하 여 UE-V 에이전트를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1c577-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="1c577-113">관리자 권한이 있는 계정을 사용 하 여 PowerShell 창을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="1c577-114">다음 명령을 사용 하 여 UE-V PowerShell 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="1c577-115">다음 PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="1c577-116">PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="1c577-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="1c577-117">설명</span><span class="sxs-lookup"><span data-stu-id="1c577-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-118">Get UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="1c577-119">유효한 UE-V agent 설정을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="1c577-120">사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-121">Get UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="1c577-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="1c577-122">현재 사용자에 대해서만 UE-V agent 설정 값을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-123">Get UevConfiguration-컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1c577-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-124">컴퓨터의 모든 사용자에 대 한 UE-V 에이전트 구성 설정 값을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-125">UevConfiguration-Computer-SettingsStoragePath &lt; 경로를 _settings_storage_location로 설정&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-126">컴퓨터당 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-127">UevConfiguration-CurrentComputerUser- &lt; settings_settings_storage_location에 대 한 Storagepath 경로를 설정 합니다.&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-128">사용자별 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-129">UevConfiguration-컴퓨터-SyncTimeoutInMilliseconds &lt; 제한 시간 (밀리초)&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-130">동기화 시간 제한을 밀리초로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-131">UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; timeout in 밀리초&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-132">현재 사용자에 대 한 동기화 시간 제한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-133">UevConfiguration-컴퓨터 MaxPackageSizeInBytes &lt; 크기 (바이트)&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-134">설정 패키지 파일 크기가 정의 된 임계값에 도달 하는 경우 UE-V agent가 보고 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="1c577-135">임계값 패키지 크기 (바이트)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-136">UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; size (바이트)&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-137">현재 사용자에 대 한 패키지 크기 경고 임계값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-138">UevConfiguration – Computer-SettingsTemplateCatalogPath &lt; 경로를 카탈로그에 설정&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-139">설정 서식 파일 카탈로그 경로를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-140">UevConfiguration-컴퓨터 SyncMethod &lt; 동기화 방법&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-141">동기화 방법 (안 함 파일 또는 없음)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-142">UevConfiguration-CurrentComputerUser-SyncMethod &lt; sync 메서드&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-143">현재 사용자:가 중 파일 또는 없음에 대 한 동기화 방법을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-144">UEVConfiguration-컴퓨터-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="1c577-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-145">사용자 설정 가져오기가 지연 되는 경우 알림이 발생 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="1c577-146">알림 기능을 사용 하지 않으려면 – DisableSettingsImportNotify를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-147">UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="1c577-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-148">사용자 설정 가져오기가 지연 되는 경우 현재 사용자에 대 한 알림을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="1c577-149">알림 기능을 사용 하지 않으려면 – DisableSettingsImportNotify를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-150">UEVConfiguration-컴퓨터 SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="1c577-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-151">사용자에 게 알림을 보내기 전의 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-152">UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="1c577-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-153">현재 사용자에 대 한 알림 전의 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-154">UevConfiguration – 컴퓨터-DisableSync</span><span class="sxs-lookup"><span data-stu-id="1c577-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-155">컴퓨터의 모든 사용자에 대해 UE-V를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="1c577-156">– EnableSync를 사용 하 여 설정 하거나 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-157">UevConfiguration – CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="1c577-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-158">컴퓨터에서 현재 사용자에 대해 UE-V를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="1c577-159">– EnableSync를 사용 하 여 설정 하거나 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-160">일반-UevConfiguration-컴퓨터 &lt; 설정 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-161">컴퓨터의 모든 사용자에 대 한 특정 설정을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-162">일반-UevConfiguration – CurrentComputerUser- &lt; 설정 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-163">현재 사용자에 대해서만 특정 설정의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-164">내보내기-UevConfiguration &lt; 설정 마이그레이션 파일&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-165">UE-V 컴퓨터 구성을 설정 마이그레이션 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="1c577-166">파일 확장명은 "uev" 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="1c577-167">Export cmdlet은-computer 매개 변수를 사용 하 여 구성할 수 있는 모든 UE-V agent 설정을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-168">가져오기-UevConfiguration &lt; 설정 마이그레이션 파일&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-169">설정 마이그레이션 파일 (uev 파일)에서 UE-V 컴퓨터 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="1c577-170">UE-V 패키지 설정을 내보내고 PowerShell을 사용 하 여 UE-V 템플릿을 복구 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1c577-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="1c577-171">관리자 권한으로 PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="1c577-172">다음 명령을 사용 하 여 UE-V PowerShell 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="1c577-173">다음 PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="1c577-174">PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="1c577-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="1c577-175">설명</span><span class="sxs-lookup"><span data-stu-id="1c577-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-176">Export-UevPackage MicrosoftCalculator6.</span><span class="sxs-lookup"><span data-stu-id="1c577-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-177">Microsoft 계산기 패키지 파일에서 설정을 추출 하 여 XML에서 사람이 읽을 수 있는 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-178">복구-Uev서식 색인</span><span class="sxs-lookup"><span data-stu-id="1c577-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-179">UE-V 설정 위치 템플릿의 인덱스를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="1c577-180">WMI를 사용 하 여 UE-V 에이전트를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1c577-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="1c577-181">사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="1c577-182">관리자는이 인터페이스를 사용 하 여 명령줄에서 UE-V agent를 구성 하 고 일반적인 구성 작업을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="1c577-183">관리자 권한이 있는 계정을 사용 하 여 PowerShell 창을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="1c577-184">다음 WMI 명령을 사용 하 여 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="1c577-185">PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="1c577-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="1c577-186">설명</span><span class="sxs-lookup"><span data-stu-id="1c577-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-187">WmiObject-네임 스페이스 root\Microsoft\UEV 구성</span><span class="sxs-lookup"><span data-stu-id="1c577-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="1c577-188">활성 UE-V agent 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="1c577-189">사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-190">WmiObject-네임 스페이스 root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-191">사용자에 대해 정의 된 UE-V agent 구성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-192">WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-193">컴퓨터에 대해 정의 된 UE-V agent 구성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-194">$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="1c577-196">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-197">컴퓨터당 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-198">$config = WmiObject-네임 스페이스 root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="1c577-200">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-201">사용자별 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-202">$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="1c577-204">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-205">동기화 시간 제한을 밀리초로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-206">$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="1c577-208">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-209">설정 패키지 파일 크기가 정의 된 임계값에 도달 하는 경우 UE-V agent가 보고 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="1c577-210">임계값 패키지 파일 크기 (바이트)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-211">$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-212">$config. SyncMethod = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="1c577-213">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-214">동기화 방법 (안 함 파일 또는 없음)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1c577-215">$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-216">$config. &lt; 설정 이름 &gt;  =  &lt; 설정 값&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="1c577-217">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-218">특정 컴퓨터 별로 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="1c577-219">설정을 지우려면 설정 값으로 $null를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1c577-220">$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c577-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="1c577-221">$config. &lt; 설정 이름 &gt;  =  &lt; 설정 값&gt;</span><span class="sxs-lookup"><span data-stu-id="1c577-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="1c577-222">$config. 올리기 ()</span><span class="sxs-lookup"><span data-stu-id="1c577-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1c577-223">특정 사용자별 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-223">Update a specific per-user setting.</span></span> <span data-ttu-id="1c577-224">설정을 지우려면 설정 값으로 $null를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c577-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="1c577-225">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1c577-225">Related topics</span></span>


[<span data-ttu-id="1c577-226">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="1c577-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="1c577-227">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="1c577-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









