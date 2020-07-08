---
title: 제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기
description: 제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823098"
---
# 제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기


이 항목에서는 Windows 운영 체제의 일부로 제어판에 기본적으로 표시 되는 **BitLocker 드라이브 암호화** 제어판 항목을 숨기는 방법에 대해 설명 합니다.

**참고**  Microsoft BitLocker 관리 및 모니터링 (MBAM)은 **BitLocker 암호화 옵션**이라는 추가 사용자 지정 제어판 항목을 만들어 최종 사용자가 PIN 및 암호를 관리 하 고, 드라이브의 BitLocker를 켜고, 암호화를 확인할 수 있도록 합니다.

 

[제어판의 Bitlocker 암호화 옵션 및 Bitlocker 드라이브 암호화 항목 이해](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) 를 참조 하 여 다음 사항을 읽어 보세요.

-   MBAM과 기본 제어판 항목의 차이점

-   Windows 탐색기에서 드라이브를 마우스 오른쪽 단추로 클릭할 때 표시 되는 BitLocker 바로 가기 메뉴 **관리**

**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요. 이 경우 MBAM이 제대로 작동 하지 않습니다. **MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.

 

**제어판에서 기본 BitLocker 드라이브 암호화 항목을 숨기려면**

1.  GPMC (그룹 정책 관리 콘솔) 또는 고급 그룹 정책 관리에서 **사용자 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **제어판**을 찾습니다.

2.  **세부 정보** 창에서 **지정 된 제어판 항목 숨기기**를 두 번 클릭 한 다음 **사용**을 클릭 합니다.

3.  **표시**를 클릭 하 고 **추가**를 클릭 한 다음 **Microsoft. bitlocker드라이브 암호화**를 입력 합니다.



## 관련 항목


[BitLocker 암호화 옵션 및 제어판의 BitLocker 드라이브 암호화 항목 이해](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[MBAM 2.5 그룹 정책 개체 배포](deploying-mbam-25-group-policy-objects.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





