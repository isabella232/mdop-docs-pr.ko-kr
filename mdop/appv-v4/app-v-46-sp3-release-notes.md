---
title: App-V 4.6 SP3 릴리스 정보
description: App-V 4.6 SP3 릴리스 정보
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819793"
---
# App-V 4.6 SP3 릴리스 정보


이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.

이 릴리스 정보는 App-v (Microsoft Application Virtualization) 관리 시스템을 설치 하기 전에 자세히 읽어 보세요. 이 릴리스 정보에는 Application Virtualization (App-v) 4.6 SP3을 성공적으로 설치 하는 데 도움이 되는 정보가 포함 되어 있습니다. 이 문서에는 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 노트와 다른 App-v 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## 보안 취약점 및 바이러스 방지


보안 취약점과 바이러스 로부터 보호 하려면 설치 하는 새 소프트웨어에 대해 사용 가능한 최신 보안 업데이트를 설치 하는 것이 중요 합니다. 자세한 내용은 [Microsoft 보안 웹 사이트](https://go.microsoft.com/fwlink/?LinkId=3482) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=3482) .

## Application Virtualization 4.6 SP3의 알려진 문제점


이 섹션에서는 Microsoft App-v (Application Virtualization) 4.6 SP3과 관련 된 문제에 대 한 최신 정보를 제공 합니다. 이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다. 가능 하면 이후 릴리스에서 문제가 해결 될 것입니다.

### 가상 환경 내에서 Microsoft Windows 8.1의 인터넷 Explorer11을 사용 하 여 하이퍼링크를 열 수 없음

가상 환경에서 하이퍼링크를 열려고 하는 경우 Internet Explorer 11을 사용 하 여 Windows 8.1에서 실패 합니다. 지금 Internet Explorer 11이 기본적으로 사용 하도록 설정 된 향상 된 보호 모드 (EPM)와 함께 제공 되기 때문에,이로 인해 App-v가 필요한 레지스트리 키, 파일 및 통신 포트 개체에 액세스할 수 없습니다.

해결 방법: App-v 패키지를 열기 전에 인터넷 Explorer11에서 EPM을 사용 하지 않도록 설정 합니다. 이렇게 하면 가상 환경 내에서 Internet Explorer를 열 수 있습니다.

## 관련 항목


[Microsoft Application Virtualization 4.6 SP3 정보](about-microsoft-application-virtualization-46-sp3.md)

 

 





