---
title: App-V Server 게시 메타데이터 보기
description: App-V Server 게시 메타데이터 보기
author: dansimp
ms.assetid: 048dd42a-24d4-4cc4-81f6-7a919aadd9b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 304aa656de98a0c9d59f0a6166811ead911033ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813265"
---
# App-V Server 게시 메타데이터 보기


게시 관련 문제를 해결 하는 데 도움이 될 수 있는 게시 메타 데이터를 보려면이 절차를 사용 합니다. 이 절차를 사용 하려면 App-v 관리 서버를 사용 해야 합니다.

이 문서에는 다음 정보가 포함 되어 있습니다.

-   [게시 메타 데이터 보기에 대 한 app-v 5.0 SP3 요구 사항](#bkmk-50sp3-reqs-pub-meta)

-   [게시 메타 데이터를 보는 데 사용할 구문](#bkmk-syntax-view-pub-meta)

-   [클라이언트 운영 체제 및 버전에 대 한 쿼리 값](#bkmk-values-query-pub-meta)

-   [게시 메타 데이터의 정의](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-50sp3-reqs-pub-meta"></a>게시 메타 데이터 보기에 대 한 app-v 5.0 SP3 요구 사항


App-v 5.0 SP3에서는 메타 데이터에 대해 App-v 게시 서버를 쿼리할 때 주소에 다음 값을 제공 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">값</th>
<th align="left">추가적인 세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p><strong>쿼리에서 clientversion 매개 변수를 생략 하면 </strong> 메타 데이터가 새 APP-V 5.0 SP3 기능을 제외 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ClientOS</strong></p></td>
<td align="left"><p>패키지를 시퀀싱 할 때 특정 클라이언트 운영 체제를 선택 하는 경우에만이 값을 제공 해야 합니다. 기본값 (모든 운영 체제)을 선택 하는 경우 쿼리에이 값을 지정 하지 마세요.</p>
<p><strong>쿼리에서 clientos 매개 변수를 생략 하면 </strong> 모든 운영 체제를 지원 하도록 시퀀싱 된 패키지만 메타 데이터에 표시 됩니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>게시 메타 데이터를 보기 위한 쿼리 구문


다음 표에서는 구문 및 쿼리 예제를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">앱 버전-V</th>
<th align="left">쿼리 구문</th>
<th align="left">매개 변수 설명</th>
<th align="left">예</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 5.0 SP3</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;PubServer&gt;</p></td>
<td align="left"><p>App-v 게시 서버의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;게시 포트 #&gt;</p></td>
<td align="left"><p>게시 서버를 구성할 때 정의한 App-v 게시 서버 포트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClientVersion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>App-V 클라이언트의 버전입니다. 사용할 올바른 값에 대해서는 다음 표를 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ClientOS = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>App-v 클라이언트를 실행 하는 컴퓨터의 운영 체제입니다. 사용할 올바른 값에 대해서는 다음 표를 참조 하세요.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>App-v 클라이언트에서 게시 서버의 이름과 포트 번호 (http:// &lt; pubserver &gt; : &lt; Publishing 포트 #)를 가져오려면 &gt; <strong> AppvPublishingServer PowerShell cmdlet의 URL 구성을 참조 하세요 </strong> .</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>예제:</p>
<ul>
<li><p>"Pubsvr01" 이라는 Windows Server 2012 R2는 게시 서비스를 호스팅합니다.</p></li>
<li><p>Windows 클라이언트는 Windows 8.1 64 비트입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 5.0-app-v 5.0 SP2를 통해</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>참고</strong><br/><p><strong>ClientVersion </strong> 및 <strong> clientversion </strong> 는 app-v 5.0 SP3 에서만 지원 됩니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>앱-V 5.0 SP3에 대 한 정보를 참조 하세요.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>이 예제에서 "pubsvr01" 라는 Windows Server 2012 R2는 관리 및 게시 서비스를 호스팅합니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>클라이언트 운영 체제 및 버전에 대 한 쿼리 값


게시 메타 데이터 쿼리에서 사용 중인 클라이언트 운영 체제 및 버전에 해당 하는 문자열 값을 입력 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">아키텍처</th>
<th align="left">작동 문자열 문자열 값</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>WindowsClient_6 2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>WindowsClient_6 2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>WindowsClient_6 2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>WindowsClient_6 2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>WindowsServer_6 2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>WindowsServer_6 2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>WindowsServer_6 2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>WindowsServer_6 2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>WindowsClient_6 1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>WindowsClient_6 1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>WindowsServer_6 1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>WindowsServer_6 1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>게시 메타 데이터의 정의


패키지가 App-v 클라이언트를 실행 하는 컴퓨터에 게시 되 면 게시 되는 패키지 및 연결 그룹을 나타내는 메타 데이터가 해당 컴퓨터로 전송 됩니다. App-v 클라이언트는 다음에 대 한 두 개의 개별 요청을 만듭니다.

-   클라이언트 컴퓨터에 부여 되는 패키지 및 연결 그룹

-   현재 사용자에 게 부여 되는 패키지 및 연결 그룹

게시 서버는 관리 서버와 통신 하 여 요청자에 게 사용할 수 있는 패키지 및 연결 그룹을 결정 합니다. 메타 데이터를 생성 하려면 게시 서버를 관리 서버에 등록 해야 합니다.

특정 사용자 또는 컴퓨터의 컨텍스트에 있는 쿼리를 사용 하 여 인터넷 브라우저의 각 요청에 대 한 메타 데이터를 볼 수 있습니다.






## 관련 항목


[App-V 5.0에 대한 기술 참조](technical-reference-for-app-v-50.md)









