---
title: MBAM 2.0 그룹 정책 요구 사항 계획
description: MBAM 2.0 그룹 정책 요구 사항 계획
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812828"
---
# MBAM 2.0 그룹 정책 요구 사항 계획


MBAM (Microsoft BitLocker 관리 및 모니터링) 클라이언트 컴퓨터를 관리 하려면 조직에서 지원할 BitLocker 프로텍터 유형을 고려해 야 하며, 적용할 해당 그룹 정책 설정을 구성 해야 합니다. 이 항목에서는 Microsoft BitLocker 관리 및 모니터링을 사용 하 여 엔터프라이즈의 BitLocker 드라이브 암호화를 관리 하는 데 사용할 수 있는 그룹 정책 설정에 대해 설명 합니다.

MBAM은 운영 체제 드라이브에 대해 TPM (신뢰할 수 있는 플랫폼 모듈), TPM + PIN, TPM + USB 키, TPM + PIN + USB 키, 암호, 숫자 암호, 데이터 복구 에이전트의 BitLocker 보호기 유형을 지원 합니다. 암호 보호기는 Windows To Go 장치 및 TPM이 없는 Windows 8 장치에만 지원 됩니다. MBAM은 운영 체제 볼륨이 MBAM이 설치 되기 전에 암호화 된 경우에만 TPM + USB 키 및 TPM + PIN + USB 키 보호기를 지원 합니다.

MBAM은 고정 데이터 드라이브에 대 한 다음과 같은 유형의 BitLocker 보호기 인 암호, 자동 잠금 해제, 숫자 암호, 데이터 복구 에이전트를 지원 합니다.

숫자 암호 보호기는 볼륨 암호화의 일부로 자동 적용 되며 구성할 필요가 없습니다.

**중요**  
기본 Windows BitLocker 드라이브 암호화 GPO (그룹 정책 개체) 설정은 MBAM에서 사용 되지 않으며 사용 하도록 설정 된 경우 충돌 하는 동작이 발생할 수 있습니다. MBAM이 BitLocker를 관리 하도록 설정 하려면 mbam 그룹 정책 템플릿을 설치한 후에만 MBAM 그룹 정책 설정을 정의 해야 합니다.



향상 된 시작 Pin에는 대 문자와 소문자, 숫자 등의 문자를 포함할 수 있습니다. BitLocker와 달리 MBAM은 향상 된 Pin에 대 한 기호 및 공백 사용을 지원 하지 않습니다.

GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) MDOP 기술을 실행할 수 있는 컴퓨터에 MBAM 그룹 정책 템플릿을 설치 합니다. Mbam 기능을 사용 하도록 설정 하는 GPO 설정을 편집 하려면 먼저 mbam 그룹 정책 템플릿을 설치 하 고 GPMC 또는 AGPM을 열고 해당 gpo를 편집한 후 다음 GPO 노드로 이동 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker 관리).**

MDOP (BitLocker 관리) GPO 노드에는 4 개의 글로벌 정책 설정과 클라이언트 관리, 고정 드라이브, 운영 체제 드라이브, 이동식 드라이브의 네 가지 하위 GPO 설정 노드가 있습니다. 다음 섹션에서는 MBAM GPO 정책 설정 요구 사항에 대 한 계획을 수립할 수 있도록 정책 정의 및 제안 된 정책 설정을 제공 합니다.

**참고**  
MBAM이 BitLocker 암호화를 관리 하도록 설정 하는 데 권장 되는 최소 GPO 설정을 구성 하는 방법에 대 한 자세한 내용은 [mbam 2.0 GPO 설정을 편집 하는 방법을](how-to-edit-mbam-20-gpo-settings-mbam-2.md)참조 하세요.



## 전역 정책 정의


이 섹션에서는 다음과 같은 GPO 노드에서 볼 수 있는 mbam 글로벌 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker 관리)**.

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


이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 클라이언트 관리 정책 정의 ( **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)** \\ **클라이언트 관리**)에 대해 설명 합니다.

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
<li><p><strong>MBAM 복구 및 하드웨어 서비스 끝점 </strong> 입니다. 이 설정을 사용 하 여 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 설정 합니다. 다음 예제와 유사한 끝점 위치를 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스를/MBAMRecoveryAndHardwareService/CoreService.svc에 연결 &gt; </em><strong> </strong> 하는 포트입니다.</p></li>
<li><p><strong>저장할 BitLocker 복구 정보를 선택 </strong> 합니다. 이 정책 설정을 통해 BitLocker 복구 정보를 백업 하도록 키 복구 서비스를 구성할 수 있습니다. 또한 준수 및 감사 보고서를 수집 하는 상태 보고 서비스도 구성할 수 있습니다. 이 정책은 키 정보가 부족 하 여 데이터 손실을 방지 하기 위해 BitLocker에서 암호화 한 데이터를 복구 하는 관리 방법을 제공 합니다. 상태 보고서 및 키 복구 작업이 구성 된 보고서 서버 위치에 자동으로 전송 됩니다.</p>
<p>이 정책 설정을 구성 하지 않거나 사용 하지 않도록 설정 하면 키 복구 정보가 저장 되지 않으며 상태 보고서 및 키 복구 작업이 서버에 보고 되지 않습니다. 이 설정이 <strong> 복구 암호 및 키 패키지로 설정 되어 있으면 </strong> 복구 암호와 키 패키지가 자동으로 구성 된 키 복구 서버 위치에 백업 됩니다.</p></li>
<li><p><strong>클라이언트 검사 상태 빈도를 분 단위로 입력 </strong> 합니다. 이 정책 설정은 클라이언트가 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하는 빈도를 관리 합니다. 또한이 정책은 클라이언트 준수 상태가 서버에 저장 되는 빈도를 관리 합니다. 클라이언트는 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하 고 구성 된 빈도로 클라이언트 복구 키를 백업 합니다.</p>
<p>회사에서 설정한 요구 사항에 따라 컴퓨터의 준수 상태를 확인 하는 빈도 및 클라이언트 복구 키를 백업 하는 빈도를 기준으로이 빈도를 설정 합니다.</p></li>
<li><p><strong>MBAM 상태 보고 서비스 끝점 </strong> 입니다. 이 설정을 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 구성 해야 합니다. 다음 예제와 유사한 끝점 위치를 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스를/MBAMComplianceStatusService/StatusReportingService.svc에 연결 &gt; </em><strong> </strong> 하는 포트입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 예외 정책 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 사용자에 게 BitLocker 암호화 예외를 요청 하도록 지시할 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 구성할 수 있습니다.</p>
<p>이 정책 설정을 사용 하 고 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 제공 하면 사용자에 게 BitLocker 보호에서 예외를 적용 하는 방법에 대 한 지침을 제공 하는 대화 상자가 표시 됩니다. 사용자의 BitLocker 암호화 예외를 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> 사용자 Bitlocker 암호화 예외를 관리 하는 방법을 참조 하세요 </a> .</p>
<p>이 정책 설정을 사용 하지 않거나 구성 하지 않으면 예외 요청 지침이 사용자에 게 표시 되지 않습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>사용자 예외는 컴퓨터당만 관리 됩니다. 여러 사용자가 같은 컴퓨터에 로그온 하 고 한 사용자가 제외 되지 않은 경우 컴퓨터는 암호화 됩니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 환경 개선 프로그램 구성</p></td>
<td align="left"><p>이 정책 설정을 사용 하면 사용자 환경 개선 프로그램에 MBAM이 참여할 수 있는 기간을 구성할 수 있습니다. 이 프로그램은 컴퓨터 하드웨어와 사용자가 작업을 중단 하지 않고 MBAM을 사용 하는 방법에 대 한 정보를 수집 합니다. 이 정보는 Microsoft가 향상 시킬 MBAM 기능을 식별 하는 데 도움이 됩니다. Microsoft는이 정보를 사용 하 여 MBAM 사용자를 식별 하거나 연락 하지 않습니다.</p>
<p>이 정책 설정을 사용 하도록 설정 하면 사용자가 고객 환경 개선 프로그램에 참가할 수 있습니다.</p>
<p>이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자가 고객 환경 개선 프로그램에 참여할 수 없게 됩니다.</p>
<p>이 정책 설정을 구성 하지 않으면 사용자 환경 개선 프로그램에 참가할 수 있는 옵션이 제공 됩니다.</p></td>
</tr>
</tbody>
</table>



## 고정 드라이브 정책 정의


이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 고정 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 서식 파일** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)** \\ **고정 드라이브**.

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
<td align="left"><p>권장 구성: <strong> 사용</strong></p>
<p>이 정책 설정을 통해 고정 드라이브를 암호화 해야 하는지 여부를 관리할 수 있습니다.</p>
<p>운영 체제 볼륨을 암호화 해야 하는 경우에는 <strong> 고정 데이터 드라이브 자동 잠금 해제 옵션을 선택 </strong> 합니다.</p>
<p>이 정책을 사용 하는 경우 <strong> </strong> 고정 데이터 드라이브에 대 한 자동 잠금 해제를 허용 하거나 요구 하지 않는 한 고정 데이터 드라이브에 대 한 암호 사용 구성 정책을 사용 하지 않도록 설정 해야 합니다.</p>
<p>고정 데이터 드라이브에 대 한 자동 잠금 해제를 사용 해야 하는 경우 운영 체제 볼륨을 암호화 하도록 구성 해야 합니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 모든 고정 드라이브를 BitLocker 보호에 포함 해야 하며, 드라이브가 암호화 됩니다.</p>
<p>이 정책 설정을 구성 하지 않으면 사용자가 BitLocker 보호에 고정 드라이브를 추가할 필요가 없습니다. 고정 데이터 드라이브가 암호화 된 후이 정책을 적용 하면 MBAM 에이전트는 암호화 된 고정 드라이브의 암호를 해독 합니다.</p>
<p>이 정책 설정을 사용 하지 않으면 사용자가 고정 된 데이터 드라이브를 BitLocker 보호에 저장할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker에 의해 보호되지 않는 고정 드라이브에 대한 쓰기 액세스 거부</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정은 컴퓨터에서 고정 드라이브를 쓰기 가능 하 게 하기 위해 BitLocker 보호가 필요한 지 여부를 결정 합니다. 이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</p>
<p>정책이 구성 되어 있지 않으면 컴퓨터의 모든 고정 데이터 드라이브가 읽기 및 쓰기 액세스 권한으로 탑재 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이전 버전의 Windows에서 BitLocker로 보호 되는 고정 드라이브에 대 한 액세스 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 고정 드라이브를 잠금 해제 하 고 볼 수 있도록 하려면이 정책을 사용 합니다.</p>
<p>정책을 사용 하거나 구성 하지 않으면 FAT 파일 시스템으로 포맷 한 고정 드라이브는 잠금을 해제할 수 있으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 있습니다. 이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</p>
<p>정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 된 고정 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>고정 드라이브의 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 BitLocker로 보호 된 고정 데이터 드라이브의 잠금을 해제 하는 데 암호가 필요한 지 여부를 지정 합니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 정의한 요구 사항에 맞는 암호를 구성할 수 있습니다. BitLocker는 사용자가 드라이브에서 사용할 수 있는 모든 보호기를 사용 하 여 드라이브 잠금을 해제할 수 있도록 합니다.</p>
<p>이러한 설정은 볼륨을 잠금 해제 하는 경우를 제외 하 고는 BitLocker를 켤 때 적용 됩니다.</p>
<p>이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</p>
<p>정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</p>
<p>보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 고정 데이터 드라이브에 대해 암호 필요를 선택 하 고 </strong> , <strong> 암호 복잡도 필요를 선택 하 </strong> 고, 원하는 <strong> 최소 암호 길이를 설정 </strong> 합니다.</p>
<p>이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</p>
<p>이 정책 설정을 구성 하지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 되는 고정 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>정책이 구성 되어 있지 않으면 BitLocker 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다. MBAM에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 운영 체제 드라이브 정책 정의


이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 운영 체제 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)** \\ **운영 체제 드라이브**.

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
<p>이 정책 설정을 통해 운영 체제 드라이브를 암호화 해야 하는지 여부를 관리할 수 있습니다.</p>
<p>보안을 강화 하려면 <strong> </strong> TPM + PIN 보호기를 사용 하는 경우 시스템/전원 관리/절전 모드 설정에서 다음 정책 설정을 사용 하지 않도록 설정 하는 것이 좋습니다.</p>
<ul>
<li><p>절전 모드에서 대기 상태 (S1-S3) 허용 (전원 사용)</p></li>
<li><p>절전 모드 시 대기 상태 (S1-S3) 허용 (배터리 사용)</p></li>
</ul>
<p>Microsoft Windows 8 이상을 실행 중이 고 TPM이 없는 컴퓨터에서 BitLocker를 사용 하려는 경우 <strong> 호환 되는 tpm이 없는 bitlocker 허용 확인란을 선택 </strong> 합니다. 이 모드에서는 시작 하는 데 암호가 필요 합니다. 암호를 잊어버린 경우 BitLocker 복구 옵션 중 하나를 사용 하 여 드라이브에 액세스 해야 합니다.</p>
<p>호환 되는 TPM이 있는 컴퓨터에서는 시작 시 암호화 된 데이터에 대 한 추가 보호를 제공 하기 위해 두 가지 유형의 인증 방법을 사용할 수 있습니다. 컴퓨터가 시작 되 면 인증에 TPM만 사용 하거나 PIN (개인 식별 번호)을 입력 해야 할 수도 있습니다.</p>
<p>이 정책 설정을 사용 하면 사용자가 BitLocker protection에서 운영 체제 드라이브를 설치 하 고 드라이브가 암호화 됩니다.</p>
<p>이 정책을 사용 하지 않도록 설정 하는 경우, 사용자는 운영 체제 드라이브를 BitLocker 보호 하에 둘 수 없습니다. 운영 체제 드라이브가 암호화 된 후이 정책을 적용 하면 드라이브의 암호가 해독 됩니다.</p>
<p>이 정책을 구성 하지 않으면, 운영 체제 드라이브를 BitLocker 보호 아래에 배치할 필요가 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TPM 플랫폼 유효성 검사 프로필 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책 설정을 통해 컴퓨터의 TPM 보안 하드웨어가 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다. 컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</p>
<p>이 정책 설정이 구성 되어 있지 않으면 TPM은 기본 플랫폼 유효성 검사 프로필 또는 설정 스크립트에 지정 된 플랫폼 유효성 검사 프로필을 사용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 되는 운영 체제 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>이 정책이 구성 되어 있지 않으면 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</p>
<p>MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 이동식 드라이브 정책 정의


이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 이동식 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)**  \\  **이동식 드라이브**.

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
<p>사용자가 이동식 데이터 드라이브에서 bitlocker <strong> 보호 기능을 적용할 수 있도록 허용 옵션을 사용 하도록 설정 </strong> 하 여 사용자가 이동식 데이터 드라이브에서 bitlocker 설치 마법사를 실행할 수 있도록 합니다.</p>
<p>사용자가 <strong> 드라이브에서 bitlocker 드라이브 암호화를 제거 하거나 암호를 해독 하도록 허용 옵션을 사용 하도록 설정 하 여 </strong> 유지 관리 작업을 수행 하는 동안 암호화를 일시 중단 하거나, 암호를 복구할 수 있습니다.</p>
<p>이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 BitLocker 보호 적용 허용 옵션을 </strong> 선택 하면 Mbam 클라이언트는 이동식 드라이브에 대 한 복구 정보를 mbam 키 복구 서버에 저장 하 고 사용자가 암호를 잃어버린 경우 드라이브를 복구할 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker에 의해 보호되지 않는 이동식 드라이브에 대한 쓰기 액세스 거부</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 BitLocker 보호 드라이브에 대 한 쓰기 권한만 허용 합니다.</p>
<p>이 정책을 사용 하는 경우 쓰기 액세스를 허용 하기 전에 컴퓨터의 모든 이동식 데이터 드라이브에 암호화가 필요 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이전 버전의 Windows에서 BitLocker로 보호 된 이동식 드라이브에 대 한 액세스 허용</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 고정 드라이브를 잠금 해제 하 고 볼 수 있도록 하려면이 정책을 사용 합니다.</p>
<p>이 정책이 구성 되어 있지 않은 경우, windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템으로 포맷 된 이동식 데이터 드라이브의 잠금을 해제 하 고 해당 콘텐츠를 볼 수 있습니다. 이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</p>
<p>정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 한 이동식 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이동식 데이터 드라이브에 대 한 암호 사용 구성</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>이 정책을 사용 하 여 이동식 데이터 드라이브에서 암호 보호를 구성 합니다.</p>
<p>이 정책이 구성 되어 있지 않은 경우 암호 복잡성 요구 사항이 포함 되지 않고 8 자만 필요로 하는 기본 설정으로 암호가 지원 됩니다.</p>
<p>보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 대 한 암호 필요 </strong> 를 선택 하 고, <strong> 암호 복잡도 필요 </strong> , 기본 <strong> 최소 암호 길이를 설정 해야 </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker로 보호 된 이동식 드라이브를 복구할 수 있는 방법 선택</p></td>
<td align="left"><p>권장 구성: <strong> 구성 되지 않음</strong></p>
<p>BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</p>
<p>구성 되지 않음으로 설정 하는 경우 <strong> </strong> 데이터 복구 에이전트는 허용 되 고 복구 정보는 AD DS에 백업 되지 않습니다.</p>
<p>MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MBAM 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md)









