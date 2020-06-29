---
title: App-V 5.0 정보
description: App-V 5.0 정보
author: dansimp
ms.assetid: 5799141b-44bc-4033-afcc-212235e15f00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 24d41bbe3a8f5f0af299490a025a57f4edbf8207
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814968"
---
# App-V 5.0 정보


App-v 5.0는 향상 된 통합 플랫폼, 유연한 가상화, 가상화 응용 프로그램에 대 한 강력한 관리를 제공 합니다. 자세한 내용은 [앱-V 5.0 개요](https://go.microsoft.com/fwlink/?LinkId=325265) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=325265) .

## <a href="" id="what-s-new-"></a>새로운 기능


다음 목록에는 앱-V 5.0의 새로운 기능이 표시 됩니다.

-   **IT 진단 및 모니터링** -app-v 5.0 클라이언트 및 가상화 된 패키지 5.0를 실행 하는 컴퓨터에 대 한 보고 정보를 생성 하는 기능이 향상 되었습니다.

-   **종단 간 프로그래밍** -PowerShell 3.0을 활용 하는 앱-V 5.0는 패키지, 클라이언트 및 서버 작업에 대 한 완전 한 프로그래밍 가능 솔루션을 제공 합니다.

-   **간단 하 고 효율적인 클라이언트 콘솔** -app-v 5.0는 최종 사용자 및 계층 1 지원 엔지니어 시나리오를 단순화 하도록 디자인 된 최신 클라이언트 콘솔을 제공 합니다.

-   **가상 응용 프로그램 확장** -앱-V 5.0 가상 응용 프로그램 확장을 사용 하면 가상 패키지가 로컬로 설치 된 것 처럼 실행할 수 있습니다.

-   **로컬 드라이브 만들기** -앱-V 5.0에는 가상 응용 프로그램 배포를 위한 전용 로컬 드라이브 문자가 더 이상 필요 하지 않습니다.

-   **공유 콘텐츠 저장소** – app-v 5.0 공유 콘텐츠 저장소는 이전 버전의 app-v에서 사용할 수 있는 스트리밍 서버와 유사한 기능을 제공 합니다. 또한 새 버전이 준비 되는 즉시 가상 응용 프로그램에 대 한 업데이트를 사용할 수 있을 뿐만 아니라 디스크 공간도 적게 필요 합니다.

-   **연결 그룹** -앱-V 5.0 연결 그룹을 사용 하 여 대화형으로 가상 응용 프로그램을 연결 하 고 실행할 수 있습니다.

## <a href="" id="bkmk-diff-46-50"></a>App-v 4.6와 App-v 5.0의 차이점


다음 표에는 App-v 4.6 및 App-v 5.0 간의 몇 가지 차이점이 표시 되어 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 4.6</th>
<th align="left">App-V 5.0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>전용 드라이브 문자를 사용 해야 합니다 ( <strong> Q: &lt; /strong &gt; ).</p></td>
<td align="left"><p>전용 드라이브 문자가 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4gb 패키지 크기 한도 요구 사항.</p></td>
<td align="left"><p>4gb 패키지 크기 제한 요구 사항 없음.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>가상 응용 프로그램은 로컬에 설치 된 응용 프로그램에서 격리 됩니다.</p></td>
<td align="left"><p>로컬 응용 프로그램 조작을 지원 하도록 가상 응용 프로그램을 확장할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>동적 도구 모음 컴퍼지션 미들웨어 응용 프로그램과의 상호 작용을 가능 하 게 합니다.</p></td>
<td align="left"><p>피어 응용 프로그램은 연결 그룹을 사용 하 여 공유 됩니다. 연결 그룹에 대 한 자세한 내용은 <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> 연결 그룹 관리를 참조 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VDI/RDS 환경에는 읽기 전용 공유 캐시가 필요 합니다.</p></td>
<td align="left"><p><strong> </strong> 표준 워크플로를 사용 하 여 공유 콘텐츠 저장소를 업데이트할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제한 된 명령줄 스크립트.</p></td>
<td align="left"><p>시퀀서, 클라이언트 및 서버 구성 요소에 대 한 강력한 PowerShell 스크립팅을 지원 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>웹 기반 관리 기능을 제공 합니다.</p></td>
</tr>
</tbody>
</table>

 

## MDOP 기술을 활용 하는 방법


앱-V 5.0는 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .






## 관련 항목


[App-V 5.0 시작](getting-started-with-app-v-50--rtm.md)

 

 





