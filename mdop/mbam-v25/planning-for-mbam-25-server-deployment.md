---
title: MBAM 2.5 서버 배포 계획
description: MBAM 2.5 서버 배포 계획
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826213"
---
# MBAM 2.5 서버 배포 계획


이 항목에서는 MBAM 독립 실행형 및 구성 관리자 토폴로지에 대해 배포 하는 기능을 나열 하 고 배포 해야 하는 순서를 나열 합니다. 각 토폴로지에 대해 권장 되는 구성을 사용할 수 있습니다. 그러나 확장 요구 사항에 따라 다양 한 구성 및 여러 서버에서 MBAM 서버 데이터베이스 및 기능을 구성할 수 있습니다.

## 두 토폴로지에 대 한 중요 한 계획 고려 사항


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">고려 사항</th>
<th align="left">세부 정보 또는 목적</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>배포를 시작 하기 전에 다음을 검토 하세요.</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></li>
</ul></td>
<td align="left"><p>각 MBAM 기능에는 MBAM 설치를 시작 하기 전에 충족 해야 하는 특정 전제 조건이 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM의 BitLocker 복구 키는 한 번 사용 후 만료 됩니다.</p></td>
<td align="left"><p>단일 사용은 관리 및 모니터링 웹 사이트 (헬프 데스크 라고도 함), 셀프 서비스 포털 또는 <strong> MbamBitLockerRecoveryKey Windows PowerShell cmdlet을 사용 하 여 복구 키가 검색 되었음을 의미 합니다 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>각 기능을 구성 하는 컴퓨터의 이름을 추적 하세요. 이 정보는 구성 프로세스 전체에서 사용 합니다.</p></td>
<td align="left"><p><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">이 용도로 mbam 2.5 배포 검사 목록을 사용할 수 있습니다 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>MDOP (BitLocker Management) 노드에서 그룹 정책 설정만 구성 합니다. BitLocker 드라이브 암호화 노드에서 그룹 정책 설정을 변경 하지 마세요.</p></td>
<td align="left"><p>BitLocker 드라이브 암호화 노드에서 그룹 정책 설정을 변경 하는 경우 MBAM이 작동 하지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>MBAM 서버 배포 계획-독립 실행형 토폴로지


독립 실행형 토폴로지의 경우 프로덕션 환경에는 두 대의 서버 구성을 사용 하는 것이 좋지만,이는 3 ~ 4 개 서버의 구성을 사용할 수 있습니다.

MBAM 독립 실행형 토폴로지의 서버 인프라에는 다음 기능이 포함 되어 있으며 나열 된 순서 대로 구성 되어야 합니다.

1.  데이터베이스 (준수 및 감사 데이터베이스 및 복구 데이터베이스)

2.  보고

3.  웹 응용 프로그램 및 해당 웹 서비스

    -   관리 및 모니터링 웹 사이트

    -   셀프 서비스 포털

이러한 기능에 대 한 설명은 [독립 실행형 토폴로지와 함께 MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)를 참조 하세요.

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>MBAM 서버 배포 계획 – 구성 관리자 토폴로지


구성 관리자 통합 토폴로지의 경우 추가 서버 구성을 사용할 수 있지만 프로덕션 환경에는 3 서버 구성이 권장 됩니다.

MBAM 구성 관리자 토폴로지에 대 한 서버 인프라에는 다음 기능이 포함 되어 있으며, 여기에는 나열 된 순서 대로 구성 하거나 수행 해야 합니다.

1.  데이터베이스 (준수 및 감사 데이터베이스 및 복구 데이터베이스)

2.  보고

3.  웹 응용 프로그램 및 해당 웹 서비스

    -   관리 및 모니터링 웹 사이트

    -   셀프 서비스 포털

4.  System Center Configuration Manager 통합

이러한 기능에 대 한 설명은 [구성 관리자 통합 토폴로지와 MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)를 참조 하세요.



## 관련 항목


[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)

[MBAM 2.5 서버 인프라 배포](deploying-the-mbam-25-server-infrastructure.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





