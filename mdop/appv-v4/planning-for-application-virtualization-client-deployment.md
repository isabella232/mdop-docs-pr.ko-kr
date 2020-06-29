---
title: Application Virtualization Client 배포 계획
description: Application Virtualization Client 배포 계획
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815953"
---
# Application Virtualization Client 배포 계획


가상 응용 프로그램 패키지를 최종 사용자 컴퓨터에 게시 하 고 배포 하는 방법을 결정 한 후에는 응용 프로그램 가상화 클라이언트 소프트웨어의 배포를 계획 해야 합니다.

응용 프로그램 가상화 클라이언트는 가상 응용 프로그램을 실제로 실행 하는 구성 요소입니다. 응용 프로그램 가상화 클라이언트는 사용자가 아이콘과 상호 작용 하 고 파일 형식을 두 번 클릭 하 여 가상 응용 프로그램을 시작할 수 있도록 합니다. 또한 응용 프로그램을 시작 하기 전에 스트리밍 서버에서 응용 프로그램 콘텐츠의 스트리밍을 처리 하 고 캐시 합니다. 응용 프로그램 콘텐츠는 응용 프로그램을 시작 하 고 초기 사용자 조작을 처리 하는 데 필요한 모든 콘텐츠가 최종 사용자 컴퓨터에 먼저 스트리밍되는지를 구성 합니다. Application Virtualization 클라이언트 소프트웨어에는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 응용 프로그램 가상화 클라이언트 (원격 데스크톱 세션 호스트 (RDSession Host) 서버 시스템 및 다른 모든 컴퓨터에 사용 되는 Application Virtualization 데스크톱 클라이언트에서 사용 됨)의 두 가지 유형이 있습니다.

응용 프로그램 가상화 클라이언트는 응용 프로그램 가상화 관리 콘솔에서 또는 설치 시 명령줄을 통해 다음을 포함 하 여 여러 가지 중요 한 설정으로 구성 해야 합니다.

-   모든 응용 프로그램에 대 한 아이콘의 위치입니다.

-   패키지 정의 정보를 포함 하는 OSD 파일의 위치입니다.

-   응용 프로그램 콘텐츠 원본입니다.

-   이전 항목을 검색할 때 사용할 통신 프로토콜입니다.

-   사용할 캐시 크기 및 캐시 크기 관리 방법입니다.

ESD (전자 소프트웨어 배포) 솔루션을 사용 하는 경우 응용 프로그램 가상화 클라이언트 소프트웨어를 신속 하 게 배포 하기 위해 앞의 설정을 신중 하 게 정의 해야 합니다. 이는 서로 다른 사무실에 컴퓨터를 설치 하 고 다른 원본 위치를 사용 하도록 클라이언트를 구성 해야 하는 경우 특히 중요 합니다.

**참고**  
-   아이콘 위치 및 OSD 파일 값은 Windows Installer 또는 SFTMIME을 사용 하는지 여부에 관계 없이 게시 방법을 선택할 때 고려해 야 하는 중요 한 요소입니다. 응용 프로그램 콘텐츠 원본에 대 한 설정은 스트리밍 방법 선택에 따라 정의 됩니다.

-   캐시에 배포할 수 있는 모든 패키지에 대해 충분 한 공간이 할당 되었는지 확인 하려면 필요에 따라 캐시를 확장할 수 있도록 클라이언트를 구성할 때 사용 **가능한 디스크 공간 임계값** 설정을 사용 합니다. 또는, App-v 캐시에 필요한 디스크 공간을 미리 결정 하 고 설치 시간에 캐시 크기를 적절 하 게 설정 합니다. 캐시 공간 관리 기능에 대 한 자세한 내용은 Microsoft App-v (Application Virtualization) 운영 가이드의 **캐시 공간 관리 기능을 사용** 하는 방법을 참조 하세요.

-   게시 및 HTTP (S) 스트리밍 작업 중에 App-v 4.5 SP1 클라이언트는 사용자 컴퓨터의 Internet Explorer에서 구성한 프록시 서버 설정을 사용 합니다.

클라이언트 설치 매개 변수를 구성 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.

 

마지막으로 데스크톱 클라이언트에 대 한 Application Virtualization 데스크톱 클라이언트 소프트웨어를 배포 하는 방법을 결정 해야 합니다. 각 컴퓨터에 응용 프로그램 가상화 데스크톱 클라이언트를 수동으로 배포할 수 있지만 대부분의 조직에서는 자동화 된 프로세스를 통해이 작업을 수행 해야 합니다. 중간 규모 또는 대규모 조직의 경우 운영에 ESD 시스템을 사용 하는 것 이며, 클라이언트를 배포 하는 데 이상적인 방법입니다. ESD 시스템이 없는 경우 조직에 소프트웨어를 설치 하는 표준 방법을 사용할 수 있습니다. 그룹 정책 또는 다양 한 스크립팅 기술이 선택 됩니다. 보유 하 고 있는 사무실의 수와 크기에 따라이 배포 프로세스는 복잡할 수 있으며, 모든 컴퓨터에서 올바른 구성으로 클라이언트를 설치 하도록 구조적 접근 방식을 사용 하는 것이 중요 합니다.

## 관련 항목


[Application Virtualization 시스템 배포 계획](planning-for-application-virtualization-system-deployment.md)

[명령줄을 사용하여 클라이언트를 설치하는 방법](how-to-install-the-client-by-using-the-command-line-new.md)

[클라이언트에 가상 응용 프로그램을 게시하는 방법](how-to-publish-a-virtual-application-on-the-client.md)

[Application Virtualization Client를 업그레이드하는 방법](how-to-upgrade-the-application-virtualization-client.md)

[App-V Client 제거 방법](how-to-uninstall-the-app-v-client.md)

 

 





