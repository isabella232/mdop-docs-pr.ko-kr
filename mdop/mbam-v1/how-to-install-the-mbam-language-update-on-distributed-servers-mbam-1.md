---
title: 분산 서버에 MBAM 언어 업데이트를 설치하는 방법
description: 분산 서버에 MBAM 언어 업데이트를 설치하는 방법
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825698"
---
# 분산 서버에 MBAM 언어 업데이트를 설치하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 하나 이상의 컴퓨터에서 실행할 수 있는 4 개의 서버 역할을 포함 합니다. 그러나 두 개의 MBAM 서버 기능만이 MBAM 1.0 언어 릴리스 및 MBAM 정책 템플릿의 설치를 지원 하기 위해 업데이트가 필요 합니다. 여러 컴퓨터에 MBAM 서버 기능이 설치 된 구성에서는 다음 서버 기능만 업데이트 하면 됩니다.

-   MBAM 준수 및 감사 보고서

-   MBAM 관리 및 모니터링 서버

**중요**  MBAM 서버 기능은 먼저 준수 및 감사 보고서와 관리 및 모니터링 서버 순서 대로 업데이트 해야 합니다. MBAM 그룹 정책 템플릿은 순서에 관계 없이 언제 든 업데이트할 수 있습니다.

 

**MBAM 준수 및 감사 보고서 서버 기능에 MBAM 언어 업데이트를 설치 하려면**

1.  MBAM 준수 및 감사 보고서 기능을 실행 하는 컴퓨터에서 MBAM 언어 업데이트 설정 마법사 (MBAMsetup.exe)를 찾아 실행 합니다.

2.  준수 및 감사 보고서에 대 한 마법사를 완료 한 다음 마법사를 닫습니다.

**MBAM 관리 및 모니터링 서버 기능에 MBAM 언어 업데이트를 설치 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 컴퓨터에서 IIS (인터넷 정보 서비스) 관리 콘솔을 열고 **사이트로**이동한 다음 Microsoft BitLocker 관리 및 모니터링 웹 사이트를 종료 합니다.

2.  MBAM 웹 사이트의 바인딩을 편집 하도록 선택한 다음 사이트의 바인딩을 수정 합니다. 예를 들어 443에서 9443로 포트를 변경 합니다.

3.  MBAM 언어 업데이트 설정 마법사 (MBAMsetup.exe)를 찾아 실행 합니다. 관리 및 모니터링 서버 기능에 대 한 마법사를 완료 한 다음 마법사를 닫습니다.

4.  서버 데이터베이스를 업그레이드 한 후에 IIS 관리 콘솔을 열고 Microsoft BitLocker 관리 및 모니터링 웹 사이트의 바인딩을 검토 합니다.

5.  이전 바인딩을 삭제 하 고 남아 있는 바인딩에 MBAM enterprise 구성에 대 한 올바른 호스트 이름, 인증서 및 포트 번호가 있는지 확인 합니다.

6.  MBAM 웹 사이트를 다시 시작 합니다.

7.  MBAM 웹 사이트 기능을 테스트 합니다.

    -   MBAM 웹 인터페이스를 열고 클라이언트에 대 한 복구 키를 얻을 수 있는지 확인 합니다.

    -   새 또는 수동으로 암호 해독 된 클라이언트 컴퓨터의 암호화를 적용 합니다.

        **참고**  MBAM 클라이언트는 복구 및 하드웨어 데이터베이스와 통신할 수 있는 경우에만 열립니다.

         

## 관련 항목


[MBAM 1.0 언어 릴리스 업데이트 배포](deploying-the-mbam-10-language-release-update.md)

 

 





