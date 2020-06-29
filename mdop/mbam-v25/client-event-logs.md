---
title: 클라이언트 이벤트 로그
description: 클라이언트 이벤트 로그
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824193"
---
# 클라이언트 이벤트 로그

MBAM 클라이언트 이벤트 로그는 이벤트 뷰어에 있으며, 응용 프로그램 및 서비스 로그 – Microsoft – Windows – MBAM 작동 경로입니다.
다음 표에는 MBAM 클라이언트에서 발생할 수 있는 이벤트 Id가 포함 되어 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이벤트 ID</th>
<th align="left">채널</th>
<th align="left">이벤트 기호</th>
<th align="left">메시지</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>raid-1</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>MBAM 정책이 성공적으로 적용 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>2</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>MBAM 정책을 적용 하는 동안 오류가 발생 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3-4</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>암호화 상태 데이터가 성공적으로 전송 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4(tcp/ipv4)</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>전송 실패</p></td>
<td align="left"><p>암호화 상태 데이터를 보내는 동안 오류가 발생 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>20cm(8</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>시스템 볼륨이 없습니다. 운영 체제 드라이브를 암호화 하려면 SystemVolume이 필요 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>되었는지</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>TPM 하드웨어가 없습니다. Tpm은 TPM 보호기로 운영 체제 드라이브를 암호화 하는 데 필요 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>1천만</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>컴퓨터가 암호화에서 제외 됩니다. 컴퓨터의 하드웨어 상태: 제외</p></td>
</tr>
<tr class="even">
<td align="left"><p>mb</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>컴퓨터가 암호화에서 제외 됩니다. 컴퓨터의 하드웨어 상태: 알 수 없음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>까지</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>하드웨어 예외 검사에 실패 했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>일자</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>사용자가 암호화에서 제외 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>13</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>사용자가 예외를 요청 했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>~</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>사용자 예외 검사에 실패 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserPostponed 됨</p></td>
<td align="left"><p>사용자가 암호화 프로세스를 연기 했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>17</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>TPM 초기화에 실패 했습니다. 사용자가 BIOS 변경 내용을 거부 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>18</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>MBAM 복구 및 하드웨어 서비스에 연결할 수 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>인치</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>MBAM 복구 및 하드웨어 서비스에 연결 되었습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>명</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>MBAM 정책이 충돌 하거나 손상 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>mb</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>OS 볼륨 암호화 정책이 충돌 했습니다. OS 드라이브 프로텍터와 관련 된 BitLocker 및 MBAM 정책을 확인 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>khz</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>해결 됨 고정 데이터 드라이브 볼륨 암호화 정책이 충돌 합니다. FDD 드라이브 프로텍터와 관련 된 BitLocker 및 MBAM 정책을 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>27</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p># Failednodra</p></td>
<td align="left"><p>암호화 하는 동안 오류가 발생 했습니다. Windows 사전 8.1 컴퓨터의 경우 DRA (데이터 복구 에이전트) 보호기가 FIPS 모드에서 필요 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>일까</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>TPM 소유자 Auth가 escrowed 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>개가</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>볼륨에 대 한 BitLocker 복구 키가 escrowed 되었습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>30</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>볼륨에 대 한 BitLocker 복구 키가 업데이트 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>개</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p><em> &lt; &gt; 볼륨에 대해 적용 정책 날짜, 날짜를 </em> 설정 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p><em> &lt; 볼륨에 대 한 적용 정책 날짜, 날짜 &gt; </em> 를 지웠습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>TPM 잠금을 다시 설정 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>TPM 잠금을 다시 설정 하지 못했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>MBAM 서비스에서 TPM 소유자 인증을 검색 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>MBAM 서비스에서 TPM 소유자 인증을 검색 하지 못했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>WMI 공급자에 대 한 DLL 검색 경로를 업데이트 하지 못했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>에이전트 중지 중-MBAM WMI 공급자 인스턴스를 기다리는 동안 시간이 초과 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>이동식 드라이브를 탑재 했습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>Removable드라이브 분리 됨</p></td>
<td align="left"><p>이동식 드라이브가 분리 되었습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>이 (가) FailedToEnactEndpointUnreachable 수 없음</p></td>
<td align="left"><p>MBAM 복구 및 하드웨어 서비스에 연결 하지 못해 볼륨에 성공적으로 적용 되지 않은 경우</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>볼륨 상태가 잠기면 MBAM 정책이 볼륨에 성공적으로 적용 되지 않았습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>운용</p></td>
<td align="left"><p>전송 불가능 한 전송 상태 Datafailedendpoint접근할 수 없음</p></td>
<td align="left"><p>MBAM 준수 및 상태 서비스에 연결 하지 못하면 암호화 상태 데이터를 전송할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 


## 관련 항목
[MBAM 2.5에 대한 기술 참조](technical-reference-for-mbam-25.md)

[서버 이벤트 로그](server-event-logs.md)

 


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





