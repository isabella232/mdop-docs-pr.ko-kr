---
title: MBAM 2.5 SP1 정보
description: MBAM 2.5 SP1 정보
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823783"
---
# MBAM 2.5 SP1 정보


MBAM 2.5 SP1은 BitLocker 드라이브 암호화를 위한 간단한 관리 인터페이스를 제공 합니다. BitLocker는 분실 하거나 도난당 한 컴퓨터에 대 한 데이터 절도 또는 데이터 노출에 대 한 향상 된 보호 기능을 제공 합니다. BitLocker는 Windows 운영 체제 및 드라이브 및 구성 된 데이터 드라이브에 저장 된 모든 데이터를 암호화 합니다.

## MBAM 개요


MBAM 2.5 SP1에는 다음과 같은 기능이 있습니다.

-   관리자가 엔터프라이즈 전체의 클라이언트 컴퓨터에서 볼륨을 암호화 하는 프로세스를 자동화할 수 있습니다.

-   보안 관리자가 개별 컴퓨터 또는 엔터프라이즈 자체의 준수 상태를 빠르게 확인할 수 있습니다.

-   Microsoft System Center Configuration Manager를 사용 하 여 중앙 집중식 보고 및 하드웨어 관리를 제공 합니다.

-   최종 사용자에 게 BitLocker PIN 및 복구 키 요청을 지원 하기 위해 지원 센터의 작업량을 줄입니다.

-   셀프 서비스 포털을 사용 하 여 최종 사용자가 암호화 된 장치를 별도로 복구할 수 있도록 합니다.

-   보안 책임자가 키 정보 복구에 대 한 액세스를 쉽게 감사할 수 있도록 합니다.

-   Windows Enterprise 사용자가 회사 데이터를 보호 한다는 보장으로 어디서 나 계속 작업 하도록 합니다.

MBAM은 엔터프라이즈에 대해 설정한 BitLocker 암호화 정책 옵션을 적용 하 고, 해당 정책으로 클라이언트 컴퓨터의 준수 여부를 모니터링 하 고, 엔터프라이즈 및 개인 컴퓨터의 암호화 상태를 보고 합니다. 또한, MBAM은 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있도록 합니다.

다음 그룹은 MBAM을 사용 하 여 BitLocker를 관리 하는 데 관심이 있을 수 있습니다.

-   권한 부여 없이 기밀 데이터가 공개 되지 않는지 확인 하는 관리자, IT 보안 전문가 및 규정 준수 책임자

-   원격 또는 지사에서 컴퓨터 보안을 담당 하는 관리자

-   Windows를 실행 하는 클라이언트 컴퓨터를 담당 하는 관리자

**참고**  이 MBAM 설명서에는 BitLocker에 대해 자세히 설명 되어 있지 않습니다. 자세한 내용은 [BitLocker 드라이브 암호화 개요](https://go.microsoft.com/fwlink/p/?LinkId=225013)를 참조 하세요.

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a>MBAM 2.5 SP1의 새로운 기능


이 섹션에서는 MBAM 2.5 SP1의 새로운 기능에 대해 설명 합니다.

### MBAM 2.5 SP1 클라이언트에 대해 새로 지원 되는 언어

다음 추가 언어는 MBAM 2.5 SP1에서 셀프 서비스 포털을 포함 하 여이 클라이언트에 대해서만 지원 됩니다.

체코어 (체코 공화국) cs-CZ

덴마크어 (덴마크) da-진한

네덜란드어 (네덜란드) nl-NL

핀란드어 (핀란드) fi

그리스어 (그리스) el-GR

헝가리어 (헝가리) hu-hu&platform-HU-HU&PLATFORM

노르웨이어, 복말 (노르웨이) nb-아니요

폴란드어 (폴란드) pl-PL

포르투갈어 (포르투갈) pt-PT

슬로바키아어 (슬로바키아) a/.

슬로베니아어 (슬로베니아) sl-SI

스웨덴 (스웨덴) sv-SE

터키어 (터키) tr-TR

MBAM 2.5 및 MBAM 2.5 SP1의 클라이언트 및 서버에 대해 지원 되는 모든 언어 목록은 [mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.

### Windows 10 지원

MBAM 2.5 SP1은 이전 버전의 MBAM에서 지원 되는 소프트웨어 외에도 Windows 10 및 Windows Server 2016에 대 한 지원을 추가 합니다.

Windows 10은 MBAM 2.5 및 MBAM 2.5 SP1 모두에서 지원 됩니다.

### Microsoft SQL Server 2014 SP1에 대 한 지원

MBAM 2.5 SP1에는 이전 버전의 MBAM에서 지원 되는 소프트웨어와 함께 Microsoft SQL Server 2014 SP1에 대 한 지원이 추가 되었습니다.

### MBAM은 더 이상 별도의 MSI와 함께 제공 되지 않습니다.

MBAM 2.5 SP1 부터는 별도의 MSI가 MBAM 제품에 더 이상 포함 되어 있지 않습니다. 그러나 제품에 포함 된 실행 파일 (.exe)에서 MSI를 추출할 수 있습니다.

### MBAM은 TPM을 소유 하지 않고 정식 암호를 사용할 수 있습니다.

이전에는 MBAM이 TPM을 소유 하지 않은 경우 TPM 소유자 Auth를 MBAM 데이터베이스에 escrowed 수 없습니다. TPM을 소유 하 고 암호를 저장 하도록 MBAM을 구성 하려면 TPM 자동 프로비저닝 기능을 사용 하지 않도록 설정 하 고 클라이언트 컴퓨터에서 TPM을 지워야 합니다.

Windows 8 이상에서 MBAM 2.5 SP1은 이제 TPM을 소유 하지 않고 소유자 인증 암호를 에스크로 할 수 있습니다. 서비스를 시작 하는 동안 MBAM은 TPM이 이미 소유 되어 있는지 확인 하 고, 있다면 운영 체제에서 암호를 요청 합니다. 그런 다음 MBAM 데이터베이스로 비밀 번호를 escrowed. 또한 소유자 인증이 로컬로 삭제 되지 않도록 그룹 정책을 설정 해야 합니다.

Windows 7에서 MBAM은 MBAM 데이터베이스에서 자동으로 TPM 소유자 인증 정보를 받아야 하는 TPM을 소유 하 고 있어야 합니다. MBAM이 TPM을 소유 하지 않거나 TPM의 AD (Active Directory) 백업이 그룹 정책을 통해 구성 되어 있으면 **Mbam directory (ad) 데이터 가져오기 cmdlet** 을 사용 하 여 AD에서 mbam 데이터베이스로 TPM 소유자 인증을 복사 해야 합니다. Active Directory에 저장 된 볼륨 복구 및 TPM 소유자 정보를 사용 하 여 MBAM 데이터베이스를 미리 채우는 5 개의 새 PowerShell cmdlet입니다.

자세한 내용은 [Mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-tpm)참조 하세요.

### MBAM은 잠금 이후 TPM을 자동으로 잠금 해제할 수 있습니다.

TPM 1.2를 실행 하는 컴퓨터에서 잠금을 설정 하는 경우 TPM을 자동으로 잠금 해제 하도록 MBAM을 구성할 수 있습니다. TPM 잠금 자동 재설정 기능을 사용 하도록 설정한 경우 MBAM은 사용자가 잠겨 있음을 감지 하 고 MBAM 데이터베이스에서 소유자 인증 암호를 받아 사용자의 TPM을 자동으로 잠금 해제 합니다.

이 기능은 클라이언트 쪽의 서버 쪽 및 그룹 정책 모두에서 사용 하도록 설정 해야 합니다. 자세한 내용은 [Mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-autounlock)참조 하세요.

### FIPS 규격 BitLocker 숫자 암호 보호기에 대 한 지원

MBAM 2.5에서는 Windows 8.1 운영 체제를 실행 하는 디바이스의 FIPS (연방 정보 처리 표준) 규격 BitLocker 복구 키에 대 한 지원이 추가 되었습니다. 그러나 windows 7에서 FIPS 규격 복구 키를 구현 하지 않았습니다. 따라서 Windows 7 및 Windows 8 장치에는 복구를 위한 DRA (데이터 복구 에이전트) 보호기가 계속 필요 합니다.

Windows 팀에는 핫픽스가 포함 된 FIPS 호환 복구 키가 포함 되어 있으며, MBAM 2.5 SP1에도이에 대 한 지원이 추가 되었습니다.

**참고**  Windows8 운영 체제를 실행 하는 클라이언트 컴퓨터는 해당 OS에 핫픽스를 백 이식할 수 없기 때문에 DRA 보호기가 여전히 필요 합니다. Windows 7 및 Windows 8 컴퓨터용 BitLocker 핫픽스를 다운로드 하 고 설치 하려면 [Bitlocker 관리 및 모니터링 2.5에 대 한 핫픽스 패키지 2](https://support.microsoft.com/kb/3015477) 를 참조 하세요. DRA에 대 한 자세한 내용은 [BitLocker를 사용 하 여 데이터 복구 에이전트 사용](https://go.microsoft.com/fwlink/?LinkId=393557)을 참조 하세요.

 

조직에서 FIPS 준수를 사용 하도록 설정 하려면 연방 정보 처리 표준 (FIPS) 그룹 정책 설정을 구성 해야 합니다. 구성 방법에 대 한 자세한 내용은 [BitLocker 그룹 정책 설정을](https://go.microsoft.com/fwlink/?LinkId=393560)참조 하세요.

### 새 그룹 정책 설정을 사용 하 여 사전 부팅 복구 메시지 및 URL 사용자 지정

새로운 그룹 정책 설정, **사전 부팅 복구 메시지 및 url을 구성**하면 OS 드라이브가 잠길 때 사전 부팅 BitLocker 복구 화면에 표시 되는 URL을 지정 하거나 사용자 지정 복구 메시지를 구성할 수 있습니다. 이 설정은 Windows 10을 실행 하는 클라이언트 컴퓨터 에서만 사용할 수 있습니다.

이 정책 설정을 사용 하도록 설정 하는 경우 사전 부팅 복구 메시지에 대해 다음 옵션 중 하나를 선택할 수 있습니다.

-   **사용자 지정 복구 메시지 사용**: 사전 부팅 BitLocker 복구 화면에 사용자 지정 메시지를 포함 하려면이 옵션을 선택 합니다.

-   **사용자 지정 복구 URL 사용**: 사전 부팅 BitLocker 복구 화면에 표시 되는 기본 URL을 바꾸려면이 옵션을 선택 합니다.

-   **기본 복구 메시지 및 Url 사용**: 사전 부팅 BitLocker 복구 화면에 기본 BitLocker 복구 메시지 및 url을 표시 하려면이 옵션을 선택 합니다. 이전에 사용자 지정 복구 메시지 또는 URL을 구성한 경우 기본 메시지로 돌아가려면이 정책을 사용 하도록 설정 하 고이 옵션을 선택 해야 합니다.

새 그룹 정책 설정은 다음 GPO 노드에 있습니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **운영 체제 드라이브**. 자세한 내용은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.

### 사용 된 공간 암호화에 대 한 MBAM 추가 지원

MBAM 2.5 SP1에서 BitLocker 그룹 정책을 통해 사용 하는 공간 암호화를 사용 하도록 설정 하면 MBAM 클라이언트가이를 허용 합니다.

이 그룹 정책 설정을 **운영 체제 드라이브에 드라이브 암호화 유형 강제 적용** 이라고 하며, **컴퓨터 구성** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **BitLocker 드라이브 암호화** &gt; **운영 체제 드라이브**에는 다음과 같은 GPO 노드가 있습니다. 이 정책을 사용 하 고 **사용 된 공간만 암호화**로 암호화 유형을 선택 하는 경우, mbam은 정책을 인식 하 고 BitLocker는 볼륨에 사용 되는 디스크 공간만 암호화 합니다.

자세한 내용은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.

### 암호화 된 하드 드라이브에 대 한 MBAM 클라이언트 지원

MBAM은 오 팔에 대 한 TCG 사양 요구 사항 및 IEEE 1667 표준을 충족 하는 암호화 된 하드 드라이브에서 BitLocker를 지원 합니다. 이러한 디바이스에서 BitLocker를 사용 하도록 설정 하면 암호화 된 드라이브에서 키를 생성 하 고 관리 기능을 수행 합니다. 자세한 내용은 [암호화 된 하드 드라이브](https://technet.microsoft.com/library/hh831627.aspx) 를 참조 하세요.

### Spn을 등록할 때 더 이상 위임 구성이 필요 하지 않음

MBAM 2.5 SP1에서는 응용 프로그램 풀 계정에 대해 등록 하는 Spn에 대해 제한 위임을 구성 하는 요구 사항이 더 이상 필요 하지 않습니다. 그러나이는 여전히 MBAM 2.5에 대 한 요구 사항입니다.

### Windows 배포의 일부로 MBAM을 사용 하 여 BitLocker 사용

MBAM 2.5 SP1에서는 PowerShell 스크립트를 사용 하 여 BitLocker 드라이브 암호화 및 에스크로 복구 키를 MBAM 서버에 구성할 수 있습니다.

자세한 내용은 [Windows 배포의 일부로 MBAM을 사용 하 여 BitLocker를 사용 하도록 설정 하는 방법](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md) 을 참조 하세요.

### PowerShell 또는 SSP 사용자 지정 마법사를 사용 하 여 셀프 서비스 포털을 사용자 지정할 수 있습니다.

MBAM 2.5 SP1의 경우 PowerShell을 사용 하는 것 외에도 사용자 지정 마법사를 사용 하 여 셀프 서비스 포털을 구성할 수 있습니다. [MBAM 2.5 웹 응용 프로그램을 구성 하는 방법을](how-to-configure-the-mbam-25-web-applications.md)참조 하세요.

### 웹 브라우저가 더 이상 관리자 권한으로 실행 되지 않음

MBAM 2.5의 문제는 서버 구성 도구에 대 한 도움말 링크를 통해 브라우저 창이 관리자 권한으로 열리도록 하는 데 발생 합니다. 이 문제는 MBAM 2.5 SP1에서 해결 되었습니다.

### CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하기 위해 더 이상 JavaScript 파일을 다운로드할 필요가 없습니다.

MBAM 2.5이 하에서 셀프 서비스 포털에 액세스 하는 클라이언트가 인터넷에 액세스할 수 없는 경우 셀프 서비스 포털의 구성에 사용 되는 jQuery 파일을 미리 CDN에서 다운로드 해야 합니다. MBAM 2.5 SP1에서는 모든 JavaScript 파일이 제품에 포함 되어 있으므로 다운로드할 필요가 없습니다.

### 보고서 작성기 3.0에서 보고서를 열 수 있음

MBAM 2.5 SP1에서는 보고서를 최신 보고서 정의 언어 스키마로 업데이트 하 여 사용자가 보고서 작성기 3.0에서 보고서를 열고 사용자 지정 하 고 보고서 파일을 손상 시 키 지 않고 즉시 저장할 수 있습니다.

### 새 PowerShell cmdlet

MBAM 2.5 SP1 용 새 PowerShell cmdlet을 사용 하면 데이터베이스, 보고서, 웹 응용 프로그램을 비롯 한 다양 한 MBAM 기능을 구성 하 고 관리할 수 있습니다. 각 기능에는 기능을 사용 하거나 사용 하지 않도록 설정 하거나 기능에 대 한 정보를 가져오는 데 사용할 수 있는 해당 PowerShell cmdlet이 있습니다.

MBAM 2.5 SP1에 대해 다음 cmdlet이 구현 되었습니다.

-   읽기-MbamTpmInformation

-   읽기-MbamRecoveryInformation

-   읽기-ADTpmInformation

-   읽기-ADRecoveryInformation

-   쓰기-MbamComputerUser

MBAM 2.5 SP1 용 Enable-MbamWebApplication 및 Test-MbamWebApplication cmdlet에 다음 매개 변수가 구현 되었습니다.

-   DataMigrationAccessGroup

-   TpmAutoUnlock

Cmdlet에 대 한 자세한 내용은 [Mbam 2.5 보안 고려 사항](mbam-25-security-considerations.md) 및 [Microsoft Bitlocker 관리 및 모니터링 Cmdlet 도움말](https://technet.microsoft.com/library/dn720418.aspx)을 참조 하세요.

### MBAM 에이전트는 프레젠테이션 모드를 검색 합니다.

MBAM 에이전트는 컴퓨터가 프레젠테이션 모드에 있을 때 검색 하 고 해당 시간에 MBAM UI를 호출 하지 않도록 합니다.

### 현재 MBAM 에이전트 서비스가 지연 된 시작을 사용 하도록 구성 되었습니다.

설치 후 서비스는 이제 Windows를 시작 하는 데 걸리는 시간을 줄임으로써 MBAM 에이전트 서비스를 지연 시작을 사용 하도록 설정 합니다.

### 잠긴 고정 데이터 볼륨이 이제 규격으로 보고 됨

"잠긴 고정 데이터" 볼륨에 대 한 규정 준수 계산 논리가 변경 되어 볼륨을 "규격"으로 보고 하지만, "알 수 없음"의 보호 상태와 "볼륨 잠김"의 준수 상태 세부 정보를 사용 하는 경우 이전에는 잠긴 볼륨이 "비규격", "암호화 됨"의 프로텍터 상태, "알 수 없음"의 암호화 상태, "알 수 없는 오류"에 대 한 준수 상태 세부 정보로 보고 되었습니다.


## MDOP 기술을 활용 하는 방법


MBAM은 Microsoft 데스크톱 최적화 팩 (MDOP)의 일부입니다. MDOP는 Microsoft 소프트웨어 보증 프로그램의 일부입니다. Microsoft 소프트웨어 보증 프로그램 및 MDOP를 구입 하는 방법에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.

## MBAM 2.5 SP1 릴리스 정보


이 설명서에 포함 되지 않은 최신 뉴스에 대 한 자세한 내용은 [MBAM 2.5 SP1 릴리스 노트](release-notes-for-mbam-25-sp1.md)를 참조 하세요.

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.

## 관련 항목


[Microsoft BitLocker 관리 및 모니터링 2.5](index.md)

[MBAM 2.5 시작](getting-started-with-mbam-25.md)

 

 





