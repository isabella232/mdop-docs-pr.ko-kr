---
title: 연결 그룹 가상 환경 정보
description: 연결 그룹 가상 환경 정보
author: dansimp
ms.assetid: 535fa640-cbd9-425e-8437-94650a70c264
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bd93c9e7acbf7bbf3f9da506d5d95b8df09e1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814908"
---
# 연결 그룹 가상 환경 정보


**이 항목의 내용:**

-   [패키지 우선 순위를 결정 하는 방법](#bkmk-pkg-priority-deter)

-   [연결 그룹의 하나의 가상 디렉터리에 동일한 패키지 경로 병합](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a>패키지 우선 순위를 결정 하는 방법


가상 환경과 해당 현재 상태는 개별 패키지가 아닌 연결 그룹과 연결 되어 있습니다. 연결 그룹에서 앱-V 패키지를 제거 하면 연결 그룹의 일부로 존재 하는 상태가 패키지와 함께 마이그레이션되지 않습니다.

동일한 패키지가 두 개의 다른 연결 그룹에 속해 있는 경우 app-v에서 사용할 연결 그룹을 표시 해야 합니다. 예를 들어 연결 그룹에는 각각 동일한 레지스트리 DWORD 값을 정의 하는 두 개의 패키지가 있을 수 있습니다.

사용 되는 연결 그룹은 **Appconnectiongroup** XML 문서 내에서 패키지가 표시 되는 순서에 따라 달라 집니다.

-   첫 번째 패키지의 우선 순위가 가장 높습니다.

-   두 번째 패키지의 우선 순위가 가장 높습니다.

다음 예제 섹션을 참조 하세요.

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

다음과 같이 첫 번째 및 세 번째 패키지에 동일한 DWORD 값 ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region)가 정의 되어 있다고 가정 합니다.

-   패키지 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5

-   패키지 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10

Package 1이 먼저 표시 되므로 AppConnectionGroup의 가상 환경은 단일 DWORD 값이 5 (HKEY _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5)입니다. 즉, 패키지 1, 패키지 2 및 패키지 3의 가상 응용 프로그램이 HKEY \ _LOCAL \ _MACHINE에 대해 쿼리하면 5 값이 모두 표시 됨을 의미 합니다. \\software\\contoso\\finapp\\region.

다른 가상 환경 리소스도 비슷하게 해결 되지만, 일반적인 경우는 레지스트리에서 충돌이 발생 하는 것입니다.

## <a href="" id="bkmk-merged-root-ve-exp"></a>연결 그룹의 하나의 가상 디렉터리에 동일한 패키지 경로 병합


연결 그룹에 있는 둘 이상의 패키지에 동일한 디렉터리 경로가 포함 된 경우 경로가 연결 그룹 가상 환경 내의 단일 가상 디렉터리로 병합 됩니다. 이러한 경로 병합을 통해 한 패키지의 응용 프로그램이 다른 패키지의 파일에 액세스할 수 있습니다.

연결 그룹에서 패키지를 제거 하면 제거 된 해당 패키지의 응용 프로그램이 연결 그룹의 나머지 패키지에 있는 파일에 액세스할 수 없습니다.

앱이 연결 그룹에서 파일 이름을 찾는 순서는 연결 그룹 매니페스트 파일에 앱 V 패키지가 나열 되는 순서 대로 지정 되어 있습니다.

다음 예제에서는 **패키지 a** 및 **패키지 B**의 연결 그룹에 있는 파일 이름 조회의 순서와 관계를 보여 줍니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">패키지 A</th>
<th align="left">패키지 B</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\ \ \</p></td>
<td align="left"><p>\ \ \</p></td>
</tr>
<tr class="even">
<td align="left"><p>C:\AppTest</p></td>
<td align="left"><p>C:\AppTest</p></td>
</tr>
</tbody>
</table>

 

위 예제에서 가상화 된 응용 프로그램이 특정 파일을 찾으려고 하면 먼저 패키지 A가 일치 하는 파일 경로를 검색 합니다. 일치 하는 경로를 찾을 수 없는 경우 다음 매핑 규칙을 사용 하 여 패키지 B를 검색 합니다.

-   두 응용 프로그램 패키지의 동일한 가상 폴더 계층 구조에 **test.txt** 이라는 파일이 있는 경우 첫 번째 일치 파일이 사용 됩니다.

-   하나의 응용 프로그램 패키지의 가상 폴더 계층 구조에 **bar.txt** 이라는 이름의 파일이 있지만 다른 파일에는 없는 경우에는 일치 하는 첫 번째 파일이 사용 됩니다.






## 관련 항목


[연결 그룹 관리](managing-connection-groups.md)

 

 





