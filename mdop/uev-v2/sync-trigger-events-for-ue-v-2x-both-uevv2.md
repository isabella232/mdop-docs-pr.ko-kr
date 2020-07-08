---
title: UE-V 2.x용 동기화 트리거 이벤트
description: UE-V 2.x용 동기화 트리거 이벤트
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826798"
---
# UE-V 2.x용 동기화 트리거 이벤트


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1을 사용 하면 모든 도메인에 가입한 장치에서 응용 프로그램 및 Windows 설정을 동기화 할 수 있습니다. *동기화 트리거 이벤트* 는 ue-v agent가 설정 저장소 위치와 이러한 설정을 동기화 하는 시점을 정의 합니다. UE-V 2에는 *Syncprovider*라는 새로운 *동기화 메서드가* 도입 되었습니다. 동기화 방법 구성에 대 한 자세한 내용은 [ue-v 2. x에 대 한 Sync 메서드](sync-methods-for-ue-v-2x-both-uevv2.md)를 참조 하세요.

## UE-V 2 동기화 트리거 이벤트


다음 표에서는 클래식 응용 프로그램 및 Windows 설정의 트리거 이벤트에 대해 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V 2 트리거 이벤트</strong></p></td>
<td align="left"><p><strong>SyncMethod = Syncmethod</strong></p></td>
<td align="left"><p><strong>SyncMethod = 없음</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows 로그온</strong></p></td>
<td align="left"><ul>
<li><p>설정 저장소 위치에서 응용 프로그램 및 Windows 설정을 로컬 캐시로 가져옵니다.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">비동기 Windows 설정이 </a> 적용 됩니다.</p></li>
<li><p>다음 Windows 로그온 중에 동기 Windows 설정이 적용 됩니다.</p></li>
<li><p>응용 프로그램이 시작 되 면 응용 프로그램 설정이 적용 됩니다.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>설정 저장소 위치에서 직접 응용 프로그램 및 Windows 설정을 읽습니다.</p></li>
<li><p>비동기 및 동기 Windows 설정이 적용 됩니다.</p></li>
<li><p>응용 프로그램이 시작 되 면 응용 프로그램 설정이 적용 됩니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows 로그 오프</strong></p></td>
<td align="left"><p>로컬에서 변경 내용을 저장 하 고 비동기 및 동기 Windows 설정을 설정 저장소 위치 서버 (사용 가능한 경우)에 캐시 하 고 복사 합니다.</p></td>
<td align="left"><p>비동기 및 동기 Windows 설정 저장소 위치에 대 한 변경 내용 저장</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>RDP (Windows Connect)/잠금 해제</strong></p></td>
<td align="left"><p>가능한 경우 설정 저장소 위치에서 로컬 캐시로 비동기 Windows 설정을 동기화 합니다.</p>
<p>캐시 된 Windows 설정 적용</p></td>
<td align="left"><p>설정 저장소 위치에서 비동기 windows 설정 다운로드 및 적용</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>RDP (Windows 연결 끊김)/잠금</strong></p></td>
<td align="left"><p>로컬 캐시에 비동기 Windows 설정 변경 내용을 저장 합니다.</p>
<p>로컬 캐시에서 설정 저장소 위치에 비동기 Windows 설정 (사용 가능한 경우)을 동기화 합니다.</p></td>
<td align="left"><p>설정 저장소 위치에 비동기 Windows 설정 변경 내용 저장</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>응용 프로그램 시작</strong></p></td>
<td align="left"><p>응용 프로그램이 시작 될 때 로컬 캐시에서 응용 프로그램 설정 적용</p></td>
<td align="left"><p>응용 프로그램이 시작 될 때 설정 저장소 위치에서 응용 프로그램 설정 적용</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>응용 프로그램이 닫힙니다.</strong></p></td>
<td align="left"><p>로컬 캐시에 대 한 응용 프로그램 설정 변경 내용을 저장 하 고 설정 저장소 위치에 대 한 설정을 복사 합니다 (사용 가능한 경우).</p></td>
<td align="left"><p>설정 저장소 위치에 대 한 응용 프로그램 설정 변경 내용 저장</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>회사 설정 센터에서 동기화 컨트롤러 예약 작업 또는 "지금 동기화"가 실행 됨</strong></p>
<p></p></td>
<td align="left"><p>설정 저장소 위치와 로컬 캐시 간에 응용 프로그램 및 Windows 설정이 동기화 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>설정 변경 내용은 응용 프로그램이 닫힐 때까지 로컬로 캐시 되지 않습니다. 이 트리거는 현재 실행 중인 응용 프로그램에 대 한 변경 내용을 내보내지 않습니다.</p>
<p>Windows 설정의 경우, 변경 사항은 로컬로 캐시 되지 않고 다음 잠금 (비동기) 또는 로그 오프 (비동기 및 동기)로 내보내집니다.</p>
</div>
<div>

</div>
<p>설정은 다음과 같은 경우에 적용 됩니다.</p>
<ul>
<li><p>비동기 Windows 설정이 직접 적용 됩니다.</p></li>
<li><p>응용 프로그램 설정이 시작 되 면 적용 됩니다.</p></li>
<li><p>비동기 및 동기 Windows 설정은 다음 Windows 로그온 중에 적용 됩니다.</p></li>
<li><p>다음 새로 고침 중에는 AppX (Windows 앱) 설정이 적용 됩니다. <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">자세한 내용은 응용 프로그램 설정 모니터링을 참조 하세요 </a> .</p></li>
</ul></td>
<td align="left"><p>NA</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>원격 저장소에서 비동기 설정 업데이트 *</strong></p></td>
<td align="left"><p>캐시에서 새 비동기 설정을 로드 하 고 적용 합니다.</p></td>
<td align="left"><p>중앙 서버의 설정 로드 및 적용</p></td>
</tr>
</tbody>
</table>








## 관련 항목


[UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)

[UE-V 2. x 예약 된 작업의 빈도 변경](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[UE-V 2. x에 대 한 구성 방법을 선택 합니다.](https://technet.microsoft.com/library/dn458891.aspx#config)









