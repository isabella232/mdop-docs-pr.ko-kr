---
title: 이전 버전에서 마이그레이션
description: 이전 버전에서 마이그레이션
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813556"
---
# 이전 버전에서 마이그레이션


App-v 5.0를 사용 하면 기존 App-v 4.6 인프라를 보다 유연 하 고 통합 하 고 보다 쉽게 앱-V 5.0 인프라를 관리할 수 있습니다.

마이그레이션 전략을 계획할 때는 다음 섹션을 고려 하세요.

**참고**  App-v 4.6 및 App-v 5.0 간의 차이점에 대 한 자세한 내용은 [app-v 5.0에 대 한](about-app-v-50.md)앱- **v 4.6 및 app-v 5.0 섹션의 차이점** 을 참조 하세요.

 

## 이전 버전의 App-v를 사용 하 여 만든 패키지 변환


패키지 변환기 유틸리티를 사용 하 여 이전 버전의 App-v를 사용 하 여 만든 가상 응용 프로그램 패키지를 업그레이드 합니다. 패키지 변환기는 PowerShell을 사용 하 여 패키지를 변환 하며 변환이 필요한 패키지가 여러 개 있는 경우 프로세스를 자동화 하는 데 도움이 될 수 있습니다.

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
<td align="left"><p>패키지 스크립트는 변환 되지 않습니다.</p></td>
<td align="left"><p>변환 된 패키지를 테스트 합니다. 필요한 경우 스크립트를 변환 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 레지스트리 설정 재정의가 변환 되지 않습니다.</p></td>
<td align="left"><p>변환 된 패키지를 테스트 합니다. 필요한 경우 레지스트리 재정의를 다시 추가 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DSC를 사용 하는 가상 패키지는 변환 후 연결 되지 않습니다.</p></td>
<td align="left"><p>연결 그룹을 사용 하 여 패키지를 연결 합니다. <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">연결 그룹 관리를 참조 하세요 </a> .</p></td>
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

 

패키지를 변환할 때 파일 또는 바로 가기가 실패 했는지 확인 합니다. 앱-V 4.6 패키지에서 항목을 찾습니다. 경로를 하드 코드화 할 수도 있습니다. 경로를 변환 합니다.

**참고**  기능을 활용 해야 하는 중요 한 응용 프로그램 또는 응용 프로그램을 변환 하는 데 App-v 5.0 sequencer를 사용 하는 것이 좋습니다. [앱-V 5.0를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법을](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)참조 하세요.

변환 후 변환 된 패키지가 열리지 않는 경우 App-v 5.0 sequencer를 사용 하 여 응용 프로그램을 다시 시퀀싱 하는 것이 좋습니다.

 

[이전 버전의 App-V에서 만든 패키지를 변환하는 방법](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

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
<td align="left"><p>환경을 앱-V 4.6 SP2로 업그레이드</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>공존을 사용 하도록 설정 된 App-v 5.0 클라이언트를 설치 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">앱-V 4.6 및 App-v 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법을 설명 </a> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱-V 5.0 패키지 순서 및 롤아웃 필요에 따라 App-v 4.6 패키지의 게시를 취소 합니다.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">앱-V 5.0를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법 </a></p></td>
</tr>
</tbody>
</table>

 

**중요**  공존 모드를 사용 하려면 App-V 4.6 SP3을 실행 중 이어야 합니다. 또한 패키지를 시퀀싱 하는 경우 **사용자 구성 섹션** **에 설정** 되어 있는 관리 권한 설정을 구성 해야 합니다.

 

## App-v 5.0 서버 전체 인프라 마이그레이션


전체 App-v 5.0 인프라로 업그레이드 하는 직접적인 방법은 없습니다. App-v server를 업그레이드 하는 방법에 대 한 자세한 내용은 다음 섹션의 정보를 사용 하세요.

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
<td align="left"><p>환경을 App-v 4.6 SP3으로 업그레이드 합니다.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 5.0 버전의 클라이언트를 배포 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">App-v 클라이언트를 배포 하는 방법 </a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 5.0 서버를 설치 합니다.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">App-v 5.0 서버를 배포 하는 방법 </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>기존 패키지 마이그레이션.</p></td>
<td align="left"><p><strong>이 문서의 이전 버전의 app-v 섹션을 사용 하 여 만든 패키지 변환을 참조 하세요 </strong> .</p></td>
</tr>
</tbody>
</table>

 

## 추가 마이그레이션 작업


또한 끝점 재구성, 그리고 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 이전 버전을 사용 하 여 만든 패키지를 여는 등의 추가 마이그레이션 작업을 수행할 수도 있습니다. 다음 링크는 이러한 작업을 수행 하는 방법에 대 한 자세한 정보를 제공 합니다.

[특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[특정 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## 앱-V 마이그레이션 작업을 수행 하기 위한 기타 리소스


[App-V 5.0 작업](operations-for-app-v-50.md)

[간단한 Microsoft App-v 5.1 관리 서버 업그레이드 절차](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





