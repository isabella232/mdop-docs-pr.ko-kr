---
title: MBAM 2.0 서버 인프라 배포
description: MBAM 2.0 서버 인프라 배포
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8aee322b9a1aacbf98ff8362e95e21c2dd3d289a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910803"
---
# <a name="deploying-the-mbam-20-server-infrastructure"></a>MBAM 2.0 서버 인프라 배포


독립 실행형 토폴로지용 Microsoft MBAM(BitLocker 관리 및 모니터링) 서버 기능은 프로덕션 환경의 둘 이상의 서버에 서로 다른 구성으로 설치할 수 있습니다. 권장되는 구성은 확장성 요구 사항에 따라 프로덕션 환경에 대해 두 대의 서버입니다. 테스트 환경에서만 MBAM 설치에 단일 서버를 사용합니다. MBAM Server 기능 배포 계획에 대한 자세한 내용은 [Planning for MBAM 2.0 Server Deployment을 참조하십시오.](planning-for-mbam-20-server-deployment-mbam-2.md)

다음 다이어그램에는 권장되는 두 서버 MBAM 배포를 구성하는 방법의 예가 표시됩니다. 이 구성은 프로덕션 환경에서 최대 200,000MBAM 클라이언트를 지원합니다. 아키텍처 이미지의 서버 기능 및 데이터베이스는 다음 섹션에 설명되어 있으며 설치하는 것이 권장되는 컴퓨터 또는 서버 아래에 나열되어 있습니다.

![mbam 22 서버 배포 토폴로지](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>관리 및 모니터링 서버


이 서버에는 다음과 같은 기능이 설치됩니다.

-   **관리 및 모니터링 서버.** 관리 및 모니터링 서버 기능은 Windows 서버에 설치하며 Help Desk 웹 사이트 및 모니터링 웹 서비스로 구성됩니다.

-   **셀프 서비스 포털**. Self-Service 포털이 Windows 설치됩니다. Self-Service 포털을 사용하면 클라이언트 컴퓨터의 최종 사용자가 웹 사이트에 독립적으로 로그온할 수 있습니다. 여기서 복구 키를 얻어 잠긴 BitLocker 볼륨을 복구할 수 있습니다.

## <a name="database-server"></a>데이터베이스 서버


이 서버에는 다음과 같은 기능이 설치됩니다.

-   **복구 데이터베이스.** 복구 데이터베이스는 서버 및 Windows 서버의 지원되는 인스턴스에 Microsoft SQL Server. 이 데이터베이스에는 MBAM 클라이언트 컴퓨터에서 수집된 복구 데이터가 저장됩니다.

-   **준수 및 감사 데이터베이스**. 준수 및 감사 데이터베이스는 Windows 서버 및 지원되는 서버 인스턴스에 SQL Server. 이 데이터베이스에는 MBAM 클라이언트 컴퓨터의 준수 데이터가 저장됩니다. 이 데이터는 주로 SSRS(SQL Server Reporting Services) 보고서에 사용됩니다.

-   **준수 및 감사 보고서**. 준수 및 감사 보고서는 SSRS(Windows) 기능이 설치된 SQL Server 서버 및 지원되는 SQL Server Reporting Services 인스턴스에 설치됩니다. 이러한 보고서는 지원 센터 웹 사이트 또는 SSRS 서버에서 직접 액세스할 수 있는 MBAM 보고서를 제공합니다.

## <a name="management-workstation"></a>관리 Workstation


다음 기능은 서버 또는 클라이언트 컴퓨터일 수 있는 관리 Windows 설치됩니다.

-   **정책 템플릿**. 정책 템플릿은 BitLocker 드라이브 암호화에 대한 MBAM 구현 설정을 정의하는 그룹 정책으로 구성됩니다. 정책 템플릿은 모든 서버 또는 workstation에 설치할 수 있지만 일반적으로 서버 또는 클라이언트 컴퓨터에 지원되는 관리 Windows 설치됩니다. 이 Workstation은 전용 컴퓨터가 아니어도 됩니다.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM 클라이언트


MBAM 클라이언트는 Windows 컴퓨터에 설치하며 다음과 같은 특징이 있습니다.

-   그룹 정책을 사용하여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 드라이브 암호화를 적용합니다.

-   운영 체제 드라이브, 고정 데이터 드라이브 및 USB(이동식 데이터) 드라이브의 세 가지 BitLocker 데이터 드라이브 유형에 대한 복구 키를 수집합니다.

-   컴퓨터의 준수 데이터를 수집하고 데이터를 보고 시스템에 전달합니다.

## <a name="other-resources-for-deploying-mbam-20-server-features"></a>MBAM 2.0 서버 기능 배포를 위한 기타 리소스


[MBAM 2.0 배포](deploying-mbam-20-mbam-2.md)

 

 





