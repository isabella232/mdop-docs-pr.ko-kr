---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821973"
---
# CONFIGURE SERVER


사용자가 서버의 설정을 변경할 수 있도록 합니다. 지정 하지 않은 설정은 수정 되지 않습니다.

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>서버: &lt; 서버 이름&gt;</p></td>
<td align="left"><p>게시 서버의 표시 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/NAME &lt; display-NAME&gt;</p></td>
<td align="left"><p>서버의 새 표시 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/HOST &lt; 호스트 이름&gt;</p></td>
<td align="left"><p>게시 서버의 호스트 이름 또는 IP 주소입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PORT &lt; 포트&gt;</p></td>
<td align="left"><p>게시 서버가 수신 대기 하는 포트입니다. 일반 HTTP 서버용 80, 고급 보안을 사용 하는 HTTP 서버에 대 한 443, 일반 응용 프로그램 가상화 서버의 경우 554, 고급 보안을 사용 하는 서버의 경우 322를 기본값으로 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PATH &lt; 경로&gt;</p></td>
<td align="left"><p>게시 요청에 사용 되는 URL의 경로 부분입니다. TYPE 매개 변수를 RTSP로 설정 하는 경우 경로는 선택 사항이 고 기본값은 &quot; / &quot; 입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TYPE</p></td>
<td align="left"><p>게시 서버가 웹 서버 ( &quot; HTTP &quot; ) 또는 RTSP (Application Virtualization server) 인지 여부를 나타냅니다 &quot; &quot; .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/새로 고침</p></td>
<td align="left"><p>이로 설정 되 면 사용자가 로그인 할 때 게시 정보가 새로 고쳐집니다. 기본적으로 ON으로 설정 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CSECURE</p></td>
<td align="left"><p>있는 경우 게시 서버에 향상 된 보안의 연결을 설정 해야 함을 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</p></td>
</tr>
<tr class="odd">
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

 

 





