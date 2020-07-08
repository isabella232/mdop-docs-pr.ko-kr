---
title: MBAM 2.5를 사용하여 BitLocker 관리 수행
description: MBAM 2.5를 사용하여 BitLocker 관리 수행
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826008"
---
# MBAM 2.5를 사용하여 BitLocker 관리 수행


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 계획 하 고 배포한 후에는이를 구성 하 고 사용 하 여 엔터프라이즈에서 BitLocker 드라이브 암호화를 관리할 수 있습니다. 이 섹션의 정보는 Microsoft BitLocker 관리 및 모니터링을 사용 하 여 수행 되는 사후 설치, 일상적인 BitLocker 암호화 관리 작업에 대해 설명 합니다.

## TPM 잠금 다시 설정


TPM (신뢰할 수 있는 플랫폼 모듈)은 기본적으로 암호화 키를 포함 하는 기본 보안 관련 기능을 제공 하도록 설계 된 microchip입니다. 일반적으로 TPM은 컴퓨터의 마더보드에 설치 되며 호스트 버스 어댑터를 사용 하 여 시스템의 나머지 부분과 통신 합니다. TPM이 통합 된 컴퓨터에서 암호화 키를 만들고이를 암호화 하 여 TPM 에서만 암호를 해독할 수 있도록 할 수 있습니다.

사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다. TPM 잠금이 설정 되기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수는 제조업체 마다 다릅니다. 컴퓨터 ID 및 연결 된 사용자 식별자를 제공할 때 TPM 소유자 암호 파일을 검색할 수 있는 관리 및 모니터링 웹 사이트에서 MBAM을 사용 하 여 중앙 집중화 된 키 복구 데이터 시스템에 액세스할 수 있습니다.

[TPM 잠금을 다시 설정하는 방법](how-to-reset-a-tpm-lockout-mbam-25.md)

## 드라이브 복구


특히 엔터프라이즈 환경에서 데이터 암호화를 처리 하는 경우 하드웨어 오류 발생 시 해당 데이터를 복구할 수 있는 방법, 인적 자원 변경 또는 암호화 키가 손실 될 수 있는 기타 상황을 고려해 야 합니다.

MBAM의 암호화 된 드라이브 복구 기능은 데이터를 캡처하고 저장할 수 있으며 BitLocker가 복구 모드로 전환 되거나 이동 되거나 손상 될 때 BitLocker로 보호 되는 볼륨에 액세스 하는 데 필요한 도구가 제공 되는지 확인 합니다.

[복구 모드에서 드라이브를 복구하는 방법](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[이동된 드라이브를 복구하는 방법](how-to-recover-a-moved-drive-mbam-25.md)

[손상된 드라이브를 복구하는 방법](how-to-recover-a-corrupted-drive-mbam-25.md)

## 손상 된 컴퓨터의 BitLocker 암호화 상태 확인


MBAM을 사용 하면 분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인할 수 있습니다.

[분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## 셀프 서비스 포털을 사용 하 여 컴퓨터에 다시 액세스


최종 사용자가 BitLocker로 Windows에서 잠긴 경우이 섹션의 지침에 따라 BitLocker 복구 키를 사용 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있습니다.

[셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## 관련 항목


[MBAM 2.5 작업](operations-for-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





