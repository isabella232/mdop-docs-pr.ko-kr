---
title: 가상화된 응용 프로그램이 있는 가상 환경에서 로컬로 설치된 응용 프로그램 실행
description: 가상화된 응용 프로그램이 있는 가상 환경에서 로컬로 설치된 응용 프로그램 실행
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813313"
---
# 가상화된 응용 프로그램이 있는 가상 환경에서 로컬로 설치된 응용 프로그램 실행


Microsoft Application Virtualization (App-v)를 사용 하 여 가상화 된 응용 프로그램과 함께 가상 환경에서 로컬에 설치 된 응용 프로그램을 실행할 수 있습니다. 다음과 같은 경우에이 작업을 할 수 있습니다.

-   클라이언트 컴퓨터에 로컬로 응용 프로그램을 설치 하 고 실행 하지만 해당 로컬 응용 프로그램을 사용 하는 특정 플러그 인을 가상화 하 고 실행 하려는 경우

-   App-v 클라이언트 패키지의 문제를 해결 하 고 App-v 가상 환경 내에서 로컬 응용 프로그램을 열려고 합니다.

다음 메서드 중 하나를 사용 하 여 App-v 가상 환경 내에서 로컬 응용 프로그램을 엽니다.

-   [가상 레지스트리 키 run](#bkmk-runvirtual-regkey)

-   [AppvClientPackage PowerShell cmdlet](#bkmk-get-appvclientpackage-posh)

-   [명령줄 전환/appvpid: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [명령줄 후크 스위치/appvve: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

각 메서드는 본질적으로 동일한 작업을 수행 하지만 일부 메서드는 가상화 된 응용 프로그램이 이미 실행 중인지 여부에 따라 다른 응용 프로그램에 적합 한 경우도 있습니다.

## <a href="" id="bkmk-runvirtual-regkey"></a>가상 레지스트리 키 run


패키지 또는 연결 그룹의 가상 환경에 로컬로 설치 된 응용 프로그램을 추가 하려면 `RunVirtual` 다음 섹션에서 설명 하는 대로 레지스트리 편집기에서 레지스트리 키에 하위 키를 추가 합니다.

이 레지스트리 키를 관리 하는 데 사용할 수 있는 그룹 정책 설정이 없으므로 System Center Configuration Manager 또는 다른 전자 소프트웨어 배포 (ESD) 시스템을 사용 하거나 수동으로 레지스트리를 편집 해야 합니다.

### <a href="" id="bkmk-"></a>RunVirtual을 사용할 때 패키지를 게시 하는 지원 되는 방법

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 버전</th>
<th align="left">지원 되는 게시 방법</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 5.0 SP3</p></td>
<td align="left"><p>전역 또는 사용자에 게 게시</p></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 5.0-app-v 5.0 SP2를 통해</p></td>
<td align="left"><p>전체적 으로만 게시</p></td>
</tr>
</tbody>
</table>

 

### 하위 키를 만드는 단계

1.  다음 표의 정보를 사용 하 여 **MyApp.exe**같은 실행 파일의 이름을 사용 하 여 새 레지스트리 키를 만듭니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">패키지 게시 방법</th>
    <th align="left">레지스트리 키를 만드는 위치</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>전역 게시</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>예 </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>사용자에 게 게시</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>예 </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>연결 그룹에는 다음이 포함 될 수 있습니다.</p>
    <ul>
    <li><p>사용자에 게 전역 또는 단순한 방법 으로만 게시 되는 패키지</p></li>
    <li><p>전역 및 사용자에 게 게시 되는 패키지</p></li>
    </ul></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE 또는 HKEY_CURRENT_USER 키 중 하나를 사용할 수 있지만 다음 조건이 모두 충족 되어야 합니다.</p>
    <ul>
    <li><p>가상 환경에 여러 패키지를 포함 하려는 경우 사용 하도록 설정 된 연결 그룹에 포함 해야 합니다.</p></li>
    <li><p>연결 그룹의 패키지 중 하나에 대 한 하위 키를 하나만 만듭니다. 예를 들어 전역에 게시 된 하나의 패키지와 사용자에 게 게시 되는 다른 패키지가 있는 경우 이러한 패키지 중 하나에 대해서만 하위 키를 만듭니다. 패키지 중 하나에 대해서만 하위 키를 만들 수 있지만, 연결 그룹의 모든 패키지와 로컬 응용 프로그램은 가상 환경에서 사용할 수 있습니다.</p></li>
    <li><p>하위 키를 만드는 키는 패키지에 사용 하는 게시 방법과 일치 해야 합니다.</p>
    <p>예를 들어 사용자에 게 패키지를 게시 한 경우에서 하위 키를 만들어야 합니다 <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  새 레지스트리 하위 키의 값을 패키지의 PackageId 및 인수로 설정 하 여 값을 밑줄로 구분 합니다.

    **구문**: &lt; PackageId &gt; \ _ &lt; 로&gt;

    **예**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa

    이전 예제의 응용 프로그램에서는 다음과 같이 레지스트리 내보내기 파일 (.reg 파일)을 생성 합니다.

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>AppvClientPackage PowerShell cmdlet


**시작 AppVVirtualProcess** cmdlet을 사용 하 여 패키지 이름을 검색 한 다음 지정 된 패키지의 가상 환경 내에서 프로세스를 시작할 수 있습니다. 이 메서드를 사용 하면 패키지가 현재 실행 중인지 여부와 상관 없이 App-v 패키지의 컨텍스트 내에서 명령을 실행할 수 있습니다.

** &lt; &gt; 패키지의**이름 대신 다음 예제 구문을 사용 합니다.

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

패키지의 정확한 이름을 모르는 경우 명령줄 **get-AppvClientPackage \ * executable\\**를 사용할 수 있습니다. <em> 여기서 **executable </em> * 은 응용 프로그램의 이름입니다 (예: Get-AppvClientPackage \ * Word \ *).

## <a href="" id="bkmk-cl-switch-appvpid"></a>명령줄 전환/appvpid: &lt; PID&gt;


**/Appvpid: &lt; pid &gt; ** 스위치를 모든 명령에 적용 하 여 pid (프로세스 ID)를 지정 하 여 선택한 가상 프로세스 내에서 명령이 실행 되도록 할 수 있습니다. 이 메서드를 사용 하면 이미 실행 중인 실행 파일을 비롯 하 여 동일한 App-v 환경에서 새 실행 파일이 시작 됩니다.

예: `cmd.exe /appvpid:8108`

앱-V 프로세스의 PID (프로세스 ID)를 찾으려면 관리자 권한 명령 프롬프트에서 **tasklist.exe** 명령을 실행 합니다.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>명령줄 후크 스위치/appvve: &lt; GUID&gt;


이 스위치를 사용 하 여 App-v 패키지의 가상 환경 내에서 로컬 명령을 실행할 수 있습니다. 가상 환경이 이미 실행 되 고 있어야 하는 **/appvid** 스위치와 달리이 스위치를 사용 하 여 가상 환경을 시작할 수 있습니다.

구문과 `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

예: `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

패키지 GUID 및 응용 프로그램의 버전 GUID를 가져오려면 **AppvClientPackage** cmdlet을 실행 합니다. 다음과 같이 **/appvve** 스위치를 연결 합니다.

-   콜론

-   원하는 패키지의 패키지 GUID

-   밑줄

-   원하는 패키지의 버전 ID

패키지의 정확한 이름을 모르는 경우 명령줄 **get-AppvClientPackage \ * executable\\** <em> 를 사용 하세요. 여기서 **executable </em> * 은 응용 프로그램의 이름입니다 (예: Get-AppvClientPackage \ * Word \ *).

이 메서드를 사용 하면 패키지가 현재 실행 중인지 여부와 상관 없이 App-v 패키지의 컨텍스트 내에서 명령을 실행할 수 있습니다.






## 관련 항목


[App-V 5.0에 대한 기술 참조](technical-reference-for-app-v-50.md)

 

 





