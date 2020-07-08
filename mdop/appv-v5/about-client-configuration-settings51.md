---
title: 클라이언트 구성 설정 정보
description: 클라이언트 구성 설정 정보
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814945"
---
# 클라이언트 구성 설정 정보


Microsoft App-v (Application Virtualization) 5.1 클라이언트는 레지스트리에 구성을 저장 합니다. 레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다. 레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다. 이 항목에서는 App-v 5.1 클라이언트 구성 설정을 나열 하 고 해당 사용에 대해 설명 합니다. PowerShell을 사용 하 여 클라이언트 구성 설정을 수정할 수 있습니다. PowerShell 및 App-v 5.1 사용에 대 한 자세한 내용은 PowerShell을 [사용 하 여 app-v 5.1 관리](administering-app-v-51-by-using-powershell.md)를 참조 하세요.

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> 앱-V 5.1 클라이언트 구성 설정


다음 표에서는 App-v 5.1 클라이언트 구성 설정에 대 한 정보를 보여 줍니다.

|설정 이름 | 설정 플래그 | 설명 | 설정 옵션 | 레지스트리 키 값 | 설정 되지 않은 정책 상태 키 및 값 |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| Package설치 루트 | PACKAGE설치 루트 | 모든 새 응용 프로그램과 업데이트가 설치 되는 디렉터리를 지정 합니다. | 문자열 | Streaming\PackageInstallationRoot | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| PackageSourceRoot | PACKAGESOURCEROOT | 패키지 콘텐츠를 다운로드할 원본 위치를 재정의 합니다. | 문자열 | Streaming\PackageSourceRoot | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| AllowHighCostLaunch | 사용할 수 없음 |이 설정은 데이터 통신 네트워크 연결을 통해 연결 된 Windows 10 컴퓨터에서 가상화 된 응용 프로그램을 시작할지 여부를 제어 합니다 (예: 4G). | True (enabled), False (비활성 상태) | Streaming\AllowHighCostLaunch | 0 |
| ReestablishmentRetries | 사용할 수 없음 | 삭제 된 세션을 다시 시도할 횟수를 지정 합니다. | Integer (0-99) | Streaming\ReestablishmentRetries | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| ReestablishmentInterval | 사용할 수 없음 | 삭제 된 세션을 다시 시도 하는 간격 (초)을 지정 합니다. | Integer (0-3600) | Streaming\ReestablishmentInterval | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| LocationProvider | 사용할 수 없음 | IAppvPackageLocationProvider 인터페이스의 호환 되는 구현에 대 한 CLSID를 지정 합니다. | 문자열 | Streaming\LocationProvider | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| CertFilterForClientSsl | 사용할 수 없음 | 인증서 저장소의 유효한 인증서에 대 한 경로를 지정 합니다. | 문자열 | Streaming\CertFilterForClientSsl | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| VerifyCertificateRevocationList | 사용할 수 없음 | HTTPS를 사용 steaming 전에 서버 인증서 해지 상태를 확인 합니다. | True (enabled), False (비활성 상태) | Streaming\VerifyCertificateRevocationList | 0 |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | 스트리밍된 패키지 콘텐츠를 로컬 하드 디스크에 저장 하지 않도록 지정 합니다. | True (enabled), False (비활성 상태) | Streaming\SharedContentStoreMode | 0 |
| 이름<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | PUBLISHINGSERVERNAME | 게시 서버의 이름을 표시 합니다. | 문자열 | Publishing\Servers\ {serverId} \ FriendlyName | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| URL<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | PUBLISHINGSERVERURL | 게시 서버의 URL을 표시 합니다. | 문자열 | Publishing\Servers\ {serverId} \ URL | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| GlobalRefreshEnabled<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | GLOBALREFRESHENABLED | 전역 게시 새로 고침을 사용 하도록 설정 합니다 (부울). | True (enabled), False (비활성 상태) | Publishing\Servers\ {serverId} \ GlobalEnabled | False |
| GlobalRefreshOnLogon<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | GLOBALREFRESHONLOGON | 로그온 시 전역 게시 새로 고침을 트리거합니다. 나타내는 | True (enabled), False (비활성 상태) | Publishing\Servers\ {serverId} \ GlobalLogonRefresh | False |
| GlobalRefreshInterval<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | GLOBALREFRESHINTERVAL | GlobalRefreshIntervalUnit을 사용 하 여 게시 새로 고침 간격을 지정 합니다. 패키지 새로 고침을 사용 하지 않도록 설정 하려면 0을 선택 합니다. | Integer (0-744) | Publishing\Servers\{serverId}\GlobalPeriodicRefreshInterval | 0 |
| GlobalRefreshIntervalUnit <br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | GLOBALREFRESHINTERVALUNI | 간격 단위 (시간 0-23, 일 0-31)를 지정 합니다. | 0 시간에 해당 하 고 1 일 동안 | Publishing\Servers\{serverId}\GlobalPeriodicRefreshIntervalUnit | raid-1 |
| UserRefreshEnabled<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | USERREFRESHENABLED | 사용자 게시 새로 고침을 사용 하도록 설정 합니다 (부울). | True (enabled), False (비활성 상태) | Publishing\Servers\ {serverId} \ UserEnabled | False |
| UserRefreshOnLogon<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | USERREFRESHONLOGON | 사용자 게시 새로 고침 onlogon을 트리거합니다. 나타내는<br>단어 개수 (공백 포함): 60 | True (enabled), False (비활성 상태) | Publishing\Servers\ {serverId} \ UserLogonRefresh | False |
| UserRefreshInterval<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | USERREFRESHINTERVAL | UserRefreshIntervalUnit을 사용 하 여 게시 새로 고침 간격을 지정 합니다. 패키지 새로 고침을 사용 하지 않도록 설정 하려면 0을 선택 합니다. | 단어 개수 (공백 포함): 85<br>Integer (0-744 시간) | Publishing\Servers\{serverId}\UserPeriodicRefreshInterval | 0 |
| UserRefreshIntervalUnit<br>**참고** 이 설정은 **set-AppvclientConfiguration** cmdLet을 사용 하 여 수정할 수 없습니다. **Set-AppvPublishingServer** cmdlet을 사용 해야 합니다. | USERREFRESHINTERVALUNIT | 간격 단위 (시간 0-23, 일 0-31)를 지정 합니다. | 0 시간에 해당 하 고 1 일 동안 | Publishing\Servers\{serverId}\UserPeriodicRefreshIntervalUnit | raid-1 |
| MigrationMode | MIGRATIONMODE | 마이그레이션 모드는 App-v 클라이언트에서 이전 버전의 App-v를 사용 하 여 만든 패키지에 대 한 바로 가기 및 FTA 수정할 수 있도록 합니다. | True (enabled 상태), False (비활성 상태) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | 앱-V 5.1 클라이언트를 실행 하는 컴퓨터가 특정 사용 정보를 수집 하 고 반환할 수 있도록 하 여 응용 프로그램을 더욱 개선 하는 데 도움을 드립니다. | 사용 안 함: 0 사용 하도록 설정 1 | 소프트웨어/Microsoft/AppV/CEIP/CEIPEnable | 0 | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | 실행 해야 하는 구성 파일의 패키지 매니페스트에 정의 된 스크립트를 사용 하도록 설정 합니다. | True (enabled), False (비활성 상태) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | 사용자 프로필을 사용 하 여 로밍 하지 않는% userprofile%를 기준으로 파일 경로를 지정 합니다. 사용 예:/ROAMINGFILEEXCLUSIONS = ' desktop; my pictures ' | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | 사용자 프로필로 로밍되지 않는 레지스트리 경로를 지정 합니다. 사용 예:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | 문자열 | Integration\RoamingRegistryExclusions | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| IntegrationRootUser | 사용할 수 없음 | 사용자가 게시 한 패키지의 현재 버전과 연결 된 심볼 링크를 만들 위치를 지정 합니다. 바로 가기 및 파일 형식 연결 등의 모든 가상 응용 프로그램 확장은이 경로를 가리킵니다. 경로를 지정 하지 않으면 패키지를 게시할 때 기호화 된 링크가 사용 되지 않습니다. 예:%localappdata%\Microsoft\AppV\Client\Integration.| 문자열 | Integration\IntegrationRootUser | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
|IntegrationRootGlobal | 사용할 수 없음| 전역으로 게시 된 패키지의 현재 버전과 연결 된 심볼 링크를 만들 위치를 지정 합니다. 바로 가기 및 파일 형식 연결 등의 모든 가상 응용 프로그램 확장은이 경로를 가리킵니다. 경로를 지정 하지 않으면 패키지를 게시할 때 기호화 된 링크가 사용 되지 않습니다. 예:%allusersprofile%\Microsoft\AppV\Client\Integration | 문자열 | Integration\IntegrationRootGlobal | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| VirtualizableExtensions | 사용할 수 없음 | 로컬에 설치 된 응용 프로그램을 가상 환경에서 실행할 수 있는지 확인 하는 데 사용할 수 있는 쉼표로 구분 된 파일 확장명 목록입니다.<br>게시 하는 동안 바로 가기, FTAs 및 기타 확장 지점을 만들면 앱-V는 확장 지점과 연결 된 응용 프로그램이 로컬에 설치 되어 있는 경우 목록에 확장명을 비교 합니다. 확장명이 있으면 **Runvirtual** command 명령줄 매개 변수가 추가 되 고 응용 프로그램이 가상으로 실행 됩니다.<br>**Runvirtual** 매개 변수에 대 한 자세한 내용은 가상화 된 [응용 프로그램을 사용 하 여 가상 환경 내에서 로컬로 설치 된 응용 프로그램 실행](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md)을 참조 하세요. | 문자열 | Integration\VirtualizableExtensions | 기록 되지 않은 정책 값 |
| ReportingEnabled | 사용할 수 없음 | 클라이언트가 보고 서버로 정보를 반환할 수 있도록 합니다. | True (enabled), False (비활성 상태) | Reporting\EnableReporting | False |
| ReportingServerURL | 사용할 수 없음 | 클라이언트 정보가 저장 되는 보고 서버의 위치를 지정 합니다. | 문자열 | Reporting\ReportingServer | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| ReportingDataCacheLimit | 사용할 수 없음 | 보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다. 크기는 메모리의 캐시에 적용 됩니다. 제한에 도달 하면 로그 파일이 롤오버 됩니다. 0에서 1024 사이를 설정 합니다. | Integer [0-1024] | Reporting\DataCacheLimit | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| ReportingDataBlockSize| 사용할 수 없음 | 업로드 요청을 보고 하기 위해 서버로 전송할 최대 크기 (바이트)를 지정 합니다. 이는 로그가 유효 크기에 도달 했을 때 영구 전송 오류를 방지 하는 데 도움이 됩니다. 1024에서 무제한으로 설정 합니다. | Integer [1024-무제한] | Reporting\DataBlockSize | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| ReportingStartTime | 사용할 수 없음 | 보고서 서버에 데이터를 보내는 클라이언트를 시작 하는 시간을 지정 합니다. 일일 시간에 해당 하는 0-23 사이의 유효한 정수를 지정 해야 합니다. 기본적으로 **ReportingStartTime** 는 현재 날짜에서 10 P. M 또는 22로 시작 됩니다.<br>**참고** App-v 5.1 클라이언트를 실행 하는 컴퓨터가 오프 라인 상태가 될 가능성이 적은 시간으로이 설정을 구성 해야 합니다. | Integer (0-23) | 보고 \ StartTime | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| ReportingInterval | 사용할 수 없음 | 클라이언트가 보고 서버에 데이터를 재전송 하는 데 사용할 다시 시도 간격을 지정 합니다. | 정수 | Reporting\RetryInterval | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| ReportingRandomDelay | 사용할 수 없음 | 보고 서버로 데이터를 보낼 최대 지연 시간 (분)을 지정 합니다. 예약 된 작업이 시작 되 면 클라이언트는 0과 **ReportingRandomDelay** 사이의 임의 지연 시간을 생성 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다. 서버에서 충돌을 방지 하는 데 도움이 될 수 있습니다. | Integer [0-ReportingRandomDelay] | Reporting\RandomDelay | 정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음) |
| EnableDynamicVirtualization<br>**중요** 이 설정은 App-v 5.0 SP2 이상 에서만 사용할 수 있습니다. | 사용할 수 없음 | 지원 되는 셸 확장, 브라우저 도우미 개체 및 Active X 컨트롤을 가상 응용 프로그램을 사용 하 여 가상화 하 고 실행할 수 있도록 합니다. | 1 (사용), 0 (사용 안 함) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization | |
| EnablePublishingRefreshUI<br>**중요** 이 설정은 App-v 5.0 SP2 에서만 사용할 수 있습니다. | 사용할 수 없음 | App-v 5.1 클라이언트를 실행 하는 컴퓨터에 대해 게시 새로 고침 진행률 표시줄을 사용 하도록 설정 합니다. | 1 (사용), 0 (사용 안 함) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing | |
| HideUI<br>**중요**  이 설정은 App-v 5.0 SP2 에서만 사용할 수 있습니다.| 사용할 수 없음 | 게시 새로 고침 진행률 표시줄을 숨깁니다. | 1 (사용), 0 (사용 안 함) | | |
| ProcessesUsingVirtualComponents | 사용할 수 없음 | 동적 가상화를 사용 하기 위한 후보 (지원 되는 셸 확장, 브라우저 도우미 개체 및 ActiveX 컨트롤) 인 프로세스 경로 목록 (와일드 카드를 포함할 수 있음)을 지정 합니다. 전체 경로가 이러한 항목 중 하 나와 일치 하는 프로세스만 동적 가상화를 사용할 수 있습니다. | 문자열 | Virtualization\ProcessesUsingVirtualComponents | 빈 문자열입니다. |






## 관련 항목


[App-V 5.1 Sequencer 및 Client 배포](deploying-the-app-v-51-sequencer-and-client.md)

[ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.1 Client 구성을 수정하는 방법](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[App-V Client 배포 방법](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





