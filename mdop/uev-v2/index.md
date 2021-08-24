---
title: Microsoft User Experience Virtualization(UE-V) 2.x
description: Microsoft User Experience Virtualization(UE-V) 2.x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 79748e04ae1a59afdc8f9dae3c5dc77c50e3c253
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910543"
---
# <a name="microsoft-user-experience-virtualization-ue-v-2x"></a>Microsoft User Experience Virtualization(UE-V) 2.x

>[!NOTE]
>이 설명서는 MDOP(Microsoft UE-V 최적화 팩)에 포함된 버전입니다. UE-V 포함된 최신 버전의 Windows 10 Enterprise 에 대한 자세한 내용은 시작 [를 UE-V.](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started)


Microsoft User Experience Virtualization(UE-V) 2.0 또는 Windows 구현하여 사용자의 응용 프로그램 설정을 캡처하고 중앙 집중화합니다. 그런 다음 사용자가 엔터프라이즈에서 액세스하는 장치(예: 데스크톱 컴퓨터, 랩톱 또는 VDI(가상 데스크톱 인프라) 세션)에 이러한 설정을 적용합니다.

**이 UE-V 사용할 수 있습니다.**

-   동기화할 응용 프로그램 및 데스크톱 설정 지정

-   엔터프라이즈 전체에서 사용자가 작업하는 모든 시간과 위치에 설정 제공

-   타사 또는 기간 업무 응용 프로그램의 사용자 지정 템플릿 만들기

-   하드웨어 교체 또는 업그레이드 후 또는 가상 머신을 초기 상태로 다시 구성한 후 설정 복구

## <a name="components-of-ue-v-2x"></a>UE-V 2.x의 구성 요소


이 다이어그램은 배포된 구성 UE-V 함께 작동하여 설정을 동기화하는 방법을 보여줍니다.

![uev2 아키텍처 다이어그램.](images/uev2archdiagram.gif)

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
<td align="left"><p>설정을 동기화해야 하는 모든 컴퓨터에 설치된 UE-V 에이전트는 등록된 응용 프로그램 및 운영 체제에서 설정 변경 내용을 모니터링한 다음 컴퓨터 간에 해당 설정을 <strong> </strong> 동기화합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 패키지</strong></p></td>
<td align="left"><p>응용 프로그램 설정 및 Windows 설정은 에이전트 에이전트에서 만든 설정 <strong> </strong> 패키지에 UE-V 저장됩니다. 설정 패키지가 빌드되어 로컬에 저장되며 설정 저장소 위치에 복사됩니다.</p>
<ul>
<li><p>데스크톱 응용 프로그램의 설정 값은 사용자가 응용 <strong> </strong> 프로그램을 닫을 때 저장됩니다.</p></li>
<li><p>Windows 설정 값은 사용자가 로그오프하거나 컴퓨터가 잠겨 있는 경우 또는 사용자가 컴퓨터에서 원격으로 연결을 끊을 때 <strong> </strong> 저장됩니다.</p></li>
</ul>
<p>동기화 공급자는 응용 프로그램 또는 운영 체제 설정을 패키지에서 읽고 동기화하는 설정 <strong> </strong> 확인합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>설정 저장소 위치</strong></p></td>
<td align="left"><p>사용자가 액세스할 수 있는 표준 네트워크 공유입니다. 이 UE-V 에이전트는 위치를 확인하여 사용자 설정을 저장하고 검색할 숨겨진 시스템 폴더를 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 위치 템플릿</strong></p></td>
<td align="left"><p>UE-V XML 파일을 설정 위치 템플릿으로 사용하여 데스크톱 응용 프로그램 설정을 모니터링하고 동기화하고 사용자 컴퓨터 간에 Windows 설정을 동기화합니다. 기본적으로 일부 설정 위치 템플릿은 에 UE-V. 사용자 지정 응용 프로그램에 대한 설정 동기화를 관리하여 사용자 지정 설정 위치 템플릿을 만들거나 편집하거나 유효성을 <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> 검사할 수도 </a> 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>설정 앱의 경우 위치 템플릿이 Windows 없습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows 목록</strong></p></td>
<td align="left"><p>설정 앱에 Windows 캡처 및 적용됩니다. 앱 개발자는 각 앱에 대해 동기화된 설정을 지정합니다. UE-V 관리되는 Windows 사용하여 설정 동기화를 사용할 수 있는 앱을 확인합니다. 기본적으로 이 목록에는 대부분의 Windows 포함됩니다.</p>
<p>여기에 표시된 절차에 따라 Windows 앱 목록에서 응용 프로그램을 추가하거나 제거할 수 <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> 있습니다.</p></td>
</tr>
</tbody>
</table>



### <a name="managing-settings-synchronization-for-custom-applications"></a><a href="" id="customapps"></a>사용자 지정 설정 동기화 관리

이러한 UE-V 구성 요소를 사용하여 타사 또는 업무용 응용 프로그램에 대한 사용자 지정 템플릿을 만들고 관리합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V 생성기</strong></p></td>
<td align="left"><p>UE-V 생성기를 사용하여 사용자 컴퓨터에 배포할 수 있는 사용자 지정 설정 위치 <strong> </strong> 템플릿을 만듭니다. 또한 UE-V 생성기를 사용하여 기존 템플릿을 편집하거나 다른 XML 편집기를 사용하여 만든 템플릿의 유효성을 검사할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 템플릿 카탈로그</strong></p></td>
<td align="left"><p>설정 템플릿 카탈로그는 사용자 지정 설정 위치 UE-V 저장하는 SMB(서버 메시지 블록) 네트워크 공유의 폴더 <strong> </strong> 경로입니다. 이 UE-V 에이전트는 이 위치를 확인하고, 새 서식 파일 또는 업데이트된 서식 파일을 검색하고, 동기화 동작을 업데이트합니다.</p>
<p>기본 설정 UE-V 템플릿만 사용하는 경우 설정 템플릿 카탈로그가 필요하지 않습니다. 설정 배포 카탈로그에 대한 자세한 내용은 <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> Configure a UE-V settings template catalog을 </a> 참조하십시오.</p></td>
</tr>
</tbody>
</table>



![ue-v 생성기 프로세스.](images/ue-vgeneratorprocess.gif)

## <a name="settings-synchronized-by-default"></a>설정 기본적으로 동기화


UE-V 응용 프로그램의 설정을 기본적으로 동기화합니다. 전체 목록 및 자세한 내용은 설정 배포에서 자동으로 동기화되는 UE-V [참조하세요.](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)

Microsoft Office 2013 응용 프로그램(UE-V 2.1 SP1 및 2.1)

Microsoft Office 2010 응용 프로그램(UE-V 2.1 SP1, 2.1 및 2.0)

Microsoft Office 2007 응용 프로그램(UE-V 2.0만 해당)

Internet Explorer 8, 9 및 10

Internet Explorer 2.1 SP1 UE-V 2.1의 11

많은 Windows 응용 프로그램(예: Xbox)

대부분의 Windows 데스크톱 응용 프로그램(예: 메모장

바탕 Windows 배경 무늬와 같은 여러 설정

**참고**  
또한 [기본적으로](https://technet.microsoft.com/library/dn458942.aspx) 동기화되는 UE-V 응용 프로그램에 대한 설정을 동기화하기 위해 사용자 지정할 수도 있습니다.



## <a name="compare-ue-v-to-other-microsoft-products"></a>다른 UE-V Microsoft 제품 비교


다음 표를 사용하여 UE-V 7의 프로필 동기화, Windows 프로필 동기화, Windows 8 Microsoft 계정의 PC 동기화 설정 비교합니다.

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
<th align="left">7을 사용하여 프로필 Windows 동기화</th>
<th align="left">프로필을 사용하여 프로필 Windows 8</th>
<th align="left">프로필을 사용하여 프로필 Windows 10</th>
<th align="left">Microsoft 계정</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 및 2.1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>여러 컴퓨터 간에 설정 동기화</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>실제 앱과 가상 앱 간의 설정 동기화</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱 Windows 동기화</p></td>
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
<td align="left"><p>정기적으로 설정 변경 동기화</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>설치에 대한 최소 구성</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>도메인에 가입되지 않은 컴퓨터에서 지원</p></td>
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
<td align="left"><p>VDI(가상 데스크톱 인프라)/원격 데스크톱 서비스(RDS)와 리치 데스크톱 간의 설정 동기화</p></td>
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
<td align="left"><p>동기화할 앱 설정 선택</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>IT 작업용 백업/Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>부분</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## <a name="ue-v-2x-release-notes"></a>UE-V 2.x 릴리스 정보


자세한 내용은 설명서에 추가하지 않은 늦은 속보를 참조하세요.

-   [Microsoft User Experience Virtualization(UE-V) 2.1 SP1 릴리스 정보](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Microsoft User Experience Virtualization(UE-V) 2.1 릴리스 정보](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <a name="other-resources-for-this-product"></a>이 제품에 대한 기타 리소스


-   [UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

-   [UE-V 2.x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [2.UE-V 관리](administering-ue-v-2x-new-uevv2.md)

-   [2.UE-V 문제 해결](troubleshooting-ue-v-2x-both-uevv2.md)

-   [UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)

### <a name="more-information"></a>추가 정보

<a href="" id="mdop-techcenter-page"></a>[MDOP TechCenter 페이지](https://go.microsoft.com/fwlink/p/?LinkId=225286) 최신 MDOP 정보 및 리소스에 대해 자세히 알아보습니다.

<a href="" id="mdop-information-experience"></a>[MDOP 정보 환경](https://go.microsoft.com/fwlink/p/?LinkId=236032) MDOP 기술에 대한 설명서, 비디오 및 기타 리소스를 찾아 보세요. Facebook 또는 Twitter에서 [피드백을](mailto:MDOPDocs@microsoft.com) 보내거나 업데이트에 대해 자세히 [알아보는](https://go.microsoft.com/fwlink/p/?LinkId=242445) 방법을 사용할 수도 [있습니다.](https://go.microsoft.com/fwlink/p/?LinkId=242447)














