---
title: Application Virtualization 패키지 정보
description: Application Virtualization 패키지 정보
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820083"
---
# Application Virtualization 패키지 정보


응용 프로그램 가상화에서 *패키지* 는 시퀀싱 프로세스의 출력입니다. 서버에 응용 프로그램을 처음 배포할 때와 새 버전으로 응용 프로그램을 업그레이드 하는 경우 패키지를 사용 합니다. 패키지를 사용 하 여 응용 프로그램 가상화 관리 서버에서 가상 응용 프로그램 버전을 제어할 수 있습니다. 단일 패키지에는 하나 이상의 응용 프로그램이 포함 될 수 있습니다. 각 응용 프로그램 패키지에는 자체 포함 단위의 파일 집합이 포함 되어 있습니다.

## 패키지 관리


Sequencer가 프로세스의 일부로 하나 이상의 응용 프로그램 패키지를 만든 후 시퀀서에서 생성 된 파일을 응용 프로그램 가상화 관리 서버에 복사 하 여 스트리밍할 수 있도록 할 수 있습니다.

사용 가능한 패키지는 응용 프로그램 가상화 관리 콘솔의 왼쪽 창에 있는 **패키지** 컨테이너 아래에 나타납니다. Sequencer 프로젝트 (SPRJ) 파일이 나 OSD (개방형 소프트웨어 설명자) 파일을 사용 하 여 응용 프로그램을 가져오면 **패키지** 컨테이너에 관련 항목이 표시 됩니다. 응용 프로그램 가상화 서버 관리 콘솔에서 패키지 및 해당 버전을 배포, 업그레이드 또는 삭제할 수 있습니다.

각 가상 응용 프로그램에는 연결 된 패키지가 있습니다. 이 패키지에는 다음 파일이 포함 되어 있습니다.

-   SFT-응용 프로그램을 클라이언트로 스트리밍하는 파일입니다.

-   OSD-열려 있는 소프트웨어 설명자 파일에는 응용 프로그램을 찾아 실행 하는 데 필요한 정보가 포함 됩니다.

-   .ICO-사용자 인터페이스 및 바로 가기에서 시각적으로 응용 프로그램을 나타내는 아이콘 파일입니다.

-   SPRJ-Sequencer 프로젝트 파일입니다.

SPRJ 파일을 가져올 때 기본적으로 모든 시퀀싱 된 응용 프로그램을 배포에 사용할 수 있지만 응용 프로그램은 스트리밍을 사용할 수 없습니다. 패키지의 일부 또는 일부 응용 프로그램을 스트리밍할 수 있습니다. 예를 들어 Microsoft Office를 시퀀싱 하 고 가져온 경우 사용자 설정 저장 마법사와 같은 일부 응용 프로그램을 배포 하지 않도록 선택할 수 있습니다. 이 경우에는 배포할 각 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **사용** 상자 (비어 있음)가 선택 되어 있는지 확인 합니다. **사용할 수** 있는 상자가 선택 된 응용 프로그램만 클라이언트 컴퓨터로 스트림 됩니다.

패키지를 resequence 하 고 스트리밍을 위해 새 SFT 파일을 만든 후에는 응용 프로그램 가상화 서버 관리 콘솔을 통해 이전 패키지를 빠르고 쉽게 업그레이드할 수 있습니다.

**패키지 노드를** 사용 해야 하는 유일한 작동 시나리오는 패키지용 새 버전 (SFT 파일)을 도입 하는 경우입니다. 응용 프로그램을 가져올 때마다 액세스 및 라이선스를 응용 프로그램에 할당 하면 응용 프로그램 가상화 시스템에서 패키지 수준에이 정보를 추적 합니다. 즉, 사용자가 응용 프로그램을 사용 하도록 권한을 부여 하면 동일한 패키지에서 모든 응용 프로그램을 실행할 수 있는 권한을 사용자에 게 부여 합니다.

### 패키지 버전

패키지 버전은 특정 SFT 파일로 표시 됩니다. 패키지를 업그레이드 (응용 프로그램에 업데이트 적용 또는 패키지에 응용 프로그램 추가) 하는 경우 새 SFT 파일이 생성 됩니다. 새 SFT 파일을 만들 때마다 새 패키지 버전이 생성 됩니다.

응용 프로그램 가상화 서버 관리 콘솔을 통해 응용 프로그램을 가져오는 경우 소프트웨어는 패키지와 패키지 버전이 아직 없는 경우 자동으로 만듭니다.

## 관련 항목


[Application Virtualization 응용 프로그램 정보](about-application-virtualization-applications.md)

[Application Virtualization Server Management Console 정보](about-the-application-virtualization-server-management-console.md)

[Server Management Console에서 패키지를 관리하는 방법](how-to-manage-packages-in-the-server-management-console.md)

 

 





