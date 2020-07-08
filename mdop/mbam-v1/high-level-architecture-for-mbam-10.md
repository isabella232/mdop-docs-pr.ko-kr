---
title: MBAM 1.0의 개략적인 아키텍처
description: MBAM 1.0의 개략적인 아키텍처
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825238"
---
# MBAM 1.0의 개략적인 아키텍처


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 프로비저닝 및 배포를 간소화 하 고, BitLocker 준수 및 보고 기능을 개선 하 고, 지원 비용을 줄이는 데 도움이 되는 클라이언트/서버 데이터 암호화 솔루션입니다. MBAM에는이 항목에서 설명 하는 기능이 포함 되어 있습니다.

또한 MBAM 아키텍처와 MBAM 설정에 대 한 개요를 제공 하는 비디오가 있습니다. 자세한 내용은 [Mbam 배포 및 아키텍처 개요](https://go.microsoft.com/fwlink/p/?LinkId=258392)를 참조 하세요.

## 아키텍처 개요


다음 다이어그램에는 MBAM 아키텍처가 표시 됩니다. MBAM 기능을 소개 하는 단일 서버 MBAM 배포 토폴로지가 표시 됩니다. 그러나이 MBAM 배포 토폴로지는 랩 환경에만 권장 됩니다.

**참고**  프로덕션 배포에는 최소 3 대의 컴퓨터 MBAM 배포 토폴로지가 권장 됩니다. MBAM 배포 토폴로지에 대 한 자세한 내용은 [mbam 1.0 서버 인프라 배포](deploying-the-mbam-10-server-infrastructure.md)를 참조 하세요.

 

![mbam 단일 서버 배포 토폴로지](images/mbam-1-server.jpg)

1.  **관리 및 모니터링 서버**. MBAM 관리 및 모니터링 서버는 Windows Server에 설치 되어 있으며 MBAM 관리 및 관리 웹 사이트와 모니터링 웹 서비스를 호스팅합니다. MBAM 관리 및 관리 웹 사이트는 엔터프라이즈 준수 상태를 확인 하 고, 활동을 감사 하 고, 하드웨어 기능을 관리 하 고, BitLocker 복구 키와 같은 복구 데이터에 액세스 하는 데 사용 됩니다. 관리 및 모니터링 서버는 다음 데이터베이스 및 서비스에 연결 합니다.

    -   복구 및 하드웨어 데이터베이스. 복구 및 하드웨어 데이터베이스가 Windows 기반 서버 및 지원 되는 SQLServer 인스턴스에 설치 되어 있습니다. 이 데이터베이스는 MBAM 클라이언트 컴퓨터에서 수집 된 복구 데이터 및 하드웨어 정보를 저장 합니다.

    -   준수 및 감사 데이터베이스. 준수 및 감사 데이터베이스가 Windows server 및 지원 되는 SQLServer 인스턴스에 설치 되어 있습니다. 이 데이터베이스는 MBAM 클라이언트 컴퓨터에 대 한 규정 준수 데이터를 저장 합니다. 이 데이터는 주로 SSRS (SQL Server Reporting Services)에서 호스팅되는 보고서에 사용 됩니다.

    -   준수 및 감사 보고서. 규정 준수 및 감사 보고서는 SSRS 기능이 설치 된 Windows 기반 서버 및 지원 되는 SQLServer 인스턴스에 설치 됩니다. 이러한 보고서는 Microsoft BitLocker 관리 및 모니터링 보고서를 제공 합니다. 이 보고서는 MBAM 관리 및 관리 웹 사이트에서 또는 SSRS 서버에서 직접 액세스할 수 있습니다.

2.  **Mbam 클라이언트**. Microsoft BitLocker 관리 및 모니터링 클라이언트는 다음 작업을 수행 합니다.

    -   그룹 정책을 사용 하 여 엔터프라이즈에서 클라이언트 컴퓨터의 BitLocker 암호화를 적용 합니다.

    -   세 가지 BitLocker 데이터 드라이브 유형 (운영 체제 드라이브, 고정 데이터 드라이브, 이동식 데이터 (USB) 드라이브)에 대 한 복구 키를 수집 합니다.

    -   클라이언트 컴퓨터에 대 한 복구 정보 및 하드웨어 정보를 수집 합니다.

    -   컴퓨터에 대 한 규정 준수 데이터를 수집 하 고 보고 시스템으로 데이터를 전달 합니다.

3.  **정책 서식 파일**. MBAM 그룹 정책 템플릿은 지원 되는 Windows 기반 서버 또는 클라이언트 컴퓨터에 설치 되어 있습니다. 이 템플릿은 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 지정 하는 데 사용 됩니다.

## 관련 항목


[MBAM 1.0 시작](getting-started-with-mbam-10.md)

 

 





