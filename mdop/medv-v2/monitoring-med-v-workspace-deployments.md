---
title: MED-V 작업 영역 배포 모니터링
description: MED-V 작업 영역 배포 모니터링
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827213"
---
# MED-V 작업 영역 배포 모니터링


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0의 모니터링 기능을 사용 하면 개별 MED-V 작업 영역에서 쿼리를 실행 하 여 MED-V 작업 영역이 배포 된 후 엔터프라이즈에서 처음으로 설치에 성공한 지 여부를 확인할 수 있습니다. 첫 설치가 성공적으로 완료 될 때까지 MED-V가 사용할 수 있는 상태가 아니기 때문에 첫 설치의 성공 여부를 모니터링 하는 것이 중요 합니다.

이 섹션에서는 최초 설치의 성공 또는 실패를 모니터링 하는 데 도움이 되는 정보와 지침을 제공 합니다.

## MED-V 작업 영역 배포를 모니터링 하려면


모니터링 기능은 사용자가 MED-V 작업 영역의 모든 최종 사용자에 대해 처음 설정 하는 상태를 검색 하기 위해 WMI 쿼리 언어를 사용 하 여 쿼리할 수 있는 결합 된 in-process WMI (Windows Management Instrumentation) 공급자로 구성 됩니다.

WMI 공급자는 Microsoft .Net Framework 3.5에서 WMI 공급자 확장 프레임 워크를 사용 하 여 구현 됩니다. WMI 공급자는 LocalService 컨텍스트에서 실행 되며, 처음 설치 상태가 \\Data에 안전 하 게 저장 됩니다.

WMI 공급자는 **root\\microsoft\\medv** 네임 스페이스에서 구현 되며, **Setftsstate**메서드를 노출 하는 class **ft \ _Status**를 구현 합니다. MED-V는 **Setftsstate** 를 사용 하 여 첫 번째 설정 상태를 설정 합니다.

클래스에는 다음 속성이 포함 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>컴퓨터</strong></p></td>
<td align="left"><p><strong></strong>처음 설치 시 프로 비전 된 게스트 가상 컴퓨터의 이름을 포함 하는 읽기 전용 속성입니다. 이 키에는 처음 설치에 실패 했을 때 발생 한 게스트의 이름이 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>StatusCode</strong></p></td>
<td align="left"><p><strong></strong>처음 설치에 성공한 경우 0이 포함 된 읽기 전용 속성입니다. 반환 되는 다른 값은 기록 된 오류에 대 한 이벤트 ID와 같습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>시간</strong></p></td>
<td align="left"><p>처음 설치를 완료할 때 까지의 UTC 시간입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>사용자</strong></p></td>
<td align="left"><p>처음으로 설치할 때 사용 하는 사용자입니다.</p></td>
</tr>
</tbody>
</table>

 

다음 코드에서는 **FTS \ _Status** 클래스를 정의 하는 MOF (관리 개체 형식) 파일을 보여 줍니다.

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

주요 관심사는 처음 설치가 성공적으로 완료 되지 않은 MED-V 작업 영역의 경우와 같이 처음 설치에 실패 한 오류만 반환 하도록 쿼리를 작성할 수 있습니다.

``` syntax
Select * from FTS_Status where StatusCode != 0
```

이 경우 모니터링 기능은 실패를 해결 하기 위해 적절 한 작업을 수행 하는 데 사용할 수 있는 처음 설치에 실패 한 MED-V 작업 영역의 목록을 반환 합니다.

## 관련 항목


[MED-V 작업 영역 모니터링](monitor-med-v-workspaces.md)

[처음 설치 설정을 확인하는 방법](how-to-verify-first-time-setup-settings.md)

 

 





