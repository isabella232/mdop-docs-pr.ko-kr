---
title: UE-V 예약된 작업의 빈도 변경
description: UE-V 예약된 작업의 빈도 변경
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822688"
---
# UE-V 예약된 작업의 빈도 변경


Microsoft UE-V (User Experience Virtualization) 에이전트 설치 관리자 AgentSetup.exe에서 UE-V 에이전트를 설치 하는 동안 두 개의 예약 된 작업을 만듭니다. 두 작업은 **서식 파일 자동 업데이트** 작업과 **설정 저장소 위치 상태** 작업입니다. 이러한 예약 된 작업은 UE-V 도구를 사용 하 여 구성할 수 없습니다. 이러한 항목에 대 한 예약 된 작업을 변경 하려는 관리자는 Schtasks.exe 명령줄 옵션을 사용 하는 스크립트를 만들 수 있습니다.

Schtasks.exe에 대 한 자세한 내용은 [Schtasks를 사용 하 여 Windows Server 2003에서 작업을 예약 하는 방법을](https://go.microsoft.com/fwlink/?LinkID=264854)참조 하세요.

## 서식 파일 자동 업데이트


**서식 파일 자동 업데이트** 작업은 설정 템플릿 카탈로그에서 새 서식 파일, 업데이트 또는 제거 되었는지 확인 합니다. 이 작업은 SettingsTemplateCatalog가 구성 된 경우에만 실행 됩니다. **서식 파일 자동 업데이트** 작업은 ue-v 에이전트 설치 디렉터리에 있는 ApplySettingsCatalog.exe 파일을 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 이름</th>
<th align="left">기본 트리거</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Template 자동 업데이트</p></td>
<td align="left"><p>매일 3:30 오전</p></td>
</tr>
</tbody>
</table>

 

**예:** 다음 명령은 각 시간에 설정 템플릿 카탈로그 저장소를 확인 하도록 에이전트를 구성 합니다.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## 설정 저장소 위치 상태


**저장소 위치 상태 설정** 작업에서 다음 작업을 수행 합니다.

1.  UE-V 폴더가 여전히 고정 되어 있거나 오프 라인 파일 기능을 사용 하 여 등록 되어 있는지 확인 합니다.

2.  설정 저장소 위치가 오프 라인 또는 온라인 인지 확인 합니다.

3.  오프 라인 파일의 기본 간격 대신 지정 된 간격에 따라 동기화를 강제로 수행 합니다.

4.  사전 반입 하도록 구성 된 설정 패키지를 동기화 합니다.

5.  Active Directory 홈 디렉터리 경로가 변경 되었는지 확인 합니다.

6.  현재 설정 저장소 구성을 다음 위치에 작성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">작업 이름</th>
    <th align="left">기본 트리거</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>\Microsoft\UE-V\Settings 저장소 위치 상태</p></td>
    <td align="left"><p>사용자에 게 로그온 할 때 – 트리거된 후 30 분 마다 무한정 반복 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

**예:** 다음 명령은 각 시간에 위의 작업을 실행 하도록 에이전트를 구성 합니다.

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## 관련 항목


[UE-V 1.0 관리](administering-ue-v-10.md)

[UE-V 1.0 작업](operations-for-ue-v-10.md)

 

 





