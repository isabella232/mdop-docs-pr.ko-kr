---
title: App-V 5.1 필수 구성 요소
description: App-V 5.1 필수 구성 요소
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814740"
---
# App-V 5.1 필수 구성 요소


Microsoft App-v (Application Virtualization) 5.1을 설치 하기 전에 다음 필수 필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.

App-v Server, Sequencer 및 클라이언트에 대해 지원 되는 운영 체제 및 하드웨어 요구 사항 목록은 [app-v 5.1 지원 구성을](app-v-51-supported-configurations.md)참조 하세요.

## 각 운영 체제에 사전 설치 된 소프트웨어 요약


다음 표에는 여러 운영 체제에 대해 이미 설치 된 소프트웨어가 표시 되어 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">필수 구성 요소 설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>모든 필수 소프트웨어는 이미 설치 되어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>모든 필수 소프트웨어는 이미 설치 되어 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>Windows 8을 실행 하는 경우 App-v 5.1를 사용 하기 전에 Windows 8.1으로 업그레이드 하세요.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>다음 필수 소프트웨어는 이미 설치 되어 있습니다.</p>
<ul>
<li><p>Microsoft .NET Framework 4.5</p></li>
<li><p>Windows PowerShell 3.0</p>
<div class="alert">
<strong>참고</strong><br/><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>필수 소프트웨어는 아직 설치 되지 않았습니다. App-v를 설치 하려면 먼저 설치 해야 합니다.</p></td>
</tr>
</tbody>
</table>



## App-v Server 필수 구성 요소 소프트웨어


App-v 5.1 서버 구성 요소에 필요한 필수 구성 요소 소프트웨어를 설치 합니다.

### 시작 하기 전에 알아야 할 사항

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 서버 설치 계정</p></td>
<td align="left"><p>App-v 서버 구성 요소를 설치 하는 데 사용 하는 계정에는 다음이 있어야 합니다.</p>
<ul>
<li><p>구성 요소를 설치 하는 컴퓨터에 대 한 관리자 권한</p></li>
<li><p>Active Directory 도메인 서비스를 쿼리 하는 기능입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>포트 및 방화벽</p></td>
<td align="left"><ul>
<li><p>각 구성 요소를 호스트할 포트를 지정 합니다.</p></li>
<li><p>지정 된 포트로 들어오는 요청을 허용 하는 연결 된 방화벽 규칙을 추가 합니다.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>WebDAV (웹 분산 작성 및 버전 관리)</p></td>
<td align="left"><p>WebDAV는 관리 서비스에 대해 자동으로 사용 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원 되는 배포 시나리오</p></td>
<td align="left"><ul>
<li><p>모든 구성 요소가 동일한 서버에 배포 되는 독립 실행형 배포입니다.</p></li>
<li><p>분산 배포.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>지원 되지 않는 배포 시나리오</p></td>
<td align="left"><ul>
<li><p>동일한 서버에 여러 App-v Server 버전의 side-by-side 인스턴스를 설치 합니다.</p></li>
<li><p>Server core 또는 도메인 컨트롤러를 실행 하는 컴퓨터에 App-v 서버 구성 요소 설치</p></li>
</ul></td>
</tr>
</tbody>
</table>



### 관리 서버 필수 구성 요소 소프트웨어

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필수 구성 요소 및 필수 설정</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 SQL Server 버전</p></td>
<td align="left"><p>지원 되는 버전은 <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> app-v 5.1 지원 되는 구성을 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p></td>
<td align="left"><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>KB2533623 다운로드 및 설치 <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"></a></p></td>
<td align="left"><p>Windows 7에만 적용 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64 비트 ASP.NET 등록</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 웹 서버 역할</p></td>
<td align="left"><p>이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 서버 (IIS) 관리 도구</p></td>
<td align="left"><p><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 서버 역할 서비스</p></td>
<td align="left"><p><strong>일반적인 HTTP 기능:</strong></p>
<ul>
<li><p>정적 콘텐츠</p></li>
<li><p>기본 문서</p></li>
</ul>
<p><strong>응용 프로그램 개발:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET 확장성</p></li>
<li><p>ISAPI 확장</p></li>
<li><p>ISAPI 필터</p></li>
</ul>
<p><strong>보안이</strong></p>
<ul>
<li><p>Windows 인증</p></li>
<li><p>요청 필터링</p></li>
</ul>
<p><strong>관리 도구:</strong></p>
<ul>
<li><p>IIS 관리 콘솔</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>기본 설치 위치</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization 서버</p></td>
</tr>
<tr class="odd">
<td align="left"><p>관리 데이터베이스의 위치</p></td>
<td align="left"><p>SQL Server 데이터베이스 이름, SQL Server 데이터베이스 인스턴스 이름, 데이터베이스 이름.</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리 콘솔 및 관리 데이터베이스 권한</p></td>
<td align="left"><p>배포 완료 후 관리 콘솔과 데이터베이스에 액세스할 수 있는 사용자 또는 그룹입니다. 관리 콘솔을 사용 하 여 추가 관리자가 추가 되지 않는 한 이러한 사용자 또는 그룹만 관리 콘솔과 데이터베이스에 액세스할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>관리 서비스 웹 사이트 이름</p></td>
<td align="left"><p>관리 콘솔 웹 사이트의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리 서비스 포트 바인딩</p></td>
<td align="left"><p>관리 서비스의 고유 포트 번호입니다. 이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</p></td>
</tr>
</tbody>
</table>



**중요**  
웹 관리 콘솔을 여는 브라우저에서 JavaScript를 사용 하도록 설정 해야 합니다.



### 관리 서버 데이터베이스 필수 구성 요소 소프트웨어

관리 데이터베이스는 App-v 5.1 관리 서버를 사용 하는 경우에만 필요 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필수 구성 요소 및 필수 설정</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>기본 설치 위치</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization 서버</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우)</p></td>
<td align="left"><p>사용할 형식: <strong> INSTANCENAME</strong></p>
<p>이 형식은 로컬 컴퓨터에 설치 되어 있다고 가정 하 여 결정 됩니다.</p>
<p>SVR\INSTANCE 형식으로 이름을 지정 하면 <strong> </strong> 설치에 실패 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 지정 데이터베이스 이름 (해당 하는 경우)</p></td>
<td align="left"><p>고유한 데이터베이스 이름입니다.</p>
<p>기본값: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리 서버 위치</p></td>
<td align="left"><p>관리 서버가 배포 된 컴퓨터 계정입니다.</p>
<p>사용할 형식: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>관리 서버 설치 관리자</p></td>
<td align="left"><p>관리 서버를 설치 하는 데 사용 되는 계정입니다.</p>
<p>사용할 형식: Domain\관리자 loginname</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 서비스 에이전트</p></td>
<td align="left"><p>Microsoft SQL Server 에이전트 서비스가 자동으로 다시 시작 되도록 관리 데이터베이스 컴퓨터를 구성 합니다. 지침은 <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> 서비스를 자동으로 다시 시작 하도록 SQL Server 에이전트 구성을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



### 게시 서버 필수 구성 요소 소프트웨어

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필수 구성 요소 및 필수 설정</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>64 비트 ASP.NET 등록</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 웹 서버 역할</p></td>
<td align="left"><p>이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 서버 (IIS) 관리 도구</p></td>
<td align="left"><p><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 서버 역할 서비스</p></td>
<td align="left"><p><strong>일반적인 HTTP 기능:</strong></p>
<ul>
<li><p>정적 콘텐츠</p></li>
<li><p>기본 문서</p></li>
</ul>
<p><strong>응용 프로그램 개발:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET 확장성</p></li>
<li><p>ISAPI 확장</p></li>
<li><p>ISAPI 필터</p></li>
</ul>
<p><strong>보안이</strong></p>
<ul>
<li><p>Windows 인증</p></li>
<li><p>요청 필터링</p></li>
</ul>
<p><strong>관리 도구:</strong></p>
<ul>
<li><p>IIS 관리 콘솔</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>기본 설치 위치</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization 서버</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리 서비스 URL</p></td>
<td align="left"><p>App-v 관리 서비스의 URL입니다. 이 포트는 게시 서버와 통신 하는 데 사용 됩니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">설치 아키텍처</th>
<th align="left">URL에 사용할 형식</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>관리 서버와 게시 서버가 동일한 서버에 설치 되어 있는 경우</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>관리 서버와 게시 서버가 서로 다른 서버에 설치 되어 있는 경우</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>게시 서비스 웹 사이트 이름</p></td>
<td align="left"><p>게시 웹 사이트의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>게시 서비스 포트 바인딩</p></td>
<td align="left"><p>게시 서비스에 대 한 고유 포트 번호입니다. 이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</p></td>
</tr>
</tbody>
</table>



### 보고 서버 필수 구성 요소 소프트웨어

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필수 구성 요소 및 필수 설정</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 SQL Server 버전</p></td>
<td align="left"><p>지원 되는 버전은 <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> app-v 5.1 지원 되는 구성을 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64 비트 ASP.NET 등록</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 웹 서버 역할</p></td>
<td align="left"><p>이 역할은 관리 서버에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 서버 (IIS) 관리 도구</p></td>
<td align="left"><p><strong>IIS 관리 스크립트 및 도구를 클릭 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 서버 역할 서비스</p></td>
<td align="left"><p>보고 서버로 원치 않거나 악의적인 데이터를 보내는 위험을 줄이려면 회사 보안 정책에 따라 보고 웹 서비스에 대 한 액세스를 제한 해야 합니다.</p>
<p><strong>일반적인 HTTP 기능:</strong></p>
<ul>
<li><p>정적 콘텐츠</p></li>
<li><p>기본 문서</p></li>
</ul>
<p><strong>응용 프로그램 개발:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET 확장성</p></li>
<li><p>ISAPI 확장</p></li>
<li><p>ISAPI 필터</p></li>
</ul>
<p><strong>보안이</strong></p>
<ul>
<li><p>Windows 인증</p></li>
<li><p>요청 필터링</p></li>
</ul>
<p><strong>관리 도구:</strong></p>
<ul>
<li><p>IIS 관리 콘솔</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>기본 설치 위치</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization 서버</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reporting service 웹 사이트 이름</p></td>
<td align="left"><p>보고 웹 사이트의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Reporting service 포트 바인딩</p></td>
<td align="left"><p>보고 서비스의 고유 포트 번호입니다. 이 포트는 컴퓨터의 다른 프로세스에서 사용할 수 없습니다.</p></td>
</tr>
</tbody>
</table>



### 보고 데이터베이스 필수 구성 요소 소프트웨어

보고 데이터베이스는 App-v 5.1 Reporting server를 사용 하는 경우에만 필요 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필수 구성 요소 및 필수 설정</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>기본 설치 위치</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization 서버</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우)</p></td>
<td align="left"><p>사용할 형식: <strong> INSTANCENAME</strong></p>
<p>이 형식은 로컬 컴퓨터에 설치 되어 있다고 가정 하 여 결정 됩니다.</p>
<p>SVR\INSTANCE 형식으로 이름을 지정 하면 <strong> </strong> 설치에 실패 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 지정 데이터베이스 이름 (해당 하는 경우)</p></td>
<td align="left"><p>고유한 데이터베이스 이름입니다.</p>
<p>기본값: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>보고 서버 위치</p></td>
<td align="left"><p>보고 서버가 배포 된 컴퓨터 계정입니다.</p>
<p>사용할 형식: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>보고 서버 설치 관리자</p></td>
<td align="left"><p>보고 서버를 설치 하는 데 사용 되는 계정입니다.</p>
<p>사용할 형식: Domain\관리자 loginname</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 서비스 및 Microsoft SQL Server 서비스 에이전트</p></td>
<td align="left"><p>이러한 서비스가 AD DS를 쿼리할 수 있는 액세스 권한이 있는 사용자 계정과 연결 되도록 구성 합니다.</p></td>
</tr>
</tbody>
</table>



## App-v 클라이언트 필수 구성 요소 소프트웨어


App-v 클라이언트에 대해 다음 필수 구성 요소 소프트웨어를 설치 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<p></p></td>
<td align="left"><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## 원격 데스크톱 서비스 클라이언트 필수 구성 요소 소프트웨어


App-v 원격 데스크톱 서비스 클라이언트에 대 한 다음 필수 구성 요소 소프트웨어를 설치 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<p></p></td>
<td align="left"><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Sequencer 필수 구성 요소 소프트웨어


**필수 조건을 설치 하기 전에 알아야 할 사항:**

-   모범 사례: Sequencer를 실행 하는 컴퓨터는 가상 응용 프로그램을 실행 하는 컴퓨터와 하드웨어 및 소프트웨어 구성이 동일 해야 합니다.

-   시퀀싱 프로세스는 리소스를 많이 사용 하므로 시퀀서를 실행 하는 컴퓨터에 메모리가 충분 하 고 빠른 프로세서와 빠른 하드 드라이브가 있는지 확인 합니다. 로컬에 설치 된 응용 프로그램의 시스템 요구 사항은 Sequencer를 초과할 수 없습니다. 자세한 내용은 [앱-V 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (웹 설치 관리자)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<p></p></td>
<td align="left"><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Windows 7에만 적용 됨: KB를 다운로드 하 여 설치 합니다.</p></td>
</tr>
</tbody>
</table>








## 관련 항목


[App-V 5.1 계획](planning-for-app-v-51.md)

[App-V 5.1 지원되는 구성](app-v-51-supported-configurations.md)









