---
title: 연결 그룹에서 선택적 패키지를 사용하는 방법
description: 연결 그룹에서 선택적 패키지를 사용하는 방법
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813628"
---
# 연결 그룹에서 선택적 패키지를 사용하는 방법


Microsoft Application Virtualization (App-v) 5.0 SP3에서 시작 하는 경우 연결 그룹에 선택적 패키지를 추가 하 여 연결 그룹 관리를 단순화할 수 있습니다. 다음 표에서는 선택적 패키지를 사용 하 여 더 쉽게 완료할 수 있는 작업을 요약 하 고 각 작업에 대 한 지침에 대 한 링크를 제공 합니다.

**참고** 
 **앱-V 5.0 SP3 이전의 릴리스에서는 선택적 패키지가 지원 되지 않습니다.**

 

선택적 패키지를 사용 하기 전에 [연결 그룹에서 선택적 패키지를 사용 하기 위한 요구 사항을](#bkmk-reqs-using-cg)참조 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">지침 링크</th>
<th align="left">작업</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">다른 패키지를 포함 하는 여러 사용자에 대해 선택적 패키지와 하나의 연결 그룹을 사용 합니다.</a></p></td>
<td align="left"><p>단일 연결 그룹을 사용 하 여 다른 최종 사용자가 사용할 수 있는 다른 응용 프로그램 그룹 및 플러그 인을 만듭니다.</p>
<p>예를 들어 Microsoft Office를 모든 최종 사용자에 게 배포 하지만 다른 플러그 인을 다양 한 사용자 하위 집합에 배포 하려고 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">연결 그룹을 변경 하지 않고 선택적 패키지를 게시 취소 하거나 삭제 하거나 선택적 패키지를 게시 취소 하 고 나중에 다시 게시할 수 있습니다.</a></p></td>
<td align="left"><p>App-v 클라이언트에서 연결 그룹을 사용 하지 않도록 설정, 제거, 편집, 추가, 다시 사용 하지 않고 선택적 패키지를 게시 취소 하거나, 삭제 하거나, 게시 합니다.</p>
<p>선택 패키지를 게시 취소 하 고 나중에 연결 그룹을 사용 하지 않도록 설정 하거나 다시 게시할 필요 없이 다시 게시할 수도 있습니다.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>다른 패키지를 사용 하는 여러 사용자를 위해 선택적 패키지와 함께 하나의 연결 그룹을 사용 합니다.


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 설명</th>
<th align="left">작업을 수행 하는 방법</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>App-v 5.0 SP3 및 App-V 5.1 사용</strong></p>
<p>선택적 패키지를 연결 그룹에 추가 하 여 여러 최종 사용자에 게 서로 다른 응용 프로그램 및 플러그 인 조합을 제공할 수 있습니다.</p>
<p><strong>예 </strong> : Microsoft Office를 최종 사용자에 게 배포 하려고 하지만 사용자의 하위 집합에 대해서만 특정 플러그 인을 사용 하도록 설정할 수 있습니다.</p>
<p>이렇게 하려면 Office를 사용 하는 패키지와 Office 플러그 인을 사용 하는 다른 패키지가 포함 된 연결 그룹을 만든 다음 플러그 인 패키지를 선택적으로 만듭니다.</p>
<p>플러그 인 패키지에 대 한 권한이 없는 최종 사용자는 Office를 실행할 수 있습니다.</p></td>
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
<li><p>관리 콘솔에서 <strong> 연결 그룹을 선택 </strong> 하 여 연결 그룹 라이브러리를 표시 합니다.</p></li>
<li><p>연결 그룹 라이브러리에서 올바른 연결 그룹을 선택 합니다.</p></li>
<li><p><strong> </strong> 연결 된 패키지 창에서 편집을 클릭 합니다.</p></li>
<li><p><strong> </strong> 패키지 이름 옆에 있는 선택 항목을 선택 합니다.</p></li>
<li><p><strong>그룹 액세스에 패키지 액세스 추가 확인란을 선택 </strong> 합니다. 이 필수 단계는 Active Directory 그룹에 패키지를 할당할 때 이전에 구성한 패키지 권리가 연결 그룹에 추가 됩니다.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 서버-PowerShell cmdlet</p></td>
<td align="left"><p>다음 cmdlet을 사용 하 고 <strong> -Optional 매개 변수를 지정 합니다 </strong> .</p>
<p><strong>추가-AppvServerConnectionGroupPackage</strong></p>
<p><strong>구문과</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>예:</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>독립 실행형 컴퓨터의 app-v 클라이언트</p></td>
<td align="left"><ol>
<li><p>연결 그룹 XML 문서를 만들고 <strong> Package </strong> tag 특성 <strong> isoptional </strong> 을 <strong> "true"로 설정 합니다.</strong></p></li>
<li><p>다음 cmdlet을 사용 하 여 연결 그룹을 추가 하 고 사용 하도록 설정 합니다.</p>
<ul>
<li><p>추가-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>선택적 패키지가 있는 연결 그룹 XML 문서 예:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>App-v 5.0 SP3 이전 버전을 사용 하는 경우</strong></p></td>
<td align="left"><p>특정 응용 프로그램 및 플러그 인 조합을 특정 사용자가 사용할 수 있도록 하기 위해 여러 연결 그룹을 만들어야 했습니다.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>연결 그룹을 변경 하지 않고 선택적 패키지를 게시 취소 하거나 삭제 하거나 선택적 패키지를 게시 취소 하 고 나중에 다시 게시할 수 있습니다.


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 설명</th>
<th align="left">작업을 수행 하는 방법</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>App-v 5.0 SP3 및 App-V 5.1 사용</strong></p>
<p>앱-V 클라이언트에서 연결 그룹을 사용 하지 않도록 설정 하거나 다시 사용 하지 않고 연결 그룹에 있는 선택적 패키지를 게시 취소 하거나, 삭제 하거나, 게시할 수 있습니다.</p>
<p>선택 패키지를 게시 취소 하 고 나중에 연결 그룹을 사용 하지 않도록 설정 하거나 다시 게시할 필요 없이 다시 게시할 수도 있습니다.</p>
<p><strong>예 </strong> : Microsoft Office 플러그 인이 포함 된 선택적 패키지를 게시 하는 경우 플러그 인을 제거 하려면 연결 그룹을 사용 하지 않도록 설정 하지 않고 패키지의 게시를 취소 하면 됩니다.</p></td>
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
<td align="left"><ul>
<li><p>패키지의 게시를 취소 하려면 관리 콘솔에서 패키지 선택을 선택 <strong> 하 고 </strong> , 게시 취소 하려는 패키지를 클릭 하거나 마우스 오른쪽 단추로 클릭 한 다음 <strong> 게시 취소를 클릭 </strong> 합니다.</p></li>
<li><p>연결 그룹에서 선택적 패키지를 제거 하려면 <strong> 연결 그룹 페이지에서 제거 하려는 </strong> 패키지를 선택 하 고 오른쪽 화살표를 클릭 하 여 왼쪽 아래에 있는 연결 그룹 창에서 패키지를 제거 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>독립 실행형 컴퓨터의 app-v 클라이언트</p></td>
<td align="left"><p>다음 기존 cmdlet을 사용 합니다.</p>
<ul>
<li><p>게시 취소-AppvClientPackage</p></li>
<li><p>제거-AppvClientPackage</p></li>
</ul>
<p>자세한 내용은 <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> PowerShell을 사용 하 여 독립 실행형 컴퓨터에서 실행 되는 app-v 5.1 패키지를 관리 하는 방법을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>App-v 5.0 SP3 이전 버전을 사용 하는 경우</strong></p></td>
<td align="left"><p>다음과 같은 작업을 수행 해야 합니다.</p>
<ol>
<li><p>사용 하도록 설정 된 각 App-v 클라이언트 컴퓨터에서 연결 그룹을 제거 합니다.</p></li>
<li><p>패키지 게시를 취소 합니다.</p></li>
<li><p>연결 그룹 정의에서 패키지를 제거 합니다.</p></li>
<li><p>연결 그룹을 다시 게시 합니다.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>연결 그룹에서 선택적 패키지를 사용 하기 위한 요구 사항


연결 그룹에서 선택적 패키지를 사용 하기 전에 다음 요구 사항을 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요구 사항</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>연결 그룹에는 선택 사항 외의 패키지가 하나 이상 포함 되어야 합니다.</p></td>
<td align="left"><ul>
<li><p>App-v 서버와 PowerShell cmdlet이 요구 사항이 충족 되었는지 확인 하지 않으므로이 요구 사항을 충족 하는 것이 신중 하 게 선택 되어 있는지 확인 합니다.</p></li>
<li><p>하나 이상의 선택적 패키지가 포함 되지 않은 연결 그룹을 실수로 만든 경우 최종 사용자가 해당 연결 그룹에서 패키지 된 응용 프로그램을 열려고 하면 연결 그룹이 실패 합니다.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>사용자 게시 된 연결 그룹에는 전역 또는 사용자에 게 게시 되는 패키지가 포함 될 수 있습니다.</p></li>
<li><p>전역 게시 된 연결 그룹에는 전역적으로 게시 된 패키지만 포함 해야 합니다.</p></li>
</ul></td>
<td align="left"><p>연결 그룹의 가상 환경을 시작할 때 패키지를 사용할 수 있도록 전역으로 게시 된 연결 그룹에는 전역으로 게시 되는 패키지가 포함 되어 있어야 합니다.</p>
<p>사용자가 게시 한 패키지를 포함 하는 전역으로 게시 된 연결 그룹을 추가 하거나 사용 하도록 설정 하려고 하면 연결 그룹이 실패 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>해당 패키지가 포함 된 연결 그룹을 게시 하기 전에 모든 비 선택적 패키지를 게시 해야 합니다.</p></td>
<td align="left"><p>선택적 패키지가 없는 경우 연결 그룹의 가상 환경을 시작할 수 없습니다.</p>
<p>선택적 패키지가 게시 되지 않은 경우 App-v 클라이언트에서 연결 그룹을 추가 하거나 사용할 수 있도록 설정 하지 못했습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역적으로 게시 된 패키지를 게시 취소 하기 전에 해당 컴퓨터의 모든 사용자에 게 부여 된 연결 그룹에 더 이상 패키지가 필요 하지 않은지 확인 합니다.</p></td>
<td align="left"><p>시스템이 다른 사용자의 연결 그룹에 속해 있는지 여부를 확인 하지 않습니다. 전역 패키지를 게시 취소 하면 해당 컴퓨터의 모든 사용자가 사용할 수 없게 되므로 각 사용자의 연결 그룹이 더 이상 패키지를 포함 하 고 있지 않은지 확인 하거나 패키지를 선택적으로 만들어야 합니다.</p></td>
</tr>
</tbody>
</table>

 






## 관련 항목


[연결 그룹 관리](managing-connection-groups51.md)

 

 





