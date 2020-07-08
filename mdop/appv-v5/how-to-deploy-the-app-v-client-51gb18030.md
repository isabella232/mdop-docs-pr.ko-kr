---
title: App-V Client 배포 방법
description: App-V Client 배포 방법
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814124"
---
# App-V Client 배포 방법


다음 절차를 사용 하 여 Microsoft App-v (Application Virtualization) 5.1 클라이언트 및 원격 데스크톱 서비스 클라이언트를 설치 합니다. 대상 컴퓨터의 운영 체제와 일치 하는 클라이언트 버전을 설치 해야 합니다.

<a href="" id="bkmk-clt-install-prereqs"></a>**시작 하기 전에 수행할 작업**

1. 소프트웨어 필수 구성 요소를 검토 하 고 설치 합니다.

   설치 하는 App-v 버전에 해당 하는 필수 구성 요소 소프트웨어를 설치 합니다.

   -   [App-V 5.1 정보](about-app-v-51.md)

   -   [App-V 5.1 필수 구성 요소](app-v-51-prerequisites.md)

2. 설치에 적용 가능한 경우 클라이언트 공존 및 지원 되지 않는 시나리오를 검토 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>공존할 때의 App-v 클라이언트 배포</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">App-V 5.1 Sequencer 및 Client 배포 계획</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>지원 되지 않거나 제한 된 설치 시나리오</p></td>
   <td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-v 5.1에서 지원 되는 구성의 클라이언트 섹션을 참조 하세요.</a></p></td>
   </tr>
   </tbody>
   </table>



3. 클라이언트 레지스트리, 로그 및 문제 해결 정보에 대 한 위치를 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>클라이언트 레지스트리 정보</p></td>
<td align="left"><ul>
<li><p>기본적으로 App-v 5.1 클라이언트를 설치 하 고 나면 클라이언트 정보가 다음 레지스트리 키의 레지스트리에 저장 됩니다.</p>
<p><strong>HKEY_LOCAL_MACHINE \ 소프트웨어 \ MICROSOFT \ APPV \ 클라이언트</strong></p></li>
<li><p>가상화 된 패키지를 App-v 클라이언트를 실행 하는 컴퓨터에 배포 하는 경우 연결 된 패키지 데이터는 다음 위치에 저장 됩니다.</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>그러나 다음 레지스트리 키를 사용 하 여이 위치를 다시 구성할 수 있습니다.</p>
<p><strong>HKEY_LOCAL_MACHINE \ 소프트웨어 \ MICROSOFT \ 소프트웨어 \ MICROSOFT \ APPV \ 클라이언트 \ 스트리밍 \ 패키지 설치 루트</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>클라이언트 로그 파일</p></td>
<td align="left"><ul>
<li><p>App-v 5.1 클라이언트와 연결 된 로그 파일 정보는 다음 로그에서 검색 합니다.</p>
<p><strong>이벤트 로그/응용 프로그램 및 서비스 로그/Microsoft/AppV</strong></p></li>
<li><p>App-v 5.0 SP3에서는 일부 로그가 통합 되어 다음 위치로 이동 했습니다.</p>
<p><strong>이벤트 로그/응용 프로그램 및 서비스 로그/Microsoft/AppV/ServiceLog</strong></p>
<p>이동한 로그 목록은 <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> 앱-V 5.0 SP3 정보를 참조 하세요 </a> .</p></li>
<li><p>App-v 5.1 클라이언트를 실행 하는 컴퓨터에 현재 저장 된 패키지는 다음 위치에 저장 됩니다.</p>
<p><strong>C:\ProgramData\App-V &amp; lt; 패키지 id &gt; &amp; lt; 버전 id&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>클라이언트 설치 문제 해결 정보</p></td>
<td align="left"><p><strong>% Temp% 폴더에 오류 로그를 표시 </strong> 합니다. 로그 파일을 검토 하려면 시작을 클릭 하 고 <strong> </strong> <strong> % temp% </strong> 를 입력 한 다음 <strong> appv_ 로그를 찾습니다 </strong> .</p></td>
</tr>
</tbody>
</table>



**App-v 5.1 클라이언트를 설치 하려면**

1.  앱-V 5.1 클라이언트 설치 파일을 설치할 컴퓨터에 복사 합니다. 다음 클라이언트 유형 중에서 선택 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">클라이언트 유형</th>
    <th align="left">사용할 파일</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>표준 버전의 클라이언트</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>클라이언트의 원격 데스크톱 서비스 버전</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  설치 파일을 두 번 클릭 하 고 **설치**를 클릭 합니다. 설치가 시작 되기 전에 설치 관리자는 컴퓨터에 누락 된 [app-v 5.1 필수 조건이](app-v-51-prerequisites.md)있는지 확인 합니다.

3.  소프트웨어 사용 조건을 검토 하 고 동의 하 고 Microsoft 업데이트 사용 여부와 Microsoft 사용자 환경 개선 프로그램에 참여할지 여부를 선택한 후 **설치**를 클릭 합니다.

4.  **설정 완료** 됨 페이지에서 **닫기를**클릭 합니다.

    설치 **프로그램**에서 앱-V 클라이언트에 대해 다음 항목을 만듭니다.

    -   **.exe**

    -   **.msi**

    -   **언어 팩**

        **참고**  
        설치 후에는 .exe 파일만 제거할 수 있습니다.



**스크립트를 사용 하 여 App-v 5.1 클라이언트 설치**

1. 대상 컴퓨터에 필수 구성 요소 소프트웨어를 모두 설치 합니다. [시작 하기 전에 수행할 작업을](#bkmk-clt-install-prereqs)참조 하세요. .Msi 파일을 사용 하 여 클라이언트를 설치 하는 경우 필수 구성 요소가 누락 되 면 설치에 실패 하 게 됩니다.

2. 스크립트를 사용 하 여 App-v 5.1 클라이언트를 설치 하려면 **appv\_client\_setup.exe**에 다음 매개 변수를 사용 합니다.

   **참고**  
   클라이언트 Windows Installer (.msi)는 **/log** 매개 변수를 제외 하 고 동일한 스위치 집합을 지원 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>설치 디렉터리를 지정 합니다. 사용 예: <strong> /INSTALLDIR = C:\Program Files\AppV Client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>사용자 환경 개선 프로그램의 참여를 사용 하도록 설정 합니다. 사용 예: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Microsoft 업데이트를 사용 하도록 설정 합니다. 사용 예: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/REPACKAGE설치 루트</p></td>
   <td align="left"><p>모든 새 응용 프로그램 및 업데이트를 설치할 디렉터리를 지정 합니다. 사용 예: <strong> /Package설치 루트 =&#39;C:\App-V 패키지&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>패키지 콘텐츠를 다운로드 하는 데 사용할 원본 위치를 재정의 합니다. 사용 예: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>앱-V 5.1에서 새 패키지를 특정 컴퓨터에 로드 하는 방법을 지정 합니다. 다음 옵션을 사용할 수 있습니다: [1]. 모든 패키지 [2]을 (를) 자동으로 로드 합니다. 또는 자동으로 패키지 [0]을 (를) 로드 합니다. <strong> 사용 예:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>스트리밍된 패키지 콘텐츠를 로컬 하드 디스크에 저장 하지 않도록 지정 합니다. 사용 예: <strong> /Sharedcontentstoremode = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>이전 버전을 사용 하 여 만든 패키지와 연결 되는 것 처럼 App-v 5.1 클라이언트에서 바로 가기 및 FTAs 수정할 수 있습니다. 사용 예: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>패키지 매니페스트 파일에 정의 된 스크립트 또는 실행 해야 하는 구성 파일을 사용 하도록 설정 합니다. 사용 예: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>사용자 프로필과 로밍할 수 없는 레지스트리 경로를 지정 합니다. 사용 예: <strong> /ROAMINGREGISTRYEXCLUSIONS = \\수업, \클라이언트</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>사용자&#39;s 프로필을 사용 하 여 로밍 하지 않는% userprofile%를 기준으로 하는 파일 경로를 지정 합니다. 사용 예: <strong> /ROAMINGFILEEXCLUSIONS &#39;desktop, 내 사진&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>게시 서버의 이름을 표시 합니다. 사용 예: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>게시 서버의 URL을 표시 합니다. 사용 예: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>전역 게시 새로 고침을 사용 하도록 설정 합니다. 사용 예: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>사용자가 로그온 할 때 전역 게시 새로 고침을 시작 합니다. 사용 예: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>게시 새로 고침 간격을 지정 합니다 <strong> . 여기서 0 </strong> 은 주기적으로 새로 고쳐지지 않습니다. 사용 예: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>간격 단위 (시 [0], 일 [1])를 지정 합니다. 사용 예: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>사용자 게시 새로 고침을 사용 하도록 설정 합니다. 사용 예: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>사용자가 로그온 할 때 사용자 게시 새로 고침을 시작 합니다. 사용 예: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>게시 새로 고침 간격을 지정 합니다 <strong> . 여기서 0 </strong> 은 주기적으로 새로 고쳐지지 않습니다. 사용 예: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>간격 단위 (시 [0], 일 [1])를 지정 합니다. 사용 예: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Log</p></td>
   <td align="left"><p>로그 정보가 저장 되는 위치를 지정 합니다. 기본 위치 는% Temp%입니다. 사용 예: <strong> /Log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/q</p></td>
   <td align="left"><p>무인 설치를 지정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/REPAIR</p></td>
   <td align="left"><p>이전 클라이언트 설치를 복구 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>클라이언트 설치 후 컴퓨터가 다시 부팅 되지 않도록 합니다.</p>
   <p>이 매개 변수는 각 업데이트가 설치 된 후 최종 사용자 컴퓨터가 다시 부팅 되지 않도록 하 고, 편리한 시간에 재부팅을 예약할 수 있도록 합니다. 예를 들어 App-v 5.1를 설치한 다음 서비스 팩 설치 후 재부팅 하지 않고 핫픽스 패키지 Y를 설치할 수 있습니다. 설치 후에는 App-v를 사용 하기 전에 다시 부팅 해야 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/UNINSTALL</p></td>
   <td align="left"><p>클라이언트를 제거 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>사용권 계약을 수락 합니다. 무인 설치에 필요 합니다. 사용 예: <strong> /ACCEPTEULA </strong> 또는 <strong> /ACCEPTEULA = 1 </strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>연결 된 레이아웃 작업을 지정 합니다. 또한 앱-V 5.1를 설치 하지 않고 Windows Installer (.msi) 및 스크립트 파일을 폴더로 추출 합니다. 값이 필요 하지 않습니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>레이아웃 디렉터리를 지정 합니다. 문자열 값이 필요 합니다. 사용 예: <strong> /Layoutdir = "C:\Application Virtualization Client" </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/help</p></td>
   <td align="left"><p>이전 설치 매개 변수에 대 한 도움말을 요청 합니다.</p></td>
   </tr>
   </tbody>
   </table>



**Windows Installer (.msi) 파일을 사용 하 여 App-v 5.1 클라이언트를 설치 하려면**

1.  대상 컴퓨터에 필수 구성 요소를 설치 합니다. [시작 하기 전에 수행할 작업을](#bkmk-clt-install-prereqs)참조 하세요. 전제 조건이 충족 되지 않으면 설치가 실패 합니다.

2.  앱-V 5.1 Windows Installer (.msi) 파일을 사용 하 여 클라이언트를 설치 하기 전에 대상 컴퓨터에 보류 중인 다시 시작이 없는지 확인 합니다. Windows Installer 파일은 보류 중인 다시 시작에 플래그를 지정 하지 않습니다.

3.  다음 Windows Installer 파일 중 하나를 대상 컴퓨터에 배포 합니다. 지정 하는 파일은 대상 컴퓨터의 구성과 일치 해야 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">배포 유형</th>
    <th align="left">이 파일 배포</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>컴퓨터에서 32 비트 Microsoft Windows 운영 체제를 실행 중입니다.</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>컴퓨터에서 64 비트 Microsoft Windows 운영 체제를 실행 중입니다.</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>App-v 5.1 원격 데스크톱 서비스 클라이언트를 배포 하는 경우</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  다음 표의 정보를 사용 하 여 대상 컴퓨터에 대해 원하는 언어를 기반으로 설치할 해당 언어 팩 (.msi)을 선택 합니다 **.** 테이블의 **xxxx** 는 언어 팩의 대상 로캘을 참조 합니다.

    **시작 하기 전에 알아야 할 사항:**

    -   언어 팩은 표준 App-v 5.1 클라이언트와 App-v 5.1 클라이언트의 원격 데스크톱 서비스 버전에 모두 공통으로 표시 됩니다.

    -   **.Exe**를 사용 하 여 app-v 5.1 클라이언트를 설치 하면 설치 관리자가 대상 컴퓨터에서 실행 중인 운영 체제와 일치 하는 언어 팩만 배포 합니다.

    -   대상 컴퓨터에 추가 언어 팩을 배포 하려면 **Windows Installer (.msi) 파일을 사용 하 여 app-v 5.1 클라이언트를 설치 하**는 절차를 사용 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">배포 유형</th>
    <th align="left">이 파일 배포</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>컴퓨터에서 32 비트 Microsoft Windows 운영 체제를 실행 중입니다.</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>컴퓨터에서 64 비트 Microsoft Windows 운영 체제를 실행 중입니다.</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x64.msi</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## 관련 항목


[App-V 5.1 배포](deploying-app-v-51.md)

[클라이언트 구성 설정 정보](about-client-configuration-settings51.md)

[App-V 5.1 Client 제거 방법](how-to-uninstall-the-app-v-51-client.md)









