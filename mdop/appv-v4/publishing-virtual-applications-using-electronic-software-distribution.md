---
title: 전자 소프트웨어 배포를 사용하여 가상 응용 프로그램 게시
description: 전자 소프트웨어 배포를 사용하여 가상 응용 프로그램 게시
author: dansimp
ms.assetid: 295fbc1d-ed1c-43b4-aeee-0df384d4e630
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0354fc1226aa78d947dd764a0ab6157b563a321
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815743"
---
# 전자 소프트웨어 배포를 사용하여 가상 응용 프로그램 게시


ESD (전자 소프트웨어 배포) 시스템은 느리거나 빠른 네트워크 연결을 통해 다양 한 컴퓨터로 소프트웨어를 효율적으로 이동 하도록 디자인 되었습니다. ESD 시스템을 사용 하는 응용 프로그램 가상화의 경우 다음 방법 중 하나를 사용 하 여 가상 응용 프로그램 패키지를 배포할 수 있습니다.

-   응용 프로그램 가상화 시퀀서에서 생성 된 패키지의 Windows Installer 버전을 사용 하 여 패키지를 각 클라이언트 컴퓨터에 직접 배포 하도록 ESD 시스템을 구성 합니다. Windows Installer 파일에는 아이콘, 패키지 정의 정보 및 콘텐츠가 포함 되며, Windows Installer를 사용 하는 경우 아이콘을 Windows 데스크톱 및 시작 메뉴에 게시 하 고 패키지 콘텐츠를 응용 프로그램 가상화 클라이언트 캐시로 로드 합니다. 사용자는 더 이상 설정 요구 사항 없이 응용 프로그램을 바로 사용할 수 있습니다. Windows Installer를 사용 하 여 package.msi 파일을 제거한 다음 새 버전을 설치 하 여 패키지를 최신 버전으로 업그레이드 하는 작업을 수행 합니다.

-   LAN과 같이 양호한 대역폭의 네트워크 연결을 통해 클라이언트 컴퓨터에 쉽게 액세스할 수 있는 소프트웨어 배포 지점이 나 응용 프로그램 가상화 스트리밍 서버에 패키지 콘텐츠를 배치 합니다. 예를 들어, 각 지사에서 기존 ESD 시스템 배포 지점 컴퓨터를 사용할 수 있습니다. 명령줄 매개 변수를 사용 하 여 클라이언트가 가상 응용 프로그램 패키지를 스트리밍하는 스트리밍 소스를 정의 하면 ESD 시스템에서 패키지의 Windows Installer 버전을 각 클라이언트에 배포 합니다. ESD 시스템을 사용 하 여 패키지 콘텐츠를 포함 하는 SFT 파일을 모든 스트리밍 서버의 파일 공유에 복사할 수도 있습니다. Windows Installer를 사용 하 여 package.msi 파일을 제거한 다음 새 버전을 설치 하 여 패키지를 최신 버전으로 업그레이드 하는 작업을 수행 합니다.

-   위의 모드 중 하나에 자체 포함 Windows Installer 파일을 사용 하 여 패키지를 배포 하는 대신 Application Virtualization 명령줄 언어 SFTMIME을 사용 하 여 훨씬 더 자세한 방법으로 배포를 제어할 수 있습니다. 이는 패키지 관리의 모든 측면을 제어 하는 많은 명령을 제공 합니다. 또한 SFTMIME은 강력 하지만 복잡 하므로 관리자는 프로덕션을 사용 하기 전에 모든 명령을 스크립트로 만들고 테스트 환경에서 철저히 테스트 하는 계획을 세워야 합니다. 사용할 수 있는 SFTMIME 명령에 대 한 자세한 내용은 [Sftmime 명령 참조](sftmime--command-reference.md)를 참조 하세요.

## 관련 항목


[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[Application Virtualization 시스템 배포 계획](planning-for-application-virtualization-system-deployment.md)

[전자 소프트웨어 배포 구현에서 스트리밍 솔루션 계획](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)

[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





