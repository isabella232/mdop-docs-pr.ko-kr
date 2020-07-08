---
title: 사용자 BitLocker 암호화 예외를 관리하는 방법
description: 사용자 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826793"
---
# 사용자 BitLocker 암호화 예외를 관리하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하면 BitLocker 드라이브 암호화 요구 사항에서 사용자를 제외할 수 있습니다.

BitLocker 보호에서 사용자를 제외 하려면 다음을 수행 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>제외 된 사용자를 지원 하는 인프라를 만듭니다.</p></td>
<td align="left"><p>이 인프라의 예로는 사용자에 게 예외를 요청 하는 데 사용할 수 있는 연락처 전화 번호, 웹 페이지 또는 메일 주소를 제공 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외 된 사용자에 대해 특별히 구성 되어 있는 그룹 정책 개체에 대 한 보안 그룹에 제외 된 사용자를 추가 합니다.</p></td>
<td align="left"><p>이 보안 그룹의 구성원이 컴퓨터에 로그인 하면 사용자의 그룹 정책 설정이 BitLocker 보호에서 사용자를 제외 합니다. 사용자의 그룹 정책 설정이 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>컴퓨터에 이미 BitLocker로 보호 되어 있고 사용자가 제외 된 경우에는 MBAM이 암호화 정책을 규정 하지 않습니다. 그러나 암호화 정책에서 제외 되지 않은 다른 사용자가 컴퓨터에 로그인 하는 경우에는 암호화가 발생 합니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



다음 단계에서는 최종 사용자가 MBAM 클라이언트를 통해 또는 조직에서 사용 하는 프로세스를 통해 BitLocker 드라이브 암호화 예외 프로세스에서 예외를 요청할 때 발생 하는 상황을 설명 합니다. 최종 사용자가 BitLocker 드라이브 암호화에서 예외를 요청할 수 있도록 MBAM 그룹 정책 설정을 구성 해야 합니다.

1.  최종 사용자가 암호화 해야 하는 컴퓨터에 로그인 하면 컴퓨터가 암호화 될 것임을 알리는 알림을 받습니다. 이를 통해 **예외 요청** 을 선택 하 고 **연기**를 선택 하 여 암호화를 연기 하거나, **암호화 시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.

    **참고**  
    **요청 예외** 선택 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호를 연기 합니다.



2.  최종 사용자가 **예외 요청**을 선택 하는 경우 조직의 BitLocker 관리 그룹에 문의 하 라는 알림을 받게 됩니다. **사용자 예외 구성 정책이** 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.

    -   전화번호

    -   웹 페이지 URL

    -   우편 주소

3.  예외 요청이 수신 된 후에는 MBAM 관리자가 사용자를 BitLocker 면제 AD DS (Active Directory 도메인 서비스) 그룹에 추가할지 여부를 결정 합니다.

4.  최종 사용자가 예외 요청을 제출 하면 MBAM 클라이언트가 사용자에 게 "일시적으로 제외 됨"으로 보고 합니다. 그러면 클라이언트는 관리자가 구성 하는 지정 된 일 수를 기다린 후 컴퓨터의 규정 준수를 다시 확인 합니다. MBAM 관리자가 예외 요청을 거부 하는 경우 예외 요청 옵션이 비활성화 되어 사용자가 예외를 다시 요청할 수 없습니다.

Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하면 BitLocker 드라이브 암호화 요구 사항에서 사용자를 제외할 수 있습니다.

BitLocker 보호에서 사용자를 제외 하려면 다음을 수행 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>제외 된 사용자를 지원 하는 인프라를 만듭니다.</p></td>
<td align="left"><p>이 인프라의 예로는 사용자에 게 예외를 요청 하는 데 사용할 수 있는 연락처 전화 번호, 웹 페이지 또는 메일 주소를 제공 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외 된 사용자에 대해 특별히 구성 되어 있는 그룹 정책 개체에 대 한 보안 그룹에 제외 된 사용자를 추가 합니다.</p></td>
<td align="left"><p>이 보안 그룹의 구성원이 컴퓨터에 로그인 하면 사용자의 그룹 정책 설정이 BitLocker 보호에서 사용자를 제외 합니다. 사용자의 그룹 정책 설정이 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>컴퓨터가 이미 BitLocker로 보호 되는 경우 사용자 예외 정책이 적용 되지 않습니다. 또한 다른 사용자가 암호화 정책에서 제외 되지 않은 컴퓨터에 로그인 하는 경우에는 암호화가 발생 합니다.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



다음 단계에서는 최종 사용자가 MBAM 클라이언트를 통해 또는 조직에서 사용 하는 프로세스를 통해 BitLocker 드라이브 암호화 예외 프로세스에서 예외를 요청할 때 발생 하는 상황을 설명 합니다. 최종 사용자가 BitLocker 드라이브 암호화에서 예외를 요청할 수 있도록 MBAM 그룹 정책 설정을 구성 해야 합니다.

1.  최종 사용자가 암호화 해야 하는 컴퓨터에 로그인 하면 컴퓨터가 암호화 될 것임을 알리는 알림을 받습니다. 이를 통해 **예외 요청** 을 선택 하 고 **연기**를 선택 하 여 암호화를 연기 하거나, **암호화 시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.

    **참고**  
    **요청 예외** 선택 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호를 연기 합니다.



2.  최종 사용자가 **예외 요청**을 선택 하는 경우 조직의 BitLocker 관리 그룹에 문의 하 라는 알림을 받게 됩니다. **사용자 예외 구성 정책이** 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.

    -   전화번호

    -   웹 페이지 URL

    -   우편 주소

3.  예외 요청이 수신 된 후에는 MBAM 관리자가 사용자를 BitLocker 면제 AD DS (Active Directory 도메인 서비스) 그룹에 추가할지 여부를 결정 합니다.

4.  최종 사용자가 예외 요청을 제출 하면 MBAM 클라이언트가 사용자에 게 "일시적으로 제외 됨"으로 보고 합니다. 그러면 클라이언트는 관리자가 구성 하는 지정 된 일 수를 기다린 후 컴퓨터의 규정 준수를 다시 확인 합니다. MBAM 관리자가 예외 요청을 거부 하는 경우 예외 요청 옵션이 비활성화 되어 사용자가 예외를 다시 요청할 수 없습니다.

**BitLocker 드라이브 암호화에서 사용자를 제외 하려면**

1.  BitLocker 암호화 요구 사항에서 사용자 예외를 관리 하는 데 사용 되는 AD DS 보안 그룹을 만듭니다.

2.  Microsoft BitLocker 관리 및 모니터링 그룹 정책 서식 파일을 사용 하 여 그룹 정책 개체를 만듭니다.

3.  이전 단계에서 만든 AD DS 그룹과 그룹 정책 개체를 연결 합니다. 사용자를 제외 하는 정책 설정은 **userconfiguration** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** 에 있습니다.

4.  BitLocker에 제외 된 사용자를 위해 만든 보안 그룹에 대해 예외를 요청 하는 사용자의 이름을 추가 합니다.

    사용자가 BitLocker로 제어 되는 컴퓨터에 로그인 하면 MBAM 클라이언트는 사용자 예외 정책 설정을 확인 합니다. 컴퓨터가 이미 암호화 된 경우에는 BitLocker 보호가 일시 중단 되지 않습니다. 컴퓨터가 암호화 되어 있지 않으면 MBAM은 사용자에 게 암호화를 묻지 않습니다.

    **중요**  
    공유 컴퓨터 시나리오는 BitLocker 사용자 예외를 사용 하는 경우 특별 한 고려 사항이 필요 합니다. 예외 비 사용자가 예외 사용자와 공유 된 컴퓨터에 로그인 하는 경우 컴퓨터가 암호화 될 수 있습니다.




## 관련 항목


[MBAM 2.5 기능 관리](administering-mbam-25-features.md)

[MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)




## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




