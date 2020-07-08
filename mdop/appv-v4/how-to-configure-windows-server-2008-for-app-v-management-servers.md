---
title: App-V Management Server용 Windows Server 2008을 구성 방법
description: App-V Management Server용 Windows Server 2008을 구성 방법
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817723"
---
# App-V Management Server용 Windows Server 2008을 구성 방법


Microsoft App-v (Application Virtualization) 관리 웹 서비스를 설치 하는 Windows Server 2008 서버에서 서버에 역할을 하는 IIS (인터넷 정보 서비스)를 설치 해야 합니다. Vserver 설치를 지원 하도록 Windows Server 2008를 구성 하려면 다음 절차를 사용 합니다.

**Windows Server2008 컴퓨터에 IIS를 설치 하려면**

1.  Windows Server2008 컴퓨터에서 **시작**을 클릭 하 고 **모든 프로그램**, **관리 도구**를 차례로 클릭 한 다음 **서버 관리자** 를 클릭 하 여 서버 관리자를 시작 합니다. 서버 관리자에서 **역할** 노드를 마우스 오른쪽 단추로 클릭 하 고 **역할 추가** 를 클릭 하 여 **역할 추가 마법사**를 시작 합니다.

2.  **역할 추가 마법사**의 **서버 역할 선택** 페이지에서 **웹 서버 (IIS)** 를 선택 합니다. 메시지가 표시 되 면 **필수 기능 추가** 를 클릭 하 여 종속 기능을 추가 합니다.

3.  **서버 역할 선택** 페이지에서 **다음**을 클릭 하 고 **다음** 을 다시 클릭 합니다.

4.  역할 **추가 마법사**의 **역할 서비스 선택** 페이지에서 다음을 수행 합니다.

    1.  **응용 프로그램 개발**에서 **ASP.NET** 를 선택 하 고 메시지가 표시 되 면 **필수 역할 서비스 추가** 를 클릭 하 여 종속 역할 서비스 및 기능을 추가 합니다.

    2.  **보안**에서 **Windows 인증**을 선택 합니다.

    3.  **관리 도구** 노드에서 **IIS 관리 스크립트 및 도구**를 선택 합니다. **IIS6 관리 호환성**에서 **IIS6 메타 베이스 호환성** 및 **IIS6 WMI 호환성** 이 모두 선택 되어 있는지 확인 하 고 **다음**을 클릭 합니다.

5.  **설치 선택 확인** 페이지에서 **설치**를 클릭 한 다음 마법사의 나머지 단계를 완료 합니다.

6.  **닫기를** 클릭 하 여 **역할 추가 마법사**를 종료 한 다음 서버 관리자를 닫습니다.

## 관련 항목


[Application Virtualization 배포 요구 사항](application-virtualization-deployment-requirements.md)

[Application Virtualization 배포 및 업그레이드 검사 목록](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





