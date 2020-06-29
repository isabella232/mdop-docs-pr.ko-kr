---
title: TPM 잠금을 다시 설정하는 방법
description: TPM 잠금을 다시 설정하는 방법
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823323"
---
# TPM 잠금을 다시 설정하는 방법


이 항목에서는 관리 및 모니터링 웹 사이트 (지원 데스크 라고도 함)를 사용 하 여 TPM 잠금을 다시 설정 하는 방법에 대해 설명 합니다. 최종 사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다. TPM 잠금이 설정 되기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수는 제조업체 마다 다릅니다.

관리 및 모니터링 웹 사이트의 **Tpm 관리** 영역에서 컴퓨터 ID 및 연결 된 사용자 식별자를 제공할 때 tpm 소유자 암호 파일을 제공 하는 중앙 집중화 된 키 복구 데이터 시스템에 액세스할 수 있습니다.

관리 및 모니터링 웹 사이트의 TPM 관리 영역에 액세스 하려면 MBAM 헬프데스크 사용자 역할 또는 MBAM 고급 헬프 데스크 사용자 역할을 할당 받아야 합니다. 이러한 역할은 관리자가 Active Directory에서 만드는 그룹입니다. 이러한 그룹에 임의의 이름을 사용할 수 있습니다. 자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)을 참조 하세요.

MBAM 및 TPM 소유권에 대 한 자세한 내용은 [mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-tpm)참조 하세요.

**TPM 잠금을 다시 설정 하려면**

1.  웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.

2.  왼쪽 창에서 **Tpm 관리** 를 클릭 하 여 **tpm 관리** 페이지를 엽니다.

3.  컴퓨터 및 컴퓨터 이름의 정규화 된 도메인 이름을 입력 합니다.

4.  최종 사용자의 Windows 로그온 도메인 및 사용자 이름을 입력 하 여 TPM 소유자 암호 파일을 검색 합니다.

    **참고**  MBAM 헬프데스크 사용자 그룹에 속한 사용자 도메인 및 사용자 ID 필드는 필요 하지 않습니다.

     

5.  **TPM 소유자 암호 요청 이유** 목록에서 요청의 이유를 선택 하 고 **제출을**클릭 합니다.

    MBAM 다음 중 하나를 반환 합니다.

    -   일치 하는 TPM 소유자 암호 파일을 찾을 수 없는 경우 오류 메시지

    -   제출 된 컴퓨터에 대 한 TPM 소유자 암호 파일

    TPM 소유자 암호를 검색 한 후 소유자 암호가 표시 됩니다.

6.  Tpm 파일에 암호를 저장 하려면 **저장** 단추를 클릭 합니다.

7.  **관리 및 모니터링 웹 사이트**의 **tpm 관리** 영역에서 **tpm 잠금 다시 설정** 옵션을 선택 하 고 tpm 소유자 암호 파일을 제공 합니다.

    TPM 잠금이 다시 설정 되 고 최종 사용자의 액세스가 복원 됩니다.

    **중요**  TPM 해시 값 또는 TPM 소유자 암호 파일을 최종 사용자에 게 제공 하지 마세요. TPM 정보는 변경 되지 않으므로 파일을 최종 사용자에 게 제공 하는 것이 보안 위험을 생성 합니다.

     



## 관련 항목


[MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





