---
title: UE-V 2. x에서 관리 백업 및 복원 관리
description: UE-V 2. x에서 관리 백업 및 복원 관리
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827388"
---
# UE-V 2. x에서 관리 백업 및 복원 관리


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1의 관리자는 응용 프로그램 및 Windows 설정을 원래 상태로 복원할 수 있습니다. 또한 UE-V 2.1의 새로운 기능을 사용 하면 사용자가 새 장치를 사용할 때 추가 설정을 복원할 수도 있습니다.

## 사용자가 새 장치를 사용할 때 UE-V 2.1 또는 UE-V 2.1 SP1의 설정을 복원 합니다.


사용자가 새 장치를 사용할 때 설정을 복원 하려면 Set Uev서식 파일 PowerShell cmdlet을 사용 하 여 **백업** 또는 **로밍 (기본)** 프로필에 설정 위치 템플릿을 추가할 수 있습니다. 이렇게 하면 컴퓨터 설정이 사용자 설정 외에도 새 컴퓨터와 동기화 될 수 있습니다. 백업 프로필에 할당 된 서식 파일은 해당 장치에 대해 백업 되 고 장치별로 구성 됩니다. 서식 파일에 대 한 설정을 백업 하려면 Windows PowerShell에서 다음 cmdlet을 사용 합니다.

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   &lt;TemplateID &gt; 는 Ue-v 템플릿 ID입니다.

-   &lt;백업은 &gt; 백업 또는 로밍 중 하나일 수 있습니다.

사용자의 장치를 바꿀 때 UE-V는 사용자의 도메인, 사용자 이름 및 장치 이름이 모두 일치 하는 경우 설정을 자동으로 복원 합니다. 모든 동기화 및 백업 데이터는 장치에서 자동으로 복원 됩니다.

새 PowerShell cmdlet, Restore UevBackup을 사용 하 여 다른 장치에서 설정을 복원할 수도 있습니다. 새 장치에 대 한 설정 패키지를 복제 하려면 Windows PowerShell에서 다음 cmdlet을 사용 합니다.

``` syntax
Restore-UevBackup –Machine <MachineName>
```

여기서 &lt; MachineName &gt; 는 디바이스의 컴퓨터 이름입니다.

여러 응용 프로그램을 포함 하는 Office 2013 서식 파일 등의 서식 파일은 모두 roamed (기본값) 또는 백업 프로필에 포함 될 수 있습니다. 서식 파일 모음의 개별 앱은 그룹을 따릅니다. Office 2013 in box 서식 파일에는 로밍 및 백업 전용 설정이 모두 포함 되어 있습니다. 로밍 프로필에는 백업 전용 설정을 포함할 수 없습니다.

백업/복원 기능의 일부로 **마지막으로 알려진 양호한 (LKG)** 를 설정으로 롤백하는 옵션에 추가 했습니다. 이번 릴리스에서는 원래 설정 또는 LKG 설정으로 롤백할 수 있습니다. LKG 설정을 사용 하면 사용자가 설정의 사전 UE-V 상태 앞에 있는 중간 및 안정적인 시점으로 롤백할 수 있습니다.

### UE-V를 사용 하 여 템플릿을 백업/복원 하는 방법

다음은 UE-V의 키 백업 및 복원 구성 요소입니다.

-   서식 파일 프로필

-   설정 저장소 위치 템플릿 내의 설정 패키지 위치

-   백업 트리거

-   설정 복원 방법

**서식 파일 프로필**

UE-V 템플릿 프로필은 템플릿이 디바이스에 등록 되거나 PowerShell/WMI 구성 유틸리티를 통해 등록 후에 정의 됩니다. 프로필 유형에는 다음이 포함 됩니다.

-   로밍 (기본값)

-   백업

-   BackupOnly

달리 지정 하지 않는 한 등록 되 면 모든 템플릿은 로밍 프로필에 포함 됩니다. 이러한 서식 파일은 해당 서식 파일을 사용 하도록 설정 된 모든 UE-V 사용 디바이스에 설정을 동기화 합니다.

명령줄에서 PowerShell 또는 WMI를 사용 하 여 서식 파일을 추가할 수 있습니다. Set Uev서식 파일 cmdlet. 백업 프로필의 서식 파일은 특수 한 디바이스 이름 디렉터리의 설정 저장소 위치에 이러한 설정을 백업 합니다. 지정 된 설정이이 위치에 백업 됩니다.

지정 된 BackupOnly에는 명시적으로 복원 하지 않는 한 동기화 하지 않아야 하는 장치와 관련 된 설정만 포함 됩니다. 이러한 설정은 설정 저장소 위치에서 Backedup 설정으로 동일한 디바이스 관련 설정 패키지 위치에 저장 됩니다. 이러한 서식 파일에는이 프로필의 일부로 지정 되는 특수 식별자가 서식 파일에 포함 되어 있습니다.

**설정 저장소 위치 템플릿 내의 설정 패키지 위치**

로밍 프로필 설정은 설정 저장소 위치에 저장 됩니다. 백업 또는 BackupOnly 프로필에 할당 된 템플릿은 해당 설정을 특수 디바이스 이름 디렉터리의 설정 저장소 위치에 저장 합니다. 이러한 프로필에 서식 파일을 사용 하는 각 디바이스에는 고유한 장치 이름이 있습니다. UE-V를 통해 이러한 디렉터리가 정리 되지 않습니다.

**백업 트리거**

백업은 UE-V 동기화를 트리거하는 동일한 이벤트에 의해 트리거됩니다.

**설정 복원 방법**

사용자의 장치를 복원 하면 현재 등록 된 템플릿의 설정이 다른 디바이스의 백업 폴더와 모든 동기화 된 설정 중 현재 컴퓨터에 복원 됩니다. 설정은 다음 두 가지 방법으로 복원 됩니다.

-   **자동 복원**

    사용자의 UE-V 설정 저장소 경로, 도메인 및 컴퓨터 이름이 현재 사용자와 일치 하는 경우에는 해당 사용자의 모든 설정이 동기화 되 고 최신 설정만 적용 됩니다. 사용자가 처음으로 새 장치에 로그온 하 고 이러한 조건이 충족 되는 경우 설정 데이터가 해당 장치에 적용 됩니다.

    **참고**  
    접근성 및 Windows 데스크톱 설정을 적용 하려면 사용자가 Windows에 다시 로그온 해야 합니다.



-   **수동 복원**

    새로 고침 중에 장치를 복원 하 여 사용자를 지원 하려는 경우 Restore UevBackup cmdlet을 사용 하도록 선택할 수 있습니다. 이 명령을 사용 하면 설정 저장소 위치에서 사용자의 설정이 다운로드 됩니다.

## 응용 프로그램 및 Windows 설정을 원래 상태로 복원


WMI 및 Windows PowerShell 명령을 사용 하 여 UE-V Agent가 설치 된 후 처음으로 응용 프로그램을 시작할 때 컴퓨터에 있던 설정 값으로 응용 프로그램 및 Windows 설정을 복원할 수 있습니다. 이 복원 작업은 응용 프로그램 또는 Windows 설정 기준에 따라 수행 됩니다. 설정은 다음에 응용 프로그램을 실행할 때 복원 되거나, 사용자가 운영 체제에 로그온 할 때 설정이 복원 됩니다.

**UE-V 2. x 용 Windows PowerShell을 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면**

1.  Windows PowerShell 창을 엽니다.

2.  다음 Windows PowerShell cmdlet을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Windows PowerShell cmdlet</strong></th>
    <th align="left"><strong>설명</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p>응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</p></td>
    </tr>
    </tbody>
    </table>



**WMI를 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면**

1.  Windows PowerShell 창을 엽니다.

2.  다음 WMI 명령을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>WMI 명령</strong></th>
    <th align="left"><strong>설명</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p>응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## 관련 항목


[Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)









