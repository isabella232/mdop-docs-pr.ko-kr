---
title: 배포 패키지를 사용하여 MED-V 작업 영역 배포
description: 배포 패키지를 사용하여 MED-V 작업 영역 배포
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823633"
---
# 배포 패키지를 사용하여 MED-V 작업 영역 배포


배포 패키지 설치는 필요한 모든 필수 구성 요소와 관리자가 미리 정의한 모든 설정과 함께 MED-V 클라이언트를 설치 하는 방법을 제공 합니다.

배포 패키지를 사용 하는 경우 패키지가 공유 네트워크 또는 이동식 미디어를 통해 배포 됩니다. 이미지는 패키지에 포함 되거나 별도로 배포 될 수 있습니다.

배포 패키지를 만들기 전에 배포 준비가 된 MED-V 이미지를 만들었는지 확인 합니다. MED-V 이미지를 만드는 방법에 대 한 자세한 내용은 [Med-v 이미지 만들기](creating-a-med-v-image.md)를 참조 하세요.

MED-V 이미지를 준비한 후에는 환경에서 이미지를 배포 하는 가장 좋은 방법을 고려해 야 합니다. 이미지는 다음 방법 중 하나로 배포할 수 있습니다.

-   웹에 업로드 되 고 웹 다운로드를 통해 배포 되며 선택적으로 트리밍 전환 기술을 사용할 수 있습니다.

-   이미지 사전 준비를 사용 하 여 배포

-   배포 패키지에 포함 되어 다른 모든 MED-V 구성 요소와 함께 배포 됩니다.

이미지가 패키지에 포함 되는 경우 이미지에 다른 구성은 필요 하지 않습니다. 이미지가 배포 패키지에 포함 되지 않을 경우 다음 중 하나를 수행 합니다.

-   웹을 통해 이미지를 배포 하는 경우에는 이미지 웹 배포 서버에 MED-V 이미지를 업로드 합니다. 이미지 웹 배포 서버를 구성 하는 방법에 대 한 자세한 내용은 [이미지 웹 배포 서버를 구성 하는 방법을](how-to-configure-the-image-web-distribution-server.md)참조 하세요. 서버에 이미지를 업로드 하는 방법에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.

-   이미지를 미리 준비 하 여 이미지를 배포 하는 경우 단계 전 폴더를 구성 하 고 MED-V 이미지를 폴더에 밀어넣습니다. 미리 준비 이미지를 구성 하는 방법에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.

**참고**  이미지 사전 준비를 사용 하는 경우 배포 패키지를 만들기 전에 이미지 미리 스테이지 폴더를 구성 하는 것이 중요 합니다. 폴더 경로를 배포 패키지에 포함 해야 합니다.

 

마지막으로 배포 패키지를 만듭니다. 배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요. 패키지가 완료 되 면 배포를 위해 배포 합니다.

배포 패키지가 배포 된 후에는 MED-V 클라이언트를 설치 하 고 이미지를 배포할 수 있습니다. MED-V 클라이언트 설치에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법](how-to-install-med-v-clientdeployment-package.md)을 참조 하세요. 이미지 배포에 대 한 자세한 내용은 [작업 영역 이미지를 배포 하는 방법을](how-to-deploy-a-workspace-imagedeployment-package.md)참조 하세요.

 

 





