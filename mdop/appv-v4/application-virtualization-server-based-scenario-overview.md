---
title: Application Virtualization Server 기반 시나리오 개요
description: Application Virtualization Server 기반 시나리오 개요
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822093"
---
# Application Virtualization Server 기반 시나리오 개요


Microsoft 응용 프로그램 가상화 환경에 대해 서버 기반 배포 시나리오를 사용 하려는 경우에는 *응용 프로그램 가상화 관리 서버* 와 *응용 프로그램 가상화 스트리밍 서버의*차이점을 이해 하는 것이 중요 합니다. 이 항목에서는 이러한 차이점에 대해 설명 하 고 배포를 진행할 때 고려해 야 하는 패키지 배달 방법, 전송 프로토콜 및 외부 구성 요소에 대 한 정보를 제공 합니다.

## Application Virtualization 관리 서버


Application Virtualization Management Server는 게시 함수와 스트리밍 함수를 모두 수행 합니다. 서버는 승인 된 사용자를 위해 App-v 클라이언트에 응용 프로그램 아이콘, 바로 가기 및 파일 형식 연결을 게시 합니다. 응용 프로그램에 대 한 사용자 요청이 수신 되 면 서버는 RTSP 또는 RTSPS 프로토콜을 사용 하는 승인 된 사용자에 게 요청 시 데이터를 스트리밍합니다. 이 서버를 사용 하는 대부분의 구성에서 하나 이상의 관리 서버가 구성 및 패키지 정보에 대 한 공통 데이터 저장소를 공유 합니다.

응용 프로그램 가상화 관리 서버는 Active Directory 그룹을 사용 하 여 사용자 인증을 관리 합니다. Active Directory 도메인 서비스 외에도 이러한 서버에는 데이터베이스 및 데이터 저장소를 관리 하는 SQL Server가 설치 되어 있습니다. 관리 서버는 Microsoft Management Console의 스냅인 인 Application Virtualization 관리 콘솔을 통해 제어 됩니다.

응용 프로그램 가상화 관리 서버는 응용 프로그램을 필요할 때 최종 사용자에 게 스트리밍할 수 있기 때문에, 이러한 서버는 안정적인 고대역폭 Lan이 있는 시스템 구성에 이상적입니다.

## Application Virtualization 스트리밍 서버


Application Virtualization 스트리밍 서버는 관리 서버에서 제공 하는 것과 동일한 스트리밍 및 패키지 업그레이드 기능을 제공 하지만 Active Directory 또는 SQL Server 요구 사항은 필요 하지 않습니다. 그러나 스트리밍 서버에는 게시 서비스가 없으며 라이선스 또는 계량 기능도 없습니다. 별도의 App-v 관리 서버의 게시 서비스는 App-v 스트리밍 서버와 함께 사용 됩니다. App-v 스트리밍 서버는 기본 서버 구성의 스트리밍 기능을 사용 하 여 여러 위치에 응용 프로그램 가상화를 사용 하려고 하지만 모든 위치에서 App-v 관리 서버를 지 원하는 인프라를 보유 하 고 있지 않은 기업에 대 한 요구 사항을 해결 합니다.

응용 프로그램 가상화 스트리밍 서버는 기존 전자 소프트웨어 배포 시스템 (ESD)을 사용 하는 환경 에서도 사용할 수 있습니다. ESD를 사용 하 여 스트리밍 응용 프로그램을 관리 합니다. 응용 프로그램 가상화 관리 서버와 달리 스트리밍 서버는 SQL 또는 관리 콘솔을 사용 하지 않습니다. 이러한 서버는 Acl (액세스 제어 목록)을 사용 하 여 사용자 권한을 부여 합니다.

## 패키지 배달 방법


응용 프로그램 가상화 서버를 게시 배달 방법으로 사용 하려는 경우 시나리오에 따라 다음과 같은 패키지 배달 방법을 결정 해야 합니다.

-   *동적 패키지 배달*

-   *파일 패키지 배달에서 로드*

### 동적 패키지 배달

동적 패키지를 전달 하는 동안 서버 (응용 프로그램 가상화 관리 서버, 응용 프로그램 가상화 스트리밍 서버 또는 IIS 서버)는 주문형 배포를 통해 가상화 된 응용 프로그램을 최종 사용자에 게 전달 합니다. 서버는 사용자가 응용 프로그램을 처음 시작 하려고 할 때 (요청 시)에만 가상화 된 응용 프로그램 및 패키지를 클라이언트 컴퓨터에 전달 합니다. 서버는 응용 프로그램을 시작 하는 데 필요한 블록만 스트리밍합니다 (기본 기능 블록). 기본 기능 블록이 클라이언트에 게 전달 되 면 응용 프로그램이 실행 됩니다. 클라이언트가 기본 기능 블록에 포함 되지 않은 응용 프로그램 부분에 대 한 액세스 권한을 필요로 하는 경우가 아니면 클라이언트는 전체 응용 프로그램 (증분 배포)을 받지 않습니다. 이 문제가 발생 하면 클라이언트가 순서 없는 요청을 수행 하 고 보조 기능 블록이 클라이언트로 스트리밍됩니다. 동적 패키지 전달을 통해 신속한 응용 프로그램 실행을 할 수 있습니다.

### 파일 패키지 배달에서 로드

파일 패키지 배달에서 로드 하는 경우 서버는 사용자가 응용 프로그램을 시작 하기 전에 가상화 된 전체 응용 프로그램 패키지를 클라이언트 컴퓨터에 전달 합니다. 이 시나리오에서는 가상화 된 응용 프로그램이 동적 배달 모델에 사용 되는 동적, 증분 메서드 대신 전체 패키지로 제공 됩니다.

**참고**  각 배달 방법에 대해 초기 가상 응용 프로그램 배달 프로세스와 가상 응용 프로그램 업데이트 프로세스가 동일 합니다. 업데이트 된 가상 응용 프로그램 패키지가 원래 응용 프로그램 패키지를 대체 합니다.

 

다음 표에서는 각 패키지 배달 방법의 장점과 단점을 비교 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">장점</th>
<th align="left">단점</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>동적 패키지 배달</p></td>
<td align="left"><p>요청에 따라 응용 프로그램이 전달 되 고 업데이트 됩니다.</p>
<p>응용 프로그램은 시작 시간을 최적화 하기 위해 점진적으로 전달 및 업데이트 됩니다.</p>
<p>업데이트는 자동으로 클라이언트 데스크톱에 제공 됩니다.</p></td>
<td align="left"><p>서버 요구 사항으로 인해 엔터프라이즈 토폴로지의 공간이 큽니다.</p>
<p>응용 프로그램 스트리밍은 LAN을 통해 수행 되어야 합니다. WAN을 통해 또는 서버와 클라이언트 간에 불안정 하거나 간헐적인 연결을 사용 하는 배포 시나리오를 사용할 수 없습니다.</p></td>
<td align="left"><p>스트리밍 인프라가 필요 합니다.</p>
<p>Windows Installer는 응용 프로그램 가상화 데스크톱 클라이언트 소프트웨어를 최종 사용자 컴퓨터에 배포 하는 데 사용 됩니다.</p>
<p>대규모 엔터프라이즈는 응용 프로그램 가상화 스트리밍 서버를 배포 지점으로 사용 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>파일 패키지 배달에서 로드</p></td>
<td align="left"><p>일반적인 엔터프라이즈 관리 방법과 일관성을 유지 합니다.</p>
<p>독립 실행형 구성 시나리오를 지원 합니다.</p>
<p>마이크로 지점 문제에 대 한 해결 방법을 제공 합니다.</p></td>
<td align="left"><p>응용 프로그램 배달과 업데이트는 주문형으로 할 수 없습니다.</p>
<p>응용 프로그램 배달과 업데이트는 증분 되지 않습니다. 동적 전달을 기준으로 리소스 소모를 늘립니다.</p></td>
<td align="left"><p>IT 조직은 종종 응용 프로그램 라이선스, 사용자 권한 부여, 인증을 관리 해야 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 서버 관련 프로토콜 및 외부 구성 요소


다음 표에는 응용 프로그램 가상화 서버 기반 시나리오에서 사용할 수 있는 서버 유형과 해당 전송 프로토콜 및 특정 서버 구성을 지 원하는 데 필요한 외부 구성 요소가 나와 있습니다. 또한이 표에는 보고 메커니즘과 각 서버 유형에 대 한 활성 업그레이드 메커니즘도 포함 되어 있습니다. 이러한 시나리오는 모두 응용 프로그램 가상화 관리 서버를 사용 하기 때문에 시스템에 기본으로 제공 되는 내부 보고 기능을 사용할 수 있습니다. 응용 프로그램 가상화 관리 또는 응용 프로그램 가상화 스트리밍 서버를 사용 하 여 클라이언트에 패키지를 제공 하는 경우, 사용자가 클라이언트에 로그인 할 때 서버의 패키지가 자동으로 업그레이드 됩니다. IIS 서버나 파일을 사용 하 여 패키지를 클라이언트에 게 전달 하는 경우 클라이언트의 패키지를 수동으로 업그레이드 해야 합니다.

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
<th align="left">외부 구성 요소 필요</th>
<th align="left">보고</th>
<th align="left">활성 업그레이드</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Application Virtualization 관리 서버</p></td>
<td align="left"><p>플레이어가</p>
<p>RTSPS</p></td>
<td align="left"><p>HTTPS를 사용 하는 경우 IIS 서버를 사용 하 여 .ICO 및 OSD 파일과 방화벽을 다운로드 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</p></td>
<td align="left"><p>내부</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="even">
<td align="left"><p>Application Virtualization 스트리밍 서버</p></td>
<td align="left"><p>플레이어가</p>
<p>RTSPS</p></td>
<td align="left"><p>관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 메커니즘을 사용 합니다. HTTPS를 사용 하는 경우 IIS 서버를 사용 하 여 .ICO 및 OSD 파일을 다운로드 하 고 방화벽을 사용 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</p></td>
<td align="left"><p>내부</p></td>
<td align="left"><p>지원함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IIS 서버</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 메커니즘을 사용 합니다. HTTP 또는 HTTPS를 사용 하는 경우 IIS 서버를 사용 하 여 .ICO 및 OSD 파일과 방화벽을 다운로드 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</p></td>
<td align="left"><p>내부</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p>File</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 방법이 필요 합니다. 파일 공유 또는 스트리밍 기능이 있는 클라이언트 컴퓨터가 필요 합니다.</p></td>
<td align="left"><p>내부</p></td>
<td align="left"><p>지원되지 않음</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[서버 기반 배포용 서버를 구성하는 방법](how-to-configure-servers-for-server-based-deployment.md)

[서버 및 시스템 구성 요소 설치 방법](how-to-install-the-servers-and-system-components.md)

 

 





