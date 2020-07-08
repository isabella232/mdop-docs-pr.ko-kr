---
title: Application Virtualization Server 모니터링
description: Application Virtualization Server 모니터링
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816143"
---
# Application Virtualization Server 모니터링


App-v (Application Virtualization) 서버 관리를 간소화 하기 위해 System Center Operations Manager2007 관리 팩을 사용할 수 있습니다. 이 관리 팩은 Application Virtualization (App-v) 4.5 서버만 지원 합니다. 이전 서버 버전을 지원 하지 않습니다. 관리 팩은 app-v 클라이언트 요청을 처리 하기 위해 App-v 서버 가용성을 극대화 합니다.

## 상태 표시기


App-v 서버의 상태 표시기가 색으로 구분 됩니다. 색은 다음 상태 값을 나타냅니다.

-   색 없음은 서버가 복구할 수 없는 오류 없이 실행 되 고 있음을 나타냅니다.

-   노란색은 구성 요소 중 하나가 제대로 작동 하지 않음을 나타냅니다. 서버의 전반적인 기능이 저하 되지만 서버는 계속 사용할 수 있습니다.

-   빨간색은 서버를 사용할 수 없으며 키 서비스를 제공 하거나 외부 서비스 종속성과 통신할 수 없음을 나타냅니다.

## 모니터링 기준


관리 팩은 서버 상태의 다음 측면을 모니터링 합니다.

-   서버 상태-서버에서 예상 서비스를 제공 하 고 있는지 확인 하기 위해 서버 이벤트를 모니터링 합니다.

-   데이터 저장소 액세스 — 앱-v 데이터 저장소에 액세스 하 고 통신 하는 하나 이상의 App-v 관리 서버 기능을 추적 합니다.

-   콘텐츠 데이터 액세스-\\Content 디렉터리에 대 한 액세스를 모니터링 합니다 (로컬 디렉터리 또는 네트워크 공유 일 수 있음) 및 요청 된 파일을 읽을 수 있는 기능

-   보안-app-v 서버의 인증서 및 보안 통신을 사용 하 여 오류를 보고 합니다.

-   클라이언트 요청 처리-하나 이상의 App-v 서버가 클라이언트 요청에 대해 처리 하 고 올바르게 응답할 수 있는 능력을 모니터링 합니다. 이러한 요청에는 구성 요청, 패키지 로드 요청, 순서 없는 요청 등의 항목을 게시 하는 것이 포함 됩니다.

-   서버 구성-App-v 서버의 구성 설정을 확인 합니다. 이러한 구성 설정에는 레지스트리와 App-v 데이터 저장소의 설정이 포함 됩니다.

## 서버 차이점


App-v 관리 서버와 App-v 스트리밍 서버의 주요 차이점은 다음과 같습니다.

-   앱-V 관리 서버는 게시, 스트리밍, 관리 및 보고 서비스를 제공할 수 있습니다. 따라서 관리 팩은 패키지 스트리밍을 제공 하는 App-v 스트리밍 서버에서 관리할 수 있는 App-v 관리 서버의 많은 측면을 관리할 수 있습니다.

-   App-v 스트리밍 서버에는 App-v 데이터 저장소가 없으므로 데이터 저장소 액세스가 모니터링 되지 않습니다. App-v 스트리밍 서버에 대 한 구성 정보는 레지스트리에서 관리 합니다.

-   App-v 스트리밍 서버는 App-v 서버 관리 콘솔 인터페이스를 사용 하지 않습니다. 다른 도구를 사용 하 여 구성을 관리 합니다.

## 관련 항목


[Application Virtualization Server](application-virtualization-server.md)

 

 





