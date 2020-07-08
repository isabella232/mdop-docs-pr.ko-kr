---
title: App-V용 Windows Server 2008 방화벽을 구성하는 방법
description: App-V용 Windows Server 2008 방화벽을 구성하는 방법
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817718"
---
# App-V용 Windows Server 2008 방화벽을 구성하는 방법


Windows Server2008 도입으로 방화벽과 IPsec 구성 요소가 하나의 서비스에 통합 되어이 서비스의 기능이 향상 되었습니다. 새 방화벽 서비스는 수신 및 발신 상태 저장 검사를 지원 합니다. 또한 그룹 정책을 통해 특정 방화벽 규칙과 IPsec 정책을 구성할 수 있습니다. Windows Server2008의 Windows 방화벽에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=151980> 하세요.

다음 절차에서는 SMB 또는 HTTP/HTTPS를 통해 .ICO 및 OSD 게시에 대 한 예외 추가를 포함 하지 않습니다. 이러한 예외는 Windows Server 2008 방화벽에 설치 된 네트워크 프로필 및 역할에 따라 자동으로 추가 됩니다.

**참고**  관리 서버가 RTSP를 사용 하도록 구성 된 경우이 절차를 반복 하 여 `sghwsvr.exe` 프로그램을 예외로 추가 합니다.

App-v 스트리밍 서버에는 `sglwdsptr.exe` RTSPS 통신을 위한 프로그램 예외가 필요 합니다. 통신을 위해 RTSP를 사용 하는 App-v 스트리밍 서버에도에 대 한 프로그램 예외가 필요 `sglwsvr.exe` 합니다.

 

**App-v 용 Windows Server2008 방화벽을 구성 하려면**

1.  제어판을 통해 **고급 보안 관리 콘솔을 사용 하 여 Windows 방화벽** 을 열거나 `wf.msc` 실행 줄에 입력 합니다.

2.  새 인바운드 규칙을 만들고 **프로그램**을 선택 합니다.

3.  프로그램 경로를 선택 하 고 `sghwdsptr.exe` 기본적으로에 있는을 찾습니다 `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

4.  **다음**을 클릭합니다.

5.  **작업** 페이지에서 **연결 허용**을 선택 하 고 **다음**을 클릭 합니다.

6.  적절 한 **프로필** 을 선택 하 여 인바운드 규칙에 적용 합니다.

7.  규칙의 이름과 설명을 입력 하 고 **마침을**클릭 합니다.

## 관련 항목


[App-V용 Windows Server 2003 방화벽을 구성하는 방법](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





