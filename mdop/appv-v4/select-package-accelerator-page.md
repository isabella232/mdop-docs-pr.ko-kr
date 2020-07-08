---
title: 패키지 가속기 선택 페이지
description: 패키지 가속기 선택 페이지
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815593"
---
# 패키지 가속기 선택 페이지


**패키지 가속기 선택** 페이지를 사용 하 여 새 가상 응용 프로그램 패키지를 만드는 데 사용 되는 패키지 가속기를 선택 합니다. 패키지 가속기는 App-v Sequencer를 실행 하는 컴퓨터의 폴더에 복사 해야 합니다. 자세한 내용은 [앱-v 패키지 가속기 정보 (app-v 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)를 참조 하세요.

신뢰할 수 있는 게시자의 패키지 바로 연결만 실행 합니다. 패키지 가속기에는 일반적으로 디지털 서명이 포함 되어 있습니다. 디지털 서명은 소프트웨어의 게시자를 표시 하는 데 도움이 될 수 있는 전자 보안 표시와 변환이 원래 서명 된 후 패키지가 훼손 되었는지 여부를 나타냅니다. 게시자에 의해 디지털 서명 된 변환을 사용 하는 경우 게시자가 인증 기관에서 해당 id를 확인 한 경우 해당 게시자가 변환을 생성 하 고 변경 되지 않았다는 확신을 가질 수 있습니다.

App-v Sequencer는 다음 조건 중 하나라도 충족 되는 경우 사용자에 게 알립니다.

-   선택한 변환이 디지털 서명 되어 있지 않습니다.

-   선택한 변환이 인증 기관에서 해당 id를 확인 하지 않은 게시자에 의해 서명 되었습니다.

-   디지털 서명 및 해제 된 후 선택한 변환이 변경 되었습니다.

패키지 가속기를 사용할 때 이러한 메시지가 표시 되는 경우 패키지 가속기 게시자의 웹 사이트를 방문 하 여 디지털 서명 된 버전의 변환을 얻을 수 있습니다.

이 페이지에는 다음 요소가 포함 되어 있습니다.

<a href="" id="browse"></a>**찾아보기**  
**찾아보기를** 클릭 하 여 가상 응용 프로그램 패키지를 만드는 데 사용할 패키지 가속기를 지정 합니다. Sequencer를 실행 하는 컴퓨터에 로컬로 지정 된 패키지 가속기를 저장 합니다.

## 관련 항목


[Sequencer 마법사 - 패키지 가속기(App-V 4.6 SP1)](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





