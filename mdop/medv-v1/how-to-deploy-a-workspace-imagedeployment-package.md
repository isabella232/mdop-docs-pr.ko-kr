---
title: 작업 영역 이미지를 배포하는 방법
description: 작업 영역 이미지를 배포하는 방법
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827013"
---
# 작업 영역 이미지를 배포하는 방법


배포 패키지를 사용 하는 경우 다음 중 한 가지 방법으로 새 이미지를 클라이언트 컴퓨터에 배포할 수 있습니다.

-   [웹 다운로드](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [이미지 사전 준비](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [배포 패키지 내에 이미지 배포](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>웹을 통해 작업 영역 이미지를 배포 하는 방법


**웹을 통해 작업 영역 이미지를 배포 하려면**

1.  MED-V 이미지를 서버에 업로드 합니다.

    이미지 업로드에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.

2.  배포 패키지를 만들고 이미지의 위치에 대 한 서버 경로를 포함 합니다.

    배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.

3.  패키지를 최종 사용자에 게 배포 합니다.

    패키지 배포에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientdeployment-package.md)참조 하세요.

    MED-V 클라이언트는 처음 설치 및 시작 됩니다. 처음 시작 시 클라이언트는 클라이언트 설치에 지정 된 서버 주소에서 이미지를 다운로드 합니다.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>이미지 사전 준비를 사용 하 여 작업 영역 이미지를 배포 하는 방법


**이미지 사전 준비를 사용 하 여 작업 영역 이미지를 배포 하려면**

1.  이미지의 스테이지 미리 만들기 폴더를 만들고 이미지를 폴더에 밀어넣습니다.

    이미지 준비 사전 구성에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.

2.  배포 패키지를 만들고 이미지의 스테이지 준비 폴더 경로를 포함 합니다.

    배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.

3.  패키지를 최종 사용자에 게 배포 합니다.

    패키지 배포에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientdeployment-package.md)참조 하세요.

    MED-V 클라이언트는 처음 설치 및 시작 됩니다. 처음 시작 시 클라이언트는 클라이언트 설치에 지정 된 단계 전 폴더에서 이미지를 페치합니다.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a>배포 패키지를 사용 하 여 작업 영역 이미지를 배포 하는 방법


**배포 패키지를 사용 하 여 작업 영역 이미지를 배포 하려면**

1.  배포 패키지를 만들고 패키지에 이미지를 포함 합니다.

    배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.

2.  패키지를 최종 사용자에 게 배포 합니다.

    패키지 배포에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientdeployment-package.md)참조 하세요.

    패키지 설치의 일부로 이미지를 호스트로 가져옵니다.

## 관련 항목


[이미지 웹 배포 서버를 구성하는 방법](how-to-configure-the-image-web-distribution-server.md)

[배포 패키지를 구성하는 방법](how-to-configure-a-deployment-package.md)

 

 





