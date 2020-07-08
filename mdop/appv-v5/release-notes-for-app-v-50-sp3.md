---
title: App-V 5.0 SP3 릴리스 정보
description: App-V 5.0 SP3 릴리스 정보
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813324"
---
# App-V 5.0 SP3 릴리스 정보


다음은 Microsoft Application Virtualization (App-v) 5.0 SP3의 알려진 문제점입니다.

## 새 App-v 5.0 SP3 서버 설치 후 서버 파일이 삭제 되지 않음


App-v 5.0 SP1 서버를 제거한 다음 App-v 5.0 SP3 서버를 설치 하면 설치에 실패 하 고 잘못 된 버전의 관리 서버를 설치 합니다. 다음과 같은 오류가 표시 됩니다.

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

이 문제는 App-v 5.0 SP1을 제거 하는 경우 서버 파일이 삭제 되지 않기 때문에 발생 하므로 App-v 5.0 SP3 설치 프로세스가 새로 설치 대신 업그레이드 되지 않습니다.

**해결 방법**: 앱-V 5.0 SP3 설치를 시작 하기 전에 다음 레지스트리 키를 삭제 합니다.

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## AD DS를 쿼리하면 일부 응용 프로그램이 올바르게 작동 하지 않을 수 있음


업데이트 된 그룹 구성원 자격에 대해 Active Directory 도메인 서비스를 쿼리하여 업데이트 된 패키지를 받는 경우 응용 프로그램이 사용자의 액세스 토큰에 의존 하는 경우 일부 응용 프로그램이 올바르게 작동 하지 않을 수 있습니다. 또한 빈번 하 게 그룹 구성원 쿼리를 실행 하면 도메인 컨트롤러가 오버 로드 될 수 있습니다. 사용자 액세스 토큰에 대 한 자세한 내용은 [액세스 토큰](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx)을 참조 하세요.

**해결 방법**: 업데이트 된 그룹 구성원을 쿼리 하기 전에 사용자가 로그 오프할 때까지 기다렸다가 다시 로그온 합니다. 업데이트 된 그룹 구성원에 대 한 쿼리를 위해 [Microsoft Application Virtualization 5.0 서비스 팩 1에 대 한 핫픽스 패키지 2](https://support.microsoft.com/kb/2897087)에 설명 된 레지스트리 키를 사용 하지 마세요.






## 관련 항목


[App-V 5.0 SP3 정보](about-app-v-50-sp3.md)

 

 





