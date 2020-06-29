---
title: Microsoft 고급 그룹 정책 관리 4.0 SP1 릴리스 정보
description: Microsoft 고급 그룹 정책 관리 4.0 SP1 릴리스 정보
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818533"
---
# Microsoft 고급 그룹 정책 관리 4.0 SP1 릴리스 정보


이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.

이 릴리스 정보는 Microsoft AGPM (고급 그룹 정책 관리) 4.0 SP1을 설치 하기 전에 자세히 읽어 보세요. 이 릴리스 정보에는 AGPM 4.0 SP1을 성공적으로 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 정보와 다른 AGPM 설명서 사이에 차이가 있는 경우 최신 변경 내용을 신뢰할 수 있는 것으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## AGPM 4.0 SP1의 알려진 문제점


이 섹션에서는 AGPM 4.0 SP1에 대 한 릴리스 정보를 포함 합니다.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>AGPM 서버 설정을 변경 하려고 하면 제어판의 "제거" 도구가 작동 하지 않을 수 있음

AGPM 서버 설정을 변경 하려고 할 때 프로그램을 제거 하거나 변경할 수 있는 제어판의 도구가 작동 하지 않을 수 있습니다.

해결 방법: 제어판을 사용 하 여 AGPM 서버 설정을 변경 하려고 하기 전에 AGPM 보관 폴더의 복사본을 만듭니다. 그런 다음 Setup.exe를 사용 하 여 AGPM 서버를 다시 설치 하 고 원하는 구성 매개 변수를 선택할 수 있습니다.

### 보고서는 그룹 정책 개체에 추가 된 링크를 표시 하지 않습니다.

AGPM 설정 및 차이점 보고서에는 GPO (그룹 정책 개체)에 추가 된 링크가 표시 되지 않습니다.

해결 방법: 보고서의 링크를 보려면 GPMC (그룹 정책 관리) 콘솔에서 GPO를 선택 하 고 오른쪽 창에서 **설정** 탭을 클릭 합니다.

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a>보고서에 모든 "선택 옵션 속성" 설정이 표시 되지 않음

AGPM 설정 및 차이점 보고서에는 그룹 정책 개체 편집기의 선택 옵션 속성 창에서 선택한 설정이 모두 표시 되지 않습니다.

해결 방법: GPMC를 사용 하 여 보고서에서 선택한 선택 옵션의 속성 설정을 봅니다.

### 특정 브라우저에서 보고서에 표시 및 숨기기 탭이 표시 되지 않음

Google Chrome 또는 Mozilla Firefox에서 보고서를 볼 때 AGPM 설정 및 차이점 보고서의 오른쪽에 표시 되는 보기 및 숨기기 탭이 표시 되지 않습니다.

해결 방법: Internet Explorer를 사용 하 여 보고서를 봅니다.

### AGPM 설정 및 차이점 보고서에 GPMC 보고서의 다른 콘텐츠가 표시 될 수 있음

AGPM 설정 및 차이점 보고서에는 GPMC (그룹 정책 관리) 콘솔의 보고서와 동일한 콘텐츠가 표시 되지 않을 수 있습니다.

해결 방법: GPMC를 사용 하 여 AGPM 보고서를 봅니다.

### 도메인 컨트롤러가 온라인 상태가 아닌 경우 AGPM 서비스가 시작 되지 않음

Windows 8의 도메인 컨트롤러에 AGPM 서비스가 설치 되어 있으면 도메인 컨트롤러가 온라인 상태가 아닌 경우 서비스가 시작 되지 않습니다.

해결 방법: 도메인 컨트롤러가 온라인 상태 이면 AGPM 서비스를 수동으로 시작 합니다.

### Agpm 4.0 릴리스에서 핫픽스를 plus 하 여 업그레이드할 때 agpm 서버를 AGPM 4.0 SP1로 업그레이드 하는 것이 차단 됨

AGPM 서버를 AGPM 4.0로 업그레이드 하려고 합니다. AGPM 4.0를 설치한 다음 AGPM 핫픽스 설치 후의 SP1 (기술 자료 문서 [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)참조), 업그레이드가 실패 하 고 완료할 수 없습니다.

해결 방법: AGPM 4.0 서버를 제거한 다음 AGPM 4.0 SP1을 설치 합니다.

### 보고서가 조직 구성 단위 링크를 표시 하지 않음

제어 되지 않은 GPO를 조직 구성 단위에 연결한 다음 AGPM을 사용 하 여 해당 GPO를 제어 하는 경우 AGPM 설정 및 차이점 보고서에 조직 구성 단위 링크가 표시 되지 않습니다.

해결 방법: **변경 설정** 노드의 **제어** 탭에서 gpo를 마우스 오른쪽 단추로 클릭 하 고 **설정을** 클릭 한 다음 **gpo 링크** 를 클릭 하 여 조직 링크를 봅니다. 또는 GPMC를 사용 하 여 **범위** 탭에서 GPO에 대 한 링크를 볼 수 있습니다.

## 관련 항목


[고급 그룹 정책 관리](index.md)

[AGPM 4.0 SP1의 새로운 기능](whats-new-in-agpm-40-sp1.md)

 

 





