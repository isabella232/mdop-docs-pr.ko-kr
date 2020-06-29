---
title: 관리 서버 보안 사후 설치를 구성하는 방법
description: 관리 서버 보안 사후 설치를 구성하는 방법
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817938"
---
# 관리 서버 보안 사후 설치를 구성하는 방법


앱-V 관리 콘솔을 사용 하 여 인증서를 추가 하 고 앱-V 관리 서버를 구성 하 여 강화 된 보안을 설정 합니다. 다음 절차를 사용 하 여 보안 사후 설치를 구성할 수 있습니다.

**관리 서버 보안을 구성 하려면 설치 후**

1.  App-v 관리 콘솔을 열고 앱-V 관리자 권한을 사용 하 여 **관리 서비스** 에 연결 합니다.

2.  서버를 확장 하 고 **서버 그룹**을 확장 한 다음 관리 서버가 등록 된 적절 한 서버 그룹을 선택 합니다.

3.  관리 서버 개체를 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.

4.  **포트** 탭에서 **서버 인증서** 를 클릭 하 고 마법사를 완료 하 여 적절 하 게 프로 비전 된 인증서를 선택 합니다.

    **참고**  마법사에 인증서가 표시 되지 않으면 인증서가 구축 되지 않았거나 인증서가 App-v의 요구 사항을 충족 하는 것입니다.

     

5.  **다음** 을 클릭 하 여 **인증서 시작 마법사** 페이지를 계속 진행 합니다.

6.  **사용 가능한 인증서** 화면에서 올바른 인증서를 선택 합니다.

7.  **마침**을 클릭합니다.

8.  마법사를 완료 한 후 사용 가능한 수신 대기 포트로 **RTSP** 를 지웁니다. 이렇게 하면 비보안 통신 채널을 통해 연결이 이루어지지 않습니다.

9.  **적용**을 클릭 하 고 **Microsoft 가상 응용 프로그램 서버** 서비스를 다시 시작 합니다. 서비스의 MMC 스냅인을 사용 하 여이 작업을 수행 합니다.

## 관련 항목


[Streaming Server 보안 사후 설치를 구성하는 방법](how-to-configure-streaming-server-security-post-installation.md)

[인증서 권한 문제 해결](troubleshooting-certificate-permission-issues.md)

 

 





