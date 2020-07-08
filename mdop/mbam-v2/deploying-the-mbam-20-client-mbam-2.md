---
title: MBAM 2.0 클라이언트 배포
description: MBAM 2.0 클라이언트 배포
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823448"
---
# MBAM 2.0 클라이언트 배포


관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다. BitLocker 클라이언트는 Active Directory 도메인 서비스와 같은 전자 소프트웨어 배포 시스템을 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터를 직접 암호화 하 여 조직에 통합할 수 있습니다.

Microsoft BitLocker 관리 및 모니터링 클라이언트를 배포 하는 경우 최종 사용자가 컴퓨터를 받기 전에 또는 나중에 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MBAM 클라이언트 소프트웨어를 배포 하 고 그룹 정책을 구성 하 여 조직의 컴퓨터에서 BitLocker 암호화를 사용 하도록 설정할 수 있습니다.

## 데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포


그룹 정책을 구성한 후 Microsoft System Center Configuration Manager 2012 또는 Active Directory 도메인 서비스와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 대상 컴퓨터에 MBAM 클라이언트 설치 Windows Installer 파일을 배포할 수 있습니다. 32 비트 또는 64 비트 MbamClientSetup.exe 파일 또는 MBAM 소프트웨어와 함께 제공 되는 32 비트 또는 64 비트 MBAMClient.msi 파일을 사용 하 여 클라이언트를 배포할 수 있습니다. MBAM 그룹 정책 개체를 배포 하는 방법에 대 한 자세한 내용은 [mbam 2.0 그룹 정책 개체 배포](deploying-mbam-20-group-policy-objects-mbam-2.md)를 참조 하세요.

[데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## Windows 배포의 일부로 MBAM 클라이언트 배포


컴퓨터를 중앙에서 받고 구성 하는 조직에서 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 암호화를 관리할 수 있습니다. 이 프로세스의 장점은 모든 컴퓨터가 BitLocker 암호화 규격을 준수 한다는 것입니다. 관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다. 이 시나리오의 주요 전제는 사용자에 게 컴퓨터를 전달 하기 전에 조직의 정책이 회사 Windows 이미지를 설치 하는 것입니다. 그룹 정책이 PIN을 요구 하도록 구성 된 경우 사용자가 그룹 정책을 받은 후 PIN을 설정 하 라는 메시지가 표시 됩니다.

[Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## 명령줄을 사용하여 MBAM 클라이언트를 설치하는 방법


이 섹션에서는 명령줄을 사용 하 여 MBAM 클라이언트를 설치 하는 방법을 설명 합니다.

[명령줄을 사용하여 MBAM 클라이언트를 설치하는 방법](how-to-use-a-command-line-to-install-the-mbam-client.md)

## MBAM 클라이언트 배포에 대 한 기타 리소스


Mbam [2.0](deploying-mbam-20-mbam-2.md)[2.0 계획 배포 클라이언트 배포](planning-for-mbam-20-client-deployment-mbam-2.md)

 

 





