---
title: 보안 관리를 위한 App-V 구성
description: 보안 관리를 위한 App-V 구성
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c95fab4b2b4f402df4ff0f82f2f346c9bd226e00
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910483"
---
# <a name="configuring-app-v-for-secure-administration"></a>보안 관리를 위한 App-V 구성


관리 작업 보안이 중요한 환경에서 App-V를 사용하면 App-V 웹 관리 서비스와 App-V 관리 콘솔 간의 보안 통신을 허용합니다. 관리 서비스는 웹 기반 응용 프로그램으로, 관리 서비스를 호스팅하는 웹 서버에서 App-V 관리 서버 응용 프로그램을 보안해야 합니다. 다음 그림과 같이 이 프로세스에는 통신에 HTTPS를 사용하고 통합 인증만 허용하도록 IIS Windows 포함됩니다.

![app-v 웹 서비스 네트워크 구성.](images/appvmgmtwebservice.gif)

App-V 웹 관리 서비스는 IIS에 웹 기반 응용 프로그램으로 설치됩니다. 웹 관리 서비스가 App-V 관리 콘솔과 웹 관리 서비스 간의 보안(SSL) 연결을 지원하려면 웹 관리 서비스가 설치된 IIS 서버를 구성하고 App-V 관리 콘솔을 구성해야 합니다.

## <a name="in-this-section"></a>이 섹션의 내용


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[App-V 웹 관리 서비스를 지원하기 위해 인증서 구성](configuring-certificates-to-support-the-app-v-web-management-service.md)  
App-V 웹 관리 서비스에 대한 보안 통신을 지원하기 위해 SSL 기반 연결을 지원하기 위해 인증서를 구성하는 데 유용한 정보를 제공합니다.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
보안 연결을 사용하여 App-V Web Management Service에 연결하는 단계별 절차를 제공합니다.

 

 





