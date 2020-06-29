---
title: 연결 그룹에서 패키지 버전을 무시하는 방법
description: 연결 그룹에서 패키지 버전을 무시하는 방법
author: dansimp
ms.assetid: db16b095-dbe2-42c7-863d-b0d5d91b2f4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 026ef1b3a2aa073a684b1fe5da4f79aa1067072d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813932"
---
# 연결 그룹에서 패키지 버전을 무시하는 방법


Microsoft Application Virtualization (App-v) 5.1에서는 패키지 업그레이드를 간소화 하 고 만들어야 하는 연결 그룹의 수를 줄이기 위해 모든 버전의 패키지를 사용 하도록 연결 그룹을 구성할 수 있습니다.

일부 이전 버전의 App-v에서 패키지를 업그레이드 하려면 연결 그룹을 사용 하지 않도록 설정 하 고 연결 그룹의 XML 정의 파일을 수정 하는 등 몇 가지 단계를 수행 해야 했습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-v 5.1 작업 설명</th>
<th align="left">앱을 사용 하 여 작업을 수행 하는 방법-V 5.1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>연결 그룹을 사용 하지 않도록 설정 하지 않고 패키지를 업그레이드할 수 있도록 모든 버전의 패키지를 받아들이도록 연결 그룹을 구성할 수 있습니다.</p>
<p><strong>기능이 작동 하는 방식입니다.</strong></p>
<ul>
<li><p>연결 그룹이 여러 버전의 패키지에 대 한 액세스 권한이 있는 경우 최신 버전이 사용 됩니다.</p></li>
<li><p>연결 그룹에 잘못 된 버전이 있는 선택적 패키지가 포함 된 경우 패키지가 무시 되 고 연결 그룹의 가상 환경이 만들어지지 않도록 차단 되지 않습니다.</p></li>
<li><p>연결 그룹에 잘못 된 버전이 있는 선택적 패키지가 포함 되어 있지 않은 경우 연결 그룹의 가상 환경을 만들 수 없습니다.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">단계</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v Server – 관리 콘솔</p></td>
<td align="left"><ol>
<li><p>관리 콘솔에서 <strong> 연결 그룹을 선택 </strong> 합니다.</p></li>
<li><p>연결 그룹 라이브러리에서 올바른 연결 그룹을 선택 합니다.</p></li>
<li><p><strong> </strong> 연결 된 패키지 창에서 편집을 클릭 합니다.</p></li>
<li><p><strong> </strong> 패키지 이름 옆에 있는 버전 사용 확인란을 선택 하 고 적용을 <strong> 클릭 </strong> 합니다.</p></li>
</ol>
<p>패키지를 추가 하거나 업그레이드 하는 방법에 대 한 자세한 내용은 <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)"> 관리 콘솔을 사용 하 여 패키지를 추가 하거나 업그레이드 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>독립 실행형 컴퓨터의 app-v 클라이언트</p></td>
<td align="left"><ol>
<li><p>연결 그룹 XML 문서를 만듭니다.</p></li>
<li><p>패키지를 업그레이드 하려면 <strong> package </strong> 태그 특성을 <strong> </strong> 별표 ( <strong>*</strong> )로 설정 합니다.</p></li>
<li><p>다음 cmdlet을 사용 하 여 연결 그룹을 추가 하 고 연결 그룹 XML 문서의 경로를 포함 합니다.</p>
<p><strong>추가-AppvClientConnectionGroup</strong></p></li>
<li><p>패키지를 업그레이드 하는 경우 다음 cmdlet을 사용 하 여 이전 패키지를 제거 하 고 업그레이드 된 패키지를 추가 하 고 업그레이드 된 패키지를 게시 합니다.</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>추가-AppvClientPackage</p></li>
<li><p>게시-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>자세한 내용은 다음을 참조하세요.</p>
<ul>
<li><p>예제 XML 파일, <strong> 선택적 패키지가 포함 된 연결 그룹 XML 파일 </strong> ,이 섹션에서는 <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)"> 연결 그룹에서 선택적 패키지를 사용 하는 방법에 대해 설명 합니다.</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.1 패키지를 관리하는 방법</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## 관련 항목


[연결 그룹 관리](managing-connection-groups51.md)

 

 





