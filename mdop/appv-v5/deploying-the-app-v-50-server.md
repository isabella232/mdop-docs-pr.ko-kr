---
title: App-V 5.0 Server 배포
description: App-V 5.0 Server 배포
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814572"
---
# App-V 5.0 Server 배포


이 항목에서 설명 하는 다양 한 배포 구성을 사용 하 여 App-v 5.0 서버 기능을 설치할 수 있습니다. 서버 기능을 설치 하기 전에 [app-v 5.0 보안 고려](app-v-50-security-considerations.md)사항의 서버 섹션을 검토 합니다.

App-v 5.0 SP3 서버 배포에 대 한 자세한 내용은 [앱-v 5.0 sp3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3)정보를 참조 하세요.

**중요**  App-v 5.0 서버를 설치 하 고 구성 하기 전에 각 구성 요소를 호스팅할 포트를 지정 해야 합니다. 또한 들어오는 요청에 대해 지정 된 포트에 액세스할 수 있도록 연결 된 방화벽 규칙도 추가 해야 합니다. 설치 관리자가 방화벽 설정을 수정 하지 않습니다.

 

## <a href="" id="---------app-v-5-0-server-overview"></a> 앱-V 5.0 서버 개요


App-v 5.0 서버는 다섯 개의 구성 요소로 이루어집니다. 각 구성 요소는 App-v 5.0 환경에서 서로 다른 목적으로 사용 됩니다. 다음의 다섯 가지 구성 요소 각각에 대해 간략하게 설명 합니다.

-   관리 서버-App-v 5.0 인프라에 대 한 전반적인 관리 기능을 제공 합니다.

-   관리 데이터베이스 – App-v 5.0 management에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.

-   게시 서버 – 가상 응용 프로그램에 대 한 호스팅 및 스트리밍 기능을 제공 합니다.

-   보고 서버-App-v 5.0 reporting services를 제공 합니다.

-   보고 데이터베이스-App-v 5.0 reporting에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> App-v 5.0 독립 실행형 배포


App-v 5.0 독립 실행형 배포는 소규모 배포 또는 테스트 환경에 적합 한 토폴로지를 제공 합니다. 이러한 유형의 구현을 사용 하는 경우 모든 서버 구성 요소가 단일 컴퓨터에 배포 됩니다. 서비스 및 관련 데이터베이스는 App-v 5.0 구성 요소를 실행 하는 컴퓨터의 리소스에 대 한 경합을 받습니다. 따라서 대규모 배포에는이 토폴로지를 사용해 서는 안 됩니다.

[App-V 5.0 Server 배포 방법](how-to-deploy-the-app-v-50-server-50sp3.md)

[스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> App-v 5.0 서버 분산 배포


분산 배포 토폴로지는 대규모 App-v 5.0 클라이언트 기반을 지원할 수 있으며, 더 쉽게 환경을 관리 하 고 확장 확장할 수 있습니다. 이 유형의 배포를 사용 하는 경우 앱-V 5.0 서버 구성 요소는 조직의 구조 및 요구 사항에 따라 여러 컴퓨터에 배포 됩니다.

[관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법](how-to-deploy-the-app-v-50-server-using-a-script.md)

[원격 컴퓨터에 게시 서버를 설치하는 방법](how-to-install-the-publishing-server-on-a-remote-computer.md)

[독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## ESD (엔터프라이즈 소프트웨어 배포) 솔루션 및 앱-V 5.0 사용


App-v 5.0을 배포할 필요 없이 ESD를 사용 하 여 App-v 5.0 클라이언트 및 패키지를 배포할 수도 있습니다. 통합에 대 한 전체 접근 권한 값은 사용 하는 ESD에 따라 달라 집니다.

**참고**  앱-V 5.0 보고 서버 및 보고 데이터베이스는 ESD와 함께 배포 하 여 App-v 5.0 클라이언트에서 보고 데이터를 수집할 수 있습니다. 그러나 나머지 세 개의 서버 구성 요소는 ESD 기능과 충돌 하므로 배포 되어서는 안 됩니다.

 

[ESD(전자 소프트웨어 배포)를 사용하여 App-V 5.0 패키지 배포](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> 앱-V 5.0 서버 로그


App-v 5.0를 사용 하는 동안 서버 설치 및 작동 이벤트 문제를 해결 하는 데 도움이 되는 앱-V 5.0 서버 로그 정보를 사용할 수 있습니다. **이벤트 뷰어**를 사용 하 여 서버 관련 로그 정보를 검토할 수 있습니다. 다음 줄에는 서버 관련 이벤트의 특정 경로가 표시 됩니다.

**이벤트 뷰어 \ \ 응용 프로그램 및 서비스 로그 \ \ Microsoft \\ App V**

연결 된 설치 로그는 다음 디렉터리에 저장 됩니다.

**temp**

App-v 5.0 SP3에서는 일부 로그가 통합 및 이동 되었습니다. [앱-V 5.0 SP3 정보](about-app-v-50-sp3.md#bkmk-event-logs-moved)를 참조 하세요.

## <a href="" id="---------app-v-5-0-reporting"></a> 앱-V 5.0 보고


App-v 5.0 보고 기능을 사용 하면 App-v 5.0 클라이언트가 데이터를 수집 하 고 다시 전송 하 여 중앙 리포지토리에 저장 될 수 있습니다. 이 정보를 사용 하 여 조직 내에서 가상 응용 프로그램 사용 현황을 더 자세히 확인할 수 있습니다. 다음 목록에는 App-v 5.0 클라이언트가 수집 하는 일부 정보 유형이 표시 됩니다.

-   App-v 5.0 클라이언트를 실행 하는 컴퓨터에 대 한 정보입니다.

-   App-v 5.0 클라이언트를 실행 하는 특정 컴퓨터의 가상화 된 패키지에 대 한 정보입니다.

-   특정 사용자의 패키지 열기 및 종료에 대 한 정보입니다.

보고 정보는 보고 서버 데이터베이스로 성공적으로 전송 될 때까지 유지 됩니다. 데이터를 데이터베이스에 추가한 후에는 Microsoft SQL Server Reporting Services를 사용 하 여 필요한 보고서를 생성할 수 있습니다.

보고서 정보를 검색 하려면 Microsoft SQL에서 사용할 수 있는 Microsoft SSRS (SQL Server Reporting Services)를 사용 해야 합니다. App-v 5.0 reporting server를 설치할 때 SSRS가 설치 되지 않으며 연결 된 보고서를 생성 하려면 별도로 배포 해야 합니다.

[앱-V 5.0 보고에 대 한](about-app-v-50-reporting.md)자세한 내용은 다음 링크를 사용 하세요.

[PowerShell을 사용하여 App-V 5.0 Client에서 보고를 사용하도록 설정하는 방법](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## App-v 서버에 대 한 기타 리소스


[App-V 5.0 배포](deploying-app-v-50.md)






 

 





