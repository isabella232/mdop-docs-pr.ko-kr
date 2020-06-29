---
title: 환경 필수 구성 요소 구성
description: 환경 필수 구성 요소 구성
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826448"
---
# 환경 필수 구성 요소 구성


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0를 배포 하 고 실행 하려면 먼저 환경이 다음 최소 필수 조건을 충족 하는지 확인 해야 합니다.

**Windows 7**

MED-V 호스트 에이전트 및 MED-V 작업 영역 포장기는 Windows 7 이상 버전 에서만 지원 됩니다.

**Windows XP SP3**

MED-V 게스트 에이전트는 Windows XP SP3 에서만 지원 됩니다.

**.NET Framework 3.5 SP1**

MED-V 호스트와 게스트 에이전트 및 MED-V 작업 영역 포장기에는 Microsoft .NET Framework 3.5 SP1이 필요 합니다.

**중요**  또한 [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) https://go.microsoft.com/fwlink/?LinkId=204950) 알려진 여러 응용 프로그램 호환성 문제를 해결 하는 업데이트 KB959209를 설치 해야 합니다.

 

**참고**  .NET Framework 3.5 SP1 및 업데이트 KB959209을 MED-V와 함께 사용 하기 위해 준비 하는 Windows 가상 PC 이미지에 수동으로 설치 해야 합니다. 그러나 호스트 컴퓨터에 Windows 7을 설치 하면 기본적으로 Microsoft .NET Framework 3.5 SP1 및 업데이트가 포함 됩니다.

 

**Active Directory 인프라**

그룹 정책은 Active Directory 환경에서 운영 체제, 응용 프로그램 및 사용자 설정의 중앙 집중화 된 관리 및 구성을 제공 합니다.

## 관련 항목


[설치 필수 구성 요소 구성](configure-installation-prerequisites.md)

[개략적인 아키텍처](high-level-architecturemedv2.md)

[MED-V 2.0 지원되는 구성](med-v-20-supported-configurations.md)

 

 





