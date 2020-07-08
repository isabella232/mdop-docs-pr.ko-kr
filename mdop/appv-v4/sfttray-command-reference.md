---
title: SFTTRAY 명령 참조
description: SFTTRAY 명령 참조
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815353"
---
# SFTTRAY 명령 참조


Microsoft App-v (Application Virtualization) 클라이언트 트레이 응용 프로그램 sfttray.exe는 사용자가 일반적으로 사용 하는 동안 상호 작용 하는 App-v 클라이언트의 기본 사용자 인터페이스 요소입니다. 이 프로그램은 모든 가상 응용 프로그램의 스트리밍 및 시작을 제어 하며 알림 영역에 표시 된 아이콘을 마우스 오른쪽 단추로 클릭 하 여 클라이언트 함수의 메뉴를 표시 하는 방법으로 액세스할 수 있습니다. 이 메뉴를 통해 사용자는 응용 프로그램을 로드 하거나, 게시 새로 고침을 시작 하거나, 요청을 취소 하거나, 클라이언트를 오프 라인 모드로 변경할 수 있습니다. 또한 사용자는 **끝내기**를 클릭 하 여 응용 프로그램 가상화 클라이언트 트레이 응용 프로그램과 모든 활성 응용 프로그램을 닫을 수 있습니다.

기본적으로 가상 응용 프로그램이 시작 될 때마다 아이콘이 표시 되지만 SFTTRAY 명령을 사용 하 여이 동작을 제어할 수 있습니다. 또한 응용 프로그램 가상화 클라이언트 트레이 응용 프로그램에는 시작 된 각 응용 프로그램에 대 한 진행률 표시줄과 활성 응용 프로그램에 대 한 상태 메시지가 표시 됩니다. 진행률 표시줄을 클릭 하면 응용 프로그램의 로드 또는 시작을 취소할 수 있는 메시지가 표시 됩니다.

## SFTTRAY 명령


명령 창에서 다음 명령을 실행 하 여 명령 및 명령줄 스위치의 목록을 표시할 수 있습니다.

**참고**  
각 사용자 컨텍스트에 대해 응용 프로그램 가상화 클라이언트 트레이 인스턴스가 하나 밖에 없기 때문에 새 SFTTRAY 명령을 시작 하면 이미 실행 중인 프로그램으로 전달 됩니다.



`Sfttray.exe /?`

### 명령 사용법

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### 명령줄 스위치

SFTTRAY 명령줄 스위치는 다음 표에 설명 되어 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">스위치</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/CHIDE</p></td>
<td align="left"><p>Windows 알림 영역에서 SFTTRAY 아이콘을 숨깁니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Drivers</p></td>
<td align="left"><p>Windows 알림 영역에 SFTTRAY 아이콘을 표시 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/QUIET</p></td>
<td align="left"><p>오류를 방지 하 여 사용자 승인이 필요한 메시지 상자를 표시 하지 못하게 하 여 무인 사용을 지원 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/EXE &lt; 대체 EXE&gt;</p></td>
<td align="left"><p>/LAUNCH와 함께 사용 하 여 OSD에 지정 된 대상 파일 대신 가상 응용 프로그램이 시작 될 때 가상 환경에서 실행 프로그램을 시작 하도록 지정 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>예를 들어 "SFTTRAY.EXE/EXE REGEDIT.EXE/LAUNCH &lt; app"를 사용 &gt; 하 여 응용 프로그램이 실행 되 고 있는 가상 환경의 레지스트리를 검사할 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAUNCH &lt; app &gt; [ &lt; args &gt; ]</p></td>
<td align="left"><p>가상 응용 프로그램을 시작 합니다. 응용 프로그램의 이름 및 버전 또는 OSD 파일 경로를 지정 합니다. 선택적으로 명령줄 인수를 가상 응용 프로그램에 전달할 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>"SFTMIME.EXE/QUERY OBJ: APP/SHORT" 명령을 사용 하 여 사용 가능한 가상 응용 프로그램의 이름 및 버전 목록을 가져옵니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>/CLOAD</p></td>
<td align="left"><p>가상 응용 프로그램을 로드 하거나 가져옵니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOADALL</p></td>
<td align="left"><p>모든 응용 프로그램을 캐시로 로드 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESHALL</p></td>
<td align="left"><p>모든 응용 프로그램에 대 한 게시 새로 고침을 시작 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAUNCHRESULT &lt; 고유 ID&gt;</p></td>
<td align="left"><p>고유 ID에 대해 지정 된 루트 이름을 기반으로 하는 메모리 매핑된 파일 및 전역 이벤트를 사용 하 여 sfttray.exe를 실행 하는 프로세스에 대 한 시작 결과 코드를 반환 합니다. ¹</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTFILE &lt; sft&gt;</p></td>
<td align="left"><p>선택 사항인 스위치는/TLOAD와 함께 사용 하 여 응용 프로그램의 SFT 파일 경로를 지정 합니다. 지정 된 경우 응용 프로그램을 로드 하지 않고 가져옵니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CEXIT</p></td>
<td align="left"><p>SFTTRAY 프로그램과 모든 활성 가상 응용 프로그램을 닫고 Windows 알림 영역에서 아이콘을 제거 합니다.</p></td>
</tr>
</tbody>
</table>



**참고**  
¹ */Prresult* 명령줄 매개 변수는 전역 이벤트의 루트 이름을 지정 하 고 프로세스에 대 한 실행 결과 코드를 반환 하는 데 사용 되는 메모리 매핑된 파일을 sfttray.exe를 시작 하는 프로세스에 대 한 방법을 제공 합니다. 가상 환경 내에서 시작 프로세스가 호출 될 때 이벤트 이름이 가상화 되지 않도록 하려면 고유 식별자 이름을 "SFT-"로 시작 해야 합니다. 메모리 매핑 영역의 크기는 64 비트입니다.

이 매개 변수를 사용 하기 위해 시작 프로세스가 "고유 id-결과 \ _event" 라는 이름을 가진 이벤트와 "고유 id- &lt; &gt; 결과 \ _value" 라는 이름을 가진 메모리 매핑 파일을 만들고, &lt; 선택적으로 &gt; 이벤트에 " &lt; 고유 id &gt; -종료 \ _event"를 추가한 다음 시작 프로세스가 sfttray.exe를 실행 하 고 이벤트 신호를 받을 때까지 기다립니다. " &lt; 고유 ID &gt; -결과 \ _event" 이벤트가 신호를 받은 후에는 시작 프로세스가 메모리 매핑된 영역에서 64 비트 반환 코드를 검색 합니다.

&lt; &gt; 가상 응용 프로그램이 종료 될 때 선택적 이벤트 "고유 ID-종료 \ _event"가 있는 경우 sfttray.exe가 이벤트를 열고 신호를 보냅니다. 시작 프로세스는 가상 응용 프로그램이 종료 되는 시점을 확인 해야 하는 경우이 종료 이벤트를 기다립니다.











