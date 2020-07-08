---
title: MBAM 웹 사이트를 보호하는 방법 계획
description: MBAM 웹 사이트를 보호하는 방법 계획
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825023"
---
# MBAM 웹 사이트를 보호하는 방법 계획


이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털을 보호 하기 위한 다음 방법에 대해 설명 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">필수 또는 선택 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>인증서를 사용 하 여 MBAM 웹 사이트 보안</p></td>
<td align="left"><p>선택 사항 이지만 매우 좋음</p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램 풀 계정에 대 한 SPN (서비스 사용자 이름) 등록</p></td>
<td align="left"><p>필수</p></td>
</tr>
</tbody>
</table>



MBAM 배포를 보호 하는 방법에 대 한 자세한 내용은 [mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md)참조 하세요.

## 인증서를 사용 하 여 MBAM 웹 사이트 보안


인증서를 사용 하 여 다음 간의 통신을 보호 하는 것이 좋습니다.

-   MBAM 클라이언트 및 웹 서비스

-   브라우저 및 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털 웹 사이트

인증서 요청 및 설치에 대 한 자세한 내용은 [인터넷 서버 인증서 구성을](https://technet.microsoft.com/library/cc731977.aspx)참조 하세요.

**참고**  
Windows PowerShell을 사용 하는 경우에만 다른 서버에서 웹 사이트 및 웹 서비스를 구성할 수 있습니다. MBAM 서버 구성 마법사를 사용 하 여 웹 사이트를 구성 하는 경우에는 동일한 서버에서 웹 사이트 및 웹 서비스를 구성 해야 합니다.



웹 서비스와 데이터베이스 간의 통신을 보호 하려면 SQL Server에 암호화를 강제로 적용 하는 것이 좋습니다. 웹 서비스와 SQL Server 간의 통신을 비롯 하 여 SQL Server에 대 한 모든 연결을 보호 하는 방법에 대 한 자세한 내용은 [Mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-secure-databases)참조 하세요.

## 응용 프로그램 풀 계정에 대 한 Spn 등록


MBAM 서버에서 관리 및 모니터링 웹 사이트와 셀프 서비스 포털의 통신을 인증 하도록 설정 하려면 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 호스트 이름에 대 한 SPN (서비스 사용자 이름)을 등록 해야 합니다.

이 항목에는 다음 유형의 호스트 이름에 대해 Spn을 등록 하는 방법에 대 한 지침이 포함 되어 있습니다.

-   정규화 된 도메인 이름

-   NetBIOS 이름

-   가상 이름

### 초기 MBAM 설치에 대 한 Spn을 만들기 전에

Spn 만들기를 시작 하기 전에 다음 표의 정보를 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 또는 항목</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AD DS (Active Directory 도메인 서비스)에서 서비스 계정을 만듭니다.</p></td>
<td align="left"><p>서비스 계정은 AD DS에서 만든 사용자 계정으로, MBAM 웹 사이트에 보안을 제공 합니다. MBAM 웹 사이트는 응용 프로그램 풀에서 실행 되며, 해당 id는 서비스 계정의 이름입니다. 그러면 Spn이 응용 프로그램 풀 계정에 등록 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>모든 웹 서버에 같은 응용 프로그램 풀 계정을 사용 해야 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>IIS-IUSRS 그룹 계정 또는 응용 프로그램 풀 계정에 필요한 권한이 부여 되었는지 확인 합니다.</p></td>
<td align="left"><p>이를 확인 하려면 다음 단계를 따르세요.</p>
<ol>
<li><p><strong>로컬 보안 정책 편집기를 열고 </strong> <strong> 로컬 정책 노드를 확장 </strong> 합니다.</p></li>
<li><p><strong>사용자 권한 할당 </strong> 노드를 선택 하 고 인증 후 클라이언트로 가장을 두 번 클릭 하 고 <strong> </strong> <strong> 오른쪽 창에서 일괄 작업으로 로그온 </strong> 그룹 정책 설정을 사용 합니다.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>도메인 관리 계정을 사용 하 여 MBAM 웹 사이트를 구성 하는 경우 MBAM이 사용자를 위한 Spn을 만듭니다.</p></td>
<td align="left"><p>도메인 관리 계정을 사용 하 여 MBAM 웹 사이트를 구성 하는 경우 사용 중인 호스트 이름 유형에 Spn을 수동으로 등록 하려면이 항목의 단계를 따르세요.</p></td>
</tr>
</tbody>
</table>



### 정규화 된 도메인 호스트 이름을 사용할 때 Spn 등록

MBAM을 구성할 때 정규화 된 도메인 호스트 이름을 사용 하는 경우 다음 예제에 표시 된 대로 SPN을 하나만 등록 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">수행 해야 할 작업</th>
<th align="left">예제 및 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>정규화 된 도메인 이름에 대 한 SPN을 등록 합니다.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>정규화 된 호스트 이름이 <strong> mybitlockerrecovery.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램 풀 계정에 대해 등록 하는 SPN에 대해 제한 된 위임을 구성 합니다.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">제한 된 위임 구성</a></p>
<p>이 요구 사항은 MBAM 2.5에만 적용 됩니다. MBAM 2.5 SP1에서는 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



### NetBIOS 호스트 이름을 사용할 때 Spn 등록

MBAM을 구성할 때 NetBIOS 호스트 이름을 사용 하는 경우 다음 예제와 같이 NetBIOS 이름에 대해 하나의 SPN 및 정규화 된 도메인 이름에 대 한 다른 SPN을 등록 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">수행 해야 할 작업</th>
<th align="left">예제 및 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>NetBIOS 호스트 이름에 대 한 SPN을 등록 합니다.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>NetBIOS 호스트 이름이 <strong> nbname01 </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>정규화 된 도메인 이름에 대 한 SPN을 등록 합니다.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>정규화 된 도메인 이름이 <strong> nbname01.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>응용 프로그램 풀 계정에 대해 등록 하는 Spn에 대해 제한 된 위임을 구성 합니다.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">제한 된 위임 구성</a></p>
<p>이 요구 사항은 MBAM 2.5에만 적용 됩니다. MBAM 2.5 SP1에서는 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>가상 호스트 이름을 사용할 때 Spn 등록

정규화 된 도메인 이름인 가상 호스트 이름으로 MBAM을 구성 하는 경우 가상 호스트 이름에 대해 SPN을 하나만 등록 합니다. 구성 하는 가상 호스트 이름이 정규화 된 도메인 이름이 아니면 다음 예제와 같이 정규화 된 도메인 이름을 지정 하는 두 번째 SPN을 만들어야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">수행 해야 할 작업</th>
<th align="left">예제 및 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이 예제와 같이 가상 호스트 이름이 정규화 된 도메인 이름이 면 SPN을 하나만 등록 합니다.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>이 예제에서는 가상 호스트 이름이 <strong> mbamvirtual.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>가상 호스트 이름이 정규화 된 도메인 이름이 아닌 경우이 추가 SPN을 등록 합니다.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>이 예제에서 가상 호스트 이름은 <strong> mbamvirtual이 </strong> 고 웹 응용 프로그램 풀에 사용 되는 도메인 계정은 <strong> contoso\mbamapppooluser입니다 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>가상 호스트 이름이 정규화 된 도메인 이름이 아닌 경우이 추가 SPN을 등록 합니다.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>이 예제에서는 가상 호스트 이름이 <strong> mbamvirtual.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DNS (도메인 이름 서버) 서버에서 사용자 지정 호스트 이름에 대해 "A record"를 만들고 웹 서버 또는 부하 분산 장치를 가리킵니다.</p></td>
<td align="left"><p>DNS 호스트 레코드 구성에서 "DNS 호스트 A 레코드를 구성 하려면" 섹션을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> </a> .</p>
<p>CNAMES 대신 레코드를 사용 하는 것이 좋습니다. 도메인 주소를 가리키는 CNAMES을 사용 하는 경우 응용 프로그램 풀 계정에서 웹 서버 이름에 대 한 Spn도 등록 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>응용 프로그램 풀 계정에 대해 등록 하는 Spn에 대해 제한 된 위임을 구성 합니다.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">제한 된 위임 구성</a></p>
<p>이 요구 사항은 MBAM 2.5에만 적용 됩니다. MBAM 2.5 SP1에서는 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>이전 버전의 MBAM에서 업그레이드할 때 SPN 등록

다음과 같은 경우에만이 섹션의 단계를 완료 합니다.

-   이전 버전의 MBAM에서 업그레이드 합니다.

-   부하 분산 또는 분산 구성에서 MBAM 2.5에서 웹 사이트를 실행 하 고 현재 부하 분산 되지 않은 구성으로 실행 중입니다.

응용 프로그램 풀 계정이 아닌 컴퓨터 계정에 Spn을 등록 한 경우, MBAM은 기존 Spn을 사용 하며 부하 분산 또는 분산 구성에서 웹 사이트를 구성할 수 없습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">수행 해야 할 작업</th>
<th align="left">예제 및 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AD DS (Active Directory 도메인 서비스)에 응용 프로그램 풀 계정을 만듭니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>현재 설치 된 웹 사이트 및 웹 서비스를 제거 합니다.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">MBAM 서버 기능 또는 소프트웨어 제거</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 계정에서 Spn을 제거 합니다.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램 풀 계정에 Spn을 등록 합니다.</p></td>
<td align="left"><p><a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">가상 호스트 이름을 사용할 때 spn을 등록 하는 단계를 따릅니다 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>웹 응용 프로그램 및 웹 서비스를 다시 구성 합니다.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>구성에 사용 하는 방법에 따라 다음 중 하나를 수행 합니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAM 서버 구성 마법사</strong></p></td>
<td align="left"><p><strong>웹 서비스 응용 프로그램 풀 도메인 계정 필드에 응용 프로그램 풀 계정을 입력 </strong> 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Windows PowerShell cmdlet</p></td>
<td align="left"><p><code>WebServiceApplicationPoolCredential</code>매개 변수에 계정을 입력 합니다.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>중요</strong><br/><p>입력 하는 호스트 이름은 Spn을 만드는 가상 호스트 이름과 동일 해야 합니다. 또한 웹 팜에서는 구성 하는 모든 서버에서 호스트 이름 및 응용 프로그램 풀 자격 증명이 동일 해야 합니다.</p>
</div>
<div>

</div>
<p>MBAM이 웹 응용 프로그램을 구성 하는 경우 Spn을 등록 하려고 시도 하지만이 작업은 사용자가 MBAM을 설치 하는 서버에 대 한 도메인 관리자 권한이 있는 경우에만 가능 합니다. 이러한 권한이 없는 경우 구성을 완료할 수 있지만, MBAM을 구성 하기 전이나 후에 Spn을 설정 해야 합니다.</p></td>
</tr>
</tbody>
</table>

## 필수 요청 필터링 설정

 응용 프로그램이 정상적으로 작동 하려면 ' 나열 되지 않은 파일 이름 확장명 허용 '이 필요 합니다.  이는 ' Microsoft BitLocker 관리 및 모니터링 ' > 요청 필터링-> 편집 기능 설정을 탐색 하 여 찾을 수 있습니다.


## 관련 항목


[MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)

[MBAM 2.5 배포 필수 구성 요소](mbam-25-deployment-prerequisites.md)





## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.



