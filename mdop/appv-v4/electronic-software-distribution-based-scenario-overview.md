---
title: 전자 소프트웨어 배포 기반 시나리오 개요
description: 전자 소프트웨어 배포 기반 시나리오 개요
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821598"
---
# 전자 소프트웨어 배포 기반 시나리오 개요


ESD (전자 소프트웨어 배포) 솔루션을 사용 하 여 가상 응용 프로그램을 배포 하려는 경우에는 해당 결정에 영향을 주는 요소를 이해 하는 것이 중요 합니다. 이 항목에서는 ESD 기반 시나리오를 사용 하는 경우의 이점에 대해 설명 하 고 배포를 진행할 때 고려해 야 하는 게시 및 패키지 스트리밍 메서드에 대 한 정보를 제공 합니다.

**중요**  사용 하는 ESD 솔루션에 따라 특정 솔루션의 요구 사항에 대해 잘 알고 있어야 합니다. Microsoft Endpoint Configuration Manager를 사용 하는 경우에는에서 Configuration Manager 설명서를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=66999> .

 

기존 ESD 시스템을 사용 하면 다음과 같은 이점을 얻을 수 있습니다.

-   듀얼 관리 인프라를 제거 합니다.

-   추가 하드웨어 비용 감소

-   추가 운영 체제 및 데이터베이스 라이선스의 비용 감소

## 게시 방법


ESD 기반 시나리오를 사용 하는 경우 클라이언트에 응용 프로그램을 게시할 때 다음과 같은 옵션을 선택할 수 있습니다.

-   **독립 실행형 Windows Installer.** Windows Installer 파일에는 클라이언트가 패키지를 구성 하는 데 사용 하는 매니페스트와 OSD 및 .ICO 파일이 포함 되어 있습니다. 또한이 시나리오는 서버를 사용 하지 않으므로 Windows Installer 파일은 SFT 파일을 클라이언트에 복사 합니다.

-   **패키지 매니페스트를 사용 하는 Windows Installer.** Windows Installer 파일에는 클라이언트가 패키지를 구성 하는 데 사용 하는 매니페스트와 OSD 및 .ICO 파일이 포함 되어 있습니다. SFT 파일은 서버에 저장 됩니다. 명령줄 매개 변수는 클라이언트를 SFT 파일의 위치로 보냅니다.

-   **SFTMIME 명령** SFTMIME 명령은 매니페스트, OSD, .ICO 및 SFT 파일과 함께 사용 되어 클라이언트에 패키지를 추가 합니다. 매니페스트 파일은 클라이언트 컴퓨터에 있거나 UNC 경로를 통해 액세스할 수 있어야 합니다. 클라이언트 구성과 명령줄 옵션에 따라 OSD, .ICO 및 SFT 파일은 클라이언트 컴퓨터 또는 서버에 있을 수 있습니다.

앞의 게시 방법에 대 한 자세한 내용은 [게시 방법 결정](determine-your-publishing-method.md)을 참조 하세요.

## 패키지 스트리밍 메서드


응용 프로그램 가상화 시스템에서 서버에서 클라이언트로 클라이언트에 게 가상 응용 프로그램 패키지 또는 SFT 파일을 스트리밍하는 데 사용할 방법을 결정 해야 합니다. 사용할 수 있는 스트리밍 옵션은 다음과 같습니다.

-   **Application Virtualization 스트리밍 서버.** 구성에서 응용 프로그램 가상화 스트리밍 서버를 사용 하는 경우 SFT 파일이 RTSP 또는 RTSPS 프로토콜을 사용 하 여 해당 서버의 클라이언트로 스트리밍됩니다. 컴퓨터에 서버 소프트웨어를 설치 하 고 레지스트리를 통해 구성 해야 하지만이 구성은 SQL 또는 Active Directory 도메인 서비스와 같은 서비스에 종속 되지 않습니다. SFT 파일은 클라이언트가 액세스할 수 있는 위치에 있는 서버에 저장 됩니다. 배포 메커니즘을 통해 게시 정보를 클라이언트에 배포할 수 있습니다. 그러나 구성 되 면 클라이언트는 자동으로 패키지 업그레이드를 받고 활성 업그레이드가 지원 됩니다.

-   **응용 프로그램 가상화 관리 서버.** 구성에서 응용 프로그램 가상화 관리 서버를 사용 하는 경우 SFT 파일이 RTSP 또는 RTSPS 프로토콜을 사용 하 여 해당 서버의 클라이언트로 스트리밍됩니다. 응용 프로그램 가상화 관리 콘솔을 통해이 서버를 관리 합니다. 이 구성은 SQL 데이터베이스와 Active Directory 서비스를 사용 합니다. 서버에서 게시 정보를 클라이언트에 배포할 수 있으므로 추가 게시 메커니즘이 필요 하지 않습니다.

-   **파일 서버.** 구성에서 파일 서버를 사용 하는 경우, SFT 파일은 SMB 프로토콜을 사용 하 여 다른 클라이언트 컴퓨터로 스트리밍됩니다. 이 구성에 사용 되는 파일 서버는 파일 공유 및 SFT 파일에 대 한 Acl (액세스 제어 목록)을 만들어 관리 합니다. 클라이언트를 파일 서버의 올바른 파일로 이동 하려면 주의를 기울여야 합니다.

-   **IIS 서버.** 구성에서 IIS 서버를 사용 하는 경우 SFT 파일은 HTTP 또는 HTTPS 프로토콜을 사용 하 여 해당 서버의 클라이언트로 스트리밍됩니다. IIS 서버는 쉽게 구성 하 고 관리할 수 있습니다. IIS 서버에서 클라이언트를 올바른 파일로 보내도록 주의를 기울여야 합니다.

앞의 스트리밍 방법에 대 한 자세한 내용은 [스트리밍 방법 결정](determine-your-streaming-method.md)을 참조 하세요.

## 관련 항목


[Application Virtualization Client 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)

[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[게시 방법 결정](determine-your-publishing-method.md)

[스트리밍 방법 결정](determine-your-streaming-method.md)

[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[SFTMIME 명령 참조](sftmime--command-reference.md)

 

 





