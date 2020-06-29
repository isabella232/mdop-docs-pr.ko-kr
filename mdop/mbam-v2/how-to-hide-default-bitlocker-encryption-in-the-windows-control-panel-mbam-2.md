---
title: Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법
description: Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824083"
---
# Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법


Microsoft bitlocker 관리 및 모니터링 (MBAM)은 BitLocker 암호화 옵션 이라고 하는 Microsoft BitLocker 관리 및 모니터링 클라이언트 컴퓨터에 대 한 사용자 지정 제어판을 제공 합니다. 이 사용자 지정 제어판은 BitLocker 드라이브 암호화 라고 하는 기본 Windows BitLocker 제어판을 교체할 수 있습니다. 시스템 및 보안의 제어판에 있는 사용자 지정 제어판은 사용자가 PIN 및 암호를 관리 하 고 드라이브 잠금을 해제할 수 있도록 허용 하 고 관리자가 드라이브를 해독 하거나 BitLocker 드라이브 암호화를 일시 중단 하거나 다시 시작할 수 있는 인터페이스를 숨깁니다.

**Windows 제어판에서 기본 BitLocker 드라이브 암호화를 숨기려면**

1.  GPMC (그룹 정책 관리 콘솔), AGPM (고급 그룹 정책 관리) 또는 BitLocker 그룹 정책 컴퓨터의 로컬 그룹 정책 편집기에서 **사용자 구성을**찾습니다.

2.  그런 다음 **정책을**클릭 하 고 **관리 템플릿을**선택한 다음 **제어판**을 클릭 합니다.

3.  **세부 정보** 창에서 **지정 된 제어판 항목 숨기기** 를 두 번 클릭 한 다음 **사용**을 선택 합니다.

4.  **표시**를 클릭 하 고 **추가**를 클릭 한 다음 **Microsoft. bitlocker드라이브 암호화**를 입력 합니다. 이 정책은 Windows 제어판에서 기본 Windows BitLocker 관리 도구를 숨기고 사용자가 시스템 및 보안에서 업데이트 된 MBAM BitLocker 암호화 옵션 도구를 열 수 있도록 합니다.

## 관련 항목


[MBAM 2.0 그룹 정책 개체 배포](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





