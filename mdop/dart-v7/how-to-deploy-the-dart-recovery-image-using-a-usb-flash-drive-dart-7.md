---
title: USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법
description: USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823668"
---
# USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법


**DaRT 복구 이미지 마법사**실행을 완료 한 후에는의 도구를 사용 하 여 <https://go.microsoft.com/fwlink/?LinkId=218888> ISO 이미지 파일을 UFD (USB 플래시 드라이브)에 복사할 수 있습니다.

이 섹션에 설명 된 단계에 따라 수동으로 ISO 이미지 파일을 UFD에 복사할 수도 있습니다.

**DaRT 복구 이미지를 USB 플래시 드라이브에 저장 하려면**

1.  USB 플래시 드라이브를 포맷 합니다.

    1.  실행 중인 유효한 운영 체제 또는 WindowsPE 세션에서 UFD를 삽입 합니다.

    2.  관리자 권한으로 명령 프롬프트에서 **DISKPART** 를 입력 하 고 **디스크 목록을**입력 합니다.

        명령 프롬프트 창에 UFD의 디스크 번호 (예: **디스크 1)** 가 표시 됩니다.

    3.  명령 프롬프트에서 다음 명령을 한 번에 하나씩 입력 합니다.

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        **참고**  앞의 코드 예제에서는 Disk1가 UFD 라고 가정 합니다. 필요한 경우 디스크 1을 디스크 번호로 바꿉니다.

         

2.  회사의 선호 하는 이미지 탑재 방법을 사용 하 여 **DaRT 복구 이미지 마법사**의 **시작 이미지 만들기** 대화 상자에서 만든 ISO 이미지 파일을 탑재 합니다. 이를 위해서는 이미지 파일을 탑재할 수 있는 메서드가 있어야 합니다.

3.  탑재 된 ISO 이미지 파일을 열고 모든 내용을 서식이 지정 된 USB 플래시 드라이브로 복사 합니다.

    **참고**  복구 이미지의 CD 또는 DVD를 구운 경우 CD 또는 DVD의 파일을 열고 콘텐츠를 UFD에 복사할 수 있습니다. 이렇게 하면 이미지를 탑재할 필요를 건너뛸 수 있습니다.

     

## 관련 항목


[DaRT 7.0 복구 이미지 배포](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





