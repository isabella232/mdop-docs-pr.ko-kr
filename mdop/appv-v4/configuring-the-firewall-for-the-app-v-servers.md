---
title: App-V Server용 방화벽 구성
description: App-V Server용 방화벽 구성
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821818"
---
# App-V Server용 방화벽 구성


Microsoft App-v (Application Virtualization) 관리 서버 또는 스트리밍 서버를 설치 하 고 RTSP 또는 RTSPS 프로토콜을 사용 하도록 구성한 후에는 App-v 프로그램에 대 한 방화벽 예외를 만들어야 합니다.

## Application Virtualization 관리 서버에 대 한 방화벽 예외 구성


**sghwdsptr.exe** 및 **sghwsvr.exe**에 대 한 방화벽 예외를 만듭니다. 이러한 프로그램은 32 비트 운영 체제의 C:\\program files Files\\Microsoft System Center App Virt 관리 Server\\App Virt 관리 Server\\app 폴더에 있습니다. 64 비트 운영 체제 버전을 사용 하는 경우 폴더는 C:\\program files Files (x86) \\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin에 있습니다.

## Application Virtualization 스트리밍 서버용 방화벽 예외 구성


**sglwdsptr.exe** 및 **sglwsvr.exe**에 대 한 방화벽 예외를 만듭니다. 이러한 프로그램은 32 비트 운영 체제의 C:\\program files Files\\Microsoft System Center App Virt 스트리밍 Server\\App Virt 스트리밍 Server\\app 폴더에 있습니다. 64 비트 운영 체제 버전을 사용 하는 경우 폴더는 C:\\program files Files (x86) \\Microsoft System 센터 앱 Virt Streaming Server\\App Virt 스트리밍 Server\\bina에 있습니다.

## 관련 항목


[서버 기반 배포용 서버를 구성하는 방법](how-to-configure-servers-for-server-based-deployment.md)

[기본 응용 프로그램을 설치 및 구성하는 방법](how-to-install-and-configure-the-default-application.md)

 

 





