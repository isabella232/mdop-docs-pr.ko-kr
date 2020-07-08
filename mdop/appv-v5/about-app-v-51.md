---
title: App-V 5.1 정보
description: App-V 5.1 정보
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814948"
---
# App-V 5.1 정보


다음 섹션을 사용 하 여 Application Virtualization (App-v) 5.1에 적용 되는 중요 한 변경 사항에 대 한 정보를 검토 합니다.

[앱-V 5.1 소프트웨어 필수 구성 요소 및 지원 되는 구성](#bkmk-51-prereq-configs)

[App-V 5.1으로 마이그레이션](#bkmk-migrate-to-51)

[앱-V 5.1의 새로운 기능](#bkmk-whatsnew)

[Windows 10 용 app-v 지원](#bkmk-win10support)

[앱-V 관리 콘솔 변경](#bkmk-mgmtconsole)

[Sequencer 개선 사항](#bkmk-seqimprove)

[패키지 변환기 개선](#bkmk-pkgconvimprove)

[단일 이벤트 트리거에서 여러 스크립트에 대 한 지원](#bkmk-supmultscripts)

[설치 폴더에 대 한 하드 코드 경로가 가상 파일 시스템 루트에 리디렉션 됨](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a>앱-V 5.1 소프트웨어 필수 구성 요소 및 지원 되는 구성


앱-V 5.1 소프트웨어 필수 구성 요소 및 지원 되는 구성에 대 한 다음 링크를 참조 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">전제 조건과 지원 되는 구성에 대 한 링크</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)">App-V 5.1 필수 구성 요소</a></p></td>
<td align="left"><p>앱-V 5.1 설치를 시작 하기 전에 설치 해야 하는 필수 구성 요소 소프트웨어</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 지원되는 구성</a></p></td>
<td align="left"><p>App-v Server, Sequencer 및 클라이언트 구성 요소에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항</p></td>
</tr>
</tbody>
</table>



**Configuration Manager For App-V 사용에 대 한 지원:** 앱-V 5.1는 System Center 2012 R2 Configuration Manager SP1을 지원 합니다. 앱-V 환경을 구성 관리자 및 구성 관리자와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager와 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx) 을 참조 하세요.

## <a href="" id="bkmk-migrate-to-51"></a>App-V 5.1으로 마이그레이션


다음 정보를 사용 하 여 이전 버전의 App-v 5.1으로 업그레이드 합니다. 자세한 내용은 [이전 버전에서 앱-V 5.1으로 마이그레이션을](migrating-to-app-v-51-from-a-previous-version.md) 참조 하세요.

### 업그레이드를 시작 하기 전에

업그레이드를 시작 하기 전에 다음 정보를 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">업그레이드 하기 전에 검토할 항목</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>업그레이드할 구성 요소 (순서에 관계 없음)</p></td>
<td align="left"><ol>
<li><p>App-v Server</p></li>
<li><p>않았음이</p></li>
<li><p>앱-V 클라이언트 또는 App-v (원격 데스크톱 서비스) 클라이언트</p></li>
</ol>
<div class="alert">
<strong>참고</strong><br/><p>App-v 5.0 SP2 이전에는 App-v 클라이언트 설치와 함께 클라이언트 관리 UI (사용자 인터페이스)가 제공 되었습니다. App-v 5.0 SP2 설치 (이상)의 경우 <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> 응용 프로그램 가상화 5.0 클라이언트 UI 응용 프로그램에서 다운로드 하 여 클라이언트 관리 UI를 사용할 수 있습니다 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 4. x에서 업그레이드</p></td>
<td align="left"><p>먼저 App-v 5.0으로 업그레이드 해야 합니다. 앱-V 4. x에서 App-v 5.1로 직접 업그레이드할 수 없습니다. 자세한 내용은 다음을 참조하세요.</p>
<ul>
<li><p>"App-v 4.6 및 App-v 5.0"의 차이점에 <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> 대 한 자세한 내용은 ' v e y e 5.0 "</a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">App-V의 이전 버전에서 마이그레이션 계획</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱-V 5.0 이상에서 업그레이드</p></td>
<td align="left"><p>다음 버전 중 하나에서 앱-V 5.1으로 직접 업그레이드할 수 있습니다.</p>
<ul>
<li><p>App-V 5.0</p></li>
<li><p>App-v 5.0 SP1</p></li>
<li><p>App-v 5.0 SP2</p></li>
<li><p>App-v 5.0 SP3</p></li>
</ul>
<p>App-v 5.1으로 업그레이드 하려면이 항목의 나머지 섹션에 나와 있는 단계를 따르세요.</p>
<p>패키지 및 연결 그룹은 현재 사용 중인 앱-V 5.1에서 계속 작동 합니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>앱-V 인프라를 업그레이드 하는 단계

앱-v 인프라의 각 구성 요소를 App-v 5.1으로 업그레이드 하려면 다음 단계를 완료 하세요. 다음 주문은 제안 사항입니다. 구성 요소를 순서에 관계 없이 업그레이드할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">자세한 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1 단계: App-v Server를 업그레이드 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>App-v 서버를 사용 하지 않는 경우에는이 단계를 건너뛰고 다음 단계로 이동 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>다음 단계를 따르세요.</p>
<ol>
<li><p>관리 데이터베이스 및/또는 보고 데이터베이스를 업그레이드 하는 데 사용 하는 방법에 따라 다음 중 하나를 수행 합니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">데이터베이스 업그레이드 방법</th>
<th align="left">단계</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>이 단계를 건너뛰고 2 단계 ("App-v Server를 업그레이드 하는 경우 ...")로 이동 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL 스크립트</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법의 단계를 따릅니다 </a> .</p></td>
</tr>
</tbody>
</table>
<li><p>App-v 5.0 SP1 핫픽스 패키지 3 이상에서 App-v 서버를 업그레이드 하는 경우 <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> app-v 5.0 SP3 서버 설치 후 레지스트리 키 확인 섹션의 단계를 완료 </a> 하세요.</p></li>
<li><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">App-v 5.1 서버를 배포 하는 방법의 단계를 따릅니다.</a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>2 단계: App-v Sequencer를 업그레이드 합니다.</p></td>
<td align="left"><p><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">Sequencer를 설치 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3 단계: App-v 클라이언트 또는 App-v RDS 클라이언트를 업그레이드 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">App-v 클라이언트를 배포 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



### 이전 버전의 App-v를 사용 하 여 만든 패키지 변환

패키지 변환기 유틸리티를 사용 하 여 앱-V 5.0 이전 버전의 app-v를 사용 하 여 만든 가상 응용 프로그램 패키지를 업그레이드 합니다. 패키지 변환기는 PowerShell을 사용 하 여 패키지를 변환 하며 변환이 필요한 패키지가 여러 개 있는 경우 프로세스를 자동화 하는 데 도움이 될 수 있습니다.

**참고**  
App-v 5.1 패키지는 앱-v 5.0 패키지와 정확히 동일 합니다. 버전 간에는 패키지 형식이 변경 되지 않으므로 App-v 5.0 패키지를 App-v 5.1 패키지로 변환할 필요가 없습니다..



## <a href="" id="bkmk-whatsnew"></a>앱-V 5.1의 새로운 기능


이 섹션은 app-v에 이미 익숙한 사용자를 위한 것 이며 App-v 5.1에서 변경 된 내용을 알아야 합니다. App-v에 익숙하지 않은 경우 [에는 앱-v 5.1에 대 한 읽기 계획](planning-for-app-v-51.md)부터 시작 해야 합니다.

### <a href="" id="bkmk-win10support"></a>Windows 10 용 app-v 지원

다음 표에는 App-v에 대 한 Windows 10 지원이 나와 있습니다. 앱-V 5.1 이전 버전의 App-v에서는 Windows 10이 지원 되지 않습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">구성 요소</th>
<th align="left">App-V 5.1</th>
<th align="left">App-V 5.0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 클라이언트</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v RDS 클라이언트</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 시퀀서</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a>앱-V 관리 콘솔 변경

이 섹션에서는 App-v 관리 콘솔의 현재 기능과 이전 기능을 비교 합니다.

### Silverlight는 더 이상 필요 하지 않습니다.

관리 콘솔 UI에 더 이상 Silverlight가 필요 하지 않습니다. 5.1 관리 콘솔은 HTML5 및 Javascript에 빌드됩니다.

### 알림 및 메시지가 대화 상자에 개별적으로 표시 됨

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">앱의 새로운 기능-V 5.1</th>
<th align="left">앱-V 5.1 이전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>메시지 표시기 수:</strong></p>
<p>앱-V 관리 콘솔의 제목 표시줄에서 플래그 아이콘 옆에 번호가 표시 되어 읽으려는 메시지 수를 나타냅니다.</p></td>
<td align="left"><p>메시지 또는 오류를 한 번에 하나만 볼 수 있으며 메시지 수를 확인할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>메시지 모양:</strong></p>
<ul>
<li><p>사용자 입력이 필요한 메시지가 표시 되는 현재 페이지의 맨 위에 표시 되는 별도의 대화 상자에 나타나고 해당 메시지를 해제 하기 전에 응답이 필요 합니다.</p></li>
<li><p>메시지와 오류는 목록에 표시 되 고, 다른 하나 아래에는 나열 됩니다.</p></li>
</ul></td>
<td align="left"><p>한 번에 하나의 메시지나 오류만 볼 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>메시지 해제:</strong></p>
<p><strong>모두 해제 링크를 사용 하 여 한 번에 </strong> 모든 메시지 및 오류를 해제 하거나 한 번에 하나씩 해제 합니다.</p></td>
<td align="left"><p>메시지 및 오류를 한 번에 하나씩만 해제할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



### 이제 콘솔 페이지는 별도의 Url입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">앱의 새로운 기능-V 5.1</th>
<th align="left">앱-V 5.1 이전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>콘솔의 각 페이지에는 다른 URL이 있으므로, 앞으로 빠르게 액세스할 수 있도록 특정 페이지에 책갈피를 지정 합니다.</p>
<p>일부 Url에 표시 되는 번호는 특정 패키지를 나타냅니다. 이러한 번호는 고유 합니다.</p></td>
<td align="left"><p>모든 콘솔 페이지에는 같은 URL을 통해 액세스 합니다.</p></td>
</tr>
</tbody>
</table>



### 새로 만들기, 별도의 연결 그룹 페이지 및 메뉴 옵션

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">앱의 새로운 기능-V 5.1</th>
<th align="left">앱-V 5.1 이전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>연결 그룹 페이지는 이제 패키지 페이지와 동일한 수준에 있는 주 메뉴의 일부입니다.</p></td>
<td align="left"><p>연결 그룹 페이지를 열려면 패키지 페이지를 탐색 합니다.</p></td>
</tr>
</tbody>
</table>



### 패키지에 대 한 메뉴 옵션 변경 됨

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">앱의 새로운 기능-V 5.1</th>
<th align="left">앱-V 5.1 이전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>다음 옵션은 이제 패키지 페이지 아래쪽에 표시 되는 단추입니다.</p>
<ul>
<li><p>추가 또는 업그레이드</p></li>
<li><p>게시</p></li>
<li><p>문서만</p></li>
<li><p>삭제</p></li>
</ul>
<p>드롭다운 상황에 맞는 메뉴를 열려면 패키지를 마우스 오른쪽 단추로 클릭 하면 다음 옵션이 계속 표시 됩니다.</p>
<ul>
<li><p>게시</p></li>
<li><p>문서만</p></li>
<li><p>광고 액세스 편집</p></li>
<li><p>배포 구성 편집</p></li>
<li><p>배포 구성 전송</p></li>
<li><p>다음에서 액세스 및 구성 전송 ...</p></li>
<li><p>삭제</p></li>
</ul>
<p><strong>삭제 </strong> 를 클릭 하 여 패키지를 제거 하면 대화 상자가 열리고 패키지를 삭제할 것인지 묻는 메시지가 표시 됩니다.</p></td>
<td align="left"><p><strong>추가 또는 업그레이드 </strong> 옵션은 패키지 페이지 오른쪽 위에 있는 단추입니다.</p>
<p><strong>게시 </strong> , 게시 <strong> 취소 </strong> 및 <strong> 삭제 옵션은 </strong> 패키지 목록에서 패키지 이름을 마우스 오른쪽 단추로 클릭 한 경우에만 사용할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>다음 패키지 작업은 이제 각 패키지에 대 한 패키지 세부 정보 페이지의 단추입니다.</p>
<ul>
<li><p>전송 (다음 옵션을 사용 하 여 드롭다운 메뉴):</p>
<ul>
<li><p>배포 구성 전송</p></li>
<li><p>다음에서 액세스 및 구성 전송 ...</p></li>
</ul></li>
<li><p>편집 (연결 그룹 및 광고 액세스)</p></li>
<li><p>문서만</p></li>
<li><p>삭제</p></li>
<li><p>기본 구성 편집</p></li>
</ul></td>
<td align="left"><p>이러한 패키지 옵션은 패키지 목록에서 패키지 이름을 마우스 오른쪽 단추로 클릭 한 경우에만 사용할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



### 왼쪽 창의 아이콘에는 새로운 색과 텍스트가 있습니다.

왼쪽 창의 아이콘 색과 추가 된 텍스트가 변경 되어 다른 Microsoft 제품에서 아이콘을 일관 되 게 만들 수 있습니다.

### 개요 페이지가 제거 되었습니다.

관리 콘솔의 왼쪽 창에서 개요 메뉴 옵션 및 관련 개요 페이지가 제거 되었습니다.

### <a href="" id="bkmk-seqimprove"></a>Sequencer 개선 사항

App-v 5.1 Sequencer의 패키지 편집기에 다음 개선 사항이 적용 되었습니다.

### 매니페스트 파일 가져오기 및 내보내기

AppxManifest.xml 파일을 가져오고 내보낼 수 있습니다. 매니페스트 파일을 내보내려면 **고급** 탭을 선택 하 고 매니페스트 파일 상자에서 **내보내기를**클릭 합니다. 셸 확장 제거 또는 파일 형식 연결 편집과 같은 매니페스트 파일을 변경할 수 있습니다.

변경 작업을 수행한 후 **가져오기** ...를 클릭 하 고 편집한 파일을 선택 합니다. 성공적으로 다시 가져오면 매니페스트 파일이 패키지 편집기 내에서 즉시 업데이트 됩니다.

**주의**  
파일을 가져올 때 XML 스키마를 기준으로 변경 내용의 유효성을 검사 합니다. 파일이 유효 하지 않으면 오류가 표시 됩니다. XML 스키마에 대해 유효성을 검사 했지만 다른 이유 때문에 여전히 실행 되지 않을 수 있는 파일을 가져올 수 있다는 점에 유의 하세요.



### Windows 10에서 운영 체제 목록 추가

배포 탭에서 패키지를 시퀀싱 할 수 있는 운영 체제 목록에 Windows 10 32 비트 및 Windows 10-64 비트가 추가 되었습니다. **운영 체제**를 선택 하면 Windows 10이 시퀀싱 된 패키지에서 지원 되는 운영 체제에 자동으로 포함 됩니다.

### 가상 레지스트리 편집기의 맨 아래에 표시 되는 현재 경로

이제 가상 레지스트리 탭의 경로가 가상 레지스트리 편집기의 맨 아래에 표시 되며,이를 통해 현재 선택 된 키를 확인할 수 있습니다. 이전에는 레지스트리 트리를 스크롤하여 현재 선택 된 키를 찾아야 했습니다.

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a>가상 레지스트리 편집기에 추가 된 "찾기 및 바꾸기" 대화 상자 및 바로 가기 키 조합

가상 레지스트리 편집기에서 찾기 옵션 (Ctrl + F)에 대 한 바로 가기 키가 추가 되 고 "찾기" 및 "바꾸기" 작업을 결합 하 여 값과 데이터를 찾고 바꿀 수 있는 대화 상자가 추가 되었습니다. 이 결합 된 대화 상자에 액세스 하려면 키를 선택 하 고 다음 중 하나를 수행 합니다.

-   **Ctrl + H** 를 누릅니다.

-   키를 마우스 오른쪽 단추로 클릭 하 고 **바꾸기를**선택 합니다.

-   **View** &gt; **가상 레지스트리** &gt; **바꾸기**보기를 선택 합니다.

이전에는 "바꾸기" 대화 상자가 없으므로 수동으로 변경 해야 합니다.

### 레지스트리 키와 패키지 파일의 이름을 변경 했습니다.

Sequencer 문제 없이 가상 레지스트리 키 및 파일의 이름을 바꿀 수 있습니다. 이전에는 키 이름을 바꾸려고 하면 Sequencer가 작동을 중지 했습니다.

### 가상 레지스트리 키 가져오기 및 내보내기

가상 레지스트리 키를 가져오고 내보낼 수 있습니다. 키를 가져오려면 키를 가져올 노드를 마우스 오른쪽 단추로 클릭 하 고 가져올 키로 이동한 다음 **가져오기를**클릭 합니다. 키를 내보내려면 키를 마우스 오른쪽 단추로 클릭 하 고 **내보내기를**선택 합니다.

### 가상 파일 시스템으로 디렉터리 가져오기

디렉터리를 VFS로 가져올 수 있습니다. 디렉터리를 가져오려면 **패키지 파일** 탭을 클릭 한 다음 **View** &gt; **가상 파일 시스템** &gt; **가져오기 디렉터리**보기를 클릭 합니다. 이미 VFS에 있는 파일을 포함 하는 디렉터리를 가져오려고 하면 가져오기에 실패 하 고 설명 메시지가 표시 됩니다. App-v 5.1 이전에는 디렉토리를 가져올 수 없습니다.

### 삭제할 필요 없이 VFS 파일을 가져오거나 내보내어 패키지에 다시 추가

파일을 삭제 한 다음 패키지에 다시 추가할 필요 없이 VFS에서 파일을 가져오거나 파일을 내보낼 수 있습니다. 예를 들어이 기능을 사용 하 여 변경 로그를 로컬 드라이브로 내보내고, 외부 편집기를 사용 하 여 파일을 편집 하 고, 파일을 VFS로 다시 가져올 수 있습니다.

파일을 내보내려면 **패키지 파일** 탭을 선택 하 고 VFS에서 파일을 마우스 오른쪽 단추로 클릭 하 고 **내보내기를**클릭 한 다음 편집을 수행할 수 있는 내보내기 위치를 선택 합니다.

파일을 가져오려면 **패키지 파일** 탭을 선택 하 고 내보낸 파일을 마우스 오른쪽 단추로 클릭 합니다. 편집한 파일을 찾은 다음 **가져오기를**클릭 합니다. 가져온 파일은 기존 파일을 덮어쓰게 됩니다.

파일을 가져온 후에는 **파일** 저장을 클릭 하 여 패키지를 저장 해야 합니다 &gt; **Save**.

### 패키지 파일 추가 메뉴가 이동 됨

패키지 파일을 추가 하기 위한 메뉴 옵션이 이동 되었습니다. 추가 옵션을 찾으려면 **패키지 파일** 탭을 선택한 다음 **View** &gt; **가상 파일 시스템** &gt; **추가 파일**보기를 클릭 합니다. 이전에는 VFS 노드에서 폴더를 마우스 오른쪽 단추로 클릭 하 고 **파일 추가**를 선택 했습니다.

### 가상 레지스트리 노드는 기본적으로 컴퓨터 및 사용자 하이브를 확장 합니다.

가상 레지스트리를 열면 컴퓨터 및 사용자 하이브는 최상위 수준 레지스트리 노드 아래에 표시 됩니다. 이전에는 레지스트리 노드를 확장 하 여 아래에 있는 하이브를 표시 했습니다.

### 브라우저 도우미 개체 사용 또는 사용 안 함

시퀀서 사용자 인터페이스의 고급 탭에서 새 확인란을 선택 하 고 브라우저 도우미 개체를 사용 하도록 설정 하 여 브라우저 도우미 개체를 사용 하거나 사용 하지 않도록 설정할 수 있습니다. 브라우저 도우미 개체:

-   패키지에 존재 하 고 사용 하도록 설정 되어 있으면 기본적으로 확인란이 선택 되어 있습니다.

-   패키지에 존재 하며 사용 하지 않도록 설정 된 경우 확인란은 기본적으로 선택 되어 있지 않습니다.

-   패키지에 하나 이상의 사용 가능 및 하나 이상의 사용 안 함이 있으면 기본적으로 확인란이 확정 되지 않음으로 설정 되어 있습니다.

-   패키지에 없는 경우 확인란을 사용할 수 없습니다.

### <a href="" id="bkmk-pkgconvimprove"></a>패키지 변환기 개선

이제 패키지 변환기를 사용 하 여 스크립트를 포함 하는 App-v 4.6 패키지를 변환할 수 있으며, 이제 원본 osd 파일의 레지스트리 정보와 스크립트가 패키지 변환기 출력에 포함 됩니다.

예제를 비롯 한 자세한 내용은 [이전 버전에서 앱-V 5.1으로 마이그레이션을](migrating-to-app-v-51-from-a-previous-version.md)참조 하세요.

### <a href="" id="bkmk-supmultscripts"></a>단일 이벤트 트리거에서 여러 스크립트에 대 한 지원

App-v 5.1는 app-v 4.6에서 App-v 5.0 이상으로 변환 하는 패키지를 포함 하 여 앱-V 패키지에 대 한 단일 이벤트 트리거에서 여러 스크립트의 사용을 지원 합니다. 여러 스크립트를 사용할 수 있도록 앱-V 5.1는 App-v 클라이언트 설치의 일부로 설치 되는 ScriptRunner.exe 라는 스크립트 시작 관리자 응용 프로그램을 사용 합니다.

이벤트 트리거 목록과 스크립트를 실행할 수 있는 컨텍스트를 비롯 한 자세한 내용은 [app-v 5.1 동적 구성에 대 한](about-app-v-51-dynamic-configuration.md)스크립트 섹션을 참조 하세요.

### <a href="" id="bkmk-hardcodepath"></a>설치 폴더에 대 한 하드 코드 경로가 가상 파일 시스템 루트에 리디렉션 됨

앱-V 4.6에서 5.1로 패키지를 변환할 때 앱-V 5.1 패키지는 4.6 패키지를 만들 때 사용 하는 데 필요한 하드 코드 된 드라이브에 액세스할 수 있습니다. 드라이브 문자는 4.6 시퀀싱 시스템에서 설치 드라이브로 선택한 드라이브입니다. (기본 드라이브 문자는 Q:\\.)

이전에는 4.6 루트 폴더가 인식 되지 않고 App-v 5.0 패키지에서 액세스할 수 없었습니다. App-v 5.1 패키지는 전체 경로로 하드 코드 된 파일에 액세스 하거나 App-v 4.6 설치 루트 아래의 파일을 프로그래밍 방식으로 열거할 수 있습니다.

**기술 정보:** App-v 5.1 패키지 변환기는 Filesystem 요소의 FilesystemMetadata.xml 파일에 App-v 4.6 설치 루트 폴더와 짧은 폴더 이름을 저장 합니다. App-v 5.1 클라이언트는 가상 프로세스를 만들 때 앱-V 4.6 설치 루트의 요청을 가상 파일 시스템 루트에 매핑합니다.

## MDOP 기술을 활용 하는 방법


앱-V는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.






## 관련 항목


[App-V 5.1 릴리스 정보](release-notes-for-app-v-51.md)









