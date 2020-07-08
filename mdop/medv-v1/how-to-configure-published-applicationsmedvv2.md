---
title: 게시된 응용 프로그램을 구성하는 방법
description: 게시된 응용 프로그램을 구성하는 방법
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824313"
---
# 게시된 응용 프로그램을 구성하는 방법


호스트 운영 체제와 호환 되지 않는 응용 프로그램은 MED-V 작업 영역 내에서 실행할 수 있으며, 데스크톱에서 시작 하는 것과 같은 방식으로 (시작 메뉴 또는 로컬 호스트 바로 가기에서) MED-V 작업 영역 내에서 시작 됩니다. 선택 되 고 정의 된 응용 프로그램을 게시 된 응용 프로그램 이라고 합니다. 이 섹션의 절차에서는 게시 된 응용 프로그램을 추가 하 고 제거 하는 방법에 대해 설명 합니다.

다음 중 한 가지 방법으로 응용 프로그램을 게시할 수 있습니다.

-   응용 프로그램으로, 응용 프로그램의 명령줄에 입력 하 여 특정 응용 프로그램을 선택 합니다. 선택한 응용 프로그램만 게시 됩니다.

-   메뉴 — 여러 응용 프로그램을 포함 하는 폴더를 선택 합니다. 폴더 내의 모든 응용 프로그램이 메뉴에 게시 되 고 표시 됩니다.

## <a href="" id="bkmk-addingapublishedapplication"></a>MED-V 작업 영역에 게시 된 응용 프로그램을 추가 하는 방법


**MED-V 작업 영역에 응용 프로그램을 추가 하려면**

1.  MED-V 작업 영역을 클릭 하 여 구성 합니다.

2.  **응용 프로그램** 창의 **게시 된 응용 프로그램** 섹션에서 **추가** 를 클릭 하 여 새 응용 프로그램을 추가 합니다.

3.  다음 표의 설명 대로 응용 프로그램 속성을 구성 합니다.

4.  **정책** 메뉴에서 **커밋을**선택 합니다.

    **참고**  
    Internet Explorer를 게시 된 응용 프로그램으로 설정 하 여 웹 리디렉션이 제대로 작동 하는지 확인 하는 경우 모든 매개 변수가 괄호 안에 있지 않은지 확인 합니다.



**게시 된 응용 프로그램 속성**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>설정됨</p></td>
<td align="left"><p>게시 된 응용 프로그램을 사용 하도록 설정 하려면이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>표시 이름</p></td>
<td align="left"><p>사용자&#39;s Windows 시작 메뉴의 바로 가기 이름입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>표시 이름은 <strong> </strong> 대/소문자를 구분 하지 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>사용자가 바로 가기를 마우스로 가리킬 때 도구 설명으로 표시 되는 게시 된 응용 프로그램에 대 한 설명입니다.&#39;.</p></td>
</tr>
<tr class="even">
<td align="left"><p>명령줄</p></td>
<td align="left"><p>MED-V 작업 영역 내에서 응용 프로그램을 실행 하는 데 사용 되는 명령입니다. 전체 경로가 필요 하며, 다른 Windows 명령과 비슷한 방식으로 매개 변수를 응용 프로그램에 전달할 수 있습니다.</p>
<p>Revertible med-v 작업 영역에서 mapnetworkdrive 구문: mapnetworkdrive 드라이브 경로를 사용 하 여 네트워크 드라이브를 매핑할 수 있습니다 &quot; <em> &lt; &gt; &lt; &gt; </em> &quot; (예: &quot; <em> mapnetworkdrive t: \name) </em> &quot; .</p>
<p>예를 들어 Windows 탐색기를 게시 하려면 &quot; <em> c: &lt; /em &gt; &quot; 또는 &quot; <em> c:\windows </em> 와 같은 구문을 사용 합니다.&quot;</p>
<div class="alert">
<strong>참고</strong><br/><p>이름 확인을 하려면 다음 중 하나를 수행 해야 합니다.</p>
</div>
<div>

</div>
<ul>
<li><p>기본 MED-V 작업 영역 이미지에서 DNS를 구성 합니다.</p></li>
<li><p>DNS 확인이 호스트에 정의 되어 있는지 확인 하 고 호스트 DNS를 사용 하도록 구성 합니다.</p></li>
<li><p>네트워크 드라이브를 정의 하는 데 IP를 사용 합니다.</p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>경로에 공백이 포함 되어 있으면 전체 경로가 따옴표로 묶여 있어야 합니다.</p>
</div>
<div>

</div>
<div class="alert">
<strong>참고</strong><br/><p>경로는 백슬래시 ()로 끝날 수 없습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>시작 메뉴</p></td>
<td align="left"><p>사용자&#39;s Windows 시작 메뉴에서 응용 프로그램에 대 한 바로 가기를 만들려면이 확인란을 선택 합니다.</p></td>
</tr>
</tbody>
</table>



게시 된 모든 응용 프로그램은 Windows **시작** 메뉴에서 바로 가기로 표시 됩니다 (** &gt; 모든 프로그램의 &gt; med-v 응용 프로그램 시작**).

## MED-V 작업 영역에서 게시 된 응용 프로그램을 제거 하는 방법


**MED-V 작업 영역에서 응용 프로그램을 제거 하려면**

1.  MED-V 작업 영역을 클릭 합니다.

2.  **응용 프로그램** 창의 **게시 된 응용 프로그램** 섹션에서 제거할 응용 프로그램을 선택 합니다.

3.  **제거**를 클릭 합니다.

    응용 프로그램이 게시 된 응용 프로그램 목록에서 제거 됩니다.

4.  **정책** 메뉴에서 **커밋을**선택 합니다.

## MED-V 작업 영역에 게시 된 메뉴를 추가 하는 방법


**MED-V 작업 영역에 게시 된 메뉴를 추가 하려면**

1.  MED-V 작업 영역을 클릭 하 여 구성 합니다.

2.  **응용 프로그램** 창의 **게시 된 메뉴** 구역에서 **추가** 를 클릭 하 여 새 메뉴를 추가 합니다.

3.  다음 표의 설명 대로 메뉴 속성을 구성 합니다.

4.  **정책** 메뉴에서 **커밋을**선택 합니다.

**게시 된 메뉴 속성**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>설정됨</p></td>
<td align="left"><p>게시 된 메뉴를 사용 하도록 설정 하려면이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>표시 이름</p></td>
<td align="left"><p>사용자&#39;s Windows 시작 메뉴의 바로 가기 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>사용자가 바로 가기를 마우스로 가리킬 때 도구 설명으로 표시 되는 설명입니다.&#39;합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>작업 영역의 폴더</p></td>
<td align="left"><p>폴더 내의 모든 응용 프로그램이 포함 된 메뉴로 게시할 폴더를 선택 합니다.</p>
<p>표시 되는 텍스트는 프로그램 폴더의 상대 경로입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 값을 비워 두면 호스트의 모든 프로그램이 메뉴로 게시 됩니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



모든 게시 된 메뉴는 Windows **시작** 메뉴에 바로 가기로 표시 됩니다 (** &gt; 모든 프로그램의 &gt; med-v 응용 프로그램 시작**). **시작 메뉴 바로 가기 폴더** 필드에서 바로 가기의 이름을 변경할 수 있습니다.

**참고**  
두 MED-V 작업 영역을 구성할 때 시작 메뉴 바로 가기 폴더에 대해 다른 이름을 구성 하는 것이 좋습니다.



## MED-V 작업 영역에서 게시 된 메뉴를 제거 하는 방법


**MED-V 작업 영역에서 게시 된 메뉴를 제거 하려면**

1.  MED-V 작업 영역을 클릭 합니다.

2.  **응용 프로그램** 창의 **게시 된 메뉴** 섹션에서 제거할 메뉴를 선택 합니다.

3.  **제거**를 클릭 합니다.

    메뉴가 게시 된 메뉴 목록에서 제거 됩니다.

4.  **정책** 메뉴에서 **커밋을**선택 합니다.

## 클라이언트의 명령줄에서 게시 된 응용 프로그램 실행


관리자는 다음 명령을 사용 하 여 바탕 화면 바로 가기 등의 모든 위치에서 게시 된 응용 프로그램을 실행할 수 있습니다.

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**참고**  
게시 된 응용 프로그램이 정의 된 MED-V 작업 영역이 실행 중 이어야 합니다.



## 관련 항목


[고급 설정으로 게시된 응용 프로그램을 편집하는 방법](how-to-edit-a-published-application-with-advanced-settings.md)

[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

[MED-V 작업 영역 만들기](creating-a-med-v-workspacemedv-10-sp1.md)









