---
title: 웹 서비스 요청 성능 카운터 모니터링
description: 웹 서비스 요청 성능 카운터 모니터링
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823878"
---
# 웹 서비스 요청 성능 카운터 모니터링


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음 웹 서비스로 전송 되는 요청의 성능을 기록 하는 성능 카운터를 제공 합니다.

-   **StatusReportingService** – 준수 상태에 대 한 요청을 수신 하는 서비스

-   **CoreService** – 키 복구 시도에 대 한 요청을 수신 하는 서비스

## MBAM이 제공 하는 성능 카운터


MBAM은 해당 StatusReportingService 및 CoreService 웹 서비스에서 구현 하는 각 공용 메서드에 대해 다음과 같은 성능 카운터를 제공 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">성능 카운터 형식</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>총 요청 수</p></td>
<td align="left"><p>서버를 시작 하거나 다시 시작할 때 0부터 시작 하는 증분 수를 제공 합니다.</p>
<p>시스템 활동의 전체 보기를 제공 합니다. 서버의 상태를 확인 하 고 지정 된 기간 동안 카운터가 지속적으로 증가 하는지 확인 하기 위해 자동 도구를 통해 모니터링할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>초당 요청 수</p></td>
<td align="left"><p>Mbam 서버의 현재 처리량을 MBAM 클라이언트 베이스를 지원 하는 것으로 나타냅니다.</p>
<p>사이트 관리자가 다음을 할 수 있습니다.</p>
<ul>
<li><p>MBAM 클라이언트 수 및 보고 빈도를 기준으로 초당 평균 요청 수를 계산 합니다.</p></li>
<li><p>초당 계산 된 평균 요청 수와 광범위 하 게 연관 되는 초당 요청 수를 확인 합니다. 상당한 분산으로 인해 MBAM 클라이언트가 클라이언트 기반 백분율에 설치 되지 않았거나 MBAM 그룹 정책 개체가 성공적으로 배포 되지 않았음을 나타낼 수 있습니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>요청 기간</p></td>
<td align="left"><p>요청 기간 (밀리초)을 기록 합니다.</p>
<p>이 카운터는 각 요청의 기간에 따라 업데이트 되지만, Windows 성능 모니터는 정기적으로 (일반적으로 매 초)에만 해당 값의 가변성을 확인할 수 있습니다. 이 때문에 성능 모니터에 표시 되는 평균값을 사용 하는 것이 좋습니다.</p></td>
</tr>
</tbody>
</table>

 

## 성능 카운터 결과 및 권장 사항


여분 용량으로 새 MBAM 클라이언트를 MBAM 서버에 추가 하는 경우 초당 요청 수가 증가 하는 것을 알 수 있습니다. 이러한 증가는 새 클라이언트 컴퓨터 수에 비례하여 표시 됩니다. 평균 요청 기간은 상대적으로 정적으로 유지 됩니다. 서버가 최대 용량에 도달 함에 따라 초당 요청 수는 수준 아웃을 시작 하 고, 평균 요청 기간이 길어질 때까지 시작 됩니다.

MBAM 서버가 클라이언트 기반을 지원할 수 있는지 걱정 하는 경우 다양 한 클라이언트 컴퓨터 컬렉션에서 MBAM을 배포 하는 것이 좋습니다. 클라이언트 컴퓨터의 각 컬렉션에 MBAM을 배포할 때 성능 카운터의 스냅숏을 만들어 각 새 클라이언트 컬렉션에 배포 하는 상대적인 영향을 확인 하는 것이 좋습니다. 초당 요청 수가 수준 끄기를 시작 하 고 평균 요청 기간이 늘어나면 다음 중 하나를 수행 하 여 MBAM 서버 인프라를 향상 하는 것이 좋습니다.

-   MBAM 데이터베이스를 전용 Microsoft SQL Server 또는 SQL Server 클러스터로 이동

-   여러 IIS (인터넷 정보 서비스) 웹 서버에 걸친 MBAM 분산

-   보다 강력한 서버 하드웨어에 MBAM 배포

## 성능 카운터 보기


MBAM 성능 카운터를 보는 데 권장 되는 도구는 Windows와 함께 제공 되는 Windows 성능 모니터입니다. Windows PowerShell을 사용 하는 경우 Windows PowerShell **enable-webapplication** cmdlet에서 자동으로 등록 되므로 표시 하기 전에 카운터를 사용할 필요가 없습니다.

성능 카운터를 보는 방법에 대 한 자세한 지침은 [MBAM 성능 카운터를 보는 방법을](https://go.microsoft.com/fwlink/?LinkId=393457)참조 하세요.



## 관련 항목


[MBAM 2.5 유지 관리](maintaining-mbam-25.md)

 

 


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.


