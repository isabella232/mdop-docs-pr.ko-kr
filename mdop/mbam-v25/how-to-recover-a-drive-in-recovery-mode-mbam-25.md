---
title: 복구 모드에서 드라이브를 복구하는 방법
description: 복구 모드에서 드라이브를 복구하는 방법
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823368"
---
# 복구 모드에서 드라이브를 복구하는 방법


이 항목에서는 관리 및 모니터링 웹 사이트 (지원 데스크 라고도 함)를 사용 하 여 BitLocker로 보호 된 드라이브가 복구 모드로 전환 되는 경우 최종 사용자에 게 제공 하는 복구 암호를 가져오는 방법을 설명 합니다. 사용자가 PIN 또는 암호를 분실 하거나 잊어버린 경우 또는 TPM (신뢰할 수 있는 모듈 플랫폼) 칩에서 컴퓨터의 BIOS 또는 시작 파일의 변경 내용을 감지 하는 경우 드라이브는 복구 모드로 전환 됩니다.

복구 암호를 얻으려면 관리 및 모니터링 웹 사이트의 **드라이브 복구** 영역을 사용 합니다. 웹 사이트의이 영역에 액세스 하려면 MBAM 헬프데스크 사용자 역할 또는 MBAM 헬프데스크 사용자 역할을 할당 받아야 합니다.

**참고**  
이러한 역할을 만들 때 서로 다른 이름을 지정 했을 수 있습니다. 자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)을 참조 하세요.



**중요**  
복구 암호는 한 번 사용 후 만료 됩니다. 운영 체제 드라이브 및 고정 데이터 드라이브에서는 단일 사용 규칙이 자동으로 적용 됩니다. 이동식 드라이브를 관리 하는 데 사용할 수 있는 그룹 정책 설정이 활성화 된 컴퓨터에서 드라이브를 제거 하 고 다시 삽입 한 후 잠금이 해제 되는 경우에 적용 됩니다.



**복구 모드에서 드라이브를 복구 하려면**

1.  웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.

2.  왼쪽 창에서 **드라이브 복구** 를 선택 하 여 암호화 된 **드라이브에 대 한 액세스 복구** 페이지를 엽니다.

3.  최종 사용자의 Windows 로그온 도메인 및 사용자 이름을 입력 하 여 복구 정보를 확인 합니다.

    **참고**  
    MBAM 헬프데스크 사용자 그룹에 속한 사용자 도메인 및 사용자 ID 필드는 필요 하지 않습니다.



4.  복구 키 ID의 처음 8 자리를 입력 하 여 일치 하는 복구 키 목록을 확인 하거나 전체 복구 키 ID를 입력 하 여 정확한 복구 키를 가져옵니다.

5.  **드라이브 잠금 해제 이유** 목록에서 미리 정의 된 옵션 중 하나를 선택한 다음 **제출을**클릭 합니다.

    MBAM은 다음을 반환 합니다.

    -   일치 하는 복구 암호를 찾을 수 없는 경우 오류 메시지

    -   사용자에 게 일치 하는 복구 암호가 여러 개 있는 경우 일치 하는 항목 수

    -   제출 된 사용자의 복구 암호 및 복구 패키지

        **참고**  
        손상 된 드라이브를 복구 하는 경우 복구 패키지 옵션은 드라이브를 복구 하는 데 필요한 중요 한 정보를 BitLocker에 제공 합니다.



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. 암호를 복사 하려면 **키 복사**를 클릭 한 다음 복구 암호를 전자 메일 메시지에 붙여 넣습니다. 또는 **저장** 을 클릭 하 여 복구 암호를 파일에 저장 합니다.

   사용자가 시스템에 복구 암호를 입력 하거나 복구 패키지를 사용 하는 경우 드라이브의 잠금이 해제 됩니다.



## 관련 항목


[MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





