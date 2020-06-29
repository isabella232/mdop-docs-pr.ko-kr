---
title: UE-V 2. x 예약 된 작업의 빈도 변경
description: UE-V 2. x 예약 된 작업의 빈도 변경
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824428"
---
# UE-V 2. x 예약 된 작업의 빈도 변경


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1 에이전트 설치 관리자 AgentSetup.exe, UE-V 에이전트를 설치 하는 동안 다음과 같은 예약 된 작업을 만듭니다.

-   **응용 프로그램 설정 모니터링**

-   **동기화 컨트롤러 응용 프로그램**

-   **로그 오프할 때 설정 동기화**

-   **서식 파일 자동 업데이트**

-   **CEIP 데이터 수집**

-   **CEIP 데이터 업로드**

**참고**  CEIP 데이터 수집을 제외 하 고는 UE-V를 사용 하지 않고 작동할 수 없으므로 이러한 작업은 활성 상태로 유지 되어야 합니다.

 

이러한 예약 된 작업은 UE-V 도구를 사용 하 여 구성할 수 없습니다. 이러한 항목에 대 한 예약 된 작업을 변경 하려는 관리자는 Schtasks.exe 명령줄 옵션을 사용 하는 스크립트를 만들 수 있습니다.

Schtasks.exe에 대 한 자세한 내용은 [Schtasks를 사용 하 여 Windows Server 2003에서 작업을 예약 하는 방법을](https://go.microsoft.com/fwlink/?LinkID=264854)참조 하세요.

자세한 내용은

## UE-V 예약 작업


다음 예약 된 작업은 예제 예약 작업 구성 명령이 있는 UE-V 2에 포함 되어 있습니다.

### CEIP 데이터 수집

설치 시 사용자 또는 관리자가 CEIP (고객 환경 개선 프로그램)에 참여 하도록 choses 경우 UE-V는 향후 릴리스에서 제품을 개선 하는 데 도움이 되는 데이터를 수집 합니다. 이 예약 된 작업은 로그온 할 때만 실행 됩니다. **CEIP 데이터 수집** 작업은 ue-v 에이전트 설치 디렉터리에 있는 UevSqmSession.exe를 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 이벤트</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Collect CEIP 데이터</p></td>
<td align="left"><p>로그온</p></td>
</tr>
</tbody>
</table>

 

### 응용 프로그램 설정 모니터링

Windows 앱에 대 한 설정을 동기화 하는 데 **응용 프로그램 설정 모니터링** 작업을 사용 합니다. 이는 로그온 할 때 실행 되지만, 로그온 detrimentally에 영향을 주지 않도록 30 초 지연 됩니다. 응용 프로그램 상태 모니터링 작업은 UE-V 에이전트 설치 디렉터리에 있는 UevAppMonitor.exe 파일을 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 이벤트</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Monitor 응용 프로그램 상태</p></td>
<td align="left"><p>로그온</p></td>
</tr>
</tbody>
</table>

 

### 동기화 컨트롤러 응용 프로그램

동기화 컨트롤러 **응용 프로그램** 작업은 동기화 컨트롤러를 시작 하 여 컴퓨터에서 설정 저장소 위치로 설정을 동기화 하는 데 사용 됩니다. 기본적으로 작업은 30 분 마다 실행 됩니다. 해당 시점에 로컬 설정이 설정 저장소 위치와 동기화 되 고 설정 저장소 위치의 업데이트 된 설정이 컴퓨터에 동기화 됩니다. 동기화 컨트롤러 응용 프로그램은 UE-V 에이전트 설치 디렉터리에 있는 Microsoft.Uev.SyncController.exe를 실행 합니다.
**참고:** 이 작업은 **응용 프로그램 설정 모니터링** 작업에 따라 로그온 할 때 실행 되지만, 로그온 detrimentally에 영향을 주지 않도록 30 초 단위로 지연 됩니다.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 이벤트</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Sync 컨트롤러 응용 프로그램</p></td>
<td align="left"><p>로그온 및 30 분 후에 모두</p></td>
</tr>
</tbody>
</table>

 

예를 들어 다음 명령은 기본 30 분 대신 15 분 마다 설정을 동기화 하도록 에이전트를 구성 합니다.

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### 로그 오프할 때 설정 동기화

**로그 오프할 때 설정 동기화** 작업은 ue-v를 사용 하 여 로그 오프할 때 응용 프로그램의 동기화를 제어 하는 로그온 할 때 응용 프로그램을 시작 하는 데 사용 됩니다. 로그 오프할 때 설정 동기화 작업은 UE-V 에이전트 설치 디렉터리에 있는 Microsoft.Uev.SyncController.exe 파일을 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 이벤트</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>로그 오프할 때 설정 \Microsoft\UE-V\Synchronize</p></td>
<td align="left"><p>로그온</p></td>
</tr>
</tbody>
</table>

 

### 서식 파일 자동 업데이트

**서식 파일 자동 업데이트** 작업은 설정 템플릿 카탈로그에서 새 서식 파일, 업데이트 또는 제거 되었는지 확인 합니다. 이 작업은 SettingsTemplateCatalog가 구성 된 경우에만 실행 됩니다. **서식 파일 자동 업데이트** 작업은 ue-v 에이전트 설치 디렉터리에 있는 ApplySettingsCatalog.exe 파일을 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 이벤트</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Template 자동 업데이트</p></td>
<td align="left"><p>시스템 시작 및 3:30 오전 1 시간 창 내 임의 시간에</p></td>
</tr>
</tbody>
</table>

 

**예:** 다음 명령은 UE-V Agent를 구성 하 여 각 시간에 설정 템플릿 카탈로그 저장소를 확인 합니다.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### CEIP 데이터 업로드

사용자나 관리자가 CEIP (사용자 환경 개선 프로그램)에 참여 하도록 선택한 경우 설치 중에 **Ceip 데이터 업로드** 작업이 실행 됩니다. 이 작업은 데이터를 사용 하는 CEIP 서버에 데이터를 업로드 하 여 향후 릴리스의 UE-V를 위해 제품을 개선 하는 데 도움을 줍니다. 이 예약 된 작업은 로그온 시와 4 시간 간격으로 실행 됩니다. **CEIP 데이터 업로드** 작업은 ue-v 에이전트 설치 디렉터리에 있는 UevSqmUploader.exe 파일을 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 이벤트</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Upload CEIP 데이터</p></td>
<td align="left"><p>로그온 및 4 시간 마다</p></td>
</tr>
</tbody>
</table>

 

## UE-V 2 예약 된 작업 세부 정보


다음 차트는 UE-V 2에 대 한 예약 된 작업에 대 한 추가 정보를 제공 합니다.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>작업 이름 </strong> (파일 이름)</p></td>
<td align="left"><p><strong>기본 빈도</strong></p></td>
<td align="left"><p><strong>전원 켜기/끄기</strong></p></td>
<td align="left"><p><strong>유휴 전용</strong></p></td>
<td align="left"><p><strong>네트워크 연결</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>응용 프로그램 설정 모니터링 </strong> (UevAppMonitor.exe)</p></td>
<td align="left"><p>로그온 후 30 초 후에 시작 되며 로그 오프할 때까지 계속 됩니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>Windows (AppX) 앱에 대 한 설정을 동기화 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>동기화 컨트롤러 응용 프로그램 </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>로그온 시와 30 분 마다</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>네트워크가 연결 된 경우에만</p></td>
<td align="left"><p>로컬 설정을 설정 저장소 위치와 동기화 하는 동기화 컨트롤러를 시작 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>로그 오프 </strong> (Microsoft.Uev.SyncController.exe)에서 설정 동기화</p></td>
<td align="left"><p>로그온 할 때 실행 되며, 로그 오프가 설정을 동기화 하기 위해 기다립니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>로그 오프할 때 응용 프로그램의 동기화를 제어 하는 로그온 할 때 응용 프로그램을 시작 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>서식 파일 자동 업데이트 </strong> (ApplySettingsCatalog.exe)</p></td>
<td align="left"><p>초기 로그온 시와 매일 오전 3:30 시에 실행 됩니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>설정 서식 파일 카탈로그에서 새 서식 파일, 업데이트 또는 제거 되었는지 확인 합니다. 이 작업은 SettingsTemplateCatalog가 구성 된 경우에만 실행 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>CEIP 데이터 수집 </strong> (UevSqmSession.exe)</p></td>
<td align="left"><p>로그온 시작 시 서비스</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>사용자 또는 관리자가 CEIP (고객 환경 개선 프로그램)에 opts이 작업은 UE-V 이후 릴리스를 개선 하는 데 도움이 되는 데이터를 수집 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>CEIP 데이터 업로드 </strong> (UevSqmUploader.exe)</p></td>
<td align="left"><p>로그온 할 때마다 실행 되며, 이후 매일 4:00 오전</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>네트워크가 연결 된 경우에만</p></td>
<td align="left"><p>사용자나 관리자가 CEIP (사용자 환경 개선 프로그램)에 opts 경우이 작업을 통해 해당 데이터를 CEIP 서버에 업로드 합니다.</p></td>
</tr>
</tbody>
</table>

 

**Legend**

-   **Power Toggle** -작업 스케줄러는 AC 전원에 연결 되지 않은 경우 전력 소모량을 최적화 합니다. 컴퓨터가 배터리 전원으로 전환 되는 경우 작업이 중지 될 수 있습니다.

-   **유휴 전용** – 컴퓨터가 유휴 상태가 끝나면 작업의 실행이 중지 됩니다. 컴퓨터가 다시 유휴 상태일 때는 기본적으로 작업이 다시 시작 되지 않습니다. 대신 다음 작업 트리거에서 작업을 다시 시작 합니다.

-   **네트워크 연결** – 컴퓨터가 네트워크 연결을 사용할 수 있는 경우에만 "예"로 표시 된 작업을 실행 합니다. 네트워크 연결에 관계 없이 "N/A"로 표시 된 작업을 실행 합니다.

### 예약 된 작업을 관리 하는 방법

예약 된 작업을 찾으려면 다음을 수행 합니다.

1.  사용자 컴퓨터에서 "작업 예약"을 엽니다.

2.  이동: 작업 스케줄러- &gt; 작업 스케줄러 라이브러리- &gt; Microsoft- &gt; ue-v

3.  세부 정보 창에서 관리 하 고 구성 하려는 예약 된 작업을 선택 합니다.

### 추가 정보

UE-V 예약 작업에는 다음과 같은 추가 정보가 적용 됩니다.

-   작업 순서 프로그램은 기본적으로 UE-V Agent 설치 폴더에 있습니다 `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` .

-   UE-V SyncMethod가 "Syncmethod"로 설정 된 경우 동기화 컨트롤러 응용 프로그램 예약 된 작업은 중요 한 구성 요소입니다 (UE-V 2 기본 구성). 이 예약 된 작업은 SettingsSToragePath를 로컬에 캐시 된 설정 패키지 파일 버전과 동기화 상태로 유지 합니다. 사용자가 설정 된 설정이 자주 동기화 되지 않는 경우에는 예약 된 작업 설정을 1 분 정도 줄일 수 있습니다.필요한 경우 30 분 기본값을 더 높은 값으로 늘릴 수도 있습니다. 사용자가 로그온 할 때 설정이 빠른 속도로 동기화 되지 않는 경우에는 예약 된 작업에 대 한 지연 설정을 제거할 수 있습니다. ( **트리거 편집** 대화 상자에서 지연 설정을 찾을 수 있습니다.)

-   다른 방법을 사용 하 여 클라이언트 템플릿을 동기화 된 상태로 유지 하는 경우 (예: 그룹 정책 또는 Configuration Manager 기준) 서식 파일 자동 업데이트 예약 된 작업을 사용 하지 않도록 설정할 필요는 없습니다. SettingsTemplateCatalog 속성 값을 비워 두면 UE-V가 사용자 지정 서식 파일의 설정 카탈로그를 검사 하지 않습니다. 이 예약 된 작업은 ApplySettingsCatalog.exe 실행 되며 기본적으로 즉시 반환 됩니다.

-   예약 된 응용 프로그램 설정 모니터링 작업은 각 앱에 기본 제공 되는 Windows 앱 프로그램 설정 트리거를 기반으로 AppX (Windows 앱) 설정을 실시간으로 업데이트 합니다.






## 관련 항목


[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

[사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





