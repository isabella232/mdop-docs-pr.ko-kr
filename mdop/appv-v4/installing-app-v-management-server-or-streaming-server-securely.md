---
title: 안전하게 App-V Management Server 또는 Streaming Server 설치
description: 안전하게 App-V Management Server 또는 Streaming Server 설치
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816328"
---
# 안전하게 App-V Management Server 또는 Streaming Server 설치


이 섹션의 항목에서는 향상 된 보안 버전의 App-v 관리 서버 또는 App-v 스트리밍 서버를 설치 하는 방법에 대 한 정보를 제공 합니다.

**참고**  향상 된 보안을 사용 하도록 App-v 관리 또는 스트리밍 서버 설치 또는 구성 (예: 전송 계층 보안 또는 TLS) 하려면 x.509 V3 인증서가 App-v Server에 프로 비전 되어 있어야 합니다.

 

보안 관리 또는 스트리밍 서버를 설치 또는 구성 하려고 준비 하는 경우 다음 기술 요구 사항을 고려 하세요.

-   인증서가 유효해야 합니다. 인증서가 유효 하지 않으면 클라이언트가 연결을 종료 합니다.

-   인증서에는 올바른 EKU ( *확장 된 키 사용* ) (서버 인증 (OID 1.3.6.1.5.5.7.3.1)가 포함 되어 있어야 합니다. 인증서에이 EKU가 포함 되어 있지 않으면 클라이언트가 연결을 종료 합니다.

-   인증서의 FQDN (정규화 된 도메인 이름)이 설치 된 서버와 일치 해야 합니다. 예를 들어 클라이언트를 호출 하 `RTSPS://Myserver.mycompany.com/content/MyApp.sft` 고 인증서 **발급 대상** 필드를로 설정한 경우 `Server1.mycompany.com` 클라이언트는 서버에 연결 되지 않고 세션이 종료 됩니다. 장애가 사용자에 게 보고 됩니다.

    **참고**  네트워크 부하 분산 클러스터에서 App-v를 사용 하는 경우 RTSPS를 지원 하기 위해 San (주체 대체 이름)을 사용 하 여 인증서를 구성 해야 합니다. CA (인증 기관)를 구성 하 고 San을 사용 하 여 인증서를 만드는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=133228> 하세요.

     

-   클라이언트와 서버는 루트 CA를 신뢰 해야 하며, 서버에 연결 되는 인증서를 앱-V 서버에 발급 하는 CA를 신뢰할 수 있어야 합니다. 그렇지 않으면 클라이언트가 연결을 종료 합니다.

-   인증서의 개인 키에 대 한 사용 권한이 변경 되어 앱-V 서비스 계정이 인증서에 액세스할 수 있도록 허용 해야 합니다. 기본적으로 App-v는 네트워크 서비스 계정을 사용 하며 기본적으로 네트워크 서비스 계정에는 개인 키에 액세스할 수 있는 권한이 없으므로 보안 연결이 차단 됩니다.

## 이 섹션의 내용


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[인증서를 구성하여 보안 스트리밍 지원](configuring-certificates-to-support-secure-streaming.md)  
보안 스트리밍을 지 원하는 인증서를 가져오고, 구성 하 고, 설치 하는 방법에 대 한 정보를 제공 합니다.

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
Windows Server2003 및 Windows Server2008에서 키를 수정 하는 데 사용할 수 있는 절차를 제공 합니다.

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
네트워크 부하 분산 환경용 인증서 구성에 대 한 정보를 포함 하 여 App-v 관리 또는 스트리밍 서버의 인증서를 구성 하는 방법에 대 한 정보를 제공 합니다.

 

 





