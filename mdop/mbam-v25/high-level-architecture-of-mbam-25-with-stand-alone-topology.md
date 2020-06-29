---
title: 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
description: 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826558"
---
# 독립 실행형 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처


이 항목에서는 Configuration Manager 독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포 하는 데 권장 되는 아키텍처에 대해 설명 합니다. 이 토폴로지에서 MBAM은 독립 실행형 제품으로 배포 됩니다. 또한 configuration manager와 MBAM을 통합 하는 Configuration Manager 통합 토폴로지로 MBAM을 배포할 수 있습니다. 자세한 내용은 [Configuration Manager 통합 토폴로지에 있는 MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)를 참조 하세요.

이 항목에 설명 된 소프트웨어의 지원 되는 버전 목록은 [Mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.

**참고**  테스트 환경 에서만 단일 서버 아키텍처를 사용 하는 것이 좋습니다.

 

## 권장 서버 수 및 지원 되는 클라이언트 수


프로덕션 환경에서 권장 되는 서버 수 및 지원 되는 클라이언트 수는 다음과 같습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">프로덕션 환경의 권장 아키텍처</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>서버 및 다른 컴퓨터 수</p></td>
<td align="left"><p>두 서버</p>
<p>하나의 워크스테이션</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원 되는 클라이언트 컴퓨터 수</p></td>
<td align="left"><p>50만</p></td>
</tr>
</tbody>
</table>

 

## 독립 실행형 토폴로지가 있는 권장 MBAM 상위 수준 아키텍처


다음 다이어그램 및 표에서는 독립 실행형 토폴로지에 대 한 MBAM에 대해 권장 되는 높은 수준의 두 서버 아키텍처에 대해 설명 합니다. MBAM 다중 포리스트 배포에는 단방향 또는 양방향 트러스트가 필요 합니다. 단방향 트러스트의 경우 서버 도메인이 클라이언트 도메인을 신뢰 해야 합니다.

![mbam2](images/mbam2-5-2servers.png)

이 서버 설명 데이터베이스 서버에 구성할 서버 기능

준수 및 감사 데이터베이스

이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에 구성 됩니다.

**규정 준수 및 감사 데이터베이스** 는 SQL Server Reporting Services가 호스트 하는 보고서에 주로 사용 되는 규정 준수 데이터를 저장 합니다.

복구 데이터베이스

이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에 구성 됩니다.

**복구 데이터베이스** 는 mbam 클라이언트 컴퓨터에서 수집 된 복구 데이터를 저장 합니다.

보고

이 기능은 Windows Server 및 지원 되는 SQL Server 인스턴스를 실행 하는 서버에 구성 됩니다.

**보고서** 는 엔터프라이즈의 클라이언트 컴퓨터에 대 한 복구 감사 및 준수 상태 데이터를 제공 합니다. 관리 및 모니터링 웹 사이트에서 또는 SQL Server Reporting Services에서 직접 보고서에 액세스할 수 있습니다.

관리 및 모니터링 서버

관리 및 모니터링 웹 사이트

이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.

**관리 및 모니터링 웹 사이트** 는 다음 작업을 수행 하는 데 사용 됩니다.

-   최종 사용자가 잠겨 있는 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있도록 지원 합니다. (이 웹 사이트의이 영역을 일반적으로 지원 센터 라고 합니다.)

-   클라이언트 컴퓨터에 대 한 호환성 상태 및 복구 작업을 표시 하는 보고서를 봅니다.

셀프 서비스 포털

이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.

**셀프 서비스 포털** 은 클라이언트 컴퓨터의 최종 사용자가 자신의 BitLocker 암호를 분실 하거나 잊어버린 경우 복구 키를 사용 하 여 개별적으로 웹 사이트에 로그온 할 수 있도록 하는 웹 사이트입니다.

이 웹 사이트의 웹 서비스 모니터링

이 기능은 Windows Server를 실행 하는 컴퓨터에서 구성 되었습니다.

**모니터링 웹 서비스** 는 Mbam 클라이언트와 웹 사이트에서 데이터베이스와 통신 하는 데 사용 됩니다.

**중요**  MBAM 웹 사이트는 복구 데이터베이스와 직접 통신 하므로 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1에서는 모니터링 웹 서비스를 더 이상 사용할 수 없습니다.

 

관리 워크스테이션

MBAM 그룹 정책 서식 파일

-   MBAM 그룹 정책 템플릿은 MBAM에 대 한 구현 설정을 정의 하는 그룹 정책 설정으로, BitLocker 드라이브 암호화를 관리할 수 있습니다.

-   MBAM을 실행 하기 전에, [MDOP 그룹 정책 (admx) 템플릿을 가져오고](https://go.microsoft.com/fwlink/p/?LinkId=393941) 지원 되는 Windows Server 또는 Windows 운영 체제를 실행 하는 서버 또는 워크스테이션에 복사 하는 방법에서 그룹 정책 템플릿을 다운로드 해야 합니다.

-   워크스테이션이 전용 컴퓨터 일 필요는 없습니다.

MBAM 클라이언트 및 Configuration Manager 클라이언트 컴퓨터

MBAM 클라이언트 소프트웨어

MBAM 클라이언트:

-   그룹 정책 개체를 사용 하 여 엔터프라이즈의 클라이언트 컴퓨터에 BitLocker 드라이브 암호화를 적용 합니다.

-   운영 체제 드라이브, 고정 데이터 드라이브, 이동식 (USB) 데이터 드라이브 등 세 가지 데이터 드라이브 유형의 Bitlocker 복구 키를 수집 합니다.

-   클라이언트 컴퓨터에 대 한 복구 정보 및 컴퓨터 정보를 수집 합니다.



## 관련 항목


[MBAM 2.5 시작](getting-started-with-mbam-25.md)

[Configuration Manager 통합 토폴로지를 사용하는 MBAM 2.5의 개략적인 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[MBAM 2.5 배포의 예시된 기능](illustrated-features-of-an-mbam-25-deployment.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





