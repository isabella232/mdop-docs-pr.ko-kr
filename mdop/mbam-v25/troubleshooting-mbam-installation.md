---
title: MBAM 2.5 설치 문제 해결
description: MBAM 2.5 설치 문제를 해결하는 방법을 소개합니다.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 6ea152792801c630fa365f37d1668d1a4d84b3a5
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910633"
---
# <a name="troubleshooting-mbam-25-installation-problems"></a>MBAM 2.5 설치 문제 해결

이 문서에서는 독립 실행형 구성에서 Microsoft BitLocker 관리 및 모니터링(MBAM) 2.5 설치 문제를 해결하는 방법을 소개합니다.

## <a name="referring-mbam-log-files-for-troubleshooting"></a>문제 해결을 위해 MBAM 로그 파일 참조

MBAM에는 서버 설치, 클라이언트 설치 및 이벤트에 대한 로깅이 포함됩니다. 이 로깅은 문제 해결을 위해 참조해야 합니다. 
 
### <a name="mbam-server-installation-log-files"></a>MBAM 서버 설치 로그 파일

MBAMServerSetup.exe MBAM 설치 중에 사용자의 %temp% 폴더에 다음 로그 파일을 생성합니다.<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14개 숫자>.log**

MBAMServerSetup.exe MBAM 설치 및 MBAM 서버 기능 설치 중에 수행된 작업을 기록합니다.<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log**

MBAMServerSetup.exe 동안 수행된 추가 작업을 기록합니다.

### <a name="mbam-client-installation-log-file"></a>MBAM 클라이언트 설치 로그 파일

클라이언트 설치는 %temp% 폴더(또는 클라이언트 설치 방법에 따라 사용자 지정 위치)에 다음 로그 파일에 기록됩니다. <br />**MSI \<five random characters\> .log**

이 로그에는 MBAM 클라이언트 설치 중에 수행된 작업이 포함되어 있습니다.
 
### <a name="mbam-client-event-logging-channel"></a>MBAM 클라이언트 이벤트 로깅 채널

MBAM에는 별도의 이벤트 로깅 채널이 있습니다. 관리자, 분석 및 운영 로그 파일은 이벤트 뷰어의 응용 **** 프로그램 및 서비스 로그 Microsoft Windows  >  ****  >  ****  >  **MBAM에 있습니다.**

다음 표에서는 각 이벤트 로그에 대한 간략한 설명을 소개합니다.
 
|이벤트 로그| 설명|
|----------|-------|
|Microsoft-Windows-MBAM/관리자|  오류 메시지가 들어 있습니다.|
|Microsoft-Windows-MBAM/분석|   고급 로깅 정보가 들어 있습니다.|
|Microsoft-Windows-MBAM/Operational|    성공 메시지가 들어 있습니다.|

### <a name="mbam-server-event-logging-channel"></a>MBAM 서버 이벤트 로깅 채널

로그 파일은 이벤트 뷰어의 응용 **** 프로그램 및 서비스 로그 Microsoft Windows  >  ****  >  ****  >  **MBAM에 있습니다.** 다음 표에는 MBAM 2.5에서 도입된 서버 이벤트 로그가 포함되어 있습니다.

|이벤트 로그| 설명|
|--------|-------------|
|Microsoft-Windows-MBAM/관리자|  오류 메시지가 들어 있습니다.|
|Microsoft-Windows-MBAM/분석|   고급 로깅 정보가 들어 있습니다.|
|Microsoft-Windows-MBAM/Operational|    성공 메시지가 들어 있습니다.|

### <a name="mbam-web-service-logs"></a>MBAM 웹 서비스 로그

각 MBAM 웹 서비스 로그는 SVCLOG 파일에 로깅 정보를 기록합니다. 기본적으로 각 웹 서비스는 C:\inetpub\Microsoft BitLocker Management Solution\Logs 폴더에 해당 이름을 사용하는 폴더 아래에 추적 파일을 씁니다.

서비스 추적 뷰어 도구(Microsoft Visual Studio 부분)를 사용하여 svclog 추적을 검토할 수 있습니다.

## <a name="troubleshooting-encryption-and-reporting-issues"></a>암호화 및 보고 문제 해결

이 섹션에는 서버 기능, 클라이언트 기능, 구성 설정 및 알려진 문제에 대한 문제 해결 정보가 포함되어 있습니다.
 
### <a name="mbam-client-installation-group-policy-settings"></a>MBAM 클라이언트 설치, 그룹 정책 설정

클라이언트 컴퓨터에 MBAM 에이전트가 설치되어 있는지 확인합니다. MBAM을 설치하면 BitLocker 관리 클라이언트 서비스라는 서비스가 생성됩니다. 이 서비스는 자동으로 시작하도록 구성됩니다. 서비스가 실행 중인지 여부를 판단합니다.

MBAM 그룹 정책 설정이 클라이언트 컴퓨터에 적용되는지 확인합니다. 다음 레지스트리 하위 키는 그룹 정책 설정이 클라이언트 컴퓨터에 적용된 경우 **만들어집니다.** HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement

이 키가 있으며 그룹 정책 설정에 따라 값을 사용하여 채워지는지 확인합니다.

### <a name="mbam-agent-in-the-initial-delay-period"></a>초기 지연 기간의 MBAM 에이전트

MBAM 클라이언트는 설치 직후에 작업을 시작하지 않습니다. MBAM 에이전트가 작업을 시작하기까지 1~18분의 초기 임의 지연이 있습니다. 초기 지연 외에 최소 90분의 지연이 있습니다. 이 지연은 클라이언트 상태를 검사하는 빈도에 대해 구성된 그룹 정책 설정에 따라 다를 수 있습니다. 따라서 클라이언트 시작 전의 총 지연은 *임의*시작 지연  +  *클라이언트 확인 빈도 지연입니다.*

Operational 및 Admin 이벤트 로그가 비어 있는 경우 클라이언트는 아직 작업을 시작하지 않았고 앞서 언급한 지연 기간에 있습니다. 지연을 무시하려는 경우 다음 단계를 수행합니다.
 
1. BitLocker 관리 클라이언트 서비스 서비스를 중지합니다.

2. HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**** 레지스트리 하위 키에서 **NoStartupDelay** 레지스트리 값을 만들고 해당 형식을 REG_DWORD **로**설정한 다음 값을 **1로 설정합니다.**

3. 의 **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement** **ClientWakeupFrequency** 및 **StatusReportingFrequency** 값을 **1로 설정합니다.** 이러한 값은 컴퓨터에 그룹 정책 업데이트가 적용된 후 원래 설정으로 되버려 습니다.

4. BitLocker 관리 클라이언트 서비스 서비스를 시작합니다.

서비스가 시작된 후 컴퓨터에 로컬로 로그인하고 오류가 없는 경우 1분 이내에 컴퓨터를 암호화하는 요청을 수신해야 합니다. 요청을 받지 못하면 MBAM 관리자 로그에서 오류 항목을 검토해야 합니다.

### <a name="computer-does-not-have-a-tpm-device-or-the-tpm-device-is-not-enabled-in-the-bios"></a>컴퓨터에 TPM 장치가 없는 경우 또는 BIOS에서 TPM 장치를 사용할 수 없습니다.

MBAM 관리자 이벤트 로그를 검토합니다. MBAM 관리자 이벤트 로그에 다음과 같은 이벤트 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

TPM 관리(tpm.msc)를 열고 컴퓨터에 TPM 장치가 있는지 확인합니다. tpm.msc에 디바이스가 표시되지 않는 경우 장치 관리자(devmgmt.msc)를 열고 보안 장치에서 신뢰할 수 있는 플랫폼 모듈을 확인합니다. 신뢰할 수 있는 플랫폼 모듈 장치가 없는 경우 다음 이유 중 하나에 해당될 수 있습니다.

* 시스템에 TPM/보안(신뢰할 수 있는 플랫폼 모듈) 장치가 없습니다.

* BIOS에서 TPM 장치를 사용할 수 없습니다.

* TPM 장치는 BIOS에서 사용하도록 설정되어 있지만 BIOS에서 운영 체제 설정의 TPM 장치 관리를 사용할 수 없습니다.

* TPM 장치에 Microsoft 드라이버를 사용하지 않습니다. 장치 관리자에 나열된 장치를 검토하여 Microsoft TPM 장치 드라이버를 확인합니다.

TPM 장치가 C:\Windows\System32\tpm.sys 드라이버를 사용하지 않는 경우 C:\Windows\Inf\tpm.inf 파일을 선택하여 드라이버를 업데이트해야 합니다.

### <a name="computer-does-not-have-a-valid-system-partition"></a>컴퓨터에 유효한 SYSTEM 파티션이 없습니다.

MBAM 관리자 이벤트 로그를 검토합니다. MBAM 관리자 이벤트 로그에 다음과 같은 이벤트 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

BitLocker는 암호화를 사용하도록 설정하기 위해 시스템 파티션이[필요합니다(Windows 7:](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)질문과 대답의 BitLocker 드라이브 암호화).

MBAM은 시스템 파티션을 자동으로 만들지 않습니다. BitLocker 드라이브 준비 유틸리티(bdehdcfg.exe)를 사용하여 시스템 파티션을 만들고 필요한 시작 파일을 이동할 수 있습니다.

예를 들어 **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** 명령을 사용하여 드라이브를 암호화하기 위해 MBAM을 배포하기 전에 자동으로 드라이브를 준비할 수 있습니다. 이렇게 하려면 다시 시작해야 합니다. 필요한 경우 작업을 스크립팅할 수도 있습니다. 다음 문서에서는 BitLocker 드라이브 준비 도구에 대해 설명하고 있습니다.

[BitLocker 드라이브 준비 도구에 대한 설명](https://support.microsoft.com/help/933246)

### <a name="drives-are-not-formatted-to-have-a-compatible-file-system"></a>호환되는 파일 시스템을 사용할 수 있는 드라이브의 형식이 지정되지 않은 경우

BitLocker에 대한 파일 시스템 요구 사항은 [TechNet 문서를 참조하세요.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)

### <a name="group-policy-conflict"></a>그룹 정책 충돌

MBAM 관리자 이벤트 로그에 다음과 같은 이벤트 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

그룹 정책 설정을 확인하여 MBAM 그룹 정책 설정 사이에 충돌 설정이 없는지 확인합니다.

BitLocker 드라이브 암호화 템플릿이 아닌 MDOP MBAM 템플릿을 사용하여 그룹 정책을 구성해야 합니다.

예를 들어 다음과 같은 가치를 제공해야 합니다.

운영 체제 드라이브 암호화 설정에서 보호 기능으로 TPM을 선택한 다음 시작 시 향상된 **PI 허용도 선택했습니다.** TPM 전용 보호에는 PIN이 필요하지 않습니다. 따라서 향상된 PINS 설정을 사용하지 않도록 설정해야 합니다.

### <a name="user-may-have-requested-an-exemption"></a>사용자가 면세를 요청한 것일 수 있습니다.

컴퓨터 구성\관리 템플릿\Windows 구성 요소\MDOP MBAM(BitLocker 관리)\클라이언트 관리\사용자 면제 정책 그룹 정책 구성 설정을 사용하도록 설정한 경우 사용자에게 면제 요청 옵션이 제공됩니다.

기본적으로 사용자가 면제를 요청하는 경우 면제는 7일 동안 유효하며 이 기간 동안 암호화하라는 메시지가 사용자에게 전송되지 않습니다. 정책 구성 중에 기본값을 늘리거나 낮출 수 있습니다. 면제 기간이 끝났을 때 사용자에게 암호화를 요청하는 메시지가 사용자에게 전송됩니다.

컴퓨터가 사용자 면제에 있는 경우 MBAM 관리 이벤트 로그에 다음 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

컴퓨터에 대한 사용자 제외를 수동으로 다시 설정하려면 다음 단계를 수행합니다.
 
1. 다음 레지스트리 하위 키에서 AllowUserExemption 값을 **0으로** 설정하십시오. <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. **AgentVersion,** **EncodedComputerName**및 Installed를 제외한 다음 레지스트리 하위 키의 모든 레지스트리 값을 **삭제합니다.**<br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**

    **참고** 변경 내용을 적용하려면 MBAM 에이전트를 다시 시작해야 합니다.

컴퓨터에 그룹 정책을 적용한 후 이러한 값은 원래 설정으로 되버려도 됩니다.

### <a name="wmi-issue"></a>WMI 문제

MBAM은 win32_encryptablevolume 메서드를 사용하여 BitLocker를 관리합니다. 이 모듈이 등록되지 않은 경우 또는 손상된 경우 MBAM 클라이언트가 제대로 작동하지 않으면 MBAM 관리 이벤트 로그에 다음 이벤트 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

또한 오류 코드와 함께 복구 및 하드웨어 정책이 적용되지 0x8007007e. "지정한 모듈을 찾을 수 없습니다."로 변환됩니다.

이 문제를 해결하기 위해 다음 명령을 사용하여 win32_encryptablevolume **클래스를** 다시 발급해야 합니다.

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <a name="troubleshooting-mbam-agent-communication-issues"></a>MBAM 에이전트 통신 문제 해결

이 섹션에는 MBAM 에이전트 통신과 관련된 다음과 같은 문제에 대한 문제 해결 정보가 포함되어 있습니다.

### <a name="incorrect-mbam-service-url"></a>잘못된 MBAM 서비스 URL

MBAM 준수 상태 서비스 또는 복구 및 하드웨어 서비스의 값이 올바르지 않은 경우 클라이언트 컴퓨터의 MBAM 관리자 이벤트 로그에 다음과 같은 이벤트 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

클라이언트 컴퓨터에서 다음 레지스트리 하위 키 아래에 있는 **KeyRecoveryServiceEndPoint** 및 **StatusReportingServiceEndpoint의** 값을 확인합니다. <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

기본적으로 KeyRecoveryServiceEndPoint의 URL(MBAM 복구 및 하드웨어 서비스 끝점)은 다음과 같은 형식입니다. <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

기본적으로 StatusReportingServiceEndpoint(MBAM 상태 보고 서비스 끝점)의 URL 형식은 다음과 같습니다.<br />
**http:// : \<servername\> \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> URL에는 공백이 없습니다.

서비스 URL이 올바르지 않은 경우 다음 그룹 정책 설정에서 서비스 URL을 수정해야 합니다.

**컴퓨터 구성**  >  **정책**  >  **관리 템플릿**  >  **Windows 구성 요소**  >  **MDOP MBAM(BitLocker 관리)**  >  **클라이언트 관리**  >  **MBAM 서비스 구성**

### <a name="connectivity-issue-that-affects-the-mbam-administration-server"></a>MBAM 관리 서버에 영향을 주는 연결 문제

클라이언트 에이전트와 MBAM 관리 서버 간의 연결 문제가 있는 경우 MBAM 에이전트가 데이터베이스에 업데이트를 게시할 수 없습니다. 이 경우 클라이언트 컴퓨터의 MBAM 관리자 이벤트 로그에 연결 실패 항목이 표시됩니다.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

기본 검사:

* 이름 및 IP로 MBAM 관리 서버를 ping하여 기본 연결을 검증합니다. 텔넷 또는 포트를 사용하여 MBAM 관리 웹 사이트 또는 서비스 포트에 연결할 수 있는지 여부를 확인하십시오.

* IIS 서비스가 MBAM 관리 및 모니터링 서버에서 실행되고 있으며 MBAM 웹 서비스가 MBAM 클라이언트 컴퓨터에 구성된 포트()에서 수신하는지 확인합니다. `netstat –ano | find "portnumber"`

* MBAM 웹 사이트에 대해 구성된 포트 번호가 IIS 관리자(inetmgr)를 사용하는지 확인하세요. 포트 번호가 클라이언트가 수신하는 포트 번호와 같은지 확인 다른 응용 프로그램에서 포트 번호를 공유하지 않는지 확인 예를 들어 서버의 다른 응용 프로그램에서 같은 포트를 사용하지 말아야 합니다.

* 방화벽이 있는 경우 포트가 방화벽 또는 프록시 서버에서 열려 있는지 확인 합니다.

* 클라이언트와 서버 간의 통신이 안전한 경우 유효한 SSL 인증서를 사용하고 있는지 확인하십시오.

* 삽입을 위해 데이터가 전송되는 웹 서버와 데이터베이스 서버 간의 네트워크 연결을 확인합니다. ODBC 데이터 원본 관리자를 사용하여 웹 서버에서 데이터베이스 서버로의 데이터베이스 연결을 확인할 수 있습니다. 자세한 SQL Server 연결 문제 해결 정보는 How [to Troubleshoot Connecting to the SQL Server 데이터베이스 엔진.](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)

#### <a name="troubleshooting-the-connectivity-issue"></a>연결 문제 해결

클라이언트에 구성된 서비스 URL이 올바른지 확인합니다. 레지스트리에서 KeyRecoveryServiceEndPoint(HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement** )에 **대한 URL 값을 복사한 후 레지스트리에서 Internet Explorer.

마찬가지로 StatusReportingServiceEndpoint(HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement)에 대한 URL** **값을 복사하고 에서 Internet Explorer.

> [!Note]
> 클라이언트 컴퓨터에서 URL을 찾을 수 없는 경우 클라이언트에서 IIS를 실행하는 서버로의 기본 네트워크 연결을 테스트해야 합니다. 이전 섹션에서 포인트 1, 2, 3 및 4를 참조하세요.

또한 관리 및 모니터링 서버의 응용 프로그램 로그에서 오류가 발생하는지 검토합니다.

클라이언트와 서버 간에 동시 네트워크 추적을 만들 수 있으며 추적을 검토하여 클라이언트 에이전트와 MBAM 관리 서버 간의 연결 실패의 원인을 확인할 수 있습니다.

> [!Note]
> 클라이언트 컴퓨터에서 서비스 URL을 검색할 수 있으며 MBAM 관리 이벤트 로그에 연결 오류 항목이 있는 경우 관리 서버와 데이터베이스 서버 간의 연결 실패로 인한 것일 수 있습니다.

두 서비스 URL을 모두 검색할 수 있으며 클라이언트와 실행 중인 서버 간에 연결이 있는 경우 IIS가 작동하고 있습니다. 그러나 IIS를 실행하는 서버와 데이터베이스 서버 간의 통신에 문제가 있을 수 있습니다.

네트워크 문제 또는 잘못된 데이터베이스 연결 문자열 설정 때문에 MBAM 서비스가 데이터베이스 서버에 연결하지 못할 수 있습니다. 관리 및 모니터링 서버의 응용 프로그램 로그를 검토합니다. 원본 2.0.ASP.NET 2.0.50727.0에서 오류 항목 또는 경고가 표시될 수 있습니다.

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <a name="possible-causes"></a>가능한 원인

##### <a name="cause-1"></a>원인 1

관리자가 관리 및 모니터링 서버 구성 요소를 설치하는 동안 잘못된 데이터베이스 인스턴스 이름/데이터베이스 이름을 지정한 것일 수 있습니다.

IIS 관리 콘솔을 사용하여 데이터베이스 연결 문자열을 확인하고 수정할 수 있습니다. 이 작업을 위해 IIS 관리자를 열고 Microsoft BitLocker 관리 및 모니터링을 검색합니다. 왼쪽에 나열된 각 서비스에 대해 다음 단계에 따라 데이터베이스 연결 문자열을 변경합니다.

1. 기능 **보기에서**연결 **문자열을 두 번 선택합니다.**

2. 연결 **문자열 페이지에서** 변경할 연결 문자열을 선택합니다.

3. 작업 **창에서** 편집 을 **선택합니다.**

4. 연결 **문자열 편집** 대화 상자에서 변경할 속성을 변경한 다음 확인 을 **선택합니다.**

##### <a name="cause-2"></a>원인 2

SQL Server 차단된 포트입니다. 수신하도록 구성된 포트 SQL Server 확인하고 관리 서버와 데이터베이스 서버 간의 방화벽에서 포트가 열려 있는지 확인해야 합니다.

##### <a name="cause-3"></a>원인 3

서버 SQL TCP/IP 바인딩이 잘못되었습니다. 데이터베이스 SQL TCP/IP 바인딩의 SQL Server 구성 관리자 확인 MBAM을 사용하려면 TCP/IP 및 명명된 파이프 프로토콜을 사용하여 데이터베이스에 연결해야 합니다.

##### <a name="cause-4"></a>원인 4

NT Authority\Network Service 계정 또는 MBAM 관리 서버의 컴퓨터 계정에는 SQL 데이터베이스에 연결하는 데 필요한 권한이 없습니다.

데이터베이스 서버에 데이터베이스 구성 요소를 설치하는 동안 설치 관리자에서 MBAM 준수 감사 DB 액세스와 MBAM 복구 및 하드웨어 DB 액세스의 두 로컬 그룹을 만듭니다.

NT Authority\Network Service 계정, MBAM 관리 서버의 컴퓨터 계정 및 데이터베이스 구성 요소를 설치하는 사용자가 이러한 그룹에 자동으로 추가됩니다.

이러한 그룹에는 설치 중에 데이터베이스에 대한 필수 권한이 부여됩니다. 이 그룹에 참여하는 모든 사용자는 데이터베이스에 대한 필요한 사용 권한을 자동으로 받게 됩니다.

다음 조건 중 하나 이상이 참인 경우 사용 권한 문제로 인하여 웹 서비스가 데이터베이스 서버에 연결되지 않을 수 있습니다.

* 앞에서 언급한 그룹은 데이터베이스 서버의 로컬 그룹에서 제거됩니다.

* NT Authority\Network Service 계정 및 MBAM 관리 서버의 컴퓨터 계정은 이러한 그룹의 구성원이 아니기 때문에

* 이러한 그룹에는 데이터베이스에 대한 필수 권한이 없습니다.

MBAM 관리 및 모니터링 서버의 응용 프로그램 로그에서 이전 조건이 참인 경우 사용 권한 관련 오류가 표시됩니다. 이 경우 NT Authority\Network Service 계정 및 MBAM 관리 서버의 컴퓨터 계정을 수동으로 추가하고 2013을 사용하는 SQL 데이터베이스 서버에 서버 전체 공용 역할을 https://msdn.microsoft.com/library/aa337562.aspx) SQL Server Management Studio.

#### <a name="review-the-web-service-logs"></a>웹 서비스 로그 검토

MBAM 관리 서버의 응용 프로그램 로그에 이벤트가 기록되지 않은 경우 MBAM 관리 및 모니터링 서버에서 호스팅되는 MBAM 웹 서비스의 웹 서비스 로그(.svclog)를 검토해야 합니다. 로그 파일을 확인하려면 서비스 추적 뷰어 SvcTraceViewer.exe(서비스 추적 뷰어 도구)를 https://msdn.microsoft.com/library/ms732023.aspx 사용해야 합니다.

복구 및HardwareService 및 ComplianceStatusService의 서비스 추적 로그를 주로 조사해야 합니다. 기본적으로 웹 서비스 로그는 C:\inetpub\Microsoft BitLocker Management Solution\Logs 폴더에 있습니다. 이 폴더에서 각 서비스는 해당 .svclog 파일을 자체 폴더 아래에 쓴다.

오류 또는 경고 항목이 있는 경우 서비스 추적 로그의 활동을 검토합니다. 기본적으로 오류 항목은 빨간색으로 강조 표시됩니다. 추적 뷰어의 오른쪽 창에서 오류 설명을 선택하여 오류 항목에 대한 자세한 정보를 볼 수 있습니다. 다음은 추적 로그의 예제 오류 항목입니다.

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <a name="re-installation-or-reconfiguration-of-mbam-infrastructure"></a>MBAM 인프라 다시 설치 또는 재구성

MBAM 인프라를 다시 설치하거나 다시 구성하려면 다음을 알아야 합니다.

* 응용 프로그램 풀 계정

* MBAM 그룹(Helpdesk, Advanced, Report Users Group)

* MBAM 보고서 URL

* SQL Server 이름 및 데이터베이스 이름

* MBAM ReadWrite 및 ReadOnly 계정

### <a name="application-pool-account"></a>응용 프로그램 풀 계정

응용 프로그램 풀 계정을 찾으하려면 MBAM 웹 서버에 로그온하고 **IIS(인터넷 정보 서비스 관리자)를 연**다음 응용 프로그램 풀을 **선택합니다.**

![응용 프로그램 풀.](images/troubleshooting-MBAM-installation-1.png)

SPN(서비스 사용자 이름)은 이 계정에서 설정해야 합니다. 이 설정은 MBAM의 기능에 매우 중요합니다.

### <a name="mbam-groups-helpdesk-advanced-report-users-group-and-reports-url"></a>MBAM 그룹(Helpdesk, Advanced, Report Users Group and Reports URL)

![MBAM 그룹.](images/troubleshooting-MBAM-installation-2.png)

기술 지원 서비스 그룹, 고급 헬프데스크 그룹, 보고서 사용자 그룹 및 MBAM 보고서 URL과 같은 정보를 제공합니다. MBAM 보고서 URL은 MBAM 설정에서 제공해야 하며 http(s)://servername/ReportServer로 읽어야 합니다.

### <a name="sql-server-name-and-database-db-names"></a>SQL Server 및 데이터베이스(DB) 이름

MBAM DB를 호스팅하는 SQL Server 이름 및 인스턴스를 찾으하려면 MBAM 웹(IIS) 서버에 로그온하고 MBAM 레지스트리 하위 키로 찾은 다음을 실행합니다.

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit.](images/troubleshooting-MBAM-installation-3.png)

강조 표시된 부분은 연결 문자열입니다. 이름, SQL Server 인스턴스(명명된 경우)를 지정해야 합니다.

### <a name="mbam-readwrite-and-readonly-accounts"></a>MBAM ReadWrite 및 ReadOnly 계정

이 정보는 웹 SQL Server 이미 찾은 데이터베이스의 이름입니다.

#### <a name="readwrite-account"></a>ReadWrite 계정

1. 로그인한 SQL Management Studio.

2. **MBAM 복구**및 하드웨어를 마우스 오른쪽 단추로 클릭하고 **속성을**선택한 다음 사용 **권한을 선택합니다.**

예를 들어 랩 계정 이름은 **MBAMWrite입니다.** 응용 프로그램 풀 및 ReadWrite 계정은 동일하게 설정됩니다.

![SQL DB.](images/troubleshooting-MBAM-installation-4.png)

![DB 속성](images/troubleshooting-MBAM-installation-5.png)

보안으로 **를 검색한** 다음 **로그인을** SQL Management Studio. 이전 스크린샷에 표시된 계정으로 검색합니다.

![SQL 보안.](images/troubleshooting-MBAM-installation-6.png)

계정을 마우스 오른쪽 단추로 클릭하고 속성 **사용자**매핑으로 이동하여 MBAM 복구 및 하드웨어 데이터베이스를 찾습니다.

![사용자 매핑.](images/troubleshooting-MBAM-installation-7.png)

#### <a name="readonly-account"></a>ReadOnly 계정

SSRS SQL Server Reporting Services Configuration Manager를 열 수 있습니다. 보고서 **관리자 URL 을 선택한**다음 **URL을 검색합니다.**

![보고서 관리자.](images/troubleshooting-MBAM-installation-8.png)

**Microsoft Bitlocker 관리 및 모니터링을 선택합니다.**

![Bitlocker 관리 및 모니터링.](images/troubleshooting-MBAM-installation-9.png)

**MaltaDatasource를 선택합니다.**

![DB.](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource.](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource에는 ReadOnly 계정 이름이 필요하며 MBAM 설정에서 사용해야 합니다.

## <a name="reference"></a>참조

자세한 내용은 다음 문서를 참조하세요.

[독립 실행형 구성에서 MBAM 2.5 배포](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker 관리 및 모니터링 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
