---
title: 독립 실행형 배달 시나리오 개요
description: 독립 실행형 배달 시나리오 개요
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815308"
---
# 독립 실행형 배달 시나리오 개요


독립 실행형 배달 시나리오는 낮은 대역폭 연결 또는 연결이 없는 환경에 대 한 이상적인 애플리케이션 가상화 솔루션으로, 중앙 집중식 서버의 응용 프로그램을 스트리밍할 수 있는 응용 프로그램 가상화 데스크톱 클라이언트의 기능을 제한 합니다. 이러한 환경에서는 사용자가 Windows Installer 파일을 사용 하 여 원격 및 장치 소유자가 응용 프로그램을 설치 하는 경우가 많습니다.

Application Virtualization Sequencer를 사용 하 여 Windows Installer 파일을 포함 하는 시퀀싱 된 응용 프로그램을 만들 수 있습니다. 이러한 패키지에는 가상화 된 응용 프로그램, 게시 정보, 그리고 클라이언트 시스템에 패키지를 설치 하는 데 필요한 설치 관리자 루틴이 포함 됩니다. 설치 관리자가 가상 응용 프로그램 패키지를 Microsoft Application Virtualization 데스크톱 클라이언트에 추가 합니다. 게시 정보는 WAN을 통해 스트리밍 하는 대신 로컬 위치에서 응용 프로그램을 로드 하도록 구성 됩니다. 사용자는 일시적으로 네트워크에 연결 하 여 Windows Installer 파일을 검색 하거나 DVD에서 실행할 수 있습니다.

독립형 배달 시나리오는 사용자에 게 다음과 같은 이점을 제공 합니다.

-   간단한 배포 작업.

-   런타임에는 네트워크 및 서버가 필요 하지 않습니다.

-   사전 캐시 되어 모든 사용자가 사용할 수 있는 응용 프로그램

독립 실행형 배달 시나리오에는 다음과 같은 제한 사항이 있습니다.

-   기본 제공, 자동화 된 보고 기능을 사용할 수 없습니다. 외부 보고 도구를 사용 하 여 보고서를 생성 해야 합니다.

-   응용 프로그램은 원본 Windows Installer 파일과 같이 수동으로 클라이언트에 전달 해야 합니다.

## 관련 항목


[Application Virtualization Client를 수동으로 설치하는 방법](how-to-manually-install-the-application-virtualization-client.md)

[클라이언트에 가상 응용 프로그램을 게시하는 방법](how-to-publish-a-virtual-application-on-the-client.md)

 

 





