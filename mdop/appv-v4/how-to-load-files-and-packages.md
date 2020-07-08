---
title: 파일 및 패키지를 로드하는 방법
description: 파일 및 패키지를 로드하는 방법
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817238"
---
# 파일 및 패키지를 로드하는 방법


다음 절차를 사용 하 여 응용 프로그램 가상화 서버에서 파일 및 패키지를 로드할 수 있습니다.

**참고**  설치 프로세스 중에 **콘텐츠 경로** 페이지에서 \\content 디렉터리의 위치를 지정 했습니다. 해당 위치를 가리키기 전에이 디렉터리를 표준 파일 공유로 만들고 구성 해야 합니다.

 

**파일 및 패키지 로드**

1.  스트리밍할 응용 프로그램을 받을 컴퓨터에서 \\Content 디렉터리에 대해 지정한 위치로 이동 합니다. 필요한 경우 디렉터리를 만들고 표준 파일 공유로 구성 합니다.

2.  가상 응용 프로그램 및 패키지의 SFT 파일을 \\Content 디렉터리로 이동 합니다. SFT 파일을 정리 된 상태로 유지 하 고 혼동을 방지 하려면 전용 하위 폴더에 응용 프로그램 및 패키지를 저장 합니다.

3.  시나리오 및 구성 요구 사항에 따라 다음 조건을 고려 하 여 응용 프로그램 및 패키지를 로드 합니다.

    -   응용 프로그램과 패키지가 Application Virtualization (App-v) 관리 서버에 저장 되어 있는 경우 관리 콘솔을 통해 로드 합니다. 자세한 내용은 [응용 프로그램을 로드 또는 언로드하는 방법](how-to-load-or-unload-an-application.md) 또는 [바탕 화면 알림 영역에서 가상 응용 프로그램을 로드](how-to-load-virtual-applications-from-the-desktop-notification-area.md)하는 방법을 참조 하세요.

    -   응용 프로그램이 App-v 스트리밍 서버, 웹 서버 또는 파일 서버로 구성 된 컴퓨터에 저장 되어 있는 경우 응용 프로그램이 자동으로 로드 될 수 있습니다.

        **참고**  App-v 스트리밍 서버는 응용 프로그램 및 패키지에 대 한 \\Content 디렉터리를 자동으로 폴링하여이 정보를 RAM에 저장 하 여 응용 프로그램 요청을 처리 합니다.

        웹 서버와 파일 서버에서 응용 프로그램 및 패키지를 검색 하려면 App-v 클라이언트가 올바르게 구성 되어 있어야 합니다. 자세한 내용은 [응용 프로그램 패키지 검색을 위해 클라이언트를 구성 하는 방법을](how-to-configure-the-client-for-application-package-retrieval.md)참조 하세요.

         

## 관련 항목


[Application Virtualization Server](application-virtualization-server.md)

 

 





