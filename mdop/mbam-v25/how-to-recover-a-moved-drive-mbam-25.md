---
title: 이동된 드라이브를 복구하는 방법
description: 이동된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823343"
---
# 이동된 드라이브를 복구하는 방법
이 항목에서는 관리 및 모니터링 웹 사이트 (지원 센터 라고도 함)를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM)으로 암호화 된 운영 체제 드라이브를 복구 하는 방법에 대해 설명 합니다. 드라이브를 이동 하면 TPM (신뢰할 수 있는 플랫폼 모듈) 칩이 변경 되었기 때문에 이전 컴퓨터에서 사용한 PIN이 더 이상 수락 되지 않습니다. 이동한 드라이브를 복구 하려면 복구 키 ID를 가져와 복구 암호를 검색 해야 합니다.

이동한 드라이브를 복구 하려면 관리 및 모니터링 웹 사이트의 **드라이브 복구** 영역을 사용 해야 합니다. **드라이브 복구** 영역에 액세스 하려면 Mbam 헬프데스크 사용자 역할 또는 Mbam Advanced 헬프데스크 사용자 역할을 할당 받아야 합니다. 이러한 역할에 대 한 자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)을 참조 하세요.

**이동한 드라이브를 복구 하려면**
1.  이동한 드라이브를 포함 하는 컴퓨터에서 WinRE (Windows 복구 환경) 모드에서 컴퓨터를 시작 하거나 Microsoft 진단 및 복구 도구 집합 (DaRT)을 사용 하 여 컴퓨터를 시작 합니다.

2.  컴퓨터가 WinRE 또는 DaRT로 시작 되 면, MBAM은 이동 된 운영 체제 드라이브를 고정 데이터 드라이브로 처리 합니다. 이제 MBAM이 드라이브의 복구 암호 ID를 표시 하 고 복구 암호를 요청 합니다.

    **참고**  경우에 따라 시작 프로세스 중 **PIN을 잊어버린** 경우 복구 모드를 입력 하 여 복구 키 ID를 표시할 수 있습니다.

     

3.  복구 키 ID를 사용 하 여 복구 암호를 검색 하 고 관리 및 모니터링 웹 사이트에서 드라이브 잠금을 해제 합니다. 자세한 지침은 [복구 모드에서 드라이브를 복구 하는 방법을](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)참조 하세요.

    이동한 드라이브가 원래 컴퓨터에서 TPM 칩을 사용 하도록 구성 된 경우 다음 추가 단계를 완료 합니다. 그렇지 않으면 복구 프로세스가 완료 됩니다.

4.  드라이브 잠금을 해제 하 고 시작 프로세스를 완료 한 후에 WinRE 모드에서 명령 프롬프트를 열고 `manage-bde` 명령을 사용 하 여 드라이브의 암호를 해독 합니다. 이 도구를 사용 하는 유일한 방법은 TPM을 제거 하는 유일한 방법 이며, 원본 TPM 칩 없이는 PIN 보호기를 제거할 수 있습니다. 명령에 대 한 자세한 내용은 `manage-bde` [Manage-bde (관리)](https://go.microsoft.com/fwlink/?LinkId=393567)를 참조 하세요.

5.  제거가 완료 되 면 컴퓨터를 정상적으로 시작 합니다. MBAM 에이전트는 이제 새 컴퓨터의 TPM과 PIN을 사용 하 여 드라이브를 암호화 하는 정책을 적용 합니다.



## 관련 항목


[MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





