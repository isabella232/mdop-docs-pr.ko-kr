---
title: AGPM 업그레이드 문제 해결
description: AGPM 업그레이드 문제 해결
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818248"
---
# AGPM 업그레이드 문제 해결

이 섹션에는 AGPM (고급 그룹 정책 관리) 서버를 최신 버전으로 업그레이드할 때 발생할 수 있는 일반적인 문제 (예: AGPM 4.0에서 AGPM 4.3)가 나열 되어 있습니다. 여기에 나와 있지 않은 문제점을 진단 하려면 [문제 해결 agpm](troubleshooting-agpm-agpm40.md) 을 보거나 agpm 관리자 (모든 권한)에서 로깅 및 추적을 사용 하는 것이 유용할 수 있습니다. 자세한 내용은 [로깅 및 추적 구성을](configure-logging-and-tracing-agpm40.md)참조 하세요.

## 어떤 문제가 있나요?

-   [HTML GPO 차이점 보고서를 생성 하지 못했습니다 (오류 코드 80004003).](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a>HTML GPO 차이점 보고서를 생성 하지 못했습니다 (오류 코드 80004003).

-   **원인**: 잘못 된 계정을 사용 하 여 AGPM 업그레이드 패키지를 설치 했습니다.

-   **해결**방법:이 문제를 해결 하려면 AGPM 관리자가 필요 합니다.
    
    -   **AGPM 서비스 계정의**사용자 이름 & 암호를 알고 있는지 확인 합니다.

    -   Agpm 서비스 계정으로 AGPM 서버에 대화형으로 로그온 합니다.
        
        -   다른 계정을 사용 하는 경우에는 설치에 실패 하기 때문에이는 매우 중요 합니다.

    -   AGPM 서비스를 종료 합니다.
    
    -   필요한 핫픽스를 설치 합니다.
    
    -   AGPM 클라이언트를 사용 하 여 AGPM에 연결 하 여 차이 보고서가 현재 작동 하는지 테스트 합니다.
    
## Microsoft 고급 그룹 정책 관리 4.0 SP3 용 핫픽스 패키지 1 설치
    
**이 핫픽스의 해결 된 문제**: AGPM에서 새 Gpo (그룹 정책 개체)를 제어 하거나 관리 하는 경우 차이점 보고서를 생성할 수 없습니다.

**이 업데이트를 다운로드 하는 방법**: 최신 버전의 Microsoft 데스크톱 최적화 팩을 설치 합니다 ([2017 서비스 릴리스 3 월](https://www.microsoft.com/download/details.aspx?id=54967)). 자세한 내용은 [KB 4014009](https://support.microsoft.com/help/4014009/) 을 참조 하세요.

더 구체적으로, `AGPM4.0SP1_Server_X64_KB4014009.exe` 다운로드 단추를 누른 후 표시 되는 목록에서 첫 번째 파일만 다운로드 하도록 선택할 수 있습니다.
      
Microsoft 데스크톱 최적화 팩에 대 한 다운로드 링크 (2017 서비스 릴리스 3 월)는 [여기](https://www.microsoft.com/download/details.aspx?id=54967)에서 찾을 수 있습니다.
      
      
## 참조 링크
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
