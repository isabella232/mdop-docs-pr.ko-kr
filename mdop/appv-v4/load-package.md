---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816238"
---
# LOAD PACKAGE


지정 된 패키지를 파일 시스템 캐시에 로드 합니다.

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>로드할 패키지의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTPATH &lt; sft-경로 이름&gt;</p></td>
<td align="left"><p>지정 되는 경우 로드할 SFT 파일에 대 한 경로입니다.</p></td>
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

 

**참고**  SFTPATH가 지정 되지 않은 경우 클라이언트는 OSD 파일, ApplicationSourceRoot 레지스트리 키 값 또는 OverrideURL 설정을 기반으로 사용 하도록 구성 된 경로를 사용 하 여 패키지를 로드 합니다.

**패키지 로드** 명령은 동기 로드를 수행 하며 패키지가 완전히 로드 되거나 오류 조건이 발생할 때까지 완료 되지 않습니다.

 

## 관련 항목


[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





