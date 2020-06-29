---
title: 사용자 BitLocker 암호화 예외를 관리하는 방법
description: 사용자 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825073"
---
# 사용자 BitLocker 암호화 예외를 관리하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 드라이브를 암호화 하지 않아도 되는 사용자가 있는 경우 exempting 사용자가 BitLocker 보호를 관리할 수 있습니다.

BitLocker 보호에서 사용자를 제외 하려면 조직에서 사용자에 게 예외를 요청 하는 데 사용할 연락처 전화 번호, 웹 페이지 또는 메일 주소를 제공 하는 등 제외 된 사용자를 지원 하는 인프라를 만들어야 합니다. 또한 예외 사용자는 제외 된 사용자를 위해 특별히 만든 그룹 정책 개체에 대 한 보안 그룹에 추가 되어야 합니다. 이 보안 그룹의 구성원이 컴퓨터에 로그온 하면 사용자의 그룹 정책 설정에 따라 사용자가 BitLocker 보호에서 제외 되었다는 것이 표시 됩니다. 사용자의 그룹 정책 설정이 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.

**참고**  컴퓨터가 이미 BitLocker로 보호 되는 경우 사용자 예외 정책이 적용 되지 않습니다.

 

다음 표에서는 예외를 설정 하는 방법에 따라 BitLocker 보호가 적용 되는 방식을 보여 줍니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용자 상태</th>
<th align="left">컴퓨터가 제외 되지 않음</th>
<th align="left">컴퓨터 예외</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>사용자 제외 되지 않음</strong></p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 됨</p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되지 않음</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>사용자 예외</strong></p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되지 않음</p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되지 않음</p></td>
</tr>
</tbody>
</table>

 

**BitLocker 암호화에서 사용자를 제외 하려면**

1.  BitLocker 암호화 요구 사항에서 사용자 예외를 관리 하는 데 사용 되는 ActiveDirectoryDomainServices 보안 그룹을 만듭니다.

2.  Microsoft BitLocker 관리 및 모니터링 그룹 정책 서식 파일을 사용 하 여 그룹 정책 개체 설정을 만들고 이전 단계에서 만든 Active Directory 그룹과 연결 합니다. 사용자를 제외 하는 정책 설정은 **Userconfiguration\\administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)** 에서 찾을 수 있습니다.

3.  BitLocker 제외 된 사용자에 대 한 보안 그룹을 만든 후이 그룹에 예외를 요청 하는 사용자의 이름을 추가 합니다. 사용자가 BitLocker로 제어 되는 컴퓨터에 로그온 하면 MBAM 클라이언트가 사용자 예외 정책 설정을 확인 하 고 사용자가 BitLocker 예외 보안 그룹의 일부 인지 여부에 따라 보호를 일시 중단 합니다.

    **중요**  공유 컴퓨터 시나리오는 사용자 예외를 사용할 때 특별 한 고려 사항이 필요 합니다. 비 예외 사용자가 예외 사용자와 공유 된 컴퓨터에 로그온 하면 컴퓨터가 암호화 될 수 있습니다.

     

**사용자가 BitLocker 암호화에서 예외를 요청할 수 있도록 설정 하려면**

1.  MBAM 정책 템플릿을 사용 하 여 사용자 예외 정책을 구성한 경우 사용자는 MBAM 클라이언트를 통해 BitLocker 보호에서 예외를 요청할 수 있습니다.

2.  사용자가 암호화 해야 하는 컴퓨터에 로그온 할 때 컴퓨터가 암호화 될 것임을 알리는 알림을 받습니다. **예외 요청** 을 선택 하 고 **나중**에 선택 하 여 암호화를 연기 하거나 **시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.

    **참고**  **요청 예외** 선택 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호를 연기 합니다.

     

3.  사용자가 **예외 요청**을 선택 하는 경우 조직의 BitLocker 관리 그룹에 문의 하 라는 알림을 받게 됩니다. 사용자 예외 구성 정책이 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.

    -   전화 번호

    -   웹 페이지 URL

    -   우편 주소

    예외 요청이 수신 된 후에는 MBAM 관리자가 사용자를 BitLocker 예외 Active Directory 그룹에 추가 하는 것이 적절 한지 결정할 수 있습니다.

    **참고**  사용자가 예외 요청을 제출 하면 MBAM 에이전트는 사용자를 "일시적으로 예외"로 보고 하 고 구성 가능한 일 수를 기다린 후 컴퓨터의 준수를 다시 확인 합니다. MBAM 관리자가 예외 요청을 거부 하는 경우 예외 요청 옵션이 비활성화 되어 사용자가 예외를 다시 요청할 수 없습니다.

     

## 관련 항목


[MBAM 2.0 기능 관리](administering-mbam-20-features-mbam-2.md)

 

 





