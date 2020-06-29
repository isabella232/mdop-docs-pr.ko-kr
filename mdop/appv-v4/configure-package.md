---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819348"
---
# CONFIGURE PACKAGE


사용자가 패키지 매니페스트 파일, 패키지 원본, 로드 트리거 형식 또는 패키지에 대 한 로드 대상을 변경할 수 있습니다.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>패키지에 포함 된 응용 프로그램과 모든 게시 정보를 나열 하는 매니페스트 파일의 경로 또는 URL입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/OVERRIDEURL &lt; URL&gt;</p></td>
<td align="left"><p>패키지의 SFT 파일 위치입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>패키지에 대해 백그라운드 로드가 꺼집니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>게시 새로 고침 후 백그라운드 로드를 수행 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>사용자가 로그인 할 때 백그라운드 로드가 수행 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>백그라운드 로드는 사용자가 패키지에서 응용 프로그램을 시작한 후 수행 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADTARGET &lt; 대상&gt;</p></td>
<td align="left"><p>패키지에서 자동으로 로드 되는 응용 프로그램을 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>않아야</p></td>
<td align="left"><p>/AUTOLOADONxxx 플래그에 관계 없이 autoloading 수행 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>모든</p></td>
<td align="left"><p>Autoload trigger를 사용 하는 경우 패키지의 모든 응용 프로그램이 실행 되었는지 여부에 관계 없이 캐시로 로드 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Autoload trigger를 사용 하는 경우 이전에 사용자가이 패키지의 응용 프로그램을 시작한 경우 패키지가 로드 됩니다.</p></td>
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

 

버전 4.6 SP2의 경우 다음 옵션이 추가 되었습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/NO-UPDATE-FTA-SHORTCUT 가기 {TRUE | FALSE} {/GLOBAL}]</p></td>
<td align="left"><p>TRUE로 설정 하는 경우 사용자 당 또는/TGLOBAL 플래그가 지정 된 경우 패키지에 대 한 레지스트리 값이 만들어집니다.</p>
<p>FALSE로 설정 되 면 레지스트리 값이 제거 되 고 패키지에 대 한 파일 형식 연결 (FTA)이 다시 설치 됩니다.</p>
<p>지정 하지 않으면 일반 FTA 및 바로 가기 게시 동작이 발생 합니다. App-v 4.6 SP2 클라이언트에서 이후 게시 새로 고침 작업을 수행 하는 경우이 레지스트리 값이 설정 된 패키지에 대 한 바로 가기 및 FTAs 변경 되지 않으며, 플래그를 다시 설정 하지 않는 한 시스템 시작 또는 사용자 로그인에서 바로 가기 및 FTAs가 등록 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT 가기 플래그와 함께 작동 합니다. /GLOBAL 플래그가 있으면 모든 사용자에 대해 해당 패키지에 대 한 레지스트리 값이 생성 됨을 나타냅니다. 기본적으로이 사용자에 대해서만 레지스트리 값이 생성 됩니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





