---
title: Application Virtualization System에 대 한 계획 및 배포 가이드
description: Application Virtualization System에 대 한 계획 및 배포 가이드
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815958"
---
# Application Virtualization System에 대 한 계획 및 배포 가이드


Microsoft Application Virtualization Management는 해당 컴퓨터에 직접 응용 프로그램을 설치할 필요 없이 최종 사용자 컴퓨터에서 응용 프로그램을 사용할 수 있도록 하는 접근 권한 값을 제공 합니다. 이 작업은 *응용 프로그램 시퀀싱*이라고 하는 프로세스를 통해 가능 하며, 이렇게 하면 클라이언트 컴퓨터의 자체 자체 포함 가상 환경에서 각 응용 프로그램을 실행할 수 있습니다. 시퀀싱 된 응용 프로그램은 서로 격리 되어 응용 프로그램 충돌을 제거 하지만 여전히 클라이언트 컴퓨터와 상호 작용할 수 있습니다.

응용 프로그램 가상화 클라이언트는 응용 프로그램 가상화 시스템 구성 요소 이며, 최종 사용자가 컴퓨터에 게시 한 후 응용 프로그램과 상호 작용할 수 있습니다. 클라이언트는 각 컴퓨터에서 가상화 된 응용 프로그램이 실행 되는 가상 환경을 관리 합니다. 컴퓨터에 클라이언트를 설치한 후에는 최종 사용자가 가상 응용 프로그램을 실행할 수 있도록 *게시*라는 프로세스를 통해 컴퓨터에서 응용 프로그램을 사용할 수 있어야 합니다. 게시 프로세스는 Windows 데스크톱 또는 **시작** 메뉴에 있는 컴퓨터에 가상 응용 프로그램 아이콘과 바로 가기를 배치 하 고 패키지 정의 및 파일 형식 연결 정보를 컴퓨터에 배치 합니다. 게시는 또한 최종 사용자의 컴퓨터에서 응용 프로그램 패키지 콘텐츠를 사용할 수 있도록 합니다.

가상 응용 프로그램 패키지 콘텐츠는 요청에 따라 클라이언트로 스트림 하 고 로컬로 캐시할 수 있도록 하나 이상의 응용 프로그램 가상화 서버에 배치할 수 있습니다. 파일 서버와 웹 서버는 스트리밍 서버로도 사용할 수 있으며, 예를 들어 Microsoft 끝점 구성 관리자와 같은 전자 소프트웨어 배포 시스템을 사용 하는 경우와 같이 콘텐츠를 최종 사용자의 컴퓨터에 직접 배치할 수 있습니다. 다중 서버 구현에서 모든 스트리밍 서버에서 패키지 콘텐츠를 유지 관리 하 고 최신 상태로 유지 하려면 종합적인 패키지 관리 솔루션이 필요 합니다. 조직의 규모에 따라 전세계에 있는 최종 사용자가 액세스할 수 있는 가상 응용 프로그램이 여러 개 필요할 수 있습니다. 패키지를 관리 하 여 모든 사용자가 적절 한 응용 프로그램을 사용할 수 있도록 하는 것이 중요 한 요구 사항입니다.

응용 프로그램 가상화 계획 및 배포 가이드에서는 Microsoft 응용 프로그램 가상화 응용 프로그램 및 해당 구성 요소를 더 잘 이해 하 고 배포 하는 데 도움이 되는 정보를 제공 합니다. 또한 주요 배포 시나리오를 구현 하기 위한 단계별 절차를 제공 합니다.

## 이 섹션의 내용


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[Application Virtualization 시스템 배포 계획](planning-for-application-virtualization-system-deployment.md)  
응용 프로그램 가상화 시스템의 구현 및 배포를 계획 하는 데 필요한 지침을 제공 합니다.

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[Application Virtualization 배포 및 업그레이드 고려 사항](application-virtualization-deployment-and-upgrade-considerations.md)  
다양 한 응용 프로그램 가상화 구성 요소를 설치 하기 위한 하드웨어 및 소프트웨어 요구 사항 및 업그레이드 정보에 대 한 정보를 제공 합니다.

<a href="" id="electronic-software-distribution-based-scenario"></a>[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)  
ESD (전자 소프트웨어 배포) 시스템을 사용한 응용 프로그램 가상화 배포에 대 한 정보를 제공 합니다.

<a href="" id="application-virtualization-server-based-scenario"></a>[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)  
Application Virtualization 관리 서버를 사용 하 여 응용 프로그램 가상화를 배포 하는 방법을 설명 합니다.

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[Application Virtualization Client에 대한 독립 실행형 배달 시나리오](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
ESD 또는 서버 기반 리소스를 사용 하지 않고 독립 실행형 모드에서 응용 프로그램 가상화를 배포 하는 방법에 대해 설명 합니다.

<a href="" id="application-virtualization-reference"></a>[Application Virtualization 참조](application-virtualization-reference.md)  
시스템 구성 요소 설치 및 관리와 관련 된 자세한 기술 참조 자료가 포함 되어 있습니다.

 

 





