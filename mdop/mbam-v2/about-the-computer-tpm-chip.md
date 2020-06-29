---
title: 컴퓨터 TPM 칩 정보
description: 컴퓨터 TPM 칩 정보
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823533"
---
# 컴퓨터 TPM 칩 정보


BitLocker는 TPM (신뢰할 수 있는 플랫폼 모듈) 칩과 함께 사용 하는 경우 추가 보호 기능을 제공 합니다. TPM 칩은 컴퓨터 제조업체가 많은 최신 컴퓨터에 설치 하는 하드웨어 구성 요소입니다. Microsoft BitLocker 관리 및 모니터링 (MBAM)은 TPM 칩 외에도 BitLocker를 사용 하 여 데이터에 대 한 추가 보호를 제공 하 고 컴퓨터가 훼손 되지 않았는지 확인 합니다.

## TPM을 설정 하는 방법


컴퓨터에서 BitLocker 드라이브 암호화 마법사를 시작 하면 조직에서 TPM 칩을 사용 하도록 BitLocker를 구성한 경우 BitLocker에서 TPM 칩을 확인 합니다. BitLocker에서 호환 되는 TPM 칩을 발견 하면 TPM 칩을 사용할 수 있도록 컴퓨터를 다시 시작 하 라는 메시지가 표시 될 수 있습니다. 컴퓨터가 다시 시작 되 면 지침에 따라 BIOS에서 TPM 칩을 구성 합니다 (BIOS가 컴퓨터 소프트웨어의 Windows 이전 계층).

BitLocker를 구성한 후 Windows 제어판에서 BitLocker 암호화 옵션 도구를 열고 **Tpm 관리**를 선택 하 여 tpm 칩에 대 한 추가 정보에 액세스할 수 있습니다.

**참고**  이 도구에 액세스 하려면 컴퓨터에 관리 자격 증명이 있어야 합니다.

 

TPM 오류, BIOS의 변경 또는 특정 Windows 업데이트가 있으면 BitLocker에서 컴퓨터를 잠그고 지원 센터에 연락 하 여 잠금을 해제 하도록 요구 합니다. 컴퓨터의 이름과 컴퓨터의 도메인도 제공 해야 합니다. 지원 센터에서 컴퓨터의 잠금을 해제 하는 데 사용할 수 있는 암호 파일을 제공할 수 있습니다.

## TPM 문제 해결


TPM 오류, BIOS에서 변경 또는 특정 Windows 업데이트가 발생 하는 경우 BitLocker에서 컴퓨터를 잠그고 지원 센터에 문의 하 여 잠금을 해제 해야 합니다. 컴퓨터의 이름과 컴퓨터의 도메인도 제공 해야 합니다. 헬프 데스크는 컴퓨터를 잠금 해제 하는 데 사용할 수 있는 암호 파일을 제공할 수 있습니다.

## 관련 항목


[최종 사용자의 BitLocker 관리 지원](helping-end-users-manage-bitlocker.md)

[PIN 또는 암호 사용](using-your-pin-or-password.md)

 

 





