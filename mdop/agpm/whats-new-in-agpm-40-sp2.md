---
title: AGPM 4.0 SP2의 새로운 기능
description: AGPM 4.0 SP2의 새로운 기능
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818148"
---
# AGPM 4.0 SP2의 새로운 기능


이 콘텐츠는 Microsoft AGPM (고급 그룹 정책 관리)의 Pack2에 대 한 향상 된 구성 및 지원 되는 SP2 (서비스)를 설명 합니다. 이 콘텐츠와 다른 AGPM 설명서 사이에 차이가 있는 경우이 콘텐츠를 신뢰할 수 있는 것으로 간주 하 고 다른 문서를 대체 한다고 가정 합니다.

## <a href="" id="what-s-new"></a>새로운 기능


AGPM 4.0 SP2는 다음 기능과 기능을 지원 합니다.

### Windows 8.1 및 Windows Server2012 R2에 대 한 지원

AGPM 4.0 SP2는 Windows 8.1 및 Windows Server2012 R2 운영 시스템에 대 한 지원을 추가 합니다.

### 새로 만들고 변경 된 클라이언트 쪽 확장

Windows 8.1에서 새 정책 설정을 지원 하도록 AGPM에 대해 그룹 정책 클라이언트 쪽 확장이 추가 또는 변경 되었습니다. 그룹 정책 관리자는 이러한 정책 설정을 통해 두 Gpo (그룹 정책 개체) 또는 서식 파일 간에 변경 되는 Windows 8.1 관련 정책 설정을 관리 하 고 추적할 수 있습니다. 클라이언트 쪽 확장을 보려면 AGPM 클라이언트에서 사용할 수 있는 설정 및 차이점 보고서를 사용 합니다.

새로 만들고 변경 된 그룹 정책 클라이언트 쪽 확장명은 다음과 같습니다.

-   **클라우드 폴더 설정을 지정**합니다. 이 정책 설정을 사용 하면 IT 관리자가 클라우드 폴더를 자동으로 만들도록 구성할 수 있습니다. 클라우드 폴더 기능을 사용 하면 최종 사용자가 Windows 데스크톱 장치에서 다른 장치로 파일을 동기화 할 수 있습니다. 이 정책 설정을 사용 하 여 최종 사용자의 장치에 대 한 동기화 관계를 만들고 사용자의 클라우드 폴더를 저장 하는 파일 서버를 식별 하는 방법을 구성 합니다. **자동 프로 비전 동기화** 확인란을 선택 하면 사용자 입력 없이 동기화 파트너 관계가 생성 되 고 데이터가 자동으로 사용자의 디바이스와 동기화 시작 됩니다. **자동 프로 비전 동기화** 확인란을 선택 하지 않은 경우 사용자가 동기화를 시작 하기 위한 입력을 제공 해야 합니다.

-   **모든 사용자에 대해 자동 설정을 적용**합니다. 이 정책 설정을 사용 하면 IT 관리자가 최종 사용자의 입력 없이 최종 사용자 장치에서 자동으로 클라우드 폴더 파트너 관계를 만들지 여부를 결정할 수 있습니다. 이 정책 설정을 사용 하면 **클라우드 폴더 설정 지정** 정책 설정을 구성 하는 방법에 따라 동기화가 설정 됩니다. **모든 사용자에 대해 자동 설정 적용** 정책 설정을 **사용 안 함** 또는 **구성 되지 않음**으로 설정한 경우 **클라우드 폴더 설정 지정** 정책 설정에서 **자동 프로 비전** 옵션을 설정 하는 방법에 따라 작업 폴더의 파트너 관계가 구성 됩니다.

클라우드 폴더 기능에 대 한 자세한 내용은 [클라우드 폴더 개요](https://go.microsoft.com/fwlink/?LinkId=330444)를 참조 하세요.

### 고객 의견 및 핫픽스 롤업

AGPM 4.0 SP2에는 AGPM 4.0 SP1(서비스 Pack1) 릴리스 이후 발견 된 문제를 해결 하는 핫픽스의 롤업이 포함 되어 있습니다. AGPM 4.0 SP2에는 Microsoft 고급 그룹 정책 관리 4.0 SP1 Hotfix1에 대 한 최신 수정 사항이 포함 되어 있습니다. 자세한 내용은 기술 자료 문서 [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)을 참조 하세요.

### 설정 및 차이점 보고서의 새로운 그룹 정책 확장

설정 및 차이점 보고서에 새 그룹 정책 확장이 추가 되었습니다.

### 설치 관리자 변경 및 지원

AGPM 4.0 SP2 설치 관리자에 대 한 변경 및 지원은 다음과 같습니다.

-   Windows 8 또는 Windows Server 2012 운영 체제 이상 운영 체제에 AGPM 4.0 SP2를 설치 하는 경우 AGPM 설치 관리자가 필수 필수 구성 요소 소프트웨어 (GPMC (그룹 정책 관리 콘솔) 및 Microsoft .NET Framework 3.5)가 설치 되어 있는지 확인 합니다. 이 필수 소프트웨어가 설치 되어 있지 않으면 AGPM 4.0 SP2 설치가 차단 됩니다.

-   AGPM 서버를 설치할 때 WCF 활성화, 비 HTTP 활성화 및 Windows 프로세스 활성화 서비스가 자동으로 활성화 됩니다.

-   WindowsVista 클라이언트 운영 체제 및 이후 버전의 운영 시스템에서는 AGPM 4.0 SP2를 설치 하기 전에 해당 운영 체제의 적절 한 버전의 원격 시스템 관리 도구를 다운로드 합니다.

-   AGPM 4.0 SP2는 이전에 지원 되는 운영 체제와의 호환성을 지원 합니다.

### 구성 매개 변수를 사용 하지 않고 AGPM 4.0 SP2로 업그레이드 하는 기능

다음 표에 표시 된 대로 agpm 4.0 이후 구성 매개 변수 (스마트 업그레이드)를 다시 입력 하 라는 메시지가 표시 되지 않고 agpm 클라이언트 또는 AGPM 서버를 AGPM 4.0 SP2로 업그레이드할 수 있습니다. 표에서와 같이 다른 버전의 AGPM으로 AGPM 4.0 SP2로 업그레이드 하는 경우에는 구성 매개 변수를 다시 입력 해야 하는 클래식 업그레이드를 사용 해야 합니다. 각 버전의 AGPM이 특정 운영 체제와 연결 되어 있기 때문에 [설치할 Agpm 버전 선택을](https://go.microsoft.com/fwlink/?LinkId=254350) 참조 하 여 agpm을 업그레이드 하기 전에 해당 운영 체제를 적절 하 게 업그레이드 해야 합니다.

**AGPM 4.0 SP2 지원 되는 업그레이드**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>업그레이드할 수 있는 AGPM 버전</strong></p></td>
<td align="left"><p><strong>2.5</strong></p></td>
<td align="left"><p><strong>3.0</strong></p></td>
<td align="left"><p><strong>4.0</strong></p></td>
<td align="left"><p><strong>4.0 SP1</strong></p></td>
<td align="left"><p><strong>4.0 SP2</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2.5</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
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
</tr>
<tr class="even">
<td align="left"><p>4.0</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
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
</tr>
</tbody>
</table>

 

## 지원되는 구성


AGPM 4.0 SP2는 다음 표의 구성을 지원 합니다. AGPM이 혼합 구성을 지원 하지만, windows Server2012 R2, windows 8 for windows Server 2012와 같은 운영 체제 줄에서 AGPM 클라이언트와 AGPM 서버를 실행 하는 것이 좋습니다.

**AGPM 4.0 SP2 지원 되는 운영 체제 및 정책 설정**

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
<td align="left"><p>Windows Server2012 R2 또는 Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 또는 Windows 8.1</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012, Windows 8.1 또는 Windows 8</p></td>
<td align="left"><p>Windows Server 2012 또는 Windows 8</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원 되지만, Windows 8.1 또는 Windows 8에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</p></td>
<td align="left"><p>지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 또는 Windows7</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP2 설치를 위한 필수 구성 요소


다음 표에서는 Windows 8.1에서 .NET Framework 3.5 또는 원격 서버 관리 도구의 GPMC가 없는 경우 AGPM 4.0 SP2 클라이언트 및 서버 설치 관리자의 동작에 대해 설명 합니다.

**AGPM 클라이언트**

**AGPM 서버**

**운영 체제**

**.NET Framework**

**원격 서버 관리 도구**

**.NET Framework**

**원격 서버 관리 도구**

**Windows 8.1**

.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.

GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다.

.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.

GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다.

**Windows Server2012 R2**

.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.

GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.

.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.

GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.

 

## MDOP 기술을 활용 하는 방법


AGPM 4.0 SP2는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .

## 관련 항목


[고급 그룹 정책 관리](index.md)

[Microsoft 고급 그룹 정책 관리 4.0 SP2 릴리스 정보](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[설치할 AGPM 버전 선택](choosing-which-version-of-agpm-to-install.md)

 

 





