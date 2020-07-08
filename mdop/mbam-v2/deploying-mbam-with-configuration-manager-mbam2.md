---
title: Configuration Manager에서 MBAM 배포
description: Configuration Manager에서 MBAM 배포
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823453"
---
# Configuration Manager에서 MBAM 배포


다음 절차에서는 microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager을 사용 하 여 microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포 하는 방법을 설명 [합니다. usingthe](getting-started---using-mbam-with-configuration-manager.md)권장 구성 권장 되는 구성은 하나 이상의 Microsoft BitLocker 관리 및 모니터링 서버에 관리 및 모니터링 기능을 설치 하 고 별도의 서버에 Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager를 설치 하는 것입니다.

설치를 시작 하기 전에 [Configuration manager를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 검토 하 여 configuration manager에서 mbam을 설치 하기 위한 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항을 충족 했는지 확인 합니다.

Configuration Manager 토폴로지로 MBAM을 다시 설치 해야 하는 경우 먼저 특정 Configuration Manager 개체를 제거 해야 합니다. 자세한 내용은 [기술 자료 문서](https://go.microsoft.com/fwlink/?LinkId=286306) 를 참조 하세요.

Configuration Manager를 사용 하 여 MBAM을 설치 하는 단계는 다음 범주로 분류 됩니다. 각 범주에 대 한 단계를 완료 하 여 설치를 완료 합니다.

## mof 파일을 만들거나 편집하는 방법


클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 하려면, **구성 .mof** 파일을 편집 하 고 사용 중인 configuration Manager 버전에 따라 Sms \ _def .mof 파일을 편집 하거나 만들어야 합니다.

[mof 파일을 만들거나 편집하는 방법](how-to-create-or-edit-the-mof-files.md)

## Configuration Manager를 사용하여 MBAM을 설치하는 방법


이 섹션에서는 다음을 설치 하는 방법에 대 한 단계를 제공 합니다. MBAM이 Configuration Manager 서버에 있습니다. 데이터베이스 서버의 복구 및 감사 데이터베이스 관리 및 모니터링 서버에서 관리 및 모니터링 서버 기능을 제공 합니다.

[Configuration Manager를 사용하여 MBAM을 설치하는 방법](how-to-install-mbam-with-configuration-manager.md)

## Configuration Manager 서버에서 MBAM 서버 기능 설치의 유효성을 검사 하는 방법


Microsoft BitLocker 관리 및 모니터링 설치가 완료 되 면 설치에서 Configuration Manager 서버에 필요한 모든 MBAM 기능을 성공적으로 설정 했는지 확인 합니다.

[Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## 관련 항목


[Configuration Manager와 함께 MBAM 사용](using-mbam-with-configuration-manager.md)

 

 





