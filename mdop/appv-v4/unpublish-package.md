---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815133"
---
# UNPUBLISH PACKAGE


전체 패키지에 대 한 바로 가기 및 파일 형식을 제거할 수 있습니다.

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>패키지: &lt; 패키지 이름&gt;</p></td>
<td align="left"><p>패키지 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CLEAR</p></td>
<td align="left"><p>표시 되 면 사용자 설정도 제거 됩니다. (자세한 내용은이 항목의 뒷부분에 있는 중요 참고를 참조 하세요.)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>있는 경우 패키지가이 컴퓨터의 모든 사용자에 대해 게시 취소 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</p></td>
</tr>
</tbody>
</table>

 

버전 4.6의 경우 다음 옵션이 추가 되었습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</p></td>
</tr>
</tbody>
</table>

 

**중요**  **패키지 게시 취소** 명령을 실행 하려면 패키지가 Application Virtualization 클라이언트에 이미 추가 되어 있어야 합니다.

**전역**을 사용 하려면 **게시 취소 패키지가** 로컬 관리자로 실행 되어야 합니다. 그렇지 않으면 **Clearapp** 권한만 필요 합니다.

**게시 취소 패키지** 를 사용 하 여 패키지의 모든 전역 파일 형식 및 바로 **가기를 제거 합니다** . **CLEAR** 는 해당 되지 않습니다.

**전역** 이 아닌 **패키지 게시 취소** 를 사용 하면 패키지의 사용자 바로 가기 키와 파일 형식이 제거 되 고, **CLEAR** 가 설정 된 경우 사용자의 컨텍스트 아래에 있는 백그라운드 로드도 중지 됩니다.

패키지 **게시 취소** 패키지를 **추가**, **편집**및 **게시**하기 위한 원본 ID로 사용 된 것과 동일한 패키지 이름 또는 GUID의 응용 프로그램에서 작동 합니다.

**패키지 게시를 취소** 하면/clear 스위치 사용에 관계 없이 항상 모든 사용자 설정, 바로 가기 및 파일 형식이 지워집니다.

 

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





