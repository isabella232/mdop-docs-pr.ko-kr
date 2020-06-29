---
title: Application Virtualization Sequencer의 모범 사례
description: Application Virtualization Sequencer의 모범 사례
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821998"
---
# Application Virtualization Sequencer의 모범 사례


이 항목에서는 Microsoft App-v (Application Virtualization) Sequencer를 실행 하기 위한 모범 사례를 제공 합니다. 환경에서 시퀀서를 계획 하 고 사용할 때 다음과 같은 권장 사항을 검토 하 고 고려 합니다.

## 시퀀싱 컴퓨터 구성 모범 사례


App-v Sequencer를 실행 하는 컴퓨터를 구성할 때 다음과 같은 모범 사례를 고려해 야 합니다.

-   **비슷한 구성을 가지 며 대상 컴퓨터 보다 이전 버전의 운영 체제를 실행 하는 컴퓨터의 시퀀스입니다.**

    Sequencer를 실행 하는 컴퓨터가 대상 컴퓨터 보다 이전 버전의 운영 체제를 실행 하 고 있는지 확인 합니다. 여기에는 서비스 팩 및 업데이트 버전이 포함 됩니다. 예를 들어 대상 컴퓨터에서 WindowsVista 및 WindowsXP를 실행 하는 경우에는 WindowsXP를 실행 하는 컴퓨터에 응용 프로그램을 시퀀싱 해야 합니다. 한 운영 체제에서 시퀀스를 실행 하 고 다른 운영 체제에서 가상화 된 응용 프로그램을 실행할 수 있는 기능은 보장 되지 않으며 특정 응용 프로그램 및 운영 체제에 따라 달라 집니다. 문제가 발생 하는 경우 App-v 클라이언트가 실행 되는 운영 체제 환경과 동일한 환경에서 순서를 설정 해야 할 수 있습니다.

-   **여러 파티션을 사용 하 여 시퀀서를 실행 하는 컴퓨터를 구성 합니다.**

    두 개 이상의 주 파티션을 사용 하 여 시퀀서를 실행 하는 컴퓨터를 구성 해야 합니다. 첫 번째 파티션 (**C:**)은 운영 체제를 포함 해야 하며, NTFS 파일 시스템을 사용 하 여 포맷 되어야 합니다. 두 번째 파티션 (**Q:**)은 가상 응용 프로그램 설치의 대상 경로로 사용 되며 NTFS 파일 시스템을 사용 하 여 형식도 지정 해야 합니다.

-   **충분 한 디스크 공간을 사용 하 여 임시 디렉터리를 구성 합니다.**

    시퀀서는 시퀀싱 하는 동안 임시 파일을 저장 하는 데 **% TMP%** 또는 **% TEMP%** 디렉터리 및 **스크래치** 디렉터리를 사용 합니다. Sequencer를 실행 하는 컴퓨터에서 예상 되는 응용 프로그램 설치 요구 사항에 해당 하는 디스크 공간을 사용 하 여 이러한 디렉터리를 구성 해야 합니다. Sequencer 콘솔을 열고 **도구**, **옵션**을 선택한 다음 **경로** 탭을 선택 하 여 **스크래치** 디렉터리의 위치를 확인할 수 있습니다. 다른 하드 드라이브 파티션에서 임시 디렉터리 및 **스크래치** 디렉터리를 구성 하면 시퀀싱 하는 동안 성능이 향상 될 수 있습니다.

-   **Microsoft VirtualPC를 사용 하 여 응용 프로그램을 시퀀싱 합니다.**

    대부분의 응용 프로그램을 두 번 이상 시퀀싱 하 게 됩니다. 이를 쉽게 수행할 수 있도록 가상 환경에서 실행 되는 컴퓨터에서 시퀀싱을 고려해 야 합니다. 이를 통해 응용 프로그램을 시퀀싱 하 고 시퀀서를 실행 하는 컴퓨터에서 최소 재구성을 통해 깨끗 한 상태로 되돌릴 수 있습니다.

    환경에서 Microsoft Hyper-v를 실행 하는 경우 앱이 실행 되는 Hyper-v 가상 컴퓨터가 다음과 같이 실행 됩니다.

    -   일시 중지 및 다시 시작.

    -   의 상태를 저장 하 고 복원 했습니다.

    -   스냅숏으로 저장 되며 복원 됩니다.

    -   실시간 마이그레이션의 일부로 다른 하드웨어에 마이그레이션.

-   **새 응용 프로그램을 시퀀싱 하기 전에 실행 중인 다른 프로그램을 종료 합니다.**

    시퀀싱 컴퓨터에서 일반적으로 실행 되는 프로세스 및 예약 된 작업은 시퀀싱 프로세스의 속도를 늦추거나 시퀀싱 중에 관련이 없는 데이터를 수집할 수 있습니다. 시퀀싱을 시작 하기 전에 불필요 한 모든 응용 프로그램과 프로그램을 종료 해야 합니다.

-   **터미널 서비스를 실행 하는 컴퓨터의 순서**

    Sequencer를 설치 하기 전에 터미널 서비스를 실행 하는 컴퓨터에서 설치 모드를 구성 하지 않아야 합니다.

## 시퀀싱 모범 사례


새 응용 프로그램을 시퀀싱 하는 경우 다음과 같은 모범 사례를 고려해 야 합니다.

-   

    **참고**  App-v 4.6 SP1을 실행 중인 경우에는 8.3 명명 규칙을 따르는 디렉터리로 순서를 지정할 필요가 없습니다.

     

-   **8.3 명명 규칙을 따르는 고유 디렉터리에 대 한 시퀀스입니다.**

    모든 응용 프로그램을 8.3 명명 규칙을 따르는 디렉터리로 시퀀싱 해야 합니다. 지정 된 디렉터리 이름에는 8 자 보다 많은 문자를 포함할 수 없으며, 그 뒤에 3 자의 파일 이름 확장명 (예: Q:\\MYAPP.)이 있습니다. ** ABC**.

-   **하위 디렉터리가 아닌 드라이브의 루트에 있는 대상 폴더에 대 한 시퀀스입니다.**

    응용 프로그램 제품군에 여러 부분이 있는 경우 각 응용 프로그램을 주 디렉터리의 하위 디렉터리에 설치 합니다. 예를 들어 패키지에 클라이언트와 함께 응용 프로그램이 포함 된 경우 **Q:\\AppSuite** 를 주 디렉터리로 사용 하 고 기본 응용 프로그램을 **Q:\\AppSuite\\Main**로 시퀀스 하 고 클라이언트를 **Q:\\AppSuite\\Client**로 시퀀싱 합니다.

-   **설치 단계 중에 응용 프로그램을 구성 하 고 테스트 합니다.**

    응용 프로그램 설치를 완료 하는 경우 응용 프로그램 설치 프로세스에 포함 되지 않는 몇 가지 수동 단계를 수행 해야 하는 경우가 자주 있습니다. 이러한 단계에는 데이터베이스에 대 한 연결을 구성 하거나 업데이트 된 파일을 복사할 수 있는 단계가 포함 됩니다. 설치 단계 중에 이러한 구성을 수행한 다음 응용 프로그램을 실행 하 여 작동 하는지 확인 해야 합니다.

-   **필요한 경우 프로그램이 안정적이 될 때까지 응용 프로그램을 여러 번 실행 합니다.**

    설치 중에는 응용 프로그램을 여러 번 실행 하 여 연결 된 모든 등록 및 대화 상자 구성이 완료 되었는지 확인 해야 합니다. 설치 중에 응용 프로그램을 여러 번 열면 관련 응용 프로그램 기능만 **기본 기능 블록**에 로드 됩니다.

-   **응용 프로그램과 연결 된 모든 자동 업데이트 기능을 사용 하지 않도록 설정 합니다.**

    일부 응용 프로그램에서는 설치 하는 동안 최신 업데이트를 자동으로 확인할 수 있습니다. 가상 응용 프로그램 패키지의 버전 관리를 지원 하려면 시퀀싱 하는 동안이 기능을 사용 하지 않도록 설정 해야 합니다. 필수 업데이트가 있는 경우 관련 업데이트가 설치 된 새 가상 응용 프로그램 패키지를 시퀀싱 해야 합니다.

## 관련 항목


[Application Virtualization 시스템 배포 계획](planning-for-application-virtualization-system-deployment.md)

 

 




