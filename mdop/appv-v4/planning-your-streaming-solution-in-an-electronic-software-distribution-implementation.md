---
title: 전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획
description: 전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815858"
---
# 전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획


시스템을 사용 하 여 응용 프로그램 콘텐츠를 최종 사용자의 컴퓨터에서 사용할 수 있도록 하는 경우에는 기존에 있는 모든 인프라를 활용 하 여 여러 가지 대안 중에서 선택할 수 있습니다. 예를 들어, ESD 시스템에 서버에 대 한 소프트웨어 배포 공유가 있는 경우 해당 서버에 응용 프로그램 가상화 \\CONTENT 공유를 배치 하 고 해당 콘텐츠 공유를 응용 프로그램 콘텐츠 원본으로 사용 하도록 구성할 수 있습니다. 지원 되는 옵션에는 파일 서버나 IIS 서버를 사용 하는 것이 포함 됩니다. 기존 파일 서버나 IIS 서버에 응용 프로그램 가상화 스트리밍 서버를 설치할 수도 있습니다.

Application Virtualization 스트리밍 서버는 응용 프로그램 가상화의 활성 업그레이드 기능에 대 한 지원을 제공 합니다. 활성 업그레이드 기능을 사용 하면 현재 응용 프로그램을 실행 중인 사용자에 게 영향을 주지 않고 App-v 관리 서버 또는 스트리밍 서버에 새 버전의 응용 프로그램을 추가할 수 있습니다. 앱-V 클라이언트는 다음에 사용자가 응용 프로그램을 시작할 때 App-v 관리 서버 또는 스트리밍 서버에서 최신 버전의 응용 프로그램을 자동으로 받게 됩니다. 이 기능에는 RTSP (S) 프로토콜을 사용 해야 합니다. Application Virtualization 스트리밍 서버를 사용 하지 않도록 선택한 경우에는 ESD 시스템을 사용 하 여 응용 프로그램 패키지 업그레이드를 명시적으로 관리 해야 합니다.

**참고**  응용 프로그램에 대 한 액세스는 Active Directory 도메인 서비스의 보안 그룹을 통해 제어 되므로 각 가상 응용 프로그램에 대 한 보안 그룹을 설정 하 고 각 그룹에 추가 되는 사용자를 관리 하는 프로세스를 계획 해야 합니다. 응용 프로그램 가상화 시스템 관리자는 Active Directory 그룹 구성원을 기반으로 하는 패키지에 대 한 액세스를 제어 하는 콘텐츠 공유 아래의 응용 프로그램 디렉터리에 Acl을 적용 하 여 이러한 Active Directory 그룹을 사용 하도록 각 스트리밍 서버를 구성 합니다.

 

사용할 수 있는 스트리밍 옵션의 특성은 다음 표에 요약 되어 있습니다.

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Application Virtualization Management Server 구성 방법</a></p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[ESD 기반 배포용 서버를 구성하는 방법](how-to-configure-servers-for-esd-based-deployment.md)

[보안 및 보호 개요](security-and-protection-overview.md)

[전자 소프트웨어 배포를 사용하여 가상 응용 프로그램 게시](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





