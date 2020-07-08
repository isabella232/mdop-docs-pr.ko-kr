---
title: 테스트 환경을 만드는 방법
description: 테스트 환경을 만드는 방법
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827288"
---
# 테스트 환경을 만드는 방법


다음은 엔터프라이즈 전체에 MED-V 작업 영역 패키지를 배포 하기 전에 로컬로이를 테스트 하는 데 사용할 수 있는 테스트 환경을 만드는 데 도움이 되는 몇 가지 단계와 지침입니다. 이 섹션에서는 수동 또는 전자 소프트웨어 배포 시스템을 사용 하 여 테스트 환경을 만드는 방법에 대 한 지침을 제공 합니다.

**ESD를 사용 하 여 테스트 환경을 만들려면**

1.  기업 전체에 소프트웨어를 배포 하는 회사의 방법을 사용 하 여 테스트 컴퓨터에 필요한 다음 구성 요소를 배포 합니다. 다음 순서로 설치 합니다.

    -   **Windows 가상 PC** – 아직 설치 되지 않은 경우 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    -   **Windows 가상 PC 추가 및 업데이트**-아직 설치 되지 않은 경우 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    -   **Med-v 호스트 에이전트 설치 파일** – 호스트 에이전트 (Med-v-v _HostAgent \ _Setup 설치 파일)를 설치 합니다. 자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.

    -   Med-v 작업 **영역 설치 관리자, VHD, 설치 실행 파일** – **Med-v 작업 영역 포장기**에서 생성 됩니다. 자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.

        **중요**  VHD 및 설치 실행 프로그램은 MED-V 작업 영역 설치 관리자와 같은 폴더에 있어야 합니다. 그런 다음 setup.exe를 실행 하 여 MED-V 작업 영역 설치 관리자를 설치 합니다.

         

2.  테스트 컴퓨터에 모든 구성 요소를 설치한 후에는 MED-V 호스트 에이전트를 실행 하 여 처음 설치를 시작 합니다.

    **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**, **med-v 호스트 에이전트**를 차례로 클릭 합니다.

    **참고**  테스트 컴퓨터에서 MED-V 호스트 에이전트를 실제로 실행할 수 없는 경우 다음에 컴퓨터가 다시 시작 될 때 설치가 처음으로 시작 됩니다.

     

처음 설치를 시작 하 고 완료 하는 데 10 분 정도 걸릴 수 있습니다.

처음 설치를 실행할 때 구성 설정을 테스트 하는 방법에 대 한 자세한 내용은 [최초 설치 설정을 확인 하는 방법을](how-to-verify-first-time-setup-settings.md)참조 하세요.

**테스트 환경을 수동으로 만들려면**

1.  추가 및 업데이트를 포함 하는 Windows 가상 PC와 같은 MED-V 필수 구성 요소를 포함 하는 로컬 테스트 환경에 MED-V 호스트 에이전트를 설치 합니다. 자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.

2.  MED-V 작업 영역 파일을 테스트 환경에 복사 합니다. MED-V 작업 영역 파일은 **Med-v 작업 영역 포장기**에서 지정한 대상 폴더에 있습니다.

    **중요**  VHD 및 설치 실행 프로그램은 MED-V 작업 영역 설치 관리자와 테스트 환경의 같은 폴더에 있어야 합니다.

     

3.  setup.exe를 실행 하 여 MED-V 작업 영역을 설치 합니다.

4.  MED-V 호스트 에이전트를 실행 하 여 처음 설치를 시작 합니다.

    **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**, **med-v 호스트 에이전트**를 차례로 클릭 합니다.

설치 프로그램이 시작 될 때 지정 된 VHD 크기에 따라 완료 하는 데 몇 분 정도 걸릴 수 있습니다.

이제 MED-V 작업 영역에 대해 지정한 구성, 응용 프로그램 게시 및 URL 리디렉션에 대 한 다른 설정을 테스트할 준비가 되었습니다.

**참고**  기본적으로 MED-V는 게스트의 화면 잠금 정책을 재정의 합니다. 그러나 호스트 컴퓨터에서 화면 잠금 정책을 계속 해 서 준수 하기 때문에이는 보안 문제를 일으키지 않습니다.

 

## 관련 항목


[처음 설치 설정을 확인하는 방법](how-to-verify-first-time-setup-settings.md)

[응용 프로그램 게시를 테스트하는 방법](how-to-test-application-publishing.md)

[URL 리디렉션을 테스트하는 방법](how-to-test-url-redirection.md)

 

 





