---
title: 로깅 및 추적 구성
description: 로깅 및 추적 구성
author: dansimp
ms.assetid: 4f89552f-e949-48b0-9325-23746034eaa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6edcb643dd34a20a845cb3d44a0fe8b353a6291
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818983"
---
# 로깅 및 추적 구성


관리 템플릿을 사용 하 여 선택적 로깅 및 추적을 중앙에서 구성할 수 있습니다. 이는 AGPM (고급 그룹 정책 관리)과 관련 된 문제를 진단할 때 유용할 수 있습니다.

이 절차를 완료 하려면 agpm 관리자 (전체 제어) 역할이 있는 사용자 계정, 이러한 프로시저에 사용 되는 GPO (그룹 정책 개체)를 만든 승인자의 사용자 계정 또는 AGPM에서 필요한 권한이 있는 사용자 계정이 필요 합니다. 또한 agpm 서버에 대 한 로깅을 시작 하려면 AGPM 서버에 대 한 액세스 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**AGPM에 대 한 로깅 및 추적을 구성 하려면**

1.  **그룹 정책 관리 콘솔** 트리에서 로깅 및 추적을 설정 하려는 모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다. (자세한 내용은 [GPO 편집](editing-a-gpo-agpm30ops.md)을 참조 하세요.)

2.  **그룹 정책 관리 편집기** 창에서 **컴퓨터 구성**, **정책**, **관리 템플릿**, **Windows 구성 요소**및 **AGPM**을 클릭 합니다.

3.  세부 정보 창에서 **AGPM: 로깅 구성을**두 번 클릭 합니다.

4.  **속성** 창에서 **사용**을 클릭 하 고 로그에 기록할 세부 정보 수준을 구성 합니다.

5.  **확인**을 클릭합니다.

6.  **그룹 정책 관리 편집기** 창을 닫습니다. (자세한 내용은 [GPO 배포](deploy-a-gpo-agpm30ops.md)를 참조 하세요.) 그룹 정책이 업데이트 되 면 agpm 서비스를 다시 시작 하 여 AGPM 서버에서 로깅을 시작, 수정 또는 중지 해야 합니다. 그룹 정책 관리자는 컴퓨터에 대 한 로깅을 시작, 수정 또는 중지 하려면 GPMC를 닫았다가 다시 시작 해야 합니다.

    **추적 파일 위치**:

    -   클라이언트:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   서버:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### 추가 고려 사항

-   AGPM 로깅 및 추적을 구성 하려면 GPO를 편집 하 고 배포할 수 있어야 합니다. 추가 세부 정보는 [Gpo 편집](editing-a-gpo-agpm30ops.md) 및 [gpo 배포](deploy-a-gpo-agpm30ops.md) 를 참조 하세요.

### 추가 참조

-   [고급 그룹 정책 관리 구성](configuring-advanced-group-policy-management.md)

 

 





