---
title: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
description: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826703"
---
# 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법


셀프 서비스 포털은 IT 관리자가 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 배포의 일부로 구성 하는 웹 사이트입니다. 웹 사이트를 사용 하면 Windows에서 잠긴 경우 최종 사용자가 자신의 컴퓨터에 개별적으로 액세스할 수 있습니다. 셀프 서비스 포털에는 지원 센터 직원의 지원이 필요 하지 않습니다.

다음 지침은 최종 사용자의 관점에서 작성 되었지만 IT 관리자가 이해 하는 데 유용할 수 있습니다.

**중요**  최종 사용자가 직접 컴퓨터에 로그온 해야 합니다 (원격이 아닌 경우). 셀프 서비스 포털을 사용 하 여 해당 키를 복구 하기 위해 적어도 한 번은 성공적으로 완료 되었습니다. 그렇지 않으면 키 복구를 위해 헬프 데스크 포털을 사용 해야 합니다.

 

다음과 같은 경우 최종 사용자가 잠금을 경험할 수 있습니다.

-   암호 또는 PIN을 잊으셨습니까?

-   운영 체제 파일, BIOS 또는 TPM (신뢰할 수 있는 플랫폼 모듈) 변경

**참고**  IT 관리자가 IIS 세션 상태 시간을 구성한 경우 셀프 서비스 포털에는 시간 제한 보다 60 초 전에 메시지가 표시 됩니다.

 

**셀프 서비스 포털을 사용 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻으려면**

1.  **복구 KeyId** 필드에 컴퓨터의 BitLocker 복구 화면에 표시 되는 32 자리 BITLOCKER 키 ID 중 최소 8 개를 입력 합니다. 첫 8 자리가 여러 키와 일치 하는 경우 복구 키 ID의 모든 32 자릿수를 입력 해야 한다는 메시지가 표시 됩니다.

2.  **이유** 필드에서 복구 키에 대 한 요청 이유를 선택 합니다.

3.  **키 가져오기를**클릭 합니다. Bitlocker **복구 키 필드에** 표시 됩니다.

4.  컴퓨터의 BitLocker 복구 화면에 48 자리 코드를 입력 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있습니다.



## 관련 항목


[MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





