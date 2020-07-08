---
title: Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소
description: Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812564"
---
# Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소


System Center Configuration Manager 통합 기능을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 설치 하는 경우 [독립 실행형 및 구성 관리자 통합 토폴로지에 대해 mbam 2.5 Server 필수 구성 요소와](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)함께이 항목에서 설명 하는 필수 구성 요소를 완료 해야 합니다. 또한 Configuration Manager 통합 토폴로지에 필요한 .mof 파일을 만들거나 수정 해야 합니다.

## Configuration Manager 통합 기능의 필수 구성 요소


System Center Configuration Manager 통합 토폴로지로 MBAM을 구성 하는 경우에는 구성 관리자에 필요한 추가 필수 구성 요소를 완료 해야 합니다.

[Configuration Manager 통합 기능의 필수 구성 요소](prerequisites-for-the-configuration-manager-integration-feature.md)

## 구성 .mof 파일 편집


클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면 SystemCenter2012 ConfigurationManager 및 Microsoft System Center Configuration Manager 2007에 대 한 구성. mof 파일을 편집 해야 합니다.

[Configuration.mof 파일 편집](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Sms \ _def .mof 파일 만들기 또는 편집


클라이언트 컴퓨터가 MBAM Configuration Manager 보고서에서 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면, Sms \ _def .mof 파일을 만들거나 편집 해야 합니다. SystemCenter2012 ConfigurationManager를 사용 하는 경우에는 파일을 만들어야 합니다. Configuration Manager 2007에서 파일이 이미 있으므로 기존 파일을 편집 하 고 덮어쓰지 않아도 됩니다.

[Sms \ _def .mof 파일 만들기 또는 편집](create-or-edit-the-sms-defmof-file-mbam-25.md)


## 관련 항목


[MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)

[MBAM 2.5 지원되는 구성](mbam-25-supported-configurations.md)

[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)

 

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




