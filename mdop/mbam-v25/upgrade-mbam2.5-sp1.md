---
title: MBAM 2.5에서 MBAM 2.5 SP1 서비스 릴리스 업데이트 업그레이드
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812769"
---
# MBAM 2.5에서 MBAM 2.5 SP1 서비스 릴리스 업데이트 업그레이드

이 문서에서는 microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 [Microsoft 데스크톱 최적화 팩 (MDOP)](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) 과 함께 mbam 2.5 서비스 팩 1 (SP1)으로 업그레이드 하는 단계별 지침을 제공 합니다. 독립 실행형 구성에서 서비스를 업데이트할 수 2019 있습니다.

이 가이드에서는 2 서버 구성을 사용 합니다. 한 서버는 Microsoft SQL Server 2016을 실행 하는 데이터베이스 서버입니다. 이 서버는 MBAM 데이터베이스와 보고서를 호스팅합니다. 다른 서버는 Windows Server 2012 R2 웹 서버입니다. 이 서버는 "관리 및 모니터링" 및 "셀프 서비스 포털"을 호스팅합니다.

## MBAM 2.5 SP1 업그레이드 준비

### 환경에서 MBAM 서버 파악

1. SQL Server 데이터베이스 엔진: MBAM 데이터베이스를 호스트 하는 서버입니다.
2. SQL Server Reporting Services: MBAM 보고서를 호스팅하는 서버입니다.
3. IIS (인터넷 정보 서비스) 웹 서버: MBAM 웹 응용 프로그램 및 MBAM 서비스를 호스팅하는 서버입니다.
4. ) Microsoft System Center Configuration Manager 기본 사이트 서버: MBAM 구성 응용 프로그램은이 서버에서 실행 되어 MBAM 보고서를 구성 관리자와 통합 합니다. 그런 다음이 보고서가 Configuration Manager의 SSRS (SQL Server Reporting Services) 인스턴스에 대 한 기존 Configuration Manager 보고서와 병합 됩니다.

### 서비스 계정, 그룹, 서버 이름, 보고서 URL 확인

1. IIS 웹 서버에서 MBAM 데이터베이스의 데이터를 읽고 쓰는 데 사용 하는 MBAM 응용 프로그램 풀 서비스 계정을 식별 합니다.
2. MBAM 웹 기능 구성 및 보고서 웹 서비스 URL 중 사용 되는 그룹을 식별 합니다.
3. SQL Server 이름 및 인스턴스 이름을 식별 합니다. 자세한 내용은이 비디오를 시청 하세요.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. 준수 및 감사 데이터베이스에서 규정 준수 데이터를 읽는 데 사용 되는 SQL Server Reporting Services 계정을 식별 합니다. 자세한 내용은이 비디오를 시청 하세요.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## MBAM 인프라를 사용 가능한 최신 버전으로 업그레이드

MBAM 서버 인프라 설치 또는 업그레이드는 항상 아래 나열 된 순서 대로 수행 됩니다.

- SQL Server 데이터베이스 엔진: 데이터베이스
- SQL Server Reporting Services: 보고서
- 웹 서버: 웹 응용 프로그램
- SCCM 서버: SCCM 통합 보고서 (해당 하는 경우)
- 클라이언트: MBAM 에이전트 또는 클라이언트 업데이트
- 그룹 정책 서식 파일: 기존 그룹 정책을 새 템플릿으로 업데이트 하 고 기존 MBAM 그룹 정책에서 새 설정을 사용 하도록 설정 합니다.

> [!NOTE]
> 업그레이드를 실행 하기 전에 MBAM 데이터베이스의 전체 데이터베이스 백업을 만드는 것이 좋습니다.

### MBAM SQL Server 업그레이드

이 비디오를 시청 하 여 MBAM SQL Server를 업그레이드 하는 방법을 알아보세요.

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### MBAM 웹 서버 업그레이드

이 비디오를 시청 하 여 MBAM 웹 서버를 업그레이드 하는 방법을 알아보세요.

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## 추가 정보

MBAM 2.5 SP1의 알려진 문제에 대 한 자세한 내용은 [mbam 2.5 sp1에 대 한 릴리스 정보](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1)를 참조 하세요.
