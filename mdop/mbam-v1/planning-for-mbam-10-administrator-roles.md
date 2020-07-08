---
title: MBAM 1.0 관리자 역할 계획
description: MBAM 1.0 관리자 역할 계획
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825888"
---
# MBAM 1.0 관리자 역할 계획


이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 및 로컬 그룹을 만든 서버 위치에서 사용할 수 있는 관리자 역할에 대해 설명 합니다.

## MBAM 관리자 역할


<a href="" id="---------------mbam-system-administrators"></a> **MBAM 시스템 관리자**  
이 역할의 관리자는 모든 MBAM 기능에 액세스할 수 있습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다.

<a href="" id="---------------mbam-hardware-users"></a> **MBAM 하드웨어 사용자**  
이 역할의 관리자는 MBAM의 하드웨어 기능 기능에 액세스할 수 있습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다.

<a href="" id="---------------mbam-helpdesk-users"></a> **MBAM 헬프데스크 사용자**  
이 역할의 관리자는 MBAM의 헬프데스크 기능에 액세스할 수 있습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다.

<a href="" id="---------------mbam--report-users"></a> **MBAM 보고서 사용자**  
이 역할의 관리자는 MBAM의 규정 준수 및 감사 보고서 기능에 액세스할 수 있습니다. 이 역할에 대 한 로컬 그룹은 관리 및 모니터링 서버, 준수 및 감사 데이터베이스에 설치 되 고 규정 준수 및 감사 보고서를 호스팅하는 서버에서 설정 됩니다.

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **MBAM 헬프데스크 사용자**  
이 역할의 관리자는 MBAM의 헬프데스크 기능에 대 한 액세스 권한을 향상 시켰습니다. 이 역할의 로컬 그룹이 관리 및 모니터링 서버에 설치 되어 있습니다. 사용자가 MBAM 헬프데스크 사용자와 Mbam 헬프데스크 사용자의 구성원 인 경우 MBAM 헬프데스크 사용자 권한은 MBAM 헬프데스크 사용자 권한을 덮어씁니다.

**중요**  보고서를 보려면 관리 사용자가 관리 및 모니터링 서버, 준수 및 감사 데이터베이스 및 준수 및 보고서 기능을 호스팅하는 서버에 있는 **Mbam 보고서 사용자** 보안 그룹의 구성원 이어야 합니다. 최상의 방법으로 Active Directory에서 관리 및 모니터링 서버와 규정 준수 및 보고서를 호스팅하는 서버 모두에서 로컬 **Mbam 보고서 사용자** 보안 그룹에 대 한 권한을 사용 하 여 보안 그룹을 만듭니다.

 

## 관련 항목


[MBAM 1.0용 환경 준비](preparing-your-environment-for-mbam-10.md)

 

 





