---
title: MBAM 관리자 역할을 관리하는 방법
description: MBAM 관리자 역할을 관리하는 방법
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812969"
---
# MBAM 관리자 역할을 관리하는 방법


모든 서버 기능에 대해 Microsoft BitLocker 관리 및 모니터링 (MBAM) 설치가 완료 된 후에는 관리 사용자에 게 이러한 서버 기능에 대 한 액세스 권한을 부여 해야 합니다. 가장 좋은 방법으로, MBAM 서버 기능을 관리 하거나 사용 하는 관리자는 Active Directory 보안 그룹에 할당 한 다음 해당 그룹을 해당 MBAM 관리 로컬 그룹에 추가 해야 합니다.

**MBAM 관리자 역할 구성원 자격을 관리 하려면**

1.  ActiveDirectoryDomain 서비스의 보안 그룹에 관리 사용자를 할당 합니다.

2.  ActiveDirectoryDomain 서비스 보안 그룹을 해당 기능에 대 한 Microsoft BitLocker 관리 및 모니터링 서버의 MBAM 관리 로컬 그룹 역할에 추가 합니다. 사용자 역할은 다음과 같습니다.

    -   **Mbam 시스템 관리자** 는 mbam 관리 웹 사이트의 모든 Microsoft BitLocker 관리 및 모니터링 기능에 액세스할 수 있습니다.

    -   **Mbam 하드웨어 사용자** 는 mbam 관리 웹 사이트의 하드웨어 호환성 기능에 액세스할 수 있습니다.

    -   **Mbam 헬프데스크 사용자** 는 mbam 관리 웹 사이트의 TPM 관리 및 드라이브 복구 옵션에 액세스할 수 있지만, 두 옵션 중 하나를 사용 하는 경우 모든 필드를 채워야 합니다.

    -   **Mbam 보고서 사용자** 는 mbam 관리 웹 사이트의 규정 준수 및 감사 보고서에 액세스할 수 있습니다.

    -   **Mbam Advanced 헬프데스크** 는 mbam 관리 웹 사이트의 TPM 관리 및 드라이브 복구 옵션에 액세스할 수 있습니다. 이러한 사용자는 두 옵션 중 하나를 사용할 때 모든 필드를 입력할 필요가 없습니다.

    Microsoft BitLocker 관리 및 모니터링에 대 한 역할에 대 한 자세한 내용은 [MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)을 참조 하세요.

## 관련 항목


[MBAM 1.0 기능 관리](administering-mbam-10-features.md)

 

 





