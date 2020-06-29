---
title: DaRT 8.0 복구 이미지를 저장 및 배포하는 방법 계획
description: DaRT 8.0 복구 이미지를 저장 및 배포하는 방법 계획
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821243"
---
# DaRT 8.0 복구 이미지를 저장 및 배포하는 방법 계획


다음 방법을 사용 하 여 Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지를 저장 하 고 배포할 수 있습니다. 사용할 방법을 결정할 때는 각각의 장점과 단점을 고려해 야 합니다. 또한 인프라 및 지원 직원을 고려해 야 합니다. 소규모 인프라를 사용 하는 경우에는 복구 이미지를 로컬 하드 드라이브에 설치 하는 경우 항상 사용할 수 있기 때문에 이동식 미디어로 DaRT 8.0을 배포 하는 것이 좋습니다.

조직에서 AD DS (Active Directory 도메인 서비스)를 사용 하는 경우 Windows DS를 사용 하 여 복구 이미지를 네트워크 서비스로 배포 하는 것이 필요할 수 있습니다. 연결 된 컴퓨터는 항상 복구 이미지를 사용할 수 있습니다. Windows DS에서 여러 이미지를 배포 하 고 한 곳에서 모두 유지 관리할 수 있습니다.

**참고**  조직에서 두 개 이상의 메서드를 사용 하는 것이 필요할 수 있습니다. 예를 들어 대부분의 경우 원격 파티션에서 DaRT로 부팅 하 고 최종 사용자 컴퓨터가 네트워크에 연결할 수 없는 경우 USB 플래시 드라이브를 사용할 수 있습니다.

 

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
<td align="left"><p><strong>이동식 미디어</strong></p>
<p>복구 이미지는 지원 직원이이를 불안정 한 컴퓨터로 복구 도구를 사용할 수 있도록 CD, DVD 또는 USB 드라이브에 기록 됩니다.</p></td>
<td align="left"><p>MBR (마스터 부트 레코드)이 손상 되 고 하드 디스크에 액세스할 수 없고 네트워크 연결이 없는 경우를 지원 하는 시나리오를 지원 합니다.</p>
<p>여러 도구를 사용 하 여 다양 한 지원 수준을 제공 하는 다양 한 복구 이미지를 만들 수 있습니다.</p>
<p>이동식 미디어에 복구 이미지를 구울 수 있는 기본 제공 도구를 제공 합니다.</p></td>
<td align="left"><p>지원 직원이 물리적으로 최종 사용자 컴퓨터를 사용 하 여 DaRT로 부팅 하도록 요구 합니다.</p>
<p>32 비트 및 64 비트 컴퓨터에 대해 서로 다른 구성을 사용 하 여 여러 미디어를 만들려면 시간과 유지 관리가 필요 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>원격 (네트워크) 파티션에서</strong></p>
<p>복구 이미지는 사용자 또는 지원 직원이 필요할 때 컴퓨터에 스트리밍할 수 있도록 하는 windows DS (Windows 배포 서비스)와 같은 네트워크 부팅 서버에서 호스팅됩니다.</p></td>
<td align="left"><p>네트워크 부팅 서버에 대 한 액세스 권한이 있는 모든 컴퓨터에서 사용할 수 있습니다.</p>
<p>복구 이미지는 중앙 서버에서 호스팅되므로 중앙 집중식 업데이트를 가능 하 게 합니다.</p>
<p>중앙 집중화 된 지원 센터 직원은 원격 연결을 사용 하 여 복구를 제공할 수 있습니다.</p>
<p>클라이언트에 로컬 저장소 요구 사항이 없습니다.</p>
<p>특정 지원 수준에 대 한 다양 한 도구를 사용 하 여 여러 복구 이미지를 만들 수 있습니다.</p></td>
<td align="left"><p>일반 사용자가 전체 운영 체제 이미징 프로세스가 아닌 DaRT 복구 이미지만 시작할 수 있도록 Windows DS 인프라를 보호 해야 합니다.</p>
<p></p>
<p></p>
<p>최종 사용자 컴퓨터가 런타임에 네트워크에 연결 되어 있어야 합니다.</p>
<p>네트워크를 통해 복구 이미지를 가져와야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>로컬 하드 드라이브의 복구 파티션에서</strong></p>
<p>복구 이미지는 수동으로 또는 System Center Configuration Manager와 같은 전자 소프트웨어 배포 시스템을 사용 하 여 로컬 하드 드라이브에 설치 됩니다.</p></td>
<td align="left"><p>복구 이미지는 컴퓨터에 미리 준비 되어 있으므로 항상 사용할 수 있습니다.</p>
<p>중앙 집중화 된 지원 센터 직원은 원격 연결을 사용 하 여 지원을 제공할 수 있습니다.</p>
<p>복구 이미지는 중앙에서 관리 되 고 배포 됩니다.</p>
<p>Windows BitLocker 드라이브 암호화로 보호 되는 컴퓨터의 추가 복구 키 요청이 제거 됩니다.</p></td>
<td align="left"><p>로컬 저장소가 필요 합니다.</p>
<p>복구 이미지 배치에 대 한 암호화 되지 않은 전용 파티션을 사용할 경우 실패 한 부팅 파티션의 위험을 줄이는 것이 좋습니다.</p>
<p>DaRT를 업데이트 하는 경우 한 파티션 (네트워크의 경우) 또는 이동식 장치에 대 한 것이 아니라 엔터프라이즈의 모든 컴퓨터를 업데이트 해야 합니다.</p>
<p>BitLocker를 사용 하도록 설정한 후 복구 이미지를 배포 하는 경우 추가 고려 사항이 필요 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[DaRT 8.0 배포 계획](planning-to-deploy-dart-80-dart-8.md)

 

 





