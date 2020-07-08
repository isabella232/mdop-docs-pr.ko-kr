---
title: App-V용 Active Directory에서 필수 구성 요소 그룹 구성
description: App-V용 Active Directory에서 필수 구성 요소 그룹 구성
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821863"
---
# App-V용 Active Directory에서 필수 구성 요소 그룹 구성


Microsoft App-v (Application Virtualization) 관리 서버를 설치 하기 전에 Active Directory에 다음 개체를 만들어야 합니다. 앱-V는 Active Directory 그룹을 사용 하 여 응용 프로그램 및 관리 기능에 대 한 액세스를 제어 합니다. 이러한 그룹은 서버 설치 프로세스 중 및 응용 프로그램을 게시할 때 사용 합니다.

## Active Directory에서 응용 프로그램 가상화에 대 한 필수 그룹 구성


이 표에는 App-v를 설치 하는 데 필요한 Active Directory 그룹이 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">개체</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>OU (조직 구성 단위)</p></td>
<td align="left"><p>Active Directory에서 App-v에 필요한 특정 그룹에 대 한 OU를 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 관리 그룹</p></td>
<td align="left"><p>App-v 관리 서버를 설치 하는 동안 관리 콘솔에 대 한 관리 액세스를 제어 하기 위해 앱-V 관리자 그룹으로 사용할 Active Directory 그룹을 선택 해야 합니다. App-v 관리자에 대 한 보안 그룹을 만들고 관리 콘솔을 사용 해야 하는 모든 사용자에 게이 그룹에 추가 합니다. App-v 관리 서버 설치 관리자에서이 그룹을 직접 만들 수 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 사용자 그룹</p></td>
<td align="left"><p>App-v 함수에 액세스 하는 모든 사용자 계정은 일반 플랫폼 액세스를 위한 단일 그룹과 연결 된 공급자 정책의 구성원 이어야 합니다. 기존 그룹 사용 예를 들어 모든 사용자가 App-v에 대 한 액세스 권한이 있거나 새 그룹을 만드는 경우 도메인 사용자입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램 그룹</p></td>
<td align="left"><p>App-v는 Active Directory 그룹과 개별 응용 프로그램을 사용 하도록 권한을 연결 합니다. 각 응용 프로그램에 대해 Active Directory 그룹을 만들고 필요에 따라이 그룹에 사용자를 할당 하 여 응용 프로그램에 대 한 사용자 액세스를 제어 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[Application Virtualization 배포 요구 사항](application-virtualization-deployment-requirements.md)

[App-V Management Server용 Windows Server 2008을 구성 방법](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





