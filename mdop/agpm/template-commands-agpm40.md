---
title: 템플릿 명령
description: 템플릿 명령
author: dansimp
ms.assetid: 243a9b18-bf3f-44fa-94d7-5c793f7322da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2c540bf87462f501a4db5596faca43ef66ee8558
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818288"
---
# 템플릿 명령


**서식 파일** 탭:

-   새 Gpo (그룹 정책 개체)를 만드는 데 사용할 수 있는 사용 가능한 서식 파일 목록을 표시 합니다.

-   선택한 서식 파일을 기반으로 GPO를 만들고 서식 파일을 관리 하 고 서식 파일에 대 한 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.

-   선택한 서식 파일에 액세스할 수 있는 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.

서식 파일을 변경할 수 없기 때문에 서식 파일에는 기록이 없습니다. 그러나 GPO 버전과 마찬가지로 서식 파일의 설정을 설정 보고서와 함께 표시 하거나 차이점 보고서를 사용 하 여 다른 GPO와 비교할 수 있습니다.

**참고**  서식 파일은 편집 가능한 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.

 

이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 다음 중 해당 되는 옵션을 비롯 한 바로 가기 메뉴가 표시 됩니다.

## 컨트롤


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>새로운 제어 된 GPO</strong></p></td>
<td align="left"><p>선택한 서식 파일을 기반으로 새 GPO를 만듭니다. 도메인의 프로덕션 환경에 새 GPO를 배포 하는 옵션이 제공 됩니다. GPO를 만들 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다. (이 옵션은 다음을 마우스 오른쪽 단추로 클릭할 <strong> 때 GPO가 선택 되어 있지 않은 경우 표시 됩니다. 그룹 정책 개체 </strong> 목록.</p></td>
</tr>
</tbody>
</table>

 

## 보고


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>설정</strong></p></td>
<td align="left"><p>선택한 GPO 내의 설정을 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>차이점</strong></p></td>
<td align="left"><p>두 개의 선택한 GPO 템플릿 내의 설정을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 서식 파일 관리


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>기본값으로 설정</strong></p></td>
<td align="left"><p>선택한 서식 파일을 새 GPO를 만들 때 자동으로 사용할 기본값으로 설정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>삭제</strong></p></td>
<td align="left"><p>선택한 서식 파일을 휴지통으로 이동 <strong> </strong> 합니다. GPO를 삭제할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>선택한 서식 파일의 이름을 변경 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 기타


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>새로 고침</strong></p></td>
<td align="left"><p>변경 내용을 통합 하도록 그룹 정책 관리 콘솔의 표시를 업데이트 합니다. 일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Help</strong></p></td>
<td align="left"><p>AGPM (고급 그룹 정책 관리)에 대 한 도움말을 표시 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

-   [내용 탭](contents-tab-agpm40.md)

-   [편집기 작업 수행](performing-editor-tasks-agpm40.md)

-   [검토자 작업 수행](performing-reviewer-tasks-agpm40.md)

 

 





