---
title: App-V 5.1 시작
description: App-V 5.1 시작
author: dansimp
ms.assetid: 49a20e1f-0566-4e53-a417-1521393fc974
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff10f12bc672a24f2837f50bfb1f0033ede3e46f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814548"
---
# App-V 5.1 시작


Microsoft App-v (Application Virtualization) 5.1를 사용 하면 관리자가 응용 프로그램을 필요한 기준에 따라 실시간으로 서비스를 서비스로 배포, 업데이트 및 지원할 수 있습니다. 개별 응용 프로그램은 로컬로 설치 된 제품에서 중앙 관리 서비스로 변환 되며 컴퓨터를 미리 구성 하거나 운영 체제 설정을 변경할 필요 없이 필요할 때마다 사용할 수 있습니다.

App-v는 다음 요소로 구성 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 관리 서버</p></td>
<td align="left"><ul>
<li><p>App-v 데스크톱 클라이언트와 원격 데스크톱 서비스 (이전의 터미널 서비스) 클라이언트 모두에 가상 응용 프로그램을 제공 하는 App-v 인프라를 관리할 수 있는 중앙 위치를 제공 합니다.</p></li>
<li><p>하나 이상의 App-v 관리 서버가 단일 SQL Server 데이터 저장소를 공유할 수 있는 데이터 저장소에 대해 Microsoft SQL Server®를 사용 합니다.</p></li>
<li><p>요청을 인증 하 고 보안, 계량, 모니터링, 데이터 수집을 제공 합니다. 서버는 Active Directory 및 지원 도구를 사용 하 여 사용자 및 응용 프로그램을 관리 합니다.</p></li>
<li><p>모든 컴퓨터에서 앱-V 인프라를 구성할 수 있는 관리 사이트를 보유 합니다. 응용 프로그램을 추가 및 제거 하 고, 바로 가기를 조작 하 고, 사용자 및 그룹에 대 한 액세스 권한을 할당 하 고, 연결 그룹을 만들 수 있습니다.</p></li>
<li><p>App-v 웹 관리 콘솔과 SQL Server 데이터 저장소 간의 통신을 사용 하도록 설정 합니다. 이러한 구성 요소는 필요한 시스템 아키텍처에 따라 단일 서버 컴퓨터 또는 하나 이상의 개별 컴퓨터에 모두 설치할 수 있습니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 게시 서버</p></td>
<td align="left"><ul>
<li><p>특정 사용자를 위한 응용 프로그램을 사용 하 여 App-v 클라이언트 제공</p></li>
<li><p>스트리밍을 위한 가상 응용 프로그램 패키지를 호스팅합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 데스크톱 클라이언트</p></td>
<td align="left"><ul>
<li><p>가상 응용 프로그램 검색</p></li>
<li><p>클라이언트에 응용 프로그램 게시</p></li>
<li><p>Windows 끝점의 런타임에 가상 환경을 자동으로 설정 하 고 관리 합니다.</p></li>
<li><p>레지스트리와 파일 변경 등의 사용자 특정 가상 응용 프로그램 설정을 각 사용자&#39;s 프로필에 저장 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 원격 데스크톱 서비스 (RDS) 클라이언트</p></td>
<td align="left"><p>원격 데스크톱 세션 호스트 서버에서 공유 데스크톱 세션에 대 한 App-v 데스크톱 클라이언트의 기능을 사용할 수 있도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 시퀀서</p></td>
<td align="left"><ul>
<li><p>기존 응용 프로그램을 가상 응용 프로그램으로 변환 하는 데 사용 하는 마법사 기반 도구입니다.</p></li>
<li><p>다음과 같이 구성 된 "package" 응용 프로그램을 생성 합니다.</p>
<ol>
<li><p>APPV (시퀀싱 된 응용 프로그램) 파일</p></li>
<li><p>독립 실행형 작업을 위해 구성 된 클라이언트에 배포할 수 있는 MSI (Windows Installer 파일)</p></li>
<li><p>Report.XML, PackageName_DeploymentConfig.XML 및 PackageName_UserConfig.XML을 비롯 한 여러 XML 파일 UserConfig 및 DeploymentConfig XML 파일은 패키지의 기본 동작에 대 한 사용자 지정 변경을 구성 하는 데 사용 됩니다.</p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

이러한 요소에 대 한 자세한 내용은 [앱-V 5.1의 상위 수준 아키텍처](high-level-architecture-for-app-v-51.md)를 참조 하세요.

이 제품을 처음 사용할 경우에는 문서를 철저히 읽어 보는 것이 좋습니다. 프로덕션 환경에 배포 하기 전에 테스트 네트워크 환경에서 배포 계획의 유효성을 검사 하는 것이 좋습니다. 관련 기술에 대 한 수업을 할 수도 있습니다. Microsoft 교육 기회에 대 한 자세한 내용은의 Microsoft 교육 개요를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**참고**  이 관리자 가이드의 다운로드 가능한 버전을 사용할 수 없습니다. 그러나 문서를 선택 하 고, 컬렉션에서 그룹화 하 고, 인쇄 하거나, 파일 ()에 파일로 내보내는 기능을 제공 하는 TechNet 라이브러리의 특별 한 모드에 대해 배울 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=272491> https://go.microsoft.com/fwlink/?LinkId=272491) .

 

앱-V 5.1 관리자 가이드의이 섹션에서는 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 이해를 제공 하기 위해 App-v 5.1에 대 한 상위 수준의 정보를 포함 합니다.

## 앱 시작-V 5.1


-   [App-V 5.1 정보](about-app-v-51.md)

    앱-V 5.1에 대 한 간략 한 개요와 조직에서 사용할 수 있는 방법에 대해 설명 합니다.

-   [App-V 5.1 평가](evaluating-app-v-51.md)

    조직에서 사용할 앱-V 5.1을 최적화 하는 방법에 대 한 정보를 제공 합니다.

-   [App-V 5.1의 개략적인 아키텍처](high-level-architecture-for-app-v-51.md)

    App-v 5.1 기능에 대 한 설명과 함께 작동 하는 방식에 대해 설명 합니다.

-   [App-V 5.1의 접근성](accessibility-for-app-v-51.md)

    장애가 있는 사용자가이 제품 및 해당 문서에 더욱 쉽게 액세스할 수 있도록 하는 기능 및 서비스에 대 한 정보를 제공 합니다.

## <a href="" id="other-resources-for-this-product-"></a>이 제품에 대 한 기타 리소스


-   [Microsoft Application Virtualization 5.1 관리자 가이드](microsoft-application-virtualization-51-administrators-guide.md)

-   [App-V 5.1 계획](planning-for-app-v-51.md)

-   [App-V 5.1 배포](deploying-app-v-51.md)

-   [App-V 5.1 작업](operations-for-app-v-51.md)

-   [App-V 5.1 문제 해결](troubleshooting-app-v-51.md)

-   [App-V 5.1에 대한 기술 참조](technical-reference-for-app-v-51.md)






 

 





