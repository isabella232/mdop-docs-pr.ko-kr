---
title: Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법
description: Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827283"
---
# Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법


모든 MED-V 구성 요소를 windows 7에 설치 하는 것과 마찬가지로 기업 전체에 배포 하는 Windows 7 이미지에 설치할 수 있습니다. 그러면 최종 사용자가 MED-V를 시작 하도록 구성한 **시작** 메뉴 바로 가기를 클릭 하 여 med-v 작업 영역의 설치를 완료 합니다. 처음으로 설치가 시작 되 고 최종 사용자가 지침에 따라 구성을 완료 합니다.

다음 섹션에서는 Windows 7 이미지를 사용 하 여 엔터프라이즈 전체에 MED-V 작업 영역을 배포 하는 데 도움이 되는 정보와 지침을 제공 합니다.

**Windows 7 이미지에 MED-V 작업 영역을 배포 하려면**

1.  Windows 7 표준 이미지를 만듭니다. 자세한 내용은 [Windows 7의 표준 이미지 빌드: 단계별 가이드](https://go.microsoft.com/fwlink/?LinkId=204843) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  Windows 7 이미지에서 Windows 가상 PC 및 Windows 가상 PC 업데이트를 설치 합니다. 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

3.  MED-V \ _HostAgent \ _Setup 설치 파일을 사용 하 여 MED-V 호스트 에이전트를 설치 합니다. 자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.

    **경고가**  MED-V 호스트 에이전트를 설치 하기 전에 Internet Explorer를 닫아야 하며 그렇지 않으면 나중에 URL 리디렉션으로 충돌이 발생할 수 있습니다. 배포 중에 컴퓨터 다시 시작을 지정 하 여이 작업을 수행할 수도 있습니다.

     

4.  MED-V 작업 영역 패키지 파일을 Windows 7 이미지에 복사 합니다. Med-v 작업 영역 패키지 파일은 **med-v 작업 영역**설치 관리자, medv 파일, 사용자가 직접 만든 setup.exe 파일입니다.

    **중요**  Medv 및 setup.exe 파일은 MED-V 작업 영역 설치 관리자와 같은 폴더에 있어야 합니다. 그런 다음 setup.exe를 실행 하 여 MED-V 작업 영역을 설치 합니다.

     

5.  **시작** 메뉴에서 med-v 작업 영역 패키지 설치를 열기 위한 바로 가기를 구성 합니다.

    최종 사용자가 필요에 따라 MED-V 설치를 시작할 수 있도록 하는 setup.exe 파일에 대 한 **시작** 메뉴 바로 가기를 만듭니다.

6.  회사 표준 이미지 배포 프로세스를 사용 하 여 Windows 7 이미지를 MED-V가 필요한 엔터프라이즈의 컴퓨터에 배포 합니다.

최종 사용자가 MED-V 작업 영역에 게시 된 응용 프로그램에 액세스 해야 하는 경우 **시작** 메뉴 바로 가기를 클릭 하 여 med-v 작업 영역을 설치할 수 있습니다. 처음으로 설치를 시작 하 고 MED-V의 구성을 완료 합니다. 처음 설치를 완료 한 후 최종 사용자는 **시작** 메뉴의 med-v 응용 프로그램에 액세스할 수 있습니다.

## 관련 항목


[MED-V 2.0 배포 개요](med-v-20-deployment-overview.md)

[전자 소프트웨어 배포 시스템을 통해 MED-V 작업 영역을 배포하는 방법](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





