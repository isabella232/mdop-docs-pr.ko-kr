---
title: 보고서를 생성하는 방법
description: 보고서를 생성하는 방법
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826993"
---
# 보고서를 생성하는 방법


MED-V의 관리자는 다음 보고서 유형을 만들 수 있습니다.

-   [상태 (status](#bkmk-generatingastatusreport))-상태 보고서를 사용 하 여 지정 된 기간을 기준으로 각 사용자의 모든 활성 사용자 및 모든 med-v 작업 영역의 현재 상태를 검토 합니다. 여기에는 현재 서버에 연결 되어 있는 컴퓨터를 보거나, 현재 연결 되어 있지 않은 경우, 서버에 마지막으로 연결 된 날짜와 시간, 각 컴퓨터의 상태, 기타 관련 정보가 포함 됩니다.

-   [활동 로그](#bkmk-generatinganactivitylogreport)-이 보고서를 사용 하 여 정의 된 날짜 범위에서 특정 호스트 또는 사용자가 생성 한 이벤트를 검토 합니다.

-   [오류 로그](#bkmk-generatinganerrorlogreport)-이 보고서를 사용 하 여 정의 된 날짜 범위에서 특정 호스트 또는 사용자가 생성 한 오류를 봅니다.

적절 한 열 이름을 클릭 하 여 열을 기준으로 보고서 결과를 정렬할 수 있습니다.

보고서 결과는 열 머리글을 보고서의 맨 위로 끌어 그룹화 할 수 있습니다. 여러 열 머리글을 끌어 한 열 뒤에 그룹화 합니다.

## <a href="" id="bkmk-generatingastatusreport"></a>상태 보고서를 생성 하는 방법


**상태 보고서를 생성 하려면**

1.  **보고서** 관리 단추를 클릭 합니다.

2.  **보고서 모듈의** **보고서 형식** 메뉴에서 **상태**를 선택 하 고 **생성**을 클릭 합니다.

    보고서 매개 변수 대화 상자가 나타납니다.

3.  **보고서 매개 변수** 대화 상자의 **일 수** 필드에 숫자를 입력 하거나 화살표를 사용 하 여 상황 보고서에 포함할 일 수를 선택 하 고 **확인**을 클릭 합니다.

    상태 보고서가 생성 됩니다. 보고서 매개 변수는 다음 표에 정의 되어 있습니다.

**클라이언트 MED-V 작업 영역 속성**

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
<td align="left"><p>시간</p></td>
<td align="left"><p>이벤트가 발생 한 날짜 및 시간입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>기본적으로 이벤트는 내림차순 날짜 순서로 표시 됩니다. 그러나 받은 시간 열을 클릭 하 여 변경할 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 이름</p></td>
<td align="left"><p>이벤트를 시작한 사용자입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>사용자가 로그온 하기 전에 이벤트가 발생 한 경우 사용자 이름은 시스템입니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>호스트 이름</p></td>
<td align="left"><p>호스트 컴퓨터의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>작업 영역 이름</p></td>
<td align="left"><p>MED-V 작업 영역의 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>작업 영역 컴퓨터 이름</p></td>
<td align="left"><p>MED-V 작업 영역이 실행 되는 컴퓨터의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>온라인</p></td>
<td align="left"><p>클라이언트 컴퓨터의 현재 상태입니다.</p>
<ul>
<li><p><strong>멈추었습니다</strong></p></li>
<li><p><strong>&lt;작업 영역이 시작 된 날짜 및 시간에 시작 됨&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>클라이언트 버전</p></td>
<td align="left"><p>클라이언트의 버전 번호입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>정책 버전</p></td>
<td align="left"><p>MED-V 작업 영역이 현재 사용 중인 정책 버전입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>이미지 이름</p></td>
<td align="left"><p>이미지의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이미지 버전</p></td>
<td align="left"><p>MED-V 작업 영역이 현재 사용 중인 이미지 버전입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>컴퓨터에 아직 다운로드 하지 않은 경우 MED-V 작업 영역 버전을 알 수 없습니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a>활동 로그 보고서를 생성 하는 방법


**활동 로그 보고서를 생성 하려면**

1.  **보고서** 관리 단추를 클릭 합니다.

    보고서 모듈이 나타납니다.

2.  **보고서 모듈의** **보고서 형식** 메뉴에서 **활동 로그**를 선택 하 고 **생성**을 클릭 합니다.

3.  **보고서 매개 변수** 대화 상자에서 다음 매개 변수 중 하나 이상을 구성 합니다.

    -   **일 수**-보고서에 표시할 일 수입니다.

    -   **사용자 이름 포함**-입력 된 텍스트를 포함 하는 사용자 이름이 보고서에 포함 된 경우 사용 합니다.

    -   **호스트 이름에**는 호스트 이름에 입력 된 텍스트가 포함 된 모든 이벤트가 보고서에 포함 됩니다.

4.  **확인**을 클릭합니다.

    이벤트 및 날짜가 선택 된 상태로 보고서가 생성 됩니다. 보고서 매개 변수는 다음 표에 정의 되어 있습니다.

**활동 로그 보고서 속성**

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
<td align="left"><p>이벤트 ID</p></td>
<td align="left"><p>이벤트 ID입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>심각도</p></td>
<td align="left"><p><strong>정보, 오류, 경고</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>범주</p></td>
<td align="left"><p>보고서가 참조 하는 모듈입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설명</p></td>
<td align="left"><p>이벤트에 대 한 설명입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>수신 시간</p></td>
<td align="left"><p>서버에서 이벤트를 받은 날짜 및 시간입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>클라이언트가 오프 라인으로 작업 하는 경우 서버는 클라이언트가 온라인 상태일 때 보고서를 받습니다.</p>
</div>
<div>

</div>
<div class="alert">
<strong>참고</strong><br/><p>기본적으로 이벤트는 내림차순 날짜 순서로 표시 됩니다. 그러나 받은 시간 열을 클릭 하 여 변경할 수 있습니다 <strong> </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>클라이언트 시간</p></td>
<td align="left"><p>클라이언트 시계에 따라 이벤트가 발생 한 날짜와 시간입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>호스트 이름</p></td>
<td align="left"><p>호스트 컴퓨터의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 이름</p></td>
<td align="left"><p>이벤트를 시작한 사용자입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>작업 영역 이름</p></td>
<td align="left"><p>MED-V 작업 영역의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>작업 영역 컴퓨터 이름</p></td>
<td align="left"><p>MED-V 작업 영역이 실행 되는 컴퓨터의 이름입니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a>오류 로그 보고서를 생성 하는 방법


**오류 로그 보고서를 생성 하려면**

1.  **보고서** 관리 단추를 클릭 합니다.

2.  **보고서 모듈의** **보고서 유형** 메뉴에서 **오류 로그**를 선택 하 고 **생성**을 클릭 합니다.

3.  **보고서 매개 변수** 대화 상자에서 다음 매개 변수 중 하나 이상을 구성 합니다.

    -   **일 수**-보고서에 표시할 일 수입니다.

    -   **사용자 이름 포함**-입력 된 텍스트를 포함 하는 사용자 이름이 보고서에 포함 된 경우 사용 합니다.

    -   **호스트 이름에**는 호스트 이름에 입력 된 텍스트가 포함 된 모든 이벤트가 보고서에 포함 됩니다.

4.  **확인**을 클릭합니다.

    이벤트 및 날짜가 선택 된 상태로 보고서가 생성 됩니다. 보고서 매개 변수는 다음 표에 정의 되어 있습니다.

**오류 로그 보고서 속성**

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
<td align="left"><p>이벤트 ID</p></td>
<td align="left"><p>이벤트 ID입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>범주</p></td>
<td align="left"><p>보고서가 참조 하는 모듈입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>이벤트에 대 한 설명입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>수신 시간</p></td>
<td align="left"><p>서버에서 이벤트를 받은 날짜 및 시간입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>클라이언트가 오프 라인으로 작업 하는 경우 서버는 클라이언트가 온라인 상태일 때 보고서를 받습니다.</p>
</div>
<div>

</div>
<div class="alert">
<strong>참고</strong><br/><p>기본적으로 이벤트는 내림차순 날짜 순서로 표시 됩니다. 그러나 받은 시간 열을 클릭 하 여 변경할 수 있습니다 <strong> </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>클라이언트 시간</p></td>
<td align="left"><p>클라이언트 시계에 따라 이벤트가 발생 한 날짜와 시간입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>호스트 이름</p></td>
<td align="left"><p>호스트 컴퓨터의 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 이름</p></td>
<td align="left"><p>이벤트를 시작한 사용자입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>작업 영역 이름</p></td>
<td align="left"><p>MED-V 작업 영역의 이름입니다.</p></td>
</tr>
</tbody>
</table>











