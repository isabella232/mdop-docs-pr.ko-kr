---
title: App-V 5.1 Client Management Console 사용
description: App-V 5.1 Client Management Console 사용
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813257"
---
# App-V 5.1 Client Management Console 사용


이 항목에서는 Microsoft App-v (Application Virtualization) 5.1 클라이언트를 구성 하 고 관리 하는 방법에 대 한 정보를 제공 합니다.

## 앱-V 5.1 클라이언트 구성 수정


App-v 5.1 클라이언트에는 환경에서 클라이언트가 실행 되는 방식을 결정 하도록 구성할 수 있는 설정이 연결 되어 있습니다. 클라이언트를 실행 하는 컴퓨터 또는 PowerShell 또는 그룹 정책을 사용 하 여 이러한 설정을 관리할 수 있습니다. PowerShell 또는 그룹 정책 구성을 사용 하 여 클라이언트를 수정 하는 방법에 대 한 자세한 내용은 [powershell을 사용 하 여 클라이언트 구성을 수정](how-to-modify-client-configuration-by-using-powershell51.md)하는 방법을 참조 하세요.

## <a href="" id="the-app-v-5-1-client-management-console-"></a>App-v 5.1 클라이언트 관리 콘솔


App-v 5.1 클라이언트 관리 콘솔을 사용 하 여 App-v 5.1 클라이언트에 대 한 정보를 얻고 특정 작업을 수행할 수 있습니다. 클라이언트 관리 콘솔에서 수행할 수 있는 많은 작업은 PowerShell을 사용 하 여 수행할 수도 있습니다. 각 작업에 대해 연결 된 PowerShell cmdlet도 다음 표에 표시 됩니다. PowerShell을 사용 하는 방법에 대 한 자세한 내용은 [powershell을 사용 하 여 앱-V 5.1 관리](administering-app-v-51-by-using-powershell.md)를 참조 하세요.

클라이언트 관리 콘솔에는 다음의 설명 된 기본 탭이 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">탭</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>개요</p></td>
<td align="left"><p><strong>개요 </strong> 탭에는 다음 요소가 포함 됩니다.</p>
<ul>
<li><p>업데이트 – <strong> 업데이트 타일을 사용 </strong> 하 여 가상화 된 응용 프로그램을 새로 고치거 나 새 가상화 된 패키지를 받습니다.</p>
<p><strong>마지막 새로 고침에는 </strong> 가상화 된 패키지의 현재 버전이 표시 됩니다.</p></li>
<li><p>모든 가상 응용 프로그램 다운로드- <strong> 다운로드 타일을 사용 </strong> 하 여 현재 사용자에 게 프로 비전 된 모든 패키지를 다운로드 합니다.</p>
<p>(연결 된 PowerShell cmdlet: <strong> Mount-AppvClientPackage </strong> )</p>
<p></p></li>
<li><p>오프 라인으로 작업-이 타일을 사용 하 여 모든 자동 및 수동 가상 응용 프로그램 업데이트를 허용 하지 않습니다.</p>
<p>(연결 된 PowerShell cmdlet: <strong> Set-AppvPublishServer-UserRefreshEnabled – GlobalRefreshEnabled </strong> )</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>가상 앱</p></td>
<td align="left"><p><strong>가상 앱 탭에는 </strong> 사용자에 게 게시 된 모든 패키지가 표시 됩니다. 특정 패키지를 클릭 하 여 해당 패키지에 포함 된 모든 응용 프로그램을 볼 수도 있습니다. 이는 현재 사용 중인 패키지에 대 한 정보와 컴퓨터에 다운로드 된 각 패키지의 크기를 표시 합니다. 패키지 다운로드를 시작 하 고 중지할 수도 있습니다. 또한 사용자 상태를 복구할 수 있습니다. 복구는 패키지와 연결 된 모든 사용자 데이터를 삭제 합니다.</p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱 연결 그룹</p></td>
<td align="left"><p><strong>앱 연결 그룹 탭에는 </strong> 현재 사용자가 사용할 수 있는 모든 연결 그룹이 표시 됩니다. 특정 연결 그룹을 클릭 하 여 선택한 그룹의 일부인 모든 패키지를 표시 합니다. 이는 이미 사용 중인 연결 그룹에 대 한 정보와 컴퓨터에 다운로드 된 연결 그룹 콘텐츠의 양을 표시 합니다. 또한 연결 그룹 다운로드를 시작 하 고 중지할 수 있습니다. 이 섹션을 사용 하 여 복구를 시작할 수 있습니다. 복구는 연결 그룹과 연결 된 모든 사용자 상태를 제거 합니다.</p>
<p>(연결 된 PowerShell cmdlet: 다운로드- <strong> Mount-AppvClientConnectionGroup </strong> . 복구- <strong> AppvClientConnectionGroup </strong> .)</p>
<p></p></td>
</tr>
</tbody>
</table>

 

[Client Management Console에 액세스하는 방법](how-to-access-the-client-management-console51.md)

[클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

 

 





