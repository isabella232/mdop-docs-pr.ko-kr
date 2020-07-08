---
title: MBAM 2.5 배포 검사 목록
description: MBAM 2.5 배포 검사 목록
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822833"
---
# MBAM 2.5 배포 검사 목록


이 검사 목록을 사용 하 여 독립 실행형 토폴로지와 Microsoft BitLocker 관리 및 모니터링 (MBAM) 배포 중에 도움이 될 수 있습니다.

**참고**  
이 검사 목록에서는 Microsoft BitLocker 관리 및 모니터링 기능을 배포할 때 고려해 야 할 항목의 권장 단계 및 상위 수준 목록을 간략하게 설명 합니다. 이 검사 목록을 스프레드시트 프로그램에 복사 하 여 사용을 위해 사용자 지정 하는 것이 좋습니다.



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
<td align="left"><p>모든 계획 단계를 검토 하 고 완료 하 여 MBAM 배포 환경을 준비 합니다.</p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)">MBAM 2.5 계획 검사 목록</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>지원 되는 구성 정보를 검토 하 여 MBAM이 선택한 클라이언트 및 서버 컴퓨터를 지원 하는지 확인 합니다.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 서버 소프트웨어를 설치 합니다.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 서버 기능을 구성 합니다.</p>
<ul>
<li><p>준수 및 감사 데이터베이스 및 복구 데이터베이스</p></li>
<li><p>보고</p></li>
<li><p>웹 응용 프로그램</p></li>
<li><p>Configuration Manager 통합 토폴로지 (이 토폴로지에서 MBAM을 실행 중인 경우에만 필요 함)</p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>각 기능을 구성한 서버의 이름을 기록해 둡니다. 이 정보는 구성 프로세스 전체에서 사용 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)">MBAM 2.5 서버 기능 구성</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 구성의 유효성을 검사 합니다.</p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)">MBAM 2.5 서버 기능 구성의 유효성 검사</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 그룹 정책 템플릿을 복사 하 고 그룹 정책 설정을 편집 합니다.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">MBAM 2.5 그룹 정책 템플릿을 복사 </a> 하 고 <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> mbam 2.5 그룹 정책 설정 편집</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 소프트웨어를 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)">MBAM 2.5 클라이언트 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## 관련 항목


[MBAM 2.5 배포](deploying-mbam-25.md)




## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




