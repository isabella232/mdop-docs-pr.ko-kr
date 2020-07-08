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
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816268"
---
# Application Virtualization 보안 가이드 소개


이 Microsoft App-v (Application Virtualization) 보안 가이드는 App-v 배포를 위해 선택한 보안 기능을 구성 하는 관리자를 위한 지침을 제공 합니다.

**참고**  이 설명서에서는 특정 보안 옵션 선택에 대 한 지침을 제공 하지 않습니다. 이 정보는에 있는 App-v 보안 모범 사례 백서에서 제공 됩니다 <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

이 가이드를 사용 하는 App-v 관리자는 다음 보안 관련 기술에 대해 잘 알고 있어야 합니다.

-   Active Directory Domain Services

-   PKI (공개 키 인프라)

-   IPsec (인터넷 프로토콜 보안)

-   그룹 정책

-   IIS (인터넷 정보 서비스)

## 앱-V 인프라 구성 요소


향상 된 보안 App-v 환경을 계획할 때 여러 다른 인프라 모델을 고려할 수 있습니다.

**참고**  앱-V 인프라 모델에 대 한 자세한 내용은 다음 문서를 참조 하세요.

-   [App-v 계획 및 배포 가이드](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [인프라 계획 및 디자인 가이드 시리즈](https://go.microsoft.com/fwlink/?LinkId=151986)

 

이러한 모델은 다음 그림에 표시 된 것과는 다른 일부 App-v 구성 요소를 활용 합니다.

![앱-v 분기 office 다이어그램](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Application Virtualization (App-v) 관리 서버  
앱-V 관리 서버는 패키지 콘텐츠를 스트리밍하 고 바로 가기 키와 파일 형식 연결을 App-v 클라이언트에 게시 합니다. 또한 App-v 관리 서버는 활성 업그레이드, 라이선스 관리 및 보고에 사용할 수 있는 데이터베이스를 지원 합니다.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Application Virtualization (App-v) 스트리밍 서버  
App-v 스트리밍 서버는 App-v 관리 서버 연결의 대역폭이 클라이언트에 게 패키지 콘텐츠를 스트리밍하는 데 충분 하지 않은 지점 등의 환경에서 App-v 클라이언트로 스트리밍할 패키지를 호스팅합니다. 스트리밍 서버는 스트리밍 기능만 포함 하며 app-v 관리 콘솔 또는 App-v 관리 웹 서비스를 제공 하지 않습니다.

<a href="" id="application-virtualization--app-v--data-store"></a>App-v (Application Virtualization) 데이터 저장소  
SQL 데이터베이스의 App-v 데이터 저장소는 App-v 인프라와 관련 된 정보를 유지 합니다. App-v 데이터 저장소의 정보에는 모든 응용 프로그램 레코드, 응용 프로그램 할당, 응용 프로그램 가상화 환경을 관리 하는 그룹이 포함 됩니다.

<a href="" id="application-virtualization--app-v--management-service"></a>Application Virtualization (App-v) 관리 서비스  
App-v 관리 서비스는 Application Virtualization data store에 대 한 읽기/쓰기 요청을 전달 합니다. 이 구성 요소는 App-v 관리 서버와 같은 컴퓨터 또는 IIS가 설치 된 별도의 컴퓨터에 설치할 수 있습니다.

<a href="" id="application-virtualization--app-v--management-console"></a>App-v (Application Virtualization) 관리 콘솔  
App-v 관리 콘솔은 App-v 서버 관리용 스냅인 관리 유틸리티입니다. 이 구성 요소는 App-v 서버와 같은 컴퓨터 또는 MMC 3.0 및이 있는 별도의 워크스테이션에 설치할 수 있습니다. NET 2.0이 설치 되어 있습니다.

<a href="" id="application-virtualization--app-v--sequencer"></a>Application Virtualization (App-v) Sequencer  
App-v 시퀀서는 응용 프로그램 설치를 모니터링 하 고 캡처하여 가상 응용 프로그램 패키지를 만듭니다. 시퀀서의 출력은 응용 프로그램 아이콘, 응용 프로그램 정의 정보를 포함 하는 OSD 파일, 패키지 매니페스트 파일, 응용 프로그램의 콘텐츠 파일을 포함 하는 SFT 파일 등으로 구성 됩니다. 선택적으로, App-v 인프라를 사용 하지 않고 패키지를 설치 하기 위해 Windows Installer 파일을 만들 수 있습니다.

<a href="" id="application-virtualization--app-v--client"></a>Application Virtualization (App-v) 클라이언트  
App-v 클라이언트가 App-v 데스크톱 클라이언트 컴퓨터 또는 App-v 터미널 서비스 클라이언트 컴퓨터에 설치 되어 있습니다. 가상 응용 프로그램 패키지에 대 한 가상 환경을 제공 합니다. App-v 클라이언트는 캐시 스트리밍, 가상 응용 프로그램 게시 새로 고침, 응용 프로그램 가상화 서버와의 상호 작용에 대 한 패키지 스트리밍을 관리 합니다.

 

 





