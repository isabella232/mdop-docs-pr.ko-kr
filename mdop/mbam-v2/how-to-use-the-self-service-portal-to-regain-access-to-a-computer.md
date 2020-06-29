---
title: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
description: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826078"
---
# 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법


최종 사용자가 암호나 PIN을 잊었거나, 운영 체제 파일을 변경 하거나, BIOS 또는 TPM (신뢰할 수 있는 플랫폼 모듈)을 변경 하 였 기 때문에 Windows에서 BitLocker를 통해 잠긴 경우 셀프 서비스 포털을 사용 하 여 지원 부서에 도움을 요청 하지 않고 Windows에 다시 액세스할 수 있습니다.

**참고**  IT 관리자가 IIS 세션 상태 시간 초과를 구성한 경우에는 시간 초과 전에 60 초 후에 메시지가 표시 됩니다.

 

**참고**  이러한 지침은 최종 사용자의 관점에서 작성 되었습니다.

 

**셀프 서비스 포털을 사용 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻으려면**

1.  **복구 KeyId** 필드에 컴퓨터의 BitLocker 복구 화면에 표시 되는 32 자리 BITLOCKER 키 ID 중 최소 8 개를 입력 합니다.

    **참고**  첫 8 자리가 여러 키와 일치 하는 경우 복구 키 ID의 모든 32 자릿수를 입력 해야 한다는 메시지가 표시 됩니다.

     

2.  **이유** 필드에서 복구 키에 대 한 요청 이유를 선택 합니다.

3.  **키 가져오기를**클릭 합니다. BitLocker 복구 키가 "BitLocker 복구 키" 필드에 표시 됩니다.

4.  컴퓨터의 BitLocker 복구 화면에 48 자리 코드를 입력 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있습니다.

## 관련 항목


[MBAM을 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





