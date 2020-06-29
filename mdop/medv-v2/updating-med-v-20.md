---
title: MED-V 2.0 업데이트
description: MED-V 2.0 업데이트
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823733"
---
# MED-V 2.0 업데이트


MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에 적절 한 보안 업데이트를 적용 하 여 시스템을 보호할 수 있습니다.

## 업데이트 MED-V


일반 사용자 또는 전자 소프트웨어 배포 시스템을 사용 하 여 자동으로 MED-V를 업데이트 하거나 대화형으로 업데이트할 수 있습니다. MED-V 호스트 에이전트의 설치는 MED-V 호스트 에이전트를 업그레이드 한 다음 필요한 경우 MED-V 작업 영역을 업데이트 합니다. MED-V 호스트 에이전트와 게스트 에이전트는 동기화 상태를 유지 합니다. MED-V 호스트 에이전트를 업데이트 하는 동안 MED-V 작업 영역에서 응용 프로그램을 실행 하는 경우 업데이트를 완료 하려면 호스트 컴퓨터를 다시 시작 해야 합니다. 실행 중인 응용 프로그램이 없는 경우 MED-V가 자동으로 다시 시작 되 고 호스트 컴퓨터를 다시 시작 하지 않고 업그레이드가 완료 됩니다.

전자 소프트웨어 배포 시스템을 사용 하 여 MED-V를 업데이트 하는 경우 다시 시작 동작을 제어할 수 있습니다. 이렇게 하려면 MED-V\_HostAgent\_Setup.exe를 설치할 때 명령 프롬프트에서 **REBOOT = "ReallySuppress"** 를 입력 하 여 다시 시작 하지 않도록 합니다. 그런 다음 전자 소프트웨어 배포 시스템을 구성 하 여 3010 반환 코드 (다시 시작 필요)를 캡처하여 설정 다시 시작 동작을 수행 합니다.

## 관련 항목


[MED-V에 대한 기술 참조](technical-reference-for-med-v.md)

 

 





