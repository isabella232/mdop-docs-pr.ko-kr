---
title: 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법
description: 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823568"
---
# 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법


DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 네트워크의 원격 파티션으로 배포할 수 있습니다.

**DaRT를 원격 파티션으로 배포 하려면**

1.  DaRT ISO 이미지 파일에서 부팅 .wim 파일을 추출 합니다.

    1.  회사의 기본 이미지 탑재 방법을 사용 하 여 **시작 이미지 만들기** 대화 상자에서 만든 ISO 이미지 파일을 탑재 합니다.

    2.  ISO 이미지 파일을 열고 탑재 된 이미지의 \\sources 폴더에서 컴퓨터 또는 외부 드라이브의 위치로 부팅 .wim 파일을 복사 합니다.

        **참고**  복구 이미지의 CD 또는 DVD를 구운 경우 CD 또는 DVD의 파일을 열고 \\sources 폴더에서 boot.ini 파일을 복사할 수 있습니다. 이렇게 하면 이미지를 탑재할 필요를 건너뛸 수 있습니다.

         

2.  엔터프라이즈의 최종 사용자 컴퓨터에서 액세스할 수 있는 WDS 서버에 부팅 .wim 파일을 배포 합니다.

3.  표준 WDS 배포 절차에 따라 DaRT 용 부팅 .wim 파일을 사용 하도록 WDS 서버를 구성 합니다.

DaRT를 원격 파티션으로 배포 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.

-   [연습: PXE를 사용 하 여 이미지 배포](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [Windows 배포 서비스 시작 가이드](https://go.microsoft.com/fwlink/?LinkId=212106)

## 관련 항목


[DaRT 7.0 복구 이미지 배포](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





