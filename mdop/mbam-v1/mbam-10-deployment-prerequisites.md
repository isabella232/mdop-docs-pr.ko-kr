---
title: MBAM 1.0 배포 필수 구성 요소
description: MBAM 1.0 배포 필수 구성 요소
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822663"
---
# MBAM 1.0 배포 필수 구성 요소


Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하는 데 필요한 필수 구성 요소를 충족 하는지 확인 합니다. 이 섹션에서는 MBAM 클라이언트 및 서버 기능을 배포 하기 전에 컴퓨팅 환경을 성공적으로 준비 하는 데 도움이 되는 정보를 제공 합니다.

## MBAM 서버 기능에 대 한 설치 필수 조건


각 MBAM 서버 기능에는 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다. MBAM 설정 설치를 시작 하기 전에 모든 필수 구성 요소를 충족 하는지 확인 합니다.

### 관리 및 모니터링 서버용 설치 필수 조건

다음 표에는 MBAM 관리 및 모니터링 서버의 설치 필수 구성 요소가 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows ServerWeb 서버 역할</strong></p></td>
<td align="left"><p>이 역할은 mbam 관리 및 모니터링 서버 기능에 대해 지원 되는 서버 운영 체제에 추가 되어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>웹 서버 (IIS) 관리 도구</strong></p></td>
<td align="left"><p><strong>IIS 관리 스크립트 및 도구</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>웹 서버 역할 서비스</strong></p></td>
<td align="left"><p><strong>일반적인 HTTP 기능:</strong></p>
<ul>
<li><p>정적 콘텐츠</p></li>
<li><p>기본 문서</p></li>
</ul>
<p><strong>응용 프로그램 개발:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET 확장성</p></li>
<li><p>ISAPI 확장</p></li>
<li><p>ISAPI 필터</p></li>
</ul>
<p><strong>보안이</strong></p>
<ul>
<li><p>Windows 인증</p></li>
<li><p>요청 필터링</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Server 기능</strong></p></td>
<td align="left"><p><strong>Microsoft .NET Framework 3.5.1 기능:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>WCF 활성화</p>
<ul>
<li><p>HTTP 활성화</p></li>
<li><p>비 HTTP 활성화</p></li>
</ul></li>
</ul>
<p><strong>Windows Process Activation Service</strong></p>
<ul>
<li><p>프로세스 모델</p></li>
<li><p>.NET 환경</p></li>
<li><p>구성 Api</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**참고**  지원 되는 운영 체제 목록은 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.

 

### 규정 준수 및 감사 보고서 설치 필수 조건

지원 되는 버전의 SQLServer에 준수 및 감사 보고서를 설치 해야 합니다. 이 기능의 설치 전제 조건에는 SQL Server Reporting Services (SSRS)가 포함 됩니다.

MBAM 서버 설치 중에 SSRS를 설치 하 고 실행 해야 합니다. SSRS는 "구성 되지 않음" 또는 "SharePoint" 모드가 아니라 "기본" 모드 에서도 구성 되어야 합니다.

**참고**  지원 되는 운영 체제 및 SQLServer 버전 목록은 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.

 

### 복구 및 하드웨어 데이터베이스용 설치 필수 조건

복구 및 하드웨어 데이터베이스는 지원 되는 버전의 SQLServer에 설치 되어 있어야 합니다.

SQL Server는 MBAM 서버 설치 중에 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다. TDE (투명 한 데이터 암호화) 기능을 사용 하도록 설정 해야 합니다.

**참고**  지원 되는 운영 체제 및 SQLServer 버전 목록은 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.

 

TDE SQLServer 기능은 실시간 입/출력 (I/o) 암호화 및 데이터 및 로그 파일의 암호 해독을 수행 합니다. TDE는 데이터와 로그 파일을 포함 하 여 "rest" 인 데이터를 보호 합니다. 다양 한 업계에서 설정 된 여러 법률, 규정 및 지침을 준수 하는 기능을 제공 합니다.

**참고**  TDE는 데이터베이스 정보에 대 한 실시간 암호 해독을 수행 하기 때문에 로그인 하는 계정에 복구 키 정보 SQL 테이블을 볼 때 데이터베이스에 대 한 사용 권한이 있는 경우 복구 키 정보가 표시 됩니다.

 

### 준수 및 감사 데이터베이스에 대 한 설치 필수 조건

준수 및 감사 데이터베이스는 지원 되는 버전의 SQLServer에 설치 되어 있어야 합니다.

SQL Server는 MBAM 서버 설치 중에 데이터베이스 엔진 서비스를 설치 하 고 실행 해야 합니다.

**참고**  지원 되는 운영 체제 및 SQLServer 버전 목록은 [Mbam 1.0 지원 구성을](mbam-10-supported-configurations.md)참조 하세요.

 

## MBAM 클라이언트에 대 한 설치 필수 조건


MBAM 클라이언트 설치를 시작 하기 전에 충족 해야 하는 필수 구성 요소는 다음과 같습니다.

-   TPM (신뢰할 수 있는 플랫폼 모듈) v 1.2의 기능

-   TPM 칩이 BIOS에서 켜져 있어야 하며 운영 체제에서 재설정 가능 해야 합니다. 자세한 내용은 BIOS 설명서를 참조 하세요.

**경고가**  키보드, 마우스 및 비디오가 키보드, 비디오, 마우스 (KVM) 스위치 대신 컴퓨터에 직접 연결 되어 있는지 확인 합니다. KVM 스위치는 컴퓨터의 실제 현재 상태를 감지 하는 기능을 방해할 수 있습니다.

 

## 관련 항목


[MBAM 1.0 배포 계획](planning-to-deploy-mbam-10.md)

[MBAM 1.0 지원되는 구성](mbam-10-supported-configurations.md)

 

 





