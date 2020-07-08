---
title: PowerShell을 사용하여 MBAM 2.0 관리
description: PowerShell을 사용하여 MBAM 2.0 관리
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823503"
---
# PowerShell을 사용하여 MBAM 2.0 관리


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음과 같이 나열 된 Windows PowerShell cmdlet 집합을 제공 합니다. 관리자는이 PowerShell cmdlet을 사용 하 여 MBAM 관리 웹 사이트가 아닌 명령줄에서 다양 한 Microsoft BitLocker 관리 및 모니터링 서버 작업을 수행할 수 있습니다.

## PowerShell을 사용 하 여 MBAM을 관리 하는 방법


여기에 설명 된 PowerShell cmdlet을 사용 하 여 MBAM을 관리 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>설치-Mbam</p></td>
<td align="left"><p>고급 정책, 암호화, 키 복구, 준수 보고를 제공 하는 MBAM 기능을 설치 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제거-Mbam</p></td>
<td align="left"><p>고급 정책, 암호화, 키 복구, 준수 보고 도구를 제공 하는 MBAM 기능을 제거 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>사용자가 컴퓨터 또는 암호화 된 드라이브의 잠금을 해제할 수 있는 MBAM 키를 요청 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-Mbamtpmo<c13> Erpassword</p></td>
<td align="left"><p>Tpm에서 tpm (신뢰할 수 있는 플랫폼 모듈)을 잠그고 해당 사용자의 PIN을 더 이상 허용 하지 않는 경우 잠금을 해제 하는 데 사용할 수 있는 TPM 소유자 암호를 제공 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 2.0 작업](operations-for-mbam-20-mbam-2.md)

 

 





