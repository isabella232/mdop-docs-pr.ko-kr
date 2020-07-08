---
title: DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획
description: DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822798"
---
# DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획


Microsoft 진단 및 DaRT (복구 도구 모음) 7 복구 이미지를 저장 하 고 배포 하려는 경우이 섹션의 정보를 사용 합니다.

## DaRT 복구 이미지를 저장 하 고 배포 하는 방법 계획


다음 방법을 사용 하 여 DaRT 복구 이미지를 저장 하 고 배포할 수 있습니다. 사용할 방법을 결정할 때는 각각의 장점과 단점을 고려해 야 합니다. 또한 enterprise에서 DaRT를 사용 하는 방법도 고려해 야 합니다.

**참고**  조직에서 두 개 이상의 메서드를 사용 하는 것이 좋습니다. 예를 들어 대부분의 경우 원격 파티션에서 DaRT로 부팅 하 고 최종 사용자 컴퓨터가 네트워크에 연결할 수 없는 경우 USB 플래시 드라이브를 사용할 수 있습니다.

 

다음 표에는 조직에서 DaRT를 사용 하는 각 방법의 장점과 단점이 나와 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">DaRT로 부팅 하는 방법</th>
<th align="left">장점</th>
<th align="left">단점</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CD 또는 DVD에서</p></td>
<td align="left"><p>MBR (마스터 부트 레코드)이 손상 되 고 하드 디스크에 액세스할 수 없는 시나리오를 지원 합니다. 또한 네트워크 연결이 없는 경우를 지원 합니다.</p>
<p>이는 이전 버전의 DaRT 사용자에 게 가장 친숙 하며, <strong> Dart 복구 이미지 마법사에서 직접 CD 또는 DVD를 구울 수 있습니다 </strong> .</p></td>
<td align="left"><p>CD 또는 DVD에 대 한 액세스 권한이 있는 사용자가 물리적으로 사용자 컴퓨터를 사용 하 여 DaRT로 부팅 되어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UFD (USB 플래시 드라이브)에서</p></td>
<td align="left"><p>CD 또는 DVD에서 부트할 때와 동일한 이점을 제공 하며 CD 또는 DVD 드라이브가 없는 컴퓨터에도 지원 합니다.</p></td>
<td align="left"><p>DaRT로 부팅 하는 데 UFD를 사용 하기 전에 먼저 UFD의 서식을 지정 해야 합니다. 또한 UFD에 대 한 액세스 권한이 있는 다른 사용자가 물리적으로 사용자 컴퓨터를 사용 하 여 DaRT로 부팅 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>원격 (네트워크) 파티션에서</p></td>
<td align="left"><p>CD, DVD 또는 UFD 없이 DaRT로 부트할 수 있습니다. 또한 업데이트할 파일 위치가 하나 밖에 없기 때문에 DaRT를 쉽게 업그레이드할 수 있습니다.</p></td>
<td align="left"><p>최종 사용자 컴퓨터가 네트워크에 연결 되어 있지 않은 경우에는 작동 하지 않습니다.</p>
<p>최종 사용자가 광범위 하 게 사용할 수 있으며 복구 이미지를 만들 때 추가 보안 고려 사항이 필요할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>복구 파티션에서</p></td>
<td align="left"><p>네트워크 연결이 없는 인스턴스를 포함 하는 CD, DVD 또는 UFD 없이 DaRT로 부팅할 수 있습니다.</p>
<p>또한 Microsoft 끝점 구성 관리자와 같은 자동화 된 배포 도구를 사용 하 여 표준 Windows 이미지 프로세스의 일부로 구현 하 고 관리할 수 있습니다.</p></td>
<td align="left"><p>DaRT를 업데이트 하는 경우 한 파티션 (네트워크) 또는 장치 (CD, DVD 또는 UFD)가 아니라 엔터프라이즈의 모든 컴퓨터를 업데이트 해야 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[DaRT 7.0 배포 계획](planning-to-deploy-dart-70.md)

 

 





