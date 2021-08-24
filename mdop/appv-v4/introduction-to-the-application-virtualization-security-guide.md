---
title: Application Virtualization 보안 가이드 소개
description: Application Virtualization 보안 가이드 소개
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 82914de48a5a5777f6ce4b50fe3e8af34dd82494
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910783"
---
# <a name="introduction-to-the-application-virtualization-security-guide"></a>Application Virtualization 보안 가이드 소개


이 Microsoft App-V(Application Virtualization) 보안 가이드에서는 App-V 배포에 대해 선택된 보안 기능을 구성하는 관리자를 위한 지침을 제공합니다.

**참고**  
이 설명서에서는 특정 보안 옵션을 선택하는 방법에 대한 지침을 제공하지 않습니다. 이 정보는 에서 사용할 수 있는 App-V 보안 모범 사례 백서에 <https://go.microsoft.com/fwlink/?LinkId=127120> 제공됩니다.

 

이 가이드를 사용하는 App-V 관리자는 다음과 같은 보안 관련 기술에 익숙해야 합니다.

-   Active Directory Domain Services

-   PKI(공개 키 인프라)

-   IPsec(인터넷 프로토콜 보안)

-   그룹 정책

-   인터넷 정보 서비스(IIS)

## <a name="app-v-infrastructure-components"></a>APP-V 인프라 구성 요소


향상된 보안 App-V 환경을 계획할 때 여러 가지 인프라 모델을 고려할 수 있습니다.

**참고**  
App-V 인프라 모델에 대한 자세한 내용은 다음 설명서를 참조하십시오.

-   [App-V 계획 및 배포 가이드](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [인프라 계획 및 디자인 가이드 시리즈](https://go.microsoft.com/fwlink/?LinkId=151986)

 

이러한 모델은 다음 그림에 설명된 App-V 구성 요소 중 일부만 활용합니다.

![app-v 지점 다이어그램.](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>App-V(Application Virtualization) 관리 서버  
App-V 관리 서버는 패키지 콘텐츠를 스트리밍하고 바로 가기 및 파일 형식 연결과 App-V 클라이언트를 게시합니다. App-V 관리 서버는 또한 보고에 사용할 수 있는 활성 업그레이드, 라이선스 관리 및 데이터베이스를 지원합니다.

<a href="" id="application-virtualization--app-v--streaming-server"></a>App-V(Application Virtualization) 스트리밍 서버  
App-V 스트리밍 서버는 App-V 관리 서버에 대한 연결 대역폭이 클라이언트에 대한 스트리밍 패키지 콘텐츠에 부족한 지점과 같은 환경에서 App-V 클라이언트로 스트리밍하기 위한 패키지를 호스트합니다. 스트리밍 서버는 스트리밍 기능만 포함하며 App-V 관리 콘솔 또는 App-V 관리 웹 서비스를 제공하지 않습니다.

<a href="" id="application-virtualization--app-v--data-store"></a>App-V(Application Virtualization) 데이터 저장소  
App-V 데이터 저장소는 SQL App-V 인프라와 관련된 정보를 보존합니다. App-V 데이터 저장소의 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 할당 및 Application Virtualization 환경을 관리하는 그룹이 포함됩니다.

<a href="" id="application-virtualization--app-v--management-service"></a>App-V(Application Virtualization) 관리 서비스  
App-V 관리 서비스는 응용 프로그램 가상화 데이터 저장소에 읽기/쓰기 요청을 전달합니다. 이 구성 요소는 App-V 관리 서버와 동일한 컴퓨터 또는 IIS가 설치된 별도의 컴퓨터에 설치할 수 있습니다.

<a href="" id="application-virtualization--app-v--management-console"></a>App-V(Application Virtualization) 관리 콘솔  
App-V 관리 콘솔은 App-V Server 관리를 위한 스냅인 관리 유틸리티입니다. 이 구성 요소는 App-V Server와 동일한 컴퓨터 또는 MMC 3.0 및 .NET 2.0이 설치된 별도의 Workstation에 설치할 수 있습니다.

<a href="" id="application-virtualization--app-v--sequencer"></a>App-V(Application Virtualization) Sequencer  
App-V Sequencer는 응용 프로그램 설치를 모니터링하고 캡처하고 가상 응용 프로그램 패키지를 만듭니다. Sequencer의 출력은 응용 프로그램 아이콘, 응용 프로그램 정의 정보가 포함된 OSD 파일, 패키지 매니페스트 파일 및 응용 프로그램의 콘텐츠 파일이 포함된 SFT 파일로 구성됩니다. 선택적으로 app-Windows 사용하지 않고 패키지를 설치하기 위해 설치 관리자 파일을 만들 수 있습니다.

<a href="" id="application-virtualization--app-v--client"></a>App-V(Application Virtualization) 클라이언트  
App-V 클라이언트는 App-V 데스크톱 클라이언트 컴퓨터 또는 App-V 터미널 서비스 클라이언트 컴퓨터에 설치됩니다. 가상 응용 프로그램 패키지에 대한 가상 환경을 제공합니다. App-V 클라이언트는 캐시에 대한 패키지 스트리밍, 가상 응용 프로그램 게시 새로 고침 및 Application Virtualization Server와의 상호 작용을 관리합니다.

 

 





