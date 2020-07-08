---
title: Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 설정 위치 템플릿 관리
description: Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 설정 위치 템플릿 관리
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812881"
---
# Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 설정 위치 템플릿 관리


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1은 XML 설정 위치 템플릿을 사용 하 여 사용자 환경 가상화가 캡처 및 적용 하는 설정을 정의 합니다. UE-V는 표준 설정 위치 템플릿 집합을 포함 합니다. 또한 사용자 지정 설정 위치 템플릿을 만드는 데 사용할 수 있는 UE-V 생성기 도구가 포함 됩니다. 설정 위치 템플릿을 만들고 배포한 후에는 Windows PowerShell 및 WMI (Windows Management Instrumentation)를 사용 하 여 해당 템플릿을 관리할 수 있습니다. UE-V PowerShell cmdlet의 전체 목록은 [ue-v 2 Cmdlet 참조](https://go.microsoft.com/fwlink/p/?LinkId=393495) ()를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Windows PowerShell을 사용 하 여 UE-V 2 설정 위치 템플릿 관리


UE-V의 WMI 및 Windows PowerShell 기능에는 설정 위치 템플릿을 사용, 사용 안 함, 등록, 업데이트 및 등록 취소 하는 기능이 포함 됩니다. 이러한 기능을 사용 하 여 UE-V Agent를 사용 하 여 서식 파일을 등록, 업데이트 또는 등록 취소 하는 프로세스를 자동화할 수 있습니다. 또한 WMI 및 Windows PowerShell 명령을 사용 하 여 수동으로 템플릿을 등록할 수 있습니다. 이러한 기능을 전자 소프트웨어 배포 솔루션, 그룹 정책 또는 스크립트와 같은 다른 자동화 된 배포 방법과 함께 사용 하면 해당 프로세스를 더 자동화할 수 있습니다.

설정 위치 템플릿을 업데이트, 등록 또는 등록 취소 하려면 관리자 권한이 있어야 합니다. 관리자 권한은 서식 파일을 사용, 사용 안 함 또는 나열할 때 필요 하지 않습니다.

***<em>Windows PowerShell을 사용 하 여 설정 위치 템플릿을 관리 하려면ell</em>***

1.  관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 명령 프롬프트를 엽니다.

2.  다음 Windows PowerShell cmdlet을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.

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
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>컴퓨터에 등록 된 모든 설정 위치 템플릿을 나열 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>응용 프로그램 이름 또는 서식 파일 이름에 문자열이 포함 된 컴퓨터에 등록 되어 있는 모든 설정 위치 템플릿을 &lt; 나열 &gt; 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>서식 파일 ID에 문자열이 포함 된 컴퓨터에 등록 되어 있는 모든 설정 위치 템플릿을 나열 &lt; 합니다 &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>응용 프로그램 또는 서식 파일 이름 또는 서식 파일 ID에 문자열이 포함 된 컴퓨터에 등록 되어 있는 모든 설정 위치 템플릿을 &lt; 나열 &gt; 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>서식 파일 ID에 따라 달라 지는 프로그램의 이름과 버전 정보를 가져옵니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Windows 앱의 유효 목록을 가져옵니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>컴퓨터에 대해 구성 된 Windows 앱 목록을 가져옵니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>현재 사용자에 대해 구성 된 Windows 앱 목록을 가져옵니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>파일 경로에 상대 경로 및/또는 와일드 카드 문자를 사용 하 여 UE-V를 사용 하 여 하나 이상의 설정 위치 템플릿을 등록 합니다. 템플릿을 등록 한 후에는 UE-V가 등록 된 템플릿이 있는 컴퓨터 간에 서식 파일에 정의 된 설정을 동기화 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>문자를 와일드 카드 문자로 해석할 수 없는 리터럴 경로를 사용 하 여 UE-V를 사용 하 여 하나 이상의 설정 위치 템플릿을 등록 합니다. 템플릿을 등록 한 후에는 UE-V가 등록 된 템플릿이 있는 컴퓨터 간에 서식 파일에 정의 된 설정을 동기화 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다. 템플릿이 등록 취소 되 면 UE-V는 더 이상 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 모든 설정 위치 템플릿의 등록을 취소 합니다. 템플릿이 등록 취소 되 면 UE-V는 더 이상 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>하나 이상의 설정 위치 템플릿을 최신 버전의 템플릿으로 업데이트 합니다. 파일 경로에 상대 경로 및/또는 와일드 카드 문자를 사용 합니다. 새 서식 파일은 기존 서식 파일 보다 최신 버전 이어야 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>하나 이상의 설정 위치 템플릿을 최신 버전의 템플릿으로 업데이트 합니다. 문자를 와일드 카드 문자로 해석할 수 없는 경우 서식 파일의 전체 경로를 사용 합니다. 새 서식 파일은 기존 서식 파일 보다 최신 버전 이어야 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 모든 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 모든 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 비활성화 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 사용 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하도록 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하도록 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>하나 이상의 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다. 상대 경로와 와일드 카드 문자를 사용할 수 있습니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>하나 이상의 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다. 경로는 서식 파일에 대 한 전체 경로 여야 하지만 와일드 카드 문자는 포함 하지 않습니다.</p></td>
    </tr>
    </tbody>
    </table>



UE-V Windows PowerShell 기능을 사용 하면 엔터프라이즈에 배포 된 설정 서식 파일 그룹을 관리할 수 있습니다. Windows PowerShell을 사용 하 여 서식 파일 그룹을 관리 하려면 다음 절차를 사용 합니다.

**Windows PowerShell을 사용 하 여 설정 위치 템플릿의 그룹을 관리 하려면**

1.  원하는 설정 위치 템플릿을 수정 하거나 업데이트 합니다.

2.  설정 위치 템플릿을 수정 하거나 업데이트 하려는 경우 해당 설정 위치 템플릿을 로컬 컴퓨터에서 액세스할 수 있는 폴더에 배포 합니다.

3.  로컬 컴퓨터에서 관리자 권한이 있는 Windows PowerShell 창을 엽니다.

4.  다음 명령을 입력 하 여 이전에 등록 된 모든 버전의 템플릿을 등록 취소 합니다.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    이 명령은 컴퓨터에 있는 모든 활성 서식 파일의 등록을 취소 합니다.

5.  다음 명령을 입력 하 여 업데이트 된 서식 파일을 등록 합니다.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    이 명령은 지정 된 서식 파일 폴더에 있는 모든 설정 위치 템플릿을 등록 합니다.

### <a href="" id="win8applist"></a>Windows 앱 목록

Windows 앱 목록에 Windows 앱을 나열 하 여 설정 동기화를 위해 앱을 사용할지 여부를 지정 합니다. 앱은 패키지 패밀리 이름 및 해당 앱에 대 한 설정 동기화를 사용할지 여부를 기준으로 목록에서 식별 됩니다. 목록에 없는 기본 동기화 동작 설정과 함께 이러한 설정을 사용 하면 Windows 앱이 동기화 되는지 여부를 제어할 수 있습니다.

설치 된 Windows 앱의 패키지 패밀리 이름을 표시 하려면 Windows PowerShell 명령 프롬프트에서 다음을 입력 합니다.

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Windows PowerShell 명령 프롬프트에서 컴퓨터의 설정을 동기화 할 수 있는 Windows 앱 목록 (패키지 패밀리 이름, 사용 상태 및 활성화 된 원본)을 표시 하려면 다음을 입력 합니다. `Get-UevAppxPackage`

**Get-UevAppxPackage 속성 정의**

<a href="" id="displayname"></a>**DisplayName**  
회사 설정 센터 응용 프로그램에서 사용자에 게 표시 되는 이름입니다. 속성이 `DisplayName` 속성에서 파생 됩니다 `PackageFamilyName` .

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
현재 사용자 용으로 설치 된 패키지의 이름입니다.

<a href="" id="enabled"></a>**설정됨**  
앱 설정이 동기화 되도록 구성 되었는지 여부를 정의 합니다.

<a href="" id="enabledsource"></a>**EnabledSource**  
앱을 사용 하거나 사용 하지 않도록 설정할 구성이 설정 된 위치입니다. 사용할 수 있는 값은 *NotSet*, *LocalMachine*, *localuser*, *policymachine*, *policymachine*입니다.

<a href="" id="notset"></a>**NotSet**  
정책이이 앱을 동기화 하도록 구성 되어 있지 않습니다.

<a href="" id="localmachine"></a>**LocalMachine**  
사용 상태는 레지스트리의 로컬 컴퓨터 섹션에 설정 됩니다.

<a href="" id="localuser"></a>**LocalUser**  
사용할 수 있는 상태는 레지스트리의 현재 사용자 섹션에 설정 됩니다.

<a href="" id="policymachine"></a>**PolicyMachine**  
사용 상태는 레지스트리의 로컬 컴퓨터 섹션의 정책 섹션에서 설정 됩니다.

Windows 앱의 사용자 구성 목록을 가져오려면 Windows PowerShell 명령 프롬프트에서 다음을 입력 합니다. `Get-UevAppxPackage –CurrentComputerUser`

Windows 앱의 컴퓨터 구성 목록을 가져오려면 Windows PowerShell 명령 프롬프트에서 다음을 입력 합니다. `Get-UevAppxPackage –Computer`

CurrentComputerUser 또는 컴퓨터 중 하나의 매개 변수를 사용 하는 경우 cmdlet은 사용자 또는 컴퓨터 수준에서 구성 된 Windows 앱 목록을 반환 합니다.

**속성 정의**

<a href="" id="displayname"></a>**DisplayName**  
회사 설정 센터 응용 프로그램에서 사용자에 게 표시 되는 이름입니다. 속성이 `DisplayName` 속성에서 파생 됩니다 `PackageFamilyName` .

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
현재 사용자 용으로 설치 된 패키지의 이름입니다.

<a href="" id="enabled"></a>**설정됨**  
지정 된 스위치 (즉, **사용자** 또는 **컴퓨터**)에 대해 앱 설정이 동기화 되도록 구성 되었는지 여부를 정의 합니다.

<a href="" id="installed"></a>**설치됨**  
현재 사용자에 대 한 PackageFamilyName가 설치 되어 있으면 True이 고, 그렇지 않으면 false입니다.

### WMI를 사용 하 여 UE-V 2 설정 위치 템플릿 관리

사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다. 관리자는 이러한 인터페이스를 사용 하 여 Windows PowerShell에서 설정 위치 템플릿을 관리 하 고 템플릿 관리 작업을 자동화할 수 있습니다.

**WMI를 사용 하 여 설정 위치 템플릿을 관리 하려면**

1.  관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.

2.  다음 WMI 명령을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>컴퓨터에 대해 등록 된 모든 설정 위치 템플릿을 나열 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>서식 파일 이름에 따라 달라 지는 프로그램의 이름과 버전 정보를 가져옵니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Windows 앱의 유효 목록을 가져옵니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>WmiObject-네임 스페이스 root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>컴퓨터에 대해 구성 된 Windows 앱 목록을 가져옵니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>현재 사용자에 대해 구성 된 Windows 앱 목록을 가져옵니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 등록 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다. 서식 파일이 등록 취소 되 면 UE-V는 더 이상 컴퓨터 간에 서식 파일에 정의 된 설정을 동기화 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 업데이트 합니다. 새 템플릿은 기존 버전과 최신 버전 이어야 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 하나 이상의 설정 위치 템플릿을 사용할 수 없도록 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 사용 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>컴퓨터 Windows 앱 목록에서 Windows 앱을 사용 하도록 설정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>현재 사용자 Windows 앱 목록에서 Windows 앱을 사용 하도록 설정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>지정 된 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Windows PowerShell을 사용 하 여 UE-V 에이전트 배포

**Windows PowerShell을 사용 하 여 UE-V 에이전트를 배포 하는 방법**

1.  액세스 가능한 네트워크 공유에서 UE-V Agent 설치 패키지를 준비 합니다.

    **참고**  
    AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다. Windows Installer 패키지 AgentSetupx86.msi 및 AgentSetupx64.msi 각 아키텍처에서 사용할 수 있습니다. 나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.



2.  다음 Windows PowerShell 명령 중 하나를 사용 하 여 UE-V 에이전트를 설치 합니다.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Ue-v에 대 한 제안이 있으십니까**? [여기](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)에서 제안을 추가 하거나 투표 합니다. **Ue-v 문제가**있나요? [Ue-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)을 사용 합니다.

## 관련 항목


[Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)









