---
title: 서버 이벤트 로그
description: 서버 이벤트 로그
author: dansimp
ms.assetid: 04e724d2-28cc-4fa8-86a1-0d4ab0234b11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 269e9b4bc2644fae4dc5796652c7587bb0ef6076
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823383"
---
# 서버 이벤트 로그


이 섹션의 표에서는 MBAM 서버 로그 이벤트 Id에 대 한 정보를 제공 합니다.

## 구성


다음 표에는 구성 중에 MBAM 서버에서 발생할 수 있는 이벤트 Id에 대 한 메시지 및 문제 해결 정보가 나와 있습니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이벤트 ID</th>
<th align="left">소스</th>
<th align="left">이벤트 기호</th>
<th align="left">메시지</th>
<th align="left">문제 해결</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>오류</p></td>
<td align="left"><p>VSS 등록 중에 예외가 발생 했습니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>VssDeregistrationException</p></td>
<td align="left"><p>VSS 등록 취소 중에 예외가 발생 했습니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>300</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>CmdletError</p></td>
<td align="left"><p>폴더 제거에 실패 했습니다.</p></td>
<td align="left"><p>작업을 수행 하는 동안 종료 오류가 발생 했음을 나타냅니다. 로그의 다른 이벤트 메시지를 검사 하 여 MBAM 설정의 진단을 추가 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>301</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>cmdletUnexpectedError</p></td>
<td align="left"><p>예기치 않은 Cmdlet 오류입니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>302</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>CmdletWarning</p></td>
<td align="left"><p>Cmdlet 경고.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>303</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>CmdletInformation</p></td>
<td align="left"><p>Cmdlet 정보</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다. 이 이벤트는 enabling\disabling 기능을 제거 하거나 작업을 취소 하는 등 Cmdlet에서 작업이 수행 되 고 있음을 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>400</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>의 하 중 오류</p></td>
<td align="left"><p>구성자 오류.</p></td>
<td align="left"><p>MBAM 구성자를 시작 하는 동안 오류가 발생 했음을 나타냅니다. 사용자에 게 MBAM 구성자를 시작할 수 있는 적절 한 권한이 있는지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>401</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>ConfiguratorUnexpectedError</p></td>
<td align="left"><p>예기치 않은 구성자 오류.</p></td>
<td align="left"><p>MBAM 구성자 작업을 수행 하는 동안 종료 오류가 발생 했음을 나타냅니다. 오류에 대 한 자세한 내용이 오류 메시지에 포함 됩니다. 이벤트 로그의 다른 오류 메시지를 검사 하 여 MBAM 설정 진단 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>사용자가 선택한 인증서를 검색 하거나 확인 하지 못하는 경우</p></li>
<li><p>보고서 URL 구문 분석 실패</p></li>
<li><p>사용자에 대 한 이벤트 로그 열기 실패</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>402</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>모든 메시지</p></td>
<td align="left"><p>구성자 경고.</p></td>
<td align="left"><p>MBAM 구성자 작업이 예상 대로 완료 되지 않지만 완전 하 게 실패 하지 않았음을 나타냅니다. 알려진 작업에는 웹 응용 프로그램 기능에서 구성한 LocalMachine\My 스토어의 인증서 누락 또는 보류 중인 작업에 대 한 시간 제한 등이 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>410</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>모든 정보</p></td>
<td align="left"><p>구성자 정보.</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다. 이 이벤트는 MBAM 구성자에 의해 작업이 호출 되 고 있음을 나타냅니다. 알려진 작업은 다음과 같습니다.</p>
<ul>
<li><p>구성자 시작</p></li>
<li><p>MBAM 기능에 대 한 소프트웨어 필수 구성 요소 확인</p></li>
<li><p>MBAM 기능에 대 한 매개 변수 유효성 검사</p></li>
<li><p>MBAM 기능 Enabling\disabling\committing</p></li>
<li><p>구성자에서 PowerShell 스크립트 생성</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>500</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>WebProviderUnexpectedError</p></td>
<td align="left"><p>웹 응용 프로그램 공급자의 예기치 않은 오류입니다.</p></td>
<td align="left"><p>IIS에서 MBAM 웹 사이트 또는 웹 서비스를 사용 하도록 설정 하 고 구성 하는 동안 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>IIS WWW 루트 폴더 찾기 실패</p></li>
<li><p>잘못 된 파일 또는 누락 된 설정으로 인해 web.config에서 IIS 구성에 액세스 하지 못했습니다.</p></li>
<li><p>웹 응용 프로그램 만들기 또는 제거 실패</p></li>
<li><p>IIS 액세스 위반</p></li>
</ul>
<p>이 오류는 MBAM에서 사용자 계정의 유효성을 검사 하기 위해 AD (Active Directory)에 액세스할 수 없는 경우에도 기록 됩니다. IIS가 설치 되어 있고 올바르게 구성 되어 있고 IIS 서비스가 실행 중인지 확인 합니다. 모든 MBAM 소프트웨어 필수 구성 요소 확인이 통과 하는지 확인 합니다. 사용자에 게 IIS 인스턴스에서 웹 응용 프로그램을 만들 수 있는 올바른 권한이 있는지 확인 합니다. 사용자에 게 AD의 사용자 계정 개체를 읽을 수 있는 액세스 권한이 있는지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>501</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>WebProviderError</p></td>
<td align="left"><p>웹 응용 프로그램 공급자의 예기치 않은 오류입니다.</p></td>
<td align="left"><p>IIS에서 MBAM 웹 사이트 또는 웹 서비스를 사용, 사용 안 함 또는 구성 하는 동안 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>IIS에서 기본 또는 WSHttp 바인딩 정보를 읽지 못하는 경우</p></li>
<li><p>IIS 구성 파일의 identity 섹션에 id 섹션 또는 DNS 항목이 없음</p></li>
<li><p>레지스트리 키 HKLM\SOFTWARE\Microsoft\InetStp 열기 실패</p></li>
<li><p>레지스트리 키에서 PathWWWRoot 값을 읽지 못했습니다. HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>사용자가 MBAM에 예약 된 이름을 사용 하 여 가상 디렉터리 이름을 지정 하려고 합니다.</p></li>
</ul>
<p>IIS가 설치 되어 있고 올바르게 구성 되어 있는지 확인 합니다. 레지스트리 키 HKLM\SOFTWARE\Microsoft\InetStp가 있는지, 경로를 사용할 수 있는지 확인 합니다. IIS의 바인딩 정보가 손상 되지 않았는지 확인 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>502</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>WebProviderWarning</p></td>
<td align="left"><p>웹 응용 프로그램 공급자 경고.</p></td>
<td align="left"><p>MBAM 웹 사이트 또는 웹 서비스를 사용 하도록 설정 하는 동안 비 종료 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>앱 풀 계정에서 SPN (서비스 사용자 이름)의 유효성을 검사 하기 위해 AD에 액세스 하지 못하는 경우</p></li>
<li><p>AD의 여러 계정에 할당 되어 SPN의 유효성 검사 실패</p></li>
<li><p>AD의 앱 풀 계정에 SPN을 등록 하지 못하는 경우</p></li>
<li><p>SPN이 AD의 앱 풀 이외의 계정에 등록 되어 있습니다.</p></li>
<li><p>롤백 작업 중 AD의 앱 풀 계정에서 SPN을 제거 하지 못하는 경우</p></li>
<li><p>IIS_IUSRS 그룹에 IIS 서버에서 일괄 작업으로 로그온 권한이 부여 되었는지 확인 하지 못했습니다.</p></li>
</ul>
<p>이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다. MBAM 설정이 실행 되는 서버에서 광고에 연결할 수 있는지 확인 합니다. MBAM 설정을 실행 중인 사용자에 게 AD의 앱 풀 계정에 대 한 읽기 권한이 있는지 확인 합니다. SPN이 이미 AD의 앱 풀 계정에 등록 되어 있는 경우 다른 계정에 등록 되어 있지 않은지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>503</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>WebProviderInformation</p></td>
<td align="left"><p>웹 응용 프로그램 공급자 정보. 설명은</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다. 이 이벤트는 MBAM 설정에 의해 작업이 호출 되 고 있음을 나타냅니다. 알려진 작업에는 바인딩 정보 및 루트 사이트 등의 IIS 구성 가져오기, SPN (서비스 사용자 이름) 구성 등이 포함 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>600</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>SetupUnexpectedError</p></td>
<td align="left"><p>예기치 않은 설치 오류입니다.</p></td>
<td align="left"><p>MBAM 기능을 enabling\disabling 하거나 구성 하는 동안 종료 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>오류가 발생 한 후 작업을 롤백하는 데 실패 한 경우</p></li>
<li><p>레지스트리에서 읽지 못하는 경우</p></li>
<li><p>파일 시스템에서 폴더 만들기 또는 삭제 실패</p></li>
<li><p>SQL 버전 정보 읽기 실패</p></li>
<li><p>SQL에서 VSS 기록기 등록 실패</p></li>
</ul>
<p>이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다. 모든 MBAM 소프트웨어 필수 구성 요소 검사 통과 여부를 확인 합니다. MBAM 레지스트리 경로가 존재 하는 경우 \SOFTWARE\Microsoft\MBAM Server HKEY_LOCAL_MACHINE 하 고 모든 하위 키를 읽을 수 있는지 확인 합니다. MBAM 설정이 실행 되는 서버에서 광고에 연결할 수 있는지 확인 합니다. MBAM 설정을 실행 중인 사용자에 게 AD에서 읽기 권한이 있는지 확인 합니다.</p>
<p>VSS 기록기 등록이 성공적으로 수행 되는 경우 지원 되는 SQL 버전이 설치 되어 있고 MBAM 설정을 실행 하는 사용자가 인스턴스에 액세스할 수 있는지 확인 합니다. MBAM 기능을 사용 하지 않도록 설정 하거나 MBAM을 제거 하면 로그 파일 및 web.config 파일 등의 모든 파일이 닫혔는지 확인 하 여 MBAM에서 웹 사이트와 웹 서비스를 제거할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>601</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>SetupError</p></td>
<td align="left"><p>설치 오류.</p></td>
<td align="left"><p>MBAM 기능을 enabling\disabling 하거나 구성 하는 동안 종료 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>IIS에서 MBAM 구성 읽기 실패</p></li>
<li><p>IIS 구성의 appSettings 섹션 손상 또는 잘못 된 설정</p></li>
<li><p>호스트 이름 유효성 검사 실패</p></li>
<li><p>SQL 버전 정보 읽기 실패</p></li>
<li><p>SQL에서 VSS 기록기 등록 실패</p></li>
</ul>
<p>이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다. IIS가 올바르게 설치 되 고 구성 되었는지 확인 합니다. 모든 MBAM 소프트웨어 필수 구성 요소 검사 통과 여부를 확인 합니다. VSS 기록기 등록이 성공적으로 수행 되는 경우 지원 되는 SQL 버전이 설치 되어 있고 MBAM 설정을 실행 하는 사용자가 인스턴스에 액세스할 수 있는지 확인 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>602</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>SetupWarning</p></td>
<td align="left"><p>설정 경고.</p></td>
<td align="left"><p>CM (구성 관리자) 통합 또는 MBAM 웹 응용 프로그램과 같은 MBAM 기능을 enabling\disabling 하거나 구성 하는 동안 비 종료 오류가 발생 했음을 나타냅니다. 알려진 오류에는 CM의 SRS 역할 점에서 MBAM 보고서를 삭제 하는 것이 실패 하 고 도메인 컨트롤러에서 호스트 이름을 확인 하지 못합니다. 이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다.</p>
<p>MBAM 설정이 실행 되는 서버에서 광고에 연결할 수 있는지 확인 합니다. MBAM 설정을 실행 중인 사용자가 CM에서 SRS 역할 점으로 구성 된 SSRS 인스턴스에 대 한 제거 권한을가지고 있는지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>603</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>SetupInformation</p></td>
<td align="left"><p>설정 정보.</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>605</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>Webprovider\오류 검사기</p></td>
<td align="left"><p>하나 이상의 소프트웨어 종속성이 충족 되지 않아 웹 응용 프로그램을 사용 하도록 설정할 수 없습니다.</p></td>
<td align="left"><p>MBAM 웹 사이트/웹 서비스 설치 시 MBAM 설치는 필요한 필수 조건이 있는지 확인 합니다. 이 메시지는 필요한 필수 구성 요소가 없기 때문에 MBAM이 요청 된 웹 사이트/웹 서비스 설치에 실패 했음을 나타냅니다. 누락 된 필수 구성 요소에 대 한 자세한 정보를 확인 하려면이 메시지 앞에 나오는 오류 메시지를 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>606</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailure 오류</p></td>
<td align="left"><p>서버 기능을 사용 하도록 설정 하는 데 필요한 매개 변수가 지정 되지 않았거나 유효성 검사를 통과 하지 못했습니다.</p></td>
<td align="left"><p>MBAM 기능을 구성 하는 데 필요한 매개 변수가 지정 되지 않았거나 유효성 검사를 통과 하지 못했음을 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>607</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailureWithError</p></td>
<td align="left"><p>서버 기능을 사용 하도록 설정 하는 데 필요한 지정 된 매개 변수의 유효성을 검사 하는 동안 오류가 발생 했습니다.</p></td>
<td align="left"><p>서버 기능을 사용 하도록 설정 하는 데 필요한 지정 된 매개 변수의 유효성을 검사 하는 동안 오류가 발생 했음을 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>700</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>DbProviderUnexpectedError</p></td>
<td align="left"><p>DB 공급자 예기치 않은 오류입니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>701</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>DbProviderError</p></td>
<td align="left"><p>DB 공급자 오류입니다.</p></td>
<td align="left"><p>실제 오류에 대 한 자세한 정보를 제공 해야 하는 EventDetails 섹션에 포함 된 메시지입니다. 다음은 확인할 영역입니다.</p>
<ul>
<li><p>MBAM 설치에서 제공 된 연결 정보를 사용 하 여 데이터베이스에 연결 하지 못했습니다. MBAM 설정에 제공 된 연결 문자열 세부 정보를 확인 합니다.</p></li>
<li><p>MBAM 설정 제공 된 도메인 계정 자격 증명을 사용 하 여 지정 된 데이터베이스에 연결할 수 없습니다. 도메인 계정 사용자 이름 및 암호가 유효한 지 확인 합니다.</p></li>
<li><p>MBAM 설정 제공 된 도메인 계정 자격 증명을 사용 하 여 지정 된 데이터베이스에 연결할 수 없습니다. 제공 된 도메인 계정에 MBAM 데이터베이스에 연결 하는 데 필요한 권한이 있는지 확인 합니다.</p></li>
<li><p>새 버전의 MBAM 데이터베이스가 이미 설치 되어 있는 경우 MBAM Dac pac가 실패 합니다. 새 버전의 MBAM가 지정 된 SQL server에 없는지 확인 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>702</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>DbProviderWarning</p></td>
<td align="left"><p>DB 공급자 경고.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>703</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>DbProviderInformation</p></td>
<td align="left"><p>DB 공급자 정보입니다.</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>704</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>DbProviderDacError</p></td>
<td align="left"><p>데이터 계층 응용 프로그램을 배포 하는 동안 오류가 발생 했습니다.</p></td>
<td align="left"><p>MBAM은 데이터베이스를 데이터 계층 응용 프로그램으로 패키지화 하 고 DacServices를 사용 하 여 등록 하려고 합니다. 컨텍스트의 오류 메시지는 DAC 서비스에서 보고 됩니다. 이벤트는 발생 한 원인에 대 한 자세한 정보를 포함 해야 합니다. 오류 메시지의 정보를 읽고 문제를 해결 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>705</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>DbProviderDacWarning</p></td>
<td align="left"><p>데이터 계층 응용 프로그램을 배포 하는 동안 경고가 발생 했습니다.</p></td>
<td align="left"><p>MBAM은 해당 데이터베이스를 데이터 계층 응용 프로그램으로 패키지화 하 고 DacServices를 사용 하 여 등록 하려고 합니다. 컨텍스트에서 경고 메시지가 DAC 서비스에서 보고 됩니다. 이벤트는 발생 한 원인에 대 한 자세한 정보를 포함 해야 합니다. 경고 메시지의 정보를 읽고 문제를 해결 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>706</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>DbProviderDacInformation</p></td>
<td align="left"><p>데이터 계층 응용 프로그램을 배포 하는 동안 메시지가 발생 했습니다.</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>800</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>ReportProviderUnexpectedError</p></td>
<td align="left"><p>보고서 공급자의 예기치 않은 오류입니다.</p></td>
<td align="left"><p>보고서 공급자의 예기치 않은 오류입니다. 설명은 {exceptionDetails} 발생할 수 있는 예외 정보는 다음과 같습니다.</p>
<p><strong>&#39; {directoryName} 디렉터리의 이름을 가져오는 동안 오류가 발생 했습니다 &#39;</strong></p>
<p><strong>디렉터리 &#39; {directoryName}에 대 한 파일을 가져오는 동안 예외가 발생 했습니다 &#39;</strong></p>
<p><strong>디렉터리 &#39; {directoryName}에서 디렉터리를 열거 하는 동안 예외가 발생 했습니다 &#39;</strong></p>
<p><strong>파일 &#39; {fileName}에 대 한 모든 바이트를 읽는 동안 예외가 발생 했습니다 &#39;</strong></p>
<p>MBAM 설치 중에 모든 보고서 파일을 지정 된 설치 경로에 unzips 설정 합니다. 보고서 설치의 일부로 설치 모듈은 설치 경로에서 압축을 푼 보고서 파일에 액세스 하 고 SQL Reporting services와 통신 하 여 보고서 파일을 게시 하려고 합니다. 위의 오류는 MBAM 설치 경로에서 파일/폴더에 액세스할 수 없는 경우에 발생 합니다. 다음은이 문제를 해결 하기 위한 몇 가지 팁입니다.</p>
<ul>
<li><p>MBAM이 설치 되어 있는지 확인 합니다.</p></li>
<li><p>Regkey HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\InstallationPath이 있고 실행 중인 사용자에 게 액세스할 수 있는지 확인 합니다.</p></li>
<li><p>MBAM 설치 경로에 있는 보고서 파일의 경로가 248 자를 초과 하지 않는지 확인 합니다.</p></li>
<li><p>설치 후 MBAM 설치 폴더 또는 MBAM 설치 경로에 포함 된 파일이 수정 되지 않았는지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 MBAM 설치 폴더 읽기/쓰기 권한이 있는지 확인 합니다.</p></li>
</ul>
<p><strong>Reporting Services 연결에 실패 했습니다. {exceptionDetails}</strong></p>
<p>MBAM 보고서 설치 중에 모듈은 SSRS 웹 서비스와 통신 하 여 폴더를 만들고 보고서를 게시 하려고 합니다. 위의 메시지는 MBAM이 SSRS 웹 서비스를 찾거나 통신할 수 없음을 나타냅니다. 다음은이 문제를 해결 하기 위한 몇 가지 팁입니다.</p>
<ul>
<li><p>지정 된 컴퓨터에 SSRS가 설치 되어 있는지 확인 합니다.</p></li>
<li><p>SSRS 콘솔을 사용 하 여 SSRS가 사용 하도록 설정 되 고 실행 중인지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 SSRS에 액세스할 권한이 있는지 확인 합니다.</p></li>
</ul>
<p><strong>Reporting Services 인스턴스 URL &#39; {SSRSInstanceUrl} &#39;을 (를) 사용 하 여 MBAM 보고서를 제거 하지 못했습니다. MBAM 보고서에 필요한 SSRS 인스턴스가 실행 중이 고 올바르게 구성 되어 있는지 확인 합니다.</strong></p>
<p>MBAM 설치가 실패 하거나 사용자가 MBAM 보고 기능을 사용 하지 않도록 설정 하면 설치 모듈이 SSRS 보고서를 제거 합니다. 위의 메시지는 MBAM이 SSRS 보고서 제거에 실패 했음을 나타냅니다. 다음은이 문제를 해결 하기 위한 몇 가지 팁입니다.</p>
<ul>
<li><p>지정 된 컴퓨터에 SSRS가 설치 되어 있는지 확인 합니다.</p></li>
<li><p>SSRS 콘솔을 사용 하 여 SSRS가 사용 하도록 설정 되 고 실행 중인지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 SSRS에 액세스할 권한이 있는지 확인 합니다.</p></li>
</ul>
<p><strong>보고서를 게시 하는 동안 오류가 발생 했습니다. {exceptionDetails}.</strong></p>
<p>MBAM 보고서 설치 중에 모듈은 SSRS 웹 서비스와 통신 하 여 폴더를 만들고 보고서를 게시 하려고 합니다. 위의 메시지는 SSRS 웹 서비스가 보고서를 게시 하는 동안 보고 되 고 예외를 표시 합니다. 다음은이 문제를 해결 하기 위한 몇 가지 팁입니다.</p>
<ul>
<li><p>SSRS 콘솔을 사용 하 여 SSRS가 사용 하도록 설정 되 고 실행 중인지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 보고서에 대 한 액세스/게시 권한이 있는지 확인 합니다.</p></li>
</ul>
<p><strong>그룹 사용자 이름 &#39; {userName} &#39;이 (가) 이미 있습니다. 이 잘못 된 경우에는 중복 되거나 잘못 된 정책에 대 한 보고 서비스를 수동으로 수정 합니다.</strong></p>
<p>Mbam 보고서를 게시 한 후 MBAM 설정에서 MBAM 보고서 사용자 역할 (아직 없는 경우)을 만들고 해당 하는 사용자 정책을 설정 하려고 합니다. 위의 오류는 보고서 사용자 역할 정책을 설정 하는 동안 SSRS 웹 서비스가 예외를 throw 했음을 나타냅니다. 이벤트 메시지의 지침에 따라 다음을 참조 하세요 &quot; <a href="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;ProdVer=8.00&amp;EvtID=rsInvalidPolicyDefinition&amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;LCID=1033&amp;quot" data-raw-source="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;amp;ProdVer=8.00&amp;amp;EvtID=rsInvalidPolicyDefinition&amp;amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;amp;LCID=1033&amp;quot"> https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp . ProdVer = 8.00 &amp; evtid = Rsin, Policydefinition &amp; evtsrc = Microsoft ReportingServices. 문자열 &amp; LCID = 1033&" </a> ; 자세한 도움말</p>
<p><strong>SSRS {exceptionDetails}에 대 한 액세스 유효성을 검사 하는 동안 오류가 발생 했습니다.</strong></p>
<p>필수 구성 요소 확인의 일부로, MBAM 설치는 사용자가 SSRS 아래에서 폴더에 액세스/만드는 데 필요한 권한이 있는지 확인 합니다. 오류 메시지는 SSRS에 대 한 액세스를 확인 하는 동안 예외가 발생 했음을 나타냅니다. 디버깅 팁에 대 한 예외 정보를 참조 하세요.</p>
<p><strong>SSRS URL을 확인 하는 동안 SOAP 오류가 발생 했습니다. {exceptionDetails}</strong></p>
<p><strong>SSRS URL을 확인 하는 동안 웹 오류가 발생 했습니다. {exceptionDetails}</strong></p>
<p><strong>SSRS URL을 확인 하는 동안 http/https 오류가 발생 했습니다. {exceptionDetails}</strong></p>
<p><strong>SSRS URL을 확인 하는 동안 오류가 발생 했습니다. {exceptionDetails}</strong></p>
<p>필수 구성 요소 확인의 일부로 MBAM setup은 제공 된 SSRS 인스턴스와 연결 된 Url을 검색 하 고 SSRS 웹 서비스와 통신을 시도 합니다. 위의 오류 메시지는 지정 된 URL에 대 한 SSRS 웹 서비스에서 예외를 throw 했음을 나타냅니다. 자세한 내용은 예외 정보를 참조 하세요. 다음은 SSRS 통신 문제를 해결 하기 위한 몇 가지 팁입니다.</p>
<ul>
<li><p>지정 된 컴퓨터에 SSRS가 설치 되어 있는지 확인 합니다.</p></li>
<li><p>SSRS 콘솔을 사용 하 여 SSRS가 사용 하도록 설정 되 고 실행 중인지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 SSRS에 액세스할 권한이 있는지 확인 합니다.</p></li>
</ul>
<p><strong>SSRS 버전을 검색 하는 동안 오류가 발생 했습니다. {exceptionDetails}</strong></p>
<p>필수 구성 요소 확인의 일환으로, MBAM 설치는 WMI를 쿼리하여 제공 된 SSRS 인스턴스와 연결 되는 버전 번호를 검색 합니다. 위의 오류 메시지는 WMI를 쿼리 하는 동안 예외가 발생 했음을 나타냅니다. 자세한 내용은 exceptionDetails를 참조 하세요. 수행할 수 있는 검사는 다음과 같습니다.</p>
<ul>
<li><p>지정 된 인스턴스 이름을 가진 SSRS가 지정한 컴퓨터에 설치 되어 있는지 확인 합니다.</p></li>
<li><p>SSRS 콘솔을 사용 하 여 SSRS가 사용 하도록 설정 되 고 실행 중인지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 WMI 네임 스페이스에서 SSRS 클래스를 쿼리할 권한이 있는지 확인 합니다.</p></li>
</ul>
<p><strong>현재 사용자는 &#39; {ssrsWMINamespace} &#39; WMI 네임 스페이스에 액세스할 수 있는 권한이 없습니다.</strong></p>
<p><strong>네임 스페이스 &#39; {ssrsWMINamespace} &#39;을 (를) 열거 하는 동안 오류가 발생 했습니다. 로컬 호스트의 SSRS WMI 공급자에 대 한 RPC 서버를 찾을 수 없습니다.</strong></p>
<p><strong>네임 스페이스 &#39; {ssrsNamespace} &#39;을 (를) 열거 하는 동안 오류가 발생 했습니다. 로컬 호스트에서 SSRS 인스턴스를 찾을 수 없습니다.</strong></p>
<p><strong>WMI에 액세스 하는 동안 오류가 발생 했습니다. &#39; {ssrsInstance} &#39; 인스턴스에 대 한 RPC 서버를 찾을 수 없습니다.</strong></p>
<p><strong>WMI에 액세스 하는 동안 오류가 발생 했습니다. &#39; {ssrsInstanceName} &#39;에 대 한 인스턴스 이름이 올바르지 않습니다.</strong></p>
<p><strong>WMI에 액세스 하는 동안 오류가 발생 했습니다. 로컬 호스트에서 &#39; 인스턴스 &#39; {ssrsInstanceName}을 (를) 찾을 수 없습니다.</strong></p>
<p>필수 구성 요소 확인의 일부로 MBAM은 WMI를 쿼리하여 주어진 인스턴스와 연결 된 WMI 네임 스페이스를 검색 합니다. 위의 오류 메시지는 WMI를 쿼리 하는 동안 예외가 발생 했음을 나타냅니다. 자세한 내용은 exceptionDetails를 참조 하세요. 수행할 수 있는 검사는 다음과 같습니다.</p>
<ul>
<li><p>지정 된 인스턴스 이름을 가진 SSRS가 지정한 컴퓨터에 설치 되어 있는지 확인 합니다.</p></li>
<li><p>SSRS 콘솔을 사용 하 여 SSRS가 사용 하도록 설정 되 고 실행 중인지 확인 합니다.</p></li>
<li><p>설치 프로그램을 실행 하는 사용자에 게 WMI 네임 스페이스에서 SSRS 클래스에 대 한 액세스/쿼리 권한이 있는지 확인 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>801</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>ReportProviderError</p></td>
<td align="left"><p>보고서 공급자의 예기치 않은 오류입니다.</p></td>
<td align="left"><p>SQL server reporting services 인스턴스 이름이 지정 된 경우 MBAM은 보고 인스턴스에 해당 하는 WMI 네임 스페이스를 찾아 연결 하려고 합니다. 이 오류는 mbam이 SSRS WMI 네임 스페이스에 대 한 연결을 검색 하거나 시도 하는 경우에 예외가 발생 합니다. 이 메시지에 대 한 자세한 내용을 보려면 MBAM 설정 채널에 기록 된 오류 메시지의 정보를 읽으십시오. 확인할 수 있는 작업은 다음과 같습니다.</p>
<ul>
<li><p>제공 된 인스턴스 이름을 가진 SSRS가 작동 중인지 확인 합니다.</p></li>
<li><p>MBAM 설치를 실행 하는 사용자 계정에 SSRS WMI 네임 스페이스를 쿼리하거나 연결 하는 데 필요한 권한이 있는지 확인 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>802</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>ReportProviderWarning</p></td>
<td align="left"><p>보고서 공급자 경고.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>803</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>ReportProviderInformation</p></td>
<td align="left"><p>공급자 정보를 보고 합니다.</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>900</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>CMProviderUnexpectedError</p></td>
<td align="left"><p>CM 공급자의 예기치 않은 오류입니다.</p></td>
<td align="left"><p>MBAM의 CM (구성 관리자) 통합 기능을 enabling\disabling 하거나 구성 하는 동안 종료 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>SMS 공급자를 통해 CM 사이트 서버에 연결 하지 못하는 경우</p></li>
<li><p>레지스트리에서 읽지 못하는 경우</p></li>
<li><p>파일 시스템에서 폴더 만들기 또는 삭제 실패</p></li>
<li><p>로컬 컴퓨터에서 Configuration Manager 콘솔 설치를 찾지 못했습니다.</p></li>
<li><p>CM의 SRS 역할 점으로 구성 된 SSRS 인스턴스에 대 한 정보를 검색 하지 못하는 경우</p></li>
</ul>
<p>이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다. 모든 MBAM 소프트웨어 필수 구성 요소 검사 통과 여부를 확인 합니다. MBAM 레지스트리 경로가 존재 하는 경우 \SOFTWARE\Microsoft\MBAM Server HKEY_LOCAL_MACHINE 하 고 모든 하위 키를 읽을 수 있는지 확인 합니다. MBAM이 지원 되는 버전의 Configuration Manager와 통합 되어 있는지 확인 합니다. MBAM 설정이 호출 되는 컴퓨터에 Configuration Manager 콘솔이 설치 되어 있고 콘솔을 대상 CM 사이트 서버에 연결 하는 데 사용할 수 있는지 확인 합니다. 유효한 SSRS 인스턴스가 CM에서 SRS 역할 점으로 구성 되어 있고 MBAM 설정 실행 사용자에 게 SSRS 인스턴스에 대 한 read\write 권한이 있는지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>901</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/Admin</p></td>
<td align="left"><p>CMProviderError</p></td>
<td align="left"><p>CM 공급자의 예기치 않은 오류입니다.</p></td>
<td align="left"><p>MBAM의 CM (구성 관리자) 통합 기능을 enabling\disabling 하거나 구성 하는 동안 종료 오류가 발생 했음을 나타냅니다. 알려진 오류는 다음과 같습니다.</p>
<ul>
<li><p>SMS 공급자를 통해 CM 사이트 서버에 연결 하지 못하는 경우</p></li>
<li><p>레지스트리에서 읽지 못하는 경우</p></li>
<li><p>파일 시스템에서 폴더 만들기 또는 삭제 실패</p></li>
<li><p>로컬 컴퓨터에서 Configuration Manager 콘솔 설치를 찾지 못했습니다.</p></li>
<li><p>SRS 역할 지점의 루트 폴더로 서 SSRS에 ConfigMgr 폴더가 없음</p></li>
<li><p>SSRS에 ConfigMgr 공유 데이터 원본이 없음</p></li>
<li><p>CM의 SRS 역할 점으로 구성 된 SSRS 인스턴스에서 SSRS 보고서를 배포 하지 못하는 경우</p></li>
<li><p>CM에서 구성 항목 및 기준을 만들지 못하는 경우</p></li>
</ul>
<p>이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다. 모든 MBAM 소프트웨어 필수 구성 요소 검사 통과 여부를 확인 합니다. MBAM 레지스트리 경로가 존재 하는 경우 \SOFTWARE\Microsoft\MBAM Server HKEY_LOCAL_MACHINE 하 고 모든 하위 키를 읽을 수 있는지 확인 합니다. MBAM이 지원 되는 버전의 Configuration Manager와 통합 되어 있는지 확인 합니다. MBAM 설정이 호출 되는 컴퓨터에 Configuration Manager 콘솔이 설치 되어 있고 콘솔을 대상 CM 사이트 서버에 연결 하는 데 사용할 수 있는지 확인 합니다. 사용자에 게 CM에서 구성 항목, 기준 및 컬렉션을 만드는 데 필요한 read\write 권한이 있는지 확인 합니다. 유효한 SSRS 인스턴스가 CM에서 SRS 역할 점으로 구성 되어 있고 MBAM 설정 실행 사용자에 게 SSRS 인스턴스에 대 한 read\write 권한이 있는지 확인 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>902</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>CMProviderWarning</p></td>
<td align="left"><p>CM 공급자 경고입니다.</p></td>
<td align="left"><p>CM (구성 관리자) 통합 기능을 사용 하도록 설정 하는 동안 비 종료 오류가 발생 했음을 나타냅니다. 알려진 오류에는 m AM에서 지원 되는 컴퓨터 컬렉션의 CM 및 기타 SSRS 및 네트워크 관련 오류에 대 한 컬렉션 규칙 커밋을 실패 합니다.</p>
<p>이벤트 메시지에는 특정 오류에 대 한 자세한 정보가 포함 됩니다. 이 경고를 발생 시킨 일부 작업은 경고 후에 만료 됩니다. 몇 번의 재시도 후에도 오류가 계속 되 면 MBAM이 실제 오류로 끝날 가능성이 있습니다. 로그의 다른 이벤트 메시지를 검사 하 여 MBAM 설정의 진단을 추가 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>903</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-서버/운영</p></td>
<td align="left"><p>CMProviderInformation</p></td>
<td align="left"><p>CM 공급자 정보입니다.</p></td>
<td align="left"><p>정보용 으로만 가능 합니다. 문제 해결이 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

## 작업


다음 표에는 MBAM이 실행 되는 동안 발생할 수 있는 이벤트 Id에 대 한 메시지 및 문제 해결 정보가 나와 있습니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이벤트 ID</th>
<th align="left">소스</th>
<th align="left">이벤트 기호</th>
<th align="left">메시지</th>
<th align="left">문제 해결</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>raid-1</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>WebAppSpnError</p></td>
<td align="left"><p>Application: {SiteName} {VirtualDirectory}에 다음 Spn (서비스 사용자 이름)이 없습니다: {ListOfSpns} 계정: {ExecutionAccount}에 필요한 Spn을 등록 합니다.</p></td>
<td align="left"><p>Windows 통합 인증을 성공적으로 수행 하려면 필요한 Spn을 준비 해야 합니다. 이 메시지는 MBAM 응용 프로그램에 필요한 SPN이 올바르게 구성 되지 않았음을 나타냅니다. 이 이벤트에 포함 된 세부 정보는 자세한 정보를 제공 해야 합니다.</p>
<p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams)">자세한 내용은 mbam 2.5 서버 필수 구성 요소 및 독립 실행형 및 구성 관리자 통합 토폴로지에 대 한 "SPN (서비스 사용자 이름)"을 참조 </a> 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4(tcp/ipv4)</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/운영</p></td>
<td align="left"><p>PerformanceCounterError</p></td>
<td align="left"><p>성능 카운터를 검색 하는 동안 오류가 발생 했습니다.</p>
<p>메시지: {EventMessage} 범주: {Category Ofperformancecounter} 성능 카운터: {NameOfPerformanceCounter} 인스턴스: {성능 카운터 범주 인스턴스의 이름} 예외: {ExceptionThrown}</p>
<p>추적 메시지에는 실제 예외 메시지가 포함 되며, 그 중 일부는 여기에서 설명 합니다.</p>
<p><strong>ArgumentNullException </strong> :이 예외는 요청 된 성능 카운터의 범주, 카운터 또는 인스턴스가 유효 하지 않은 경우에 throw 됩니다.</p>
<p><strong>InvalidOperationException </strong> : 범주는 빈 문자열 ( &quot; &quot; )입니다.-또는-counterName가 빈 문자열 ( &quot; &quot; ) 인 경우</p>
<p>-또는-이 카운터에 대해 요청 된 읽기/쓰기 권한 설정이 잘못 되었습니다.</p>
<p>-또는-지정 된 범주가 없는 경우 (readOnly가 true 인 경우)</p>
<p>-또는-지정 된 범주가 .NET Framework 사용자 지정 범주가 아닌 경우 (readOnly가 false 인 경우)</p>
<p>-또는-지정 된 범주가 다중 인스턴스로 표시 되어 있으며, 인스턴스 이름을 사용 하 여 성능 카운터를 만들어야 합니다.</p>
<p>-또는-instanceName이 127 자를 초과 하는 경우</p>
<p>-또는-범주와 counterName 여러 언어로 지역화 되어 있습니다.</p>
<p><strong>Win32Exception </strong> : 시스템 API에 액세스 하는 동안 오류가 발생 ComponentModel.</p>
<p><strong>PlatformNotSupportedException </strong> : 플랫폼은 성능 카운터를 지원 하지 않는 windows 98 또는 Windows Millennium Edition (ME)입니다.</p>
<p><strong>UnauthorizedAccessException </strong> : 관리 권한 없이 실행 되는 코드가 성능 카운터 읽기를 시도 했습니다.</p></td>
<td align="left"><p>이벤트에 포함 된 메시지는 발생 한 예외에 대 한 자세한 정보를 제공 합니다. UnauthorizedAccessException이 throw 된 경우 MBAM 실행 계정 (앱 풀)에 성능 카운터 Api에 대 한 액세스 권한이 있는지 확인 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>100</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>AdminServiceRecoveryDbError</p></td>
<td align="left"><p><strong>GetMachineUsers </strong> : 데이터베이스에서 사용자 정보를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetRecoveryKey </strong> : 데이터베이스에서 복구 키를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetRecoveryKey </strong> : 데이터베이스에서 사용자 정보를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetRecoveryKeyIds </strong> : 데이터베이스에서 복구 키 id를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetTpmHashForUser </strong> : 복구 데이터베이스에서 TPM 해시 데이터를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetTpmHashForUser </strong> : 복구 데이터베이스에서 TPM 해시 데이터를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>Querydriverec과잉 Ydata </strong> : 데이터베이스에서 드라이브 복구 데이터를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : 데이터베이스에서 복구 키 id를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>QueryVolumeUsers </strong> : 데이터베이스에서 사용자 정보를 가져오는 동안 오류가 발생 했습니다.</p></td>
<td align="left"><p>이 메시지는 MBAM 데이터베이스와 통신 하는 동안 예외가 발생할 때마다 기록 됩니다. 추적에 포함 된 정보를 읽어 예외에 대 한 특정 세부 정보를 가져옵니다.</p>
<p>문제 해결에 대 한 자세한 내용은 <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> SQL Server 데이터베이스 엔진 연결 문제를 해결 하는 방법에 대 한 TechNet 문서를 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>101</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>AdminServiceComplianceDbError</p></td>
<td align="left"><p><strong>GetRecoveryKey </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetRecoveryKeyIds </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>GetTpmHashForUser </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>Querydriverec과잉 Ydata </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}</p></td>
<td align="left"><p>이 메시지는 MBAM 데이터베이스를 통신 하는 동안 예외가 발생할 때마다 기록 됩니다. 추적에 포함 된 정보를 읽어 예외에 대 한 특정 세부 정보를 가져옵니다.</p>
<p>문제 해결에 대 한 자세한 내용은 <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> SQL Server 데이터베이스 엔진 연결 문제를 해결 하는 방법에 대 한 TechNet 문서를 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>102</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>AgentServiceRecoveryDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>이 메시지는 MBAM 서비스가 복구 데이터베이스와 통신 하려고 할 때 발생 하는 예외를 나타냅니다. 이벤트에 포함 된 메시지를 읽어 예외에 대 한 특정 정보를 가져옵니다.</p>
<p><a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)">SQL Server 데이터베이스 엔진에 연결 문제를 해결 하 여 mbam </a> 복구 데이터베이스에서 연결 하거나 실행할 때 사용 권한이 필요한 지 여부를 확인 하는 방법에 대 한 자세한 내용은 TechNet 문서를 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>AgentServiceError</p></td>
<td align="left"><p>클라이언트 컴퓨터 계정 또는 데이터 마이그레이션 사용자 계정을 검색할 수 없습니다. -또는-</p>
<p>발신자 id에 대 한 계정 확인에 실패 했습니다.</p></td>
<td align="left"><p>&quot; &quot; &quot; Mbam 에이전트 서비스의 postkeyrecoveryinfo, isrecoverykeyresetrequired &quot; , &quot; commitrecoverykeyrest &quot; 또는 &quot; gettpmhash 웹 메서드를 호출할 때마다 &quot; 호출자의 자격 증명을 가져오는 호출자 컨텍스트를 검색 합니다. 호출자 컨텍스트가 null 이거나 비어 있으면 MBAM 서비스 로그에서 &quot; 클라이언트 컴퓨터 계정 또는 데이터 마이그레이션 사용자 계정을 검색할 수 없습니다.&quot;</p>
<p>&quot; &quot; 웹 메서드에서 호출자를 컴퓨터 계정으로 예상 하 고 호출자가 컴퓨터 계정이 아니거나 웹 메서드가 사용자 계정 이거나 데이터 마이그레이션 그룹 계정의 구성원이 아닌 경우 호출자가 호출자 id를 확인 하는 데 실패 하는 경우 메시지 계정이 기록 됩니다. excepting</p></td>
</tr>
<tr class="odd">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>StatusServiceComplianceDbConfigError</p></td>
<td align="left"><p>&quot;레지스트리의 준수 데이터베이스 연결 문자열이 비어 있습니다.&quot;</p></td>
<td align="left"><p>이 메시지는 규정 준수 db 연결 문자열이 잘못 된 경우에 기록 됩니다.</p>
<p>레지스트리 키 HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString에서 값을 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>105</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>StatusServiceComplianceDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>이 오류는 MBAM 웹 사이트/웹 서비스가 Mbam준수 데이터베이스에 연결할 수 없음을 나타냅니다.</p>
<p><a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> </a> IIS 앱 풀 계정이 mbam 준수 데이터베이스에 연결할 수 있는지 확인 하려면 SQL Server 데이터베이스 엔진 연결 문제를 해결 하는 방법에 대해 설명 하는 TechNet 문서를 참조 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>106</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>HelpdeskError</p></td>
<td align="left"><p>URL {url}에 대 한 요청에서 내부 오류가 발생 했습니다. -또는-</p>
<p>실행 컨텍스트 정보를 가져오는 동안 오류가 발생 했습니다. SPN (서비스 사용자 이름) 등록을 확인할 수 없습니다. -또는-</p>
<p>SPN (서비스 사용자 이름) 등록을 확인 하는 동안 오류가 발생 했습니다.</p></td>
<td align="left"><p>처리 되지 않은 예외가 헬프 데스크 응용 프로그램에서 발생 했음을 나타냅니다. MBAM 관리 작업 채널의 로그 항목을 검토 하 여 특정 예외를 찾습니다. 또는</p>
<p>초기 헬프데스크 웹 사이트 로드 작업 중에 SPN 검사를 수행 합니다. SPN을 확인 하기 위해 헬프 데스크에는 실행 계정 정보, IIS Sitename 및 헬프데스크 웹사이트에 해당 하는 ApplicationVirtualPath 필요 합니다. 이 오류 메시지는 해당 중 하나 이상이 유효 하지 않거나 누락 된 경우 기록 됩니다. 또는</p>
<p>이 메시지는 SPN 확인을 수행 하는 동안 보안 예외가 발생 했음을 나타냅니다. 이벤트 세부 정보 섹션에 포함 된 예외를 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>107</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>SelfServicePortalError</p></td>
<td align="left"><p>사용자에 대 한 복구 키를 가져오는 동안 오류가 발생 했습니다. EventDetails: {ExceptionMessage}-또는-</p>
<p>실행 컨텍스트 정보를 가져오는 동안 오류가 발생 했습니다. SPN (서비스 사용자 이름) 등록을 확인할 수 없습니다. EventDetails: User: {username Id} 응용 프로그램: {SiteName\ApplicationVirtualPath}-또는-</p>
<p>SPN (서비스 사용자 이름) 등록을 확인 하는 동안 오류가 발생 했습니다. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>복구 키를 검색 하기 위해 요청을 했을 때 예기치 않은 예외가 발생 했음을 나타냅니다. 이벤트 세부 정보 섹션에 포함 된 예외 메시지를 참조 하세요. MBAM 헬프데스크에서 추적을 사용 하는 경우 자세한 예외 메시지를 얻으려면 추적 데이터를 참조 하세요. 또는</p>
<p>초기 로드 작업 중에 SSP (셀프 서비스 포털)는 셀프 서비스 웹 사이트에 해당 하는 실행 계정 정보, IIS Sitename 및 ApplicationVirtualPath를 검색 하 여 SPN을 확인 합니다. 이 오류 메시지는 하나 이상의 잘못 된 경우 기록 됩니다. 또는</p>
<p>이 메시지는 SPN 확인을 수행 하는 동안 보안 예외가 발생 했음을 나타냅니다. 이벤트 세부 정보 섹션에 포함 된 예외를 참조 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>108</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>DomainControllerError</p></td>
<td align="left"><p>도메인 이름 {DomainName}을 확인 하는 동안 오류가 발생 했습니다. 메모리 할당이 실패 했습니다. -또는-</p>
<p>DsGetDcName 메서드를 호출할 수 없습니다. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>도메인 이름을 확인 하기 위해 MBAM은 &quot; DsGetDcName &quot; windows API를 활용 합니다. 이 메시지는 DsGetDcName이 &quot; &quot; &quot; &quot; 메모리 할당 실패를 나타내는 ERROR_NOT_ENOUGH_MEMORY를 반환 하면 기록 됩니다. 또는</p>
<p>이 메시지는 &quot; &quot; 호스팅 시스템에서 DsGetDcName API 메서드를 사용할 수 없음을 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>109</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>WebAppRecoveryDbError</p></td>
<td align="left"><p>복구 데이터베이스의 구성을 읽는 동안 오류가 발생 했습니다. 복구 데이터베이스에 대 한 연결 문자열이 구성 되지 않았습니다. 메시지: {message}-또는-</p>
<p><strong>DoesUserHaveMatchingRecoveryKey </strong> : 사용자의 복구 키 id를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>Querydriverec과잉 Ydata </strong> : 드라이브 복구 데이터를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : 사용자에 대 한 복구 키 id를 가져오는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p>복구 데이터베이스에서 TPM 암호 해시를 가져오는 동안 오류가 발생 했습니다. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>이 메시지는 HKLM\Software\Microsoft\MBAM Server\Web\RecoveryDBConnectionString에 대 한 복구 데이터베이스 연결 문자열 정보가 &quot; &quot; 유효 하지 않음을 나타냅니다. 지정 된 레지스트리 키 값을 확인 합니다. 또는</p>
<p>나머지 메시지가 기록 된 경우, <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> SQL Server 데이터베이스 엔진 연결 문제를 해결 하 여 </a> 앱 풀 자격 증명을 사용 하는 IIS 서버에서 Mbam 복구 데이터베이스에 연결할 수 있는지 여부를 확인 하는 방법에 대해 설명 하는 TechNet 문서에 나와 있는 문제 해결 단계를 참조 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>110</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>WebAppComplianceDbError</p></td>
<td align="left"><p>준수 데이터베이스의 구성을 읽는 동안 오류가 발생 했습니다. 준수 데이터베이스에 대 한 연결 문자열이 구성 되지 않았습니다. -또는-</p>
<p><strong>GetRecoveryKeyForCurrentUser </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}-또는-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : 감사 이벤트를 준수 데이터베이스에 로깅하는 동안 오류가 발생 했습니다. 메시지: {message}</p></td>
<td align="left"><p>이 메시지는 HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString의 규정 준수 db 연결 문자열 정보가 잘못 되었음을 나타냅니다 &quot; &quot; . 위의 레지스트리 키에 해당 하는 값을 확인 합니다. 또는</p>
<p>나머지 메시지가 기록 된 경우, <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> SQL Server 데이터베이스 엔진 연결 문제를 해결 하 여 </a> 앱 풀 자격 증명을 사용 하는 IIS 서버의 Mbam 준수 데이터베이스에 연결할 수 있는지 여부를 확인 하는 방법에 대해 설명 하는 TechNet 문서에 나와 있는 문제 해결 단계를 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>111</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>WebAppDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>이러한 오류는 다음 두 조건 중 하나를 나타냅니다.</p>
<ul>
<li><p>MBAM 웹 사이트/webservices는 Mbam준수 또는 MBAMRecovery 데이터베이스에 연결할 수 없습니다.</p></li>
<li><p>MBAM websites/webservices 실행 계정 (앱 풀 계정)은 Mbam준수 또는 MBAMRecovery 데이터베이스에서 GetVersion 저장 프로시저를 실행할 수 없습니다.</p></li>
</ul>
<p>이벤트에 포함 된 메시지는 예외에 대 한 자세한 정보를 제공 합니다.</p>
<p><a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)">SQL Server 데이터베이스 엔진 연결 문제를 해결 하 여 </a> mbam 실행 계정 (앱 풀 계정)이 mbam 준수/복구 데이터베이스에 연결할 수 있고 GetVersion 저장 프로시저를 실행할 권한이 있는지 확인 하는 방법에 대해 설명 하는 TechNet 문서에 나와 있는 문제 해결 단계를 참조 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>112</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/관리자</p></td>
<td align="left"><p>WebAppError</p></td>
<td align="left"><p>SPN (서비스 사용자 이름) 등록을 확인 하는 동안 오류가 발생 했습니다. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>SPN 확인을 수행 하기 위해 MBAM은 Active Directory를 쿼리하여 Spn 매핑된 실행 계정 목록을 검색 합니다. 또한 MBAM은ApplicationHost.config를 쿼리하여 &quot; &quot; mbam 웹 사이트 바인딩을 가져옵니다. 이 오류 메시지는 MBAM이 Active Directory와 통신할 수 없거나 applicationHost.config 파일을 로드할 수 없음을 나타냅니다.</p>
<p>실행 계정 (앱 풀 계정)에 광고 또는 ApplicationHost.config 파일을 쿼리할 수 있는 권한이 있는지 확인 합니다. 또한 ApplicationHost.config 파일에서 사이트 바인딩 항목을 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>200</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/운영</p></td>
<td align="left"><p>HelpDeskInformation</p></td>
<td align="left"><p>관리 웹 사이트 응용 프로그램을 찾아 지원 되는 복구 데이터베이스 버전에 연결 했습니다. -또는-</p>
<p>관리 웹 사이트 응용 프로그램을 찾아 지원 되는 버전의 준수 데이터베이스에 연결 했습니다.</p></td>
<td align="left"><p>MBAM 헬프데스크 웹사이트의 복구/준수 데이터베이스에 대 한 성공적인 연결을 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>201</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/운영</p></td>
<td align="left"><p>SelfServicePortalInformation</p></td>
<td align="left"><p>셀프 서비스 포털 응용 프로그램을 찾아 지원 되는 복구 데이터베이스 버전에 연결 했습니다. -또는-</p>
<p>셀프 서비스 포털 응용 프로그램을 찾아 지원 되는 버전의 준수 데이터베이스에 연결 했습니다.</p></td>
<td align="left"><p>MBAM 셀프 서비스 포털에서 복구/준수 데이터베이스에 대 한 성공적인 연결을 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>202</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-웹/운영</p></td>
<td align="left"><p>WebAppInformation</p></td>
<td align="left"><p>응용 프로그램의 Spn이 올바르게 등록 되어 있습니다.</p></td>
<td align="left"><p>MBAM 헬프데스크 웹사이트에 필요한 Spn이 실행 계정에 제대로 등록 되어 있음을 나타냅니다.</p></td>
</tr>
</tbody>
</table>

 


## 관련 항목


[MBAM 2.5에 대한 기술 참조](technical-reference-for-mbam-25.md)

[클라이언트 이벤트 로그](client-event-logs.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





