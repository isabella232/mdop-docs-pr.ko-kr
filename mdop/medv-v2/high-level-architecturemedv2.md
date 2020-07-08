---
title: 개략적인 아키텍처
description: 개략적인 아키텍처
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827293"
---
# 개략적인 아키텍처


이 섹션에서는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0의 상위 수준 시스템 아키텍처 및 구성 요소 디자인에 대해 설명 합니다.

## 시스템 아키텍처


MED-V는 Windows 가상 PC를 사용 하 여 한 장치에서 두 운영 체제를 실행 하 여 가상 이미지 배달, 그룹 정책 기반 프로비저닝, 중앙 집중식 관리를 추가 합니다. MED-V를 사용 하 여 Windows 7 Professional, Enterprise 또는 Windows 7 Ultimate를 실행 하는 모든 Windows 기반 데스크톱에서 회사 Windows 가상 PC 이미지를 쉽게 구성, 배포 및 관리할 수 있습니다. MED-V 솔루션에는 다음 구성 요소가 포함 되어 있습니다.

<a href="" id="---------------med-v-host"></a> **MED-V 호스트**  
MED-V 호스트 에이전트, ESD (전자 소프트웨어 배포) 시스템, 레지스트리 관리 시스템, MED-V 게스트를 포함 하는 Windows 7 환경입니다. MED-V 호스트는 특정 설치 기능 및 시스템 정보를 처리할 수 있도록 MED-V 게스트와 상호 작용 합니다.

<a href="" id="-------------------med-v-host-agent"></a> **MED-V 호스트 에이전트**  
Med-v 게스트와 통신 하는 채널을 제공 하는 med-v 호스트에 포함 된 MED-V 소프트웨어입니다. 또한 처음 설치 및 응용 프로그램 게시와 같은 기능을 제공 합니다.

**참고**  MED-V와 필수 구성 요소가 설치 된 후 MED-V를 구성 해야 합니다. MED-V의 구성을 첫 번째 설정 이라고 합니다.

 

<a href="" id="esd-system"></a>**ESD 시스템**  
MED-V가 만드는 MED-V 작업 영역 패키지 파일을 배포 하 고 설치할 수 있는 기존 소프트웨어 배포 방법입니다.

<a href="" id="registry-management-system"></a>**레지스트리 관리 시스템**  
기존 그룹 정책 설정 및 기본 설정 관리 방법

<a href="" id="windows-virtual-pc-image"></a>**Windows 가상 PC 이미지**  
관리자가 정의한 가상 컴퓨터에는 다음 구성 요소가 포함 되어 있습니다.

<a href="" id="corporate-operating-system"></a>**기업 운영 체제**  
표준 기업 운영 체제.

<a href="" id="management-and-security-tools"></a>**관리 및 보안 도구**  
사용자의 표준 관리 및 보안 도구 (예: 바이러스 방지)

<a href="" id="-----------------------med-v-guest"></a> **MED-V 게스트**  
Windows 7에서 실행 되는 windows XP SP3 환경으로 다음 구성 요소를 포함 합니다.

<a href="" id="---------------------------med-v-guest-agent"></a> **MED-V 게스트 에이전트**  
Med-v 호스트와 통신 하는 채널을 제공 하는 med-v 게스트에 포함 된 MED-V 소프트웨어입니다. 이는 또한 MED-V 호스트 에이전트에 게 최초 설정 수행 등의 기능을 지원 합니다.

**참고**  MED-V 게스트 에이전트는 처음 설정 하는 동안 자동으로 설치 됩니다.

 

<a href="" id="esd-client"></a>**ESD 클라이언트**  
소프트웨어 패키지를 설치 하 고 ESD 시스템에 상태를 보고 하는 ESD 시스템의 선택적 부분입니다.

## 관련 항목


[응용 프로그램 운영 체제 호환성 계획](planning-for-application-operating-system-compatibility.md)

[MED-V 배포 환경 준비](prepare-the-deployment-environment-for-med-v.md)

 

 





