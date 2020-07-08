---
title: MBAM 2.5 클라이언트 필수 구성 요소
description: MBAM 2.5 클라이언트 필수 구성 요소
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826968"
---
# MBAM 2.5 클라이언트 필수 구성 요소


최종 사용자의 컴퓨터에 MBAM 클라이언트 소프트웨어를 설치 하기 전에 사용자 환경과 클라이언트 컴퓨터가 다음 필수 조건을 충족 하는지 확인 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>엔터프라이즈 도메인은 적어도 하나 이상의 Windows Server 2008 (이상) 도메인 컨트롤러를 포함 해야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>클라이언트 컴퓨터는 엔터프라이즈 인트라넷에 로그온 해야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 클라이언트 컴퓨터에만 해당: 각 클라이언트에 TPM (신뢰할 수 있는 플랫폼 모듈) 기능 (TPM 1.2 이상)이 있어야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1, Windows 10 RTM 또는 Windows 10 버전 1511 클라이언트 컴퓨터에만 해당: MBAM이 TPM 복구 키를 저장 하 고 관리 하도록 하려면 TPM 자동 프로비저닝이 해제 되어 있어야 하며 mbam을 배포 하기 전에 TPM의 소유자로 설정 해야 합니다.</p>
<p>MBAM 2.5 SP1 전용에서는 더 이상 TPM 자동 프로비저닝을 해제할 필요가 없지만 TPM 그룹 정책 개체가 Active Directory에 대 한 에스크로 TPM 소유자 인증을 사용 하지 않도록 설정 되어 있는지 확인 해야 합니다.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">MBAM 2.5 보안 고려 사항</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다. Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다.</p>
<p>MBAM 2.5 SP1에서는 자동 프로비저닝을 켜야 합니다.</p>
</p></td>
<td align="left"><p>자세한 내용은 <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> TPM 소유자 암호를 참조 하세요 </a> .
</p></td>
</tr>
<tr class="even">
<td align="left"><p>TPM 칩이 BIOS에서 켜져 있고 운영 체제에서 재설정 가능 해야 합니다.</p></td>
<td align="left"><p>자세한 내용은 BIOS 설명서를 참조 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터의 하드 디스크에는 파티션이 두 개 이상 있어야 하 고 NTFS 파일 시스템으로 포맷 되어야 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>컴퓨터의 하드 디스크에는 컴퓨터 시작 중에 USB 장치를 지 원하는 TPM과 호환 되는 BIOS가 있어야 합니다.</p></td>
<td align="left"><div class="alert">
<strong>참고</strong><br/><p>키보드, 비디오 또는 마우스가 키보드, 비디오 또는 마우스 (KVM) 스위치를 통해 직접 연결 되어 관리 되지 않는지 확인 합니다. KVM 스위치는 컴퓨터의 실제 현재 상태를 감지 하는 기능을 방해할 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>프록시를 사용 하는 경우에는 시스템이 시스템 컨텍스트에서 표시 되어야 합니다. MBAM은 사용자 컨텍스트가 아닌 시스템 컨텍스트에서 실행 됩니다.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**중요**  
MBAM 없이 BitLocker를 사용 하는 경우에는 MBAM을 설치 하 고 기존 TPM 정보를 활용할 수 있습니다.




## 관련 항목


[MBAM 2.5 지원되는 구성](mbam-25-supported-configurations.md)

[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.






