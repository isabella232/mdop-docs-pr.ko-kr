---
title: DaRT 7.0를 사용하여 컴퓨터 복구
description: DaRT 7.0를 사용하여 컴퓨터 복구
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822768"
---
# DaRT 7.0를 사용하여 컴퓨터 복구


Microsoft 진단 및 복구 도구 집합 (DaRT) 7을 사용 하 여 컴퓨터를 복구 하는 방법에는 두 가지가 있습니다. DaRT7 복구 이미지를 로컬로 실행 하거나 DaRT7에서 사용할 수 있는 원격 연결 기능을 사용 하 여 원격 컴퓨터를 복구할 수 있습니다. 두 방법 모두이 섹션에서 자세히 설명 합니다.

## DaRT 복구 이미지를 사용 하 여 로컬 컴퓨터 복구


DaRT7를 사용 하 여 로컬 컴퓨터를 복구 하려면 DaRT가 필요한 문제가 발생 하는 최종 사용자 컴퓨터에 실제로 설치 되어 있어야 합니다.

DaRT 복구 이미지를 배포 하는 방법에 따라 DaRT로 부팅 하는 데 선택할 수 있는 여러 가지 방법이 있습니다.

-   DaRT 복구 이미지 CD, DVD 또는 USB 플래시 드라이브를 문제 컴퓨터에 삽입 하 고 컴퓨터를 부팅 하는 데 사용 합니다.

-   문제가 있는 컴퓨터의 복구 파티션에서 DaRT로 부팅 합니다.

-   네트워크의 원격 파티션에서 DaRT로 부팅 합니다.

각 방법의 장점과 단점에 대 한 자세한 내용은 [DaRT 7.0 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)을 참조 하세요.

DaRT로 부팅 하는 데 사용 하는 방법에 관계 없이 부팅 옵션에 대 한 부팅 장치를 사용 하도록 설정 하 고 최종 사용자가 사용할 수 있도록 할 옵션을 선택 해야 합니다.

**참고**  BIOS 구성은 조직에 사용 되는 하드 디스크 드라이브, 네트워크 어댑터 및 기타 하드웨어의 종류에 따라 고유 합니다.

 

[DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## DaRT 복구 이미지를 사용 하 여 원격 컴퓨터 복구


IT 관리자는 DaRT의 Remote Connection 기능을 사용 하 여 최종 사용자 컴퓨터에서 원격으로 DaRT 도구를 실행할 수 있습니다. 최종 사용자가 특정 정보를 제공 하거나 (또는 사용자 컴퓨터에서 지원 되는 헬프데스크 전문가 인 경우) IT 관리자 또는 헬프데스크 에이전트는 최종 사용자의 컴퓨터를 제어 하 고 필요한 DaRT 도구를 원격으로 실행할 수 있습니다.

**중요**  원격 연결을 설정 하는 두 컴퓨터는 동일한 네트워크의 일부 여야 합니다.

 

**진단 및 복구 도구 집합** 창에는 관리자 컴퓨터에서 원격으로 최종 사용자 컴퓨터에 DaRT를 실행 하는 옵션이 포함 되어 있습니다. 최종 사용자는 문제 컴퓨터에서 DaRT 도구를 열고 **원격 연결**을 클릭 하 여 원격 세션을 시작 합니다.

최종 사용자 컴퓨터의 원격 연결 기능은 티켓 번호, 포트, 사용 가능한 모든 IP 주소 목록 등의 연결 정보를 만듭니다. 티켓 번호와 포트는 임의로 생성 됩니다.

IT 관리자 또는 헬프데스크 에이전트는이 정보를 **DaRT 원격 연결 뷰어에** 입력 하 여 최종 사용자 컴퓨터에 터미널 서비스 연결을 설정 합니다. 설정 된 터미널 서비스 연결을 통해 IT 관리자가 최종 사용자 컴퓨터의 DaRT 도구와 원격으로 상호 작용할 수 있습니다. 최종 사용자 컴퓨터는 연결 정보를 처리 하 고, 해당 화면을 공유 하 고, IT 관리자 컴퓨터의 지침에 응답 합니다.

[DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## DaRT7를 사용 하 여 컴퓨터를 복구 하기 위한 기타 리소스


[DaRT 7.0 작업](operations-for-dart-70-new-ia.md)

 

 





