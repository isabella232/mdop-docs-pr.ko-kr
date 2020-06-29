---
title: UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원
description: UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812377"
---
# UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원


Microsoft UE-V (User Experience Virtualization)의 WMI 및 PowerShell 기능은 설정 패키지를 복원할 수 있는 기능을 제공 합니다. WMI 및 PowerShell 명령을 사용 하면 UE-V Agent가 설치 된 후 처음으로 응용 프로그램을 시작할 때 컴퓨터에 있던 설정 값으로 응용 프로그램 및 Windows 설정을 복원할 수 있습니다. 이 복원 작업은 응용 프로그램 또는 Windows 설정 기준에 따라 수행 됩니다. 이 설정은 다음에 응용 프로그램을 실행 하거나 사용자가 운영 체제에 로그온 할 때 복원 됩니다.

**PowerShell을 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면**

1.  Windows PowerShell 창을 엽니다. Microsoft UE-V PowerShell 모듈을 가져오려면 다음 명령을 입력 합니다.

    ``` syntax
    Import-module UEV
    ```

2.  다음 PowerShell cmdlet을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>PowerShell Cmdlet</strong></th>
    <th align="left"><strong>설명</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Restore UevUserSetting</p></td>
    <td align="left"><p>응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

**WMI를 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면**

1.  PowerShell 창을 엽니다.

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
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</p></td>
    <td align="left"><p>응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

## 관련 항목


[UE-V 1.0 관리](administering-ue-v-10.md)

[UE-V 1.0 작업](operations-for-ue-v-10.md)

 

 





