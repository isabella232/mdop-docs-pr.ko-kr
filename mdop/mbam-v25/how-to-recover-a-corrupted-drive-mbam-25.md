---
title: 손상된 드라이브를 복구하는 방법
description: 손상된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822553"
---
# 손상된 드라이브를 복구하는 방법


이 절차는 관리 및 모니터링 웹사이트 (지원 센터 라고도 함) 웹 사이트에서 BitLocker로 보호 되는 손상 된 드라이브를 복구 하는 데 사용할 수 있습니다. 이렇게 하려면 다음 표에서 설명 하는 작업을 완료 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">자세한 내용 및 추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong> </strong> 관리 및 모니터링 웹 사이트의 드라이브 복구 영역에 액세스 하 여 복구 키 패키지 파일을 만듭니다.</p></td>
<td align="left"><p><strong>드라이브 복구 영역에 액세스 하려면 </strong> Mbam 헬프데스크 사용자 역할 또는 Mbam Advanced 헬프데스크 사용자 역할을 할당 받아야 합니다. 이러한 역할을 만들 때 서로 다른 이름을 지정 했을 수 있습니다. 자세한 내용은 <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> MBAM 2.5 그룹 및 계정 계획을 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>손상 된 드라이브를 포함 하는 컴퓨터에 패키지 파일을 복사 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><code>repair-bde</code>복구 프로세스를 완료 하려면 명령을 사용 합니다.</p></td>
<td align="left"><p>잠재적인 데이터 손실을 방지 하려면 <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> 사용 하기 전에 manage-bde 명령을 검토 하는 것이 좋습니다 </a> .</p></td>
</tr>
</tbody>
</table>

 

**손상 된 드라이브 복구**

1.  웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.

2.  왼쪽 창에서 **드라이브 복구** 를 선택 하 여 암호화 된 **드라이브에 대 한 액세스 복구** 페이지를 엽니다.

3.  최종 사용자의 Windows 로그온 도메인 및 사용자 이름, 드라이브 잠금 해제 이유, 최종 사용자의 복구 암호 ID를 입력 합니다.

    **참고**  고급 헬프데스크 사용자 액세스 그룹의 구성원 인 경우 사용자의 도메인 이름 또는 사용자 이름을 입력할 필요가 없습니다.

     

4.  **제출**을 클릭합니다. 복구 키가 표시 됩니다.

5.  **저장**을 클릭 한 다음 **복구 키 패키지**를 선택 합니다. 컴퓨터에 복구 키 패키지가 생성 됩니다.

6.  복구 키 패키지를 손상 된 드라이브가 있는 컴퓨터에 복사 합니다.

7.  관리자 권한 명령 프롬프트를 엽니다. 이렇게 하려면 **시작** 을 클릭 하 고 `cmd` **프로그램 및 파일 검색** 텍스트 상자에 입력 합니다. **cmd.exe**를 마우스 오른쪽 단추로 클릭 하 고 **관리자 권한으로 실행**을 선택 합니다.

8.  명령 프롬프트에서 다음을 입력 합니다.

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **참고**  손상 된 드라이브를 사용 하는 &lt; *fixed drive* &gt; 하드 디스크 드라이브 (드라이브의 데이터 보다 더 크거나 같은 여유 공간)로 수정 합니다. 손상 된 드라이브의 데이터를 복구 하 여 지정한 하드 디스크 드라이브로 옮깁니다.

     


## 관련 항목


[MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





