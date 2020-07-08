---
title: MBAM 2.5 SP1에 핫픽스 적용
description: MBAM 2.5 SP1에 핫픽스 적용
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824188"
---
# MBAM 2.5 SP1에 핫픽스 적용
이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) Server 2.5 SP1 용 핫픽스를 적용 하는 프로세스에 대해 설명 합니다.

### 시작 하기 전에 Microsoft BitLocker 관리 및 모니터링 (MBAM) Server 2.5 SP1의 최신 핫픽스를 다운로드 합니다.
[데스크톱 최적화 팩](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> 핫픽스 릴리스에 대 한 자세한 내용은 [Mbam 버전 차트](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart)를 참조 하세요.

#### 기존 MBAM 환경에 대 한 MBAM 서버를 업데이트 하는 단계 
1. Mbam 서버 구성 도구를 열고 기능 제거를 선택 하 여이 작업을 수행 합니다.
2. 제어판에서 MDOP MBAM 제거 | 프로그램 및 기능.
3. MBAM 2.5 SP1 RTM 서버 구성 요소를 설치 합니다.
4. 최신 MBAM 2.5 SP1 핫픽스 롤업을 설치 합니다.
5. MBAM 서버 구성자를 사용 하 여 MBAM 기능을 구성 합니다.

#### 새 MBAM 2.5 SP1 서버 핫픽스를 설치 하는 단계
[새 서버 설치](deploying-the-mbam-25-server-infrastructure.md)에 대 한 문서를 참조 하세요.
