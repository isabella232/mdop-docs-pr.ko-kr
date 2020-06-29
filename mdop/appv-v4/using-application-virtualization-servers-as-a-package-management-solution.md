---
title: 패키지 관리 솔루션으로 Application Virtualization Server 사용
description: 패키지 관리 솔루션으로 Application Virtualization Server 사용
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815123"
---
# 패키지 관리 솔루션으로 Application Virtualization Server 사용


응용 프로그램 가상화 솔루션을 배포 하기 위해 기존 ESD 시스템을 보유 하 고 있지 않거나이를 사용 하지 않으려는 경우에는 시스템 아키텍처의 핵심으로 하나 이상의 응용 프로그램 가상화 관리 서버를 설치 해야 합니다. Application Virtualization Management Server에는 전용 서버 컴퓨터가 필요 하며 Microsoft SQL Server 데이터베이스가 필요 합니다. 데이터베이스는 같은 서버에 있거나 고속 LAN 연결을 통해 응용 프로그램 가상화 관리 서버에 액세스할 수 있는 회사 데이터베이스 서버에서 구성할 수 있습니다. 또한 앱 가상화 관리 서버 또는 지정 된 관리 워크스테이션에서 Microsoft Application Virtualization 관리 콘솔을 설치 해야 하며, 응용 프로그램 가상화 관리 서버 또는 별도의 IIS 서버에도 설치할 수 있는 Microsoft Application Virtualization 관리 웹 서비스를 설치 해야 합니다. Application virtualization 관리 콘솔은 응용 프로그램 가상화 관리 웹 서비스에 연결 하 여 시스템 관리자가 Application Virtualization 관리 서버와 상호 작용할 수 있도록 하는 데 사용 됩니다.

**참고**  응용 프로그램에 대 한 액세스는 Active Directory 도메인 서비스의 보안 그룹을 통해 제어 되므로 가상화 된 각 응용 프로그램에 대해 보안 그룹을 설정 하 고 각 그룹에 추가 되는 사용자를 관리 하는 프로세스를 계획 해야 합니다. 응용 프로그램 가상화 관리 서버 관리자는 이러한 Active Directory 그룹을 사용 하도록 서버를 구성 하 고 서버는 Active Directory 그룹 구성원을 기준으로 패키지에 대 한 액세스를 자동으로 제어 합니다.

 

## 이 섹션의 내용


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Application Virtualization 시스템 구성 요소 개요](overview-of-the-application-virtualization-system-components.md)  
Microsoft Application Virtualization 관리 시스템의 기본 구성 요소를 나열 하 고 설명 합니다.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
응용 프로그램 가상화 서버 기반 배포 시나리오에서 가상 응용 프로그램을 게시 하는 방법에 대해 간략하게 설명 합니다.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
Application virtualization 스트리밍 서버를 응용 프로그램 가상화 관리 서버 기반 구현과 함께 사용 하는 데 사용할 수 있는 옵션에 대해 설명 합니다.

## 관련 항목


[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[Application Virtualization 시스템 배포 계획](planning-for-application-virtualization-system-deployment.md)

 

 





