---
title: Application Virtualization Sequencer 설치 방법
description: Application Virtualization Sequencer 설치 방법
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817308"
---
# Application Virtualization Sequencer 설치 방법


Microsoft Application Virtualization Sequencer는 응용 프로그램을 가상 응용 프로그램으로 실행할 수 있도록 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고 기록 합니다. 운영 체제만 설치 되어 있는 컴퓨터에 시퀀서를 설치 해야 합니다. 또는 가상 환경을 실행 하는 컴퓨터 (예: Microsoft 가상 PC)에 시퀀서를 설치할 수 있습니다. 이 메서드는 최소한의 추가 구성으로 재사용할 수 있는 깨끗 한 시퀀싱 환경을 유지 관리 하는 것이 더 쉽기 때문에 유용 합니다.

응용 프로그램을 시퀀싱 하는 데 사용 하는 컴퓨터에 대 한 관리자 권한이 있어야 하 고 컴퓨터가 Application Virtualization (App-v) 클라이언트 버전을 실행 하지 않아야 합니다. 시퀀서를 사용 하 여 가상 응용 프로그램을 만드는 것은 매우 많은 리소스를 필요로 하므로 권장 요구 사항을 충족 하거나 초과 하는 컴퓨터에 시퀀서를 설치 하는 것이 중요 합니다. 안전 모드에서 App-v 시퀀서를 실행 하는 것은 지원 되지 않습니다. 시스템 요구 사항에 대 한 자세한 내용은 [응용 프로그램 가상화 시스템 요구 사항을](application-virtualization-system-requirements.md)참조 하세요.

**중요**  응용 프로그램을 시퀀싱 한 후 새 응용 프로그램을 적절 하 게 시퀀싱 하려면 운영 체제와 응용 프로그램을 시퀀싱 하는 데 사용 하는 컴퓨터의 Sequencer를 다시 설치 해야 합니다.

 

**Microsoft Application Virtualization Sequencer를 설치 하려면**

1.  설치 하려는 컴퓨터에 Microsoft Application Virtualization Sequencer 설치 파일을 복사 합니다.

2.  Microsoft Application Virtualization Sequencer 설치 마법사를 시작 하려면 **setup.exe**를 선택 합니다. 설치 전에 **Microsoft Visual c + + SP1 재배포 가능 패키지 (x86)** 가 검색 되지 않으면 **setup.exe** 에서 설치 합니다.

3.  **시작** 페이지에서 **다음**을 클릭 합니다.

4.  **사용권 계약 페이지에서** 사용권 계약 조건에 동의 **하려면 동의 함을 선택 합니다**. **다음**을 클릭합니다.

5.  **대상 폴더** 페이지에서 기본 설치 폴더를 그대로 사용 하려면 **다음**을 클릭 합니다. 다른 대상 폴더를 지정 하려면 **변경을** 클릭 하 고 설치에 사용 될 설치 폴더를 지정 합니다. **다음**을 클릭합니다.

6.  **프로그램 설치 준비** 페이지에서 설치를 시작 하려면 **설치**를 클릭 합니다.

7.  **InstallShield 마법사 완료** 페이지에서 설치 마법사를 닫고 시퀀서를 열려면 **마침을**클릭 합니다. Sequencer를 열지 않고 설치 마법사를 닫으려면 **프로그램 실행** 을 선택 취소 하 고 **마침을**클릭 합니다.

## 관련 항목


[Application Virtualization Sequencer 업그레이드 방법](how-to-upgrade-the-application-virtualization-sequencer.md)

[Application Virtualization 배포 요구 사항](application-virtualization-deployment-requirements.md)

 

 





