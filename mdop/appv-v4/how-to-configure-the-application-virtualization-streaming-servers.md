---
title: Application Virtualization Streaming Server 구성 방법
description: Application Virtualization Streaming Server 구성 방법
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817823"
---
# Application Virtualization Streaming Server 구성 방법


가상 응용 프로그램을 Application Virtualization 데스크톱 클라이언트 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 클라이언트로 스트림할 수 있으려면 먼저 Application Virtualization 스트리밍 서버를 구성 해야 합니다. 서버를 구성할 때 SFT 파일이 로드 되 고 저장 되는 *콘텐츠 디렉터리* 를 설정 하 게 됩니다. SFT 파일에는 가상 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.

**중요**  Application Virtualization 서버는 RTSP 또는 RTSPS 프로토콜만 사용 하 여 원격 데스크톱 서비스에 대 한 클라이언트와 데스크톱 클라이언트에 SFT 파일을 스트리밍합니다. .ICO (아이콘) 파일 및 OSD (개방형 소프트웨어 설명자) 파일은 다른 파일 또는 HTTP 서버에서 스트림할 수 있도록 구성 됩니다.

 

**Application Virtualization 스트리밍 서버를 구성 하려면**

1.  Application Virtualization 스트리밍 서버용 설치 절차를 완료 합니다. 설치 절차 중에 **콘텐츠 경로** 화면에서 \\content 디렉터리의 위치를 지정 합니다.

2.  \\Content 디렉터리에 대해 지정한 위치로 이동 하 고 필요한 경우 디렉터리를 만듭니다.

3.  콘텐츠 디렉터리가 만들어지면이 디렉터리를 표준 파일 공유로 구성 합니다.

4.  Content 디렉터리 아래에 있는 콘텐츠 디렉터리와 패키지 폴더에 대 한 NTFS 파일 시스템 사용 권한을 구성 합니다. 각 응용 프로그램에 액세스할 수 있는 사용자를 정의 하는 Active Directory 도메인 서비스의 보안 그룹을 사용 해야 합니다.

## 관련 항목


[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[Application Virtualization Management Server 구성 방법](how-to-configure-the-application-virtualization-management-servers.md)

[파일 서버를 구성하는 방법](how-to-configure-the-file-server.md)

[IIS용 서버를 구성하는 방법](how-to-configure-the-server-for-iis.md)

 

 





