---
title: 파일 서버를 구성하는 방법
description: 파일 서버를 구성하는 방법
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817783"
---
# 파일 서버를 구성하는 방법


다음 절차를 사용 하 여 파일 공유로 사용 되는 로컬 컴퓨터를 구성 하 고 응용 프로그램 가상화 데스크톱 클라이언트와 원격 데스크톱 서비스용 클라이언트 (이전의 터미널 서비스)로 스트림 할 수 있습니다. 이 시나리오는 기존 하드웨어 환경에 추가 서버 인프라를 추가 하지 않으려는 경우에 사용 됩니다.

로컬 사무실에 설치 된 파일 공유의 배포 지점으로 응용 프로그램 가상화 관리 서버를 사용 하는 경우 가상 응용 프로그램을 파일 공유로 사용 되는 컴퓨터로 스트림할 수 있으려면 먼저이 서버를 구성 해야 합니다. 서버와 파일 공유를 구성 하는 경우 SFT 파일이 로드 되 고 저장 되는 콘텐츠 디렉터리를 설정 하 게 됩니다. SFT 파일에는 가상 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.

**중요**  응용 프로그램 가상화 데스크톱 클라이언트 및 원격 데스크톱 서비스에 대 한 클라이언트에 올바르게 스트리밍할 수 있도록 응용 프로그램에서 가상 응용 프로그램을 저장 하는 서버의 콘텐츠 디렉터리에서 SFT 파일이 스트리밍됩니다. .ICO (아이콘) 파일 및 OSD (개방형 소프트웨어 설명자) 파일을 다른 서버에서 스트림할 수 있도록 구성할 수 있습니다.

 

**Application Virtualization 파일 서버를 구성 하려면**

1.  배포 점으로 사용 되는 서버를 구성 하려면 다음 설치 절차를 완료 합니다.

    [Application Virtualization Management Server 설치 방법](how-to-install-application-virtualization-management-server.md)

    **참고**  설치 절차 중에 **콘텐츠 경로** 화면에서 \\content 디렉터리의 위치를 지정 합니다.

     

2.  서버를 설치할 때 지정한 디렉터리에 해당 하는 \\Content 디렉터리를 파일 공유로 사용 하는 각 컴퓨터에 만듭니다.

    **중요**  Application Virtualization Server 또는 IIS 서버가 아닌 파일 공유로 사용 하는 컴퓨터에서 응용 프로그램을 스트림 하는 응용 프로그램 가상화 데스크톱 클라이언트를 구성 합니다.

     

3.  \\Content 디렉터리가 만들어지면이 디렉토리를 표준 파일 공유로 구성 합니다.

## 관련 항목


[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[Application Virtualization Management Server 구성 방법](how-to-configure-the-application-virtualization-management-servers.md)

[Application Virtualization Streaming Server 구성 방법](how-to-configure-the-application-virtualization-streaming-servers.md)

[IIS용 서버를 구성하는 방법](how-to-configure-the-server-for-iis.md)

 

 





