---
title: 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법
description: 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823838"
---
# 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법


일반적으로, 문제가 있는 최종 사용자 컴퓨터의 진단 및 복구 도구 집합 창에서 Microsoft 진단 및 복구 도구 집합 (DaRT) 7 분석기를 실행 합니다. 충돌 분석기는 문제 컴퓨터에서 Windows 용 디버깅 도구를 찾으려고 시도 합니다. 디렉터리 경로 대화 상자가 비어 있으면 위치를 입력 하거나 Windows 용 디버깅 도구 위치를 탐색 해야 합니다 (Microsoft에서 파일을 다운로드할 수 있음). 또한 기호 파일이 있는 위치에 대 한 경로도 제공 해야 합니다.

**최종 사용자 컴퓨터에서 충돌 분석기를 열고 실행 하려면**

1.  최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기**를 클릭 합니다.

2.  다음에 대 한 필수 정보를 제공 합니다.

    -   Windows 용 Microsoft 디버깅 도구

    -   기호 파일

        기호 파일에 대 한 자세한 내용은 [충돌 분석기가 기호 파일에 액세스할 수 있도록 하는 방법](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)을 참조 하세요.

    -   크래시 덤프 파일

        다음 단계에 따라 크래시 덤프 파일의 위치를 확인 합니다.

        1.  **시스템 속성** 창을 엽니다.

            **시작**을 클릭 하 고 sysdm.cpl를 입력 한 다음 enter 키를 누릅니다.

        2.  **고급** 탭을 클릭합니다.

        3.  **시작 및 복구** 영역에서 **설정을**클릭 합니다.

        **참고**  **시스템 속성** 창에 대 한 액세스 권한이 없는 경우 DaRT의 **검색** 도구를 사용 하 여 최종 사용자 컴퓨터에서 덤프 파일을 검색할 수 있습니다.

         

3.  **충돌 분석기** 는 크래시 덤프 파일을 검사 하 고 충돌이 발생할 가능성이 있는 경우를 보고 합니다. 충돌에 대 한 자세한 내용, 특정 충돌 메시지, 설명, 충돌 시 로드 되는 드라이버, 분석의 전체 출력 등을 볼 수 있습니다.

4.  적절 한 전략을 결정 하 여 문제를 해결 합니다. 이 경우 DaRT에서 **컴퓨터 관리** 도구의 **서비스 및 드라이버** 노드를 사용 하 여 충돌을 일으킨 장치 드라이버를 사용 하지 않도록 설정 하거나 업데이트 해야 할 수 있습니다.

## 관련 항목


[크래시 분석기를 사용하여 시스템 오류 진단](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





