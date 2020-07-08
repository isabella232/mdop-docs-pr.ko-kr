---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815818"
---
# PUBLISH APP


사용자의 시작 메뉴, 바탕 화면 또는 기타 지정 된 위치에 응용 프로그램 바로 가기를 게시 합니다.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>응용 프로그램: &lt; 응용 프로그램&gt;</p></td>
<td align="left"><p>응용 프로그램의 이름 및 버전 (선택 사항)</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESKTOP</p></td>
<td align="left"><p>사용자의 바탕 화면에 바로 가기를 게시 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/START</p></td>
<td align="left"><p>시작 메뉴의 프로그램 폴더에 있는 Application Virtualization 응용 프로그램 폴더에 대 한 바로 가기를 게시 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TARGET &lt; 대상 경로&gt;</p></td>
<td align="left"><p>바로 가기를 게시할 절대 경로입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/아이콘 &lt; 아이콘-pathname&gt;</p></td>
<td align="left"><p>아이콘 파일의 경로 또는 URL입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DISPLAY &lt; 표시 이름&gt;</p></td>
<td align="left"><p>바로 가기의 표시 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/인수 &lt; 명령-인수&gt;</p></td>
<td align="left"><p>매개 변수를 응용 프로그램에 전달 합니다.</p></td>
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

 

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





