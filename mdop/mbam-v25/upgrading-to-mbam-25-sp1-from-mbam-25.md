---
title: MBAM 2.5에서 MBAM 2.5 SP1으로 업그레이드
description: MBAM 2.5에서 MBAM 2.5 SP1으로 업그레이드
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812745"
---
# MBAM 2.5에서 MBAM 2.5 SP1으로 업그레이드
이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 2.5 및 MBAM 클라이언트를 2.5에서 MBAM 2.5 SP1로 업그레이드 하는 프로세스에 대해 설명 합니다.

### 시작하기 전에
#### 2019 년 5 월 서비스 릴리스 다운로드
[데스크톱 최적화 팩](https://www.microsoft.com/download/details.aspx?id=58345)

#### 설치 documentaion 확인
모든 서버 이름, 데이터베이스 이름, 서비스 계정 및 암호를 포함 하 여 현재 MBAM 환경에 대 한 문서가 있는지 확인 합니다.

### 업그레이드 단계
#### MBAM 데이터베이스를 업그레이드 하는 단계 (SQL Server)
1. MBAM 구성자 사용 SQL server에서 또는 SSRS 데이터베이스가 호스팅되는 모든 위치에서 보고서 역할을 제거 합니다. 환경에 따라 동일한 서버 또는 개별 항목 일 수 있습니다.
  > [!NOTE]
  > 데이터베이스를 제거 하는 옵션이 표시 되지 않습니다. 이는 예상 되는 방법입니다.  
2. 볼륨 라이선스 서비스 센터 사이트의 MDOP-Microsoft 데스크톱 최적화 팩 2015에 있는 2.5 SP1을 설치 합니다.  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. 지금 구성 하지 않음 
4. MBAM 구성자 사용 보고서 역할 다시 추가
5. MBAM 구성자 사용 SQL Server에서 SQL 데이터베이스 역할 다시 추가
6. 마지막에는 해당 레코드가 이미 존재 하 고 생성 되지 않았다는 경고가 표시 되지만, 이것은 예상 되는 것입니다.
7. 이 프로세스는 기존 데이터베이스를 설치 중인 현재 버전으로 업데이트 합니다.              

#### MBAM 서버를 업그레이드 하는 단계 (MBAM 및 IIS 실행)
1. MBAM 구성자 사용 IIS 서버에서 관리자 및 셀프 서비스 포털 제거
2. MBAM 2.5 SP1 설치
3. 지금 구성 하지 않음  
4. MBAM 구성자 사용 관리자 및 셀프 서비스 포털을 IIS 서버에 다시 추가 
5. 관리자 권한 명령 프롬프트를 열고 **IISRESET**을 입력 한 다음 enter 키를 누릅니다.
 
#### MBAM 클라이언트/끝점을 업그레이드 하는 단계
1. 클라이언트 끝점에서 2.5 에이전트 제거
2. 클라이언트 끝점에 2.5 SP1 에이전트 설치
3. 2.5 SP1 에이전트를 실행 하는 클라이언트에 대 한 2019 롤업 클라이언트 업데이트를 푸시 종료 합니다. 
4. 5 월 2019 롤업을 설치 하기 전에 기존 클라이언트를 제거할 필요는 없습니다.  
