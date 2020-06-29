---
title: Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법
description: Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817028"
---
# Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법


더 안전한 App-v 설치를 지원 하려면 다음 절차를 사용 하 여 Windows Server2003 또는 Windows Server2008에서 개인 키를 수정할 수 있습니다. 개인 키의 사용 권한을 수정 하려면 Windows Server2003 리소스 키트 도구를 사용 하면 `WinHttpCertCfg.exe` 됩니다.

Windows Server2003의 경우이 절차를 수행 하려면이 문서에 나열 된 필수 구성 요소를 충족 하는 인증서가 App-v 관리 또는 스트리밍 서버를 설치 하려는 컴퓨터에 설치 되어 있어야 합니다. 도구 사용에 대 한 추가 정보 `WinHttpCertCfg.exe` 는에서 확인할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=151981> .

Windows Server2008에서 개인 키의 Acl을 변경 하는 프로세스는 훨씬 간단 합니다. 인증서의 사용자 인터페이스를 사용 하 여 개인 키 사용 권한을 관리할 수 있습니다.

**참고**  기본 보안 컨텍스트는 네트워크 서비스입니다. 그러나 도메인 계정은 대신 사용할 수 있습니다.

 

**Windows Server2003에서 개인 키를 관리 하려면**

1.  앱-V 관리 또는 스트리밍 서버가 되는 컴퓨터에서 명령 프롬프트에 다음 명령을 입력 하 여 특정 인증서에 할당 된 현재 사용 권한을 나열 합니다.

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  필요한 경우 관리 또는 스트리밍 서비스에 사용 되는 보안 컨텍스트에 대 한 읽기 권한을 제공 하도록 인증서의 사용 권한을 수정 합니다.

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  인증서에 대 한 사용 권한을 나열 하 여 보안 컨텍스트가 적절 하 게 추가 되었는지 확인 합니다.

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**Windows Server2008에서 개인 키를 관리 하려면**

1.  *로컬 컴퓨터* 인증서 저장소를 대상으로 하는 *인증서* 스냅인을 사용 하 여 MMC (Microsoft Management Console)를 만듭니다.

2.  MMC를 확장 하 고 **개인 키 관리**를 선택 합니다.

3.  **보안** 탭에서 **읽기** 권한이 있는 **네트워크 서비스** 계정을 추가 합니다.

## 관련 항목


[인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[인증서를 구성하여 보안 스트리밍 지원](configuring-certificates-to-support-secure-streaming.md)

 

 





