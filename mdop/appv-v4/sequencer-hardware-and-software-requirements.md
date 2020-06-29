---
title: Sequencer 하드웨어 및 소프트웨어 요구 사항
description: Sequencer 하드웨어 및 소프트웨어 요구 사항
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815533"
---
# Sequencer 하드웨어 및 소프트웨어 요구 사항


이 항목에서는 Microsoft App-v (Application Virtualization) Sequencer를 실행 하는 컴퓨터에 대해 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항에 대해 설명 합니다.

시퀀서를 설치 하 고 각 응용 프로그램의 순서를 설정한 후에는 시퀀싱 된 컴퓨터에 클린 운영 체제 이미지를 복원 해야 합니다. 다음 방법 중 하나를 사용 하 여 Sequencer를 실행 하는 컴퓨터를 복원할 수 있습니다.

-   하드 드라이브를 다시 포맷 하 고 운영 체제를 다시 설치 합니다.

-   다른 디스크 이미징 소프트웨어를 사용 하 여 Sequencer 이미지를 실행 하는 컴퓨터의 하드 드라이브를 복원 합니다.

다음 목록에는 App-v 시퀀서를 실행 하기 위한 권장 하드웨어 요구 사항이 요약 되어 있습니다.

### <a href="" id="hardware-requirements-"></a>하드웨어 요구 사항

-   프로세서-Intel 펜티엄 III, 1Ghz (32 비트 또는 64 비트). 시퀀싱 프로세스는 단일 스레드 프로세스 이며 이중 프로세서를 사용 하지 않습니다.

-   메모리-1GB 이상, 2gb 권장.

-   하드 디스크-최소 15gb의 하드 디스크 공간을 사용 하는 40gb (하드 디스크 공간) 시퀀싱 하는 응용 프로그램에 필요한 하드 디스크 공간에는 세 배 이상 있는 것이 좋습니다.

    **참고**  시퀀싱에는 디스크 사용량이 많이 필요 합니다. 빠른 디스크 속도를 통해 시퀀싱 시간을 줄일 수 있습니다.

     

### 소프트웨어 요구 사항

다음 목록에서는 Sequencer 실행을 위해 지원 되는 운영 체제에 대해 간략하게 설명 합니다.

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
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP2 또는 SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>비즈니스, 엔터프라이즈 또는 궁극적인</p></td>
<td align="left"><p>서비스 팩, SP1 또는 SP2 없음</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise 또는 Ultimate</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ 4.5 (SP1 또는 SP2 포함), app-v 4.6에 대해서만 지원 됨

**참고**  App-v (Application Virtualization) 4.6 Sequencer는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.

 

시퀀서를 실행 하는 컴퓨터는 대상 컴퓨터에 설치 된 것과 동일한 응용 프로그램을 구성 해야 합니다.

### 원격 데스크톱 서비스에 대 한 소프트웨어 요구 사항

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
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**참고**  원격 데스크톱 서비스의 App-v (Application Virtualization) 4.6는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.

 

## 관련 항목


[Application Virtualization Sequencer 개요](application-virtualization-sequencer-overview.md)

 

 





