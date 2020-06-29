---
title: mof 파일을 만들거나 편집하는 방법
description: mof 파일을 만들거나 편집하는 방법
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825323"
---
# mof 파일을 만들거나 편집하는 방법


Configuration Manager를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하기 전에 구성 .mof 파일을 편집 해야 합니다. 또한 사용 중인 구성 관리자 버전에 따라 Sms \ _def .mof 파일을 편집 하거나 만들어야 합니다.

## Configuration.mof 파일 편집


클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 하려면 Microsoft System Center Configuration Manager 2007 및 SystemCenter2012 ConfigurationManager에 대 한 구성. mof 파일을 편집 해야 합니다.

[Configuration.mof 파일 편집](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Sms \ _def .mof 파일 만들기 또는 편집


클라이언트 컴퓨터가 MBAM Configuration Manager 보고서에서 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면, Sms \ _def .mof 파일을 만들거나 편집 해야 합니다. Configuration Manager 2007에서 파일이 이미 있으므로 기존 파일을 편집 하 고 덮어쓰지 않아도 됩니다. SystemCenter2012 ConfigurationManager를 사용 하는 경우에는 파일을 만들어야 합니다.

[Sms \ _def .mof 파일 만들기 또는 편집](create-or-edit-the-sms-defmof-file.md)

## 관련 항목


[Configuration Manager에서 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





