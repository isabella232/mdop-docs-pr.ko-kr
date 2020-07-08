---
title: MBAM 관리자 역할을 관리하는 방법
description: MBAM 관리자 역할을 관리하는 방법
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825118"
---
# MBAM 관리자 역할을 관리하는 방법


모든 서버 기능에 대해 Microsoft BitLocker 관리 및 모니터링 (MBAM) 설치가 완료 된 후에는 관리 사용자에 게 액세스 권한을 부여 해야 합니다. Microsoft BitLocker 관리 및 모니터링 서버 기능을 관리 하거나 사용 하는 관리자가 도메인 서비스 보안 그룹에 할당 되 면 해당 그룹을 적절 한 MBAM 관리 로컬 그룹에 추가 하는 것이 가장 좋습니다.

**MBAM 관리자 역할 구성원 자격을 관리 하려면**

1.  ActiveDirectory 도메인 서비스의 보안 그룹에 관리자 사용자를 할당 합니다.

2.  각각의 기능에 대해 MBAM 서버에서 MBAM 관리 로컬 그룹의 역할에 ActiveDirectory 보안 그룹을 추가 합니다.

    -   **Mbam 시스템 관리자** 는 Mbam 관리 및 모니터링 웹 사이트의 모든 mbam 기능에 액세스할 수 있습니다.

    -   **Mbam 헬프데스크 사용자** 는 mbam 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 옵션에 액세스할 수 있지만, 두 옵션 중 하나를 사용 하는 경우 모든 필드를 채워야 합니다.

    -   **Mbam 보고서 사용자** 는 Mbam 관리 및 모니터링 웹 사이트의 규정 준수 및 감사 보고서에 액세스할 수 있습니다.

    -   **Mbam 헬프데스크 사용자** 는 mbam 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 옵션에 액세스할 수 있지만, 두 옵션 중 하나를 사용할 때 모든 필드를 채우지 않아도 됩니다.

    Microsoft BitLocker 관리 및 모니터링에 대 한 역할에 대 한 자세한 내용은 [MBAM 2.0 관리자 역할 계획](planning-for-mbam-20-administrator-roles-mbam-2.md)을 참조 하세요.

## 관련 항목


[MBAM 2.0 기능 관리](administering-mbam-20-features-mbam-2.md)

 

 





