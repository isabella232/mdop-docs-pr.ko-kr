---
title: 엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포
description: 엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823628"
---
# 엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포


MED-V 클라이언트는 Microsoft System Center Configuration Manager와 같은 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 배포할 수 있습니다.

**참고**  Microsoft System Center Configuration Manager를 사용 하 여 MED-V를 설치한 경우 MED-V에 대 한 패키지를 만들 때 실행 모드를 관리 권한으로 설정 합니다.

 

엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MED-V를 배포 하기 전에 배포 준비를 위한 MED-V 이미지를 만들었는지 확인 합니다. MED-V 이미지를 만드는 방법에 대 한 자세한 내용은 [Med-v 이미지 만들기](creating-a-med-v-image.md)를 참조 하세요.

MED-V 이미지를 준비한 후에는 환경에서 이미지를 배포 하는 가장 좋은 방법을 고려해 야 합니다. 이미지는 다음 방법 중 하나로 배포할 수 있습니다.

-   웹에 업로드 되 고 웹 다운로드를 통해 배포 되며 필요에 따라 트리밍 전환 기술을 활용할 수 있습니다.

-   이미지 사전 준비를 사용 하 여 배포

## 웹을 통해 이미지 배포


웹을 통해 이미지를 배포 하는 경우에는 이미지 웹 배포 서버에 MED-V 이미지를 업로드 합니다. 이미지 웹 배포 서버를 구성 하는 방법에 대 한 자세한 내용은 [이미지 웹 배포 서버를 구성 하는 방법을](how-to-configure-the-image-web-distribution-server.md)참조 하세요. 서버에 이미지를 업로드 하는 방법에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.

## 사전 준비를 통해 이미지 배포


이미지를 미리 준비 하 여 이미지를 배포 하는 경우 단계 전 폴더를 구성 하 고 MED-V 이미지를 폴더에 밀어넣습니다. 이미지 사전 준비 구성에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.

**참고**  이미지 사전 준비를 사용 하는 경우에는 클라이언트 .msi 패키지를 푸시 하기 전에 이미지 미리 스테이지 폴더를 구성 하는 것이 중요 합니다. 폴더 경로는 클라이언트 .msi 패키지에 포함 되어야 합니다.

 

마지막으로, 엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 클라이언트 .msi 패키지를 푸시 합니다. 그런 다음 MED-V를 설치 하 고 이미지를 배포할 수 있습니다. MED-V 클라이언트 설치에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법](how-to-install-med-v-clientesds.md)을 참조 하세요. 이미지 배포에 대 한 자세한 내용은 [작업 영역 이미지를 배포 하는 방법을](how-to-deploy-a-workspace-imageesds.md)참조 하세요.

 

 





