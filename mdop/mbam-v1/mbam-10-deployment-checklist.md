---
title: MBAM 1.0 배포 검사 목록
description: MBAM 1.0 배포 검사 목록
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812537"
---
# MBAM 1.0 배포 검사 목록


이 검사 목록은 Microsoft BitLocker 관리 및 모니터링 (MBAM) 배포를 용이 하 게 하기 위해 고안 되었습니다.

**참고**  
이 검사 목록에서는 권장 단계를 개략적으로 설명 하 고, MBAM 기능을 배포할 때 고려해 야 할 항목의 상위 수준 목록을 제공 합니다. 이 검사 목록을 스프레드시트 프로그램에 복사 하 여 특정 요구 사항에 맞게 사용자 지정 하는 것이 좋습니다.



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
<td align="left"><p>이 계획 단계를 완료 하 여 MBAM 배포에 대 한 컴퓨팅 환경을 준비 합니다.</p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">MBAM 1.0 계획 검사 목록</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 지원 구성의 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치를 지원 하는지 확인 합니다.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">MBAM 1.0 지원되는 구성</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 설치 프로그램을 실행 하 여 다음과 같은 순서로 MBAM 서버 기능을 배포 합니다.</p>
<ol>
<li><p>복구 및 하드웨어 데이터베이스</p></li>
<li><p>준수 상태 데이터베이스</p></li>
<li><p>준수 감사 및 보고서</p></li>
<li><p>관리 및 모니터링 서버</p></li>
<li><p>MBAM 그룹 정책 서식 파일</p></li>
</ol>
<div class="alert">
<strong>참고</strong><br/><p>각 기능이 설치 된 서버의 이름을 추적 하세요. 이 정보는 설치 프로세스 전체에서 사용 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">MBAM 1.0 서버 인프라 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>계획 단계 중에 만든 Active Directory 도메인 서비스 보안 그룹을 적절 한 서버의 적절 한 로컬 MBAM 서버 기능 관리자 그룹에 추가 합니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">MBAM 1.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">MBAM 1.0 그룹 정책 개체 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 소프트웨어를 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">MBAM 1.0 클라이언트 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MBAM 1.0 배포](deploying-mbam-10.md)









