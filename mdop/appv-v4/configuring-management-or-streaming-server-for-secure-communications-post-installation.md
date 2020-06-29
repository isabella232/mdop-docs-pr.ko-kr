---
title: 보안 통신 사후 설치를 위해 Management Server 또는 Streaming Server 구성
description: 보안 통신 사후 설치를 위해 Management Server 또는 Streaming Server 구성
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821878"
---
# 보안 통신 사후 설치를 위해 Management Server 또는 Streaming Server 구성


App-v 관리 서버나 App-v 스트리밍 서버를 설치 하기 전에 적절 한 인증서를 프로 비전 하지 않은 경우에는 초기 설치 후에 고급 보안을 위해 App-v를 구성할 수 있습니다. App-v 관리 콘솔을 통해 App-v 관리 서버를 구성할 수 있습니다. 그러나 App-v 스트리밍 서버는 레지스트리를 통해 관리 됩니다. 두 경우 모두 인증서에는 서버 인증을 위한 적절 한 EKU ( *확장 키 사용* )가 포함 되어 있어야 하 고, 네트워크 서비스에는 개인 키에 대 한 읽기 권한이 있어야 합니다.

## 이 섹션의 내용


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[관리 서버 보안 사후 설치를 구성하는 방법](how-to-configure-management-server-security-post-installation.md)  
앱-V 관리 콘솔을 사용 하 여 사전 설치를 수행 하 고, 인증서를 추가 하 고, 강화 된 보안을 위해 App-v 관리 서버를 구성할 수 있는 절차를 제공 합니다.

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[Streaming Server 보안 사후 설치를 구성하는 방법](how-to-configure-streaming-server-security-post-installation.md)  
설치 후에 인증서를 추가 하 고 앱-V 스트리밍 서버를 구성 하 여 강화 된 보안을 수행할 수 있는 절차를 제공 합니다.

<a href="" id="troubleshooting-certificate-permission-issues"></a>[인증서 권한 문제 해결](troubleshooting-certificate-permission-issues.md)  
개인 키가 네트워크 서비스의 적절 한 ACL로 구성 되지 않은 경우에 대 한 문제 해결 지침을 제공 합니다.

 

 





