---
title: 설치할 AGPM 버전 선택
description: 설치할 AGPM 버전 선택
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819098"
---
# 설치할 AGPM 버전 선택


AGPM (MicrosoftAdvanced Group Policy Management)의 각 릴리스는 특정 버전의 Windows 운영 체제를 지원 합니다. 같은 시스템의 운영 체제에서 AGPM 클라이언트와 AGPM 서버를 실행 하는 것이 좋습니다. 예를 들어 windows Server 2016, windows 8.1 for windows Server2012 R2 등이 포함 되어 있는 Windows 10

해당 도메인에 있는 최신 버전의 운영 체제에 AGPM 서버를 설치 하는 것이 좋습니다. AGPM은 Gpo (그룹 정책 개체)를 백업 및 복원 하기 위해 GPMC (그룹 정책 관리 콘솔)를 사용 합니다. 최신 버전의 GPMC는 이전 버전에서 사용할 수 없는 추가 정책 설정을 제공 하기 때문에 최신 버전의 운영 체제를 사용 하 여 더 많은 정책 설정을 관리할 수 있습니다.

모든 버전의 AGPM은 AGPM이 실행 되는 운영 체제의 버전 또는 이전 버전에서 도입 된 정책 설정만 관리할 수 있습니다. 예를 들어 Windows Server 2012에 AGPM 4.0 SP2를 설치 하는 경우 Windows Server 2012 또는 이전 버전에서 도입 된 정책 설정을 관리할 수 있지만, Windows 8.1 또는 Windows Server2012 R2에서 나중에 도입 된 정책 설정은 관리할 수 없습니다.

AGPM 서버의 GPMC 버전이 관리자가 그룹 정책을 관리 하는 데 사용 하는 컴퓨터의 버전 보다 오래 된 경우 AGPM 서버는 이전 버전의 GPMC에서 사용할 수 없는 모든 정책 설정을 저장할 수 없게 됩니다. Windows에 포함된 그룹 정책 설정의 스프레드시트에 대해서는 [Windows 및 Windows Server에 대한 그룹 정책 설정 참조](https://go.microsoft.com/fwlink/p/?LinkId=613627)를 참조하세요.

## AGPM 4.0 SP3


Windows 10을 실행 하는 컴퓨터를 사용 하 여 Gpo를 관리 하는 경우 AGPM 4.0 SP3을 사용 해야 합니다. Windows 10 운영 체제를 실행 하는 컴퓨터에는 이전 버전의 AGPM을 설치할 수 없습니다.

표 1에는 AGPM 4.0 SP3을 설치할 수 있는 운영 체제와 AGPM 4.0 SP3을 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.

**표 1: AGPM 4.0 SP3에서 지원 되는 운영 체제 및 정책 설정**

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
<td align="left"><p>Windows Server 2016 또는 Windows 10</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>KB 4015786에서 설명한 주의 사항으로 지원 됩니다. <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 또는 Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 또는 Windows 8.1</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 또는 Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 또는 Windows 8.1</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</p></td>
<td align="left"><p>지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 또는 Windows7</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP2


Windows Server2012 R2 또는 Windows 8.1을 실행 하는 컴퓨터를 사용 하 여 Gpo를 관리 하는 경우 AGPM 4.0 SP2를 사용 해야 합니다. 이러한 운영 체제를 실행 하는 컴퓨터에는 이전 버전의 AGPM을 설치할 수 없습니다.

표 1에는 AGPM 4.0 SP2를 설치할 수 있는 운영 체제와 AGPM 4.0 SP2를 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.

**표 2: AGPM 4.0 SP2에서 지원 되는 운영 체제 및 정책 설정**

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
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 또는 Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 또는 Windows 8.1</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</p></td>
<td align="left"><p>지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP1


표 2에는 AGPM 4.0 SP1을 설치할 수 있는 운영 체제와 AGPM 4.0 SP1을 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.

**표 3: AGPM 4.0 SP1에서 지원 되는 운영 체제 및 정책 설정**

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
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0


표 3에 AGPM 4.0을 설치할 수 있는 운영 체제와 AGPM 4.0을 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.

**표 4: AGPM 4.0에서 지원 되는 운영 체제 및 정책 설정**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">AGPM 서버용으로 지원 되는 운영 체제</th>
<th align="left">AGPM 클라이언트용으로 지원 되는 운영 체제</th>
<th align="left">AGPM 지원</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008R2 또는 Windows7</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>Windows Server2008 또는 Windows Vista SP1</p></td>
<td align="left"><p>지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 이전의 AGPM 버전


표 4에는 AGPM 4.0 이전의 AGPM 버전을 설치할 수 있는 운영 체제 목록이 나와 있습니다. 운영 체제가 나열 되지 않으면 해당 운영 체제에 AGPM을 설치할 수 없습니다.

**표 5: AGPM 4.0 이전의 AGPM 버전에 대해 지원 되는 운영 체제**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">설치할 수 있는 AGPM 버전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>3.0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista SP1</p></td>
<td align="left"><p>3.0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>서비스 팩이 설치 되지 않은 WindowsVista (32 비트)</p></td>
<td align="left"><p>2.5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 (32 비트)</p></td>
<td align="left"><p>2.5</p></td>
</tr>
</tbody>
</table>

 

## MDOP 기술을 활용 하는 방법


AGPM 4.0 SP2는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .

## 관련 항목


[고급 그룹 정책 관리](index.md)

 

 





