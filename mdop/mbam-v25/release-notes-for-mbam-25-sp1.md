---
title: MBAM 2.5 SP1 릴리스 정보
description: MBAM 2.5 SP1 릴리스 정보
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824988"
---
# MBAM 2.5 SP1 릴리스 정보


이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.

이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1을 설치 하기 전에 자세히 읽어 보세요. 이 릴리스 노트에는 MBAM을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있으며 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 노트가 다른 MBAM 2.5 SP1 설명서와 다를 경우 신뢰할 수 있는 최신 변경 사항을 고려해 야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> MBAM 2.5 SP1의 알려진 문제점


이 섹션에는 MBAM 2.5 SP1에 대 한 릴리스 정보가 포함 되어 있습니다.

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a>PowerShell 읽기-AD \ * cmdlet은 사용자에 게 충분 한 권한이 없는 경우 피드백을 제공 하지 않습니다.

MBAM 서버에 대 한 PowerShell Read AD \ * cmdlet을 사용 하려는 사용자에 게 Active Directory 복구 정보를 읽거나 TPM 정보를 읽을 수 있는 사용자 권한이 없는 경우에는 cmdlet이 사용자에 게 오류 또는 경고를 제공 하지 않습니다.

**해결 방법:** 필요한 사용자 권한이 있는 경우 PowerShell 읽기-AD \ * cmdlet만 사용 합니다.

### MBAM Active Directory (AD) 마이그레이션 cmdlet이 볼륨 복구 정보를 검색 하지 않음

MBAM Active Directory (AD) 마이그레이션 cmdlet은 슬래시 문자 (/)가 OU 이름의 일부인 경우 조직 구성 단위 (Ou)의 컴퓨터에 대 한 볼륨 복구 정보를 검색 하지 못합니다. 이 오류가 발생 했을 때 파이프라인 종료 오류로 인해 반복 되는 광고를 수행할 수 없습니다.

**기술 정보:** 명령을 실행할 때 다음 오류가 표시 됩니다.

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

또한 예외 스택 추적도 `Error[0].Exception.StackTrace` 다음과 같이 표시 됩니다.

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

**해결 방법:** 이 문제를 해결 하려면 다음 작업 중 하나를 수행 합니다.

-   OU의 이름을 변경 하 여 슬래시 문자를 제거 하 고 스크립트를 실행 합니다.

-   백업 프로세스에서 문제가 있는 OU를 제외 하려면 이름에 슬래시 문자가 포함 되지 않은 Ou 목록을 찾습니다. 이러한 Ou에 대해 한 번에 하나의 OU에 대해 스크립트를 실행 합니다.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> H/pc에서 TPM + PIN 보호기를 설정한 경우 MBAM이 볼륨을 암호화 하는 데 실패 하 고 오류를 보고 함

최종 사용자가 태블릿 장치에서 TPM + PIN 보호기를 설정 하려고 하면 MBAM이 암호화에 실패 하 고 오류를 보고 합니다. 이 문제는 태블릿 장치에 부팅 전 환경 키보드가 없기 때문에 발생 합니다.

**해결 방법:** **태블릿에서 부팅 가능 키보드 입력이 필요한 BitLocker 인증 사용** 그룹 정책 설정을 사용 하도록 설정 합니다. 이 설정은 BitLocker 그룹 정책 설정 이며, MBAM 그룹 정책 템플릿에서 사용할 수 없습니다.

### 모든 서비스 계정에 대해 사용자 계정 이름이 필요 합니다.

모든 서비스 계정에 대해 UPN (사용자 계정 이름)을 MBAM으로 설정 해야 합니다. 계정에 대 한 UPN을 만들지 못한 경우 구성 프로세스 중에 사용자 또는 그룹을 Active Directory에서 찾을 수 없음을 나타내는 오류 메시지가 표시 됩니다.

**해결 방법:** UPN을 서비스 계정에 추가 합니다.

### IIS를 .NET Framework 4.5으로 업그레이드 한 후 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않음

IIS (인터넷 정보 서비스)를 Microsoft .NET Framework 4.5으로 업그레이드 하면 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않습니다.

**해결 방법:** [.Net Framework 4.0을 설치 하면 "system.servicemodel: HttpModule '을 로드할 수 없습니다. 라는 문서 오류 메시지](https://go.microsoft.com/fwlink/?LinkId=393568)를 참조 하세요.

### 보고서가 구성 되지 않은 경우 관리 및 모니터링 웹 사이트에 "보고서를 찾을 수 없음" 오류 메시지가 표시 됨

관리 및 모니터링 웹 사이트를 구성한 다음 보고서 기능을 먼저 구성 하지 않고 보고서를 보려고 하면 오류 메시지에 해당 보고서를 찾을 수 없음을 표시 합니다.

**해결 방법:** 웹 응용 프로그램을 구성 하기 전에 보고서 기능을 구성 합니다.

### SSL이 SSRS에 구성 되어 있지 않은 경우 관리 및 모니터링 웹 사이트의 보고서에 경고가 표시 됨

SQL Server Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 구성할 때 보고서 기능에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다. 그런 다음 관리 및 모니터링 웹 사이트를 열고 보고서를 선택 하면 "보안 콘텐츠만 표시 됨"과 같은 오류 메시지가 나타납니다.

**해결 방법:** 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다. 이 문제를 해결 하려면 SQL Server Reporting Services가 설치 되어 있는 MBAM 컴퓨터로 이동한 다음 **Reporting Services 구성 관리자**를 실행 하 고 **웹 서비스 URL**을 클릭 합니다. 서버에 대 한 적절 한 SSL 인증서를 선택 하 고 적절 한 SSL 포트 (기본 포트 443)를 입력 한 다음 **적용**을 클릭 합니다.

### BitLocker 준수 요약 보고서에서 "뒤로"를 클릭 하면 오류가 발생 하는 경우

BitLocker 준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.

**해결 방법:** 않아야.

### 암호화 강도가 BitLocker 컴퓨터 준수 보고서에 잘못 표시 됨

**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 강도를 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 BitLocker 컴퓨터 준수 보고서에 항상 암호화 수준에 대 한 "unknown"이 표시 됩니다. 그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.

**해결 방법:** **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.

### 드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨

SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.

**해결 방법:** 않아야. MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.

### 보안 강화 구성으로 인해 보고서에 오류 메시지가 잘못 표시 될 수 있음

Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타날 수 있습니다. 웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 기본적으로 ESC가 설정 됩니다.

**해결 방법:** MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타나면 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다. 또는 ESC가 설정 되지 않은 다른 컴퓨터에서 보고서를 볼 수도 있습니다.

### Bitlocker XTS 암호화 알고리즘에 대 한 지원
Windows 10 버전 1511의 XTS 암호화 알고리즘에 대 한 Bitlocker 추가 지원이 제공 됩니다. HF02를 사용 하면이 Bitlocker 옵션 및 HF04에 대 한 클라이언트 지원이 추가 되어 서버 쪽 지원이 추가 되었습니다. 그러나, 다음과 같은 한 가지 알려진 제한 사항이 있습니다.

* 고객은 동일한 컴퓨터에서 OS와 데이터 볼륨에 대해 동일한 암호화 강도를 사용 해야 합니다.
다른 암호화 강도가 사용 되는 경우 MBAM은 컴퓨터를 **비규격**으로 보고 합니다.

### 셀프 서비스 포털이 키 ID 항목에 "-"를 자동으로 추가 합니다.
HF02에서 MBAM 셀프 서비스 포털은 키 ID 항목에 '-'를 자동으로 추가 합니다.  
**참고:** Javascript를 적용 하려면 서버를 다시 구성 해야 합니다.

### MBAM 2.5 Sp1 보고서가 작동 하지 않거나 올바르게 렌더링 되지 않음
SQL Server 2016 edition에서 SSRS가 호스팅되는 경우 보고서 페이지가 올바르게 렌더링 되지 않습니다. 
예를 들어 헬프데스크 탐색 – 보고서를 클릭 하면 (강조 표시 된 부분에 "x"가 있음) Fiddler를 사용 하 여 더 많은 작업을 하 고, 보고서를 클릭 한 후에는, HTML 4.0 렌더링 형식을 사용 하 여 SSRS 페이지를 호출 하는 것 처럼 보입니다.

**해결 방법:** 사이트 마스터 코드를 보고 X-UA 모드가 IE8으로 결정 되었습니다. IE8은 수명이 만료 되는 방식이 고, 고객은 IE11를 사용 합니다. 설정을 다음 코드로 업데이트 합니다. 이를 통해 사이트는 IE11 렌더링 기술을 활용할 수 있습니다.

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

원래 설정: 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


Chrome, Firefox 등의 다른 브라우저에 문제가 표시 되지 않는 이유입니다.



## 관련 항목


[MBAM 2.5 정보](about-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





