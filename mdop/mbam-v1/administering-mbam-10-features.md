---
title: MBAM 1.0 기능 관리
description: MBAM 1.0 기능 관리
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821223"
---
# MBAM 1.0 기능 관리


필요한 모든 Microsoft BitLocker 관리 및 모니터링 (MBAM) 계획 및 배포를 완료 한 후에 MBAM을 구성 하 고 사용 하 여 엔터프라이즈 BitLocker 암호화를 관리할 수 있습니다. 이 섹션의 정보는 사후 설치 일 대 일일 MBAM 작업에 대해 설명 합니다.

## MBAM 관리자 역할 관리


모든 서버 기능에 대해 MBAM 설정이 완료 되 면 관리 사용자에 게 이러한 서버 기능에 대 한 액세스 권한을 부여 해야 합니다. 가장 좋은 방법으로, MBAM 서버 기능을 관리 하거나 사용 하는 관리자는 Active Directory 보안 그룹에 할당 한 다음 해당 그룹을 해당 MBAM 관리 로컬 그룹에 추가 해야 합니다.

[MBAM 관리자 역할을 관리하는 방법](how-to-manage-mbam-administrator-roles-mbam-1.md)

## 하드웨어 호환성 관리


MBAM 하드웨어 호환성 기능은 BitLocker를 지원 하도록 지정 하는 컴퓨터 하드웨어만 암호화 되도록 하는 데 도움이 될 수 있습니다. 이 기능이 설정 되어 있으면 비트 \ _admmontla는 호환으로 표시 된 컴퓨터만 암호화 합니다.

**중요**  이 기능을 끄면 MBAM 정책이 배포 된 모든 컴퓨터가 암호화 됩니다.

 

MBAM은 "하드웨어 호환성 검사 허용" 그룹 정책을 배포 하는 경우 클라이언트 컴퓨터의 제조업체와 모델 모두에 대 한 정보를 수집할 수 있습니다. 이 정책을 구성 하는 경우 mbam 에이전트는 MBAM 클라이언트가 클라이언트 컴퓨터에 배포 될 때 MBAM 서버에 대 한 정보를 보고 하 고 사용자에 게 모델을 표시 합니다.

[하드웨어 호환성을 관리하는 방법](how-to-manage-hardware-compatibility-mbam-1.md)

[사용자 BitLocker 암호화 예외를 관리하는 방법](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## BitLocker 암호화 예외 관리


MBAM은 BitLocker 암호화 (컴퓨터 예외 및 사용자 예외)에 두 가지 형태의 예외를 부여할 수 있습니다. 컴퓨터 예외는 일반적으로 회사에는 개발 또는 테스트에 사용 되는 컴퓨터 또는 BitLocker를 지원 하지 않는 이전 컴퓨터와 같이 암호화 하지 않아도 되는 컴퓨터가 있는 경우에 사용 됩니다. 경우에 따라 지역 법에서 특정 컴퓨터가 암호화 되지 않도록 요구할 수도 있습니다. 또한 드라이브를 암호화 하지 않아도 되는 사용자를 제외 하도록 선택할 수 있습니다.

[컴퓨터 BitLocker 암호화 예외를 관리하는 방법](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## 제어판을 사용 하 여 MBAM 클라이언트 BitLocker 암호화 옵션 관리


GPO (그룹 정책 개체)를 통해 사용 하도록 설정한 경우 **시스템 및 보안**에서 BitLocker 암호화 옵션 이라고 하는 사용자 지정 mbam 제어판을 사용할 수 있게 됩니다. 이 사용자 지정 제어판은 기본 Windows BitLocker 제어판으로 대체 됩니다. MBAM 제어판을 사용 하면 암호화 된 드라이브 (수정 및 이동식)의 잠금을 해제할 수 있으며 PIN 또는 암호를 관리 하는 데 도움이 될 수도 있습니다.

[제어판을 사용하여 MBAM 클라이언트 BitLocker 암호화 옵션을 관리하는 방법](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## MBAM 기능을 관리 하기 위한 기타 리소스


[MBAM 1.0 작업](operations-for-mbam-10.md)

 

 





