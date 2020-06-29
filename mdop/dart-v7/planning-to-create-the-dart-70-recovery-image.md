---
title: DaRT 7.0 복구 이미지 만들기 계획
description: DaRT 7.0 복구 이미지 만들기 계획
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821333"
---
# DaRT 7.0 복구 이미지 만들기 계획


이 섹션의 정보를 사용 하 여 Microsoft 진단 및 복구 도구 모음 (DaRT) 7 복구 이미지 만들기를 계획 합니다.

## DaRT 7 복구 이미지 만들기 계획


DaRT 복구 이미지를 만들 때는 이미지에 포함할 도구를 결정 해야 합니다. 이러한 결정을 내릴 때는 최종 사용자가 다양 한 DaRT 도구에 액세스할 수 있다는 점에 유의 해야 합니다. DaRT 도구에 대 한 자세한 내용은 [dart 7.0의 도구 개요](overview-of-the-tools-in-dart-70-new-ia.md)를 참조 하세요. 보안 복구 이미지를 만드는 데 도움이 되는 방법에 대 한 자세한 내용은 [DaRT 7.0의 보안 고려 사항을](security-considerations-for-dart-70-dart-7.md)참조 하세요.

DaRT 복구 이미지를 만들 때 추가 드라이버 또는 파일을 포함할 것인지 여부도 지정 합니다. DaRT 복구 이미지에 포함 하려는 추가 드라이버 또는 파일의 위치를 확인 합니다.

## 필수 구성 요소


DaRT 복구 이미지를 만들려면 다음 항목이 필요 하거나 권장 됩니다.

-   Windows 7 원본 파일

    Windows 7 DVD 또는 Windows 7 원본 파일의 경로를 제공 해야 합니다. DaRT 복구 이미지를 만들려면 Windows 7 원본 파일이 필요 합니다.

-   플랫폼용 Windows 디버깅 도구

    Windows 디버깅 도구는 **충돌 분석기** 를 실행 하 여 컴퓨터 충돌 원인을 확인할 때 필요 합니다. DaRT 복구 이미지를 만들 때 Windows 디버깅 도구의 경로를 지정 하는 것이 좋습니다. 필요한 경우 windows [용 디버깅 도구 다운로드 및 설치](https://go.microsoft.com/fwlink/?LinkId=99934)를 참조 하 여 Windows 디버깅 도구를 다운로드할 수 있습니다.

-   선택 사항: **독립 실행형 시스템 Sweeper** 정의

    이 도구를 실행할 때 **독립 실행형 시스템 Sweeper** 에 대 한 최신 정의가 필요 합니다. **독립 실행형 시스템 Sweeper**를 실행할 때 정의를 다운로드할 수 있지만 DaRT 복구 이미지를 만들 때 최신 정의를 다운로드 하는 것이 좋습니다. 이 방법으로, 문제가 있는 컴퓨터에 네트워크 연결이 없는 경우에도 최신 정의로 도구를 실행할 수 있습니다.

-   선택 사항: **충돌 분석기** 에서 사용할 Windows 기호 파일

    일반적으로 디버깅 정보는 실행 파일과는 별도의 기호 파일에 저장 됩니다. 충돌 하는 경우와 같이 응답을 중지 한 응용 프로그램을 디버깅 하는 경우 기호 정보에 액세스할 수 있어야 합니다. 자세한 내용은 [충돌 분석기를 사용 하 여 시스템 오류 진단을](diagnosing-system-failures-with-crash-analyzer--dart-7.md)참조 하세요.

## 관련 항목


[DaRT 7.0 배포 계획](planning-to-deploy-dart-70.md)

 

 





