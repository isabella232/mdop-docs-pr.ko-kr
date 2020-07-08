---
title: App-V용 Windows Server 2003 방화벽을 구성하는 방법
description: App-V용 Windows Server 2003 방화벽을 구성하는 방법
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817728"
---
# App-V용 Windows Server 2003 방화벽을 구성하는 방법


App-v 용 WindowsServer 2003 방화벽을 구성 하려면 다음 절차를 사용 합니다.

**앱 용 WindowsServer 2003 방화벽을 구성 하려면**

1.  **제어판**에서 **Windows 방화벽**을 엽니다.

    **참고**  이 단계를 수행 하기 전에 서버에서 방화벽 서비스를 실행 하도록 구성 하지 않은 경우 방화벽 서비스를 시작 하 라는 메시지가 표시 됩니다.

     

2.  .ICO 및 OSD 파일이 SMB를 통해 게시 되는 경우 **예외** 탭에서 **파일 및 프린터 공유** 를 사용 하도록 설정 해야 합니다.

    **참고**  .ICO 및 OSD 파일이 관리 서버에서 HTTP/HTTPS를 통해 게시 되는 경우 HTTP 또는 HTTPS에 대 한 예외를 추가 해야 할 수 있습니다. .ICO 및 OSD 파일을 호스트 하는 IIS 서버가 관리 서버와 별개인 컴퓨터에서 호스팅되는 경우 해당 컴퓨터에 예외를 추가 해야 합니다. 성능을 최대화 하려면 관리 서버와는 별도의 서버에서 .ICO 및 OSD 파일을 호스트 하는 것이 좋습니다.

     

3.  관리 서버 서비스 실행 파일인 경우에 대 한 프로그램 예외를 추가 `sghwdsptr.exe` 합니다. 이 실행 파일의 기본 경로는 `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` 입니다.

    **참고**  관리 서버에서 통신을 위해 RTSP를 사용 하는 경우에도 프로그램 예외를 추가 해야 합니다 `sghwsvr.exe` .

    App-v 스트리밍 서버에는 `sglwdsptr.exe` RTSPS 통신을 위한 프로그램 예외가 필요 합니다. 통신을 위해 RTSP를 사용 하는 App-v 스트리밍 서버에도에 대 한 프로그램 예외가 필요 `sglwsvr.exe` 합니다.

     

4.  각 예외에 대해 적절 한 범위가 구성 되어 있는지 확인 합니다. 위험을 줄이려면 컴퓨터를 제거 하 고 서버가 응답 하는 IP 주소를 엄격 하 게 제한 합니다.

## 관련 항목


[App-V용 Windows Server 2008 방화벽을 구성하는 방법](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





