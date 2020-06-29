---
title: App-V 5.0 필수 구성 요소
description: App-V 5.0 필수 구성 요소
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814812"
---
# App-V 5.0 필수 구성 요소

Microsoft App-v (Application Virtualization) 5.0 설정을 시작 하기 전에 제품을 설치 하기 위한 전제 조건을 충족 하는지 확인 해야 합니다. 이 항목에서는 App-v 5.0 기능을 배포 하기 전에 컴퓨팅 환경을 준비 하기 위해 성공적으로 계획 하는 데 도움이 되는 정보를 제공 합니다.

> [!Important]
> **이 문서의 필수 조건은 app-v 5.0에만 적용**됩니다. App-v 5.0 서비스 팩에 적용 되는 추가 전제 조건은 다음 웹 페이지를 참조 하세요.

-   [App-V 5.0 SP1의 새로운 기능](whats-new-in-app-v-50-sp1.md)

-   [App-V 5.0 SP2 정보](about-app-v-50-sp2.md)

-   [App-V 5.0 SP3 필수 구성 요소](app-v-50-sp3-prerequisites.md)

다음 표에는 특정 운영 체제와 관련 된 필수 구성 요소 정보가 나와 있습니다.

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
<td align="left"><p>를 실행 하는 컴퓨터:</p>
<ul>
<li><p>Windows8</p></li>
<li><p>Windows Server 2012</p></li>
</ul></td>
<td align="left"><p>다음 필수 구성 요소가 이미 설치 되어 있습니다.</p>
<ul>
<li><p>Microsoft .NET Framework 4.5 – Microsoft .NET Framework 4가 필요 하지 않습니다.</p></li>
<li><p>Windows PowerShell 3.0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>를 실행 하는 컴퓨터:</p>
<ul>
<li><p>Windows 7</p></li>
<li><p>Windows Server 2008</p></li>
</ul></td>
<td align="left"><p>다음 KB를 다운로드 하 고 싶을 수 있습니다.</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Microsoft 보안 권고: 안전 하지 않은 라이브러리 로드로 인해 원격 코드 실행이 가능 합니다.</a></p>
<p>이를 대체 한 이후 KBs을 확인 하 고 일부 KBs 이전 업데이트를 제거 해야 할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

## 앱 설치 필수 구성 요소-V 5.0

> [!Note]  
> Windows 8을 실행 하는 컴퓨터에 대해 다음 필수 구성 요소가 이미 설치 되어 있습니다.

각 App-v 5.0 기능에는 App-v 5.0 기능을 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다.

### App-v 5.0 클라이언트에 대 한 필수 구성 요소

다음 표에는 App-v 5.0 클라이언트에 대 한 설치 필수 구성 요소가 나와 있습니다.

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
<td align="left"><p><strong>소프트웨어 요구 사항</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<p></p>
<div class="alert">
<strong>참고</strong><br/><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p>
</div>
<div>

</div></li>
<li><p>KB2533623 다운로드 및 설치 <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"></a></p>
<p></p>
<div class="alert">
<strong>중요</strong><br/><p>이전 KB 문서를 다운로드 하 여 설치할 수 있습니다. 그러나 최신 버전으로 대체 했을 수 있습니다.</p>
</div>
<div>

</div></li>
<li><p>클라이언트 설치 관리자 (.exe)는 다음 필수 구성 요소를 설치 해야 하는지 여부를 감지 하 고 그에 따라 적절 하 게 수행 합니다.</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p>
<p>이 필수 구성 요소는 Application Virtualization 5.0 SP2 이상 버전에 핫픽스 패키지 4를 설치한 경우에만 필요 합니다.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Microsoft Visual c + + 2010 재배포 가능 패키지</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### App-v 5.0 원격 데스크톱 서비스 클라이언트에 대 한 필수 조건

> [!Note]  
> Windows Server 2012를 실행 하는 컴퓨터에 대해 다음 필수 구성 요소가 이미 설치 되어 있습니다.

다음 표에는 App-v 5.0 원격 데스크톱 서비스 클라이언트에 대 한 설치 필수 구성 요소가 나와 있습니다.

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
<td align="left"><p><strong>소프트웨어 요구 사항</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET 프레임 워크 4 (전체 패키지)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<p></p>
<div class="alert">
<strong>참고</strong><br/><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p>
</div>
<div>

</div></li>
<li><p>KB2533623 다운로드 및 설치 <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"></a></p>
<p></p>
<div class="alert">
<strong>중요</strong><br/><p>이전 KB 문서를 다운로드 하 여 설치할 수 있습니다. 그러나 최신 버전으로 대체 했을 수 있습니다.</p>
</div>
<div>

</div></li>
<li><p>클라이언트 (.exe) 설치 관리자는 다음 필수 구성 요소를 설치 해야 하는지 여부를 감지 하 고 그에 따라 적절 하 게 수행 합니다.</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p>
<p>이 필수 구성 요소는 Application Virtualization 5.0 SP2 이상 버전에 핫픽스 패키지 4를 설치한 경우에만 필요 합니다.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Microsoft Visual c + + 2010 재배포 가능 패키지</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### 앱-V 5.0 시퀀서에 대 한 필수 조건

> [!Note]
> Windows 8 및 Windows Server 2012를 실행 하는 컴퓨터에 대해 다음 필수 구성 요소가 이미 설치 되어 있습니다.

다음 표에는 App-v 5.0 시퀀서에 대 한 설치 필수 구성 요소가 나와 있습니다. 가능 하다 면 시퀀서를 실행 하는 컴퓨터는 가상 응용 프로그램을 실행 하는 컴퓨터와 하드웨어 및 소프트웨어 구성이 동일 해야 합니다.

> [!Note]  
> 로컬에 설치 된 응용 프로그램의 시스템 요구 사항이 시퀀서의 요구 사항을 초과 하는 경우 해당 응용 프로그램의 요구 사항을 충족 해야 합니다. 또한 시퀀싱 프로세스는 시스템 리소스를 많이 사용 하기 때문에 시퀀서를 실행 하는 컴퓨터에는 메모리가 충분 하 고 빠른 프로세서와 빠른 하드 드라이브가 필요 하다는 것이 좋습니다. 자세한 내용은 [앱-V 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.

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
<td align="left"><p><strong>소프트웨어 요구 사항</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual Studio 2013 용 visual c + + 재배포 가능 패키지</a></p>
<p>이 필수 구성 요소는 Application Virtualization 5.0 SP2 용 핫픽스 패키지 4를 설치한 경우에만 필요 합니다.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<p></p></li>
<li><p>KB2533623 다운로드 및 설치 <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"></a></p>
<p></p></li>
<li><p>Microsoft Windows Server 2008 R2 SP1을 실행 하는 컴퓨터의 경우 KB2533623을 다운로드 하 고 설치 합니다. <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"></a></p>
<p></p>
<div class="alert">
<strong>중요</strong><br/><p>이전 KB 문서 중 하나를 다운로드 하 여 설치할 수 있습니다. 그러나 최신 버전으로 대체 했을 수 있습니다.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### App-v 5.0 서버에 대 한 필수 조건

> [!Note]
> Windows Server 2012를 실행 하는 컴퓨터에 대해 다음 필수 구성 요소가 이미 설치 되어 있습니다.

-   Microsoft .NET Framework 4.5. 이렇게 하면 Microsoft .NET Framework 4 요구 사항이 제거 됩니다.

-   Windows PowerShell 3.0

-   [KB2533623](https://support.microsoft.com/kb/2533623) 다운로드 및 설치 (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > 이전 KB 설치를 다운로드할 수 있습니다. 그러나 최신 버전으로 대체 했을 수 있습니다.

다음 표에는 App-v 5.0 서버에 대 한 설치 필수 구성 요소가 나와 있습니다. 서버 구성 요소를 설치 하는 데 사용 하는 계정에는 설치 하려는 컴퓨터에 대 한 관리자 권한이 있어야 합니다. 이 계정에도 Active Directory 디렉터리 서비스를 쿼리할 수 있는 권한이 있어야 합니다. App-v 5.0 서버를 설치 하 고 구성 하기 전에 각 구성 요소를 호스팅할 포트를 지정 해야 합니다. 또한 들어오는 요청을 지정 된 포트로 허용 하도록 관련 방화벽 규칙도 추가 해야 합니다.

> [!Note]
> 관리 서비스에 대해 WebDAV (웹 분산 작성 및 버전 관리)가 자동으로 해제 됩니다.

모든 구성 요소가 동일한 서버에 배포 되는 독립 실행형 배포 및 분산 배포에 대해 App-v 5.0 서버를 지원 합니다. App-v 5.0 서버를 배포 하는 데 사용 하는 토폴로지에 따라 각 구성 요소에 필요한 데이터가 약간 변경 될 수 있습니다.

> [!Important]
> 앱-V의 이전 버전 또는 구성 요소를 실행 하는 컴퓨터에 App-v 5.0 서버를 설치 하는 것은 지원 되지 않습니다. 또한 서버 Core 또는 도메인 컨트롤러를 실행 하는 컴퓨터에 서버 구성 요소를 설치 하는 방법도 지원 되지 않습니다.

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
<td align="left"><p><strong>관리 서버</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3.0</a></p>
<div class="alert">
<strong>참고</strong><br/><p>PowerShell 3.0를 설치 하려면 다시 시작 해야 합니다.</p>
</div>
<div>

</div></li>
<li><p>IIS 역할을 사용할 수 있는 Windows 웹 서버와 <strong> 일반적인 HTTP 기능 </strong> (정적 콘텐츠 및 기본 문서), <strong> 응용 프로그램 개발 </strong> (ASP.NET, .Net 확장성, Isapi 확장 및 isapi 필터), <strong> 보안 </strong> (Windows 인증, 요청 필터링), <strong> 관리 도구 </strong> (iis 관리 콘솔)가 있습니다.</p></li>
<li><p>KB2533623 다운로드 및 설치 <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"></a></p>
<p></p>
<div class="alert">
<strong>중요</strong><br/><p>이전 KB 설치를 다운로드할 수 있습니다. 그러나 최신 버전으로 대체 했을 수 있습니다.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Microsoft Visual c + + 2010 SP1 재배포 가능 패키지 (x64)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual c + + 2010 SP1 재배포 가능 패키지 (x86)</a></p></li>
<li><p>64 비트 ASP.NET 등록</p></li>
</ul>
<p>App-v 5.0 서버 구성 요소는 종속 되지만, 배포 해야 하는 다양 한 요구 사항 및 설치 옵션이 있습니다. 다음 정보를 사용 하 여 앱-V 5.0 관리 서버를 실행 하도록 환경을 준비 합니다.</p>
<ul>
<li><p>설치 위치-기본적으로이 구성 요소는 <strong> %PROGRAMFILES%\Microsoft Application Virtualization Server에 설치 됩니다 </strong> .</p></li>
<li><p>앱-V 5.0 관리 데이터베이스의 위치-SQL Server 이름, SQL 인스턴스 이름, 데이터베이스 이름.</p></li>
<li><p>App-v 5.0 관리 콘솔에 대 한 액세스 권한-배포 종료 시 관리 콘솔에 대 한 액세스 권한을 부여 해야 하는 사용자 또는 그룹입니다. 배포 후에는 관리 콘솔을 통해 추가 관리자가 추가 될 때까지 이러한 사용자만 관리 콘솔에 액세스할 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>보안 그룹 및 단일 사용자는 지원 되지 않습니다. AD DS 그룹을 지정 해야 합니다.</p>
</div>
<div>

</div></li>
<li><p>App-v 5.0 관리 서비스 웹사이트 이름-웹 사이트의 이름을 지정 하거나 기본 이름을 사용 합니다.</p></li>
<li><p>App-v 5.0 관리 서비스 포트 바인딩-이는 컴퓨터의 다른 웹 사이트에서 사용 하지 않는 고유한 포트 번호 여야 합니다.</p></li>
<li><p>Microsoft Silverlight에 대 한 지원 – 관리 콘솔을 사용 하려면 먼저 Microsoft Silverlight를 설치 해야 합니다. 이는 배포에 필요 하지 않지만, 서버는 Microsoft Silverlight를 지원할 수 있어야 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>관리 데이터베이스</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>참고</strong><br/><p>데이터베이스는 App-v 5.0 관리 서버를 사용 하는 경우에만 필요 합니다.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual c + + 2010 SP1 재배포 가능 패키지 (x86)</a></p></li>
</ul>
<p>App-v 5.0 서버 구성 요소는 종속 되지만, 배포 해야 하는 다양 한 요구 사항 및 설치 옵션이 있습니다. 다음 정보를 사용 하 여 앱-V 5.0 관리 데이터베이스를 실행 하는 환경을 준비 합니다.</p>
<ul>
<li><p>설치 위치-기본적으로이 구성 요소는 <strong> %PROGRAMFILES%\Microsoft Application Virtualization 서버에 설치 됩니다 </strong> .</p></li>
<li><p>사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우) – <strong> </strong> 설치 시 로컬 컴퓨터에 있다고 가정 하므로 형식이 INSTANCENAME 이어야 합니다. 다음 형식의 이름을 지정 하면 <strong> SVR\INSTANCE </strong> 가 실패 합니다.</p></li>
<li><p>사용자 지정 앱-V 5.0 데이터베이스 이름 (해당 하는 경우)-고유한 데이터베이스 이름을 지정 해야 합니다. 관리 데이터베이스의 기본 값은 AppVManagement입니다 <strong> </strong> .</p></li>
<li><p>App-v 5.0 관리 서버 위치 – 관리 서버가 배포 되는 컴퓨터 계정을 지정 합니다. 다음 형식으로 Domain\machineaccount에서 지정 해야 합니다 <strong> </strong> .</p></li>
<li><p>App-v 5.0 관리 서버 설치 관리자-app-v 5.0 관리 서버를 설치 하는 데 사용 되는 계정을 지정 합니다. Domain\관리자 loginname 형식을 사용 해야 합니다 <strong> </strong> .</p></li>
<li><p>Microsoft SQL Server 서비스 에이전트-Microsoft SQL Server 에이전트 서비스가 자동으로 다시 시작 되도록 App-v 5.0 관리 데이터베이스를 실행 하는 컴퓨터를 구성 합니다. 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> SQL Server 에이전트에서 서비스를 자동으로 다시 시작 하도록 구성을 참조 하세요.</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>보고 서버</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual c + + 2010 SP1 재배포 가능 패키지 (x86)</a></p></li>
<li><div class="alert">
<strong>참고</strong><br/><p>보고 서버로 원치 않거나 악의적인 데이터를 보내는 위험을 줄이려면 회사 보안 정책에 따라 보고 웹 서비스에 대 한 액세스를 제한 해야 합니다.</p>
</div>
<div>

</div>
<p>Windows Web Server에는 <strong> 일반적인 HTTP 기능 </strong> (정적 콘텐츠 및 기본 문서), <strong> 응용 프로그램 개발 </strong> (ASP.NET, .Net 확장성, Isapi 확장 및 isapi 필터), <strong> 보안 </strong> (windows 인증, 요청 필터링), <strong> 보안 </strong> (Windows 인증, 요청 필터링), <strong> 관리 도구 </strong> (iis 관리 콘솔) 등의 기능이 포함 되어 있습니다.</p></li>
<li><p>64 비트 ASP.NET 등록</p></li>
<li><p>설치 위치-기본적으로이 구성 요소는 <strong> %PROGRAMFILES%\Microsoft Application Virtualization 서버에 설치 됩니다 </strong> .</p></li>
<li><p>App-v 5.0 reporting service 웹 사이트 이름-웹 사이트의 이름이 나 사용할 기본 이름을 지정 합니다.</p></li>
<li><p>App-v 5.0 reporting service 포트 바인딩-이는 컴퓨터에서 실행 되는 다른 웹 사이트에서 이미 사용 하 고 있지 않은 고유한 포트 번호 여야 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>보고 데이터베이스</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>참고</strong><br/><p>데이터베이스는 App-v 5.0 reporting server를 사용 하는 경우에만 필요 합니다.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual c + + 2010 SP1 재배포 가능 패키지 (x86)</a></p></li>
</ul>
<p>App-v 5.0 서버 구성 요소는 종속 되지만, 배포 해야 하는 다양 한 요구 사항 및 설치 옵션이 있습니다. 다음 정보를 사용 하 여 앱이 App-v 5.0 보고 데이터베이스를 실행할 수 있도록 준비 합니다.</p>
<ul>
<li><p>설치 위치-기본적으로이 구성 요소는 <strong> %PROGRAMFILES%\Microsoft Application Virtualization 서버에 설치 됩니다 </strong> .</p></li>
<li><p>사용자 지정 SQL Server 인스턴스 이름 (해당 하는 경우) – <strong> </strong> 설치 시 로컬 컴퓨터에 있다고 가정 하므로 형식이 INSTANCENAME 이어야 합니다. 다음 형식의 이름을 지정 하면 <strong> SVR\INSTANCE </strong> 가 실패 합니다.</p></li>
<li><p>사용자 지정 앱-V 5.0 데이터베이스 이름 (해당 하는 경우)-고유한 데이터베이스 이름을 지정 해야 합니다. 보고 데이터베이스의 기본 값은 AppVReporting입니다 <strong> </strong> .</p></li>
<li><p>App-v 5.0 보고 서버 위치 – 보고 서버가 배포 된 컴퓨터 계정을 지정 합니다. 다음 형식으로 Domain\machineaccount에서 지정 해야 합니다 <strong> </strong> .</p></li>
<li><p>App-v 5.0 보고 서버 설치 관리자-App-v 5.0 reporting server를 설치 하는 데 사용 될 계정을 지정 합니다. Domain\관리자 loginname 형식을 사용 해야 합니다 <strong> </strong> .</p></li>
<li><p>Microsoft SQL Server 서비스 및 Microsoft SQL Server 에이전트 서비스 – 이러한 서비스는 AD 쿼리 액세스 권한이 있는 사용자 계정과 연결 되어 있어야 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>게시 서버</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (전체 패키지)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual c + + 2010 SP1 재배포 가능 패키지 (x86)</a></p></li>
<li><p>Windows Web Server에는 <strong> 일반적인 HTTP 기능 </strong> (정적 콘텐츠 및 기본 문서), <strong> 응용 프로그램 개발 </strong> (ASP.NET, .Net 확장성, Isapi 확장 및 isapi 필터), <strong> 보안 </strong> (windows 인증, 요청 필터링), <strong> 보안 </strong> (Windows 인증, 요청 필터링), <strong> 관리 도구 </strong> (iis 관리 콘솔) 등의 기능이 포함 되어 있습니다.</p></li>
<li><p>64 비트 ASP.NET 등록</p></li>
</ul>
<p>App-v 5.0 서버 구성 요소는 종속 되지만, 배포 해야 하는 다양 한 요구 사항 및 설치 옵션이 있습니다. 다음 정보를 사용 하 여 앱-V 5.0 게시 서버를 실행 하도록 환경을 준비 합니다.</p>
<ul>
<li><p>설치 위치-기본적으로이 구성 요소는 <strong> %PROGRAMFILES%\Microsoft Application Virtualization 서버에 설치 됩니다 </strong> .</p></li>
<li><p>App-v 5.0 관리 서비스 URL-app-v 5.0 관리 서비스의 URL을 지정 합니다. 게시 서버가 통신 하는 포트는 다음과 같은 형식을 사용 하 여 지정 해야 합니다 <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> http://localhost:12345 </a></strong> .</p></li>
<li><p>App-v 5.0 publishing 서비스 웹사이트 이름 – 웹 사이트의 이름이 나 사용할 기본 이름을 지정 합니다.</p></li>
<li><p>App-v 5.0 게시 서비스 포트 바인딩-이는 컴퓨터에서 실행 되는 다른 웹 사이트에서 이미 사용 하지 않는 고유한 포트 번호 여야 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## 관련 항목

[App-V 배포 계획](planning-to-deploy-app-v.md)

[App-V 5.0 지원되는 구성](app-v-50-supported-configurations.md)
