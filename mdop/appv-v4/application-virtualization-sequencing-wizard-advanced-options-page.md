---
title: 응용 프로그램 가상화 시퀀싱 마법사 고급 옵션 페이지
description: 응용 프로그램 가상화 시퀀싱 마법사 고급 옵션 페이지
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819598"
---
# 응용 프로그램 가상화 시퀀싱 마법사 고급 옵션 페이지


Application Virtualization (App-v) 시퀀싱 마법사의 **고급 옵션** 페이지를 사용 하 여 설치할 응용 프로그램에 대 한 고급 옵션을 지정 합니다. 이 페이지에는 다음 표에 설명 된 요소가 포함 되어 있습니다.

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
<td align="left"><p><strong>블록 크기</strong></p></td>
<td align="left"><p>네트워크 상에 서 SFT 파일을 스트리밍할 때 나눌 블록의 크기를 지정 하는 데 사용 됩니다. 모든 블록은 지정 된 크기와 동일 합니다. 그러나 마지막 블록이 지정 된 것 보다 작을 수 있습니다. 다음 값 중 하나를 선택 합니다.</p>
<ul>
<li><p><strong>4KB</strong></p></li>
<li><p><strong>16kb</strong></p></li>
<li><p><strong>32 KB</strong></p></li>
<li><p><strong>64 KB</strong></p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>블록 크기를 선택 하는 경우 SFT 파일과 네트워크 대역폭의 크기를 고려 합니다. 더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다. 블록 크기가 더 많은 파일은 스트리밍할 수 있지만 더 많은 네트워크 대역폭을 사용 합니다. 실험을 통해 네트워크의 스트리밍 응용 프로그램에 대 한 최적의 블록 크기를 찾을 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>모니터링 중 Microsoft Update 사용</strong></p></td>
<td align="left"><p>시퀀싱 마법사&#39;s 모니터링 단계 중에 Microsoft 업데이트를 설치할 수 있도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Dll 다시 기준 다시 하기</strong></p></td>
<td align="left"><p>지원 되는 동적 연결 라이브러리를 RAM의 연속 공간으로 다시 매핑하는 데 사용할 수 있도록 하 여 메모리를 절약 하 고 성능을 개선 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Back</strong></p></td>
<td align="left"><p>시퀀싱 마법사&#39;s 이전 페이지에 액세스 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Next</strong></p></td>
<td align="left"><p>시퀀싱 마법사&#39;s 다음 페이지에 액세스 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>취소</strong></p></td>
<td align="left"><p>시퀀싱 마법사의 작업을 종료 합니다.</p></td>
</tr>
</tbody>
</table>



\ [Template 토큰 값 \]

앱-V 시퀀싱 마법사의 **고급 옵션** 페이지를 사용 하 여 시퀀싱 하는 응용 프로그램의 고급 옵션을 지정할 수 있습니다. 이 페이지에는 다음 표에 설명 된 요소가 포함 되어 있습니다.

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
<td align="left"><p><strong>모니터링 중 Microsoft Update 실행 허용</strong></p></td>
<td align="left"><p>응용 프로그램 시퀀싱 중 모니터링 단계에서 소프트웨어 업데이트를 응용 프로그램에 적용할지 여부를 지정 합니다. 이 옵션은 응용 프로그램 설치를 성공적으로 완료 하기 위해 업데이트가 필요한 경우에 유용 합니다. 이 옵션은 기본적으로 선택 되어 있지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Dll 다시 기준 다시 하기</strong></p></td>
<td align="left"><p>지원 되는 동적 연결 라이브러리를 RAM의 연속 공간으로 다시 매핑할 수 있습니다. 이 옵션을 선택 하면 메모리를 관리 하 고 응용 프로그램 성능을 향상 시킬 수 있습니다. 이 옵션은 기본적으로 선택 되어 있지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Back</strong></p></td>
<td align="left"><p>마법사의 이전 페이지로 이동 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Next</strong></p></td>
<td align="left"><p>마법사의 다음 페이지로 이동 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>취소</strong></p></td>
<td align="left"><p>설정을 취소 하 고 마법사를 종료 합니다.</p></td>
</tr>
</tbody>
</table>



\ [Template 토큰 값 \]

## 관련 항목


[시퀀싱 마법사](sequencing-wizard.md)









