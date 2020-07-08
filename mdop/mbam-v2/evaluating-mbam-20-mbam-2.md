---
title: MBAM 2.0 평가
description: MBAM 2.0 평가
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824738"
---
# MBAM 2.0 평가


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 프로덕션 환경에 배포 하기 전에 테스트 환경에서 평가 해야 합니다. 이 항목의 정보를 사용 하 여 평가 목적 으로만 단일 서버 테스트 환경에서 독립 실행형 토폴로지로 Microsoft BitLocker 관리 및 모니터링을 설정할 수 있습니다. 단일 서버 토폴로지는 프로덕션 환경에는 권장 되지 않습니다.

테스트 환경에서 MBAM을 배포 하는 방법에 대 한 지침은 [단일 서버에서 MBAM을 설치 하 고 구성 하는 방법을](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)참조 하세요.

## 테스트 환경 설정


테스트 환경에서 평가할 MBAM의 비프로덕션 인스턴스를 설정 하는 경우에도 필수 구성 요소와 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 여전히 확인 해야 합니다. 설치를 시작 하기 전에 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md), [Mbam 2.0 지원 되는 구성](mbam-20-supported-configurations-mbam-2.md), 그리고 [mbam 2.0에 대 한 환경 준비](preparing-your-environment-for-mbam-20-mbam-2.md)를 참조 하세요.

### MBAM 평가 배포 계획

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">작업</th>
<th align="left">참조</th>
<th align="left">참고</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM에 대 한 시작 정보를 검토 하 여 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 지식을 얻으십시오.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">MBAM 2.0 시작</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 2.0 배포 필수 구성 요소를 계획 하 고 컴퓨팅 환경을 준비 합니다.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">MBAM 2.0 배포 필수 구성 요소</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 그룹 정책 요구 사항 계획 및 구성</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">MBAM 2.0 그룹 정책 요구 사항 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>필요한 ActiveDirectoryDomainServices 보안 그룹을 계획 하 고 만들고 MBAM 로컬 보안 그룹 구성원 요구 사항에 대 한 계획을 수립 합니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">MBAM 2.0 관리자 역할 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 서버 기능 배포를 배포 하기 위한 계획입니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">MBAM 2.0 서버 배포 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 배포 배포 계획입니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">MBAM 2.0 클라이언트 배포 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### MBAM 평가 배포 수행

MBAM 설치에 대 한 컴퓨팅 환경을 준비 하기 위해 필요한 계획 및 소프트웨어 필수 구성 요소 설치를 완료 한 후 MBAM 평가판 배포를 시작할 수 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치를 지원 하는지 확인 합니다.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 지원되는 구성</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>평가판을 위해 MBAM 설치를 실행 하 여 단일 서버에 MBAM 서버 기능을 배포 합니다.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">단일 서버에서 MBAM을 설치 및 구성하는 방법</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>계획 단계 중에 만든 ActiveDirectoryDomainServices 보안 그룹을 새 MBAM 서버의 적절 한 로컬 MBAM 서버 기능 로컬 그룹에 추가 합니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">MBAM 2.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">MBAM 2.0 그룹 정책 개체 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 소프트웨어를 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">MBAM 2.0 클라이언트 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## MBAM 평가에 대 한 Lab 컴퓨터 구성


이 섹션에는 MBAM 클라이언트 상태 보고 속도를 향상 하는 데 사용할 수 있는 정보가 포함 되어 있습니다. 그러나 이러한 수정은 테스트 목적 으로만 사용 해야 합니다.

**참고**  다음 섹션의 정보는 Windows 레지스트리를 수정 하는 방법에 대해 설명 합니다. 레지스트리 편집기를 잘못 사용 하면 심각한 문제가 발생할 수 있으며,이 경우 Windows를 다시 설치 해야 할 수 있습니다. Microsoft는 레지스트리 편집기의 잘못 된 사용으로 인해 발생 하는 문제에 대 한 해결을 보장할 수 없습니다. 레지스트리 편집기 사용에 따른 모든 책임은 사용자에 게 있습니다.

 

### MBAM 클라이언트 상태 보고 빈도 설정을 수정 합니다.

그룹 정책을 사용 하 여 설정 하는 경우 MBAM 클라이언트 웨이크업 및 상태 보고 빈도는 최소 90 분입니다. Windows 레지스트리를 사용 하 여 테스트 속도를 향상 시킬 수 있도록 MBAM 클라이언트 컴퓨터에서 이러한 주파수를 더 낮은 값으로 변경 합니다.

MBAM 클라이언트 상태 보고 빈도 설정을 수정 하려면 다음을 수행 합니다.

1.  레지스트리 편집기를 사용 하 여 **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**로 이동 합니다.

2.  **ClientWakeupFrequency** 및 **StatusReportingFrequency** 의 값을 클라이언트에서 지원 되는 최소 값으로 **1** 로 변경 합니다. 이 변경으로 인해 MBAM 클라이언트가 분 단위로 보고 됩니다.

3.  **BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.

**참고**  낮은 값을 설정 하려면 레지스트리에서 수동으로 설정 해야 합니다.

 

### MBAM 클라이언트 서비스 시작 지연 수정

Mbam 클라이언트 웨이크업 및 상태 보고 빈도 외에도 클라이언트 컴퓨터에서 MBAM 클라이언트 에이전트 서비스가 시작 될 때 최대 90 분의 지연이 있습니다. 임의 지연을 원하지 않으면 **HKLM\\Software\\Microsoft\\MBAM**에서 a 2의 **DWORD** 값을 만들고 해당 **NoStartupDelay** 값을 **1**로 설정한 다음 **BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.

## 관련 항목


[MBAM 2.0 시작](getting-started-with-mbam-20-mbam-2.md)

 

 





