---
title: UE-V 2.x에 대한 필수 기능 배포
description: UE-V 2.x에 대한 필수 기능 배포
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824668"
---
# UE-V 2.x에 대한 필수 기능 배포


모든 Microsoft UE-V (사용자 환경 가상화) 2.0, 2.1 및 2.1 SP1 배포에는 다음 기능이 필요 합니다.

-   최종 사용자가 액세스할 수 있는 [설정 저장소 위치를 배포](#ssl) 합니다.

    사용자 설정을 저장 하 고 검색 하는 표준 네트워크 공유입니다.

-   [UE-V에 대 한 구성 방법 선택](#config)

    UE-V는 그룹 정책, 구성 관리자 또는 Windows 관리 인프라 및 Powershell을 비롯 한 일반적인 관리 도구를 사용 하 여 배포 및 구성할 수 있습니다.

-   설정을 동기화 하는 모든 컴퓨터에 설치할 [Ue-v agent를 배포](#agent) 합니다.

    이는 등록 된 응용 프로그램 및 운영 체제를 모니터링 하 여 설정을 변경 하 고 컴퓨터 간에 해당 설정을 동기화 합니다.

이 섹션의 항목에서는 이러한 기능을 배포 하는 방법에 대해 설명 합니다.

## <a href="" id="ssl"></a>UE-V 설정 저장소 위치 배포


UE-V를 사용 하려면 설정 패키지 파일에 사용자 설정을 저장할 위치가 필요 합니다. 다음 방법 중 하나를 수행 하 여이 설정 저장소 위치를 구성할 수 있습니다.

-   자신만의 설정 저장소 위치 만들기

-   설정 저장소 위치에 기존 Active Directory 사용

설정 저장소 위치를 만들지 않으면 UE-V Agent가 기본적으로 AD (Active Directory)를 사용 합니다.

**참고**  
[성능 및 용량 계획](https://technet.microsoft.com/library/dn458932.aspx#capacity) 의 일환으로 네트워크 지연 문제를 줄이기 위해 사용자 컴퓨터가 있는 동일한 로컬 네트워크에 설정 저장소 위치를 만듭니다. 설정 저장소 위치에 대해 사용자 당 20mb의 디스크 공간을 사용 하는 것이 좋습니다.



### UE-V 설정 저장소 위치 만들기

설정 저장소 위치를 정의 하기 전에 공유에 설정을 저장 하는 사용자에 대 한 읽기/쓰기 권한을 사용 하 여 루트 디렉터리를 만들어야 합니다. UE-V Agent는이 루트 디렉터리 아래에 사용자 관련 폴더를 만듭니다.

설정 저장소 위치는 다음 방법 중 하나를 사용 하 여 구성할 수 있는 SettingsStoragePath 구성 옵션을 설정 하 여 정의 합니다.

-   명령줄 매개 변수 또는 일괄 처리 스크립트를 통해 [Ue-v 에이전트를 배포](#agent) 하는 경우

-   [그룹 정책](https://technet.microsoft.com/library/dn458893.aspx) 설정

-   UE-V 용 [System Center 구성 팩](https://technet.microsoft.com/library/dn458917.aspx) 사용

-   UE-V 에이전트를 설치한 후 [Windows PowerShell 또는 WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx) 를 사용 하는 경우

경로는 서버 및 공유의 UNC (범용 명명 규칙) 경로에 있어야 합니다. 예를 **\\\\Server\\Settingsshare\\**. 이 구성 옵션은 특정 동기화 시나리오를 사용 하도록 설정 하는 변수 사용을 지원 합니다. 예를 들어 `%username%\%computername%` 다음과 같은 시나리오에서 변수를 사용 하 여 최종 사용자 설정 환경을 유지할 수 있습니다.

-   엔터프라이즈에서 여러 물리적 컴퓨터를 사용 하는 최종 사용자

-   여러 최종 사용자가 사용 하는 Enterprise 컴퓨터

UE-V Agent는 `SettingsPackages` **Settingsstoragepath**의 구성 설정을 기반으로 명명 된 숨겨진 시스템 폴더를 사용 하 여 사용자 관련 설정 저장소 경로를 동적으로 만듭니다. 에이전트는 등록 된 UE-V 설정 위치 템플릿에서 정의한 대로이 위치에 대 한 설정을 읽고 씁니다.

**Ue-v 설정은 "마지막 쓰기 wins" 규칙에 따라 결정 됩니다.** 설정 저장소 위치가 여러 관리 컴퓨터를 사용 하는 사용자의 경우, 한 UE-V Agent가 다른 컴퓨터에서 실행 되는 에이전트와 독립적으로 설정 위치를 읽고 씁니다. 마지막으로 작성 한 설정 및 값은 다음 에이전트가 설정 저장소 위치에서 읽을 때 적용 되는 것입니다.

**설정 저장소 위치 배포:** 다음 단계에 따라 기존 Active Directory 서비스를 사용 하는 대신 설정 저장소 위치를 정의 합니다. 아래 표에 표시 된 것 처럼 설정 저장소 공유에 대 한 액세스 권한을 필요로 하는 사용자에 게 제한 해야 합니다.

**UE-V 네트워크 공유를 배포 하려면**

1.  UE-V 사용자에 대 한 새 보안 그룹을 만듭니다.

2.  UE-V 설정 패키지를 저장 하는 중앙 컴퓨터에서 새 폴더를 만든 다음이 폴더에 대 한 그룹 사용 권한을 사용 하 여 UE-V 사용자에 게 액세스 권한을 부여 합니다. UE-V를 지 원하는 관리자는이 공유 폴더에 대 한 사용 권한이 있어야 합니다.

3.  설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준 서버 메시지 블록) 사용 권한을 설정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>사용자 계정</strong></th>
    <th align="left"><strong>권장 되는 사용 권한</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>모두</p></td>
    <td align="left"><p>권한 없음</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UE-V 사용자의 보안 그룹</p></td>
    <td align="left"><p>모든 권한</p></td>
    </tr>
    </tbody>
    </table>



4.  설정 저장소 위치 폴더에 대해 다음 NTFS 파일 시스템 사용 권한을 설정 합니다.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>사용자 계정</strong></th>
    <th align="left"><strong>권장 되는 사용 권한</strong></th>
    <th align="left"><strong>Folder</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>만든이/소유자</p></td>
    <td align="left"><p>모든 권한</p></td>
    <td align="left"><p>하위 폴더 및 파일만</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UE-V 사용자의 보안 그룹</p></td>
    <td align="left"><p>폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</p></td>
    <td align="left"><p>이 폴더만</p></td>
    </tr>
    </tbody>
    </table>



이 구성을 사용 하면 UE-V Agent가 사용자 컨텍스트에서 실행 되는 동안 Settingspackage 폴더를 만들고 보호 하며, 설정 저장소에 대 한 폴더를 만들 수 있는 권한을 각 사용자에 게 부여 합니다. 다른 사용자가 액세스할 수 없는 동안 사용자는 자신의 Settingspackage 폴더에 대 한 모든 권한을 받습니다.

**참고**  
Windows Server 운영 체제를 실행 하는 컴퓨터에서 설정 저장소 공유를 만드는 경우 UE-V를 구성 하 여 로컬 관리자 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 합니다. 이 추가 보안을 사용 하도록 설정 하려면 Windows Server 레지스트리 편집기에서 다음 설정을 지정 합니다.

1.  **"RepositoryOwnerCheckEnabled"** 이라는 **REG \ _DWORD** 레지스트리 키를 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**에 추가 합니다.

2.  레지스트리 키 값을 *1*로 설정 합니다.



### UE-V를 사용 하 여 Active Directory/V 2. x 포함

설정 저장소 위치가 달리 정의 되지 않은 경우 UE-V Agent가 기본적으로 Active Directory (AD)를 사용 합니다. 이러한 경우 UE-V Agent가 각 사용자의 AD home 디렉터리 아래에서 동적으로 설정 저장소 폴더를 만듭니다. 그러나 AD에서 사용자 지정 디렉터리 설정이 구성 되어 있으면 해당 디렉터리가 대신 사용 됩니다.

## <a href="" id="config"></a>UE-V 2. x에 대 한 구성 방법을 선택 합니다.


이는 UE-V 에이전트를 배포 하는 데 사용 하는 구성 방법 이므로 배포 후 UE-V를 관리 하는 데 사용할 구성 방법을 알아내는 것입니다. 일반적으로이는 Windows PowerShell 또는 Configuration Manager와 같이 환경에서 이미 사용 하는 구성 방법입니다.

UE-V 에이전트를 설치 하기 전이나 설치한 후에는 사용 하는 구성 방법에 따라 UE-V를 구성할 수 있습니다.

-   [그룹 정책](https://technet.microsoft.com/library/dn458893.aspx)**:** 기존 그룹 정책 인프라를 사용 하 여 ue-v 에이전트 배포 전 또는 후에 ue-v를 구성할 수 있습니다. UE-V 그룹 정책 ADMX 서식 파일은 일반적인 UE-V 에이전트 구성 옵션의 중앙 관리를 가능 하 게 하며 UE-V 동기화를 구성 하는 설정을 포함 합니다.

    **Ue-v 그룹 정책 ADMX 템플릿 설치:** UE-V 용 그룹 정책 ADMX 템플릿은 UE-V 에이전트에 대 한 동기화 설정을 구성 하 고 기존 그룹 정책 인프라를 사용 하 여 일반적인 UE-V Agent 구성 설정의 중앙 관리를 사용 하도록 설정 합니다.

    그룹 정책 개체를 배포 하는 도메인 컨트롤러에 대해 지원 되는 운영 체제는 다음과 같습니다.

    Windows Server 2008 R2

    Windows Server 2012 및 Windows Server 2012 R2

-   [구성 관리자](https://technet.microsoft.com/library/dn458917.aspx)**:** ue-v 구성 팩을 사용 하면 System Center configuration Manager 2012 SP1 이상 버전의 규정 준수 설정 기능을 통해 ue-v 및 Configuration manager가 설치 된 사이트에서 일관 된 구성을 적용할 수 있습니다.

-   [Windows powershell 및 wmi](https://technet.microsoft.com/library/dn458937.aspx)**:** windows powershell 및 wmi (windows Management Instrumentation)에 대해 스크립팅된 명령을 사용 하 여 ue-v 에이전트를 설치한 후 구성을 수정할 수 있습니다.

    **참고**  
    레지스트리를 수정 하면 데이터가 손실 되거나 컴퓨터가 응답 하지 않을 수 있습니다. 다른 구성 메서드를 사용 하는 것이 좋습니다.



-   **명령줄 또는 배치 스크립트 설치:** [Ue-v 에이전트를 배포할](#agent) 때 사용 되는 매개 변수는 여러 ue-v 설정을 구성 합니다. System Center 2012 구성 관리자와 같은 전자 소프트웨어 배포 시스템에서는 이러한 매개 변수를 사용 하 여 UE-V 에이전트 소프트웨어를 배포 하 고 설치할 때 해당 클라이언트를 구성 합니다.

## <a href="" id="agent"></a>UE-V 2. x 에이전트 배포


UE-V Agent는 UE-V 배포의 핵심 이며 UE-V를 사용 하 여 응용 프로그램 및 Windows 설정을 동기화 하는 각 컴퓨터에서 실행 해야 합니다.

**Ue-v 에이전트 설치 파일:** AgentSetup.exe 단일 설치 파일은 32 비트 및 64 비트 운영 체제에 모두 UE-V Agent를 설치 합니다. 또한 AgentSetupx86.msi 또는 AgentSetupx64.msi 아키텍처 관련 Windows Installer 파일이 제공 되며,이는 크기가 작기 때문에 에이전트 배포를 단순화할 수 있습니다. Windows Installer 설치에도 [AgentSetup.exe 설치 관리자의 명령줄 매개 변수가](#params) 지원 됩니다.

**중요**  
UE-V 에이전트 설치 또는 제거 중에 AgentSetup.exe 파일 또는 AgentSetup &lt; 아치 &gt; .msi 파일을 사용할 수 있습니다. UE-V 에이전트를 설치 하는 데 사용 된 UE-V Agent를 제거 하려면 같은 파일을 사용 해야 합니다.



### UE-V 에이전트를 배포 하려면

다음 메서드를 사용 하 여 UE-V 에이전트를 배포할 수 있습니다.

-   Windows Installer (.msi) 파일을 설치할 수 있는 구성 관리자 등의 ESD (전자 소프트웨어 배포) 솔루션 시스템입니다.

-   공유에 중앙에 저장 된 Windows Installer (.msi) 파일을 참조 하는 설치 스크립트입니다.

-   컴퓨터에서 수동으로 실행 하는 설치 프로그램

네트워크 공유에서 UE-V Agent를 배포 하려면 다음 절차를 사용 합니다.

**네트워크 공유에서 UE-V Agent를 설치 하 고 구성 하려면**

1.  사용자가 읽기 권한을 가지는 네트워크 공유에 AgentSetup.exe UE-V 에이전트 설치 파일을 준비 합니다.

2.  UE-V Agent를 설치 하는 사용자 컴퓨터에 스크립트를 배포 합니다. 스크립트는 설정 저장소 위치를 지정 해야 합니다.

**배포 옵션:** UE-V 에이전트를 설치할 때 올바른 변수 형식을 사용 해야 합니다. 다음 표에서는 AgentSetup.exe 또는 Windows Installer (.msi) 파일을 사용 하는 배포 옵션의 예를 제공 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>배포 유형</strong></th>
<th align="left"><strong>배포 설명</strong></th>
<th align="left"><strong>예</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>명령 프롬프트</p></td>
<td align="left"><p>명령 프롬프트에서 UE-V Agent를 설치 하는 경우 <em> % ^ username% </em> 변수 형식을 사용 합니다. 설정 저장소 경로의 공간 때문에 인용 부호가 필요한 경우 배포용 배치 스크립트 파일을 사용 합니다.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>일괄 처리 스크립트</p></td>
<td align="left"><p>배치 스크립트 파일에서 UE-V 에이전트를 설치 하는 경우 <em> %% username%% </em> 변수 형식을 사용 합니다. 이 설치 방법을 사용 하는 경우%% 문자로 변수를 이스케이프 해야 합니다. 이 문자를 사용 하지 않으면 스크립트가 <em> 런타임 대신 설치 시 사용자 이름 변수를 확장 하 여 </em> ue-v가 모든 사용자에 대해 단일 설정 저장소 위치를 사용할 수 있도록 합니다.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell</p></td>
<td align="left"><p>Windows PowerShell 프롬프트 또는 Windows PowerShell 스크립트에서 UE-V Agent를 설치 하는 경우 <em> % username% </em> 변수 형식을 사용 합니다.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>전자 소프트웨어 배포 (예: Configuration Manager 소프트웨어 배포 배포)</p></td>
<td align="left"><p>Configuration Manager를 사용 하 여 UE-V 에이전트를 설치 하는 경우 <em> ^% username ^% </em> 변수 형식을 사용 합니다.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**참고**  
UE-V 에이전트를 설치 하려면 관리자 권한이 필요 하며, 컴퓨터를 다시 시작 해야 UE-V Agent를 실행할 수 있습니다.



### <a href="" id="params"></a>UE-V 에이전트 배포의 명령줄 매개 변수

UE-V 에이전트의 명령줄 매개 변수는 다음과 같습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>명령줄 매개 변수</strong></th>
<th align="left"><strong>정의</strong></th>
<th align="left"><strong>참고</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/help 또는/h 또는/?</p></td>
<td align="left"><p>AgentSetup.exe 사용 대화 상자를 표시 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>설정이 저장 되는 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</p></td>
<td align="left"><div class="alert">
<strong>중요</strong><br/><p>UE-V 2.1 및 UE-V 2.1 SP1에서 SettingsStoragePath를 지정 해야 합니다. AdHomePath 문자열을 설정 하 여 사용자&#39;s Active Directory home path를 사용 하도록 지정할 수 있습니다. 예를 들면 <code>SettingsStoragePath = \share\path|AdHomePath</code>입니다.</p>
<p>UE-V 2.0에서 Active Directory home 경로를 대신 사용 하도록 SettingsStoragePath를 비워 둘 수 있습니다.</p>
</div>
<div>

</div>
<p>% username% 또는% computername% 환경 변수를 허용 합니다. 스크립팅에는 이스케이프 된 변수가 필요할 수 있습니다.</p>
<p><strong>기본값 </strong> : &lt; 없음&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsStoragePathReg</p></td>
<td align="left"><p>설치 하는 동안 레지스트리에서 SettingsStoragePath 값을 가져옵니다.</p></td>
<td align="left"><p>명령 프롬프트에서 다음 예제를 입력 하 여 UE-V가 특정 UNC 대신 Active Directory home 경로를 사용 하도록 합니다.</p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</p></td>
<td align="left"><p>사용자 지정 설정 위치 서식 파일에만 필요 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.</p></td>
<td align="left"><p>True | 해제</p>
<p><strong>기본값 </strong> : True</p></td>
</tr>
<tr class="even">
<td align="left"><p>Powerschool</p></td>
<td align="left"><p>사용할 동기화 방법을 지정 합니다.</p></td>
<td align="left"><p>SyncProvider | 않아야</p>
<p><strong>기본값 </strong> : syncprovider</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>설정 저장소 위치에서 사용자 설정을 검색할 때 시간이 초과 되기 전에 컴퓨터가 대기 하는 시간 (밀리초)을 지정 합니다.</p></td>
<td align="left"><p><strong>기본값 </strong> : 2000 밀리초</p>
<p>(2 초까지 대기)</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>UE-V 동기화를 사용할지 여부를 지정 합니다.</p></td>
<td align="left"><p>True | 해제</p>
<p><strong>기본값 </strong> : True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>UE-V Agent가 해당 파일이 임계값을 초과 하는 것으로 보고할 때 설정 패키지 파일 크기 (바이트)를 지정 합니다.</p></td>
<td align="left"><p>&lt;크기&gt;</p>
<p><strong>기본값 </strong> : 없음 (경고 임계값 없음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>사용자 환경 개선 프로그램의 참여에 대 한 설정을 지정 합니다. True로 설정 <strong> 하면 </strong> 설치 관리자 정보가 Microsoft 사용자 환경 개선 프로그램 사이트에 업로드 됩니다. False로 설정 <strong> </strong> 된 경우 정보는 업로드 되지 않습니다.</p></td>
<td align="left"><p>True | 해제</p>
<p><strong>기본값 </strong> : False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoRestart</p></td>
<td align="left"><p>UE-V Agent가 설치 된 후 컴퓨터를 다시 시작 하는 지연을 지원 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>INSTALLFOLDER</p></td>
<td align="left"><p>UE-V 에이전트 또는 UE-V 생성기에 대해 다른 설치 폴더를 설정할 수 있도록 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MUENABLED</p></td>
<td align="left"><p>설치 프로그램이 Microsoft Update 프로그램에 포함 되는 옵션을 허용 하도록 설정 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ACCEPTLICENSETERMS</p></td>
<td align="left"><p>UE-V를 자동으로 설치할 수 있습니다. <strong> </strong> Ue-v를 자동으로 설치 하 고 사용자가 ue-v 라이선스 조건을 허용 하는 요구 사항을 무시 하려면이를 True로 설정 해야 합니다. False로 설정 <strong> </strong> 되거나 비어 있는 경우 사용자에 게 오류 메시지가 발생 하 고 ue-v가 설치 되어 있지 않습니다.</p></td>
<td align="left"><div class="alert">
<strong>중요</strong><br/><p>이 매개 변수는 UE-V를 자동으로 설치 하는 데 필요 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NORESTART</p></td>
<td align="left"><p>UE-V Agent가 설치 된 후 필수 다시 시작을 방지 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### UE-V 에이전트 업데이트

UE-V 에이전트 소프트웨어에 대 한 업데이트는 Microsoft Update를 통해 제공 됩니다. ESD (엔터프라이즈 소프트웨어 배포) 인프라 시스템을 사용 하 여 UE-V 에이전트 업데이트를 배포할 수 있습니다.

UE-V 에이전트 업그레이드 중에 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치 템플릿의 기본 그룹을 업데이트할 수 있습니다.

### UE-V 2. x 에이전트 업그레이드

UE-V 2. x 에이전트는 여러 가지 새로운 기능을 도입 하 고 에이전트가 설정 저장소 공유에 콘텐츠를 업로드 하는 방법과 시기를 수정 합니다. 업그레이드 프로세스는 이러한 변경을 자동화 합니다. UE-V Agent를 업그레이드 하려면 사용자 컴퓨터에서 UE-V Agent 설치 패키지 (AgentSetup.exe, AgentSetupx86.msi 또는 AgentSetupx64.msi)를 실행 합니다.

**참고**  
UE-V Agent를 업그레이드 하는 경우 이전 UE-V 에이전트를 설치 하는 동일한 설치 관리자 유형 (.exe 파일 또는 .msi 패킷)을 사용 해야 합니다. 예를 들어 UE-V 1.0 AgentSetup.exe를 사용 하 여 AgentSetup.exe를 사용 하 여 설치한 UE-V 에이전트를 업그레이드 합니다.



에이전트 설정 프로그램이 실행 될 때 다음 구성이 유지 됩니다.

-   설정 저장소 경로

-   레지스트리 설정

-   예약 된 작업 (간격 설정이 기본값으로 다시 설정 됨)

**참고**  
Ue-v 1.0 에이전트에 등록 되어 있는 UE-V 2. x 설정 위치 템플릿이 있는 컴퓨터는 Windows 이벤트 로그에 오류를 등록 합니다.



Microsoft System Center 2012 구성 관리자 또는 다른 엔터프라이즈 소프트웨어 배포 도구를 사용 하 여 UE-V 에이전트 업그레이드를 자동화 하 고 배포할 수 있습니다.

**권장 사항:** 컴퓨팅 환경에서 모든 UE-V 1.0 에이전트를 업그레이드 하는 것이 좋지만, 꼭 필요한 것은 아닙니다. UE-V 2. x 설정 위치 템플릿은 설정 저장소 경로의 설정만 공유 하므로 UE-V 1.0 에이전트와 상호 작용할 수 있습니다. 그러나 관리를 간소화 하 고 UE-V를 지원 하기 위해 배포를 단일 에이전트 버전으로 이동 하는 것이 좋습니다.

### 업그레이드 실패 후 UE-V 에이전트 복구

다음 작업 중 하나를 시도한 후 오류가 발생할 수 있습니다.

-   UE-V 1.0에서 UE-V 2로 업그레이드

-   예를 들어 Windows 7에서 Windows 8으로 또는 Windows 8에서 Windows 8.1까지 최신 버전의 Windows로 업그레이드 합니다.

-   UE-V Agent를 업그레이드 한 후 에이전트 제거

문제를 해결 하려면 에이전트가 설치 된 컴퓨터의 명령 프롬프트에이 명령을 입력 하 여 UE-V 에이전트 복구를 시도 합니다.

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

그런 다음 최신 버전의 UE-V Agent를 설치 하 여 제거 프로세스나 업그레이드를 다시 시도할 수 있습니다.






## 관련 항목


[UE-V 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









