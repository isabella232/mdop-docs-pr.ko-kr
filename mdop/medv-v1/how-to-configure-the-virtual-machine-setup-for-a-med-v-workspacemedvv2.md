---
title: MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법
description: MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827073"
---
# MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법


모든 가상 컴퓨터 설정 구성 설정은 **정책** 모듈의 **VM 설정** 탭에서 구성 합니다.

## 영구 MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하는 방법


**영구 MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하려면**

1.  구성할 영구 MED-V 작업 영역을 클릭 합니다.

2.  **영구 VM 설정** 섹션에서 다음 표에 설명 된 대로 속성을 구성 합니다.

    **참고**  
    영구 VM 설정 속성은 영구 MED-V 작업 영역에만 사용할 수 있습니다.



3.  **정책** 메뉴에서 **커밋을**선택 합니다.

**영구 VM 설치 속성**

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
<td align="left"><p>VM 설치 프로그램 실행</p></td>
<td align="left"><p>MED-V 작업 영역을 처음 실행할 때 설정 스크립트를 실행 하려면이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>스크립트 편집기</p></td>
<td align="left"><p>설치 스크립트를 구성 하려면 클릭 합니다. 자세한 내용은 <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> 스크립트 동작을 설정 하는 방법을 참조 </a> 하세요.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 단추는 <strong> VM 설치 스크립트 실행이 선택 된 경우에만 사용할 수 </strong> 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>스크립트가 실행 중일 때 표시 되는 메시지</p></td>
<td align="left"><p>스크립트를 실행 하는 동안 표시할 메시지입니다. 공백으로 두면 기본 메시지가 표시 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 필드는 <strong> VM 설치 스크립트 실행이 선택 되어 있는 경우에만 사용할 수 </strong> 있습니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Revertible MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하는 방법


**Revertible MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하려면**

1.  Revertible MED-V 작업 영역을 클릭 하 여 구성 합니다.

2.  **REVERTIBLE VM 설정** 섹션에서 다음 표에 설명 된 대로 속성을 구성 합니다.

    **참고**  
    Revertible VM 설치 속성은 revertible MED-V 작업 영역에만 사용할 수 있습니다.



3.  **정책** 메뉴에서 **커밋을**선택 합니다.

**Revertible VM 설치 속성**

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
<td align="left"><p>컴퓨터 이름 패턴에 따라 VM 이름 바꾸기</p></td>
<td align="left"><p>동일한 MED-V 작업 영역을 사용 하 여 여러 컴퓨터를 구분할 수 있도록 MED-V 작업 영역을 사용 하 여 각 컴퓨터에 고유한 이름을 할당 하려면이 확인란을 선택 합니다.</p>
<p>컴퓨터 이미지 이름을 구성 하는 방법에 대 한 자세한 내용은 <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

[MED-V 작업 영역 만들기](creating-a-med-v-workspacemedv-10-sp1.md)

[가상 컴퓨터 구성의 예](examples-of-virtual-machine-configurationsv2.md)









