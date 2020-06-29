---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822398"
---
# ADD PACKAGE


패키지 레코드를 추가 합니다. 패키지가 이미 있는 경우이 명령을 통해 기존 패키지의 구성을 업데이트 합니다.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>패키지에 대해 사용자에 게 표시 되는 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PMANIFEST &lt; 매니페스트-경로&gt;</p></td>
<td align="left"><p>패키지에 포함 된 응용 프로그램과 모든 게시 정보를 나열 하는 매니페스트 파일의 경로입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/OVERRIDEURL &lt; URL&gt;</p></td>
<td align="left"><p>패키지의 SFT 파일 위치입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>게시 새로 고침 후 백그라운드 로드를 수행 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>사용자가 로그인 할 때 백그라운드 로드가 수행 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>백그라운드 로드는 사용자가 패키지에서 응용 프로그램을 시작한 후 수행 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADTARGET 대상</p></td>
<td align="left"><p>패키지에서 자동으로 로드 되는 응용 프로그램을 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>않아야</p></td>
<td align="left"><p>/AUTOLOADONxxx 플래그에 관계 없이 autoloading 수행 되지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>모든</p></td>
<td align="left"><p>Autoload trigger를 사용 하는 경우 패키지의 모든 응용 프로그램은 이전에 시작 되었는지 여부에 관계 없이 캐시로 로드 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Autoload trigger를 사용 하는 경우 이전에 사용자가이 패키지의 응용 프로그램을 시작한 경우 패키지가 로드 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>설치 되어 있는 경우이 컴퓨터의 모든 사용자가 패키지를 사용할 수 있게 됩니다.</p></td>
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

 

 





