---
title: 경계 네트워크에 대한 인터넷 연결 서버 시나리오
description: 경계 네트워크에 대한 인터넷 연결 서버 시나리오
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7415cf7a97edc646653df552723667bac8d25fdc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910693"
---
# <a name="internet-facing-server-scenarios-for-perimeter-networks"></a>경계 네트워크에 대한 인터넷 연결 서버 시나리오


App-V 4.5는 회사 네트워크에 연결되지 않은 사용자나 네트워크 연결을 끊은 사용자가 App-V를 계속 사용할 수 있는 인터넷 연결 서버 시나리오를 지원합니다. 다음 그림과 같이 인터넷에서 보안 프로토콜(RTSPS 및 HTTPS)만 사용할 수 있습니다.

![app-v 방화벽 위치 다이어그램.](images/appvfirewalls.gif)

다음과 같은 방법으로 App-V 인프라가 내부 네트워크에 있는 ISA Server를 사용하여 인터넷 연결 솔루션을 설정할 수 있습니다.

-   ICO 및 OSD 파일을 호스팅하는 IIS 서버에 대한 웹 게시 규칙을 만들며, 필요한 경우 내부 네트워크에 있는 스트리밍용 패키지를 만들 수 있습니다. 자세한 단계는 에서 <https://go.microsoft.com/fwlink/?LinkId=151982> 제공됩니다.

-   App-V RTSPS(웹 관리 서버)에 대한 서버 게시 규칙을 만들 수 있습니다. 자세한 단계는 에서 [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) 제공됩니다.

다음 그림과 같이 인프라가 클라이언트와 ISA 서버 간에 또는 ISA 서버와 내부 네트워크 간에 다른 방화벽을 구현한 경우 트래픽 흐름을 지원하려면 RTSPS(TCP 322) 및 HTTPS(TCP 443) 방화벽 규칙을 모두 만들어야 합니다. 또한 ISA 서버와 내부 네트워크 간에 방화벽이 구현된 경우 도메인 구성원에 필요한 기본 트래픽이 방화벽(DNS, LDAP, Kerberos, SMB/CIFS)을 통해 터널링할 수 있어야 합니다.

![app-v 경계 네트워크 방화벽 다이어그램.](images/appvperimeternetworkfirewall.gif)

방화벽 솔루션은 환경마다 다르기 때문에 이 항목에서 제공하는 지침은 경계 네트워크에서 인터넷 연결 App-V 환경을 구성하는 데 필요한 트래픽에 대해 설명하고 있습니다. 이 정보에는 권장되는 내부 네트워크 서버도 포함됩니다.

다음 서버를 경계 네트워크에 저장합니다.

-   App-V 관리 서버

-   게시 및 스트리밍용 IIS 서버

**참고**  
관리 서버 및 IIS 서버를 별도의 컴퓨터에 두는 것이 가장 좋습니다.

 

내부 네트워크에 다음 서버를 저장합니다.

-   콘텐츠 서버

-   데이터 저장소(SQL Server)

-   Active Directory 도메인 컨트롤러

## <a name="traffic-requirements"></a>트래픽 요구 사항


다음 표에서는 인터넷 및 경계 네트워크와 경계 네트워크에서 내부 네트워크로의 통신에 필요한 트래픽 요구 사항을 나열합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">인터넷에서 경계 네트워크로의 트래픽 요구 사항</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS(새로 고침 및 스트리밍 패키지 게시)</p></td>
<td align="left"><p>기본적으로 TCP 322; 이 설정은 App-V Management Server에서 변경할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS(ICO 및 OSD 파일 및 스트리밍 패키지 게시)</p></td>
<td align="left"><p>기본적으로 TCP 443; IIS 구성에서 변경할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">경계 네트워크에서 내부 네트워크로의 트래픽 요구 사항</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>TCP 1433은 기본값이지만 기본 설정에서 구성할 SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>콘텐츠 디렉터리가 관리 서버 또는 IIS 서버에서 원격으로 있는 경우(권장).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP 및 UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP 및 UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>내부 리소스의 이름 확인을 위해(경계 네트워크 서버에서 호스트 파일을 사용하여 제거할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

 

 





