---
title: 사용자 BitLocker 암호화 예외를 관리하는 방법
description: 사용자 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812964"
---
# 사용자 BitLocker 암호화 예외를 관리하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 드라이브를 암호화 하지 않아도 되는 사용자를 exempting BitLocker 보호를 관리할 수 있습니다.

BitLocker 보호에서 사용자를 제외 하려면 먼저 조직이 해당 예외를 지원 하기 위한 인프라를 만들어야 합니다. 지원 인프라에는 예외를 요청 하는 연락처 전화 번호, 웹 페이지 또는 메일 주소가 포함 될 수 있습니다. 또한 예외 사용자는 제외 된 사용자를 위해 특별히 만든 그룹 정책의 보안 그룹에 추가 해야 합니다. 이 보안 그룹의 구성원이 컴퓨터에 로그온 하면 사용자 그룹 정책에 의해 사용자가 BitLocker 보호에서 제외 된 것으로 표시 됩니다. 사용자 정책은 컴퓨터 정책을 덮어쓰므로 컴퓨터는 BitLocker 암호화에서 예외로 유지 됩니다.

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
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되었습니다.</p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>사용자 예외</strong></p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되지 않습니다.</p></td>
<td align="left"><p>컴퓨터에 BitLocker 보호가 적용 되지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

**BitLocker 암호화에서 사용자를 제외 하려면**

1.  BitLocker 암호화에서 사용자 예외를 관리 하는 데 사용 되는 ActiveDirectoryDomainServices 보안 그룹을 만듭니다.

2.  MBAM 그룹 정책 서식 파일을 사용 하 여 그룹 정책 개체 설정 만들기 이전 단계에서 만든 Active Directory 그룹과 그룹 정책 개체를 연결 합니다. 사용자가 BitLocker 암호화에서 예외를 요청할 수 있도록 하는 데 필요한 정책 설정에 대 한 자세한 내용은 [MBAM 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)의 사용자 예외 구성 정책 섹션을 참조 하세요.

3.  BitLocker 제외 된 사용자에 대 한 보안 그룹을 만든 후이 그룹에 예외를 요청 하는 사용자의 이름을 추가 합니다. 사용자가 BitLocker로 제어 되는 컴퓨터에 로그온 하면 MBAM 클라이언트가 사용자 예외 정책 설정을 확인 하 고 사용자가 BitLocker 예외 보안 그룹의 일부 인지 여부에 따라 보호를 일시 중단 합니다.

    **참고**  공유 컴퓨터 시나리오는 사용자 예외에 대 한 특별 한 고려 사항이 필요 합니다. 비 예외 사용자가 예외 사용자와 공유 된 컴퓨터에 로그온 하면 컴퓨터가 암호화 될 수 있습니다.

     

**사용자가 BitLocker 암호화에서 예외를 요청할 수 있도록 설정 하려면**

1.  MBAM 정책 템플릿을 usingwith 하 여 사용자 예외 정책을 구성한 후에는 사용자가 MBAM 클라이언트를 통해 BitLocker 보호의 예외를 요청할 수 있습니다.

2.  사용자가 MBAM 하드웨어 호환성 목록에서 **호환** 되는 것으로 표시 된 컴퓨터에 로그온 하면 시스템은 컴퓨터를 암호화할 수 있는 알림을 사용자에 게 제공 합니다. 사용자는 **예외 요청** 을 선택 하 고 **나중**에 선택 하 여 암호화를 연기 하거나 **시작** 을 선택 하 여 BitLocker 암호화를 수락할 수 있습니다.

    **참고**  **요청 예외** 를 선택 하면 사용자 예외 정책에 설정 된 최대 시간까지 BitLocker 보호가 연기 됩니다.

     

3.  사용자가 **예외 요청**을 선택 하면 조직의 BitLocker 관리 그룹에 게 연락할 수 있는 알림이 사용자에 게 전송 됩니다. 사용자 예외 구성 정책이 구성 되는 방법에 따라 다음 연락 방법 중 하나 이상을 사용 하 여 사용자를 제공할 수 있습니다.

    -   전화 번호

    -   웹 페이지 URL

    -   우편 주소

    요청을 제출 하 고 나면 MBAM 관리자는 BitLocker 예외 Active Directory 그룹에 사용자를 추가 하는 것이 적절 한지 여부를 결정할 수 있습니다.

    **참고**  사용자 예외 정책의 연기 시간 한도가 만료 된 후에는 사용자가 암호화 정책에 대 한 예외를 요청 하는 옵션이 표시 되지 않습니다. 이 시점에서 사용자는 BitLocker 보호에서 예외를 수신 하기 위해 MBAM 관리자에 게 직접 문의 해야 합니다.

     

## 관련 항목


[MBAM 1.0 기능 관리](administering-mbam-10-features.md)

 

 





