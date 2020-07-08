---
title: MED-V 설치 파일에 대한 명령줄 옵션
description: MED-V 설치 파일에 대한 명령줄 옵션
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826468"
---
# MED-V 설치 파일에 대한 명령줄 옵션


Microsoft Enterprise 데스크톱 가상화 (MED-V) 2.0을 설치 하거나 제거할 때 명령 프롬프트에서 설치 파일을 실행 하는 옵션이 있습니다. 이 섹션에서는 명령 프롬프트에 MED-V를 설치 하거나 제거할 때 지정할 수 있는 다양 한 옵션에 대해 설명 합니다.

### 명령줄 인수

다음 명령줄 인수를 각 MED-V 설치 파일과 함께 사용할 수 있습니다.

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
<th align="left">설치 파일</th>
<th align="left">인수</th>
<th align="left">허용 값</th>
<th align="left">형식</th>
<th align="left">설명</th>
<th align="left">Default</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>호스트 에이전트</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;설치 경로&gt;</p></td>
<td align="left"><p>설치</p></td>
<td align="left"><p>설치 된 디렉터리 변경</p></td>
<td align="left"><p>설치 Files\Microsoft 엔터프라이즈 데스크톱 가상화 프로그램으로 이동 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MED-V 작업 영역 포장기</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;설치 경로&gt;</p></td>
<td align="left"><p>설치</p></td>
<td align="left"><p>설치 된 디렉터리 변경</p></td>
<td align="left"><p>설치 Files\Microsoft 엔터프라이즈 데스크톱 가상화 프로그램으로 이동 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MED-V 작업 영역</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;설치 경로&gt;</p></td>
<td align="left"><p>설치</p></td>
<td align="left"><p>설치 된 디렉터리 변경</p></td>
<td align="left"><p>ProgramData\Microsoft\Medv\Workspace.로 이동 하는 설치</p></td>
</tr>
<tr class="even">
<td align="left"><p>MED-V 작업 영역</p></td>
<td align="left"><p>VHD 덮어쓰기</p></td>
<td align="left"><p>0 또는 1</p></td>
<td align="left"><p>설치</p></td>
<td align="left"><p>VHD가 있거나 (0) 기존 VHD를 덮어쓰는 경우 설치에 실패 합니다 (1).</p></td>
<td align="left"><p>덮어쓰기가 발생 하지 않으며 VHD (가상 하드 디스크)가 이미 있는 경우 설치가 실패 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MED-V 작업 영역</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0 또는 1</p></td>
<td align="left"><p>설치</p></td>
<td align="left"><p>MED-V 작업 영역을 설치한 후 시작 (0) 또는 시작 안 함 (1) MED-V-V</p></td>
<td align="left"><p>MED-V 작업 영역이 UI (사용자 인터페이스)와 함께 설치 된 경우에는 완료 페이지의 확인란이 MED-V를 <strong> </strong> 시작할지 여부를 제어 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MED-V 작업 영역</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0 또는 1</p></td>
<td align="left"><p>제거</p></td>
<td align="left"><p>저장 (0) 또는 delete (1) ' MED-V에서 생성 된 Vhd</p></td>
<td align="left"><p>Vhd는 삭제 되지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

### 명령줄 인수의 예

다음 예제에서는 MED-V 작업 영역 포장기에서 만든 MED-V 작업 영역을 설치 합니다. 설치 파일은 임시 디렉터리에 로그 파일을 만들고 자동 모드에서 설치 파일을 실행 하지만 완료 시 MED-V 호스트 에이전트를 시작 하지 않습니다. 설치 파일은 동일한 이름을 가진 이전 설치에서 남겨진 모든 VHD를 덮어씁니다.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

다음 예제에서는 이전에 설치 된 MED-V 작업 영역을 제거 합니다. 설치 파일은 임시 디렉터리에 로그 파일을 만들고 자동 모드에서 설치 파일을 실행 합니다. 설치 파일은 파일 시스템에서 남아 있는 가상 하드 디스크 파일을 모두 삭제 합니다.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## 관련 항목


[MED-V 구성 요소 배포](deploy-the-med-v-components.md)

[MED-V에 대한 기술 참조](technical-reference-for-med-v.md)

 

 





