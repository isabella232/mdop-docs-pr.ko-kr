---
title: MED-V 작업 영역 구성 설정 관리
description: MED-V 작업 영역 구성 설정 관리
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826158"
---
# MED-V 작업 영역 구성 설정 관리


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0은 레지스트리에 구성 설정을 저장 합니다. 여기에 포함 된 정보는 MED-V 서비스를 더 잘 관리 하는 데 도움이 될 수 있습니다.

MED-V는 결과 설정 값을 찾을 때 다음 검색 경로를 사용 합니다.

MED-V는 먼저 컴퓨터 정책을 찾습니다.

값이 없는 경우 MED-V는 사용자 정책을 찾습니다.

값이 없는 경우 MED-V는 HKEY \ _LOCAL \ _MACHINE \\System 하이브를 찾습니다.

값이 없는 경우 MED-V는 HKEY \ _CURRENT 사용자 레지스트리 하이브를 찾습니다.

여전히 값이 없는 경우 MED-V는 기본값을 사용 합니다.

일반적으로 HKEY \ _LOCAL \ _MACHINE \\System hive 또는 컴퓨터 정책에 값을 설정 하는 것이 가장 좋습니다. 그러나 최종 사용자가 특정 설정을 구성할 수 있도록 하려면 종료 해야 합니다.

**참고**  
MED-V 작업 영역을 배포 하기 전에, 스크립트 편집기를 사용 하 여 MED-V 작업 영역 포장기에서 만든 Windows PowerShell 스크립트 (ps1 파일)를 변경할 수 있습니다. 자세한 내용은 [Windows PowerShell을 사용 하 여 고급 설정 구성을](configuring-advanced-settings-by-using-windows-powershell.md)참조 하세요.

MED-V 작업 영역을 배포한 후에는 레지스트리 항목을 편집 하 여 특정 MED-V 구성 설정을 변경할 수 있습니다.



이 섹션에는 구성 가능한 모든 MED-V 레지스트리 키와 사용에 대 한 설명이 나와 있습니다.

## 진단 키


다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">Data/Default </th>
<th align="left">설명 </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 3</p></td>
<td align="left"><p>이벤트 로그에 기록 되는 정보의 유형입니다. 수준에는 0 (없음), 1 (오류), 2 (경고), 3 (정보), 4 (디버그)가 포함 됩니다.</p></td>
</tr>
</tbody>
</table>



## Fts 키


다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">유형</th>
<th align="left">Data/Default</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>처음 설치 시 관리자에 게 자동으로 최종 사용자를 추가할지 여부를 구성&#39;s 그룹에 추가 합니다. 0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 처음 설치 시 관리자에 게 최종 사용자를 자동으로 추가 하지 않습니다&#39;s 그룹에 적용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 처음 설치 시 관리자&#39;s 그룹에 최종 사용자를 자동으로 추가 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>MEDV * </p></td>
<td align="left"><p>게스트 가상 컴퓨터를 만드는 데 사용 되는 컴퓨터 이름 마스크&#39;s 컴퓨터 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>마스크에 는% username% 태그를 포함 하 여 컴퓨터 이름의 일부로 사용자 이름을 삽입할 수 있습니다. 마찬가지로,% hostname% 태그는 호스트 컴퓨터의 이름을 삽입 합니다.</p>
<p>&quot; # &quot; 마스크의 모든 문자는 임의의 숫자로 바뀝니다. 마스크 끝에 있는 별표 (*) 문자는 임의의 영숫자 문자로 바뀝니다.</p>
<p>괄호를 사용 하 여% hostname% 와% username%의 특정 문자 수를 캡처할 수 있습니다. 예를 들어, &quot; % username% [3]은 (는) &quot; 사용자 이름의 처음 세 문자를 사용 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Default = 90</p></td>
<td align="left"><p>처음 설치 시 가상 컴퓨터를 삭제 하 려 할 때 시간 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 120</p></td>
<td align="left"><p>첫 설치 프로그램이 가상 컴퓨터에서 가상 플로피 디스크를 분리 하려고 할 때 시간 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>내부 웹 페이지에 연결 되며 최초 설정 대화 상자 메시지에 표시 되는 사용자 지정 가능 URL입니다. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 900</p></td>
<td align="left"><p>처음 설치 시 Windows 탐색기를 기다리는 시간 제한 값 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>메시지가 리소스 파일에 있습니다. </p></td>
<td align="left"><p>처음 설치를 완료할 수 없을 때 최종 사용자에 게 표시 되는 사용자 지정 가능한 메시지</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 3</p></td>
<td align="left"><p>MED-V가 최종 사용자 그룹 권한을 부여 하려고 할 때의 최대 횟수입니다. 최종 사용자 그룹 권한을 성공적으로 제공할 수 없는 경우 지정 된 다시 시도 값을 초과 하면 가상 컴퓨터 준비 실패가 발생 하 여 MaxRetryCount 값에 적용 될 가능성이 큽니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 300</p></td>
<td align="left"><p>사용자 그룹 권한을 부여할 때의 제한 시간 값 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>처음 설정 하는 동안 MED-V가 수집 하는 로그 파일 경로 목록입니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 120</p></td>
<td align="left"><p>최종 사용자가 처음 설치할 때 연기 될 수 있는 최대 시간 (일)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 3</p></td>
<td align="left"><p>각 시도가 소프트웨어 오류 이외의 오류로 종료 되는 경우 MED-V가 가상 컴퓨터를 준비 하기 위해 시도할 수 있는 최대 횟수입니다. 가상 컴퓨터에 대 한 준비가 실패 하 고 처음으로 설정 다시 시도 횟수가 초과 되는 경우 MED-V는 최종 사용자에 게 실패에 대해 알리고 다시 시도할 수 있는 옵션을 제공 하지 않습니다. 이 수는 MED-V가 시작 될 때마다 다시 설정 됩니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>모드 </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>기본값 = 무인</p></td>
<td align="left"><p>첫 설정이 사용자와 상호 작용 하는 방법을 구성 합니다. 사용할 수 있는 값은 다음과 같습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>참석.</strong> 최종 사용자는 처음 설정 하는 동안 정보를 입력 해야 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>미니 설치가 완료 되려면 사용자 입력이 필요 하도록 Sysprep.inf 파일을 만든 경우, <strong> </strong> 처음 설정 하는 동안 유인 모드 또는 문제가 발생할 수 있습니다 .를 선택 해야 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>무인 설치 </strong> . 처음 설정 하는 동안에는 가상 컴퓨터가 최종 사용자에 게 표시 되지 않지만 최종 사용자에 게 처음 설치를 시작 하기 전에 메시지가 표시 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>자동 </strong> . 가상 머신은 처음 설정 하는 동안에는 최종 사용자에 게 표시 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 15</p></td>
<td align="left"><p>설치를 다시 시도할 때 처음 설정 하는 대화형 모드에서 설치를 완료 해야 하는 시간 초과 값 (분)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 45</p></td>
<td align="left"><p>처음 설정 대화형 모드에서 설치를 완료 해야 하는 시간 초과 값 (분)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>처음 설정 연기를 할 수 있는 날짜 및 시간 (UTC DateTime 형식)입니다. &quot;Yyyy-mm-dd hh: MM 형식으로 &quot; 24 시간 시계 표준으로 지정 된 시간을 입력 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>메시지가 리소스 파일에 있습니다. </p></td>
<td align="left"><p>처음 설치를 다시 시도 해야 할 때 최종 사용자에 게 표시 되는 사용자 지정 가능한 메시지입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>게스트에서 Sysprep.inf 파일의 [UserData] 섹션 아래에 있는 ComputerName 항목을 지정 된 ComputerNameMask에 따라 업데이트 해야 하는지 여부를 구성 합니다.   0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Sysprep .inf 파일의 ComputerName 항목이 ComputerNameMask에 따라 업데이트 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: Sysprep .inf 파일의 ComputerName 항목이 ComputerNameMask에 따라 업데이트 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>게스트에서 Sysprep.inf 파일의 [Id] 섹션 아래에 있는 JoinDomain 설정을 호스트의 설정에 맞게 업데이트 해야 하는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Sysprep.inf 파일의 JoinDomain 설정이 호스트의 설정에 맞게 업데이트 되지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: Sysprep .inf 파일의 JoinDomain 설정이 호스트의 설정과 일치 하도록 업데이트 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>게스트에서 Sysprep .inf 파일의 [Id] 구역 아래에 있는 MachineObjectOU 설정이 호스트와 일치 하도록 업데이트 되는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Sysprep .inf 파일의 MachineObjectOU 설정이 호스트의 설정에 맞게 업데이트 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: Sysprep .inf 파일의 MachineObjectOU 설정이 호스트의 설정과 일치 하도록 업데이트 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Set국가 Alsettings사용 </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>게스트에서 Sysprep .inf 파일의 [지역 Alsettings] 섹션 아래에 있는 설정이 호스트에 맞게 업데이트 되는지 여부를 구성 합니다.  0 = false, 1 = true.</p>
<div class="alert">
<strong>참고</strong><br/><p>기본적으로 게스트의 표준 시간대 설정은 호스트의 TimeZone 설정과 항상 동기화 됩니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트에 있는 Sysprep.inf 파일의 [지역 Alsettings] 섹션 아래에 있는 설정이 호스트에 맞게 업데이트 되지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트에 있는 Sysprep.inf 파일의 [지역 Alsettings] 섹션 아래에 있는 설정이 호스트와 일치 하도록 업데이트 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>게스트에서 Sysprep .inf 파일의 [UserData] 구역에 있는 FullName 및 OrgName 설정이 호스트의 설정과 일치 하도록 업데이트 되는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Sysprep .inf 파일의 FullName 및 OrgName 설정이 호스트의 설정에 맞게 업데이트 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: Sysprep .inf 파일의 FullName 및 OrgName 설정이 호스트의 설정과 일치 하도록 업데이트 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>메시지가 리소스 파일에 있습니다. </p></td>
<td align="left"><p>처음으로 설정을 시작할 준비가 되 면 최종 사용자에 게 표시 되는 사용자 지정 가능한 메시지 </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 30</p></td>
<td align="left"><p>설치 프로그램이 취소 작업에 대 한 가상 컴퓨터의 응답을 처음 기다리는 시간 제한 값 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 60</p></td>
<td align="left"><p>처음 설치 시 가상 컴퓨터가 종료 될 때까지 대기 하는 시간 제한 값 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 600</p></td>
<td align="left"><p>MED-V 게스트 에이전트 소프트웨어의 업그레이드 시도가 시간 초과 되기 전의 시간 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
</tbody>
</table>



## UserExperience 키


다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key 및 HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">유형</th>
<th align="left">Data/Default</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트의 응용 프로그램 게시를 호스트로 사용할 수 있는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트에서 호스트로의 응용 프로그램 게시를 비활성화 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트에서 호스트로 응용 프로그램을 게시할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트와 호스트 간에 오디오 i/o 장치 공유를 사용 하도록 설정 했는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트와 호스트 간의 오디오 i/o 장치 공유를 사용 하지 않도록 설정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트와 호스트 간에 오디오 i/o 장치를 공유할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트와 호스트 간에 클립보드 공유를 사용 하도록 설정 했는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트와 호스트 간의 클립보드 공유를 사용 하지 않도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트와 호스트 간에 클립보드를 공유할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 300</p></td>
<td align="left"><p>설정 시작 대화 상자가 처음 시간 초과 되기 전의 시간 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>대기 시간 제한</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 30</p></td>
<td align="left"><p>긴 로그온 시도 중에 전체 화면 가상 컴퓨터 창이 최종 사용자에 게 숨겨지도록 하는 시간 초과 값 (분)입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>최종 사용자가 바탕 화면에 로그온 할 때 또는 첫 번째 게스트 응용 프로그램이 시작 될 때 게스트를 시작할지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 첫 번째 게스트 응용 프로그램이 시작 될 때 게스트가 시작 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트는 최종 사용자가 바탕 화면에 로그온 할 때 시작 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트와 호스트 간에 프린터 공유를 사용할 수 있는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트와 호스트 간 프린터 공유를 사용 하지 않도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트와 호스트 간의 프린터 공유를 사용 하도록 설정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1440</p></td>
<td align="left"><p>처음 설치 시 다시 시작을 기다리는 시간 초과 값 (분)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>지정 된 URL 목록</p></td>
<td align="left"><p>호스트에서 게스트로 리디렉션할 Url 목록을 지정 합니다. </p></td>
</tr>
<tr class="even">
<td align="left"><p>Smart(스마트) Logon사용</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>사용자를 MED-V에 인증 하는 데 스마트 카드를 사용할 수 있는지 여부를 구성 합니다. 0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 스마트 카드가 MED-V에 대 한 최종 사용자를 인증 하도록 허용 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 스마트 카드가 일반 사용자를 MED-V로 인증할 수 있습니다.</p>
<div class="alert">
<strong>중요</strong><br/><p>Smart을 사용 하도록 설정 하 고 CredentialCacheEnabled를 모두 사용 하는 경우 Smart지 인 Logonenabled가 CredentialCacheEnabled를 재정의 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트와 호스트 간에 스마트 카드를 공유할 수 있는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트와 호스트 간 스마트 카드 공유를 사용 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트와 호스트 간에 스마트 카드를 공유할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트와 호스트 간에 USB 장치 공유를 사용 하도록 설정 했는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트와 호스트 간의 USB 장치 공유를 비활성화 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트와 호스트 간의 USB 장치 공유를 사용 하도록 설정 합니다.</p></td>
</tr>
</tbody>
</table>



## VM 키


다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM key 및 HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">유형</th>
<th align="left">Data/Default</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CloseAction </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>기본값 = 최대 절전 모드</p></td>
<td align="left"><p>실행 중인 마지막 응용 프로그램을 닫은 후에 가상 컴퓨터에서 수행 하는 작업입니다. LogonStartEnabled 값을 사용 하도록 설정한 경우이 설정은 무시 됩니다. 사용할 수 있는 옵션은 다음과 같습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>최대 절전 모드 </strong> . 이 옵션은 메모리 및 CPU와 같이 가상 컴퓨터에서 사용 중인 모든 물리적 리소스를 해제 하 고 실행 중인 모든 응용 프로그램 및 작업의 상태를 저장 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>종료 </strong> 합니다. 이 옵션은 게스트 운영 체제를 안전 하 게 종료 한 다음 가상 컴퓨터에서 사용 중인 메모리 및 CPU 등의 실제 리소스를 모두 해제 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>해제 </strong> 합니다. 이 옵션을 선택 하면 전원 단추를 끄거나 물리적 컴퓨터에서 전원 코드를 잡아당겨 데이터 손실이 발생할 수 있습니다. 다른 두 옵션 중 하나를 사용할 수 없는 경우에만이 옵션을 사용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>게스트에 대 한 메모리 (MB) 값의 목록입니다. 이 값은 게스트에서 사용할 수 있는 RAM의 크기를 결정 하는 데 사용 됩니다. HostMemToGuestMem와 결합 하 여 게스트 가상 컴퓨터에 할당할 RAM의 양을 결정 하기 위해 조회 테이블이 만들어집니다. 가능한 값은 128 ~ 3712입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 240</p></td>
<td align="left"><p>GuestUpdateTime 값에 지정 된 시간에 시작 하 여 MED-V가 자동 업데이트를 위해 게스트 활성 상태를 유지 해야 하는 분 수입니다. 범위는 0 ~ 1440입니다. 이 값을 0으로 설정 하면 게스트 패치 기능을 사용할 수 없습니다.</p>
<p>자동 업데이트의 게스트 패치에 대 한 자세한 내용은 <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Med-v 작업 영역에 대 한 자동 업데이트 관리를 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>기본값 = 00:00</p></td>
<td align="left"><p>MED-V가 자동 업데이트를 위해 24 시간 시계 표준으로 게스트를 종료 해야 하는 날짜의 시간 및 분입니다. HH: MM 형식으로 시간을 지정 합니다.  </p>
<p>자동 업데이트의 게스트 패치에 대 한 자세한 내용은 <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Med-v 작업 영역에 대 한 자동 업데이트 관리를 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>호스트에서 사용할 수 있는 RAM에 따라 게스트에 대 한 메모리 (MB) 값의 목록입니다. GuestMemFromHostMem와 결합 하 여 게스트 가상 컴퓨터에 할당할 RAM의 양을 결정 하기 위해 조회 테이블이 만들어집니다. 가능한 값은 1024 ~ 16384입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 1</p></td>
<td align="left"><p>게스트에 대해 할당 된 메모리가 호스트에 있는 메모리에서 계산 되는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 게스트에 대해 할당 된 메모리가 호스트에 있는 메모리에서 계산 되지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 게스트에 대해 할당 된 메모리는 호스트에 있는 메모리를 기준으로 계산 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>메모리 </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 512</p></td>
<td align="left"><p>게스트 가상 머신에 할당할 RAM (MB)입니다. HostMemToGuestMemEnabled 설정을 사용 하는 경우이 설정은 무시 됩니다. 범위 = 128 ~ 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0</p></td>
<td align="left"><p>여러 사용자가 동일한 MED-V 작업 영역을 공유 하는지 여부를 구성 합니다.  0 = false, 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: 여러 사용자가 동일한 MED-V 작업 영역을 공유 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: 여러 사용자가 동일한 MED-V 작업 영역을 공유 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NetworkingMode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Default = NAT</p></td>
<td align="left"><p>게스트에 사용 되는 네트워크 연결의 종류입니다. 사용할 수 있는 값은 다음과 같습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>브리지 </strong> . MED-V에는 일반적으로 DHCP를 통해 얻은 고유한 네트워크 주소가 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>NAT </strong> . MED-V는 NAT (Network Address Translation)를 사용 하 여 송신 트래픽에 대 한 호스트&#39;s IP를 공유 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 600</p></td>
<td align="left"><p>시작 및 종료와 같은 작업이 완료 될 때까지 MED-V가 대기 하는 일반적인 시간 제한 값 (초)입니다. 범위는 0 ~ 2147483647입니다.</p></td>
</tr>
</tbody>
</table>



## 게스트 레지스트리 설정


이 섹션에서는 구성 가능한 MED-V 게스트 레지스트리 키를 나열 하 고 그 사용에 대해 설명 합니다.

### chapv2

다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\ key와 연결 된 게스트 레지스트리 값에 대 한 정보를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름 </th>
<th align="left">유형 </th>
<th align="left">Data/Default </th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>기본값 = 1 </p></td>
<td align="left"><p>MED-V가 키 BufferPolicyReads 및 GroupPolicyMinTransferRate를 처리 하는 방법을 구성 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>기본적으로 MED-V는 다음과 같이 이러한 키를 설정 합니다.</p>
<p>BufferPolicyReads = 1 및 GroupPolicyMinTransferRate = 0.</p>
<p>필요한 경우 EnableGPWorkarounds 키를 만들고, MED-V Policyreads 및 GroupPolicyMinTransferRate의 기본 설정을 변경 하지 않으려는 경우 키를 0으로 설정 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>MED-V 작업 영역이 NAT 모드로 실행 되는 경우 EnableGPWorkarounds 레지스트리 키 BufferPolicyReads 및 GroupPolicyMinTransferRate에 영향을 줍니다. MED-V 작업 영역이 브리지 모드로 실행 되는 경우 EnableGPWorkarounds는 레지스트리 키 BufferPolicyReads에만 영향을 줍니다.</p>
</div>
<div>

</div>
<p>1 = true: MED-V는 키 BufferPolicyReads = 1과 GroupPolicyMinTransferRate = 0 (NAT 모드로 실행 하는 경우) 또는 단순한 BufferPolicyReads = 1 (브리지 모드로 실행 되는 경우)을 설정 합니다.</p>
<p>0 = false 인 경우 MED-V는 키 BufferPolicyReads 및 GroupPolicyMinTransferRate에 대 한 변경 작업을 수행 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MED-V 작업 영역 응용 프로그램 관리](manage-med-v-workspace-applications.md)

[MED-V URL 리디렉션 관리](manage-med-v-url-redirection.md)

[MED-V 작업 영역 설정 관리](manage-med-v-workspace-settings.md)









