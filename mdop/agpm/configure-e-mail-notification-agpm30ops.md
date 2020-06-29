---
title: 전자 메일 알림 구성
description: 전자 메일 알림 구성
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819003"
---
# 전자 메일 알림 구성


편집기나 검토자가 GPO (그룹 정책 개체)를 만들거나, 배포 하거나, 삭제 하려고 할 때 승인자가 요청을 평가 하 고이를 구현 하거나 거부할 수 있도록이 작업에 대 한 요청이 지정 된 전자 메일 주소 또는 주소로 전송 됩니다. 알림이 전송 되는 전자 메일 주소 또는 주소와 알림을 보내는 별칭을 결정할 수 있습니다.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**AGPM에 대 한 전자 메일 알림을 구성 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창에서 **도메인 위임** 탭을 클릭 합니다.

3.  보낸 사람 **전자 메일 주소** 필드에 알림을 보낼 AGPM의 전자 메일 별칭을 입력 합니다.

4.  받는 사람 **전자 메일 주소** 필드에 승인 요청을 받을 승인자의 전자 메일 주소 목록을 쉼표로 구분 하 여 입력 합니다.

5.  **Smtp 서버** 필드에 유효한 SMTP 메일 서버를 입력 합니다.

6.  **사용자 이름** 및 **암호** 필드에 SMTP 서비스에 대 한 액세스 권한이 있는 사용자의 자격 증명을 입력 합니다.

7.  **적용**을 클릭합니다.

### 추가 고려 사항

-   기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다. 특히 도메인에 대 한 **목록 콘텐츠** 및 **옵션 수정** 권한이 있어야 합니다.

-   AGPM에 대 한 전자 메일 알림은 도메인 수준 설정입니다. 각 도메인의 **도메인 위임** 탭에 다른 승인자 전자 메일 주소 또는 AGPM 전자 메일 별칭을 제공 하거나 환경 전체에서 동일한 전자 메일 주소를 사용할 수 있습니다.

-   기본적으로 AGPM (고급 그룹 정책 관리)에서 작업의 결과로 전송 된 전자 메일 메시지는 암호화 되지 않습니다. 그러나 레지스트리 설정을 사용 하 여 AGPM에 대 한 전자 메일 보안을 구성 하 여 SSL (Secure Sockets Layer) 암호화 사용 여부와 사용할 SMTP 포트를 지정할 수 있습니다. 자세한 내용은 [AGPM 용 전자 메일 보안 구성을](configure-e-mail-security-for-agpm-agpm30ops.md) 참조 하세요.

### 추가 참조

-   [고급 그룹 정책 관리 구성](configuring-advanced-group-policy-management.md)

 

 





