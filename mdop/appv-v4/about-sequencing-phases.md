---
title: 시퀀싱 단계 정보
description: 시퀀싱 단계 정보
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820003"
---
# 시퀀싱 단계 정보


시퀀싱은 Microsoft Application Virtualization (App-v) Sequencer를 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 만드는 프로세스입니다. 시퀀싱 하는 동안 Sequencer는 응용 프로그램의 모든 설치 및 설정 프로세스를 모니터링 하 고 기록 하 고, .ICO, OSD, SFT, SPRJ 파일을 만듭니다. 이러한 파일에는 응용 프로그램에 대 한 필요한 모든 정보가 포함 되어 있으며, 해당 응용 프로그램을 가상 환경에서 실행할 수 있습니다.

응용 프로그램을 시퀀싱 하 고 가상 응용 프로그램 패키지를 만드는 네 가지 단계는 설치, 시작, 사용자 지정 및 저장입니다. 다음 목록에서는 각 단계에 대 한 정보를 제공 합니다.

1.  **설치 단계**-설치 단계에서는 패키지 이름 및 해당 패키지와 연결 되는 선택적 관련 설명을 지정 합니다. 이 단계 중에 고급 모니터링 옵션을 구성할 수도 있습니다. 고급 모니터링 옵션에는 블록 크기와 모니터링 중에 자동 업데이트를 설치할지 여부를 지정 하는이 포함 됩니다. 시퀀서는 가상 응용 프로그램 패키지를 만드는 데 필요한 모든 정보와 구성을 기록 하 고 연결 된 파일 및 레지스트리 설정에 대해 설명 합니다.

    **중요**  고급 옵션을 보려면 **패키지 정보** 페이지에서 **고급 모니터링 옵션 표시** 를 선택 합니다.

     

2.  **시작 단계**-시작 단계 중에는 패키지를 사용 하 여 구성 해야 하는 필수 파일 연결 및 보안 설명자를 지정할 수 있습니다. 응용 프로그램의 기능과 안정성을 위해 필요한 횟수 만큼 응용 프로그램을 열어야 합니다.

3.  **사용자 지정 단계**-사용자 지정 단계에서는 연결 된 .osd 파일을 사용 하 여 패키지를 구성할 수 있습니다. 가상 환경 내부 또는 외부에서 관련 스크립트를 실행할지 여부를 지정 하 고, 수행할 추가 작업을 지정 하 고, 연결 된 스크립트를 동기적 또는 비동기적으로 실행 하는 방법을 지정 하 고, 사용자 컨텍스트에서 실행할 추가 스크립트를 지정할 수 있습니다.

4.  **저장 단계**-저장 단계에서 가상 응용 프로그램 패키지에 필요한 모든 파일이 생성 됩니다. 생성 되는 파일은 sprj, sft, .osd, .ico, .xml 매니페스트 및 Windows installer (.msi) 파일입니다.

## 관련 항목


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





