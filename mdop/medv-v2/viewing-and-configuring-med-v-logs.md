---
title: MED-V 로그 보기 및 구성
description: MED-V 로그 보기 및 구성
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823728"
---
# MED-V 로그 보기 및 구성


MED-V 문제와 문제를 해결할 때 MED-V 이벤트 로그에 액세스 하는 데 유용 하거나 필요할 수 있습니다. MED-V 관리 도구 키트를 사용 하 여 호스트 컴퓨터 및 게스트 가상 컴퓨터에 대 한 이벤트 뷰어를 열 수 있습니다. MED-V 관리 도구 키트를 사용 하 여 med-v 이벤트 로그가 MED-V 이벤트를 보고 하는 로깅 수준을 설정할 수도 있습니다.

MED-V 관리 도구 키트를 여는 방법에 대 한 자세한 내용은 [관리 도구 키트를 사용 하 여 Med-v 문제 해결](troubleshooting-med-v-by-using-the-administration-toolkit.md)을 참조 하세요.

## MED-V 이벤트 로그 보기


**Med-v 관리 툴킷** 창에서 **호스트 이벤트** 를 클릭 하 여 호스트 컴퓨터에 대 한 이벤트 뷰어를 엽니다. 또는 **게스트 이벤트** 를 클릭 하 여 게스트 가상 컴퓨터에 대 한 이벤트 뷰어를 엽니다.

이벤트 뷰어가 열리고 MED-V를 배포 하거나 관리할 때 발생할 수 있는 문제를 해결 하는 데 사용할 수 있는 해당 이벤트 로그가 표시 됩니다. 기본적으로 오류 및 경고만 표시 됩니다. 특정 이벤트 Id 및 메시지에 대 한 자세한 내용은 [Med-v 이벤트 로그 메시지](med-v-event-log-messages.md)를 참조 하세요.

**참고**  관리자 권한이 있는 경우 최종 사용자는 이벤트 로그 파일만 게스트에 저장할 수 있습니다.

 

### 호스트 컴퓨터에서 이벤트 뷰어를 수동으로 열려면

1.  **시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **관리 도구**를 클릭 합니다.

2.  **이벤트 뷰어**를 두 번 클릭 한 다음 **응용 프로그램 및 서비스 로그**를 클릭 합니다.

3.  **Medv**를 두 번 클릭 합니다.

## MED-V 이벤트 로그 구성


MED-V 관리 도구 키트에서 해당 옵션 단추를 선택 하 여 MED-V 이벤트 로깅 수준을 지정할 수 있습니다. 이벤트 로깅에서 오류, 오류, 경고, 오류, 경고 및 정보 메시지를 포함 하는지 여부를 결정할 수 있습니다. 호스트 컴퓨터와 게스트 가상 컴퓨터에 대해 지정 된 이벤트 로깅 수준이 설정 됩니다.

또한 EventLogLevel 레지스트리 값을 편집 하 여 이벤트 로깅 수준을 지정할 수도 있습니다. 자세한 내용은 [Med-v 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)를 참조 하세요.

**참고**  **Med-v 관리 도구 키트** 창에서 지정 하는 수준은 향후 med-v 이벤트 로깅에 적용 됩니다. 모든 오류, 경고 및 정보 메시지를 캡처하도록 수준을 설정 하면 이벤트 로그가 더 빠르게 채워지기 때문에 이전 이벤트가 제거 됩니다.

 

## 관련 항목


[MED-V 작업 영역을 다시 시작하고 다시 설정](restarting-and-resetting-a-med-v-workspace.md)

[MED-V 작업 영역 구성 보기](viewing-med-v-workspace-configurations.md)

 

 





