---
title: 패키지를 병렬 실행하는 방법
description: 패키지를 병렬 실행하는 방법
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818128"
---
# 패키지를 병렬 실행하는 방법


이 절차를 사용 하 여 원래 시퀀싱 된 응용 프로그램 패키지와 함께 실행할 수 있도록 기존 시퀀싱 된 응용 프로그램 패키지를 수정 합니다. 이 프로세스를 분기 라고 합니다. 가상 응용 프로그램 패키지를 분기할 때 동일한 패키지의 두 버전을 실행할 수 있습니다. 예를 들어 기존 패키지에 서비스 팩을 적용 하 고 원래 시퀀싱 된 가상 응용 프로그램 패키지를 사용 하 여이를 나란히 실행할 수 있습니다.

다음 절차를 사용 하 여 시퀀싱 된 가상 응용 프로그램 패키지를 분기할 수 있습니다.

**시퀀싱 된 가상 응용 프로그램 패키지를 분기 하려면**

1.  Microsoft Application Virtualization (App-v) Sequencer를 엽니다. 분기할 **파일**선택 (sprj)을 포함 하는 대상 디렉터리를 지정 하려면 **열기를 엽니다**.

2.  분기할 시퀀싱 된 응용 프로그램이 포함 된 디렉터리로 이동 하 고 **열기**를 클릭 합니다.

3.  패키지 복사본을 저장 하려면 App-v Sequencer에서 **파일**, **다른 이름으로 저장**을 선택 합니다. 고유한 새 이름을 지정 하 고 패키지 복사본에 대해 고유한 새 패키지 루트 디렉터리를 지정 합니다. **Save**을 클릭합니다.

    **중요**  
    새 패키지 이름을 지정 하거나 기존 버전의 패키지를 덮어써야 합니다.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. 새 버전을 저장 한 후에는 필요한 구성 변경 내용을 적용 하 고 연결 된 .ICO, OSD, SFT 및 SPRJ 파일을 Application Virtualization (App-v) 서버의 위치에 맞게 저장할 수 있습니다.

## 관련 항목


[Application Virtualization Sequencer에 대한 작업](tasks-for-the-application-virtualization-sequencer.md)









