---
title: MED-V 작업 영역의 번호 및 유형 식별
description: MED-V 작업 영역의 번호 및 유형 식별
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827263"
---
# MED-V 작업 영역의 번호 및 유형 식별


MED-V는 Windows XP가 필요 하거나 호스트 컴퓨터의 버전과 다른 Internet Explorer 버전을 필요로 하는 응용 프로그램을 실행 하기 위한 가상 환경을 만듭니다. 이 가상 환경은 MED-V 작업 영역 이라고 합니다.

Windows 7로 마이그레이션할 때 조직이 직면 하는 응용 프로그램 호환성 요구 사항에 따라 특정 사용자 또는 부서에만 MED-V 작업 영역이 필요할 수 있습니다. 배포를 계획할 때 엔터프라이즈에서 필요한 MED-V 작업 영역의 수를 확인 해야 합니다. 또한 각 MED-V 작업 영역의 요구 사항을 정의 해야 합니다.

## MED-V 작업 영역의 수 및 유형 식별


엔터프라이즈에서 MED-V 작업 영역을 만들 컴퓨터와 그룹을 식별 합니다. 일반적으로 이러한 응용 프로그램에 액세스 해야 하는 사용자는 Windows 7로 마이그레이션할 수 없습니다. 마이그레이션할 수 없는 응용 프로그램과이 응용 프로그램을 실행 하는 데 MED-V 작업 영역이 필요한 사용자를 식별 합니다.

아직 Windows 7에 최적화 되지 않은 인트라넷 주소도 있을 수도 있습니다. MED-V 작업 영역에서는 최종 사용자가 아직 Windows 7로 마이그레이션할 준비가 되지 않은 해당 웹 주소에 더 잘 액세스할 수 있는 Internet Explorer 브라우저를 제공 합니다. MED-V 배포를 준비 하 고 계획 하는 동안에는 호스트 컴퓨터의 Internet Explorer에서 MED-V 작업 영역의 Internet Explorer로 리디렉션할 URL 주소 목록을 식별 하 고 컴파일해야 합니다.

마지막으로, 디스크 공간 요구 사항을 평가 해야 합니다. 대부분의 MED-V 작업 영역은 2gb 이상입니다. 시스템에서 사용 가능한 디스크 공간은 MED-V의 구성 및 사용자 수에 따라 신속 하 게 사용 될 수 있습니다. 또한 회사의 기본 배포 방법에 추가 공간이 필요할 수 있습니다. 일반적으로 MED-V 작업 영역에 대해 최소 10gb의 디스크 공간을 확보 해야 하지만 이미지 크기에 따라 크게 달라 집니다.

### MED-V 작업 영역에 대 한 디스크 공간 요구 사항 계산

MED-V 작업 영역에는 설치 되어 있는 호스트 컴퓨터의 메모리와 디스크 공간이 필요 합니다. 최소한 호스트에 2gb의 디스크 공간이 필요 합니다. 디스크 공간은 변수 이며 사용자의 MED-V 작업 영역에 있는 응용 프로그램 및 데이터의 수에 따라 달라 집니다.

MED-V에 최소 10gb의 디스크 공간을 권장 합니다. 이 크기는 기본 Windows XP 작업 영역 및 몇 가지 기본 설치 응용 프로그램 및 웹 리디렉션을 허용 합니다. 또한 호스트 스왑 드라이브에 사용 가능한 공간을 제공 합니다. 기본 구성에서는 MED-V와 배포 된 단일 MED-V 작업 영역이 6 ~ 8gb 만큼 소모 됩니다. MED-V 작업 영역에 많은 수의 응용 프로그램을 포함 하거나 각 컴퓨터에 둘 이상의 사용자가 있는 경우 다음과 같은 계산을 사용 하 여 MED-V 작업 영역에 필요한 디스크 공간을 보다 정확 하 게 결정할 수 있습니다.

*기본 VHD + (컴퓨터별 사용자 x (차이점 디스크 + 저장 된 상태))*

필요한 디스크 공간을 계산 하려면 다음을 결정 합니다.

-   **기본 VHD의 크기** -med-v 작업 영역을 만드는 데 사용 된 가상 하드 디스크입니다.

    **중요**  .. A i a dv 파일을 압축 했으므로 계산에는. a dv 파일 크기를 사용 하지 마세요.

     

-   **컴퓨터당 사용자** – med-v는 컴퓨터의 각 사용자에 대해 med-v 작업 영역을 만듭니다. MED-V 작업 영역은 각 사용자가 로그온 할 때 디스크 공간을 소모 하 고 MED-V 작업 영역이 만들어집니다.

-   기본 VHD와의 차이를 추적 하는 데 사용 되는 **차이점 보관용 디스크의 크기** 입니다. 이 크기는 가상 하드 디스크에 응용 프로그램 및 소프트웨어 업데이트를 추가 하는 경우에 따라 달라 집니다. 각 MED-V 사용자가 처음으로 MED-V를 시작할 때 차이점 보관용 디스크가 만들어집니다.

-   **저장 된 상태 파일의 크기로,** 가상 컴퓨터에서 상태를 유지 관리 하는 데 사용 됩니다. 일반적으로이는 가상 컴퓨터에 할당 된 RAM 보다 약간 더 큽니다. 예를 들어 1 GB의 RAM이 할당 되 면 1081000 KB에 대 한 파일을 만듭니다.

다음 예제에서는 2.6 GB 가상 하드 디스크가 있는 MED-V 작업 영역의 세 가지 사용자를 기준으로 계산을 보여 줍니다.

*2.6 gb + (3 x (1.5 gb + 1gb)) = 10.1 gb*

**참고**  MED-V 모범 사례는 랩 배포를 사용 하 여 요구 사항의 유효성을 검사 하는 데 필요한 공간을 계산 하는 것입니다.

 

### 파일 크기를 확인 하기 위해 파일 찾기

다음 위치에는 컴퓨터 및 사용자 설정에 대 한 파일이 포함 됩니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">형식</th>
<th align="left">위치</th>
<th align="left">파일</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>기본 VHD</p></td>
<td align="left"><p>%ProgramData%\Microsoft\Medv\Workspace</p></td>
<td align="left"><p><em>InternalName </em> -여기서 <em> INTERNALNAME </em> 는 Med-v 작업 영역 포장기에서 선택한 가상 하드 디스크의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>차이점 보관용 디스크</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\MEDV\v2\Virtual 컴퓨터</p></td>
<td align="left"><p><em>WorkspaceName </em></p></td>
</tr>
<tr class="odd">
<td align="left"><p>저장 된 상태 파일</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\MEDV\v2\Virtual 컴퓨터</p></td>
<td align="left"><p><em>WorkspaceName </em> v</p></td>
</tr>
</tbody>
</table>

 

### 공유 MED-V 작업 영역의 디스크 공간 요구 사항 계산

단일 컴퓨터에서 공유 MED-V 작업 영역 배포를 계산 하는 경우 MED-V는 모든 사용자에 대해 하나의 차이점 보관용 디스크만 구성 되므로 계산에서 컴퓨터당 사용자 수는 항상 "1"입니다.

%ProgramData%\\Microsoft\\Medv\\AllUsers.의 공유 MED-V 작업 영역에 대 한 차이점 보관용 디스크와 저장 된 상태 파일을 찾을 수 있습니다.

## 관련 항목


[MED-V 배포 정의 및 계획](define-and-plan-your-med-v-deployment.md)

[MED-V 계획](planning-for-med-v.md)

 

 





