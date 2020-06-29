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
# PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리


WMI 및 PowerShell을 사용 하 여 Microsoft UE-V (User Experience Virtualization) 에이전트 구성 및 동기화 동작을 관리할 수 있습니다.

**PowerShell을 사용 하 여 UE-V 에이전트를 배포 하는 방법**

1.  액세스 가능한 네트워크 공유에서 UE-V 설치 관리자 파일을 준비 합니다.

    **참고**  
    AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다. 각 아키텍처에 대해 Windows Installer 파일 버전, AgentSetupx86.msi 및 AgentSetupx64.msi를 사용할 수 있습니다. 나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.



2.  다음 PowerShell 명령 중 하나를 사용 하 여 에이전트를 설치 합니다.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**PowerShell을 사용 하 여 UE-V 에이전트를 구성 하는 방법**

1.  관리자 권한이 있는 계정을 사용 하 여 PowerShell 창을 열 수 있습니다. 다음 명령을 사용 하 여 UE-V PowerShell 모듈을 가져옵니다.

    ``` syntax
    Import-module UEV
    ```

2.  다음 PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>PowerShell 명령</strong></p></td>
    <td align="left"><p><strong>설명</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>유효한 UE-V agent 설정을 봅니다. 사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>현재 사용자에 대해서만 UE-V agent 설정 값을 봅니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get UevConfiguration-컴퓨터</p></td>
    <td align="left"><p>컴퓨터의 모든 사용자에 대 한 UE-V 에이전트 구성 설정 값을 봅니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration-Computer-SettingsStoragePath &lt; 경로를 _settings_storage_location로 설정&gt;</p></td>
    <td align="left"><p>컴퓨터당 설정 저장소 위치를 정의 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UevConfiguration-CurrentComputerUser- &lt; settings_settings_storage_location에 대 한 Storagepath 경로를 설정 합니다.&gt;</p></td>
    <td align="left"><p>사용자별 설정 저장소 위치를 정의 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration-컴퓨터-SyncTimeoutInMilliseconds &lt; 제한 시간 (밀리초)&gt;</p></td>
    <td align="left"><p>동기화 시간 제한을 밀리초로 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; timeout in 밀리초&gt;</p></td>
    <td align="left"><p>현재 사용자에 대 한 동기화 시간 제한을 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration-컴퓨터 MaxPackageSizeInBytes &lt; 크기 (바이트)&gt;</p></td>
    <td align="left"><p>설정 패키지 파일 크기가 정의 된 임계값에 도달 하는 경우 UE-V agent가 보고 하도록 구성 합니다. 임계값 패키지 크기 (바이트)를 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; size (바이트)&gt;</p></td>
    <td align="left"><p>현재 사용자에 대 한 패키지 크기 경고 임계값을 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration – Computer-SettingsTemplateCatalogPath &lt; 경로를 카탈로그에 설정&gt;</p></td>
    <td align="left"><p>설정 서식 파일 카탈로그 경로를 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UevConfiguration-컴퓨터 SyncMethod &lt; 동기화 방법&gt;</p></td>
    <td align="left"><p>동기화 방법 (안 함 파일 또는 없음)을 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration-CurrentComputerUser-SyncMethod &lt; sync 메서드&gt;</p></td>
    <td align="left"><p>현재 사용자:가 중 파일 또는 없음에 대 한 동기화 방법을 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UEVConfiguration-컴퓨터-EnableSettingsImportNotify</p></td>
    <td align="left"><p>사용자 설정 가져오기가 지연 되는 경우 알림이 발생 하도록 설정 합니다.</p>
    <p>알림 기능을 사용 하지 않으려면 – DisableSettingsImportNotify를 사용 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>사용자 설정 가져오기가 지연 되는 경우 현재 사용자에 대 한 알림을 사용 하도록 설정 합니다.</p>
    <p>알림 기능을 사용 하지 않으려면 – DisableSettingsImportNotify를 사용 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UEVConfiguration-컴퓨터 SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>사용자에 게 알림을 보내기 전의 시간 (초)을 지정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>현재 사용자에 대 한 알림 전의 시간 (초)을 지정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UevConfiguration – 컴퓨터-DisableSync</p></td>
    <td align="left"><p>컴퓨터의 모든 사용자에 대해 UE-V를 사용 하지 않도록 설정 합니다.</p>
    <p>– EnableSync를 사용 하 여 설정 하거나 다시 사용 하도록 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UevConfiguration – CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>컴퓨터에서 현재 사용자에 대해 UE-V를 사용 하지 않도록 설정 합니다.</p>
    <p>– EnableSync를 사용 하 여 설정 하거나 다시 사용 하도록 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>일반-UevConfiguration-컴퓨터 &lt; 설정 이름&gt;</p></td>
    <td align="left"><p>컴퓨터의 모든 사용자에 대 한 특정 설정을 지웁니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>일반-UevConfiguration – CurrentComputerUser- &lt; 설정 이름&gt;</p></td>
    <td align="left"><p>현재 사용자에 대해서만 특정 설정의 선택을 취소 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>내보내기-UevConfiguration &lt; 설정 마이그레이션 파일&gt;</p></td>
    <td align="left"><p>UE-V 컴퓨터 구성을 설정 마이그레이션 파일로 내보냅니다. 파일 확장명은 "uev" 이어야 합니다.</p>
    <p>Export cmdlet은-computer 매개 변수를 사용 하 여 구성할 수 있는 모든 UE-V agent 설정을 내보냅니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>가져오기-UevConfiguration &lt; 설정 마이그레이션 파일&gt;</p></td>
    <td align="left"><p>설정 마이그레이션 파일 (uev 파일)에서 UE-V 컴퓨터 구성을 가져옵니다.</p></td>
    </tr>
    </tbody>
    </table>



**UE-V 패키지 설정을 내보내고 PowerShell을 사용 하 여 UE-V 템플릿을 복구 하는 방법**

1.  관리자 권한으로 PowerShell 창을 엽니다. 다음 명령을 사용 하 여 UE-V PowerShell 모듈을 가져옵니다.

    ``` syntax
    Import-module UEV
    ```

2.  다음 PowerShell 명령을 사용 하 여 에이전트를 구성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>PowerShell 명령</strong></p></td>
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



**WMI를 사용 하 여 UE-V 에이전트를 구성 하는 방법**

1.  사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다. 관리자는이 인터페이스를 사용 하 여 명령줄에서 UE-V agent를 구성 하 고 일반적인 구성 작업을 자동화할 수 있습니다.

    관리자 권한이 있는 계정을 사용 하 여 PowerShell 창을 열 수 있습니다.

2.  다음 WMI 명령을 사용 하 여 에이전트를 구성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">PowerShell 명령</th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>WmiObject-네임 스페이스 root\Microsoft\UEV 구성</p>
    <p></p></td>
    <td align="left"><p>활성 UE-V agent 설정을 확인 합니다. 사용자 관련 설정이 컴퓨터 설정 보다 우선 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>WmiObject-네임 스페이스 root\Microsoft\UEV UserConfiguration</p></td>
    <td align="left"><p>사용자에 대해 정의 된 UE-V agent 구성을 봅니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>컴퓨터에 대해 정의 된 UE-V agent 구성을 봅니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>컴퓨터당 설정 저장소 위치를 정의 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV UserConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>사용자별 설정 저장소 위치를 정의 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>동기화 시간 제한을 밀리초로 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>설정 패키지 파일 크기가 정의 된 임계값에 도달 하는 경우 UE-V agent가 보고 하도록 구성 합니다. 임계값 패키지 파일 크기 (바이트)를 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncMethod = &lt; sync_method&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>동기화 방법 (안 함 파일 또는 없음)을 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; 설정 이름 &gt;  =  &lt; 설정 값&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>특정 컴퓨터 별로 설정을 업데이트 합니다. 설정을 지우려면 설정 값으로 $null를 사용 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = WmiObject-네임 스페이스 root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; 설정 이름 &gt;  =  &lt; 설정 값&gt;</p>
    <p>$config. 올리기 ()</p></td>
    <td align="left"><p>특정 사용자별 설정을 업데이트 합니다. 설정을 지우려면 설정 값으로 $null를 사용 합니다.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## 관련 항목


[UE-V 1.0 관리](administering-ue-v-10.md)

[UE-V 1.0 작업](operations-for-ue-v-10.md)









