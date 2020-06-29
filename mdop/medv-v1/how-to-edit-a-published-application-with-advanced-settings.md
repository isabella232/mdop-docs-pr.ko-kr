---
title: 고급 설정으로 게시된 응용 프로그램을 편집하는 방법
description: 고급 설정으로 게시된 응용 프로그램을 편집하는 방법
author: dansimp
ms.assetid: 06a79049-9ce9-490f-aad7-fd4fdf185590
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 843aebb38f54959f209e742b398e3979acac3334
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826998"
---
# 고급 설정으로 게시된 응용 프로그램을 편집하는 방법


게시 된 응용 프로그램을 추가 하 고 구성한 후에는 게시 된 응용 프로그램을 편집할 수 있고 추가 고급 설정을 구성할 수 있습니다.

**고급 설정을 사용 하 여 게시 된 응용 프로그램 편집**

1.  **응용 프로그램** 창에서 게시 된 응용 프로그램을 추가 하 고 구성 합니다.

2.  편집할 게시 된 응용 프로그램을 선택 합니다.

3.  **편집**을 클릭합니다.

4.  게시 된 **응용 프로그램** 대화 상자에서 다음 표에 설명 된 대로 매개 변수를 구성 합니다.

5.  **확인**을 클릭합니다.

6.  **정책** 메뉴에서 **커밋을**선택 합니다.

**게시 된 응용 프로그램 속성 편집**

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
<td align="left"><p>표시 이름</p></td>
<td align="left"><p>사용자&#39;s Windows 시작 메뉴의 바로 가기 이름입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>표시 이름은 <strong> </strong> 대/소문자를 구분 하지 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>설명</p></td>
<td align="left"><p>게시 된 메뉴에 대 한 설명입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>시작</p></td>
<td align="left"><p>응용 프로그램을 시작할 디렉터리입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>경로에 따옴표를 포함할 필요는 없습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>명령줄</p></td>
<td align="left"><p>MED-V 작업 영역 내에서 응용 프로그램을 실행 하는 데 사용할 명령입니다.</p>
<p>전체 경로가 필요 하며, 다른 Windows 명령과 비슷한 방식으로 매개 변수를 응용 프로그램에 전달할 수 있습니다.</p>
<p>도메인 구성에서 공유 드라이브는 일반적으로 모든 도메인 컴퓨터가 매핑되는 서버에 있습니다. 여기에 디렉터리를 매핑하고 사용자 인증이 필요한 폴더인 경우 <strong> 에는이 응용 프로그램을 실행 하는 데 med-v 자격 증명 사용 </strong> 확인란을 선택 해야 합니다.</p>
<p>Revertible med-v 작업 영역에서 mapnetworkdrive 구문: &quot; <em> mapnetworkdrive &lt; 드라이브, 예를 들어 mapnetworkdrive &gt; &lt; &gt; </em> &quot; &quot; <em> t: \tux\data </em> &quot; 와 같은 네트워크 드라이브를 매핑할 수 있습니다.</p>
<p>예를 들어 Windows 탐색기를 게시 하려면 &quot; <em> c: &amp; "또는 &quot; c:\windows와 </em> &quot; 같은 구문을 사용 합니다.</p>
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
<td align="left"><p>호스트 Windows 시작 메뉴에 바로 가기 추가</p></td>
<td align="left"><p>사용자&#39;s Windows 시작 메뉴에서 응용 프로그램에 대 한 바로 가기를 만들려면이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>작업 영역이 시작 될 때이 응용 프로그램 시작</p></td>
<td align="left"><p>MED-V 작업 영역이 시작 될 때 응용 프로그램을 자동으로 실행 하려면이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MED-V 자격 증명을 사용 하 여이 응용 프로그램 실행</p></td>
<td align="left"><p>이 확인란을 선택 하 여 응용 프로그램에 대 한 자격 증명 집합 대신 MED-V 자격 증명을 사용 하 여 사용자 이름과 암호를 요청 하는 응용 프로그램을 인증 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>SSO를 사용 하는 경우 명령줄은 <strong> 폴더 경로C:\Windows\Explorer.exe 해야 합니다 &quot; &quot; </strong> . SSO를 사용 하지 않는 경우 명령줄이 &quot; <strong> 폴더 경로 여야 합니다 </strong> &quot; .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## 관련 항목


[게시된 응용 프로그램을 구성하는 방법](how-to-configure-published-applicationsmedvv2.md)









