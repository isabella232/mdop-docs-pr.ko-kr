---
title: Microsoft UE-V (User Experience Virtualization) 2. x
description: Microsoft UE-V (User Experience Virtualization) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795970"
---
# Microsoft UE-V (User Experience Virtualization) 2. x

>[!NOTE]
>이 설명서는 MDOP (Microsoft 데스크톱 최적화 팩)에 포함 된 for UE-V for 버전입니다. Windows 10 Enterprise에 포함 되어 있는 최신 버전의 UE-V에 대 한 자세한 내용은 [Ue-v 시작](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started)을 참조 하세요.


UE-V (사용자 환경 가상화) 2.0 또는 2.1을 구현 하 여 사용자의 응용 프로그램 설정 및 Windows OS 설정을 캡처하고 중앙 집중화할 수 있습니다. 그런 다음 데스크톱 컴퓨터, 랩톱 또는 VDI (가상 데스크톱 인프라) 세션과 같은 사용자의 엔터프라이즈 액세스 장치에 이러한 설정을 적용 합니다.

**UE-V를 사용 하 여 다음을 수행할 수 있습니다.**

-   동기화 할 응용 프로그램 및 데스크톱 설정 지정

-   엔터프라이즈 전체에서 사용자가 작업하는 모든 시간과 위치에 설정 제공

-   타사 또는 기간 업무 응용 프로그램의 사용자 지정 템플릿 만들기

-   하드웨어를 대체 하거나 업그레이드 한 후 또는 가상 컴퓨터를 초기 상태로 reimaging 후에 설정 복구

## UE-V 2. x의 구성 요소


이 다이어그램은 배포 된 UE-V 구성 요소가 함께 작동 하 여 설정을 동기화 하는 방법을 보여 줍니다.

![uev2 아키텍처 다이어그램](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">구성 요소</th>
<th align="left">함수</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V 에이전트</strong></p></td>
<td align="left"><p>설정을 동기화 해야 하는 모든 컴퓨터에 설치 되어 있는 경우 <strong> Ue-v agent가 </strong> 설정 변경에 대해 등록 된 응용 프로그램 및 운영 체제를 모니터링 한 다음 해당 설정을 컴퓨터 간에 동기화 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 패키지</strong></p></td>
<td align="left"><p>응용 프로그램 설정 및 Windows 설정은 <strong> Ue-v agent에서 만든 설정 패키지에 저장 됩니다 </strong> . 설정 패키지가 빌드되어 로컬에 저장되며 설정 저장소 위치에 복사됩니다.</p>
<ul>
<li><p>데스크톱 응용 프로그램에 대 한 설정 값은 <strong> </strong> 사용자가 응용 프로그램을 닫을 때 저장 됩니다.</p></li>
<li><p>Windows 설정에 대 한 값 <strong> </strong> 은 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있거나 컴퓨터에서 원격으로 연결이 끊어질 때 저장 됩니다.</p></li>
</ul>
<p>동기화 공급자는 설정 패키지에서 응용 프로그램 또는 운영 체제 설정을 읽고 동기화 할 때를 결정 <strong> </strong> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>설정 저장소 위치</strong></p></td>
<td align="left"><p>사용자가 액세스할 수 있는 표준 네트워크 공유입니다. UE-V Agent는 위치를 확인 하 고 사용자 설정을 저장 하 고 검색할 숨겨진 시스템 폴더를 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 위치 템플릿</strong></p></td>
<td align="left"><p>UE-V는 XML 파일을 설정 위치 템플릿으로 사용 하 여 데스크톱 응용 프로그램 설정 및 사용자 컴퓨터 간에 Windows 데스크톱 설정을 모니터링 하 고 동기화 합니다. 기본적으로 일부 설정 위치 템플릿은 UE-V에 포함 되어 있습니다. <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">사용자 지정 응용 프로그램의 설정 동기화를 관리 하 여 사용자 지정 설정 위치 템플릿을 만들거나 편집 하거나 유효성을 검사할 수도 있습니다 </a> .</p>
<div class="alert">
<strong>참고</strong><br/><p>Windows 앱에는 설정 위치 템플릿이 필요 하지 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows 앱 목록</strong></p></td>
<td align="left"><p>Windows 앱에 대 한 설정이 동적으로 캡처되고 적용 됩니다. 앱 개발자는 각 앱에 대해 동기화 되는 설정을 지정 합니다. UE-V는 관리 되는 앱 목록을 사용 하 여 설정 동기화를 사용 하도록 설정 된 Windows 앱을 결정 합니다. 기본적으로이 목록에는 대부분의 Windows 앱이 포함 되어 있습니다.</p>
<p>다음 절차에 따라 Windows 앱 목록에서 응용 프로그램을 추가 하거나 제거할 수 있습니다 <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>사용자 지정 응용 프로그램의 설정 동기화 관리

이러한 UE-V 구성 요소를 사용 하 여 타사 또는 lob (기간 업무) 응용 프로그램에 대 한 사용자 지정 템플릿을 만들고 관리할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V 생성기</strong></p></td>
<td align="left"><p><strong> </strong> 사용자 컴퓨터에 배포할 수 있는 사용자 지정 설정 위치 템플릿을 만들려면 ue-v 생성기를 사용 합니다. 또한 UE-V 생성기를 통해 기존 서식 파일을 편집 하거나 다른 XML 편집기를 사용 하 여 만든 서식 파일의 유효성을 검사할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 서식 파일 카탈로그</strong></p></td>
<td align="left"><p><strong>설정 템플릿 카탈로그는 </strong> ue-v 컴퓨터의 폴더 경로 이거나 사용자 지정 설정 위치 템플릿을 저장 하는 SMB (서버 메시지 블록) 네트워크 공유입니다. UE-V Agent가 하루에 한 번이 위치를 확인 하 고, 새 템플릿 또는 업데이트 된 템플릿을 검색 하 고, 동기화 동작을 업데이트 합니다.</p>
<p>UE-V 기본 설정 위치 템플릿만 사용 하는 경우 설정 템플릿 카탈로그는 필요 하지 않습니다. 설정 배포 카탈로그에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> ue-v 설정 템플릿 카탈로그 구성을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>



![ue-v 생성자 프로세스](images/ue-vgeneratorprocess.gif)

## 설정이 기본적으로 동기화 됨


UE-V는 기본적으로 이러한 응용 프로그램에 대 한 설정을 동기화 합니다. 전체 목록 및 자세한 내용은 [ue-v 배포에서 자동으로 동기화 되는 설정을](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)참조 하세요.

Microsoft Office 2013 응용 프로그램 (UE-V 2.1 SP1 및 2.1)

Microsoft Office 2010 응용 프로그램 (UE-V 2.1 SP1, 2.1 및 2.0)

Microsoft Office 2007 응용 프로그램 (UE-V 2.0에만 해당)

Internet Explorer 8, 9, 10

Internet Explorer 11 (UE-V 2.1 SP1 및 2.1)

Xbox와 같은 대부분의 Windows 응용 프로그램

여러 Windows 데스크톱 응용 프로그램 (예: 메모장)

바탕 화면 배경 또는 배경 무늬 등의 다양 한 Windows 설정

**참고**  
기본적으로 동기화 되지 않은 응용 프로그램에 대 한 [설정을 동기화 하도록 ue-v를 사용자 지정할](https://technet.microsoft.com/library/dn458942.aspx) 수도 있습니다.



## UE-V를 다른 Microsoft 제품과 비교


이 표를 사용 하 여 Windows 7에서 UE-V를 비교 하 고, Windows 8의 프로필을 동기화 하 고, Microsoft 계정의 동기화 PC 설정 기능을 변경 합니다.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">기능</th>
<th align="left">Windows 7을 사용 하 여 프로필 동기화</th>
<th align="left">Windows 8을 사용 하 여 프로필 동기화</th>
<th align="left">Windows 10을 사용 하 여 프로필 동기화</th>
<th align="left">Microsoft 계정</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 및 2.1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>여러 컴퓨터 간 설정 동기화</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>실제 및 가상 앱 간에 설정 동기화</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 앱 설정 동기화</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>WMI를 통해 관리</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정 변경 내용을 정기적으로 동기화</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>최소 설치 구성</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>비도메인 가입 컴퓨터에서 지원</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>기본 컴퓨터 Active Directory 특성 지원</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>VDI (가상 데스크톱 인프라)에서 RDS (/Remote 데스크톱 서비스) 및 리치 데스크톱 간의 설정을 동기화 합니다.</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>무제한 설정 저장소 공간</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>동기화 할 앱 설정을 선택 합니다.</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>IT 전문가를 위한 백업/복원</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>부분</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## UE-V 2. x 릴리스 정보


이 문서에 대 한 자세한 내용 및 최신 뉴스를 보려면 다음을 참조 하세요.

-   [Microsoft User Experience Virtualization(UE-V) 2.1 SP1 릴리스 정보](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Microsoft User Experience Virtualization(UE-V) 2.1 릴리스 정보](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## 이 제품에 대 한 기타 리소스


-   [UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

-   [UE-V 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

-   [UE-V 2. x 문제 해결](troubleshooting-ue-v-2x-both-uevv2.md)

-   [UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)

### 추가 정보

<a href="" id="mdop-techcenter-page"></a>[MDOP TechCenter 페이지](https://go.microsoft.com/fwlink/p/?LinkId=225286) 최신 MDOP 정보 및 리소스에 대해 알아보세요.

<a href="" id="mdop-information-experience"></a>[MDOP 정보 환경](https://go.microsoft.com/fwlink/p/?LinkId=236032) MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다. [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 팔 로우 하 여 [피드백을 보내거나](mailto:MDOPDocs@microsoft.com) 업데이트에 대 한 정보를 확인할 수도 있습니다.














