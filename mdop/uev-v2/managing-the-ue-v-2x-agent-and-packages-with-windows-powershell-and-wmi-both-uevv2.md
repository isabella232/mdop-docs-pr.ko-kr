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
# Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 에이전트 및 패키지 관리


WMI (Windows Management Instrumentation) 및 Windows PowerShell을 사용 하 여 Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1 에이전트 구성 및 동기화 동작을 관리할 수 있습니다. UE-V PowerShell cmdlet의 전체 목록은 [ue-v 2 Cmdlet 참조](https://go.microsoft.com/fwlink/?LinkId=393495) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=393495) .

**Windows PowerShell을 사용 하 여 UE-V 에이전트를 배포 하려면**

1.  액세스 가능한 네트워크 공유에서 UE-V 설치 관리자 파일을 준비 합니다.

    **참고**  
    AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다. 각 아키텍처에 대해 Windows Installer 패키지, AgentSetupx86.msi 및 AgentSetupx64.msi를 사용할 수 있습니다. 나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.



2.  다음 Windows PowerShell 명령 중 하나를 사용 하 여 UE-V 에이전트를 설치 합니다.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Windows PowerShell을 사용 하 여 UE-V 에이전트를 구성 하려면**

1. Windows PowerShell 창을 엽니다. *컴퓨터 매개 변수* 를 사용 하 여 컴퓨터의 모든 사용자에 게 영향을 주는 컴퓨터 설정을 관리 하려면 관리자 권한이 있는 계정을 사용 하 여 창을 엽니다.

2. 다음 Windows PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Windows PowerShell 명령</th>
   <th align="left">설명</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>유효한 UE-V Agent 설정을 가져옵니다. 사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>현재 사용자에 대해서만 UE-V 에이전트 설정 값을 가져옵니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대 한 UE-V 에이전트 구성 설정 값을 가져옵니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>각 구성 설정에 대 한 세부 정보를 가져옵니다. 설정이 구성 된 위치를 표시 하거나 기본값을 사용 합니다. 현재 설정이 유효한 경우 표시 됩니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>도움말 링크에 대 한 회사 설정 센터에 표시 되는 텍스트를 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>도움말 링크에 대 한 회사 설정 센터의 링크에 대 한 URL을 설정 합니다. 모든 URL 프로토콜을 사용할 수 있습니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대해 Windows 앱을 동기화 하지 않도록 UE-V Agent를 구성 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>현재 컴퓨터 사용자에 대 한 Windows 앱을 동기화 하지 않도록 UE-V Agent를 구성 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자가 처음으로 에이전트를 실행할 때 UE-V Agent에서 알림을 표시 하도록 구성 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자가 처음으로 에이전트를 실행할 때 UE-V Agent가 알림을 표시 하지 않도록 구성 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>설정 동기화가 지연 될 때 UE-V Agent를 구성 하 여 컴퓨터의 모든 사용자에 게 알립니다.</p>
   <p><em>DisableSettingsImportNotify </em> 매개 변수를 사용 하 여 알림을 사용 하지 않도록 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>설정 동기화가 지연 될 때 현재 사용자에 게 알리기 위해 UE-V Agent를 구성 합니다.</p>
   <p><em>DisableSettingsImportNotify </em> 매개 변수를 사용 하 여 알림을 사용 하지 않도록 설정 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대해 Windows 앱 목록에서 명시적으로 사용 하지 않도록 설정 하지 않은 모든 Windows 앱을 동기화 하도록 UE-V Agent를 구성 합니다. 자세한 내용은 &quot; &quot; <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> WINDOWS PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿을 관리 UevAppxPackage을 참조 하세요 </a> .</p>
   <p><em>DisableSyncUnlistedWindows8Apps </em> 매개 변수를 사용 하 여 Windows 앱 목록에서 명시적으로 사용 하도록 설정 된 windows 앱만 동기화 하도록 ue-v agent를 구성 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>컴퓨터의 현재 사용자에 대해 Windows 앱 목록에서 명시적으로 사용 하지 않도록 설정 되지 않은 모든 Windows 앱을 동기화 하도록 UE-V Agent를 구성 합니다. 자세한 내용은 &quot; &quot; <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> WINDOWS PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿을 관리 UevAppxPackage을 참조 하세요 </a> .</p>
   <p><em>DisableSyncUnlistedWindows8Apps </em> 매개 변수를 사용 하 여 Windows 앱 목록에서 명시적으로 사용 하도록 설정 된 windows 앱만 동기화 하도록 ue-v agent를 구성 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대해 UE-V를 사용 하지 않도록 설정 합니다.</p>
   <p><em>EnableSync </em> 매개 변수를 사용 하 여 활성화 하거나 다시 사용 하도록 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>컴퓨터에서 현재 사용자에 대 한 UE-V를 사용 하지 않도록 설정 합니다.</p>
   <p><em>EnableSync </em> 매개 변수를 사용 하 여 활성화 하거나 다시 사용 하도록 설정 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대 한 알림 영역에서 UE-V 아이콘을 사용 하도록 설정 합니다.</p>
   <p><em>DisableTrayIcon </em> 매개 변수를 사용 하 여 아이콘을 사용 하지 않도록 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>설정 패키지 파일 크기가 컴퓨터의 모든 사용자에 대해 정의 된 임계값에 도달 하는 경우 UE-V agent가 보고 하도록 구성 합니다. 임계값 패키지 크기 (바이트)를 설정 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>설정 패키지 파일 크기가 정의 된 임계값에 도달할 때이를 보고 하도록 UE-V agent를 구성 합니다. 현재 사용자에 대 한 패키지 크기 경고 임계값을 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>사용자가 컴퓨터의 모든 사용자에 게 알림을 보내기 전의 시간 (초)을 지정 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>현재 사용자에 대 한 알림을 보내는 시간 (초)을 지정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대 한 컴퓨터별 설정 저장소 위치를 정의 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>사용자별 설정 저장소 위치를 정의 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대 한 설정 템플릿 카탈로그 경로를 설정 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대 한 동기화 방법 (SyncProvider 또는 없음)을 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>현재 사용자: SyncProvider 또는 없음에 대 한 동기화 방법을 설정 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대 한 동기화 시간 초과 (밀리초)를 설정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>현재 사용자에 대 한 동기화 시간 초과 설정</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>컴퓨터의 모든 사용자에 대해 지정 된 설정을 지웁니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>현재 사용자에 대해서만 지정 된 설정을 지웁니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>UE-V 컴퓨터 구성을 설정 마이그레이션 파일로 내보냅니다. 파일 이름 확장명은 uev 이어야 합니다.</p>
   <p><code>Export</code>Cmdlet은 <em> 컴퓨터 매개 변수를 사용 하 여 구성할 수 있는 모든 ue-v agent 설정을 내보냅니다 </em> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>설정 마이그레이션 파일에서 UE-V 컴퓨터 구성을 가져옵니다. 파일 이름 확장명은 uev 이어야 합니다.</p></td>
   </tr>
   </tbody>
   </table>



**Windows PowerShell을 사용 하 여 UE-V 패키지 설정을 내보내고 UE-V 템플릿을 복구 하려면**

1.  Windows PowerShell 창을 관리자로 엽니다.

2.  다음 Windows PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Windows PowerShell 명령</strong></p></td>
    <td align="left"><p><strong>설명</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6.</p></td>
    <td align="left"><p>Microsoft 계산기 패키지 파일에서 설정을 추출 하 여 XML에서 사람이 읽을 수 있는 형식으로 변환 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>복구-Uev서식 색인</p></td>
    <td align="left"><p>UE-V 설정 위치 템플릿의 인덱스를 복구 합니다.</p></td>
    </tr>
    </tbody>
    </table>



**WMI를 사용 하 여 UE-V 에이전트를 구성 하려면**

1.  사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다. 관리자는이 인터페이스를 사용 하 여 명령줄에서 UE-V agent를 구성 하 고 일반적인 구성 작업을 자동화할 수 있습니다.

    관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.

2.  다음 WMI 명령을 사용 하 여 에이전트를 구성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>활성 UE-V Agent 설정을 표시 합니다. 사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>사용자에 대해 정의 된 UE-V Agent 구성을 표시 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>컴퓨터에 대해 정의 된 UE-V Agent 구성을 표시 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>각 구성 항목에 대 한 세부 정보를 표시 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>컴퓨터당 설정 저장소 위치를 정의 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>사용자별 설정 저장소 위치를 정의 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>컴퓨터의 모든 사용자에 대 한 동기화 시간 초과 (밀리초)를 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>설정 패키지 파일 크기가 정의 된 임계값에 도달할 때이를 보고 하도록 UE-V Agent를 구성 합니다. 컴퓨터의 모든 사용자에 대 한 임계값 패키지 파일 크기 (바이트)를 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>컴퓨터의 모든 사용자에 대 한 동기화 방법 (SyncProvider 또는 없음)을 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>특정 컴퓨터별 설정을 사용 하도록 설정 하려면 설정을 지우고 <em> $null를 </em> 설정 값으로 사용 합니다. 사용자 단위 설정에 UserConfiguration을 사용 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>특정 컴퓨터별 설정을 사용 하지 않도록 설정 하려면 설정을 지우고 <em> $null를 </em> 설정 값으로 사용 합니다. 사용자별 설정에 대해 사용자 구성을 사용 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>컴퓨터 별로 특정 설정을 업데이트 합니다. 설정을 지우려면 <em> </em> 설정 값으로 $null를 사용 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; 설정 이름 &gt;  =  &lt; 설정 값&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>컴퓨터의 모든 사용자에 대해 특정 사용자별 설정을 업데이트 합니다. 설정을 지우려면 <em> </em> 설정 값으로 $null를 사용 합니다.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**WMI를 사용 하 여 UE-V 패키지 설정을 내보내고 UE-V 서식 파일을 복구 하려면**

1.  UE-V는 다음과 같은 WMI 명령 집합을 제공 합니다. 관리자는이 인터페이스를 사용 하 여 패키지를 내보내거나 UE-V 템플릿을 복구할 수 있습니다.

2.  다음 WMI 명령을 사용 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">WMI 명령</th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>패키지 파일에서 설정을 추출 하 여 XML에서 사람이 읽을 수 있는 형식으로 변환 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>UE-V 설정 위치 템플릿의 인덱스를 복구 합니다. 관리자 권한으로 실행 해야 합니다.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## 관련 항목


[Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)









