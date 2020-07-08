---
title: AGPM 4.0 SP3의 새로운 기능
description: AGPM 4.0 SP3의 새로운 기능
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: a98bda82fab561113522382b4de6539a9dc23d0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820118"
---
# AGPM 4.0 SP3의 새로운 기능


이 콘텐츠는 Microsoft AGPM (고급 그룹 정책 관리) (SP3) 4.0 서비스 Pack3의 향상 된 구성 및 지원 되는 구성을 설명 합니다. 이 콘텐츠와 다른 AGPM 설명서 사이에 차이가 있는 경우이 콘텐츠를 신뢰할 수 있는 것으로 간주 하 고 다른 문서를 대체 한다고 가정 합니다.

## <a href="" id="what-s-new"></a>새로운 기능


AGPM 4.0 SP3은 다음 기능과 기능을 지원 합니다.

### Windows10에 대 한 지원

AGPM 4.0 SP3은 Windows10 및 Windows Server 2016 운영 체제에 대 한 지원을 추가 합니다.

### PowerShell에 대 한 지원

AGPM 4.0 SP3에는 PowerShell cmdlet에 대 한 지원이 추가 되었습니다. 설명 및 구문을 비롯 하 여 AGPM 4.0 SP3에서 사용할 수 있는 cmdlet 목록은 [Windows PowerShell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps)를 참조 하세요.

### 고객 의견 및 핫픽스 롤업

AGPM 4.0 SP3에는 Microsoft 고급 그룹 정책 관리 4.0 SP2에 대 한 모든 수정 사항에 대 한 롤업을 비롯 하 여 AGPM 4.0 SP2 이후 발견 된 문제에 대 한 수정 사항이 포함 되어 있습니다.

### 구성 매개 변수를 다시 입력 하지 않고 AGPM 4.0 SP3으로 업그레이드 하는 기능

다음 표에 표시 된 대로 agpm 4.0 이상 에서만 구성 매개 변수 (스마트 업그레이드)를 다시 입력 하 라는 메시지가 표시 되지 않고 agpm 클라이언트 또는 AGPM 서버를 AGPM 4.0 SP3으로 업그레이드할 수 있습니다. 표에서와 같이 다른 버전의 AGPM으로 AGPM 4.0 SP3으로 업그레이드 하는 경우에는 구성 매개 변수를 다시 입력 해야 하는 클래식 업그레이드를 사용 해야 합니다. 각 버전의 AGPM이 특정 운영 체제와 연결 되어 있기 때문에 [설치할 Agpm 버전 선택을](https://go.microsoft.com/fwlink/?LinkId=254350) 참조 하 여 agpm을 업그레이드 하기 전에 해당 운영 체제를 적절 하 게 업그레이드 해야 합니다.

**AGPM 4.0 SP3 지원 되는 업그레이드**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>업그레이드할 수 있는 AGPM 버전</strong></p></td>
<td align="left"><p><strong>2.5</strong></p></td>
<td align="left"><p><strong>3.0</strong></p></td>
<td align="left"><p><strong>4.0</strong></p></td>
<td align="left"><p><strong>4.0 SP1</strong></p></td>
<td align="left"><p><strong>4.0 SP2</strong></p></td>
<td align="left"><p><strong>4.0 SP3</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2.5</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>설치 차단 됨</p></td>
<td align="left"><p>설치 차단 됨</p></td>
<td align="left"><p>설치 차단 됨</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3.0</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>설치 차단 됨</p></td>
<td align="left"><p>설치 차단 됨</p></td>
<td align="left"><p>설치 차단 됨</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.0</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4.0 SP1</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.0 SP2</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
</tr>
</tbody>
</table>

 

## 지원되는 구성


AGPM 4.0 SP3은 다음 표의 구성을 지원 합니다. AGPM이 혼합 구성을 지원 하지만, Windows Server 2016, windows 8.1 for windows Server 2012 R2 등의 운영 체제 줄에 AGPM 클라이언트와 AGPM 서버를 실행 하는 것이 좋습니다 (예: Windows10).

**AGPM 4.0 SP3 지원 되는 운영 체제 및 정책 설정**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>AGPM 서버에서 지원 되는 구성</strong></th>
<th align="left"><strong>AGPM 클라이언트에 대해 지원 되는 구성</strong></th>
<th align="left"><strong>AGPM 지원</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2016 또는 Windows 10</p></td>
<td align="left"><p>Windows10</p></td>
<td align="left"><p>지원</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 또는 Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 또는 Windows 8.1</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 또는 Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</p></td>
<td align="left"><p>지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP3 설치를 위한 필수 구성 요소

다음 표에서는 원격 서버 관리 도구의 .NET Framework 4.5.1, PowerShell 3.0 또는 GPMC가 없는 경우 AGPM 4.0 SP3 클라이언트 및 서버 설치 관리자의 동작에 대해 설명 합니다.

| AGPM 클라이언트            |                                                                                                 |                                                                            | AGPM 서버                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| 운영 체제       | .NET Framework                                                                                  | PowerShell                                                                 | 원격 서버 관리 도구                                              | .NET Framework                                                                                  | 원격 서버 관리 도구                                              |
| Windows 10             | .NET Framework 4.5.1을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | Powershell 3.0이 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다. | GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | .NET Framework 4.5.1을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다. |
| Windows 8.1            | .NET Framework 4.5.1을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | Powershell 3.0이 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다. | GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | .NET Framework 4.5.1을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다. |
| Windows Server 2012 R2 | .NET Framework 4.5.1을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | Powershell 3.0이 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다. | GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.   | .NET Framework 4.5.1을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다. | GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.   |

 

## MDOP 기술을 활용 하는 방법


AGPM 4.0 SP3은 MDOP 2015 이후 Microsoft 데스크톱 최적화 팩 (MDOP)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .

## 관련 항목


[고급 그룹 정책 관리](index.md)

[Microsoft 고급 그룹 정책 관리 4.0 SP3 릴리스 정보](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[설치할 AGPM 버전 선택](choosing-which-version-of-agpm-to-install.md)

 

 





