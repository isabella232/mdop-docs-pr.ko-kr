---
title: Application Virtualization 개요
description: Application Virtualization 개요
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816063"
---
# Application Virtualization 개요


Microsoft App-v (Application Virtualization)를 사용 하면 응용 프로그램을 해당 컴퓨터에 직접 설치 하지 않고도 응용 프로그램을 최종 사용자 컴퓨터에서 사용할 수 있습니다. 이 작업은 *응용 프로그램 시퀀싱*이라고 하는 프로세스를 통해 가능 하며, 이렇게 하면 클라이언트 컴퓨터의 자체 자체 포함 가상 환경에서 각 응용 프로그램을 실행할 수 있습니다. 시퀀싱 된 응용 프로그램은 서로 격리 됩니다. 이렇게 하면 응용 프로그램 충돌이 해결 되지만 응용 프로그램이 클라이언트 컴퓨터와 계속 상호 작용할 수 있습니다.

App-v 클라이언트는 최종 사용자가 컴퓨터에 게시 된 후 응용 프로그램을 조작할 수 있도록 하는 기능입니다. 클라이언트는 각 컴퓨터에서 가상화 된 응용 프로그램이 실행 되는 가상 환경을 관리 합니다. 컴퓨터에 클라이언트를 설치한 후에는 최종 사용자가 가상 응용 프로그램을 실행할 수 있도록 *게시*라는 프로세스를 통해 컴퓨터에서 응용 프로그램을 사용할 수 있어야 합니다. 게시 프로세스는 가상 응용 프로그램 아이콘 및 바로 가기를 컴퓨터 (일반적으로 Windows 바탕 화면 또는 **시작** 메뉴)에 복사 하 고 패키지 정의 및 파일 형식 연결 정보를 컴퓨터에 복사 합니다. 게시는 또한 최종 사용자의 컴퓨터에서 응용 프로그램 패키지 콘텐츠를 사용할 수 있도록 합니다.

가상 응용 프로그램 패키지 콘텐츠는 요청에 따라 클라이언트로 스트림 하 고 로컬로 캐시할 수 있도록 하나 이상의 응용 프로그램 가상화 서버에 복사 될 수 있습니다. 파일 서버와 웹 서버는 스트리밍 서버로도 사용할 수 있으며, 예를 들어 Microsoft 끝점 구성 관리자와 같은 전자 소프트웨어 배포 시스템을 사용 하는 경우와 같이 콘텐츠를 최종 사용자의 컴퓨터에 직접 복사할 수 있습니다. 다중 서버 구현에서 모든 스트리밍 서버에서 패키지 콘텐츠를 유지 관리 하 고 최신 상태로 유지 하려면 종합적인 패키지 관리 솔루션이 필요 합니다. 조직의 규모에 따라 전세계의 모든 사용자에 게 제공 되는 가상 응용 프로그램이 여러 개 필요할 수 있습니다. 패키지를 관리 하 여 모든 사용자가 적절 한 응용 프로그램을 사용할 수 있도록 하는 것이 중요 한 이유는 어디서 든 액세스 권한이 필요 합니다.

## Microsoft Application Virtualization 시스템 기능


다음 표에서는 Microsoft Application Virtualization 관리 시스템의 기본 기능에 대해 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">기능</th>
<th align="left">함수</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization 관리 서버</p></td>
<td align="left"><p>패키지 콘텐츠 스트리밍을 수행 하 고 바로 가기 및 파일 형식 연결을 응용 프로그램 가상화 클라이언트에 게시 하는 책임을 집니다.</p></td>
<td align="left"><p>응용 프로그램 가상화 관리 서버는 활성 업그레이드, 라이선스 관리 및 보고에 사용할 수 있는 데이터베이스를 지원 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>콘텐츠 </strong> 폴더</p></td>
<td align="left"><p>스트리밍을 위한 응용 프로그램 가상화 패키지의 위치를 나타냅니다.</p></td>
<td align="left"><p>이 폴더는 응용 프로그램 가상화 관리 서버의 공유 위치에 있을 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization 관리 콘솔</p></td>
<td align="left"><p>이 콘솔은 Microsoft Application Virtualization 서버 관리에 사용 되는 MMC 3.0 스냅인 관리 도구입니다.</p></td>
<td align="left"><p>이 도구는 Microsoft Application Virtualization server에 설치 하거나 MMC (Microsoft Management Console) 3.0과 Microsoft가 있는 별도의 워크스테이션에 배치할 수 있습니다. NETFramework 2.0이 설치 되어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization 관리 웹 서비스</p></td>
<td align="left"><p>Application Virtualization data store에 대 한 읽기 및 쓰기 요청을 통신 하는 책임을 집니다.</p></td>
<td align="left"><p>Microsoft 응용 프로그램 가상화 관리 서버 또는 Microsoft IIS (인터넷 정보 서비스)가 설치 된 별도의 컴퓨터에 관리 웹 서비스를 설치할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Data Store</p></td>
<td align="left"><p>응용 프로그램 가상화 인프라와 관련 된 모든 정보를 저장 해야 하는 App-v SQL Server 데이터베이스입니다.</p></td>
<td align="left"><p>이 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 지정, 응용 프로그램 가상화 환경 관리를 담당 하는 그룹이 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization 스트리밍 서버</p></td>
<td align="left"><p>응용 프로그램 가상화 관리 서버로 다시 연결 되는 WAN (광역 네트워크) 연결로 간주 되는 지점에서 클라이언트에 스트리밍하는 데 사용할 수 있는 응용 프로그램 가상화 패키지 호스팅을 담당 합니다.</p></td>
<td align="left"><p>이 서버는 스트리밍 기능만 포함 하며 응용 프로그램 가상화 관리 콘솔 및 응용 프로그램 가상화 관리 웹 서비스를 제공 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>Sequencer는 가상 응용 프로그램 패키지를 만들기 위한 응용 프로그램 설치를 모니터링 하 고 캡처하는 데 사용 됩니다.</p></td>
<td align="left"><p>출력은 응용 프로그램 아이콘, 패키지 정의 정보, 패키지 매니페스트 파일, 응용 프로그램 프로그램의 콘텐츠 파일을 포함 하는 sft 파일 등이 포함 된 .osd 파일로 구성 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Application Virtualization 클라이언트</p></td>
<td align="left"><p>Application Virtualization 데스크톱 클라이언트 및 원격 데스크톱 서비스용 응용 프로그램 가상화 클라이언트는 가상화 된 응용 프로그램의 가상 환경을 제공 하 고 관리 합니다.</p></td>
<td align="left"><p>Microsoft 응용 프로그램 가상화 클라이언트는 패키지 스트리밍을 캐시로, 게시 새로 고침, 전송, 응용 프로그램 가상화 서버와의 모든 조작을 관리 합니다.</p></td>
</tr>
</tbody>
</table>

 

 

 





