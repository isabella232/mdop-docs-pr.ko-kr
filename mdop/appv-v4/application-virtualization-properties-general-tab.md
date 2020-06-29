---
title: 응용 프로그램 가상화 속성 일반 탭
description: 응용 프로그램 가상화 속성 일반 탭
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819688"
---
# Application Virtualization 속성: 일반 탭


**응용 프로그램 가상화 속성** 대화 상자의 **일반** 탭을 사용 하 여 로그 설정과 데이터 위치를 수정 합니다.

이 탭에는 다음 요소가 포함 되어 있습니다.

<a href="" id="log-level"></a>**로그 수준**  
드롭다운 목록에서 수준을 선택 합니다. 기본 수준은 **정보**입니다.

<a href="" id="reset-log"></a>**로그 다시 설정**  
현재 로그 파일을 백업 하 고 즉시 새 로그 파일을 시작 하려면이 단추를 클릭 합니다.

<a href="" id="location"></a>**위치**  
로그 파일 sftlog.txt를 저장할 위치를 입력 하거나 찾아 선택 합니다. 기본 위치는 다음과 같습니다.

-   WindowsXP, Windows Server2003 —*C:\\documents 및 Settings\\All Users\\Application Data\\Microsoft\\Application 가상화 클라이언트*

-   Windows Vista, Windows 7, Windows Server2008-*C:\\ProgramData\\Microsoft\\Application 가상화 클라이언트*

<a href="" id="system-log-level"></a>**시스템 로그 수준**  
드롭다운 목록에서 수준을 선택 합니다. 기본 수준에는 **경고가**표시 됩니다.

**참고**  **시스템 로그 수준** 설정은 시스템 이벤트 로그에 전송 되는 메시지의 수준을 제어 합니다. 기록 된 메시지는 클라이언트 이벤트 로그에 기록 되는 메시지와 동일 하지만 클라이언트 이벤트 로그의 공간 제한이 없는 다른 위치에 저장 됩니다. 시스템 이벤트 로그에는 공간 제한이 없기 때문에 자세한 로깅이 필요한 상황에 가장 적합 합니다.

 

<a href="" id="global-data-directory"></a>**전역 데이터 디렉터리**  
로그 파일 디렉터리의 위치를 입력 하거나 찾습니다. 기본 위치는 다음과 같습니다.

-   WindowsXP, Windows Server2003 —*C:\\documents 및 Settings\\All Users\\Application Data\\Microsoft\\Application 가상화 클라이언트*

-   Windows Vista, Windows 7, Windows Server2008-*C:\\ProgramData\\Microsoft\\Application 가상화 클라이언트*

<a href="" id="user-data-directory"></a>**사용자 데이터 디렉터리**  
사용자 관련 데이터가 저장 되는 디렉터리의 위치를 입력 하거나 찾습니다. 기본값 은% APPDATA%입니다. 이 경로는 클라이언트 컴퓨터의 유효한 환경 변수 여야 합니다.

## 관련 항목


[Client Management Console: 응용 프로그램 가상화 속성](client-management-console-application-virtualization-properties.md)

 

 





