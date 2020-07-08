---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822383"
---
# ADD TYPE


지정 된 파일 형식 연결을 추가 합니다.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>유형: &lt; 파일 확장명&gt;</p></td>
<td align="left"><p>지정 된 응용 프로그램과 연결 되는 파일 이름 확장명입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/APP &lt; 응용 프로그램&gt;</p></td>
<td align="left"><p>응용 프로그램의 이름 및 버전 (선택 사항)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/아이콘 &lt; 아이콘-pathname&gt;</p></td>
<td align="left"><p>아이콘 파일의 경로 또는 URL입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/설명 &lt; 형식-desc&gt;</p></td>
<td align="left"><p>파일 형식에 대 한 사용자에 게 친숙 한 이름입니다. &quot;확장명 파일이 기본값으로 설정 됩니다.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONTENT-TYPE &lt; 콘텐츠-형식&gt;</p></td>
<td align="left"><p>파일의 콘텐츠 형식입니다. 기본적으로 &quot; application/softricity를 확장 합니다.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>설치 되어 있는 경우이 컴퓨터의 모든 사용자가 패키지를 사용할 수 있게 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; 인식 형&gt;</p></td>
<td align="left"><p>파일의 인식 형식입니다. 기본적으로 없음이 설정 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PROGID &lt; progid&gt;</p></td>
<td align="left"><p>파일 형식에 대 한 프로그래밍 식별자입니다. 기본적으로 App Virt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>이 형식의 파일을 다운로드 하는 사용자에 게 파일을 열지 아니면 저장할지 묻는 메시지가 표시 되는지 여부를 나타냅니다. 기본값은 YES입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>사용자가 모든 확장을 숨기도록 요청한 경우에도 파일의 확장명을 항상 표시할지 여부를 나타냅니다. 기본값은 NO입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>셸에서 새 메뉴에 항목을 추가할지 여부를 나타냅니다 <strong> </strong> . 기본값은 NO입니다.</p></td>
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

 

 





