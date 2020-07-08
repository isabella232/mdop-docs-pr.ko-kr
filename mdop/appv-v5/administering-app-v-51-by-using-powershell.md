---
title: PowerShell을 사용하여 App-V 5.1 관리
description: PowerShell을 사용하여 App-V 5.1 관리
author: dansimp
ms.assetid: 9e10ff07-2cd9-4dc1-9e99-582f90c36081
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0c64d7e0330ff5d737dfa02d87f156cc3236b04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814873"
---
# PowerShell을 사용하여 App-V 5.1 관리


Microsoft Application Virtualization (App-v) 5.1는 관리자가 다양 한 App-v 5.1 작업을 수행 하는 데 도움이 되는 Windows PowerShell cmdlet을 제공 합니다. 다음 섹션에서는 PowerShell을 App-v 5.1와 함께 사용 하는 방법에 대 한 자세한 정보를 제공 합니다.

## PowerShell을 사용 하 여 App-v 5.1를 관리 하는 방법


다음 PowerShell 프로시저를 사용 하 여 다양 한 App-v 5.1 작업을 수행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)">PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법</a></p></td>
<td align="left"><p>PowerShell cmdlet을 설치 하 고 cmdlet 도움말 및 예제를 찾는 방법에 대해 설명 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.1 패키지를 관리하는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 독립 실행형 컴퓨터에서 클라이언트 패키지 수명 주기를 관리 하는 방법에 대해 설명 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 연결 그룹을 관리 하는 방법을 설명 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell51.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md)">PowerShell을 사용하여 클라이언트 구성을 수정하는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 클라이언트를 수정 하는 방법을 설명 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)">PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 사용자 구성 파일을 적용 하는 방법에 대해 설명 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)">PowerShell을 사용하여 배포 구성 파일을 적용하는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 배포 구성 파일을 적용 하는 방법에 대해 설명 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-51.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-51.md)">PowerShell을 사용 하 여 패키지를 시퀀싱 하는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 새 패키지를 만드는 방법에 대해 설명 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell51.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md)">PowerShell을 사용하여 패키지 가속기를 만드는 방법</a></p></td>
<td align="left"><p>PowerShell을 사용 하 여 패키지 가속기를 만드는 방법에 대해 설명 합니다. 패키지 가속기를 사용 하는 경우에는 복잡 한 대형 응용 프로그램을 자동으로 실행할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)">PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법</a></p></td>
<td align="left"><p>앱-V 5.1를 실행 하는 컴퓨터에서 보고 정보를 보낼 수 있도록 설정 하는 방법에 대해 설명 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md)">App-v 데이터베이스를 설치 하 고 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환 하는 방법</a></p></td>
<td align="left"><p>계정 이름의 배열을 가져와 표준 및 16 진수 형식으로 해당 SID로 변환 하는 방법에 대해 설명 합니다.</p></td>
</tr>
</tbody>
</table>

 

**중요**  App-v 패키지를 사용 하 여 실행 하는 모든 스크립트가 PowerShell 용으로 구성한 실행 정책과 일치 하는지 확인 합니다.

 

## PowerShell 오류 처리


앱-V 5.1 PowerShell 오류 처리에 대 한 정보를 보려면 다음 표를 사용 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Event</th>
<th align="left">작업</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>포함 된 스크립트와 함께 RollbackOnError 특성 사용</p></td>
<td align="left"><p><strong> </strong> 포함 된 스크립트와 함께 RollbackOnError 특성을 사용 하는 경우 다음 이벤트에 대 한 특성이 무시 됩니다.</p>
<ul>
<li><p>패키지 제거</p></li>
<li><p>패키지 게시 취소</p></li>
<li><p>가상 환경 종료</p></li>
<li><p>프로세스 종료</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 이름에<strong>$</strong></p></td>
<td align="left"><p>패키지 이름에 문자 ()가 포함 된 경우 <strong> $ </strong> 작은따옴표 (')를 사용 해야 합니다 <strong> ( </strong> 예:).</p>
<p><strong>추가-AppvClientPackage ' Contoso $ App. e 1 '</strong></p></td>
</tr>
</tbody>
</table>

 






## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

 

 





