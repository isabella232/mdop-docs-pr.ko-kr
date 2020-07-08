---
title: PowerShell 명령을 사용하여 DaRT 작업을 수행하는 방법
description: PowerShell 명령을 사용하여 DaRT 작업을 수행하는 방법
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822598"
---
# PowerShell 명령을 사용하여 DaRT 작업을 수행하는 방법


Microsoft 진단 및 복구 도구 집합 (DaRT) 10은 다음과 같이 나열 된 Windows PowerShell cmdlet 집합을 제공 합니다. 관리자는이 PowerShell cmdlet을 사용 하 여 DaRT 복구 이미지 마법사 대신 명령 프롬프트에서 다양 한 DaRT 10 서버 작업을 수행할 수 있습니다.

## PowerShell 명령을 사용 하 여 DaRT를 관리 하려면


여기에서 설명 하는 PowerShell cmdlet을 사용 하 여 DaRT를 관리 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>복사-DartImage</p></td>
<td align="left"><p>ISO를 CD, DVD 또는 USB 드라이브로 굽습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Export-DartImage</p></td>
<td align="left"><p>DaRT 이미지가 포함 된 원본 WIM 파일을 ISO 파일로 변환할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>새로운 DartConfiguration</p></td>
<td align="left"><p>Windows 이미지에 DaRT 도구 집합을 적용 하는 데 필요한 DaRT 구성 개체를 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-DartImage</p></td>
<td align="left"><p>DartConfiguration 개체를 탑재 된 Windows 이미지에 적용 합니다. 여기에는 모든 파일, 구성, 패키지 종속성을 추가 하는 것이 포함 됩니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[PowerShell을 사용하여 DaRT 10 관리](administering-dart-10-using-powershell.md)

 

 





