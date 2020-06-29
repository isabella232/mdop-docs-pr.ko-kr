---
title: Application Virtualization Client 설치 관리자 명령줄 매개 변수
description: Application Virtualization Client 설치 관리자 명령줄 매개 변수
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819718"
---
# Application Virtualization Client 설치 관리자 명령줄 매개 변수


다음 표에서는 사용 가능한 모든 Microsoft Application Virtualization 클라이언트 설치 관리자 명령줄 매개 변수, 해당 값, 각 매개 변수에 대 한 간략 한 설명을 나열 합니다. 매개 변수는 대/소문자를 구분 하며 모두 대문자로 입력 해야 합니다. 모든 매개 변수 값은 큰따옴표로 묶어야 합니다.

**참고**  
-   App-v 버전 4.6의 경우 클라이언트 업그레이드 중 명령줄 매개 변수를 사용할 수 없습니다.

-   *Swicachesize* 및 *MINFREESPACEMB* 매개 변수는 명령줄에서 함께 사용할 수 없습니다. 두 가지를 모두 사용 하는 경우 *Swicachesize* 매개 변수가 무시 됩니다.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">값</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>클라이언트가 <em> APPLICATIONSOURCEROOT 매개 변수를 사용 하 여 구성 된 방식에 관계 없이 파일에서 스트리밍을 사용할 수 있는지 여부를 나타냅니다 </em> . FALSE로 설정 된 경우 OSD HREF 또는 <em> APPLICATIONSOURCEROOT </em> 매개 변수에 파일 경로가 포함 된 경우에도 트랜스포트가 파일에서 스트리밍을 사용할 수 없게 됩니다.</p>
<p>가능한 값:</p>
<ul>
<li><p>TRUE — 수동으로 배포 된 응용 프로그램이 디스크에서 로드 될 수 있습니다.</p></li>
<li><p>FALSE — 모든 응용 프로그램은 원본 스트리밍 서버에서 가져와야 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>APPLICATIONSOURCEROOT</em></p></td>
<td align="left"><p>RTSP:// <em> URL </em> (동적 패키지 배달의 경우)</p>
<p>File:// <em> URL </em> 또는 <em> UNC </em> (파일 패키지 배달의 로드)</p></td>
<td align="left"><p>토폴로지 관리 체계를 준수 하 여 응용 프로그램 로드가 수행 되도록 관리자나 전자 소프트웨어 배포 시스템을 사용 하도록 설정 하려면 응용 프로그램 HREF 요소 (원본 위치)에 대 한 OSD 코드 베이스의 재정의를 허용 합니다. 값이 기본값인 "" 이면 기존 OSD 파일 설정이 사용 됩니다.</p>
<p>URL에는 다음과 같은 몇 가지 부분이 있습니다.</p>
<p>&lt;프로토콜 &gt; // &lt; 서버 &gt; : &lt; 포트 &gt; / &lt; 경로 &gt; / &lt; ? 쿼리 &gt; &lt; #fragment&gt;</p>
<p>UNC 경로에는 다음 세 가지 부분이 있습니다.</p>
<p>&amp;lt; computername &gt; &amp; lt; 폴더 공유 &gt; &amp; lt; 리소스&gt;</p>
<p><em>APPLICATIONSOURCEROOT </em> 매개 변수가 클라이언트에 지정 되어 있는 경우 클라이언트는 osd 파일의 URL 또는 UNC 경로를 구성 요소로 나눠 osd 섹션을 해당 <em> APPLICATIONSOURCEROOT 섹션으로 바꿉니다 </em> .</p>
<div class="alert">
<strong>중요</strong><br/><p>UNC 경로에 file://를 사용할 때는 올바른 형식을 사용 해야 합니다. 올바른 형식은 file:// &amp; lt; 서버 &gt; &amp; lt; share입니다 &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>ICONSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>HTTP:// <em> url </em> 또는 HTTPS:// <em> url</em></p></td>
<td align="left"><p>관리자가 게시 하는 동안 시퀀싱 된 응용 프로그램 패키지의 아이콘 검색에 대 한 원본 위치를 지정할 수 있도록 합니다. 아이콘 원본 루트가 UNC 경로 및 Url (HTTP 또는 HTTPS)을 지원 합니다. 값이 기본값인 "" 이면 기존 OSD 파일 설정이 사용 됩니다.</p>
<p>URL에는 다음과 같은 몇 가지 부분이 있습니다.</p>
<p>&lt;프로토콜 &gt; // &lt; 서버 &gt; : &lt; 포트 &gt; / &lt; 경로 &gt; / &lt; ? 쿼리 &gt; &lt; #fragment&gt;</p>
<p>UNC 경로에는 다음 세 가지 부분이 있습니다.</p>
<p>&amp;lt; computername &gt; &amp; lt; 폴더 공유 &gt; &amp; lt; 리소스&gt;</p>
<div class="alert">
<strong>중요</strong><br/><p>UNC 경로를 사용 하는 경우 올바른 형식을 사용 해야 합니다. 허용 되는 형식은 &amp; lt, 서버 &gt; &amp; lt; share &gt; 또는 &lt; drive 문자 &gt; : &amp; lt; folder &gt; 입니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>HTTP:// <em> url </em> 또는 HTTPS:// <em> url</em></p></td>
<td align="left"><p>관리자가 게시 중에 응용 프로그램 패키지에 대 한 OSD 파일 검색의 원본 위치를 지정할 수 있도록 합니다. OSD 원본 루트는 UNC 경로 및 Url (HTTP 또는 HTTPS)을 지원 합니다. 값이 기본값인 "" 이면 기존 OSD 파일 설정이 사용 됩니다.</p>
<p>URL에는 다음과 같은 몇 가지 부분이 있습니다.</p>
<p>&lt;프로토콜 &gt; // &lt; 서버 &gt; : &lt; 포트 &gt; / &lt; 경로 &gt; / &lt; ? 쿼리 &gt; &lt; #fragment&gt;</p>
<p>UNC 경로에는 다음 세 가지 부분이 있습니다.</p>
<p>&amp;lt; computername &gt; &amp; lt; 폴더 공유 &gt; &amp; lt; 리소스&gt;</p>
<div class="alert">
<strong>중요</strong><br/><p>UNC 경로를 사용 하는 경우 올바른 형식을 사용 해야 합니다. 허용 되는 형식은 &amp; lt, 서버 &gt; &amp; lt; share &gt; 또는 &lt; drive 문자 &gt; : &amp; lt; folder &gt; 입니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>응용 프로그램의 자동 로드를 시작 하는 이벤트를 정의 하는 AutoLoad 트리거입니다. AutoLoad는 백그라운드 스트리밍을 사용 하 여 응용 프로그램을 캐시에 완전히 로드할 수 있도록 합니다.</p>
<p>기본 기능 블록이 최대한 빨리 로드 됩니다. 나머지 기능 블록은 백그라운드에서 로드 되어 응용 프로그램과 사용자의 상호 작용 등의 포그라운드 작업을 수행 하 고, 우선 순위를 사용 하 고, 최적의 성능을 제공할 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p><em>Autoloadtarget </em> 매개 변수는 자동으로 로드 되는 응용 프로그램을 결정 합니다. 기본적으로 <em> autoloadtarget이 설정 되지 않은 경우 사용 된 패키지는 자동으로 로드 됩니다 </em> .</p>
</div>
<div>

</div>
<p>각 매개 변수는 다음과 같이 로드 동작에 영향을 줍니다.</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> -사용자가 로그인 할 때 로드가 시작 됩니다.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> -사용자가 응용 프로그램을 시작할 때 로드를 시작 합니다.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> -게시 새로 고침이 발생할 때 로드가 시작 됩니다.</p></li>
</ul>
<p>세 값을 조합할 수 있습니다. 다음 예제에서는 사용자 로그인에서 AutoLoad 트리거를 사용 하 고 새로 고침을 게시할 때 다음을 수행 합니다.</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONLOGIN</em></p>
<div class="alert">
<strong>참고</strong><br/><p>클라이언트가 처음 설치할 때 이러한 값으로 구성 된 경우 다음에 사용자가 로그 오프 한 다음 다시 로그온 할 때까지 Autoload가 트리거되지 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>않아야</p>
<p>모든</p>
<p>PREVUSED</p></td>
<td align="left"><p>지정 된 AutoLoad 트리거가 발생할 때 자동으로 로드 되는 항목을 나타냅니다.</p>
<p>가능한 값:</p>
<ul>
<li><p>없음-설정 될 수 있는 트리거에 관계 없이 자동으로 로드 되지 않습니다.</p></li>
<li><p>ALL (모두)-AutoLoad trigger를 사용 하는 경우 모든 패키지가 실행 되었는지 여부에 관계 없이 자동으로 로드 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 SFTMIME <strong> 패키지 추가 </strong> 및 <strong> 패키지 구성 명령을 사용 하 여 개별 패키지에 대해 구성 됩니다 </strong> . 이러한 명령에 대 한 자세한 내용은 <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> sftmime 명령 참조를 참조 </a> 하세요.</p>
</div>
<div>

</div></li>
<li><p>PREVUSED-AutoLoad trigger를 사용 하는 경우 패키지에서 하나 이상의 응용 프로그램이 이전에 사용 된 패키지 (즉, 시작 또는 precached)만 로드 합니다.</p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>읽기 전용 캐시 (예: VDI 서버 구현)를 사용 하도록 App-v 클라이언트를 설치 하는 경우에 <em> </em> 는 클라이언트가 읽기 전용 캐시에서 응용 프로그램을 업데이트 하는 것을 방지 하려면 autoloadtarget 매개 변수를 no로 설정 해야 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (기본값)</p>
<p>1 – 1439998560 분 (범위)</p></td>
<td align="left"><p>연결이 끊긴 작업에서 응용 프로그램을 사용할 수 있는 시간 (분)을 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;경로&gt;</p></td>
<td align="left"><p>App-v 클라이언트의 설치 디렉터리를 지정 합니다.</p>
<p>예: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization 클라이언트&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>OPTIN</em></p></td>
<td align="left"><p>FALSE</p>
<p>“”</p></td>
<td align="left"><p>일반 공용에서 업데이트를 사용할 수 있는 경우 microsoft Update를 통해 microsoft Application Virtualization 클라이언트 구성 요소를 업그레이드할 수 있습니다. Windows 운영 체제에 설치 된 Microsoft Update 에이전트는 사용자가 서비스를 사용 하도록 명시적으로 옵트인 해야 합니다. 이 옵트인은 디바이스의 모든 응용 프로그램에 대해 한 번만 필요 합니다. Microsoft 업데이트에 이미 옵트인 한 경우 디바이스의 Microsoft Application Virtualization 구성 요소는 자동으로 서비스를 활용 하 게 됩니다.</p>
<p>명령줄 설치의 경우 자동으로 Microsoft 업데이트를 허용 해야 하기 때문에 Microsoft 업데이트는 기본적으로 옵트아웃 (이전 응용 프로그램에서 옵트인 (opt in) 하도록 설정 되지 않은 경우)를 사용 하는 것이 좋습니다. 따라서 명령줄 설치의 경우에는 명시적으로 옵트인 해야 합니다. 명령줄 매개 변수 <em> OPTIN </em> 를 TRUE로 설정 하면 Microsoft Update 옵트인이 설정 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>REQUIREAUTHORIZATIONIFCACHED</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>응용 프로그램이 이미 캐시에 있는지 여부에 관계 없이 항상 인증이 필요한 지 여부를 나타냅니다.</p>
<p>가능한 값:</p>
<ul>
<li><p>TRUE — 시작할 때 항상 응용 프로그램에 권한을 부여 해야 합니다. RTSP로 스트리밍된 응용 프로그램의 경우 인증을 위해 사용자 인증 토큰이 서버로 전송 됩니다. 파일 기반 응용 프로그램의 경우 파일 Acl은 사용자가 응용 프로그램에 액세스할 수 있는지 여부를 결정 합니다.</p></li>
<li><p>FALSE — 항상 서버 연결을 시도 합니다. 서버에 대 한 연결을 설정할 수 없는 경우에도 클라이언트는 사용자가 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 있도록 허용 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>캐시 크기 (MB)</p></td>
<td align="left"><p>클라이언트 캐시의 크기 (mb)를 지정 합니다. 기본 크기는 4096 MB 이며, 최대 크기는 1048576 MB (1TB)입니다. 시스템에서 설치할 때 사용 가능한 공간을 확인 하지만 공간은 예약 되어 있지 않습니다.</p>
<p>예: <strong> swicachesize = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>표시 이름</p></td>
<td align="left"><p>게시 서버의 표시 된 이름을 지정 합니다. <em>SWIPUBSVRHOST </em> 를 사용할 때 필요 합니다.</p>
<p>예: <strong> SWIPUBSVRDISPLAY = &quot; 프로덕션 환경&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[HTTP | 플레이어가</p></td>
<td align="left"><p>게시 서버 유형을 지정 합니다. 기본 서버 유형은 Application Virtualization Server입니다. <strong>/Secure </strong> 스위치는 대/소문자를 구분 하지 않습니다.</p>
<ul>
<li><p>HTTP-표준 HTTP 서버</p></li>
<li><p>HTTP <strong> /secure </strong> -향상 된 보안 http 서버</p></li>
<li><p>RTSP-Application Virtualization Server</p></li>
<li><p>RTSP <strong> /secure </strong> -향상 된 보안 애플리케이션 가상화 서버</p></li>
</ul>
<p>예: <strong> SWIPUBSVRTYPE = &quot; HTTP/secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>IP 주소 | 호스트 이름</p></td>
<td align="left"><p>서버&#39;s IP 주소로 확인 되는 서버의 호스트 이름 또는 응용 프로그램 가상화 서버의 IP 주소를 지정 합니다. <em>SWIPUBSVRDISPLAY </em> 를 사용할 때 필요 합니다.</p>
<p>예: <strong> SWIPUBSVRHOST = &quot; SERVER01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>포트 번호</p></td>
<td align="left"><p>이 응용 프로그램 가상화 서버에서 클라이언트의 요청을 수신 대기 하는 데 사용 하는 논리 포트 (기본값 = 554)를 지정 합니다.</p>
<ul>
<li><p>표준 HTTP 서버-기본값 = 80.</p></li>
<li><p>향상 된 보안 HTTP 서버-기본값 = 443.</p></li>
<li><p>Application Virtualization Server-Default = 554.</p></li>
<li><p>향상 된 보안 애플리케이션 가상화 서버-기본값 = 322.</p></li>
</ul>
<p>예: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>경로 이름</p></td>
<td align="left"><p>파일 형식 연결을 정의 하는 파일의 게시 서버 위치를 지정 합니다 (기본값 =/). <em>SWIPUBSVRTYPE </em> 매개 변수 값이 HTTP 인 경우 필요 합니다.</p>
<p>예: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[켜기] | 끄십시오</p></td>
<td align="left"><p>사용자가 클라이언트에 로그인 할 때 파일 형식 연결 및 응용 프로그램에 대해 클라이언트가 게시 서버를 자동으로 쿼리할 지 여부를 지정 합니다 (기본값 = 설정).</p>
<p>예: <strong> SWIPUBSVRREFRESH = &quot; off&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>전역 데이터 디렉터리</p></td>
<td align="left"><p>특정 사용자와 관련 되지 않은 데이터를 저장할 디렉터리 (기본값 = C:\Documents 및 Settings\All Users\Documents)를 지정 합니다.</p>
<p>예: <strong> SWIGLOBALDATA = &quot; D:\microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>사용자 데이터 디렉터리</p></td>
<td align="left"><p>특정 사용자와 관련 된 데이터가 저장 되는 디렉터리를 지정 합니다 (기본값 =% APPDATA%).</p>
<p>예: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization 클라이언트&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>기본 설정 드라이브 문자</p></td>
<td align="left"><p>가상 드라이브에 대해 선택한 드라이브 문자에 해당 합니다.</p>
<p>예: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 – 4</p></td>
<td align="left"><p>로그 메시지가 NT 이벤트 로그에 기록 되는 로깅 수준을 나타냅니다. 값은 기록 되는 항목의 임계값 (즉, 해당 값과 같거나 작은 모든 항목은 기록 됨)을 나타냅니다. 예를 들어 0x3 (경고) 값은 경고 (0x3), 오류 (0x2) 및 치명적 오류 (0x1)가 기록 됨을 나타냅니다.</p>
<p>가능한 값:</p>
<ul>
<li><p>0 = = 없음</p></li>
<li><p>1 = = 요주의</p></li>
<li><p>2 = = 오류</p></li>
<li><p>3 = = 경고</p></li>
<li><p>4 = = 정보</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>(MB)</p></td>
<td align="left"><p>캐시 크기가 증가 하기 전에 호스트에서 사용할 수 있는 사용 가능한 공간의 크기 (mb)를 지정 합니다. 다음 예제에서는 캐시 크기를 늘리기 위해 디스크에서 5gb 이상의 여유 공간을 확보 하도록 클라이언트를 구성 합니다. 기본값은 설치 시 디스크에서 사용할 수 있는 5000 MB의 빈 공간입니다.</p>
<p>예: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>그룹 정책을 사용 하는 경우와 같이 클라이언트를 배포 하기 전에 레지스트리 설정을 적용 한 경우 사용 합니다. 클라이언트가 배포 되 면이 매개 변수를 값 1로 설정 하 여 레지스트리 설정을 덮어쓰지 않도록 해야 합니다.</p>
<div class="alert">
<strong>중요</strong><br/><p>값을 1로 설정 하면 다음 클라이언트 설치 관리자 명령줄 매개 변수가 무시 됩니다.</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , <strong> ICONSOURCEROOT </strong> , <strong> OSDSOURCEROOT </strong> , <strong> systemeventloglevel </strong> , <strong> SWIGLOBALDATA </strong> , <strong> dotimeoutminutes </strong> , <strong> SWIFSDRIVE </strong> , <strong> autoloadtarget </strong> , <strong> autoloadtarget </strong> , <strong> SWIUSERDATA </strong> .</p>
<p>설치 후 이러한 값을 설정 하는 방법에 대 한 자세한 내용은 Application Virtualization (App-v) Operations Guide ()에서 "명령줄을 사용 하 여 App-v 클라이언트 레지스트리 설정을 구성 하는 방법"을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## 관련 항목


[Application Virtualization Client를 수동으로 설치하는 방법](how-to-manually-install-the-application-virtualization-client.md)

[Application Virtualization Client를 업그레이드하는 방법](how-to-upgrade-the-application-virtualization-client.md)

[SFTMIME 명령 참조](sftmime--command-reference.md)









