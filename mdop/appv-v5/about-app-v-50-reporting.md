---
title: App-V 5.0 보고 정보
description: App-V 5.0 보고 정보
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815023"
---
# App-V 5.0 보고 정보


Microsoft App-v (Application Virtualization) 5.0에는 App-v 5.0 클라이언트를 실행 하는 컴퓨터와 가상 응용 프로그램 패키지 사용에 대 한 정보를 수집 하는 데 도움이 되는 기본 제공 보고 기능이 포함 되어 있습니다. 이 정보를 사용 하 여 중앙 집중화 된 데이터베이스에서 보고서를 생성할 수 있습니다.

## <a href="" id="---------app-v-5-0-reporting-overview"></a> 앱-V 5.0 보고 개요


다음 목록에는 App-v 5.0에서 보고에 대 한 종단 간 상위 수준 워크플로가 표시 됩니다.

1.  Microsoft App-v (Application Virtualization) 5.0 보고 서버에는 다음과 같은 전제 조건이 있습니다.

    -   IIS (인터넷 정보 서비스) 웹 서버 역할

    -   Windows 인증 역할 ( **IIS/보안**)

    -   Sql Server가 SSRS (SQL Server Reporting Services)로 설치 및 실행 되는 경우

    SQL Server Reporting Services가 실행 중인지 확인 하려면 `http://localhost/Reports` 웹 브라우저에서 app-v 5.0 Reporting을 호스팅할 서버의 관리자로 표시 합니다. SQL Server Reporting Services 홈 페이지가 표시 됩니다.

2.  App-v 5.0 reporting server 및 연결 된 데이터베이스를 설치 합니다. 보고 서버를 설치 하는 방법에 대 한 자세한 내용은 [독립 실행형 컴퓨터에 보고 서버를 설치 하 고 데이터베이스에 연결 하는 방법을](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)참조 하세요. App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 보고 서버로 데이터를 보내야 하는 시간을 구성 합니다.

3.  구성 관리자와 같은 전자 소프트웨어 배포 시스템을 사용 하 여 보고서를 보려면 SQL Server Reporting Service에서 보고서를 정의 하면 됩니다. 의 다운로드 센터에서 미리 정의 된 appvshort 보고서를 다운로드 <https://go.microsoft.com/fwlink/?LinkId=397255> 합니다.

    **참고**  앱-V 5.0와 함께 구성 관리자 통합을 사용 하는 경우 대부분의 보고서가 App-v 5.0이 아닌 구성 관리자에서 생성 됩니다.

     

4.  관리자로 사용 하 여 App-v 5.0 PowerShell 모듈을 가져온 후 `Import-Module AppvClient` app-v 5.0 클라이언트를 사용 하도록 설정 합니다. 이 샘플 PowerShell cmdlet은 App-v 5.0 보고 기능을 사용 하도록 설정 합니다.

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    앱-V 5.0 보고서 데이터를 즉시 보내려면 `Send-AppvClientReport` app-v 5.0 클라이언트에서 실행 합니다.

    보고 사용으로 App-v 5.0 클라이언트를 설치 하는 방법에 대 한 자세한 내용은 [클라이언트 구성 설정 정보](about-client-configuration-settings.md)를 참조 하세요. Windows PowerShell에서 App-v 5.0 Reporting을 관리 하려면 [PowerShell을 사용 하 여 app-v 5.0 클라이언트에서 보고 기능을 사용 하도록 설정 하는 방법을](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)참조 하세요.

5.  보고 서버는 App-v 5.0 클라이언트에서 데이터를 받은 후 보고 데이터베이스로 데이터를 보냅니다. 데이터베이스에서 클라이언트 데이터를 받아서 처리 하는 경우 응답은 성공적으로 보고 서버로 보내지며 App-v 5.0 클라이언트에 게 알림이 전송 됩니다.

6.  App-v 5.0 클라이언트는 성공 알림을 받을 때 공간을 절약 하기 위해 데이터 캐시를 비웁니다.

    **참고**  기본적으로 서버가 데이터 수신을 확인 한 후 캐시가 지워집니다. 데이터 캐시를 저장 하도록 클라이언트를 수동으로 구성할 수 있습니다.

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> 앱-V 5.0 보고 서버 자주 묻는 질문

다음 표에서는 App-v 5.0 reporting에 대 한 일반적인 질문에 대 한 대답을 보여 줍니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">질문</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>보고서 정보를 보고 데이터베이스로 보내는 빈도는 어떻게 되나요?</p></td>
<td align="left"><p>빈도는 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 보고 작업을 구성 하는 방법에 따라 달라 집니다. 보고 데이터를 보낼 빈도/간격을 구성 해야 합니다. App-v 5.0 보고 기능은 기본적으로 사용 하도록 설정 되어 있지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>보고 서버 데이터베이스에 저장 되는 정보는 무엇 인가요?</p></td>
<td align="left"><p>다음 목록에는 보고 데이터베이스에 저장 되어 있는 항목이 표시 됩니다.</p>
<ul>
<li><p>App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 실행 되는 운영 체제: 호스트 이름, 버전, 서비스 팩, 형식-클라이언트/서버, 프로세서 아키텍처.</p></li>
<li><p>앱-V 5.0 클라이언트 정보: 버전.</p></li>
<li><p>게시 된 패키지 목록: GUID, 버전 GUID, name.</p></li>
<li><p>응용 프로그램 사용 정보: 이름, 버전, 스트리밍 서버, 사용자 (domain\alias), 패키지 버전 GUID, 시작 상태 및 시간, 종료 시간.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>보고 서버로 보내는 정보의 평균 량은 얼마 입니까?</p></td>
<td align="left"><p>그것은 사정 나름이에요. 다음 목록에는 보고 서버로 전송 되는 세 가지 데이터 집합이 표시 됩니다.</p>
<ol>
<li><p>운영 체제, 앱-V 5.0 클라이언트 정보. ~ 150 바이트,이 데이터를 보낼 때마다</p></li>
<li><p>게시 된 패키지 목록. 30 개 패키지의 경우 ~ 7kb 이는 패키지 목록이 게시 새로 고침으로 업데이트 된 경우에만 전송 되며,이는 자주 수행 되지 않습니다. 변경 내용이 없는 경우에는이 정보가 전송 되지 않습니다.</p></li>
<li><p>가상 응용 프로그램 사용 정보 – 이벤트 당 0.25 KB 정보 정보를 보내기 전에 두 경우를 모두 열고 닫는 경우 하나의 이벤트로 계산 됩니다. 예약 된 작업을 사용 하 여 보내는 경우 마지막 업로드에 성공한 데이터만 서버로 전송 됩니다. PowerShell cmdlet을 통해 수동으로 전송 하는 경우 다음에 데이터를 다시 보내야 하는지 여부를 제어 하는 선택적 인수 (인수는 DeleteOnSuccess)가 있습니다 <strong> </strong> .</p>
<p></p>
<p>예를 들어 20 개의 응용 프로그램을 열고, 그리고 보고 정보를 매일 전송 하도록 예약 하는 경우 일반적인 일일 트래픽은 약 0.15 KB + 20 x 0.25 KB 또는 약 5KB/사용자에 해당 됩니다.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>보고를 예약할 수 있나요?</p></td>
<td align="left"><p>예. PowerShell Cmdlet (AppvClientReport)을 사용 하 여 보고를 수동으로 보내는 <strong> </strong> 것 외에도 자동으로 수행 되도록 작업을 예약할 수 있습니다. 다음과 같은 두 가지 방법으로 보고를 예약할 수 있습니다.</p>
<ol>
<li><p>PowerShell cmdlet을 사용 하 여 <strong> AppvClientConfiguration를 설정 </strong> 합니다. 예:</p>
<p>Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</a></p>
<p></p>
<p>클라이언트 구성 설정에 대 한 전체 목록은 <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> 클라이언트 구성 설정 정보를 참조 </a> 하 고 <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay, </strong> ReportingInterval <strong> </strong> 항목을 확인 하세요.</p>
<p></p></li>
<li><p>그룹 정책을 사용 합니다. 도메인 컨트롤러를 사용 하 여 배포 하는 경우에는 이전에 나열 된 설정과 동일 하 게 설정 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>PowerShell을 사용 하 여 구성 된 로컬 설정이 그룹 정책 설정 보다 우선 합니다.</p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> 앱-V 5.0 클라이언트 보고


App-v 5.0 보고 기능을 사용 하려면 App-v 5.0 클라이언트를 설치 하 고 구성 해야 합니다. 클라이언트가 설치 되 면 **AppVClientConfiguration** PowerShell Cmdlet 또는 **ADMX 서식 파일** 을 사용 하 여 보고를 구성 합니다. 보고 기능 cmdlet은 다음 링크를 사용 하 여 사용할 수 있으며, **보고**로 앞에 있습니다. 클라이언트 구성 설정에 대 한 전체 목록은 [클라이언트 구성 설정 정보](about-client-configuration-settings.md)를 참조 하세요. 다음 섹션에서는 PowerShell을 사용 하 여 App-v 5.0 클라이언트 보고 구성에 대 한 예제를 제공 합니다.

### PowerShell을 사용 하 여 App-v 클라이언트 보고 구성

다음 예제에서는 PowerShell 매개 변수를 통해 App-v 5.0 클라이언트의 보고 기능을 구성 하는 방법을 보여 줍니다.

**참고**  
앱-V 5.0 ADMX 템플릿에서 그룹 정책 설정을 사용 하 여 다음 구성 작업을 구성할 수도 있습니다. ADMX 서식 파일을 사용 하는 방법에 대 한 자세한 내용은 [Admx 서식 파일 및 그룹 정책을 사용 하 여 app-v 5.0 클라이언트 구성을 수정 하는 방법을](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)참조 하세요.
 


**보고 기능을 사용 하도록 설정 하 고 app-v 5.0 클라이언트를 실행 하는 컴퓨터에서 데이터 수집을 시작**하려면 다음을 수행 합니다.

`Set-AppVClientConfiguration –ReportingEnabled 1`

**특정 보고 서버에 데이터를 자동으로 보내도록 클라이언트를 구성 하려면 다음을 수행 합니다**.

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

이 예제에서는 보고 데이터를 보고 서버 URL로 자동으로 보내도록 클라이언트를 구성 합니다 <strong> http://MyReportingServer:MyPort/ </strong> . 또한 보고 데이터는 세션에 대해 생성 되는 임의 지연에 따라 매일 8:00와 8:30 PM 사이에 전송 됩니다.

**클라이언트에서 데이터 캐시 크기를 제한 하려면 다음을**수행 합니다.

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

App-v 5.0 클라이언트를 실행 하는 컴퓨터의 보고 캐시 최대 크기를 100 MB로 구성 합니다. 서버로 데이터를 전송 하기 전에 캐시 제한에 도달 하면 필요한 경우 로그가 롤업되 고 데이터가 덮어쓰여집니다.

**클라이언트와 서버 간에 네트워크를 통해 전송 되는 데이터 블록 크기를 구성 하려면 다음을 수행 합니다**.

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

클라이언트가 10240 MB로 보내는 최대 데이터 블록 수를 지정 합니다.

### 수집 된 데이터 형식

다음 표에는 App-v 5.0 보고를 사용 하 여 수집할 수 있는 정보의 유형이 표시 됩니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">클라이언트 정보</th>
<th align="left">패키지 정보</th>
<th align="left">응용 프로그램 사용</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>호스트 이름</p></td>
<td align="left"><p>패키지 이름</p></td>
<td align="left"><p>시작 및 종료 시간</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 5.0 클라이언트 버전</p></td>
<td align="left"><p>패키지 버전</p></td>
<td align="left"><p>실행 상태</p></td>
</tr>
<tr class="odd">
<td align="left"><p>프로세서 아키텍처</p></td>
<td align="left"><p>패키지 원본</p></td>
<td align="left"><p>종료 상태</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제 버전</p></td>
<td align="left"><p>캐시 된 백분율</p></td>
<td align="left"><p>응용 프로그램 이름</p></td>
</tr>
<tr class="odd">
<td align="left"><p>서비스 팩 수준</p></td>
<td align="left"><p></p></td>
<td align="left"><p>응용 프로그램 버전</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제 종류</p></td>
<td align="left"><p></p></td>
<td align="left"><p>사용자 이름</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>연결 그룹</p></td>
</tr>
</tbody>
</table>
 


클라이언트는이 데이터를 수집 하 여 **.xml** 형식으로 저장 합니다. 데이터 캐시는 기본적으로 숨겨지며, XML 파일을 열기 위한 관리자 권한이 필요 합니다.

### 서버로 데이터 보내기

앱-V 5.0 클라이언트를 실행 하는 컴퓨터를 구성 하 여 지정 된 보고 서버로 데이터를 자동으로 보낼 수 있습니다. 서버를 지정 하려면 **Set-AppvClientConfiguration** cmdlet을 다음 설정으로 사용 합니다.

-   ReportingEnabled

-   ReportingServerURL

-   ReportingStartTime

-   ReportingInterval

-   ReportingRandomDelay

이전 설정을 구성한 후에는 예약 된 작업을 만들어야 합니다. 예약 된 작업은 **ReportingServerURL** 설정으로 지정 된 서버에 연결 하 고 전송을 시작 합니다. 예약 된 시간 밖으로 데이터를 수동으로 보내려면 다음 PowerShell cmdlet을 사용 합니다.

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

보고 서버를 이전에 구성한 경우 **– URL** 매개 변수를 생략할 수 있습니다. 또는 데이터를 대체 위치로 보내야 하는 경우 다른 URL을 지정 하 여이 데이터 컬렉션에 대해 구성 된 **ReportingServerURL** 를 재정의 합니다.

**-DeleteOnSuccess** 매개 변수는 전송이 성공적으로 수행 되는 경우 데이터 캐시가 지워지는 것을 나타냅니다. 이를 지정 하지 않으면 캐시가 지워지지 않습니다.

### 수동 데이터 수집

**AppVClientReport** cmdlet을 사용 하 여 데이터를 수동으로 수집할 수도 있습니다. 이 솔루션은 기존 보고 서버와 함께 유용 하거나 사용 하지 않을 수 있습니다. 다음 목록에는 보고 서버와 함께 데이터를 수집 하거나 포함 하지 않은 상태에 대 한 정보가 표시 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">보고 서버 사용</th>
<th align="left">보고 서버 없이</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>기존 App-v 5.0 reporting Server가 있는 경우 사용자 지정 된 예약 작업 또는 스크립트를 만듭니다. 클라이언트가 원하는 빈도를 사용 하 여 데이터를 지정 된 위치로 보내도록 지정 합니다.</p></td>
<td align="left"><p>기존 App-v 5.0 reporting Server가 없는 경우 <strong> – URL </strong> 매개 변수를 사용 하 여 데이터를 지정 된 공유에 보냅니다. 예:</p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p>앞의 예제에서는 <strong> &lt; &gt; <strong> -URL 매개 변수를 통해 표시 되는 \MyShare\MyData/strong 위치에 보고 데이터를 보냅니다 </strong> . 데이터를 보낸 후에는 캐시가 지워집니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>보고 서버 이외의 위치를 지정 하면 데이터는 <strong> 추가 처리 없이 .xml 형식을 사용 하 여 전송 됩니다 </strong> .</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### 보고서 만들기

앱-V 5.0를 사용 하 여 보고서 정보를 검색 하 고 보고서를 만들려면 다음 방법 중 하나를 사용 해야 합니다.

-   Microsoft sql server **Reporting services (SSRS)** 를 제공 합니다. App-v 5.0 reporting server를 설치할 때 SSRS가 설치 되지 않습니다. 연결 된 보고서를 생성 하려면 별도로 배포 해야 합니다.

    [MICROSOFT SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596)를 사용 하는 방법에 대 한 자세한 내용은 다음 링크를 사용 하세요.

-   **스크립팅** -app-v 5.0 보고 데이터베이스에 대해 직접 스크립팅 하 여 보고서를 생성할 수 있습니다. 예:

    **저장 프로시저:**

    **Spprocessclientreport** 는 자정 또는 12:00 오전에 실행 되도록 예약 되어 있습니다.

    Microsoft SQL Server 예약 된 저장 프로시저를 실행 하려면 Microsoft SQL Server 에이전트를 실행 중 이어야 합니다. Microsoft SQL Server 에이전트가 **자동**시작으로 설정 되어 있는지 확인 해야 합니다. 자세한 내용은 [Sql Server 에이전트 자동 시작 (Sql Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045)을 참조 하세요.

    또한 App-v 5.0 데이터베이스 스크립트를 사용 하 여 저장 프로시저를 만들 수 있습니다.

또한 보고 서버 웹 서비스의 **최대 동시 연결이** 가용성에 영향을 주지 않고 관리할 수 있는 값으로 설정 되어 있는지도 확인 해야 합니다. **보고 웹 서비스** 의 권장 되는 **최대 동시 연결** 수는 **1만**입니다.






## 관련 항목


[App-V 5.0 Server 배포](deploying-the-app-v-50-server.md)

[독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





