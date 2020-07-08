---
title: AGPM 4.0 SP1의 새로운 기능
description: AGPM 4.0 SP1의 새로운 기능
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818153"
---
# AGPM 4.0 SP1의 새로운 기능


이 "새로운 기능" 콘텐츠는 Microsoft AGPM (고급 그룹 정책 관리) 4.0 SP1에 대 한 개선 및 지원 되는 구성을 설명 합니다. 이 콘텐츠 및 다른 AGPM 설명서 사이에 차이가 있는 경우이 콘텐츠는 정식으로 간주 되어야 하며이 제품에 포함 된 콘텐츠를 대체 해야 합니다.

## <a href="" id="what-s-new"></a>새로운 기능


AGPM 4.0 SP1에서는 다음과 같은 향상 된 기능을 지원 합니다.

### 새로 만들고 변경 된 클라이언트 쪽 확장

Windows 8 및 Windows Server 2012에서 새 그룹 정책을 지원 하도록 AGPM에 대해 CSEs (그룹 정책 클라이언트 쪽 확장)가 추가 또는 변경 되었습니다. 그룹 정책 관리자는 이러한 그룹 정책을 사용 하 여 두 Gpo (그룹 정책 개체) 또는 서식 파일 간에 변경 되는 Windows 8 관련 그룹 정책 설정을 관리 하 고 추적할 수 있습니다. Windows 8 관련 설정을 사용 하 여 사용자 지정 Gpo를 만들고 Gpo를 서식 파일로 구성 하 고 저장할 수도 있습니다. CSEs를 보려면 AGPM 4.0 SP1 클라이언트에서 사용할 수 있는 설정 및 차이점 보고서를 사용 합니다.

새로 만들고 변경 된 그룹 정책 클라이언트 쪽 확장명은 다음과 같습니다.

-   **중앙 액세스 정책:** 그룹 정책 관리자가 그룹 정책 서버 (예: 파일 서버)에서 중앙 액세스 정책을 지정할 수 있도록 합니다. 중앙 액세스 정책은 GPO 항목으로 지정 되 고, 리소스의 중앙 집중화 된 액세스 및 제어를 위해 정책 대상에 적용 되는 권한 부여 정책입니다. 이러한 중앙 액세스 정책은 Active Directory 내에서 그룹 정책 클라이언트 컴퓨터에 구성 해야 합니다. 그룹 정책은 해당 중앙 액세스 정책에 대 한 정보를 적용 해야 하는 컴퓨터에 배포 합니다.

-   **이름 확인 정책 변경 내용:** 그룹 정책 관리자가 DNS 클라이언트 컴퓨터에서 DNS 보안 및 DirectAccess에 대 한 설정을 구성할 수 있도록 합니다. 일반 DNS 서버 설정 및 인코딩 설정 구성을 위한 새 탭이 추가 되었습니다.

-   **그룹 정책 기본 설정 변경 내용:** Windows 8에 추가 된 Internet Explorer 10 설정의 구성 및 관리에 대 한 지원을 추가 합니다.

-   **원격 응용 프로그램 및 데스크톱 연결:** 그룹 정책 관리자가 원격 응용 프로그램 및 데스크톱 연결에 사용 되는 기본 연결 URL을 지정할 수 있도록 합니다.

-   **Windows To Go 시작 옵션:** Windows To Go 작업 영역이 포함 된 USB 장치가 연결 되어 있는 경우 그룹 정책 관리자가 Windows to Go로 부팅 되는지 여부를 구성할 수 있습니다.

-   **Windows To Go 최대 절전 모드 옵션:** Windows To Go 작업 영역에서 컴퓨터를 시작할 때 컴퓨터에서 최대 절전 모드 절전 상태 (S4)를 사용할 수 있는지 여부를 그룹 정책 관리자가 구성할 수 있도록 합니다.

### 고객 의견 및 핫픽스 롤업

AGPM 4.0 SP1에는 AGPM 4.0 릴리스 이후 발견 된 문제 해결에 대 한 수정 롤업이 포함 되어 있습니다. AGPM 4.0 SP1에는 Microsoft 고급 그룹 정책 관리 4.0 핫픽스 1에 대 한 최신 수정 사항이 포함 되어 있습니다.

### 설정 및 차이점 보고서에 새 그룹 정책 확장이 표시 됩니다.

설정 및 차이점 보고서에 새 그룹 정책 확장이 추가 되었습니다.

### 설치 관리자 변경 및 지원

AGPM 4.0 SP1 설치 관리자에 대 한 변경 및 지원은 다음과 같습니다.

-   Windows 8 또는 Windows Server 2012에 AGPM 4.0 SP1을 설치 하는 경우 AGPM 설치 관리자가 필수 필수 구성 요소 소프트웨어 (그룹 정책 관리 콘솔 및 .NET 3.5 프레임 워크)가 설치 되어 있는지 확인 합니다. 이러한 전제 조건이 설치 되어 있지 않으면 AGPM 4.0 SP1 설치가 차단 됩니다.

-   AGPM 4.0 SP1을 설치 하면 WCF 정품 인증, 비 HTTP 정품 인증 및 Windows 프로세스 활성화 서비스가 자동으로 활성화 됩니다.

-   Windows Vista, Windows 7 및 Windows 8 클라이언트 운영 체제에서는 AGPM 4.0 SP1을 설치 하기 전에 운영 체제에 적합 한 버전의 원격 시스템 관리 도구 키트를 다운로드 합니다.

-   이전에 지원 되는 운영 체제와의 이전 버전과의 호환성이 지원 됩니다.

### 구성 매개 변수를 다시 입력 하지 않고 AGPM 4.0 SP1로 업그레이드 하거나 업데이트 하는 기능

다음 표에 표시 된 대로 구성 매개 변수 ("Smart Upgrade")를 다시 입력 하지 않고 agpm 4.0에서 agpm 4.0 SP1로, agpm 클라이언트 또는 서버를 확인할 수 있습니다. 표에서와 같이 다른 버전의 AGPM으로 AGPM 4.0 SP1로 업그레이드 하는 경우에는 구성 매개 변수를 다시 입력 해야 하는 "클래식 업그레이드"를 사용 해야 합니다. 각 버전의 AGPM이 특정 운영 체제와 연결 되어 있으므로 [설치할 Agpm 버전 선택](https://go.microsoft.com/fwlink/?LinkId=254350)을 참조 하 고 업그레이드를 수행 하기 전에 운영 체제를 적절 하 게 업그레이드 해야 합니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>업그레이드할 수 있는 AGPM 버전</strong></p></td>
<td align="left"><p><strong>2.5</strong></p></td>
<td align="left"><p><strong>3.0</strong></p></td>
<td align="left"><p><strong>4.0</strong></p></td>
<td align="left"><p><strong>4.0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2.5</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>설치 차단 됨</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3.0</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>클래식 업그레이드</p></td>
<td align="left"><p>설치 차단 됨</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.0</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>스마트 업그레이드</p></td>
</tr>
</tbody>
</table>

 

## 지원되는 구성


AGPM은 다음 표의 구성을 지원 합니다. AGPM이 혼합 구성을 지원 하지만, windows Server 2012, windows Server 2008 R2와 같이 windows 8과 같은 운영 체제 제품군에서 AGPM 클라이언트와 서버를 실행 하는 것이 좋습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM 4.0 SP1 서버용으로 지원 되는 구성</strong></p></td>
<td align="left"><p><strong>AGPM 4.0 SP1 클라이언트에 지원 되는 구성</strong></p></td>
<td align="left"><p><strong>AGPM 4.0 SP1 지원</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 또는 Windows Server 2012</p></td>
<td align="left"><p>Windows 8 또는 Windows Server 2012</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 또는 Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 또는 Windows 7</p></td>
<td align="left"><p>지원 되지만 Windows 8에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 또는 Windows 7 또는 windows 8 또는 Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 되지만, Windows Server 2008 R2 또는 Windows 7 또는 Windows 8에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 또는 Windows 7 또는 windows 8 또는 Windows Server 2012</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 되지만, Windows Server 2008 R2 또는 Windows 7 또는 Windows 8에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP1 설치를 위한 필수 구성 요소


다음 표에는 Windows 8 용 AGPM 4.0 SP1 클라이언트 및 서버 설치 관리자에서 .NET 3.5 또는 RSAT (원격 서버 관리 도구)의 그룹 정책 관리 콘솔이 없는 경우의 동작에 대 한 설명이 나와 있습니다.

**AGPM 클라이언트 4.0 SP1**

**AGPM 서버 4.0 SP1**

**운영 체제**

**.NET**

**RSAT**

**.NET**

**RSAT**

**Windows8**

.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.

시스템에 GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다.

.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.

시스템에 GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다.

**Windows Server 2012**

.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.

GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.

.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.

GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.

 

## 관련 항목


[고급 그룹 정책 관리](index.md)

[Microsoft 고급 그룹 정책 관리 4.0 SP1 릴리스 정보](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





