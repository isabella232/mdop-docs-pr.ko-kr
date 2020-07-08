---
title: App-V 사전 설치 검사 목록
description: App-V 사전 설치 검사 목록
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819788"
---
# App-V 사전 설치 검사 목록


다음 검사 목록은 Microsoft App-v (Application Virtualization) 서버를 설치 하기 전에 고려할 항목의 상위 수준 목록을 제공 하 고 수행 해야 하는 단계를 설명 하기 위한 것입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">참고자료</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>컴퓨팅 환경이 App-v에 필요한 지원 되는 구성을 충족 하는지 확인 합니다.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Application Virtualization 배포 요구 사항</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>필요한 Active Directory 그룹 및 계정을 구성 합니다.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">App-V용 Active Directory에서 필수 구성 요소 그룹 구성</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>IIS를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 설정을 구성 합니다.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">App-V Management Server용 Windows Server 2008을 구성 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>IIS를 실행 하는 서버를 위임용으로 트러스트할 수 있도록 구성 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이는 분산 시스템 아키텍처를 사용 하 여 app-v 관리 서버를 설치 하는 경우 (예를 들어, 앱 V 관리 콘솔, 관리 웹 서비스 및 데이터베이스를 다른 컴퓨터에 설치 하는 경우)에만 필요 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">위임을 위해 신뢰할 수 있는 서버를 구성하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008을 설치 합니다.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> )를 설치 합니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[Application Virtualization 배포 및 업그레이드 검사 목록](application-virtualization-deployment-and-upgrade-checklists.md)

[App-V 설치 검사 목록](app-v-installation-checklist.md)









