---
title: 이동된 드라이브를 복구하는 방법
description: 이동된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812929"
---
# 이동된 드라이브를 복구하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 이전에 암호화 된 운영 체제 드라이브를 이동 하는 경우 특정 문제를 해결 해야 합니다. 새 컴퓨터에 PIN을 연결 하면 드라이브는 이전 컴퓨터에서 사용한 시작 PIN을 허용 하지 않습니다. 시스템은 TPM (신뢰할 수 있는 플랫폼 모듈) 칩에 대 한 변경 때문에 PIN이 유효 하지 않은 것으로 간주 합니다. 복구 암호를 검색 하려면 이동한 드라이브를 사용 하기 위해 복구 키 ID를 얻어야 합니다. 이렇게 하려면 다음 절차를 사용 합니다.

**이동한 드라이브를 복구 하려면**

1.  이동한 드라이브를 포함 하는 컴퓨터에서 WinRE (Windows 복구 환경) 모드를 시작 하거나 Microsoft 진단 및 복구 도구 집합 (DaRT)을 사용 하 여 컴퓨터를 시작 합니다.

2.  컴퓨터가 WinRE 또는 DaRT로 시작 되 면, MBAM은 이동 된 운영 체제 드라이브를 데이터 드라이브로 간주 합니다. 이제 MBAM이 드라이브의 복구 암호 ID를 표시 하 고 복구 암호를 요청 합니다.

    **참고**  경우에 따라 시작 프로세스 중 **PIN을 잊어버린** 을 클릭 하 여 복구 모드로 전환 하는 경우도 있을 수 있습니다. 여기에는 복구 키 ID도 표시 됩니다.

     

3.  MBAM 관리 웹 사이트에서 복구 키 ID를 사용 하 여 복구 암호를 검색 하 고 드라이브 잠금을 해제 합니다.

4.  이동한 드라이브가 원래 컴퓨터에서 TPM 칩을 사용 하도록 구성 된 경우 드라이브 잠금을 해제 하 고 시작 프로세스를 완료 한 후에 추가 단계를 수행 해야 합니다. WinRE 모드에서 명령 프롬프트를 열고 **manage-bde** 도구를 사용 하 여 드라이브의 암호를 해독 합니다. 이 도구의 사용은 원본 TPM 칩 없이도 TPM과 핀 보호를 제거 하는 유일한 방법입니다.

5.  제거가 완료 되 면 시스템을 정상적으로 시작 합니다. MBAM 에이전트는 계속 해 서 새 컴퓨터의 TPM plus PIN을 사용 하 여 드라이브를 암호화 하도록 정책을 적용 합니다.

## 관련 항목


[MBAM을 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam.md)

 

 





