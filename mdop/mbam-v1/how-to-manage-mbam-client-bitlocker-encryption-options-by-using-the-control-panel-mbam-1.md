---
title: 제어판을 사용하여 MBAM 클라이언트 BitLocker 암호화 옵션을 관리하는 방법
description: 제어판을 사용하여 MBAM 클라이언트 BitLocker 암호화 옵션을 관리하는 방법
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812956"
---
# 제어판을 사용하여 MBAM 클라이언트 BitLocker 암호화 옵션을 관리하는 방법


MBAM 클라이언트가 설치 되어 있는 경우 **시스템 및 보안** 에서 Bitlocker 암호화 옵션 이라고 하는 Microsoft bitlocker 관리 및 모니터링 (mbam) 제어판 응용 프로그램을 사용할 수 있습니다. 이 사용자 지정 된 MBAM 제어판은 기본 Windows BitLocker 제어판을 대신 합니다. MBAM 제어판을 사용 하면 암호화 된 드라이브 (수정 및 이동식)의 잠금을 해제할 수 있으며 PIN 또는 암호를 관리 하는 데 도움이 될 수도 있습니다. MBAM 제어판을 사용 하는 방법에 대 한 자세한 내용은 [Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법을](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)참조 하세요.

**참고**  BitLocker 클라이언트의 경우 관리 및 운영 로그 파일이 이벤트 뷰어에 위치 하 고, **응용 프로그램 및 서비스**에서  /  **Microsoft**  /  **Windows**  /  **bits lockermanagement**를 기록 합니다.

 

**MBAM 클라이언트 제어판을 사용 하려면**

1.  BitLocker 암호화 옵션을 열려면 **시작**을 클릭 한 다음 **제어판**을 선택 합니다. **제어판** 이 열리면 **시스템 및 보안**을 선택 합니다.

2.  **BitLocker 암호화 옵션** 을 두 번 클릭 하 여 사용자 지정 된 mbam 제어판을 엽니다. 컴퓨터의 모든 하드 디스크 드라이브 목록과 해당 암호화 상태가 표시 됩니다. 또한 PIN 또는 암호를 관리 하는 옵션도 표시 됩니다.

3.  컴퓨터의 하드 디스크 드라이브 목록을 사용 하 여 암호화 상태를 확인 하거나, 드라이브 잠금을 해제 하거나, 사용자 및 컴퓨터 예외 정책이 배포 된 경우 BitLocker 보호에 대 한 예외를 요청 합니다.

4.  비 관리자는 BitLocker 암호화 옵션 제어판을 사용 하 여 핀 이나 암호를 관리할 수 있습니다. 사용자는 **Pin 관리를** 선택한 다음 현재 pin과 새 pin을 모두 입력할 수 있습니다. 사용자가 새 PIN을 확인할 수도 있습니다. **UPDATE pin** 함수는 사용자가 선택 하는 새 pin으로 다시 설정 됩니다.

5.  비밀 번호를 관리 하려면 **드라이브 잠금 해제** 를 선택 하 고 현재 비밀 번호를 입력 합니다. 드라이브 잠금이 해제 되는 즉시 **암호 재설정** 을 선택 하 여 현재 암호를 변경 합니다.

## 관련 항목


[MBAM 1.0 기능 관리](administering-mbam-10-features.md)

 

 





