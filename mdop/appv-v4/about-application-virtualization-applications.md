---
title: Application Virtualization 응용 프로그램 정보
description: Application Virtualization 응용 프로그램 정보
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820088"
---
# Application Virtualization 응용 프로그램 정보


Application Virtualization에서 응용 *프로그램* 은 Microsoft Visio와 같은 실행 프로그램으로, 응용 프로그램 가상화 데스크톱 클라이언트 또는 이전 터미널 서비스에 대 한 원격 데스크톱 서비스에 대 한 클라이언트에는 Application Virtualization Management Server의 클라이언트로 스트리밍됩니다. 응용 프로그램을 클라이언트로 스트림할 수 있으려면 먼저 응용 프로그램 가상화 시퀀서를 사용 하 여 응용 프로그램을 처리 하 여 스트리밍을 준비 해야 합니다.

## 응용 프로그램 관리


사용자가 응용 프로그램을 사용할 수 있도록 하려면 먼저 시스템에 응용 프로그램을 추가 해야 합니다. 시스템에 응용 프로그램을 추가 하는 가장 일반적인 방법은 파일을 가져오는 것입니다. 이 기능에 액세스 하려면 응용 프로그램 가상화 서버 관리 콘솔에서 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 하 고 **응용 프로그램 가져오기를**선택 합니다.

두 개 이상의 OSD (개방형 소프트웨어 설명자) 파일을 동시에 가져오거나 여러 OSD 파일을 포함할 수 있는 Sequencer 프로젝트 파일 (SPRJ)을 가져올 수 있습니다. 이 기능을 통해 관련 응용 프로그램을 유사 하 게 구성할 수 있습니다.

다음과 같은 기능을 사용 하 여 응용 프로그램을 관리 하는 데 도움이 될 수도 있습니다.

-   **응용 프로그램 그룹**-간소화 된 관리를 위해 응용 프로그램의 논리적 그룹을 만들 수 있습니다. 그룹이 변경 되는 경우 (예: 액세스 권한) 해당 변경 내용이 그룹의 모든 응용 프로그램에 적용 됩니다. 그룹의 응용 프로그램은 다양 한 패키지에서 얻을 수 있습니다.

-   **다중 선택**-응용 프로그램 속성을 수정할 수 있도록 CTRL 키를 누른 상태로 여러 응용 프로그램을 한 번에 선택할 수 있습니다. 그러나 응용 프로그램 간의 관계를 유지 하려는 경우에는 응용 프로그램을 저장 하는 응용 프로그램 그룹을 만들어야 합니다.

-   **시스템 간 복사**-한 단계에서 동일한 버전의 app-v를 실행 하는 다른 환경으로 응용 프로그램을 복사할 수 있습니다. 예를 들어 응용 프로그램을 처음 배포 하 고 구성 하는 사용자 수용 테스트 환경이 있을 수 있습니다. 테스트 단계를 완료 한 후에는 같은 응용 프로그램 집합 (권한을 포함)을 프로덕션 환경에 복제 하는 것이 좋습니다.

## 관련 항목


[Application Virtualization 패키지 정보](about-application-virtualization-packages.md)

[Application Virtualization Server Management Console 정보](about-the-application-virtualization-server-management-console.md)

[Server Management Console에서 응용 프로그램 그룹을 관리하는 방법](how-to-manage-application-groups-in-the-server-management-console.md)

[Server Management Console에서 응용 프로그램을 관리하는 방법](how-to-manage-applications-in-the-server-management-console.md)

 

 





