---
title: MBAM 1.0의 개략적인 아키텍처
description: MBAM 1.0의 개략적인 아키텍처
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d06c7bd801a9dd63916d310af75e88a307e7226a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910413"
---
# <a name="high-level-architecture-for-mbam-10"></a>MBAM 1.0의 개략적인 아키텍처


Microsoft BitLocker 관리 및 모니터링(MBAM)은 BitLocker 프로비저닝 및 배포를 간소화하고, BitLocker 규정 준수 및 보고를 개선하고, 지원 비용을 절감하는 데 도움이 되는 클라이언트/서버 데이터 암호화 솔루션입니다. MBAM에는 이 항목에 설명된 기능이 포함되어 있습니다.

또한 MBAM 아키텍처 및 MBAM 설치에 대한 개요를 제공하는 비디오가 있습니다. 자세한 내용은 [MBAM 배포 및 아키텍처 개요 를 참조하세요.](https://go.microsoft.com/fwlink/p/?LinkId=258392)

## <a name="architecture-overview"></a>아키텍처 개요


다음 다이어그램에는 MBAM 아키텍처가 표시됩니다. 단일 서버 MBAM 배포 토폴로지에서는 MBAM 기능을 소개합니다. 그러나 이 MBAM 배포 토폴로지는 랩 환경에서만 권장됩니다.

**참고**  
프로덕션 배포에는 3대 이상의 컴퓨터 MBAM 배포 토폴로지가 권장됩니다. MBAM 배포 토폴로지에 대한 자세한 내용은 [Deploying the MBAM 1.0 Server Infrastructure를 참조하십시오.](deploying-the-mbam-10-server-infrastructure.md)

 

![mbam 단일 서버 배포 토폴로지.](images/mbam-1-server.jpg)

1.  **관리 및 모니터링 서버.** MBAM 관리 및 모니터링 서버는 Windows 서버에 설치하고 MBAM 관리 및 관리 웹 사이트와 모니터링 웹 서비스를 호스팅합니다. MBAM 관리 및 관리 웹 사이트는 엔터프라이즈 준수 상태를 결정하고, 활동을 감사하고, 하드웨어 기능을 관리하고, BitLocker 복구 키와 같은 복구 데이터에 액세스하는 데 사용됩니다. 관리 및 모니터링 서버는 다음 데이터베이스 및 서비스에 연결합니다.

    -   복구 및 하드웨어 데이터베이스. 복구 및 하드웨어 데이터베이스는 Windows 및 지원되는 SQL Server 인스턴스에 설치됩니다. 이 데이터베이스에는 MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터 및 하드웨어 정보가 저장됩니다.

    -   준수 및 감사 데이터베이스. 준수 및 감사 데이터베이스는 Windows 설치하고 지원되는 SQL Server 인스턴스입니다. 이 데이터베이스에는 MBAM 클라이언트 컴퓨터의 준수 데이터가 저장됩니다. 이 데이터는 주로 SSRS(SQL Server Reporting Services) 보고서에 사용됩니다.

    -   규정 준수 및 감사 보고서. 준수 및 감사 보고서는 SSRS 기능이 Windows 지원되는 SQL Server 인스턴스에 설치됩니다. 이러한 보고서는 Microsoft BitLocker 관리 및 모니터링 보고서를 제공 합니다. 이러한 보고서는 MBAM 관리 및 관리 웹 사이트에서 액세스하거나 SSRS 서버에서 직접 액세스할 수 있습니다.

2.  **MBAM 클라이언트.** Microsoft BitLocker 관리 및 모니터링 클라이언트는 다음 작업을 수행합니다.

    -   그룹 정책을 사용하여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 암호화를 적용합니다.

    -   운영 체제 드라이브, 고정 데이터 드라이브 및 USB(이동식 데이터) 드라이브의 세 가지 BitLocker 데이터 드라이브 유형에 대한 복구 키를 수집합니다.

    -   클라이언트 컴퓨터에 대한 복구 정보 및 하드웨어 정보를 수집합니다.

    -   컴퓨터의 준수 데이터를 수집하고 데이터를 보고 시스템에 전달합니다.

3.  **정책 템플릿**. MBAM 그룹 정책 템플릿은 지원되는 Windows 서버 또는 클라이언트 컴퓨터에 설치됩니다. 이 템플릿은 BitLocker 드라이브 암호화에 대한 MBAM 구현 설정을 지정하는 데 사용됩니다.

## <a name="related-topics"></a>관련 항목


[MBAM 1.0 시작](getting-started-with-mbam-10.md)

 

 





