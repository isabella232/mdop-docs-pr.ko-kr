---
title: MED-V 1.0 릴리스 정보
description: MED-V 1.0 릴리스 정보
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826593"
---
# MED-V 1.0 릴리스 정보


## MED-V의 알려진 문제점


이 섹션에서는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 플랫폼의 일반적인 문제에 대 한 최신 정보를 제공 합니다. 이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다. 이러한 문제는 가능한 경우 이후 릴리스에서 해결 될 것입니다.

### 파일 다운로드는 웹 리디렉션 규칙을 따르지 않음

파일 다운로드는 MED-V 작업 영역 정책에 설정 된 웹 리디렉션 규칙을 따르지 않습니다.

### 콘솔에서 게시 된 응용 프로그램 창을 전체 화면으로 확장 하면 사라집니다.

원활한 통합 모드에서 구성 된 MED-V 작업 영역 내에서 콘솔에서 게시 된 응용 프로그램 (예: cmd.exe) 창을 전체 화면으로 확장 하면 응용 프로그램 창이 사라지거나 응답 하지 않을 수 있습니다.

### 전체 데스크톱 모드에서 작업 하는 경우 데스크톱의 아이콘 위치는 저장 되지 않습니다.

전체 데스크톱 모드로 작업할 때 데스크톱의 아이콘에 대 한 수동 위치 변경은 MED-V 작업 영역 세션 간에 저장 되지 않습니다.

### 동일한 도메인에 이름이 같은 로컬 이미지 및 테스트 이미지가 있을 수 없음

로컬 이미지가 도메인에 가입 되어 있고 관리자가 테스트 이미지와 컴퓨터 이름이 같은 새 버전의 동일한 이미지를 만드는 경우 테스트 이미지가 도메인에 가입 하면 도메인 참가 작업이 실패 하거나, 로컬 이미지가 도메인에서 제거 됩니다.

### MED-V는 Windows Aero 기능을 지원 하지 않습니다.

MED-V는 Windows Aero 기능 (예: Aero 플립 3D)을 지원 하지 않습니다.

### 관리 콘솔은 컴퓨터 당 하나의 Windows 사용자만 사용할 수 있습니다.

MED-V 관리 콘솔은 관리자와 관리 응용 프로그램을 설치한 Windows 사용자만 사용할 수 있습니다.

### MED-V 서버 구성 유틸리티는 MED-V 서버 서비스 컨텍스트가 아닌 사용자 컨텍스트에서 Microsoft SQL Server 연결을 테스트 합니다.

MED-V는 Microsoft SQL Server 보고서 데이터베이스에서 보고서를 수집 하는 데 MED-V 서버 서비스 컨텍스트를 사용 합니다. MED-V 서버 구성 유틸리티는 데이터베이스를 확인 하 고 데이터베이스 연결 문자열을 테스트 합니다. 데이터베이스에 대해 MED-V 서버 서비스에 대 한 액세스를 확인 하지 않습니다.

 

 





