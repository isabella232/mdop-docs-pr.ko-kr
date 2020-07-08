---
title: 단일 서버에서 MBAM 언어 업데이트를 설치하는 방법
description: 단일 서버에서 MBAM 언어 업데이트를 설치하는 방법
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824753"
---
# 단일 서버에서 MBAM 언어 업데이트를 설치하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 하나 이상의 컴퓨터에서 실행할 수 있는 4 개의 서버 역할을 포함 합니다. 그러나 mbam 1.0 언어 릴리스 및 MBAM 정책 템플릿의 설치를 지원 하기 위해 두 개의 MBAM 서버 기능만 업데이트 해야 합니다. 컴퓨터 하나에 설치 되도록 필요한 세 가지 MBAM 기능을 모두 업데이트 하려면이 항목에서 설명 하는 단계를 수행 합니다.

**단일 서버에 MBAM 언어 업데이트를 설치 하려면**

1.  IIS (인터넷 정보 서비스) 관리 콘솔을 열고 **사이트로**이동한 다음 Microsoft BitLocker 관리 및 모니터링 웹 사이트를 종료 합니다.

2.  MBAM 웹 사이트의 바인딩을 편집한 다음 사이트의 바인딩을 일시적으로 수정 합니다. 예를 들어 443에서 9443로 포트를 변경 합니다.

3.  MBAM 설정 마법사 (MBAMsetup.exe)를 찾아 실행 하 고 다음 세 가지 기능을 선택 합니다.

    1.  규정 준수 및 감사 보고서

    2.  관리 및 모니터링 서버

    3.  그룹 정책 서식 파일

    **중요**  MBAM 서버 기능은 먼저 준수 및 감사 보고서로 업데이트 한 다음 관리 및 모니터링 서버 순서 대로 업데이트 해야 합니다. 그룹 정책 템플릿은 순서에 관계 없이 언제 든 업데이트할 수 있습니다.

     

4.  서버 데이터베이스를 업그레이드 한 후에 IIS 관리 콘솔을 열고 Microsoft BitLocker 관리 및 모니터링 웹 사이트의 바인딩을 검토 합니다.

5.  바인딩 중 하나를 삭제 하 고 남아 있는 바인딩에 MBAM enterprise 구성에 대 한 올바른 호스트 이름, 인증서 및 포트 번호가 있는지 확인 합니다.

6.  MBAM 웹 사이트를 다시 시작 합니다.

7.  MBAM 웹 사이트 기능을 테스트 합니다.

    -   MBAM 웹 인터페이스를 열고 클라이언트에 대 한 복구 키를 반입할 수 있는지 확인 합니다.

    -   새 또는 수동으로 암호 해독 된 클라이언트 컴퓨터의 암호화를 적용 합니다.

        **참고**  MBAM 클라이언트는 복구 및 하드웨어 데이터베이스와 통신할 수 있는 경우에만 열립니다.

         

## 관련 항목


[MBAM 1.0 언어 릴리스 업데이트 배포](deploying-the-mbam-10-language-release-update.md)

 

 





