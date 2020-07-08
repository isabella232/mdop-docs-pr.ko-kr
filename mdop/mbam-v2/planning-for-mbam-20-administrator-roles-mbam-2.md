---
title: MBAM 2.0 관리자 역할 계획
description: MBAM 2.0 관리자 역할 계획
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824893"
---
# MBAM 2.0 관리자 역할 계획


이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 및 로컬 그룹을 만든 서버 위치에서 사용할 수 있는 관리자 역할을 나열 하 고 설명 합니다.

## MBAM 관리자 역할


<a href="" id="---------------mbam-system-administrators"></a> **MBAM 시스템 관리자**  
이 역할의 관리자는 모든 Microsoft BitLocker 관리 및 모니터링 기능에 액세스할 수 있습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다.

<a href="" id="---------------mbam-helpdesk-users"></a> **MBAM 헬프데스크 사용자**  
이 역할의 관리자는 MBAM의 지원 센터 기능에 액세스할 수 있습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다.

<a href="" id="---------------mbam-report-users"></a> **MBAM 보고서 사용자**  
이 역할의 관리자는 MBAM의 규정 준수 및 감사 보고서에 액세스할 수 있습니다. 이 역할에 대 한 로컬 그룹은 관리 및 모니터링 서버, 준수 및 감사 데이터베이스에 설치 되 고 규정 준수 및 감사 보고서를 호스팅하는 서버에서 설정 됩니다.

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **MBAM 헬프데스크 사용자**  
이 역할의 관리자는 MBAM의 지원 센터 기능에 대 한 액세스 권한을 향상 시켰습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다. 사용자가 MBAM 헬프데스크 사용자와 Mbam 헬프데스크 사용자의 구성원 인 경우 MBAM 헬프데스크 사용자 권한은 MBAM 헬프데스크 사용자 권한을 무시 합니다.

**중요**  보고서를 보려면 관리 사용자가 관리 및 모니터링 서버, 준수 및 감사 데이터베이스의 사용자 보안 그룹 및 준수 및 감사 보고서 기능을 호스트 하는 서버에 있는 **Mbam 보고서** 의 구성원 이어야 합니다. 최상의 방법으로, 관리 및 모니터링 서버와 규정 준수 및 감사 보고서를 호스트 하는 서버 모두에서 로컬 **Mbam 보고서 사용자** 보안 그룹에 대 한 권한을 사용 하 여 Active Directory 도메인 서비스에서 보안 그룹을 만듭니다.

 

## 관련 항목


[MBAM 2.0용 환경 준비](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





