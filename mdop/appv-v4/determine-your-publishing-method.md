---
title: 게시 방법 결정
description: 게시 방법 결정
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821678"
---
# 게시 방법 결정


Application Virtualization Sequencer를 사용 하 여 응용 프로그램을 시퀀싱 한 후 해당 응용 프로그램을 사용자에 게 *게시* 해야 합니다. 응용 프로그램 게시는 응용 프로그램 가상화 클라이언트가 설치 된 각 컴퓨터에 아이콘, 패키지 정의 정보 및 콘텐츠 원본 위치를 제공 하는 것으로 구성 됩니다. 다음 표에서는 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 응용 프로그램 가상화를 배포할 때 지원 되는 게시 방법에 대해 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">장점</th>
<th align="left">단점</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>독립 실행형 솔루션으로 시퀀싱 하는 동안 Windows Installer 파일을 생성 합니다.</p></td>
<td align="left"><ul>
<li><p>사용 하기 매우 간단 합니다.</p></li>
<li><p>패키지가 각 컴퓨터에 로컬로 캐시에 로드 되었습니다.</p></li>
<li><p>사용자에 게 표시 되는 아이콘</p></li>
<li><p>기존 소프트웨어 배포와 유사 합니다.</p></li>
<li><p>스트리밍 서버를 사용할 필요가 없습니다.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>컴퓨터에 있는 패키지 콘텐츠의 위치에는 유연성이 없으며 모든 컴퓨터에 같은 위치가 있습니다.</p></li>
<li><p>응용 프로그램을 제거 하려면 프로그램 추가/제거 또는 msiexec만 사용 해야 합니다.</p></li>
<li><p>패키지 업데이트에 필요한 새 버전으로 제거 및 대체</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>시퀀싱 하는 동안 모드, 부하, OVERRIDEURL 명령줄 속성 및 패키지 매니페스트와 함께 사용 하 여 Windows Installer 파일을 생성 합니다.</p></td>
<td align="left"><ul>
<li><p>유연성을 높이기 위해 간편 하 게 사용할 수 있습니다.</p></li>
<li><p>사용자에 게 표시 되는 아이콘</p></li>
<li><p>응용 프로그램이 포함 된 SFT 파일을 스트리밍 원본 위치에 배치 하 고 클라이언트가 해당 위치를 사용 하도록 구성할 수 있습니다.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>유연성이 제한 됨-패키지 콘텐츠의 위치만 런타임에 제어 될 수 있습니다.</p></li>
<li><p>응용 프로그램을 제거 하려면 프로그램 추가/제거 또는 msiexec만 사용 해야 합니다.</p></li>
<li><p>스트리밍 서버를 사용 하지 않는 경우 패키지 업데이트에 새 버전을 제거 하 고 바꿀 필요가 있습니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>SFTMIME 명령을 실행 합니다.</p></td>
<td align="left"><ul>
<li><p>완전 한 유연성-모든 패키지 관리 기능을 완벽 하 게 제어 합니다.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ESD 시스템에서 사용할 수 있도록 명령을 스크립트로 만들어야 합니다.</p></li>
<li><p>각 컴퓨터에서 올바른 순서로 명령을 실행 해야 합니다.</p></li>
<li><p>명령 언어에 대 한 상세한 이해와 필요한 신중한 계획</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

이러한 게시 방법을 사용 하는 방법에 대 한 자세한 내용은 [클라이언트에 가상 응용 프로그램을 게시 하는 방법을](how-to-publish-a-virtual-application-on-the-client.md)참조 하세요.

## 관련 항목


[스트리밍 방법 결정](determine-your-streaming-method.md)

[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[전자 소프트웨어 배포 기반 시나리오 개요](electronic-software-distribution-based-scenario-overview.md)

[클라이언트에 가상 응용 프로그램을 게시하는 방법](how-to-publish-a-virtual-application-on-the-client.md)

[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





