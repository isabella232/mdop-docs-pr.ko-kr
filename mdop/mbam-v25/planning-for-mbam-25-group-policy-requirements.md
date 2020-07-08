---
title: MBAM 2.5 그룹 정책 요구 사항 계획
description: MBAM 2.5 그룹 정책 요구 사항 계획
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823768"
---
# MBAM 2.5 그룹 정책 요구 사항 계획


다음 정보를 사용 하 여 엔터프라이즈에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트 컴퓨터를 관리 하는 데 사용할 수 있는 BitLocker 프로텍터 유형을 확인 합니다.

## MBAM이 지 원하는 BitLocker 프로텍터 종류


MBAM은 다음 유형의 BitLocker 보호기를 지원 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">드라이브 또는 볼륨 종류</th>
<th align="left">지원 되는 BitLocker 프로텍터</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>운영 체제 볼륨</p></td>
<td align="left"><ul>
<li><p><strong>TPM(신뢰할 수 있는 플랫폼 모듈)</strong></p></li>
<li><p><strong>TPM + PIN</strong></p></li>
<li><p><strong>TPM + USB 키 </strong> – MBAM이 설치 되기 전에 운영 체제 볼륨을 암호화 한 경우에만 지원 됩니다.</p></li>
<li><p><strong></strong> - 컴퓨터 운영 체제 볼륨이 mbam이 설치 되기 전에 암호화 된 경우에만 지원 되는 TPM + PIN + USB 키</p></li>
<li><p><strong>TPM이 없는 </strong> - Windows to Go 장치, 고정 데이터 드라이브, windows 8, windows 8.1 및 windows 10 장치 에서만 지원 되는 암호</p></li>
<li><p><strong>숫자 암호는 </strong> - 볼륨 암호화의 일부로 자동 적용 되며 Windows 7에서 FIPS 모드를 제외 하 고 구성할 필요는 없습니다.</p></li>
<li><p><strong>DRA (Data recovery agent)</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>고정 데이터 드라이브</p></td>
<td align="left"><ul>
<li><p><strong>암호</strong></p></li>
<li><p><strong>자동 잠금 해제</strong></p></li>
<li><p><strong>숫자 암호는 </strong> - 볼륨 암호화의 일부로 자동 적용 되며 Windows 7에서 FIPS 모드를 제외 하 고 구성할 필요는 없습니다.</p></li>
<li><p><strong>DRA (Data recovery agent)</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>이동식 드라이브</p></td>
<td align="left"><ul>
<li><p><strong>암호</strong></p></li>
<li><p><strong>자동 잠금 해제</strong></p></li>
<li><p><strong>숫자 암호는 </strong> - 볼륨 암호화의 일부로 자동 적용 되며 구성할 필요가 없습니다.</p></li>
<li><p><strong>DRA (Data recovery agent)</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### 사용 된 공간 암호화 BitLocker 정책에 대 한 지원

MBAM 2.5 SP1에서 BitLocker 그룹 정책을 통해 사용 하는 공간 암호화를 사용 하도록 설정 하면 MBAM 클라이언트가이를 허용 합니다.

이 그룹 정책 설정을 **운영 체제 드라이브에 드라이브 암호화 유형 강제 적용** 이라고 하며, **컴퓨터 구성** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **BitLocker 드라이브 암호화** &gt; **운영 체제 드라이브**에는 다음과 같은 GPO 노드가 있습니다. 이 정책을 사용 하 고 **사용 된 공간만 암호화**로 암호화 유형을 선택 하는 경우, mbam은 정책을 인식 하 고 BitLocker는 볼륨에 사용 되는 디스크 공간만 암호화 합니다.

## MBAM 그룹 정책 템플릿을 가져오고 설정을 편집 하는 방법


원하는 MBAM 그룹 정책 설정을 구성할 준비가 되었으면 다음을 수행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">팔 로우 단계</th>
<th align="left">지침을 받을 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 그룹 정책 서식 파일을 복사 하 여 <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> </a> GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 실행할 수 있는 컴퓨터에 설치 하는 방법에서 MDOP 그룹 정책 (Admx) 서식 파일을 다운로드 합니다.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">MBAM 2.5 그룹 정책 템플릿 복사</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>엔터프라이즈에서 사용할 그룹 정책 설정을 구성 합니다.</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">MBAM 2.5 그룹 정책 설정 편집</a></p></td>
</tr>
</tbody>
</table>



## MBAM 그룹 정책 설정에 대 한 설명


**MDOP (BitLocker 관리)** GPO 노드에는 4 개의 글로벌 정책 설정과 **클라이언트 관리**, **고정 드라이브**, **운영 체제 드라이브**, **이동식 드라이브**의 네 개의 자식 GPO 노드가 있습니다. 다음 섹션에서는 MBAM 그룹 정책 설정에 대 한 설정 및 제안 사항을 설명 합니다.

**중요**  
**BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다. MBAM은 **MDOP mbam (BitLocker Management)** 노드에서 설정을 구성할 때이 노드의 설정을 자동으로 구성 합니다.



### 글로벌 그룹 정책 정의

이 섹션에서는 다음과 같은 GPO 노드에서 mbam 전역 그룹 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 그룹 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>드라이브 암호화 방법 및 암호화 수준 선택</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>특정 암호화 방법 및 암호화 강도를 사용 하도록이 정책을 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 BitLocker는 기본 암호화 방법 인 AES 128-디퓨저를 사용 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>BitLocker 컴퓨터 준수 보고서의 문제는 &quot; &quot; 기본값을 사용 하는 경우에도 암호화 강도에 대해 알 수 없는 것으로 표시 되도록 합니다. 이 문제를 해결 하려면이 설정을 사용 하 고 암호화 수준에 대 한 값을 설정 해야 합니다.</p>
</div>
<div>

</div>
<ul>
<li><p>AES 128-디퓨저-Windows 7 전용</p></li>
<li><p>Windows 8, Windows 8.1 및 Windows 10 용 AES 128</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>다시 시작할 때 메모리 덮어쓰기 방지</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>다시 시작 시 메모리의 BitLocker 비밀을 덮어쓰지 않고 다시 시작 성능을 향상 시키려면이 정책을 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 컴퓨터가 다시 시작 될 때 BitLocker 비밀이 메모리에서 제거 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>스마트 카드 인증서 용도 규칙 유효성 검사</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>스마트 카드 인증서 기반 BitLocker 보호를 사용 하도록이 정책을 구성 합니다.</p>
<p>이 정책이 구성 되지 않은 경우에는 기본 개체 식별자 1.3.6.1.4.1.311.67.1.1를 사용 하 여 인증서를 지정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>조직의 고유 식별자를 제공 합니다.</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>인증서 기반 데이터 복구 에이전트 또는 BitLocker To Go 읽기 프로그램을 사용 하도록이 정책을 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 <strong> 식별 </strong> 필드가 사용 되지 않습니다.</p>
<p>회사에서 더 높은 수준의 보안을 요구 하는 경우 <strong> id 필드를 구성 </strong> 하 여 모든 USB 장치에이 필드 집합을 포함 하 고이를이 그룹 정책 설정에 맞출지 여부를 확인 합니다.</p></td>
</tr>
</tbody>
</table>



### 클라이언트 관리 그룹 정책 정의

이 섹션에서는 다음 GPO 노드에서 mbam에 대 한 클라이언트 관리 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **클라이언트 관리**.

다음 표에 표시 된 대로 구성 관리자 통합 토폴로지를 사용 하는 경우 한 가지 예외를 제외 하 고 독립 실행형 및 System Center Configuration ** &gt; ** Manager 통합 토폴로지에 대해 동일한 그룹 정책 설정을 설정할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 그룹 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 서비스 구성</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<ul>
<li><p><strong>MBAM 복구 및 하드웨어 서비스 끝점 </strong> 입니다. 이 설정을 사용 하 여 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 설정 합니다. 다음 예제와 유사한 끝점 위치를 입력 합니다. <strong> http (s)// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가/MBAMRecoveryAndHardwareService/CoreService.svc에 바인딩된 포트입니다 &gt; </em><strong> </strong> .</p></li>
<li><p><strong>저장할 BitLocker 복구 정보를 선택 </strong> 합니다. 이 정책 설정을 통해 BitLocker 복구 정보를 백업 하도록 키 복구 서비스를 구성할 수 있습니다. 또한 보고서를 수집 하는 상태 보고 서비스도 구성할 수 있습니다. 이 정책은 키 정보가 부족 하 여 데이터 손실을 방지 하기 위해 BitLocker에서 암호화 한 데이터를 복구 하는 관리 방법을 제공 합니다. 상태 보고서 및 키 복구 작업이 자동으로 구성 된 보고서 서버 위치에 전송 됩니다.</p>
<p>이 정책 설정을 구성 하지 않거나 사용 하지 않도록 설정 하면 키 복구 정보가 저장 되지 않으며 상태 보고서 및 키 복구 작업이 서버에 보고 되지 않습니다. 이 설정이 <strong> 복구 암호 및 키 패키지로 설정 되어 있으면 </strong> 복구 암호와 키 패키지가 자동으로 구성 된 키 복구 서버 위치에 백업 됩니다.</p></li>
<li><p><strong>클라이언트 검사 상태 빈도를 분 단위로 입력 </strong> 합니다. 이 정책 설정은 클라이언트가 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하는 빈도를 관리 합니다. 또한이 정책은 클라이언트 준수 상태가 서버에 저장 되는 빈도를 관리 합니다. 클라이언트는 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하 고 구성 된 빈도로 클라이언트 복구 키를 백업 합니다.</p>
<p>회사에서 설정한 요구 사항에 따라 컴퓨터의 준수 상태를 확인 하는 빈도 및 클라이언트 복구 키를 백업 하는 빈도를 기준으로이 빈도를 설정 합니다.</p></li>
<li><p><strong>MBAM 상태 보고 서비스 끝점:</strong></p>
<p><strong>독립 실행형 토폴로지에서 MBAM </strong> : Mbam 클라이언트 BitLocker 암호화 관리를 설정 하려면이 설정을 구성 해야 합니다.</p>
<p>다음 예와 비슷한 끝점 위치를 입력 합니다.</p>
<p><strong>http (s)// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가/MBAMComplianceStatusService/StatusReportingService.svc에 바인딩된 포트입니다. &gt; </em><strong></strong></p>
<p><strong>Configuration Manager 통합 토폴로지의 MBAM </strong> :이 설정을 사용 하지 않도록 설정 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 예외 정책 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 사용자가 BitLocker 암호화에서 예외를 요청 하도록 하는 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 구성할 수 있습니다.</p>
<p>이 정책 설정을 사용 하 고 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 제공 하는 경우, 사용자는 BitLocker 보호에서 예외를 적용 하는 방법에 대 한 지침이 있는 대화 상자가 표시 됩니다. 사용자의 BitLocker 암호화 예외를 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> 사용자 Bitlocker 암호화 예외를 관리 하는 방법을 참조 하세요 </a> .</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 예외 요청 지침이 사용자에 게 표시 되지 않습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>사용자 예외는 컴퓨터당만 관리 됩니다. 여러 사용자가 같은 컴퓨터에 로그온 하 고 한 사용자가 제외 되지 않은 경우 컴퓨터는 암호화 됩니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 환경 개선 프로그램 구성</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 사용 하면 사용자 환경 개선 프로그램에 MBAM이 참여할 수 있는 기간을 구성할 수 있습니다. 이 프로그램은 컴퓨터 하드웨어와 사용자가 작업을 중단 하지 않고 MBAM을 사용 하는 방법에 대 한 정보를 수집 합니다. 이 정보는 Microsoft가 향상 시킬 MBAM 기능을 식별 하는 데 도움이 됩니다. Microsoft는이 정보를 사용 하 여 MBAM 사용자를 식별 하거나 연락 하지 않습니다.</p>
<p>이 정책 설정을 사용 하면 사용자 환경 개선 프로그램에 참가할 수 있습니다.</p>
<p>이 정책을 사용 하지 않도록 설정 하면 사용자 환경 개선 프로그램에 참여할 수 없습니다.</p>
<p>이 정책 설정을 구성 하지 않으면 사용자 환경 개선 프로그램에 참가할 수 있는 옵션이 제공 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>보안 정책 링크의 URL을 입력 합니다.</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 사용 하 여 최종 사용자에 게 회사 보안 정책 이라는 링크로 표시 되는 URL을 지정 &quot; 합니다. &quot; 링크는 회사의 내부 보안 정책을 가리키고 최종 사용자에 게 암호화 요구 사항에 대 한 정보를 제공 합니다. 드라이브를 암호화 하기 위해 사용자에 게 메시지를 표시 하는 경우에는 MBAM이 링크를 표시 합니다.</p>
<p>이 정책 설정을 사용 하도록 설정 하는 경우 보안 정책 링크에 대 한 URL을 구성할 수 있습니다.</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 보안 정책 링크가 사용자에 게 표시 되지 않습니다.</p></td>
</tr>
</tbody>
</table>



### 고정 드라이브 그룹 정책 정의

이 섹션에서는 다음 GPO 노드에서 Microsoft BitLocker 관리 및 모니터링에 대 한 고정 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **고정식 드라이브**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 그룹 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>고정 데이터 드라이브 암호화 설정</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 통해 고정 데이터 드라이브를 암호화할지 여부를 관리할 수 있습니다.</p>
<p>운영 체제 볼륨을 암호화 해야 하는 경우에는 <strong> 고정 데이터 드라이브 자동 잠금 해제 사용을 클릭 </strong> 합니다.</p>
<p>이 정책을 사용 하는 경우 <strong> </strong> 고정 데이터 드라이브에 대 한 자동 잠금 해제를 사용 하도록 설정 하거나 요구 하지 않는 한 고정 데이터 드라이브에 대 한 암호 사용 구성을 사용 하지 않도록 설정 해야 합니다.</p>
<p>고정 데이터 드라이브에 대 한 자동 잠금 해제를 사용 해야 하는 경우 운영 체제 볼륨을 암호화 하도록 구성 해야 합니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 모든 고정 데이터 드라이브를 BitLocker 보호에 포함 해야 하며 데이터 드라이브는 암호화 됩니다.</p>
<p>이 정책 설정을 구성 하지 않으면 사용자가 BitLocker 보호 아래에 고정 데이터 드라이브를 추가할 필요가 없습니다. 고정 데이터 드라이브가 암호화 된 후이 정책을 적용 하면 MBAM 에이전트는 암호화 된 고정 데이터 드라이브의 암호를 해독 합니다.</p>
<p>이 정책 설정을 사용 하지 않으면 사용자가 BitLocker 보호에 고정 데이터 드라이브를 추가할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker에 의해 보호되지 않는 고정 드라이브에 대한 쓰기 액세스 거부</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정은 컴퓨터에서 고정 데이터 드라이브를 쓰기 가능 하 게 하기 위해 BitLocker 보호가 필요한 지 여부를 결정 합니다. 이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</p>
<p>정책이 구성 되지 않은 경우 컴퓨터의 모든 고정 데이터 드라이브는 읽기/쓰기 권한으로 탑재 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이전 버전의 Windows에서 BitLocker로 보호 되는 고정 드라이브에 대 한 액세스 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 수정 된 드라이브를 잠금 해제 하 고 볼 수 있도록이 정책을 사용 하도록 설정 합니다.</p>
<p>정책을 사용 하거나 구성 하지 않으면 FAT 파일 시스템으로 포맷 된 고정 드라이브를 잠금 해제할 수 있으며 windows Server 2008, Windows Vista, Windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 있습니다. 이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</p>
<p>정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 된 고정 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>고정 드라이브의 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 BitLocker로 보호 된 고정 데이터 드라이브의 잠금을 해제 하는 데 암호가 필요한 지 여부를 지정 합니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 정의한 요구 사항을 충족 하는 암호를 구성할 수 있습니다. BitLocker는 사용자가 드라이브에서 사용할 수 있는 모든 보호기를 사용 하 여 드라이브 잠금을 해제할 수 있도록 합니다.</p>
<p>이러한 설정은 볼륨을 잠금 해제할 때가 아닌 BitLocker를 켤 때 적용 됩니다.</p>
<p>이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</p>
<p>정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</p>
<p>보안을 강화 하려면이 정책을 사용 하도록 설정한 다음 <strong> 고정 데이터 드라이브에 대해 암호 요구를 선택 하 고 </strong> <strong> 암호 복잡도 필요를 클릭 하 </strong> 고 <strong> 원하는 최소 암호 길이를 설정 </strong> 합니다.</p>
<p>이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</p>
<p>이 정책 설정을 구성 하지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 되는 고정 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>정책이 구성 되어 있지 않으면 BitLocker 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다. MBAM에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>암호화 정책 적용 설정</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 사용 하 여 고정 데이터 드라이브가 MBAM 정책에 부합 될 때까지 비규격으로 유지 될 수 있는 날짜 수를 구성 합니다. 사용자는 필요한 작업을 연기 하거나 유예 기간 후에 예외를 요청할 수 없습니다. 유예 기간은 고정 데이터 드라이브가 비규격 인 것으로 판단 되는 경우 시작 됩니다. 그러나 고정 데이터 드라이브 정책은 운영 체제 드라이브가 호환 될 때까지 적용 되지 않습니다.</p>
<p>유예 기간이 만료 되 고 고정 데이터 드라이브가 여전히 호환 되지 않는 경우 사용자는 예외를 연기 하거나 요청 하는 옵션을 사용할 수 없습니다. 암호화 프로세스에 사용자 입력이 필요한 경우 필요한 정보를 제공할 때까지 사용자가 닫을 수 없는 대화 상자가 나타납니다.</p>
<p><strong> </strong> <strong> </strong> 운영 체제 드라이브에 대 한 유예 기간이 만료 된 후 즉시 암호화 프로세스가 시작 되도록 하려면 0을 입력 하 여 고정 드라이브의 비 준수 유예 기간 일 수를 구성 합니다.</p>
<p>이 설정을 사용 하지 않거나 구성 하지 않으면 사용자가 MBAM 정책에 부합 하지 않습니다.</p>
<p>보호기를 추가 하기 위해 사용자 조작이 필요 하지 않은 경우, 유예 기간이 만료 된 후 백그라운드에서 암호화가 시작 됩니다.</p></td>
</tr>
</tbody>
</table>



### 운영 체제 드라이브 그룹 정책 정의

이 섹션에서는 다음 GPO 노드에서 Microsoft BitLocker 관리 및 모니터링에 대 한 운영 체제 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **운영 체제 드라이브**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 그룹 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>운영 체제 드라이브 암호화 설정</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 통해 운영 체제 드라이브를 암호화 해야 하는지 여부를 관리할 수 있습니다.</p>
<p>보안을 강화 하려면 <strong> </strong> &gt; <strong> </strong> &gt; <strong> </strong> TPM + PIN 보호기를 사용 하 여 시스템 전원 관리 절전 모드 설정에서 다음 정책 설정을 해제 하는 것이 좋습니다.</p>
<ul>
<li><p>절전 모드에서 대기 상태 (S1-S3) 허용 (전원 사용)</p></li>
<li><p>절전 모드 시 대기 상태 (S1-S3) 허용 (배터리 사용)</p></li>
</ul>
<p>Microsoft Windows 8 이상을 실행 중이 고 TPM이 없는 컴퓨터에서 BitLocker를 사용 하려는 경우 <strong> 호환 되는 tpm이 없는 bitlocker 허용 확인란을 선택 </strong> 합니다. 이 모드에서는 시작 하는 데 암호가 필요 합니다. 암호를 잊어버린 경우 BitLocker 복구 옵션 중 하나를 사용 하 여 드라이브에 액세스 해야 합니다.</p>
<p>호환 되는 TPM이 있는 컴퓨터에서는 시작 시 암호화 된 데이터에 대 한 추가 보호를 제공 하기 위해 두 가지 유형의 인증 방법을 사용할 수 있습니다. 컴퓨터가 시작 되 면 인증에 TPM만 사용 하거나 PIN (개인 식별 번호)을 입력 해야 할 수도 있습니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 BitLocker protection에 운영 체제 드라이브를 설치 하 고 드라이브가 암호화 됩니다.</p>
<p>이 정책을 사용 하지 않도록 설정 하는 경우 사용자는 BitLocker protection에 운영 체제 드라이브를 추가할 수 없습니다. 운영 체제 드라이브를 암호화 한 후에이 정책을 적용 하면 드라이브의 암호가 해독 됩니다.</p>
<p>이 정책을 구성 하지 않으면, 운영 체제 드라이브를 BitLocker 보호 아래에 배치할 필요가 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>시작 시 향상 된 Pin 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 사용 하 여 향상 된 시작 Pin을 BitLocker와 함께 사용할지 여부를 구성 합니다. 향상 된 시작 Pin에는 대/소문자, 기호, 숫자, 공백 등의 문자 사용이 허용 됩니다. 이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</p>
<p>이 정책 설정을 사용 하면 모든 새 BitLocker 시작 Pin이 설정 되어 최종 사용자가 향상 된 Pin을 만들 수 있습니다. 그러나 일부 컴퓨터는 사전 부팅 환경에서 향상 된 Pin을 지원할 수 없습니다. 관리자가 사용 하도록 설정 하기 전에 해당 시스템이이 기능과 호환 되는지 여부를 평가 하도록 강력히 권장 합니다.</p>
<p><strong> </strong> 프리 부팅 환경에 입력할 수 있는 문자 종류 또는 수를 제한 하는 컴퓨터와 향상 된 pin을 더 호환 되도록 하려면 ASCII 전용 pin 필요 확인란을 선택 합니다.</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 강화 된 Pin이 사용 되지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 되는 운영 체제 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</p>
<p>MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제 드라이브에 대 한 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker로 보호 되는 운영 체제 드라이브의 잠금을 해제 하는 데 사용 되는 암호에 대 한 제약 조건을 설정 하려면이 정책 설정을 사용 합니다. 운영 체제 드라이브에서 TPM이 아닌 보호기를 사용할 수 있는 경우 암호를 프로 비전 하 고 암호에 복잡성 요구 사항을 적용 하 고 암호의 최소 길이를 구성할 수 있습니다. 복잡 한 요구 사항 설정을 적용 하려면 그룹 정책 설정 &quot; 암호가 &quot; 컴퓨터 구성 &gt; Windows 설정 &gt; 보안 설정 &gt; 계정 정책 &gt; 암호 정책에 있는 복잡성 요구 사항을 충족 해야 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이러한 설정은 볼륨을 잠금 해제할 때가 아닌 BitLocker를 켤 때 적용 됩니다. BitLocker를 사용 하면 드라이브에서 사용할 수 있는 모든 보호기를 사용 하 여 드라이브 잠금을 해제할 수 있습니다.</p>
</div>
<div>

</div>
<p>이 정책 설정을 사용 하면 사용자가 정의한 요구 사항을 충족 하는 암호를 구성할 수 있습니다. 비밀 번호에 복잡성을 적용 하려면 <strong> 비밀 번호 복잡성 요구를 클릭 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BIOS 기반 펌웨어 구성에 대 한 TPM 플랫폼 유효성 검사 프로필 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 컴퓨터&#39;s TPM (신뢰할 수 있는 플랫폼 모듈) 보안 하드웨어에서 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다. 컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</p>
<div class="alert">
<strong>중요</strong><br/><p>이 그룹 정책 설정은 BIOS 구성을 사용 하는 컴퓨터에만 적용 되 고 CSM (호환성 서비스 모듈)가 설정 된 UEFI 펌웨어가 있는 컴퓨터에만 적용 됩니다. 네이티브 UEFI 펌웨어 구성을 사용 하는 컴퓨터는 플랫폼 구성 레지스터 (PCRs)에 여러 값을 저장 합니다. 기본 uefi 펌웨어 구성 &quot; 에 tpm 플랫폼 유효성 검사 프로필 구성 &quot; 그룹 정책 설정을 사용 하 여 네이티브 uefi 펌웨어를 사용 하는 컴퓨터에 대 한 tpm PCR 프로필을 구성 합니다.</p>
</div>
<div>

</div>
<p>BitLocker를 설정 하기 전에이 정책 설정을 사용 하도록 설정 하면 BitLocker로 암호화 된 운영 체제 드라이브에 대 한 액세스를 잠금 해제 하기 전에 TPM에서 유효성을 검사 하는 부팅 구성 요소를 구성할 수 있습니다. BitLocker 보호가 적용 되는 동안 이러한 구성 요소 중 하나라도 변경 되 면 TPM은 암호화 키를 해제 하 여 드라이브 잠금을 해제 하지 않으며, 컴퓨터는 BitLocker 복구 콘솔을 표시 하 고 복구 암호 또는 복구 키를 제공 하 여 드라이브 잠금을 해제 해야 합니다.</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 BitLocker는 설치 스크립트에 지정 된 기본 플랫폼 유효성 검사 프로필 또는 플랫폼 유효성 검사 프로필을 사용 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TPM 플랫폼 유효성 검사 프로필 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 사용 하 여 컴퓨터&#39;s TPM (신뢰할 수 있는 플랫폼 모듈) 보안 하드웨어에서 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다. 컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</p>
<p>BitLocker를 설정 하기 전에이 정책 설정을 사용 하도록 설정 하면 BitLocker로 암호화 된 운영 체제 드라이브에 대 한 액세스를 잠금 해제 하기 전에 TPM에서 유효성을 검사 하는 부팅 구성 요소를 구성할 수 있습니다. BitLocker 보호가 적용 되는 동안 이러한 구성 요소 중 하나라도 변경 되 면 TPM은 암호화 키를 해제 하 여 드라이브 잠금을 해제 하지 않으며, 컴퓨터는 BitLocker 복구 콘솔을 표시 하 고 복구 암호 또는 복구 키를 제공 하 여 드라이브 잠금을 해제 해야 합니다.</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 BitLocker는 설치 스크립트에 지정 된 기본 플랫폼 유효성 검사 프로필 또는 플랫폼 유효성 검사 프로필을 사용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>기본 UEFI 펌웨어 구성에 대 한 TPM 플랫폼 유효성 검사 프로필 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 컴퓨터&#39;s TPM (신뢰할 수 있는 플랫폼 모듈) 보안 하드웨어에서 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다. 컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</p>
<div class="alert">
<strong>중요</strong><br/><p>이 그룹 정책 설정은 네이티브 UEFI 펌웨어 구성을 사용 하는 컴퓨터에만 적용 됩니다.</p>
</div>
<div>

</div>
<p>BitLocker를 설정 하기 전에이 정책 설정을 사용 하면 BitLocker로 암호화 된 운영 체제 드라이브에 대 한 액세스를 잠금 해제 하기 전에 TPM에서 유효성을 검사 하는 부팅 구성 요소를 구성할 수 있습니다. BitLocker 보호가 적용 되는 동안 이러한 구성 요소 중 하나라도 변경 되 면 TPM은 암호화 키를 해제 하 여 드라이브 잠금을 해제 하지 않으며, 컴퓨터는 BitLocker 복구 콘솔을 표시 하 고 복구 암호 또는 복구 키를 제공 하 여 드라이브 잠금을 해제 해야 합니다.</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 BitLocker는 설치 스크립트에 지정 된 기본 플랫폼 유효성 검사 프로필 또는 플랫폼 유효성 검사 프로필을 사용 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker 복구 후 플랫폼 유효성 검사 데이터 다시 설정</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 복구 후 Windows를 시작할 때 플랫폼 유효성 검사 데이터를 새로 고칠지 여부를 제어 하려면이 정책 설정을 사용 합니다.</p>
<p>이 정책 설정을 사용 하면 BitLocker 복구 후 Windows가 시작 될 때 플랫폼 유효성 검사 데이터가 새로 고쳐집니다. 이 정책 설정을 사용 하지 않으면 BitLocker 복구 이후 Windows가 시작 될 때 플랫폼 유효성 검사 데이터가 새로 고쳐지지 않습니다. 이 정책 설정을 구성 하지 않으면 BitLocker 복구 후 Windows가 시작 될 때 플랫폼 유효성 검사 데이터가 새로 고쳐집니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>향상 된 부팅 구성 데이터 유효성 검사 프로필 사용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 플랫폼 유효성 검사 중에 확인할 특정 BCD (부팅 구성 데이터) 설정을 선택할 수 있습니다.</p>
<p>이 정책 설정을 사용 하면 다른 설정을 추가 하거나 기본 설정을 제거 하거나 둘 다 제거할 수 있습니다. 이 정책 설정을 사용 하지 않으면 컴퓨터가 Windows 7에서 사용 하는 기본 BCD 프로필과 비슷한 BCD 프로필로 돌아갑니다. 이 정책 설정을 구성 하지 않으면 컴퓨터에서 기본 Windows BCD 설정을 확인 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>BitLocker에서 무결성 유효성 검사에 보안 부팅 허용 정책에 정의 된 대로 플랫폼 및 BCD (부팅 구성 데이터) 무결성 유효성 검사에 대 한 보안 부팅을 사용 하는 경우 &quot; &quot; 향상 된 &quot; 부팅 구성 데이터 유효성 검사 프로필 &quot; 정책 사용이 무시 됩니다.</p>
</div>
<div>

</div>
<p>부팅 디버깅 (0x16000010)을 제어 하는 설정은 항상 유효성을 검사 하며 제공 된 필드에 포함 된 경우 아무런 영향도 주지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>암호화 정책 적용 설정</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 사용 하 여 사용자가 운영 체제 드라이브에 대 한 MBAM 정책 준수를 연기할 수 있는 일 수를 구성 합니다. 유예 기간은 비규격으로 운영 체제를 처음 검색할 때 시작 됩니다. 이 유예 기간이 만료 된 후에는 사용자가 필요한 작업을 연기 하거나 예외를 요청할 수 없습니다.</p>
<p>암호화 프로세스에 사용자 입력이 필요한 경우 필요한 정보를 제공할 때까지 사용자가 닫을 수 없는 대화 상자가 나타납니다.</p>
<p>이 설정을 사용 하지 않거나 구성 하지 않으면 사용자가 MBAM 정책에 부합 하지 않습니다.</p>
<p>보호기를 추가 하기 위해 사용자 조작이 필요 하지 않은 경우, 유예 기간이 만료 된 후 백그라운드에서 암호화가 시작 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사전 부팅 복구 메시지 및 URL 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 사용 하 여 사용자 지정 복구 메시지를 구성 하거나 OS 드라이브가 잠길 때 사전 부팅 BitLocker 복구 화면에 표시 되는 URL을 지정 합니다. 이 설정은 Windows 10을 실행 하는 클라이언트 컴퓨터 에서만 사용할 수 있습니다.</p>
<p>이 정책을 사용 하는 경우 사전 부팅 복구 메시지에 대해 다음 옵션 중 하나를 선택할 수 있습니다.</p>
<ul>
<li><p><strong>사용자 지정 복구 메시지 사용 </strong> : 사전 부팅 BitLocker 복구 화면에 사용자 지정 메시지를 포함 하려면이 옵션을 선택 합니다. <strong>사용자 지정 복구 메시지 옵션 </strong> 상자에 표시할 메시지를 입력 합니다. 복구 URL도 지정 하려는 경우에는 사용자 지정 복구 메시지의 일부로 포함 합니다.</p></li>
<li><p><strong>사용자 지정 복구 URL 사용 </strong> : 사전 부팅 BitLocker 복구 화면에 표시 되는 기본 URL을 바꾸려면이 옵션을 선택 합니다. <strong>사용자 지정 복구 URL 옵션 </strong> 상자에 표시할 URL을 입력 합니다.</p></li>
<li><p><strong>기본 복구 메시지 및 URL 사용 </strong> : 사전 부팅 BitLocker 복구 화면에 기본 BitLocker 복구 메시지 및 url을 표시 하려면이 옵션을 선택 합니다. 이전에 사용자 지정 복구 메시지 또는 URL을 구성한 경우 기본 메시지로 돌아가려면이 정책을 사용 하도록 설정 하 고 <strong> 기본 복구 메시지 및 URL 사용 옵션을 선택 해야 합니다 </strong> .</p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>모든 문자 및 언어가 사전 부팅에서 지원 되는 것은 아닙니다. 사전 부팅 BitLocker 복구 화면에서 사용자 지정 메시지 또는 URL에 사용 하는 문자가 올바르게 표시 되는지 테스트 하는 것이 좋습니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### 이동식 드라이브 그룹 정책 정의

이 섹션에서는 다음 GPO 노드에서 Microsoft BitLocker 관리 및 모니터링을 위한 이동식 드라이브 그룹 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **이동식 드라이브**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 그룹 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이동식 드라이브에서 BitLocker 사용 제어</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책은 이동식 데이터 드라이브의 BitLocker 사용을 제어 합니다.</p>
<p>사용자가 이동식 데이터 <strong> </strong> 드라이브에서 bitlocker 설치 마법사를 실행할 수 있도록 이동식 데이터 드라이브에 bitlocker 보호 적용 허용을 클릭 합니다.</p>
<p>사용자가 <strong> 이동식 데이터 드라이브에서 bitlocker 드라이브 암호화를 제거 하거나 암호를 해독 하는 </strong> 동안 사용자가 암호화를 일시 중지할 수 있도록 허용을 클릭 합니다.</p>
<p>이 정책을 사용 하도록 설정 하 고 <strong> 사용자가 이동식 데이터 드라이브에서 BitLocker 보호를 적용 하도록 허용을 클릭 하면 </strong> , Mbam 클라이언트는 이동식 드라이브에 대 한 복구 정보를 mbam 키 복구 서버에 저장 하 고, 사용자가 암호를 분실 한 경우 드라이브를 복구할 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker에 의해 보호되지 않는 이동식 드라이브에 대한 쓰기 액세스 거부</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 BitLocker 보호 드라이브에 대 한 쓰기 권한만 허용 합니다.</p>
<p>이 정책을 사용 하는 경우 쓰기 권한을 허용 하기 전에 컴퓨터의 모든 이동식 데이터 드라이브에 암호화가 필요 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이전 버전의 Windows에서 BitLocker로 보호 된 이동식 드라이브에 대 한 액세스 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 고정 드라이브를 잠금 해제 하 고 볼 수 있도록 하려면이 정책을 사용 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 Windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템으로 포맷 된 이동식 드라이브를 잠금 해제 하 고 해당 콘텐츠를 볼 수 있습니다. 이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</p>
<p>정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 한 이동식 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이동식 데이터 드라이브에 대 한 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 이동식 데이터 드라이브에서 암호 보호를 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않은 경우 암호 복잡성 요구 사항이 포함 되지 않고 8 자만 필요로 하는 기본 설정으로 암호가 지원 됩니다.</p>
<p>보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 대해 암호 요구를 선택 하 고 </strong> , <strong> 암호 복잡도 필요를 클릭 하 </strong> 고, 기본 <strong> 최소 암호 길이를 설정 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 된 이동식 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>구성 되지 않음으로 설정 하는 경우 <strong> </strong> 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</p>
<p>MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>




## 관련 항목


[MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)

[MBAM 2.5 배포 필수 구성 요소](mbam-25-deployment-prerequisites.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.






