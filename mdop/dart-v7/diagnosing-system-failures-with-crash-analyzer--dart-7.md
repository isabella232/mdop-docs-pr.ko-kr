---
title: 크래시 분석기를 사용하여 시스템 오류 진단
description: 크래시 분석기를 사용하여 시스템 오류 진단
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823468"
---
# 크래시 분석기를 사용하여 시스템 오류 진단


Microsoft 진단 및 복구 도구 집합 (DaRT) 7의 충돌 분석기를 사용 하 여 Windows 기반 컴퓨터에서 크래시 덤프 파일을 디버그 하 고 관련 컴퓨터 오류를 진단할 수 있습니다. 충돌 분석기는 Windows 용 Microsoft 디버깅 도구를 사용 하 여 컴퓨터에 장애가 발생 한 드라이버의 크래시 덤프 파일을 검사 합니다.

## 최종 사용자 컴퓨터에서 충돌 분석기 실행


일반적으로 문제가 있는 최종 사용자 컴퓨터의 진단 및 복구 도구 집합 창에서 충돌 분석기를 실행 합니다. 충돌 분석기는 문제 컴퓨터에서 Windows 용 디버깅 도구를 찾으려고 시도 합니다. 디렉터리 경로 대화 상자가 비어 있으면 위치를 입력 하거나 Windows 용 디버깅 도구 위치를 탐색 해야 합니다 (Microsoft에서 파일을 다운로드할 수 있음). 또한 기호 파일이 있는 위치에 대 한 경로도 제공 해야 합니다.

Windows 용 Microsoft 디버깅 도구를 포함 하 고 있으며 DaRT 복구 이미지를 만들 때 기호 파일을 추가한 경우에는 문제 컴퓨터에서 충돌 분석기를 실행할 때 사용할 수 있어야 합니다.

[최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## 최종 사용자 컴퓨터가 아닌 컴퓨터에서 독립 실행형 모드로 충돌 분석기 실행


충돌 분석기는 문제 컴퓨터에서 Windows 용 디버깅 도구를 찾으려고 시도 합니다. 디렉터리 경로 대화 상자가 비어 있으면 위치를 입력 하거나 Windows 용 디버깅 도구 위치를 탐색 해야 합니다 (Microsoft에서 파일을 다운로드할 수 있음). 또한 기호 파일이 있는 위치에 대 한 경로도 제공 해야 합니다.

DaRT 복구 이미지를 만들 때 Windows 용 Microsoft 디버깅 도구 및 기호 파일을 포함 하지 않은 경우 또는 디스크 크기 또는 네트워크 연결 문제로 인해 문제가 발생 한 경우에는 문제 컴퓨터에서 덤프 파일을 복사 하 고 독립 실행형 버전의 크래시 분석기가 설치 된 컴퓨터에서이를 분석할 수 있습니다. (예: 헬프데스크 관리자의 컴퓨터)

[최종 사용자 컴퓨터 이외의 컴퓨터에서 독립 실행형 모드로 크래시 분석기를 실행하는 방법](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## 충돌 분석기가 기호 파일에 액세스할 수 있는지 확인


일반적으로 디버깅 정보는 실행 파일과는 별도의 기호 파일에 저장 됩니다. 충돌 하는 경우와 같이 응답을 중지 한 응용 프로그램을 디버깅 하는 경우 기호 정보에 액세스할 수 있어야 합니다.

심볼 파일은 충돌 분석기를 실행할 때 자동으로 다운로드 됩니다. 컴퓨터에 인터넷 연결이 없거나 네트워크에 설치 되어 있는 컴퓨터에서 HTTP 프록시 서버에 액세스 해야 하는 경우 기호 파일을 다운로드할 수 없습니다.

[크래시 분석기가 기호 파일에 액세스할 수 있도록 하는 방법](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## 충돌 분석기를 사용 하 여 시스템 오류를 진단 하는 기타 리소스


[DaRT 7.0 작업](operations-for-dart-70-new-ia.md)

 

 





