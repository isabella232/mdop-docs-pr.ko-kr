---
title: MBAM 1.0 클라이언트 배포
description: MBAM 1.0 클라이언트 배포
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822903"
---
# MBAM 1.0 클라이언트 배포


관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다. Active Directory 도메인 서비스 등의 도구를 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터를 직접 암호화 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.

MBAM 클라이언트를 배포 하는 경우 최종 사용자가 컴퓨터를 받을 전이나 후에 조직의 컴퓨터에서 BitLocker 암호화를 사용 하도록 설정할 수 있습니다. 이 타이밍을 제어 하려면 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 그룹 정책을 구성 하 고 MBAM 클라이언트 소프트웨어를 배포 합니다.

조직에서 이러한 메서드 중 하나 또는 모두를 사용할 수 있습니다. 두 방법을 모두 사용 하는 경우 준수, 보고 및 키 복구 지원을 향상 시킬 수 있습니다.

## 데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포


그룹 정책을 구성한 후에는 대상 컴퓨터에 MBAM 클라이언트 설치 Windows Installer 파일을 배포할 수 있습니다. Microsoft System Center 2012 구성 관리자 또는 Active Directory 도메인 서비스와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여이 작업을 수행할 수 있습니다. 사용할 수 있는 두 개의 MBAM 클라이언트 설치 Windows Installer 파일은 MBAMClient-64bit.msi 및 MBAMClient-32bit.msi입니다. 이러한 파일은 MBAM 소프트웨어와 함께 제공 됩니다. MBAM 그룹 정책 개체를 배포 하는 방법에 대 한 자세한 내용은 [mbam 1.0 그룹 정책 개체 배포](deploying-mbam-10-group-policy-objects.md)를 참조 하세요.

[데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## Windows 배포의 일부로 MBAM 클라이언트 배포


일부 조직에서는 새 컴퓨터가 중앙에서 수신 및 구성 됩니다. 이러한 상황에서는 관리자가 컴퓨터에 모든 사용자 데이터를 기록 하기 전에 MBAM 클라이언트를 설치 하 여 각 컴퓨터에서 BitLocker 암호화를 관리할 수 있습니다. 이 방법은 관리자가 최종 사용자 작업에 의존 하지 않고 작업을 수행 하기 때문에 컴퓨터가 적절 하 게 암호화 되도록 하는 데 도움이 됩니다. 이 시나리오의 주요 전제는 사용자에 게 컴퓨터를 전달 하기 전에 조직의 정책이 회사 Windows 이미지를 설치 하는 것입니다.

[Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## MBAM 클라이언트 배포에 대 한 기타 리소스


[MBAM 1.0 배포](deploying-mbam-10.md)

[MBAM 1.0 클라이언트 배포 계획](planning-for-mbam-10-client-deployment.md)

 

 





