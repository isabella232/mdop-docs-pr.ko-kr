---
title: 크래시 분석기를 사용하여 시스템 오류 진단
description: 크래시 분석기를 사용하여 시스템 오류 진단
author: dansimp
ms.assetid: 7ebef49e-a294-4173-adb1-7e6994aa01ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d0f4b71bf267d65ec53dd1b3e23fd8a59190b0b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813108"
---
# 크래시 분석기를 사용하여 시스템 오류 진단


Microsoft 진단 및 복구 도구 집합 (DaRT) 10의 **충돌 분석기** 를 사용 하 여 Windows 기반 컴퓨터에서 메모리 덤프 파일을 디버그 하 고 관련 컴퓨터 오류를 진단할 수 있습니다. **충돌 분석기** 는 Windows 용 Microsoft 디버깅 도구를 사용 하 여 컴퓨터에 오류가 발생 한 드라이버에 대 한 메모리 덤프 파일을 검사 합니다. 최종 사용자 컴퓨터 또는 최종 사용자 컴퓨터가 아닌 컴퓨터의 독립 실행형 모드에서 충돌 분석기를 실행할 수 있습니다.

## 최종 사용자 컴퓨터에서 충돌 분석기 실행


일반적으로 문제가 발생 하는 최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기** 를 실행 합니다. **충돌 분석기** 는 문제 컴퓨터에서 Windows 용 디버깅 도구를 찾으려고 시도 합니다. 디렉터리 경로 대화 상자가 비어 있는 경우에는 위치를 입력 하거나 Windows 용 디버깅 도구 (Microsoft에서 파일을 다운로드할 수 있음)의 위치를 탐색 해야 합니다. 또한 기호 파일이 있는 위치에 대 한 경로도 제공 해야 합니다.

Windows 용 Microsoft 디버깅 도구 및 # 10 복구 이미지를 만들 때 기호 파일을 포함 한 경우에는 문제 컴퓨터에서 **충돌 분석기** 를 실행할 때 도구 및 기호 파일을 사용할 수 있어야 합니다. DaRT 복구 이미지에 포함 하지 않았거나 디스크 크기 또는 네트워크 연결 문제로 인해이를 가져올 수 없는 경우 다음 섹션에서 설명 하는 대로 최종 사용자의 컴퓨터가 아닌 다른 컴퓨터의 독립 실행형 모드에서 충돌 분석기를 실행 합니다.

[최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-10.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a>최종 사용자의 컴퓨터가 아닌 컴퓨터에서 독립 실행형 모드로 충돌 분석기 실행


일반적으로 문제가 발생 하는 최종 사용자 컴퓨터에서 **충돌 분석기** 를 실행 하지만 최종 사용자 컴퓨터가 아닌 컴퓨터에서 독립 실행형 모드의 충돌 분석기를 실행할 수도 있습니다. DaRT 복구 이미지에 Windows 디버깅 도구를 포함 하지 않았거나 디스크 크기 또는 네트워크 연결 문제로 인해 디버깅 도구를 가져오지 못하는 경우이 옵션을 선택할 수 있습니다. 이 경우 문제 컴퓨터에서 덤프 파일을 복사 하 고 지원 센터 에이전트 컴퓨터와 같이 독립 실행형 버전의 **크래시 분석기** 가 설치 된 컴퓨터에서이를 분석할 수 있습니다.

[최종 사용자 컴퓨터 이외의 컴퓨터에서 독립 실행형 모드로 크래시 분석기를 실행하는 방법](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-10.md)

## 충돌 분석기가 기호 파일에 액세스할 수 있는지 확인 하는 방법


응답을 중지 한 응용 프로그램을 디버깅 하려면 프로그램에서 분리 된 기호 파일에 대 한 액세스가 필요 합니다. 충돌 분석기를 실행할 때 기호 파일은 자동으로 다운로드 되지만, 문제가 있는 컴퓨터에서 인터넷에 액세스할 수 없는 경우도 있을 수 있습니다. 기호 파일에 대 한 액세스를 보장 하는 방법에는 여러 가지가 있습니다.

[크래시 분석기가 기호 파일에 액세스할 수 있도록 하는 방법](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md)

## 충돌 분석기를 사용 하 여 시스템 오류를 진단 하는 기타 리소스


[DaRT 10 작업](operations-for-dart-10.md)

 

 





