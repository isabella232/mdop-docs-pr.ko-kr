---
title: Microsoft BitLocker 관리 및 모니터링 2.5
description: Microsoft BitLocker 관리 및 모니터링 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795697"
---
# Microsoft BitLocker 관리 및 모니터링 2.5

Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5는 BitLocker 드라이브 암호화를 관리 하는 데 사용할 수 있는 간단한 관리 인터페이스를 제공 합니다. 엔터프라이즈에 적합 한 BitLocker 드라이브 암호화 정책 옵션을 설정한 다음이를 사용 하 여 해당 정책에 대 한 클라이언트 준수를 모니터링할 수 있는 MBAM 그룹 정책 템플릿을 구성할 수 있습니다. 개별 컴퓨터와 엔터프라이즈 전체의 암호화 상태에 대 한 보고를 할 수도 있습니다. 또한 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있습니다. MBAM에 대 한 자세한 설명은 [mbam 2.5](about-mbam-25.md)을 참조 하세요.

MBAM을 얻으려면 MDOP를 [가져오는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop)을 참조 하세요.

## 개요

- <a href="" id="getting-started-with-mbam-2-5"></a>[MBAM 2.5 시작](getting-started-with-mbam-25.md)
  - [MBAM 2.5 정보](about-mbam-25.md)
  - [MBAM 2.5 릴리스 정보](release-notes-for-mbam-25.md)
  - [MBAM 2.5 SP1 정보](about-mbam-25-sp1.md)
  - [MBAM 2.5 SP1 릴리스 정보](release-notes-for-mbam-25-sp1.md)
  - [테스트 환경에서 MBAM 2.5 평가](evaluating-mbam-25-in-a-test-environment.md)
  - [MBAM 2.5의 개략적인 아키텍처](high-level-architecture-for-mbam-25.md)
  - [MBAM 2.5에 대한 접근성](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[MBAM 2.5 계획](planning-for-mbam-25.md)
  - [MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)
  - [MBAM 2.5 배포 필수 구성 요소](mbam-25-deployment-prerequisites.md)
  - [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)
  - [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md)
  - [MBAM 웹 사이트를 보호하는 방법 계획](planning-how-to-secure-the-mbam-websites.md)
  - [MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)
  - [MBAM 2.5 지원되는 구성](mbam-25-supported-configurations.md)
  - [MBAM 2.5 고가용성 계획](planning-for-mbam-25-high-availability.md)
  - [MBAM 2.5 보안 고려 사항](mbam-25-security-considerations.md)
  - [MBAM 2.5 계획 검사 목록](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[MBAM 2.5 배포](deploying-mbam-25.md)
  - [MBAM 2.5 서버 인프라 배포](deploying-the-mbam-25-server-infrastructure.md)
  - [MBAM 2.5 그룹 정책 개체 배포](deploying-mbam-25-group-policy-objects.md)
  - [MBAM 2.5 클라이언트 배포](deploying-the-mbam-25-client.md)
  - [MBAM 2.5 배포 검사 목록](mbam-25-deployment-checklist.md)
  - [이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [MBAM 서버 기능 또는 소프트웨어 제거](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[MBAM 2.5 작업](operations-for-mbam-25.md)
  - [MBAM 2.5 기능 관리](administering-mbam-25-features.md)
  - [MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)
  - [MBAM 2.5 유지 관리](maintaining-mbam-25.md)
  - [Windows PowerShell을 사용하여 MBAM 2.5 관리](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[MBAM 2.5 문제 해결](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[MBAM 2.5에 대한 기술 참조](technical-reference-for-mbam-25.md)
  - [클라이언트 이벤트 로그](client-event-logs.md)
  - [서버 이벤트 로그](server-event-logs.md)

## 추가 정보

- [MDOP 정보 환경](index.md)

  MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다.

- [MBAM 배포 가이드](https://www.microsoft.com/download/details.aspx?id=38398)

  각 방법에 대 한 단계별 지침을 포함 하 여 MBAM에 대 한 배포 방법을 선택 하는 방법에 대 한 도움말을 확인 하세요.
    
- [MBAM 2.5 SP1 서버에서 핫픽스 적용](apply-hotfix-for-mbam-25-sp1.md)

  MBAM 2.5 SP1 서버 핫픽스를 적용 하는 방법에 대 한 가이드
