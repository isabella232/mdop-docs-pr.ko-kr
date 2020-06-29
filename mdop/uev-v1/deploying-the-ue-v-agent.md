---
title: UE-V 에이전트 배포
description: UE-V 에이전트 배포
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827183"
---
# <span data-ttu-id="a3a12-103">UE-V 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="a3a12-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="a3a12-104">Microsoft UE-V (User Experience Virtualization) 에이전트는 UE-V를 사용 하 여 응용 프로그램 및 Windows 설정을 로밍 하는 각 컴퓨터에서 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="a3a12-105">AgentSetup.exe 단일 설치 관리자 파일은 32 비트 및 64 비트 운영 체제에 모두 UE-V agent를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="a3a12-106">UE-V 에이전트의 명령줄 매개 변수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="a3a12-107">명령줄 매개 변수 AgentSetup.exe</span><span class="sxs-lookup"><span data-stu-id="a3a12-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="a3a12-108">명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3a12-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3a12-109">정의</span><span class="sxs-lookup"><span data-stu-id="a3a12-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3a12-110">참고</span><span class="sxs-lookup"><span data-stu-id="a3a12-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-111">/help 또는/h 또는/?</span><span class="sxs-lookup"><span data-stu-id="a3a12-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-112">AgentSetup.exe 사용 대화 상자를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3a12-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="a3a12-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-114">설정이 저장 되는 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-115">% username% 또는% computername% 환경 변수를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="a3a12-116">스크립팅에는 이스케이프 된 변수가 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="a3a12-117">기본값 </strong> : &lt; 없음 &gt; (Active Directory 사용자 홈)</span><span class="sxs-lookup"><span data-stu-id="a3a12-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="a3a12-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-119">새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-120">사용자 지정 설정 위치 서식 파일에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3a12-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="a3a12-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-122">설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-123">True | 해제</span><span class="sxs-lookup"><span data-stu-id="a3a12-123">True | False</span></span></p>
<p><strong><span data-ttu-id="a3a12-124">기본값 </strong> : True</span><span class="sxs-lookup"><span data-stu-id="a3a12-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-125">Powerschool</span><span class="sxs-lookup"><span data-stu-id="a3a12-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-126">사용할 동기화 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-127">기타 파일 | 않아야</span><span class="sxs-lookup"><span data-stu-id="a3a12-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="a3a12-128">기본값 </strong> :가 중 파일</span><span class="sxs-lookup"><span data-stu-id="a3a12-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3a12-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="a3a12-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-130">컴퓨터가 설정 저장소 위치에서 사용자 설정을 검색할 때 시간 초과 전에 대기 하는 밀리초 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a3a12-131">기본값 </strong> : 2000 밀리초</span><span class="sxs-lookup"><span data-stu-id="a3a12-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="a3a12-132">(2 초까지 대기)</span><span class="sxs-lookup"><span data-stu-id="a3a12-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="a3a12-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-134">UE-V 동기화를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-135">True | 해제</span><span class="sxs-lookup"><span data-stu-id="a3a12-135">True | False</span></span></p>
<p><strong><span data-ttu-id="a3a12-136">기본값 </strong> : True</span><span class="sxs-lookup"><span data-stu-id="a3a12-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3a12-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a3a12-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-138">UE-V agent가 해당 파일이 임계값을 초과 하는 것으로 보고할 때 설정 패키지 파일 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-139">&lt;크기&gt;</span><span class="sxs-lookup"><span data-stu-id="a3a12-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="a3a12-140">기본값 </strong> : 없음 (경고 임계값 없음)</span><span class="sxs-lookup"><span data-stu-id="a3a12-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="a3a12-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-142">사용자 환경 개선 프로그램의 참여에 대 한 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="a3a12-143">True로 설정 하면 설치 관리자 정보가 Microsoft 사용자 환경 개선 프로그램 사이트에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="a3a12-144">False로 설정 된 경우 정보는 업로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-145">True | 해제</span><span class="sxs-lookup"><span data-stu-id="a3a12-145">True | False</span></span></p>
<p><strong><span data-ttu-id="a3a12-146">기본값 </strong> : False</span><span class="sxs-lookup"><span data-stu-id="a3a12-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="a3a12-147">Windows 7 </strong> : True</span><span class="sxs-lookup"><span data-stu-id="a3a12-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a3a12-148">설치 하는 동안 SettingsStoragePath 명령줄 매개 변수는 설정 값에 대 한 설정 저장소 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="a3a12-149">UE-V 에이전트를 배포 하기 전에 설정 저장소 위치를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="a3a12-150">설정 저장소 위치가 정의 되지 않은 경우 UE-V-V는 Active Directory 사용자 홈 디렉터리를 설정 저장소 위치로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="a3a12-151">설치 중에 SettingsStoragePath 구성을 지정 하 고 값의 일부로% username%을 (를) 사용 하는 경우,이는 사용자가 로그인 하는 모든 컴퓨터 또는 세션의 동일한 사용자 설정 환경을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="a3a12-152">SettingsStoragePath 값의 일부로%username%\\%computername% 변수를 지정 하면 각 컴퓨터에 대 한 설정 환경이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="a3a12-153">32 비트 및 64 비트 설치 프로그램 외에도 UE-V 에이전트 설치에 대 한 아키텍처 관련 Windows Installer (.msi) 파일이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="a3a12-154">AgentSetupx86.msi 또는 AgentSetupx64.msi 설치 파일은 AgentSetup.exe 파일 보다 작으며 에이전트 배포를 간소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="a3a12-155">AgentSetup.exe 설치 관리자의 명령줄 매개 변수는 Windows Installer (.msi) 설치에 대해 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="a3a12-156">**참고**  UE-V 에이전트 설치 또는 제거 중에 AgentSetup.exe 파일 또는 AgentSetup &lt; 아치 &gt; .msi 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="a3a12-157">Ue-v 에이전트를 설치 하는 데 사용 된 것과 동일한 파일을 사용 하 여 UE-V Agent를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="a3a12-158">UE-V 에이전트를 설치할 때 올바른 변수 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="a3a12-159">다음 표에서는 AgentSetup.exe 또는 Windows Installer (.msi) 설치 파일을 사용 하는 배포 옵션의 예를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="a3a12-160">배포 유형</span><span class="sxs-lookup"><span data-stu-id="a3a12-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3a12-161">배포 설명</span><span class="sxs-lookup"><span data-stu-id="a3a12-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3a12-162">예</span><span class="sxs-lookup"><span data-stu-id="a3a12-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-163">명령 프롬프트</span><span class="sxs-lookup"><span data-stu-id="a3a12-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-164">명령 프롬프트에서 UE-V agent를 설치 하는 경우% ^ username% 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="a3a12-165">설정 저장소 경로의 공간 때문에 인용 부호가 필요한 경우 배포용 배치 스크립트 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3a12-166">일괄 처리 스크립트</span><span class="sxs-lookup"><span data-stu-id="a3a12-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-167">배치 스크립트 파일에서 UE-V 에이전트를 설치 하는 경우%% username%% 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="a3a12-168">이 설치 방법을 사용 하는 경우%% 문자로 변수를 이스케이프 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="a3a12-169">이 문자가 없으면 스크립트는 설치 시에 런타임 대신 사용자 이름 변수를 확장 하 여 UE-V가 모든 사용자에 대해 단일 설정 저장소 위치를 사용 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3a12-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3a12-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-171">PowerShell 프롬프트 또는 PowerShell 스크립트에서 UE-V agent를 설치 하는 경우% username% 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3a12-172">전자 소프트웨어 배포 (예: Configuration Manager 소프트웨어 배포 배포)</span><span class="sxs-lookup"><span data-stu-id="a3a12-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3a12-173">구성 관리자를 사용 하 여 UE-V Agent를 설치 하는 경우 ^% username ^% 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a3a12-174">**참고**  U-EV 에이전트 설치에는 관리자 권한이 필요 하며, 컴퓨터를 다시 시작 해야 UE-V agent를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="a3a12-175">네트워크 공유의 UE-V Agent 배포 방법</span><span class="sxs-lookup"><span data-stu-id="a3a12-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="a3a12-176">다음 메서드를 사용 하 여 UE-V 에이전트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="a3a12-177">Windows Installer (.msi) 파일을 설치할 수 있는 ESD (전자 소프트웨어 배포) 솔루션입니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="a3a12-178">공유에 중앙에 저장 된 Windows Installer (.msi) 파일을 참조 하는 설치 스크립트입니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="a3a12-179">컴퓨터에서 설치 프로그램을 수동으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="a3a12-180">네트워크 공유에서 UE-V agent를 배포 하려면 다음 단계를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="a3a12-181">네트워크 공유에서 UE-V Agent를 설치 하 고 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="a3a12-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="a3a12-182">사용자에 게 "읽기" 권한이 있는 네트워크 공유에서 UE-V agent 설치 파일 (AgentSetup.exe)을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="a3a12-183">UE-V agent를 설치 하는 사용자 컴퓨터에 스크립트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="a3a12-184">스크립트는 설정 저장소 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="a3a12-185">UE-V 에이전트 업데이트</span><span class="sxs-lookup"><span data-stu-id="a3a12-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="a3a12-186">UE-V 에이전트 소프트웨어에 대 한 업데이트는 Microsoft Update를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="a3a12-187">UE-V 에이전트 업그레이드 중에 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치 템플릿의 기본 그룹이 업데이트 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="a3a12-188">UE-V 에이전트 업데이트는 엔터프라이즈 소프트웨어 배포 (ESD) 인프라를 사용 하 여 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3a12-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="a3a12-189">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a3a12-189">Related topics</span></span>


[<span data-ttu-id="a3a12-190">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="a3a12-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="a3a12-191">UE-V 1.0에 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="a3a12-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="a3a12-192">UE-V 1.0에 대한 설정 저장소 위치 배포</span><span class="sxs-lookup"><span data-stu-id="a3a12-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="a3a12-193">UE-V 생성기 설치</span><span class="sxs-lookup"><span data-stu-id="a3a12-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="a3a12-194">사용자 환경 가상화 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="a3a12-194">Deploy the User Experience Virtualization Agent</span></span>
 

 





