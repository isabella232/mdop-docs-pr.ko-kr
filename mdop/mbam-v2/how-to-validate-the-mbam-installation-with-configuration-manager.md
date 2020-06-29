---
title: Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법
description: Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822638"
---
# Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법


Configuration Manager와 함께 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치한 후 다음 단계를 완료 하 여 해당 설치가 MBAM에 대해 필요한 모든 기능을 성공적으로 설정 했는지 확인 합니다.

**구성 관리자를 사용 하 여 MBAM 서버 기능 설치의 유효성을 검사 하려면**

1.  System Center Configuration Manager를 배포 하는 서버에서 **제어판**을 엽니다. 프로그램을 제거 하거나 변경 하는 데 사용 되는 프로그램을 선택 합니다. **Microsoft BitLocker 관리 및 모니터링** 이 프로그램 및 기능 목록에 표시 되는지 확인 합니다.

    **참고**  설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.

     

2.  Configuration Manager 콘솔을 사용 하 여 "MBAM 지원 컴퓨터" 라는 새 컬렉션이 표시 되는지 확인 합니다.

    Configuration Manager 2007에서 컬렉션을 보려면 **사이트 데이터베이스** ( &lt; **SiteCode** &gt;  -  &lt; **ServerName** &gt; , &lt; **SiteName** &gt; ), **컴퓨터 관리**를 차례로 클릭 합니다.

    SystemCenter2012 ConfigurationManager를 사용 하 여 컬렉션을 보려면 다음을 수행 합니다. **자산 및 준수** 작업 영역, **장치 모음**을 클릭 합니다.

3.  Configuration Manager 콘솔을 사용 하 여 다음 보고서가 **Mbam** 폴더에 나열 되어 있는지 확인 합니다.

    -   BitLocker 컴퓨터 준수

    -   BitLocker 엔터프라이즈 준수 대시보드

    -   BitLocker 엔터프라이즈 준수 세부 정보

    -   BitLocker Enterprise 규정 준수 요약

    구성 관리자 2007를 사용 하 여 보고서를 보려면 **reporting**, **reporting Services**, \\ \ \ &lt; **서버 이름** &gt; , **보고서 폴더** 를 클릭 합니다.

    SystemCenter2012 ConfigurationManager를 사용 하 여 보고서를 보려면 **모니터링** 작업 영역, **보고**, **보고서**를 차례로 클릭 합니다.

4.  Configuration Manager 콘솔을 사용 하 여 구성 기준 "BitLocker Protection"이 나열 되는지 확인 합니다.

    구성 관리자 2007를 사용 하 여 구성 기준을 보려면 **원하는 구성 관리**, **구성 기준을**클릭 합니다.

    SystemCenter2012 ConfigurationManager를 사용 하 여 구성 기준을 보려면 **자산 및 준수** 작업 영역, **준수 설정**, **구성 기준을**클릭 합니다.

5.  Configuration Manager 콘솔을 사용 하 여 다음과 같은 새 구성 항목이 표시 되는지 확인 합니다.

    -   BitLocker 고정 데이터 드라이브 보호

    -   BitLocker 운영 체제 드라이브 보호

    구성 관리자 2007를 사용 하 여 구성 항목을 보려면 **원하는 구성 관리**인 **구성 항목**을 클릭 합니다.

    SystemCenter2012 ConfigurationManager를 사용 하 여 구성 항목을 보려면 **자산 및 준수** 작업 영역, **준수 설정**, **구성 항목**을 클릭 합니다.

## 관련 항목


[Configuration Manager에서 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





