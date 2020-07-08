---
title: Application Virtualization 시스템 구성 요소 개요
description: Application Virtualization 시스템 구성 요소 개요
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816053"
---
# Application Virtualization 시스템 구성 요소 개요


다음 표에서는 Microsoft Application Virtualization 관리 시스템의 기본 구성 요소에 대해 설명 합니다. 이러한 시스템 구성 요소를 배포 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 서버 기반 시나리오](application-virtualization-server-based-scenario.md)를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">구성 요소</th>
<th align="left">함수</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization 관리 서버</p></td>
<td align="left"><p>패키지 콘텐츠 스트리밍을 수행 하 고 바로 가기 및 파일 형식 연결을 응용 프로그램 가상화 클라이언트에 게시 하는 역할을 하는 구성 요소입니다.</p></td>
<td align="left"><p>응용 프로그램 가상화 관리 서버는 활성 업그레이드, 라이선스 관리 및 보고에 사용할 수 있는 데이터베이스를 지원 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>콘텐츠 </strong> 폴더</p></td>
<td align="left"><p>스트리밍을 위한 응용 프로그램 가상화 패키지의 위치입니다.</p></td>
<td align="left"><p>이 폴더는 응용 프로그램 가상화 관리 서버의 공유 위치에 있을 수 있습니다. 폴더는 SAN (저장 영역 네트워크)에 있을 수도 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization 관리 콘솔</p></td>
<td align="left"><p>Microsoft Application Virtualization 서버 관리용 MMC 3.0 스냅인 관리 유틸리티.</p></td>
<td align="left"><p>이 구성 요소는 Microsoft Application Virtualization server에 설치 하거나 MMC 3.0 및이 있는 별도의 워크스테이션에 배치할 수 있습니다. NET 2.0이 설치 되어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization 관리 웹 서비스</p></td>
<td align="left"><p>응용 프로그램 가상화 데이터 저장소에 대 한 읽기/쓰기 요청을 통신 하는 데 책임이 있는 구성 요소입니다.</p></td>
<td align="left"><p>이 구성 요소는 Microsoft Application Virtualization Server 또는 IIS가 설치 된 별도의 컴퓨터에 설치할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Data Store</p></td>
<td align="left"><p>SQL 데이터베이스에 저장 되 고 응용 프로그램 가상화 인프라와 관련 된 모든 정보를 저장 하는 역할을 하는 구성 요소입니다.</p></td>
<td align="left"><p>이 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 지정, 응용 프로그램 가상화 환경 관리를 담당 하는 그룹이 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization 스트리밍 서버</p></td>
<td align="left"><p>응용 프로그램 가상화 관리 서버로 다시 연결 하는 WAN으로 간주 되는 지점에서 클라이언트에 스트리밍하는 응용 프로그램 가상화 패키지 호스팅을 담당 하는 구성 요소입니다.</p></td>
<td align="left"><p>이 서버는 스트리밍 기능만 포함 하며 응용 프로그램 가상화 관리 콘솔 및 응용 프로그램 가상화 관리 웹 서비스를 제공 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>가상 응용 프로그램 패키지를 만들기 위한 응용 프로그램 설치를 모니터링 하 고 캡처하는 데 사용 되는 구성 요소입니다.</p></td>
<td align="left"><p>출력은 응용 프로그램 아이콘, 패키지 정의 정보를 포함 하는 OSD 파일, 패키지 매니페스트 파일, 응용 프로그램 프로그램의 콘텐츠 파일이 포함 된 SFT 파일 등으로 구성 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization 클라이언트</p></td>
<td align="left"><p>응용 프로그램 가상화 데스크톱 클라이언트에 설치 된 구성 요소 또는 원격 데스크톱 서비스에 대 한 Application Virtualization 클라이언트 (이전의 터미널 서비스) 및 가상화 된 응용 프로그램에 대 한 가상 환경을 제공 합니다.</p></td>
<td align="left"><p>Microsoft 응용 프로그램 가상화 클라이언트는 패키지 스트리밍을 캐시로, 게시 새로 고침, 전송, 응용 프로그램 가상화 서버와의 모든 조작을 관리 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





