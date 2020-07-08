---
title: App-V 5.0 유지 관리
description: App-V 5.0 유지 관리
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813617"
---
# App-V 5.0 유지 관리


필요한 계획을 모두 완료 한 후 App-v 5.0을 배포 하면 다음 정보를 사용 하 여 App-v 5.0 인프라를 유지할 수 있습니다.

## <a href="" id="move-the-app-v-5-0-server-"></a>App-v 5.0 서버 이동


App-v 5.0 서버는 App-v 5.0 데이터베이스에 연결 됩니다. 따라서 네트워크의 컴퓨터에 관리 구성 요소를 설치한 다음 App-v 5.0 데이터베이스에 연결할 수 있습니다.

[App-V Server를 다른 컴퓨터로 이동하는 방법](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a>App-v 5.0 응용 프로그램이 가상화 된 것으로 실행 중인지 확인


앱이 App-v 5.0 이상에서 가상화로 실행 되 고 있는지 확인 하려는 ISV (독립 소프트웨어 공급 업체)는 기본 네임 스페이스에서 **AppVVirtual- &lt; PID &gt; ** 라는 명명 된 개체를 열어야 합니다. 예를 들어 Windows API **Getcurrentprocessid ()** 를 사용 하 여 4052 등의 현재 프로세스 ID를 가져온 다음 읽기 액세스를 위해 기본 네임 스페이스에서 **openevent ()** 를 사용 하 여 **4052 AppVVirtual** 이라는 명명 된 이벤트 개체를 열 수 있는 경우 응용 프로그램이 가상입니다. **Openevent ()** 호출이 실패 하는 경우 응용 프로그램이 가상이 아닌 것입니다.

또한 앱-V 5.0 이상에서 특정 API의 호출을 명시적으로 가상화 하거나 가상화 하려는 ISV는 AppEntSubsystems32.dll 모듈에서 구현 된 **VirtualizeCurrentThread ()** 및 **CurrentThreadIsVirtualized ()** 함수를 사용할 수 있습니다. 이는 다운스트림 구성 요소에 대 한 힌트를 제공 하는 방법으로, 호출이 가상화 되지 않아야 하는 것입니다.






## 앱 유지 관리를 위한 기타 리소스-V 5.0


[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





