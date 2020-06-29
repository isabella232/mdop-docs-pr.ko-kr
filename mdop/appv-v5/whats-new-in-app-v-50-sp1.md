---
title: App-V 5.0 SP1의 새로운 기능
description: App-V 5.0 SP1의 새로운 기능
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813217"
---
# App-V 5.0 SP1의 새로운 기능


이 섹션은 app-v에 이미 익숙한 사용자를 위한 것 이며 App-v 5.0 SP1에서 변경 된 내용을 알아야 합니다. App-v에 익숙하지 않은 경우 [에는 앱-v 5.0에 대 한 읽기 계획](planning-for-app-v-50-rc.md)부터 시작 해야 합니다.

## 표준 기능 변경


다음 섹션에는 App-v 5.0 SP1의 표준 기능 변경 사항에 대 한 정보가 포함 되어 있습니다.

### 지원 되는 언어 변경

자세한 내용은 [앱-V 5.0 SP1 정보](about-app-v-50-sp1.md)를 참조 하세요.

다음 목록에는 새 언어 팩에 대 한 자세한 정보가 나와 있습니다.

-   App-v 5.0 SP1 언어 팩은 모든 App-v 5.0 구성 요소에 대 한 **appv\_xxx\_setup.exe** 설치 관리자에 번들로 제공 됩니다.

-   설치 관리자를 실행 하면 대상 컴퓨터에서 실행 되는 연결 된 운영 체제의 로캘에 따라 가장 적합 한 언어 팩이 자동으로 설치 됩니다.

-   추가 언어 팩이 필요한 경우 다음 명령을 실행 하 여 설치 관리자에서 이러한 언어 팩의 압축을 풀어야 합니다 `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` . 이를 실행 하면 설치 관리자의 내용이 지정 된 위치로 추출 됩니다.

-   적절 한 언어 팩 Windows 설치 파일을 적용 하 여 원하는 언어 팩을 설치 해야 합니다. 예를 들어, **appv\_hib\_LP\_jmmb\_x86.msi** 또는 **appv\_hib\_LP\_jmmb\_x64.msi**를 사용할 수 있습니다. 여기서 **b** 는 구성 요소를 참조 하 고 **jmmb** 는 로캘을 참조 합니다.

## Microsoft Office2010에 대 한 향상 된 지원


**Microsoft Office 2010 시퀀싱 키트 For Application Virtualization 5.0** -microsoft Office2010의 가상화 된 버전을 사용 하 여 일관 된 환경을 사용자에 게 제공할 수 있습니다. **Application Virtualization 5.0 용 Microsoft office 2010 시퀀싱 키트** 는 **App-v 용 Microsoft Office 2010 배포 키트** 와 함께 사용 되며, 필요한 microsoft Office2010 라이선스 서비스도 제공 합니다.






## 관련 항목


[App-V 5.0 정보](about-app-v-50.md)

 

 





