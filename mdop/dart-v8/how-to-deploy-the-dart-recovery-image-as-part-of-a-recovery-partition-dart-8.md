---
title: 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법
description: 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824383"
---
# 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법


Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지 마법사 실행을 완료 하 고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 8 이미지에 복구 파티션으로 배포할 수 있습니다. Windows 운영 체제를 시작 하는 것을 방지 하는 손상 문제로 인해 복구 이미지가 시작 되지 않는 등 파티션을 설정 하는 것이 좋습니다. 또한 별도의 파티션을 통해 BitLocker 복구 키를 두 번 제공할 필요가 없어집니다. 사용자가 파일을 저장할 수 없도록 파티션을 숨기는 것이 좋습니다.

**Windows 8 이미지의 복구 파티션에 DaRT를 배포 하려면**

1.  **DaRT 8.0 복구 이미지 마법사**를 사용 하 여 만든 ISO 이미지 파일의 크기 보다 크거나 같은 Windows 8 이미지에 대상 파티션을 만듭니다.

    DaRT 파티션에 필요한 최소 크기는 DaRT의 원격 연결 기능을 수용 하는 500MB입니다.

2.  DaRT ISO 이미지 파일에서 부팅 .wim 파일을 추출 합니다.

    1.  회사의 선호 하는 방법을 사용 하 여 **시작 이미지 만들기** 페이지에서 만든 ISO 이미지 파일을 탑재 합니다.

    2.  ISO 이미지 파일을 열고 탑재 된 이미지의 \\sources 폴더에서 컴퓨터 또는 외부 드라이브의 위치로 부팅 .wim 파일을 복사 합니다.

        **참고**  복구 이미지의 CD, DVD 또는 USB를 구운 경우 이동식 미디어에서 파일을 열고 \\sources 폴더에서 boot.ini 파일을 복사할 수 있습니다. 부팅 .wim 파일을 복사 하는 경우 이미지를 탑재할 필요가 없습니다.

         

3.  Boot.ini 파일을 사용 하 여 사용자 지정 Windows RE 이미지 만들기에 대 한 회사의 표준 방법을 사용 하 여 부팅 가능한 복구 파티션을 만듭니다.

    복구 파티션을 만들거나 사용자 지정 하는 방법에 대 한 자세한 내용은 [WINDOWS RE 환경 사용자 지정](https://go.microsoft.com/fwlink/?LinkId=214222)을 참조 하세요.

4.  Windows 8 이미지의 대상 파티션을 복구 파티션으로 바꿉니다.

    시스템 실패가 발생 하는 경우에 복구 솔루션을 배포 하 여 공장 이미지를 다시 설치 하는 방법에 대 한 자세한 내용은 [시스템 복구 이미지 배포](https://go.microsoft.com/fwlink/?LinkId=214221)를 참조 하세요.

## 관련 항목


[DaRT 8.0 복구 이미지 만들기](creating-the-dart-80-recovery-image-dart-8.md)

[DaRT 복구 이미지 배포](deploying-the-dart-recovery-image-dart-8.md)

[DaRT 8.0 계획](planning-for-dart-80-dart-8.md)

 

 





