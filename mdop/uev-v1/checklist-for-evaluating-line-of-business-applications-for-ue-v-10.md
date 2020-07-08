---
title: UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록
description: UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826458"
---
# UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록


UE-V 배포에 포함할 lob (기간 업무) 응용 프로그램을 평가 하려면 다음 사항을 고려 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>이 응용 프로그램에 사용자가 사용자 지정할 수 있는 설정이 포함 되어 있습니까?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>이 설정을 로밍 하는 사용자에 게 중요 한가요?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>이러한 사용자 설정이 응용 프로그램 관리 또는 설정 정책 솔루션에 의해 이미 관리 되나요? UE-V는 로그온, 잠금 해제 또는 원격 연결 이벤트에 대 한 응용 프로그램 시작 및 Windows 설정에 응용 프로그램 설정을 적용 합니다. UE-V를 다른 설정 정책 솔루션과 함께 사용 하는 경우 사용자가 roamed 설정 간에 일관성 문제가 발생할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>컴퓨터에 대 한 응용 프로그램 설정이 있나요? 하드웨어 또는 특정 컴퓨터 구성과 관련 된 응용 프로그램 기본 설정 및 사용자 지정은 세션 간에 일관 되 게 로밍하지 않으며 응용 프로그램 환경이 잘못 될 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>응용 프로그램이 Program Files 디렉터리 또는 <strong> 사용자 </strong> \ [사용자 이름] \ <strong> AppData </strong>  \  <strong> </strong> lochdirectory에 있는 파일 디렉터리에 있는 설정을 사용 합니까? 이러한 위치 중 하나에 저장 된 응용 프로그램 데이터는 해당 컴퓨터에 대 한 정보 이거나 데이터가 너무 커서 로밍할 수 없기 때문에 일반적으로 사용자와 로밍할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>응용 프로그램에서 로밍 하지 않아야 하는 다른 응용 프로그램 데이터를 포함 하는 파일의 설정을 저장 합니까? UE-V는 파일을 단일 단위로 동기화 합니다. 설정이 아닌 다른 응용 프로그램 데이터를 포함 하는 파일에 설정을 저장 한 경우이 추가 데이터를 동기화 하면 응용 프로그램 환경이 잘못 될 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>설정이 포함 된 파일의 크기 설정 동기화의 성능은 크기가 큰 파일의 영향을 받을 수 있습니다. 큰 파일을 포함 하면 설정 동기화의 성능에 영향을 줄 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[UE-V 구성 방법 계획](planning-for-ue-v-configuration-methods.md)

[UE-V 1.0 계획](planning-for-ue-v-10.md)

 

 





