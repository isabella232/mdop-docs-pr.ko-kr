---
title: 시간 제한 복구 이미지를 만드는 방법
description: 시간 제한 복구 이미지를 만드는 방법
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812633"
---
# 시간 제한 복구 이미지를 만드는 방법


특정 일 수만 생성 된 후에만 사용할 수 있는 DaRT 복구 이미지를 만들 수 있습니다. 이렇게 하려면 명령 프롬프트에서 **DaRT 복구 이미지 마법사** 를 실행 하 고 일 수를 지정 해야 합니다.

**시간 제한이 있는 복구 이미지를 만들려면**

1.  관리자 자격 증명을 사용 하 여 명령 프롬프트를 엽니다.

2.  디렉터리를 ERDC.exe 프로그램의 위치로 변경 합니다.

3.  다음 구문을 사용 하 여 **DaRT 복구 이미지 마법사**를 실행 합니다. *Numberofdays* 는 DaRT 복구 이미지를 사용할 수 있는 일 수를 나타내는 양의 정수입니다.

    ``` syntax
    ERDC /e NumberOfDays
    ```

## 관련 항목


[DaRT 7.0 복구 이미지 만들기](creating-the-dart-70-recovery-image-dart-7.md)

 

 





