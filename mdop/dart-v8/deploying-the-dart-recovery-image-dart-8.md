---
title: DaRT 복구 이미지 배포
description: DaRT 복구 이미지 배포
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824113"
---
# DaRT 복구 이미지 배포


Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지가 포함 된 국제 표준화 기구 (ISO) 파일을 만든 후에는 전체 엔터프라이즈에서 DaRT 8.0 복구 이미지를 배포 하 여 최종 사용자와 헬프 데스크 직원에 게 제공 됩니다. DaRT 복구 이미지를 배포 하는 데 사용할 수 있는 지원 되는 네 가지 메서드는 다음과 같습니다. 각 방법의 장점과 단점을 검토 하려면 [DaRT 8.0 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md)을 참조 하세요.

DaRT 복구 이미지 마법사를 사용 하 여 CD 또는 DVD에 ISO 이미지 파일 굽기

DaRT 복구 이미지 마법사를 사용 하 여 ISO 이미지 파일의 콘텐츠를 UFD (USB 플래시 드라이브)에 저장

ISO 이미지에서 부팅 .wim 파일을 추출 하 고 최종 사용자 컴퓨터에서 사용할 수 있는 원격 파티션으로 배포 합니다.

ISO 이미지에서 부팅 .wim 파일을 추출 하 고 새 Windows 8 설치의 복구 파티션에 배포

**중요**  **DaRT 복구 이미지 마법사** 는 이미지를 CD, DVD 또는 UFD에 굽는 옵션을 제공 하지만 복구 이미지를 저장 하 고 배포 하는 다른 방법은 DaRT에 포함 되지 않은 도구를 포함 하는 추가 단계가 필요 합니다. 이 섹션에는 이러한 다른 메서드에 대 한 몇 가지 지침 및 링크가 나와 있습니다.

 

## DaRT 복구 이미지를 복구 파티션의 일부로 배포


DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 8 이미지의 복구 파티션으로 배포할 수 있습니다.

[복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## DaRT 복구 이미지를 원격 파티션으로 배포


Windows 배포 서비스와 같은 중앙 네트워크 부팅 서버에서 복구 이미지를 호스팅하고 사용자 또는 지원 직원이 필요에 따라 컴퓨터에 이미지를 스트리밍할 수 있도록 합니다.

[원격 파티션으로 DaRT 복구 이미지를 배포하는 방법](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## DaRT 복구 이미지 배포에 대 한 기타 리소스


[DaRT 8.0 배포](deploying-dart-80-dart-8.md)

 

 





