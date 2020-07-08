---
title: MBAM 2.0 기능 관리
description: MBAM 2.0 기능 관리
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823508"
---
# MBAM 2.0 기능 관리


필요한 모든 계획을 완료 한 다음 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포한 후 엔터프라이즈에서 BitLocker 암호화를 관리 하는 데 사용할 수 있습니다 .이 섹션의 정보는 설치 후 일일 Microsoft BitLocker 관리 및 모니터링 기능 작업에 대해 설명 합니다.

## MBAM 관리자 역할 관리


모든 서버 기능에 대해 MBAM 설정이 완료 되 면 관리 사용자에 게 액세스 권한을 부여 해야 합니다. 가장 좋은 방법으로, MBAM 서버 기능을 관리 하거나 사용 하는 관리자는 Active Directory 도메인 서비스 보안 그룹에 할당 한 다음 해당 그룹을 해당 MBAM 관리 로컬 그룹에 추가 해야 합니다.

[MBAM 관리자 역할을 관리하는 방법](how-to-manage-mbam-administrator-roles-mbam-2.md)

## BitLocker 암호화 예외 관리


MBAM을 사용 하면 드라이브를 암호화 하지 않아도 되는 특정 사용자에 게 암호화 예외를 부여할 수 있습니다. 컴퓨터 예외는 일반적으로 회사에는 개발 또는 테스트에 사용 되는 컴퓨터 또는 BitLocker를 지원 하지 않는 이전 컴퓨터와 같이 암호화 하지 않아도 되는 컴퓨터가 있는 경우에 사용 됩니다. 경우에 따라 지역 법에서 특정 컴퓨터가 암호화 되지 않도록 요구할 수도 있습니다.

[사용자 BitLocker 암호화 예외를 관리하는 방법](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## 제어판을 사용 하 여 MBAM 클라이언트 BitLocker 암호화 옵션 관리


MBAM은 **시스템 및 보안**아래에 표시 되는 BitLocker 암호화 옵션 이라고 하는 사용자 지정 제어판을 제공 합니다. MBAM 제어판을 사용 하 여 암호화 된 고정 및 이동식 드라이브를 잠금 해제 하 고 PIN 또는 암호를 관리할 수도 있습니다.

**참고**  이 사용자 지정 제어판은 기본 Windows BitLocker 제어판을 대체 하지 않습니다.

 

[제어판을 사용하여 MBAM 클라이언트 BitLocker 암호화 옵션을 관리하는 방법](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## MBAM 기능을 관리 하기 위한 기타 리소스


[MBAM 2.0 작업](operations-for-mbam-20-mbam-2.md)

 

 





