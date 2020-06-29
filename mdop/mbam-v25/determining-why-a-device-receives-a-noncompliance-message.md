---
title: 장치에서 규정 미준수 메시지를 수신하는 이유 확인
description: 장치에서 규정 미준수 메시지를 수신하는 이유 확인
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824573"
---
# 장치에서 규정 미준수 메시지를 수신하는 이유 확인


다음 비 호환성 코드는 WMI에서 제공 되며, 비규격으로 인해 특정 장치가 보고 되는 이유를 설명 합니다.

선호 하는 방법을 사용 하 여 WMI를 볼 수 있습니다. PowerShell을 사용 하는 경우 `gwmi -class mbam_volume -Namespace root\microsoft\mbam` powershell 프롬프트에서 실행 하 고 ReasonsForNoncompliance를 검색 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">비호환 코드</th>
<th align="left">준수 하지 않는 이유</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>0</p></td>
<td align="left"><p>암호화 강도가 AES 256이 아닙니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>raid-1</p></td>
<td align="left"><p>MBAM 정책은이 볼륨을 암호화 해야 하지만, 그렇지 않은 경우에는 그렇지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>MBAM 정책에서는이 볼륨을 암호화 하지 않아도 되지만,</p></td>
</tr>
<tr class="even">
<td align="left"><p>3-4</p></td>
<td align="left"><p>MBAM 정책은이 볼륨에 TPM 보호기를 사용 해야 하지만, 그렇지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4(tcp/ipv4)</p></td>
<td align="left"><p>이 볼륨에는이 볼륨이 TPM + PIN 보호기를 사용 해야 하지만 MBAM 정책이 필요 하지는 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>5mb</p></td>
<td align="left"><p>MBAM 정책은 비 TPM 컴퓨터를 규격으로 보고 하도록 허용 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>26</p></td>
<td align="left"><p>볼륨에 TPM 보호기가 있지만 TPM이 표시 되지 않습니다 (BIOS에서 TPM을 사용 하지 않도록 설정한 후 복구 키로 부팅 됨).</p></td>
</tr>
<tr class="even">
<td align="left"><p>7</p></td>
<td align="left"><p>이 볼륨에는 암호 보호기를 사용 해야 하지만 MBAM 정책에는 암호가 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>20cm(8</p></td>
<td align="left"><p>MBAM 정책에 의해이 볼륨에는 암호 보호기가 사용 되지 않지만, 하나는 필요 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>되었는지</p></td>
<td align="left"><p>이 볼륨에는이 볼륨이 자동 잠금 해제 보호 기능을 사용 하도록 요구 하지만 MBAM 정책에는 포함 되어 있지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>1천만</p></td>
<td align="left"><p>MBAM 정책에 의해이 볼륨에는 자동 잠금 해제 보호기가 사용 되지 않지만, 하나는 필요 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>mb</p></td>
<td align="left"><p>정책 충돌이 감지 되어 MBAM이이 볼륨을 준수 하는 것으로 보고 하지 못하도록 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>까지</p></td>
<td align="left"><p>시스템 볼륨이 OS 볼륨을 암호화 하는 데 필요 하지만 제공 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>일자</p></td>
<td align="left"><p>볼륨에 대 한 보호가 일시 중단 되었습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>13</p></td>
<td align="left"><p>OS 볼륨이 암호화 되지 않은 경우 AutoUnlock 안전 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>~</p></td>
<td align="left"><p>정책에는 최소 cypher 강도가 XTS-AES-128 비트 이지만 실제 cypher 강도가 약한 것 보다 적습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>정책에는 최소 cypher 강도가 XTS-AES-256 비트 이지만 실제 cypher 강도가 약한 것 보다 적습니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 2.5에 대한 기술 참조](technical-reference-for-mbam-25.md)

[Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





