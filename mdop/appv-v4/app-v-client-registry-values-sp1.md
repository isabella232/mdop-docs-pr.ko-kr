---
title: App-V Client 레지스트리 값
description: App-V Client 레지스트리 값
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819808"
---
# App-V Client 레지스트리 값


Microsoft App-v (Application Virtualization) 클라이언트는 레지스트리에 구성을 저장 합니다. 레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다. 레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다. 이 항목에서는 모든 App-v (Application Virtualization) 클라이언트 레지스트리 키와 사용에 대해 설명 합니다.

**중요**  
64 비트 운영 체제를 실행 하는 컴퓨터에서 다음 섹션에 설명 된 키와 값이 HKEY \ _LOCAL \ _MACHINE에 있습니다. \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.



## 구성 키


다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">유형</th>
<th align="left">데이터 (예제)</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Microsoft Application Virtualization 데스크톱 클라이언트</p></td>
<td align="left"><p>수정 하지 마세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>버전 </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>4.5.0.xxx </p></td>
<td align="left"><p>수정 하지 마세요. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>드라이버 </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>Sftfs.sys </p></td>
<td align="left"><p>이 키 값이 있으면 마지막으로 코어를 시작 했을 때 중지 오류를 일으킨 드라이버의 이름을 포함 합니다. 중지 오류를 해결 한 후에는이 키 값을 삭제 하 여 sftlist를 시작할 수 있도록 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>InstallPath </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>기본값 = C:\Program Files\Microsoft 응용 프로그램 가상화 클라이언트</p></td>
<td align="left"><p>클라이언트가 설치 된 위치입니다. 수정 하지 마세요. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFileName </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>Default = CSIDL_COMMON_APPDATA \Microsoft\Application 가상화 Client\sftlog.txt</p></td>
<td align="left"><p>클라이언트 로그 파일의 경로 및 이름입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>앱-V 4.6, SP1 보다 이전 버전을 실행 중이 고 로그 파일 이름 또는 위치를 수정한 경우에는 sftlist 서비스를 다시 시작 해야 변경 내용이 적용 됩니다.</p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>로그 인 Min심각도 </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 4, 정보</p></td>
<td align="left"><p>로그에 기록할 메시지를 제어 합니다. 값은 기록 되는 항목의 임계값을 나타내며, 해당 값 보다 작거나 같은 모든 항목은 기록 됩니다. 예를 들어 0x3 (경고) 값은 경고 (0x3), 오류 (0x2) 및 치명적 오류 (0x1)가 기록 됨을 나타냅니다.</p>
<p>값 범위: 0x0 = 없음, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (기본값), 0x5 = Verbose입니다.</p>
<p>로그 수준은 Application Virtualization (App-v) 클라이언트 콘솔과 명령 프롬프트에서 구성할 수 있습니다. 명령 프롬프트에서 명령이/verboselog를 sftlist.exe 하면 로그 수준이 verbose로 증가 합니다. 명령줄 세부 정보에 대 한 자세한 내용은 다음을 참조 하세요.</p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogRolloverCount</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 4</p></td>
<td align="left"><p>다시 설정 될 때 보관 되는 로그 파일의 백업 복사본 수를 정의 합니다. 유효한 범위는 0 – 9999입니다. 기본값은 4입니다. 값이 0 이면 복사본이 보존 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>로그 Maxsize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 256</p></td>
<td align="left"><p>로그 파일이 다시 설정 되기 전에 커질 수 있는 최대 크기를 mb 단위로 정의 합니다. 기본 크기는 256 MB입니다. 이 크기에 도달 하면 다음 쓰기 시도 시 로그 재설정이 강제 적용 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SystemEventLogLevel</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Default = 0x4 (App-V 4.5)</p>
<p>기본값 = 0x3 (App-V 4.6)</p></td>
<td align="left"><p>로그 메시지가 NT 이벤트 로그에 기록 되는 로깅 수준을 나타냅니다. 값은 기록 되는 항목의 임계값 (즉, 해당 값과 같거나 작은 모든 항목은 기록 됨)을 나타냅니다. 예를 들어 0x3 (경고) 값은 경고 (0x3), 오류 (0x2) 및 치명적 오류 (0x1)가 기록 됨을 나타냅니다.</p>
<p>값 범위</p>
<p>0x0 = 없음</p>
<p>0x1 = 중요</p>
<p>0x2 = 오류</p>
<p>0x3 = 경고</p>
<p>0x4 = 정보 (기본값)</p>
<p>0x5 = Verbose</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowIndependentFileStreaming</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>클라이언트가 APPLICATIONSOURCEROOT 매개 변수를 사용 하 여 구성 된 방식에 관계 없이 파일에서 스트리밍을 사용할 수 있는지 여부를 나타냅니다. FALSE로 설정 된 경우 OSD HREF 또는 APPLICATIONSOURCEROOT 매개 변수에 파일 경로가 포함 된 경우에도 트랜스포트가 파일에서 스트리밍을 사용할 수 없게 됩니다.</p>
<p>0x0 = False (기본값)</p>
<p>0x1 = True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ApplicationSourceRoot</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps</p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p>파일://\uncserver\share\prodapps</p>
<p>파일://\uncserver\share</p></td>
<td align="left"><p>관리자 또는 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 토폴로지 관리 체계에 따라 응용 프로그램 로딩을 수행 하도록 합니다. 이 키 값을 사용 하 여 응용 프로그램의 HREF 요소 (예: 원본 위치)에 대 한 OSD CODEBASE를 재정의 합니다. 응용 프로그램 원본 루트는 Url 및 UNC (범용 명명 규칙) 경로 형식을 지원 합니다.</p>
<p>URL 경로의 올바른 형식은 프로토콜://servername: [port] [/path] [/], 여기서 port와 path는 선택 사항입니다. 포트를 지정 하지 않으면 프로토콜에 대 한 기본 포트가 사용 됩니다. OSD URL의//server: port 부분만 대체 되는 프로토콜: </p>
<p>UNC 경로에 대 한 올바른 형식은 \computername. 폴더 [folder] []입니다. 여기서 폴더는 선택 사항입니다. 컴퓨터 이름은 FQDN (정규화 된 도메인 이름) 또는 IP 주소이 될 수 있으며, sharefolder는 드라이브 문자 일 수 있습니다. OSD 경로의 \computernameatesharefolder 또는 drive letter 부분만 대체 됩니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>OSDSourceRoot</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computer\ 내용</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>관리자가 게시 하는 동안 시퀀싱 된 응용 프로그램 패키지에 대 한 OSD 파일 검색의 원본 위치를 지정할 수 있도록 합니다. OSDSourceRoot에 허용 되는 형식에는 UNC 경로 및 Url (http 또는 https)이 포함 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IconSourceRoot</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computer\ 내용</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>관리자가 게시 하는 동안 시퀀싱 된 응용 프로그램 패키지의 아이콘 파일 검색에 대 한 원본 위치를 지정할 수 있도록 합니다. IconSourceRoot에 허용 되는 형식에는 UNC 경로 및 Url (http 또는 https)이 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoadTriggers</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 5</p></td>
<td align="left"><p>AutoLoad는 가상화 된 응용 프로그램의 보조 기능 블록을 백그라운드에서 자동으로 클라이언트로 스트리밍할 수 있도록 하는 클라이언트 런타임 정책 구성 매개 변수입니다. AutoLoad 트리거는 응용 프로그램의 자동 로드를 시작 하는 이벤트를 나타내기 위한 플래그입니다. AutoLoad는 백그라운드 스트리밍을 사용 하 여 응용 프로그램을 캐시에 완전히 로드할 수 있도록 합니다. 기본 기능 블록이 먼저 로드 되 고, 응용 프로그램과의 사용자 조작 등의 포그라운드 작업을 수행 하기 위해 나머지 기능 블록이 백그라운드에 로드 되 고 최적의 성능을 제공 합니다.</p>
<p>비트 마스크 값:</p>
<p>(0) Never: 비트가 설정 되어 있지 않으면 (값이 0), 트리거가 설정 되지 않았으므로 자동 로드를 수행 하지 않습니다.</p>
<p>(1) OnLaunch: 로드는 사용자가 응용 프로그램을 시작할 때 시작 됩니다.</p>
<p>(2) OnRefresh: 로드는 응용 프로그램을 게시할 때 시작 됩니다. 이는 게시 새로 고침이 발생 하는 등의 경우와 같이 패키지 레코드가 추가 되거나 업데이트 될 때마다 발생 합니다.</p>
<p>(4) OnLogin: 사용자가 로그인 할 때 로드가 시작 됩니다.</p>
<p>(5) OnLaunch 및 Onlaunch: Default.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AutoLoadTarget</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>지정 된 AutoLoad 트리거가 발생할 때 자동으로 로드 되는 항목을 나타냅니다. 비트 마스크 값:</p>
<p>(0) 없음: 어떤 트리거가 설정 될 수 있는지에 관계 없이 자동으로 로드 되지 않습니다.</p>
<p>(1) PreviouslyUsed (기본값): AutoLoad trigger를 사용 하는 경우 패키지에서 하나 이상의 응용 프로그램이 이미 사용 된 패키지 (즉, 시작 됨 또는 precached)만 로드 합니다.</p>
<p>(2) 모두: AutoLoad trigger를 사용 하는 경우 패키지 (패키지 당) 또는 모든 패키지 (클라이언트에 대해 설정)의 모든 응용 프로그램이 시작 된 적이 없는지 여부에 관계 없이 자동으로 로드 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RequireAuthorizationIfCached</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>응용 프로그램이 이미 캐시에 있는지 여부에 관계 없이 항상 인증이 필요 함을 나타냅니다. 가능한 값:</p>
<p>0 = False: 항상 서버 연결을 시도 합니다. 서버에 대 한 연결을 설정할 수 없는 경우에도 클라이언트는 사용자가 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 있도록 허용 합니다.</p>
<p>1 = True (기본값): 응용 프로그램을 시작할 때 항상 권한을 부여 해야 합니다. RTSP로 스트리밍된 응용 프로그램의 경우 인증을 위해 사용자 인증 토큰이 서버로 전송 됩니다. 파일 기반 응용 프로그램의 경우 파일 Acl은 사용자가 응용 프로그램에 액세스할 수 있는지 여부를 제어 합니다.</p>
<p>변경 내용을 적용 하려면 sftlist 서비스를 다시 시작 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserDataDirectory </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>APPDATA</p></td>
<td align="left"><p>아이콘 캐시와 사용자 설정이 저장 되는 위치입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalDataDirectory </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>C:\Users\Public\Documents </p></td>
<td align="left"><p>OSD 파일에 대 한 캐시, 아이콘 파일, 바로 가기 정보 및 .ini 파일과 같은 SystemGuard 리소스를 포함 하 여 전역 App-v 데이터에 사용할 디렉터리입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowCrashes </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0 또는 1 </p></td>
<td align="left"><p>Default = 0: 값 0은 클라이언트가 내부 프로그램 예외를 catch 하 여 충돌이 발생할 경우 다른 사용자 응용 프로그램이 복구 하 고 계속할 수 있도록 하는 것을 의미 합니다. 값 1은 클라이언트에서 내부 프로그램 예외가 발생 하 여 디버거에서 캡처할 수 있다는 것을 의미 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CoreInternalTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>60</p></td>
<td align="left"><p>코어와 프런트 엔드 간의 내부 IPC 요청에 대 한 제한 시간 (초)입니다. 수정 하지 마세요. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DefaultSuiteCombineTime </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1천만</p></td>
<td align="left"><p>이 값을 사용 하 여 프로그램이 종료 되는 시간을 표시 하 고 동일한 도구 모음의 다른 응용 프로그램이 실행 되는 동안에는 오류 메시지가 생성 되지 않도록 할 수 있습니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SerializedSuiteLaunchTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 60000</p></td>
<td align="left"><p>클라이언트가 프로그램을 직렬화 하는 데 걸리는 시간 (밀리초)을 동일한 도구 모음에서 정의 합니다. 클라이언트가 시간 초과 되 면 프로그램 시작은 계속 되지만 직렬화 되지 않습니다. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ScriptTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>300</p></td>
<td align="left"><p>WAIT = TRUE 일 경우 OSD 파일의 스크립트에 대 한 기본 제한 시간 (초)입니다. WAIT 대신 TIMEOUT을 사용 하 여 스크립트 단위 시간 제한을 지정할 수 있습니다. 값 0은 기다리지 않음을 의미 하 고 0xFFFFFFFF는 영원히 대기 합니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordLogPath </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p></p></td>
<td align="left"><p>HKLM 또는 HKCU에이 값이 로그 파일에 대 한 유효한 경로를 포함 하는 경우, 프로그램을 시작 하 고, 종료 하 고, 시작 하지 못하거나, 연결이 끊긴 모드를 입력 하거나 종료할 때 Ft트레이가이 로그에 기록 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LaunchRecordMask </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x1A (26) 시작 오류 및 연결 끊김 모드 항목과 종료 활동을 기록 합니다.</p>
<p>0x1F (31)는 모든 것을 기록 합니다.</p>
<p>0x0 (0)은 아무것도 기록 하지 않습니다. </p></td>
<td align="left"><p>다섯 가지 이벤트 (비트 마스크 값) 중에서 어떤 것을 기록 하도록 지정 합니다.</p>
<p>프로그램이 시작 되는 경우 1</p>
<p>2 시작 실패 오류</p>
<p>시스템 종료 4</p>
<p>연결이 끊긴 모드를 시작 하는 방법 8</p>
<p>16 연결이 끊긴 모드를 종료 하 고 서버에 다시 연결</p>
<p>이러한 숫자의 조합을 추가 하 여 각 메시지를 켭니다. 0x1F가 레지스트리에 없으면 기본값으로 설정 됩니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordWriteTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 3000</p></td>
<td align="left"><p>다른 프로세스에서 사용 중인 레코드 로그에 쓰려고 할 때 트레이가 대기 하는 시간 (밀리초)을 지정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ImportSearchPath </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>d:\files; C:\documents 및 settings\user1\SFTs </p></td>
<td align="left"><p>디렉터리를 선택 하도록 사용자에 게 요청 하기 전에 이동식 SFT 파일을 검색 하는 최대 5 개 디렉터리의 세미콜론으로 구분 된 목록입니다. 경로의 후행 백슬래시는 선택 사항입니다. 이 값은 기본적으로 제공 되지 않으며 수동으로 설정 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserImportPath</p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>D:\SFTs\ </p></td>
<td align="left"><p>HKCU 에서만 유효 합니다. 패키지 가져오기에 대 한 SFT 파일을 찾는 동안 사용자가 찾아본 마지막 위치입니다. SFT를 성공적으로 찾은 경우 자동으로 설정 합니다. 이는 SFT 파일을 자동으로 찾는 동안 연속 가져오기에 사용 됩니다.</p></td>
</tr>
</tbody>
</table>



## 공유 키


HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key는 App-v 구성 요소 간에 공유 되는 값을 제어 합니다. 다음 표에서는 공유 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">데이터 (예제) </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>가을 경로 </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>기본값 = C:\ </p></td>
<td align="left"><p>예외에 대 한 미니 덤프를 생성할 때 덤프 파일을 만들기 위한 기본 경로입니다. 기본값은 C:\입니다. 지정 하지 않은 경우 클라이언트 설치 관리자가이 키를 &lt; 앱 가상화 전역 데이터 디렉터리 &gt; \Dumps. 설정 합니다. Sequencer 설치 관리자가이 키를 설치 디렉터리로 설정 합니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>가을 Pathsizelimit </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1000</p></td>
<td align="left"><p>미니 덤프를 저장 하는 데 사용할 수 있는 최대 디스크 공간 크기 (mb)를 지정 합니다. 기본값 = 1000 MB.</p></td>
</tr>
</tbody>
</table>



## 네트워크 키


HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key는 다양 한 네트워크 관련 매개 변수를 제어 합니다. 이 키는 주로 네트워크 전송 에이전트에서 사용 합니다. 다음 표에서는 네트워크 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">데이터 (예제) </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>온라인</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>오프 라인 모드를 설정 하거나 해제 합니다. 0으로 설정 되 면 클라이언트가 App-v 관리 서버 또는 게시 서버와 통신 하지 않습니다. 연결이 끊긴 작업에서는 클라이언트가 App-v 관리 서버에 연결 되어 있지 않은 경우에도 로드 된 응용 프로그램을 시작할 수 있습니다. 오프 라인 모드에서는 클라이언트가 App-v 관리 서버 또는 게시 서버에 연결 하려고 시도 하지 않습니다. 연결이 끊긴 작업을 오프 라인으로 작업할 수 있도록 허용 해야 합니다. 기본값은 1 (온라인)으로 설정 되 고, 0은 비활성 (오프 라인)입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowDisconnectedOperation </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>연결이 끊긴 작업을 설정 하거나 해제 합니다. 기본값은 1로 설정 되 고 0을 사용 하지 않도록 설정 됩니다. 연결이 끊긴 작업을 사용 하는 경우 app-v 클라이언트는 App-v 관리 서버에 연결 되어 있지 않은 경우에도 로드 된 응용 프로그램을 시작할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FastConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1000</p></td>
<td align="left"><p>이 값은 연결이 끊긴 작업 모드로 전환 되는 시점을 결정 하는 TCP 연결 시간 초과 (밀리초)를 지정 합니다. 이 값을 사용 하 여 기본 ConnectTimeout을 20 초 (App-v connect (네트워크 거래)에 대 한 시간 제한) 또는 시스템의 TCP 시간 제한 (약 25 초)을 무시할 수 있습니다. 이렇게 하면 클라이언트가 연결이 끊긴 작업 모드로 빠르게 전환 됩니다. 다음 연결에 적용 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LimitDisconnectedOperation</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1 </p></td>
<td align="left"><p>AllowDisconnectedOperation가 1 인 경우에만 사용 가능 합니다. 이 값은 연결이 끊긴 작업에서 클라이언트가 작동할 수 있는 기간에 대 한 시간 제한이 있는지 여부를 결정 합니다. 1 = 제한 됨. 0 = 무제한.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DOTimeoutMinutes</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Default = 129600</p></td>
<td align="left"><p>연결이 끊긴 작업 모드에서 응용 프로그램을 사용할 수 있는 시간 (분)을 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>유효한 값은 1 – 999999 in (1 – 1439998560 분)으로 표시 됩니다. 기본값은 90 일 또는 129600 분입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>프로토콜</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 8</p></td>
<td align="left"><p>사용할 기본 프로토콜 (TCP vs SSL)입니다. 옵션 대화 상자에서 구성 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReadTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>명</p></td>
<td align="left"><p>네트워크 거래에 대 한 시간 제한 (초)입니다. 수정 하지 마세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WriteTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>명</p></td>
<td align="left"><p>네트워크 거래에 대 한 쓰기 시간을 초 단위로 입력 합니다. 수정 하지 마세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>명</p></td>
<td align="left"><p>네트워크 거래에 대 한 연결 시간 제한 (초)입니다. 수정 하지 마세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>3-4</p></td>
<td align="left"><p>삭제 된 세션을 다시 설정 하는 횟수입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>~</p></td>
<td align="left"><p>손실 된 세션 다시 시작을 시도 하는 간격 (초)입니다.</p></td>
</tr>
</tbody>
</table>



## Http 키


HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http 키는 Http 스트림과 관련 된 매개 변수를 제어 합니다. 이 키는 주로 네트워크 전송 에이전트에서 사용 합니다. 다음 표에서는 Http 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">데이터 (예제) </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>LaunchIfNotFound</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>Http 서버에 대 한 연결을 설정할 수 있고 패키지 파일이 더 이상 HTTP 서버에 존재 하지 않는 경우 HTTP 스트리밍의 동작을 제어 합니다. 값이 없거나 1로 설정 되어 있지 않은 경우 App-v 클라이언트에서 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>raid-1</p></td>
<td align="left"><p>이 값을 1로 설정 하면 App-v 클라이언트를 사용 하 여 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



## 파일 시스템 키


HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS 키 아래에 포함 된 값이 App-v의 파일 시스템 매개 변수를 제어 합니다. 다음 표에서는 AppFS 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">데이터 (예제) </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FileSize </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>4096</p></td>
<td align="left"><p>파일 시스템 캐시 파일의 최대 크기 (mb)입니다. 레지스트리에서이 값을 변경 하는 경우 상태를 0으로 설정 하 고 다시 부팅 해야 합니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>FileName </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\sftfsordfd </p></td>
<td align="left"><p>파일 시스템 캐시 파일의 위치입니다. 레지스트리에서이 값을 변경 하는 경우 FileSize을 동일 하 게 유지 하 고 다시 부팅 하거나 상태를 0으로 설정 하 고 다시 부팅 해야 합니다. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DriveLetter </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>Q: </p></td>
<td align="left"><p>사용할 수 있는 경우 App-v 파일 시스템이 탑재 될 드라이브 이 값은 수신기 또는 설치 관리자가 설정 하며 파일 시스템에서 읽습니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>시 </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x100 </p></td>
<td align="left"><p>파일 시스템의 상태입니다. 0으로 설정 하 고 다시 부팅 하 여 파일 시스템 캐시를 완전히 지웁니다. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileSystemStorage </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>C:\Profiles\Joe\SG </p></td>
<td align="left"><p>Symlinks의 경로 이며 HKCU 아래에서 설정 됩니다. 수정 안 함 (구성 아래의 데이터 디렉터리를 사용 하 여 변경) </p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalFileSystemStorage </p></td>
<td align="left"><p>문자열 </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\AppFS 저장소 </p></td>
<td align="left"><p>전역 파일 시스템 데이터의 경로입니다. 수정 하지 마세요. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPercentToLockInCache </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Default = 90 </p></td>
<td align="left"><p>잠글 수 있는 파일 시스템 캐시 파일의 최대 백분율을 지정 합니다. 수정 하지 마세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UnloadLeastRecentlyUsed</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>파일 시스템 캐시 공간 관리 기능은 LRU (최근에 사용한) 알고리즘을 사용 하며 기본적으로 사용 하도록 설정 되어 있습니다. 새 패키지에 필요한 공간이 캐시의 사용 가능한 공간을 초과 하는 경우 App-v 클라이언트는이 기능을 사용 하 여 새 패키지를 위한 공간을 만들기 위해 캐시에서 삭제할 수 있는 기존 패키지를 결정 합니다. 클라이언트가 MinPkgAge 레지스트리 값에 지정 된 값 보다 오래 된 경우 가장 오래 된 마지막으로 액세스 한 날짜를 사용 하 여 패키지를 삭제 합니다. 값은 0 (사용 안 함) 및 1 (기본값, 사용)입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MinPackageAge</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>raid-1</p></td>
<td align="left"><p>삭제를 위해 패키지를 선택할 수 있는 시간을 결정 하려면이 레지스트리 값을 패키지를 마지막으로 액세스 한 이후 경과 되는 최소 날짜 수와 동일 하 게 설정 합니다. 최근에 사용한 패키지는 삭제 되지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 사용 권한 키


사용자가 실수 하는 것을 방지 하기 위해 관리자는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions 키를 사용 하 여 관리자가 아닌 사용자의 일부 작업에 대 한 액세스를 제어할 수 있습니다 (예: 사용자가 실수로 프로그램을 언로드하는 것을 방지). 관리 권한이 있는 사용자는 자신에 게 이러한 사용 권한을 부여할 수 있습니다. RD 세션 호스트 (원격 데스크톱 세션 호스트) 서버 (이전의 터미널 서버) 시스템 등의 공유 시스템에서는 이러한 사용 권한 중 일부는 사용자가 시스템의 모든 사용자가 사용 하는 응용 프로그램을 제어할 수 있도록 허용 하므로 주의를 기울여야 합니다. 이러한 설정의 가능 값은 1 (허용) 및 0 (허용 안 함)입니다.

권한 키 설정은 명명 된 작업을 사용 하도록 설정 하는 모든 인터페이스를 제어 합니다. 여기에는 옵션 대화 상자, SFTTray, Sfttray이 포함 됩니다. 이러한 설정은 관리자에 게 영향을 주지 않습니다. 다음 표에서는 사용 권한 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

이름 형식 데이터 (예제) 설명 ChangeFSDrive

DWORD

기본값 = 0

값 1은 사용자가 파일 시스템 드라이브로 사용할 다른 드라이브 문자를 선택할 수 있도록 합니다.

ChangeCacheSize

DWORD

기본값 = 0

값 1은 사용자가 캐시 크기를 변경할 수 있도록 합니다.

ChangeLogSettings

DWORD

기본값 = 0

값 1은 사용자가 로그 수준을 수정 하 고, 위치를 변경 하 고, 사용자 인터페이스를 통해 다시 설정할 수 있도록 합니다.

AddApp

DWORD

기본값 = 0

값 1을 사용 하면 사용자가 응용 프로그램을 명시적으로 추가할 수 있습니다. 이는 게시 새로 고침을 통해 추가 되는 응용 프로그램에는 사용자가 아직 추가 되지 않은 응용 프로그램을 시작 (및 암시적으로 추가 하지 않음) 하는 것은 영향을 주지 않습니다. 값은 0 또는 1입니다.

LoadApp 

DWORD 

0

사용자가 응용 프로그램을 로드할 수 없습니다. 이것은 RD 세션 호스트의 기본값입니다. 모바일 사용자는 연결 되지 않은 작업 또는 오프 라인 모드에서 응용 프로그램을 사용 하도록 캐시에 완전히 로드 하는 것이 좋습니다. App-v 관리 서버 또는 App-v 스트리밍 서버에서 응용 프로그램을 스트리밍하려면 응용 프로그램을 로드 하려면 서버에 연결 되어 있어야 합니다.

raid-1

사용자가 응용 프로그램을 로드할 수 있도록 합니다. Windows 데스크톱의 기본값입니다. 

UnloadApp 

DWORD 

0

사용자가 응용 프로그램을 언로드할 수 없습니다. 패키지를 로드 하거나 언로드하면 패키지의 모든 응용 프로그램이 캐시에서 로드 되거나 제거 됩니다.

raid-1

사용자가 응용 프로그램을 언로드할 수 있도록 합니다. 

LockApp 

DWORD 

0

사용자가 응용 프로그램을 잠그고 잠금을 해제할 수 없습니다. 이것은 RD 세션 호스트의 기본값입니다. 잠긴 응용 프로그램을 캐시에서 제거 하 여 새 응용 프로그램을 위한 공간을 확보할 수 없습니다. App-v 데스크톱 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 캐시의 클라이언트에서 잠긴 응용 프로그램을 제거 하려면 잠금을 해제 해야 합니다.

raid-1

사용자가 응용 프로그램을 잠그고 잠금을 해제할 수 있습니다. Windows 데스크톱의 기본값입니다. 

ManageTypes 

DWORD 

0

사용자가 해당 사용자의 파일 형식 연결을 추가 하거나 편집 하거나 제거할 수 없습니다. 이것은 RD 세션 호스트의 기본값입니다. 

raid-1

사용자가 해당 사용자의 파일 형식 연결을 추가, 편집 및 제거할 수 있습니다 (전역에만 해당). Windows 데스크톱의 기본값입니다. 

RefreshServer 

DWORD 

0

사용자가 MIME 설정 새로 고침을 트리거할 수 없습니다. 이것은 RD 세션 호스트의 기본값입니다. 

raid-1

사용자가 MIME 설정 새로 고침을 트리거할 수 있도록 합니다. Windows 데스크톱의 기본값입니다. 

UpdateOSDFile

DWORD

기본값 = 0

값 1은 사용자가 수정 된 OSD 파일을 사용할 수 있도록 합니다.

ImportApp 

DWORD 

0

사용자가 응용 프로그램을 캐시로 가져올 수 없습니다. 로드와 가져오기의 차이점은 로드가 트리거되면 클라이언트는 OSD, ASR 또는 Override URL에 포함 된 현재 구성 된 위치에서 패키지를 가져옵니다. 가져오기를 사용 하는 경우 패키지를 가져올 위치를 지정 해야 합니다. 

raid-1

사용자가 응용 프로그램을 캐시로 가져올 수 있도록 합니다. 

ChangeRefreshSettings

DWORD

기본값 = 0

값 1은 사용자가 서버에 대 한 새로 고침 설정을 수정할 수 있도록 합니다 (로그인 및 주기적 새로 고침 시 새로 고침). 이는 사용자가 다른 서버 설정 (path, host 등)을 수정할 수 있다는 것을 의미 하지는 않습니다.

ManageServers

DWORD

기본값 = 0

값 1을 사용 하면 사용자가 ChangeRefreshSettings 사용 권한에 의해 제어 되는 새로 고침 설정 편집을 제외 하 고 서버를 추가, 편집 및 제거할 수 있습니다.

기타 바로 가기

DWORD

기본값 = 0

값 1은 사용자 인터페이스를 통해 바로 가기를 게시할 수 있도록 합니다. 이는 게시 새로 고침 중에 게시 되는 바로 가기에는 영향을 주지 않습니다.

ViewAllApplications

DWORD

기본값 = 0

값 1은 사용자 인터페이스를 통해 모든 응용 프로그램을 표시 합니다. 그렇지 않으면 사용자의 응용 프로그램만 표시 됩니다.

RepairApp

DWORD

기본값 = 1

값 1은 사용자가 SFTMime 또는 클라이언트 관리 콘솔의 응용 프로그램에 대해 복구 작업을 사용할 수 있도록 합니다. 응용 프로그램을 복구 하는 경우 사용자 지정 사용자 설정을 제거 하 고 기본 설정을 복원 합니다. 이 작업은 바로 가기 또는 파일 형식 연결을 변경 하거나 삭제 하지 않으며 캐시에서 응용 프로그램을 제거 하지 않습니다.

ClearApp

DWORD

기본값 = 1

값 1은 사용자가 SFTMime 또는 클라이언트 관리 콘솔의 응용 프로그램에 대해 Clear 작업을 사용할 수 있도록 합니다. 콘솔에서 응용 프로그램을 지우면 해당 응용 프로그램을 더 이상 사용할 수 없습니다. 그러나 응용 프로그램은 캐시에 유지 되며 동일한 시스템의 다른 사용자가 계속 사용할 수 있습니다. 게시 새로 고침 후에는 지워진 응용 프로그램을 다시 사용할 수 있게 됩니다.

DeleteApp

DWORD

기본값 = 0

값 1은 사용자가 SFTMime 또는 클라이언트 관리 콘솔의 응용 프로그램에 대해 Delete 작업을 사용할 수 있도록 합니다. 응용 프로그램을 삭제 하면 해당 클라이언트의 모든 사용자가 선택한 응용 프로그램을 더 이상 사용할 수 없게 됩니다. 바로 가기 및 파일 형식 연결이 삭제 되 고 응용 프로그램이 캐시에서 삭제 됩니다. 그러나 다른 응용 프로그램이 선택한 응용 프로그램에 대 한 파일 시스템 캐시 또는 설정 데이터의 데이터를 참조 하는 경우 이러한 항목은 삭제 되지 않습니다.

게시 새로 고침을 수행한 후에는 삭제 된 응용 프로그램을 다시 사용할 수 있게 됩니다.

ToggleOfflineMode

DWORD

값 1은 사용자가 오프 라인 모드에서 클라이언트를 실행 하도록 선택할 수 있도록 합니다. 오프 라인 모드에서 응용 프로그램 가상화 클라이언트는 응용 프로그램 가상화 서버에 연결 되어 있지 않은 경우에도 로드 된 응용 프로그램을 시작할 수 있습니다.



## 사용자 지정 설정


HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings 키에는 프런트 엔드 구성 요소에 대 한 값이 포함 되어 있습니다. 모든 사용자 지정 설정은 문자열로 저장 됩니다. 다음 표에서는 CustomSettings 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">데이터 (예제) </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TrayErrorDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 30 </p></td>
<td align="left"><p>응용 프로그램 가상화 알림 영역에 시작 실패와 같은 오류 메시지가 표시 되는 시간 (초)입니다 &quot; &quot; . 최 솟 값 1 </p></td>
</tr>
<tr class="even">
<td align="left"><p>TraySuccessDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 10 </p></td>
<td align="left"><p>Appvmed 알림 영역에 &quot; Word 시작 &quot; 또는 &quot; Excel 종료와 같은 성공 메시지가 표시 되는 시간 (초)입니다 &quot; . 0 인 경우 해당 메시지가 표시 되지 않습니다. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayVisibility</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>0 = 가상화 된 응용 프로그램을 사용 하는 경우 트레이를 표시 합니다.</p>
<p>1 = 항상 용지함을 표시 합니다.</p>
<p>2 = 용지함을 표시 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TrayShowRefresh</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>이 값을 1로 설정 하면 트레이 메뉴에 메뉴 항목 새로 고침 응용 프로그램이 표시 되 고 사용자가 액세스할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayShowLoad</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>값을 1로 설정 하면 트레이 메뉴에 메뉴 항목 로드 응용 프로그램이 표시 되 고 사용자가 액세스할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



## 보고 설정


HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting 키에는 App-v 관리 서버에 대 한 보고 관련 값이 포함 되어 있습니다. 다음 표에서는 보고 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">데이터 (예제) </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DataCacheLimit</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 20</p></td>
<td align="left"><p>이 값은 보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다. 크기는 메모리의 캐시에 적용 됩니다. 제한에 도달 하면 로그 파일이 롤오버 됩니다. 목록 맨 아래에 새 레코드가 추가 되 면 하나 이상의 가장 오래 된 레코드 (목록 맨 위)가 삭제 되어 공간을 확보 합니다. 경고가 처음 발생 하면 클라이언트 로그 및 이벤트 로그에 기록 되 고, 전송이 성공적으로 취소 되 고 로그가 다시 채워지면 다시 기록 됩니다. 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DataBlockSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 65536</p></td>
<td align="left"><p>이 값은 로그가 유효 크기에 도달 했을 때 영구 전송 오류를 방지 하기 위해 게시 새로 고침 시 서버로 전송할 최대 크기 (바이트)를 지정 합니다. 기본값은 65536입니다. 보고서 데이터를 서버에 전송할 때 응용 프로그램 레코드의 블록 (바이트의 블록 크기 (XML 데이터))이 캐시에서 제거 되 고 서버로 전송 됩니다. 각 블록에는 일반 클라이언트 데이터 및 전역 패키지 목록 데이터가 앞에 있으며 블록 크기 계산에는 영향을 주지 않습니다. 매우 큰 패키지 목록을 통해 낮은 대역폭과 불안정 한 연결을 통해 전송 오류가 발생할 가능성이 있습니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[Application Virtualization Client 참조](application-virtualization-client-reference.md)









