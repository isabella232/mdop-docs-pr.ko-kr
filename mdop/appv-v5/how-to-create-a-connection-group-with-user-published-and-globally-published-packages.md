---
title: 사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법
description: 사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814353"
---
# 사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법
다음 방법 중 하나를 사용 하 여 사용자가 게시 하 고 전역적으로 게시 된 패키지를 모두 포함 하는 사용자 관련 연결 그룹을 만들 수 있습니다.

-   [PowerShell cmdlet을 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법](#bkmk-posh-userentitled-cg)

-   [App-v 서버를 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법](#bkmk-appvserver-userentitled-cg)

**시작 하기 전에 알아야 할 사항:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">지원 되지 않는 시나리오 및 잠재적인 문제</th>
<th align="left">결과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 게시 패키지는 전역으로 제공 되는 연결 그룹에 포함할 수 없습니다.</p></td>
<td align="left"><p>연결 그룹이 작동 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지를 전역적으로 게시 한 다음 해당 패키지를 선택 하지 않은 사용자가 게시 한 연결 그룹을 만드는 경우, <strong> &lt; &gt; 다른 연결 그룹에서 해당 패키지를 사용 하는 경우에도 게시 취소-AppvClientPackage 패키지-전역 </strong> 을 실행 하 여 패키지를 게시 취소할 수 있습니다.</p></td>
<td align="left"><p>다른 연결 그룹이 해당 패키지를 사용 하는 경우 해당 연결 그룹에서 패키지가 실패 합니다.</p>
<p>다른 연결 그룹에서 사용 중인 비 선택적 패키지의 게시를 실수로 취소 하지 않도록 하려면 선택 사항 이외의 패키지를 사용한 연결 그룹을 추적 하는 것이 좋습니다.</p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**PowerShell cmdlet을 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법**

1.  다음 명령을 사용 하 여 패키지를 추가 하 고 게시 합니다.

    **추가-AppvClientPackage Package1 \ _AppV \ _file \ _Path**

    **추가-AppvClientPackage Package2 \ _AppV \ _file \ _Path**

    **게시-AppvClientPackage-PackageId Package1 \ _ID--~ Package1 \ _Version ID-전역**

    **게시-AppvClientPackage-PackageId Package2 \ _ID-VersionIdPackage2 \ _ID**

2.  연결 그룹 XML 파일을 만듭니다. 자세한 내용은 [연결 그룹 파일 정보](about-the-connection-group-file.md)를 참조 하세요.

3.  다음 명령을 사용 하 여 연결 그룹을 추가 하 고 게시 합니다.

    **추가-AppvClientConnectionGroup 연결 \ _Group \ _XML \ _file \ _Path**

    **Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**App-v 서버를 사용 하 여 사용자에 게 부여 된 연결 그룹을 만드는 방법**

1.  App-v 5.0 관리 콘솔을 엽니다.

2.  [관리 콘솔을 사용](how-to-publish-a-package-by-using-the-management-console-50.md) 하 여 패키지를 게시 하는 방법의 지침에 따라 패키지를 전역 및 사용자에 게 게시 합니다.

3.  연결 [그룹을 만드는 방법](how-to-create-a-connection-group.md) 의 지침에 따라 연결 그룹을 만들고 사용자가 게시 하 고 전역적으로 게시 된 패키지를 추가 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[연결 그룹 관리](managing-connection-groups.md)

[연결 그룹에서 선택적 패키지를 사용하는 방법](how-to-use-optional-packages-in-connection-groups.md)

 

 





