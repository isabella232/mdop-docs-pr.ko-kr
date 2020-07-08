---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815738"
---
# QUERY OBJ


현재 응용 프로그램, 패키지, 파일 형식 연결 또는 게시 서버의 탭으로 구분 된 목록을 반환 합니다.

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

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
<td align="left"><p>내</p></td>
<td align="left"><p>응용 프로그램 목록을 반환 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지할</p></td>
<td align="left"><p>패키지 목록을 반환 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TYPE</p></td>
<td align="left"><p>파일 형식 연결 목록을 반환 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER</p></td>
<td align="left"><p>게시 서버 목록을 반환 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/간단히</p></td>
<td align="left"><p>각에 대 한 전체 속성을 표시 하지 않고 응용 프로그램 이름, 패키지, 연결 또는 서버 이름 목록을 반환 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>응용 프로그램의 경우 현재 사용자가 액세스할 수 있는 모든 알려진 응용 프로그램을 반환 합니다. 패키지의 경우 현재 사용자가 액세스할 수 있는 패키지를 제외한 모든 알려진 패키지만 반환 됩니다. 연결에 대해 사용자가 아닌 모든 사용자에 게 적용 되는 연결만 반환 합니다. 서버에 유효 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</p></td>
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

 

**참고**  버전 4.6에서 SFTMIME 쿼리 OBJ: APP \ [/GLOBAL\]의 출력에 새 열이 추가 되었습니다. 출력의 마지막 열은 응용 프로그램이 게시 되었는지 여부를 나타내는 숫자 값입니다.

게시 됨 = 1은 응용 프로그램을 게시 서버 새로 고침을 사용 하 여 응용 프로그램을 게시 한 후 Windows Installer 파일 (. MSI) 또는 패키지 매니페스트를 사용 하 여 SFTMIME 패키지 추가, 패키지 구성 또는 패키지 게시 명령을 실행 합니다.

게시 됨 = 0은 응용 프로그램이 게시 되지 않았거나 지우기 작업을 수행 하거나 SFTMIME 게시 취소 명령을 실행 하는 등의 결과로 더 이상 게시 되지 않았음을 의미 합니다.

/CGLOBAL 매개 변수를 사용 하는 경우 게시 된 상태는 전역으로 게시 된 응용 프로그램의 경우 1이 고, 사용자 컨텍스트에 게시 된 응용 프로그램에 대해서는 0입니다. /GLOBAL 매개 변수가 없으면 명령을 실행 하는 사용자의 컨텍스트에서 게시 된 응용 프로그램에 대해 게시 된 상태 1이 반환 되 고, 전역으로 게시 되는 응용 프로그램에 대해 0 상태가 반환 됩니다.

 

SFTMIME 쿼리 OBJ 명령을 사용 하 여 위에 표시 된 모든 개체 (응용 프로그램, 패키지, 파일 형식 연결, 서버)에 대 한 정보를 쿼리할 수 있습니다.일반 작업 작업에서 SFTMIME 쿼리 OBJ 명령을 사용 하는 방법을 표시 하려면 다음 예제에서는 특정 패키지에 대 한 OVERRIDEURL 매개 변수 값을 설정 하 여 패키지 콘텐츠의 새 경로를 지정 하려는 경우 수행할 프로세스를 보여 줍니다. 

1.  구성 하고자 하는 패키지를 찾으려면 다음 명령을 실행 합니다.

    `SFTMIME QUERY OBJ:PACKAGE`

    이 명령은 검색 된 각 패키지 이름을 출력의 첫 번째 열에 GUID로 반환 합니다 (예: {AF78ABE1-57D4-4297-89DE-C308684AEDD6}).

2.  OVERRIDEURL 매개 변수 값을 설정 하려면 SFTMIME [패키지 구성](configure-package.md) 명령을 사용 합니다. 예를 들어이 패키지에 대 한 OVERRIDEURL 값을 *\\\\server\\share\\mypackage.sft*값으로 설정 하려면 다음과 같이 SFTMIME 패키지 구성 명령을 사용 하 고, 1 단계에서 SFTMIME 쿼리 OBJ 명령의 출력에서 선택한 패키지 GUID를 지정 하 고, overrideurl 매개 변수와 새 값을 입력 합니다.

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

버전 4.6 SP2의 경우 다음 옵션이 추가 되었습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT 가기</p></td>
<td align="left"><p>/NO-UPDATE-FTAI 바로 가기 플래그의 현재 상태를 나타냅니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





