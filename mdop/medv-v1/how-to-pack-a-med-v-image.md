---
title: MED-V 이미지를 압축하는 방법
description: MED-V 이미지를 압축하는 방법
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824678"
---
# MED-V 이미지를 압축하는 방법


MED-V 이미지를 배포 패키지에 추가 하거나 서버에 업로드 하기 전에 먼저 압축 해야 합니다.

**압축 된 MED-V 이미지를 만들려면**

1.  **이미지** 관리 단추를 클릭 합니다.

2.  **이미지** 모듈의 **로컬 압축 이미지** 창에서 **새로 만들기**를 클릭 합니다.

3.  압축 된 **이미지 만들기** 대화 상자에서 다음 중 하나를 수행 하 여 가상 컴퓨터 이미지를 선택 합니다.

    -   **기본 이미지 파일** 필드에 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리의 전체 경로를 입력 합니다.

    -   **찾아보기를** 클릭 하 여 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리로 이동 합니다.

4.  다음 중 하나를 수행 하 여 새 이미지의 이름을 지정 합니다.

    -   **이미지 이름** 필드에 원하는 이름을 입력 합니다.

        **참고**  
        Image 이름에는 다음 문자를 포함할 수 없습니다: space " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. **확인**을 클릭합니다.

   다음 표에 정의 된 속성을 사용 하 여 호스트 컴퓨터에 새 MED-V 압축 이미지가 만들어집니다.

**참고**  
서버 창의 **로컬 압축 이미지** 및 **압축 된 이미지** 에서 각 이미지의 최신 버전이 부모 노드로 표시 됩니다. 부모 노드를 클릭 하 여 다른 모든 기존 버전의 이미지를 표시 합니다.



**로컬 압축 이미지 속성**

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
<td align="left"><p>이미지 이름</p></td>
<td align="left"><p>관리자가 이미지를 만들었을 때 정의 된 압축 이미지의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>버전</p></td>
<td align="left"><p>표시 된 이미지의 버전입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이전 버전은 삭제 되지 않는 한 유지 됩니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>파일 크기 (압축)</p></td>
<td align="left"><p>이미지의 실제 압축 크기입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이미지 크기 (압축 되지 않음)</p></td>
<td align="left"><p>물리적으로 압축 되지 않은 이미지 크기입니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법](how-to-install-med-v-client-and-med-v-management-console.md)

[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

[MED-V에 대한 가상 PC 이미지 만들기](creating-a-virtual-pc-image-for-med-v.md)









