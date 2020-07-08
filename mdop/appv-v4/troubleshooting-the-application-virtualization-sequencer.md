---
title: Application Virtualization Sequencer 문제 해결
description: Application Virtualization Sequencer 문제 해결
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815183"
---
# Application Virtualization Sequencer 문제 해결


이 항목에서는 Application Virtualization (App-v) Sequencer의 일반적인 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.

## 앱-V 시퀀서를 사용 하 여 SFTD 파일을 만들면 버전 번호가 예기치 않게 증가 합니다.


SFTD 파일과 연결 된 버전 번호가 갑자기 늘어납니다.

**해결 방법**

명령줄을 사용 하 여 새 sft 파일을 생성 합니다. 명령줄을 사용 하 여 sft 파일을 만들려면 명령 프롬프트에서 다음을 입력 합니다.

**mkdiffpkg.exe &lt; 기본 sft 파일 이름 &gt; &lt; 차등 sft 파일 이름&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>패키지 업그레이드 후 OSD 파일의 파일 이름이 올바르지 않음


기존 패키지를 업그레이드 한 후에는 파일 이름이 올바르지 않습니다.

**해결 방법**

업그레이드를 위해 패키지를 열 때 루트 Q:\\ 드라이브를 패키지의 출력 위치로 지정 해야 합니다. 연결 된 파일 이름을 출력 위치와 함께 지정 하지 마세요.

## Microsoft Word2003 기본 설치로 인해 클라이언트로 스트리밍할 때 오류가 발생 하는 경우


Microsoft Word2003를 클라이언트로 스트리밍할 때 오류가 반환 되지만 Microsoft Word는 계속 실행 됩니다.

**해결 방법**

가상 응용 프로그램 패키지를 Resequence 하 고 **전체 설치**를 선택 합니다.

## 종속 패키지를 만들 때 패키지 업그레이드가 작동 하지 않음


패키지 업그레이드를 사용 하 여 종속 패키지를 만들고 새 레지스트리 항목을 추가 하는 경우 올바르게 작동 하는 것 처럼 보이지만 업데이트 된 레지스트리 항목은 사용할 수 없습니다.

**해결 방법**

레지스트리 설정은 항상 패키지의 원본 버전과 함께 저장 되므로 원본 패키지를 복구 하지 않는 한 패키지에 대 한 업데이트는 사용할 수 없는 것으로 표시 됩니다.

## 시퀀스를 시도 하는 동안 오류가 발생 했습니다. NET 2.0


필요한 패키지를 시퀀싱 하는 경우 NET 2.0을 시작 하면 오류가 발생 합니다.

**해결 방법**

필요한 시퀀싱 패키지 NET 2.0은 지원 되지 않습니다.

## 관련 항목


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





