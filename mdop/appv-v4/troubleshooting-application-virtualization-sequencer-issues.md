---
title: Application Virtualization Sequencer 문제 해결
description: Application Virtualization Sequencer 문제 해결
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815243"
---
# Application Virtualization Sequencer 문제 해결


이 항목에서는 Application Virtualization (App-v) Sequencer의 일반적인 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.

## 앱-V 시퀀서를 사용 하 여 SFTD 파일을 만들면 버전 번호가 예기치 않게 증가 합니다.


명령줄을 사용 하 여 새 sft 파일을 생성 합니다. 명령줄을 사용 하 여 sft 파일을 만들려면 명령 프롬프트에서 다음을 입력 합니다.

**mkdiffpkg.exe &lt; 기본 sft 파일 이름 &gt; &lt; 차등 sft 파일 이름&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>패키지 업그레이드 후 OSD 파일의 파일 이름이 올바르지 않음


업그레이드를 위해 패키지를 열 때 루트 Q:\\ 드라이브를 패키지의 출력 위치로 지정 해야 합니다. 연결 된 파일 이름을 출력 위치와 함께 지정 하지 마세요.

## Microsoft Word2003 기본 설치로 인해 클라이언트로 스트리밍할 때 오류가 발생 하는 경우


Microsoft Word2003를 클라이언트로 스트리밍할 때 오류가 반환 되지만 Microsoft Word는 계속 실행 됩니다.

**해결 방법**

가상 응용 프로그램 패키지를 Resequence 하 고 **전체 설치**를 선택 합니다.

## 종속 패키지를 만들 때 활성 업그레이드가 작동 하지 않음


활성 업그레이드를 사용 하 여 종속 패키지를 만들고 새 레지스트리 항목을 추가 하는 경우 올바르게 작동 하는 것 처럼 보이지만 업데이트 된 레지스트리 항목은 사용할 수 없습니다.

**해결 방법**

레지스트리 설정은 항상 패키지의 원본 버전과 함께 저장 되므로 원본 패키지를 복구 하지 않는 한 패키지에 대 한 업데이트는 사용할 수 없는 것으로 표시 됩니다.

## 속성 페이지를 사용 하 여 Microsoft Office2007 문서에 대 한 자세한 정보가 표시 되지 않음


속성 페이지를 사용 하 여 Microsoft Office2007 문서와 관련 된 세부 정보를 보려고 하면 자세한 정보가 표시 되지 않습니다.

**해결 방법**

App-v는 이러한 속성 페이지에 필요한 셸 확장을 지원 하지 않습니다.

## 16 비트 응용 프로그램을 시퀀싱 할 때 일부 레지스트리 키가 캡처되지 않음


App-v 4.5에서 레지스트리 후크는 커널 모드에서 사용자 모드로 이동 되었습니다. 16 비트 응용 프로그램이 나 16 비트 설치 관리자를 사용 하는 응용 프로그램을 시퀀싱 하려면 먼저 Windows NT NTVDM (가상 DOS 시스템)의 고유한 복사본에서 프로세스가 실행 되도록 sequencer 컴퓨터를 구성 해야 합니다.

**해결 방법**

응용 프로그램을 순서 대로 설정 하기 전에 시퀀싱 컴퓨터에서 다음과 같은 전역 REGSZ 레지스트리 키 값을 "yes"로 설정 합니다.

HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM

이 효과를 적용 하려면 컴퓨터를 다시 시작 해야 합니다.

## 관련 항목


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





