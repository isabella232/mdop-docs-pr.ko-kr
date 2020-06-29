---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819898"
---
# ADD APP


응용 프로그램 레코드를 추가 합니다.

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>앱: &lt; 응용 프로그램&gt;</p></td>
<td align="left"><p>응용 프로그램의 이름 및 버전 (선택 사항)</p></td>
</tr>
<tr class="even">
<td align="left"><p>/OSD &lt; osd-pathname&gt;</p></td>
<td align="left"><p>OSD 파일의 경로 또는 URL입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/아이콘 &lt; 아이콘-pathname&gt;</p></td>
<td align="left"><p>아이콘 파일의 경로 또는 URL입니다.</p></td>
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

 

**참고**  응용 프로그램의 결과 이름은 앱: 응용 프로그램에 제공 된 이름이 아니라 OSD 파일에서 가져옵니다 &lt; &gt; .

 

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





