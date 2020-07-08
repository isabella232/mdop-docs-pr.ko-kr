---
title: Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
description: Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825763"
---
# Configuration Manager 통합 토폴로지와 함께 MBAM 2.5의 상위 수준 아키텍처

이 항목에서는 Configuration Manager 통합 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포 하는 데 권장 되는 아키텍처에 대해 설명 합니다. 이 토폴로지는 MBAM을 System Center Configuration Manager와 통합 합니다. 독립 실행형 토폴로지에 MBAM을 배포 하려면 [독립 실행형 토폴로지와 함께 mbam 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)를 참조 하세요.

이 항목에 설명 된 소프트웨어의 지원 되는 버전 목록은 [Mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.

**중요**  Windows To Go는 Configuration Manager 2007를 사용 중인 경우 Configuration Manager 통합 토폴로지 설치에 대해 지원 되지 않습니다.

 

## 권장 서버 수 및 지원 되는 클라이언트 수


프로덕션 환경에서 권장 되는 서버 수 및 지원 되는 클라이언트 수는 다음과 같습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">권장 아키텍처</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>서버 및 다른 컴퓨터 수</p></td>
<td align="left"><p>3 대의 서버</p>
<p>하나의 워크스테이션</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원 되는 클라이언트 컴퓨터 수</p></td>
<td align="left"><p>50만</p></td>
</tr>
</tbody>
</table>

 

## 구성 관리자 통합 및 독립 실행형 토폴로지 간의 차이점


토폴로지 간의 주요 차이점은 다음과 같습니다.

-   준수 및 보고 기능은 MBAM에서 제거 되며 구성 관리자에서 액세스할 수 있습니다.

-   보고서는 MBAM 관리 및 모니터링 웹 사이트에서 계속 볼 수 있는 복구 감사 보고서에 대 한 예외를 포함 하 여 Configuration Manager 관리 콘솔에서 표시 됩니다.

## Configuration Manager 통합 토폴로지가 있는 권장 MBAM 상위 수준 아키텍처


다음 다이어그램 및 표에서는 Configuration Manager 통합 토폴로지와 함께 MBAM에 권장 되는 상위 수준 아키텍처에 대해 설명 합니다. MBAM 다중 포리스트 배포에는 단방향 또는 양방향 트러스트가 필요 합니다. 단방향 트러스트의 경우 서버 도메인이 클라이언트 도메인을 신뢰 해야 합니다.

![mbam2\-5](images/mbam2-5-cmserver.png)

### 데이터베이스 서버

#### 복구 데이터베이스

이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 컴퓨터에서 구성 됩니다.

**복구 데이터베이스** 는 Mbam 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.

#### 데이터베이스 감사

이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 컴퓨터에서 구성 됩니다.

**감사 데이터베이스** 는 복구 데이터에 액세스 한 클라이언트 컴퓨터에서 수집 된 감사 활동 데이터를 저장 합니다.

#### 보고

이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 컴퓨터에서 구성 됩니다.

**보고서** 는 엔터프라이즈의 클라이언트 컴퓨터에 대 한 복구 감사 데이터를 제공 합니다. Configuration Manager 콘솔에서 또는 SQL Server Reporting Services에서 직접 보고서를 볼 수 있습니다.

### Configuration Manager 주 사이트 서버

System Center Configuration Manager 통합 기능

-   이 기능은 configuration manager 인프라의 최상위 계층 서버인 Configuration Manager 기본 사이트 서버에서 구성 됩니다.

-   **Configuration Manager 서버** 는 클라이언트 컴퓨터에서 하드웨어 인벤터리 정보를 수집 하 고 클라이언트 컴퓨터의 BitLocker 규격을 보고 하는 데 사용 됩니다.

-   Microsoft BitLocker 관리 및 모니터링 설정 마법사를 실행 하 여 서버 소프트웨어를 설치 하는 경우 MBAM 지원 컴퓨터 모음, 구성 기준 및 보고서가 Configuration Manager 기본 사이트 서버에 구성 됩니다.

-   **Configuration Manager 콘솔** 은 Mbam 서버 소프트웨어를 설치 하는 동일한 컴퓨터에 설치 해야 합니다.

### 관리 및 모니터링 서버

#### 관리 및 모니터링 웹 사이트

이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.

**관리 및 모니터링 웹 사이트** 는 다음 작업을 수행 하는 데 사용 됩니다.

-   최종 사용자가 잠겨 있는 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있도록 지원 합니다. (이 웹 사이트의이 영역을 일반적으로 지원 센터 라고 합니다.)

-   클라이언트 컴퓨터에 대 한 복구 작업을 보여 주는 복구 감사 보고서를 봅니다. 다른 보고서는 Configuration Manager 콘솔에서 볼 수 있습니다.

#### 셀프 서비스 포털

이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.

**셀프 서비스 포털** 은 클라이언트 컴퓨터의 최종 사용자가 자신의 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 사용 하 여 개별적으로 웹 사이트에 로그온 할 수 있도록 하는 웹 사이트입니다.

#### 이 웹 사이트의 웹 서비스 모니터링

이 기능은 Windows Server를 실행 하는 컴퓨터에 설치 되어 있습니다.

**모니터링 웹 서비스** 는 Mbam 클라이언트와 웹 사이트에서 데이터베이스와 통신 하는 데 사용 됩니다.

**중요**<br>MBAM 웹 사이트는 복구 데이터베이스와 직접 통신 하므로 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1에서는 모니터링 웹 서비스를 더 이상 사용할 수 없습니다. 

 

### 관리 워크스테이션

#### MBAM 그룹 정책 서식 파일

-   **Mbam 그룹 정책 템플릿은** mbam에 대 한 구현 설정을 정의 하는 그룹 정책 설정으로, BitLocker 드라이브 암호화를 관리할 수 있습니다.

-   MBAM을 실행 하기 전에, [MDOP 그룹 정책 (admx) 템플릿을 가져오고](https://go.microsoft.com/fwlink/p/?LinkId=393941) 지원 되는 Windows Server 또는 Windows 운영 체제를 실행 하는 서버 또는 워크스테이션에 복사 하는 방법에서 그룹 정책 템플릿을 다운로드 해야 합니다.

    **참고**<br>워크스테이션이 전용 컴퓨터 일 필요는 없습니다.

     

### MBAM 클라이언트 및 Configuration Manager 클라이언트 컴퓨터

#### MBAM 클라이언트 소프트웨어

**Mbam 클라이언트**:

-   그룹 정책 개체를 사용 하 여 엔터프라이즈의 클라이언트 컴퓨터에 BitLocker 드라이브 암호화를 적용 합니다.

-   운영 체제 드라이브, 고정 데이터 드라이브, 이동식 (USB) 데이터 드라이브 등 세 가지 데이터 드라이브 유형의 BitLocker 복구 키를 수집 합니다.

-   클라이언트 컴퓨터에 대 한 복구 정보 및 컴퓨터 정보를 수집 합니다.

#### 구성 관리자 클라이언트

Configuration manager **클라이언트** 는 구성 관리자가 클라이언트 컴퓨터에 대 한 하드웨어 호환성 데이터를 수집 하 고 규정 준수 정보를 보고할 수 있도록 합니다.

 

## 지원 되는 Configuration Manager 버전에 대 한 MBAM 배포의 차이점


Configuration Manager 통합 토폴로지로 MBAM을 배포 하는 경우 기본 사이트 서버에 MBAM을 설치할 수 있습니다. 그러나 MBAM 설치는 시스템 Center2012 구성 관리자 및 구성 Manager2007에 따라 다르게 작동 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration Manager 버전</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>System Center2012 R2 구성 관리자</p>
<p>시스템 Center2012 구성 관리자</p></td>
<td align="left"><p>주 사이트 서버 또는 중앙 관리 서버에 MBAM을 설치 하는 경우 MBAM은 해당 사이트 서버에서 모든 설치 작업을 수행 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>구성 Manager2007 R2</p>
<p>구성 Manager2007</p></td>
<td align="left"><p>중앙 사이트 상위 서버를 사용 하 여 더 큰 구성 관리자 계층 구조의 일부인 주 사이트 서버에 MBAM을 설치 하는 경우 MBAM은 중앙 사이트 상위 서버를 식별 하 고 해당 상위 서버의 모든 설치 작업을 수행 합니다. 설치에는 필수 조건을 확인 하 고 Configuration Manager 개체 및 보고서를 설치 하는 작업이 포함 됩니다.</p>
<p>예를 들어, 중앙 사이트 상위 서버의 자식인 주 사이트 서버에 MBAM을 설치 하는 경우 MBAM은 상위 서버에 모든 Configuration Manager 개체와 보고서를 설치 합니다. 부모 서버에 MBAM을 설치 하는 경우 MBAM은 해당 상위 서버의 모든 설치 작업을 수행 합니다.</p></td>
</tr>
</tbody>
</table>

 

## MBAM이 구성 관리자와 작동 하는 방식


Configuration Manager와 MBAM의 통합은 다음 표에 설명 된 항목을 설치 하는 구성 팩을 기반으로 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration Manager에 설치 된 항목</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>구성 데이터</p></td>
<td align="left"><p>구성 데이터는 두 개의 구성 항목을 포함 하는 "BitLocker Protection" 이라는 구성 기준을 설치 합니다.</p>
<ul>
<li><p>BitLocker 운영 체제 드라이브 보호</p></li>
<li><p>BitLocker 고정 데이터 드라이브 보호</p></li>
</ul>
<p>구성 기준은 MBAM이 설치 되어 있는 경우에도 만들어지는 MBAM 지원 컴퓨터 컬렉션에 배포 됩니다.</p>
<p>두 개의 구성 항목은 클라이언트 컴퓨터의 준수 상태를 평가 하기 위한 기반을 제공 합니다. 이 정보는 구성 관리자에서 캡처, 저장 및 평가 됩니다.</p>
<p>구성 항목은 운영 체제 드라이브 및 고정 데이터 드라이브에 대 한 규정 준수 요구 사항에 기반을 둔 것입니다. 이러한 드라이브 유형에 대 한 준수를 평가할 수 있도록 배포 된 컴퓨터에 대 한 필수 세부 정보가 수집 됩니다.</p>
<p>기본적으로 구성 기준은 준수 상태 every12 시간을 평가 하 고 규정 준수 데이터를 구성 관리자에 게 보냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 지원 컴퓨터 모음</p></td>
<td align="left"><p>MBAM 지원 컴퓨터 라고 하는 컬렉션을 만듭니다. 구성 기준은이 컬렉션에 있는 클라이언트 컴퓨터를 대상으로 합니다.</p>
<p>이것은 동적 컬렉션입니다. 기본적으로 every12 시간을 실행 하 고 다음 세 가지 조건을 기준으로 멤버 자격을 평가 합니다.</p>
<ul>
<li><p>컴퓨터가 지원 되는 Windows 운영 체제 버전입니다.</p></li>
<li><p>컴퓨터가 물리적 컴퓨터입니다. 가상 머신은 지원 되지 않습니다.</p></li>
<li><p>컴퓨터에 사용할 수 있는 TPM (신뢰할 수 있는 플랫폼 모듈)이 있습니다. Windows7에 대해 호환 되는 버전의 TPM 1.2 이상이 필요 합니다. Windows10, Windows 8.1, Windows8 및 Windows To Go는 TPM이 필요 하지 않습니다.</p></li>
</ul>
<p>컬렉션이 모든 컴퓨터에 대해 평가 되 고 호환 컴퓨터의 하위 집합이 만들어지고, 준수 평가 및 MBAM 통합에 대 한 보고를 위한 기반을 제공 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>보고</p></td>
<td align="left"><p>Configuration Manager 통합 토폴로지로 MBAM을 구성 하는 경우 복구 감사 보고서를 제외한 모든 보고서를 볼 수 있으며,이는 MBAM 관리 및 모니터링 웹 사이트에서 계속 볼 수 있습니다. Configuration Manager에서 사용할 수 있는 보고서는 다음과 같습니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">보고서</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>BitLocker 엔터프라이즈 준수 대시보드</p></td>
<td align="left"><p>IT 관리자에 게 단일 보고서 (준수 상태 배포, 비규격-오류 배포, 드라이브 유형별 준수 상태 배포)의 세 가지 정보 보기를 제공 합니다. 보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker 엔터프라이즈 준수 세부 정보</p></td>
<td align="left"><p>IT 관리자가 엔터프라이즈의 BitLocker 암호화 준수 상태에 대 한 정보를 볼 수 있으며 각 컴퓨터에 대 한 준수 상태가 포함 됩니다. 보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>BitLocker 컴퓨터 준수</p></td>
<td align="left"><p>IT 관리자가 개별 컴퓨터를 보고 규격 상태 또는 비규격으로 보고 된 이유를 확인할 수 있습니다. 또한이 보고서에는 운영 체제 드라이브 및 고정 데이터 드라이브의 암호화 상태도 표시 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise 규정 준수 요약</p></td>
<td align="left"><p>IT 관리자가 엔터프라이즈에서 MBAM 정책 준수 상태를 볼 수 있도록 합니다. 각 컴퓨터의 상태가 평가 되며,이 보고서에는 정책에 대 한 엔터프라이즈의 모든 컴퓨터 준수에 대 한 요약이 표시 됩니다. 보고서의 드릴 다운 옵션을 통해 IT 관리자가 데이터를 클릭 하 고 선택한 상태와 일치 하는 컴퓨터 목록을 볼 수 있습니다.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## 관련 항목


[MBAM 2.5 시작](getting-started-with-mbam-25.md)

[독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[MBAM 2.5 배포의 예시된 기능](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




