---
title: BitLocker 암호화 옵션 및 제어판의 BitLocker 드라이브 암호화 항목 이해
description: BitLocker 암호화 옵션 및 제어판의 BitLocker 드라이브 암호화 항목 이해
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812772"
---
# BitLocker 암호화 옵션 및 제어판의 BitLocker 드라이브 암호화 항목 이해


이 항목에서는 **Bitlocker 암호화 옵션** 및 **bitlocker 드라이브 암호화** 제어판 항목에 대해 설명 하 고 다음을 설명 합니다.

-   이러한 항목을 만드는 방법

-   수행할 수 있는 작업

-   **BitLocker 관리** "마우스 오른쪽 단추 클릭"이 표시 되는 경우 바로 가기 메뉴에서 또는 숨겨진 경우와 기본적으로 표시 되도록 설정 하는 방법

## BitLocker 암호화 옵션 및 BitLocker 드라이브 암호화 제어판 항목


다음 표에서는 각 제어판 항목에서 수행할 수 있는 작업을 보여 주고 이러한 항목을 만드는 방법을 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">BitLocker 암호화 옵션 (MBAM)</th>
<th align="left">BitLocker 드라이브 암호화 (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>수행할 수 있는 작업</p></td>
<td align="left"><ul>
<li><p>PIN 또는 암호 변경</p></li>
<li><p>드라이브에 대 한 암호화 상태 확인</p></li>
<li><p>TPM 관리 콘솔 열기</p></li>
<li><p>BitLocker 켜기</p></li>
</ul></td>
<td align="left"><ul>
<li><p>드라이브 보호 일시 중단</p></li>
<li><p>복구 키 백업</p></li>
<li><p>PIN 변경</p></li>
<li><p>드라이브에 대 한 BitLocker 끄기</p></li>
<li><p>드라이브에 대 한 BitLocker 켜기</p></li>
<li><p>TPM 관리 콘솔 열기</p></li>
<li><p>드라이브 암호 해독 (MBAM 클라이언트가 설치 되어 있지 않은 경우에만 나타남)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>제어판 항목을 만드는 방법</p></td>
<td align="left"><p>MBAM 클라이언트를 설치 하면 제어판에서 만들어집니다. 이 항목은 숨길 수 없습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 항목은 기본 BitLocker 드라이브 암호화 제어판 항목 외에도 표시 되지만 대체 되지는 않습니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>제어판은 기본적으로 Windows 운영 체제의 일부로 표시 되지만 숨길 수 있습니다.</p>
<p>이 <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> 창을 숨기려면 제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기를 참조 </a> 하세요.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>"BitLocker 관리" 바로 가기 메뉴


다음 표에서는 MBAM 클라이언트 설치 여부에 따라 **BitLocker 관리** 바로 가기 메뉴의 차이점에 대해 설명 합니다. "바로 가기 메뉴" 라는 용어는 Windows 탐색기에서 드라이브를 마우스 오른쪽 단추로 클릭할 때 표시 되는 옵션을 의미 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">MBAM 클라이언트가 설치 된 경우</th>
<th align="left">MBAM 클라이언트가 설치 되어 있지 않은 경우</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>바로 가기 메뉴 표시</p></td>
<td align="left"><p>BitLocker 관리 옵션이 숨겨져 있습니다.</p>
<p>바로 가기 메뉴에 BitLocker 관리 옵션을 표시 하 여 드라이브의 암호를 해독 하는 옵션이 표시 되 게 하려면 다음 레지스트리 키를 삭제 합니다.</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>바로 가기 메뉴에 BitLocker 관리 옵션이 나타납니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자가 수행할 수 있는 작업</p></td>
<td align="left"><p>바로 가기가 숨겨져 있는 경우 사용자는 BitLocker 드라이브 암호화 제어판 항목을 열 수 있지만 드라이브 암호를 해독 하는 옵션을 사용할 수 없습니다.</p></td>
<td align="left"><p>바로 가기가 표시 된 상태에서 <strong> bitlocker 관리 옵션을 선택 하면 드라이브의 암호를 </strong> 해독 하는 옵션이 표시 된 Bitlocker 드라이브 암호화 제어판 항목이 열립니다.</p></td>
</tr>
</tbody>
</table>




## 관련 항목


[MBAM 2.5 기능 관리](administering-mbam-25-features.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





