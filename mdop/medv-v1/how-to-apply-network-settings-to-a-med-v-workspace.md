---
title: MED-V 작업 영역에 네트워크 설정을 적용하는 방법
description: MED-V 작업 영역에 네트워크 설정을 적용하는 방법
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826518"
---
# MED-V 작업 영역에 네트워크 설정을 적용하는 방법


관리자는 각 MED-V 작업 영역에 대 한 네트워크 설정을 정의할 수 있습니다.

**네트워크 탭의** **정책** 모듈에서 모든 네트워크 설정을 구성 합니다.

**MED-V 작업 영역에 네트워크 설정을 적용 하려면**

1.  MED-V 작업 영역을 클릭 하 여 구성 합니다.

2.  **네트워크** 창에서 다음 표에 설명 된 대로 설정을 구성 합니다.

3.  **정책** 메뉴에서 **커밋을**선택 합니다.

**MED-V 작업 영역 네트워크 속성**

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
<td align="left"><p>TCP/IP 속성</p></td>
<td align="left"><ul>
<li><p><strong>호스트의 IP 주소 (NAT) 사용 </strong> -작업 영역에서 nat를 사용 하 여 송신 트래픽에 대 한 호스트의 IP를 공유 하 게 됩니다.</p></li>
<li><p><strong>호스트와 다른 IP 주소 사용 (브리지) </strong> -med-v 작업 영역에는 일반적으로 DHCP를 통해 얻을 수 있는 고유한 네트워크 주소가 있습니다.</p></li>
</ul>
<p><strong>호스트 컴퓨터에 여러 어댑터가 있으면 작업 영역에 여러 어댑터 매핑 확인란을 선택 합니다 </strong> . 호스트가 다른 어댑터를 사용 하는 다른 네트워크 간을 이동할 때이 구성을 사용 하는 것이 좋습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DNS 서버</p></td>
<td align="left"><ul>
<li><p><strong>변경 안 함 </strong> -med-v 작업 영역에 설정 된 DNS 설정은 가상 컴퓨터에서 변경 되지 않습니다.</p></li>
<li><p><strong>호스트의 DNS 주소 사용 </strong> -med-v 작업 영역 dns 설정은 호스트의 설정에 맞게 동기화 됩니다. DNS 동기화는 동적입니다. 호스트에서 변경 되 면 MED-V 작업 영역에서 동적으로 변경 되도록 호스트와 정기적으로 동기화 됩니다.</p></li>
<li><p><strong>특정 DNS 주소 사용 </strong> -med-v 작업 영역에서 지정 된 대로 특정 dns를 사용 합니다.</p>
<p><strong>기본 </strong> 및 <strong> 보조 필드에 </strong> 기본 및 보조 DNS 주소를 입력 합니다.</p>
<p>호스트의 <strong> dns 주소 추가 확인란을 선택 </strong> 하 여 호스트를 구성 된 DNS 주소에 추가 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS 접미사 할당</p></td>
<td align="left"><ul>
<li><p><strong>다음 접미사 할당 </strong> -이 확인란을 선택 하 여 특정 DNS 접미사를 할당 하 고 상자에서 접미사 또는 쉼표로 구분 된 여러 접미사를 입력 합니다.</p></li>
<li><p><strong>호스트 접미사 추가 </strong> -호스트 접미사를 DNS 주소에 추가 하려면이 확인란을 선택 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MED-V 작업 영역 만들기](creating-a-med-v-workspacemedv-10-sp1.md)

[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

 

 





