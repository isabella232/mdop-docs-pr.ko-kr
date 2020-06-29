---
title: MED-V 작업 영역에 대한 웹 설정을 구성하는 방법
description: MED-V 작업 영역에 대한 웹 설정을 구성하는 방법
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827068"
---
# MED-V 작업 영역에 대한 웹 설정을 구성하는 방법


이전 버전의 Internet Explorer 에서만 표시할 수 있고 호스트 운영 체제에는 없는 웹 사이트는 MED-V 작업 영역 내에 있는 이전 버전의 Internet Explorer에서 볼 수 있습니다. 사용자가 MED-V 작업 영역에서 브라우저를 열지 않아도 지정 된 웹 사이트를 볼 수 있습니다. 사용자는 호스트에서 브라우저를 열고 MED-V 작업 영역으로 자동으로 리디렉션되고 그 반대의 경우도 마찬가지입니다.

다음 절차에서는 MED-V 작업 영역의 웹 검색 규칙 목록을 설정 하는 방법에 대해 설명 합니다. 규칙에 포함 된 모든 사이트는 MED-V 작업 영역이 나 관리자가 정의한 호스트에서 찾아볼 수 있습니다. 규칙 내에 정의 되지 않은 모든 사이트는 해당 사이트가 요청 된 환경에서 탐색 됩니다. 그러나이를 그룹으로 구성 하 여 MED-V 작업 영역이 나 호스트에서 검색할 수도 있습니다.

**참고**  
웹 설정은 Internet Explorer 및 다른 브라우저에만 적용 됩니다.



모든 웹 설정은 **정책** 모듈의 **웹** 탭에 구성 되어 있습니다.

## MED-V 작업 영역에 대 한 웹 설정을 구성 하는 방법


**MED-V 작업 영역에 대 한 웹 설정을 구성 하려면**

1.  구성할 MED-V 작업 영역을 클릭 합니다.

2.  사용자가 지정 된 웹 규칙을 준수 하는 URL을 탐색할 때 사용자를 MED-V 작업 영역 또는 호스트 내의 브라우저로 리디렉션하려면 **다음 표에 정의 된 url 목록 검색** 확인란을 선택 합니다.

3.  다음 중 하나를 클릭 합니다.

    -   **작업 영역에서**-med-v 작업 영역의 브라우저로 이동 합니다.

    -   **호스트에서**-호스트의 브라우저로 리디렉션합니다.

4.  **다른 모든 Url 찾아보기** 확인란을 선택 하 여 웹 규칙에서 제외한 모든 url을 호스트 또는 med-v 작업 영역으로 리디렉션합니다.

5.  다음 중 하나를 클릭 합니다.

    -   **작업 영역에서**-다른 모든 URL을 med-v 작업 영역의 브라우저로 리디렉션합니다.

    -   **호스트에서**— 다른 모든 url을 호스트의 브라우저로 리디렉션합니다.

6.  **정책** 메뉴에서 **커밋을**선택 합니다.

## 웹 규칙을 추가 하는 방법


**웹 규칙을 추가 하려면**

1.  **다음 표에 정의 된 url 목록 찾아보기** 확인란을 선택 하 여 웹 검색 규칙을 사용 하도록 설정 합니다.

2.  **추가**를 클릭합니다.

    새 웹 규칙이 추가 됩니다.

3.  다음 표의 설명 대로 웹 규칙 속성을 구성 합니다.

4.  **정책** 메뉴에서 **커밋을**선택 합니다.

**MED-V 작업 영역 웹 속성**

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
<td align="left"><p>유형</p></td>
<td align="left"><ul>
<li><p><strong>도메인 접미사 </strong> -Value 속성에 지정 된 접미사로 끝나는 모든 호스트 주소에 대 <strong> </strong> 한 액세스 이며 웹 검색의 옵션 집합에 따라 설정 됩니다 <strong> </strong> .</p></li>
<li><p><strong>IP 접두사 </strong> -Value 속성에 지정 된 접두사 범위에서 전체 또는 부분 IP 주소에 액세스 하 <strong> </strong> 고 웹 검색에 설정 된 옵션에 따라 설정 됩니다 <strong> </strong> .</p></li>
<li><p><strong>모든 로컬 주소 </strong> -&#39; 없이 모든 주소에 액세스 하며, 웹 검색의 옵션 집합에 따라 설정 됩니다 &#39;. <strong> </strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>값</p></td>
<td align="left"><ul>
<li><p><strong> </strong> Type 속성에 도메인 접미사가 선택 되어 <strong> 있으면 </strong> 도메인 접미사를 입력 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><ul>
<li><p>&quot; * &quot; 접미사 앞에 입력 하지 마세요.</p></li>
<li><p>도메인 접미사는 별칭도 지원 합니다.</p></li>
</ul>
</div>
<div>

</div></li>
<li><p>Type 속성에서 IP 접두사를 선택한 <strong> 경우 </strong> 전체 또는 일부 ip 주소를 입력 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>



## 웹 규칙을 삭제 하는 방법


**웹 규칙을 삭제 하려면**

1.  **웹** 창에서 삭제할 웹 규칙을 선택 합니다.

2.  **제거**를 클릭 합니다.

    웹 규칙이 삭제 됩니다.

## 관련 항목


[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

[MED-V 작업 영역 만들기](creating-a-med-v-workspacemedv-10-sp1.md)









