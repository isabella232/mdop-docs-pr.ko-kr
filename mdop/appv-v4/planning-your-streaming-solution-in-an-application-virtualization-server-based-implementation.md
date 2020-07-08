---
title: Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획
description: Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815868"
---
# Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획


Application virtualization 스트리밍 서버를 응용 프로그램 가상화 관리 서버 기반 구현과 함께 사용 하려는 경우에는 이미 사용 중인 모든 인프라를 활용 하 여 여러 대안 중에서 선택할 수 있습니다. 예를 들어 필드에 이미 서버가 있는 경우 해당 서버에 Application Virtualization \\CONTENT share를 배치 하 고 해당 콘텐츠 공유를 응용 프로그램 콘텐츠 원본으로 사용 하도록 구성할 수 있습니다. 예를 들어 단일 office만 있는 경우와 같이 응용 프로그램 가상화 관리 서버만 사용 하도록 선택한 경우 클라이언트는 해당 서버의 콘텐츠를 스트리밍할 수 있습니다.

지원 되는 옵션에는 파일 서버, IIS 서버 또는 응용 프로그램 가상화 스트리밍 서버를 사용 하는 것이 포함 됩니다. 기존 파일 서버나 IIS 서버에 응용 프로그램 가상화 스트리밍 서버를 설치할 수도 있습니다. 이러한 여러 옵션의 특성은 다음 표에 요약 되어 있습니다.

**참고**  활성 업그레이드 기능을 사용 하면 현재 응용 프로그램을 실행 중인 사용자에 게 영향을 주지 않고 App-v 관리 서버 또는 스트리밍 서버에 새 버전의 응용 프로그램을 추가할 수 있습니다. 앱-V 클라이언트는 다음에 사용자가 응용 프로그램을 시작할 때 App-v 관리 서버 또는 스트리밍 서버에서 최신 버전의 응용 프로그램을 자동으로 받게 됩니다. 이 기능에는 RTSP (S) 프로토콜을 사용 해야 합니다.

 

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">서버 유형</th>
<th align="left">프로토콜</th>
<th align="left">장점</th>
<th align="left">단점</th>
<th align="left">링크</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>파일 서버</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><ul>
<li><p>\CONTENT share를 사용 하 여 기존 파일 서버를 구성 하는 간단한 저렴 한 솔루션</p></li>
</ul></td>
<td align="left"><ul>
<li><p>활성 업그레이드 없음</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">파일 서버를 구성하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>IIS 서버</p></td>
<td align="left"><p>HTTP/HTTPS</p></td>
<td align="left"><ul>
<li><p>HTTPS 프로토콜을 사용 하 여 향상 된 보안 지원</p></li>
<li><p>인터넷에서 원격 컴퓨터로의 스트리밍을 지원 합니다.</p></li>
<li><p>방화벽의 한 포트만 열 수 있습니다.</p></li>
<li><p>가용성</p></li>
<li><p>친숙 한 프로토콜</p></li>
</ul></td>
<td align="left"><ul>
<li><p>IIS를 관리 해야 합니다.</p></li>
<li><p>활성 업그레이드 없음</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">IIS용 서버를 구성하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Application Virtualization 스트리밍 서버</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>활성 업그레이드</p></li>
<li><p>RTSPS 프로토콜을 사용 하 여 향상 된 보안 지원</p></li>
<li><p>방화벽의 한 포트만 열 수 있습니다.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>이중 인프라</p></li>
<li><p>서버 관리 요구 사항</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Application Virtualization Streaming Server 구성 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Application Virtualization 관리 서버</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>활성 업그레이드</p></li>
<li><p>RTSPS 프로토콜을 사용 하 여 향상 된 보안 지원</p></li>
<li><p>방화벽의 한 포트만 열 수 있습니다.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>이중 인프라</p></li>
<li><p>서버 관리 요구 사항</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Application Virtualization Management Server 구성 방법</a></p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[Application Virtualization 시스템 구성 요소 개요](overview-of-the-application-virtualization-system-components.md)

[Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





