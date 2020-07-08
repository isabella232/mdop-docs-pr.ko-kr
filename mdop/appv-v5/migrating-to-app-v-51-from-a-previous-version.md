---
title: 이전 버전에서 App-V 5.1로 마이그레이션
description: 이전 버전에서 App-V 5.1로 마이그레이션
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813553"
---
# 이전 버전에서 App-V 5.1로 마이그레이션


Microsoft Application Virtualization (App-v) 5.1를 사용 하 여 기존 App-v 4.6 또는 App-v 5.0 인프라를 보다 유연 하 고 통합 하 고 앱-v 5.1 인프라를 더 쉽게 관리할 수 있습니다.
그러나 앱-V 4. x에서 App-v 5.1으로 직접 마이그레이션할 수는 없으며 먼저 App-v 5.0로 마이그레이션해야 합니다. App-v 4. x에서 App-v 5.0으로 마이그레이션하는 방법에 대 한 자세한 내용은 [이전 버전에서 마이그레이션을](migrating-from-a-previous-version-app-v-50.md) 참조 하세요.  

**참고**  App-v 5.1 패키지는 앱-v 5.0 패키지와 정확히 동일 합니다. 버전 간에 패키지 형식이 변경 되지 않았으므로 app-v 5.0 패키지를 App-v 5.1 패키지로 변환할 필요는 없습니다 .이 문제가 발생 합니다.

App-v 4.6 및 App-v 5.1 간의 차이점에 대 한 자세한 내용은 [app-v 5.0에 대 한](about-app-v-50.md)앱- **v 4.6 및 app-v 5.0 섹션의 차이점** 을 참조 하세요.

 

## <a href="" id="bkmk-pkgconvimprove"></a>앱-V 5.1 패키지 변환기의 향상 된 기능


이제 패키지 변환기를 사용 하 여 스크립트를 포함 하는 App-v 4.6 패키지를 변환할 수 있으며, 이제 원본 osd 파일의 레지스트리 정보와 스크립트가 패키지 변환기 출력에 포함 됩니다.

또한 cmdlet에 매개 변수를 사용 하 여 `–OSDsToIncludeInPackage` `ConvertFrom-AppvLegacyPackage` 변환 되는 osd 파일의 정보를 지정 하 고 새 패키지 내에 배치할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">앱의 새로운 기능-V 5.1</th>
<th align="left">앱-V 5.1 이전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>패키지와 연결 된 .osd 파일에 해당 하는 새 .xml 파일이 만들어집니다. 이러한 파일에는 다음 정보가 포함 됩니다.</p>
<ul>
<li><p>환경 변수</p></li>
<li><p>정의</p></li>
<li><p>파일 형식 연결</p></li>
<li><p>레지스트리 정보</p></li>
<li><p>문자</p></li>
</ul>
<p>이제 매개 변수를 사용 하 여 원본 디렉터리에 있는 .osd 파일의 하위 집합에 있는 정보를 패키지에 추가 하도록 선택할 수 있습니다 <code>-OSDsToIncludeInPackage</code> .</p></td>
<td align="left"><p>패키지와 연결 된 osd 파일에 포함 된 레지스트리 정보와 스크립트는 패키지 변환기 출력에 포함 되어 있지 않습니다.</p>
<p>패키지 변환기는 원본 디렉터리에 있는 모든 .osd 파일의 정보로 새 패키지를 채웁니다.</p></td>
</tr>
</tbody>
</table>

 

### 예제 변환 문

새 프로세스를 이해 하려면 다음 예제 `ConvertFrom-AppvLegacyPackage` package converter 문을 검토 하세요.

**원본 디렉터리 (\\\\OldPkgStore\\ContosoApp)에 다음이 포함 된 경우:**

-   ContosoApp. sft

-   ContosoApp.msi

-   ContosoApp.sprj

-   ContosoApp\_manifest.xml

-   X. osd

-   Y osd

-   Z. i a osd

**다음 명령을 실행 합니다.**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**대상 디렉토리 (\\\\NewPkgStore\\ContosoApp)에서 다음이 생성 됩니다.**

-   ContosoApp

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**위의 예제에서 다음을 수행 합니다.**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">다음 원본 디렉터리 파일 ...</th>
<th align="left">... 이러한 대상 디렉터리 파일로 변환 됩니다.</th>
<th align="left">... 그리고 다음 항목이 포함 됩니다.</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. osd</p></li>
<li><p>Y osd</p></li>
<li><p>Z. i a osd</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>환경 변수</p></li>
<li><p>정의</p></li>
<li><p>파일 형식 연결</p></li>
<li><p>레지스트리 정보</p></li>
<li><p>스크립트</p></li>
</ul></td>
<td align="left"><p>각 .osd 파일은 앱-V 5.1 배포 구성 형식에 나열 된 항목을 포함 하는 별도의 해당 .xml 파일로 변환 됩니다. 이러한 항목은 이러한 .xml 파일에서 복사 하 여 원하는 대로 배포 구성 또는 사용자 구성 파일에 배치할 수 있습니다.</p>
<p>이 예제에는 원본 디렉터리에 있는 세 개의 .osd 파일에 해당 하는 세 개의 .xml 파일이 있습니다. 각 .xml 파일에는 환경 변수, 바로 가기, 파일 형식 연결, 레지스트리 정보 및 해당 .osd 파일의 스크립트가 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. osd</p></li>
<li><p>Y osd</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>환경 변수</p></li>
<li><p>정의</p></li>
<li><p>파일 형식 연결</p></li>
</ul></td>
<td align="left"><p>매개 변수에 지정 된 .osd 파일의 정보는 <code>-OSDsToIncludeInPackage</code> 변환 되어 패키지 내에 배치 됩니다. 그런 다음 새 패키지를 시퀀싱 하는 경우 앱-V 시퀀서와 마찬가지로 배포 구성 파일과 사용자 구성 파일을 패키지의 내용으로 채웁니다.</p>
<p>이 예제에서는 X. osd 및 Y osd에 포함 된 환경 변수, 바로 가기 및 파일 형식 연결을 변환 하 여 App-v 패키지에 배치 했으며 이러한 정보 중 일부는 배포 구성 및 사용자 구성 파일에도 포함 되었습니다. 이 매개 변수는 인수로 포함 되기 때문에 X. osd 및 Y osd가 사용 되었습니다 <code>-OSDsToIncludeInPackage</code> . 이 인수 중 하나로 포함 되지 않았으므로 Z.e.n.works의 정보는 패키지에 포함 되어 있지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

## 이전 버전의 App-v를 사용 하 여 만든 패키지 변환


패키지 변환기 유틸리티를 사용 하 여 앱-V 5.0 이전 버전의 app-v를 사용 하 여 만든 가상 응용 프로그램 패키지를 업그레이드 합니다. 패키지 변환기는 PowerShell을 사용 하 여 패키지를 변환 하며 변환이 필요한 패키지가 여러 개 있는 경우 프로세스를 자동화 하는 데 도움이 될 수 있습니다.

**중요**  기존 패키지를 변환한 후에는 패키지를 배포 하기 전에 패키지를 테스트 하 여 변환 프로세스가 성공적으로 수행 되었는지 확인 해야 합니다.

 

**기존 패키지를 변환 하기 전에 알아야 할 사항**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">문제</th>
<th align="left">해결 방법</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DSC를 사용 하는 가상 패키지는 변환 후 연결 되지 않습니다.</p></td>
<td align="left"><p>연결 그룹을 사용 하 여 패키지를 연결 합니다. <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">연결 그룹 관리를 참조 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>환경 변수 충돌은 변환 중에 검색 됩니다.</p></td>
<td align="left"><p>관련 된 .osd 파일의 모든 충돌을 해결 <strong> </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>변환 하는 동안 하드 코드 된 경로가 감지 됩니다.</p></td>
<td align="left"><p>하드 코드 된 경로는 제대로 변환 하기가 어렵습니다. 패키지 변환기는 하드 코드 된 경로가 들어 있는 파일을 사용 하 여 패키지를 감지 하 고 반환 합니다. 하드 코드 된 경로를 사용 하 여 파일을 보고 패키지에 파일이 필요한 지 여부를 결정 합니다. 그렇다면 패키지를 다시 시퀀싱 하는 것이 좋습니다.</p></td>
</tr>
</tbody>
</table>

 

패키지를 변환할 때 파일 또는 바로 가기가 실패 했는지 확인 합니다. 앱-V 4.6 패키지에서 항목을 찾습니다. 하드 코딩 된 경로일 수도 있습니다. 경로를 변환 합니다.

**참고**  기능을 활용 해야 하는 중요 한 응용 프로그램 또는 응용 프로그램을 변환 하는 데 App-v 5.1 sequencer를 사용 하는 것이 좋습니다. [앱-V 5.1를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법을](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)참조 하세요.

변환 후 변환 된 패키지가 열리지 않는 경우 App-v 5.1 sequencer를 사용 하 여 응용 프로그램을 다시 시퀀싱 하는 것이 좋습니다.

 

[이전 버전의 App-V에서 만든 패키지를 변환하는 방법](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## 클라이언트 마이그레이션


다음 표에서는 클라이언트 업그레이드에 권장 되는 방법을 보여 줍니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>환경을 최신 버전의 App-V 4.6으로 업그레이드</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>공존을 사용 하도록 설정 된 App-v 5.1 클라이언트를 설치 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">앱-V 4.6 및 App-v 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법을 설명 </a> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱-V 5.1 패키지 순서 및 롤아웃 필요에 따라 App-v 4.6 패키지의 게시를 취소 합니다.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">앱-V 5.1를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법 </a></p></td>
</tr>
</tbody>
</table>

 

**중요**  공존 모드를 사용 하려면 최신 버전의 App-V 4.6을 실행 해야 합니다. 또한 패키지를 시퀀싱 하는 경우 **사용자 구성 섹션** **에 설정** 되어 있는 관리 권한 설정을 구성 해야 합니다.

 

## App-v 5.1 서버 전체 인프라 마이그레이션


전체 App-v 5.1 인프라로 업그레이드 하는 직접적인 방법은 없습니다. App-v server를 업그레이드 하는 방법에 대 한 자세한 내용은 다음 섹션의 정보를 사용 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>환경을 최신 버전인 App-v 4.6으로 업그레이드 합니다.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 5.1 버전의 클라이언트를 배포 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">App-v 클라이언트를 배포 하는 방법 </a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 5.1 서버를 설치 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">App-v 5.1 서버를 배포 하는 방법 </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>기존 패키지 마이그레이션.</p></td>
<td align="left"><p><strong>이 문서의 이전 버전의 app-v 섹션을 사용 하 여 만든 패키지 변환을 참조 하세요 </strong> .</p></td>
</tr>
</tbody>
</table>

 

## 추가 마이그레이션 작업


또한 끝점 재구성, 그리고 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 이전 버전을 사용 하 여 만든 패키지를 여는 등의 추가 마이그레이션 작업을 수행할 수도 있습니다. 다음 링크는 이러한 작업을 수행 하는 방법에 대 한 자세한 정보를 제공 합니다.

[특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.1 패키지로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.1로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[특정 컴퓨터의 모든 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[특정 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## 앱-V 마이그레이션 작업을 수행 하기 위한 기타 리소스


[App-V 5.1 작업](operations-for-app-v-51.md)

[간단한 Microsoft App-v 5.1 관리 서버 업그레이드 절차](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





