---
title: Application Virtualization Client 문제 해결 정보
description: Application Virtualization Client 문제 해결 정보
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815193"
---
# Application Virtualization Client 문제 해결 정보


이 항목에서는 Application Virtualization (App-v) 클라이언트의 다양 한 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.

## 게시 새로 고침이 매우 느리게 됨


특정 컴퓨터의 게시 새로 고침이 예상 보다 오래 걸리므로 클라이언트가 **IconSourceRoot** 설정을 사용 하도록 구성 된 경우 **IconSourceRoot** 에 올바르지 않은 URL이 포함 되어 있는지 여부를 확인 합니다. 유효 하지 않은 URL이 있으면 게시 새로 고침 중 매우 오래 지연 됩니다.

## 사용자가 서버에 연결 하 여 연결이 끊긴 작업 모드로 전환할 수 없음


RTSPS 프로토콜을 사용 하 여 구성 된 App-v 관리 서버를 사용 하는 경우 사용자가 연결할 수 없고 연결이 끊긴 작업 모드로 전환 되는 경우 서버에서 사용 중인 인증서가 유효한 지 여부를 확인 합니다. 유효 하지 않은 인증서는 사용자가 연결 하는 것을 방지 하 고 연결이 끊긴 작동 모드로 전환 됩니다.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>사용자가 응용 프로그램이 완전히 캐시 되지 않은 경우 성능이 느려지는 문제가 발생 함


응용 프로그램이 완전히 캐시 되지 않은 경우에는 사용자가 응용 프로그램을 시작 하거나 사용할 때 일시적인 성능이 간헐적으로 느려지는 문제가 발생할 수 있습니다. 이 문제가 발생할 수 있는 몇 가지 이유는 다음과 같습니다 (예: App-v 클라이언트가 응용 프로그램을 자동으로 로드 하는 과정 또는 순서 대로 요청이 처리 되는 경우). 응용 프로그램이 완전히 캐시 되 면 이러한 문제가 더 이상 발생 하지 않습니다.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>업데이트가 제거 된 후 표시 되는 오류


다음과 같이 올바른 Windows Installer 3.1 명령 형식을 사용 하 여 앱-V 클라이언트에서 업데이트를 제거 해야 합니다.

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

이전 명령 형식을 사용 하면 `msiexec /package <GUID> /uninstall <GUID>` 오류 6003 "Application 가상화 클라이언트를 시작할 수 없습니다."가 발생 합니다.

## 응용 프로그램을 시작 하려고 할 때 발생 하는 오류 코드 0A-0000E01E


오류 코드 0A-0000E01E는 시퀀싱 된 응용 프로그램 패키지가 손상 되었을 수 있음을 나타냅니다. 해결 방법은 패키지를 resequence 하는 것입니다.

## 사용자가 Q: 드라이브에서 만든 파일에 액세스할 수 없는 경우


사용자가 **Q:** 드라이브에 파일을 저장 하는 경우 드라이브에 대 한 읽기 권한이 없기 때문에 검색할 수 없습니다. 사용자는 파일을 **Q:** 드라이브에 저장 하면 안 됩니다.

## 사용자에 게 1D1 오류가 표시 됨


파일 스트리밍 URL이 OSD (Open Software Descriptor) 파일에서 잘못 설정 된 경우 App-v 클라이언트는 "파일을 찾을 수 없습니다." 오류가 발생 하는 대신 1d1 오류를 반환 합니다. 이 오류는 응용 프로그램 시작이 실패 하 고 사용자가 강제로 연결이 끊긴 작업 모드로 전환 되었음을 나타냅니다. 파일 스트리밍 URL을 수정 합니다.

## 일부 응용 프로그램과 관련 된 잘못 된 아이콘


게시 작업에 아이콘을 사용 하는 경우 App-v 클라이언트는 먼저 게시 작업에 지정 된 아이콘의 경로와 원래 원본 경로가 일치 하는 항목에 대 한 아이콘 캐시를 검색 하 여 아이콘의 캐시 된 복사본을가지고 있는지 여부를 확인 합니다. 앱-V 클라이언트가 일치 하는 항목을 찾으면 이미 캐시 된 아이콘을 사용 하 게 됩니다. 그렇지 않으면 새 아이콘이 캐시로 다운로드 됩니다. 아이콘 경로가 스크래치 디렉터리 이거나 새 아이콘 또는 패키지에 다시 사용 되는 경우 캐시의 조회가 이전 작업에서 잘못 된 아이콘을 선택할 수 있습니다.

## 사용자가 응용 프로그램을 시작할 때 자격 증명을 묻는 메시지가 표시 됨


사용자가 시스템 관리자가 액세스를 제한 한 가상 응용 프로그램을 시작 하려고 하면 사용자에 게 자격 증명을 입력 하 라는 메시지가 표시 될 수 있습니다. 사용자는 응용 프로그램을 실행할 권한이 있는 계정의 사용자 이름 및 암호를 입력 한 다음 enter 키를 누릅니다.

## 앱-V 클라이언트를 버전 4.5으로 업그레이드 한 후 게시 새로 고침이 실패 함


사용자 데이터 디렉터리가 이전에 비표준 위치에 배치 된 경우 (%*allpeople 프로필*%\\Document\ \Softgrid Client\\Users\\%*username*), 컴퓨터에 대 한 관리자 권한이 없는 사용자는 app-v 클라이언트를 업그레이드 한 후 게시 새로 고침이 실패 하는 것을 확인할 수 있습니다. 업그레이드 중에는 앱-V 클라이언트 전역 데이터 디렉터리 및 모든 하위 디렉터리가 관리자만 사용할 수 있는 제한 된 액세스 권한으로 구성 됩니다. 전역 데이터 디렉터리의 하위 디렉터리가 아닌 사용자 데이터 디렉터리를 업그레이드 하기 전에 변경 하 여이 문제를 방지할 수 있습니다.

## 설치 실패 후 다시 부팅 필요


어떤 이유로 든 클라이언트 설치에 실패 하 고 클라이언트를 설치 하려는 후속 시도도 실패 하면 Windows Installer 로그를 확인 하 여 "sftplay 실패, 오류 = 1072" 라는 오류 메시지가 표시 되는지 확인 합니다. 그렇다면 클라이언트를 다시 설치 하기 전에 컴퓨터를 다시 시작 합니다.

## 손상 된 가상 응용 프로그램 복구


어떤 이유로 든 지 Windows Installer 패키지 (MSI) 파일을 사용 하 여 설치 된 가상 응용 프로그램 패키지가 손상 되는 경우 패키지를 다시 설치 합니다. Windows Installer에서 사용할 수 있는 복구 기능은 사용자 볼륨을 업데이트 하지 않습니다.

## 관련 항목


[Application Virtualization Client 참조](application-virtualization-client-reference.md)

 

 





