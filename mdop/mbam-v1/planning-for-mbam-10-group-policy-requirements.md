---
title: MBAM 1.0 그룹 정책 요구 사항 계획
description: MBAM 1.0 그룹 정책 요구 사항 계획
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812436"
---
# MBAM 1.0 그룹 정책 요구 사항 계획


Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트 관리에서 사용자 지정 그룹 정책 설정을 적용 해야 합니다. 이 항목에서는 MBAM을 사용 하 여 엔터프라이즈의 BitLocker 드라이브 암호화를 관리 하는 경우 GPO (그룹 정책 개체)에 사용할 수 있는 정책 옵션에 대해 설명 합니다.

**중요**  
MBAM은 Windows BitLocker 드라이브 암호화에 대 한 기본 GPO 설정을 사용 하지 않습니다. 기본 설정을 사용 하도록 설정 하면 충돌 하는 동작이 발생할 수 있습니다. MBAM이 BitLocker를 관리 하도록 설정 하려면 MBAM 그룹 정책 템플릿을 설치한 후 GPO 정책 설정을 정의 해야 합니다.



MBAM 그룹 정책 템플릿을 설치한 후에는 MBAM에서 엔터프라이즈 BitLocker 암호화를 관리 하는 데 사용 가능한 사용자 지정 MBAM GPO 정책 설정을 보고 수정할 수 있습니다. MBAM 그룹 정책 템플릿은 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) MDOP 기술을 실행할 수 있는 컴퓨터에 설치 해야 합니다. 다음으로 해당 GPO를 편집 하려면 GPMC 또는 AGPM을 열고 다음 GPO 노드로 이동 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP (BitLocker 관리)**.

MDOP (BitLocker Management) GPO 노드에는 각각 4 개의 전역 정책 설정과 네 개의 자식 GPO 설정 노드가 있습니다. 4 개의 GPO 전역 정책 설정은 클라이언트 관리, 고정 드라이브, 운영 체제 드라이브 및 이동식 드라이브입니다. 다음 섹션에서는 MBAM GPO 정책 설정 요구 사항을 계획 하는 데 도움이 되는 정책 정의 및 제안 된 정책 설정을 제공 합니다.

**참고**  
MBAM이 BitLocker 암호화를 관리 하도록 허용 하도록 최소 추천 GPO 설정을 구성 하는 방법에 대 한 자세한 내용은 [mbam 1.0 GPO 설정을 편집 하는 방법을](how-to-edit-mbam-10-gpo-settings.md)참조 하세요.



## 전역 정책 정의


이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 mbam 전역 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>드라이브 암호화 방법 및 암호화 수준 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>특정 암호화 방법 및 암호화 강도를 사용 하도록이 정책을 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면, BitLocker는 AES 128 비트의 기본 암호화 방법으로 디퓨저 또는 설정 스크립트에 의해 지정 된 암호화 방법을 사용 합니다.</p></td>
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
<p>회사에서 더 높은 수준의 보안을 요구 하는 경우 id 필드를 구성 하 여 <strong> </strong> 모든 USB 장치에이 필드 집합을 포함 하 고이 그룹 정책 설정에 맞출지 여부를 확인할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



## 클라이언트 관리 정책 정의


이 섹션에서는 다음 GPO 노드에서 볼 수 있는 mbam 클라이언트 관리 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mblaam (BitLocker Management)**  \\  **클라이언트 관리**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 서비스 구성</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<ul>
<li><p><strong>MBAM 복구 및 하드웨어 서비스 끝점 </strong> 입니다. 이는 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 구성 해야 하는 첫 번째 정책 설정입니다. 이 설정에 대 한 끝점 위치를 다음 예제와 같이 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가/MBAMRecoveryAndHardwareService/CoreService.svc에 바인딩된 포트입니다 &gt; </em><strong> </strong> .</p></li>
<li><p><strong>저장할 BitLocker 복구 정보를 선택 </strong> 합니다. 이 정책 설정을 통해 BitLocker 복구 정보를 백업 하도록 키 복구 서비스를 구성할 수 있습니다. 또한 준수 및 감사 보고서를 수집 하는 상태 보고 서비스도 구성할 수 있습니다. 이 정책은 키 정보가 부족 하 여 데이터 손실을 방지 하기 위해 BitLocker에서 암호화 한 데이터를 복구 하는 관리 방법을 제공 합니다. 상태 보고서 및 키 복구 작업이 구성 된 보고서 서버 위치에 자동으로 전송 됩니다.</p>
<p>이 정책 설정을 구성 하지 않거나 사용 하지 않도록 설정 하면 키 복구 정보가 저장 되지 않으며 상태 보고서 및 키 복구 작업이 서버에 보고 되지 않습니다. 이 설정이 <strong> 복구 암호 및 키 패키지로 설정 되어 있으면 </strong> 복구 암호와 키 패키지가 자동으로 구성 된 키 복구 서버 위치에 백업 됩니다.</p></li>
<li><p><strong>클라이언트 검사 상태 빈도 (분)를 입력 합니다 </strong> . 이 정책 설정은 클라이언트가 BitLocker 보호 정책 및 클라이언트 컴퓨터의 상태를 확인 하는 빈도를 관리 합니다. 또한이 정책은 클라이언트 준수 상태가 서버에 저장 되는 빈도를 관리 합니다. 클라이언트는 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하 고 구성 된 주파수에서 클라이언트 복구 키를 백업 하기도 합니다.</p>
<p>컴퓨터의 준수 상태를 확인 하는 빈도 및 클라이언트 복구 키를 백업 하는 빈도에 따라 회사에서 설정한 요구 사항을 기반으로이 빈도를 설정 합니다.</p></li>
<li><p><strong>MBAM 상태 보고 서비스 끝점 </strong> 입니다. 이는 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 구성 해야 하는 두 번째 정책 설정입니다. 이 설정에 대해 다음 예제를 사용 하 여 끝점 위치를 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가 &gt; /MBAMComplianceStatusService/StatusReportingService.에 바인딩된 포트 </em><strong> svc </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>하드웨어 호환성 검사 허용</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 사용 하면 MBAM 클라이언트 컴퓨터의 드라이브에서 BitLocker 보호 기능을 사용 하도록 설정 하기 전에 하드웨어 호환성 확인을 관리할 수 있습니다.</p>
<p>엔터프라이즈에 TPM (신뢰할 수 있는 플랫폼 모듈)을 지원 하지 않는 이전 컴퓨터 하드웨어 또는 컴퓨터가 있는 경우이 정책 옵션을 사용 하도록 설정 해야 합니다. 이러한 조건 중 하나라도 참이 면 하드웨어 호환성 확인을 사용 하 여 MBAM이 BitLocker를 지 원하는 컴퓨터 모델에만 적용 되도록 합니다. 조직의 모든 컴퓨터에서 BitLocker를 지 원하는 경우 하드웨어 호환성을 배포할 필요가 없으며이 정책을 <strong> 구성 되지 않도록 설정할 수 있습니다 </strong> .</p>
<p>이 정책 설정을 사용 하면 컴퓨터 드라이브에서 BitLocker 보호 기능을 사용 하도록 설정 하기 전에 하드웨어 호환성 목록에 대해 모든 24 시간에 대 한 작업의 모델이 확인 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 정책 설정을 사용 하기 전에 <strong> </strong> <strong> mbam 서비스 구성 옵션에서 mbam 복구 및 하드웨어 서비스 끝점 설정을 구성 했는지 확인 </strong> 합니다.</p>
</div>
<div>

</div>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 하드웨어 호환성 목록에 대해 컴퓨터 모델의 유효성을 검사 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 예외 정책 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 사용자에 게 BitLocker 암호화 예외를 요청 하도록 지시할 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 구성할 수 있습니다.</p>
<p>이 정책 설정을 사용 하 고 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 제공 하는 경우, 사용자에 게 BitLocker 보호에서 예외를 적용 하는 방법에 대 한 지침이 포함 된 대화 상자가 표시 됩니다. 사용자에 대 한 BitLocker 암호화 예외를 사용 하는 방법에 대 한 자세한 내용은 <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> 사용자 Bitlocker 암호화 예외를 관리 하는 방법을 참조 하세요 </a> .</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 예외 요청에 대해 적용 하는 방법에 대 한 지침이 사용자에 게 표시 되지 않습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>사용자 예외는 컴퓨터당만 관리 됩니다. 여러 사용자가 같은 컴퓨터에 로그온 하 고 한 사용자가 제외 되지 않은 경우 컴퓨터는 암호화 됩니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## 고정 드라이브 정책 정의


이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 mbam에 대 한 고정 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)**  \\  **고정 드라이브**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>고정 데이터 드라이브 암호화 설정</p></td>
<td align="left"><p>권장 구성: <strong> 사용 하도록 설정한 상태 </strong> 에서 <strong> 운영 체제 볼륨을 암호화 해야 하는 경우 자동으로 고정 데이터 드라이브 사용 확인란을 선택 </strong> 합니다.</p>
<p>이 정책 설정을 통해 고정 드라이브를 암호화할지 여부를 관리할 수 있습니다.</p>
<p>이 정책을 사용 하도록 설정 하는 경우 <strong> 고정 데이터 드라이브에 대 한 암호 사용 구성 정책을 사용 하지 않도록 설정 하지 마세요 </strong> .</p>
<p><strong>고정 데이터 드라이브 자동 잠금 해제 </strong> 확인란이 선택 되어 있으면 운영 체제 볼륨을 암호화 해야 합니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 모든 고정 드라이브를 BitLocker 보호 아래에 설치 하 여 드라이브를 암호화 해야 합니다.</p>
<p>이 정책을 구성 하지 않거나이 정책을 사용 하지 않도록 설정 하는 경우 사용자는 BitLocker 보호에 고정 드라이브를 추가할 필요가 없습니다.</p>
<p>이 정책을 사용 하지 않도록 설정 하는 경우 MBAM 에이전트는 암호화 된 모든 고정 드라이브를 해독 합니다.</p>
<p>운영 체제 볼륨을 암호화 하는 것이 필요 하지 않은 경우에는 <strong> 고정 데이터 드라이브 자동 잠금 해제 확인란의 선택을 취소 </strong> 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker로 보호 되지 않는 고정 드라이브에 대 한 "쓰기" 권한 거부</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정은 컴퓨터의 고정 드라이브에 대해 BitLocker 보호가 필요한 지 여부를 결정 하 여 쓸 수 있도록 합니다. 이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</p>
<p>정책이 구성 되어 있지 않으면 컴퓨터의 모든 고정 드라이브가 읽기/쓰기 권한으로 탑재 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이전 버전의 Windows에서 BitLocker로 보호 되는 고정 드라이브에 대 한 액세스 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 Windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT (파일 할당 테이블) 파일 시스템으로 포맷 된 고정 드라이브를 잠금 해제 하 고 볼 수 있습니다.</p>
<p>이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</p>
<p>정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 된 고정 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>고정 드라이브의 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 고정 드라이브의 암호 보호를 구성 합니다.</p>
<p>정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 사항을 포함 하지 않고 8 자만 요구 하는 기본 설정으로 암호가 지원 됩니다.</p>
<p>보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 고정 데이터 드라이브에 대해 암호 필요를 선택 하 고 </strong> , <strong> 암호 복잡도 필요를 선택 하 </strong> 고, 원하는 <strong> 최소 암호 길이를 설정 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 되는 고정 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 BitLocker 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다. MBAM에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 운영 체제 드라이브 정책 정의


이 섹션에서는 **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP \ am (BitLocker Management)**  \\  **운영 체제 드라이브**에 있는 mbam의 운영 체제 드라이브 정책 정의에 대해 설명 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>운영 체제 드라이브 암호화 설정</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정은 운영 체제 드라이브를 암호화할지 여부를 결정 합니다.</p>
<p>이 정책을 구성 하 여 다음을 수행 합니다.</p>
<ul>
<li><p>운영 체제 드라이브에 대해 BitLocker 보호를 적용 합니다.</p></li>
<li><p>운영 체제 보호를 위해 TPM (신뢰할 수 있는 플랫폼 모듈) 핀을 사용 하도록 PIN 사용을 구성 합니다.</p></li>
<li><p>대 문자와 소문자, 숫자 등의 문자를 허용 하는 향상 된 시작 Pin을 구성 합니다. MBAM은 기호 및 공백을 지원 하기에도 불구 하 고 향상 된 Pin에 대 한 기호 및 공백의 사용을 지원 하지 않습니다.</p></li>
</ul>
<p>이 정책 설정을 사용 하도록 설정 하는 경우 사용자는 BitLocker를 사용 하 여 운영 체제 드라이브를 보호 해야 합니다.</p>
<p>구성 하지 않거나 설정을 사용 하지 않도록 설정한 경우 사용자는 BitLocker를 사용 하 여 운영 체제 드라이브의 보안을 유지할 필요가 없습니다.</p>
<p>이 정책을 사용 하지 않도록 설정 하면, MBAM 에이전트는 운영 체제 볼륨을 암호화 된 상태로 해독 합니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 BitLocker 보호를 사용 하 여 운영 체제를 보호 하 고 드라이브가 암호화 됩니다. 암호화 요구 사항에 따라 운영 체제 드라이브에 대 한 보호 방법을 선택할 수 있습니다.</p>
<p>보안 요구 사항이 더 높은 경우 TPM + PIN을 사용 하 고, 향상 된 Pin을 허용 하 고, 최소 PIN 길이를 8 자로 설정 합니다.</p>
<p>TPM + PIN 보호기를 사용 하 여이 정책을 사용 하는 경우 <strong> 시스템 </strong>  /  <strong> 전원 관리 </strong>  /  <strong> 절전 모드 설정 </strong> 에서 다음 정책을 사용 하지 않도록 설정할 수 있습니다.</p>
<ul>
<li><p>절전 모드에서 대기 상태 (S1-S3) 허용 (전원 사용)</p></li>
<li><p>절전 모드 시 대기 상태 (S1-S3) 허용 (배터리 사용)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>TPM 플랫폼 유효성 검사 프로필 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 컴퓨터의 TPM 보안 하드웨어가 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다. 컴퓨터에 호환 되는 TPM이 없거나 BitLocker에 이미 TPM 보호가 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</p>
<p>이 정책이 구성 되지 않은 경우 TPM은 기본 플랫폼 유효성 검사 프로필 또는 설정 스크립트에 지정 된 플랫폼 유효성 검사 프로필을 사용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 되는 운영 체제 드라이브를 복구 하는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</p>
<p>MBAM 작업에서는 복구 정보를 AD DS에 백업할 필요가 없습니다.</p></td>
</tr>
</tbody>
</table>



## 이동식 드라이브 정책 정의


이 섹션에서는 다음 GPO 노드에서 볼 수 있는 mbam의 이동식 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mblaam (BitLocker Management)**  \\  **이동식 드라이브**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책 이름</th>
<th align="left">개요 및 제안 된 정책 설정</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이동식 드라이브에서 BitLocker 사용 제어</p></td>
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책은 이동식 데이터 드라이브의 BitLocker 사용을 제어 합니다.</p>
<p>사용자가 이동식 데이터 드라이브에서 <strong> bitlocker 설치 마법사를 실행할 수 있도록 허용 하기 위해 사용자에 게 bitlocker 보호를 적용할 수 있음 옵션을 사용 하도록 설정 </strong> 합니다.</p>
<p>사용자가 <strong> 드라이브에서 bitlocker 드라이브 암호화를 제거 하거나 암호를 해독 하도록 허용 옵션을 사용 하도록 설정 하 여 </strong> 유지 관리 작업을 수행 하는 동안 암호화를 일시 중단 하거나, 암호를 복구할 수 있습니다.</p>
<p>이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 BitLocker 보호 적용 허용 옵션을 </strong> 선택 하면 Mbam 클라이언트는 이동식 드라이브에 대 한 복구 정보를 mbam 키 복구 서버에 저장 하 고, 사용자가 암호를 분실 한 경우 드라이브를 복구할 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker로 보호 되지 않는 이동식 드라이브에 대 한 "쓰기" 사용 권한 거부</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 BitLocker 보호 드라이브에 대 한 쓰기 전용 권한을 허용 합니다.</p>
<p>이 정책을 사용 하는 경우 쓰기 권한을 허용 하기 전에 컴퓨터의 모든 이동식 데이터 드라이브에 암호화가 필요 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이전 버전의 Windows에서 BitLocker로 보호 된 이동식 드라이브에 대 한 액세스 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 Windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 (FAT) 파일 시스템으로 포맷 된 고정 드라이브를 잠금 해제 하 고 볼 수 있습니다.</p>
<p>이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</p>
<p>정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 한 이동식 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이동식 데이터 드라이브에 대 한 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 이동식 데이터 드라이브에서 암호 보호를 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 조건을 포함 하지 않고 8 자만 요구 하는 기본 설정으로 암호가 지원 됩니다.</p>
<p>보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 대해 암호 필요를 선택 하 고 </strong> , <strong> 암호 복잡도 필요 </strong> 를 선택한 다음, 기본 사용 <strong> 최소 암호 길이를 설정 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 된 이동식 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록 설정 하거나 BitLocker 복구 정보를 AD DS (Active Directory 도메인 서비스)에 저장 하도록이 정책을 구성할 수 있습니다.</p>
<p>정책이 <strong> 구성 되지 않음으로 설정 되 면 </strong> 데이터 복구 에이전트는 허용 되 고 복구 정보는 AD DS에 백업 되지 않습니다.</p>
<p>MBAM 작업에서는 복구 정보를 AD DS에 백업할 필요가 없습니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MBAM 1.0용 환경 준비](preparing-your-environment-for-mbam-10.md)









