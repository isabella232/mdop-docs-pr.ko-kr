---
title: MBAM 1.0용 환경 준비
description: MBAM 1.0용 환경 준비
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823193"
---
# MBAM 1.0용 환경 준비


Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하는 데 필요한 필수 구성 요소를 충족 하는지 확인 합니다. 사전 조건을 미리 알면 제품을 효율적으로 배포 하 고 해당 기능을 사용 하도록 설정 하 여 조직의 비즈니스 목적을 보다 효율적으로 지원할 수 있습니다.

## MBAM 1.0 배포 필수 구성 요소 검토


MBAM 클라이언트와 각 MBAM 서버 기능에는 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다.

MBAM 클라이언트와 MBAM 서버 기능을 성공적으로 설치 하려면 mbam 클라이언트 또는 MBAM 서버 기능 설치에 대해 지정 된 컴퓨터를 MBAM 설정에 적절 하 게 준비 하도록 계획 해야 합니다.

**참고**  MBAM 설치 프로그램이 시작 되기 전에 모든 선행 조건이 충족 되는지 확인 합니다. 이러한 사용자에 게 만족 하지 않으면 설치에 실패 하 게 됩니다.

 

[MBAM 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md)

## MBAM 1.0 그룹 정책 요구 사항 계획


MBAM이 엔터프라이즈에서 클라이언트를 관리할 수 있으려면 먼저 해당 환경의 암호화 요구 사항에 대 한 그룹 정책을 정의 해야 합니다.

**중요**  MBAM은 독립 실행형 BitLocker 드라이브 암호화에 대 한 정책과 함께 사용할 수 없습니다. 그룹 정책은 MBAM에 대해 정의 되어야 합니다. 그렇지 않으면 BitLocker 암호화 및 적용이 실패 합니다.

 

[MBAM 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)

## MBAM 1.0 관리자 역할에 대 한 계획


MBAM 관리자 역할은 다음을 설치할 때 MBAM 설정으로 만든 로컬 그룹에 의해 관리 됩니다. BitLocker 관리 및 모니터링 서버, 준수 및 감사 보고서 기능, 준수 및 감사 상태 데이터베이스.

MBAM 역할의 구성원은 더욱 효율적으로 관리할 수 있습니다. ActiveDirectoryDomainServices에서 보안 그룹을 만들고 해당 그룹에 적절 한 관리자 계정을 추가한 다음 해당 보안 그룹을 MBAM 로컬 그룹에 추가 합니다. 자세한 내용은 [MBAM 관리자 역할을 관리 하는 방법을](how-to-manage-mbam-administrator-roles-mbam-1.md)참조 하세요.

[MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)

## MBAM 계획에 대 한 기타 리소스


[MBAM 1.0 계획](planning-for-mbam-10.md)

 

 





