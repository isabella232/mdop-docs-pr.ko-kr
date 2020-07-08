---
title: 스트리밍 방법 결정
description: 스트리밍 방법 결정
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821668"
---
# 스트리밍 방법 결정


사용자가 게시 프로세스를 통해 컴퓨터에 배치 된 아이콘을 처음으로 두 번 클릭할 때 응용 프로그램 가상화 클라이언트는 스트리밍 원본 위치에서 가상 응용 프로그램 패키지 콘텐츠를 가져옵니다.

**참고** 
 *스트리밍은* 기본 기능 블록부터 시작 하 여 필요에 따라 추가 블록을 가져와 시퀀싱 된 응용 프로그램 패키지에서 콘텐츠를 가져오는 프로세스를 설명 하는 데 사용 되는 용어입니다.

 

스트리밍 원본 위치는 일반적으로 사용자의 컴퓨터에서 액세스할 수 있는 서버입니다. 그러나 Microsoft Endpoint Configuration Manager와 같은 일부 전자 배포 시스템은 사용자의 컴퓨터에 SFT 파일을 배포한 다음 해당 컴퓨터의 캐시에서 로컬로 가상 응용 프로그램 패키지를 스트리밍할 수 있습니다.

**참고**  서버가 아닌 컴퓨터에서 가상 패키지의 스트리밍 원본 위치를 설정할 수 있습니다. 이는 서버가 없는 작은 지점에 특히 유용 합니다.

 

다음 표에서는 시퀀싱 된 응용 프로그램을 저장 하는 데 사용할 수 있는 스트리밍 소스에 대해 설명 합니다.

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
<td align="left"><p>File</p></td>
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
<li><p>HTTPS 프로토콜을 사용 하 여 향상 된 보안을 지원 합니다.</p></li>
<li><p>인터넷에서 원격 컴퓨터로의 스트리밍을 지원 합니다.</p></li>
<li><p>방화벽의 한 포트만 열 수 있습니다.</p></li>
<li><p>확장성 높은</p></li>
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
<li><p>방화벽의 한 포트만 열 수 있습니다 (RTSPS에만 해당).</p></li>
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


[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[전자 소프트웨어 배포 기반 시나리오 개요](electronic-software-distribution-based-scenario-overview.md)

[게시 방법 결정](determine-your-publishing-method.md)

 

 





