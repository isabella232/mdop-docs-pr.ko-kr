---
title: MBAM 2.5 지원되는 구성
description: MBAM 2.5 지원되는 구성
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823893"
---
# MBAM 2.5 지원되는 구성


독립 실행형 토폴로지 또는 MBAM을 System Center Configuration Manager와 통합 하는 Configuration Manager 통합 토폴로지에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 실행할 수 있습니다. 프로덕션 환경의 토폴로지에 권장 되는 구성을 사용 하는 경우 MBAM은 최대 50만 MBAM 클라이언트를 지원 합니다. 각 토폴로지에 대해 각 서버에 구성 되는 권장 아키텍처 및 기능에 대 한 자세한 내용은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)를 참조 하세요.

Configuration Manager 통합 토폴로지와 관련 된 추가 구성에 대 한 자세한 내용은 [MBAM이 지 원하는 구성 관리자 버전](#bkmk-cm-ramreqs)을 참조 하세요.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



## MBAM 지원 언어


다음 표에는 MBAM 클라이언트에 대해 지원 되는 언어 (셀프 서비스 포털 포함) 및 MBAM 2.5 및 MBAM 2.5 SP1의 MBAM 서버가 나와 있습니다.

**MBAM 2.5 SP1의 지원 되는 언어:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">클라이언트 언어</th>
<th align="left">서버 언어</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>체코어 (체코 공화국) cs-CZ</p>
<p>덴마크어 (덴마크) da-진한</p>
<p>네덜란드어 (네덜란드) nl-NL</p>
<p>영어 (미국) en-us-US</p>
<p>핀란드어 (핀란드) fi</p>
<p>프랑스어 (프랑스) fr-fr</p>
<p>독일어 (독일) DE-DE</p>
<p>그리스어 (그리스) el-GR</p>
<p>헝가리어 (헝가리) hu-hu&platform-HU-HU&PLATFORM</p>
<p>이탈리아어 (이탈리아) it</p>
<p>일본어 (일본) ja-jp</p>
<p>한국어 (대한민국) ko-kr-KR</p>
<p>노르웨이어, 복말 (노르웨이) nb-아니요</p>
<p>폴란드어 (폴란드) pl-PL</p>
<p>포르투갈어 (브라질) pt-BR</p>
<p>포르투갈어 (포르투갈) pt-PT</p>
<p>러시아어 (러시아)의 기능</p>
<p>슬로바키아어 (슬로바키아) a/.</p>
<p>스페인어 (스페인) es</p>
<p>스웨덴 (스웨덴) sv-SE</p>
<p>터키어 (터키) tr-TR</p>
<p>슬로베니아어 (슬로베니아) sl-SI</p>
<p>중국어 간체 (중국) zh-cn-CN</p>
<p>중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</p></td>
<td align="left"><ul>
<li><p>영어 (미국) en-us-US</p></li>
<li><p>프랑스어 (프랑스) fr-fr</p></li>
<li><p>독일어 (독일) DE-DE</p></li>
<li><p>이탈리아어 (이탈리아) it</p></li>
<li><p>일본어 (일본) ja-jp</p></li>
<li><p>한국어 (대한민국) ko-kr-KR</p></li>
<li><p>포르투갈어 (브라질) pt-BR</p></li>
<li><p>러시아어 (러시아)의 기능</p></li>
<li><p>스페인어 (스페인) es</p></li>
<li><p>중국어 간체 (중국) zh-cn-CN</p></li>
<li><p>중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</p></li>
</ul></td>
</tr>
</tbody>
</table>



**MBAM 2.5에서 지원 되는 언어:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">클라이언트 언어</th>
<th align="left">서버 언어</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>영어 (미국) en-us-US</p></li>
<li><p>프랑스어 (프랑스) fr-fr</p></li>
<li><p>독일어 (독일) DE-DE</p></li>
<li><p>이탈리아어 (이탈리아) it</p></li>
<li><p>일본어 (일본) ja-jp</p></li>
<li><p>한국어 (대한민국) ko-kr-KR</p></li>
<li><p>포르투갈어 (브라질) pt-BR</p></li>
<li><p>러시아어 (러시아)의 기능</p></li>
<li><p>스페인어 (스페인) es</p></li>
<li><p>중국어 간체 (중국) zh-cn-CN</p></li>
<li><p>중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</p></li>
</ul></td>
<td align="left"><ul>
<li><p>영어 (미국) en-us-US</p></li>
<li><p>프랑스어 (프랑스) fr-fr</p></li>
<li><p>독일어 (독일) DE-DE</p></li>
<li><p>이탈리아어 (이탈리아) it</p></li>
<li><p>일본어 (일본) ja-jp</p></li>
<li><p>한국어 (대한민국) ko-kr-KR</p></li>
<li><p>포르투갈어 (브라질) pt-BR</p></li>
<li><p>러시아어 (러시아)의 기능</p></li>
<li><p>스페인어 (스페인) es</p></li>
<li><p>중국어 간체 (중국) zh-cn-CN</p></li>
<li><p>중국어 번체 (대만) zh-cn-hy 얕은 샘물 a</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> MBAM 서버 시스템 요구 사항


### MBAM 서버 운영 체제 요구 사항

동일한 시스템의 운영 체제에서 MBAM 클라이언트와 MBAM 서버를 실행 하는 것이 좋습니다. 예를 들어 windows 10이 포함 되어 있는 windows Server 2016, windows 8.1 windows Server 2012 R2 등

다음 표에는 MBAM 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



엔터프라이즈 도메인은 적어도 하나 이상의 Windows Server 2008 (이상) 도메인 컨트롤러를 포함 해야 합니다.

### <a href="" id="bkmk-stand-alone-ramreqs"></a>MBAM 서버 프로세서, RAM, 디스크 공간 요구 사항-독립 실행형 토폴로지

이러한 요구 사항은 MBAM 독립 실행형 토폴로지에 대 한 것입니다. Configuration Manager 통합 토폴로지의 요구 사항에 대해서는 [Mbam 서버 프로세서, RAM 및 디스크 공간 요구 사항-구성 관리자 통합 토폴로지](#bkmk-cm-ramreqs)를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">하드웨어 항목</th>
<th align="left">최소 요구 사항</th>
<th align="left">권장 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>처리자</p></td>
<td align="left"><p>2.33 GHz</p></td>
<td align="left"><p>2.33 GHz 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8gb</p></td>
<td align="left"><p>12gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>2GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a>MBAM 서버 프로세서, RAM, 디스크 공간 요구 사항-구성 관리자 통합 토폴로지

다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 MBAM 서버의 서버 프로세서, RAM, 디스크 공간 요구 사항이 나열 되어 있습니다. 독립 실행형 토폴로지에 대 한 요구 사항에 대해서는 [Mbam 서버 프로세서, RAM 및 디스크 공간 요구 사항-독립 실행형 토폴로지](#bkmk-stand-alone-ramreqs)를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">하드웨어 항목</th>
<th align="left">최소 요구 사항</th>
<th align="left">권장 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>처리자</p></td>
<td align="left"><p>2.33 GHz</p></td>
<td align="left"><p>2.33 GHz 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4GB</p></td>
<td align="left"><p>8gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>2GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>MBAM이 지 원하는 Configuration Manager 버전

MBAM은 다음 버전의 Configuration Manager를 지원 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">지원 되는 버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (현재 분기), 버전이 최대 1902입니다.</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (LTSB-버전 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft System Center 2012 구성 관리자</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 이상</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p>

&gt;<strong>참고 </strong> Configuration Manager 2007 R2는 32 비트 이지만 64 비트 MBAM 소프트웨어와 일치 하려면 64 비트 운영 체제에 SQL Server를 설치 해야 합니다.
</td>
</tr>
</tbody>
</table>



Configuration Manager 서버에서 지원 되는 구성 목록은 사용 중인 구성 관리자 버전에 해당 하는 TechNet 문서를 참조 하세요. MBAM에는 Configuration Manager 서버에 대 한 추가 시스템 요구 사항이 없습니다.

### <a href="" id="sql-server-database-requirements-"></a>SQL Server 데이터베이스 요구 사항

다음 표에는 복구 데이터베이스, 준수 및 감사 데이터베이스, 보고서 기능을 포함 하는 MBAM 서버 기능에 대해 지원 되는 Microsoft SQL Server 버전이 나와 있습니다. 필요한 버전은 독립 실행형 또는 Configuration Manager 통합 토폴로지에 적용 됩니다.

Sql **\ _Latin1 \ _General \ _CP1 \ _CI \ _AS** 데이터 정렬을 사용 하 여 sql Server를 설치 해야 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server 버전</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64비트</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64비트</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p>이상을</p></td>
<td align="left"><p>64비트</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard 또는 Enterprise</p></td>
<td align="left"><p>이상을</p></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>

**참고**  
SQL 2016을 지원 하려면 MDOP 용 2017 서비스 릴리스를 설치 하 https://www.microsoft.com/download/details.aspx?id=54967 고 SQL 2017을 지원 하려면 mdop에 대해 7 월 2018 서비스 릴리스를 설치 해야 합니다 https://www.microsoft.com/download/details.aspx?id=57157 . 일반적으로 최신 서비스 업데이트를 항상 사용 하는 것은 물론, 모든 버그 수정과 새로운 기능도 포함 하 고 있습니다.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>SQL Server 프로세서, RAM, 디스크 공간 요구 사항-독립 실행형 토폴로지

다음 표에는 독립 실행형 토폴로지를 사용 하는 경우 SQL Server 컴퓨터에 권장 되는 서버 프로세서, RAM, 디스크 공간 요구 사항이 나열 되어 있습니다. 이러한 요구 사항을 지침으로 사용 합니다. 특정 요구 사항은 엔터프라이즈에서 지원 되는 클라이언트 컴퓨터 수에 따라 달라 집니다. Configuration Manager 통합 토폴로지에 대 한 요구 사항을 보려면 [SQL Server 프로세서, RAM 및 디스크 공간 요구 사항-구성 관리자 통합 토폴로지](#bkmk-cm-sql-ramreqs)를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">하드웨어 항목</th>
<th align="left">최소 요구 사항</th>
<th align="left">권장 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>처리자</p></td>
<td align="left"><p>2.33 GHz</p></td>
<td align="left"><p>2.33 GHz 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8gb</p></td>
<td align="left"><p>12gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>5GB</p></td>
<td align="left"><p>5gb 이상</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a>SQL Server 프로세서, RAM 및 디스크 공간 요구 사항-구성 관리자 통합 토폴로지

다음 표에는 Configuration Manager 통합 토폴로지를 사용 하는 경우 Microsoft SQL Server 컴퓨터에 대 한 서버 프로세서, RAM, 디스크 공간 요구 사항이 나와 있습니다. [SQL Server 프로세서, ram 및 디스크 공간 요구 사항-독립 실행형 토폴로지](#bkmk-sql-stand-alone-ramreqs)를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">하드웨어 항목</th>
<th align="left">최소 요구 사항</th>
<th align="left">권장 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>처리자</p></td>
<td align="left"><p>2.33 GHz</p></td>
<td align="left"><p>2.33 GHz 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4GB</p></td>
<td align="left"><p>8gb</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 가능한 디스크 공간</p></td>
<td align="left"><p>5GB</p></td>
<td align="left"><p>5GB</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> MBAM 클라이언트 시스템 요구 사항


### 클라이언트 운영 체제 요구 사항

동일한 시스템의 운영 체제에서 MBAM 클라이언트와 MBAM 서버를 실행 하는 것이 좋습니다. 예를 들어 windows 10이 포함 되어 있는 windows Server 2016, windows 8.1 windows Server 2012 R2 등

다음 표에는 MBAM 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다. 독립 실행형 및 Configuration Manager 통합 토폴로지에도 동일한 요구 사항이 적용 됩니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p>Windows 10 IoT</p></td>
    <td align="left"><p>엔터프라이즈</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32비트 또는 64비트</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>엔터프라이즈</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>엔터프라이즈</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>엔터프라이즈 또는 Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8.1 및 Windows 10 Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>클라이언트 RAM 요구 사항

MBAM 클라이언트 설치와 관련 된 RAM 요구 사항은 없습니다.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> MBAM 그룹 정책 시스템 요구 사항


다음 표에는 MBAM 그룹 정책 서식 파일 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p>Windows 10 IoT</p></td>
      <td align="left"><p>엔터프라이즈</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32비트 또는 64비트</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>엔터프라이즈</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>엔터프라이즈</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise 또는 Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>

## Azure IaaS에서 MBAM

MBAM 서버는 위에 나열 된 지원 OS 버전의 IaaS (Azure 인프라 as Services)에 배포 될 수 있으며, 온-프레미스에서 호스트 되는 Active Directory 또는 Azure IaaS에 호스트 된 Active Directory에 연결 됩니다.  Azure IaaS에서 Active Directory를 설정 및 구성 하는 방법에 대 한 문서는 [다음과](https://msdn.microsoft.com/library/azure/jj156090.aspx)같습니다.

MBAM 클라이언트는 가상 머신에서 지원 되지 않으며, Azure IaaS 에서도 지원 되지 않습니다.


## 서비스 릴리스 

- [4 월 2016 핫픽스](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [2016 년 9 월](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [2016년 12월](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [2017년 3월](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [2017년 6월](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [2017년 9월](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [2018년 3월](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2018 년 7 월](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2019 년 5 월](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## 관련 항목


[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)

[MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)




## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




