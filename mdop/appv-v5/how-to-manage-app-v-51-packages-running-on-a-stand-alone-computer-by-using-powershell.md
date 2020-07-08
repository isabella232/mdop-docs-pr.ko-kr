---
title: PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.1 패키지를 관리하는 방법
description: PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.1 패키지를 관리하는 방법
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813916"
---
# PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.1 패키지를 관리하는 방법


다음 섹션에서는 PowerShell을 사용 하 여 독립 실행형 클라이언트 컴퓨터에서 다양 한 관리 작업을 수행 하는 방법을 설명 합니다.

-   [패키지 목록을 반환 하려면](#bkmk-return-pkgs-standalone-posh)

-   [패키지를 추가 하려면](#bkmk-add-pkgs-standalone-posh)

-   [패키지 게시](#bkmk-pub-pkg-standalone-posh)

-   [특정 사용자에 게 패키지를 게시 하려면](#bkmk-pub-pkg-a-user-standalone-posh)

-   [패키지를 추가 하 고 게시 하려면](#bkmk-add-pub-pkg-standalone-posh)

-   [기존 패키지의 게시를 취소 하려면](#bkmk-unpub-pkg-standalone-posh)

-   [특정 사용자에 대 한 패키지의 게시를 취소 하려면](#bkmk-unpub-pkg-specfc-use)

-   [기존 패키지를 제거 하려면](#bkmk-remove-pkg-standalone-posh)

-   [관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면](#bkmk-admins-pub-pkgs)

-   [보류 중인 패키지 이해 (UserPending 및 GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>패키지 목록을 반환 하려면


다음 정보를 사용 하 여 특정 사용자에 게 부여 되는 패키지 목록을 반환 합니다.

**Cmdlet**: Get-AppvClientPackage

**매개 변수**:-Name-Version-PackageID-이름

**예**: Get-help – Name "ContosoApplication"-Version 2 AppvClientPackage

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>패키지를 추가 하려면


다음 정보를 사용 하 여 패키지를 컴퓨터에 추가 합니다.

**중요**  이 예제에서는 패키지만 추가 합니다. 사용자 또는 컴퓨터에 패키지를 게시 하지는 않습니다.

 

**Cmdlet**: Add-AppvClientPackage

**예**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>패키지 게시


다음 정보를 사용 하 여 특정 사용자에 게 추가 된 패키지 또는 컴퓨터의 모든 사용자에 게 전역적으로 게시할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">게시 방법</th>
<th align="left">Cmdlet 및 예제</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자에 게 게시</p></td>
<td align="left"><p><strong>Cmdlet </strong> : 게시-AppvClientPackage</p>
<p><strong>예 </strong> : Publish-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 게시</p></td>
<td align="left"><p><strong>Cmdlet </strong> : 게시-AppvClientPackage</p>
<p><strong>예 </strong> : 게시-AppvClientPackage "ContosoApplication"-Global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>특정 사용자에 게 패키지를 게시 하려면


**참고**  이 매개 변수를 사용 하려면 App-v 5.0 SP2 핫픽스 패키지 5 이상을 사용 해야 합니다.

 

관리자는 **AppvClientPackage** cmdlet을 사용 하 여 Optional **– usersid** 매개 변수를 지정 하 여 특정 사용자에 게 패키지를 게시할 수 있습니다. 여기서 **-USERSID** 는 최종 사용자의 SID (보안 식별자)를 나타냅니다.

이 매개 변수를 사용 하려면:

-   사용자 또는 관리자 세션에서이 cmdlet을 실행할 수 있습니다.

-   매개 변수를 사용 하려면 관리 자격 증명으로 로그인 해야 합니다.

-   최종 사용자는 로그인 해야 합니다.

-   최종 사용자의 SID (보안 식별자)를 제공 해야 합니다.

**Cmdlet**: 게시-AppvClientPackage

**예**: 게시-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>패키지를 추가 하 고 게시 하려면


다음 정보를 사용 하 여 패키지를 컴퓨터에 추가 하 고 사용자에 게 게시 합니다.

**Cmdlet**: Add-AppvClientPackage

**예**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | 게시-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>기존 패키지의 게시를 취소 하려면


다음 정보를 사용 하 여 사용자에 게 자격이 있는 패키지를 게시 취소 하지만 컴퓨터에서 패키지를 제거할 수는 없습니다.

**Cmdlet**: 게시 취소-AppvClientPackage

**예**: 게시 취소-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>특정 사용자에 대 한 패키지의 게시를 취소 하려면


**참고**  이 매개 변수를 사용 하려면 App-v 5.0 SP2 핫픽스 패키지 5 이상을 사용 해야 합니다.

 

관리자는 **AppvClientPackage** cmdlet을 사용 하 여 Optional **– usersid** 매개 변수를 사용 하 여 특정 사용자에 대 한 패키지를 게시 취소할 수 있으며, 여기서 **-USERSID** 는 최종 사용자의 SID (보안 식별자)를 나타냅니다.

이 매개 변수를 사용 하려면:

-   사용자 또는 관리자 세션에서이 cmdlet을 실행할 수 있습니다.

-   매개 변수를 사용 하려면 관리 자격 증명으로 로그인 해야 합니다.

-   최종 사용자는 로그인 해야 합니다.

-   최종 사용자의 SID (보안 식별자)를 제공 해야 합니다.

**Cmdlet**: 게시 취소-AppvClientPackage

**예**: 게시 취소-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>기존 패키지를 제거 하려면


다음 정보를 사용 하 여 컴퓨터에서 패키지를 제거 합니다.

**Cmdlet**: Remove-AppvClientPackage

**예**: Remove-AppvClientPackage "ContosoApplication"

**참고**  위의 예제에서 명확 하 게만 사용할 수 있도록 app-v cmdlet이 변수에 할당 되었습니다. 과제는 요구 사항이 아닙니다. 대부분의 cmdlet은에 표시 된 대로 결합 [하 여 패키지를 추가 하 고 게시할](#bkmk-add-pub-pkg-standalone-posh)수 있습니다. 자세한 자습서는 [app-v 5.0 클라이언트 PowerShell 딥](https://go.microsoft.com/fwlink/?LinkId=324466)을 참조 하세요.

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면


**참고** 
 **이 기능은 app-v 5.0 SP3에서 시작 하는 것으로 지원 됩니다.**

 

다음 cmdlet 및 매개 변수를 사용 하 여 패키지를 게시 하거나 게시 취소 하는 관리자 (최종 사용자 아님)만 사용 하도록 설정 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cmdlet</strong></p></td>
<td align="left"><p>Set-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>매개 변수</strong></p></td>
<td align="left"><p>-Require# asadmin</p>
<p>매개 변수 값:</p>
<ul>
<li><p>0-거짓</p></li>
<li><p>1-참</p></li>
</ul>
<p><strong>예: </strong> : Set-AppvClientConfiguration-RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

앱-V 관리 콘솔을 사용 하 여이 구성을 설정 하려면 [관리 콘솔을 사용 하 여 패키지를 게시 하는 방법을](how-to-publish-a-package-by-using-the-management-console-51.md)참조 하세요.

## <a href="" id="bkmk-understd-pend-pkgs"></a>보류 중인 패키지 이해 (UserPending 및 GlobalPending)


**App-v 5.0 SP2에서 시작**: 현재 사용 중인 패키지에 영향을 주는 PowerShell cmdlet을 실행 하는 경우 수행 하려는 작업이 보류 상태로 전환 됩니다. 예를 들어 해당 패키지의 응용 프로그램을 사용 중인 경우 패키지를 게시 하려고 하면 **AppvClientPackage**를 실행 하 고 다음과 같이 보류 상태를 cmdlet 출력에 표시 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet 출력 항목</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>UserPending</p></td>
<td align="left"><p>나열 된 패키지에 사용자에 게 적용 되는 보류 중인 작업이 있는지 여부를 나타냅니다.</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>나열 된 패키지에 컴퓨터에 전역적으로 적용 되는 보류 중인 작업이 있는지 여부를 나타냅니다.</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

보류 중인 작업은 다음 규칙에 따라 나중에 실행 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 종류</th>
<th align="left">해당 규칙</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업 (예: 패키지를 사용자에 게 게시)</p></td>
<td align="left"><p>보류 중인 작업은 사용자가 로그 오프 한 다음 다시 로그온 하면 수행 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업 (예: 연결 그룹을 전역적으로 사용 가능)</p></td>
<td align="left"><p>보류 중인 작업은 컴퓨터를 종료 한 후 다시 시작 하면 수행 됩니다.</p></td>
</tr>
</tbody>
</table>

 

보류 중인 작업에 대 한 자세한 내용은 [앱-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks)정보를 참조 하세요.

**App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

[PowerShell을 사용하여 App-V 5.1 관리](administering-app-v-51-by-using-powershell.md)

 

 





