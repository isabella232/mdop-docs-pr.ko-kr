---
title: 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법
description: 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법
author: dansimp
ms.assetid: d36213e5-7719-44d7-be65-971c3ef7df2c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 028f1dd0a1651809ec54ae19094302586d864f99
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824368"
---
# 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법


문제가 발생 하는 최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기** 를 실행 하려면 Windows 용 Microsoft 디버깅 도구와 기호 파일이 설치 되어 있어야 합니다. Windows 디버깅 도구를 다운로드 하려면 [windows 용 디버깅 도구](https://go.microsoft.com/fwlink/?LinkId=266248)를 참조 하세요.

**최종 사용자 컴퓨터에서 충돌 분석기를 실행 하려면**

1.  최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기**를 클릭 합니다.

2.  Windows 용 Microsoft 디버깅 도구에 필요한 정보를 제공 합니다.

3.  기호 파일에 필요한 정보를 제공 합니다. 기호 파일에 대 한 자세한 내용은 [충돌 분석기가 기호 파일에 액세스할 수](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)있도록 하는 방법을 참조 하세요.

4.  메모리 덤프 파일에 필요한 정보를 제공 합니다. 메모리 덤프 파일의 위치를 확인 하려면 다음을 실행 합니다.

    1.  **시스템 속성** 창을 엽니다.

    2.  **시작**을 클릭 하 고 **sysdm.cpl**를 입력 한 다음 **enter 키를**누릅니다.

    3.  **고급** 탭을 클릭합니다.

    4.  **시작 및 복구** 영역에서 **설정을**클릭 합니다.

        **시스템 속성** 창에 대 한 액세스 권한이 없으면 Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0의 **검색** 도구를 사용 하 여 최종 사용자 컴퓨터에서 덤프 파일을 검색할 수 있습니다.

    **충돌 분석기** 는 메모리 덤프 파일을 검사 하 고 문제의 예상 되는 원인을 보고 합니다. 오류에 대 한 자세한 정보 (예: 특정 메모리 덤프 메시지 및 설명, 오류 발생 시 로드 되는 드라이버, 분석의 전체 출력)를 볼 수 있습니다.

5.  적절 한 전략을 식별 하 여 문제를 해결 합니다. 전략에는 DaRT 8.0의 **컴퓨터 관리** 도구에 있는 **서비스 및 드라이버** 노드를 사용 하 여 오류를 일으킨 장치 드라이버를 사용 하지 않도록 설정 하거나 업데이트 해야 할 수 있습니다.

## 관련 항목


[크래시 분석기를 사용하여 시스템 오류 진단](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[DaRT 8.0 작업](operations-for-dart-80-dart-8.md)

 

 





