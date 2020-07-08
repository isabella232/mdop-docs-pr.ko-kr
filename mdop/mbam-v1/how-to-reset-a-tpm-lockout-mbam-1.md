---
title: TPM 잠금을 다시 설정하는 방법
description: TPM 잠금을 다시 설정하는 방법
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812921"
---
# TPM 잠금을 다시 설정하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)의 암호화 된 드라이브 복구 기능에는 데이터 캡처 및 저장소와 TPM (신뢰할 수 있는 플랫폼 모듈)을 관리 하는 데 필요한 도구의 가용성이 모두 포함 됩니다. 이 항목에서는 bit \ _admmon \ _tlanextref 관리 웹 사이트에서 중앙 집중화 된 키 복구 데이터 시스템에 액세스 하는 방법에 대해 설명 합니다. 키 복구 데이터 시스템은 컴퓨터 id 및 연결 된 사용자 식별자가 제공 되는 경우 TPM 소유자 암호 파일을 제공할 수 있습니다.

사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다. TPM 잠금이 컴퓨터 제조업체의 사양을 기반으로 하기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수입니다.

**TPM 잠금을 다시 설정 하려면**

1.  MBAM 관리 웹 사이트를 엽니다.

2.  탐색 창에서 **TPM 관리**를 선택 합니다. **TPM 관리** 페이지가 열립니다.

3.  컴퓨터 및 컴퓨터 이름의 FQDN (정규화 된 도메인 이름)을 입력 합니다. 사용자의 Windows 로그온 도메인 및 사용자의 사용자 이름을 입력 합니다. **TPM 소유자 암호 파일 요청 이유** 드롭다운 메뉴에서 미리 정의 된 옵션 중 하나를 선택 합니다. **제출**을 클릭합니다.

4.  MBAM은 다음 중 하나를 반환 합니다.

    -   일치 하는 TPM 소유자 암호 파일을 찾을 수 없는 경우 오류 메시지

    -   제출 된 컴퓨터에 대 한 TPM 소유자 암호 파일

    **참고**  고급 헬프 데스크 사용자 인 경우 사용자 도메인 및 사용자 ID 필드가 필요 하지 않습니다.

     

5.  검색 시 소유자 암호가 표시 됩니다. 이 암호를 tpm 파일에 저장 하려면 **저장** 단추를 클릭 합니다.

6.  사용자는 TPM 관리 콘솔을 실행 하 고 tpm **잠금 다시 설정** 옵션을 선택 하 고 tpm 소유자 암호 파일을 제공 하 여 tpm 잠금을 다시 설정 합니다.

## 관련 항목


[MBAM을 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam.md)

 

 





