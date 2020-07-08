---
title: MBAM 2.0용 환경 준비
description: MBAM 2.0용 환경 준비
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825608"
---
# MBAM 2.0용 환경 준비


Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하기 위한 전제 조건을 충족 하는지 확인 해야 합니다. 사전 요구 사항이 앞에 있는 것을 알면 제품을 효율적으로 배포 하 고 해당 기능을 사용 하도록 설정 하 여 조직의 비즈니스 목표를 효과적으로 지원할 수 있습니다.

Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 배포 하는 경우 [Configuration manager를 사용 하 여 MBAM 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.

## MBAM 2.0 배포 필수 구성 요소 검토


MBAM 클라이언트와 각 MBAM 서버 기능에는 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다.

MBAM 클라이언트와 MBAM 서버 기능을 성공적으로 설치 하려면 mbam 클라이언트 또는 MBAM 서버 기능 설치에 대해 지정 된 컴퓨터가 MBAM 설정에 적절 하 게 준비 되어 있는지 확인 합니다.

**참고**  MBAM 설치 프로그램이 설치를 시작 하기 전에 모든 필수 구성 요소를 충족 하는지 확인 합니다. 모든 선행 조건이 충족 되지 않으면 설치에 실패 합니다.

 

[MBAM 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md)

## MBAM 2.0 그룹 정책 요구 사항 계획


MBAM이 엔터프라이즈에서 클라이언트를 관리할 수 있으려면 사용자 환경의 암호화 요구 사항에 대 한 그룹 정책을 정의 해야 합니다.

**중요**  MBAM은 독립 실행형 BitLocker 드라이브 암호화에 대 한 정책과 함께 사용할 수 없습니다. MBAM에 대해 그룹 정책 설정을 정의 해야 하며, BitLocker 암호화 및 적용이 실패 합니다.

 

[MBAM 2.0 그룹 정책 요구 사항 계획](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## MBAM 2.0 관리자 역할에 대 한 계획


MBAM 관리자 역할은 BitLocker 관리 및 모니터링 서버, 준수 및 감사 보고서 기능, 준수 및 감사 상태 데이터베이스를 설치할 때 MBAM 설정으로 만든 로컬 그룹에서 관리 합니다.

Microsoft BitLocker 관리 및 모니터링 역할의 구성원은 ActiveDirectoryDomainServices에서 보안 그룹을 만들고 해당 그룹에 적절 한 관리자 계정을 추가한 다음 해당 보안 그룹을 BitLocker 관리 및 로컬 그룹 모니터링에 추가 하 여 관리할 수 있습니다. 자세한 내용은 [MBAM 관리자 역할을 관리 하는 방법을](how-to-manage-mbam-administrator-roles-mbam-2.md)참조 하세요.

## MBAM 계획에 대 한 기타 리소스


[MBAM 2.0 계획](planning-for-mbam-20-mbam-2.md)

[MBAM 2.0 지원되는 구성](mbam-20-supported-configurations-mbam-2.md)

 

 





