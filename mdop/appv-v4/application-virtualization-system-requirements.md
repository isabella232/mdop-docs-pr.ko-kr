---
title: Application Virtualization 시스템 요구 사항
description: Application Virtualization 시스템 요구 사항
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819518"
---
# Application Virtualization 시스템 요구 사항


이 항목에서는 Microsoft App-v (Application Virtualization) 관리 서버 및 스트리밍 서버의 최소 하드웨어 및 소프트웨어 요구 사항에 대해 설명 합니다.

## 응용 프로그램 가상화 관리 및 스트리밍 서버


다음 목록에는 App-v 관리 서버 및 App-v 스트리밍 서버용으로 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항이 포함 되어 있습니다.

### 하드웨어 요구 사항

-   프로세서-인텔 펜티엄 III, 1Ghz

-   RAM-512 MB

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)

### 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>스탠더드 버전</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ 앱-V 4.5 SP1 및 SP2에만 적용 됩니다.

## 데이터 저장소


다음 목록에는 데이터 저장소를 별도의 서버에 설치할 때 사용 하는 컴퓨터에 대해 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항이 포함 되어 있습니다. 데이터 저장소는 응용 프로그램 가상화 관리 서버에만 필요 합니다.

### 하드웨어 요구 사항

-   프로세서-Intel 펜티엄 III, 850 MHz

-   RAM-512 MB

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간

### 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>스탠더드 버전</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ 앱-V 4.5 SP1 및 SP2에만 적용 됩니다.

-   데이터베이스-Microsoft SQL Server2000 SP3a 또는 SP4, SQL Server2005 SP1, SP2 또는 SP3 또는 SQL Server2008 (서비스 팩 또는 SP1 또는 SQL Server2008 R2 (32 비트 또는 64 비트)

-   Microsoft Data Access 구성 요소-MDAC 2.7

-   도메인 컨트롤러-중앙 인증 기관으로 서 Active Directory 도메인 서비스 또는 Windows NT 4.0 기반 주 도메인 컨트롤러 (PDC)

## 관리 웹 서비스


다음 목록에는 응용 프로그램 가상화 관리 웹 서비스를 별도의 컴퓨터에 설치할 때 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항이 포함 되어 있습니다.

### 하드웨어 요구 사항

-   프로세서-Intel 펜티엄 III, 800 MHz

-   RAM (256 MB)

-   디스크 공간 – 50mb 사용 가능한 하드 디스크 공간

### 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>스탠더드 버전</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ 앱-V 4.5 SP1 및 SP2에만 적용 됩니다.

-   Iis (인터넷 정보 서비스)-Microsoft ASP.NET, IIS 7을 사용 하 여 구성 된 IIS (인터넷 정보 서비스) 6.0

-   Microsoft .NET Framework 2.0

## 관리 콘솔


다음 목록에는 응용 프로그램 가상화 관리 콘솔을 별도의 컴퓨터에 설치할 때 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항이 포함 되어 있습니다.

### 하드웨어 요구 사항

-   프로세서-Intel 펜티엄 III, 450 MHz

-   RAM (256 MB)

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간

### 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 또는 SP3</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>비즈니스, 엔터프라이즈 또는 Ultimate Edition</p></td>
<td align="left"><p>서비스 팩, SP1 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise 또는 Ultimate Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ 앱-V 4.5 SP1 및 SP2에만 적용 됩니다.

-   Microsoft 관리 콘솔-MMC 3.0 이상

-   Microsoft .NET Framework 2.0 SP2 (최소)

    **중요**  App-v 관리 콘솔을 실행 하는 컴퓨터에 App-v 핫픽스 KB980850 또는 후속 App-v 핫픽스를 설치 해야 하는 경우에는 최소 요구 사항이 .NET Framework 2.0 SP2입니다.

     

## 관련 항목


[Application Virtualization Client 하드웨어 및 소프트웨어 요구 사항](application-virtualization-client-hardware-and-software-requirements.md)

[Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항](application-virtualization-sequencer-hardware-and-software-requirements.md)

[서버 기반 배포용 서버를 구성하는 방법](how-to-configure-servers-for-server-based-deployment.md)

[서버 및 시스템 구성 요소 설치 방법](how-to-install-the-servers-and-system-components.md)

[서버 및 시스템 구성 요소를 업그레이드하는 방법](how-to-upgrade-the-servers-and-system-components.md)

 

 





