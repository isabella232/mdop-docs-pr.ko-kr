---
title: PowerShell을 사용하여 MBAM 1.0 관리
description: PowerShell을 사용하여 MBAM 1.0 관리
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825138"
---
# PowerShell을 사용하여 MBAM 1.0 관리


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음과 같이 나열 된 Windows PowerShell cmdlet 집합을 제공 합니다. 관리자는 이러한 PowerShell cmdlet을 사용 하 여 MBAM 관리 웹 사이트 대신 명령 프롬프트에서 다양 한 MBAM 서버 작업을 수행할 수 있습니다.

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
<td align="left"><p>추가-Mbam하드 다시 입력</p></td>
<td align="left"><p>MBAM 하드웨어 인벤토리에 새 하드웨어 모델을 추가 합니다. 이 cmdlet은 하드웨어가 BitLocker 드라이브 암호화에 지원 되는지 또는 지원 되지 않는 경우에도 지정할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>사용자가 컴퓨터 또는 암호화 된 드라이브의 잠금을 해제할 수 있는 MBAM 키를 요청 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-Mbam하드 다시 입력</p></td>
<td align="left"><p>하드웨어 모델이 BitLocker 드라이브 암호화와 호환 되는지 또는 호환 되지 않는지 여부를 나타내는 데이터를 포함 하는 마스터 하드웨어 인벤토리를 가져옵니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-Mbamtpmo<c13> Erpassword</p></td>
<td align="left"><p>사용자가 TPM (신뢰할 수 있는 플랫폼 모듈) 액세스를 관리 하는 데 사용할 TPM 소유자 암호를 제공 합니다. TPM이 파일을 잠그고 해당 PIN을 더 이상 허용 하지 않는 사용자에 게 도움을 줍니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설치-Mbam</p></td>
<td align="left"><p>고급 그룹 정책, 암호화, 키 복구, 준수 보고 도구를 제공 하는 MBAM 기능을 설치 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제거-Mbam하드 다시 입력</p></td>
<td align="left"><p>하드웨어 인벤토리에서 하드웨어 모델을 제거 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정-Mbam하드 다시 입력</p></td>
<td align="left"><p>하드웨어 모델이 BitLocker 암호화를 수행할 수 있는지 여부를 지정 하기 위해 마스터 하드웨어 인벤토리를 관리할 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제거-Mbam</p></td>
<td align="left"><p>고급 정책, 암호화, 키 복구, 준수 보고 도구를 제공 하는 이전에 설치 된 MBAM 기능을 제거 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 1.0 작업](operations-for-mbam-10.md)

 

 





