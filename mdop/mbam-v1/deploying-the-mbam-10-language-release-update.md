---
title: MBAM 1.0 언어 릴리스 업데이트 배포
description: MBAM 1.0 언어 릴리스 업데이트 배포
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812825"
---
# MBAM 1.0 언어 릴리스 업데이트 배포


Microsoft BitLocker 관리 및 모니터링 (MBAM) 1.0 언어 릴리스는 MBAM에 대 한 업데이트 이며 새 언어에 대 한 지원을 포함 합니다. 새로운 언어는 다음과 같습니다.

-   영어 (en-us)

-   프랑스어 (fr)

-   이탈리아어 (it)

-   독일어 (de)

-   스페인어 (es)

-   한국어 (ko-kr)

-   일본어 (ja-jp)

-   포르투갈어 (브라질) (pt-br)

-   러시아어 (가)

-   중국어 번체 (zh-cn-hy)

-   중국어 간체 (zh-cn-cn)

MBAM 1.0 언어 업데이트는 버전 번호를 MBAM 1.0.1237.1에서 MBAM 1.0.2001로 변경 합니다.

이러한 추가 언어를 추가 하기 위해 모든 MBAM 기능을 다시 설치할 필요는 없습니다. 이 항목에서는 새로 지원 되는 언어를 추가 하는 데 필요한 단계를 정의 합니다.

## MBAM 서버 기능에 MBAM 국제 릴리스 배포


시작 하려면 다음 MBAM 서버 기능을 업데이트 해야 합니다.

-   준수 및 감사 보고서

-   관리 및 모니터링 서버

-   정책 서식 파일

그런 다음 동일한 서버에서 동시에 실행 되는 MBAM 기능을 업그레이드 하려면 **MbamSetup.exe** 를 실행 해야 합니다.

[단일 서버에서 MBAM 언어 업데이트를 설치하는 방법](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[분산 서버에 MBAM 언어 업데이트를 설치하는 방법](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## 그룹 정책에 대해 MBAM 언어 업데이트 설치


MBAM 그룹 정책 서식 파일을 각 관리 워크스테이션에 설치 하거나 그룹 정책 중앙 저장소에 복사 하 여 모든 그룹 정책 관리자가 해당 템플릿을 사용할 수 있도록 할 수 있습니다. 도메인 컨트롤러에는 정책 서식 파일을 직접 설치할 수 없습니다. 그룹 정책 중앙 저장소를 사용 하지 않는 경우에는 MBAM 그룹 정책을 관리 하는 각 도메인 컨트롤러에 정책을 수동으로 복사 해야 합니다.

MBAM 언어 정책 템플릿을 추가 하려면 "정책 템플릿" 역할이 설치 된 컴퓨터 의%SystemRoot%\\PolicyDefinitions에서 그룹 정책 언어 파일을 워크스테이션 컴퓨터의 동일한 위치에 복사 합니다. 다음은 그룹 정책 파일의 몇 가지 예입니다.

-   BitLockerManagement. admx

-   BitLockerUserManagement. admx

-   en-us\\BitLockerManagement.adml

-   en-us\\BitLockerUserManagement.adml

-   fr-fr\\ BitLockerManagement. adml

-   fr-fr\\ BitLockerUserManagement. adml

-   (및 각각의 지원 되는 언어에 대해 유사)

## MBAM 국제 릴리스의 알려진 문제점


이 항목에서는 Microsoft BitLocker 관리 및 국제 릴리스의 알려진 문제점에 대해 설명 합니다.

[MBAM 다국어 릴리스의 알려진 문제](known-issues-in-the-mbam-international-release-mbam-1.md)

## MBAM 1.0 언어 업데이트를 배포 하기 위한 기타 리소스


[MBAM 1.0 배포](deploying-mbam-10.md)

 

 





