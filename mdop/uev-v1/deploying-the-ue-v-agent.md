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
# UE-V 에이전트 배포


Microsoft UE-V (User Experience Virtualization) 에이전트는 UE-V를 사용 하 여 응용 프로그램 및 Windows 설정을 로밍 하는 각 컴퓨터에서 실행 해야 합니다. AgentSetup.exe 단일 설치 관리자 파일은 32 비트 및 64 비트 운영 체제에 모두 UE-V agent를 설치 합니다. UE-V 에이전트의 명령줄 매개 변수는 다음과 같습니다.

**명령줄 매개 변수 AgentSetup.exe**

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
<td align="left"><p>% username% 또는% computername% 환경 변수를 허용 합니다. 스크립팅에는 이스케이프 된 변수가 필요할 수 있습니다.</p>
<p><strong>기본값 </strong> : &lt; 없음 &gt; (Active Directory 사용자 홈)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</p></td>
<td align="left"><p>사용자 지정 설정 위치 서식 파일에만 필요 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.</p></td>
<td align="left"><p>True | 해제</p>
<p><strong>기본값 </strong> : True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Powerschool</p></td>
<td align="left"><p>사용할 동기화 방법을 지정 합니다.</p></td>
<td align="left"><p>기타 파일 | 않아야</p>
<p><strong>기본값 </strong> :가 중 파일</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>컴퓨터가 설정 저장소 위치에서 사용자 설정을 검색할 때 시간 초과 전에 대기 하는 밀리초 수를 지정 합니다.</p></td>
<td align="left"><p><strong>기본값 </strong> : 2000 밀리초</p>
<p>(2 초까지 대기)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>UE-V 동기화를 사용할지 여부를 지정 합니다.</p></td>
<td align="left"><p>True | 해제</p>
<p><strong>기본값 </strong> : True</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>UE-V agent가 해당 파일이 임계값을 초과 하는 것으로 보고할 때 설정 패키지 파일 크기 (바이트)를 지정 합니다.</p></td>
<td align="left"><p>&lt;크기&gt;</p>
<p><strong>기본값 </strong> : 없음 (경고 임계값 없음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>사용자 환경 개선 프로그램의 참여에 대 한 설정을 지정 합니다. True로 설정 하면 설치 관리자 정보가 Microsoft 사용자 환경 개선 프로그램 사이트에 업로드 됩니다. False로 설정 된 경우 정보는 업로드 되지 않습니다.</p></td>
<td align="left"><p>True | 해제</p>
<p><strong>기본값 </strong> : False</p>
<p><strong>Windows 7 </strong> : True</p></td>
</tr>
</tbody>
</table>

 

설치 하는 동안 SettingsStoragePath 명령줄 매개 변수는 설정 값에 대 한 설정 저장소 위치를 지정 합니다. UE-V 에이전트를 배포 하기 전에 설정 저장소 위치를 정의할 수 있습니다. 설정 저장소 위치가 정의 되지 않은 경우 UE-V-V는 Active Directory 사용자 홈 디렉터리를 설정 저장소 위치로 사용 합니다. 설치 중에 SettingsStoragePath 구성을 지정 하 고 값의 일부로% username%을 (를) 사용 하는 경우,이는 사용자가 로그인 하는 모든 컴퓨터 또는 세션의 동일한 사용자 설정 환경을 로밍 합니다. SettingsStoragePath 값의 일부로%username%\\%computername% 변수를 지정 하면 각 컴퓨터에 대 한 설정 환경이 유지 됩니다.

32 비트 및 64 비트 설치 프로그램 외에도 UE-V 에이전트 설치에 대 한 아키텍처 관련 Windows Installer (.msi) 파일이 제공 됩니다. AgentSetupx86.msi 또는 AgentSetupx64.msi 설치 파일은 AgentSetup.exe 파일 보다 작으며 에이전트 배포를 간소화할 수 있습니다. AgentSetup.exe 설치 관리자의 명령줄 매개 변수는 Windows Installer (.msi) 설치에 대해 지원 됩니다.

**참고**  UE-V 에이전트 설치 또는 제거 중에 AgentSetup.exe 파일 또는 AgentSetup &lt; 아치 &gt; .msi 파일을 사용할 수 있습니다. Ue-v 에이전트를 설치 하는 데 사용 된 것과 동일한 파일을 사용 하 여 UE-V Agent를 제거 해야 합니다.

 

UE-V 에이전트를 설치할 때 올바른 변수 형식을 사용 해야 합니다. 다음 표에서는 AgentSetup.exe 또는 Windows Installer (.msi) 설치 파일을 사용 하는 배포 옵션의 예를 제공 합니다.

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
<td align="left"><p>명령 프롬프트에서 UE-V agent를 설치 하는 경우% ^ username% 변수 형식을 사용 합니다. 설정 저장소 경로의 공간 때문에 인용 부호가 필요한 경우 배포용 배치 스크립트 파일을 사용 합니다.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>일괄 처리 스크립트</p></td>
<td align="left"><p>배치 스크립트 파일에서 UE-V 에이전트를 설치 하는 경우%% username%% 변수 형식을 사용 합니다. 이 설치 방법을 사용 하는 경우%% 문자로 변수를 이스케이프 해야 합니다. 이 문자가 없으면 스크립트는 설치 시에 런타임 대신 사용자 이름 변수를 확장 하 여 UE-V가 모든 사용자에 대해 단일 설정 저장소 위치를 사용 하도록 합니다.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>PowerShell 프롬프트 또는 PowerShell 스크립트에서 UE-V agent를 설치 하는 경우% username% 변수 형식을 사용 합니다.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>전자 소프트웨어 배포 (예: Configuration Manager 소프트웨어 배포 배포)</p></td>
<td align="left"><p>구성 관리자를 사용 하 여 UE-V Agent를 설치 하는 경우 ^% username ^% 변수 형식을 사용 합니다.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**참고**  U-EV 에이전트 설치에는 관리자 권한이 필요 하며, 컴퓨터를 다시 시작 해야 UE-V agent를 실행할 수 있습니다.

 

## 네트워크 공유의 UE-V Agent 배포 방법


다음 메서드를 사용 하 여 UE-V 에이전트를 배포할 수 있습니다.

-   Windows Installer (.msi) 파일을 설치할 수 있는 ESD (전자 소프트웨어 배포) 솔루션입니다.

-   공유에 중앙에 저장 된 Windows Installer (.msi) 파일을 참조 하는 설치 스크립트입니다.

-   컴퓨터에서 설치 프로그램을 수동으로 실행 합니다.

네트워크 공유에서 UE-V agent를 배포 하려면 다음 단계를 사용 합니다.

**네트워크 공유에서 UE-V Agent를 설치 하 고 구성 하려면**

1.  사용자에 게 "읽기" 권한이 있는 네트워크 공유에서 UE-V agent 설치 파일 (AgentSetup.exe)을 준비 합니다.

2.  UE-V agent를 설치 하는 사용자 컴퓨터에 스크립트를 배포 합니다. 스크립트는 설정 저장소 위치를 지정 해야 합니다.

**UE-V 에이전트 업데이트**

UE-V 에이전트 소프트웨어에 대 한 업데이트는 Microsoft Update를 통해 제공 됩니다. UE-V 에이전트 업그레이드 중에 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치 템플릿의 기본 그룹이 업데이트 될 수 있습니다. UE-V 에이전트 업데이트는 엔터프라이즈 소프트웨어 배포 (ESD) 인프라를 사용 하 여 배포할 수 있습니다.

## 관련 항목


[UE-V 1.0 배포](deploying-ue-v-10.md)

[UE-V 1.0에 지원되는 구성](supported-configurations-for-ue-v-10.md)

[UE-V 1.0에 대한 설정 저장소 위치 배포](deploying-the-settings-storage-location-for-ue-v-10.md)

[UE-V 생성기 설치](installing-the-ue-v-generator.md)

사용자 환경 가상화 에이전트 배포
 

 





