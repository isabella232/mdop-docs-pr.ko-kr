---
title: PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법
description: PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법
author: dansimp
ms.assetid: 0624495b-943e-485b-9e54-b50e4ee6591c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 7692d3e36aabc4f3142f664e94d9d71b2cfc1bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813956"
---
# PowerShell cmdlet을 로드하고 cmdlet 도움말을 가져오는 방법


이 주제에 대 한 설명:

-   [PowerShell cmdlet 사용에 대 한 요구 사항](#bkmk-reqs-using-posh)

-   [PowerShell cmdlet 로드](#bkmk-load-cmdlets)

-   [PowerShell cmdlet에 대 한 도움말 보기](#bkmk-get-cmdlet-help)

-   [PowerShell cmdlet에 대 한 도움말 표시](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>PowerShell cmdlet 사용에 대 한 요구 사항


App-v PowerShell cmdlet을 사용 하기 위해 다음 요구 사항을 검토 합니다.

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
<td align="left"><p>사용자는 다음 방법 중 하나를 사용 하 여 액세스 권한을 부여한 경우에만 App-v 서버 cmdlet을 실행할 수 있습니다.</p></td>
<td align="left"><ul>
<li><p><strong>App-v 서버를 배포 하 고 구성 하는 경우 </strong> :</p>
<p>Active Directory 그룹 또는 App-v 환경을 관리할 수 있는 권한이 있는 개별 사용자를 지정 합니다. <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">App-v 5.0 서버를 배포 하는 방법을 참조 하세요 </a> .</p></li>
<li><p><strong>App-v 서버를 배포한 후에는 다음을 </strong> 수행 합니다.</p>
<p>앱-V 관리 콘솔을 사용 하 여 추가 Active Directory 그룹 또는 사용자를 추가 합니다. <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)">관리 콘솔을 사용 하 여 관리자를 추가 하거나 제거 하는 방법에 대해 알아봅니다 </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>관리자 권한 명령 프롬프트를 필요로 하는 cmdlet</p></td>
<td align="left"><ul>
<li><p>추가-AppvClientPackage</p></li>
<li><p>제거-AppvClientPackage</p></li>
<li><p>Set-AppvClientConfiguration</p></li>
<li><p>추가-AppvClientConnectionGroup</p></li>
<li><p>제거-AppvClientConnectionGroup</p></li>
<li><p>추가-AppvPublishingServer</p></li>
<li><p>제거-AppvPublishingServer</p></li>
<li><p>송신-AppvClientReport</p></li>
<li><p>Set-AppvClientMode</p></li>
<li><p>Set-AppvClientPackage</p></li>
<li><p>Set-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>관리자 권한 명령 프롬프트를 요구 하도록 구성 하지 않은 경우 최종 사용자가 실행할 수 있는 cmdlet</p></td>
<td align="left"><ul>
<li><p>게시-AppvClientPackage</p></li>
<li><p>게시 취소-AppvClientPackage</p></li>
</ul>
<p>관리자 권한 명령 프롬프트가 필요 하도록 이러한 cmdlet을 구성 하려면 다음 방법 중 하나를 사용 합니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">추가 리소스</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong> </strong> <strong> -RequireAppvClientConfiguration asadmin 매개 변수를 사용 하 여 Set-cmdlet을 실행 합니다 </strong> .</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 클라이언트에 대 한 "관리자 권한으로 게시 필요" 그룹 정책 설정을 사용 하도록 설정 합니다.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">관리 콘솔을 사용하여 패키지를 게시하는 방법</a> </p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>PowerShell cmdlet 로드
PowerShell cmdlet 모듈을 로드 하려면:

1.  Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.

2.  다음 명령 중 하나를 입력 하 여 원하는 모듈에 대 한 cmdlet을 로드 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-v 구성 요소</th>
<th align="left">명령을 입력 합니다.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v Server</p></td>
<td align="left"><p>가져오기-모듈 AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 시퀀서</p></td>
<td align="left"><p>가져오기-모듈 AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 클라이언트</p></td>
<td align="left"><p>가져오기-모듈 AppvClient</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-get-cmdlet-help"></a>PowerShell cmdlet에 대 한 도움말 보기
App-v 5.0 SP3에서 시작 하는 cmdlet 도움말은 두 가지 형식으로 제공 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">형식</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>다운로드 가능한 모듈</p></td>
<td align="left"><p>Cmdlet 모듈을 다운로드 한 후에 최신 도움말을 다운로드 하려면 다음을 수행 합니다.</p>
<ol>
<li><p>Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</p></li>
<li><p>다음 명령 중 하나를 입력 하 여 원하는 모듈에 대 한 cmdlet을 로드 합니다.</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-v 구성 요소</th>
<th align="left">명령을 입력 합니다.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v Server</p></td>
<td align="left"><p>업데이트-도움말-모듈 AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 시퀀서</p></td>
<td align="left"><p>업데이트-도움말-모듈 AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 클라이언트</p></td>
<td align="left"><p>업데이트-도움말-모듈 AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>TechNet에서 웹 페이지로</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Windows PowerShell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화의 앱-V 노드를 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-display-help-cmdlet"></a>PowerShell cmdlet에 대 한 도움말 표시
특정 PowerShell cmdlet에 대 한 도움말을 표시 하려면 다음을 수행 합니다.

1.  Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.

2.  Get-help **Get-Help** &lt; *cmdlet* &gt; 을 입력 합니다 (예: **AppvClientPackage 게시--help)**.

**App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가**있나요? [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

 

 





