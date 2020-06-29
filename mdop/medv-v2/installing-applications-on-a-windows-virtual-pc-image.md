---
title: Windows 가상 PC 이미지에 응용 프로그램 설치
description: Windows 가상 PC 이미지에 응용 프로그램 설치
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826833"
---
# Windows 가상 PC 이미지에 응용 프로그램 설치


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0와 함께 사용할 Windows 가상 PC 이미지를 만든 후에는 ESD (전자 소프트웨어 배포) 시스템 및 바이러스 백신 소프트웨어와 같은 MED-V를 실행할 때 유용한 다른 구성 요소를 설치할 수 있습니다.

다음 섹션에서는 MED-V 이미지에 소프트웨어를 설치 하는 데 도움이 되는 정보를 제공 합니다.

**주의**  사항 배포 후에 MED-V 작업 영역을 관리 하려면 MED-V 이미지에 설치 하는 구성 요소의 수를 필요 하거나 MED-V를 사용할 때 도움이 되는 구성 요소를 제한 하는 것이 좋습니다. 예를 들어 MED-V를 실행할 필요는 없지만, 나중에 응용 프로그램을 MED-V 작업 영역에 설치 하 고 바이러스 백신 소프트웨어를 사용 하 여 이미지의 보안을 위해 ESD 시스템을 설치할 수 있습니다.

 

**MED-V 이미지에 소프트웨어 설치**

1.  현재 실행 중이지 않은 경우 MED-V 가상 컴퓨터를 엽니다.

    1.  **시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **windows 가상 Pc** 를 클릭 하 고 **windows 가상 pc**를 클릭 합니다.

    2.  MED-V 가상 컴퓨터를 두 번 클릭 합니다.

2.  가상 컴퓨터 운영 체제 내에서 설치할 소프트웨어의 설치 파일을 찾습니다.

3.  소프트웨어 공급 업체에서 제공 하는 설치 지침을 따릅니다.

    **참고**  설치가 완료 되 면 가상 컴퓨터를 닫았다가 다시 시작 해야 할 수 있습니다.

     

MED-V 이미지에 설치 하려는 소프트웨어 또는 응용 프로그램에 대해이 단계를 반복 합니다. 이미지에 사전 설치 하는 응용 프로그램의 수를 제한 하는 것이 좋습니다. 이미지에 응용 프로그램 및 기타 소프트웨어를 설치 하는 데 권장 되는 프로세스는 지금 ESD 시스템을 사전 설치 하 고 나중에 소프트웨어를 이미지에 배포 하는 데 사용 하는 것입니다. 또는 그룹 정책 또는 App-v를 사용 하 여 MED-V 작업 영역에서 응용 프로그램을 추가 하거나 제거할 수도 있습니다. 자세한 내용은 [Med-v 작업 영역에 배포 된 응용 프로그램 관리](managing-applications-deployed-to-med-v-workspaces.md)를 참조 하세요.

가상 이미지에 소프트웨어를 설치 하는 방법에 대 한 자세한 내용은 다음 문서를 참조 하세요.

-   [가상 응용 프로그램 게시 및 사용](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .

-   [Windows 가상 PC 도움말](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

MED-V 이미지에 원하는 모든 소프트웨어를 설치한 후 이미지를 패키지할 준비가 된 것입니다.

## 관련 항목


[MED-V에 대한 Windows 가상 PC 이미지 구성](configuring-a-windows-virtual-pc-image-for-med-v.md)

[MED-V 이미지 준비](prepare-a-med-v-image.md)

 

 





