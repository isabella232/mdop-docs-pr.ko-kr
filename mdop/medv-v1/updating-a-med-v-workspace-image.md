---
title: MED-V 작업 영역 이미지 업데이트
description: MED-V 작업 영역 이미지 업데이트
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825853"
---
# MED-V 작업 영역 이미지 업데이트


이미지는 다음 방법 중 하나로 업데이트할 수 있습니다.

-   엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 업데이트를 게스트 운영 체제에 밀어넣을 수 있습니다.

-   업데이트를 이미지 웹 배포 서버에 업로드 한 다음 클라이언트에서 다운로드 하 고 MED-V 이미지에 적용할 수 있습니다.

-   MED-V 기본 이미지는 업데이트 및 다시 배포 될 수 있습니다.

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a>엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MED-V 이미지를 업데이트 하는 방법


**엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MED-V 이미지를 업데이트 하려면**

-   사용 중인 시스템의 설명서를 참조 하세요.

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a>웹 다운로드를 사용 하 여 MED-V 이미지를 업데이트 하는 방법


**웹 다운로드를 사용 하 여 MED-V 이미지를 업데이트 하려면**

1.  MED-V 관리의 **가상 컴퓨터** 탭에서 다음 설정이 업데이트 되는 med-v 이미지와 연결 된 med-v 작업 영역 정책에 적용 되었는지 확인 합니다.

    -   **새 버전을 사용할 수 있을 때 업데이트 제안** 확인란을 선택 합니다.

    -   필요에 따라 **클라이언트가이 작업 영역의 이미지를 다운로드 하는 동안 트리밍 전송 사용** 확인란을 선택 해야 합니다.

    자세한 내용은 [Med-v 작업 영역에 가상 컴퓨터 설정을 적용 하는 방법을](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)참조 하세요.

2.  이미지 업데이트를 이미지 웹 배포 서버에 업로드 합니다.

    업데이트 해야 하는 이미지가 포함 된 모든 클라이언트는 자동으로 업데이트를 다운로드 하 여 이미지에 적용 합니다.

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a>MED-V 기본 이미지를 업데이트 하는 방법


**MED-V 기본 이미지를 업데이트 하려면**

1.  가상 PC2007에서 기존 이미지를 엽니다.

2.  이미지를 필요한 대로 변경 하 고 이미지 (예: 새 소프트웨어 설치)를 업데이트 합니다.

3.  가상 PC2007을 닫습니다.

4.  이미지를 테스트 합니다.

5.  이미지를 테스트 한 후 기존 이미지와 동일한 이름을 사용 하 여 로컬 저장소에 압축 합니다.

    **참고**  기존 버전과 다른 이름으로 이미지 이름을 지정할 경우 기존 이미지의 새 버전이 아닌 새 이미지가 생성 됩니다.

     

6.  서버에 새 버전을 업로드 하 고 이미지 준비 단계 폴더로 푸시 하거나 배포 패키지를 통해 배포 합니다.

## 관련 항목


[MED-V 이미지 만들기](creating-a-med-v-image.md)

[MED-V 이미지를 업데이트하는 방법](how-to-update-a-med-v-image.md)

[MED-V 작업 영역 정책 구성](configuring-med-v-workspace-policies.md)

[이미지 웹 배포 서버를 구성하는 방법](how-to-configure-the-image-web-distribution-server.md)

 

 





