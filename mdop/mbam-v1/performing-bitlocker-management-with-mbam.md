---
title: MBAM을 사용하여 BitLocker 관리 수행
description: MBAM을 사용하여 BitLocker 관리 수행
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825893"
---
# MBAM을 사용하여 BitLocker 관리 수행


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포한 후에는 MBAM을 구성 하 고 사용 하 여 엔터프라이즈 BitLocker 암호화를 관리할 수 있습니다. 이 섹션에서는 MBAM을 사용 하 여 수행할 수 있는 사후 설치, 일상적인 BitLocker 암호화 관리 작업에 대해 설명 합니다.

## MBAM을 사용 하 여 TPM 잠금 다시 설정


기본 보안 관련 기능을 제공 하는 TPM (신뢰할 수 있는 플랫폼 모듈) microchip. 이러한 함수는 주로 암호화 키를 사용 하 여 수행 됩니다. 일반적으로 TPM은 컴퓨터 또는 랩톱의 마더보드에 설치 되며 하드웨어 버스를 사용 하 여 시스템의 나머지와 통신 합니다. TPM을 통합 하는 컴퓨터는 TPM을 통해서만 암호를 해독할 수 있는 암호화 키를 만들 수 있습니다. 사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다. TPM 잠금이 설정 되기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수는 제조업체 마다 다릅니다. MBAM 관리 웹 사이트의 키 복구 데이터 시스템을 사용 하 여 TPM 소유자 암호 재설정 파일을 얻을 수 있습니다.

[TPM 잠금을 다시 설정하는 방법](how-to-reset-a-tpm-lockout-mbam-1.md)

## MBAM을 사용 하 여 드라이브 복구


하드웨어 오류 발생 시 암호화 된 드라이브에서 데이터 복구를 시도 하는 방법, 인적 자원의 변경 내용 또는 암호화 키가 손실 되는 기타 상황을 확인 해야 합니다. MBAM의 암호화 된 드라이브 복구 기능은 볼륨을 복구 모드로 전환 하거나 이동 하거나 손상 시킬 때 BitLocker 보호 볼륨에 액세스 하는 데 필요한 도구 (데이터의 캡처 및 저장소 사용 가능)를 제공 합니다.

[복구 모드에서 드라이브를 복구하는 방법](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[이동된 드라이브를 복구하는 방법](how-to-recover-a-moved-drive-mbam-1.md)

[손상된 드라이브를 복구하는 방법](how-to-recover-a-corrupted-drive-mbam-1.md)

## MBAM을 사용 하 여 손실 된 컴퓨터의 BitLocker 암호화 상태 확인


MBAM을 사용 하면 분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인할 수 있습니다.

[분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## MBAM을 사용 하 여 BitLocker 관리를 수행 하기 위한 기타 리소스


[MBAM 1.0 작업](operations-for-mbam-10.md)

 

 





