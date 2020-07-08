---
title: 개략적인 아키텍처
description: 개략적인 아키텍처
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826203"
---
# 개략적인 아키텍처


MED-V 솔루션은 다음과 같은 요소로 이루어져 있습니다.

-   **관리자 정의 가상 컴퓨터**-운영 체제, 응용 프로그램, 선택적 관리 및 보안 도구를 포함 하 여 전체 데스크톱 환경을 캡슐화 합니다.

-   **이미지 리포지토리**-모든 가상 이미지를 표준 IIS 서버에 저장 하 고 가상 이미지 버전 관리, 클라이언트 인증 이미지 검색, 그리고 트리밍 전송 기술을 통해 새 이미지 또는 업데이트의 효율적인 다운로드를 사용할 수 있도록 합니다.

-   **관리 서버**-이미지 리포지토리의 가상 이미지를 관리자 사용 정책과 함께 Active Directory® 사용자 또는 그룹과 연결 합니다. 또한 관리 서버는 모니터링 및 보고 목적으로 클라이언트의 이벤트를 집계 하 고 외부 데이터베이스 (Microsoft SQL Server®)에 저장 합니다.

-   **관리 콘솔**-관리자가 관리 서버 및 이미지 리포지토리를 제어할 수 있도록 합니다.

-   **최종 사용자 클라이언트**

    1.  가상 이미지 수명 주기? 인증, 이미지 검색, 사용 정책 적용.

    2.  가상 컴퓨터 세션 관리-가상 컴퓨터를 시작 하 고 중지 하 고 잠급니다.

    3.  단일 데스크톱 환경-가상 컴퓨터에 설치 된 응용 프로그램을 표준 데스크톱 시작 메뉴를 통해 원활 하 게 사용 하 고 사용자 데스크톱의 다른 응용 프로그램과 통합할 수 있습니다.

클라이언트와 서버 (관리 서버 및 이미지 저장소) 간의 모든 통신은 표준 HTTP 또는 HTTPS 채널의 맨 위에 전달 됩니다.

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





