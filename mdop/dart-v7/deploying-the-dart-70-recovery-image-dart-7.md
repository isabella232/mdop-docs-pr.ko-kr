---
title: DaRT 7.0 복구 이미지 배포
description: DaRT 7.0 복구 이미지 배포
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812657"
---
# DaRT 7.0 복구 이미지 배포


Microsoft 진단 및 복구 도구 집합 (DaRT) 7 복구 이미지가 포함 된 국제 표준화 기구 (ISO) 파일을 만든 후에는 enterprise 전체에서 DaRT 복구 이미지를 배포 하 여 최종 사용자 및 헬프데스크 상담원에 게 제공 될 수 있습니다. DaRT 복구 이미지를 배포 하는 데 사용할 수 있는 지원 되는 네 가지 메서드는 다음과 같습니다.

-   CD 또는 DVD에 ISO 이미지 파일 굽기

-   UFD (USB 플래시 드라이브)에 ISO 이미지 파일의 내용 저장

-   ISO 이미지에서 부팅 .wim 파일을 추출 하 고 최종 사용자 컴퓨터에서 사용할 수 있는 원격 파티션으로 배포 합니다.

-   ISO 이미지에서 부팅 .wim 파일을 추출 하 고 새 Windows 7 설치의 복구 파티션에 배포

**중요**  **DaRT 복구 이미지 마법사** 는 CD 또는 DVD를 구울 수 있는 옵션만 제공 합니다. 복구 이미지를 저장 하 고 배포 하는 다른 모든 방법에는 DaRT에 포함 되지 않은 도구를 포함 하는 추가 단계가 필요 합니다. 이 섹션에는 이러한 다른 메서드에 대 한 몇 가지 지침 및 링크가 나와 있습니다.

 

## USB 플래시 드라이브를 사용 하 여 DaRT 복구 이미지 배포


DaRT 복구 이미지 마법사 실행을 완료 한 후에는의 도구를 사용 하 여 <https://go.microsoft.com/fwlink/?LinkId=218888> ISO 이미지 파일을 UFD (USB 플래시 드라이브)에 복사할 수 있습니다.

[USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## DaRT 복구 이미지를 복구 파티션의 일부로 배포


DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 7 이미지의 복구 파티션으로 배포할 수 있습니다.

[복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## DaRT 복구 이미지를 원격 파티션으로 배포


DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 네트워크의 원격 파티션으로 배포할 수 있습니다.

[원격 파티션으로 DaRT 복구 이미지를 배포하는 방법](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## DaRT 복구 이미지 배포를 유지 관리 하기 위한 기타 리소스


-   [DaRT 7.0 배포](deploying-dart-70-new-ia.md)

 

 





