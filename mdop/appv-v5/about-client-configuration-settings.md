---
title: 클라이언트 구성 설정 정보
description: 클라이언트 구성 설정 정보
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814940"
---
# 클라이언트 구성 설정 정보


Microsoft App-v (Application Virtualization) 5.0 클라이언트는 레지스트리에 구성을 저장 합니다. 레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다. 레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다. 이 항목에서는 App-v 5.0 클라이언트 구성 설정을 나열 하 고 해당 사용에 대해 설명 합니다. PowerShell을 사용 하 여 클라이언트 구성 설정을 수정할 수 있습니다. PowerShell 및 App-v 5.0 사용에 대 한 자세한 내용은 PowerShell을 [사용 하 여 App-v 관리](administering-app-v-by-using-powershell.md)를 참조 하세요.

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> 앱-V 5.0 클라이언트 구성 설정


다음 표에서는 App-v 5.0 클라이언트 구성 설정에 대 한 정보를 보여 줍니다.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">설정 이름</th>
<th align="left">설정 플래그</th>
<th align="left">설명</th>
<th align="left">설정 옵션</th>
<th align="left">레지스트리 키 값</th>
<th align="left">설정 되지 않은 정책 상태 키 및 값</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Package설치 루트</p></td>
<td align="left"><p>PACKAGE설치 루트</p></td>
<td align="left"><p>모든 새 응용 프로그램과 업데이트가 설치 되는 디렉터리를 지정 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>패키지 콘텐츠를 다운로드할 원본 위치를 재정의 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>이 설정은 데이터 통신 네트워크 연결을 통해 연결 된 Windows 8 컴퓨터에서 가상화 된 응용 프로그램을 시작할지 여부를 제어 합니다 (예: 4G).</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>삭제 된 세션을 다시 시도할 횟수를 지정 합니다.</p></td>
<td align="left"><p>Integer (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>삭제 된 세션을 다시 시도 하는 간격 (초)을 지정 합니다.</p></td>
<td align="left"><p>Integer (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>AUTOLOAD</p></td>
<td align="left"><p>새 패키지를 앱-V가 특정 컴퓨터에서 자동으로 로드 하는 방법을 지정 합니다.</p></td>
<td align="left"><p>(0x0) 없음; (0x1) 이전에 사용한 경우 (0x2) 모두</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocationProvider</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>IAppvPackageLocationProvider 인터페이스의 호환 되는 구현에 대 한 CLSID를 지정 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>인증서 저장소의 유효한 인증서에 대 한 경로를 지정 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>HTTPS를 사용 steaming 전에 서버 인증서 해지 상태를 확인 합니다.</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>스트리밍된 패키지 콘텐츠를 로컬 하드 디스크에 저장 하지 않도록 지정 합니다.</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이름</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>게시 서버의 이름을 표시 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ FriendlyName</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>게시 서버의 URL을 표시 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ URL</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>전역 게시 새로 고침을 사용 하도록 설정 합니다 (부울).</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>로그온 시 전역 게시 새로 고침을 트리거합니다. 나타내는</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>GlobalRefreshIntervalUnit을 사용 하 여 게시 새로 고침 간격을 지정 합니다. 패키지 새로 고침을 사용 하지 않도록 설정 하려면 0을 선택 합니다.</p></td>
<td align="left"><p>Integer (0-744</p></td>
<td align="left"><p>Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>간격 단위 (시간 0-23, 일 0-31)를 지정 합니다. </p></td>
<td align="left"><p>0 시간에 해당 하 고 1 일 동안</p></td>
<td align="left"><p>Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>raid-1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>사용자 게시 새로 고침을 사용 하도록 설정 합니다 (부울).</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>사용자 게시 새로 고침 onlogon을 트리거합니다. 나타내는</p>
<p>단어 개수 (공백 포함): 60</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>UserRefreshIntervalUnit을 사용 하 여 게시 새로 고침 간격을 지정 합니다. 패키지 새로 고침을 사용 하지 않도록 설정 하려면 0을 선택 합니다.</p>
<p>단어 개수 (공백 포함): 85</p></td>
<td align="left"><p>Integer (0-744 시간)</p></td>
<td align="left"><p>Publishing\Servers{serverId}\UserPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> . <strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>간격 단위 (시간 0-23, 일 0-31)를 지정 합니다. </p></td>
<td align="left"><p>0 시간에 해당 하 고 1 일 동안</p></td>
<td align="left"><p>Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>raid-1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MigrationMode</p></td>
<td align="left"><p>MIGRATIONMODE</p></td>
<td align="left"><p>마이그레이션 모드는 App-v 클라이언트에서 이전 버전의 App-v를 사용 하 여 만든 패키지에 대 한 바로 가기 및 FTA 수정할 수 있도록 합니다.</p></td>
<td align="left"><p>True (enabled 상태), False (비활성 상태)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>앱-V 5.0 클라이언트를 실행 하는 컴퓨터가 특정 사용 정보를 수집 하 고 반환할 수 있도록 하 여 응용 프로그램을 더욱 개선 하는 데 도움을 드립니다.</p></td>
<td align="left"><p>사용 안 함: 0 사용 하도록 설정 1</p></td>
<td align="left"><p>소프트웨어/Microsoft/AppV/CEIP/CEIPEnable</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>실행 해야 하는 구성 파일의 패키지 매니페스트에 정의 된 스크립트를 사용 하도록 설정 합니다.</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>사용자&#39;s 프로필을 사용 하 여 로밍 하지 않는% userprofile%를 기준으로 하는 파일 경로를 지정 합니다. 사용 예:/ROAMINGFILEEXCLUSIONS =&#39;desktop, 내 사진&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>사용자 프로필로 로밍되지 않는 레지스트리 경로를 지정 합니다. 사용 예:/ROAMINGREGISTRYEXCLUSIONS = \\수업, \클라이언트</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>사용자가 게시 한 패키지의 현재 버전과 연결 된 심볼 링크를 만들 위치를 지정 합니다. 바로 가기 및 파일 형식 연결 등의 모든 가상 응용 프로그램 확장은이 경로를 가리킵니다. 경로를 지정 하지 않으면 패키지를 게시할 때 기호화 된 링크가 사용 되지 않습니다. 예:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>전역으로 게시 된 패키지의 현재 버전과 연결 된 심볼 링크를 만들 위치를 지정 합니다. 바로 가기 및 파일 형식 연결 등의 모든 가상 응용 프로그램 확장은이 경로를 가리킵니다. 경로를 지정 하지 않으면 패키지를 게시할 때 기호화 된 링크가 사용 되지 않습니다. 예:%allusersprofile%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>로컬에 설치 된 응용 프로그램을 가상 환경에서 실행할 수 있는지 확인 하는 데 사용할 수 있는 쉼표로 구분 된 파일 확장명 목록입니다.</p>
<p>게시 하는 동안 바로 가기, FTAs 및 기타 확장 지점을 만들면 앱-V는 확장 지점과 연결 된 응용 프로그램이 로컬에 설치 되어 있는 경우 목록에 확장명을 비교 합니다. 확장명이 있으면 <strong> runvirtual </strong> command 명령줄 매개 변수가 추가 되 고 응용 프로그램이 가상으로 실행 됩니다.</p>
<p><strong>Runvirtual 매개 변수에 대 한 자세한 내용은 </strong> 가상화 된 <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> 응용 프로그램을 사용 하 여 가상 환경 내에서 로컬로 설치 된 응용 프로그램 실행을 참조 하세요 </a> .</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>기록 되지 않은 정책 값</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>클라이언트가 보고 서버로 정보를 반환할 수 있도록 합니다.</p></td>
<td align="left"><p>True (enabled), False (비활성 상태)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>클라이언트 정보가 저장 되는 보고 서버의 위치를 지정 합니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다. 크기는 메모리의 캐시에 적용 됩니다. 제한에 도달 하면 로그 파일이 롤오버 됩니다. 0에서 1024 사이를 설정 합니다.</p></td>
<td align="left"><p>Integer [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>업로드 요청을 보고 하기 위해 서버로 전송할 최대 크기 (바이트)를 지정 합니다. 이는 로그가 유효 크기에 도달 했을 때 영구 전송 오류를 방지 하는 데 도움이 됩니다. 1024에서 무제한으로 설정 합니다.</p></td>
<td align="left"><p>Integer [1024-무제한]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>보고서 서버에 데이터를 보내는 클라이언트를 시작 하는 시간을 지정 합니다. 일일 시간에 해당 하는 0-23 사이의 유효한 정수를 지정 해야 합니다. 기본적으로 <strong> ReportingStartTime는 </strong> 현재 날짜에서 10 P. M 또는 22로 시작 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>App-v 5.0 클라이언트를 실행 하는 컴퓨터가 오프 라인 상태가 될 가능성이 적은 시간으로이 설정을 구성 해야 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>Integer (0-23)</p></td>
<td align="left"><p>보고 \ StartTime</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>클라이언트가 보고 서버에 데이터를 재전송 하는 데 사용할 다시 시도 간격을 지정 합니다.</p></td>
<td align="left"><p>정수</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>보고 서버로 데이터를 보낼 최대 지연 시간 (분)을 지정 합니다. 예약 된 작업이 시작 되 면 클라이언트는 0과 ReportingRandomDelay 사이의 임의 지연 시간을 <strong> 생성 </strong> 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다. 서버에서 충돌을 방지 하는 데 도움이 될 수 있습니다.</p></td>
<td align="left"><p>Integer [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>중요</strong><br/><p>이 설정은 App-v 5.0 SP2 이상 에서만 사용할 수 있습니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>지원 되는 셸 확장, 브라우저 도우미 개체 및 Active X 컨트롤을 가상 응용 프로그램을 사용 하 여 가상화 하 고 실행할 수 있도록 합니다.</p></td>
<td align="left"><p>1 (사용), 0 (사용 안 함)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>중요</strong><br/><p>이 설정은 App-v 5.0 SP2 에서만 사용할 수 있습니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>App-v 5.0 클라이언트를 실행 하는 컴퓨터에 대해 게시 새로 고침 진행률 표시줄을 사용 하도록 설정 합니다.</p></td>
<td align="left"><p>1 (사용), 0 (사용 안 함)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>중요</strong><br/><p>이 설정은 App-v 5.0 SP2 에서만 사용할 수 있습니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>게시 새로 고침 진행률 표시줄을 숨깁니다.</p></td>
<td align="left"><p>1 (사용), 0 (사용 안 함)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>사용할 수 없음</p></td>
<td align="left"><p>동적 가상화를 사용 하기 위한 후보 (지원 되는 셸 확장, 브라우저 도우미 개체 및 ActiveX 컨트롤) 인 프로세스 경로 목록 (와일드 카드를 포함할 수 있음)을 지정 합니다. 전체 경로가 이러한 항목 중 하 나와 일치 하는 프로세스만 동적 가상화를 사용할 수 있습니다.</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>빈 문자열입니다.</p></td>
</tr>
</tbody>
</table>








## 관련 항목


[App-V 5.0 Sequencer 및 Client 배포](deploying-the-app-v-50-sequencer-and-client.md)

[ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[App-V Client 배포 방법](how-to-deploy-the-app-v-client-gb18030.md)









