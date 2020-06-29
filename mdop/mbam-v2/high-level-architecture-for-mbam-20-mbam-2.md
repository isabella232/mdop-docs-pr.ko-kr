---
title: MBAM 2.0의 개략적인 아키텍처
description: MBAM 2.0의 개략적인 아키텍처
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824703"
---
# MBAM 2.0의 개략적인 아키텍처


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 프로비저닝 및 배포를 간소화 하 고, BitLocker에서 준수 및 보고 기능을 개선 하 고, 지원 비용을 줄이는 데 도움이 되는 클라이언트/서버 솔루션입니다. Microsoft BitLocker 관리 및 모니터링에는이 항목에서 설명 하는 기능이 포함 되어 있습니다.

Microsoft BitLocker 관리 및 모니터링은 독립 실행형 토폴로지에서 또는 Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager와 통합 된 토폴로지에서 배포할 수 있습니다. 이 항목에서는 독립 실행형 토폴로지의 아키텍처에 대해 설명 합니다. 통합 된 구성 관리자 토폴로지에 배포 하는 방법에 대 한 자세한 내용은 [구성 관리자에서 MBAM 사용](using-mbam-with-configuration-manager.md)을 참조 하세요.

다음 다이어그램에는 두 개의 서버와 관리 워크스테이션으로 구성 되는 프로덕션 환경의 MBAM 권장 아키텍처가 나와 있습니다. 이 아키텍처는 최대 20만 MBAM 클라이언트를 지원 합니다. 아키텍처 이미지의 서버 기능 및 데이터베이스는 다음 섹션에 설명 되어 있으며, 설치 하는 것이 좋습니다. 컴퓨터 또는 서버 아래에 나열 되어 있습니다.

**참고**  단일 서버 아키텍처는 테스트 환경 에서만 사용 해야 합니다.

 

![mbam 2 2-서버 배포 토폴로지](images/mbam2-3-servers.gif)

## 관리 및 모니터링 서버


다음 기능이이 서버에 설치 되어 있습니다.

-   **관리 및 모니터링 서버**. 관리 및 모니터링 서버 기능은 Windows Server에 설치 되어 있으며 보고서 및 지원 센터 포털, 모니터링 웹 서비스를 포함 하는 관리 및 모니터링 웹 사이트로 구성 됩니다.

-   **셀프 서비스 포털**. 셀프 서비스 포털이 Windows server에 설치 되어 있습니다. 셀프 서비스 포털을 사용 하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그온 할 수 있으며, 여기에서 잠금 BitLocker 볼륨을 복구 하는 데 복구 키를 얻을 수 있습니다.

## 데이터베이스 서버


다음 기능이이 서버에 설치 되어 있습니다.

-   **복구 데이터베이스**. 복구 데이터베이스는 Windows server와 Microsoft SQLServer의 지원 되는 인스턴스에 설치 되어 있습니다. 이 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.

-   **준수 및 감사 데이터베이스**. 준수 및 감사 데이터베이스는 Windows server와 SQLServer의 지원 되는 인스턴스에 설치 됩니다. 이 데이터베이스는 MBAM 클라이언트 컴퓨터에 대 한 규정 준수 데이터를 저장 합니다. 이 데이터는 주로 SQL Server Reporting Services (SSRS) 호스트가 보고 하는 데 사용 됩니다.

-   **준수 및 감사 보고서**. 규정 준수 및 감사 보고서는 Windows server에 설치 되어 있으며, SQL Server Reporting Services (SSRS) 기능이 설치 된 SQLServer의 지원 되는 인스턴스에 설치 됩니다. 이러한 보고서는 관리 및 모니터링 웹 사이트에서 또는 SSRS 서버에서 직접 액세스할 수 있는 MBAM 보고서를 제공 합니다.

## 관리 워크스테이션


다음 기능은 Windows server 또는 클라이언트 컴퓨터 일 수 있는 관리 워크스테이션에 설치 되어 있습니다.

-   **정책 서식 파일**. 정책 템플릿은 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정으로 구성 됩니다. 모든 서버 또는 워크스테이션에 정책 템플릿을 설치할 수 있지만, 일반적으로 지원 되는 Windows server 또는 클라이언트 컴퓨터인 관리 워크스테이션에 설치 됩니다. 워크스테이션이 전용 컴퓨터 일 필요는 없습니다.

## <a href="" id="---------mbam-client"></a> MBAM 클라이언트


MBAM 클라이언트는 Windows 컴퓨터에 설치 되어 있으며 다음과 같은 특징이 있습니다.

-   그룹 정책을 사용 하 여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 드라이브 암호화를 적용 합니다.

-   세 가지 BitLocker 데이터 드라이브 유형 (운영 체제 드라이브, 고정 데이터 드라이브, 이동식 데이터 (USB) 드라이브)에 대 한 복구 키를 수집 합니다.

-   컴퓨터에 대 한 규정 준수 데이터를 수집 하 고 보고 시스템으로 데이터를 전달 합니다.

## 관련 항목


[MBAM 2.0 시작](getting-started-with-mbam-20-mbam-2.md)

 

 





