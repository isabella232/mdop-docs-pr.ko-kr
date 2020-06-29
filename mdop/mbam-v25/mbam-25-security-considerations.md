---
title: MBAM 2.5 보안 고려 사항
description: MBAM 2.5 보안 고려 사항
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826838"
---
# MBAM 2.5 보안 고려 사항


이 항목에는 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 보호 하는 방법에 대 한 다음 정보가 포함 되어 있습니다.

-   [TPM을 에스크로 하기 위해 MBAM 구성 및 스토어 소유자 인증 암호](#bkmk-tpm)

-   [잠금 후 자동으로 TPM 잠금을 해제 하도록 MBAM 구성](#bkmk-autounlock)

-   [SQL Server에 대 한 보안 연결](#bkmk-secure-databases)

-   [계정 및 그룹 만들기](#bkmk-accts-groups)

-   [MBAM 로그 파일 사용](#bkmk-logfiles)

-   [MBAM 데이터베이스 TDE 고려 사항 검토](#bkmk-tde)

-   [일반 보안 고려 사항 이해](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a>TPM을 에스크로 하기 위해 MBAM 구성 및 스토어 소유자 인증 암호

**참고** Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다. 또한 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다. 자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.

구성에 따라 TPM (신뢰할 수 있는 플랫폼 모듈)은 잘못 된 암호를 너무 많이 입력 하 여 일정 기간 동안 잠금 상태로 유지 되는 경우와 같은 특정 상황에서 함에 의해 자동으로 잠깁니다. TPM 잠금을 사용 하는 동안 BitLocker는 사용자가 운영 체제 드라이브에 액세스 하기 위해 BitLocker 복구 키를 입력 하도록 요구 하는 잠금 해제 또는 암호 해독 작업을 수행 하기 위해 암호화 키에 액세스할 수 없습니다. TPM 잠금을 다시 설정 하려면 TPM 소유자 인증 암호를 제공 해야 합니다.

MBAM이 TPM을 소유 하거나 암호가 escrows 경우 MBAM 데이터베이스에 TPM 소유자 인증 암호를 저장할 수 있습니다. 그런 다음, TPM 잠금에서 복구 해야 하는 경우 관리 및 모니터링 웹 사이트에서 잠금이 자체적으로 확인 될 때까지 대기 해야 하는 경우에 대 한 접근성 암호를 쉽게 액세스할 수 있습니다.

### Windows 8 이상에서 Escrowing TPM 소유자 인증

**참고** Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다. Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다. 자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.

Windows 8 이상에서 로컬 컴퓨터에서 소유자 인증을 사용할 수 있는 경우에는 MBAM가 소유자 인증 암호를 저장할 수 있도록 TPM을 소유 하 고 있지 않아야 합니다.

MBAM을 에스크로으로 설정한 다음 TPM 소유자 인증 암호를 저장 하려면 이러한 그룹 정책 설정을 구성 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 정책 설정</th>
<th align="left">구성</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Active Directory 도메인 서비스에 대 한 TPM 백업 설정</p></td>
<td align="left"><p>사용 안 함 또는 구성 되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제에서 사용할 수 있는 TPM 소유자 권한 부여 정보 수준 구성</p></td>
<td align="left"><p>대리인/없음 또는 구성 되지 않음</p></td>
</tr>
</tbody>
</table>

 

이러한 그룹 정책 설정의 위치는 **컴퓨터 구성** &gt; **관리 템플릿** &gt; **시스템** 의 &gt; **신뢰할 수 있는 플랫폼 모듈 서비스**입니다.

**참고**  Windows는 MBAM이이 설정으로 성공적으로 escrows 후 소유자 인증을 로컬로 제거 합니다.

 

### Windows 7의 Escrowing TPM 소유자 인증

Windows 7에서 MBAM은 MBAM 데이터베이스에서 자동으로 TPM 소유자 인증 정보를 받아야 하는 TPM을 소유 하 고 있어야 합니다. MBAM이 TPM을 소유 하 고 있지 않은 경우 AD (Active Directory) 데이터 가져오기 cmdlet을 사용 하 여 Active Directory에서 MBAM 데이터베이스로 TPM 소유자 인증을 복사 해야 합니다.

### MBAM Active Directory 데이터 가져오기 cmdlet

MBAM Active Directory 데이터 가져오기 cmdlet을 사용 하면 Active Directory에 저장 된 복구 키 패키지와 소유자 인증 암호를 검색할 수 있습니다.

MBAM 2.5 SP1 서버는 볼륨 복구 및 Active Directory에 저장 된 TPM 소유자 정보를 사용 하 여 MBAM 데이터베이스를 미리 채우는 4 개의 PowerShell cmdlet을 제공 합니다.

볼륨 복구 키 및 패키지:

-   읽기-ADRecoveryInformation

-   읽기-MbamRecoveryInformation

TPM 소유자 정보:

-   읽기-ADTpmInformation

-   읽기-MbamTpmInformation

사용자를 컴퓨터에 연결 하는 방법:

-   쓰기-MbamComputerUser

읽기-광고 \ * cmdlet은 Active Directory에서 정보를 읽습니다. 쓰기-Mbam \ * cmdlet은 데이터를 MBAM 데이터베이스로 푸시 합니다. 구문, 매개 변수, 예제 등의 이러한 cmdlet에 대 한 자세한 내용은 [Microsoft Bitlocker 관리 및 모니터링 2.5에 대 한 Cmdlet 참조](https://technet.microsoft.com/library/dn459018.aspx) 를 참조 하세요.

**사용자 대 컴퓨터 연결 만들기:** MBAM Active Directory 데이터 가져오기 cmdlet은 Active Directory에서 정보를 수집 하 고 MBAM 데이터베이스에 데이터를 삽입 합니다. 그러나 사용자를 볼륨에 연결 하지는 않습니다. Add-ComputerUser.ps1 PowerShell 스크립트를 다운로드 하 여 사용자 간 연결을 만들어 사용자가 관리 및 모니터링 웹 사이트를 통해 컴퓨터에 액세스 하거나 복구에 셀프 서비스 포털을 사용할 수 있습니다. Add-ComputerUser.ps1 스크립트는 AD (Active Directory)의 **관리** 속성 또는 광고의 개체 소유자 또는 사용자 지정 CSV 파일에서 데이터를 수집 합니다. 그런 다음이 스크립트는 검색 된 사용자를 복구 정보 파이프라인 개체에 추가 하 여 복구 데이터베이스에 데이터를 삽입 하도록 MbamRecoveryInformation에 전달 해야 합니다.

[Microsoft 다운로드 센터](https://go.microsoft.com/fwlink/?LinkId=613122)에서 Add-ComputerUser.ps1 PowerShell 스크립트를 다운로드 합니다.

Cmdlet 및 스크립트를 사용 하는 방법에 대 한 예제를 포함 하 여 스크립트에 대 한 도움말을 제공 하는 **도움말 Add-ComputerUser.ps1** 지정할 수 있습니다.

MBAM 서버를 설치한 후 사용자 간 연결을 만들려면 쓰기-MbamComputerUser PowerShell cmdlet을 사용 합니다. 이 cmdlet은 Add-ComputerUser.ps1 PowerShell 스크립트와 유사 하 게, 셀프 서비스 포털을 사용 하 여 지정 된 컴퓨터에 대 한 TPM 소유자 인증 정보 또는 볼륨 복구 암호를 가져올 수 있는 사용자를 지정 하는 데 사용 됩니다.

**참고**  MBAM 에이전트는 컴퓨터에서 서버에 보고 하기 시작 하면 사용자 간 연결을 재정의 합니다.

 

**전제 조건:** 읽기-AD \ * cmdlet은 도메인 관리자 등의 높은 권한이 있는 사용자 계정으로 실행 되거나 정보에 대 한 읽기 권한을 부여 받은 사용자 지정 보안 그룹의 계정으로 실행 되는 경우에만 AD에서 정보를 검색할 수 있습니다 (권장).

[BitLocker 드라이브 암호화 작업 가이드: AD DS를 사용 하 여 암호화 된 볼륨 복구](https://technet.microsoft.com/library/cc771778(WS.10).aspx) 광고 정보에 대 한 읽기 권한이 있는 사용자 지정 보안 그룹 (또는 여러 그룹)을 만드는 방법에 대 한 세부 정보를 제공 합니다.

**Mbam 복구 및 하드웨어 웹 서비스 쓰기 권한:** 쓰기-Mbam \ * cmdlet은 복구 또는 TPM 정보를 게시 하는 데 사용 되는 MBAM 복구 및 하드웨어 서비스의 URL을 수락 합니다. 일반적으로 도메인 컴퓨터 서비스 계정만 MBAM 복구 및 하드웨어 서비스와 통신할 수 있습니다. MBAM 2.5 SP1에서는 구성원이 도메인 컴퓨터 서비스 계정 확인을 우회할 수 있는 DataMigrationAccessGroup 이라는 보안 그룹을 사용 하 여 MBAM 복구 및 하드웨어 서비스를 구성할 수 있습니다. 이 구성 된 그룹에 속하는 사용자로 서 쓰기-Mbam \ * cmdlet을 실행 해야 합니다. 또는 쓰기-Mbam \ * cmdlet에서 – Credential 매개 변수를 사용 하 여 구성 된 그룹에 있는 개별 사용자의 자격 증명을 지정할 수 있습니다.

다음 방법 중 하나를 사용 하 여이 보안 그룹의 이름으로 MBAM 복구 및 하드웨어 서비스를 구성할 수 있습니다.

-   사용-MbamWebApplication – AgentService Powershell cmdlet의-DataMigrationAccessGroup 매개 변수에 보안 그룹 또는 개인의 이름을 제공 합니다.

-   &lt;Inetpub &gt; \\Microsoft Bitlocker 관리 솔루션 \ 복구 및 하드웨어 Service\\ 폴더에서 web.config 파일을 편집 하 여 Mbam 복구 및 하드웨어 서비스를 설치한 후 그룹을 구성 합니다.

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    여기서 &lt; groupName &gt; 이 Active Directory에서 데이터 마이그레이션을 허용 하는 데 사용 되는 도메인 및 그룹 이름 (또는 개별 사용자)으로 바뀝니다.

-   IIS 관리자의 구성 편집기를 사용 하 여이 appSetting을 편집 합니다.

다음 예에서는 ADRecoveryInformation 그룹 및 데이터 마이그레이션 사용자 그룹의 구성원으로 실행 될 때 명령으로 contoso.com 도메인의 워크스테이션 OU (조직 구성 단위)에 있는 컴퓨터의 볼륨 복구 정보를 가져와 mbam.contoso.com 서버에서 실행 되는 MBAM 복구 및 하드웨어 서비스를 사용 하 여 MBAM에 씁니다.

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

**읽기-AD \ * cmdlet** 은 복구 또는 TPM 정보에 대해 쿼리할 Active Directory 호스팅 서버 컴퓨터의 이름 또는 IP 주소를 받아들입니다. 컴퓨터 개체가 있는 AD 컨테이너의 고유 이름을 SearchBase 매개 변수의 값으로 제공 하는 것이 좋습니다. 컴퓨터가 여러 Ou에 저장 되어 있는 경우 cmdlet에서 파이프라인 입력을 허용 하 여 각 컨테이너에 대해 한 번씩 실행할 수 있습니다. 광고 컨테이너의 고유 이름은 OU = 기계, DC = contoso, DC = com과 유사 하 게 표시 됩니다. 특정 컨테이너를 대상으로 하는 검색을 수행 하면 다음과 같은 혜택을 얻을 수 있습니다.

-   컴퓨터 개체에 대 한 대규모 광고 데이터 집합을 쿼리 하는 동안 시간이 초과 될 위험을 줄입니다.

-   백업 하는 것이 원하지 않거나 필요 하지 않은 데이터 센터 서버 또는 다른 종류의 컴퓨터를 포함 하는 Ou를 생략할 수 있습니다.

또 다른 옵션은 지정 된 SearchBase 또는 전체 도메인 아래에 있는 모든 컨테이너에서 컴퓨터 개체를 검색 하는 – a i a i a i a i a i a i a i a i a i a i a i a i -A 재귀 플래그를 사용 하는 경우-MaxPageSize 매개 변수를 사용 하 여 쿼리를 처리 하는 데 필요한 로컬 및 원격 메모리의 양을 제어할 수도 있습니다.

이러한 cmdlet은 PsObject 유형의 파이프라인 개체에 씁니다. 각 PsObject 인스턴스에는 단일 볼륨 복구 키 또는 TPM 소유자 문자열 (관련 컴퓨터 이름, 타임 스탬프, 그리고 MBAM 데이터 저장소에 게시 하는 데 필요한 기타 정보)이 포함 됩니다.

**쓰기-Mbam \ * cmdlet** 은 파이프라인의 복구 정보 매개 변수 값을 속성 이름으로 받아들입니다. 이렇게 하면 쓰기-Mbam \ * cmdlet이 읽기-AD \ * cmdlet의 파이프라인 출력을 수락할 수 있습니다 (예: 읽기-ADRecoveryInformation-Server contoso.com-재귀적 |). 쓰기-MbamRecoveryInformation-RecoveryServiceEndpoint mbam.contoso.com).

**쓰기-Mbam \ * cmdlet** 에는 내결함성, 자세한 로깅 및 WhatIf 및 확인에 대 한 기본 설정에 대 한 옵션을 제공 하는 선택적 매개 변수가 포함 됩니다.

**쓰기-Mbam \ * cmdlet** 에는 값이 **DateTime** 개체인 선택적 *시간* 매개 변수도 포함 되어 있습니다. 이 개체에는, 또는으로 설정할 수 있는 *Kind* 특성이 포함 되어 있습니다 `Local` `UTC` `Unspecified` . *시간* 매개 변수가 Active Directory에서 가져온 데이터로 채워지면 시간이 UTC로 변환 되 고이 *Kind* 특성이 자동으로로 설정 됩니다 `UTC` . 그러나 텍스트 파일과 같은 다른 소스를 사용 하 여 *시간* 매개 변수를 채울 때는 *Kind* 특성을 해당 값으로 명시적으로 설정 해야 합니다.

**참고**  읽기-광고 \ * cmdlet에는 컴퓨터 사용자를 나타내는 사용자 계정을 검색 하는 기능이 없습니다. 사용자 계정 연결에는 다음이 필요 합니다.

-   셀프 서비스 포털을 사용 하 여 볼륨 암호/패키지를 복구 하는 사용자

-   다른 사용자를 대신 하 여 설치 하는 동안 MBAM 헬프데스크 사용자의 보안 그룹에 정의 된 사용자를 복구 합니다.

 

## <a href="" id="bkmk-autounlock"></a>잠금 후 자동으로 TPM 잠금을 해제 하도록 MBAM 구성


잠금을 설정 하는 경우 자동으로 TPM 잠금을 해제 하도록 MBAM 2.5 SP1을 구성할 수 있습니다. TPM 잠금 자동 재설정을 사용 하도록 설정한 경우 MBAM은 사용자가 잠겨 있음을 감지 하 고 MBAM 데이터베이스에서 소유자 인증 암호를 받아 사용자의 TPM을 자동으로 잠금 해제 합니다. TPM 잠금 자동 재설정은 셀프 서비스 포털 또는 관리 및 모니터링 웹 사이트를 사용 하 여 해당 컴퓨터의 OS 복구 키를 검색 한 경우에만 사용할 수 있습니다.

**중요**  TPM 잠금 자동 재설정을 사용 하도록 설정 하려면 클라이언트측에서 서버 쪽 및 그룹 정책 모두에이 기능을 구성 해야 합니다.

 

-   클라이언트 쪽에서 TPM 잠금 자동 재설정을 사용 하도록 설정 하려면 **컴퓨터 구성** 관리 템플릿에 있는 그룹 정책 설정 "TPM 잠금 자동 재설정 구성"을 구성 합니다 &gt; **Administrative Templates** &gt; . **Windows 구성 요소** &gt; **MDOP mblaam** &gt; **클라이언트 관리**.

-   서버 쪽에서 TPM 잠금 자동 재설정을 사용 하도록 설정 하려면 설치 하는 동안 MBAM 서버 구성 마법사에서 "TPM 잠금 자동 재설정 사용"을 선택 하면 됩니다.

    또한 에이전트 서비스 웹 구성 요소를 사용 하도록 설정 하는 동안 "-TPM 잠금 자동 재설정" 스위치를 지정 하 여 PowerShell에서 TPM 잠금 자동 재설정을 사용 하도록 설정할 수 있습니다.

사용자가 셀프 서비스 포털 또는 관리 및 모니터링 웹 사이트에서 받은 BitLocker 복구 키를 입력 하면 MBAM 에이전트는 TPM이 잠겨 있는지 확인 합니다. 잠겨 있는 경우 MBAM 데이터베이스에서 컴퓨터에 대 한 TPM 소유자 인증을 검색 하려고 시도 합니다. TPM 소유자 인증이 성공적으로 검색 되 면 TPM의 잠금을 해제 하는 데 사용 됩니다. Tpm 잠금을 해제 하면 tpm이 완전히 작동 하므로 사용자는 TPM 잠금에서 이후 다시 부팅 하는 동안 복구 암호를 입력 하지 않습니다.

TPM 잠금 자동 재설정은 기본적으로 사용 되지 않습니다.

**참고**  Tpm 잠금 자동 재설정은 TPM 버전 1.2를 실행 하는 컴퓨터 에서만 지원 됩니다. TPM 2.0는 기본 제공 잠금 자동 재설정 기능을 제공 합니다.

 

**복구 감사 보고서** 에는 TPM 잠금 자동 재설정 관련 이벤트가 포함 됩니다. MBAM 클라이언트에서 TPM 소유자 인증 암호를 검색 하는 데 요청이 이루어지면 복구를 나타내기 위해 이벤트가 기록 됩니다. 감사 항목에는 다음 이벤트가 포함 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">엔트리에서</th>
<th align="left">값</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>감사 요청 원본</p></td>
<td align="left"><p>에이전트 TPM 잠금 해제</p></td>
</tr>
<tr class="even">
<td align="left"><p>키 유형</p></td>
<td align="left"><p>TPM 암호 해시</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이유 설명</p></td>
<td align="left"><p>TPM 다시 설정</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a>SQL Server에 대 한 보안 연결


MBAM은 sql server Reporting Services와 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털의 웹 서비스와 통신 합니다. SQL Server와 통신을 보호 하는 것이 좋습니다. 자세한 내용은 [SQL Server에 대 한 연결 암호화](https://technet.microsoft.com/library/ms189067.aspx)를 참조 하세요.

MBAM 웹 사이트 보안에 대 한 자세한 내용은 [MBAM 웹 사이트 보안 방법 계획](planning-how-to-secure-the-mbam-websites.md)을 참조 하세요.

## <a href="" id="bkmk-accts-groups"></a>계정 및 그룹 만들기


사용자 계정을 관리 하는 가장 좋은 방법은 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다. 권장 계정 및 그룹에 대 한 설명은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md)을 참조 하세요.

## <a href="" id="bkmk-logfiles"></a>MBAM 로그 파일 사용


이 섹션에서는 MBAM 서버 및 MBAM 클라이언트 로그 파일에 대해 설명 합니다.

**MBAM 서버 설정 로그 파일**

**MBAMServerSetup.exe** 파일은 mbam 설치 중 사용자의 **% temp%** 폴더에 다음 로그 파일을 생성 합니다.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 개 번호 &gt; . 로그**

    MBAM 설정 및 MBAM 서버 기능 구성 중에 수행 된 작업을 기록 합니다.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. .log**

    설치 중에 수행한 추가 작업을 기록 합니다.

**MBAM 서버 구성 로그 파일**

-   **응용 프로그램 및 서비스 로그/Microsoft Windows/MBAM-설정**

    Windows Powershell cmdlet 또는 MBAM 서버 구성 마법사를 사용 하 여 MBAM 서버 기능을 구성할 때 발생 하는 오류를 기록 합니다.

**MBAM 클라이언트 설치 로그 파일**

-   **MSI &lt; 5 임의 문자 &gt; 로그**

    MBAM 클라이언트 설치 중 수행 된 작업을 기록 합니다.

**MBAM-웹 로그 파일**

-   웹 포털 및 서비스의 활동을 표시 합니다.

## <a href="" id="bkmk-tde"></a>MBAM 데이터베이스 TDE 고려 사항 검토


SQL Server에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능은 MBAM 데이터베이스 기능을 호스팅하는 데이터베이스 인스턴스의 선택적 설치입니다.

TDE를 사용 하 여 실시간 전체 데이터베이스 수준의 암호화를 수행할 수 있습니다. TDE는 규정 준수 또는 기업 데이터 보안 표준을 충족 하기 위해 일괄 암호화를 위한 최적의 선택입니다. TDE는 파일 수준에서 작동 하며, 파일 시스템 암호화 (EFS)와 BitLocker 드라이브 암호화의 두 가지 Windows 기능과 유사 합니다. 또한 두 기능은 모두 하드 드라이브의 데이터를 암호화 합니다. TDE는 셀 수준 암호화, EFS 또는 BitLocker를 대체 하지 않습니다.

데이터베이스에서 TDE를 사용 하도록 설정 하면 모든 백업이 암호화 됩니다. 따라서 데이터베이스 암호화 키를 보호 하는 데 사용 된 인증서가 데이터베이스 백업과 함께 백업 되 고 유지 되도록 주의를 기울여야 합니다. 이 인증서 (또는 인증서)가 손실 되 면 데이터를 읽을 수 없게 됩니다.

데이터베이스와 인증서를 백업 합니다. 각 인증서 백업에는 두 개의 파일이 있어야 합니다. 이러한 파일은 모두 보관 되어야 합니다. 보안을 위해 가장 적합 한 것은 데이터베이스 백업 파일과 별도로 백업 해야 한다는 것입니다. 또는 TDE에 사용 되는 키 저장소 및 유지 관리를 위해 EKM (확장할 수 있는 키 관리) 기능 (확장 가능한 키 관리)을 사용 하는 것이 좋습니다.

MBAM 데이터베이스 인스턴스의 TDE를 사용 하는 방법에 대 한 예제는 [투명 한 데이터 암호화 (tde) 이해](https://technet.microsoft.com/library/bb934049.aspx)를 참조 하세요.

## <a href="" id="bkmk-general-security"></a>일반 보안 고려 사항 이해


**보안 위험을 파악 합니다.** Microsoft BitLocker 관리 및 모니터링을 사용할 때 가장 심각한 위험은 BitLocker 드라이브 암호화를 다시 구성 하 고 MBAM 클라이언트에서 BitLocker 암호화 키 데이터를 얻을 수 있는 권한이 없는 사용자가 해당 기능을 손상 시킬 수 있다는 것입니다. 그러나 서비스 거부 공격으로 인해 짧은 시간 동안에는 MBAM 기능이 손실 되는 것은 일반적으로 전자 메일 이나 네트워크 통신이 손실 되는 등의 경우와 달리 심각한 영향을 미치지 않는다는 것입니다.

**컴퓨터를 물리적으로 보호**합니다. 물리적 보안 없이 보안이 제공 되지 않습니다. MBAM 서버에 물리적으로 액세스 하는 공격자는이를 사용 하 여 전체 클라이언트 기반을 공격할 수도 있습니다. 모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다. MBAM 서버는 액세스 권한이 있는 안전한 서버 방에 저장 되어야 합니다. 운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.

**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다. [보안 TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819)에서 보안 알림 서비스에 가입 하 여 Windows 운영 체제, SQL SERVER 및 mbam에 대 한 새 업데이트에 대 한 정보를 지속적으로 유지 합니다.

**강력한 암호 또는 암호 문구를 사용**합니다. 모든 MBAM 관리자 계정에 대해 15 개 이상의 문자로 강력한 암호를 항상 사용 합니다. 빈 암호를 사용 하지 마세요. 암호 개념에 대 한 자세한 내용은 [암호 정책을](https://technet.microsoft.com/library/hh994572.aspx)참조 하세요.



## 관련 항목


[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





