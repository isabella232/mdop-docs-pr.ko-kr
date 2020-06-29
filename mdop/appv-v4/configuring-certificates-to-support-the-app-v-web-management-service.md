---
title: App-V 웹 관리 서비스를 지원하기 위해 인증서 구성
description: App-V 웹 관리 서비스를 지원하기 위해 인증서 구성
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821888"
---
# App-V 웹 관리 서비스를 지원하기 위해 인증서 구성


보안 통신을 위해 SSL 기반 연결을 지원 하도록 App-v 웹 관리 서비스를 구성 해야 합니다. 이 프로세스를 실행 하려면 관리 서비스를 설치 하는 웹 서버 또는 컴퓨터에 서비스 또는 컴퓨터에 대 한 인증서가 발급 되어 있어야 합니다.

다음 시나리오는이 용도로 인증서를 가져오는 방법을 보여 줍니다.

1.  회사 인프라에는 컴퓨터에 자동으로 인증서를 발급 하는 PKI (공개 키 인프라)가 이미 있습니다.

2.  회사 인프라는 이미 PKI를 보유 하 고 있지만, 컴퓨터에 자동으로 인증서를 발급 하지는 않습니다.

3.  회사 인프라에는 현재 PKI가 없습니다.

앞의 각 시나리오에서 인증서를 가져오는 방법은 서로 다르지만 결과는 동일 합니다. 관리자는 IIS 기본 웹 사이트에 인증서를 할당 하 고 보안 통신을 요구 하도록 App-v 웹 관리 서비스를 구성 해야 합니다.

**중요**  인증서 이름은 서버 이름과 일치 해야 합니다. 인증서의 일반 이름에 Fqdn (정규화 된 도메인 이름)을 사용 하는 것이 가장 좋습니다.

 

앱-V는 IIS 서버를 사용 하 여 다른 인프라 구성을 지원할 수 있습니다. HTTPS를 지원 하도록 IIS 서버를 구성 하는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=151972> 하세요.

## 관련 항목


[더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





