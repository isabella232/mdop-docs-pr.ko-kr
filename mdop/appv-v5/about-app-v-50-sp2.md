---
title: App-V 5.0 SP2 정보
description: App-V 5.0 SP2 정보
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814988"
---
# App-V 5.0 SP2 정보


App-v 5.0 SP2는 향상 된 통합 플랫폼, 유연한 가상화, 가상화 응용 프로그램에 대 한 강력한 관리 기능을 제공 합니다. 자세한 내용은 [앱-V 5.0 개요](https://go.microsoft.com/fwlink/p/?LinkId=325265) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=325265) .

## 표준 App-v 5.0 SP2 기능 변경 사항


다음 섹션에는 App-v 5.0 SP2의 표준 기능 변경 사항에 대 한 정보가 포함 되어 있습니다.

### <a href="" id="bkmk-sp2-supported-cfg"></a>Windows Server 2012 R2 및 Windows 8.1에 대 한 지원

앱-V 5.0에는 Windows Server 2012 R2 및 Windows 8.1에 대 한 지원이 포함 되어 있습니다.

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> 이제 app-v 5.0 SP2는 사용자 로밍 AppData 디렉터리에 대 한 폴더 리디렉션을 지원 합니다.

App-v 5.0 SP2는 로밍 AppData (% AppData%)를 지원 합니다. 폴더 리디렉션. 자세한 내용은 [app-v에서 폴더 리디렉션 사용 계획](planning-to-use-folder-redirection-with-app-v.md)을 참조 하세요.

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a>패키지 업그레이드 개선 사항 및 보류 중인 작업

앱-V 5.0 SP2에서는 더 이상 최신 버전의 패키지 또는 연결 그룹을 게시할 때 실행 중인 가상 응용 프로그램을 닫을지 묻는 메시지가 표시 되지 않습니다. 관련 작업을 수행 하려고 할 때 패키지 또는 연결 그룹이 사용 중인 경우 개체가 사용 중임을 나타내고 작업을 나중에 시도 한다는 메시지가 표시 됩니다.

보류 상태에 배치 된 작업은 다음 규칙에 따라 수행 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 종류</th>
<th align="left">해당 규칙</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업 (예: 패키지를 사용자에 게 게시)</p></td>
<td align="left"><p>보류 중인 작업은 사용자가 로그 오프 한 다음 다시 로그온 하면 수행 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업 (예: 연결 그룹을 전역적으로 사용 가능)</p></td>
<td align="left"><p>보류 중인 작업은 컴퓨터를 종료 한 후 다시 시작 하면 수행 됩니다.</p></td>
</tr>
</tbody>
</table>

 

작업이 보류 상태에 배치 되 면 App-v 클라이언트는 다음과 같이 보류 중인 작업에 대 한 레지스트리 키도 생성 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용자 기반 또는 전역 기반 작업</th>
<th align="left">레지스트리 키가 생성 되는 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

### App-v 5.0을 사용 하 여 Microsoft Office 2013 및 Microsoft Office 2010 가상화

앱-V 5.0 지원 되는 Microsoft Office 시나리오에 대 한 자세한 내용은 다음 링크를 사용 하세요.

[Application Virtualization(App-V) 5.0을 위한 Microsoft Office 2013 가상화](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

**참고**  이 문서에서는 Microsoft Office 2013 App-v 5.0 패키지 만들기에 대해 중점적으로 설명 합니다. 그러나 Microsoft Office 2010 for App-v 5.0에 대 한 시나리오에 대 한 정보도 제공 됩니다.

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> 앱-V 5.0 클라이언트 관리 사용자 인터페이스 응용 프로그램

이전 버전의 App-v 5.0에서 클라이언트 관리 UI (사용자 인터페이스)는 App-v 5.0 클라이언트 설치와 함께 제공 됩니다. App-v 5.0 SP2를 사용 하는 경우에는이 기능이 더 이상 없습니다. 이제 관리자는 App-v 5.0 클라이언트 UI를 가상 응용 프로그램 (지원 되는 모든 앱-V 배포 구성 사용) 또는 설치 된 응용 프로그램으로 배포 하는 옵션을 사용할 수 있습니다.

자세한 내용은 [Microsoft Application Virtualization 5.0 클라이언트 UI 응용 프로그램](https://go.microsoft.com/fwlink/p/?LinkId=386345) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=386345) .

### 나란히 (SxS) 어셈블리 자동 패키징 및 배포

이제 app-v 5.0 SP2는 자동으로 나란히 (SxS) 어셈블리를 감지 하 고 App-v 5.0 SP2 클라이언트를 실행 하는 컴퓨터에 배포 합니다. SxS 어셈블리는 주로 VC + + 런타임 종속성 또는 MSXML로 구성 됩니다. 이전 버전의 App-v에서는 VC 런타임에 종속성이 있는 가상 응용 프로그램에서 이러한 종속성이 App-v 5.0 SP2 클라이언트를 실행 하는 컴퓨터에 로컬로 있어야 합니다.

이제 다음 기능이 지원 됩니다.

-   앱-V 5.0 시퀀서는 VC 런타임이 시퀀서를 실행 하는 컴퓨터에 이미 설치 되었는지 여부에 관계 없이 패키지의 SxS 어셈블리를 자동으로 캡처합니다.

-   App-v 5.0 클라이언트는 게시할 때 필요에 따라 클라이언트를 실행 하는 컴퓨터에 필요한 SxS 어셈블리를 자동으로 설치 합니다.

-   App-v 5.0 sequencer는 sequencer 보고 메커니즘을 사용 하 여 VC 런타임 종속성을 보고 합니다.

-   이제 App-v 5.0 sequencer를 사용 하 여 sequencer를 실행 하는 컴퓨터에서 종속성을 이미 사용할 수 있는 경우 VC 런타임 종속성을 제외할 수 있습니다.

### 게시 새로 고침 개선

앱-V 5.0는 특정 사용자에 대 한 응용 프로그램 집합을 새로 고칠 때의 전반적인 환경을 개선 하기 위해 여러 기능을 추가할 수 있도록 지원 합니다.

다음 목록에는 게시 새로 고침 향상이 표시 되어 있습니다.

다음 목록에는 새 게시 새로 고침 개선 기능을 사용 하도록 설정 하는 방법에 대 한 자세한 정보가 나와 있습니다.

-   **EnablePublishingRefreshUI** -App-v 5.0 클라이언트를 실행 하는 컴퓨터에 대해 게시 새로 고침 진행률 표시줄을 사용 하도록 설정 합니다.

-   **HideUI** -수동 동기화 중에 게시 새로 고침 진행률 표시줄을 숨깁니다.

### 새 클라이언트 구성 설정

다음과 같은 새 클라이언트 구성 설정은 App-v 5.0 SP2에서 사용할 수 있습니다.

**Enabledynamicvirtualization** -지원 되는 셸 확장, 브라우저 도우미 개체 및 Active X 컨트롤을 가상 응용 프로그램을 사용 하 여 가상화 하 고 실행할 수 있도록 합니다.

자세한 내용은 [클라이언트 구성 설정](about-client-configuration-settings.md)정보를 참조 하세요.

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> 앱-V 5.0 셸 확장

앱-V 5.0 SP2는 이제 셸 확장을 지원 합니다.

자세한 내용은 app-v **5.0 sp2 셸 확장 지원** 섹션을 참조 하세요 [-v 5.0 가상화 된 응용 프로그램 만들기 및 관리](creating-and-managing-app-v-50-virtualized-applications.md)

## <a href="" id="---------app-v-5-0-documentation-updates"></a> 앱-V 5.0 문서 업데이트


App-v 5.0 SP2는 다음 시나리오에 대 한 업데이트 된 문서를 제공 합니다.

-   [이전 버전에서 마이그레이션](migrating-from-a-previous-version-app-v-50.md)

-   [App-V 5.0 정보](about-app-v-50.md)

-   [앱-V 5.0 보고](about-app-v-50-reporting.md) (질문과 대답 섹션)

## MDOP 기술을 활용 하는 방법


앱-V 5.0는 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .






## 관련 항목


[App-V 5.0 SP2 릴리스 정보](release-notes-for-app-v-50-sp2.md)

 

 





