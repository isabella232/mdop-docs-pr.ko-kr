---
title: PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법
description: PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813889"
---
# PowerShell을 사용하여 독립 실행형 컴퓨터에서 연결 그룹을 관리하는 방법


App-v 연결 그룹을 사용 하면 모든 가상 응용 프로그램을 단일 가상 환경에서 정의 된 패키지 집합으로 실행할 수 있습니다. 예를 들어 별도의 패키지를 사용 하 여 응용 프로그램 및 플러그 인을 가상화 하 고 단일 연결 그룹에서 함께 실행할 수 있습니다.

연결 그룹 XML 파일은 App-v 클라이언트를 설치한 컴퓨터에서 실행 되는 연결 그룹을 정의 합니다. 연결 그룹 XML 파일과이 파일을 구성 하는 방법에 대 한 자세한 내용은 [연결 그룹 파일](about-the-connection-group-file51.md)정보를 참조 하세요.

이 항목에서는 다음 절차에 대해 설명 합니다.

-   [연결 그룹에 App-v 패키지를 추가 하 고 게시 하려면](#bkmk-add-pub-pkgs-in-cg)

-   [App-v 클라이언트에서 연결 그룹을 추가 하 고 사용 하도록 설정 하려면](#bkmk-add-enable-cg-on-clt)

-   [특정 사용자에 대 한 연결 그룹을 설정 하거나 해제 하려면](#bkmk-enable-cg-for-user-poshtopic)

-   [관리자만 연결 그룹을 사용할 수 있도록 허용 하려면](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>*연결 그룹에 App-v 패키지를 추가 하 고 게시 하려면**

1.  App-v 클라이언트를 실행 하는 컴퓨터에 App-v 5.1 패키지를 추가 하 고 게시 하려면 다음 명령을 입력 합니다.

    추가-AppvClientPackage-path c:\\tmpstore\\quartfin.appv | 게시-AppvClientPackage

2.  연결 그룹의 각 패키지에 대해이 절차의 **1 단계** 를 반복 합니다.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**App-v 클라이언트에서 연결 그룹을 추가 하 고 사용 하도록 설정 하려면**

1.  다음 명령을 입력 하 여 연결 그룹을 추가 합니다.

    추가-AppvClientConnectionGroup – 경로 c:\\tmpstore\\financ.xml

2.  다음 명령을 입력 하 여 연결 그룹을 사용 하도록 설정 합니다.

    Enable-AppvClientConnectionGroup – name "재무 응용 프로그램"

    구성원 패키지에 있는 가상 응용 프로그램이 대상 컴퓨터에서 실행 되는 경우 연결 그룹의 가상 환경 내에서 실행 되며 연결 그룹의 다른 패키지에 있는 모든 가상 응용 프로그램에서 사용할 수 있게 됩니다.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**특정 사용자에 대 한 연결 그룹을 설정 하거나 해제 하려면**

1.  매개 변수 설명 및 요구 사항을 검토 합니다.

    -   관리자는이 매개 변수를 사용 하 여 특정 사용자에 대 한 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.

    -   이 매개 변수를 사용 하려면 App-v 5.0 SP2 핫픽스 패키지 5 이상을 사용 해야 합니다.

    -   사용자 또는 관리자 세션에서이 cmdlet을 실행할 수 있습니다.

    -   매개 변수를 사용 하려면 관리 자격 증명으로 로그인 해야 합니다.

    -   최종 사용자는 로그인 해야 합니다.

    -   최종 사용자의 SID (보안 식별자)를 제공 해야 합니다.

2.  다음 cmdlet을 사용 하 고 선택적 **– usersid** 매개 변수를 추가 합니다. 여기서 **-usersid** 는 최종 사용자의 SID (보안 식별자)를 나타냅니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">예</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Disable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**관리자만 연결 그룹을 사용할 수 있도록 허용 하려면**

1.  이 cmdlet을 사용 하는 데 필요한 설명과 요구 사항을 검토 합니다.

    -   이 cmdlet 및 매개 변수를 사용 하 여 관리자 (최종 사용자가 아님)만 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있도록 App-v 클라이언트를 구성 합니다.

    -   이 cmdlet을 사용 하려면 앱-V 5.0 SP3 이상을 사용 해야 합니다.

2.  다음 cmdlet 및 매개 변수를 실행 합니다.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">매개 변수 및 값</th>
    <th align="left">예</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Set-AppvClientConfiguration</p></td>
    <td align="left"><p>– Require# asadmin</p>
    <ul>
    <li><p>0-거짓</p></li>
    <li><p>1-참</p></li>
    </ul></td>
    <td align="left"><p>Set-AppvClientConfiguration-RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

[PowerShell을 사용하여 App-V 5.1 관리](administering-app-v-51-by-using-powershell.md)









