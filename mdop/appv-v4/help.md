---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821463"
---
# HELP


Application Virtualization (App-v)에서 사용할 수 있는 다양 한 SFTMIME 명령에 대 한 정보를 표시 합니다.

## HELP


`SFTMIME [/? | /HELP [VERB:<verb>]]`

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
<td align="left"><p>/?,/HELP</p></td>
<td align="left"><p>사용 정보를 표시 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>동사</p></td>
<td align="left"><p>추가, 새로 고침, 도움말 또는 제거와 같이 실행할 명령입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>개체</p></td>
<td align="left"><p>앱: &quot; 기본 응용 프로그램 등 명령이 적용 되는 항목&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>변수</p></td>
<td align="left"><p>지정 된 동사 및 개체에 대 한 선택적 매개 변수입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>지정 된 경로 이름으로 출력을 기록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>활성 콘솔 창에 출력을 표시 합니다 (기본값).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>대화 상자에 오류를 표시 합니다 (쿼리에 대해 유효 하지 않음).</p></td>
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

 

다음 표에 설명 된 동사가 지원 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>ADD</p></td>
<td align="left"><p>앱-V 클라이언트에 새 응용 프로그램, 패키지, 파일 형식 연결 또는 게시 서버를 추가 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>구성할</p></td>
<td align="left"><p>응용 프로그램, 패키지, 파일 형식 연결 또는 게시 서버의 구성을 변경 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>응용 프로그램, 패키지, 파일 형식 연결 또는 서버를 제거 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>불러오려면</p></td>
<td align="left"><p>패키지를 파일 시스템 캐시로 로드 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>복구</p></td>
<td align="left"><p>응용 프로그램의 개인 설정을 다시 설정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>고치지</p></td>
<td align="left"><p>게시 서버 새로 고침을 트리거합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>부분만</p></td>
<td align="left"><p>사용자의 시작 메뉴, 데스크톱 또는 기타 지정 된 위치에 응용 프로그램 바로 가기를 게시 하거나 전체 패키지의 콘텐츠를 게시 하는 데 사용 될 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>문서만</p></td>
<td align="left"><p>전체 패키지에 대 한 바로 가기 및 파일 형식을 제거 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>쿼리</p></td>
<td align="left"><p>현재 응용 프로그램, 패키지, 파일 형식 연결 또는 게시 서버의 목록을 가져옵니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>선택 취소</p></td>
<td align="left"><p>하나 이상의 응용 프로그램에 대 한 개인 설정 및 데스크톱 구성을 제거 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>선에서</p></td>
<td align="left"><p>파일 시스템 캐시에서 패키지를 언로드합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>잠금</p></td>
<td align="left"><p>파일 시스템 캐시에 지정 된 응용 프로그램을 잠급니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>잠금 해제</p></td>
<td align="left"><p>파일 시스템 캐시에 지정 된 응용 프로그램의 잠금을 해제 합니다.</p></td>
</tr>
</tbody>
</table>

 

앞의 작업에 대 한 자세한 내용을 보려면 다음 명령을 사용 합니다.

`SFTMIME /HELP VERB:verb`

예를 들어 다음 명령은 ADD 동사에 대 한 정보를 표시 합니다.

`SFTMIME /HELP VERB:ADD`

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





