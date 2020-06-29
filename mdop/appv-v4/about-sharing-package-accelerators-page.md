---
title: 패키지 가속기 공유 페이지 정보
description: 패키지 가속기 공유 페이지 정보
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819993"
---
# 패키지 가속기 공유 페이지 정보


다음 정보는 패키지 가속기를 공유 하는 방법에 대 한 모범 사례 정보를 제공 합니다. 패키지 가속기 파일을 공유 하려는 경우 컴퓨터 이름, 사용자 계정 정보, 변형에 포함 된 응용 프로그램에 대 한 정보 등의 정보가 패키지 가속기 파일에 포함 될 수 있습니다. 가상 응용 프로그램 패키지와 연결 된 설정 또는 구성 파일을 검토 하 여 응용 프로그램에 개인 정보가 포함 되지 않도록 해야 합니다. 이 페이지에는 다음 요소가 포함 되어 있습니다.

-   **사용자 이름**. Microsoft App-v Sequencer를 실행 하는 컴퓨터에 로그온 하는 경우 기본 제공 **관리자** 계정과 같은 일반 사용자 계정을 사용 해야 합니다. 기존 사용자 이름을 기반으로 하는 계정은 사용해 서는 안 됩니다.

-   **컴퓨터 이름**입니다. Sequencer를 실행 하는 컴퓨터의 식별 되지 않는 일반 이름을 지정 합니다.

-   **서버 URL**입니다. App-v Sequencer 콘솔의 **배포** 탭에서 서버 URL 구성 정보에 대 한 기본 설정을 사용 합니다.

-   **응용 프로그램**. 패키지 가속기를 만들 때 Sequencer를 실행 하는 컴퓨터에 설치 된 응용 프로그램 목록을 공유 하지 않으려는 경우 **appv\_manifest.xml** 파일을 삭제 해야 합니다. 이 파일은 가상 응용 프로그램 패키지의 패키지 루트 디렉터리에 있습니다.

## 관련 항목


[패키지 가속기 만들기 마법사(App-V 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

[App-V 패키지 가속기(App-V 4.6 SP1) 정보](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





