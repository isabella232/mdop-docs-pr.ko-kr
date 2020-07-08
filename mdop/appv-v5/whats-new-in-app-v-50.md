---
title: App-V 5.0의 새로운 기능
description: App-V 5.0의 새로운 기능
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813220"
---
# App-V 5.0의 새로운 기능


이 섹션은 app-v에 대해 잘 알고 있고 App-v 5.0에서 변경 된 내용을 알고 싶은 사용자를 위한 것입니다. App-v에 익숙하지 않은 경우 앱-v [5.0에 대 한 읽기 계획](planning-for-app-v-50-rc.md)부터 시작 해야 합니다.

## 표준 기능 변경


다음 섹션에는 앱-V 5.0의 표준 기능 변경 사항에 대 한 정보가 포함 되어 있습니다.

### 지원 되는 운영 체제 변경

자세한 내용은 [앱-V 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.

## Sequencer 변경


다음 섹션에는 App-v 5.0 sequencer의 변경 사항에 대 한 정보가 포함 되어 있습니다.

### 시퀀서에 대 한 특정 변경

다음 표에서는 App-v 5.0 sequencer로 변경 된 사항에 대 한 정보를 보여 줍니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sequencer 기능</th>
<th align="left">App-v 5.0 Sequencer 기능</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>다시 부팅 처리</p></td>
<td align="left"><p>응용 프로그램이 다시 시작에 대 한 메시지를 표시 하는 경우 응용 프로그램에서 sequencer를 실행 하는 컴퓨터를 다시 시작 하도록 허용 해야 합니다. Sequencer를 실행 하는 컴퓨터는 다시 시작 되 고 sequencer는 모니터링 모드로 다시 시작 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>가상 응용 프로그램 디렉터리 지정</p></td>
<td align="left"><p>가상 응용 프로그램 디렉터리는 필수 매개 변수입니다. 최상의 결과를 위해서는 응용 프로그램 설치 관리자의 설치 디렉터리와 일치 해야 합니다. 이로 인해 성능이 최적화 되 고 응용 프로그램 호환성이 향상 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>편집 바로 가기/FTAs</p></td>
<td align="left"><p><strong> </strong> 시퀀싱 마법사를 완료 한 후에 고급 편집 페이지의 바로 가기/FTA 페이지가 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>변경 기록 탭</p></td>
<td align="left"><p>앱-V 5.0에 대 한 변경 내용 탭이 제거 되었습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OSD탭</p></td>
<td align="left"><p>OSD 탭이 App-v 5.0 용으로 제거 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>가상 서비스 탭</p></td>
<td align="left"><p>앱-V 5.0에 대 한 가상 서비스 탭이 제거 되었습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>파일/가상 파일 시스템 탭</p></td>
<td align="left"><p>이러한 탭을 결합 하 여 패키지 파일을 수정할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>배포 탭</p></td>
<td align="left"><p>패키지에서 서버 URL을 구성 하는 옵션이 더 이상 없습니다. 배포 구성 또는 관리 서버를 사용 하 여 지금이를 구성 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지 변환기 도구</p></td>
<td align="left"><p>이제 PowerShell을 사용 하 여 이전 버전에서 만든 패키지를 변환할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>추가 기능/미들웨어</p></td>
<td align="left"><p>추가 기능 또는 미들웨어 응용 프로그램을 시퀀싱 하는 경우 부모 패키지를 확장할 수 있습니다. 앱-V 5.0의 연결 그룹을 사용 하 여 추가 기능 및 미들웨어 패키지를 연결 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>파일 출력</p></td>
<td align="left"><p>앱-V 5.0, Windows Installer (.msi), appv, 배포 구성, 사용자 구성 및 Report.XML으로 생성 되는 파일은 다음과 같습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>압축/보안 설명자/MSI 패키지</p></td>
<td align="left"><p>Windows Installer (.msi) 파일의 압축 및 만들기는 모든 패키지에 대해 자동 이므로 더 이상 보안 설명자를 재정의할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>도구/옵션</p></td>
<td align="left"><p>진단 창이 제거 되었으며 다른 몇 가지 설정도 포함 되어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설치 드라이브</p></td>
<td align="left"><p>설치 드라이브는 응용 프로그램을 설치할 때 더 이상 필요 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OOS 스트리밍</p></td>
<td align="left"><p>스트림 최적화가 수행 되지 않으면 앱이 시작 될 때까지 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 요청 하는 경우 패키지에서 스트림 오류가 발생 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Q: &lt; /p&gt;</td>
<td align="left"><p>App-v 5.0는 기본 파일 시스템을 사용 하며 더 이상 Q:. 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

## 시퀀싱 오류 감지


App-v 5.0 시퀀서는 시퀀싱 중에 일반적인 시퀀싱 문제를 검색할 수 있습니다. 시퀀싱 마법사의 끝에 있는 **설치 보고서** 페이지에는 문제의 심각도에 따라 **오류**, **경고**및 **정보** 로 분류 된 진단 메시지가 표시 됩니다.

이벤트에 대 한 자세한 정보를 표시 하려면 보고서에서 검토 하려는 항목을 두 번 클릭 합니다. 시퀀싱 문제는 물론 문제를 해결 하는 방법에 대 한 제안이 표시 됩니다. 패키지 만들기를 완료 하면 시스템 준비 보고서 및 설치 보고서의 정보가 요약 됩니다. 다음 목록에는 보고서에서 사용할 수 있는 문제의 유형이 표시 됩니다.

-   제외 된 파일.

-   드라이버 정보.

-   COM + 시스템 차이점.

-   나란히 (SxS) 충돌

-   셸 확장.

-   지원 되지 않는 서비스에 대 한 정보입니다.

-   DCOM-IN.

## 연결 그룹


이전에 **동적 도구 모음 컴퍼지션** 으로 알려진 app-v 기능을 이제 app-v 5.0의 **연결 그룹** 이라고 합니다. 연결 그룹 사용에 대 한 자세한 내용은 [연결 그룹 관리](managing-connection-groups.md)를 참조 하세요.

## 라이선스 및 계량 기능


Application 및 라이선스 기능은 App-v 5.0에서 제거 되었습니다. 사용자 환경의 실제 라이선스 위치는 관련 라이선스 조건에서 부여한 특정 소프트웨어 타이틀 라이선스 및 사용 권한에 따라 달라 집니다.

## 파일 및 응용 프로그램 캐시


App-v 5.0에서 사용할 수 있는 파일 또는 응용 프로그램 캐시가 없습니다.






## 관련 항목


[App-V 5.0 정보](about-app-v-50.md)

 

 





